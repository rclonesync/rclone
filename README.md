# Rclone personal OAuth website — updated package

Application: Rclone
Effective date: 20-10-2026
Support: rclonegdrivesync@gmail.com

## Public URLs

- Home: https://rclonesync.github.io/rclone/
- Privacy: https://rclonesync.github.io/rclone/privacy.html
- Terms: https://rclonesync.github.io/rclone/terms.html

## Before submitting to Google

The privacy policy has expanded disclosures based on https://support.google.com/cloud/answer/13806988. Google requires an actual app-specific policy, not a template. The owner must confirm the exact OAuth scopes and local-only architecture, resolve the reported https://www.googleapis.com/auth/docs scope (not verified in current documentation), confirm whether the metadata scope is needed alongside full drive access, and remove the setup/verification notices only once the statements match actual behavior. Check logs, caches, backups, destinations, encryption settings and support-message retention. No unverified security or compliance guarantee is made. Review the Limited Use commitment and terms against actual practice. Update the effective date if the revised policy takes effect after 20-10-2026.

## Deploy or replace the existing site

1. Extract the ZIP.
2. Under GitHub account rclonesync, open repository rclone.
3. Upload/replace index.html, privacy.html, terms.html, styles.css and .nojekyll at the repository root; commit to main.
4. In Settings → Pages choose Deploy from a branch, main, /(root), then Save. If already configured this way, the commit should trigger redeployment.
5. Wait for the Pages deployment to succeed. Check all three public URLs, navigation and support links on desktop and mobile.
6. In Google Auth Platform branding/consent settings use the Home, Privacy and Terms URLs above. Ensure app name and support contact match the actual OAuth app. Meet applicable domain ownership verification requirements; publishing these pages does not guarantee Google verification.
7. If the privacy URL is unchanged, respond to the verification correspondence after the live policy has been updated, as Google’s guidance directs. If the URL changes, update the consent settings as well.

Do not use GitHub Pages as an OAuth callback. Follow https://rclone.org/drive/#making-your-own-client-id for local rclone OAuth client setup. Never upload secrets, tokens or rclone configuration files.

## Checks

This package uses static HTML/CSS, relative links, no JavaScript or third-party fonts. Open index.html locally to preview. The live site could not be retrieved during this revision; this download does not change the hosted repository.

## Reported scopes

- https://www.googleapis.com/auth/docs — reported, requires validation; not silently replaced with documents.
- https://www.googleapis.com/auth/drive
- https://www.googleapis.com/auth/drive.metadata.readonly

The operator has not yet confirmed whether use is exclusively local with no backend or additional destinations. The verification notice remains for this reason.

## Confirmed deployment architecture

rclone runs only on the user’s own computer. Transfers are between that computer and Google Drive only. There is no backend or additional cloud storage destination. Public policy setup notices have been removed on this basis. The auth/docs permission description now reflects the operator’s supplied Google consent description; keep it consistent with the actual consent configuration and remove redundant scopes if not needed.

## Custom domain pending

The owner has a domain in Cloudflare but has not yet supplied its name. Current HTML URLs still use the existing GitHub Pages address. Before resubmission, update all website URLs to the exact custom domain, configure GitHub Pages custom-domain hosting and HTTPS, and complete Google Search Console DNS Domain-property verification using a Google Cloud Project Owner account. Keep the DNS verification record. Wait at least the 24 hours specified by the verification rejection, and update Google Auth Platform Home, Privacy, Terms, and authorized-domain settings. Do not submit the old github.io URL as proof of DNS ownership.
