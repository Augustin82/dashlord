
# ZAP Scanning Report

Generated on Sat, 12 Jun 2021 04:25:59


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 4 |
| Low | 5 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| CSP: Wildcard Directive | Medium | 2 | 
| Reverse Tabnabbing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 12 | 
| Feature Policy Header Not Set | Low | 11 | 
| Incomplete or No Cache-control and Pragma HTTP Header Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 1 | 
| Storable and Cacheable Content | Informational | 10 | 
| Storable but Non-Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 158 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/robots.txt](https://volontaires.fonction-publique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/sitemap.xml](https://volontaires.fonction-publique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Content-Security-Policy`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a title="Voir le code source" href="https://github.com/betagouv/renforts" target="_blank" rel="noopener">Voir le code source</a>`
  
  
  
  
Instances: 11
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-analyste-suivi-donnees](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-analyste-suivi-donnees)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-secretariat](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-secretariat)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/conseiller-contact-tracing](https://volontaires.fonction-publique.gouv.fr/missions/conseiller-contact-tracing)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-cadre-specialise-en-marches-publics)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-logisticiens](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-logisticiens)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form>`
  
  
  
  
Instances: 12
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "public-sector-yes" "public-sector-no" "fonctionnaire-yes" "fonctionnaire-no" "retired-yes" "retired-no" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Feature Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Feature Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Feature Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/sitemap.xml](https://volontaires.fonction-publique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/robots.txt](https://volontaires.fonction-publique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to set the Feature-Policy header.</p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Feature-Policy
* https://developers.google.com/web/updates/2018/06/feature-policy
* https://scotthelme.co.uk/a-new-security-header-feature-policy/
* https://w3c.github.io/webappsec-feature-policy/
* https://www.smashingmagazine.com/2018/12/feature-policy/

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control and Pragma HTTP Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control and pragma HTTP header have not been set properly or are missing allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/css/custom.css](https://volontaires.fonction-publique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `public, max-age=0`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate; and that the pragma HTTP header is set with no-cache.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s)
##### Low (Medium)
  
  
  
  
#### Description
<p>The web/application server is leaking information via one or more "X-Powered-By" HTTP response headers. Access to such information may facilitate attackers identifying other frameworks/components your web application is reliant upon and the vulnerabilities such components may be subject to.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/sitemap.xml](https://volontaires.fonction-publique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/css/custom.css](https://volontaires.fonction-publique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/robots.txt](https://volontaires.fonction-publique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
Instances: 11
  
### Solution
<p>Ensure that your web server, application server, load balancer, etc. is configured to suppress "X-Powered-By" headers.</p>
  
### Reference
* http://blogs.msdn.com/b/varunm/archive/2013/04/23/remove-unwanted-http-response-headers.aspx
* http://www.troyhunt.com/2012/02/shhh-dont-let-your-response-headers.html

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Content-Type-Options Header Missing
##### Low (Medium)
  
  
  
  
#### Description
<p>The Anti-MIME-Sniffing header X-Content-Type-Options was not set to 'nosniff'. This allows older versions of Internet Explorer and Chrome to perform MIME-sniffing on the response body, potentially causing the response body to be interpreted and displayed as a content type other than the declared content type. Current (early 2014) and legacy versions of Firefox will use the declared content type (if one is set), rather than performing MIME-sniffing.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/images/favicon/favicon-32x32.png](https://volontaires.fonction-publique.gouv.fr/static/images/favicon/favicon-32x32.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/images/favicon/favicon-16x16.png](https://volontaires.fonction-publique.gouv.fr/static/images/favicon/favicon-16x16.png)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/css/custom.css](https://volontaires.fonction-publique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
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

  
#### CWE Id : 16
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur?fonctionnaire-radio=on&publicSectorRadio=on&retired-radio=on)
  
  
  * Method: `GET`
  
  
  * Evidence: `606c-jEasrdYTFJFhHGf/FaKVnkwtF6w`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Evidence: `6c13-IOOg6rl+RbIwoAPSPL1pb6FNO5s`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/images/organisations/logo-arsge-card.png](https://volontaires.fonction-publique.gouv.fr/static/images/organisations/logo-arsge-card.png)
  
  
  * Method: `GET`
  
  
  * Evidence: `org/std/Iptc4xmpExt/2008-02-29/`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid)
  
  
  * Method: `GET`
  
  
  * Evidence: `66f9-aE7ZUgm/do/ONzF9nexYQkL88pI`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `66fe-kLpuArbCDN3VsBwzTBK2hf1P65s`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `28df-lpQAARQm7gFtscABY4QVbXxCilE`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5798-RrFGWB1k3S/WcC0gs+pUpF7N2GM`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `5917-U/bc5r+60SoHtSU/Su628H/lk0Q`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Evidence: `606c-jEasrdYTFJFhHGf/FaKVnkwtF6w`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `55dc-36WRoVDA6lbor2zR89o78+vQVLQ`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `6239-42HmyYV65zNLpy9JwbFu4jAf5wE`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�N��1\x001a��XLRE�q��V�Vy0�^�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 8
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bTODO\b and was detected 2 times, the first in the element starting with: "<!-- todo(estellecomment) : import min css and js -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `TODO`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/js/dsfr.module.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `from`
  
  
  
  
Instances: 3
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bSELECT\b and was detected 3 times, the first in the element starting with: "  select: {", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css](https://volontaires.fonction-publique.gouv.fr/~/@gouvfr/dsfr/dist/css/dsfr.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>`
  
  
  
  
Instances: 1
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>Links have been found that do not have traditional href attributes, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/robots.txt](https://volontaires.fonction-publique.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr](https://volontaires.fonction-publique.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/sitemap.xml](https://volontaires.fonction-publique.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/mentions-legales](https://volontaires.fonction-publique.gouv.fr/mentions-legales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/](https://volontaires.fonction-publique.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants](https://volontaires.fonction-publique.gouv.fr/missions/cellule-de-crise-communicants)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/faq](https://volontaires.fonction-publique.gouv.fr/faq)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/autres-missions-1](https://volontaires.fonction-publique.gouv.fr/autres-missions-1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1](https://volontaires.fonction-publique.gouv.fr/missions/charge-mission-gestion-crise-covid-1)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur](https://volontaires.fonction-publique.gouv.fr/missions/gestionnaire-renfort-covid-investigateur)
  
  
  * Method: `GET`
  
  
  
  
Instances: 10
  
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
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/static/css/custom.css](https://volontaires.fonction-publique.gouv.fr/static/css/custom.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000088564`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000072690`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000096791`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000059659`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000071106`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000079390`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000075991`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000063741`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000052190`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000075329`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000047667`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000125540`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000047958`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000075078`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000040886`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000057024`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000067430`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000068970`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000104799`
  
  
  
  
* URL: [https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf](https://volontaires.fonction-publique.gouv.fr/documents/plaquette_pour_superieur.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `0000062180`
  
  
  
  
Instances: 158
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>0000088564, which evaluates to: 1970-01-02 00:36:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
