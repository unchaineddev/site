+++
title = 'Integrate Umami on your Hugo Site'
date = 2024-04-04T06:50:07+05:30
draft = false
tags = ['web', 'technology']
+++


I always sought after an open-source solution for web analytics primarily to track visitor counts on my site. While I used Google Analytics for 
a few months due to its seamless integration with Hugo, it was without a doubt contradicting to my ethical principles.

So starting today, this site will be using umami[^1] for web analytics. I opted umami because it is open-source, privacy-focused and the setup takes less than 10 minutes! 
Here's how you can integrate it in your website --


## Prerequisites

1. A working Hugo Site
2. [Umami Account](https://umami.is/)


## Set Up

{{% steps %}}

### Locate the Base Template File

In Hugo, the base template file is either `baseof.html` or `base.html`. 

You can find this typically in `layouts/_default/baseof.html`


### Find the Head Section

If you don't find the `<head>` tag in `base.html`, look for a `head.html` file in your `partials/` folder.

Inside the head section, you need to add the script tag which was generated after you created your umami account.


```javscript
<script async src="https://example.com/path/to/script.js" data-website-id="a1a11aaa1-a1a1a1a-a1a1a1a1-a1a1a1a1"></script>
```

{{% /steps %}}


Save the changes and rebuild your Hugo site. Voila, umami is analyzing traffic.. unagi!


[^1]: https://umami.is/
