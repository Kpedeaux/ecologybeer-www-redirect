# www.ecologybeer.com redirect

Forwards www.ecologybeer.com to https://ecologybeer.com. It is hosted on GitHub
Pages on purpose, so the www hostname does not pass through Cloudflare. The
site itself lives in a separate repository, `Kpedeaux/ecology`.

GitHub Pages cannot send a 301. It can answer 200 with a page that redirects
at once, and Google reads an instant meta refresh on a 200 page as a permanent
redirect. So every address that matters has its own small page here:

- one for each page of the current site, forwarding to the same path
- one for each address of the old Wix site, forwarding to its new home

Any other address gets `404.html`, which forwards people to the same path on
ecologybeer.com but answers 404, so search engines treat it as gone.

Do not edit the pages by hand. They are generated from the site's sitemap and
`_redirects` file. In the `ecology` repo run:

    python _internal/build-www-redirect.py

then commit and push this repo.
