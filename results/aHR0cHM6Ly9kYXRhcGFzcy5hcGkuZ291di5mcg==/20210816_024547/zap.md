
# ZAP Scanning Report

Generated on Mon, 16 Aug 2021 02:36:53


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 1 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 5 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 6 | 
| Permissions Policy Header Not Set | Low | 7 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 3 | 
| Information Disclosure - Suspicious Comments | Informational | 2 | 
| Modern Web Application | Informational | 6 | 
| Non-Storable Content | Informational | 5 | 
| Storable and Cacheable Content | Informational | 6 | 
| Timestamp Disclosure - Unix | Informational | 164 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
Instances: 5
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js`
  
  
  * Evidence: `<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js`
  
  
  * Evidence: `<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Dangerous JS Functions
##### Low (Low)
  
  
  
  
#### Description
<p>A dangerous JS function seems to be in use that would leave the site vulnerable.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 1
  
### Solution
<p>See the references for security advice on the use of these functions.</p>
  
### Reference
* https://angular.io/guide/security

  
#### CWE Id : 749
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-store, must-revalidate`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 6
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js](https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  
  
Instances: 7
  
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

  
  
  
  
### Server Leaks Version Information via "Server" HTTP Response Header Field
##### Low (High)
  
  
  
  
#### Description
<p>The web/application server is leaking version information via the "Server" HTTP response header. Access to such information may facilitate attackers identifying other vulnerabilities your web/application server is subject to.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css](https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
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

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css](https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that the application/web server sets the Content-Type header appropriately, and that it sets the X-Content-Type-Options header to 'nosniff' for all web pages.</p><p>If possible, ensure that the end user uses a standards-compliant and modern web browser that does not perform MIME-sniffing at all, or that can be directed by the web application/web server to not perform MIME-sniffing.</p>
  
### Other information
<p>This issue still applies to error type pages (401, 403, 500, etc.) as those pages are often still affected by injection issues, in which case there is still concern for browsers sniffing pages away from their actual content type.</p><p>At "High" threshold this scan rule will not alert on client or server error responses.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx
* https://owasp.org/www-community/Security_Headers

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.0e0727bd.chunk.css](https://datapass.api.gouv.fr/static/css/2.0e0727bd.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js](https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `fr/loda/id/LEGIARTI000034459398/2017-04-24/`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/TR/2001/REC-SVG-20010904/DTD/svg10`
  
  
  
  
Instances: 3
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>wOFF\x0000\x0001\x0000\x0000\x0000\x0000\x0018�\x0000\x000b\x0000\x0000\x0000\x00002\x0014\x0000\x0001\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000GSUB\x0000\x0000\x0001\x0008\x0000\x0000\x0000;\x0000\x0000\x0000T �%zOS/2\x0000\x0000\x0001D\x0000\x0000\x0000A\x0000\x0000\x0000VI�N�cmap\x0000\x0000\x0001�\x0000\x0000\x0001�\x0000\x0000\x0005�4��\x000cglyf\x0000\x0000\x0003\x0010\x0000\x0000\x0011\x0011\x0000\x0000!ܳ��\x0013head\x0000\x0000\x0014$\x0000\x0000\x00001\x0000\x0000\x00006\x001c��hhea\x0000\x0000\x0014X\x0000\x0000\x0000\x001c\x0000\x0000\x0000$\x0008r\x0004\x000ehmtx\x0000\x0000\x0014t\x0000\x0000\x0000\x0011\x0000\x0000\x00014d@\x0000\x0000loca\x0000\x0000\x0014�\x0000\x0000\x0000�\x0000\x0000\x0000�\x001dU&<maxp\x0000\x0000\x0015$\x0000\x0000\x0000\x001d\x0000\x0000\x0000 \x0001a\x0000`name\x0000\x0000\x0015D\x0000\x0000\x0001\x001d\x0000\x0000\x0001�\x0014���post\x0000\x0000\x0016d\x0000\x0000\x00020\x0000\x0000\x0005\x0003{vxlx�c`d``�b0`�c`rq�	a��I,�c�b`a�\x0000�<2�1'3=��\x0003�\x0003ʱ�i\x000e f��\x0002\x0000&;\x0005H\x0000x�c`dY�8��������\x0003H���L\x000e\x000cV��@����\x0001+\x0008HsMap���ч��\x0001�\x001c�\x0003\x000c\x001f� 9\x0000z\x0005\x000b\x0014\x0000\x0000\x0000x���Wn�@\x0000\x0006�%w���{�w[��1r�<�'p8�s�\x0010�v�\x0005\x001b�K�\x0015���K5������r�Ҝ��՜��yM�����S�\x0015���\x001c[�kk�\x0013�h����n���K\x001f�\x000c0�\x0010Ì0�\x0018�L0�\x0014��0�\x001c�,��\x0012ˬ��\x001a�l��V��\x001dv�c�\x0003\x000e9�\x0013N9�\x000b.��\x001bn��\x0007\x001ey�\x0017^y�\x000f>��Q~X\x001b���C���Yõ��j�\x0004�\x001a\x0016�o�\x001a-���\x0008lg`�Tt\x0007�\x001e~]�\x0013����\x0005�?�\x0003�\x001d\x000c�P`�\x0003;\x0012����\x0005v<�\x0013��\x000c�T`�\x0003;\x0013����\x0005v>�\x000b�]\x000c�R`�\x0003�\x0012����\x0005v=�\x001b��\x000c�V`�ÿ��	�n`�\x0002�\x001f؃�\x001e\x0006�(�ǁ=	�i`�\x0002{\x001e؋�^\x0006�*�ׁ�	�m`�\x0002{\x001f؇�>\x0006�)�ρ}	�k`�\x0002�\x001e؏�~\x0006�+����\x00174#��\x0000\x0000\x0000x��Y\x000bpSgv��^��O�B��\x0018[����z�l���\x0001����\x000b�\x0003��qBB!��@B3Ŕ!@Ɇj3l6�8�5\x001d6�n�nôԙ�jw���!L��\x001d�;��t6�N�\x001b\x001c�u����J����b�կ�����s�s�/�c��\x000f\x0018z�!���`j\x0019\x0006|�M�\x0015\x001by#_!y%oq8\x0014\x000eq8��A\x001d���/\x0002\x0001\x001c���\x0001���\x0003�:��:�\x001dP�\x001a�7��p}ú\x0015�/��˿�ꮬ��'7np�kPLF�\x001d\x001b�\x001b\x001a�\x001fjno\x001f�_�\x001b�3K�\x0010���2L�+-QEZJ\x000f\x000e�h&0J\x0011�&�S�\x000e$�\x0011'x|�㪃@\x0004|\x000e(1��\x000b\x0005�.�Ė!�&\x0008\x0015������\x0019��ƞ���������RX�Z�����;/T,5�۠=4\x0018</p><p>
>Nn�������3s�P
�m)��lm�\x0015lk��s\x0015��ѯ�\x0018\x001c>i�����>�CY��:\x0015�)�L\x000b�03�Q�z\x0007q?�~�/�\x0005w�\x001d�f�_"\x001b\x0013</p><p>�'.�<a�J<��\x0013Yt<����`8\x001c�:t'5���帒��M\x0013eֻt�b1D���?��\x000cX�\x0016�സ-� r�\x001a���ނ��A�B�z�0�u2\x0016F`J\x0019&\x000fl�\x001dn'ٜ0���8�\x001f$\x0017{\x0002>�Mb�tO��"#|b\x0014�\x0016\x000f(��-��EA��d��\x0017pM\x0005&Sr���p"AD1d�/a\x00163��8�\x00138��\x0005�lLԍ\���O��k�#v<�\x0007\x0005&\x0012T��?����br\x0019�\x0003b\x001e��\x0002�i(��GգQ(T�O��`LV��n'�i���\x001e��\x0010&k؁�n�=uB��{Qu\x0002"Q��}�~Nh\x0003\x001a\x0015�y �)v{�\x0012��4ᢢNFa\x000cƢ\x000cK�\x001ea/����N�\x001e�F�\x0008p^a���\x0014Rf/$O�Ǣ��d��׵5��7Q\x0016�{"a�P$�}'!�7�CVoi�	\x0018M�Ё#��ޔ\x0013i]\x0004�5�\x000b]�:t\x0015`��\x000cm\x0010�����@\x0002g��R'e\x0018#v*J��N2c��l'f�A�BuD�*�d��\x0003�����\x001d���\x0008'\x000f��WDz����\x0003\x0018�#�dMB�L�S��Cױ/\x0010F�\x0004�3%�\x00138H�Md��\x0010e��</p><p>�?</p><p>W�1����n�1\x0006���3~Bv\x0006��F�tz�ئ�+�\x000e�\x000fQb\x000e9�#
T\x000e#}y@7'��\x0002i����q��Be\x000ccuZJxtso\x0010�>�\x001d�</p><p>�Z\x0008l8�~���.L\x001f\x0013��\x0017q�>��.�1<\x0015��F\x0004�]���B"!���u�y
��\x001c#2nFB\x0019���"n��jt\x00128�\x0011�8��8�F��\x000c0�\x0018W\x0011S\x0012�w�</p><p>n9>�K\x0019VPfq��W����1��\x001eK���\x0002\x0003�W�~4�9
��<U��ϓ\x000b�baX</p><p>����>\x000b\x0016�ܒ�A��\x0015ӳ a�V�,��̑/� �Y�$`%�D\x0004]��O��Ϟ���|�|n����s�9\�\x000bq��o�G�/����� ӗS�W��/���N�S8��S2�s?�9��q ��r\x0011w�\x001ft��%\B�\x000b�.��\x0004L�{q��)%���\x0001�\x0005��eu/�'��ߙt�$�9���E�Ӓ㷸�x�0L����\x00015B�</p><p>9(\x0019<�]썘�&\x00157K�\x0007�\x00142L\x0018�5/��1���1��\x0006Y\x001dP��@����)���-�~��i�\x000f��mL>cBou\x0007!�[�Y�H���[l���t�l��=��J����T�a�I�v����\x0019+�w	\x0004q\x000e��𧨚��,�4��]"�\x0006Y�i�	i���\x0015���i9��`\x0001\x0008$\x0007�3b��A�!\x001f�M&\x0010��b���Wԧd8�){\x0001�*�ޢ&;-��\��'�L^=D�W�:�T�\x000e\x0010IqUA�\x0008�CV��aoڱ�6\x001ay�+�Yu���}?\x0010�\x001f�;���G\x0007�F����\x0014ŕ�ۆ�mf8\x001ay����c�\x0016q5�\M]��-om����\x000f�[S��wkk�mصkú�ڙ���R�)�R���r\x0013�u�)b\x001c�\x00075kŘ�
�BR\x0018�\x0014�\x000e6\x0014�LP�\x001f��;�p���&g�B\x000eV䍀\x001fF�\x0003�������+_�r�\x0019��|��m\x0016O����H����΂��/���U.8��</p><p>O���ֵO~��y�m��԰����\x0012����-/��\x0014�vE����\x000fw�^�\\x0010\x0018)/p��>R���UA�i_�g������u�Ňy��G�\x0017��k[��k�0�T�\x0017�\x0007B	�'\x001a��\x0006�a�\x001b���7�-dӂ\x0014�t�Y\x0011�y���-���ګ�E��\x000e\x001e�\x0019^A�D+�O\x001d}|�\x0015���\x0019\x001a��9���5|^�l=3��Q�>��
e(C\x0011� V\x0006�n\x00084Y���D*\x0017��\x0012�ǹ�\x0004	at�\x0013�]-���X\x0019dx�U��~��\x000f�Øn,n\x000f\x0012t"y�F�=��b�(��x�
�い��F��(�8}\x0017g\x0004;r*1��\x00023\x0013˃��\x0002ɡ�P��L�;	�\x000e\x000b1�A</p><p>�4�ݵ\x0015�\x0013���5Z�3�\x0004�\x0006->Sz\x000f��\x0018�Vpf�M\x001a�\x0016��z5:Hq8��`\x001bR�H,&�w�����Q.bC�Yz�\x0015� �\x0006�\x0015ss	_
�\x0006=O[�\x0010� 6&U�,�&�h��XXC:
\x0003՟�U\x001e"��\x0011�xf�k��U8i���Y��m=\x0010�S6\x0017)�X��5A.\x00119�\x0015�đ\x0013�d\x0018�Am��+i��5Wr�B$�\x000edˈ�(�5�^�o�i=c���k��\x0007�ʤ��<��A�O�,�\x0018k@�����}�;
L\x001b#3\x000fQ|E��D��)��h���y���8tKo \x001c\x0008G�p�\x001f\x00125,�\£���P���\x001a��\x0003;�9��#}\x0012�\x0002���7"W۽\x0013�&�w������\x0000<~\x000f�W��l�������gL&t:x+*%�<[2z{��\x0015��j�{\x000f�L\x000bͥ��\x001aB�\x000e͏[�g\x0011���
���[�\x00018]<\x0006��O#\x0016�����1.�T\Qo5��9\x0014;��vx����/+jk;���'O��$S&Ie���T^��kQ���Z��\x0008���\x0017��\x00167VvL�u����p\x00156x˦�2���c˼��$�bǪ�:k]\x001c .��k\x000cji�\x000e"�h��Rqo\x0017|
u����]]�B�����vA-�ы8�{�<#/=������i�hȐ��V��6)rh�$�!-�<��\x0012�\x0014gPCE�W ZF)q8�\x0012L�=z�60�\x0018:K�<ҺJ1\x0002>:��\x001d��Jx\x0016����\x0011�k��W�\x0019���=H\x001f��\x0019�V��jN\x001eX�yl&Y�\x0011���8W1��#p`6�[�\x000fAI�\x0004U�	����a	�d\x001cc$u�\x0015k��\x001f-\x0002ف�\x001b�sJI�߂֤��k\x000e�|�M\x0018�*��\x001fF�f^�;M@�\i��a\x001c���\x000bŸ*Zb/\x0018会�z��p�5\x001f�{iT��v@)�</p><p>�A��\x001b</p><p>�'��\x001b�
��P}��gy~�\x0017��=c�\x0003��h+1\x0003��-�ph�}Y%�7����\x0013Q\x0017l��q��3��l\x001e\x000f�T\x0003&#�~E�\x001a��h�8\x000f�En�\x001eH\x0005\x0007\x0010�q���\x001ba^\x001eHv)��Ob"�#!��z\x000f:iB\x000bp-�a\x0012���]��\x0004l�r�|��OA�	3\x0013"�\x000c�P��\x0014�T���g\x001b�~��c\x0015�X��E@�&FX�4���\x000c�(�w�Z+��\x0013��k��L!��F��S��\x0017��%\x000f�b0�̭'\x001a��0��\x0006\x0011��ò^��\x0003�{�����\x0014\x0018�m�\x0005�=��\x0004rw�46{
�\x000e\x0014#뎢\x0010Ja�ڍ]U�{eU�ݕ[�Zi\x0017�d�A�\x0007:�@Ӆ\x00057-�#P\x0007<9�v\x0010\x0005\x001e�*�\x000b�j����ߑ\x001bX�������j���P�W�\x0011앭��.{I��e\U�ƵM�̜:�����,��sF\x0011;%�m��:6�ǎ������h$,<��뽍M�<�\x001akll&\x001fg�ɬB�����e[J\x000b�?kW�\x001bXB?��T_�\x0018�p��\x001e0@�\x0019;#\x001bJ��\x0003u\x001c�qd\x0007�o\x0006(��]��Ba�\x000c\x001f9x��ϖ/7���b�{���\x0017����#�\x000e~���UfsOz�\x001b���K_;��Gw�c���"lӊ�Hy���:�\x001e\x001bQ������\x0014����9\x0007C�t:�E\x001aL�<�D�
E�����$.�\x0012��RZ�4�\x0008�z�$�r\x0019\x001b�\x0004c\x0014�a��p�̮�F!B�r6������\x0011�P�O\x0000��?���*���@\x0005�\x0008Rt��r�a\x0010�w1�\x0016�\x0012�\x0018��\x0019eF	ϝ�-�n;��ԣ#�mm�#�N���Y�m𧿓�S���{�Ѭ�\x0006��\x0008\x0004�D\x0003�$ad\x0016��z\x001f�\x000b
�t=C�������s\x0004�;/6\x001e�J�4�}����u�H�J�;�h�.�Hry>�\lx����rvC�x)\x0013 �\x0008�O</p><p>�\x0004�\V�	ȅ�K\x000eJaF�� 'Ź߂E:�܃��G���eG�ӷ�7���'�\x000c��N��*;���յ�ի{�\x001a�\x001f�(-���I����o�E\�]���\x0017�\x0006G�B�et��\x001c\x0017��-�~>�+�&�B�\x0006 &\x000f�F�;����\x000b�����
��K��\x0007�~�'\x0014\x000c\x0004C��M����H����������r_�������A�ݹ�o\x001e�\x0019������VWy#��ܒ�e\x001eS@�|��rg��`9�r��[�\x000b�:�C�6��!�ۺq��c���T�\x001e�>�����\x00181�A`�ǔ\x0010\x0013�Ө��������~558�F�'`b�\x0013:H�\x0019�'25��fqt�xcv�ηfDQ��|YF\x000ePs�P�3?&fȷA�\x001e�\x001b�I���n��蟰/0#\x0002x2����8L�&�J�\x001c���W</p><p>�\x0014</p><p>\x000b7&H�O@\x001eo*��-2��\x0014�o�S��i_"�\x001c���\x0006�/̝�4��g
�v��?T\x001f�Z�S}����Y���;\x0007+\�\x0017\x0019�e\x0016�\x0005���~�?}�_�Y\x0010v�s�礅H���*��k>;�B��=,��~���k�k��ߖ�]�f�B<�\x0014�3i\x001b\�mP��6��r\x001e\x0003�\x0012b~\x000b̖D���\x0007��z�g�cd��x�gݖ�����z5�-N�ю���z�#���#�w�*���!-��3�\x000f�5s�׆�\x0008=�9�Er�����W��h]��_</p><p>���D?�@ ��\x0010�7HA����C~\x0002\x0010Xn@-\x0018������\x0018����2������Cѝ�e�<\x0013ϥ�on\�O'�4?\x001f�z�m�@�?Z�	�\x0017��\x0014�<+�7��\x001e	\x001f�5\x001a8����G��\x0001��*�\x0000\x0000\x0000x�c`d``\x0000b��\x0007����|e�f�\x0000\x0014a�3�*/��/����\x0000����\x0004\x0012\x0005\x0000ce\x000c#\x0000\x0000\x0000x�c`d``>�_���e\x0003\x0003\x0003�dd@\x0005�\x0000V�\x0003�x�c````�0�I�\x0000�%5q\x0000\x0000\x0000\x0000\x0000\x0000\x0000\x0000L\x0000�\x0001\x001c\x00014\x0001d\x0001�\x0001�\x0001�\x0001�\x0001�\x0002\x001a\x0002.\x0002H\x0002b\x0002�\x0002�\x0002�\x0002�\x0002�\x0003\x0006\x0003@\x0003T\x0003�\x0003�\x0004\x0018\x0004D\x0004v\x0004�\x0004�\x0004�\x0005\x0010\x0005|\x0005�\x0006&\x0006L\x0006|\x0006�\x0006�\x0006�\x0007:\x0007n\x0007�\x0008:\x0008�\x0008�	\x001e	H	x	�	�	�</p><p>2</p><p>n</p><p>�\x000b</p><p>\x000bb\x000b�\x000c\x001e\x000cr\x000c�\x000c�
\x000e
8
�
�
�\x000eN\x000e�\x000e�\x000f\x001e\x000fd\x000f�\x000f�\x00108\x0010�\x0010�x�c`d``�e\x0008a�b\x0000\x0001& �\x0002����\x000c\x0000\x0019�\x0001�\x0000\x0000\x0000x�]��N�0\x0014�O��h\x0010\x0002!1��\x000bR�3�\x0001ڙ\x000e���I[%q丕*13�\x0014�<\x0005�ŉ{%*l��;�\x001e_\x001b�\x0003~\x0010�[\x0001��v��\x001b�\x000b�Iw�\x0003��\x0010!��GT/�c�b"\x001c�	o�\x0010\x000cn錑	�p�Z�O�]x@�\x0010\x001er�������\x00181��CL��>5u��űL�g_bm۽��<�y�ֵ��әڞU{*\x0016��*��R+S;]�F5�\x001ctꢝs�r:�ŏRSa�\x0014�n��F�#J$�W�\x001f�LX�tZa�\x0008������g\x00128�\x00193[�Y[�8{A�!�Ι1�H+�K�܆N�{\x0007:)�\x0008;��\x0012S��_>�W�0�Sb\x0000\x0000\x0000x�mS�Z�@\x0010Ԑf\x001b\x001bcC\x0002���\x0014�{���w8K'��ӝs�0~��v%[\x000e臾��m7+y\x000b\x001e?m��g\x0007\x000b8��8��8�\x0006�ha\x0011mt��.��C\x001f+X�i��\x001aֱ��8�󸀋��˸����븁���۸�������\x0000\x000f�\x0008���'x�gx�\x0017x�Wx�7x�wx�\x000f��O��-l�\x000b��\x001b��\x0007~�\x0017~c\x0007��\x0008\x0002��̏b��D�ZvE\x0018�Al\x0003%�7\x001cw�%���PB\x000e�֌�Ќ5�^���\x0008%#�X��(gS���t�\x0014U�J�\x000e�Y���p�&\x000bE�(kn��ϊ�\x000f��ԥ|DZ���u��3:Aa�\x000e�%Wf��</p><p>�2�+�\x001c\x001c�\x0003v(P&�u�[�8�\x0018J%3I�*L%���\x0008^ES�1o����� �V\x000b�\x0018�m�	g�\x001d0QDd5\x0012�\x001c\x0018�W������M���/Iԗ\x0010MFh\x0014F���ўb\x001d\x0019��,6���\x0004\x0017�\x0014�4\x0013�V$t�s�\x0017WҾs�\x001a)S�8C4F"b�\x001a!2.�:�7K�a�7\x0012����</p><p>U\x001b)1�<Bd��ƺ�����u��2��g�(����t�Y\x0015�\x001e��/�#D\x0013�R؀�+L\x001d�|�Y\x0011�Z[�P&����qV
�,nQGd��Qy�;c��B="��olN���B��\x001a�\x001bNL��\x0003���w>��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `xxx`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js](https://datapass.api.gouv.fr/static/js/main.04af181c.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 2
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bXXX\b and was detected in the element starting with: "(this.webpackJsonpdatapass=this.webpackJsonpdatapass||[]).push([[2],[function(e,t,n){"use strict";e.exports=n(248)},function(e,t", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript">/MSIE \d|Trident.*rv:/.test(navigator.userAgent)&&(document.write('<script src="https://unpkg.com/@babel/polyfill@7.0.0/dist/polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/url-polyfill@1.0.14/url-polyfill.js"><\/script>'),document.write('<script src="https://unpkg.com/stickyfilljs@2.1.0/dist/stickyfill.min.js"><\/script>'))</script>`
  
  
  
  
Instances: 6
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/sitemap.xml](https://datapass.api.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr](https://datapass.api.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/robots.txt](https://datapass.api.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22](https://datapass.api.gouv.fr/%5C%22mailto:contact@api.gouv.fr?subject=Erreur%2520sur%2520datapass.api.gouv.fr%5C%22)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/](https://datapass.api.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png](https://datapass.api.gouv.fr/favicons/apple-icon-180x180.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg](https://datapass.api.gouv.fr/favicons/safari-pinned-tab.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css](https://datapass.api.gouv.fr/static/css/main.15d01710.chunk.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-16x16.png](https://datapass.api.gouv.fr/favicons/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/manifest.json](https://datapass.api.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/favicons/favicon-32x32.png](https://datapass.api.gouv.fr/favicons/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  
  
Instances: 6
  
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

  
  
  
  
### Timestamp Disclosure - Unix
##### Informational (Low)
  
  
  
  
#### Description
<p>A timestamp was disclosed by the application/web server - Unix</p>
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11674146`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16775920`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `11393254`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `155497632`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16776960`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1120210379`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1019803690`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `405537848`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1839030562`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `722521979`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13789470`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `16738740`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1700485571`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/css/2.0e0727bd.chunk.css](https://datapass.api.gouv.fr/static/css/2.0e0727bd.chunk.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `23000091`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1069501632`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `10824234`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `15792383`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `909522486`
  
  
  
  
* URL: [https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js](https://datapass.api.gouv.fr/static/js/2.a3950311.chunk.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
Instances: 164
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>1073741823, which evaluates to: 2004-01-10 13:37:03</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
