# Markdown CV

This project was a fork from [elipapa's markdown-cv project](https://github.com/elipapa/markdown-cv) and based on [blmoore's CV](https://github.com/blmoore/md-cv) with a slight tweak, the usage is essentially the same. I use this as my personal CV but you can use the styling theme for your own CV.

See live demo [here](https://bruhtus.github.io/cv).

### How to use

To build, clone the repo and run jekyll:

```bash
git clone https://github.com/bruhtus/cv.git
cd cv
jekyll s --config _config.yml
```
(You may need to [install jekyll](https://jekyllrb.com/docs/installation/).)

### HTML version

The HTML version is generated by Jekyll under `_site` using `media/cv-screen.css`. Most changes from the original repo are artificial:

* changed the year and the layout (simplify the layout).
* messed with colours.
* now imports font-awesome icons and Open sans
* moved `ul` into 3-col layout (iirc following [another markdown cv](https://github.com/davidhampgonsalves/resume) I tried)

### PDF version

Note the separate CSS for print and screen media (see `media/cv-print.css`), my approach was to build a somewhat "jazzy" html version and a toned-down print version (for PDF). My changes introduce CSS3 columns in some sections which currently don't print to PDF under the blink/webkit engines (as of March 2015), so to print properly I suggest firefox.

Another problem with the PDF is pagebreaks, they're often not handled gracefully so I've added one in explicitly. Say you want a pagebreak before the section titled "education" (`h2` text is set to `id` so use unique section headers!), the print media CSS would be:

```CSS
#technical-skills {
	page-break-before: always;
}
```
