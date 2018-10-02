# Ads.txt

Ads.txt stands for Authorized Digital Sellers and is a method for publishers and distributors to declare who is authorized to sell their ad inventory. You can learn more about it [here](https://iabtechlab.com/ads-txt/).

## 1. How to implement ads.txt for Google ads

> Jump directly to [step two](ads-txt.md#2-including-our-entry-in-your-adstxt-file) if you already have an ads.txt file.

**Please note**: these steps only describe how to create an ads.txt file for Google ads. You can also refer to Google's guide [here](https://support.google.com/dfp_premium/answer/7441288?).

1. Create a text \(.txt\) file.
2. If you have an AdSense, DoubleClick for Publishers \(DFP\), or Ad Exchange account managed by yourself \(not through a third party\), **include** the following **line**:

   `google.com, pub-0000000000000000, DIRECT, f08c47fec0942fa0`

   **⚠️ Important:** you must replace `pub-0000000000000000` with your own **publisher ID**. [Here's where to find it](ads-txt.md#where-to-find-your-publisher-id).

3. Host your ads.txt on your root domain \(for example: [https://www.example.com/ads.txt](https://www.example.com/ads.txt)\). If you're not sure how to do this, [this plugin](ads-txt.md#adstxt-manager-wordpress-plugin) will help.

If you monetize through multiple Ad Exchange and/or AdSense accounts, you must include a separate row for each account, with its corresponding `pub-` code.

## 2. Including our entry in your ads.txt file

In order to allow us to [use one ad placement](../../useful-information/business-model.md) on your website, you have to include our publisher information in the ads.txt file by adding the following line:

### `google.com, pub-6240751379550204, DIRECT, f08c47fec0942fa0`

> **⚠️ Important:** even though your site is verified by Google AdSense to display ads, you must include your publisher information in the ads.txt file.

## Where to find your Publisher ID

Your publisher ID is your AdSense, DoubleClick for Publishers \(DFP\), or Ad Exchange account ID. This ID is in the format of `pub-0000000000000000` with the zeros replaced by your own 16 digit number.

* In **AdSense**: Sign in to your [AdSense account](https://www.google.es/adsense/), then click Settings &gt; Account &gt; Account information.
* In **DFP**: Sign in to [DoubleClick for Publishers](https://google.com/dfp), then click Admin &gt; Global settings to find the publisher ID of your [primary Ad Exchange account](https://support.google.com/dfp_premium/answer/188529#primary-vs-linked) and any other linked accounts.
* In **Ad Exchange**: Sign in to your [Ad Exchange account](https://www.google.com/adx), then click Admin &gt; Account information.

## Ads.txt Manager \(WordPress Plugin\)

If you are not sure how to host your ads.txt file at the root level of your domain you can install the [Ads.txt Manager plugin](https://wordpress.org/plugins/ads-txt/). It will help you create, manage, and **automatically validate** your ads.txt from within WordPress.

The validation baked into the plugin helps avoid malformed records, which can cause issues that can lead to a drop in ad revenue.

After installing and activating the Ads.txt Manager plugin:

1. Go to **Settings** \(from your WordPress dashboard\) &gt; **Ads.txt**
2. Add the lines / entries you need
3. Save changes
4. Check it out at _www.yoursite.com/ads.txt_.

