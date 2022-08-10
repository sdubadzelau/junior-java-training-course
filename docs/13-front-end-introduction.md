[![index.md](assets/back_main_page_icon_124174_32.png)](index.md) [Go to Contents](index.md)

## Introduction to Front-End
1. Introducing HTML
   1. HTML importance
   2. Basic HTML syntax
   3. Current HTML state
      1. What is the difference of HTML 5 and HTML 4?
         1. Browser support: HTML5 has browser support. It means even if some browsers are not supporting HTML5 you will be able to load a webpage on that browser.
         2. Geolocation: HTML5 provides a geolocation feature. With the help of the geolocation feature, we can insert or implement maps on our web pages for example world maps, etc.
         3. Web storage:  HTML provides two types of storage. There are two types of storages session storage( only available within the browser tab or window session ) and local storage ( localStorage is kept even between browser sessions)
         4. Footer: HTML5 provides a footer element The footer element is typically found at the bottom or foot of a webpage. It can contain copyright information, links to social media, and additional site navigation items.
         5. New Application Programming Interface (API): HTML5 features like 2D drawing on a web page, Drag and Drop, timed media playback, and browser history management.
   4. HTML resources
2. Basic Page Structure
   1. HTML document
   2. DOCTYPE declaration
      1. When authoring document is HTML or XHTML, it is important to Add a Doctype declaration. This makes sure the document will be parsed the same way by different browsers.
         The simplest and most reliable doctype declaration to use is the one defined in HTML5:
         ```
         <!DOCTYPE html>
         ```
         If you need a doctype matching a specific version of (X)HTML, the doctype declaration must be exact (both in spelling and in case) to have the desired effect, which makes it sometimes difficult. To ease the work, below is a list of recommended doctype declarations that you can use in your Web documents.
   3. `<html lang="en">`
   4. The document head
      1. `<meta charset="utf-8">` - better to have it for each page
      2. `<meta name="description" content="Page description">`
      3. `<title>Page Title</title>`
   5. The document body
   6. Content models
      1. HTML 4
         1. Block level elements - heading, paragraph tags
         2. inline level elements - bold tag, link
      2. HTML 5
         1. **Flow** - Most elements that are used in the body of documents and applications
         2. **Metadata** - is content that sets up the presentation or behavior of the rest of the content, or that sets up the relationship of the document with other documents, or that conveys other "out of band" information.
            `base, command, link, meta, noscript, script, style, title`
         3. **Embedded** - is content that imports another resource into the document, or content from another vocabulary that is inserted into the document.
            `audio, canvas, embed, iframe, img, math, object, svg, video`
         4. **Interactive** is content that is specifically intended for user interaction
            ```
            a, audio (if the controls attribute is present), button, details, embed, iframe, img (if the usemap attribute is present), 
            input (if the type attribute is not in the hidden state), keygen, label, menu (if the type attribute is in the toolbar state), 
            object (if the usemap attribute is present), select, textare, avideo (if the controls attribute is present)
            ```
         5. **Heading** - defines the header of a section (whether explicitly marked up using sectioning content elements, or implied by the heading content itself).
            `h1, h2, h3, h4, h5, h6, hgroup`
         6. **Phrasing** - 
            ```
            a (if it contains only phrasing content), abbr, area (if it is a descendant of a map element), audio,b, bdi, bdo, br, button, canvas, 
            cite, code, command, datalist, del (if it contains only phrasing content), dfn, em, embed, i, iframe, img, 
            input, ins (if it contains only phrasing content), kbd, keygen, label, map (if it contains only phrasing content), 
            mark, math, meter, noscript, object, output, progress, q, ruby, s, samp, script, select, small, span, strong, 
            sub, sup, svg, textarea, time, u, var, video, wbr, text
            ```
         7. **Section** is content that defines the scope of headings and footers.
            `article, aside, nav, section`
3. Formatting page content
   1. Special characters - `"<"`, `&lang;` `&copy;`, `&trade;`
   2. Controlling whitespace - any whitespace characters except first are ignored, To add space add `&nbsp;`
      `&nbsp;` connect word making them behave like one word.
4. Structuring content
   1. Using headings `h1`, `h2` etc.
   2. Nav element - `nav` - The <nav> tag defines a set of navigation links.\
      Notice that NOT all links of a document should be inside a `<nav>` element. The `<nav>` element is intended only for major block of navigation links.\
      Browsers, such as screen readers for disabled users, can use this element to determine whether to omit the initial rendering of this content.
   3. `article`, `section`
      1. `<article>` Tag: This tag contains independent content that doesn’t require any other context. So the <article> tag can be placed inside the main content.\
         But each of the articles will contain independent content within it.\
         Like YouTube use to contain different kinds of videos on a single page, each video is independent or you can see the course page of GeeksforGeeks each course is independent, each course can have its own page.
         * An article can have nested articles and that should refer to parent article.
         * Article tags are perfect for Microdata information.
      2. `<section>` Tag: This tag is used to split a page into sections like Introduction, Contact Information, Details, etc and each of these sections can be in a different `<section>` tag.\
         The `<section>` tag is introduced to wrap-up the things in a particular section.\
         The `<section>` tag divides the content into sections and subsections.\
         The section tag is used when requirements of two headers or footers or any other section of documents needed. Section tag grouped the generic block of related content.
         * A section can have nested sections
      3. `aside` - The `<aside>` tag defines some content aside from the content it is placed in.\ 
         The aside content should be indirectly related to the surrounding content.\
         Tip: The `<aside>` content is often placed as a sidebar in a document.\
         Note: The `<aside>` element does not render as anything special in a browser. However, you can use CSS to style the `<aside>` element (see example below).
      4. Using WI-ARIA roles - WAI-ARIA, the Accessible Rich Internet Applications Suite, defines a way to make Web content and Web applications
         more accessible to people with disabilities. It especially helps with dynamic content and advanced user
         interface controls developed with HTML, JavaScript, and related technologies.
         1. Roles - ARIA roles provide semantic meaning to content, allowing screen readers and other tools to present and support interaction with object in a way that is consistent with user expectations of that type of object. ARIA roles can be used to describe elements that don't natively exist in HTML or exist but don't yet have full browser support.