# Fast security scanners/checks
![Logo](images/Logo.png)

## XSS via Web Cache Deception
`docker run --rm -it --name wcdscanner -e VULN_ID=1 -e FIND_XSS=True -e DOMAIN=site.com whitespots/wcdxss`

## CORS misconfiguration on pages from Webarchives
`docker run --rm -it --name corsfinder -e VULN_ID=1 -e DOMAIN=site.com whitespots/corsfinder`

## CRLF vulnerabilities via url path and headers
`docker run --rm -it --name crlf-finder -e VULN_ID=1 -e DOMAIN=site.com whitespots/crlf-finder`

## Path Traversal via url path
`docker run --rm -it --name ptrav-finder -e VULN_ID=1 -e DOMAIN=site.com whitespots/ptrav-finder`

## Check your 403 for bypasses
`docker run --rm --name forbid-bypasser -e VULN_ID=1 -e DOMAIN=site.com whitespots/forbid-bypasser`
