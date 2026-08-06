# Daniele Malleo

Source for Daniele Malleo's professional website.

The site is intentionally static and can be published by any hosting service that serves `index.html` from the repository root.

## Contents

- `index.html` — professional profile
- `patents.html` — patent and invention-family portfolio
- `Daniele_Malleo_Resume_Jul2026.pdf` — downloadable résumé

The profile and patent pages use externally hosted IBM Plex fonts and otherwise require no build process or runtime dependencies.

## Search-engine discovery

- `robots.txt` allows crawling and points search engines to `sitemap.xml`.
- `sitemap.xml` lists the public profile and patent-portfolio pages.
- `b5220f3aa6764f61b460bd8cf26e438c.txt` is the domain-verification key for [IndexNow](https://www.indexnow.org/).

After publishing a content change, notify IndexNow with:

```sh
curl -X POST 'https://api.indexnow.org/indexnow' \
  -H 'Content-Type: application/json; charset=utf-8' \
  --data '{
    "host": "danielemalleo.com",
    "key": "b5220f3aa6764f61b460bd8cf26e438c",
    "keyLocation": "https://danielemalleo.com/b5220f3aa6764f61b460bd8cf26e438c.txt",
    "urlList": [
      "https://danielemalleo.com/",
      "https://danielemalleo.com/patents.html"
    ]
  }'
```
