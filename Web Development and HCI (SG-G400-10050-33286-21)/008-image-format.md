### Image formats (Stefan Pletschacher)

_2020-10-20 1:00:00 - 2020-10-20 15:50:00_

#### Image formats

When choosing images it's important to choose the right format:

* JPEG is best used for images which have a wide range of colours, like photos from a camera. JPEG is "lossy" which means it is compressed for size and loses some information during that compression.
* PNG is best used for images with few colours or where the image is computer generated or has a lot of gradients. PNG is "lossless".
* GIF is best used for images which are animated or where very few colours are needed.

There is another set of image formats which store images in a different way called Vectors:

* Traditional image formats store pixels in bitmaps (maps of pixel bits) like JPEG, PNG, etc.
* Vector image formats store information about how to generate the image instead.
* Vector images are scaleable to any size of pixels without losing any information or causing any artifacting (weird abberations or lossses of quality when rendering the images)

Think, instead of saying `here is a bunch of pixels` it says `draw a square here which is red`, `now draw a circle on top of the square`. For simple, computer generated images, vectors can store the same information in a **much** smaller amount of hard drive space.

Examples of vector image formats are: SVG and EPS.

_Editor's note: For anyone interested in SVGs it's worth mentioning that because they're made up of rules, those rules can be ANIMATED. You can make some really cool animations by interpolating between values in an SVG._

#### Transparency

Some images have a property where parts of them can be seen through. For instance, an icon without a background, or a cutout of somebody's face.

The GIF and PNG file formats (and SVG) have transparent backgrounds _by default_.
