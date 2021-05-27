## CSS image styling:
![image](https://miro.medium.com/max/600/1*OFsc0SD55jhi8cjo7aCA4w.jpeg)
Zach takes a look at some fundamental HTML+CSS usage for fluid, responsive images. Most of it, I’d say, is what you’d expect, but things get weird when srcset gets involved.

I poked my way through, and in addition to the weird thing Zach noted, wanted to add one more thing. Let’s start like this:

`<img src="./img.jpg" alt="" />`
With no other CSS involved, this renders at the “intrinsic size” of the image. Say the original image is 400px wide, it renders 400px wide.

We should be putting width and height attributes on images, because it allows the browser to make space for them even before they are downloaded (even when they are fluid, which is super cool). So:

`<img src="./img.jpg" alt="" width="400" height="300" />`
Also nothing terribly weird there. Even if we slap max-width: 100% in the CSS, that’ll do what we want: preserving space, behave fluidly, and not growing bigger than it should.

But let’s hold off on the max-width: 100% thing for a second. If we just use srcset and set up multiple sources.

`<img src="./img.jpg" alt=""
     srcset="./img-200.jpg 200w, ./img-400.jpg 400w" />`
BAM, we blow out the width of the thing.

That won’t render at 200px or 400px—it’ll actually render at 100vw, believe it or not. I think that’s because that’s the default sizes value. I normally think of the sizes attribute as not information about anything to do with actual layout, but just information for the browser to choose a source

See the little one below it where all I change is the sizes.

Anyway that’s not what Zach honed in on, but it’s similar. Let’s put back the responsible thing and add in width and height attributes.

`<img src="./img.jpg" alt="" width="200" height="137"
     srcset="./img-200.jpg 200w, ./img-400.jpg 200w" />`
No more blowout (with or without sizes) but now we have a new weird problem. This is basically like saying max-width: 200px. Even though we have sources that are wider than 200px, we’ve capped the width at 200px. Zach puts it like:

Using max-width: 100% constrains the image to the container, but be careful when you use this with srcset—it may cap smaller than you want when using [width]! Pair with width: auto to fix this.

Zach’s final snippet is this, which I think reigns in all the weirdness:

    img {
    max-width: 100%;
    }
    img[width] {
    width: auto; /* Defer to max-width */
    }
    img[width][height] {
    height: auto; /* Preserve aspect ratio */
    }

/* Let SVG scale without boundaries */
    img[src$=".svg"] {
    width: 100%;
    height: auto;
    max-width: none;
    }

### CSS colors
![image](https://cdn.educba.com/academy/wp-content/uploads/2020/03/CSS-Color-Codes.jpg)

### Color Keywords
The first and easiest way to specify a color is using one of the 140 predefined color keywords specified in CSS.

### RGB Color Values
Most of you have probably heard about CMYK values for print design. RGB, which stands for red, green, and blue is the color model that monitors use. Since in web design we're primarily concerned with what web pages look like on screens, RGB is the color model we use.

### RGB colors have three values that represent: red, green, and blue
Each value can be a number between 0 and 255 or a percentage from 0 to 100%
A value of 0 means none of that color is being used
A value of 255 or 100% means all of that color is being used
A 0 for all three color values will be black
A 255 or 100% for all three color values will be white
The CSS syntax for using RGB colors is a little different than we've seen before. In the example below, we are styling:

    A black paragraph
    A white h1
    A purple unordered list
    p { color: rgb(0, 0, 0); }              /* black */
    h1 { color: rgb(255, 255, 255); }       /* white */
    ul { color: rgb(128, 80, 200); }        /* purple */

/* Percentages work too */
    h1 { color: rgb(100%, 100%, 100%); }    /* white */
    RGBA Color Values
    RGBA is all the rage.

Seriously though, it's just like RGB, except with the addition of a fourth value: the alpha channel.

The alpha value represents the level of transparency that the rgb color should have. It can be a value from 0 to 1 or a percentage from 0 to 100%. Note that you must specify RGBA instead of RGB.

### HSL
The HSL color model is one of the least used, but gaining traction because can be more intuitive to use when working with shades and color adjustments.

HSL stands for: hue, saturation, and lightness

### Hue
A picture of the HSL color wheel

Hue is defined by a color wheel. Each color represents a degree on the wheel. This page shows a nice visual animation of the color wheel:

### HSL Color wheel demo
Saturation
The boxes below demonstrate varying levels of saturation (color intensity) for the hue at 240°. The lightness value is set at 50% for each box.

### Lightness
Here's the same hue (240°) shown at various lightness levels with 100% saturation.

### HSL Color Grid Example
This grid shows varying saturation and lightness together.

hsl(240, 100%, 90%)hsl(240, 100%, 75%)hsl(240, 100%, 50%)hsl(240, 100%, 25%)hsl(240, 100%, 10%)hsl(240, 75%, 90%)hsl(240, 75%, 75%)hsl(240, 75%, 50%)hsl(240, 75%, 25%)hsl(240, 75%, 10%)hsl(240, 50%, 90%)hsl(240, 50%, 75%)

### HSLA
HSLA is simply the HSL color model with the addition of an alpha channel. This works exactly the same way as the alpha channel in RGBA.

    h1 {
    background-color: hsla(240, 25%, 50%, .5);
    }
Example of HSLA
Example of HSLA (on different background color)
Hexadecimal Color Values
A digram explaining hex code

Probably the most common (yet least intuitive) way to specify colors in CSS is to use their hexadecimal (or hex) values. Hex values are actually just a different way to represent RGB values. Instead of using three numbers between 0 and 255, you use six hexadecimal numbers. Hex numbers can be 0-9 and A-F. Hex values are always prefixed with a # symbol.

Demonstrated here are some basic CSS rules rules using hex values.

p { color: #000000; }     /* black */
h1 { color: #ffffff; }    /* white */
h1 { color: #aaaaaa; }    /* medium gray */
ul { color: #8050c8; }    /* purple */
Shorthand Notation for Hex Values
If both digits of the red, green and blue values are the same, you may use the short three-digit notation. This is best shown by an example:

p { color: #000; }     /* black same as #000000 */
p { color: #fff; }    /* white same as #ffffff */
p { color: #f00; }     /* red: same as #ff0000 */
h1 { color: #0f0; }    /* lime: same as #00ff00 */
ul { color: #ff0; }    /* yellow: same as #ffff00 */

### CSS font styles
![image](https://storage.googleapis.com/blog-images-backup/1*qQPAMr_eVqnutHKhlYoT2A.png)


### Weight
You used the <i> and <b> HTML elements to mark certain sections of text as being italic or bold. However, you can also use CSS to accomplish the same things. For example, the CSS font-weight declaration can be used not only to make your selected text bold, but also to specify how bold it should be. 

There are a few different ways to specify the boldness of your chosen font, but the simplest is just a single-word value:

font-weight: bold; 
Alignment
Finally, you may also want to change the alignment of your text. By default, your browser will display any text you add to your page as left-aligned, just like you would read it in a book.

However, you may occasionally have reason to align it to the right, or to justify it (where each line has equal width, like in a newspaper or magazine). Most commonly, though, you might want to center it.

You can use the CSS text-align declaration to change the alignment of your selected text, and the values are predictable: left, right, justify, or center. For example:

    text-align: center;

### Multiple Declarations
Now that you've see a few different CSS declarations, it's also important to note that a ruleset can include more than one declaration at once. For example, let's say you wanted to make some changes to the main header to which you attached the #header id. You can add just one ruleset to your stylesheet:

    #header {
    }
And then add multiple declarations all in a stack:

    #header {
    font-size: 18px;
    font-family: 'georgia';
    font-weight: bold;
    text-align: center;
    }
As with HTML, your browser is not particularly concerned with formatting, and it's mostly for your own sake that you should try to keep your CSS neat and orderly. For example, your browser wouldn't care if the ruleset above looked more like this:

`#header{font-size:18px;font-family:'georgia';font-weight:bold;text-align:center;}`
However, keep in mind that your browser will definitely get confused if you leave out the semi-colons that end each declaration. They are the only way your browser can know when one declaration ends and the next begins.