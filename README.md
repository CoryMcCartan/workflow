# Best Practices for Computational Research Workflow

This document collects my opinionated recommendations on how to organize and
manage data, writing, and code for a computational research project.

**Using this document:**

- Quickly jump to [**Project setup**](#project-setup), [**Code**](#code), [**Writing**](#writing), or [**Figures**](#figures).
- I recommend reading the whole document once in order, if you haven't before.
- If you are viewing this file on GitHub, the upper right corner of this container
contains a table-of-contents dropdown.

## General principles

- overview of components of a computational project
- version ctrl and reproducibility
- keeping things lightweight and simple

## System setup

This document assumes R is your primary analysis language, but most of the advice will be relevant for other languages as well.

You should install [Quarto](https://quarto.org/docs/get-started/), if it is not already installed or included in your IDE (it is bundled with Positron and RStudio).

You should also have `git` installed, and an account on [GitHub](https://github.com) or similar.
I find the [`gh`](https://cli.github.com/) command-line utility useful for managaing GitHub repositories, but many people I work with use [GitHub Desktop](https://github.com/apps/desktop) and like it.

## Project setup

## Code

## Writing

## Figures

### Figure theming

### Exporting figures

Figure export is done via `ggsave` and should *always* be to a PDF file.
<summary>Why PDF?</summary>
<details>
Saving figures as PDFs (or very rarely, when there are PDF bugs, as SVGs) is preferable to PNGs for a few reasons. 

1. File sizes are smaller, so `git` syncs faster and your repository uses less disk space
1. PDF figuress avoids grainy images in the paper PDF and reduces the paper PDF file size
1. Many journals need high-res images and prefer you to provide PDFs anyway
</details>

You should always specify a `height` and `width`, which are measured in inches by default.
For most figures, I use `width=6.5`, which is the width of the text block on letter-sized pages.
If the figure will not be occupying the full width, you can use a smaller number.
Always using the same width ensures that the text size in your figures will be consistent across figures and will match your paper text.

