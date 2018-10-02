# How to move to HTTPS

## What is SSL / HTTPS?

SSL \(Secure Socket Layer\) is a cryptographic protocol to provide security over internet communications and protect data being transferred through a computer network.

Sites' URLs that are encrypted using SSL begin with **HTTPS** \(Hypertext Transfer Protocol Secure\) instead of HTTP. This connection ensures maximum security and privacy for the visitors and site data as they do not get exposed to attacks and other vulnerabilities.

In addition, Google takes note of HTTPS and SSL in their search ranking algorithms. That is, they are a **ranking factor** in search results.

Progressive Web Apps are served over HTTPS too. This means that if your site is not encrypted using SSL we **cannot guarantee** that it will properly work with our solution.

## How to add a free SSL certificate in WordPress and move to HTTPS

Some WordPress hosting providers offer free SSL certificates with their plans. But if this is not your case, and you don't want to buy a third party certificate, we recommend setting up a **free SSL certificate** from **CloudFlare**.

To do so, you can **follow this guide**: [How to Setup CloudFlare Flexible SSL for WordPress](https://jonnyjordan.com/blog/how-to-setup-cloudflare-flexible-ssl-for-wordpress/).

{% hint style="warning" %}
**Important**: read the information below about CloudFlare Flexible SSL before taking any steps.
{% endhint %}

> _"Flexible SSL encrypts traffic from Cloudflare to end users of your website, but not from Cloudflare to your origin server. This is the easiest way to enable HTTPS because it doesn’t require installing an SSL certificate on your origin. While not as secure as the other options, Flexible SSL does protect your visitors from a large class of threats including public WiFi snooping and ad injection over HTTP."_ - More info at [https://www.cloudflare.com/en/ssl/](https://www.cloudflare.com/en/ssl/).

