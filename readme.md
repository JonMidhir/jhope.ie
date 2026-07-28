# jhope.ie

My website. A single static page, hosted on GitHub Pages.

### Deploying

Push to `master`. GitHub Pages serves the repository root, so there is no build
step and nothing to sync.

```
git push github master
```

### Hosting setup

Pages is configured to deploy from the `master` branch, root folder
(Settings → Pages → Build and deployment → Deploy from a branch).

- `CNAME` binds the site to the apex domain `jhope.ie`. To switch the canonical
  host to `www.jhope.ie` instead, change the single line in that file and update
  the `canonical` / `og:url` / `twitter:url` tags in `index.html`.
- `.nojekyll` disables Jekyll processing so files are served verbatim.
- "Enforce HTTPS" must be ticked in Settings → Pages once the certificate has
  been issued.

### DNS (Blacknight)

Apex `jhope.ie` — four A records to the GitHub Pages addresses:

```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

And optionally the AAAA records for IPv6:

```
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

`www.jhope.ie` — a CNAME to `jonmidhir.github.io.`, which GitHub redirects to
the apex.
