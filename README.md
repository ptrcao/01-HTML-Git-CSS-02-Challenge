# Readme.md for 01-HTML-Git-CSS-02-Challenge (by Peter Cao)

This Readme.md documents my response to 01-HTML-Git-CSS-02-Challenge and includes relevant links and resources.

URL for public repository containing the completed task for this challenge: <a href="https://github.com/ptrcao/01-HTML-Git-CSS-02-Challenge.git">https://github.com/ptrcao/01-HTML-Git-CSS-02-Challenge.git</a>

URL to the deployed refactored webpage: URL to the deployed refactored webpage: <a href="https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/">https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/</a> - or more precisely - <a href="https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/index.html">https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/index.html</a>


## Response to Acceptance Criteria

> GIVEN a webpage meets accessibility standards<br/>
> WHEN I view the source code

I have viewed the source code in Visual Studio Code and also using developer panel in Chrome.
> THEN I find semantic HTML elements
1. Changed div to semantic element:

    a. HTML: `<div class="header">` -> `<header></header>`

    b. CSS: all instances of `.header` -> `header`

1. Changed div to semantic element:

    a. HTML: `<div>` -> `<nav></nav>`

    b. CSS: `header div` -> `header nav`, `header div ul` -> `header nav ul`, `header div ul li` -> `header nav ul li`

2. Changed div to semantic element:

    a. HTML: `<div class="footer">` -> `<footer></footer>`

    b. CSS: `.footer` -> `footer`
3. Changed div to semantic element: 

    HTML: `<div></div>` -> `<section></section>`

4. Changed div to semantic element:

    a. HTML: `<div class="content"></div>` -> `<main></main>`

    b. CSS: `.content` -> `main`

5. Changed div to semantic element: 

    a. HTML: `<div class="benefits"></div>` -> `<aside></aside>`

    b. CSS: `.benefits` -> `aside`
> WHEN I view the structure of the HTML elements<br/>
> THEN I find that the elements follow a logical structure independent of styling and positioning

The following shows the logical, hierarchical structure of this html page after refactoring:
```
<html>
  <head>
    <title>
    </title>
  </head>
  <body>
    <header>
      <h1>
      </h1>
      <nav>
      </nav>
    </header>
    <main>
      <section>
        <h2>
        </h2>    
      </section>
      <section>
        <h2>
        </h2>   
      </section>
      <section>
        <h2>
        </h2>
      </section>
    </main>
    <aside>
      <section>
        <h3>
        </h3>   
      </section>
      <section>
        <h3>
        </h3>   
      </section>
      <section>
        <h3>
        </h3>   
      </section>
    </aside>
    <footer>
        <h4>
        </h4>       
    </footer>
  <body>
</html>
```

> WHEN I view the icon and image elements<br />
> THEN I find accessible alt attributes

alt attribute has been added for images with the name of the image file as the value to indicate to viewer the placement of an image in case of retrieval failure.

> WHEN I view the heading attributes<br />
> THEN they fall in sequential order

`<h1></h1>`, `<h2></h2>`, `<h3></h3>` and `<h4></h4>` follow a natural hierarchy based on their parent elements `<header></header>`, `<main></main>`, `<aside></aside>` and `<footer></footer>` respectively:
```
<header>
  <h1></h1>
</header>

<main>
  <section>
    <h2></h2>
  </section>
</main>

<aside>
  <section>
  <h3></h3>
  </section>
</aside>

<footer>
  <h4></h4>
</footer>
```

> WHEN I view the title element<br/>
> THEN I find a concise, descriptive title

Changed from generic to descriptive title: `<title>website</title>` -> `<title>Horiseon Web Marketing and SEO Services</title>`



## Satisfies all of the preceding acceptance criteria plus the following code improvements:

> Application's links all function correctly.

Link fixed: class="search-engine-optimization" changed to id="search-engine-optimization" to fix a broken link.

> Application's CSS selectors and properties are consolidated and organized to follow semantic structure.

  In the CSS file, I have:

  a. Consolidated `.benefit-lead, .benefit-brand, .benefit-cost` as they share the exact same styling

  b. Consolidated `.benefit-lead h3, .benefit-brand h3, .benefit-cost h3` as they share the exact same styling

  c. Consolidated `.benefit-lead img, .benefit-brand img, .benefit-cost img` as they share the exact same styling

  d. Consolidated `.search-engine-optimization, .online-reputation-management, .social-media-marketing img` as they share the exact same styling

  e. Consolidated `.search-engine-optimization img, .online-reputation-management img, .social-media-marketing img` as they share the exact same styling

  f. Consolidated `.search-engine-optimization h2, .online-reputation-management h2 and .social-media-marketing h2` as they share the exact same styling

Furthermore, several `<div>` tags were replaced with semantic HTML tags in line with HTML accessibility practices, in the HTML file, and any redundant/unused classes were then removed.  Corresponding edits needed to be made in the CSS file so that the relevant selectors were replaced with semantic element selectors.  These included replacing various div and class CSS selectors with the following semantic elements:

* `<header></header>`
* `<nav></nav>`
* `<footer></footer>`
* `<section></section>`
* `<main></main>`
* `<aside></aside>`

> Application's CSS file is properly commented.

  I have made use of `/* Comments go here */` within, to include comments that track the changes made in the CSS file.


## Repository Setup and GitHub Pages deloyment

A remote repository was created, cloned to a local folder.  Work on the project then proceeded locally and commits were intermittenly pushed to the Github cloud.
Once the refactoring project was complete, Page deployment was enabled in GitHub Settings.

1. URL for public repository containing the completed task for this challenge: <a href="https://github.com/ptrcao/01-HTML-Git-CSS-02-Challenge.git">https://github.com/ptrcao/01-HTML-Git-CSS-02-Challenge.git</a>.

2. URL to the deployed refactored webpage: <a href="https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/">https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/</a> - or more precisely - <a href="https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/index.html">https://ptrcao.github.io/01-HTML-Git-CSS-02-Challenge/index.html</a>.


## Screenshot
Screenshot of the final deployed, refactored website (the img is linked directly to the repository's copy):

<img src="./assets/images/Final Screenshot of Refactored Website as Deployed Live.png" alt="Final Screenshot of Refactored Website as Deployed Live.png"/>


## Additional improvements of my own initiative
1. Demonstrated advanced use of readme markdown to format this readme file.
2. It turned out that having the classes seemed redundant, as there was only one instance of elements using the classes, so all references to classes in the html and CSS were removed for the following and supplanted with just the id equivalent.
In the HTML:
* `class = "online-reputation-management"` changed to `id = "online-reputation-management"`
* Redundant `class = "social-media-marketing"` removed
* Redundant `class = "search-engine-optimization"` removed

In the CSS:
* `.online-reputation-management` changed to `#online-reputation-management`
* `.social-media-marketing` changed to `#social-media-marketing`
* `.search-engine-optimization` changed to `#search-engine-optimization`