# Compatibility

## Does Frontity support my WordPress site?

Frontity supports **blog posts** and **pages**.

For example, any news site, magazine or blog such as [blog.frontity.com](https:/blog.frontity.com/). As you can see, it has categories, authors, galleries, menus, featured images, tags, sharing buttons, etc.

However, our plugin **does not** support business/corporate websites, eCommerce, and neither custom templates.

## Does Frontity support my current WordPress theme?

We create a Progressive Web App that is **independent** of your WordPress theme.

We doesn’t use PHP to render HTML anymore. Our solution uses a new system made with React and Node, carefully designed with performance in mind. We have made a lot of improvements which are \(sadly\) not possible in PHP.

This means that we are not able to re-use your theme. But it opens a new world of possibilities to build the best UX/UIs for the vibrant WordPress ecosystem.

Our system uses the new WordPress REST API to fetch the content \(only the content\).

## Compatibility with third-party plugins

We use the REST API to take the content from your WordPress site and display it in a client-side rendered PWA. If a third-party plugin is compatible with the REST API, it should be compatible with ours as well. But it really depends on each plugin.

WordPress PWA is **compatible** with some of the most **popular plugins**, such as [**YOAST SEO**](../integrations/yoast-seo-compatibility.md).

It does not support, however, those third-party plugins that implement major features such as WooCommerce.

