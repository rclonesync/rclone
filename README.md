# Configured application details

- Application: Rclone
- Effective date: 20-10-2026
- Contact: rclonegdrivesync@gmail.com
- Home: https://rclonegdrivesync.github.io/
- Privacy: https://rclonegdrivesync.github.io/privacy.html
- For this root GitHub Pages URL, create the repository `rclonegdrivesync.github.io` under the GitHub account `rclonegdrivesync`.

These details are already applied to both HTML pages. The configured scopes and actual data handling still require owner verification. The generic customization instructions below are retained as a reference.

# Personal rclone OAuth website

Two static pages, shared CSS, no JavaScript, dependencies, build step, or external fonts. Open index.html locally to preview. All internal links are relative, including for GitHub project Pages URLs.

## 1. Customize before publication

Use a text editor to replace placeholders in BOTH HTML files:

- `[APP_NAME]`: the exact application display name used in Google’s consent screen.
- `[SUPPORT_EMAIL]` and the literal `SUPPORT_EMAIL` inside mailto links: a monitored address you own.
- `[EFFECTIVE_DATE]`: the date the verified policy takes effect, for example 2026-10-20.
- `[GITHUB_PAGES_URL]`: the final public HTTPS home URL, including repository path and trailing slash, for example https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/.
- `[CONFIGURED_SCOPES_AND_PURPOSE]`: exact configured Google scope URLs and their purposes. Rewrite the section to state actual requested permissions; remove unused examples if they would confuse readers.

Verify the consent screen, rclone configuration and runtime overrides, OAuth scopes, logs, caches, destinations, backups, token handling, and support-message retention. Never paste credentials into the site. If rclone runs on a NAS, server, or another machine, explain that actual storage location. Revise the privacy promises if your deployment includes additional services. Remove the owner-setup notice on Home and replace the policy verification notice with a factual description of your verified configuration once this review is complete.

## 2. Deploy using GitHub Pages (no terminal needed)

1. Sign into GitHub and create a repository, for example `personal-drive-app`. A public repository is the simplest option; Pages availability for private repositories depends on your plan.
2. Extract this ZIP. In the repository choose **Add file → Upload files**. Upload `index.html`, `privacy.html`, `styles.css`, and `.nojekyll` to the repository ROOT, not inside an extra folder. Commit to `main`. README.md is optional. Ensure hidden files are visible if uploading `.nojekyll`; it is included in the ZIP.
3. Open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, choose **main** and **/(root)**, then **Save**.
4. Wait for the Pages deployment to finish. Use the exact URL GitHub displays. For a project repository it is usually `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/`. For a repository named `YOUR_USERNAME.github.io`, it is usually `https://YOUR_USERNAME.github.io/`.
5. Update `[GITHUB_PAGES_URL]` with that URL and commit. Check both pages on desktop and mobile, navigation, and the support email links. Changes redeploy automatically.

Home URL: `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/`
Privacy URL: `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/privacy.html`

## 3. Use with your Google OAuth application

Enable the Google Drive API in your Google Cloud project. Configure Google Auth Platform branding, audience, data access, and OAuth client settings for your actual use case. Enter the public Home and Privacy URLs in the corresponding consent/branding fields. Keep app name, support contact, scopes, and policy consistent.

Follow rclone’s official “Making your own client_id” instructions for the appropriate OAuth client type (typically Desktop app for local rclone). The GitHub Pages website is informational: DO NOT use it as an OAuth callback or put client secrets or tokens in HTML, repository files, commits, or screenshots. Domain ownership, authorized-domain rules, testing restrictions, publishing, and verification requirements depend on Google’s current rules and your app’s scopes/audience. A published website does not itself publish or verify an OAuth app, remove consent warnings, or guarantee approval. If Google requires domain ownership verification that a shared github.io address cannot satisfy, use a domain you control.

## Files

- index.html — Home
- privacy.html — Application Privacy Policy
- styles.css — responsive layout and accessible navigation
- .nojekyll — serve as plain static files
- README.md — customization and deployment guide

## Official references

- https://docs.github.com/en/pages/quickstart
- https://rclone.org/drive/#making-your-own-client-id
- https://rclone.org/docs/#config-config-file
- https://developers.google.com/workspace/drive/api/guides/api-specific-auth

This independent template uses no rclone or Google logos and claims no affiliation. It describes an intended configuration, not verified behavior of your installed app.
