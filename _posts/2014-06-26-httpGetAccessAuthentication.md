---
layout: post
title: "HTTP GET 方法的简单访问效验"
description: ""
category: Web
tags: []
---

### 情景 ###

有这样一个获取数据的接口，此接口需要效验合法性，如果效验通过则返回正确数据。

****

### 解决方案 ###

自定义一套签名算法，接口和请求者使用签名算法一致，并使用一致的 token。请求接口时将签名结果作为必要参数，接口收到请求效验签名合法性。

****

### 代码 ###

接口定义

	{% highlight python %}
    print('dddd')
	{% endhighlight %}

    private bool CheckTimeOut(string timestamp)
    {
        var result = default(bool);
        var now = int.Parse(SignatureHelper.CreateTimestamp());
        int time;
        if (int.TryParse(timestamp, out time))
        {
            // 超过30秒网页就过期
            if (now - time >= 30)
            {
                result = false;
                LogHelper.Log("网页过期");
            }
            else
            {
                result = true;
            }
        }
        else
        {
            result = false;
        }
        return result;
    }

接口定义

	[config] brush:csharp; first-line:10; highlight:[11,12]
    [HttpGet]
    public string GetData(string signature, string timestamp, string nonce)
    {
        var result = string.Empty;
        var token = "wangwenzhuang";
        if (!string.IsNullOrEmpty(token))
        {
            // 可以检测时间是否超时
            if (CheckTimeOut(timestamp))
            {
                if (CheckSignature(token, signature, timestamp, nonce))
                {
                    result = "我是测试数据";
                }
            }
        }
        return result;
    }
