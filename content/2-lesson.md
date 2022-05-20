---
title: Datasets
nav: Datasets
topics: Datasets
---

In this workshop, we will use two different datasets to explore novoSpaRc.

## Kidney Dataset

Here, we will use novoSpaRc to spatially reconstruct a single-cell dataset from whole kidney [1], which is a complex tissue with stereotypical organization. Since there is no reference atlas of gene expression, the reconstruction will performed de novo. 

{% capture text %} [1] Park, J. et al. Single-cell transcriptomics of the mouse kidney reveals potential cellular targets of kidney disease. Science 360, 758–763 (2018).
{% include card.html header="Overview" text=text %}



## Basic Configuration

Edit the "_config.yml" to get your workshop website set up with the basics such as `title` and `author`.
Check comments (denoted by `#` in YAML) in the file for all the options!

Once you have edited the "_config.yml", you are ready to start editing your content pages.
All your content is written in Markdown in the "content" folder.
See [Create Lesson Content]({{ '/content/3-lesson.html' | relative_url }}) for details and options.

## Style customization [optional]

The file "assets/css/custom.scss" exposes variables that can customize the basic style of website:

- `$top-border` adds a tiny splash of color on the header and footer borders. Try tweaking the color using an [HTML # value](https://www.w3schools.com/colors/colors_picker.asp).
- `$text-color` sets the body text color
- `$link-color` sets link color
- `$base-font-size` sets the body text size
- `$container-max` sets a maximum width for the text body--keeping it narrow can make it easier to read, but gives less screen space!

To use the Bootstrap defaults for *any* of these values, comment out the variable in "custom.scss", using `//` in front of the option's line (e.g. `// $text-color: #111 !default;` ).

To add your own custom CSS, use the file "_sass/_custom.scss".
Any CSS/SASS you add to this file will override the template and Bootstrap classes.

## Add Optional Analytics [optional]

To use Google Analytics, add your analytics id to "_config.yml" in `google-analytics-id:` (if `google-analytics-id` is blank, the GA code will not added).
To use an alternative analytics, paste the code snippet provided by the platform into the file "_includes/template/analytics.html".

The analytics code will only be added when using "production" environment. 
This happens automatically on GitHub Pages. 
To build manually you need to add "JEKYLL_ENV", like: `JEKYLL_ENV=production jekyll build`.
