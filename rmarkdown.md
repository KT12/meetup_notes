# Back to Basics: R you markDOWN?

## New York Open Statistical Programming Meetup
June 26, 2017
Work-Bench
110 5th Ave.

Daniel Chen

### Rmarkdown
Rmarkdown - example of literate coding

Rundown on [cheatsheet](https://www.rstudio.com/wp-content/uploads/2016/03/rmarkdown-cheatsheet-2.0.pdf)

3 parts to RMD file
* yaml header
* code snippets
* regular text

revealjs presentation

Output is determined by yaml header

Can even run r code inline:
`r n` # n = 10
Renders '10'

Can also run code and hide output (say if you are faking something for a presentation)

knit button renders (ctrl shft k)

In the yaml header, can set params to use in the code.

Pandoc is converting markdown into other doc types.  Would use Pandoc from command line.

### R Notebook
Rnotebook is rstudio version of Jupyter notebook.
R markdown doc - all code is sent to console at once
For notebook, one line at a time is sent to console, easier to handle errors

Can run SQL code natively, and save it to an R variable

Can use shiny interactive documents or even full blown dashboards, using flexdashboard
Can also use rmarkdown to create blog, using blogdown
Can also publish book using bookdown

