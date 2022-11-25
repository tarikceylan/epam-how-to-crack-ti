# **HTML and CSS Interview Questions**

## **Week 1**

---

## **1. HTML**

### **1. 1 What is Critical Rendering Path?**

**Critical Rendering Path(CRP)** is the sequence of steps the **browser** take in order to convert **HTML, CSS** and **JavaScript** into pixels. **Critical Rendering Path** includes DOM, CSSOM, render tree and layout.

It's the minimal requirements for a document to render.

> **References:**
>
> - [Critical Rendering Path | MDN](https://developer.mozilla.org/en-US/docs/Web/Performance/Critical_rendering_path#:~:text=The%20Critical%20Rendering%20Path%20is,render%20path%20improves%20render%20performance.)

### **1. 2 How can I get indexed better by search engines?**

- **Use semantic HTML tags** which will allow search engines to index more related content.
- **Implement a responsive and mobile-friendly design**
- **Provide unique, high-quality** content
- **Update content** regularly
- **Submit a sitemap** to each search engine
- **Configure keywords** to allow search engines index properly
- **Track crawl status** using tools provided by the search engine
- **Exclude pages that is not related to your content from indexing** by configuring robots meta tags

> **References:**
>
> - [How Search Engines Work](https://moz.com/beginners-guide-to-seo/how-search-engines-operate)
> - [Improving Your Site's Indexing and Ranking](https://developers.google.com/search/blog/2006/02/improving-your-sites-indexing-and)
> - [How To Get Search Engines Index Right Content for Better Discoverability](https://search.gov/indexing/how-search-engines-index-content-better-discoverability.html)

### **1. 3 What is desktop first and mobile first design approach?**

In **Desktop First Design Approach**, the design is **based on a desktop machine** (a fixed computer, or a laptop) and then it is adapted for **mobile**. This adaptation process includes, resizing, changing the order or hiding of specific elements on the page. **This approach aims for the best user experience for desktop devices.**

In **Mobile First Design Approach**, the design is **based on a mobile device** and then it is ensured that responsive design can also be used on desktop. Certain elements can have more space or hidden elements can be shown. **This approach aims for the best user exprience for mobile devices.**

> **References:**
>
> - [Mobile or Desktop First Design?](https://toomba.com/en/blogs/mobile-or-desktop-first-design)

### **1. 4 How to make a page responsive?**

To make a responsive web page, there are several approachs we can consider.

- **Viewport Meta Tag** allow mobile browsers to set the document width with the same as mobile device width

```html
<meta name="viewport" content="width=device-width,initial-scale=1" />
```

- **Media queries** allow us to customize styles when certain size values are met on the viewport
- Layout technologies that helps to achieve responsive design approach
  - CSS Flexbox and Grid
  - Multiple-Column Layout
  - Using responsive images and typography

> **References:**
>
> - [Responsive Design | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

### **1. 5 What are the building blocks of HTML5?**

HTML5 building blocks consist of **semantics, connectivity, multimedia support, online and offline storage, performance and integration and styling** in a general sense. Some of those categories are provided by additions to HTML listed below.

- **Semantic HTML tags** which provide better accessibility and indexing for search engines
- **Form elements** that improve user experience and accessibility
- **Canvas and SVG** support to provide a cleaner interface
- **Geolocation API** which provides location information to the users
- **Web Workers** which improves performance and allow to run scripts on background threads.
- **Web Storage API** allow storing data in key/value pairs

> **References:**
>
> - [Building Blocks of HTML5 (Video)](https://www.youtube.com/watch?v=ObLwuNcyiQ8)
> - [Clearing your Front End Job Interview — HTML](https://codeburst.io/clearing-your-front-end-job-interview-html-706f8b2c7dca)

### **1. 6 When should you use section, div or article?**

`<section`, `<div>` and `<article>` tags are used for grouping content.The key differences about when they should be used is as follows:

- `<section>` can be used when a content is structured with a title, paragraph and other elements to support the current content which is related and makes sense with the rest of the page.
- `<article>` is almost same as `<section>` but the content should make sense by its own. It doesn't have to be related to the rest of the page.
- `<div>` is mostly used for grouping content when other grouping tags' requirements are not met. Such as anchors, buttons, etc.

> **References:**
>
> - [When to use Section vs Article vs Div (Video)](https://www.youtube.com/watch?v=swWeWesZVZU)
> - [HTML Elements `<section>` vs `<div>` vs `<article>`](https://medium.com/design-code-repository/html-elements-section-vs-div-vs-article-a8c34e6548cf)

### **1. 7 What are the semantic tags available in HTML5?**

`<main>`, `<header>`, `<footer>`, `<article>`, `<section>`, `<nav>`, `<aside>`, `<details>`, `<figcaption>`, `<figure>`, `<mark>`, `<summary>` and `<time>` are the main semantic HTML5 tags available

> **References:**
>
> - [Semantic HTML5 Elements Explained](https://www.freecodecamp.org/news/semantic-html5-elements/)

### **1. 8 Why would you like to use semantic tag?**

**Semantic HTML** provides an **easier to read** and **more consistent** HTML code, **better accesibility** and helps with **search engine indexing**

> **References:**
>
> - [Semantic HTML5 Elements Explained](https://www.freecodecamp.org/news/semantic-html5-elements/)

### **1. 9 What is accessibility? ARIA role means in a web application**

**Web accessibility** is the practice of ensuring that there are no limitations or blockages that prevent interaction with a website by people with any kind of disabilities or restrictions.

**Accessible Rich Internet Applciations(ARIA)** is a set of roles and attributes which improves accessibility for people with disabilities.

**ARIA roles** provide semantic meaning for the content of a website, allowing screen readers and other tools to ensure better user experience.

> **References:**
>
> - [Web Accessibility | Wikipedia](https://en.wikipedia.org/wiki/Web_accessibility)
> - [ARIA | MDN](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)

### **1. 10 What is the purpose of the alt attribute on images?**

`alt` attribute provide a text for an image. It can be used to **ensure to deliver an idea about the content on error**, **better accessibility** and **better indexing** for search engines.

> **References:**
>
> - [HTML alt Attribute](https://www.w3schools.com/tags/att_alt.asp)

### **1. 11 Define semantic markup. What are the semantic meanings for `<section>`, `<article>`, `<aside>`, `<nav>`, `<header>`, `<footer>` and when/how should each be used in structuring html markup?**

- `<section>` is used for grouping a content that makes sense with the rest of the page.
- `<article>` is used for grouping content which can make sense independently from the rest of the page.
- `<aside>` is used as a portion of the document when the content is indeirectly related to the main ocntent
- `<nav>` is used to provide and group navigation links
- `<header>` is used to represent a group introductory content or navigation elements
- `<footer>` usually contains information about the auther, copyright data and links to related documents

> **References:**
>
> - [HTML Elements Reference | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

### **1. 12 Describe the difference between a cookie, sessionStorage and localStorage?**

| Property            | Cookie             | Session Storage              | Local Storage                                               |
| ------------------- | ------------------ | ---------------------------- | ----------------------------------------------------------- |
| **Storage Size**    | Up to 4KB          | Up to 5MB                    | Up to 10MB                                                  |
| **Readble From**    | Client & Server    | Client                       | Client                                                      |
| **Expiration**      | Configured by Code | Session Based(Window or Tab) | No expiration, must be deleted manually or using JavaScript |
| **Browser Support** | More Support       | Less Support                 | Less Support                                                |

> **References:**
>
> - [Difference Between `localStorage`, `sessionStorage` and `cookie` | StackOverflow](https://stackoverflow.com/questions/19867599/what-is-the-difference-between-localstorage-sessionstorage-session-and-cookies)

---

## **2. CSS**

### **2. 1 What are the possible ways to apply CSS styles to a web page?**

There are three methods to apply a CSS style to a web page.

- **Linked**
  CSS rules are stored in a seperate file and `<link>` tag is used to refer to that file inside the `<head>` element.

```HTML
    <link rel='stylesheet' type='text/css' href='style.css'>
```

- **Embedded**
  CSS rules are defined inside the HTML document's `<head>` element within the `<style>` tag
  **Note:** This approach should be kept to a minimum.

- **Inline**
  CSS rules are inserted into HTML tags as an attribute

> **References:**
>
> - [Applying CSS to HTML](https://en.wikibooks.org/wiki/Cascading_Style_Sheets/Applying_CSS_to_HTML_and_XHTML)

### **2. 2 What does the cascading portion of CSS mean?**

**Cascading** in CSS describes an algorithm which determines defined CSS rule priorities and which rules to apply depending on provided selectors across multiple styling resources.

> **References:**
>
> - [Introducing the CSS Cascade | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)

### **2. 3 What is CSS preprocessor?**

A **CSS Preprocessor** is a program which generates CSS from its unique syntax that allows developers to have more functionality compared to basic CSS.

> **References:**
>
> [CSS preprocessor | MDN](https://developer.mozilla.org/en-US/docs/Glossary/CSS_preprocessor)

### **2. 4 What are media queries?**

**Media queries** is used for applying different CSS rules for different screen resolutions or viewport width.

> **References:**
>
> [Using Media Queries | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)

### **2. 5 What does `box-sizing` do?**

`box-sizing` property is used to determine how the total width and height of an element is calculated.

> **References:**
>
> [Box Sizing | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing)

### **2. 6 Explain some pros and cons for CSS animations versus JavaScript animations**

**CSS Animations** can be created using **transitions** or **keyframes** are easier to implement, they can porivde smoother visuals and can be optimized by the browser for performance for simple animations. However, they do not perform well for advanced animations.

**JavaScript Animations** are more efficient as the desired effect complexity increases. Although they become more complex than writing CSS animations

> **References:**
>
> - [Animations: CSS vs JavaScript](https://medium.com/neocoast/animations-css-vs-javascript-226903d6976a)
> - [CSS and JavaScript Animations Performance | MDN ](https://developer.mozilla.org/en-US/docs/Web/Performance/CSS_JavaScript_animation_performance)

### **2. 7 What is theming? How to respond on the system theme change?**

**Theming** is giving end-users the ability to make custimizations on websites or web apps.

We can store theme preference with client information and provide the prefered configurations on request.

> **References:**
>
> - [Website Theming with CSS Custom Properties](https://www.freecodecamp.org/news/website-theming-with-css-custom-properties-and-gatsbyj)

### **2. 8 How to make images responsive?**

- Changing image resolution with `media-queries`
- Set relative units based on the viewport (`vw`, `vh` etc.) rather than absolute units (`px`, `in` etc. ).
- Using `srcset` and `sizes` attributes in the `<img>` tag

> **References:**
>
> - [Responsive Images | MDN ](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images)

### **2. 9 Explain CSS grid layout with example**

**CSS Grid Layout** is used for dividing a page into grids which allows developers to use a column-row like structure.

**For example:** We can use grid system to layout a blog page. The navigation links would be on the top, under it there would be main content on the right hand side and more information about the website map, categories etc. on the left hand side.

> **References:**
>
> - [CSS Grid Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)

---

## **Week 2**

---

## **1. HTML**

### **1. 13 Ways to improve website performnace**

As far as HTML is concerned there are few ways to improve a website performance.

- **Optimizing image size** is one of the first steps that could be taken for optimizing performance which includes **compressing images**, implementing **responsive design**, **formatting images in `JPEG` for images with wide color palettes**
- **Using CDN (Content Delivery Network)** is benefitial when we need to serve static files on the website like fonts, images, huge css files etc. Hosting them on our website would defeat the purpose of a static website and could cause performance issues. CDN will optimize the delivery of said static files using a 3rd party's infrastructure.
- **Minification and Bundling** can also help with increasing performance.
  - **Minification** is optimizing the size of JavaScript and CSS files by removing or shortening the characters in the source code. The functionality doesn't change but it becomes relatively non-readable by humans evevn though theye can be perfectly read by browsers.
  - **Bundling** is the process of combining JS and CSS files together into a single file which reduces the size. This process will help to decrease the number of file requests and improve performance.
- **Caching** is the process of saving a specific version of the content into temporary storage which allows the browser to access the content faster if there is no change. This method is mostly preferable for static websites which doesn't require real-time interaction with the end user.

> **References:**
>
> [Improve Website Performance](https://sematext.com/blog/improve-website-performance/)

### **1. 14 What does `async` and `defer` refer in script tag? Describe the difference between `<script>`, `<script async>` and `<script defer>`**

`<script>` tag freezes the building of DOM when a page is being loaded which leads to problems like script not being able to access the elements that comes after it or entire failure of loading a page if there is a bulk script blocking the page at the top.

We can workaround this problem by using `<script>` tag at the end of the page body but this might also cause some delay when loading the script if the HTML document is too long.

`defer` and `async` attributes help us to solve this problem.

- `defer` attribute tells the browser not to wait for the script. The browser continues to process the HTML and loads the script in the background. When DOM is fully built and ready, script is ran.

- `async` attribute indicates that the script is completely independent. These scripts also loads in background like `defer`. Only difference is `async` scripts are ran when they're ready.

> **References**
>
> [`async` and `defer` | JavaScript.info](https://javascript.info/script-async-defer)

### \*\*1. 15 What is an iframe and how does it work?

**iframe** is an HTML element represents another embedded HTML element which has its own session history and `document`.

`<iframe>` tag can have a source attribute which will point to another HTML document.

```HTML
<iframe id="inlineFrameExample"
    title="Inline Frame Example"
    width="300"
    height="200"
    src="https://www.openstreetmap.org/export/embed.html?bbox=-0.004017949104309083%2C51.47612752641776%2C0.00030577182769775396%2C51.478569861898606&layer=mapnik">
</iframe>
```

> **References**
>
> [iframe | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/iframe)

### **1.16 Explain the use of rel="nofollow", rel="noreferrer", rel="noopener" attribute?**

`rel` is sued to define a relationship between a linked resource and the current document

- `nofollow` option indiates that the auther of the current document does not endoerse the referenced document
- `noreferer` option is used to protect the information about where request is originating from to resource.
- `noopener` option is used to limit the access to the original window object.
  > **References**
  >
  > [`rel` attribute | MDN ]()

### **1. 17 Explain the use of rel="preload", rel="prefetch", rel="preconnect" attribute?**

- `rel='preload'` is used whenever we need a resource to be loaded early in the page lifecycle before the rendering engine kicks in. This ensures that the resource will be available and less likely to block rendering which improves performance.

- `rel='prefetch'` has a lower priority compared to `preload`. It allows the browser to fetch resources in the background which might be needed later and stores thme in its cache.

- `rel='preconnect'` allows the browser to setup early connections even before an HTTP request is sent to the server which could save time on whole request response lifecycle

> **References**
>
> [Resource Hints](https://www.keycdn.com/blog/resource-hints)

### **1. 18 What does CORS stand for and what issue does it address?**

**CORS** stand for Cross-Origin Resource Sharing which is an HTTP-header based mechanism. It solves the problem when a reasource request from a different origin other than the one its own.

> **References**
>
> [CORS | MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS)

### **1. 19 What is the DOM? How does the DOM work?**

**DOM (Document Object Model) is the representation of the elements and objects that structures a page on the web. **DOM\*\* represents the elements of the document as objects which are interactable by programming languages.

> **References**
>
> [What is DOM? | MDN](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

---

## 2. CSS

### **2.10 What are the css selectors?**

**CSS Selectors** are used to target a specific HTML elements which the css rules should be applied. They can be used to select a certain group of elements, like all `h1`s, or specific ones like `img` element with the logo id.

> **References**
>
> [CSS Selectors | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Selectors)

### **2.11 When to use css grid and flexbox?**

For starters, both CSS `grid` and `flexbox` is helpful to have a responsive design.

- `grid` is used more for complex layout structures in two dimensions.
- `flexbox` is useful for responsive and maintainable designs with simpler, one-dimentional layouts.

> **References**
>
> [CSS Flexbox vs Grid](https://blog.logrocket.com/flexbox-vs-css-grid/)

### **2.12 What is CSS BEM?**

**BEM (Block Element Modifier)** is a methodology that helps you create reusable components. It uses blocks, elements and modifiers to create modular architecture.

> **References**
>
> [Introduction | BEM Official Website](https://getbem.com/introduction/)

### **2.13 Explain the CSS “box model” and the layout components that it consists of**

When browser is rendering the lay out of a document, its rendering engine represents each element as a standard CSS box model. Every box is composed of four areas :

- **Content Area** is bounded by content edge and contains the content of the element.
- **Padding Area** is bounded by padding edge and extends the content area to include element's padding.
- **Border Area** is bounded by border edge and extends the padding area to include element's borders
- **Margin Area** is bounded by margin edge and extends the border area to include an empty area between elements

> **References**
>
> [Intorduction to CSS Box Model | MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)

### **2.14 What is CSS flexbox?**

`flexbox` is a one-dimensional layout method for arranging items in a row-column structure. Every element or item "flex" to fill or shrink to fit in its container

> **References**
>
> [Flexbox | MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox)
