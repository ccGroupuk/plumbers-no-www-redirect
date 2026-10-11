# cardiffandcaerphillyplumbers.com (no www) redirect

This repository does one job: it sends anyone who opens
`cardiffandcaerphillyplumbers.com` **without the www** on to the real site at
`https://www.cardiffandcaerphillyplumbers.com`, keeping the page they asked for.

## DO NOT DELETE OR RENAME THIS REPOSITORY

The domain's DNS (held at Wix) points the no-www address at GitHub Pages:

    A  @  185.199.108.153
    A  @  185.199.109.153
    A  @  185.199.110.153
    A  @  185.199.111.153

If this repository goes while those records still exist, the address is left
pointing at nothing, and a stranger can claim it on GitHub and serve their own
page under the business's name. That happened to the electricians' domain on
another host. Remove the four records in Wix FIRST, then the repository.

## Why it exists

Wix is the registrar and offers no forwarding and no nameserver change, and the
real site's host (Railway) cannot take a bare domain from Wix's DNS. Until this
was added (October 2026) the no-www address showed a security warning: it still
pointed at a removed Wix site whose certificate expired in May 2026.

The planned tidy-up is to move the domain to a registrar with proper
forwarding. When that is done, this repository can be retired (records first).

`index.html` and `404.html` are the same file on purpose: GitHub Pages serves
`404.html` for any path that is not the home page.
