## This is a library that allows you to align display objects relative to one another
Calculate the x and y position of a child display object relative to the parent. 

Relationships: center, left, right, top, or bottom 

Get a calculation by passing in the display object or passing in numbers. 

If you pass in the display objects, the x and/or y positions of the child will get set. 

You have the option to add the child to the parent.
   
This library works with any javascript display objects that have these properties/methods: x, y, width, height, addChild. You can use it with frameworks like PIXI and Phaser.

#### Relations
![Consts](/assets/consts.png)

#### An example
![Example](/assets/example2.png)

#### How to determine whether to make the padding pos/neg when using CENTER align
![Center Padding](/assets/center-padding.png)

## Code

The functions in the Align library are static. This mean you do not need to instantiate the class. You can just call it like: LibraryName.functionName().

In your index.html, add a script tag to include the version of the align.min.js file that you want from the [dist/](/dist) directory. You will be able to use the library within your code without needing to import it.

    myFunc() {
        let parent = new Sprite();
        let child = new Sprite();

        Align.alignX(parent, child, Align.CENTER, 5, true);
    }    

## Unit tests
The tests are [here](/test/Align.spec.js).

Please open an [issue](https://github.com/genradley/JSDisplayObjectAlignment/issues) if you find any bugs. We will fix the issue and add a test for it.

## JSDocs
Please download or fork the repo and open [/docs/index.html](/docs/index.html) in a web browser

I am currently figuring out how to run jsdocs with webpack so you will not see the jsdoc plugin in the webpack.config.js as of yet. The docs here were generated with grunt in another project structure.  
## Credits
This project used the [webpack-library-starter](https://github.com/krasimir/webpack-library-starter) project