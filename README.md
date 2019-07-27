# Temple

A Hugo theme focused on content, cleanliness, speed and responsiveness. The main
goal of this theme is to be simple and fast.

> This is a fork of [nofancy](https://github.com/gizak/nofancy) with many
improvements.

A live version of this theme can be found
[on my personal blog](https://aos.github.io).

![Main List](https://raw.githubusercontent.com/aos/temple/master/images/tn.png)
![Content](https://raw.githubusercontent.com/aos/temple/master/images/screenshot.png)

[Screenshot of theme responsiveness can be found here.](https://raw.githubusercontent.com/aos/temple/master/images/responsive.png)

## Table of Contents
* [Features](#features)
* [Getting Started](#getting-started)
* [Customizing](#customizing)
* [Contributing](#contributing)
* [License](#license)

## Features
The main features of this theme include:
* Page load speed optimizations (scores 99/100 on PageSpeed)
* Syntax highlighting with `chroma`
* No JavaScript
* Multiple categories as navigation tabs
* Tags and categories have their own pages
* Footer with variable social links and RSS
* Google analytics option
* Table of contents

## Getting Started
If you have not already created a blog, I recommend you check out my [getting started guide](https://aos.github.io/2017/11/23/practical-guide-to-setting-up-a-hugo-blog/) for a comprehensive overview. Otherwise,
just download it or clone it into your `themes/` directory:
```
$ cd themes && git clone https://github.com/aos/temple.git
```
Then reference it in your `config`:
```
theme = "temple"
```
Or when building the site, pass it in to the CLI:
```
$ hugo -t temple
```

## Customizing
Your `config` file will hold all your options:
```toml
baseURL = "https://aos.github.io/"
title = "Your Blog Title"
theme = "temple"
# If not set, it will not appear. Otherwise it will show below your footer links
copyright = "(c) 2008 - 2014"

# Enables Chroma-based syntax highlighting with theme "friendly"
# See https://xyproto.github.io/splash/docs/ for other theme options
pygmentsStyle = "friendly"
# If true, Chroma will highlight GitHub-style code fences in addition to
# highlight shortcodes
pygmentsCodeFences = true

[params]
  # Enables the topmenu, which pulls from categories
  topmenu = "categories"

  # Enables custom date format (optional, the default is MM-DD-YYYY)
  # For reference to date and time templating, see:
  # https://gohugo.io/functions/format/#hugo-date-and-time-templating-reference
  dateformatpretty = "2006-01-02"

  # Enable table of contents, this can be overridden by page level parameter `toc`.
  toc = true

# Builds a list page for each category given
[taxonomies]
  tag = "tags"
  category = "categories"

[author]
  name = "Aos Dabbagh"
  github = "aos"
  email = "your@email.com"
  # Note: GA Javascript snippet is not included if "gaid" is left blank
  gaid = "Your Google Analytics ID"
  twitter = "twitterID"
  medium = "mediumUsername"
```

There is also a fixed `About` page on the navbar. Create it using:
```
$ hugo new about
```

## Contributing
Contributions are welcome.

**Features**:  
If you are adding a feature, fork the repository, create a new branch
for your feature and submit a PR. Please make sure to put documentation for your
new feature:
- Place a small comment about what your feature is doing above the code.
- If making additions that will affect the `config` file, make sure you update
  the example `config` in [README](README.md) as well as the
  [config.toml](exampleSite/config.toml).

**Issues/Bugs**:  
Submit a new issue with information about your issue and/or bug. If you
have a solution, then submit a new PR with the guidelines posted above in the
**features** section and link your issue to it using the keyword "[*closes*](https://help.github.com/articles/closing-issues-using-keywords/)".

## License
MIT License. See the [LICENSE](LICENSE).
