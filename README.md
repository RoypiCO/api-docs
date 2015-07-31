Api docs
========

Roypi's API documentation.

Getting Started
---------------

### Prerequisites

You're going to need:

 - **Ruby, version 1.9.3 or newer**
 - **Bundler** — If Ruby is already installed, but the `bundle` command doesn't work, just run `gem install bundler` in a terminal.

### Getting Set Up

 1. Fork this repository on Github.
 2. Clone *your forked repository* (not our original one) to your hard drive with `git clone https://github.com/YOURUSERNAME/slate.git`
 3. `cd api-docs`
 4. Install all dependencies: `bundle install`
 5. Start the test server: `bundle exec middleman server`

You can now see the docs at <http://localhost:4567>. And as you edit `source/index.md`, your server should automatically update! Whoa! That was fast!


How to edit
-----------

This is a reference for the Markdown syntax used in Slate.

### Headers

For headers:

    # Level 1 Header
    ## Level 2 Header
    ### Level 3 Header

Note that only level 1 and 2 headers will appear in the table of contents.

### Paragraph Text

For normal text, just type your paragraph on a single line.

    This is some paragraph text. Exciting, no?

Make sure the lines above below your paragraph are empty.

### Code Samples

For code samples:

```
	```ruby
	# This is some Ruby code!
	```

	```python
	// This is some Python code!
	```
```

Code samples will appear in the dark area to the right of the main text. We recommend positioning code samples right under headers in your markdown file.

For the full list of supported languages, see [rouge](http://rouge.jayferd.us/demo).

### Code Annotations

For code annotations:

    > This is a code annotation. It will appear in the area to the right, next to the code samples.

Code annotations are essentially the same thing as paragraphs, but they'll appear in the area to the right along with your code samples.

### Tables

Slate uses PHP Markdown Extra style tables:

```markdown
Table Header 1 | Table Header 2 | Table Header 3
-------------- | -------------- | --------------
Row 1 col 1 | Row 1 col 2 | Row 1 col 3
Row 2 col 1 | Row 2 col 2 | Row 2 col 3
```

Note that the pipes do not need to line up with each other on each line.

If you don't like that syntax, feel free to use normal html `<table>`s directly in your markdown.

### Formatted Text

    This text is **bold**, this is *italic*, this is an `inline code block`.

You can use those formatting rules in code annotations, tables, paragraphs, lists, wherever.

### Lists

    1. An
    2. Ordered
    3. List

    * A
    * Bullet
    * List

### Links

    This is an [internal link](#error-code-definitions), this is an [external link](http://google.com).

### Notes and Warnings

You can add little highlighted warnings and notes with just a little HTML embedded in your markdown document:

    <aside class="notice">
    You must replace `meowmeowmeow` with your personal API key.
    </aside>

Use `class="notice"` for blue notes, `class="warning"` for red warnings, and `class="success"` for green notes.

You can also to [change appearance](https://github.com/RoypiCO/api-docs/wiki/Custom-Themes), [customize language tab](https://github.com/RoypiCO/api-docs/wiki/Customizing-the-Language-Tabs) or make a [deeper nesting](https://github.com/RoypiCO/api-docs/wiki/Deeper-Nesting), see more on [the wiki](https://github.com/RoypiCO/api-docs/wiki).


How to publish (only for project members)
-----------------------------------------

 1. Commit your changes to the markdown source: `git commit -a -m "Update source"`
 2. Push the *markdown source* changes to Github: `git push`
 3. Add "gh-pages" (only the first time) as a local branch pointing to the remote ([GitHub doc](https://help.github.com/articles/creating-project-pages-manually))
 4. Run `rake publish`: Compile to HTML, and push the HTML to Github pages.

Done! Your changes should now be live on [http://docs.roypi.com](http://docs.roypi.com/), and the master branch should be updated with your edited markdown.
