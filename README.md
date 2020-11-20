# Fast security scanners/checks
![Logo](images/Logo.png)

## XSS via Meta tags
`docker run --rm -it --name wcdscanner -e VULN_ID=wcdxss -e FIND_XSS=True -e DOMAIN=site.com whitespots/wcdxss`

## Cache Poisoning
`docker run --rm -it --name wcdscanner -e VULN_ID=wcdxss -e FIND_XSS=False -e DOMAIN=site.com whitespots/wcdxss`

## CORS misconfiguration on pages from Webarchives
`docker run --rm -it --name corsfinder -e VULN_ID=cors -e DOMAIN=site.com whitespots/corsfinder`

## CRLF vulnerabilities via url path and headers
`docker run --rm -it --name crlf-finder -e VULN_ID=crlf -e DOMAIN=site.com whitespots/crlf-finder`

## Path Traversal via url path
`docker run --rm -it --name ptrav-finder -e VULN_ID=ptrav -e DOMAIN=site.com whitespots/ptrav-finder`

## Check your 403 for bypasses
`docker run --rm --name forbid-bypasser -e VULN_ID=forbid_bypassed -e DOMAIN=site.com whitespots/forbid-bypasser`

## Find admin panels
`docker run --rm -it --name adminfinder -e VULN_ID=adminfinder -e DOMAIN=site.com whitespots/adminfinder`

## Check your site for social networks "accounts takeover" via broken social network links
`docker run --rm -it --name scanner -e VULN_ID=1 -e DOMAIN=site.com whitespots/brokensocial`
