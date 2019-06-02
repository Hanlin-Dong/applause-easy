# Applause-Easy.js
An easy-to-use browser applause button.
DEMO: http://www.hanlindong.com

## Background
In personal websites, the site owners what to have a insight of the readers' interests. Sometimes, a 'thumbup & thumbdown' button is added to the website. However, these buttons can only be clicked once. To obtain a basic way to let readers express to what extent do they love this website or article, infinite times of a 'thumbup-like' button should be created. Therefore, the applause-easy button is provided for this purpose.

## Features
- It creates a button with the sum number of applause given in the past;
- Readers can click the button infinite times;
- on every certain times click, a user-defined function is triggered;
- Use features provided by [Animate.css](https://daneden.github.io/animate.css/);
- Inspired by an outstanding project [Valine](https://valine.js.org/);
- Users should deploy it manually to LeanCloud; It's easy, and free.

## Useage
First, download the files `applause-easy.js` & `av.min.js`, add `script` tag to your webpage.

``` html
<script src="av.min.js"></script>
<script src="applause-easy.js"></script>
```

Also, the Animate.css style sheet. You can use CDN like

``` html
<link href="https://cdn.bootcss.com/animate.css/3.7.0/animate.min.css" rel="stylesheet">
```

Then, inside `<body>`, create your own `<div>` with a prefered id.

``` html
<div id="applause-key"></div>
```

Next, add some script.

``` html
<script>
  new ApplauseEasy({
    id: 'applause-easy',
    appId: 'your-own-app-ID',
    appKey: 'your-own-app-Key',
    img_src: 'url-for-your-clap-img',
    img_width: '50px',
    img_height: '50px',
    trigger_every: 10,
    trigger_fun: function() {
        alert("Function is triggered.");
    }
  })
</script>
```

To get the appID and appKey, you have to log in [LeanCloud](https://leancloud.cn), and create an app.

If you are a [Valine](https://valine.js.org/) comment module user, you can use the same app with Valine.

In your app, please create a new Class named 'Applause'. Allow anyone to read and write. Otherwise, this widget will not work. Please add a site url whitelist in order to improve security.

A clap image is provided in this repository, you should download it and link to it with `img_src`. You can use any image with url as you wish. A square image is recommended.

Now, everything is done. Enjoy!
