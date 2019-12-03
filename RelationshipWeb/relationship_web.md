# Relationship Web
Technology required:
* HTML/CSS
* JavaScript
* D3.JS

## General
The relationship web is based on the [force directed graph](https://github.com/d3/d3/blob/master/API.md#forces-d3-force) from the D3.js library.
The version of D3.js used is `v5`. Note that there is a drastic difference between versions of D3.js, and it is generally not backwards compatible. 

## Structure
The file structure for the relationship web is as follows:
```
css/
data/
  images/
    png/
js/
index.html
```
## Data
The url to the excel sheet is linked below, under the Resources section. In general, **it is crucial that the headings of the excel sheet remain unchanged**, as the file processing procedure relies on these headings. The "Image" tab in the excel sheet contains the local path of the image belonging to the individual within the `data/images/png` directory. For instance, Edward Spencer Beesly's portrait can be found under `data/images/png/edward_spencebeesly.png`, and therefore the excel sheet contains `edward_spencebeesly.png` under the Image tab.

Code for the relationship web is separated into two files: `relationship.js` and `relationshipUtils.js`, located within the `js/` directory. The `js/` directory also contains a local copy of the D3.js library, but this file is not necessary.

### What's in the index?
The `index.html` file contains the `div` element container for the relationship web, as well as a toggleable menu. The code for the toggleable menu is found within `relationshipUtils.js`. The togglemable menu contains an empty dropdown list intended to be populated with the names of individuals present in the relationship web.

### Reading data
The data is processed through the D3.js library's asynchronous `csv` function, and appended as a JSON to a global array. After all lines of data has been processed, the JSON array is used to populate the dropdown list in the toggleable menu, as well as a base for the force graph used in D3.js. Individuals are assigned arbitrary ids based on the order they were read in. This id is used to map images and maintaining order.

### Images
SVG elements cannot use images as backgrounds. Consequently, images themselves must first be processed and treated as sort of SVG elements themselves. The portraits are pre-cropped into circles, since it is very difficult and convoluted to clip images to exact sizes through SVGs.

All images are read from the directory `data/images/png` and stored as `pattern` elements within the main svg element containing the relationship web following the naming convention `image_#`. Individuals who do not have images paths defined in the data csv are given default images based on their relationship status. 

## "Post processing" data
See `post_processing_data.md`

## Debugging
Debugging this relationship web may be challenging and frustrating. Because data points are updating at every "tick"
## Known Bugs
1. Hovering names are clipped nodes placed too close to the edge

## Resources
* Relationship web files: https://unl.app.box.com/file/321910015418