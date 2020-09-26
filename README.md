# Fast security scanners/checks

## Find XSS via Web Cache Deception
`docker run --rm -it --name wcdscanner -e VULN_ID=1 -e FIND_XSS=True -e DOMAIN=site.com whitespots/wcdxss`

## Find CORS misconfiguration on pages from Webarchives
`docker run --rm -it --name corsfinder -e VULN_ID=1 -e DOMAIN=site.com whitespots/corsfinder`

