# Simple example

## Ad definitions

```text
name: ad-1
type: doubleclick
slot: /12345678/ad-1
width: 320
height: 100

name: ad-2
type: doubleclick
slot: /12345678/ad-2
width: 300
height: 600

name: ad-3
type: doubleclick
slot: /12345678/ad-3
width: 300
height: 250
```

## Ad positions

```text
type: latest, category, tag
positions:
  1: ad-1 (below the first post)
  7: ad-2 (below the seventh post)
```

```text
type: post, page
beginning: false
end: no
ads: ad-1, ad-2, ad-3
```

```text
type: gallery
ad: ad-1
```

