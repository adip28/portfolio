# Adip Deb — Portfolio + private content dashboard

This package keeps the current public portfolio design and moves editable portfolio content into a CMS-managed JSON file.

## What has been changed

- Removed the public **Edit Site** button.
- Removed visitor-facing photo, certificate, project screenshot and video upload controls.
- Removed browser-local editing and localStorage upload behavior.
- Kept the existing theme, layout, sections, typography, navigation, cursor effects, preloader, animations, resume fallback and contact section.
- Moved the two existing case studies and four existing certificates into `content/portfolio.json`, so they can be edited in the dashboard.
- Added CMS fields for new projects, technologies, descriptions, SQL/DAX details, screenshots, videos, certificates, profile photo and resume PDF.

## Publish the website

1. Extract this ZIP.
2. Open your existing GitHub Pages repository.
3. Upload the **contents** of the extracted folder to the repository root. Do not upload the enclosing folder itself.
4. Replace the old `index.html` when prompted, and add `.pages.yml`, `content/portfolio.json`, and the other included files.
5. Commit the changes to the `main` branch.
6. Keep GitHub Pages configured to publish from `main` and `/(root)`.

The repository root must contain:

```text
index.html
.pages.yml
content/portfolio.json
media/
```

## Connect your private editing dashboard

1. Open [Pages CMS](https://app.pagescms.org/).
2. Sign in with the GitHub account that owns your portfolio repository.
3. Authorize/install the Pages CMS GitHub App for **only your portfolio repository**.
4. Select your portfolio repository and the `main` branch.
5. Open **Portfolio content**.
6. Edit existing projects and certificates, add new ones, upload screenshots/videos, replace your profile photo or resume, then save.
7. Pages CMS commits the changes to GitHub. GitHub Pages publishes the updated website automatically after its build completes.

## Security and access

- There is no admin link or editing option on the public portfolio.
- The dashboard is separate from the portfolio and uses GitHub sign-in. It is not a custom password form embedded in the website.
- Only GitHub accounts with write permission to the repository can publish changes. Do not add other people as repository collaborators or grant write access.
- Enable two-factor authentication on your GitHub account.
- The public repository and public website can be viewed by anyone. Visitors can save public images/text or recreate the design, but cannot modify your repository without write access.
- Uploaded media is stored in the repository. Keep videos and images reasonably compressed to avoid making the site slow or the repository unnecessarily large.

## Managed content

- `profilePhoto`: profile image
- `resumeFile`: replacement resume PDF (the existing embedded resume remains as a fallback)
- `projects`: title, category, accent, technologies, overview, deliverable, approach, SQL/DAX details, optional key metrics, screenshots, videos, GitHub and demo links
- `certificates`: issuer, date, title, description, badge and proof image

## Important

The files in this package are prepared for your GitHub repository, but Pages CMS is not connected to your GitHub account from this chat. The dashboard becomes usable after you upload these files and authorize Pages CMS using your own GitHub account.
