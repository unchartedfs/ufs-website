# Uncharted Frontier Services website

Source for [unchartedfs.com](https://unchartedfs.com), a single-page site built with [Hugo](https://gohugo.io/) and hosted on GitHub Pages.

## Editing content

- `content/_index.md`: hero, About section, How We Work intro, and footer text
- `content/approach/`: one file per step in the How We Work loop
- `content/leadership/`: one file per leadership bio
- `static/images/`: images (logo, graphics, headshots)
- `static/css/variables.css` and `custom.css`: colors and style tweaks
- `layouts/index.html`: which sections appear, and in what order

## Previewing locally

Requires Hugo Extended 0.145.0 or newer.

    hugo server -D

Then open http://localhost:1313. 

In a GitHub Codespace, add
`--bind 0.0.0.0 --baseURL "https://${CODESPACE_NAME}-1313.${GITHUB_CODESPACES_PORT_FORWARDING_DOMAIN}" --appendPort=false`
and open the forwarded port.

## Deploying

Every push to `main` builds and deploys the site via GitHub Actions.
