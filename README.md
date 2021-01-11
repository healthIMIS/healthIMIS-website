## Jekyll notes ("cheat sheet")

- Prerequisites: https://jekyllrb.com/docs/installation/
- Quickstart: https://jekyllrb.com/docs/
- `jekyll build` - Builds the site and outputs a static site to a directory called _site.
- `jekyll serve` - Does the same thing except it rebuilds any time you make a change and runs a local web server at `http://localhost:4000`
- When you’re developing a site you’ll use `jekyll serve` as it updates with any changes you make.
- Templating Language: Liquid
  - objects (insert programmatic content): `{{ page.title }}`
  - tags (insert programmatic logic):
    ```
    {% if page.show_sidebar  %}
        <div class="sidebar">
            sidebar content
        </div>
    {% endif %}
    ```
  - filters: `{{ "hi" | capitalize }}` -> `HI 
- YAML page variables: Frontmatter
  - section at the top of a page, where variables can be declared, that can be used in Liquid
    ```
    ---
    title: Testpage
    show_sidebar: true
    ---
    ```