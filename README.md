# Bootstrap
### Learning Objectives

* Import the Bootstrap library into a project
* Understand and implement the bootstrap grid system
* Design an HTML mockup with the aid of Bootstrap  

## Intro to Front End Frameworks

During the cohort you will hear reference to the following terms:

- Libraries
- Frameworks

Its important to understand what each one does and their purpose in web development and/or software engineering.  

> Libraries - provide additional tools and functionality for your site/app and you pick the ones you need for that project. 

> Frameworks - are more opinionaited in how they are implemented, require a bit more setup but do provide a more organized structure when building out an app. 

<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 2min

Let's take a look at some of the most popular CSS Frameworks.

<!-- [10 JavaScript Libraries and Frameworks to Learn in 2020](https://learntocodewith.me/posts/javascript-libraries-frameworks/) -->

[Best CSS Frameworks](https://hackr.io/blog/best-css-frameworkshttps://hackr.io/blog/best-css-frameworks)


Now lets see how they compare to each other in the number of web sites implementing that technology. 

[https://www.similartech.com/compare/bootstrap-vs-foundation](https://www.similartech.com/compare/bootstrap-vs-foundation)


#### SEIR
In this program you will be learning or introduced to the following libraries/frameworks:

#### Libraries

- jQuery.js
- Chart.js 

#### Frameworks


**Front End**
- Bootstrap
- React.js 

**Back End**
- Express.js 
- Rails


<hr>


## Intro to Bootstrap

[Bootstrap](http://getbootstrap.com/) is a **front-end framework** created by a small team of developers at Twitter and maintained by a much larger community of contributors.


The framework consists of the following files:

- one main CSS file
- an optional theme CSS file
- a main JS file.

Bootstrap's JS library (pre v5) requires [jQuery](https://code.jquery.com/) to work, which is a JavaScript library.


#### Benefits Of Learning Bootstrap
Bootstrap is extremely popular and knowledge of at least one CSS framework is a very valuable skill to have (and totally worth putting on your resume). 

Bootstrap comes with a ton of features, including:

- Responsive Grid System 
- CSS library for quick and easy styling
- UI components - HTML + CSS 
  - navigation
  - buttons
  - forms
  - etc.
- Javascript widgets to make your page interactive
- Many...many..more

## Sites Using Bootstrap

As we saw earlier there are close to 4 million web sites built using Bootstrap. 
<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 2min

Let's take a moment and take a look at few of them: [sites-built-with-twitter-bootstrap/](https://www.creative-tim.com/blog/web-design/sites-built-with-twitter-bootstrap/)


Now lets specifically take a look at this one: 

- https://www.crit-research.it/it/


<hr>


## Including Bootstrap with HTML

To use Bootstrap, we need to include Bootstrap's CSS and Javascript libraries. We also need to include jQuery, as much of Bootstraps interactivity is implemented via jQuery. 


<hr>

#### <g-emoji class="g-emoji" alias="alarm_clock" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/23f0.png">⏰</g-emoji> Activity - 2min


Bootstrap is ever evolving and, as of 2020, is now at **v5.0.0-beta3**. 

<img src="https://i.imgur.com/OIlqEqD.png" width=500/>

<br>
<br>

Let's head over to [Bootstrap](https://getbootstrap.com/) and look over their docs to see how we can setup our project with Bootstrap. 
<hr>



<!-- ## What is Responsive Design?

**Responsive web design (RWD)** is an approach to web design aimed at crafting sites to provide an optimal viewing and interaction experience— easy reading and navigation with a minimum of resizing, panning, and scrolling—across a wide range of devices (from desktop computer monitors to laptops to cellphones).

A site designed with RWD adapts the layout to the viewing environment by using fluid, proportion-based grids, flexible images, etc..."

Source: [Wikipedia](https://en.wikipedia.org/wiki/Responsive_web_design) -->


## Responsive Grid System

Bootstrap takes a similar approach to CSS Grid (or better yet CSS Grid took a similar approach to Bootstrap).  A Bootstrap Grid is comprised of rows and columns. 

Columns are written in the following format as a **class attribute**: 

**col-(breakpoint)-(offset)** such as: `col-sm-4`

Columns are often wrapped into an element with a class of `row` and rows often wrapped in a `container`.

**container > row > column**

Bootstrap's grid system is based on the idea that a page layout for any given screen size is represented with 12 fluid **columns**.  


![grid](https://res.cloudinary.com/jkeohan/image/upload/v1515675398/Bootstrap-grid_jwulzb.png)



## Working with the Bootstrap Grid

### Containers, Rows and Columns

**Containers**

The class **container**  will center your content and leave a small margin on the left and right sides of the page. 

Use `.container` for a responsive, fixed-width container.

```html
<div class="container">
  ...
</div>
```

We can also opt for full width of the screen (no margin) using `class="container-fluid"`

```html
<div class="container-fluid">
  ...
</div>
```

**Rows**

Next we add a **row**, which is placed withing a container. 

Let's create our Grid. 
Create a row: 

  ``` html
  <div class="container">
   <div class="row"> ... </div>
  </div>
  ```

  **Columns**

  And finally we add a column. 

 ``` html
  <div class="container">
   <div class="row">
    <div class="col-md-6"></div>
   </div>
  </div>
  ```

  ## Breakpoints

The way that Bootstrap works is that it uses column sizes to dynamically respond to changes in window width.

To be mobile (and tablet!) -friendly, the columns will break into a stack layout after a minimum width is detected.

The breakpoints you can select in your columns control at which point this happens.

Check out their [documentation](https://getbootstrap.com/docs/3.4/css/#grid-options) here to see what these breakpoints are in terms of size.
  
  - col-xs < 768px (e.g. smartphones)
  - col-sm ≥ 992px (e.g. tablets)
  - col-md ≥ 1200px (e.g. laptops, desktops)
  - col-lg ≥ 1200px (e.g. large desktops, smart TVs)

<img src="https://i.imgur.com/BUnl8tC.png" width=500/>

#### Creating Columns
Here's an example of a two-column layout that spans the width of the page.  Notice that the widths of the two columns add up to 12.  The column content of any row must always be ≤12.

``` html
 <div class="row">
   <div class="col-md-6">
     <p>I'm a medium-sized column</p>
    </div>
   <div class="col-md-6">
     <p>Me too! We have SO much in common</p>
   </div>
 </div>
```

For other examples, check out the [Bootstrap docs](http://getbootstrap.com/css/#grid)  

#### Offsets

You can also offset and nest your columns. When you offset a column, you add a column of whitespace and push the column to the right.  Example:

``` html
 <div class="row">
   <div class="col-md-3 col-md-offset-3">
     <p>This column occupies 1/4 of the page width and is moved to the right 
     by 1/4 of the page width</p>
   </div>
 </div>
```


#### Nesting Grids

Here is an example of nesting columns (putting one row inside another)

``` html
 <div class="row">
   <div class="col-md-6">
     Level 1: Column takes 1/2 the width of the page
     <div class="row">
       <div class="col-md-4">
         Level 2: This column takes 1/3 the width of its parent column
       </div>
       <div class="col-md-8">
         Level 2: This column takes 2/3 the width of its parent column
       </div>
     </div>
   </div>
 </div>
```


## Typography
For a complete list: [Bootstrap Typography classes](http://getbootstrap.com/css/#type)

To align text, use these classes.  

``` html
 <p class="text-left">Left aligned text.</p>
 <p class="text-center">Center aligned text.</p>
 <p class="text-right">Right aligned text.</p>
 <p class="text-justify">Justified text.</p>
 <p class="text-nowrap">No wrap text.</p>
```
More useful typography classes...

``` html
 <p class="lead">This text will stand out in a paragraph</p>
 <small>This line of text is meant to be treated as fine print.</small>
 <p class="text-lowercase">Lowercased text.</p>
 <p class="text-uppercase">Uppercased text.</p>
 <p class="text-capitalize">Capitalized text.</p>
```


## Icons
Bootstrap comes with a set of icons that can be included in your page using the `<i></i>` tag. Check out these icons [here](https://getbootstrap.com/docs/5.0/extend/icons/#bootstrap-icons)

## Buttons
Bootstrap provides a wide selection of button sizes and colors.  Button classes can be applied not just to `<button>` elements, but also `<a>` and `<input>` elements

Sometimes you need to provide multiple classes to an element in order for Bootstrap to style it.  The button classes are an example of this:

``` html
 <!-- Standard button -->
 <button type="button" class="btn btn-default">Default</button>
 
 <!-- Provides extra visual weight and identifies the primary action in a set of buttons -->
 <button type="button" class="btn btn-primary">Primary</button>
 
 <!-- Contextual button for informational alert messages -->
 <button type="button" class="btn btn-info">Info</button>

 <!-- Indicates caution should be taken with this action -->
 <button type="button" class="btn btn-warning">Warning</button>
```  
... and so on.  See the [docs](http://getbootstrap.com/css/#buttons) for a comprehensive list of options.  Note you can add a third class denoting size to any of the above: `.btn-lg`, `.btn-sm`, `.btn-xs`


## Images 
Bootstrap helps you format images using `class="img-rounded"` (rounds the corners), `class="img-circle"` (makes the image a circle) and `class="img-thumbnail"` (adds a border). You can also add a `class="img-responsive"` to your image to make it scale well when the screen size changes (this sets its max-width to 100% of its parent element and the height to auto for maintaining aspect)

## Forms
Bootstrap is also very helpful when you need to style your forms. All textual `<input>`, `<textarea>`, and `<select>` elements with `class="form-control"` are set to width: 100% by default. Wrap labels and their associated controls (inputs) in `class="form-group"` for optimum spacing. 
 

## Javascript plug-ins
Bootstrap allows you to incorporate interactive behavior into your page with Javascript plug-ins.  While you would ultimately have to write some JS in order for these components to provide actual functionality within the application, you don't have to write JS if you're simply mocking up a UI.

Some examples:

- [Responsive Nav bars](http://getbootstrap.com/components/#navbar)
- [Dropdowns](http://getbootstrap.com/javascript/#dropdowns)
- [Popovers](http://getbootstrap.com/javascript/#popovers)
- [Modals](http://getbootstrap.com/javascript/#modals)
- [Carousels](http://getbootstrap.com/javascript/#carousel)

Always make sure you understand what the code is doing before copying and pasting it. Fortunately, this is not too challenging and Bootstrap has excellent documentation. As always, if you're confused or things are breaking - google around. Bootstrap is pretty much ubiquitous and it is likely that others have encountered and (hopefully) solved the issues you're dealing with.

## Conclusion
- Bootstrap is a library with CSS and JavaScript components.
- It gives us pre-styled stuff we can use to make our webpages look beautiful, as well as JavaScript for some common interactive elements like drop-downs and carousels. 
- Bootstrap also gives us a responsive **grid system**

## Putting it all together

Let's build something that looks more like a real website using Bootstrap.  Something more like this: 

<img src="https://i.imgur.com/XFAgJ7s.png" width=700/>

<details>
<summary>Solution</summary>

Will be provided after codealong

<!-- ```html

<nav class="navbar navbar-inverse navbar-fixed-top">
  <div class="container">
    <div class="navbar-header">
      <a class="navbar-brand" href="#">
        Hello World
      </a>
    </div>
    <div class="navbar-collapse collapse">

      <form class="navbar-form navbar-right" role="search">
        <div class="form-group">
          <input type="text" class="form-control" placeholder="Username">
          <input type="password" class="form-control" placeholder="Password">
        </div>
        <button type="submit" class="btn btn-success">Submit</button>
      </form>
    </div>
  </div>

</nav>
<div class="jumbotron">
  <div class="container">
    <h1>Hello, world!</h1>
    <p>Here is our awesome internet website</p>
    <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a></p>
  </div>
</div>

<div class="container">
  <div class="row">
    <div class="col-sm-4">
      <h3>Header</h3>
      <p>Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content
        Content </p>
      <p><a class="btn btn-success btn-sm">Learn More</a></p>
    </div>
    <div class="col-sm-4">
      <h3>Header</h3>
      <p>Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content
        Content </p>
      <p><a class="btn btn-success btn-sm">Learn More</a></p>
    </div>
    <div class="col-sm-4">
      <h3>Header</h3>
      <p>Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content Content
        Content </p>
      <p><a class="btn btn-success btn-sm">Learn More</a></p>
    </div>
  </div>
</div>
<div class="container">
  <hr/>
  <footer>
    <p>Made with love by WDI Ada.</p>
  </footer>
</div>
``` -->

</details>

## 🚀 Lab time!!!

Instructor will provide the lab. 
