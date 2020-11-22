# Fast security scanners/checks
![Logo](images/Logo.png)

# A small contribution to community :)
We use all these tools in security assessments and in our [vulnerability monitoring service](https://whitespots.io/vulnerability-monitoring)

## Check your domain for DNS NS takeover ([Repo](https://github.com/whitespots/dnsnstakeover))
`docker run --dns=8.8.8.8 -e VULN_ID=dns_ns_takeover -e DOMAIN=site.com whitespots/dnsnstakeover`

## Cache Poisoning ([Repo](https://github.com/whitespots/wcdxss))
`docker run --rm -it --name wcdscanner -e VULN_ID=wcd -e FIND_XSS=False -e DOMAIN=site.com whitespots/wcdxss`

## XSS via Meta tags (exploitable with cache poisoning) ([Repo](https://github.com/whitespots/wcdxss))
`docker run --rm -it --name wcdscanner -e VULN_ID=xss_meta -e FIND_XSS=True -e DOMAIN=site.com whitespots/wcdxss`

## CORS misconfiguration on pages from Webarchives ([Repo](https://github.com/whitespots/corsfinder))
`docker run --rm -it --name corsfinder -e VULN_ID=cors -e DOMAIN=site.com whitespots/corsfinder`

## CRLF vulnerabilities via url path and headers ([Repo](https://github.com/whitespots/crlf-finder))
`docker run --rm -it --name crlf-finder -e VULN_ID=crlf -e DOMAIN=site.com whitespots/crlf-finder`

## Path Traversal via url path ([Repo](https://github.com/whitespots/ptrav-finder))
`docker run --rm -it --name ptrav-finder -e VULN_ID=ptrav -e DOMAIN=site.com whitespots/ptrav-finder`

## Check your 403 for bypasses ([Repo](https://github.com/whitespots/forbid-bypasser))
`docker run --rm --name forbid-bypasser -e VULN_ID=forbid_bypassed -e DOMAIN=site.com whitespots/forbid-bypasser`

## Find admin panels ([Repo](https://github.com/whitespots/adminfinder))
`docker run --rm -it --name adminfinder -e VULN_ID=adminfinder -e DOMAIN=site.com whitespots/adminfinder`

## Check your site for social networks "accounts takeover" via broken social network links ([Repo](https://github.com/whitespots/brokensocial))
`docker run --rm -it --name scanner -e VULN_ID=broken_social -e DOMAIN=site.com whitespots/brokensocial`
