# Bullpen support site

This folder is the source for the public Bullpen support and privacy pages. It is a static site with no build step.

## Published URLs

- Home: `https://dancarlstedt.github.io/bullpen-site/`
- Support: `https://dancarlstedt.github.io/bullpen-site/support.html`
- Privacy: `https://dancarlstedt.github.io/bullpen-site/privacy.html`

These URLs belong in App Store Connect and in `AppStore/app-store-listing.md`.

## Support channel

The support page links to GitHub Issues:

`https://github.com/dancarlstedt/bullpen-site/issues/new?template=support.yml`

Enable GitHub notifications for the repository so new requests are seen. Issues are public; the page warns users not to include private player information.

## Publish or update

The published copy is the `main` branch of the public `dancarlstedt/bullpen-site` repository. To publish a change from this folder:

```sh
cd AppStore/site
git init -b main
git add .
git commit -m "Update Bullpen support site"
git remote add origin git@github.com:dancarlstedt/bullpen-site.git
git push -u origin main
```

For a one-off update, clone the repository and copy the changed files instead of re-initializing. GitHub Pages serves the repository root from the `main` branch.

## Checks before publishing

- No internal notes or placeholder contact details are present.
- All links resolve, including `favicon.svg` and `apple-touch-icon.png`.
- The support request link opens the issue form.
- Both pages load over HTTPS in a private browser window.
- The published text matches `AppStore/privacy-policy.md` and `AppStore/support.md`.
