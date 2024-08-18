# Colors

The standard elephant colors are #F4EDEB for the body and #3D3741 for the outline and eye. 

These can be changed when incorporating the elephant into a logo for another site with theme 
colors. The colors should always be very light and dark with only a slight tint of color. Never
make the body fill a bright vibrant color or dark color. The outline should always be a dark 
gray with a slight tint.

# Exporting PNGs

Exported PNGs go in the docs folder and are committed in the repository. These images are
made available at logos.mwtaylor.dev for linking.

Exported PNGs are always square and named "elephant<width in pixels>.png".

Export the whole page. Only the "Elephant" layer should be visible, hide all the others.

The following files should be exported:
- elephant16.png
  - Used as a favicon
  - Set the stroke width of the main outline to 25px and the eye to 16px
  - Don't worry about the stroke going off the page, the image is too small to notice
- elephant32.png
  - Used as a favicon
  - Set the stroke width of the main outline to 25px and the eye to 16px
  - Don't worry about the stroke going off the page, the image is too small to notice
- elephant48.png
  - Used as a favicon
  - Set the stroke width of the main outline to 18px and the eye to 16px
- elephant192.png
  - Used as a high resolution favicon and Android icon
  - Set the stroke widths of the main outline and eye to 16px
- elephant100.png
  - Set the stroke width of the main outline to 18px and the eye to 16px
- elephant200.png
  - Set the stroke widths of the main outline and eye to 16px
- elephant400.png
  - Set the stroke widths of the main outline and eye to 14px
- elephant600.png
  - Set the stroke widths of the main outline and eye to 12px
- elephant800.png
  - Set the stroke widths of the main outline and eye to 10px

# Comments Related to Creating The SVG

A few things to note in case changes need to be made to the paths later. Here are details 
about how the SVG is created and what all the paths and layers are for.

The "Elephant Parts" layer contains the basic paths for each part of the elephant that 
were traced from an image I took of a paper drawing of the elephant. The end nodes of 
each path should be snapped to another path unless they clearly continue into the interior
like both ends of the ear and the lower end of the trunk.

The "Line Extensions" layer has short paths that connect to the end of each path in the parts
layer to continue the path just beyond where it intersects and snaps to another path. This is
needed for the shape builder to correctly identify the shape of the elephant.

To make the "Elephant Outline" path, select all paths in the parts layer, duplicate and then 
Path > Combine.

To make the "Elephant Fill" path, select all paths in the parts and extensions layers, 
duplicate and use the shape builder to select all shapes for the body and legs. Select the results
and Path > Combine.

The "Document" layer contains extra stuff mostly needed for exporting. The "Margin" path sets
a margin around the elephant so it doesn't go right up against the edge of the document. To 
create it select the "Elephant Fill" path and Path > Outset a few times until it looks like
the correct margin.

After changes make sure to select everything and move it so the top left corner (which should
be from the margin path) and then scale the elephant to fit the whole document.
