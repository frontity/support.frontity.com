# Google Tag Manager

* [**Introduction**](./#introduction)
* [**Create a new container**](./#create-container)
* [**Install Universal Analytics**](./#install-ua)
* [**Next steps**](./#next-steps)

## Introduction {#introduction}

If you want to use **Google Tag Manager** \(**GTM**\) to manage your analytics services, here you can find how to integrate it with our GTM events.

Our PWA currently supports the following types of events:

* [**Virtual Pageviews**](google-tag-manager-pageviews.md)
* [**Virtual Events**](google-tag-manager-events.md)

For us to be able to assume what your GTM container looks like while following this guide, you'll need to **create a new GTM container** from zero and install **Universal Analytics** \(**UA**\) as indicated in this guide. This way, you'll avoid interferences between the PWA configuration and any other setup you may have in your GTM. However, if you know what you are doing, feel free to integrate it in the way that better suits your needs.

## Create a new container {#create-container}

1. In the **accounts** view of your GTM, click the menu button for the account you want to use, and then click **Create Container**.

![](../../.gitbook/assets/gtm_create_container.png)

2. Now type a name for your container in the field under the label **Container name**, choose **Web** in the **Where To Use Container** option and click the **CREATE** button.

![](../../.gitbook/assets/gtm_create_container_setup.png)

3. You'll see now a modal telling you how to install GTM on your site. You shouldn't worry about this, as Frontity is taking care of it for you. Click the **OK** button to finish the container creation process.

![](../../.gitbook/assets/gtm_accept_modal.png)

## Install Universal Analytics {#install-ua}

Now that you have your new GTM container, you'll need to install **Universal Analytics**. For that, follow these steps:

1. Create a new **variable** clicking on the **Variables** button in the side menu and then on the **NEW** button in the **User-Defined Variables** panel.

![](../../.gitbook/assets/gtm_install_ua_new_variable.png)

2. Name your variable and click the big button above the **Choose a variable type to begin setup...** label.

![](../../.gitbook/assets/gtm_install_ua_name_variable.png)

3. Choose the **Constant** type.

![](../../.gitbook/assets/gtm_install_ua_choose_variable_type.png)

4. Type your **UA Property ID** in the **Value** field and click the **SAVE** button.

![](../../.gitbook/assets/gtm_install_ua_save_variable.png)

5. Now create a new **tag** clicking on the **Tags** button in the side menu and then on the **NEW** button.

![](../../.gitbook/assets/gtm_install_ua_new_tag.png)

6. Name your tag and click the big button above the **Choose a tag type to begin setup...** label.

![](../../.gitbook/assets/gtm_install_ua_open_tag_type_menu.png)

7. Choose the **Custom HTML** type.

![](../../.gitbook/assets/gtm_install_ua_choose_tag_type.png)

8. Copy and paste in the **HTML** field the following snippet:

```javascript
<script>
  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
  })(window,document,'script','https://www.google-analytics.com/analytics.js','ga');

  ga('create', {{UA Property ID}}, 'auto', 'mySite');
  ga('mySite.set', 'checkProtocolTask', null);
  ga('mySite.set', 'transportUrl', 'https://www.google-analytics.com/collect');
</script>
```

As you can see in the snippet above, there are three places where you can find the string `mySite`. You should replace this string with your site's name. For example, in our case instead of `mySite` and `mySite.set` we would write `frontity` and `frontity.set`.

![](../../.gitbook/assets/gtm_install_ua_tag_configuration_1.png)

9. Click **Advanced Settings**. Then click the **Tag firing options** dropdown menu and choose the _Once per page_ option.

![](../../.gitbook/assets/gtm_install_ua_tag_configuration_advanced.png)

10. Click the big icon above the **Choose a trigger to make this tag fire...** label.

![](../../.gitbook/assets/gtm_install_ua_tag_configuration_open_trigger.png)

11. Choose the **All Pages** trigger.

![](../../.gitbook/assets/gtm_install_ua_choose_trigger.png)

12. Click the **SAVE** button.

![](../../.gitbook/assets/gtm_install_ua_save.png)

Now you have installed Universal Analytics in your GTM container.

## Next steps {#next-steps}

Now that you have your new container and Universal Analytics installed, you'll have to configure them to work with our GTM events:

* [**Virtual Pageviews**](google-tag-manager-pageviews.md)
* [**Virtual Events**](google-tag-manager-events.md)

