Draw Library is simple yet powerful API to draw graphical objects.
The module name is **draw**.

**setscreen** - change screen mode text/graphics
    
    draw.setscreen ( mode)

    mode:
        O: text screen (default)
        1: graphics screen
        
    coordinate system: x is from left to right and y is from top to bottom hint: use getsize () and getport() to get screen and port dimension

**settitle** - set graphics screen title
    
    draw.settitle( text)
    text: graphics screen title

**showtitle** - set graphics screen title
    
    draw.showtitle( show)
    show: boolean
    
    true shows title bar false hides title bar
    Note: to show/hide title bar manually swipe with three fingers up/down

**clear** - clear screen
    
    draw.clear()
    draw.clear color()
    color: screen clear color, when omitted white is used

**getsize** - return overall screen size
    
    width, height = draw.getsize()
    width : overall screen width height: overall screen height

**getport** - return current viewable screen port size
    
    width, height = draw.getport()
    getport is available after calling setscreen()
    width : screen port width
    height: screen port height

**point** - draws a point
    
    draw.point ( X, Y, color )
    X: x-coordinate of point
    Y: y-coordinate of point
    color: color of the point

**moveto** - move current point to given coordinate
    
    draw.moveto ( x, y)
    X, y: coordinate

**lineto** - draw line from current point to given coordinate
    
    draw.lineto( x, y, color )
    X, y: line end coordinate 
    color : line color

**line** - draw line

    draw.line(×1, y1, ×2, y2, color)
    X1, y1: line start coordinate
    ×2, y2: line end coordinate 
    color: line color

**rect** - draw rectangle

    draw.rect(×1, y1, x2, y2, color )
    ×1, y1 : upper left corner coordinate of rectangle 
    ×2, y2: lower right corner coordinate of rectangle
    color: rectangle outline color color

**fillrect** - draw filled rectangle
    
    draw.fillrect( x1, y1, ×2, y2, color )
    ×1, y1 : upper left corner coordinate of rectangle 
    ×2, y2: lower right corner coordinate of rectangle 
    color: rectangle fill color

**circle** - draw circle

    draw.circle( xc, yc, radius, color )
    XC, yc: circle centre coordinate 
    radius: circle radius 
    color: circle outline color

**fillcircle** - draw filled circle

    draw.fillcircle ( xc, yc, radius, color )
    XC, yc: circle centre coordinate 
    radius: circle radius 
    color: circle fill color

**arc** - draw arc

    draw.arc( xc, yc, radius, s, e, color )
    XC, yc : arc centre coordinate 
    radius: arc radius
    s: arc start angle in radians
    e: arc end angle in radians 
    color: arc outline color

**fillarc** - draw filled arc

    draw.fillarc( xc, yc, radius, s, e, color )
    xC, yc: arc centre coordinate 
    radius : arc radius
    s: arc start angle in radians
    e: arc end angle in radians 
    color : arc fill color

**ellipse** - draw ellipse

    draw.ellipse ( ×1, y1, ×2, y2, color )
    ×1, y1: upper left corner of the rectangle enclosing the ellipse 
    ×2, y2: lower left corner of the rectangle enclosing the ellipse 
    color : ellipse outline color

**fillellipse** - draw filled ellipse

    draw. fillellipse ( ×1, y1, ×2, y2, color )
    ×1, y1: upper left corner of the rectangle enclosing the ellipse 
    ×2, y2: lower left corner of the rectangle enclosing the ellipse 
    color: ellipse fill color

**polygon** - draw polygon

    draw.polygon( xc, yc, radius, sides, rotation, color ) 
    xc, yc : polygon centre coordinate 
    radius: polygon radius 
    sides : polygon sides 
    rotation: polygon rotation in radians 
    color : polygon outline color

**fillpolygon** - draw filled polygon

    draw.fillpolygon( xc, yc, radius, sides, rotation, color) 
    xC, yc: polygon centre coordinate 
    radius: polygon radius 
    sides : polygon sides
    rotation : polygon rotation in radians 
    color : polygon fill color

**star** - draw star

    draw.star( xc, yc, ir, or, v, rotation, color ) 
    xC, ус : star centre coordinates 
    ir: inner radius of star 
    or: outer radius of star
    v: number of star vertices 
    rotation: star rotation in radians 
    color: star outline color

**fillstar** - draw filled star

    draw.fillstar( xc, yc, ir, or, v, rotation, color )
    XC, yc: star centre coordinates 
    ir: inner radius of star 
    or: outer radius of star
    v: number of star vertices 
    rotation: star rotation in radians 
    color: star fill color

**triangle** - draw triangle

    draw.triangle (×1, y1, x2, y2, ×3, y3, color )
    ×1, y1 : triangle first coordinate 
    ×2, y2 : triangle second coordinate
    X3, y3 : triangle third coordinate 
    color : triangle outline color

**filltriangle** - draw filled triangle

    draw.filltriangle(×1, y1, ×2, y2, ×3, y3, color)
    ×1, y1: triangle first coordinate 
    ×2, y2: triangle second coordinate 
    X3, y3: triangle third coordinate 
    color: triangle fill color

**roundedrect** - draw rectangle with rounded corners

    draw.roundedrect( ×1, y1, ×2, y2, radius, color )
    ×1, y1 : upper left coordinate of rectangle 
    ×2, y2: lower right coordinate of rectangle 
    radius: radius of rounded corner 
    color: rounded rectangle outline color

**fillroundedrect** - draw filled rounded corners rectangle

    draw.fillroundedrect(×1, y1, x2, y2, radius, color )
    ×1, y1 : upper left coordinate of rectangle 
    ×2, y2: lower right coordinate of rectangle 
    radius: radius of rounded corner 
    color: rounded rectangle fill color

**string** - draw string

    draw.string ( text, X, Y, color ) 
    text: string to draw
    X, y: top left coordinate of string 
    color: string color

**stringsize** - drawn string size

    width, height = draw.stringsize( text )
    text: string to measure
    width, height: measured text width and height

**stringinrect** - draw string inside a rectangle

    alignment: top to bottom, vertically centred 
    draw.stringinrect( text, ×1, y1, ×2, y2, color ) 
    text: string to draw 
    ×1, y1: top left coordinate of rectangle 
    ×2, y2: bottom right coordinate of rectangle 
    color: string color

**setfont** - change drawn text font name and size

    draw.setfont( name, size) 
    name: font name 
    size: font size

**setlinestyle** - change line style

    draw.setlinestyle( width, style) 
    width: line width
    style: cap style - text value one of 'butt', 'round', or 'square'

**setantialias** - set antialiasing flag

    draw.setantialias( flag)
    flag: Boolean value (default: true)

**getantialias** - get antialiasing flag

    f = draw.getantilias()
    f: Boolean value

**sleep** - wait for specified time

    draw.sleep ( ms)
    ms : time in millisecond ( 1 second = 1000 millisecond)

**gettime** - returns time in seconds (high resolution timer)

    time = draw.gettime()
    time: time in seconds since reference time

Hint: you usually use the difference of two times.

**beginframe** - start drawing into frame

    buffers drawings 
    draw.beginframe()

**endframe** - end drawing into frame

    presents frame into screen 
    draw.endframe()

**setrefresh** - set screen refresh rate

    draw.setrefresh( times)
    times: number of refreshes per second

**disablerefresh** - disable auto screen refresh

    draw.disablerefresh()

**enablerefersh** - enable auto screen refresh

    draw.enablerefresh()

**refresh** - do screen refresh

    manual screen refresh 
    draw.refresh()

**waittouch** - waits user to make screen touch

    X, y = draw.waittouch()
    X, y: coordinates of touch

**tracktouches** - register touch handlers Deprecated

    draw.tracktouches(touchBegan, touchMoved, touchEnded) 
    touchBegan : touch began handler 
    touchMoved: touch moved handler 
    touchEnded : touch ended handler

each handler has two parameters (x, y) representing touch coordinate see Paint example

**doevents** - calls appropriate event handlers

    draw.doevents()

**clearevents** - clear all evens

    draw.clearevents()

**clearscreen** - clears screen with transparent color

    not to be confused with clear( color ). used to create images 
    draw.clearscreen()

**clearrect** - clears rect with transparent color

    used to create images 
    draw.clearrect( ×1, y1, ×2, y2)
    ×1, y1 : top left coordinate of rectangle 
    ×2, y2: bottom right coordinate of rectangle

**setclearcolor** - set transparent color

    used to create images 
    draw.setclearcolor( color)
    color: how transparent color appears to user

**setclip** - set clipping rectangle

    all drawing outside the provided rect will be clipped 
    draw.setclip ( ×1, y1, ×2, y2)
    ×1, y1 : upper left coordinate of clip rectangle 
    ×2, y2: lower right coordinate of clip rectangle

**clearclip** - remove clipping rectangle

    draw.clearclip()

**image** - draw image

    draw.image( file, X, y) 
    file: image file name (path)
    X, y: top left of image

if you need to access an image in resources folder use 

    '@resources/filename.ext'

you can also use relative paths

**tiledimage** - draw tiled image

    draw tiled image repeating horizontally and vertically in rectangle area as needed
    draw.tiledimage (file, ×1, y1, ×2, y2) 
    file: image file name
    ×1, y1: upper left coordinate of rectangle 
    ×2, y2: lower right coordinate of rectangle

**transformedimage** - draw transformed image

    draw.transformedimage (file, xc, yc, scale, rotation) 
    file: image file name
    xc, yc: position of centre of image 
    scale: image scale factor (original size is 1) 
    rotation: image rotation angle in radians (no rotation is 0)

**subimage** - draw transformed sub image

    used to draw images from image sheet
    draw.subimage ( file, ×1, y1, ×2, y2, xc, yc, scale, rotation) 
    file: image file name
    ×1, y1, x2, 2y : source image area 
    xC, yc: destination position (centre of image) 
    scale: image scale factor (original size is 1) 
    rotation: image rotation angle in radians (no rotation is 0)

**cacheimage** - cache image

    loads and caches image for drawing (image(), tiledimage), ...) use image caching to improve drawing speed
    width, height = draw.cacheimage ( file )
    file: image file name
    width : image width in pixels 
    height: image height in pixels
    
file name is used as the key for cacheing (value is the image it self) when you draw an image cache is checked first before loading file

**removeimage** - remove image from cache

    unloads the image.
    use when image is no longer used for drawing 
    draw.removeimage( file )
    file: image file name

**imagesave** - save image to file

    save a portion/rectangle of screen to file with png format 
    draw.imagesave( file, ×1, y1, X2, y2 ) 
    file: image file name (should have png extension)
    ×1, y1: upper left coordinate of rectangle 
    ×2, y2: lower right coordinate of rectangle

**startaccelerometers** - start accelerometers

    use before starting to read accelerometers 
    draw.startaccelerometers()

**stopaccelerometers** - stop accelerometers

    use when accelerometer is no longer needed (save battery)
    draw.stopaccelerometers()

**accelerometers** - read accelerometers

    make sure to call draw.startacceleromters() before using (only once)
    X, Y, z = draw.accelerometers()
    X, Y, z: values of each component. range of values is -1 to 1

**startgyro** - start gyroscope

    use before starting to read gyro 
    draw.startgyro()

**stopgyro** - stop gyro

    use when gyro is no longer needed (save battery)
    draw.stopgyro()

**gyro** - read gyroscope

    make sure to call draw.startgyro() first (only once)
    X, Y, z = draw.gyro()
    X, Y, z: values for each component. value is radians per second

**touchbegan** - function that handles multi touch began event

    if set, this function is called to handle multi touch began event 
    draw.touchbegan( touches)
    touches: table of touches, every item touches[I] has :
        id = touch ID (starts from 1)
        X = x coordinate of touch
        y = y coordinate of touch

**touchmoved** - function that handles multi touch moved event

    if set, this function is called to handle multi touch moved event 
    draw.touchmoved( touchess)
    touches = table of touches, every item touches[i] has :
        id = touch ID (starts from 1)
        X = x coordinate of touch
        y = y coordinate of touch

**touchended** - function that handles multi touch ended event

    if set, this function is called to handle multi touch ended event 
    draw.touchended(touches)
    touches = table of touches, every item touches[i] has :
        id = touch ID (starts from 1)
        X = x coordinate of touch
        y = y coordinate of touch

**Pre-defined colors**

    draw.white
    draw.black
    draw.red
    draw.green
    draw.blue
    draw.cyan
    draw.magenta
    draw.orange
    draw.purple
    draw.yellow
    draw.brown
    draw.gray
    draw.darkgray
    draw.lightgray

Examples of making new colors:

    myGray = { red=0. 1, green=0.1, blue=0.1, alpha=1}
    myGray = { 0.1, 0.1, 0.1, 1}
    myGray = {r=0.1, 9=0.1, b=0.1, a=1}
    myGray.red = .1 myGray.green=.1 myGray.blue = .1 myGray.alpha=1