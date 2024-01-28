---
title: "custom domain for github pages"
date: 2023-09-26T08:16:04+05:30
draft: false
tags: ['web']
---

There are far more problems in the world than setting up a custom domain. it's ridiculous how a simple thing is made so complicated that any new user would break their head trying to make it work. 

in this blog, i will share how to set up a custom domain using github pages.

<center>
{{< figure src="/blog/custom-domain.jpg" width="500px" >}}
</center>


i already had github pages[^1] set up, and i bought a domain from hostinger. if you haven't purchased a domain, you can get it [here](https://hostinger.in/?REFERRALCODE=1YUSUFTECHI58),  and if you are lazy to create a static page on your own, you can use one of these [templates](https://html5up.net/).


## Step 1 

Deploying your page to github. 

- if you need help, you can refer the [docs](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site). 
it's pretty straight-forward.


## Step 2

Sign in to your domain.

- Go to your domain's home page. for hostinger domains go to: _[hpanel](https://hpanel.hostinger.com/)_
- Under domains, choose the domain you want to set the custom domain to by clicking on "__Manage__"
- On the left panel, click on "__DNS/Nameservers__" to configure the CNAME and A records.


## Step 3

Now this is the tricky part where most of the misconfiguration happens.

- If you find any existing "CNAME" records or "A records", **delete** them


## Step 4

Adding _CNAME and A records_

- <ins>__CNAME__</ins> -- There must be 2 CNAME records, and both records must point to 'your-github-username.github.io'

    * First CNAME record must have 'www'
    * Second CNAME record must be left blank

After saving both CNAME records, the result should look like this.

<center>
{{< figure src="/blog/add-records.png" width="500px" >}} 
</center>


- <ins>__A Records__</ins> -- There are 4 github IPs we need to add to our A records, 
and they are as follows:

<center>
185.199.108.153<br>
185.199.109.153<br>
185.199.110.153<br>
185.199.111.153
</center>


After saving all the A records, the result should look like this.

<center>
{{< figure src="/blog/a-records.png" width="500px" >}} 
</center>


## Step 5 

Add the custom domain to your github.io page.

- Head to your GitHub repository and click on the __Settings__ tab. 
- Then, click on the __Pages__ tab and enter your custom domain in the __Custom Domain__ field --> Hit __Save__
- Wait for 15 mins for the TLS cert to be generated. 


And just like that, you have set up your custom domain to GitHub Pages!

[^1]: https://pages.github.com/

