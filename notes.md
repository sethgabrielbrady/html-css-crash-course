# Agenda

1. Basics of html
  * Hyper Text Markup Language. HyperText" refers to links that connect webpages
    to one another, either within a single website or between websites. HTML uses
    "markup" to annotate text, images, and other content for display in a Web browser.
    Is not a programming language; it is a markup language
  * Most basic building block of the Web

2. Discuss the Purpose of html + Demonstrate Tags, Nesting, Attributes
    * Is used to tell your browser how to structure the webpages you visit.
    It can be as complicated or as simple as the web developer wishes it to be.
    HTML consists of a series of elements, which you use to enclose, wrap, or
    mark up different parts of the content to make it appear a certain way, or
    act a certain way. The enclosing tags can make a bit of content into a
    hyperlink to link to another page on the Web, italicize words, and so on.

    * ``<p>Example: Donuts taste good.</p>`` ``-- a tag``

      * HTML tags are the boxes around the content. Sometimes, you need to
      places boxes inside of other boxes. Those "inner" boxes are nested
      inside of others.

    * ``<p>Example: Actually, donuts taste <strong>great</strong>!.</p>```` -- a nested``

      * Elements in HTML have attributes; these are additional values that
      configure the elements or adjust their behavior in various ways
      to meet the criteria the users want.

    * ``<a href="http://giphy.com/gifs/homer-simpson-fat-mumu-EexPHv9B84xRC"><img src="images/logo.png"></a>``

      * Here, 'href' and 'src' are attributes of their tags ('a' and 'img')


3. Demonstrate Structure of a Document

``` html

<html> // The html tag indicates that this is an HTML document

	<head> // The head element is the first element to appear after the opening html tag.
    In the document head we place things like the page title and meta data,
    we add JavaScript to our page with the script tag, and we [link] to external
    stylesheets and other resources.

Read more: http://html.com/document/#ixzz4kV9BT2y4

		<title>The Doughknot Shoppe</title> This is the title of the webpage.
		<link rel="stylesheet" type="text/css" href="css/style.css">  This links our HTML document to our CSS files. Notice the attribute tags.


	</head>

	<body> // The body element contains the information that you want to display on a web page.

		<header>  The header element is used to contain the content that appears at
      the top of every page of your website: the logo, tagline, search prompt,
      and possibly a navigational menu. In most cases, the header element is best
      positioned as a direct descendant of the body element, but it’s also ok
      to place it inside the main element if you prefer.

      <nav> Navigational menus are commonly placed at the top of a web page,
        in a sidebar, or in the page footer. Wherever you happen to place a
        navigational menu, wrap it in nav tags. Note that you don’t need to use
        nav tags for every link, just for blocks of links that provide either
        sitewide navigation or navigation for a specific part of a website.


			</nav>

		</header>

		<main> /Use the main element between header and footer elements to contain
      the primary content of your web page. The main element cannot be a descendant
      of an article, aside, header, footer, or nav element. Instead, it should be a
      direct descendant of the body element. Think of it as the direct replacement
      for the div id="main" you’ve used in the past to wrap up your entire page contents.
    </main>

		<footer> The footer appears at the bottom of a section of a document.
      Typically, the footer is a direct descendant of the body element, but
      it can also be used within a main element, a section, or an article.
      The most common use of the footer element is to place it at the bottom of
       an HTML document to contain things like a copyright notice, links to
       related content, address information about the owner of the website,
       and links to administrative things like privacy policies and website’s
       terms of service.
		</footer>

	</body> // This is where the body and the information that is seen by the user ends.
</html> //this marks the end og the HTML document

 ```

4. Demonstrate Links
  * What is a link? A link is a way for the page to tell the browser to take the user to another
    website or elsewhere within the site itself.

  ``` html
    <a href="http://giphy.com/gifs/homer-simpson-fat-mumu-EexPHv9B84xRC"><img src="images/logo.png"></a>``
  ```

5. Discuss Basics of css
  * CSS -Cascading Style Sheets. A CSS file allows you to separate your web sites
    HTML content from it’s style. CSS can be used internally (within the HTML) or
    externally(inside a seperate linked style sheet).
    It is called Cascading because the CSS is interpreted from the top down. If
    you style the exact same element in a page with differenct bits of code, the browser
    will default to the most recent or last style. Top >>> Down

    What defines how the HTML looks and sometimes be have a CSS ``rule``.

    This is an example of a rule. Let's break it down.

  ``` css

    p {
      color: purple;
      font-size: 1em;
      border: 1px solid green;
    }

  ```

    The `` p `` here is the selector. You can think of it as what the ``rule`` is
      ``selecting`` to style. Next are the ``{} ``. You can see one directly next
        ``selector`` p and another at the very end of the rule. Between these is
        where will put the ``declarations``. The declarations are the style elements
        of the rule. They tell the browser how to style a specific element. A ``declaration``
        is made of two parts: A   ``property`` and a ``value``.
        ``font-size`` is the property and ``1em`` is the value. Notice that separating
        them is a colon and ending the declaration is a semi-colon. These MUST
        be inside each an every declaration. The rule is then close with the ``}``
        and all you the ``<p>`` tag elements inside your HTML documents will have a
        font-size of 1em, be purple, and have a green border surrounding them. To style
        individual or just a few elements of the same type, a class attribute with
        a name will need to be used then called inside the selector. This is a talk for
        another day ..



6. Demonstrate css Basics

7. Use css Basic Properties

8. Explain css Defaults
  If styles arent specified, the browser will default to basic black text with a
  white background. Any images will be displayed inline relative to where they where
  placed in the document and their size. Also remember that if the style sheet has
  more than one rule for any given element, ie more than one rule hase been given
  the same selector, then CSS will default the the last (closest to the bottom of
  the stylesheet) rule. If you want to style more than one of the same type of element
  with differing style, you must use classes.

  * Classes
    Classes are reusable styles that can be added to HTML elements. If you want
    an element or elements to be styled in differently than elements of the same
    type, you will make a CSS Class.

  ``` html
  <h2 class="blue-text">Blue Steel</h2>

  ```
  This is an example of a class being applied to an HTML element.

  ``` css
  .blue-text {
  color: blue;
  }

  ```
  And this is an example of the CSS Rule. ``.blue-text`` is the selector. Note
  the ``` . ``` proceeding the class name. This tells the browser that the selector
  is a class and not an HTML tag. Now, any text within an HTML element with the
  "blue-text" class will show up as blue.

  ``` html
  <h2 class="blue-text">Blue Steel</h2>
  <p> Blue Steel</p>
  <main class="blue-text"> Red Steel </main>

  ```





+ Discuss Basic Selector Strategy





Project Challenge
Build a page with html and css
Second Project Challenge (Intro to JavaScript and jQuery)
Improve your project with a little JavaScript and jQuery
Stick around for networking


Build a page with html and css
Second Project Challenge (Intro to JavaScript and jQuery)
Improve your project with a little JavaScript and jQuery
Stick around for networking




http://html.com/document/#ixzz4kV8jskFx
