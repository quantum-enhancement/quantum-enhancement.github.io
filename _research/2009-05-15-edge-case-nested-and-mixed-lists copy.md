---
title: "Research #1: test page"
categories:
  - Edge Case
tags:
  - content
  - css
  - research
---

Collections like posts and pages work as you'd expect. If you're new to them be sure to read [Jekyll's documentation](https://jekyllrb.com/docs/collections/).

The theme has been built with collections in mind and you will find [several examples]({{ "/collection-archive/" | relative_url }}) on the demo site ([portfolio]({{ "/portfolio/" | relative_url }}), [recipes]({{ "/recipes/" | relative_url }}), [pets]({{ "/pets/" | relative_url }})). 

**Collections in the Wild:** This set of documentation is also [built as a collection](https://github.com/{{ site.repository }}/blob/master/docs/_docs/) if you're looking for a fully fleshed out example to inspect.
{: .notice--info}

---

A popular use case for collections is to build a portfolio section as part of one's personal site. Let's quickly walk through the steps to do that.

**Step 1:** Configure the portfolio collection by adding the following to `_config.yml`.

```yaml
collections:
  portfolio:
    output: true
    permalink: /:collection/:path/
```

These settings essentially say output `index.html` files for each portfolio document in `_portfolio` at `_site/portfolio/<document-filename>/`.

Just like posts and pages you'll probably want to set some defaults for the Front Matter:

```yaml
defaults:
  # _portfolio
  - scope:
      path: ""
      type: portfolio
    values:
      layout: single
      author_profile: false
      share: true
```

Now make a portfolio.md file in the '_pages' folder.

```yaml
---
title: Portfolio
layout: collection
permalink: /portfolio/
collection: portfolio
entries_layout: grid
classes: wide
---
```

And then create portfolio content like [`_portfolio/foo-bar-website.md`](https://github.com/{{ site.repository }}/blob/master/docs/_portfolio/foo-bar-website.md), to end up with something like this.

![portfolio collection example]({{ "/assets/images/mm-portfolio-collection-example.jpg" | relative_url }})



Nested and mixed lists are an interesting beast. It's a corner case to make sure that

* Lists within lists do not break the ordered list numbering order
* Your list styles go deep enough.

### Ordered -- Unordered -- Ordered

1. ordered item
2. ordered item 
   * **unordered**
   * **unordered** 
     1. ordered item
     2. ordered item
3. ordered item
4. ordered item

### Ordered -- Unordered -- Unordered

1. ordered item
2. ordered item 
   * **unordered**
   * **unordered** 
     * unordered item
     * unordered item
3. ordered item
4. ordered item

### Unordered -- Ordered -- Unordered

* unordered item
* unordered item 
  1. ordered
  2. ordered 
     * unordered item
     * unordered item
* unordered item
* unordered item

### Unordered -- Unordered -- Ordered

* unordered item
* unordered item 
  * unordered
  * unordered 
    1. **ordered item**
    2. **ordered item**
* unordered item
* unordered item

### Task Lists

- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request