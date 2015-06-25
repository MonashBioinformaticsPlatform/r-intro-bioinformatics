---
layout: page
title: Test Lesson
subtitle: This is a test by Steve A.
minutes: 3
---

> ## Learning Objectives {.objectives}
> * Lalala
> * Bla bla bla
> * Etc etc

Hi there, this is a test file. `And here is some inline code!` yay.

*This is some executed R code..*


```r
print("This is some printed text")
```

```
## [1] "This is some printed text"
```

### Here's how you get R lesson generation working:
_Eg. How to make [this Rmd file](https://raw.githubusercontent.com/steveandroulakis/r-novice-inflammation/gh-pages/99-test-lesson.Rmd) generate the html page you're reading._

1. git clone the lesson on your machine `git clone https://github.com/swcarpentry/r-novice-inflammation`
2. Write your Rmd page (like the file that generated this.. [99-test-lesson.Rmd](99-test-lesson.Rmd)!). *Note: Your `Rmd` file must start with a number and dash, like the other ones currently in the directory. Eg `55-my-test.Rmd`.*
3. Install gcc, R and pandoc (use `brew` on the Mac)
4. Install pandocfilters and commonmark (it's python, use `pip`)
5. Install knitr in R (eg `install.packages('knitr', dependencies = TRUE)`)
6. `make preview` to generate the relevant markdown, html files for your lessons.
7. You'll end up with an html page like this one!
8. Your output should resemble the following:

```
$ make preview
Rscript -e "knitr::knit('$(basename 99-test-lesson.Rmd)', output = '$(basename 99-test-lesson.md)')"


processing file: 99-test-lesson.Rmd
|......................                                           |  33%
ordinary text without R code

|...........................................                      |  67%
label: steve-test-code
|.................................................................| 100%
ordinary text without R code


output file: 99-test-lesson.md

[1] "99-test-lesson.md"
pandoc -s -t html \
--smart \
--template=_layouts/page \
--filter=tools/filters/blockquote2div.py \
--filter=tools/filters/id4glossary.py \
-Vheader="$(cat _includes/header.html)" -Vbanner="$(cat _includes/banner.html)" -Vfooter="$(cat _includes/footer.html)" -Vjavascript="$(cat _includes/javascript.html)" \
-o 99-test-lesson.html 99-test-lesson.md
```

### And now, for a kitten...
<img src="fig/kitten.png" alt="A Kitten" />

> ## Challenge - Doing things. {.challenge}
>
> Do all of the things!

> ## Key Points {.callout}
>
> * Test point 1
> * Test point 2
