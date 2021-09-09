
# ZAP Scanning Report

Generated on Thu, 9 Sep 2021 00:46:11


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 5 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 1 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Incomplete or No Cache-control Header Set | Low | 10 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 7 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 2 | 
| Timestamp Disclosure - Unix | Informational | 4 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Content-Security-Policy header, to achieve optimal browser support: "Content-Security-Policy" for Chrome 25+, Firefox 23+ and Safari 7+, "X-Content-Security-Policy" for Firefox 4.0+ and Internet Explorer 10+, and "X-WebKit-CSP" for Chrome 14+ and Safari 6+.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/Security/CSP/Introducing_Content_Security_Policy
* https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
* http://www.w3.org/TR/CSP/
* http://w3c.github.io/webappsec/specs/content-security-policy/csp-specification.dev.html
* http://www.html5rocks.com/en/tutorials/security/content-security-policy/
* http://caniuse.com/#feat=contentsecuritypolicy
* http://content-security-policy.com/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a onclick="window.closeNPSModal()"  href="https://startupdetat.typeform.com/to/ehxbMpeX" target="_blank">
                👍👎 Quel est votre avis sur ce site ?
              </a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link rel="canonical" href="https://annuaire-entreprises.data.gouv.fr/administration}"/>`
  
  
  
  
Instances: 1
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher/carte" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form action="/rechercher" id="search-wrapper" method="get" class="jsx-4085546850">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "search-input-input" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/resources/favicons/manifest.webmanifest](https://annuaire-entreprises.data.gouv.fr/resources/favicons/manifest.webmanifest)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 10
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Permissions-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.21.1`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress the "Server" header or provide generic details.</p>
  
### Reference
* http://httpd.apache.org/docs/current/mod/core.html#servertokens
* http://msdn.microsoft.com/en-us/library/ff648552.aspx#ht_urlscan_007
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `43ac-oQZ3ZGJ7qVQE1UxW2nE+kyz/NC8`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `5397-3U0NOCykhJrRBeSU3lhJ6JAUA5A`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `5957-TO9/ZnYFaC6f48CTOK4CntkdE20`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `4c28-qr4+BY4wF4k2trgN/65XNwBbNKw`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `492e-6/St8MG6EKGhh4rbisOmEeySDZU`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `43ac-oQZ3ZGJ7qVQE1UxW2nE+kyz/NC8`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `71c5-xd5n0u3G4xC9m5rtYV6YwhgdiQQ`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/resources/css/dsfr.min.css](https://annuaire-entreprises.data.gouv.fr/resources/css/dsfr.min.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `d09GRgABAAAAAB0wAAsAAAAAO+QAAQAAAAAAAAAAAAAAAAAAAAAAAAAAAABHU1VCAAABCAAAAFsAAACEI3woak9TLzIAAAFkAAAAQgAAAFZZDkOMY21hcAAAAagAAAI0AAAGxrfIUzRnbHlmAAAD3AAAFE4AACiwie3OemhlYWQAABgsAAAAMAAAADYeGFz1aGhlYQAAGFwAAAAeAAAAJAiYBEhobXR4AAAYfAAAABYAAAF8krwAAGxvY2EAABiUAAAAvQAAAMDas+QAbWF4cAAAGVQAAAAdAAAAIAFzAHBuYW1lAAAZdAAAATEAAAIuRB1J2XBvc3QAABqoAAAChQAABeq9FV3peJxjYGRgYOBiMGCwY2BycfMJYeDLSSzJY5BiYGGAAJA8MpsxJzM9kYEDxgPKsYBpDiA2YmACmiUBFrUG4giGSIYoMM8TKB7BEMMQCyTj4DQjUH04QzQAp+ULKQB4nGNgZLFlnMDAysDA9JPZg4GBYQWEZnJgsGI0BdIMrMwMWEFAmmsKgwOD74NQ5hf/LRhymF8wnAAKM4LkANMFDCwAAHiczdRJT1RhFITh90KDijiiOOGMiorzPI8goqKigAyyISSuWJCQ+HPrn2Cd7lp13LnxkqdDf0Bzz82pAvqAXhu3FvTM0Pg7mimfNu3zXgba561mxO8Psd8nLT4xyxrr/GKDTbY0t73tn3af0j7tvhp/SvcXLLDMCj/4ySKrLPm3etr/qY9+drCTXb6P3Qyyh73s810c4CBD/svDDHOEoxzjOCcY4SSnOM0ZznKO84xygYtcYozLXOGq57nGdW5wk1vc5g53ucd9HvCQRzzmCU95xnNe8JJXvOYNb5lgkndM8Z5pPvDRM87wmS989azf+M4c8x6p/y9z/su1UC/L3af1fPyA6lq0Vfyc/p9rsF5av/PON+dn1VHTzEYNtRYrth6ezHvTUSNuRA26GfWZW+HJRUdtqsJbg6I2W1HbraitV3i7UHjPUHjjUHj3UFQaFN5HFDW9wjuKwtuKwnuLwhuMwruMwluNwvuNojKi8M6j8PajcA5QOBEonA0UTgkK5wWFk4PCGULhNKFwrlA4YSicNRROHQrnD4WTiMKZROF0onBOUTixKJxdFE4xCucZRTWYwhlH4bSjcO5RuAFQuAtQuBVQuB9QuClQuDNQuD1QuEdQuFFQuFtQuGVQuG9QuHlQuINQuI1QuJdQuKFQuKtQuLVQuL9QuMlQuNNQuN1QuOdQuPFQuPtQuAVRuA9RuBlRVOYVbksU7k0UblAU7lIU1REK9ysKNy0Kdy4K5v8AgDfus3ictToLcBtlevvvSis/pcjWau3YUizJ0tpYfmn1iF+KQ2zJeTp2nMQExwnu4gRCaHJJCCHhfAEnhAQHU+7Ua+HgmpTymA6Q3l24lswdNTM93XBwx9Rkegxt05s5SmcoZTgf5HTW0u/7V5JlRwZnOrWs1a9///97/d97xXAM8+XTug3cKcbCVDH1DEN8olW0LjPwBr5K8kieZaFgKMjBlA8GDcTJh3xh4oeBkVjshB08c/jgmq6uNQcPq5+mRxdbNvVd7utdueqZv33m49rumprufrxw4/OXkWU4St4x0NjU3LilddWqi6mFcGH08+gKMmuYDQyjd2YoqspQ6YYBJc1IDFKYtYpwV2ogkscAEzwsczsbiD9MfHZiMRLJF/R7nLzFmkW5Rgglbmzt0I7bhnrkU0883Nwdfv61Fzvbioqc1d8d2T088u2qFSZTB1kVHAoGh+7BS7C2ra2/rU1ZAIRy+HqbpdRqDcsr2fZAz5q1XHdnv3LH0PBpq7W8/OzuoTuUzT9NQYGLgmD62xiGmTuPQuA7AOcRkAVZcAmugCtQmot/CQ8m6Mc7TvxuwTusR4nHlXgiB49n9u/cEQiFAjt2vp8ekClcHFeS7+fiRJm3lg6ALAaJvcx+AnQyxCybHYLD7DI7AoCZeNVpRZ0mU+mBV6F8vaMb5fYxZkZgyhkmn1jhOFwOPJwQgeOxcoIcwDc7Tj7gjWLxbE9xWbGBfGAQK8oGFUXh+md/VlhpNRqtlYVcS6HRmNynKGQ4kUBSdFnwLUwZU5kLA3EQDmRphncuJOoAV6Q+4FNy4Zp9j72Y/J1CphJp3v+Vq2LyGMZNxHwSAgmwZ0lRVD2uHo+SIuWnOD5BTkXU37O7cbm2J8ZuRM0mIdzDDl7vVt9UpyJk2xdRdYqEo5l1H3ECwiYgVGLIJyI5w+5Ofp/CB5hkSlFnouQUORVlWLr+GHsFJJyPJwFnIBpEAyGTCstHr18HyOyV5Dh7IvrF9QgJ43JtzyX2XaAFT09EFA4JSJLY1xIR9Q3SGVGntc8EmUxESCeM4Lv6RiSRoVFg36G80N2sPcUCmfwiQjpIOLKQF4CeTyTiCHC16kyEnEI5FSefBSWZk1qGtvE5fkCzgB2RcFVKMoH8kHBufv6OfSvFj4SY3PRK/oDUA92sJzUgk7+nnKxPpD7TdFal+KH72CcRkToF/FyPqFMwyPCDtFF+kBnQea5K7Y+Sl9VToPlsidoHYzCkuTNP6QmeDAEZG9izmdNj70g+y96h/i6K4ohkdGSQ0mGgiwdT4iRvpQjS+AVd38hdBglVMEypw2zhQc09ASL7rDagyh9sQ7fhCMgK95FNmD0h2NhP4oJttswmxME8QY3VsGCzCVy/TUgkBBtofMr3vAO+5zIjMi5GAhoAnpAGbp6DanCgO4IRuCXRYXZw/XGEhnhSCMDqlRhXFVMSs9e4KkQze40irKLI4gp1T+oBivNhwNnPLAd/5wGcLurFBOrG4BWYc29EdEkheQXBK3slTv1Ym7x786H1JzI+Tf3RvsP79x++j165fpzaf2hk67r2lmrfKxn/pR54RfujfiONX2bWM39CuUbMFiTDJXgk+gr4kYxSeY6aOpIiFKmEsNJIPP5VJIjzvInwlhXETmTHIvNkJp4hef+J9Yc275bbcPyu0hfpqqmtremK9MXpcOC2refreJ7byvNbOZ7fUFDCD/DwX1JA6mF6m16/bf60xjRl8xVfdUv7uq0jhyiuZBeCvZCBv2OyM9ypFujPFVgLzukLCvIfgcEj+QU3zqR1WcezP0HdTPm8GfKLSPITcGCfkV9Ek/9NHRjq5lOgmxi3ly8SsTkwHcmQMwD/AxmJqr+diOYMqcRLRiLqb89HU7qaxlPLNC6CKWdsDEkhETxWLvQ5YmPbdHSCVOQmKEdkjE9Hz5OKyDw5VC0mBwk9W0gEgqTc5ExEJ9L/OQlg27JWMNm5XC3kTDchk9IQBg3JIKFwliqa/ecjE+cjj09EHpuInF+qgMjV85HzsAU2wvaUz/tz8L2FNC5mqMDo+Pn1yB++iHwOLvDq9ch1GMH365HU2W/gxtO5BMGgnnZTroAccGDcwBfXn1BsQrILvE6CzKgHMLRDIClBX8R+Am7qgnqATOI7lUNkw7Vh9uUQ5gMXzQ6zXja7SuFNhslMBn6cHVTD1LUBBiULR7KLvRLT0KR993LAwTFFDBOCCJ+fziBi3PjsCbCqpog6qG7vIY2KTyFnSGNE3U5ejKjvsg3a/qdh/8NMAWMES3QFSNC3AjIdA00W7p5m2021xvMm0+ynCE3B76YJmEruUphMfon7dYyJKUVbloggLgCzmvwxquoP4OYaUwZYHGd1EYRpNAJMU3J3BmZa12nmlVvbMb2DI8lt95h05bT5YcjxJjGHTJ9P2ubrmeabsnqa+JldS7Z7ZTGScih1QgHlmmaYufPtZ0owNhMBc2I5K4bKblAikDlcZhKQMoD23KeFYkV9IEJOf8hegfQhoU5T9Tkr2EB1PqR3lLk89z4Kv5bWRVix2YmIxU4V1j1hAnGKSiDkyYjAQINpaH4lNK+OO3Xk4FOi+NTB+9QvUqMjp/buvH3ValFcver2nb+aG+4N72lv33MCL2Fni9PZ0oUXrr+99e2xsbdb29Ofs9fqvb19d97Z1+utnxs9mNoKFyW1FS603nsQ+LrIFDN2xg2ctYNu8jqNISkE6RAWeHY2GJKMpAE+RIm3syG9BKUfZ5CCdlbkDQQ+DNw3D6v/88eXypdtW/10lPu36HPJl+Ruk3jmzfd2jnpHd69zFFZ+fMFoCqx1ksd65FJh/7Ov7dj0jc//ZdJq3aS2NN3e5eRca4V7rz6y/emOp6Ozzuhz7LbGo2v2Pret0D9aWehYt3vU+/EF19qAyXgw2rNtR2y4rLy3ftnRnx978C7yM9bZdXsTjZdfXqC6Wgdf0ikNnBP1T6AGYG0Cpjo2IhtcZjy0ANXYlH6uDL1xdGxsdLvzlupVdULJOeuRo2+EVqISamX0meP37H2slAxP3rtzVK8/XmZxDk+qF0of23vPcbo/rYuavTQx3SBNVIlgRieMhOZXGj1UXeAlAk1GjtLE5TIt9uyeLX1eb/HK4OCOX90+GFxZXF/XN7BHUfS6QovbFiqXyp3OkkLuwXLFl8POuOJwG+jS9oFm2de8dTsoVXtHMalVtjQut1rclmUcy+/S5VuWO7Yo6oFctpfiqQJ4KgYvANVHtmkRmpCGuKpEOt+EUikWj3PjCXTRYGTjgk0tisNfti8cZ3jwxWitskGSA3IIUlqzyw0AHQDeoMFnzwKgGESMIkg9ky+AbQ4mTMVWREMmEeLsNZgRbIDJYjLZBGbOV4+DrQqYp/uCAbMjk1JDUmkOCTHiBQgzNH++Zi02gU8Asr1aNm0yCuwVWuCm+R4HvsFrlxJHVmpOvYwZILEeDQ5AHE6wV9jBNCD0L4nk+1CKZPz1cipDkVlxgxQ1x1BHzJDuWi18HckW6CRtfwQhzNW2tdUq80Sb7KLdDIh1Xuxm6DJnlQ8RVQSrhnhlljX3A+EAWzGu0nnCTsl6MB6naP6SIolly1wjJI50ACrijQMm4s0Svp3KPjsX+oqYBBFBwpbDTcUk1oPxKE5rJt28nOsmY1IpNnb+v2IS1JmKFpM0GjeC7jQxHUyE2UJjBkQNTrQKEPItBiMHWs47JafUwIFaevwhfyjMhYJyUNTig6YSbq115gvqtTPUwgk7OFJtvyUyulHiWEJYTto4GqmzeaZyTe7uOrRmzaEzeCHELbvhX309u0UIS2s2LL4/azKRggOX4nIE5N6e1T/U4mQFtwXO3g0n00ZzJSp/zetiF0iGI9GKPcHt9PiDqO2lcIM4nDwYl1WmFgtK2sx95xSnNy6raiw1nvoWWWavru90O4xFyZ9X1dd3NjS4Tp9mQ0mmQpIq2C8rJalyy7vOkkpTqXO57z3ycputxFpR1lzTOdvQicvVMvIy6fNUzKoVHk8Fx1ZA2avP0ItZWSXUDD7qMebV3zT3TBNqwAQ0CAcBvATwYChPcaywU8YaZa8k/3GF1xv2evsgiypt2tNbr8hrZWxvzSvIMUON47Kw16c+SkYafNv80+9Vy7J7mhzVfM93dZu5M4yDuRW9BRw+lrKg1dhnBcWG7AMi8yoSJp5GSGUhZDewsMJIrCsgcIOWwD2MLhD/rBBEJqLNgUBzyZqhwduGTpeJYtmaaJPLtevkQ40lTU5nUzRKNi+YWLiB3RJtPnnuJEzht9NDtw0OrYk2PnRyl8vVVNL0rZNN0Yg6nZ4wN9OJyMIdc74QfZSNkWisvrHnQaOjpiaGgJYy2YiI6exlX0bYgq+pobf/J/29DU0KVco45IQ2QS2iXhP8u28X3sNFu3w+agZdPi0Q6bJocIC2Nn4dFXpagwgukqFmEUrwYLHoIV5K0qIE0fJEAaeaJiyVx2JfxJSKXfPoyce2pBRDp58KMOR99Y3V5CQ5sXq+cqmbyLIN6o9Jz4ZUf2kj1XELxIMboOrzidmRz2aD5faoh9V7uKrZBDlGDs8HPa1+jyjJHwCLPyAbtbMEYS6HIMcxBqwnS6GWSb9occUOJl/AT6jQEvBa0p7MO3vPEuqddAma+0HDbxYNLmcxuNCC5/9U73CpGnWpsaWWlq5LDi4ejcpUjqPFP+diUdZDvaloBSfgz93peLtA4HWFBTP5+bmF8gJfWKS+zhewPH+RF3hmQa+j9aairmi1gPcCt4Q6B15pqSKqAfJmCgr0PJK6ZEl1XTQI+os8z+bzpJtywGTlDdgHECH3xNwINM4dcEAGruVhaeMg6Gkc6c4u9hwgHxpMdinptAttIuZDk4YcKQZKmtAMXDN2MoMVtE2IxQQbk3muNs64QJ8CTAtkBBAZ57wMxWtL+586Imjm2cFm7oDzKRUckHTCG52QN4aoYhrO9HjOzSiz1+JaiyX5fizm0yZpvziuLaN8xKn/8uFCyLRjyftiMSj9F+ZxTYv3FjpImG3goEQUw8QOkceFAVFeJLGr6agsbOzZut6fN6JvbvXo6uzYll6s/9Bf1LppoKuWc62utdicefXtNTZhfY7cL3Kz/YiQ4KKlIIRLiKZSmLUjAzeVDdoEe53O09qsH8nzr9/a01hY2V679K7F5ar1gq2mvT7PabPUrq7marsHNrUUMQvyZxcjL8JZCCjnDCJU3YKrVOIb2IAM1bmdC+Xk4a5wSNj15PMbmlu+eXd7rLm5FT8mUpM5if689ZnnJnr56u3lhZE/XaW+ObicfqZm0zXuY7rt3JP0DJisLMPAyf4Gjjdk5ymlLoudC4aIefjYkSPHfnzLLSZT9Pux9nv/7HtPtrBDw8fuO3L/39fVmkw96UmusK+iwrbib44cvP/4ncTe+8TBMNuyMjnaX1lptz8PsydG1d9sfuLAKtISyur9YP+QwSidsWWRGhM+KxlPvqBovR3Q/zjaBdV6LaTFsRmEvS4uAyuPsWIn3Q3QoFhxmDlHdrVGrRBcgjKRfNdHQdL4SEzE60MHzTZOJLu4qniqyVSFPgKTDuxPTOiG4HzLALZokNBi8ISz0gwLz52+GrnaMbnxgbtG2zs62kfvmsGB/CLMNsmZ7zh4YMMTqbPQYDZ+BVRDmAQWWAPUgiFAFr3afgOybzfJmXyGJitdY80vwsrGBQRsnBSbx7oyOQ1dLzfNPYe7TKZQqhjfoTROdpEpjOUFQPPKlB/G+I/ZN/rjFYwfPSNJPS7GzjS+S4Engm+wXHwI5p5jIes5FRRFshmKI3S9UIQ9Grkrwgbgood38p/gwv0yBi6b9WQe9mSeyqj/qdXX3Diu4GDr+uRbuKMf9+IIEjX4S8zbRQfqdBBr7+BQiucvP9Nt5VowayAo8hBvwN9IiGAK9KGVRxKgsBN5iTYP4ao928I+VCCoG2hZ5WgsCkebJh5sXfbN/9hc6auTvXUbmhubhH1rVv/Vlp6LW88d2de7rtYTZt8uz7O0V7uNfnHNyW7+GyPNK4NDlaSca97WXlCU37mZ+OsLGpqCvh0D+/beXWSqT9vtp7pmbjVkvJuwQ2YkWC80Eo/Ei1Z8RmYi1jQ9KFR9mIVpnMJ2Jn04p9k1rkk9o/OEtGeGbFK6VSKEWIo3/cXj1rrafYPFpLh37cr7t9/W1GwutbvVfycDZyf9ZlvpCo+xoKg8Ej5451ivMnzREWwZ9ht8Va2OOtIx9pBLKBbYf5ZWS73FJWyhcPT4jsGuUF5VfpuusOzWrrvvfdxUVlkiTqx7IGj3E6IziN0V1a4fPXp8U7R8WUFeyKUrtko6hy2wemDP8Se/EzDyHJfuC3EfcZfpbzwYMcs4yAJroXzGs55b9ndrR9791+mBMvcgkUzNu0MHaV9O8YmMFyL+PIyuOUvMjX1en3iOFCWjd8R7I1H9cz+SyaJv7tlmLkqVud/DaDL6L6iJQuD93NkZihvDO6QmRtAUt15CV+KRQjAFxJIrU+jlpkg+byzOyys28up18lnUXSvX9bR22irj2FkTbL/WsXxR3uyHeUU8q/u1vadyS2NgR0VP3VhPV0drSl4abj1k91gTGlyCLEpLooE9+9IPf/jSO19NCDt2Ln5OWgo1mhxepnJwLiaHepJ5dhcSiedG3OzVS9FLlyKvvhq5dCmaUwrx9F34ZzIyeDklg5qvlsF8/DOLCGAeEYtLYD4lGh1jKT3wL1UT3AsUI5dMLkZ7erdvig6NNjWqia9Rkl9GO1/dfedrndFNHxw7um+vcoPO6DJ0ajrTenNas5DeRWW4CNGLi/NrKKe/nYH4VwW5NWR5xIrOlzpXI/1wUdeK6RP4V+qP8VFFKChTR2snpJ7oAgW8Dpt0Or4g318deHFg3ead0RFPtT8fHF6O6WScZiYXpR65w+/vkKM17mCBSVtaWBB0rzzU0gjTPdK8abX8lVeY/wV+OLQRAAB4nGNgZGBgAOItptt64/ltvjJws2wAijDcVe3RRdD/LVjWMW8DcjkYmECiADckCq94nGNgZGBgfvHfgoGBZQMDELCsY2BkQAXxAGA7A+oAAHicY2BgYGDZMIqJwj6kqScEAFLgPBUAAHicY2AAAh+GE4wyjCaMKYyzGLcwnmB8wPiLSYpJj8mDKYmpiWka0zqmY0y3mNmYHZgbWERYNFhiWNawPGN1YI1ibWPdwXqD9QebElsY2wq2G+wu7GvY33FEcNRxrOO4wvGLU48zh3MB5yeuHK4j3ELcDdyHeHh4zHjSeBp4ZvGc41XgjeHdw/uDL4BvHj8PfwL/Mv4z/H8E1ASKBBoE3gjaCO4S/CTkI9QldEGYRzhAeIkIg0gEOgQAbkYyQwAAAHicY2BkYGCIZ0hh4GIAASYg5gKz/4P5DAAc+QHkAAAAeJxtkT1OwzAYht/0D9FKCARiYfECC2r6M3ZkaPcO3dPESVMlceS4Fb0DJ+AQHIKBM3AIDsFb80mVUG3Jfr7H7xcrCYBrfCHAcQTo+/U4Wrhg9cdt0o1wh/wg3MUAj8I9+rFwH8+YCQ9wC80nBJ1Lmju8CrdwhTfhNv27cIf8IdzFPT6Fe/Tfwn2s8CM8wFPwkjSpHeaxqZqlznZFZE/iRCttm9xUahKOT3KhK20jpxO1Pqhmn02dS1VqTanmpnK6KIyqrdnq2IUb5+rZaJSKD2NTIkGDFBZD5IhhULFe8n0z7FAg4sm5xDm3YpflnvtaYYKQ3/NccsFk5dMRHPeE6TUOXBvsefOU1rFL+U6DkjT3vcd0wWloan+2pYnpQ2x8V83/NuJM/+VDf3v5C7A1ZCwAAAB4nG1U53+bMBD1S1eGs9Mm6d6bjnTPdO+9dypjEfOLkBwBcfLfF92BDU759N7T3enuHlAbqPFTr/3/WcIAtmArtmE7dmAQQxjGCOoYxRjGMYFJTGEaM9iJXZjFHOaxG3uwF/uwHwdwEIdwGEdwFMdwHCdwEqdwGmdwFh7O4Twu4CIWcAmXcQVXcQ3XcQM3cQu3cQd3sYh7uI8HeIhHeIwneIpneI4XeIlXeI03eIt3eI8P+IhP+Iwv+Ipv+I4f+Ilf+I0/WMLfWl34vkl14gWhUl2iQi3HRbPp+aH1lSQ+6LgDw0JJywk55HBrTcdrmo4mPlnicTlCyYAzZks8zsrZmPW5iu6UrEraUEXJ0sEEKzZcblVqspDFiLzmfJ/eKzq1+WS6LKVt0kZZy9l4l3HGqJ8tQjeFpa30GMX6LZF4q6lJJJ2WOa3Tb0l/heAMwYZZL/bu4jeJtF1fmViWw6oKFybFwZGmVDK/v8DUt7NHGcHGDslmyL4yctqUzCa1XkdYHeplOuyTOGo9kVYL5RjPMig3+I66AyYIeMJA+LJhzEplwn6RSmYn0uv2RxdXJWqZJGqZEA1FqN0M2Iwuoxcm1IGxkUhCo+m4IriIsVDHiVi2IuK1uoGybWjPObBZoUU7JeYulMm87CHqMRKhYo0QGRJJnXoLueowlW6LtM/VikLV2kpscB4hWnHbhjozgD/igtAuVlMZd4ftMcqyMrAybnFWQeiOWKzlWyVEHcdSWJ+DC0w3xGkjscLn12U4acmIU+tJJ0y6TRWEymcjscyIjFkzKo3YXTamLJQjojR/kSsCWZcL2WfpzkuUxt0waZI2ODf7P0popNnf0UcLtlb7B9UZ6LQAAAA=`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `54eb-L3CfqCSspfeFtcfSpMsXj+EtaSA`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `4766-yeDpNMnm0BFhPxp8O6aAypnEQJo`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `4d62-WEHWhmPYFSGMD5okj9GI0cCgFbQ`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�v���\x0019ݑ��P\x0013U1[i��L��м</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected in the element starting with: "<script></p><p>    (function addCopyFunction() {</p><p>      const copyList = document.getElementsByClassName('copy-to-clipboard-anchor');</p><p> ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher?terme](https://annuaire-entreprises.data.gouv.fr/rechercher?terme)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration](https://annuaire-entreprises.data.gouv.fr/administration)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise](https://annuaire-entreprises.data.gouv.fr/entreprise)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/faq](https://annuaire-entreprises.data.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/vie-privee](https://annuaire-entreprises.data.gouv.fr/vie-privee)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/accessibilite](https://annuaire-entreprises.data.gouv.fr/accessibilite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis](https://annuaire-entreprises.data.gouv.fr/donnees-extrait-kbis)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/comment-ca-marche](https://annuaire-entreprises.data.gouv.fr/comment-ca-marche)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a class="fr-logo" href="#" title="république française"><span class="fr-logo__title">république<br/>française</span></a>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/etablissement/](https://annuaire-entreprises.data.gouv.fr/etablissement/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/administration/](https://annuaire-entreprises.data.gouv.fr/administration/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/entreprise/](https://annuaire-entreprises.data.gouv.fr/entreprise/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/api/](https://annuaire-entreprises.data.gouv.fr/api/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/rechercher/carte](https://annuaire-entreprises.data.gouv.fr/rechercher/carte)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/annonces/](https://annuaire-entreprises.data.gouv.fr/annonces/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/justificatif/](https://annuaire-entreprises.data.gouv.fr/justificatif/)
  
  
  * Method: `GET`
  
  
  * Evidence: `308`
  
  
  
  
Instances: 7
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr](https://annuaire-entreprises.data.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
### Other information
<p>In the absence of an explicitly specified caching lifetime directive in the response, a liberal lifetime heuristic of 1 year was assumed. This is permitted by rfc7234.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/sitemap.xml](https://annuaire-entreprises.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/robots.txt](https://annuaire-entreprises.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 2
  
### Solution
<p></p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `501215367`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `400731430`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `628372620`
  
  
  
  
* URL: [https://annuaire-entreprises.data.gouv.fr/](https://annuaire-entreprises.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `695292204`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>501215367, which evaluates to: 1985-11-19 02:29:27</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
