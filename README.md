# Author's guide

## Local setup

### Prerequisites

#### Hugo

You need Hugo (extended version) to build this website locally.
Download the latest version and install it.
On Linux it is usually found in the package manager.
In macos, it can be installed from brew.
On windows, I have no idea, but I'm sure there is a simple way to get it.

#### Git

You need git. If you still do not know it

### Clone the repository

This project uses *submodules*, so cloning with a plain `git clone URL` **won't work**.
Use the `--recurse-submodules` option:

```
git clone --recurse-submodules <REPO_URI>
```

### Try the website locally

Open a terminal in the folder containing the project. Then issue:
```
hugo serve
```
The command will print on the console the address of a website in localhost.
Open it with a browser, and you'll see the website.
Changes made to the codebase are refreshed automatically.

## Project structure

The theme was meant for a blog, but it looks good for conferences, too (at least IMHO).

### Add a new page

Inside `content/post`, create a new entry.
In the header, look for `URL:` and place there a good route, e.g., for the organization committee: `URL: /organization/`.
This can be used to link the new page on the top menu, removing the feeling of a blog and getting the feeling of a page.

### Add a new link on top

In `config.toml`, look for sections like;

```
  [[params.addtional_menus]]
  title =  "Percom 2027"
  href =  "/about/"
```

Just copy one of them and change label/href. **Note:** the file is indentation sensitive!


### Add/modify socials
In `config.toml`, search for the `[params.social]` section, it is self explaining.
