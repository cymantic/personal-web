---
title: "Config File"
description: Some basics on the configuration of the theme
date: 2019-04-20T16:18:12+01:00
publishDate: 2019-04-20T19:12:12+01:00
---

Here is the basic config file used for personal_web.

You can use it as a base for your website.

<!--more-->

```TOML
baseURL = "https://example.com/"
languageCode = "en-us"
title = "Edna West"
theme = "personal_web"
copyright="© Edna West"
googleAnalytics = ""
enableEmoji=true
enableRobotsTXT=true
pygmentsUseClasses=true
pygmentsCodeFences=true

[params.intro]
  main = "Hi, I'm Edna :wave:"
  sub = "I'm a Web Developer and Entrepreneur"

[taxonomies]
  design = "designs"
  tech = "techs"

[blackfriday]
  hrefTargetBlank = true

[params]
  breadcrumb = true
  accentColor = "#FD3519"

[params.notFound]
  gopher = "/images/gopher.png"
  h1 = 'Bummer!'
  p = "It seems that this page doesn't exist."
  mainSection = 'portfolio'

[params.sections]
  post = "article"
  portfolio = "project"

[params.sidebar]
  backgroundImage = ''
  gradientOverlay = ''
  logo = ""

[params.assets]
  favicon = ""
  customCSS = ""

[params.social]
  github = "https://github.com/"
  twitter = "https://twitter.com/"
  linkedin = "https://www.linkedin.com/in/"

[params.contact]
  email = ""
  text= ""


[menu]

[[menu.main]]
  identifier = "about"
  name = "About"
  title = "About section"
  url = "/about/"
  weight = -120

[[menu.main]]
  identifier = "portfolio"
  name = "Portfolio"
  title = "Portfolio"
  url = "/portfolio/"
  weight = -110

[[menu.main]]
  identifier = "blog"
  name = "Post"
  title = "Blog section"
  url = "/post/"
  weight = -100

[sitemap]
  changefreq = "monthly"
  filename = "sitemap.xml"
  priority = 0.5

[privacy]
  [privacy.googleAnalytics]
    anonymizeIP = true
    disable = true
    respectDoNotTrack = true
    useSessionStorage = false
  [privacy.twitter]
    disable = false
    enableDNT = true
    simple = false

```

## Sidebar

The sidebar header is defined within the `params.intro` section. The `main` being the top header and `sub` the subheader

```TOML
[params.intro]
  main = "Hi, I'm Edna :wave:"
  sub = "I'm a Web Developer and Entrepreneur"
```

You can also customize the params with the  `params.sidebar` parameters. The `config.toml` file contains the default values as examples.
```TOML
[params.sidebar]
  backgroundImage = ''
  gradientOverlay = ''
  logo = ''
```

## 404

The 404 page is defined within the `params.notFound` section.
The `gopher`, `h1` and `p` params define the image and texts displayed on the page. The `mainSection` params possible values are 'portfolio' or 'post': it defines the section highlighted on the page.

NB: to see the 404 page from your development env, check `/404.html`.

```TOML
[params.notFound]
  gopher = "/images/gopher.png"
  h1 = 'Bummer!'
  p = "It seems that this page doesn't exist."
  mainSection = 'portfolio'
```

You can also define how the post and portfolio sections will be named on the 404 page, thanks to the `params.sections` params.

```TOML
[params.sections]
  post = "article"
  portfolio = "project"
```

## Customization

You can define a custom CSS file in the `customCSS` param and a favicon.
```TOML
[params.assets]
  favicon = ""
  customCSS = ""
```

## Social

You can define your social media usernames in the `params.social` and the `params.contact` paramaters. 

In this last section, the email expects your email address and the text is what will be displayed on the sidebar, right below the last item of the menu. If blank, nothing is displayed.

```TOML
[params.social]
  github = "https://github.com/"
  twitter = "https://twitter.com/"
  linkedin = "https://www.linkedin.com/in/"

[params.contact]
  email = ""
  text= ""
```