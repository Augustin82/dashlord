
# ZAP Scanning Report

Generated on Fri, 13 Aug 2021 06:18:05


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 7 |
| Low | 6 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 10 | 
| Cross-Domain Misconfiguration | Medium | 11 | 
| CSP: style-src unsafe-inline | Medium | 2 | 
| CSP: Wildcard Directive | Medium | 2 | 
| Reverse Tabnabbing | Medium | 10 | 
| Sub Resource Integrity Attribute Missing | Medium | 10 | 
| X-Frame-Options Header Not Set | Medium | 10 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Dangerous JS Functions | Low | 1 | 
| Incomplete or No Cache-control Header Set | Low | 10 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 1 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 41 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/favico.ico](https://pilotage.inclusion.beta.gouv.fr/images/favico.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation](https://pilotage.inclusion.beta.gouv.fr/experimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css](https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'; style-src 'unsafe-inline'; img-src data:; connect-src 'self'`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'; style-src 'unsafe-inline'; img-src data:; connect-src 'self'`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'; style-src 'unsafe-inline'; img-src data:; connect-src 'self'`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'; style-src 'unsafe-inline'; img-src data:; connect-src 'self'`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is properly configured to set the Content-Security-Policy header.</p>
  
### Reference
* http://www.w3.org/TR/CSP2/
* http://www.w3.org/TR/CSP/
* http://caniuse.com/#search=content+security+policy
* http://content-security-policy.com/
* https://github.com/shapesecurity/salvation
* https://developers.google.com/web/fundamentals/security/csp#policy_applies_to_a_wide_variety_of_resources

  
#### CWE Id : 693
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://emplois.inclusion.beta.gouv.fr" rel="noopener" target="_blank" class="btn btn-lg btn-link btn-ico">
                      <span>Accéder aux emplois</span>
                      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="19" viewBox="0 0 20 19">
                        <path fill="currentColor" d="M8.66517015,2.82577407 C8.34562066,3.18534827 8.34130426,3.73389577 8.67429909,4.0990571 L11.359,7.039 L1.46428571,7.03948778 C0.93400271,7.03948778 0.5,7.46464861 0.5,7.99431466 L0.506519822,8.10609811 C0.562491613,8.58254879 0.971880067,8.94914154 1.46428571,8.94914154 L11.354,8.949 L8.64311662,11.8995038 C8.28105469,12.2965343 8.31618249,12.9073498 8.7191121,13.2599671 C9.11604213,13.6073339 9.72177649,13.5739032 10.0771295,13.184224 L14.2544508,8.63732099 L14.3103844,8.56958432 L14.3728703,8.47818478 L14.4352531,8.3399089 L14.4491817,8.28987794 L14.462,8.193 L14.4705425,8.17556014 C14.4890266,8.12237865 14.5,8.06201568 14.5,7.99431466 L14.5,7.84422179 L14.4816817,7.71012206 L14.4677531,7.6600911 L14.4094639,7.52822311 L14.3908925,7.49865936 L14.3296866,7.41519605 L10.1084913,2.81453208 C9.75427649,2.42609678 9.14854213,2.39266615 8.7516121,2.74003295 L8.66517015,2.82577407 Z" transform="rotate(-45 10.56 5.732)" />
                      </svg>
                    </a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://communaute.inclusion.beta.gouv.fr/t/experimentation-reporting-iae/2664" rel="noopener" target="_blank" class="btn btn-lg btn-primary btn-ico">
                    <span>Accéder à la communauté</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="20" height="19" viewBox="0 0 20 19">
                      <path fill="currentColor" d="M8.66517015,2.82577407 C8.34562066,3.18534827 8.34130426,3.73389577 8.67429909,4.0990571 L11.359,7.039 L1.46428571,7.03948778 C0.93400271,7.03948778 0.5,7.46464861 0.5,7.99431466 L0.506519822,8.10609811 C0.562491613,8.58254879 0.971880067,8.94914154 1.46428571,8.94914154 L11.354,8.949 L8.64311662,11.8995038 C8.28105469,12.2965343 8.31618249,12.9073498 8.7191121,13.2599671 C9.11604213,13.6073339 9.72177649,13.5739032 10.0771295,13.184224 L14.2544508,8.63732099 L14.3103844,8.56958432 L14.3728703,8.47818478 L14.4352531,8.3399089 L14.4491817,8.28987794 L14.462,8.193 L14.4705425,8.17556014 C14.4890266,8.12237865 14.5,8.06201568 14.5,7.99431466 L14.5,7.84422179 L14.4816817,7.71012206 L14.4677531,7.6600911 L14.4094639,7.52822311 L14.3908925,7.49865936 L14.3296866,7.41519605 L10.1084913,2.81453208 C9.75427649,2.42609678 9.14854213,2.39266615 8.7516121,2.74003295 L8.66517015,2.82577407 Z" transform="rotate(-45 10.56 5.732)"></path>
                    </svg>
                  </a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://emplois.inclusion.beta.gouv.fr" rel="noopener" target="_blank" class="btn btn-lg btn-link btn-ico">
                      <span>Accéder aux emplois</span>
                      <svg xmlns="http://www.w3.org/2000/svg" width="20" height="19" viewBox="0 0 20 19">
                        <path fill="currentColor" d="M8.66517015,2.82577407 C8.34562066,3.18534827 8.34130426,3.73389577 8.67429909,4.0990571 L11.359,7.039 L1.46428571,7.03948778 C0.93400271,7.03948778 0.5,7.46464861 0.5,7.99431466 L0.506519822,8.10609811 C0.562491613,8.58254879 0.971880067,8.94914154 1.46428571,8.94914154 L11.354,8.949 L8.64311662,11.8995038 C8.28105469,12.2965343 8.31618249,12.9073498 8.7191121,13.2599671 C9.11604213,13.6073339 9.72177649,13.5739032 10.0771295,13.184224 L14.2544508,8.63732099 L14.3103844,8.56958432 L14.3728703,8.47818478 L14.4352531,8.3399089 L14.4491817,8.28987794 L14.462,8.193 L14.4705425,8.17556014 C14.4890266,8.12237865 14.5,8.06201568 14.5,7.99431466 L14.5,7.84422179 L14.4816817,7.71012206 L14.4677531,7.6600911 L14.4094639,7.52822311 L14.3908925,7.49865936 L14.3296866,7.41519605 L10.1084913,2.81453208 C9.75427649,2.42609678 9.14854213,2.39266615 8.7516121,2.74003295 L8.66517015,2.82577407 Z" transform="rotate(-45 10.56 5.732)" />
                      </svg>
                    </a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://twitter.com/inclusion_gouv" rel="noopener" target="_blank"><img src="./../../images/picto-twitter.svg" height="25" alt="Rejoignez-nous sur Twitter"></a>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 10
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js`
  
  
  * Evidence: `<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/AmauriC/tarteaucitron.js@1.9.3/tarteaucitron.js"></script>`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=600`
  
  
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/favico.ico](https://pilotage.inclusion.beta.gouv.fr/images/favico.ico)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css](https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/picto-close.svg](https://pilotage.inclusion.beta.gouv.fr/images/picto-close.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/picto-burger.svg](https://pilotage.inclusion.beta.gouv.fr/images/picto-burger.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-pilotage-inclusion.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-pilotage-inclusion.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to enforce Strict-Transport-Security.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
* https://owasp.org/www-community/Security_Headers
* http://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
* http://caniuse.com/stricttransportsecurity
* http://tools.ietf.org/html/rfc6797

  
#### CWE Id : 319
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css](https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-communaute-inclusion.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-communaute-inclusion.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-pilotage-inclusion.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-pilotage-inclusion.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/picto-burger.svg](https://pilotage.inclusion.beta.gouv.fr/images/picto-burger.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/picto-close.svg](https://pilotage.inclusion.beta.gouv.fr/images/picto-close.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/favico.ico](https://pilotage.inclusion.beta.gouv.fr/images/favico.ico)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-emploi-inclusion.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-emploi-inclusion.svg)
  
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyRpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoTWFjaW50b3NoKSIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDpFMTZCRDY3REIzRjAxMUUyQUQzREIxQzRENUFFNUM5NiIgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDpFMTZCRDY3RUIzRjAxMUUyQUQzREIxQzRENUFFNUM5NiI+IDx4bXBNTTpEZXJpdmVkRnJvbSBzdFJlZjppbnN0YW5jZUlEPSJ4bXAuaWlkOkUxNkJENjdCQjNGMDExRTJBRDNEQjFDNEQ1QUU1Qzk2IiBzdFJlZjpkb2N1bWVudElEPSJ4bXAuZGlkOkUxNkJENjdDQjNGMDExRTJBRDNEQjFDNEQ1QUU1Qzk2Ii8+IDwvcmRmOkRlc2NyaXB0aW9uPiA8L3JkZjpSREY+IDwveDp4bXBtZXRhPiA8P3hwYWNrZXQgZW5kPSJyIj8+SM9MCAAAA+5JREFUeNrEV11Ik1EY3s4+ddOp29Q5b0opCgKFsoKoi5Kg6CIhuwi6zLJLoYLopq4qsKKgi4i6CYIoU/q5iDAKs6syoS76IRWtyJ+p7cdt7sf1PGOD+e0c3dygAx/67ZzzPM95/877GYdHRg3ZjMXFxepQKNS6sLCwJxqNNuFpiMfjVs4ZjUa/pmmjeD6VlJS8NpvNT4QQ7mxwjSsJiEQim/1+/9lgMHgIr5ohuxG1WCw9Vqv1clFR0dCqBODElV6v90ogEDjGdYbVjXhpaendioqK07CIR7ZAqE49PT09BPL2PMgTByQGsYiZlQD4uMXtdr+JxWINhgINYhGT2MsKgMrm2dnZXgRXhaHAg5jEJodUAHxux4LudHJE9RdEdA+i3Juz7bGHe4mhE9FNrgwBCLirMFV9Okh5eflFh8PR5nK5nDabrR2BNJlKO0T35+Li4n4+/J+/JQCxhmu5h3uJoXNHPbmWZAHMshWB8l5/ipqammaAf0zPDDx1ONV3vurdidqwAQL+pEc8sLcAe1CCvQ3YHxIW8Pl85xSWNC1hADDIv0rIE/o4J0k3kww4xSlwIhcq3EFFOm7KN/hUGOQkt0CFa5WpNJlMvxBEz/IVQAxg/ZRZl9wiHA63yDYieM7DnLP5CiAGsC7I5sgtYKJGWe2A8seFqgFJrJjEPY1Cn3pJ8/9W1e5VWsFDTEmFrBcoDhZJEQkXuhICMyKpjhahqN21hRYATKfUOlDmkygrR4o4C0VOLGJKrOITKB4jijzdXygBKixyC5TDQdnk/Pz8qRw6oOWGlsTKGOQW6OH6FBWsyePxdOXLTgxiyebILZCjz+GLgMIKnXNzc49YMlcRdHXcSwxFVgTInQhC9G33UhNoJLuqq6t345p9y3eUy8OTk5PjAHuI9uo4b07FBaOhsu0A4Unc+T1TU1Nj3KsSSE5yJ65jqF2DDd8QqWYmAZrIM2VlZTdnZmb6AbpdV9V6ec9znf5Q7HjYumdRE0JOp3MjitO4SFa+cZz8Umqe3TCbSLvdfkR/kWDdNQl5InuTcysOcpFT35ZrbBxx4p3JAHlZVVW1D/634VRt+FvLBgK/v5LV9WS+10xMTEwtRw7XvqOL+e2Q8V3AYIOIAXQ26/heWVnZCVfcyKHg2CBgTpmPmjYM8l24GyaUHyaIh7XwfR9ErE8qHoDfn2LTNAVC0HX6MFcBIP8Bi+6F6cdW/DICkANRfx99fEYFQ7Nph5i/uQiA214gno7K+guhaiKg9gC62+M8eR7XsBsYJ4ilam60Fb7r7uAj8wFyuwM1oIOWgfmDy6RXEEQzJMPe23DXrVS7rtyD3Df8z/FPgAEAzWU5Ku59ZAUAAAAASUVORK5CYII=`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyRpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoTWFjaW50b3NoKSIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDpFMTZCRDY3REIzRjAxMUUyQUQzREIxQzRENUFFNUM5NiIgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDpFMTZCRDY3RUIzRjAxMUUyQUQzREIxQzRENUFFNUM5NiI+IDx4bXBNTTpEZXJpdmVkRnJvbSBzdFJlZjppbnN0YW5jZUlEPSJ4bXAuaWlkOkUxNkJENjdCQjNGMDExRTJBRDNEQjFDNEQ1QUU1Qzk2IiBzdFJlZjpkb2N1bWVudElEPSJ4bXAuZGlkOkUxNkJENjdDQjNGMDExRTJBRDNEQjFDNEQ1QUU1Qzk2Ii8+IDwvcmRmOkRlc2NyaXB0aW9uPiA8L3JkZjpSREY+IDwveDp4bXBtZXRhPiA8P3hwYWNrZXQgZW5kPSJyIj8+SM9MCAAAA+5JREFUeNrEV11Ik1EY3s4+ddOp29Q5b0opCgKFsoKoi5Kg6CIhuwi6zLJLoYLopq4qsKKgi4i6CYIoU/q5iDAKs6syoS76IRWtyJ+p7cdt7sf1PGOD+e0c3dygAx/67ZzzPM95/877GYdHRg3ZjMXFxepQKNS6sLCwJxqNNuFpiMfjVs4ZjUa/pmmjeD6VlJS8NpvNT4QQ7mxwjSsJiEQim/1+/9lgMHgIr5ohuxG1WCw9Vqv1clFR0dCqBODElV6v90ogEDjGdYbVjXhpaendioqK07CIR7ZAqE49PT09BPL2PMgTByQGsYiZlQD4uMXtdr+JxWINhgINYhGT2MsKgMrm2dnZXgRXhaHAg5jEJodUAHxux4LudHJE9RdEdA+i3Juz7bGHe4mhE9FNrgwBCLirMFV9Okh5eflFh8PR5nK5nDabrR2BNJlKO0T35+Li4n4+/J+/JQCxhmu5h3uJoXNHPbmWZAHMshWB8l5/ipqammaAf0zPDDx1ONV3vurdidqwAQL+pEc8sLcAe1CCvQ3YHxIW8Pl85xSWNC1hADDIv0rIE/o4J0k3kww4xSlwIhcq3EFFOm7KN/hUGOQkt0CFa5WpNJlMvxBEz/IVQAxg/ZRZl9wiHA63yDYieM7DnLP5CiAGsC7I5sgtYKJGWe2A8seFqgFJrJjEPY1Cn3pJ8/9W1e5VWsFDTEmFrBcoDhZJEQkXuhICMyKpjhahqN21hRYATKfUOlDmkygrR4o4C0VOLGJKrOITKB4jijzdXygBKixyC5TDQdnk/Pz8qRw6oOWGlsTKGOQW6OH6FBWsyePxdOXLTgxiyebILZCjz+GLgMIKnXNzc49YMlcRdHXcSwxFVgTInQhC9G33UhNoJLuqq6t345p9y3eUy8OTk5PjAHuI9uo4b07FBaOhsu0A4Unc+T1TU1Nj3KsSSE5yJ65jqF2DDd8QqWYmAZrIM2VlZTdnZmb6AbpdV9V6ec9znf5Q7HjYumdRE0JOp3MjitO4SFa+cZz8Umqe3TCbSLvdfkR/kWDdNQl5InuTcysOcpFT35ZrbBxx4p3JAHlZVVW1D/634VRt+FvLBgK/v5LV9WS+10xMTEwtRw7XvqOL+e2Q8V3AYIOIAXQ26/heWVnZCVfcyKHg2CBgTpmPmjYM8l24GyaUHyaIh7XwfR9ErE8qHoDfn2LTNAVC0HX6MFcBIP8Bi+6F6cdW/DICkANRfx99fEYFQ7Nph5i/uQiA214gno7K+guhaiKg9gC62+M8eR7XsBsYJ4ilam60Fb7r7uAj8wFyuwM1oIOWgfmDy6RXEEQzJMPe23DXrVS7rtyD3Df8z/FPgAEAzWU5Ku59ZAUAAAAASUVORK5CYII=`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/channel/UC06_yIYfzAiDOMTemH9q3OQ`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�PNG</p><p>\x001a</p><p>\x0000\x0000\x0000
IHDR\x0000\x0000\x0000 \x0000\x0000\x0000 \x0008\x0006\x0000\x0000\x0000szz�\x0000\x0000\x0000\x0019tEXtSoftware\x0000Adobe ImageReadyq�e<\x0000\x0000\x0003$iTXtXML:com.adobe.xmp\x0000\x0000\x0000\x0000\x0000<?xpacket begin="﻿" id="W5M0MpCehiHzreSzNTczkc9d"?> <x:xmpmeta xmlns:x="adobe:ns:meta/" x:xmptk="Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27        "> <rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"> <rdf:Description rdf:about="" xmlns:xmp="http://ns.adobe.com/xap/1.0/" xmlns:xmpMM="http://ns.adobe.com/xap/1.0/mm/" xmlns:stRef="http://ns.adobe.com/xap/1.0/sType/ResourceRef#" xmp:CreatorTool="Adobe Photoshop CS6 (Macintosh)" xmpMM:InstanceID="xmp.iid:E16BD67DB3F011E2AD3DB1C4D5AE5C96" xmpMM:DocumentID="xmp.did:E16BD67EB3F011E2AD3DB1C4D5AE5C96"> <xmpMM:DerivedFrom stRef:instanceID="xmp.iid:E16BD67BB3F011E2AD3DB1C4D5AE5C96" stRef:documentID="xmp.did:E16BD67CB3F011E2AD3DB1C4D5AE5C96"/> </rdf:Description> </rdf:RDF> </x:xmpmeta> <?xpacket end="r"?>H�L\x0008\x0000\x0000\x0003�IDATx��W]H�Q\x0018��>uө��9oJ)</p><p>\x0002��������"!�\x0008�̲K��覮*������	�(S���0</p><p>��2�.�!\x0015�ȟ���m���<c���\x001c�ܠ\x0003\x001f���<�y���\x0019�GF
ٌ����P(Ժ���'\x001a�6�i���V�\x0019�F��i�x>����6��O�\x0010�lp�+	�D"��~��`0x\x0008��!�\x0011�X,=V��rQQ�Ъ\x0004�ĕ^��J \x00108�u�Սxii�݊��Ӱ�G�@�N====\x0004��<�\x0013\x0007$\x0006����\x0000����v���b
�\x0002
b\x0011���</p><p>������^\x0004W������&�T\x0000|nǂ�trD�\x0017Dt\x000f�ܛ��{��\x0013�M�\x000c\x0001\x0008��0U}:Hyy�E����r��6��\x001d�4�J;D�����~>���%\x0000��k��{��sG=��d\x0001̲\x0015��^����f�L�\x000c<u8�w��݉ڰ\x0001\x0002��G<��\x0000{P��
�\x001f\x0012\x0016��|�\x0014�4-a\x00000ȿJ�\x0013�8'I7�\x000c8�)p"\x0017*�AE:n�7�T\x0018�$�@�k��4�L�\x0010D��\x0015@\x000c`��Y��"\x001c\x000e��6"x�Ü��</p><p> \x0006�.���-`�FY��ǅ�\x0001I���=�B�zI��V��UZ�CLI��\x0017(\x000e\x0016I\x0011	\x0017�\x0012\x00023"��\x0016��ݵ�\x0016\x0000L��:P�(+G�8\x000bEN,bJ��\x0013(\x001e#�<�_(\x0001*,r\x000b��A������\x001c:�冖��\x0018�\x0016���\x0014\x0015����t��N\x000cb���-���ዀ�</p><p>�sss�X2W\x0011tu�K\x000cEV\x0004ȝ\x0008B�m�R\x0013h$����w�}�w��Ó���\x0000{���8oN�\x0005����\x0000�I��=SSScܫ\x0012HNr'�c�]�
�\x0010�f&\x0001��3eee7gff�\x0001�]W�zy�s��P�xغgQ\x0013BN�s#�ӸHV�q��Rj��0�H��~D�`�5	y"{�s+\x000er�Sߖkl\x001cq��\x0000yYUU�\x000f���Tm�[�\x0006\x0002�����d��LLLL-G\x000e׾�����]�`��\x0001t6��^YY�	W�ȡ�� `N���6\x000c�]�\x001b&�\x001f&����}\x001fD�O*\x001e�ߟb�4\x0005B�u�0W\x0001 �\x0001����V�2\x0002�\x0003Q\x001f}|F\x0005C�i����\x0008��^ ����\x000b�j"��\x0000���<y\x001eװ\x001b\x0018'��jn�\x0015����#�\x0001r�\x00035������ˤW\x0010D3$���p׭T��܃�7���O�\x0001\x0000�e9*�}d\x0005\x0000\x0000\x0000\x0000IEND�B`�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/employeurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/metiers/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation/](https://pilotage.inclusion.beta.gouv.fr/experimentation/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/donner-votre-avis/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `username`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/prescripteurs/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord/criteres/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats/](https://pilotage.inclusion.beta.gouv.fr/stats/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected in the element starting with: "<script type="text/javascript"></p><p>      tarteaucitron.user.googleFonts = 'families';</p><p>      (tarteaucitron.job = tarteaucitron.job ", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+C+"'></a>`
  
  
  
  
Instances: 1
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/favico.ico](https://pilotage.inclusion.beta.gouv.fr/images/favico.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css](https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation](https://pilotage.inclusion.beta.gouv.fr/experimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Age: 0`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Other information
<p>The presence of the 'Age' header indicates that that a HTTP/1.1 compliant caching server is in use.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg](https://pilotage.inclusion.beta.gouv.fr/images/logo-ministere-emploi.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord](https://pilotage.inclusion.beta.gouv.fr/tableaux-de-bord)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js](https://pilotage.inclusion.beta.gouv.fr/javascripts/app.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stats](https://pilotage.inclusion.beta.gouv.fr/stats)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/robots.txt](https://pilotage.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css](https://pilotage.inclusion.beta.gouv.fr/stylesheets/app.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/experimentation](https://pilotage.inclusion.beta.gouv.fr/experimentation)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr](https://pilotage.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/images/favico.ico](https://pilotage.inclusion.beta.gouv.fr/images/favico.ico)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=600`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/sitemap.xml](https://pilotage.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request. </p>
  
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
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `06201568`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `71012206`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `47818478`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `42609678`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `03948778`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `18534827`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `12237865`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `66517015`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `81453208`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `93400271`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `58254879`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `562491613`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31618249`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `72177649`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `34562066`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `99431466`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `64311662`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `73389577`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `84422179`
  
  
  
  
* URL: [https://pilotage.inclusion.beta.gouv.fr/](https://pilotage.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `11604213`
  
  
  
  
Instances: 41
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>06201568, which evaluates to: 1970-03-13 18:39:28</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
