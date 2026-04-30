## Goal
Convert the existing static HTML website to use Eleventy (11ty) as a Static Site Generator and integrate Decap CMS (formerly Netlify CMS). This will allow for easy, UI-based management of blog articles without needing a backend server or database, preserving perfect SEO and site performance.

## Files involved
- `package.json` (New - for installing Eleventy)
- `.eleventy.js` (New - Eleventy configuration)
- `admin/index.html` (New - Decap CMS entry point)
- `admin/config.yml` (New - Decap CMS schema configuration)
- `index.html` (Modified - to use Eleventy layout)
- `blog.html` (Modified - converted to a template to dynamically list articles)
- `_includes/base.njk` (New - base HTML layout containing header/footer)
- `posts/` (New directory - to store Markdown files for blog posts)
- `_includes/post.njk` (New - template for rendering individual blog articles)

## Implementation plan
1. **Initialize Node.js & Install Eleventy**: Run `npm init -y` and `npm install @11ty/eleventy --save-dev`.
2. **Setup Eleventy Configuration**: Create `.eleventy.js` to configure the input/output directories and passthrough copies (for CSS and assets).
3. **Extract Base Layout**: Move the common `head`, `navbar`, and `footer` from `index.html` and `blog.html` into `_includes/base.njk`.
4. **Refactor Pages**: Update `index.html` and `blog.html` to inherit from `base.njk`.
5. **Dynamic Blog Listing**: Update `blog.html` to use a Nunjucks `for` loop to iterate over a `collections.posts` collection.
6. **Create Post Layout**: Create `_includes/post.njk` to render individual article content.
7. **Setup Decap CMS**: Create `admin/index.html` and `admin/config.yml`. Configure the CMS schema to output Markdown files with frontmatter (title, description, image, etc.) into the `posts/` directory.
8. **Test Build**: Run Eleventy to ensure `_site/` is generated correctly.

## Risks / edge cases
- **Asset Paths**: CSS and image paths might break during the transition. We need to ensure Eleventy's passthrough copy is set up correctly for the `assets/` directory.
- **CMS Authentication**: Decap CMS requires a backend for authentication. If deploying to Netlify, Netlify Identity can be used. If deploying elsewhere, a lightweight OAuth proxy (like Decap's standalone Go server) might be needed. We will start with `local_backend: true` for local testing.
- **RTL & Styling**: The CMS admin panel is English/LTR by default, but the generated site will remain RTL Hebrew. We need to make sure the CMS fields support Hebrew text properly (which they do natively).

## Troubleshooting log
*Pending implementation...*
