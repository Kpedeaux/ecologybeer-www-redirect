# www.ecologybeer.com redirect

One page that forwards www.ecologybeer.com to https://ecologybeer.com, keeping
the path. It is hosted on GitHub Pages on purpose, so the www hostname does
not pass through Cloudflare. The site itself lives in a separate repository.

`404.html` is a copy of `index.html`. GitHub Pages serves it for every path
that is not the home page, which is how deep links get forwarded too.
