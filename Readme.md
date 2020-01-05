# Canvas Conversion Regular Expressions

The following Regular Expressions were helpful in cleaning up Content from D2L Brighspace (.html files) in preparation for import into Instructure Canvas. You should be able to use the following Regular Expressions in any text editor that supports multi-file GREP searching. We have found success using the tags in the following order as well.

## How to Use

1. Download Content from [Manage Files](https://www.wisconsin.edu/learning-tech/resources/d2l-cleanup/how-to/download-course-files-2/) in your Brightspace course.

2. Unzip the Content on your local computer.

3. Open an HTML file using a text editor that supports multi-file GREP searching, e.g. [BBEdit](https://www.barebones.com/products/bbedit).

4. Run each expression.

### Final Steps in Our Proccess

After running each expression, we would zip the files back up and upload them back to the manage files area where they would be unzipped. At this point, clean up would continue in the Brightspace course until it was ready for export and import into Canvas.

# Regular Expressions

## Remove HTML Comments
*Find:* `<!--(.*?)-->`
*Replace:* null 

## Remove Header Tags (and everything between them)
*Find:* `<header(.*?)>[^"]*</header>`
*Replace:* null

## Remove Opening Layer/Div Tags
*Find:* `<div(.*?)>`
*Replace:* null

## Remove Closing Div Tags
*Find:* `</div>`
*Replace:* null

## Remove Opening Section Tags
*Find:* `<section(.*?)>`
*Replace:* null

## Remove Closing Section Tags
*Find:* `</section>`
*Replace:* null

## Remove Opening Article Tags
*Find:* `<article(.*?)>`
*Replace:* null

## Remove Closing Article Tags
*Find:* `</article>'
*Replace:* null

## Remove Stylesheet Links
*Find:* `<link(.*?)>`
*Replace:* null

*Note:* Will remove `<link>` tags where ever they are in the file.

## Change Opening Aside Tags to Opening Paragraphs
*Find:* `<aside`
*Replace:* `<p`

## Change Closing Aside Tags to Closing Paragraphs 
*Find:* `</aside>`
*Replace:* `</p>`

## Change Opening Figure Tags to Opening Paragraphs
*Find:* `<figure`
*Replace:* `<p`

## Change Closing Figure Tags to Closing Paragraphs 
*Find:* `</figure>`
*Replace:* `</p>`

## Change Opening FigCaption Tags
*Find:* `<figcaption>`
*Replace:* `<br /><span style="font-size: .75em; padding-left: auto; padding-right: auto;">`

## Change Closing FigCaption Tags
*Find:* `</figcaption>`
*Replace:* `</span>`

## Remove Footer Tags (and everything between them)
*Find:* `<footer(.*?)>[^"]*</footer>`
*Replace:* null

## Remove Grammerly Open Tags
*Find:* `<g(.*?)>`
*Replace:* null

19. Remove Grammerly Close Tags
*Find:* `</g>`
*Replace:* null

## Search for Media (using Find All)
*Find:* `<iframe(.*?)>`

## Wildcards
- (.*?)
- [^"]*