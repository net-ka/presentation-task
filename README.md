**Slide (Canvas)**
Hello to everybody who is watching this video! Today I'll tell you about canvas.
So let's start!

Slide (What is canvas?)
And of course the first question is what is canvas? Canvas – is just an HTML element which can be added to your web page. And it allows you to draw some graphics or some different figures or even write text on the fly just using JavaScript.
This technology was first introduced in WebKit by Apple and it was used for operation system X Dashboard. And actually now most of the browsers support this technology but Internet Explorer still doesn't support it as we want. And there is some option for browsers which don't support this technology which we will look into on our next slides.

Slide (Canvas example)
So how can we create a canvas? It is necessary to add special canvas tag to your HTML file and it has opening and closing tags. And actually it is necessary to add ID to this element because all the actions will be done with this canvas using JavaScript so ID is necessary to find this element in future. Also canvas doesn't have width of height if you don't add these properties. So it is necessary to add width and height. The shape of the canvas is just a rectangle. And also canvas doesn't have any styles. So if you want to see it, if you want to see its’ border it is necessary to add the style. 
So on this slide you can see an example of just simple canvas element.

Slide (Fallback content)
As I mentioned before not all the browsers support canvas. So what should we do in this case? What should we do if our browser doesn't support canvas? It is necessary to add fallback content to each canvas element. 
So what is this? This content is like alt attribute which is used for images. So you should put some content, some text or some image for example between opening and closing canvas tag. And if the browser supports canvas technology it will ignore this content between opening and closing canvas tag and it will just render canvas graphics. But if the browser doesn't support canvas technology it will read this text or something else what we put between opening and closing tag.
So it is actually important to add this information so don't forget about this.

Slide (HTML canvas can)
As I mentioned canvas doesn't have any visible content inside it. So we should style everything and on this slide you can see just an empty (a blank) rectangle. This is canvas and it has only a border.
So what canvas can do? Let's dive into its possibilities and its options! 

Slide (Draw text)
First of all you can draw text. You can draw it colorful, with or without animation, your letters could be filled with some color or could have only borders and there’re a lot of options which can be used for text. 

Slide (Text properties and methods)
So let's see which properties and methods this text option has. First of all you can add a font property to your text drawing and this property will define the font of the text which will be rendered for this canvas element.
And of course you can align your text. Possible values are: start, end, left, right and center. The default value is start.
Also you can add the property textBaseline and there are also several possible options. For example, the values could be top, middle, bottom, ideographic or alphabetic. The default value is alphabetic.
Also this property doesn't mentioned on this slide but you can also add a property for direction. Possible values are left to right, right to left and inherit. And the default value is inherit.
Text has some methods. For example, you can fill text or you can stroke text. The difference between these methods is that fillText method create text the letters of which are filled with a color. And strokeText method creates a text which letters has only border so the letters don't have a color. It's just outlines and that’s all. 
Also one more interesting method is measureText. This method allows you to know the size (the width) of the text which you created using the styles which you used before. So if you want to know the width in pixels of the created text object you can use this method.

Slide (Canvas drawing)
So let's continue. Let's talk about canvas drawing. Actually canvas supports only one primitive shape, it is rectangles. But it is possible to draw any shape and we will talk about this later.

Slide (Steps)
So which steps are necessary to be done to create some element? First of all you should find the canvas element and usually you can do this using DOM. So in our example you can see how it is possible. For example, our canvas is equal document.getElementbyId and in the brackets is placed ID of our canvas. So we found our canvas and we can do anything with it. 
Then we can see quite interesting method. It is getContext method and in the brackets there is a value “2d”. And actually you can’t use some other values because it is only one which exists for now. Some developers tried to create and to use 3d canvas but actually it's impossible for now. So you don't have a choice for this method.
Then we should create a drawing object and we should draw it on our canvas. You can see fillStyle method here and this method show us how it is possible to give a color to our element. And then we create an element, a rectangle by using a fillRect method.

Slide (Canvas coordinates)
So let's talk about canvas coordinates. It is not usual for somebody, I think, because canvas coordinates are not the same as we used to see in math, for example. So canvas is a two-dimensional grid and the upper left corner of the canvas has the coordinates (0, 0).
If we look at our previous slide we can see that our rectangle has coordinates (0, 0). This means that this rectangle starts in the upper left corner of our canvas and this rectangle has the width 150 pixels and its’ height is 75 pixels. Let's continue.

Slide (Draw a line)
Let's talk about drawing a line.
It is also possible for canvas And actually canvas can be compared with a pencil, path of the drawing can be compared with a pencil.
Here we can see moveTo and lineTo methods. What do they mean? moveTo method moves the pencil to the starting position. So we can see that our starting position here is (0, 0), it is upper left corner of our canvas. And lineTo method defines the ending (the finishing) point for our line. So now we know starting and finishing position and we can draw a line using stroke method, for example.

Slide (Drawing paths)
So let's continue and talk about path. 
As I mentioned before the only possible primitive shapes are rectangles but you also can use paths. And path contains a list of points which connected by the lines and due to this connection you can create any shape you want. You can fill it with different colors or it could be just outlines or something like this. A path can be closed and you should do some actions to make shapes using this path.
Of course, you should create the path. For this action you should use beginPath method which helps you to create the path. And the closing method for path is closePath. This method adds a straight line to the path and goes to the start of the current path.
Then you should use drawing commands to draw into the path. For example, you can use stroke or you can use fill. I mentioned the difference between them, so stroke method creates the shape just by drawing its outlines and fill method creates a solid shape filled by some color. 

Slide (Draw a circle)
This is an example of a circle which can be drawn using canvas. Here we can see beginPath method and we can see arc method which defines that exactly a circle will be drawn on our web page. What 95 and 50 means? It is x and y position of the center of our circle, and the figure 40 means the radius of our circle. Then we just used stroke method which draws our circle.
In this case our circle will not be filled with the color so we will see just an outline of our circle.

Slide (Canvas gradients)
Also we can use gradients for canvas. It can be used to fill different shapes, it can be used for rectangles, for circles, for lines, for text, so for everything you drew on your canvas element.
You should use some specific methods for gradient creation. You can create linear gradient or you can create a radial gradient. The difference between them is the shape of gradient if it is possible to say so.

Slide (Linear gradient)
Let's look at an example of gradient. 
One more important thing is that you should add color stops for gradient. It is a method which defines the color values and the position of the colors on your shape. The position can be between 0 to 1. You can use the color which you use for usual CSS so it is not difficult.

Slide (Images)
Also you can add some images to your canvas. It is important to add an image only after the page is fully loaded. So you need to ensure that this image is loaded on your page before you draw this image. You can use existing image or you can create an image object using JavaScript. 
Here you can see an example of image adding to the canvas and this image is added to the canvas by the event window.onload so we can be sure that our image is already loaded.

Slide (Can be animated)
The most interesting feature of the canvas is that everything can be animated. You can use any animation you want. It is necessary to do some basic animation steps. So first of all you should clear the canvas. It is necessary to draw some other animated changes which you want to use. Then you should save the canvas state and after that you can draw animated shape so it will be the actual frame rendering. Then you can restore the canvas state. This means that you should restore the state before drawing a new frame. So it's like a loop: you clear the canvas, save, restore and do some other animation.

Slide (Method for animation)
This is an example of the animation which is used for canvas. There is no exactly animated code (the actions which were done for this canvas element) but there is a necessary method which is used for animation. It is requesAanimationFrame method which tells the browser to perform an animation. So we should use this method.
Let's look at our code. As I mentioned it is necessary to clear any shapes that have been drawn before. We can use clearRect method for this and it could help us to clear the canvas. Also it is necessary to make sure that the original state is saved if you change some style or do some transformations.

Slide (Thank you)
So that's all. It was like an intro to canvas. I hope that this information was interesting for you and if you have any questions feel free to ask me in the comments under this video. I will be glad to answer.
Thank you for your attention. Bye!
