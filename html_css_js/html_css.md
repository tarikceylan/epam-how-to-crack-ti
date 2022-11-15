# **HTML and CSS Interview Questions**

## **Week 1**

---

## **1. HTML**

### **1. 1 What is Critical Rendering Path?**

**Critical Rendering Path(CRP)** is the sequence of steps the **browser** take in order to convert **HTML, CSS** and **JavaScript** into pixels. **Critical Rendering Path** includes DOM, CSSOM, render tree and layout

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
