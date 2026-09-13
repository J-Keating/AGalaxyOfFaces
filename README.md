# A Galaxy of Faces

A single-page website for a face-painting business. Open `index.html` directly in a browser to preview it; there is no build step or software to install.

- **Live website:** https://j-keating.github.io/AGalaxyOfFaces/
- **GitHub repository:** https://github.com/J-Keating/AGalaxyOfFaces

## Editing the website content

The four files in `content` are the editable source of truth:

- `content/Main.md`: business identity, hero, event types, search text, and footer.
- `content/Gallery.md`: gallery introduction, image order, captions, and alt text.
- `content/About.md`: artist biography, portrait, experience, and trust details.
- `content/Ask.md`: booking copy, form fields, contact details, and form delivery.

Edit those Markdown files rather than `index.html`. Text in square brackets is incomplete. When the content is ready, ask Copilot to regenerate `index.html` from the four files and preserve the current responsive design. The Markdown files are the inputs; `index.html` is the generated result.

## Personalize before publishing

Complete these items in the Markdown files:

- The artist name and biography in `content/About.md`.
- The business email and form mode in `content/Ask.md`.
- The service area and search text in `content/Main.md`.
- The selected photos, captions, and alt text in `content/Gallery.md`.
- The service description, event types, and hygiene wording: confirm that every claim is accurate.

Get permission from a parent or guardian before publishing identifiable photos of children. Avoid including names or other identifying information in image filenames, captions, and alternative text.

## Contact form choices

The current form uses `mailto:`. It opens the visitor's email app with the enquiry filled in, but the visitor must still press Send. Set `businessEmail` near the bottom of `index.html` to enable it.

For a form that sends without opening an email app:

1. Create a form at Formspree (or a similar static-form provider).
2. Copy the endpoint, which looks like `https://formspree.io/f/xxxxxxx`.
3. Set `formEndpoint` near the bottom of `index.html` to that endpoint.
4. Submit a test from the published site and confirm that the notification arrives.
5. Enable the provider's spam protection and keep the destination email out of the visible page if privacy matters.

Do not put SMTP, Gmail, or other email account passwords in this file. Anything in a static website is public.

## Hosting recommendation

### Recommended: GitHub Pages + Formspree

This is the best fit for the site as built. GitHub Pages hosts the static page, supports a custom domain and HTTPS, and keeps the source portable. Formspree handles the only server-side job: delivering contact enquiries. The tradeoff is that updates are made by editing files or using GitHub's web editor.

This site is published from the root of the `main` branch. Pushing a new commit to `main` automatically updates GitHub Pages.

To publish future local changes:

1. Regenerate `index.html` from the files in `content`.
2. Preview and test the page locally.
3. Run `git add .`.
4. Run `git commit -m "Describe the website update"`.
5. Run `git push`.

GitHub will redeploy the live address automatically. Connect a custom domain in **Settings > Pages** when ready.

### Canva Websites

Canva is the quickest route if your daughter wants to maintain the design herself using a visual editor. It is less suitable for this exact custom HTML file, and a true email form generally requires an embed or an external form service. Choose Canva when visual editing is more important than portability, source control, and fine control over search metadata.

### Other good options

- **Netlify**: very easy static deployment, custom domains, preview deployments, and form options. It is a strong choice if you want a friendlier publishing workflow than GitHub Pages.
- **Cloudflare Pages**: fast global static hosting with custom domains and room to add serverless functions later. It has more setup than this small site needs.
- **Carrd**: inexpensive and easy for a polished one-page site, with form integrations on eligible plans. It is less flexible than owning this HTML.
- **Squarespace, Wix, or WordPress.com**: useful when she later needs scheduling, payments, a blog, or frequent visual editing. They add cost and complexity that are unnecessary for the first version.

Service features and free-tier limits change, so check current pricing and form quotas before choosing a paid plan.

## Suggested launch path

Use GitHub Pages and Formspree now. Buy a short custom domain only after the name is settled, and keep the repository as the source of truth. Revisit Netlify, Squarespace, or Wix only if she later needs booking and payment workflows rather than a simple enquiry form.