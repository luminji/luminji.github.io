<!DOCTYPE html>
<html>
  <head>
    <meta http-equiv="content-type" content="text/html; charset=utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>{{ page.title }}</title>
    <link rel="fluid-icon" href="/fluidicon.png" />
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-114.png" />
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114.png" />
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-144.png" />
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144.png" />
    <link rel="icon" type="image/x-icon" href="/favicon.ico" />
    <link rel="stylesheet" href="/bootstrap-3.0.3/css/bootstrap.min.css" />
    <link rel="stylesheet" href="/css/style.css" />
    <script src="/js/jquery-2.1.1.min.js"></script>
    <script src="/bootstrap-3.0.3/js/bootstrap.min.js"></script>
  </head>
  <body>
    <div>
      {% include navigation.md %}
    </div>
    <div class="container content">
      {{ content }}
    </div>
    <div class="container footer">
      {% include footer.md %}
    </div>
  </body>
</html>
