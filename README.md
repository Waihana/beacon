# The Beacon

A single static page that answers one question: **is waihana.com down, and is it us or a provider?**

It is hosted here — outside every system it watches — because a status page served by the thing it
monitors is unreachable in exactly the moment it is wanted.

## What it is

`index.html`, and nothing else. No build step, no dependencies, no CDN, no webfont, no server, no
cron, no database, no secrets, no auth.

It fetches when you open it, so it is current by construction — no stale cache, and no scheduler to
be late.

## What it reads

Public status endpoints (each sends `Access-Control-Allow-Origin: *`), plus a reachability check
against the site itself.

Two providers publish nothing a browser can read; the page lists them as unreadable rather than
quietly omitting them.

## Deploying

GitHub Pages, from `main` / root. There is nothing to build.
