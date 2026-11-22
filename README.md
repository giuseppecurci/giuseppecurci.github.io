# Giuseppe Curci — minimal academic website

This is a small Jekyll site for GitHub Pages.

## Files to edit

- `index.md`: introduction and page structure.
- `_data/publications.yml`: publication metadata, authors, links, summaries, and per-paper image dimensions.
- `assets/images/`: profile and publication images.
- `assets/css/style.css`: appearance and profile-image dimensions.
- `blog.md`: currently empty blog landing page.

## Add your profile photo

Replace `assets/images/profile-placeholder.svg` with your picture (for example `profile.jpg`) and update the image path in `index.md`.

The profile image dimensions are controlled by these CSS variables near the top of `assets/css/style.css`:

```css
--profile-width: 190px;
--profile-height: 220px;
```

## Add paper figures and set their dimensions

Replace each `*-placeholder.svg` file under `assets/images/` with your figure, or change the `image` path in `_data/publications.yml`.

Each entry has independent `image_width` and `image_height` values, in pixels. For example:

```yaml
image: "/assets/images/my-paper-figure.png"
image_width: 240
image_height: 150
```

The image is contained within that box, preserving its aspect ratio.

## Keep your GitHub Pages deployment workflow

When updating your repository, keep the existing `.github/workflows/jekyll.yml` file that is already deploying your site. This ZIP does not replace that workflow.

## Add a blog post later

The Blog page is intentionally empty. When ready, create a Markdown file under `_posts/` named `YYYY-MM-DD-post-title.md` with Jekyll front matter.


## Intro layout and GitHub link

The introduction uses a horizontal flex layout: text on the left and profile photo on the right. The photo is 240 × 280 px on desktop, 190 × 225 px on medium screens, and centered above the text on very narrow screens. Adjust `.profile-figure` in `assets/css/style.css` to change these sizes.

The GitHub profile link is centered within the text column and includes an inline GitHub icon.
