# Full example

## Ad definitions

```text
name: ad-latest-1:
type: doubleclick
slot: /12345678/ad-latest-1
width: 300
height: 250

name: ad-latest-2:
type: doubleclick
slot: /12345678/ad-latest-2
width: 300
height: 250

name: ad-latest-3:
type: doubleclick
slot: /12345678/ad-latest-3
width: 300
height: 250

name: ad-latest-4:
type: doubleclick
slot: /12345678/ad-latest-4
width: 300
height: 250

------------------------------

name: ad-cat-1:
type: doubleclick
slot: /12345678/ad-cat-1
width: 300
height: 250

name: ad-cat-2:
type: doubleclick
slot: /12345678/ad-cat-2
width: 300
height: 250

------------------------------

name: ad-content-1:
type: doubleclick
slot: /12345678/ad-content-1
width: 300
height: 250

name: ad-content-2:
type: doubleclick
slot: /12345678/ad-content-2
width: 300
height: 250

name: ad-content-3:
type: doubleclick
slot: /12345678/ad-content-3
width: 300
height: 250

------------------------------

name: ad-gallery:
type: doubleclick
slot: /12345678/ad-content-3
width: 300
height: 250
```

## Ad positions

**Post list**

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

**Content of posts / pages**

```text
type: post, page
beginning: yes
end: no
ads: ad-content-1, ad-content-2, ad-content-3
```

**Galleries**

```text
type: gallery
ad: ad-media
```

