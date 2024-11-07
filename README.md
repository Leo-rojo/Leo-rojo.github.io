# Portfolio Website
This is the source code of my portfolio website. I built it based on \[[minimal-light-theme](https://minimal-light-theme.yliu.me/)\] 
of [@Yaoyao Liu](https://github.com/yaoyao-liu), which, in turn, is based on [minimal](https://github.com/orderedlist/minimal).

The website is based on Jekyll, a static site generator, and it is hosted on GitHub Pages.

## Project Architecture

```
.
├── _data                    
|   ├── publications.yml                      # the YAML file for publications
|   └── projects.yml                          # the YAML file for projects
├── _includes                    
|   ├── publications.md                       # the Markdown file for publications
|   └── projects.md                           # the Markdown file for projects
├── _layouts                  
|   └── homepage.html                         # the html template for the homepage 
├── _sass
|   ├── minimal-light.scss                    # this file will be compiled into a CSS file to control the style of the page              
|   └── minimal-light-no-dark-mode.scss       # this file is similar to minimal-light.scss with the dark mode disabled
├── _pages                    
|   ├── about.md                              # the Markdown file for about section
|   ├── projects.md                           # the Markdown file for including _includes/projects.md
    └── publications.md                       # the Markdown file for including _includes/publications.md
├── _site                                     # compiled HTML files obtained through cmd 'bundle exec jekyll server'
├── assets                                    # some files
├── .gitignore                                # this file specifies intentionally untracked files that Git should ignore
├── CNAME                                     # the custom domain, will be used by GitHub page sevice
├── Gemfile                                   # a RubyGems related file
├── README.md                                 # the readme file (English)
├── _config.yml                               # the Jekyll configuration file, including some options of the page  
└── index.md                                  # the content of the index page, using Markdown
```

## Explanation of the Files
In a Jekyll project, `.yml` files are used to store variables and data that can be accessed by the HTML files through 
Liquid syntax, which allows for the insertion of dynamic content and the application of control logic. Here’s a breakdown of the key files and folders:
- `_config.yml`: This is the main configuration file for the Jekyll project. It’s where you set options like the site’s title, base URL, theme, plugins, and other global settings.
- `_data/`: This folder contains additional `.yml` files, such as:
  - `publications.yml`: Stores information about publications, like titles, authors, and publication dates.
  - `projects.yml`: Stores data about projects, such as project names, descriptions, and links. These data files are used to dynamically populate content on the site through Liquid syntax.
- `_pages/`: This folder stores `.md` files that define content for individual pages:
  - `about.md`: Contains the full content for the "About" page.
  - `projects.md` and `publications.md`: These are placeholders that include content from `_includes/projects.md` and `_includes/publications.md` through Liquid syntax.
- `_includes/`: Contains reusable content snippets in Markdown format, such as:
  - `publications.md`: Displays publication data by pulling in data from `_data/publications.yml`.
  - `projects.md`: Displays project data, similarly pulling in data from `_data/projects.yml`.
- `_layouts/`: Stores the main layout templates in HTML. Here there’s one template:
  - `homepage.html`: This layout template is applied to all the main pages, as specified in the front matter of the `.md` files in `_pages/`.
- `index.md`: This is the homepage, which redirects directly to `about.md`. It is located at the root of the project, separate from `_pages`.
- `_sass/`: Contains `.scss` files that are compiled into CSS, controlling the style of the site. Different .scss files can provide variations in themes (e.g., dark mode vs. light mode).
- `assets/`: This folder holds static assets, such as CSS files, images, JavaScript files, and other resources referenced by the pages on the site.

## How to Run the Project
1. Using GitHub Pages: GitHub Pages provides a server to host the website and automatically compiles the Jekyll project for you.
2. Running Locally:
   - Install Ruby and Jekyll on your local machine to compile and view the 
   project locally. Running jekyll build will produce the compiled site in 
   the `_site` folder, which can then be deployed to a server.
   - Alternatively, use the command: `bundle exec jekyll server --livereload`  This will 
   compile the project, serve it locally, and update automatically when you make changes, 
   allowing you to see real-time updates.