
# ZAP Scanning Report

Generated on Thu, 26 Aug 2021 04:17:16


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 1 |
| Medium | 4 |
| Low | 13 |
| Informational | 10 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| PII Disclosure | High | 12 | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Reverse Tabnabbing | Medium | 11 | 
| Sub Resource Integrity Attribute Missing | Medium | 11 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Absence of Anti-CSRF Tokens | Low | 11 | 
| Application Error Disclosure | Low | 4 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cookie No HttpOnly Flag | Low | 2 | 
| Cookie without SameSite Attribute | Low | 4 | 
| Cookie Without Secure Flag | Low | 4 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 11 | 
| Dangerous JS Functions | Low | 4 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Information Disclosure - Debug Error Messages | Low | 4 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Content-Type Header Missing | Informational | 3 | 
| Information Disclosure - Sensitive Information in URL | Informational | 1 | 
| Information Disclosure - Suspicious Comments | Informational | 9 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 9 | 
| Storable and Cacheable Content | Informational | 1 | 
| Timestamp Disclosure - Unix | Informational | 42 | 
| User Controllable HTML Element Attribute (Potential XSS) | Informational | 15 | 

## Alert Detail


  
  
  
  
### PII Disclosure
##### High (High)
  
  
  
  
#### Description
<p>The response contains Personally Identifiable Information, such as CC number, SSN and similar sensitive data.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/642/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/642/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38758775100042`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2254/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2254/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50058634200015`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2776/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2776/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38341479400057`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3450/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3450/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38066864000051`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2368/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2368/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38073036600032`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3013/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3013/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50930450700023`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2236/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2236/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `50499856800027`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1541/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1541/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38776983900045`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1117/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1117/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38146854500060`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1471/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1471/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38442671400042`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/39/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/39/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38763298700021`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3664/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `38173482100030`
  
  
  
  
Instances: 12
  
### Solution
<p></p>
  
### Other information
<p>Credit Card Type detected: DinersClub</p><p>Bank Identification Number: 387587</p><p>Brand: DISCOVER</p><p>Category: BUSINESS CARD</p><p>Issuer: </p>
  
### Reference
* 

  
#### CWE Id : 359
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://itou.typeform.com/to/nxG0HlYx" rel="noopener" target="_blank" class="btn btn-primary btn-ico">
                                        <span>Contactez-nous</span>
                                        <svg width="17" height="15" fill="none" xmlns="http://www.w3.org/2000/svg">
                                            <path d="M16.5 13.505a.75.75 0 01-.744.745H2.244a.745.745 0 01-.744-.745v-.755H15V3.975l-6 5.4-7.5-6.75V1.5a.75.75 0 01.75-.75h13.5a.75.75 0 01.75.75v12.005zM3.325 2.25L9 7.357l5.675-5.107H3.325zM0 9.75h6v1.5H0v-1.5zM0 6h3.75v1.5H0V6z" fill="currentColor"></path>
                                        </svg>
                                    </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
            </a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://github.com/betagouv/itou-cocorico/"
               class="by pull-right credit" target="_blank">
                Github
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1133/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1133/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2124/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2124/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2424/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2424/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3309/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3309/show)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType=1&region&sector%5B%5D=121&sector%5B%5D=138&sector%5B%5D=86&sector%5B%5D=87&sector%5B%5D=88&sector%5B%5D=89&serialSectors&structureType=0&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType=1&region&sector%5B%5D=121&sector%5B%5D=138&sector%5B%5D=86&sector%5B%5D=87&sector%5B%5D=88&sector%5B%5D=89&serialSectors&structureType=0&zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType&region&sector%5B%5D=111&serialSectors&structureType%5B%5D=4&structureType%5B%5D=7&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType&region&sector%5B%5D=111&serialSectors&structureType%5B%5D=4&structureType%5B%5D=7&zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/filiere/recyclage](https://lemarche.inclusion.beta.gouv.fr/fr/filiere/recyclage)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/filiere/restauration](https://lemarche.inclusion.beta.gouv.fr/fr/filiere/restauration)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 11
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Absence of Anti-CSRF Tokens
##### Low (Medium)
  
  
  
  
#### Description
<p>No Anti-CSRF tokens were found in a HTML submission form.</p><p>A cross-site request forgery is an attack that involves forcing a victim to send an HTTP request to a target destination without their knowledge or intent in order to perform an action as the victim. The underlying cause is application functionality using predictable URL/form actions in a repeatable way. The nature of the attack is that CSRF exploits the trust that a web site has for a user. By contrast, cross-site scripting (XSS) exploits the trust that a user has for a web site. Like XSS, CSRF attacks are not necessarily cross-site, but they can be. Cross-site request forgery is also known as CSRF, XSRF, one-click attack, session riding, confused deputy, and sea surf.</p><p></p><p>CSRF attacks are effective in a number of situations, including:</p><p>    * The victim has an active session on the target site.</p><p>    * The victim is authenticated via HTTP auth on the target site.</p><p>    * The victim is on the same local network as the target site.</p><p></p><p>CSRF has primarily been used to perform an action against a target site using the victim's privileges, but recent techniques have been discovered to disclose information by gaining access to the response. The risk of information disclosure is dramatically increased when the target site is vulnerable to XSS, because XSS can be used as a platform for CSRF, allowing the attack to operate within the bounds of the same-origin policy.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="post" action="/fr/contact/creer">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form method="post" action="/fr/contact/creer">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae" class="s-hp-01__form bg-white w-100 rounded-lg shadow-lg p-3 p-lg-5">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `POST`
  
  
  * Evidence: `<form class="form-signup" action="/fr/inscription" method="POST" autocomplete="off">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/annonce/resultat-recherche" class="form-category alt col-xs-12">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-demande](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-demande)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form id="form-registerlogin" class="form form-signup form-reset-password"
                  action="/fr/mot-de-passe-reinitialisation-envoi-email" method="POST">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/identification-verification"
                          method="POST">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form class="form-signup" action="/fr/inscription" method="POST" autocomplete="off">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/repertoire/siae/export/csv?page=1">`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Evidence: `<form method="get" action="/fr/annonce/resultat-recherche" class="form-category alt col-xs-12">`
  
  
  
  
Instances: 11
  
### Solution
<p>Phase: Architecture and Design</p><p>Use a vetted library or framework that does not allow this weakness to occur or provides constructs that make this weakness easier to avoid.</p><p>For example, use anti-CSRF packages such as the OWASP CSRFGuard.</p><p></p><p>Phase: Implementation</p><p>Ensure that your application is free of cross-site scripting issues, because most CSRF defenses can be bypassed using attacker-controlled script.</p><p></p><p>Phase: Architecture and Design</p><p>Generate a unique nonce for each form, place the nonce into the form, and verify the nonce upon receipt of the form. Be sure that the nonce is not predictable (CWE-330).</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Identify especially dangerous operations. When the user performs a dangerous operation, send a separate confirmation request to ensure that the user intended to perform that operation.</p><p>Note that this can be bypassed using XSS.</p><p></p><p>Use the ESAPI Session Management control.</p><p>This control includes a component for CSRF.</p><p></p><p>Do not use the GET method for any request that triggers a state change.</p><p></p><p>Phase: Implementation</p><p>Check the HTTP Referer header to see if the request originated from an expected page. This could break legitimate functionality, because users or proxies may have disabled sending the Referer for privacy reasons.</p>
  
### Other information
<p>No known Anti-CSRF token [anticsrf, CSRFToken, __RequestVerificationToken, csrfmiddlewaretoken, authenticity_token, OWASP_CSRFTOKEN, anoncsrf, csrf_token, _csrf, _csrfSecret, __csrf_magic, CSRF] was found in the following HTML form: [Form 1: "_token" "email" "firstName" "lastName" "phone" "subject" ].</p>
  
### Reference
* http://projects.webappsec.org/Cross-Site-Request-Forgery
* http://cwe.mitre.org/data/definitions/352.html

  
#### CWE Id : 352
  
#### WASC Id : 9
  
#### Source ID : 3

  
  
  
  
### Application Error Disclosure
##### Low (Medium)
  
  
  
  
#### Description
<p>This page contains an error/warning message that may disclose sensitive information like the location of the file that produced the unhandled exception. This information can be used to launch further attacks against the web application. The alert could be a false positive if the error message is found inside a documentation page.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/cf5b90138467873a544dd24b3b9e76021487fb4b.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/cf5b90138467873a544dd24b3b9e76021487fb4b.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `HTTP/1.1 500 Internal Server Error`
  
  
  
  
Instances: 4
  
### Solution
<p>Review the source code of this page. Implement custom error pages. Consider implementing a mechanism to provide a unique error reference/identifier to the client (browser) while logging the details on the server side and not exposing them to the user.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/1abb1c03cee56e47505a4b255234e3a20c937175.png](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/1abb1c03cee56e47505a4b255234e3a20c937175.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=9&structureType%5B%5D=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=9&structureType%5B%5D=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/listings/images/0de96f0955389a322b94e602305d72a9db5ad8b4.png](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/user_profile/uploads/listings/images/0de96f0955389a322b94e602305d72a9db5ad8b4.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors&structureType%5B%5D=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors&structureType%5B%5D=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType%5B%5D=1&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=121%7C138%7C86%7C87%7C88%7C89&structureType%5B%5D=1&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-envoi-email)
  
  
  * Method: `POST`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/f8b53bbc1ddd4b41c8c7a73d9afd087d301fee56.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/f8b53bbc1ddd4b41c8c7a73d9afd087d301fee56.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/618483bd4a26928f5498c8f77f01d2e2dbdfad6b.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/618483bd4a26928f5498c8f77f01d2e2dbdfad6b.jpg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=111&structureType%5B%5D=4&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/export/csv?addressType&area&city&country&department&format=xlsx&lat&lng&page=1&postalCode&prestaType=1&region&sector%5B%5D=9&serialSectors=111&structureType%5B%5D=4&zip)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/4a7d5d2c1689eb950d960cdb7a53f54101c7df5b.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_small/uploads/listings/images/4a7d5d2c1689eb950d960cdb7a53f54101c7df5b.jpg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 135 [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xsmall/uploads/listings/images/1abb1c03cee56e47505a4b255234e3a20c937175.png].</p><p>Predicted response size: 435.</p><p>Response Body Length: 786.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie No HttpOnly Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the HttpOnly flag, which means that the cookie can be accessed by JavaScript. If a malicious script can be run on this page then the cookie will be accessible and can be transmitted to another site. If this is a session cookie then session hijacking may be possible.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that the HttpOnly flag is set for all cookies.</p>
  
### Reference
* https://owasp.org/www-community/HttpOnly

  
#### CWE Id : 1004
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie without SameSite Attribute
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the SameSite attribute, which means that the cookie can be sent as a result of a 'cross-site' request. The SameSite attribute is an effective counter measure to cross-site request forgery, cross-site script inclusion, and timing attacks.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
Instances: 4
  
### Solution
<p>Ensure that the SameSite attribute is set to either 'lax' or ideally 'strict' for all cookies.</p>
  
### Reference
* https://tools.ietf.org/html/draft-ietf-httpbis-cookie-same-site

  
#### CWE Id : 1275
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cookie Without Secure Flag
##### Low (Medium)
  
  
  
  
#### Description
<p>A cookie has been set without the secure flag, which means that the cookie can be accessed via unencrypted connections.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `_csess`
  
  
  * Evidence: `Set-Cookie: _csess`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `hl`
  
  
  * Evidence: `Set-Cookie: hl`
  
  
  
  
Instances: 4
  
### Solution
<p>Whenever a cookie contains sensitive information or is a session token, then it should always be passed using an encrypted channel. Ensure that the secure flag is set for cookies containing such sensitive information.</p>
  
### Reference
* https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes.html

  
#### CWE Id : 614
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType=1&region&sector%5B%5D=121&sector%5B%5D=138&sector%5B%5D=86&sector%5B%5D=87&sector%5B%5D=88&sector%5B%5D=89&serialSectors&structureType=0&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType=1&region&sector%5B%5D=121&sector%5B%5D=138&sector%5B%5D=86&sector%5B%5D=87&sector%5B%5D=88&sector%5B%5D=89&serialSectors&structureType=0&zip)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/3309/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/3309/show)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/1133/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/1133/show)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&region&sector%5B%5D=9&serialSectors&zip)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2424/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2424/show)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType&region&sector%5B%5D=111&serialSectors&structureType%5B%5D=4&structureType%5B%5D=7&zip](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae?address&addressType&area&city&country&department&lat&lng&postalCode&prestaType&region&sector%5B%5D=111&serialSectors&structureType%5B%5D=4&structureType%5B%5D=7&zip)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/directory/2124/show](https://lemarche.inclusion.beta.gouv.fr/fr/directory/2124/show)
  
  
  * Method: `GET`
  
  
  * Parameter: `https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ`
  
  
  * Evidence: `<script type="text/javascript"
        src="https:////maps.googleapis.com/maps/api/js?libraries=places&language=fr&key=AIzaSyA_WKj-U7bkD3UEadmabO_jEa8V5k1IUjQ">
</script>`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/common.e0c3a60d.js](https://lemarche.inclusion.beta.gouv.fr/assets/common.e0c3a60d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/tarteaucitron/tarteaucitron.js](https://lemarche.inclusion.beta.gouv.fr/assets/tarteaucitron/tarteaucitron.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js](https://lemarche.inclusion.beta.gouv.fr/assets/0.cd5673da.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/assets/itou_common.56582de8.js](https://lemarche.inclusion.beta.gouv.fr/assets/itou_common.56582de8.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `eval`
  
  
  
  
Instances: 4
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/manifest.json](https://lemarche.inclusion.beta.gouv.fr/manifest.json)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=0, must-revalidate, private`
  
  
  
  
Instances: 11
  
### Solution
<p>Whenever possible ensure the cache-control HTTP header is set with no-cache, no-store, must-revalidate.</p>
  
### Reference
* https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html#web-content-caching
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Cache-Control

  
#### CWE Id : 525
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Debug Error Messages
##### Low (Medium)
  
  
  
  
#### Description
<p>The response appeared to contain common error messages returned by platforms such as ASP.NET, and Web-servers such as IIS and Apache. You can configure the list of common debug messages.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25](https://lemarche.inclusion.beta.gouv.fr/fr/repertoire/siae/%25url%25)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/cf5b90138467873a544dd24b3b9e76021487fb4b.jpg](https://lemarche.inclusion.beta.gouv.fr/fr/media/cache/resolve/listing_xsmall/uploads/listings/images/cf5b90138467873a544dd24b3b9e76021487fb4b.jpg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Internal Server Error`
  
  
  
  
Instances: 4
  
### Solution
<p>Disable debugging messages before pushing to production.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Permissions Policy Header Not Set
##### Low (Medium)
  
  
  
  
#### Description
<p>Permissions Policy Header is an added layer of security that helps to restrict from unauthorized access or usage of browser/client features by web resources. This policy ensures the user privacy by limiting or specifying the features of the browsers can be used by the web resources. Permissions Policy provides a set of standard HTTP headers that allow website owners to limit which features of browsers can be used by the page such as camera, microphone, location, full screen etc.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales](https://lemarche.inclusion.beta.gouv.fr/fr/page/mentions-legales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion](https://lemarche.inclusion.beta.gouv.fr/fr/itou/inclusion)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/faq](https://lemarche.inclusion.beta.gouv.fr/fr/page/faq)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous](https://lemarche.inclusion.beta.gouv.fr/fr/page/qui-sommes-nous)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/css/ie.css](https://lemarche.inclusion.beta.gouv.fr/css/ie.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification](https://lemarche.inclusion.beta.gouv.fr/fr/identification)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/inscription](https://lemarche.inclusion.beta.gouv.fr/fr/inscription)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/favorite)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer](https://lemarche.inclusion.beta.gouv.fr/fr/contact/creer)
  
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user_registration_personType_1`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�ǫ�����kjب��^��'O*^�</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Content-Type Header Missing
##### Informational (Medium)
  
  
  
  
#### Description
<p>The Content-Type header was either missing or empty.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xsmall/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_xsmall/uploads/listings/images/ad9b37724d9a82342002cfc9f33a89424a771496.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/16fcfef5b9a1a0282799571f173411296d394e5a.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/16fcfef5b9a1a0282799571f173411296d394e5a.jfif)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/0ca5b2d46926dd9a6c189103ed072a6bab17adb1.jfif](https://lemarche.inclusion.beta.gouv.fr/media/cache/listing_small/uploads/listings/images/0ca5b2d46926dd9a6c189103ed072a6bab17adb1.jfif)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
### Solution
<p>Ensure each page is setting the specific and appropriate content-type value for the content being delivered.</p>
  
### Reference
* http://msdn.microsoft.com/en-us/library/ie/gg622941%28v=vs.85%29.aspx

  
#### CWE Id : 345
  
#### WASC Id : 12
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Sensitive Information in URL
##### Informational (Medium)
  
  
  
  
#### Description
<p>The request appeared to contain sensitive information leaked in the URL. This can violate PCI and most organizational compliance policies. You can configure the list of strings for this check to add or remove values specific to your environment.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-verification-email?username=ZAP](https://lemarche.inclusion.beta.gouv.fr/fr/mot-de-passe-reinitialisation-verification-email?username=ZAP)
  
  
  * Method: `GET`
  
  
  * Parameter: `username`
  
  
  * Evidence: `username`
  
  
  
  
Instances: 1
  
### Solution
<p>Do not pass sensitive information in URIs.</p>
  
### Other information
<p>The URL contains potentially sensitive information. The following string was found via the pattern: user</p><p>username</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `user`
  
  
  
  
Instances: 4
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bUSER\b and was detected 3 times, the first in the element starting with: "<!-- allow a user to go to the main content of the page -->", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script></p><p>var ORDER = 1;</p><p>var SESSION_ID = "";</p><p>var VERSION = 1;</p><p></p><p>//export function track(page, action, meta={}) {</p><p>async function t", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification](https://lemarche.inclusion.beta.gouv.fr/fr/identification-verification)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href=""/><img src="/itou/images/logo-marche-inclusion.svg" alt="Le marché de l'inclusion"></a>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/](https://lemarche.inclusion.beta.gouv.fr/fr/annonce-disponibilitee/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/login-check](https://lemarche.inclusion.beta.gouv.fr/fr/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/](https://lemarche.inclusion.beta.gouv.fr/en/listing-availabilities/*/*/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/login-check](https://lemarche.inclusion.beta.gouv.fr/en/login-check)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript>Javascript must be enabled for the correct page display</noscript>`
  
  
  
  
Instances: 11
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>A noScript tag has been found, which is an indication that the application works differently with JavaScript enabled compared to when it is not.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Non-Storable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are not storable by caching components such as proxy servers. If the response does not contain sensitive, personal or user-specific information, it may benefit from being stored and cached, to improve performance.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr](https://lemarche.inclusion.beta.gouv.fr/fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch](https://lemarche.inclusion.beta.gouv.fr/en/currency/*/switch)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price](https://lemarche.inclusion.beta.gouv.fr/en/booking/*/price)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer](https://lemarche.inclusion.beta.gouv.fr/fr/devise/*/changer)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix](https://lemarche.inclusion.beta.gouv.fr/fr/reservation/*/prix)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/sitemap.xml](https://lemarche.inclusion.beta.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr](https://lemarche.inclusion.beta.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/robots.txt](https://lemarche.inclusion.beta.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `67429909`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `10609811`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `56958432`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `11604213`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `41519605`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `82577407`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `99431466`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `52822311`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `74003295`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31618249`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/](https://lemarche.inclusion.beta.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `31536000`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `73389577`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `58254879`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `72177649`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `84422179`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `64311662`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `562491613`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `81453208`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `75427649`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/](https://lemarche.inclusion.beta.gouv.fr/fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `18534827`
  
  
  
  
Instances: 42
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>67429909, which evaluates to: 1972-02-20 10:31:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### User Controllable HTML Element Attribute (Potential XSS)
##### Informational (Low)
  
  
  
  
#### Description
<p>This check looks at user-supplied input in query string parameters and POST data to identify where certain HTML attribute values might be controlled. This provides hot-spot detection for XSS (cross-site scripting) that will require further review by a security analyst to determine exploitability.</p>
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[start]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `sort_by`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `time_range[nb_minutes]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `date_range[nb_days]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
* URL: [https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22](https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22)
  
  
  * Method: `GET`
  
  
  * Parameter: `characteristics[5]`
  
  
  
  
Instances: 15
  
### Solution
<p>Validate all input and sanitize output it before writing to any HTML attributes.</p>
  
### Other information
<p>User-controlled HTML attribute values were found. Try injecting special characters to see if XSS might be possible. The page at the following URL:</p><p></p><p>https://lemarche.inclusion.beta.gouv.fr/fr/annonce/resultat-recherche?categories%5B%5D=9&characteristics%5B2%5D=3&characteristics%5B5%5D=12&date_range%5Bend%5D&date_range%5Bnb_days%5D=1&date_range%5Bstart%5D=ZAP&location%5Baddress%5D&location%5BaddressType%5D&location%5Barea%5D&location%5Bcity%5D&location%5Bcountry%5D&location%5Bdepartment%5D&location%5Blat%5D&location%5Blng%5D&location%5Broute%5D&location%5BstreetNumber%5D&location%5Bviewport%5D&location%5Bzip%5D&page=1&sort_by=recommended&time_range%5Bend%5D%5Bhour%5D=0&time_range%5Bend%5D%5Bminute%5D=0&time_range%5Bnb_minutes%5D=60&time_range%5Bstart%5D%5Bhour%5D=0&time_range%5Bstart%5D%5Bminute%5D=0&time_range%5Bstart_picker%5D=04%3A13%3A22</p><p></p><p>appears to include user input in: </p><p></p><p>a(n) [option] tag [value] attribute </p><p></p><p>The user input found was:</p><p>characteristics[5]=12</p><p></p><p>The user-controlled value was:</p><p>126</p>
  
### Reference
* http://websecuritytool.codeplex.com/wikipage?title=Checks#user-controlled-html-attribute

  
#### CWE Id : 20
  
#### WASC Id : 20
  
#### Source ID : 3
