# My Resume (WebPage)

## Purpose

This README provides a detailed, step-by-step guide for hosting a resume website using Pelican and GitHub Pages. It is intended for professionals who may not have much technical experience, so if you are someone who uses software like Excel, QuickBooks, or emails every day, but lacks a background in programming, this guide will help you use simple tools to create and host a professional resume online. No programming experience is required—just follow the instructions, and you’ll have a resume website up and running in no time.
Moreover, we've mentioned Etter’s Principle for every instruction mentioned in Andrew Etter’s Modern Technical Writing

## Prerequisites

Before you begin, make sure you have the following resources:

### GitHub account
A GitHub account is required to host your site on GitHub Pages. If you don’t already have one, sign up at [GitHub](https://github.com/).

### Python (3.x)
Pelican, the static site generator used for this project, requires Python. Python is a programming language, but for this project, you only need to install it and use it to run Pelican. Download it from [Python’s website](https://www.python.org/downloads/).

### Git
Git is a version control tool that will help you track changes and push your website files to GitHub. If you don't have Git installed, you can get it at [Git’s website](https://git-scm.com/). Git is useful for managing changes to your site, but you won't need to understand it deeply to follow this guide.

### Pelican Static Site Generator
Pelican is a tool that takes your resume (written in Markdown format) and turns it into a website. It’s simple to use, even if you have no programming experience. Install it by following the instructions [here](https://docs.getpelican.com/en/latest/install.html).

### Basic Markdown knowledge
Markdown is a lightweight markup language used for formatting text. It’s similar to writing in plain text, but you use simple symbols to add formatting like headings, bold text, or lists. If you’re familiar with formatting emails or writing reports, you’ll find Markdown easy to learn. For a beginner’s guide to Markdown, visit the [Markdown Guide](https://www.markdownguide.org/).

### Text editor
A text editor is needed to write and edit your content. Popular options include [VS Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or even Nano (a simple editor that works in the command line).

## Instructions

### Step 1: Install Required Software
**Etter’s Principle: Use existing tools instead of reinventing the wheel.**

Run these commands to install Pelican, Git, and ghp-import:

```sh
python3 -m pip install "pelican[markdown]"
brew install git
python3 -m pip install ghp-import
```

### Step 2: Set Up Your Pelican Project
**Etter’s Principle: Automate workflows to increase efficiency.**

Create a new Pelican project:

```sh
mkdir my_pelican_site
cd my_pelican_site
pelican-quickstart
```

Follow the prompts to configure the site.

### Step 3: Add Your Resume in Markdown
**Etter’s Principle: Separate content from presentation.**

Create the content folder and add your resume:

```sh
mkdir content
nano content/resume.md
```

Paste your resume content using Markdown format.

### Step 4: Generate and Preview the Site Locally
**Etter’s Principle: Test documentation before publishing.**

Generate the site and preview it:

```sh
pelican content
pelican --listen
```

Then, visit [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

### Step 5: Set Up a GitHub Repository
**Etter’s Principle: Use version control to track changes.**

Set up Git for your project:

```sh
git init
git add .
git commit -m "First commit"
git branch -M main
git remote add origin https://github.com/yourusername/yourrepository.git
git push -u origin main
```

### Step 6: Deploy to GitHub Pages
**Etter’s Principle: Make content easily accessible.**

Generate the static files for GitHub Pages and push them:

```sh
pelican content -s publishconf.py
ghp-import output -b gh-pages
git push origin gh-pages
```

Your website will be available at:

```
https://yourusername.github.io/yourrepository/
```

## Further Resources

### Pelican Documentation
The official documentation for Pelican, a static site generator, which covers installation, setup, configuration, and more. It’s a comprehensive resource to learn Pelican in detail.

### Modern Technical Writing by Andrew Etter
A guide to modern technical writing that explains best practices, strategies, and tools for creating clear, concise documentation. This book is great for anyone interested in improving their writing skills for technical content.

### GitHub Pages Documentation
[GitHub Pages](https://pages.github.com/) lets you host static websites for free directly from your GitHub repository. This documentation explains how to set up and manage a site on GitHub Pages.

### Markdown Guide
An easy-to-follow guide to using Markdown. Learn the basics of formatting text, including headers, lists, links, and images, to create well-structured and readable content.

### Git Basics Guide
An excellent resource for learning Git, a version control system used for tracking changes in your code or documents. It covers basic concepts like cloning, committing, pushing, and pulling from repositories.

### Pelican Themes Collection
A collection of ready-made themes that you can use with Pelican to customize the look of your website. It’s an easy way to make your site look more professional and tailored to your preferences.

## FAQ

### Git & GitHub Questions

#### Q: How do I create a repository on GitHub?
A: Log in to GitHub, click **New Repository**, set a name and visibility, then **Create Repository**.

#### Q: How do I clone a repository?
A: Use:

```sh
git clone https://github.com/username/repository.git
```

#### Q: How do I check the status of my repository?
A: Run:

```sh
git status
```

#### Q: How do I resolve merge conflicts?
A: Manually edit conflicting files, then run:

```sh
git add .
git commit -m "Resolved merge conflict"
```

### Pelican & GitHub Pages Questions

#### Q: Do I need experience in Python to use Pelican?**  
A: No! While Pelican is written in Python, you only need basic command-line skills and Markdown knowledge to use it effectively.

#### Q: What templates are supported in Pelican?
A: Pelican supports Jinja2 templates for custom themes and dynamic content generation.

#### Q: Can I use custom themes in Pelican?
A: Yes, download themes from [Pelican Themes](https://github.com/getpelican/pelican-themes) and add them to `pelicanconf.py`:

```python
THEME = "themes/theme-name"
```

#### Q: How do I set the base URL for my Pelican site on GitHub Pages?
A: Set `SITEURL` in `pelicanconf.py`:

```python
SITEURL = "https://yourusername.github.io/repository"
```

#### Q: What is the `gh-pages` branch in Git?
A: The `gh-pages` branch is used by GitHub to host static sites, and `ghp-import` helps push files to it.

## Credits

- **Pelican Framework**: [Pelican](https://getpelican.com/)
- **Flex Theme:** [Alexandre Vicenzi](https://github.com/alexandrevicenzi/Flex)
- **Technical Writing Concepts**: Andrew Etter’s *Modern Technical Writing*
- **Git Documentation**: [Git SCM](https://git-scm.com/doc)
- **Nathan Parson and Ashek A Zaman:** For suggesting improvements and providing valuable feedback. 
