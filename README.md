# Barbara Long — Hugo Site

## Local preview

```bash
hugo server
```

Then open http://localhost:1313 in your browser.
The site live-reloads whenever you save a file.

---

## Adding a blog post

Create a new file in `content/posts/` named `YYYY-MM-DD-your-title.md`:

```markdown
---
title: "Your post title"
date: 2026-05-01
---

Write your post here in plain text.
You can use **bold**, *italic*, and [links](https://example.com).

To add an image, put the file in static/images/ and write:
![Description](/images/your-image.jpg)
```

---

## Adding a new artwork

Create a new file in `content/work/`:

```markdown
---
title: "Artwork Title"
image: "your-image.jpg"
weight: 7
---

Description of the work.
```

- Put the image in `static/images/`
- `weight` controls the order pieces appear in the grid (lower = first)

---

## Updating page content

All pages are plain Markdown files in `content/`:

| Page        | File                        |
|-------------|-----------------------------|
| About       | content/about.md            |
| Contact     | content/contact.md          |
| Exhibitions | content/exhibitions.md      |
| Workshops   | content/workshops.md        |

Just open the file, edit the text, and save.

---

## Adding your images

Put all images in `static/images/`. They are referenced in content files as:

```
/images/your-filename.jpg
```

The hero image on the homepage should be named `hero.jpg`.
The six grid images should be named `grid-1.jpg` through `grid-6.jpg`
(or whatever you set as `image:` in each artwork's front matter).

---

## Deploying to GitHub Pages

1. Push any change to the `main` branch
2. GitHub Actions automatically builds and publishes the site
3. Your live site updates within about 60 seconds

To check the build status, go to your GitHub repo → Actions tab.

---

## Changing the side margins

Open `static/css/style.css` and change:

```css
--page-padding: 72px;
```

---

## Updating the baseURL

Before going live, open `hugo.toml` and set:

```toml
baseURL = "https://yourusername.github.io/"
```

Replace `yourusername` with your actual GitHub username.
If you add a custom domain later, update this to `https://yourdomain.com/`.
