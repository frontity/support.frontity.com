# Ad Configuration

* [**Introduction**](./#introduction)
* [**Ad definitions**](./#ad-definitions)
* [**Ad positions**](./#ad-positions)
* [**Next steps**](./#next-steps)

## Introduction {#introduction}

Frontity allows you to insert ads in your website, between posts in post lists or within the content of posts or pages, being able to choose the position and order of these ads.

## Ad definitions {#ad-definitions}

Before deciding where to place the ads, the first thing to do is to define the ads that you want to use. The ideal would be to create a list of ads, assigning them a name along with their properties. Here is the list of currently-supported technologies, showing the properties required to configure ads using each of them:

* [**Smart AdServer**](smart-adserver.md)
* [**AdSense**](adsense.md)
* [**DoubleClick**](doubleclick.md)

We recommend assigning them a name \(it does not matter which\), so that it is easy to identify them when deciding where they are displayed, e.g.

```text
name: ad-latest-1
type: doubleclick
slot: /12345678/slot-latest-1
width: 300
height: 250

name: ad-latest-2
type: doubleclick
slot: /12345678/slot-latest-2
width: 300
height: 250
```

## Ad positions {#ad-positions}

The pages where you can place ads at this time are: lists of posts \(latest posts, category, tag\), content of articles \(post, page\) and galleries \(media\).

> **⚠️ Important:** note that we place our ad between your first ad and your second ad in each view, except for galleries. For more info, see our [business model](../../useful-information/business-model.md).

### 1. Post lists \(latest posts, categories and tag lists\)

The post lists are those views where the posts are listed, in which the title appears along with a photo and a short summary, usually grouped in pages of 10 posts. Ads in this type of view can be placed between posts.

You can choose where to show ads according to these attributes:

| ATTRIBUTES | VALUES | DESCRIPTION | MANDATORY |
| :--- | :--- | :--- | :--- |
| **type** | `latest`, `category`, `tag` | Type of list. If the type is not indicated, the ad will appear for all of them. | no |
| **page** | `1`, `2`, `3`... | Page number. If none is indicated, the ad will appear in all pages at the specified position. | no |
| **position** | `0`, `1`, `2`, ... | Position that the ad occupies in the list of posts, being `0` the position before the first post, `1` the position after the first post, `2` the one after the second post, etc. | yes |

An example of configuration would be the following:

```text
type: latest
page: 1
positions:
  1: ad-latest-1 (below the first post)
  7: ad-latest-2 (below the seventh post)

type: latest
page: 2, 3, 4, 5
positions:
  1: ad-latest-3
  7: ad-latest-4

type: category, tag
positions:
 1: ad-cat-1
 7: ad-cat-2
```

### 2. Content of posts and pages

The ads are placed in the order in which they are specified, and they occupy space according to the position to be displayed. You can choose whether to start displaying the ads from the start of content or a little below. Also, you can indicate if the last shown ad should be placed at the end of the content.

| ATTRIBUTE | VALUE | DESCRIPTION | MANDATORY |
| :--- | :--- | :--- | :--- |
| **beginning** | `yes/no` | Indicates if the first ad should be positioned at the beginning of the post content. | yes |
| **end** | `yes/no` | Indicates if the last shown ad should be positioned at the end of the post content. | yes |

An example of configuration would be the following:

```text
type: post, page
beginning: yes
end: no
ads: ad-content-1, ad-content-2, ad-content-3
```

### 3. Galleries:

You can choose an ad that will be displayed in galleries. In this type of view, we do not place any ad but the one you have specified.

```text
type: gallery
ad: ad-media
```

## Next steps {#next-steps}

Get the properties of each ad

* [**Smart AdServer**](smart-adserver.md)
* [**AdSense**](adsense.md)
* [**DoubleClick**](doubleclick.md)

See some examples

* [**simple example**](ads-simple-example.md)
* [**full example**](ads-full-example.md)

Configure ads.txt

* [**Ads.txt**](ads-txt.md)

