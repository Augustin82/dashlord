
# ZAP Scanning Report

Generated on Tue, 14 Sep 2021 14:38:53


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 8 |
| Low | 7 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 11 | 
| Cross-Domain Misconfiguration | Medium | 12 | 
| Directory Browsing - Apache 2 | Medium | 8 | 
| Reverse Tabnabbing | Medium | 3 | 
| Source Code Disclosure - Perl | Medium | 2 | 
| Source Code Disclosure - PHP | Medium | 10 | 
| Sub Resource Integrity Attribute Missing | Medium | 9 | 
| X-Frame-Options Header Not Set | Medium | 11 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 10 | 
| Incomplete or No Cache-control Header Set | Low | 11 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Server Leaks Information via "X-Powered-By" HTTP Response Header Field(s) | Low | 11 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 11 | 
| X-Content-Type-Options Header Missing | Low | 11 | 
| Base64 Disclosure | Informational | 11 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 11 | 
| Non-Storable Content | Informational | 3 | 
| Storable and Cacheable Content | Informational | 8 | 
| Timestamp Disclosure - Unix | Informational | 9 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
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

  
  
  
  
### Cross-Domain Misconfiguration
##### Medium (Medium)
  
  
  
  
#### Description
<p>Web browser data loading may be possible, due to a Cross Origin Resource Sharing (CORS) misconfiguration on the web server</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf](https://adresse.data.gouv.fr/data/docs/guide-bonnes-pratiques-v2.1.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf](https://adresse.data.gouv.fr/data/docs/charte-bal-v1.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that sensitive data is not available in an unauthenticated manner (using IP address white-listing, for instance).</p><p>Configure the "Access-Control-Allow-Origin" HTTP header to a more restrictive set of domains, or remove all CORS headers entirely, to allow the web browser to enforce the Same Origin Policy (SOP) in a more restrictive manner.</p>
  
### Other information
<p>The CORS misconfiguration on the web server permits cross-domain read requests from arbitrary third party domains, using unauthenticated APIs on this domain. Web browser implementations do not permit arbitrary third parties to read the response from authenticated APIs, however. This reduces the risk somewhat. This misconfiguration could be used by an attacker to access data that is available in an unauthenticated manner, but which uses some other form of security, such as IP address white-listing.</p>
  
### Reference
* http://www.hpenterprisesecurity.com/vulncat/en/vulncat/vb/html5_overly_permissive_cors_policy.html

  
#### CWE Id : 264
  
#### WASC Id : 14
  
#### Source ID : 3

  
  
  
  
### Directory Browsing - Apache 2
##### Medium (Medium)
  
  
  
  
#### Description
<p>It is possible to view a listing of the directory contents. Directory listings may reveal hidden scripts, include files , backup source files, etc., which be accessed to reveal sensitive information. - Apache 2</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/](https://adresse.data.gouv.fr/data/ban/adresses/latest/addok/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/addok/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/housenumber-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/housenumber-id-ign/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/](https://adresse.data.gouv.fr/data/ban/adresses/latest/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/adresses/latest/csv/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/ban/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/ban/</title>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/group-id-ign/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<title>Index of /data/ban/export-api-gestion/latest/group-id-ign/</title>`
  
  
  
  
Instances: 8
  
### Solution
<p>Configure the web server to disable directory browsing. </p>
  
### Other information
<p><title>Index of /data/ban/adresses/latest/addok/</title></p>
  
### Reference
* https://cwe.mitre.org/data/definitions/548.html

  
#### CWE Id : 548
  
#### WASC Id : 16
  
#### Source ID : 3

  
  
  
  
### Reverse Tabnabbing
##### Medium (Medium)
  
  
  
  
#### Description
<p>At least one link on this page is vulnerable to Reverse tabnabbing as it uses a target attribute without using both of the "noopener" and "noreferrer" keywords in the "rel" attribute, which allows the target page to take control of this page.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/azay-sur-cher-des-adresses-d%C3%A9taill%C3%A9es-hameau-par-hameau-et-rue-par-rue-6ba16cd18738" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
Instances: 3
  
### Solution
<p>Do not use a target attribute, or if you have to then also add the attribute: rel="noopener noreferrer".</p>
  
### Reference
* https://owasp.org/www-community/attacks/Reverse_Tabnabbing
* https://dev.to/ben/the-targetblank-vulnerability-by-example
* https://mathiasbynens.github.io/rel-noopener/
* https://medium.com/@jitbit/target-blank-the-most-underestimated-vulnerability-ever-96e328301f4c

  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - Perl
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Perl</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf](https://adresse.data.gouv.fr/data/docs/guide-mes-adresses-v4.0.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#ni4M`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#Ewh7`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#ni4M</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun
Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T
T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=M¹ø×Ïï\x001f>4uXLJÑ\Ð·xCÅ¤`Õ\ñÛ)\x001bÿúêöâür\x0016î/\x0000´û¯øã¶ÔÑSúr^Q\x000b0Â3\x001f\x0002üHÝBcu¯\x000cV`õ"°^;JÜ	;´\x0015ÕéÌ[ÌEy½XMÕ,Â\x001aà¢&¨\x0016Id$åJ¨·ßk?\x0017\x0012tbõ%Xv\x000bç&\x0012ØÀüªÎ0/³ösÑ}/X[µËÀêÀ»7àúR\x0005	{\x0011\x0008l<ÄëÐ\x0003ÖW`ýB°\x0010¹ÒÉZN5ë\Xö¼\x0002ëÞ\x0006\x000c4V@ã²·e\x0014;¶Æaoº¯úe<&VÆæ4À´èêB\x001a#\x0005bÒâpÊ¶ó¦\x001e©*j\x0019L\x001cÈM0UÎèZæXÆüÞ*·TUºJ-SVN:ö\x0010uø#å\x0000Lé#åù:¹.;\x000f![«ûÍûÿþÿ<ûîýC3ßç"øÌH\x00122å£?h\x0003Î6\x0017³//Î\x000fÎ¼Ê¨xÂ«\x0017ãwEeZ\x001d\x0015\x001e1\x001c\ºØ÷ð5Ê\x000bd.Duuq\x000f~Ë§i\x001a ¡kt	ÌMÞáÔç¬dVP5\x001b6^çry3¡NÿíqÐ±\x0002\x001dç u2\ÛXz¢\x0011º¸\x00036¹Kp\x0003\x0017+ÖB\x001eÔ¹ô\x0000eë±½8\x001fÓØLåëc¥áäã¤§G7wó÷ÿ¹¹¾øÐæ\x001b¨ÒNÌÐ, 	{\x000fÎÌ²\x0010§»9Ý\_\x001e\x0002m§ë\x0012T\x0006
A\x000b6öñËÿàôï><~ØÜ?mÞßÚ|ùññ¾uv4¤*:\J2îiÅ~Ñ\x0019Õ÷Å\x0015.\x0000ã?½¼ºÜÝÀíy»ùòúêl~öåV&KI¸%.ÐF*x8û\x001bPÖÓzÇç\x001f;©O\x0005I
\éÞä\8ø\x0002sôÉg\x001bÔ×Ón«Û76;È]\x0002\x0000é\x001eÌWÿ¯\x001fï>>Ýÿpÿáéîýæòÿüo)¼h{±`\x001f-yÈZQ«¶5Ê³Óéæ\x0000rÓÝÓë³×g7§\x0017ËÍôOþæîÛ»OOðîøíÐÞ\x0011DM+\x0018·\x001bÖ7_ölZ·áÄÑvZm1ÙªÊìÙ\x00059W°ÝnZß|I\x001b×V%hµ\x001c4ØöHÕ8íM\x0014Owêú(f|	h]ÖËAc¤0\x001b9\x0000+\x001d´ãYÙírÌ`ÈIV-Óí\x0008`	znn	h_öËAGKß&Ð.7sx©(d
fÅ\x001b\x001dKÌq1æ©¿nG@ÕM¥s^*\x001aÜ\ap\x0001èr>­\x0007\:0c\x001d2ÇòðvË=××½\x0004u­ñ«¼¨2*\x0013ÄñH\x0005õ\x001c\x000bÒ\x0012ÔöËÕGÔu\x001eÎ¡+êåô.;às3
KPWOQ.Ñ\x0016ã¢
×¶OQÈíÇzÆ´/\x0001]½E9ð\x0018Á\x001d±tÔÖ\x0010'¶¤éF\x001fÕ
DU·Z
ÜjÏ	|9¹áÜ(ä3÷øÜ0Þ\x0012ÔÕ­V\x0003·ÚG\x001c\x0007q´w[2Ó.W££Ó3N÷\x0012ÔUTËÍ"6eÑ®=å\x0005s#\x0005çV¼ÙÔx\x0017j½ëéézÙöæýÝ\x0014cÞ}×\x0016âÀ»lú\x0013´`¿	9p¹ýd®$µ\x000fH
ãÌÓ//\x001b «\x0012º\x001aîuä]£\x00101\x0015ÄFä?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ßeoH»6¸@Z9*\x0011\x0003¢/\x0018,¨,ãm¶÷ë\x0004$Þ/>,`ßå\x0017ëª8"\x0011\x0003s\x0008²d\x0004cÞ@22¢\x000b[{dµ ê.â¸D\x000c*J\x0005\x0015úÀ\x0006ÎÄð±­Yu\x001b¢é"ÉÄ(M©pâ\x0012Å\x001báq&\x001a\x0014}§½¶82\x0015ÃR*ã9UÝT½Á±½®8"ø\x001dK\x0002·Ä²hZÅÀy6É¾8&\x0015\x0007¥¨\x0010$u\x0000ÁT\x000cÇ©\x0018Óotè"IÅ0Î-\x001dçaðä]ë¶÷ómà½»2*\x000f£¤³¢Ï¹_ ¢EÎÃû\x0012\x0008ö2öNâ¨<2±\x000f´C®Êµ+vêQ½}\x001eá)\x0011Ã³¨8:eÖ\x0006m`ìN\x0001£\x00131\x000c%bXì¼±­Õ{\x001bcÿ\x0005\x001c53\x0015âzRv­nï¤ÖøFw½Àù\x001e!Ð\x000fjS\x0006Ñ:aénûm=z 9ë´G©ÞÛ?\x0017¿?ºJÎÉröÛÕõõâ\x0013ª``$\x0016´/á\x000b\x001c¶«Ô)!D\x0006éÁ²\x0002áÉd\x001aÜ	f\x001f\Tß\x0008\x0008ÿ:z\x0006z×oÇ''óCúV\x000f\x0001þ9Sàò¦!\x0002|'Ð$\x0004ccFx
¶ ½\x001aFmÿÃ«\x0000è®
\x0001D¦U\x0008\x0002Ýe	!
dJ«`Ó\x0010à1«\x0000o£¯B°¹#-"Ø7<!(	Aû­«P\x0000"1T! \x0013$&
¢É\x0008\x0001LBHU\x0008c\x0008à\x001duGÁ¤¼~\\x0004Ì\x0006ç£à\x001cï\x001c¹\x000fØq\x001dj\x0018":ÒQP9÷\x0001½\x0008\x0019!$@©P'\x0016l®ÌF\x0004ØÀ'!§\x0011AÅÃ\x001a±ÆL¦£ k6!hÇbÁûb\x0001m\x000cü©`ð©*=\x001fGy\x00103\x0005qN§1åyA\x0000±$«DSÉM\x0010òÄwdP(X\x0012\x0012n,\x0003,¬M>ç~ãi\x0016\x001bZf	\x001d5Ç±×\x0012«\x0017dpú·hÔ×dtòÑ¥¾þÀ
qàd °\x0019¬Ù*\x001b*\x0018àFË*ùYÓ2	¤¢WB 4b'P#TuÒ	\x0004³Ë\x0008Ø3,dÙ\x0000:¿+\x000cã\x0016\x0001kUx\x001e]0\x0019!¢g?!\x0004S\x0008¶JÈ
\x0004Ø?U%<Ø¨²'­Åãø qpÖZÜÈ;Å(ªJ<ys°\x0012CêÕ\x0019la\x0010c\x0019à.©*íÍã¤ì¼\x00158vî¥Pe¤4#_+ÔúT|òp\x0019\x0003­ÓX²\x0019\x0014¯\x0003Nß\x001bÇ\x0000ë§ªä\x0013\x001eHë`\x0002éop8Ãê<Ø\x000cp£U|\x0002\x001d2\x0018Z\x0007ÞÄ\x0010XoÈ=\x0011Ç À\x0016ª:ñÓth+¼Äbº¼\x000cX\x0019Æê\x001a®\x0012P^ÛîÕÄ¨Z\x0006Í\x000cÊ\x0014hé*	å±
+#èÙv`Øk\x0011Ç2xÒu"Jª\x0003:
JÑÍtÑ\x0016é ôÈ\x0013Á\x0003]'¡¬KÍÍtHi·éfÈG2;ÙÆ0À1Òu\x0012
@IÅ¦´\x0015)'>3µ/qýt\x0016jER;b°¬A¥!<ã\x0018]×II\x000bª£GSbm\x0012í\x0005=ÞÝ
\x0010ºJHb\x0016¡¤e°©¬#-f%Nj1v+à6é:!)Ì\)P$\x001cÌJy\x0019©N£Ê¡«d$¶Kà§B¤¾:y\x0015L`±òÉ|4u2\x0012e\x0003í\x000f$»\x001bD#mTM|rØÂ7ÇG1!XÁµl°ñ©O\x000e\x0013q\x0015Ý	uÌA¹r)F" ÷«J<aÊj`\x0004¶^Ú	ix'Æ>\x0018§2UÒ	ÿê\x0010p £\x0003©Éë\x0002ïÞH»\x0006®Õ3S'DHyðé4X²*à@J¶1ó1ë\x0000¢ÉÔépB¦&\x0018Ä@;a\x0014KH7öÍ#ýÌTI'\x0017B11À\x0014ÄÆ\x00041|³-\x0005[)\x001aBuL\x0008T8Ìb\x0002£ù¶N}BòTyË\x0008| ýh\x00048D¶N:¡&K\x0007RäÓ\x0018¼Ê\x0000
û\x0004\x0000¹dët'ÕAïu\x000e\x0012äã\x0018y\x001f´\x001déñÀÎVëN$J67m\x0004ßJ¹]@V0 o¾N:Ù#\x0008@ã\x0015hv	\x0011F
H<C¶J8áú[ò7ÀÃ\x00194\x001dÀË ¶;\x001c*\x0018<f\x0019W1î\x001aè¹\x0014\x001ek\x0008\x0012\x0013d\x0018{'@2Ù:ÝÉªâú1D/¾H¡ÕØ[\x0001Ëgë\x000cÌÜ<&!`ú3!¬'åG¾\x0013\x0018_qu\x0015ö´$!-Ó\x0008®lÜ\x0019ËÇa»Ïcÿ­Àñ;®îf
òmÓÍ­`áÀZ\x001cëÄ\x0007ÆÕ\x00195J\x0014wvä~\x0002áP\x0002wr¬Æù®RmH£Ò2xÅO¶-\x000f
c\x0001N²«Ó\x001at®þOv6FoÉÝ\x00108f5Ö´sp']Ý½Ä\x00067lê\x0007\x0014Uù@:6³E\x0018©¹`¯\x000fWíù\x0011´\x000c")1Ùó£x+r_Ä\x0011\x000c\x001eÔ\x0016_§º\x0018&oe×4\x0001ðq\x0014A\x0005\x0000Å×é-V²úET\x0014´J\x000e4Úíov\x0005\x0003c_'0=öÁb45#\x0014E:v>æ øJÇ´*Þ/µ
(\x000e\x0011HáG¾h\x000cù:\x0001iãÊ9\x001eÉ¨ñyNbv¹^\x00078F¾.¯\x0000{0\x0012§\x0010â\x0014b\x0015®\x0019)PíòuÁ;\x0018|$ûÒ\x000bÀêüÖkQÁ\x0005uÁ;Pe\x0005éó\x001eÓ3BÑ\x001bÙ**\x0010àóu\x0005Øk<\x0014¿Oà­\x0008E:}³\x0003¦P'°Ý},ö%Çkl±¬üv\x0011YÁ\x0000G9ÔI(lKÄÇÁ\x0014/ \x0016,¦Çz\x0001ñ¡
u\x0002ÊY\x000ei#¤­P² \x001f<:	¥
§Û-Aj$Æ\x0008x'ÆúÆÑ\x0018	uyOÿ¶6æÖ:\x0001åBêG"û©|5Gö\x000b\x001d{\x001a@6ÊäÜ'«\x0017¦ðÒÊ¢»Ø
=&%:ù\x0004\x000cwô'`\x0010ï2:xzW¨\x0013PÖ±Ú´¦d\x0013\x001c\x0012FÚôXÃ\x0006KrCeò+ëc)çF¢Ñëq\x001a½Dç]ú¨q­¤¤LýÓ³\x000bL\x0014cÛÓ¡$Þ§ôQó\\x0004òM}\x001cA´qÜy)ñ§.ó\x00075y\x0013X$ÞbT3µeJû©ËûÁP	«qp\x001c¤çX	«qR3+dÊû©Kü\x0001kîÀ\x0015A­-BÔã®Äl\x0017Yò-\x000f3A2ü\x0013è¼Úã+ÌÚy&k3^VA\x0008rÄúbmQ_ÆeÝH2òê\x001en/±\x001dãJ­÷üpþ\x001fù.²2éÅxl\x000f¥Æ2§læùÉ2
\x0013^deÖYEL¼E¿\ÐÅM?2Õ\x0002Ígé£&YÖpÈ\x0004_NÊÑLµë\x001eN\x001c}÷LÖå{\x0004)Ò`\x0010².XPúbt»í±Ìýç\x0012wQÖE¶Q·÷ªD\x0012\x001dåÿXv#Ó«%µeel\x001b4zOO\x0006Î¯&oÒEb\x0015\x0013ØH+}Td"é\x0003ejr\x0012\x0003\x000e\x001b½jô³îDY\x0017×õ>µeÉbÂÓå@\x0013£È*9\x0016\x0002/G]L\x0013ÓMè`&{\x001c¤Ø-\x0012F^\x000e\@Y\x0019OÄ,z»nöÊâtÛeö~\x0006ÔÊee$
G©GJZÉËÀ÷3·©\x001fÃÒ².\x0003z='CùÕÕ(ÊÚî¨HyÔuÔBr\x001d;²:S
7]\x0001f,&ë8IM6_@k]Ê©\x000ccß
\x0014³².c»y;\x0004\x0017YBcÐ¼\x0018Âuq@Ã®Rj½Ã\´\x0012®xJÃ8\x0015ÛÁnQç\x0011ßqô\x001dóÉ4«¬Í±ÉõáÝeJ+¿¬ré£ÈUéüJPl5ÃkrÛß-\x0012Æ¢Ê=\x00159'\x0008ÓÛÙEæ8Vu\x0014Z\x0014pÎª(þ}!g0T\x0015\x0006N*.\x0018Ør´\x0018"Ü\x0011%\x0011\x0002þ\x001a íÊK%)¦\x0002,ÚÕÖ:DññöÎÝß$s\x001c«Ô
k1ûeq÷éq\x0008Á
#é
\x0003}SR\x0006g°l\x0003Z@èùìùÙË·U\x0008(5ñc?T c9Èì\x0008VP"\x0004¶}ã\x0010PfâÇ~\x0004xEC&ð\x0012ËÙ\x0013¦3	Ô¯5\x0010 ½>ö\x0013à](\x0004¶Ag\x0006\x0008º\x0007²\x0000×@Õ­\x0001gGåE´\x0008fâ\x001a\x0008D%ÆËÿäYpIR\x0002Åâÿ;þúÅ¸oº]nª½¥¾ÃV¨d§\x0000êÙ\x001cWâ¡£`r7íù,õk¬Éå³µ0¶Ä1ÁUPM(¾ä¢YËò=þ%\x0017\x001fÖ\x0017æqv¸¼û´¼\x001eÔô0/\x001euïIõ÷JD\x000eÈ[³òvvxtöòh¨Ãx\x000f\x0004+jAtdO¦ÇÙ$ùAÅÆ"\x0004â:Í _\x000bâV\x001a_\x000cX\x001c@lq\x0015ø5Ô\x000c\x000b½ë@À<×TP)J%¡Âª5ÒúÄ­é×= \x0006\x000f'ær¡qÎDO¥Ðx\x0002H.ú®\x0003Á1\x000c@<¹³¼6\x001c\x0003Û]\x0007É¥ßu Fq\x0019>n
Å\x001f´õ¥ôZN8#¹\x0000¼\x000eD\x0007Þ\x001a\x001fLÙ\x001a[,\x00037eEr\x001dx\x001d\x000c\x0007äøÅRð,Ð´
¥\x0012\¿½\\x000c^wk°o	]_§²
ê¸Úte4sPIxåí\x0015%»Årñ©
ïã7\x000bÃë@¼-Î\x001d\x001bø­QEi?ag¨:¼ò\x0018
N`¥>yåµÒ\x001c»tbÂ ¥R°bk\x0013\x001e\x0006Ì¾¢3¢8> »u-Í$T)^ùú2#£\x0011IÄËÕi
­kòås¼ùxõF9§_\x0017_ÇÔjåíýýíÍìzy?;\äÖ[u6á´Ä¥¢RhÛ¡ÎæQÎ#±sh~¿:¿½½=??}=;9:\x001dÎûGv\x00111\x001c>Æ \x001aòÞªh\x000c5,c£:Ñ¶)éë1ØË+÷dPèLÙ
ñFçg²91\x001dQÈ¬£<f\x0019=¹ÒNg%\x0003úÀNwN`3å\x000fùýñÓzÂðÛ]\x0001+ò$`_pNwá¬i\x0015½êe\x001e½9}}1èa*ß.SË\x0000ê\x0019°ëë1÷*äç\x0014¬öUþæ¼qc7¿¾æ/[äÈ²ûïo¨õ\x0002«A)^ÇßçÉÕ}ÿ½~ôþqS\x000f~½¸}\x001c:\x0010ÚºXjÔ%½`0q	þï×%Òóùéà¤¦\x001eGOûÝÃ\x0011UéÝi¥\x000c~±jÐI\x000emæèé»9°ÎÉb\x0008.t+
kãýÜ\x0003òùGxïoÖ\x0017$Y¯n¯¯n®wa\x001c0¡9[4zHSì5\x0011·±¯NO_\x001f\x001fÍ+ zêV\x001d\x0015F¸IÅÐ¾ØÖS7¥tq\x0014W¢Y×E\x0013ÓáãÝâú*7L\x001d\x000cæp\x0011û¥R0õ/\x0019¶­ÓáÛ³ùÉñpÔ.RO\x001d¬d\x0002«ERâí"W¼¥NMïHª®JVKµ:P\ãëÊÞhG!=ðé/½æß<Ü^Ý,ggËÅ°\x00146\x0001íÿRvL\x0019fªdÇ5ÄüõÅéñë£ÙÙüp°ér\x000fheêU\x0001Å¢È¦\x001d«4/½æ7ªùãÇ/ß?¯\x000bç^\x001bàáì;
©4%ZõÚ\x000bÉè¶m×®Æ¿êÝåÝ§\x000fòa\x001b\x000bÛ'¿¿½ÞÝäkÔ-7\x0000\x0013Ö.hzó<Ï\x000e6°ïÂ¬\x001få½4Á®2é5i\ðzØUväæ¯§¡6TÕ4>pG	ì\x0003E.>Í
âD·*²\x0019;\x0010Õ/;P¥ÝR2Ò*uU5/Ì×?¾ùß·\x001eàãåÝòaø\x0005\x000bo7¦«qb·)ÙÄÑl9ÀðL\x001c]\x000c?\x0014\x001dõ'u\x001fOÍ¿Æ1÷\x0005g+¶\x001e§£jTà`\x0010K®\x0012c¸_Ôª§Û^Ò=82þ)®ïÜï2ïýbñx\x0007\x0016Ã ÊóÊW'×(µ³4Zìàaï\x0017ó·g`'\x000câø«Ç?äÇu¿,âOðTíÈ¹\x0015\g¾Yn®&Eés·í\x001c¿jø ÿxøêþ\vÞ©»«!\x0000£Ñ@È\x0000ØpD\x000cµÙÿm§îâì¸êKóíÙù¥RP7Æ\_
ß©ù[µlüÒUHs÷ßµ$ÃËY\x0007:$Á×v²Õv~ïÃç(?]m\x001a"»\x000c¡2)Ý;m¡\x000eBÏ\x0006ùÏ ô\x001c¼»\x0010¢Ó©\x0007< Èé´^9JèUQ(×\x0004ñþëãuüº\x0019$:_Üáa»\x0014ë,´W7l,
qÌ9v>?Ãé\x0008U0=Oó>\x0018ìûPRkW-8/OÛØ½0!e¸Üú¥Å¯ß\x0006ïP¶X&² ÔÚokÖ³Ûg©[ñë£·¿íHX­?m5`F¦RNáü\x001c (édfËÓ_\x0007&­x¸Úxs\x001fg°}W¹±ó×k\x0016\x001c%&çæûÅép¤6\x001dÓ°ÇØÖùÕ®CþWücù×{\x0004C[\x00183lhbî.0xh\x000f(_\x0001~9+¡\x001c_5_\x0007:îþb+È\x001a¢² d¥,øÒï+ÄÎ1®üb)ñ.ö|3ñÔÏ?ý\x0003Öúå¿3\x0017å\x001bÓ©FßýÕËÏþÎlJW·×WC\x0000Ú9ÃÇ2Õ­p?#\x0016'b3LóêôíÉq\x0015GïÙÇ\x0011Jy@×\x001b+Dî\x0013±î¸háè\x0005÷pàä<®ã\x0011äÍõ(È©Ûf\x0013zÔ~¤©(]ÓÇ\x0005È«Û!uÏ¤êüµ\x0003Rrè\x001b
Í|,\x000c¼\x0002+aq\x0001"âõñé°wýûryÝÝî\ÍW«aÕ#59Êåo¦m«n.ðjw¢æ«ùñ.EÄ<\x0008õé®#±öEÎL	ÀÃûç)7ÂëUÚåJ\x0003¢°Ìö¦øÝ¯f÷Ú¾ïvØªlä¨\x001dWU9\x0011G|7YÔû2 $W cèªâUiÝ\x000bÙ¿w¿sÜÿ÷©]Kñ¶p\x000bg6áuGÏ¨ÿj8-ø³ç«±¨ÐP=çÂF´ÉIÏ ö»%¶áL\x001fûr,âÁÊ­C\x0014ØevWv\x0003nõß\x0012\x0019?öªóØÎtÖ<uîV±ØÎùnÈê}wÌàx\x000c¶0ÁÈ &öº\x001c5×©ªÿnÌÓÃ}\x001bnJQ1NO£³V:Çëö£&±·QúØwÅ\x00147\x001aÀféÔGÙXrÛ;\x000fpõc;Ãô±/i¤d¯`\x000b`] Mé,itûýÆÙÉÏÒÇ¾à»(\x0001È\x001d`ÐrçîF\x0008UiRü¿DÇáE\x0014Ür®$eF³¦µ]ÿÝhLãÇ¾Ä\x0014ÏV\x000bh]hÖåÌ\x0014U<·fÄQGOxúØ{A\x0003\x0002<ß1eT\x0011ª#¾\x0019\x001bä¥=m,&×#¼+ÖÜrñn¿éú/ÇÄ\x0001»_¤K[«Ã¦VkîÂÃJPúØÜáJÛP¬\x0016ÜÁ'Ýê;þ1\x001fò\x000f|Ë:
dw\x0007.](ý}° ,vU\x0004Lç1Ã\x00199d¹÷ûeR_h4ÇÈ)úàIÆ4$=G\x0002«0ý¶õ\x0004¸ü4bO\x000cÙúÒfIIî3î[\x0019[\x0004ôºHê·¾g\x0017pÊ\x0012\x001d+ÙW\x0011TY\x0004Õ\x0000°\x0007áë^^~J\x0005\x001a¥\x000bÜ="<Þ/\x0007\x0019@çªpìö\x0005\x0014Å]¢z½cÏáíùQ\x0005Ì!PYGa"kvNkÌãÌQ=]Ñõ\x001aÛ´``ÿ\x0011KïÅ¹rJ±\x0010ñÒ­â\x000cT2Ù@qõ»þ!¿tsÐNöð"Ü\x000bj¶-E\`\x0003Z¥+\x0004ÝíýþÔ_ }ì\x0001\x0000]Ópç;AÊ¦à3©bw|R=\x0000ª,écß
\x0018¹\x00069
Ï¡\x0013\x00198×[©q³\x0017àæÃû+ÿwZ\x0001|\x0015ÒÄÅìåÝâf°XÈ8cY\x0005cG×2HÁ
"]wHË|öòlþúå\x000e5ÒÄaÔ]bÚoË»\x001b\x000bÃe\x0011 qæÀ\x0012èÝN
~Ó­bÿvtö\x001aÄÂ0AXÜ>èû$\x0017¨Qç|¯ËA¼P'\x001dåG\x0004[\x001a\x000bÎ)\x0017oÃ~\x0000tãÏ~\x0000ãy~\x0005\x0013×§É$*úN4g?ÁÇë«\x000f¦ë|\x0003á|ñx÷cÐýf9¿^a®YnT\x001ap\x000c\x0005ùßïæ·gÿ\x001cüv¼ÿäXXý\x0001;Eÿñóð\x001e\x0016W×Ã1Ú¨%'¬\x0004,\x001f"eEqÊ°\x0012ºïcÿÇÛw1?\x001e\x0008ßA\x000b]´Ð\x0006+Á¡\x0010\x000fj¬¦ÖGV²6á×ÜShÂä¡âU;Ä®©	äëÅÍ\x0012f/×³³åûÁ$¹EãM*öâ\x0014Z¸é±ç+z}D³\x0017G'³³£çûÉlÌ¶G­h­Kª
Ô~\x0015ì-?\x000c\x000bE×Vmñ_6éÈñÎhÒ%\x0017üóÏ/_St\x0007ÂPüÛÄ¨È\x0007¥"c±\x000fÆÆöü×ù«7)¸\x0003a>x5	½â\x001d¦ä$¯\x0012ä\x001fGÚc(Øò^¾É¤L¤¸:øð\x0018`æÃz
ï ôÒÜÛ\x0017VJÐL%Ð'84\x000f+µ^ýÄÝýT¶Ge\x001b¨\x000cOÕ\x0001*Uu2~(ãy?ë!¹\x0006$0\x0002r½s\x0017
G5\x0012Uw0]\x001b\x0015kêP¥éMµXJ\x0010\x000cf\x0013ç<N«;\x001aH5\x0014Ý/r!æ8?\x0008\x0002t¼?ã¾øt3tÒ-F\x000bs~"N§0o°FçC\x0005ÛÛÍº=zn÷çpàç/_ï:ëåûX¾\x001e\x000b½ï:ca\x0011'©`¸¤¸WÖ\x0015úX¡\x001eKqªt©¸ÒYr±ê\x0018ø­Xª¿Zªaµ\x0014K\x0006À²\x0018c¥òg¦êFÇ[©ú¥\x001a\x0016\x000b,
] H\YMñ±T!P¥\x000bSk^jË\x001f´"K$?(WMu.«µ^ô°J«\x001e\x0015¹T\x0017ehí\x0011ä@E\x0019j[Pã©tJWSI,ÈÈ\x0012\x000bSå\x0002\x0015´($:zµaÉw>.\x001f¾¦Â)\x0006ßøeyóéöñû3\x001c8Ad÷FbD$µøW\x0012=Jy\x000c8Æn$:9\x0016¸;Ì«£×/Oßþw÷ÛÕ.
OP«¥Á\x0001¬D]IT¢1Ø«7Ó¹YãhhZ%\x0000\x0005³Q\x0006ìëè\x0013ö\x0004\x0003kd¦ÀÐPµZ\x0018|\x0008Lxº\x0013L\x001a­¦7cìãhh¾ZíFÁ}òy£Rl3ä28Qçpv

M9«Þ¨Ü42mTJMk\x0013ð½Í;\x0015'­
Í;«¦\x0001Û\x0010M
\x0011åc\x0013c97hÈs]K\x0013\Ê}K4\x0002áFk¦qa


A«¦1\x0007\x0004~L¾Q¢l\x0004CóÐªaä\x0001\x001a\x001c\x00193så~)0<\x0018­ú~ç\x000eÆc}q¦Á:ÇL£'ÑÐDªj<5/Ñ8,×Ê4Ø" Ó¨)gSUÓè\x0014\x0002J4¶ìuåF©	0æ3UÃ¬^\x0005PW%m]m\x0014¤£¡aMÕ42\x000bß OCC³j\x0005Æ¦W!ò\x001be°èQçÆwS\x000e
jjWÆ\x0007\x0013§öxz\x00144öKÕ¹aèSÃ¸Õ\x000f¦N]Ïf\x0013V\x000f¦E³ñShhO%
êëÊ2\x0006\%­/?%eBªIkC\x0013\jiMnQ¤ðD\x0011"Y#¢gñ$j8¦Z,ÁÎ\x0015bÞ¨N:\x0006Ô.
<ÙoÃTÂDãyi´44Ù¤vipD|Þ\x0005äJg82L4S\x000e
ffùÇ[c]OÖk\x0002Î¥Ê/\x0014&7¦ë\x001d'-
OØ¨]\x001a\x0005"³Xh¢a}XI:_jN ±7Aµ\x0012*Ó<\x0001ulÈVôÔºL»\x0006 \x0010Ó\x001c72¦4=TÞgÓ·ë7\x000fß¸?S$¦\x000c?½Z>Î^\=Ì\x000e`ý±IEÒ\x0019\x0012ÉL
§Ìd&#ÖòÉñÑÛÙãÙá\x0011\x0018åoþYAV¦`6a¦\x0007§<\x001b\x0013Éø!\x0015Ö>\x0001\x0017Olâr51\x001b\x0004?ªJ\x000b¾uj]/\x001cCÆ³"[È0×o ´hò \x0019¦©ð=\x0001I]EMê*Ú¶li´\x0003®\x001aÜKÒía©x?µOÁvØ.[ÙDJ\x0012O[\x0011¬Ä&\x001c-5ílËÏ?â]§^òåûÏ)¥dpi\ºS
ã\x0002Åx.N\x0017#ÍÚRýrôü×nbÉ0D®!­\x0000#rS¯°?=t4!¼\x0008[!ö¯\x0004¶ýPuK!iäc¢HZ~Ö¦Ù\x0019fÜº\x0014¨§uPukjtò­(Ó©piC\x0014« ¦LNj§EÄ\x001a
ø®d\x001d+Ì(ö¨d/	ëês5\x00055\x0014Ø\x0010(d\x0012Yçà£\x0019Æ
\x001edUs*|*òJ\x000c!\x000fÏ.ÒÈ\x0014~Ý\x000fXIÑíb]Á¡09¤À¼¤bBaÆë6yÃ\x0015Ií-\x0008Ùª»]îó%ñ\x0018ÞÊv\x0015N?B$J\x0008át
¦a±\x0001YZÁóÑ°¦ãñûç??´\x001ap»ðç<¥#ìÆp¬	Caù$`\x0014_\x001d8¡ç)\x001f¡\x0013¢j8l4©3\x001c	qýF­Kz
¥ÓÙÐ°-5 ©á}áÈîF\x0015L¢F¯\x0007\&Ëº­Q&M8§­	6ob¹Ñ4¢ûð©«û¾ZÜ|¸»}Ä\x0016C»iÒÜ\x0014ÍJ.jÎÒåuAÈµuy5ý\x0002~mªxìz=\x0012öiÈ*Æ,I¬I/È?â<NÑÙ¹øÓ$Rvcb
f)
Z&\x001f¦"ÑÜã\x0016$É~YÐ°<#I&
n\x001a\x0012\x000f¾mCòÙ÷\x0018f$ÅLÎOCâAmH¤ÒÂû°B*Éù8Éü¹|º
qÓª¢icØ÷|	l;É\x0014X¹Ù»¤pL4\x0001º^\x0016\x0003Qê!m\x001bÀçG@XÅG­Mùbdm\x000fù|Ì|Æ\x0017<ó$xT@Ù'g)j±Êxn$ð­ûtGòq\x000ez+\x000e©\x001e;ñ¥äüÄWÜ@Q!Ã½(5ó\x0006m*i{EæSERÛ'á£î­Í|A¤f\x0006Èç\x0003f\x0005%>ã\x000có'9¬Ì´¯Ï\x001eP\?m]òú±òýT÷£Lo½¾>g£¦õ\x0016Î_ÑÊ£X\x000fáëÍ»i]A#²c\x000b	M\x00110®Q¬?\x0017-_ÌßîbÇãÐÁÃ6\x001fR7á\x0003¨RÉv²&\x0004%\x0012ÈÔ\x0008%kiF\x000e¯\x001fvûxy4ÔGµ\x000f÷îòê\x001e\x0001ñ¿\x0019\x0003Î¼Ë\x0006y\x001a5\x0018\x0003\x0007CW6v0\x000e- \x0017÷Ýwû¸¤\x0011\x000c7·;7Õêb\x000bbÌ×Öa\x000e\x0008"\x0005´ß×Ò\x0018×§ ¿ß/ôço(üyy·øtsûp»Gã·\x001fXã·­\x0005{ÚkÇëåÙüåëÓÓáCÕEIÖ\x00076 ­£ñÔ!Ñ\x0018,\x0011J\x0006ä8ÑªFÞ¨/\x0006Ódñ§\x001fï?§¶\x0014Ã[STÖüqp_á¨`Ù`ÖrÐMúrþÏç¿\x000e6ªï¬V_\x0017uZÜ>\Ýß/áû\x001ffoî\x0016\x000f©èÃ\x001e¯B\x001e_¼
\x0001×.»\x0015,=\x0000Võ\x0007êôâøüü\x0008~{1{s6¿HEF/j s_\x001c27ØøÉ!IÖþÜÙûû3Bêo÷ßd7òqxûx÷aùJÿï26\x001d$v£<ÈWY¥©´IêFµÆuxúöìÅÑÅ`\x000bÓ.
fáO\x001dq\x000eK\x0002\x0012,Vl¤\x0018>Î\x00123­,\x001få7guHâ [òînñþóâz\x0010Ò\x0004³¤bXZ\x0016\x00198Ó"uOÂ/Gggóç¿Î¦\x0001Èw¿|¾TYèÈ0]ËåùíãÇÝ/¶
*
Y\x0001\x001b¼w\x0018µÎ¡©u\x001e§6|¥Eæ>?}ûËçzÅ\x0003ê¼kãJóÝ²å.-[î*\x0004ÊqnÐ\x0018¨ÄÚª(Vy;Ó\x0001ÀàÄ\x0015%{9¬\x001d²÷p¹¿?)ª+¹{Ð«Û\x0007øæ}2\x0000sÉ³\x0003Tl´QòR9§²\x000cÀêë\x001e³Ó×\x0017ðËtñ²¶§»NÕDØY*K¥t¨ò"9My*@´þ×\x0010ýþñ¯?¯S	.æràÏ\x001bì!¸ÛÛ\x0018ÙÛ'âT±ä»Â?³¶6o°`
\x0003\x001chüÙÏ\x0000\x0016b´DÔh#CÐ\x001c\x0017 êq\x000cìÉÜÏÆ?%ºªæ¨!åÇ8TüF2à\x0003k«ö\x0002¾IÓ^TKö\x0002Û&æ½ÐëËÝ\x000cß}¿½®`öþW½¢eÌUGù\x0016(ªdËá¼ÖÙ|Ã¦\x001aäÛ¬4¨åË½{2À;\x0003jÞpêÎ`ÉA\x0013ßFíA%À+¦dxRB\x000ebá9jß\x0004¸QP\x000bu\ ±î2=W&\x000cçQ7\x0001n(Ôî°¶ì4G¾çYòRÍº\x001a	¸QµP}\x0004eê!"59ÏGP\x0017é5\MÑ\x0004¸QÈP	S,eþ)åþ9EÏ ´ÃÅ'M\x001bµ
µ¹\x0015J.c
h­â\x0015Tëi##\x00017Ê\x001dj\x0001(\x0019·8&>ó\x0005CryÕp"ßF\x0005D5Í©
ÊDl\x0014öi\x00017«"ª\x0001]j.qòe@Åï}\x001a9½Y(Q\x000b(Òê+f¢.) j8\x0013¿	p£v¢ú(Ö
<ÜçHWS÷äFRá8¾Írê\x001döÙ\x0004>\x0006ºå\x001dÖ\x000cèæ\x001dÙ¬°¨}è\8 Â\x000fm¹8QsÔ\x001cç[=Í\x0002nÔ\Ô>#YûÎÉâ
\x000fczFR\x000bæ¼ë9\x0006#\x00017
1j\x0017Ðæ.i\x0005\x0015öÈÍi2ó ýÓ\x0008ÍÚjM!´Û¨PÏ-Õ°ëy<#\x00017Ê5ª\x001fâ®%¸\x0012Ê¦Y×Z·G\x0002nTpT\x0003Ú\x001c¡E1­Ø\x0008²¨a®eDLoVu4HAAR\x0010çY±*\x0013\x0019\x0010'3<\x0005àF¡G-`Ä\x0012Ì\x00178W\x0018~«
ß`E\x0013ßFíG-¬)¸è0§?«2+eõi\x001eâÍz\x0006IsI{j\x001bH\x0006+\x000fñÜÍ\x0012\x0002\x0010³\x0003(\x0008³úgùª<¤¾á'O»=\x0004çuIûU)ç(å«a//
¤m1I.¨øËùÙa¿n\x0001T]@Õ
¨t\x001aD¬À¥Ä8@L\x0012\x001d×³³Ú\x0001u\x0017P·\x0002Ú@^_l.\x0004X
t\x0019n=\x001eÐv\x0001mó
z®8\x000eð(JIÔC¥­çx@×\x0005t­"°Í\x0014¤)+(¹Z\x001clºÉ±\x000b\x0018\x001b\x0001­\
Ó5óc\x001c¢.[4þ6>)zX4\x0002\x001axK¬/&d«.8_ô\x0019·©Ï4\x0012öÅL«18æ{lxtt%BYlD¿)\x000b\x001b	{rF¶
\x001ai\x001d÷$1ÞqÏ\x0002ãØ««§o²é\x0001V@P\x0013\x0018Ð¦%§ÀsêfÒT;aOÐÈVIÓ©ýÓ\x0018¨t}\x0017&h\[¼3=I#[E
\x0008\x0013¶µ\x0017Ä\x001d.è-Zu\x001bë]d×~cñ±*Ëõ8`÷-\x001dNê\x0008/½×î\x0010½H:E\x001bjÂãðÿsØC	¬"Ï\x0011N¼¦ð¸!}!ñ\x0002eºP¦\x001eJXN$Ø1BÓ\x000b\x001c³_O¼é0
åo]bÞ\x0016\x001eµP°\x000e)t³Ì\x0016³Ã[ØKØÖûÙ/8\x0014pw6\ÄÛó	±U\x000c9~q®\x0001ÅªÃz¬zË5\x001dÂ¾Â\x0016Ï~ÁQÃ9C<öÈã\x0014rgr[\x0019 _5OQh\x0011ùzAÖ$r%ºäJL!\x0007ûE3yd?\x001dª¹L>Â9\x0006\öÀå$pc\x0004¼ä=-·í-¸´àØfqÐm]²ôÙA'äS÷\x000e¹tÈ½LÍ¥Ó;n¦¤-|ÝPDîzkî&­9Î~Îù8\x000eKWhÍù}²Ü«.¹WNå\x0014\'%»àd+fÝ9
Ü÷Àýxpl¼Ó \x0014fÎpå²ZÕ&lh²#É¥"/1JþâÃ»åÕõýìÕÕòÓ¾ú<áRë|>×¬M*^\x000cgGÇ'ç³WÇG/w²©Øs=\x001cbÚL¹»7\x001fòrî©Üñ!uNU
³®±cN*\x0003ÃI:)«Eo<ÜéÍÎËW\x0001¦º`ª\x0005Ìq^±Ä\x0012õl\x0005H¯$0³®d·.iZ±<\x0002	ÁJÖôò+vFO\x0001³]0Û\x0004&èX7í©¢OS¦1låº¦	Ì¹.\x00186Ù¯&Ãq\x0011Ôc D\x0013\x0004e°AsÞäzL\x0013ï­oZ2'HjÉfÐ¨ËLñéWë\x0011°J2í¨÷@Q¦]êBð\x0006mÅã÷Yn·¼Çk\x0019¸K\x0013,\x0011ç\x0000è\x0012ÂVzÍ\x0002y\x0016ÈüíÏrßå\x001dz5ãQ'ö\x0015à¢0xÔ\x0014ÓªÜb3?ÕFªÑ:âÖ\x00154ñÝçpuýãÏ\x0004I\x0013Înÿ|\~¼ú\x0013²tf2±÷ç\x0018%ÃÌúìH\x0015\x0006ìÜ|âmP¹»1\x0006¨&û¿Þ\x001eýrüßÕýu\x0005\x0011þÔÖ¸HÜ»\x0013O
pdn\x0003ª`\x001aCM\x001dêqBÌ0Þ¦\x0008p"ò\x0004d\x0005ù\x0006F\x0003Äµj [µe AKäg"Ê\x001dK´J\x0005«$2ÑçÇ\x0007Ì¹\x000færãîM7¨ä~5\x0010%Çb&Â®í(\x0016"5¨${U\x0013ü\x000ef"\x0011(OãC"j>8\x0008î6MçÈ\x001c8:F.»åð\x0018IË@j"PI7«\x0006i.m"JX\x0013\x000bå\x0018Ñ\x0010ëÑD%¿¬\x0008\x0014}!t÷]Y"é§\x0001|²j ªc@ ¬\x001a ,Âh,Z¥Uó\x0018\x000c\x0001g\x001eÍ7?Ð\x000cY\x0004\x0012ÓÄõ*a¬H\x001e\x0002$é9£AèØ
0N{ÎV	bµ@ Í9\x0012èCÓDGô%¢i§\x001aß\x001fÓ"®­s9BROVójøÉ\x0013|ÎÍo Jå\x001dHæÆEHÄÂ±të\x0019MD-H\x001a\x0004fif"SHsä§]}?g¤£
9{*\x0013\x0019ºj:sä'®QÉ,lxÒ\x001c\x0011Ár\x0005KOSåI¸F%°zTî}\x000cD&äf`¸FÊó\x001aÙ'jZ\x001bÄtHÓZë\x0011Ñ´]ãö
»\x0016s¶yÞ5+y×jd§l®Hi0A|îJkäL½ò\x001aiêã*å³a\(k$Y¡õåá·Ó\x001eÚUgõ\x001a¢\x001b\x0019½\x0015¸FZñ\x001aéiwK;ëÈÚ("öõÊk\x0014Êí7Óî\x001aW\x00155²8¨'­\x0011µØÄ5â\x0015¨Ï®ò^«
Ù+2\x000f©ü¦½'¢§\x0008\x0016Ø6ÉGØ3&²8¶leËºi@%ó¶zT9DÚ\x0000Ã\x0012¥\x000e·ix~ñX"R¸&uMÈ4ÈHñ\x001aESÖhºÆÅÂõD*\x0016\x0005ÒÈbïã^Ñ\x001aD%\x001d¹È\x0017\x0005ÒÐt\x0015$¬\x001c\x0005?í\x001cq/´\x0006"+\x001eµ\x0018d!ö¬2¢\x001bÎ\x0011«"6\x001c#Ë§Q"t¦\x0001Qo¶%¢>hyÈÿ\x0010Ù#b&êüèávM¶µ+ÍHæÜ\x0002\x0004åêi/\x001a7)j r\x0007T\x000e§\x0002Q\x0008¶\x0008£{F=\x000b\x001a\x000eZù\x001fRº&\x001d¢«oâ®<úê5Òì.öF\x0017ñÃ\x0015éMèà\x0006Mk\x0014LY#M»æe\x0011Ø\x0013Ý¡«Tþê5¹12®9 Å(¨¢L\!\x0010Õ¾I\\x000b»ª¥\x0015¢å)ZöÀ®ê\x0008ªiBN}ÊZ¢åñ+;VN;Ó«Êõ	ì¡ñÅ}íÕêM\x0003¢Þ\x0017
@\x000eçÅ³²¯\x0018¨xCÔ4É®\x000bß$\x0019\x0005µ·Î\x0016å=+~¢\x0018ÂÙ³±é1\x0013ÔO!oQ\x000cT.ýÄ%ÂÑ³±mÏL\x001aôJD2\x0012Ñ
h\x0014âó
@6wÍþ}öÎtÂDjÒÍ}>ZÎuáá÷ÞÛw\x001a\x000eöì\x0014mhõÞ\x0003
ýk6Õ»¦§\x0006"ê\x001f\x0004ï+{&'¢Ô+"O
®w`ù\ä\x0000ö\x0006v+ìvdaÄ\x001dëF#ùg4%¸e\x001c¿g6EÁUòå$ÉI\x0002[æî¹m.,Ç\x000e#\x0017ôÊÍÇ"£Ý´UJ\x001d_eÛ«\x0016Ò8sZ%Ã§ûiBE2µxm\x000eìâ|p¡¸e¦¹ù$^×ôÑ´FÞ5R¬;rßÄ¤
\x0007Ú?K\x001fõ®GT°³2\x0012rOvDr®¨³ø«)H>\x001a6Îa«Ö,\x0002Ü\x0001t`k_O3e%zÁÒG\x0003Í¹[Häs\x001b!Db­Öè\x0012@¥þÔM.c\x001fsz%ªH1W«ÁQ2º\x0004¦\x001dn\x000c}§\x0006"Ut$,F$"],~?ñ}Ã±wé£\x001aI\x0005Ï:IÀÁÎ\x0019É¢>!95-	"M*Mé=XNC×MäéBpÛ\x0004ÇBv°ãÔMá\x0019ï\x000eXM\x0002é¤Il¯Þ[;-\x0014\x0006Ë¶d\x001aMc;ð¶E¶°\x001dì`¹mSÎv·»\ýI Ýæmsð«¼oVliJ	üEÓ ­<?®A(\x0004ð\x0014~Ð¶Õ'fA¹P.¶@©Àé\x0010\x001b#yk"\x001bÛðL\x000c­ù4Æ7-öE3Áa´PR(í4éP	ê²\x0005Êä\x000eMÙ±%I¢@Mò\x0002àñ~÷ùÇý\x0013|÷t\x0007RÒ\x0006\x0004\x001b;*'êáòîÃ_)\x001d\x0018c\x0007øóêöæÃÕÍ\x001d4\x000edGt¤Â)ô!gMh¤W\x001b¾­W§¯_\x001c¿\x001e\x0018ÂÖ'?U$Øn)Ûn 	R:\x000bä\x0002\x0012$jã`×à_\x0002êÖÄèÜï\(\x0007/H×©Ki\x0006q"´Èë«?scÙ¤ÑÂÏùíã=¶_þyñ³GáÃé\x0016Ö#\x000f{ò&`1z:2ÁolÒùéÛsì¾þü×ùÅ®<cscÿøú'åj§\x000cí^ý³«o)|×yÖÅµ\x0005¤á\x0013¤µëËÕk°vüÛP&y/Âc\x0012×ûÿ×ðÙbÈ~Ä^
té\x0010Ùð4ðýñáý\x001fWß¨p>Ë?_ü½¸ÞÍä5XI[\x0012\x0004ÑMK¿á.}>ÿ×ü¤
¦ÄTAÚ¡(£Ñ\x0017X÷Âz\x001b¨¦ÁÔq\x0008
 (]q°öbýüÔcÐÔ:È!P\x001cå\x000föR¥Õy·~Éê9hºK
	"Oüå°:7·ôÆJN½³»nÕsÐ\x0014ºõ\x0007Yæ`/Æ4=\x0017£øÒ¢p\x0003\x0018[«.ú\x00184¬¥j9£4«@.ç»b¢&\x0015,e[Ô¤ }Ôm¤x]Ðsô\x0017¶«*¢ëb¤a[PåX}R·$6\x0017\x0002JVäó(Þ\x001a¹7¸\x0007åÆüý÷Íw*¤Ãò¹çXèr\x0007oÔýnmÆ`8z\x0008Ï"Å Ó\x0004WDQaÝø{¥0gð8\x000f«2úöã­ýHEØ¹ô\x001aDýå\x000f\x0004Ú-ì.¡Cá5gV(AÉyðõ<\x0006ñoþLG·CDÃ\x0011k<æp"\x000e\x0018h\x0007\x0014ªN¯ÂVt;pö/\x0010&\x001aÇ\x0006­D^ E8·<ãÈõ»ÔD#ÓáÁz\x001cÐ\x0018DV\x001e°U\x001fÙÆ Ò\x0002)¸¡<4-\x0012ih¢À\x0019ÅµP\x0012õ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=?êî\x0005ÿ
\x0001ü|wmì÷ÿôìòîæêâ~ß6Èg\x00033\x0013\x0015I\x0011©ò\x0017RëÞ\x00179;zsz¼z;\x0006ºÜÿÿ@íáDÐQÒ¤5*Mù®êM!è§!°±=AåY7\x001eÃ`©7}bP¤\x0005\x0004ÙZ*\x0018Èz\x001cñ)°\x0012$\x0005XÂðóFûà¶\x0013\x0019È@\x001bÁà\Ó\x0001\x000cx\x001c\x0002½kExÊ\x001dSwÇ§\x0019°\x0000>\x000b\x0001Ú+ÉnéX88)&\x0007,Ðãn&&ä}íão!;Ú:¯'2Àþá_#Î$<\)Àc¿!ög\x001eÏû ÕÔo\x0001gA:\x000fØ¹ßÒnmq®(U¾ÅT\x0006¬}2£¾EjN5\x001cÐÒ\x000eHB\x0005Ö?mP\x0013¯&vÖ5£¤$Üò)MFÒløSX\x0017ÝD\x00068Fø×\x0008\x0006YÄ\x0003\x001eIO*Ý\x001cI'k\x0018þÿNtÙýô\x0017|¸¶½Ñ²üx{q¿Ç`qF°g@ûàÉÁdË\x001fH*½\x0015Kê¶P\x0001ÛeùâlõvØn)ºË¹Ýíe\x000c§!\x0017m\x0000§\x000b)$q#\x000c\x0014yc[.¨\x0004ªsK9\x0000ÅB\x0013A-¿É1´Àô]L?\x00053Ð 5ÀÄ¤H$¨a?·´ì ¡\x000b\x001a&í§)\x0007\x0014\x0007RÐ·Aµmòác\x00174N\x0002\x0014ÂÒ©0ÙÑ	%ç:\x0008[Ýâ*Qf\x0001¦Vý§FÆ@
ïuÔÔ;ÞRß\x0004´'ä$á¤Ln«ï1K¹\x001cÒ\x0018	T·Àì&9E6\x0019ms\x0010CcçÝlÅ\x001b°K4Qª¹2TmËzõHÖ¯\x0017Ç7_Þ¯o?î1àÒ°S[!0û\x0004ICÊÁg(eÉ\x000c.\x0017Ç§¯/Ï^\x000cÛqk¾LPiO\x001foé¸P\x000c<ò\x001càÄ@©)£Uq¿êøÕÞÑõö;º\x001cxGG\x0006³\n\x000cÀ)&YyÍ^Ù_Ã«»¼;ÎìÈXÈ
\x000bò\x0006{\x000ev\x0012R¶Í6ØuÝD`cÙEeXò÷20Ü:Ó
8vw¼\x0007ãÑ«·9\x00111ë¿&lvX
_¸:`Ù¿s/\x001c!\x000e¶\x001câÜQ~+æ0\x0003ØöíT`KEW@l\x001dÇ#;1í½ÚA\x0005¯êË©BÂ<\x0013
#qyÌI
ê\x0008Î\x0012{Dp%poÕÔ
¶À%c	CH±CRÀ0\x000cÕ¸'%Ôd1atma*UBÔ`àpÊµ\x0012ÄÊ÷whâ#\x0005[$£A¡Fæ(°¦9$a¶£#3CxJ>¸¤Ø\x0005\x0002éXe\x000fªIü¾_¨ç~zNz\x0018;¼\x0001>ÌºM]Sßô½d#\x0002;§\x001bI\x000fg¹F\x001b\x001eR\x000fO\x0001\x000esos[`ìþ4ªí¢ÚhÔÐE
ÿ¨`{à-ïÞÖv\x0010éëÕúòîòvÏqNå¼k¯Ñ=\x0018³.)\x0002M·åG§\x0015ÿðõñòèÍÑÙÓ¤¦Kj&ðÊ\x0011d­´çdZa9
!ÍBoj»¨v\x0012ªU\x0007´§"°S¸\x0012Òµ~PÌVº.©DÊý50\x000e.Ëç7F8x\x0013Rß%õHÍ\x0015¦¸©l\x0008Pl\x001dïi\x001c|l«HC4L"Å¹\x0004z[@¨2òZ1h× v\x001d\x001eúÃc$+:])¤)\x0011ù}MiK\x0014±mXeUNÛ×âÖ\x001eÐýWªå7]×ç¡ª\x001eªv­"%þ§ø8e»`TPÛljOüo{hÆÊÂ÷)>'9½Axö|x5ì>®bí=\x0000rÚ\x000bà\x0015{½P\x0004ð\x000b\x0010õF®¶9\x0001½\x0017`Û\x0000\x001bÉ\x001a©å\x001b
\x001cÆXbëË0h/V±öÞ\x00009í\x0011Ù\x0016HEV2y>U:\x0016\x0002Z
º;ªX{²UN\x0013®Àj)]

F£JËÂUè&ûªzÂUM\x0013®^3 #	NÂs¾\x001a z\x0002kÛþ\x001eûº\x001av¦Öpå|«`Ü,Õ\x0002j\x0014P9Ý\x001bC8Hó;@¨¦Í÷ïÉm\x001fÁXÕ¤âDê8¹XØ¯5K\x0006®~þã×»^qc\x0007ñÅÍ5û¦>kj\x0003iE&5týézýáÒZ.þ\§0­Ï6ÿ\x001cÏ¤ÁJNElæL"` \x0007Ë2=êü-_,\x000f3÷ê_o{«yqúj¥ÁÆ»]å½EQdûEY\x001cÖ.\x001c×\x001f#¯Iº¿ß¨°ù°Ñ\x001aæv(¬èIÿE c^\x0014¨IaÚ¢Ö·\x001f.¾îY\x0011UüýÏYQ)ù³¤óßþ.á¸¼$\x000b\x000f"\x0001\x0011l^Àf\x0016§»\x0011\x0002\x0015ÿG}'Îåúo¿${ýg0\x001f~\x0012À	ªSþ=ü|ñåòzñÃÅííúòêêæzÌ:ºÿ	¬#=J\x0003å¥æÝ\x0007":Û|àÐâ°Ú^Çá«WG'\x001fVggË£ããÓÁ3ö°þ¦~õõùÅUêU\»íÑJKïÕ2gçÀ .ÆÞF¯¶ýùêøx(1×ü¤¾}áºSQ<\x001aq{GMtÔÒXJC-@ô¹ó\x0002Î\x0004,óÿê\x0010¿»k÷Ë\x001fÎ\x0002¯.¯Ö£>úöáU2µ\x0014Ã]T\x0006A÷Óy°¸·A\x0014Ão\x001bñÕÑñ #Õütûí·\x001f:\x001fúÝúá·Ûû)Z¡~dIU
9*/¢ÍÃºV1´ïçïVgCIm=Ê¬\x0012M§\x000cØzÔ¼¶¾vùØ \\x000fÇ
Ê\t?\x0012óç\x0013¤©oszS4)b§:\x001d\x0017gQÆÔ#)6õ+ENj*>¹ÏI%ÿðTÄ7\x0013%\x0011+ænP\x0008B±±!KRì\x000cNª\Áé)y\x001a9©OmâÌísSþ2SËçpJJ\x0012§Kj\x001arb\x0016\x001bqúùß\x001d[á_s8q 8INx$I5Ñ§üÙ?ÿ.?É^ëÔhýiÊk\x000e\x001bjR\x001e\x0013*QÞç
DJÚ®ÒÒó8·*Z¾\x001c~/;°ÜÖe\x0016¬\x0011É«»\x001aÓ_dµy°\x0003ìªmX¹ãË<V2>\x0012+ù\x00016¥fØÁÇ³\x000eÛÁÌõ©v\x0014aq
¨%Øâ\x0013±CÇµ;ÅÌbµ\x0002û
fV¤+²zÉï½C¢ª
vÓEf\x001e­Çn§Vd\x0019Ò²\x0007ú©jB[ZÌÌ£Í5UéÐôÂ&Z]öÖ49\x0008þ3sh08x&É.\x000c¤eZ\x001c\@´~P©ª£-Íifímô)\x000e´ðÚZ-Ê´SM×¦qÍ¼­Õ)å'ÁÜ\x0000i=\x001f\x0004glÒ:ÚÒÕfÞÖ¦jéØzw@°J²òbD;V\x001aÌÌÅ>n*ª¾îº-:)ùóh7%û3% \x0005Öù\x0003C/W,¿\x001aé\x0007Þ4óÞ± \x000eI¹5IC¾&ò«Ó`\x000e­öEEÀ\x0012g5|\x0010L\x001bñµéi3ï	~È\x0014ido¾d,\x0011¼ql\x001fd¼ÿöóVËÆååmÊK¬öÿØÀ#gS?·äQ /5í8¥×Åòèl0U±Úm3\x00153\x0000\x0004±Â]31ûX\x000c{ÿbPÃêL\x0005k§EÎtV8¥¹Ù<ìkÌ9 Àjs×dd\x0015CÖW\x0015k§yÎ\x000cVM\x001dUçÚ<l:®ø\x000cøaIPÚi«3\x001d\x0015/é3ª¦ * z)	uÓ\x0005c\x0016k§ÁÍdV%C*wK¬>W9\x0008Ð\x0011,o+ÖÚÎgeWÁ<Vì^a
«ËGÀIWXK÷Y¬\x001cáÅªUR`Ue\x001f\x0007²ª<¶3¬áw¶\x0015>V³YcÎ¹\x0017©®ÁÑ\x0019`U\x0016XM}%7Ì<Vgra\x0019°Ê"\x0006pF$±\x001aÓä¼\x0006<³X-
cJg \x0004b-"k3cy\x0006«J\x001ew1÷\x0010hTùÀºkË\x0000¶¤\x001cJ®\x001a\x0008-ê@ú\x0007+Mî\x000b;ë#X¬{J°Alú:ÏEwsÅ\x0016öQ \x0015r9`cÉ#9áó\x0015n\x0010sæÛeh,¸]L\x0015{éí
vV
:¦ýúáÏ×·ÝVhÏ/?®\x001fn'\x0005\x0005\x0005JDª\x0005\x0006³ò¾\x001a\x001aùàòb0nyôby>ØR¨ÇI&âtÎ\x0010\x0005\x0015\x0005¤~ì¹Å·,OôñAz3\x0018¼\x001cÏIÆá\x000cÎ\x0000¶Ïç4,\x0013\x0016E6ÎæT2Ù.rÞâ\x00104?¼MóÐS\x000bò\x000e\x0004eãÒú\x0014§¸ùÙÜÿÒõc\x001c~^ùzqûáòâv\x0002+ì¦y¥
¾\x0011m*0PÕ~Ð~=üqùêõÛÕÙáÑj8½®\x0000+üßI?3á8:Î^ÐXg/*²òê¤\x001c:\x0006Èh_¦¹×*,í#;9ÓSã »¨\x0018\x001f/ü½ÉN¤þÄ)EDæbhØä \x0002½	ÉÈüIªOïy¸%Æi8£e¢"cl[£@¼æ\x000e8¨ËjY6x3Yö<
\x001dÖ\x001c§Çjbqkàü\x0000ÂYg\x0007¯*Xv\x0019Í¢
Á¹t¬ZÅZÌ\x0003OÐ\x0000\x001fòkÔ±Çh\x001e+`å\x0011Tº4ÅjÑÐ!Í`Ó\x001el\x000e¬Â0húy\x000e4\x0015cT09Ã	Ïµ|\x000eÄ \x0001V¾ùô3os1¼§É\x0014¯\x0006í®C/Å\x0008Ü_/.ýÏ¿öÕÄyInFI\x001a`¦°*^xºf\x0014PHöÂ\x0013¼§ÃIO¿þâ~~àb·\x0014\x000eýÏû÷\x001f\x001fÞÃ¿{ÒÁ54\x000e[9ì®I\x0003c;,Á'íxñãùóåá\x0018PÎ\x0001õpfcvÆ¸üðFÁ¯XT.ÎÑ%\x0004:\x000b2ú\x0003C6$ÿ!rúÀÞ\x0002)\x0007=qãI9ü9ë»{K3¬µ±\x0008,\x000eß]ºA_ÁxR\x000e}Î \x0005[Fç2\x000c u¹å\x001dÚ2BG&\x001döj'åHâ<RÅ__H*n\x0012\x0018G¤=ÕjØ·9\x0014Ó>âÜ[z2»m¶i@ì\x0017ÃÉ%cA\x0015jWégÞ\x0006ÅÞ\x000c+²;6Y²üTyç¦¢~úöñgõ¥£\x0008]Ü}½Z_¼¼dt{\x0015R±
¾ª8È§HRì*tF\x000c¹\x0007ÎVo^\x001f/O^\x001c\x000c\x001b`\x0005\x0017Kf¥À\x0001DÏ¶\x000e!¹¤ÐÅ\x0002szPZU\x0002£7\x001eæ\x0002ë\x001cCFýÕç =\x0002[É\x000f«\x0008CNÃ1ÀòûýÝç?Â$\x00084quÕÿps{q7*1î±OÞ¦ôdùâç5ØáÇ`µøá\x0014Sã6¬Ø|KRë\x0019¬`\x001dRü\x0000GèHòÇzÏ¾ãá,¾*X\x000c}ø\x000cûûUP77¤r*|øxq·k$\x0003vÏ[>\x000e`)²\x0017Ù\x000e\x0007*}x±z³è(´¹r#ý²ÇóÎºßBG5dôÅ»õDm6û¢£èòÐ9Ä6lûÁì}æ>_¼[&ö1ò/ßÌ·¸îì6·}}s=ñh¨¢×`W'²Ç]Ñk´\x001aÒ\x0016hìíkø\x001d ¨ÍPàÍ\x001fänÁyLæ\x0015<sËÛ÷7\x000f¸\x0005¶ä§X#XéYqÔAðÝ\x0017\x0006i\x001e/gÏOÏ;Çz«(fÃÿÓzk\x0005ëVK)õ3-¡¸Bà9aå×
æ+o/b¨²\x0007Îµø	5\x0001ñló\x0007ÏÒ?óÁ¡"+.ÓV!6²\x0005^qò \x001aÍT\x000f&Ñù¡Â*\x00143{\x0016"#,DºÍBà\x000f¥æ¼»¸ý8îÆ>Îºr\x0007ßn]Ic
äüÇ"Ág=/áÝêìÅú*Ño*ÿ õÕ\x000eÒ«»ûËÛIÞ	ì-Ò uÎy¨z²öõ`Là\x000cÎN:H¯NÏß¼=Z½Ù]ÞF\x000b*v\x0017ÿØh	Ø7\x001cm©?"\x0015\x0013ENrÐúõ%<ñ\x0019ðówWÉ7Y\x00056Á`drs\x000cw\x000c\x0018?¬\x001eV~\x0008­ûKÐí>Í­¼0-B±ù\x0000/\x0003_g§\x0007uòÚ5øþ\x001a|³5Hûþã\x001a4Ýg,
\x0008¼ÁDåÚ5þw0í¾\x0003Nc¥5àOMnò\x0010Xmw#@0uÞ¸$ÖÖ\x0011@\x0019\x0012ùb\x0007lev\x001d½¡Ñ:b§QþäI)«¸Z/ÎÖï×ww\x000c))óÀ\x0014\x001f6\x0007:\x001f)\x00135ÉXåìP@YÆñrq¶|¾|óf¨orÂV¤ÚmþàYW>ýËÃåõÝ4/«\x0006e¤\x0013(\x0000\x0007YÛ\x0000Å´
«þ\x0012ÿr~tòfÿCçÈ\x001cÜüA6\x000cYcZ§¶\x001fÑ\x0001¶v-¶Cd(\x0006sº±(¡x
\x0007ó÷XqZ¦Æ/Ð¸ÿ#4rî9,\x0008Ý\x0005¥n»"L0LßpÀY~%Ãk¸ÈfxEÃ_É´ÍknÄ3l7Kúq
GmÒ\x0012<Øè¨h¬/à^CâÇ%±}zlÞû\x0006s\x0019MÏX}ººx½1¾Cnh/jÅFÝk\x0004¡&¾zy|´çjoµD7¥%z£¾\x0014`@PMÅùÐTó*Kr»ÖCjø\x001e\x0007C¦þVtSÚ¤·ê¾c¹
#cr
÷»ïÈA7ÅE(Ó[i¶ée½\x0015«xOOâOñ<M\x0003ÀàÁzñ\x001cþ//áV\<ü6©Ã¦ú\x0000ËÑØ5+\x001c%nÔ¹|Àa´\À#÷ö\x0008.ÅÉêüÝ°÷ð½¶g\x0015=ÇL\x0019ØÜsöÍúþáöúrAçq) éT \x0017I¤=Ôj7~nGûfùöüìäh8¨HðZé.<þc\x0003ü4^5U\x0005ë"Uª`\x0003¸ìÜ0Ê\x000ff%ÆW¢wc\x000e\x0002\x001c\x001eqñásRûÖ_.>ÝÞLRû\x001cV\x0000$\x001aXíóéÌpD\x0017§`\x001cþô¾åÑ«ÕË³ÓáP4,£/Tã-ÝeÜÀÿùâÅúË´AÙ<"\x0014Öa|Ê\x0014ÃARà'Àß
ÕÍ:NNßÁ^¾Úw\x0017Üþ\x001e²ÿ=æ-D\x0007\x001bÂu"\x000f5ÆfE\x001c\x0012\x001e\x000c	O[ï.Ä7ü"Â\x001d¸¬+\x0018{ÒÄÉ)\x001c\x0006M»Úe¨\x0014\x0013etEµo³×\x000fïáøpµ¾{\x0008jd\x001eHbZ,öÅu"×O,æõùsx&\x000eÃc-;ËýåÈËÁ~ªäÂ8\x0016Ó¨í`
kýjôÖÃ¡Rm^Ë\x0003¬åò~¢/Ís/`\x0002\x0005;Ó(Á:\x0008í\x001e>^Å9¬âèí^¡ÕmgMø®\x0001¾Åùqln{\x001cj è\x001b¾äÁ¼Ûñø:P\x0006\x0000ãDÏÖËÛO©küÝâåúê
4©IQ\x001f-\x001de`b¢È·ÂxÏñÁ·ïåéÙËÔSþÍâåòø\x0018\x0014©'W¡¤í®\x0002ÿ±Ù2/·Û*
¬à{Î\x001e\x001c5¨BÕ-Ä(JçÀ+éð)\x0000/öóûõ¤5\x0008°mÌr\x0017ÖÐyý\x0006\x001d)\x0000o4'{ñ»­ý\x0013~jí_èg>\x0017ú\x0012Ô\x000bëH¯4èÏ,K\x0018õ^X±õìYÏÞëËÛ[\x000c^~ø<1÷0è\x0003sOÀ¦o\x0010£Ôì·	®×G«³3\x001e\x001dþ¸÷\x0008Yµ¥EÙäuz}æ\x0010\\x0005\x000cs9û0Í	\x0018bÔ¡¬±ØiP\x0013éÍVÙØ\x0013ö\x0004ïÂbyrxzNÀ=Ë[GÉF<Je\x0019ø\x001dÖï'\x0015³à\x0003®oÕØF5M\x0005õ\x0010\x000bRÓ"Üðe(Ào±|¾¯ª\x0016¡¨/?-\x0002ÿ±Ñ2\x000cÚCI,iÌjy\x0019`b[¾ÓùA\x0013ÑJ¸\x000c\x0014K­¾¦4'muH\x0017$}
Ë_C\x000c6µ­^FJqí,#§¼6YGÊsÉ­þ´Ã\x0018\x0018ZªRGC%a¸ñGÕ2 $\x0007^\x0013ÏºG
\x001d\x001e´ýýS`ýA$_zî¤t¦TÑéAÍ£¬\x0004½\x001e¸þûV¤¨3DYJ="`Ii\x0015·7L\x0011V\x0006\x000b@<	«ÜvÁq\x0017X\x0017v(a
³¥\x0010üðìôè/ûÀý¡ç<\x001azÙkpx{ywóõó4¯¸Ë5×¸ÿ8ÛÒ§¨±Au\x000cxÙkpxvôæíéë\x001f÷=sD¯»ôº	=\x001eÊ\x0006Ê§Ic yc/v*\x0019ñj|ÓÅ7Mðq²3¹\x0003|\x0007Eá\x0015\x0015Øp\x0008Æ\5¾ïâû6øN¥Ê×tw}\x001eá\x0004ø\x000báàï\x001dÐÅ\x000fmðu	\x00044>s:·I\x001cd*jl/E\x0017\x001f3à[\]Ð®Ã&Lª\x001fô<æ\x001fì;?ß§\x0010ÞX<`èê^¥Å\x0006j;-¥,C\x0002TódÉ\x00186>7]`\x0016å?~z%®·\x0012×l%\x0011®\x0018Gß1ß*©p+¯dØý=i%¾·\x0012ßò\x0008nÇà"GJ5W\x0002aOÔá¦,S\x0016\x0012{\x000b-?ILõwi!*ÏËLyf¾¬¤éá2¢»\x0012#\x001a®\x0004sýÈG#Ë'q±dµ\x000e\x001aCÓ\x0016"{\x000b
\x0017¢cIwÂ¯Ã)ìkÚSÜ?e\x001dª·\x000eõßv\x001dº·\x000eÝp\x001dÆ\x0005æ²´3ä\x0006Ui+1½+±bÓìDs
µFBïHïM4íÞDXc\x0008GkGÃÅX\9d\x0006ýÉÓVÒ{\x0013MË7Ñå\x0002þ´\x0012ÉÅZ8WÒöpõDÓîIÂûÍ'\x0011Ô#6\x001a\x0015ø¾ëÁÞ´ÞJBÃ\x0004Ëõ\x0011#H~e6\x0004|§»îÕ,¤÷¸»\x0014ÅúÀÓT\x0006jàØ¦gËöÞvÛðmÇ(º$²T\x0007\x001b\x001bùl
º\x000f¦-¤÷¶Ûo{\x0014f\x0005	,9ÿÔXÇoÉ¾cSVÒ{\x0015mÃWQbS:ª²°M+\x0013$¯$hRZ³Þ«h\x001b¾8®DÐ-1Z\x001a£KwÓa±íéê½¶á«(Aïå¾ÒSÿóh¼(§K7}ßmïU´
_EY!tMD	/m*ÔLÛ³Õ{\x0014mÃG\x0011Ky$°¡òºÇ§ûÍÖ¬¤÷(Ú¢ÄI´\x0012\x0011hBWÄY\x0005¼Æ÷½÷*Ú¯¢5åÀ»Bm1¬Ò\x0014¬÷´Ó°\x0012×{\x0016]ËgÑBÇµ=Ø­-÷¦bËõ\x001eE×ðQÄKBm`0ÅYQ¶ôÅ\x00071¢tÍJz&¯khò&±EÞ\x0010¸`ç)QµµÓVÒ{Þ]ËçÝ¨<\x001e5\x0013A\x000bÓÃù4Õæ]ïQt-\x001fEåY	N®:2\x0015cñÕ©¶"Øõ\x001eE×òQÔ"ÍI+qÅ0¦|=}U§¬¤÷,ºÏ"è¾W\x0012JQCPEvµ\x0015]½WÑµ|\x0015¥N3èpÑ`>ÃÐð4ý$¾÷øÖ&-¯"Í3ZÑ1mükVÒ\x0013Â¾¥\x0010Æþ,\x001bG\x0004ÝwW\x001eáQ¢ÖÑ\x0013Á¾¥\x0008ÆPÚvP´Äl¼urÄÐô,,ßÒÂR¸\x000f¬Dòu/qá¡ÓVÒ\x0013Á¾¥\x0008¦ñÎë4?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=­\x001e²àu2£;Êû\x0016JðPÐ5DlLí\x0003%E¯àFß±Íc<\x0016ðS¿Ú")Í\x000eÎè,oóÑ
ÕÞÂQr\x000bãð·@r2Ç|ð4+M7¼ÉS»¡d×¶(Sû\x000cË\x000e\x0016>yËQB¨V\x000b<`-¿ÑRÜÔ§Íf¦QA%Ó¨MüØÏTm\x0003ÓÀöJbU®ÒàíZ?bø\x0011£A®F»ÈÕê\x0012ÿ0Ò7øRÀ¾¿K&+ñ\x001a\x0004v#êü¦
üÌ£ÒÇ|\x000bÁë%ÙÐB	6\x0014xb´¯Å'È\x001a}S¥ö~IûEYÀhìlBN`\x001fyõü &O­J\x0012
å<·XÑy¿³Ò\x0004*1\x001egKAµ1þ$ñCÞF\x000cexL´üRðÃ9m©ÍMNÜd(\x001eI\x0001ÆA øÊÃ¦\x0016CPZµá³é³$¦G¯tÍrÐ\x001cå³§\x0007£ü\x001a/©Jàøñ\x001b[M\x0005Vt\x0011×õ³å%z1S \x0004¯*&£iSÕÙ)ù6¯§oÉî\x0008Jâ!ÃÁZ/Ö\x0017·,©Ñ$2¡æÊ	¶z^3ÒX­ÀàÈ\x0018¿\x001c°.£ò¡¥ò`#^}¨\x0002w\x000fOªjO5h#èE[øB\x0015$u\x0014ÀF§\x0002Eër¤\x001bõkµSÜ¡$Õ\x001d\x001aè¢ÁÜ·\x000c#\x0002í,$Rlx,a&âAïj`2\x001d¤Òm6ÒôY²¥hcñg µ\x000buí\x0006N·ÅTÓçþnz`ÂP(gpuîü §µi÷\x0013~îOºÜ¡F)Ç)\x0011Ù¢ËÏ¹AOÖ°³|\x0014\o)Lã\\x000bòq¦ú
ÍÔ£\x000bèwdå\x0005²
¶z¦24ÞÍa8 Ì5¬u4-T\x0014Ôx$ÎiÁQ3\x0014GsÊðÜ\x000fgG¯?ÓÆ@§Ïý9¯u\x0018\x000e\x000eÅ3¤Òùq~0,Cø\x001d(AÙ§É¢*
P\x000b\x001a=;ÎÝ°¡`Ì\x000e\x0011@!CAã\x0010/Më\`*3\x001aøpvî=ÁA¢û-u®$6ÖÎ)ÀdÌ\x001bçz·Ëõ®ß\x0002­c0PÄ1ZÏvqþ_
ú«ërë²kªa\x0000|û.¦Ê5RíÆ\x0012ôñ[\x0002S\x00068ÛÛÏõM´h«ÂMH»lX\x000b&aóõ\x001a²ªwt*µå&\x0008ËAâõüiw=ê_O\x001e\x0004;­'\x0019¥±þp¶ÍheÊj9A¶ZQ\x001d´	Ø-¨¸@e´àÉkõÃ%\x0019¦ç}é÷?ºà^¿Ä¤ê¦\x001duhãR¾ß]Ê÷ýKYkgp)IùA1|2\x0011ëb\x0017ë¢ÿèkt\x0019Kzb`Íú§\x0012ñÓî2~êwmg\x0019
Í\x001csqJ\0£Á7×»òúQô¤¦T=«k¢l`W2\x0016FËëó®¼º#ºÝ©\x0015¯É¶cyñ\x000b(ÀÀ\x000b\x0006\x0012Î\x0016\x0018ö®{4uyuñùËå×[p÷v»õØg¾Lc¯Qü0Óm££W'¯ß¾=¿\x001fÆ/a|\x001f\x000c\x0012\x000b´>\x0002u)¶îjPQÙ1°D	r	Üô#`\x0003±pòwËÎÔn¸ráiZY0<¨Å\x0006Gå| ÂÂ\x0016À,²«\x00173"ï£±c\x001d_I1³\x0001è¹iL\x0018£\x0006ºhðESJ®,vC(î¼\x000cÆ¥³	¼\x001b£iNî<NÛ?æJT\·pàã\x0014wF´vÓ4ÇIw'\x001cÿG4ÞP\x000eµ
÷°WÛ¦ÙÃºs\x0013×\x0008ë1}¶f\x0018gÇviö°éÛÃ.Y
~æ]£Êá\x0002ð\x0004fìh/Âyfå}X°È³ì_o\x0013a³Î\x0001\x000b¨Aæ4ÞÓ\x0004Å\x0013#Íé¹%Cv,ä\x001fi¶¯éÛ¾.±\x000b\x000cû\x0017Ré"®Sd\x001a=¸eýkúö/	¤ô\x000e\x001e\x0014MâëipÚF©¾mÚÁä5mã@)íÛ¸&Hë¥\x0016¦j9V\x0017}Üu3èÉ\x0015\x000f¹á»\x0001â 9\x0001\x000b[p\x001a·üc>\x0006J¼Èæ9&\x0005\x0018¨(0«ã\x0019q\x0002ùü¸#>\x001e\x0003B<ùR÷tØc\x0015\x0015'FÕöÉËßxDç\\¿¿|÷Gç¾~þ|yñõÖ]íÚ
	#bÖyÃæÅî\x000c©ÿqröôôÉ?:ùöõëÓ·÷ãÁ\x0012\x000f¤xº²YbsÁV6½m¾YoÖ^8Hî-3öd<UmV·Qtó LÄã9ý²3Üæ\x0019ëâ°GññÒÂNg9_høÂÿOÝ%Qr\x001cW¢[©
¼²ð!&ãW\x0011,£ ÃÀ\x0006@Z÷¬\x0008(´\x001e\x0006Y÷úmC\x001bëðL÷¸éY,"\x000b
úPå5\x0012uàáq|\x0008\x001f&Åm¤nc-èA\x0011Á7Ó&¾Ç»Â¡za\x0016_s)í|[\x0014\x0014_èêw\x001bU;\x001c>ÅgÉ\x001dÙ¨{S(ÂÃ\x0015ßT?ö7wòêr\x0006ÝJr\x0004.Uo/¤øvñU¯ÎâK\x000fseE¢~æ®ómíÌ4¾èÔ/Îª_/M|±\x001fÅ.>ÚÔ¾èìF4\x001cRßQ,\x0012¬\x0016	Æ`þY.7F\x0007/Î.Y\x000c2êµ¦}ü¶oGrä&É{lfíÉÄ¥ðRÞ4lÉ	/Í
¯¹oÕð±¹»R\x0011føâ¦îew5ò43cd¥íCõvÑ¹£Í³GÛØ¤ôÀûT¼fë,±l{èÓg\x0016N\x0012ÛðHß[ÛÙÚñmÒ^.\x000e_å\x0015è^{Î\x0003Û~-F\ÂWÜéÙÓ%ÒW(j·@«í\x0013ö»\x0001ÄWÙ-³f·o??äg^_¨±Ëoøª_¬£³TP´°9Ùíeó|«»\x001fuö~¤`yèæj\x0010ÛK7øh§Üç®G½\x001e@º¸]_°<¹L«ï×w\x000b\x001e\x0004çÊç4>R§9¢.nøØÜöèïRWu\x0002\x0015`H=±\x0014S×?àÉÇ,-àî/Àä\x0005&Ù)S\x001e¹R \x0002Æ¼ÇÏÎö\x0002N\x001a_ªds¬å:\x0007!\x0001qS\x0018=ÀIït:zâhn)\x000c=èÝ¼ èõ\x000f'õJêüÇ=H¶®\x000f7ÅGþ\x0006Óä
¦Âý\x0019l¯}\x0003Hf7%H>ëB\x000cM-\x0018·´\x0010gË©ôdlÄMñ/ÌF¾Ô"ß¢7Xýc¿ /íÙ_ða%ÌÆíÖv\x000bBùÜ\x0007Eôx¥bÜó!{ýË\x000bú\x0017S×¿XMÿJ×¿Í\x000býñæÙãå\x0007\x0001"ÚDh7`ósö\x0000'\x0013k¿¼\x0004½\x000b
³>´H°(ÅÈ
¾K\x0010wâ%Xf%HE»\x001f·°³s\x0008I\x0010÷@¨ÞÄÕY\x0013G¡\x0007ÀRâuÂþ\x0000u\x000f\x001fÃ0OFé\x0013ksgÎ8ÂÊæ#M'\x000b½Ó>B°$ÏÁñÔ@\x0019ÓÑ\x001fôö¼¬K¡ï	pÖÈ\x0005Ô-\x0001
 Íò!Ì¥¿8nâó^\x0002Îz	X«N·¤X¦`°Ü\x001fDçáU\x000fo2¹+33P\x001fG\x000bká#¡Up7\x001f{3ÃvÙJq\x0000äI\x0005ÄR-û\x001cÅQ\x0001Æj¯·u3½ì\x0015'\x0015\x0010Kì7¤IP\x0005heG
_ÚT@ßÅÙ\x0004o»«\x0016hJ·\x0005\x0000mæk-»\x0014ã\x0013¼8ámwõì!høÀÂ$´Ñ|
_ÜÔÀäß}Ód\x0002\x001f%j\x0002Z¼IØwÊÕ²FE¨ÄÙL%6\x0018g0Iiz	\x0018Ø¼6­\u |N\x0002ÔÚ3\x0019¶fèôùêuÚÚ
ºËîãu5LúùÈh¥z2W^Ï\x0017*Û\x0005I\x0017\x000e³\x0017¤ÅçI%(Å¤\x0000³QLâ½L*\x0005ÿ>\x001d&½@$\x001bêÕ\x0000Ú¤òæeÕ.Á°	\x0010\x0011Ï9í&-È!áF\x0005\x0018q/JÞK Y/¡ù¡æèÇ-\x0012\x0001d³r¸«þ©fßj ù.¬nLö\x001a\x0002`\x001cy\x0013_q\x001c(sø¤0Bïì\x001b:Y&T[¿Pw\x000f¸ToÒÏ¡(çÌ\x0016jsp¾à3\x0001BÝdA\x001f)Ñl¤\x0004©Z$'-íê\x0008\x001aÌ\x000cß7§Î\x0003ô'<ûÞ\x0000©ÆrsôÏ\x001b\x0012¬µ\x001d0ì0{æYd[K±|y(Ý\x0011\x0004Ú³Â\x001c¢\x00078}ÂÁêL¤dBÍHÈÝ@Ø`ò\x0000gO8\x0016}\x000f>4ÐðE»Â°ì`ðeD0KÒ2ßáä@¡ù¬\x0001\x000cq/cÿâÀ³/\x000e #ÜíÁ*Cß½^CÞTAr®ôQ9\x0005\x0010¢Ýá\x0018H;`?\x0014ãÌ\x0008Sñ\x0000'\x001f\x001dà±ìW.1*\x000bBy\âMì\x0001ò$ÀPm
ÉÞsA2V{th\x0000Ëæ\x0011ûhg£¥fÒl7±Ô-4µ®isö\x000cO{22þ]\x0001ÆÐ/IÐ	çTvËíØg¥y6+-GlV\x001a·#¶©Ü\x001bæ\x0001z\x001d­<	RÎ[»\x0004Ï§|l*{	\x000f.¦Ë$M\x0016\x0003'Ç¤'
\x001e\x001b¼¼1âê\x0001ÖY%k94Kú¼ø²h®oÝ³ÃÑ;
qÖQ\x0008Í¸\x0015U@ô
'ódJÚ´s\x0011Ý\x0015>!§\x0000&²Ò\x0004FÒx\x0013å½F\x0001n>¬G_\x000f\x001dg\x000b¢e\x0016¾:p\x001f<%ëÛz» \x0019£\x0018\x0006Êç\x001c@²K$C\x0012Og\x001fKß\xóe.z³$\x001d0XV¿E2Ú"Ø$XM\x0005¯3.\x0000ú¹8û2\x0017d¨kV ³)\x001a@´#>öÒn\x0001¬\x001eàdÀ\x0019B±×ëv\x001fÔÕÂ\x0016.%\x0003¸éÉÄê\x0001Öi #Ê²­sEYE­\x0000aóå!ù\x001aù\x0001Åµ\x0000<ßæd\x0016ü\x0003àÞ%Ip«ÓÁTûâ4¢\x0016½Jµ\x0004JØÌ)$ô\x0012ÄY	æl¯Ô¢ã \x0000Áòe÷ñ0ù\x001a£4Yc*Ûú+jÿÑX6\x001e«/7KÈ¤;Ìá»#MýybÔñX(Óó\x0014ßîãRòñR§b£H¶qñ\x000cn\x0006\x00106\x0001úÖ4Ùûj»\x0018Fì
Bl\x0017»n^â[{ÃäëW ëøO\x0011\x001cê+ä\x000c`Þ3tÉw\x0010¤É\x0016TÎ\x000e}ÁÍ9ç0=N\x00186]ä-q´Ä©JíÝ\x0019\x0011\x0013$»#9»Ófê7ùÔtLM7}J\x0006Ë\x0005Næ*4·p/dÏ¾\x00149O"§Õ*-I&t¾L\x0016\x0011»ÉëK\x0000}â-O&Þ\x001a@°\x001a\x0000©W(§%\x0002[\x0005È¾Lê\x0001Îò4N\x0003#§¡Ëh©ÕL4Étò9	0I®è\x0000íî\x0014\x0002ÄÍfì[\ódk\x0003\x0018Íiä"ï±'@óec½\x0017sfö½J<K3ÍáG\x0003t$Qe1	Þ§>Ì\x0003ôG<Y(Ó\x0000ö2\x0005lñ±\x0019\x0012´¬LÍ¨8³?b>bÐ%Û
 »1\x001a\x000fÂf\x001bsþãô\x0011~Ä±tg\x0006±KpóøJ<YÉj(ÚqÍiÐÔo¶6k°Ï³`eÁ,&nª¯ì!üÂfö¾VöµdÚ\x0011éÜ4±K\x00107i:y	¦I	\x0016Y¯n\x0012ÌR|\x0000\x000c¥_ÍBì­<ël7¨C¶zV¡¹8*Át6\x000fÐÌdAr\x0003,»hÝÖ\x0003­\0íÎÈÕ\x0003¬Ó\x0000m}\x0003\x0018ô\x0011±\x00014:íÆÅÏê(Ã:RÉ
\x001eq8´\x000fÉ*)RÚL\x0017È\x001eà¬\x0004sµF¨6\x0019UüJ·äÞ\x0011\x0017ö(³i\x000e$´ó°	Ð
)¦½ä²\x0005îÄ7­6ßZ*á-óùû7+.\x000b¹S>'\x0005ì\x0013\x001aá¨¥KÉ,]
ÅwVÉÎª\x0006-=
M§\x001diçÚ\x0005¸YêQ|Z¦Ì¦eÌ=\x0005\x0018ä°U\x0005Á\x0004\x0018ïsä¦\x0001zoºÌzÓbG4äÊ(3#`\x0007L½_Å\x0017uÉ¢îæ)\x00043Ä!ÐK³ÃÚ[O\6s
ÅûÒeÖ.\x0019m #d\x001b(ÛnH6¦ÍÞÃâ}é2ëK\x000b@\x001d\x0004\x00072%\x000c Ùa¬f.z	Æi	ÂË \x0012}\x0016jvÞP
¼y½7]f½i\x0001¨ñÜ±ËØâ¹»vØ;«eÚYÍ=æî£IÐ*ò\x0012Ä=gµøB2YH!^©]b©²x$Ú-Naó¡½xgµL;«^\x0012«\x000e¢=Ã&[T #\x0014÷$X}Mc¬i<|A­×\x0002äîjÙÊ¥\x0006psGõçu²ò¼\x0019âl¾`¨¶´Yb+És[1\x0000ÂmÇlÈÑ²Ó²H\x000bÙR&Á²ùS½7]§½éT;Q7£\x0007vÄ:F¡Ip¨krÉ_ùÔÁ,52Ç\x0011ÇÚÝélåP6­êËyêd9O»Å=3\x0018È&CÊ\x000bâ\x000b{'\x000cÁû2Ç÷¤3c-x<\x0019ë+'X\x000bgÜr\x0016 ÄÛ,ÉzvKú«(\x001bwÊ=¹ÊiÏ\x001flnÃPâìC'Tâµw©]2ü\x001c÷Ê\x001a!¤\x000cgïIÅ¤/(»x²1MÎp¯|\x001an³Èïiº4¢±v	B\x0005È{þB\x0003To\x0000g\x0013ºÈOÐiÌ#¤\x000eoó\x001eüÊ¬ütà
Öz­WisN)`|ì\x0004):Ræ«Ù2}`ó¹ÀÞä>ÕcÓçÊÉ­Ç±4«Í\x001eçDÔmZÇkIÐÓ\x0006ìÏÚq\x000f§Èòí]o'ÇS`ó[\x0017Ðs<E\x001f®°=!¥aüòñË_Ù\x0008ñ_ï\x0018ÿuzP²ù¾ÍIìúôøÍ@%!ßuRj¥¦uò.»óãÛïïwG~ã¡Þ*¯\x0014Éê\x0005zMÍæLvâoî'þæ×§¾cüó¯\x0005csFdÞ#øk?üF\x0003~ûæÛ\x0017\x001f÷Ó7
Ç{µ\x001f=_<Ý¹é3$£Æ{nî_¿úäÅÇþñ£öý³è
Æ!5{§MäR\}ò\x001cÈ0q¾åÔ§@+¨2\x000eK÷¸jÒB~\x000eh\x00158ÞJ\x0002f@?¼Ó{ìEIQQw³ÒmCÐ\x000cªÇ4\x0019AeÃdP\x0015í)^ Í$4Tv~ñö¶>\x0005*9Pi\x0002°l\x001esµma\x0001	Ìã£uMg\x0007g@YûJóò²m\x000ch»z\x0018oe\x00123¨¢C\x0015gPõ«&ûÚù\x0005Óõ{{ð\x000cªÇ\x0002YAxâ\x0006&
½QÊ\x0000u\x000bcè.{¸½¥ÎÊªò8WU²Þ#TT®\x0002²ö\x0019¦\x001b±O¡r\x0007g\x000eP!µ ¢qB\x0017\x0014,ëÔe)ñÁTÖ,3)\x0007Ûè.i(ÝI|4Ðæºæm\x0016Öã}àeï\x0003#°\x001amV\x0015I3ï|äËOXXÉ
çõ4cIG04X ©D\x00191\x0006+/\x001bðW\x0010fî`>÷S\x0016î\x000b\x0004C´¹\x0015\x0004Ë¬\x0000É\x001f`8@Ì©\x0007(\x000caÒ%y$¥!Ë°</À\x00041\x0014Y&­°\x001a[\x0005\x0015Vêê\x000eiý\x0000³?À<sêë\x0011hi-\x001fý[)¬ëzñ'XfN°ØêßVë&Ãiõñ\x0002-s(TÇ¡P'HT\x001eÓ\x0015\x0016ØñÙ£u£ÖeQ¡w1LhU
æY\x0015\x0000é<EÕW×VXö÷.«ÁOX3¢bKéÊ\x0012bóØÕ9á½Íz\x0006wqÆ;®¨\x000fF
íÒÝv\x0003	D8|¥ýõ©R&\x0017ÉAÔQ½÷&\x0019Xä\x000c4Òná_8¥sì¾hÖ\x001d\x00082o\x001d\x0016£Å8¥òú Ñâ>}Ð\x001c£-ßë!ÎeÜÞ\x0019âÇ85V©ßÄbo\x0004È°LZü!¦C¬liãÌÜC¯í&Ò\x0006A¤âaMDÏµ[ÃLÖÿÉG\x0001è	\x000bãº´²'<N\x00105XiW\x0016êx\x0008>Þ\x0015ÖÊ{#3Fº&-¶®
Û \x001du\x0002"nÐiñ7±ÌÜÄ¢øRÈo+ÝC±Þ&\x0004Zö´ëaÍÜÄd{­sÆLå-·Ö`åC¼\x001b<rXaü&JU>"6
í^M±ús\x000cëH>Û×\x000c\x000eÁªÝTCÓSZ\x0016ï`Ëa\x0018ySM\x0013¦ZúEåõ,ÙTP¨ë\x000e Ów¢q}\x0017QÕ\x0012Rð²°Jc0H\x001b¢ò)#È\x0019Iïº\x000f²
\x0003OI\x0005KÎ\x0000×å[HJiJ¡\x001aÃ§tf \x001bÂ}(ä\x0014(yâ\x0004Vi\x0014µÑ¬ \x0019i¸OU<5\x0019jH\x0012|\x001d°¤IÔ`Ypq\å\x0003\x001e\x0008xÄ\x001aL0A¿¡X2\x0012Ö]\x0007ö<ÊS<Z´z¸ùA¥Ç÷Õ\x001aµ er`pVaÂê4Ssó5Xý\x0002Pg¥7Xiù\x001a2;×yÜu¨MZ1\x001f<q^C{®kÁÏrÚÙKg¤\x001e°¬Ït1bUÖuË\x0016Ï\x0016Û6N´¨Á2o9D\¶Ñ\x0011Ü!F8D\x000eçÌ(äjEp
º÷Í"çÂG\x001awáe|Æ)*\x00197¨Î_óøNÅÂwF³Ï b\x0017KGÈ¿G«o²J/£Ê*\x0006\x000e$ú*¬è\x0014+Æ	ÅEë\x0018\x001bÛ®È\x0006K©\x0014k^'­èÝq"Ù-oLúÜÄ	-\x000b¶;ºÁÊËY­ü!¦C,:|\x0007¹o\x001f\x0013ieµ\x001eKGY\x0013åÇ¼\x0013ÑwFZIA¥õWèè}8ã;ÛÅ\x000ePú\x0008
Ü\x0005\x00157\x001eÆáZÖr\x0016\x0011XQËPb¹i\x000bh3eí=Ý÷BÏ%µîØ$±5®$s\x0004³Ì8éÙxK"Ý\x0017ß\x000e¡+\x001c|éEûÁJ/þôõ?~÷ýúé/ß½\x000fT"{f·UÝ£í2¦ÛÃÓ>üàO?{ñOüý§?\x000f	¯p\x001c\x0012&I\x001eÐì4e¶-²$#AÑ\x0015\x0014MÉé,%=@A6AE\x0003u\x001bQ8\x0005*^AÅ	PQ]\x0007)"°\x0019ß9ÚÆD*·ß)Pé
*M\x001dßùD.)b\x0018õøÀ@ÝÞÂ¦@å+¨<!).ûytgJ/µåw&-LaªWLu
\x0013©JÉ\x0004yS©®çéÆ¤3  8>\x0008SÇGz|@¶þ&Ûé/­r\x0000sÀ*);wÅë§\x0007\x0010`\x0011Ø:j
¶â¢SqGRìPñ¤²J*^$e|ÊN992Q¨´A¥Ýb\x001dã)#*\x001d%W«V\x001d¨<\x0013mr<\x00053DmuÍQü\x0005µ3¦ë\x000c\x001b¨CU&DÍ±!g²HdÕu}ç\x0000\x001dÂ\x000cöÉß5\x0007Ñ°SVZ÷Ät/\x000cA@q@KLS´+&«ûÖ)TÎÍÃ\x0019?¯\x000f!¯©/Ej²2½"Þ÷ôfxÝòj¶çj²êÄ°Áìè\x001dç|=­ýÆ\x001c#ÑHÂº¶£cv`v
6£âh\x00083½\x000fm/ë¨\x001cµã\x0004µÇ¨»Ô$N
ÊÆ&3á­vû
êË7_½ùáÇïß\x000fÊ1;Î0{±25\x001dMj§¨.Ê¾.)Çì8ÃìÉ¦Ä×³¸\µÊÜ½{Â}
cv`ös\x0004èJ¢P\x0015µªÈbËuTÙqÙõ\x0006Fìö&Ú\x0012Pº\x000fçAEÙiÙ©±!ª¡ËÊb@Äuç\x001c³Ó\\x0004ozÅUEVfoî\x000b:¦P9f§\x0019f¯ºr ÒÑ §7ÐÔ*l(;9
¥\x0019
Åg»tÖzÓu¬åýdõ³ \x001cÒsÜg\x000fÉS@Êw]¿?yM¡r\x0014J\x0013\x0014*¢R?TRiF¡)¬h=µ@­h­°ûV`#'\x00057XÒº¿@­h­µûÉ\x001b\x0013¿Ð-sHëlÅ­x­t'ôvf¦í÷­.S¨\x001c[ñ\x000c[©\x0013J6ÀETÝ\x00084Àzj\x001d+ð\x000c+tAI±&\x001bWé\x001a°æ¸çuZ`G\x000b<C\x000b½7³"Úæª\x0013×i\x001d-ð\x000c-mj)MP(Ö
rÀs\x000eN-*²Õ\x0001î 6¢­èî^¹{GiÚ\x0001ªýÏNDÅ¨s#ÿ\x0019=\x0013ö¸1§\x000eh+2l@1±aâ\x0004htV	´²ÍoºG\x0000_¢6Ïèø ÎðAÒiÒËat-e;½¿\x0013Ñü,&èa¾ðVÈ¼ e`Bæ\x001bjîØ Î°A¶MäE\x00054A©ÕÃûæº)HÎ\x0016Ç9[¬»KÉÚb)O"*á:I%Ç\x0007i\x000fªù-%á;AAÝ\x0008g£4C	dãÔ
ðÍ;\x0000\x0019V°\x000cÉ\x0011B!jcíe
EXý9\x0012#­_¾ä\x0008!Í\x0010B±¸¯@èI¨5ÇMV\x001bâä(!Íd^ÖöÊ¹®é¹ÛÂõý'øs©ä\x001fÿf(¡\x0018¥\x0017Ù+myFdUX§ôär/i&÷R-ûYú0¥¼ahs]Òë\x0002ÅfjJÇÅXhîp\x000bÜ×ó	É1h`P\x000e6³\¦Îö|B,ÝUX÷_²cÐ<Ã Å\x001ek\x000eY\x0019*¤.«u\x0007&;
Í3\x0014ZÌùÌõ\x0011>PåBv|gøÊÆ¯Q¶FÓv¬6NÐñUà+.öZSÂ£"^AÉë,\x001d_å	¾jÚÞÎJgéÉv\x0012u¬d\x001cà:*_­0ÁWÈ³\x0013¬½°#Y¦
òFð\x001d_å	¾bkü<dÕCR\x000b"`çq9;¾Ê3|õ\x000bêUq|U&øÁ¶lå´ÍYXÔDµáÈ\x0014|)\x0013É_R­#Ñ2A¢M­4ÈÍ8÷*&2\x0012\x001b	ìâH´LhC¥óÚ¤å3wÝHtÇ\x0015-®Ê\x000c]\x0015Õþ¬Åââ2+Êu=(\x0018Ê\x000c1àË3Ûcé\x0015_Ñ²²À\x001bÁiu7°ÎÜÀ`>_;µþ\x000eÿ8À·åê®`¸\x0011º²÷UÖí,¬v
.«»uæ\x0006öug\x0007(sÚ:ªõ\x001bXÝ
¬37¬8 7\x000fF¡FV7@¹\x000bX'.`\x0003e6°Oq\x0017PFìXÖ#ê.`¹ÖqMÒ~Ú«;Ñ\x0002®§÷À§`*?Ôö\x0002¨+Ì.u_Pãú\x0011\x0002¹\x0011gñc¦ù4ùXÌ½T¥·Ç\x0014Ö	¾ÒeZ%é°¾Q+­1EÐ\x0019íÎHoÊ\x0014A/4\x0019#8!´\x0018)¤Þ#%\x001dz\x0011ÃÆ\x0003\;¸\x0002Sà¸Úàî,\x001bïÙ$zÜ³®má\x001dm\x000bSØ0©á>Jµ-Î¸\x0014µo\x000eÔ;6ªs7¡_Sé(Ý~[¹LØx\x000e×¯Guûãçiée\x000e>H={+!È\x001b%\x0004åã,sÇù\x000bº÷!zî\x0013Ô!R­K\x0001\x001fk\x0016ÍRÙÈTV¾Ë¬ò¬Ì´P¥\x001dv«
¸nÐ7¸\x0003ß¹\x00038y\x0007úÈ^_qdU4;\x0015Gá:_ö8Ñ73w\x0000sï¦°úºÐ;<p#qþj¶ÿñ»ùË=\x001e¼c¢Ò¤ryq\x000b'¯yñ;Ðâ\x0010ßÓ$I»ãÿí§7_¿øàÍ_¿þæ·/~÷ö¿\x001e-`?¼ÿ8£F2\x000cñaÜímøÆkàþÛ\x001f_}øâW\x001føÑG¯_üîõçg+Øç?\x000f¯ y\x001ed\x0004\x000eÅ.Ó3A¦+È´\x0000²ô,¢þ"Z\x0012wy\x001fd¹,ó \x0013«»tLj&j÷1ë¥\x0012u\x0015$8\x0005¥ÒëÇyû
t©7ÓeN)aA+\x000bv\x000fJv\x0017 ±CÄ}N%aA'sÑüZ-\x0011R ßzé\\EùhL8((L£ÌÁ5`×»0+Z/Áâ2JOóJCodj 5×\\x001eUõÒÊ»\x000cÒé$Îëd\x0006è½\x0015eÍ\x001då>S¢SKWK±T¡£ÔØ£Xã± Û(É\x001d8-\x001c8óKs]«uCÖ\x0010»§SöI(iAç¢sC© 	\x001f ·1²\x0013$/\x0008²j«$66:5²fþ[ÍÓË\x0010½1o
Ù¸´2?{÷Î­ÂûvÝaóüa\x0017x8k
¥e\x000eñÝ}\x0015ct\x000b,A×½5ñeÑ\x0011Õ**¸/ÉäLN79µI²RGÉ 3#\x001eê°¯É]4qdäM×J²qÉ2ÉÜ2\x000eeß¥LîÄÓü\x001f\x001dMØc|ÌÐAæ}Ã¼s>uÞÕÚAf\x001b/k[èZÙ¹ÒyçiÞ=¯}èóò¬üfÿÒQî«ev'O_"\x0003\x000bâeÊÃ©2³£ÜWËì.O¾<%#UÏd]Öv\x0003&èW<ã\x0013dI\x000e%- dáÈ\x0003%\x0017j*ÒÌ\x0015ªû¤Ý\x0015ÏÓWü\x001f#KàGRJC²7+1Y¶¬vÐZé\x0002ý5 À¾Ï]ÚQ%*¿Ì
µ÷°Xõ\x001aÕúl±\x0011BfGÂ ¿\x000b·\x001fl\x000cÏW?½øìëÿxó·ïFÜË\x0013CÉ\x0017h¹ïõ\x0004>ü»?¾øìÃ?½úýë\x0007DW@4
HR :H©°-\x001aÊhscã-ë8'^ñÄa<fNõòç\x0002°ÇF7G¼½M\x0000ÊW@y\x0018Pâ\x0003PÎZ\x001dÂl>^Ä[ä\x0004 z\x0005TG\x0001¥h¥=!\x0007[-ÙVOG¸=µ\x0003\x0002¯ÓÃJr?³öÇª:dãø#,ãq*
Ã:ÝÄ¢O6Í	{YQñèrÃ\x0006(¬^2pJ
ÃZÉ:Ý%\x0014ÉÎ,Ü:ô&\x00109­aµÎÉ*CÌ6\x00146G[\x0001\x001f\x0003­^|pj
Ãz}îÉ:\x0011Ù áÜW`DIv¯\x0001B§Ö8¬Ö%öíÐu@KCTm[VåU5B§Ø8¬Ø¥\x0017!\x0007&zsß¶\×eä\x0014\x001b\x0015»Í_\x0008Ry¯U¸äe@N¯qX¯+Û\x000bw >p<\x0017cG.·é'\x0003b¨ÞâKçhÑw?ýx@úø»o|ññoþòýÛ\x0017_´\x001fÿ68X]m	G¨ÂQ
¼+«/ùù\x0007¸OÿøÅ\x0001ïãO?ùâÅÇ¯>úýg¯_|Ñ~üy x\x0005¿b t\x0005J¿b |\x0005Ê¿b ñ
4þ
½¶\x001fDG_ýÇÛogßo¿|Û¾úéû¯¿ûæ}Ñ\x0008ã/Ò1Y,\x000c¹O\x0007¾<á¿úÓëO·ßO>xÝ@¾úãg\x001f~úÑÏâ»\x000ckøÄõ\x0002xìémèY\x001f,e\x0015ðÉÍÅ¼\x000b\x001d<'ëdto\x000bIËfe­ª\x0005ËuÚì\x001aÂËT-9à0{ÂÍMÊ6Ò\x0018­ü\x000cJ¶Ù³å²w`\x0011at\x0008ã¬\x000cÛÑêpãÀú*¥ªzÈõ:äg
`t\x001cg\x000f¹\x0005Pç»Ú9æø Z\x0010JÕÄ&ÀKmt\x0003(õÌs\x00009jÅKCØ;x÷\x0007ÏB\x0008Ái¡|ÎB,ºÆÅ½I°\x001aÂ´\x000bðÆ3ÓDC)©KØdHV9×¢S;å\7¹\x0006.e\x000e*L³\x0010K²ÌhÃx(a·½	0yi\x0016 \x0003KûêyÊÙº~e\x0000©2ïB¬^\x000fë¬\x001e2C\x001f\x000eNhÍ¶Ç+ä	ñ:c	âe\x001fßIØÓRÑ\x0016æ²Ì>K"ø1í=æM72mT8?¤YªÚ\x000e¶éªAäÍûäý\x001aõl¸-zcÆÚ\S?è]ß\x0001£bblÎ\x0003\x0019ÄÞ\x001c\x0018-)Kw!ú\x001bÓ7:BÔ|K\x0018¬:6r¿Ñ|\x0017º\x00061{y\x001a">Y\x001f²uLX%vCÈ»·¥zU¬³ª(;JÔI\x0014Ô\x0002XÈTw½lòCÓ\x0013¨;â\x0018Ð\x001aR@HN"¡\x0013¢|N"ÌÑÖº6í³a	É4.Cf\x0016!F\x000fqÖm\x0016K=ÎI92tVÜ´-ä)¦)Gv\x001eY4ÐmV)¦lÄ}Ý3¹\x0004½§ÈÓ¢ôËè¦;ªÔG<Pw·qqØ[?¶~)kLZÊc\x0000\x0013\x001eBÜ$m&çÊÊç$¾µâªA¬½é<Ws  mê!³\x000bXäs\x0012bµIð
¢Õ	Éè\x0005ã\x001bàMJdUxþªÔÚC{y¯R5Ú"\x0010w¥\x0018ýAÇÙÎlW%5wG[jJ.ÅÝ«=Â<\x0010á*Du·e^\x0017â\x001eÂH>¶§Ùà^V9ëÒÖfmz|v×3SÒæ}>îÓq_® i<cý³
]çë\x0008È5^\x0011ã´"Ênµ|Çc\x0016y²Öý5EÜ>çäÏ9Ís	/Û.Ê=¶\x000fd\x0013ý=Ó÷¤cYTz\x001a=°\x000cNÍ= ]²ÞÓ^li\x0011}|0¶j¡-Î\x0016®Ù½'Õß:{O
÷µÐTTµ{6»Mò>vö±e¤îÊgì3®ú4MßZ6%¼g¦=\x001bHª¬Uï²¼ÉD70ó\x001bäs\x0012`®ZÉÙü×Ô7s°À²\x0019\x0005¤èî|NB¬ÜãÑÇJä,I·ÎNÉÅ)Ç\x000bÃä£Exiáh}ìO=ª»W¥øc.³Ç,+-¡
Iûmd¥mêÁÞf~©\x0014wUäóWf!økM»ËO¿Ì;%ö¯+í>5ö÷o~øñ»o_üîí7_~÷Ó÷ïy%\x000cIÅHé1¹!\x0014õ¾ÎªükÁï_}þÅ§¼øÝë>øôýçQ\x0005è
.Ñ\x0014¸æ¿¼\x000c:'ì
>rvÈ´íQ@,ØlÞ06\x001bÌ_â±ÂñÖ8Ómæî,¸êÀÕ9p-\x0006éó£õ\x0013\x001f=°'8¼õ\x0013O\x000e\\x0004ÇVCVÚÐÞÍ£YÑÝ*¶¦Ñ%.Í¡Ù\x0008*:-Þ"*Å¦nbÙ\qØÊ$6½\x0013\x001cÙ(-¹\x001b.o¡Ge ÏYx: \x0010Û\x000e\x0006Ï&>cØº\x0013\x0010ØÃ£:ya&½`Gû\x0018»q\x000fÝ£Ðë@g^Ãèr÷
É\x001aqe Â\x000b´w¶X<¼IÕkü\x001bílÁÚÂ­w\x001d!×=xÕÃ«sðN"9¥W_Æj¯Çv3BÞ;\rt\x000c4ÉÇÒ¦u¢=OQÑe;[¸mbEÇþÞòä½¥ÃM>m\x001aa¶ùñaóf<R\x0007<ÛJ0
\x000f³\x001cè)½>çzË\x0006BØw `Ò"~q±O¢#\x00003\x00192ür\x000b^ôð&­­¼löyfIi\x0005l\x0019Þ\x0007%Í¢K^xiRx\x0000º\x000e¤uU}\x0001¬6nõ²\x0017^\x0014^s@mNk
AËË\x0014õ-O\x0005ròè&]@6Bï\x0018ò®Â+6"\x001cjÝW<é9Òk§øõlCÖÆsÌ¹UÏ[Á±|N¡+ø2ØtnkÇ>2\x001cî\x0015è³èÈ\x001d-ÒÜÑbê[£rêï3fTH°u´ÈÎÜÊç\x0014¼ØWVä\x0018m.\x0016b\x001f"~o\x0017=¼8\x000b/È+Ò1\x001aÕ6;Ñ§»î\x00194L^õÒ¤ê5o *ºj\x00138 ÚN>à´'¼ä&'\x0015Z6Ã´1iÖÖ\x0006sÞç½ÎÂË^xyRxÕW2~C\x001dQ(Ü¥\x0007[(\x0016/½2)½æßÙTS°	¾Ò\nÂÛÂV½èêè~á\\x000f\x0005ëÏ)Éµ¨G×z\x001e¯§5Ô9\x0005÷Gà\x0018`AÖg'+-Ä:¯6d\x001b8\x001cJÞº\x0016ä\x0003 \x000c\x001a}Xwg\x000e¬C÷ú@òâ\x0016:rn\x001eÑd±>G±¹\x0002§\x001f\x0005hã\x0000 ìå£]è-sè¬\x000e°]\x000c{1h)F»\x0018iË\x0017 èü(s~TsZÍ\x0017Hí
,4Té=ÍK.z<FZN±J¶^¾VÎÃ
Õ\x0006ãlÓJò&\x000f7\x0015k~{ÊzÕR¡l¡cïò¤\x0017
²uOÑ5v.gÉZ`6Ó\x0016ì9g9¯? \x0017£eU±5*»ºu1Øç¤x2'\x0005\x0001lõVj§¬+9*¼¸EzÌþlyòl%&;Ñq_ò\x0011zä\x001d"m9*\¹Ï\x0019t¡\x00043·±\x0016¼±&ËÂoæ\x0005Ø»*<éª4»ªCO¤\x0008Vw\x000e4t6{:@Ú\x0012^\x0004ÿh\x0006sö,Ä¤T,6³ø¬=zsk­[×6¢ËZDËZHg~<Ó\x0016Rµz´²/Sááð¼3\x0010'\x0001éøV\x000f>&+ìâ\x0006íµ®eÏWT=¼9OJìhû~LV
Õ
\x001b¼°\x0015zÇÛ{ídº1<6ºÇ¦gõ@\x0004\x001dî}Gò4</½ÉÐ[¦\x0015\x0019­pTgå(ð:Ñ¥=/9±s¥äs\x0002]ª¹jäÍÕÞE±`Rp[¾@;ÊkÅ®
\x001eÖ¿¬UTíö²ìä=õ¯£¼ÎBu´÷cì\x00048\x0005øÙwyûýÏß|óöÛ¿|ÿÞAÕ\x00006Á¸Å\x0016h¹në/kÄ»\x0003}úû×½øüÕG¯?ùýggRµ\x0001Ã+0\x0001\x0016Z¡©Ð\x0016'v¡¥dÈÊmòþ,4¾Bã)h\x0012R(´\x0016Uå6\x0008(o\x0001KW`i\x000eX_×\x001dã\x001eôªæbJâg¡å+´<§gA|ás4PÒê
¬5ÌøxV®ÐÊ\x0014´æt"÷1JI5­è_a=ÚV¯ÐêÔÈ¢ì y±Csu ×Þ
àX#ÌÉ,é8úRµ¬Ô>vªÔ-\Í¦éÌæ+50º\x000bó(ZÒùJuër#4b4¹\x0002¨WÀ|\x0019¤=\äpÑ\x0014.FcÚ (ÏlD ­gk\x0015öÎÓ1-LQ­\\x00005O2\x0015ÞürñÆuôR-lÑasr²¦Fê\x0000k/³ÞO	ÉO¹Ñ\x0016Ù³\x00030e\x0008\x0000£õ+Õj£êÚéê@ÞF\x001cy:!9K ög%jMlÁ¦è\x00133îÉÍÑ-Ìñm\x0014´Q¼Jy¢^\x0005\x001b\x0017Ç¸g?Ñ1.Î1.?Ô ÙÐÐ&6èØÊBÇº8Çº±÷$U)\x0013³ÝR-mCïEÎ®h¨ÄY
rv[4Í\x0011/Î\x0011oä~Kl¸CvxÃØ\x001cïâ\x001cïJµBQKÛ@\x0002îÍñ.Îñn,Öä_¡wÐ\x0007}ç'ºpÌBs¼s¼+¯¿g§BW\x0011\x0013[2h{\x0014s^®LS=\x0016%hYNdhô»eHÑ±.Î±n)ÖR¢9à-±¡Í\ma#G»4G»\x0017Tl^ª!6RÝ\x000b[ò5¿pFU]ø/\x000e¬(Ýr\x000bíßô¤¿þùí?¾y\x001f¨ÔÂ\x0002{Ò§Ç\x0012Ä\­	ß©-ýø·¯¿øâÕÏÃÁ+\x001c\x001c¡?¥b±ù/Ù\x0012ã\x0000ï$wGÑÐ\x0015

¢ò\x001f-w\x0008Ë-ýUü\x001a¯Q4|EÃ£²É}Å´ìeÑ½KÁÆ|\x0003¾S4
'^áÄQ8VÑ¹o[éóVm\x0001÷\è(tE\x0006Ñ\x0014\x001b!ã\x0012úhñh¯ÜøÎCè(|EGÑß]Ê
^ÇóN]ê(rS\x0006áTì«\x001f¼ ?.ùýÁi\x0014N½Â©£ÒÉÚ%x¬ÚÖ±|ÅÞáþ²9æ'9\x00180JGþÖ^t¥¯Ô¥×¯\x0003½óÆ?ÇQ \x000cr Ti\ª¬´V¨p²Ó"ZÅãH\x0010\x0006Y0?zå¸´?Û&øÈq­Âq´\x0003¼±¾LºR;U+Ï,6.AÆ¬áqÄ\x0003ÌÓ\x001cÇÒl\x0013{ÔËÎÞi0\x0018Åã¨\x0007\x0006¹Gt¦j·H\x0008§R»E/ï¼aâqÜ\x0003ä!Û0eáBMZô0\x0014iÑl#\x001f\x0018d\x001fY&«ä­ä
Ð{ßy\x001dD|p|2¢ãB½\õÝüÎç(\x001eï\x000fö4^¶@¶¤Ò¹¬Çq\x000frd­Ï\x0004v*\x0018ÝOÖûOîÉØq8Î\x0003ÃA\x0017LÜ@PSz\x001e T4íáz>\x001fÅã¸\x0007G¹§y^`w«Øü·R¹®¸z\{p{\x0012ê,v\±ò°÷ûv\ïT|âqÜ£Ü#qTSèÜSl¹ïß(÷\x001eÅã¸\x0007G¹§\x0016+' Ý¥Yswá¯«S§ðc\x001f\x001ae\x001fI\x001e-í¹\x001aÀüÔ¶\0JÑh	½\x000eùèSù\x0014[-\x000fïVâqlH£l\x0018ñ¡?Y7~É¤|\x0016õ|<:HÍG¶zÏ\x0002ÊÎ|üÃT<\x001896¤Q6Y;´Ù0K
ÝM«A\x00059.¤Q.I'\x001f~aL§\x00079\x0017¹ÝÝâÑ»=ñ·?[m®)\x0015®\x001avvªÌ£ªl´ ¬©ë\x000bS{£)Ä²x\ì\x0019£ÊÓÎÈÚD<jÙmao\x0013ÏâÍb§=<ª=-&Íf¹@ó\x0007µwó½S\x00157
Æ-\x001e4[¥E\ùaF³	[ûÞÌè¢\x000b\x001f*ÇAU\x000eG]ÐrÈIgÕÓ¼\x0008Nã .K¹z=¥ÊË®Ò 9ùúÙQ8Nã *\x0017Ö«=}sséL3¯\x001eÓå8¨Ë{f®Æ¾l\x0006ä´h&ðVcw8Î\x0012»ÿ*ßð_¾¼Y÷/\x0007MFÑÉs\x0007'0Ûà
1¯Ð;â	I¥GÄ³%Á+=®ÛjÊ¿üÙIªüæÏXú×­\x0019³\x001e¦¦wÆ\x000cç¤îjwTRÒc:\x0015¡ç:(ôøgÕ#âà%Õ¬þ¨¤~©ÃkÞÜ ½\x0019$CºÌËGRµòvóòêÍ\x000b÷Ã£0®æò`gÁk´=ó\x0015bO¯¦b½¤G%,\x000fÜWLTä¨
b
õ.¦:®âåÑ\(ël6!õôëô\x0003]\x000ex«EnA»'\x001f}÷ã×?üðö¯2Wí7/\x000e\x0010ß}ýÃ{×¤Å\x0018ubbió\x0008k_Ã\x0003ØG~ñáç¿þXF«}ôêÅñã§\x001f~þ÷6¸)H¼Ä\x0015Iû¨\x0010ú[¶jL×{\x001d%]QÒ
ÊÚNõDÙ¬7,mÒ%Eº\x000e¯ y\x0001d#³\x000f\x0001Û+F[\x0012=ãÀã\x0015e\AYÎÖ/\x0004õxn6í¯ì(Ó\x001e2]Q¦\x0005\x0015_ª0Y{5bÀj\x0007ÎO\x0011f¾ÂÌ\x000b0ó1ÑX`³A2\x001e^é\x0011/\x0011õ:ÆrÅXV0\x0006\x001b}+Û~Ï$h;ñb¢D¢'À¬WuE/IgQbíöØ,Êt\x001d¶\x0012<§¯ºäIU1eÉ=Ýèêé­ãt´\x000eK¼Þ\x0017N\x0008c\x0006åuë hi}Â=\x0007Ç°Bd»±\x0011dºµj'ë\x000b\x0006ækãÓ:NÇG°BHÿ\x0010õt|\x0004+ô\x000fé(	V8	l0\x0019JÚ\x001eÍ\x0015ló`"~Â©_ªÅ9
¿Rq#%Z"¥\x0000Ìè¸¸âÅý¢0c¼¹íí\x0007+óûêí\x000f/>~óýÿûû\x001fÚO°?|ýÃo¾ýò½h\x001fåýTt\x0014sìÓ|êíñðw¯?ññ«Ï¾ø\x001f}Þþ|¢þüÃÏ¿xõÉ\x0007\x0003°ñ
\x001b7`7ÿ.ë\x001bQ3Pé\Êª¼zËóïÁ¦+lÚÝ¼\x0014-\x0013iÿ§Õ
6õi{\x0008¯°y\x0007vµ)|d!9Ø\x0007,Ò3u$]Q§
ÔR\x0000lcÓÍçÆÉ6\x000c÷ö¶°\x0007:_Aç\x001dQgË±\x001dãYeM}Ì+=\x0013v¹Â.;²®}\x0012"÷ìw¼\x0008ÅgÞÇz]÷TDG­\x0015)Ñ\x00046xU²ÀOý¨L<H;là®ÑòûiÏG'ç/Û\x001b\x001dk#UÊ$1k3\x0019G²ì\x001a"'âvÖ\x00066Ì
 Ûº\x001anÖªë;Ú\x001c||¦z37°ao0¤>ÙÉF2Óm¶Ñ\x001ehgl`ÃÚ`}Òu|(7ãcÈ:=\x0011wt¸ã\x0006nÈ½n¥p'\x0013CÍõ¨
+ÙB\x0013{\x0017å7º­%²=!g^Ig'aÃP¢TÜ*\x0005d[Ócìcxæt\x00126,%\x0002wíNU\x001b\x001bîh\x0006þ^)¼ÛYJØ0ÈÇ\x0017Á]ÑF.q\x0012þÄ]ð¸ÑJÜ0ØõD|+u\x0003íÍR\x0016>\x0011¶³¸a)\x001b]C%Í¦ªÞ)t:)·úÿ=Ü>.Û±XmñIy\x0018ÊÜ·\x0014py¦¸ÍÁ\x001d#q±IÑUÅê\x0012ð^\x0003¹ÛÙ\x001cÜ±9\x001a\x0004K¹
[\x0016î éº s\x001f´39¸cr(wó(¥o\x0015ºÏ½ÙÃí¨\x001bw¨»E6:\x0018ªTkbàXMÞà±\x0019:êÆ
ê\x0019ÿºï§Ö¤+\x00088U_ÚÜï'r	9ê¦\x001dêñ\x000e§¼k°\x0001\x0003{,Ò\x0013\x001dXr\x001cH;\x001c¨ö½"M8'hkÀ\x001cÈ$ä\x0018v\x00180&ÌV¡ç\x0001S¯ÃÀÌOä\x0012r\B;\zþ²b8\x001b¾9¡
ÆòL/\x001cÐ\x000e4×O\x000b:*&miaY¼a¸vew%yçJæhÃ\x000fk3Z¢¸'Lê\x0013o$»\x001bÉ;7²µÈTª¶yTÚ
ö3CJöy×KYû0Ç\x001aû»aJÖz@!?18NMâP\x000b*µV¸¦¤-\x0013ÍâX»\x001fá\x0013
NtNwÜpº9Î\x0003á \x000f\x000c§v¾S\x0001Û©wÜPoµGJ%hk7g±ÂDôL5qê\x001d7Ô-­VÏòÄ\x00037ZZM6ý<\x0011·3:qÃèÈJ'í\x0008ªµX>ë\x0014ÎæO=3Õ\x0013Ñ\x001bF¤<ê
¶\x0005sw\x0003Ó3I092I;d\x00124É\x0001\x001b³6pN`Zã\x0013oer·2íÜÊ´èCêî\x0004s±XX\x001exÛÝÊ´s+kÑnd\x000e2èw\x0001ë¿£úÄ(';qç
q3[o\x0013\x0007I=(ì¢Ë»ñOÂÙ;o»Å\x0006:\x0003eRm9Õ¤\x0006kezfT\x0019]±¶Úy+C^ãÂ¤v-jÈ`½toF\ÃÎñ6¾§ý`ÏðÿüöÍ·
ôÿùÞ0õ\x0011¤¶+©Fb°\x000c7ñÍ×þç×¯>i(G\x0010¥+¢4¨yÉ6Ä§´øEg*bÆ%»\x0005¶ã\x001eoÈÞ\x0018GT\x001f9\x0002°M{\x0011-\x0001ÖH8­B\x000eR\x001cÔ¼\x001a¤ri\x001f0G[Zs,\x0017]\x001d¤<\x000c©ýÅ:¯¶Êhp]:Ýë7èÆèãÐ!Â	D½K°f´Él©4Y½èQ°uÜ6\x0018FD¡ËHª°OMb\x0004Þ­®Bb§Ü<ªÜÍ¯I6ÜdÕÐA±ÈE\x0007CÉ\x0010¤²
É)7O(7µ¿X¥Tm\x001eÇÒsraUJÑ\x001d\\x001c?8YÚW»rë\x001c	®6>«)7-BJ¹Ó8u¾;¨>¶02u\x0017n£$& ±Äã¢ÔL6½»Åã1(;c­	Iÿ\x001bvDt¶PIå^´jM²c¥<ÌJí÷À®ÅÿçS¸Ìí\x001cPVU©+¤R!\x0015Û$+BÒ1~\x001câ¶n?Ö\x0015\x001eê0 )ªÃ.£ª\x000b½û\x0016JYz¿\x0008©ºëV¯ÛA
)¢·\x0016\x000fôx<¾O¹¿|óÕ\x001f~üþýÜ±ÕñcË\x0017\x0006ÐáõbA²Û-#3,$\x0008&ås\x0014Rê;8®\x0007WÂÃÀ­B*\x001eÒ¸ä©r}íæ]»\x0017\x001b\x001e%T\x0007"«¡\x001a@\x0014ûÐ\x001d¤þ$õV
Ò"s\x0003z\x0012m.É¨Ú­ÎÎ¤ú¹-Còþä¸ûÖôW[«äâÛjÁ&\x001cè$°èã\x00029^\x0002\x001a'&´Á
5¡õ.\x0013>¸;®½6ñ¸6a~xKI·5LÜýºJ\x0003É))IõN´QÃÉÖT¥¨=R$ós\x00171eOMy
ãg\x000e[^£ñ\x0000¬Fºí\x001fí!Û\x0014y|¶®¾±UêËvUL.ó8]¾B£\x0001°)\x0014Ø\x000b\x0010dñ\x001a&ôãYõ[æ·ë¾l6jÂºªKèi\x0000Çi@\x001eÙª4
\x000cè\x001bÆ1×E£ì\oäaß[
0tN¢@21\x0005~`ZdKôq\x001c\x0007r²ê<%ÅÄ¶\x0003\x0013¡4çUº\x0014gë)cjr²"¬¢\x0019E\x0011¥2,\x0006\x0004\x00184ò:7pöÚ\x0019;ºÞCRÂª:ù\x0000ÇC£\x0014SåÓKÒMæ½V-ÅP\x000e«\x0017S\x001d\x0017Sèïë%Y\x001dZ£íÞ´\x0012iUÃ«':N\x00042Ï²Á6[ÇK²r,Éû»4îïÊ²m=¸t¼ì\x001fl'M\x0017\x0015|²Æ³ÒÁVµ\x000e
oz¡érªÐÙ\x0014Âa\x0002-æÕñj%¢ì\x0002ìífT\x0017CLòN8;áP²\x0005\x00062Ø¶ÌcÛUq\x0015\x0013y9Ñ¸rW'æÇ~o\x001b|\x001d\x001d0È¿XÐ°×$Iú¢_¸oÓA\õ_ê1
Ç*Ò\x0005\x0018\x001fÍ:Ë\x0010 [_Ì«Dà\x0003\x0003\x001a\x000f\x000c E(ÖsAüÒv\x0007ã&\¥KþèâøÑµ8Î:SsßÐY©wÂåUmJ^Ji\Jòk¢9\x0004!§)­b*.%/£ØòqÒw
©ç\x0007m^è\x001aÕyHãÔÔb\x0001ëªMEºm=uK\x0017V\x001fS¨z1Õq1I
Ã\x0005-¸E@½cx5B>%Gã99À^+³zuFë)¯Z\x0015öï©ÇB­AHÐÛfe¼²F¾ÁV½¯\x001b\x0015\x000eÙC\x001a§K\x000c6æ9Ëê
Û\x0000×[ÔKZÅä/yüýR¶\x000fUá\x0019-X9¢{Å´úêÄè:Æá \x000e\x001e.o®Á\Þ#c¬â*&vy\x0014ù\x001cÄ\x00143m~\x001fié¬ÿìÃEW£\x0015NþÁ0
³S8Ç«c\x000e«:s-´(}åÅê\x000c»bÊÃ¡Awy[\x0014\x0010ôÉ\x0010k\x000fW .Ë©x*(ÃT\x0010bé3ãcÝ3w.«ô\ý½«Ã÷.ÄÐ·§È\x0012)\x0013A_ð\x0000rÁ|\x000e]°è·qU_\x0014ß\x0007@Zt¢ÏÅñ\x001cX³eæõfªZ©\x0015ú<h\x000e^oô1T\x001c¡ZàüÒömYÁ;V+\x001cå\x001aèc8\x001e\x001b\x0004I£*aB²+²¬ðÄËR¢â1
»\x0004AF\x001d)¤¢âX²5ã\x0002®Úßèóq<\x0019»ý
E¼Xl2eSðÕØ úØ Ç\x0006áQ<%ø=µ©9\x0002&§°KÉW}¤q['\x0003\x0012\x000fH2H÷LÌ5H`b
¸\x0005>^ÃñJªµ>µìCZbúÑÅà úç8þÜSkßí$©ªG\x0017­
9ÔÕ½]p ÃØ¶\x001dÈþ².'ìê´{=¦Qw®a)V*k¡\x0005\x0016îÛhÂê}ô±f\x001c5åÎ¶aÉÙEÕqJ³[Æäõi¸üãÀ¤bÊE{I\x001b¤¨\x001eA(iõè|ò9\x000e'ÓQ@¨b5§ù-h`\x001a¦UÆôÉç8|n±ÍNÍþé\x0014y©S\x0015oÿ¼EË£§c¢å ¤ÔY¯ì<)'&0Ë\x0012
.zsÉï¦áúÝ	,Ob\x0003R\x001f\x0017ÐE ¯ÝQc× = ¦h.\x001a¦bbÊ«,Ð×]ã¸Ç^yZ rß8\x0012ÒjqjòyÕ4Wmcn\x0018NL-88¡°Åç\x001aØ5\x001fhÑ\x0002'örâq95 Å0Ù|=Ì}Có\x0016é)qõÆ\x0019¤.O*(fír±Z°\x0016x¬R/MÃ5³I*d4ØLÍ\x0005Î`÷N!a^=ºèÙ)\x000e³S©½75\x001b£R
æºÄLÉS\x001a''ÖeæMªÙÜ\x0017:UÏ©1G4¬ß%-ýHRÅ{êw*Ý+«çV¼*qU¢hé\x0011ÖÉ\x0016aD¸zå¯u.ãÎ\x001c%{ò+w.Ùi'×-]ÄU
¯^Nu\NØÇ:Ææk~'Gë-\x000e°j}³O?çáôsC\x000fêÌÅbÉ^ÆÚ¿îâÑepbÊ0.¦¦CZ+\x0013sÕ÷hÌ¬Û§©ÅXÎ\FÇ\x0003\x0019y@f\x0015BîÎÜÙ¢m¥UàºÈ\x0004Ù¿Gçá÷è&§Ðå²6b´³ÓøZ<³è9e,\x001eÓh6%ÕÐ¬
+¦£þùÀútÐ0­VªfáÉÃ\x0019fV²y\x00042\x001dT@_}\x001a&\Õ§èè)Çaz*çd¬
Xg­`\x001e°À"gºÈã©\x000bz¥NosÛÌÁl\x0016°ªî;Æ1ù4A\x001eO\x0013\x0014C\x001dSRH:\x0007R ­Ü½?dØç\x00151©±k^%ÄLÃW»h²7ÈÃï\x0006Í%x\x001cðKó\x0008ñÀj\x0013Möï¬yøõ¨0VO.h©¹æ¯Ø#Ztåo~(ÃÍ\x000fMJ\x0007o\x000b&n`é\x0012®V\x0012\x0014ÿjP_
\x000e«&¦\x001egÊ8\\x0013Óª\x0013^|YÆãÌòXkÅ}"\x0014õ]­À,äX Ð8\x000b¤nè¸\x0008¦M\x001fÒ£[
Ç7*eÂ¨<Z\x000eùl\x0014sË
(¬Ö_\x0016ÿð[\x001f~\x001b h\x000f¬\x0003ª	Iç\x001bQ©qõà¢ãJù\x001cÖïdÙKnÔjê\)«çæ{ Ëp\x0013d*T-ÉËµ\x0005
¥àÂ ­Æ*Å÷>áÞ$ur ú-¥`ztöÆJå>xm\x001cSñÔTÆ©	«=\x001a0Aï\x0011\x0001SñÏîÖv8x:9-aªP«¤Æw\x0011S
Î	Ïa9%{ðá´.¥É©«8ÇE³R}q\x001d®1N²_V{28ÔÎ\x0001LÇïS\x0013Ç1ùÀ \x0007\x0006²/^}\x0014ªÝ»5>Ñj6\F\x0018\1ÑøÙN$c¯O\x001aÅv¶îeõA\x001d\x000f\x000c¤\x0006LËB¥[óì]Á5/'¥t«rò^x\x001d÷Â³4)&îïÑ1j«\x001fåe·úêÂ:\]²t×÷Nºþ´~'²\x0005¿²5t	\x0013\x0004ÿºr|\x000f"HçëÏ\x0001,^Éi±º\x001f.c¼OP0|óRsv5`iÿÑ©\x0016È¨ÕWW-\x001e\x0004ß\x000eu|JJ\\x0013\x0014Ê ÝÓËÒ	wâ¸FQ\x0010üËÁñ=
J\x0016lz\x000fìî6Q¦¼
*Þ$5N\x0008ò&\x0016M§zE\x0001h \x00169
\x001a{Lu\Ïc~YN\x0003gî÷\x0014\x0019½\x0016¡¯\x0019=¸
\x00008¾Uu\x000c,R/
PÉ0-\x001dà½|BNÅz¤¥=*B)¢´ztà'Ü\x001cßÃR\x0016räÅªIy³EU¼yï\x001eo>ä¤\x0019:i²É|×§ûFqP·\x0007\x00138\x0016\x000b^ ÛÚ\x0000VÝÛþÛi\x0015Tº\x001a\x000f_¤~Vç\@²VWIáb×=@öÃ	ä{X§ù,Ò¯Á]§LR°Ø@Ö|àAWÎ\x001cÇwÞ=iØÐØ³\x001dIjõ±\x0005 Ü$5Ü§qJJ1õ\x0000&Zo\x0014¥°Ø\x001b\x0005Po0þ*Sï\x0006ñ\x000fL¥*\x001a¨E³H7P\x0013¦¸Ofa\x0011®j h\x0011\x0014ÞÜ;pïbO×É\x0002iatz
ÅÕ\x000c\x000b +;¾g4ê4ÅG¬¸/ywqµ\x001a\x000bn\x0003\x0001`|"À!(R í-æHuAU?
o¶\x0018glqí$\x0015ÊK;».§¼j÷nå0ÞZÞ\x000eÌ\x000b\x000e¹'6Ãi W\x000f/Ý4j¸ª¶\x00051}RH«gIÈa\x0019ÓMPãE\x000fâÛiR:HA9wÊx7Ñ7\x001cßÃrêõ}¡¹)9é²/:|ª%P\x0014¼ÕïaPÝ\x0014\x0007ì\x0019×Hæ\x001fÄ°\x001aW\x0011øÓ#\x0018?½\x0002ÖÄÙ$®Mï
TV\x000bÃ«=pkñÎé#©¡¾y\x0008`RÑæ\x0017\x0011/Åä\x001f\x0015ï	P§Na-U§\x0005a_|Ga\x0015ÔÍ;\x001fïTN¹ÚZàZR\x0017T4=çåÈªi£Ç\x0014Çõ¼j\x000f.V©÷Uâ´Ud
Óâ+\x0015Ð8i8K°7ý\x0006ê&K±\x000b
\x0016YòMP\x0013/èM·Ó)Êp¬\x0013RWòÅÄÝÑÎtEÄÃÝ[I¶\x001e³Ì°b±ºXíµaÕca¼Â§\x0005z©B´\x001cY
É&bÕÅì4ð}rØø½+¡Ú\x0012öÒÔ]Õ)ë¢\x0015¢e/}Ñèñ=þ¢§ÂËþüÒ\x0001­FT|\x001beÆ\x0013³Ì²5m \x0014\x001dhÊ55PP	\x0017/Ý­·\x0014ÆKSéËO\x001a¨Ô\x001fô¤öé\x0004\x0015W'PJ×)èçGþóM	ÇL\x001d×\x0015AÔïs2Wç)`ü·W\2YåíùhFvw>.1\x0004)(ðd+¡9:Å çEd¥à\x001d¼Ï\x000e#K2Á Ôþºnáha{\x000e-ÎÂqÿó~ÿsø,8.G\x000bÌÖ4`ÃÏ!í¨ØWwX_ýW«¸çÿòæ\x001dýÍ¨'\x0013zúEû>ç\x0019²G\x0007®«}º"®7wq
Âú%\x001d5X_Þa}ù«õõ\x001dÖ×\x0013\x0003´ÿLt>ÛÐ#(]çWç¯4X¾Ãúó°´ú\x0003w®Ç\x0008¤SZÐ5íAäz¡G\x0015^ûá7ê>|þæëo<`½\x000fº4Í\x001aj;£LjÂCVÏ8D¿úð/\x000e\?\x000f	¯p\x001cRÕ~
Ì2ÏãD\x0014­,\x0010êßg\x0010Ñ\x0015\x0011"Ê5[\x001cd\x000cZQ!YR#Ø´\x000c¯x\H¶²º		l\x0011I:¢Ié6b\x0006RºBJãl:+Ê\x000b·®!¨LnQé\x000c¢rETÏ­q\x0013rV¯Úìáæ1ÜRû\x0013x\x001e­Çe\x000bãø¡HG]þÉô(ßæyÍ@ò÷\x0000\x0004ÇÙìÙ"¾¨¼(Û³?\x0004X¾ÿàî?\x000c\x0013@Ó$MVK5°
Eïá(Ü×Î@r·
¯dñLrÔÙp\x0015´ÅK¼Ïõs·
¯[N¡_·öG4XJ11Å²Ìàî\x001b_¸hCW0µ?ê4¯Rt-\ÃtkÏÀîÎáø¤ï1
\x0013Û\x000e\x0016¥GZ>;ô\x0016n\Ãcè<Ð>2LÔ1eöFgãpØÈ¥³Ûì \x0002SubÊE-P(°|í\x001e\x001dU\x0007¦8)>0¡éS.êÅÑQé¿);Ly0ÏZÎÉÚt¥º­\x001a¦°lçÐÝ;\x001c¾w©\x001c\x0003`\x000e}\x0002£§Ícº.¥ê\x0010ÕaD¹O´9ÒìÂí\x001f·,%rL@ÃL ó:²2¦$a³jS6v
iÙ# g~iÜüfK\x0019`lq.&k!K69-89r¢ar\x0012"\x0008ªà5Yèô w¦øÌ`ò\x000eø895FÒ0E:+Õ%È=ÿÎL\x0019LÎ' a \x0015Ò)Íøh\x001e¦ÞÞä´N\x0004ä\x0002\x001av
\x000eÉ0Ù8\x0011¹vêaºqí\x001caÒ8aÊ\x000c\x0011;»>(2÷å\x0016!¯*ä\x0008Æ	SÚsõÚµc\x000czvQWÊØßecG2i2ÓCÚ\x001fu¥LoFor¢å³cG<N)Úóg¼¾aânÓrxÀ2y2\x0013ê@M2¼R1±\x0015·T×19ÎäqÎLº%¡)ýµ²ÒPx0Ù\x0011&\x0013æñ7«¢"> Q÷RZÇäS\x0016ã\x0019k'\x0002Ù¦Dpq09Éã\x000e&RwS\x0008í1!UËØûöÔ\x0019LÃyÃÛß\¨Ûº¨nJ§ð¼®ÝÁyÁcÍBwRLr;!a\fKvlÉÃl\x0019\x000bXhÀÍKÑu²cR1ÁºUâ831wf\x0002´P3cwzqÝâ83AÔ9\x0019ÒöÒåT¬¢-ð²:EÇMqbL:¹\x0012YzO\x0005U+ÞeAÑúÑ9nãÜ\x0014¨§Á\x0010ÍÁLÉ¸6NÎñ@\x001cæ(Ãôäd\»\x001c[j®iÓúÑ9¿)\x000eûMQÕeª¦Ê¨²\x001d\x000bÐ\x0016\x0001%ç ¤a\x0007%6g@\x001d\x0014~dTS°,X¸×JÏ`rW.
_¹\x0018I'£Ë>\x001b1Ã§~k§®\x0014m­;îñ\\x0003{¡\x001eóÔím'¨\x000b%£Ò#à8oîJLÈË\x0011ýæ7\x001füÛÛ¿~ýí¯~zñ§¯ßþô¿^|ðoÿùÿ}ûþåïdEm ÛÎÕõ)Ãy\x0003å)èq\x001füÓë?üäÅïþøâO\x001f¾þãÑ¾?ù;OdðÑO!\x0008¥â×°8e\x001eaDsg¤Å¢à	±ª¡W\x0010ø\x0019ï]¾zB¤Ç;£@ÏI»Ëu,^;ÅXe«¤@~O\x0014¢Ç8-GÎV1Ñ0Z¨±\x0017VEÞ<j
Õc¿/P¬j¯ÑÌKæó¬£:\x001b2`ñçÎúç0>R¤\x0007FÉNÊ1ÎWÃRls+lýÜnô"F/G£¸ ½4\x000c5ìæúYcÚ=ëèïL¾3DGõêq¯å¤Ô£9gy&«\x0018?ë4Ö\,â\x0011\x000cgÏ\x0019÷¡Öídx÷^\x0017/Ç2Ï=üà\x001e ªlþ9ËSÐ\x0012DF\x0007Q>g!"\x0019õäBº­mÆ¢\x0016jmÙÑãQq<QæÜÔ#Ý«g"³í%¼v¤¬a|Ì\x000c?0ÊÌðY¤Mö(å\x001bç$\.æ«âµF~	b"wÔò9}«ÁüÄ£\x0016q\x001f\x001cJÇÄÆMä1Ò4FYwp²#Å¨W«ÍGX2ocÌ\x001eã4ó\x0008Æh\x0018Ý\x000ccÜ¼ÖÙ{\x0014yÞ£5ÁújÈ\x0014D¤\x0007FJ\x0016ó2lZ\x000c\x001e#ü\x001a1>\x001aÎ\x000eBes\x0018ñ|\x0006>s\x0007Y_Î9Ú6%¬é²õb	cyôz\x001dN¸´zMb<w_\x001c\x0018\x0019u\x001e?ËÀTÅx¬ÙÂ\x0008\x001eås\x001aãÑXlg
#\x001c\x00197ïuA\x0011\x00170V(,Cq5!\x0015yÓë)ìøQ>§ïLÔd]\x0019\x001d5ì:¸%yuL\x000bêhãf\x001aFÒ\x001c·¨£b,×\x001d{K\x0018«¿2uþÊ´8RFÎ\x001c\x0018©ô+CÚO%M¢3×ò9Q\x0006ær\x0004YU¨\x0001\x0005®®\x000bÊÖ0¢£Gù\ pMÉljWÆB);ÞÄèÍu]0×LV¬\x00022¯Õäh9ëªì5\\x001cDÕgÅÈ:W\x0000åöB$]\x000f {LvÅµÏYhóÛ\x0010¥\x0012A½GÁ%Ô]uÌþZçk´
\x001f\x001bÝHË±z\x0014Å0Òîµ.^\x001dË:\x0006yc;Ô\x0011«¼sê¨9
L9l\x0006\j\x0007Æº ÇbO(SE\x001eõÉ[\x0016Wì\x0019\x0008ÂïéT°'\x0014d|©éQ6
Ï\x0019÷îLÃTo\x0018\x0017ÌUßéeIÐH!ëkÔöîé#\ÊyO0Ïáfnæ°ÝÄ¨%´ãæµKaØ	QJÃf!&mcAlªirdcfØc,\x001ed'q~±åiHý\x001ekIÇ\x000ce÷Ò$ò Ó¼ÿI÷D7ö¦Æ))ùdä=c\x0008¡ÜN»ÌvSÃ \x0018#öÓNÚ¶ ©MABð§-ß\x000bÉ\x0014°«\x001d´¸¤Ì\x00062Ã¦$\x0001£\x0007\x000b/HÅ\x001eã¡Üó¸fkJØsÅ\x001b¨z\x00039Ï¬L\x0007¤Õöt,²
]l\x000e\x001aì\x0019D\x0000òÆF¾§%\x0019íe¡ýÏeçÕ)I4&i÷¸ã
d\x0007É¶\x0016\x0017ÌÔ4ÕtvO;ß0.¸hlSW0dk$kîO2ABÙ\x0015d¦\x001bÈylÈ´\x0000)H\x0008{ú?Ò	® w]\x000b¨%ùÙ·×ÞÛ\x00158uAV-!îªMè³Ç÷,ÈÒ'¢4Ó`)¾LQ\x0005y\x000c"Ù\x0003écØã{ú\h\x0004tN'j\x0004¤\x0015pÒv±\x000bÁäùl@éï4"IT\x000cdÂÍËé&Éùlé:,7´ÈÈâ¯l\x000f^\x0018\x0019wc\x001bùË=±òi2O:m\x0014	£VÒóa\x000cÏ0óf\x0016M`¾½Ã|;
3XÿÀÝæØ;\x0003§Ý¬@ùæ\x000eóÍ´s^­¥uvó{Í\x0013j0w\x0013,
æWw_M{ÅÒi"M+§I:Pò\x0019ÒLñZ,ey\x0016ùiÖF\x001eYü3E@ÚUÁ27É<¢¸)ÑöÿüÁ8î¿´syû÷sÿrúÜÙº{åÜÁÎR?÷ýTïcBÁüóJz­£\x000cz×SÈ\x001då\x0013ó_ï(ÿuúÌÙzµKd	ô¸DO8ó¯ï0¿^¸@Õ`Z±vV;sæÝ\x000bo\x0017(ÿº.PF¼Méhä¡å_½}ñÍ\x0017}÷å¿½}ñ·ßõÓ{\x0011B3zwª¼ÐÙ\x0002\x0006Û»D·Âéß½~ñÑ«\x0017}ÚÀ½øÃëÏ~÷Ç\x0001tEHÓ\x0008eÙ¯ÍKæ»1Z£\x001eÛÔ\x0015ñ
1ÎCÌ6=±YÊób7¨\x0003¼mH^\x0001¯\x0000ó4À]«2èdHË\x0000\x0012å²/ÂrEXæ\x0011ö\x000b©áÔç:f\x001bíOi\x001bb½B¬ó\x0010ûÄ\x001algihÓH(sÙ\x0008þ6Ï_çl\x001bÄ\x000fÊÞlôÃ¸-Fp÷\x0019æ/tì¾¹¬7%SFë¤\x001c·9ç2C0ò4F	sªp²\x0015
°ôp\x0018öÏÚ\x000eÌ³ÎcÎløe¥îÞÓä¸}«Áñ\x000eÌ\x0013LÅN<¨r,6z©1Ï¾>:æyê©½®¯ÈPsÕÇl#îÑ1\x000fÌS\x001d2\x001b\x0008ýZ×^õ\ö©ç2
¥a´i(3b*ÃcqÌ	°ôç¼m\x0003Ñq#ÎscµÍM\x0010w¬ÉÊm\x0008Ð
Dt\x0010ñ×'CÇÝ8ÏÝ5Ù8*Q×YÆ\x0010\x0003v_'oßgtÜóÜý\x000bÑ"Îb½f¼X\x000b|³ØGÇÆ}MtóSÉâá!GçN|\x001bE±Ü¦ù\x000b]l/cÃØkA¸<0n°b0}xÕ~°ðêõ¼yñÅ¿}÷×¿3±\x0005~º²C²R:\x000410j={\x000b§½Qyý§W/¾ø§O?\x001e@WD8m\x0004\x001aI¾Dgé\x0005¶\x0002ùZæ:®h\x0018Q [®@	msV­6à½Û(¦	D|EÄã2²\x0011$Yí
±Z¾­l@®Ò0¢\x0008ZTKÒÖ>ùìÐîá&\x0000+ 2\x000e(Û\x0014TIÁ½v
ñk¾\\x0018Gô\x0018x\µ0\x000c)Y\x0001wml]È6)´\x000cÉÝ5\x0018¿l2ÆëD$ä©$Q¡]V5\x001bfÃ¸jçd»¬éÜ\x001fr@êNn¹¯ÊäT\x001bÆu»Ø^ÖÐgn\x0007ÛZp\x001f
7\x0001Ç)6k¶ì\x0016¤~h:T(äÇ¡åUHè4\x001bÇ5[^Ò!kçìh¥\x0012n³r& y+2®Ù\x000f=Ê/U³Éú´¾5@N±q\±1jÓª\x0004Ú%q°#Z½ýè\x0014\x001bÇ\x0015\x001bª
à\x0017\x0019éT¸\x0016K? -KÉ)7+·5\x00154DÁyV[	 \x0004Ë¬í^ÄNæ¶ñ\x0001#ö$ÉÌê¼áaàúâÚi\© w\x00014­ÿæ7\x001fþõßßüðùøî\x001fßçX^&ØÊP1\x001buT@\x000bO\x0019dYÁúðã?¼úüss.ÿðéç_\x000cWpq\x0012\»v')d1wYÁiJ.Ü\x0012¸|\x0005eàê\x0015\\x0003«qleSSB¶	îñÒdº\x0002î½\x0015p½\x0012í¶Í=ã(TÑÁ]|Ï)p\x0001£ddÚb\x000f¶~xñÛ7?¾}óÓÿz\x001f.îÃi!_:°	VR0t\x000f\x0004?ñÛW_¼~õÇÿþóð	'055;ÞR©&KsT¤((¾Í\x0002EWP4\x000eI\x001b[\x000fAIªDTÜ\x0000ÅWP<\x000eª9ÇºÏ²¶\x0008ðÜª'Ûm\x0019Ì}ÂÎ\x0014¨x\x0005\x0015'$Åê×4IÑYÞ\x0004U» \x0008×1å+¦<)J­ô©\x000f¿F\x0008\x001dT¸'\x0013&@Õ+¨:¥çÎÓ«åeÉªçÕN/¿\x0019\x0007\x0005\x0010æ\x0018AWË¶8ÝþÚ\x0008Ï\x0014ë\x0006(§R0£SÅlvm>E\x0000=?2Q\x0011Ü_&P9¥	­j×¯D½~ÙÂ.¤
ßy\x001bÐ*¸º^'«ç5tõ¥Ò\x0015¢N\x0000i§¨}øLuI`L7cÃô!üí÷_¿ùö«÷C²©Ó-¦¨:\x001b Q\x0014öÕå]#øÛÏ>|õÉï~\x001e\x0012^!á8¤h	@lóo!Ù\x000bV\x000c\x0017ÕYHtDãmÈB\x001eÈ¡CZGÄWD<¨é¶íEz	º²§XrëßpG!Å+¤8\x000cIô«*É~bTêìk6Ë%´®Ò8¤ò2Fº¸U\)ÛhY6¤¯ò0$\x0019\x000b¬\x000f5KÁö4æ°~ßÊ\x0015Q\x0019G\x0014_ê\x0003<0\x001e·§Î\x0006©,CªWHu\x0018R\x0006KË\x001aÙ\\x0015R1íÎïÆ4\x001e9Ï'Ã0¤\x0012Ì1\x0008²"N}M2
à\Ö1yî\x001e'oÙÛeêÍú.{ºzÇå\x001b\x0007¼a½+kSO#&°w\x0018]N\x0015¹\x0012\x001c{Ã0},ÈÒ³ÃòRµ)Z¯Û¨f!9úaþ&\x0016\x0019\x0007\x0006©t\x0002¸~çÜ\x0006ÄÓôÊ\x000f£¦.kIw3u¨Ó0d9m*¿n\x000e6,wdq\x0006Y\x0016\x0006Y¡F¸&ã©ò72\x001d£Èà\x000c¦dò0Ê,Ë¼Óc±	ëñ5öXîÈh
Ù/ç¸¤;°4\x0003,\x0005K´KðgÔ\x0015lb\x001f_Þk¦=ª;0\x0001Æ6ñà¯¤gÙ\x0017pÅy1Þöûµ\x001fÄGõ\x001fo¿ÕÿÏoßüû_ÿðãÛ\x0017\x001f|óÿç¯o¿ýñ}\x0008s¨öl"3u\n±QYÔ\x0000>d÷êO¯?±\x001d¿}õ/>üü×/>øèõÇ¯?ùâçñâ\x0015/®âm¨Î\x0006&âvê\x001a¼öµ½%çgÁ¥+\ZÛ|W]\x0000+Ò£7R5ñ^úâ÷ðò\x0015/¯âÅ¢ÝÄ¥úÀ¢É÷Zÿwñ¾wl¬áW¼q\x0019¯µ;Hp©\x0005
¯FÁM¾½Y{òMW¼i\x0015o*Z<K\x001c­=ã¼dª¿ø,ý-W¼e\x0015ï¹ÐêÄ\x000b¶æ\x000e¿JºÔîÁ­W¸u\x0015nö+¨:Ð»«Ý*\²Ý[x\x001fÿÁ¾aY¾l¹8Y\x0010­&µM|,ê\x0000;úeþÍåìjx;ý¶¨Ü\x0014â:k\x000f¯ã3X&42¬
Ü|\x0016\x001d½^ÙvèxixÝ\x0003ì\x0008\x0002\x0019¢o\x0004m\x000cÜ÷\x0014W¶ÄGáË\x0016Ç=ÀÙ\x0001Îeñì\x00196²¬ =]­½\§%ïáu\x0006ËVlQ\x00130Û®Ê½âyÐÄý,`Çi°Jj
P/"«½Þ4<H\x0018ê$ÔpÔJÑ\x0002Ù&á`±UåÚU8<ÉÈ¡óqÕ	.2ùÀ$\x001c%Éwêp÷*!?$Ð;ÁË,\¡KXr5jc'	â'
tn0®úÁÇpm­\x0013éS6[­(À³TØ¹¸êW\x0016H\x00167u5¿§ä^Ûä÷ ³\x001a¸l5jÖuRÙÝ·¶ÛD&*O\x000bãÐY
\¶\x001a$%LZ8T5ËÁ2\x001bÆJcã\x001c	tf\x0003WÍF	Øë\x000b¥\x0013Eírê5X\x0010d6Ð
\6\x001bµZ¶F¦.¡'Í;Ïô$J#g4hÕh´+õÒ.\x001cÙÓaÍõrµ{xÍ e!ó¦¢\x0016äg\x001b&'ãnT¾×.=ÀÎfÐªÍh\x001cÛë¡ë¥¨Ï2Éäó&Ë\x0006#E«
Gi\x0004:\x001bC´&TñI\x0016\ AËFÍ½=¡¶V5~^Æ^\x0014z3q´lâRôÅ6*DÛt\x0007ØÙ8ZµqbÁÊ©£Î·\x0012\x0016kï¨áI\x000cLÎÆÑ²ÅÄ'`I\x0004+\x0003\x0018Ñ$ü¬H£e\x001bÔM T\x0012®]Â9=)FÎÆÑ²KÕ\x0012ÿR¾\x0017JØHâIN%;\x0013ÇË&®Åó .\x000c\x0002T'UK§ü$NcgãxÙÆå`ÙUl\x0003x\x0015pÊO°³\x001a¼l52Ú{1J&[9-Y¶'¥'ÙdöÙöU£Q\x001a*}\x001fÂ\x001alssQÌh >)Î`g4xÙhdÖ\x0006b) °÷ÇêSÀ1?K#Ñàe£!Ó±O¿\x00123i/@p17->hü,`g4xÙhäh/\x0004(Åµ¦Â±KøY\x001aál\x0006/ÛfÁZ\x0006\x001aGX
RÓ'¹\x0011ìl\x0006/Û\¬"\x0010*¿,j3®Nkÿíg½\x0011Dg6â²ÙHðR\x0005,\x0015JÂ=_öd\x0014ÕëVãH[u\x0019X×\x0007O2rÑÅEq9.JEçJH
´Ð
ýöXmõ\x001cÀÎÈÅU#WCoNØ§A°G.7Wv\x000f°³rqÙÊýÃ\x0014Ø¿)¯GF½
FTµÊòô}
8>+öÎÈÅe#×TXó×2j&ñ=Ãg½\x0010Dgäâzd:XB¹HØªN"=É(GgäâºcNG±©°%ÿR¨Ï²\x0019ÎÈÅõÀ(ÒM±ÇÔ	\x0002Ã|ä,FZ¶\x0018µ\x001a\x0005¦\x0019\x0016gØð¸\x0008Ï
;/âXw*µHê\x0004ÈÔ7YÜù¬@®8\x001bWmÜ?Ì\x000bz9ç¦ýæÏ«\x0006AG\x0011G»r$\x0013ª­R\x0006¤Ä¾\x0005ZË9äå\x000eÍR1×þ\x001eNÁZìSzn\x0004|\x000c8=KêÞ¬\x0016%DrgM¶¥
æ\x0001\x0012\x0005\x001fc¢OíøjUÊÕ
e/i¶ú\x0003]'\x0011r¨wí¨ëÊQBÑ¹ÑÔnM\x0016©Ùª\x000bÆgå\ßM;¸sÒý¾$ºÕ0¤ÔsÅð<
yã5äÿ\x000fJý¥üåªRu\x0016\x0008uT0ê°GÜô¬P\x001aªr;½E1\x0017*ö@2\N}
(}XF~Ò»]ä»FGÞÐhÙ\x0015{*tS\x0014]Ä\x0012\x001eQj}VUXõö°IzÑ 
whöX¸C\x001b>k¶;XðY5\x001f\x0004ïp\x0007ìpGx©OÒ²J\x0016ô|KN»á\x001fÐ­Â\ö\x0007¹é\x001füÛûÍ7ïÞ öDçååÖAPÁ\x001c|åoÍôûà^ýáõG\x001fýé
\x0006¯Ðx
<sbsÊÖ+V¥óX¡ñß·;\x000e-]¡¥\x0019hEZU\x0014¬\x0005·÷¢¾S=¿5Nr\x001cZ¾BËSÐ\x0002ÛZè{?yíYvë÷ +´2\x0005MÞ~¢J-¼T_<è\x0012céqý[£\x0019ÇÕ+²:\x000c¬]«E	\x000f;ÙUÄ¿96y\x0018Ú£hZ A\x001aÙ\x000cÝTsOÛØÅ\x0016¶®Á£mòÀ\x0006SØ0ÛÊ¬Ô}Ò¯¨1ØÁæ
¦­4í4ÐMnÉÖàµ«¥\x000eÊß\x001c\x001e?\x001c6ãhË*2°NoüÑ/i[W\x0001\x001cëÂ\x0014í\x0016Øã(Sz}O1±¿5v\x001cc]£Ý\x0014¬ë;ål¦\x0002Z5¥\x000cÃ[Âê­³¬ý eøæÍ}²ëþÿéÏß|ýÿþô~|¥75\x0014ÐâIîãa ^Ò½øèÕ\x0007}°ëë?üñ·\x001f}øßþÞXWCW8°q%JÐ¡H\x000cØ\x0007][W!ò\x0015"ÏC\x0004ÛyÖ ¥HÁx
ãåYb\x0015c¼bK\x0007­1Vû/ô"Îª}Fä¼1]1¦\x00059F{-"dÅ\x0008¤ü×Ôñ\x0012\x0007®bÌWyMEåXla°º\x001bFzÂ)WeI\x001fu@¸	º\x0015»éc59^V1Ö+Æº ÇØ¯u"u¹OImr¼Ô«,b|ø0\x00079%A*FÛ\x0013ßcÝ>kð\x0004¾ÂàQnÊ)È¤
\x0011Mºã£	ò	 \x001dÃ\x0002ó¾\x0018½Ú>èQVnn#$ÖÄ¨÷º\x0019jêbÔqÈe{ÀÙ\x0019X14Q_g\x000bue´\x000b\x0003\x0000n\x0015 32°be¢.Ö$!JÎw)Æ¸\x000fÒY\x0019X33*E\x0006m<½Üj´ÑY\x0019X13\x001dc}<ºV\x001bîiÿN;#\x0003+V&ëNÃ£0¯µ N<ýkí¬\x000c¬ôÒ¸G\x001aò4£ÕÇúµaÛ}DgfpÅÌÄ$³ö«Fv"ìtv\x0006WìÌ?@>VX±3üÒl!kë\x0008²ÛÂ´íø ³4¸fitÆU
Ç\x0015ºÝík;Õ*HgipÅÒ°u-J¡®®±\x00032}úºÑ\x0019\x001b\36*GÀ^:Q«E4×°\x0015£³5¸bkØÞ\¤±Ë1±áºk±Á5c£ý0\x0015ÌdWSÇ²\x001f, £q\£qUÇ*Y;«£³±xÝL¹\x0008Ü¡;C6¾¨C\x0007å¬}2m§\x0001È)$­($\x0007~JuJñ"¯¹ÙUÎµ \x0015×\x0002uÿc\x0003\x0008\x0005J]'Ë6ý°³Ú¼bµÑ¬v¥¾\x0000²´ÉØ÷3\x0001npÚù\x001f~É\x001f;T5¬ÑúBd\x001d\x0016÷@,vÓ³íVr¸cå°õP\x00015A±òvãU®Ç¤æU¬\x0018n\x0019Þö
ÿÝ×_½ýþ»¿S¤GúÈA\x0018Á\x0016ù¾S3Û\x0006ªß}ø»×}úwm
\x000c]ÁÐ üR÷ÏHk]`éi`îGÁÄ+8\x0006FòÝõQL `rµ\x001a\x0017Áä+<\x0004FRÛÉJuÐJU¡ïJ×Ñ¢S`Ê\x0015L\x0019<¦^ª-,Vß¹ß;:Vi/©W0uP2Å¸U
\x0011t\x00010@è\x0008±,y¤\x0004Û\x0014\x0006Ñ@ï¡¢ch¤=;5Ñ¿ÛcûØ@«[3¨qØÑÜ_~GÑ CÃ:¬-:ÆbWi 04k\x0017
\x001cÕÀ\x0018×ÔÇtUé_`=)|è
¬a\x0007\x0007E\x001f¢áÇTÚ\x000fê¶uo\x0018#>\x0018c¾c_ºÕöÀKYt/\x0019Åâx\x000f\x0006\x000f/½Õì\x0013Í/Né¾éd\x0014ã\x001a\x0018$\x001bLÒs¢I\x000fØ*=Sº\x0004\x000c¢Aw¡pðBÉv\x000ck*ÄÞ2Àx8ºÆ](\x001c¼PÜ§ôl,w\x0011ÍB§Â8¨Ââ»>ZõY+UkNJ×À$\x0007&Id'>Ü ½Så5Ãi/\x000ejoNº\x0000Qd¢ï(Í){B!ghÐ6Iòo»ãõT\x0017GÏq]\x0013
¹«DW©oÿ=®z\x0011ØøS¼×¼¢ñnðàU*U§æ\x0008Sy\x0011»d¸®\x001109_Æ½*»Ö´m®>b×Ü=O*k>Z}\x0006	¶(åç0Q´2_ýYK÷?añv×;$¬Ã~¡Ëåãú3|\x0019\x0014ÒK\x001b¶Óç<\r¯Ãú9HTnu:í\x0007«ÈýýÛï¾ÿËÛ\x0017¿nvAÁS\x001eÅ\x0006çLlÅ/·\x001dE¿ýég¿ýâó¿;8Û@Ñ\x0015\x0014jçVm2g»w@B¶\x001c/§
P|\x0005ÅÃjÿ6J\x0000ÍxØ$½Ø*ßÌÆ\x0014¦xÅ\x0014Ç\x0005U²6¹\x0011jbÏYÊ\x0014ïuPé
*\x000bªÅjç¥6X\x0013©\x0004Øk¾n¼=\x0005*_Aå	I±Íÿ(\x0014DåOI±å$¥\x0005{\x0019T¹*ãzL\x0001ãÓ \x001dKß³¸¥çõ
ªKJ´Û\x000f^®ç%/czÄïÉâ÷ÿjzÄñ\x0007* >òø\x0018Z¨¢Ê¦j\\x0007ån\x001f_?"K1OPEK}Yü¦^Î¸!*wý`øþµã	ý<d¦±êhÝ6dåî\x001f_@ÙlÕW¡è0Ï&+{=k²Jë¨Ü\x0005á\x001bØden:Ý^i×6L¼	Ý\x0005Äñ\x000bØb\x0000{ö.¡ªÿËT\x001eÇ·ÎTèî\x001fNÜ?¦®ê\x0010?	úéÅ
I9ß\x0005\x0012¢ÚË®xË\x0010A/'Î¸Ê9/8î½È|Ú\x000bÅéäÏ©ógZ¿~èH\x0001ÇIAFhè,Ý\x0006Ð2è\x0011zÁ0¬3\x0015:NÀ	N¨l69?
#ÆGÉú\x0006*Ç	8Î	Ig¿7Ý\x00129-èìµ¬\x001bDE\x0014h\x0014°19=Ú\x000f´¨±\x0005\x000f]ÕÓº¨ÈE4ô+	iÈ]@\x001a¿¿,*ç,Ð¸³ q±\x0019@i\x0011Ò\x0013Ìde©×y\x001c/Ð8/4_Åv¡f¡í
R5kSSYGå® _Ay aUÒÞ3EÛ%X'vvwgîà/¨WìâR\x001e\x000eLÛ©=\x0006C#ø\x0004]¯ ­G\x0011ìô'ô*hDÉ \x001d ºgPë:(§V<¡V)õÒõØ;\x0000\x0012æ^Ý±áZEçZÅq×JVy¿®{âdZ¸ÁìÑ¹VqÜµÂ\x0002½S+\x0015+.IÜk/i#>\x00073¡ëµÏÏ\x001aÚ¤\x0004vT×u=:]\x0013º.-¨J\x0014òTíø®U8Ó¦ÇqM§ð8>i/8©*åÔ«)óúñ%§éi\Ó)ô©ErüÊ
%Y!|uVHNÕÓ¸ª·p¡\x001bæZ¬<?`%¼)¬\x001bäT=«ºÌßÏÚçó\x0000mÇhÃ´mLNÑÓ¸¢\x0013%K\x0016KýÎE\x001dÒV·¹áÂ$§ëiB×[hª\x0006PËõí!S×õ\x0002ë¬®ç	]ÍrVô\x0018¬~*s¯Î+y\x0017²Óõ<¡ë±§û¥\x0014S{9ö\x0006º\x0011ÇûbAu®ì±æ¿Ú¿"¼#\x0001\x0007¥èX£ÅQ"<Zn×/$ò\x001d\x001bò\x0014¶{\x000f\x0002\x0004sâ¹\ÇFï\x001c*M\x001eê/\x0011¸\x001c}É§Ìúëã-~xñÛï¿ûéÇ7ÿû÷ J\x0019ûó;pV÷\x0006[4f¥p\x001fðùß~öé\x001f¿xõ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹\®Kèº\x000b:\x0004o)àt*¯b\x0000FDæ9^¢±knJè¦\x000bºOÌ Eâq9Ç&\x0017c¸Fè®îz c'2mÇGÓ»ÖÃÎoîKè¾ëÔÑFE"úP´\x0013îzÈD\x001fKñQ#ôXB}\x0017Æ3mà\¡Á¾SB®j­mÈò<ê{Ù\x0007]Päá¤sTã\x0006ì±ãBôØ+å(»´£wóC"\x001adæ°Kæ±µKüjÐ+
#»TÇµàLò)IÐFÇì¤rir±\x0011»­°Û>\x001dcÉ¤:\x001c\x000bt\x000cç^Äbú³\x0011{¥cd\x0001z¸2y?ªSLÚ\x000cwf,öJÉÈN-c¨µÀ	o	Ñ9.£¥ÊO\x001btUi\x0019Õ¥eð¥F\x001eÔÌ«îòv:±èG6b¯ü\x0018ÕåÈx\x0008Ái}\x0010Mªå·\x0008Wj(ôê¥ª¾ª
ªDrç¸'ÂºÀ}Àfi2¢\x0011{õRUßK×q#å\x001aÑ C$\x001bxÒ`^½õ¥\x0016\x0005é­~ßéCzºñ^"mRz¬|ß¦hÁïöÀïºÀkfý\x0016^Sr\x001dÀó6\x0001¡{­\x000ep
ßu¡÷QðÔt\x0012ó×\x0013zÃI)\x0007éxcö\x001a\x001aNþe\x0002\x000b¾½ùñ\x000e÷ Ýîp\x001d}Ãt²ÕÔ"\x000c\x000e<)-µbâu97÷qúöÝ$\x0002.Cúöôõ9îD:;Âõôs+zÍ\x001e\x000b\x0006£Æ£ÀÍ¤ x£Db¨¿Ð3\x0011U4ºF\x000fú8Óõ`Î$\x000féËìxª92å.iL)\x0019$\x0013ÈL®çnt1_µ¹Òp8¶\x0014Ç\x000e\x0012G¹C2×È7ª@áIõú\x0019»Ñ%+¥q£®À×Ä±\\x0003¿i
ô\
¼K\x001c_ã\x0007#%Q\x0008ÿ­ÐBN_ÇgÆ\x0016+_J­R0ê®±\x0005âHâê\x0013\x0003!+^êÛÄR8F\x0018\x000cx»\x0014N[ayw½ÝÙ#ÎSsª!ºÇ1wM\x001c:JËàT³â»Æâ¼\x0005µC0È#ÀÅ1ìÖÈ?19ìëê§ò\x0008ä \x0000¯\x001b½Izÿ¶ù¹jl×ã©zæÏ¿\x0018cK]^ÞúèU?ó=7I\x0005Èöª·Ø°òôÚýü\x000bN~¼¾ÿ¼Þa3öÐÛÔÇ¤ý¡ã>S¦ÇqznI\x0014\x000brüæèí;¬¼>¹ø°,*EPÝ"xÁ\x0004?\x001e\x0017w\x0010Ó\x0005§Â18\x0018..%ÐÝ\x0012èHë¬á#ð::ø\x0008¹¡SÍ¥M6`K\x0011ì{È¤§{dY¯ÑW¾V\x0002iö^\x0002¦lË\x0002âñÃýÍ_ùU¯¯ªÈÔxÚJrZLÐWvUEÐãËÓç\x0007½,.¥Ð#¤`Â	§qQ\x0006sónC½r°Q\x000cSa\x0006a
\x000fs`¨¡ÝA§|VÐ!´\x000báJ!Üoá¸Â¨]@Enü-ÔªqñF1B)F\x0018 ôyæ*\x0008êóâ,PYk\x0016«¶KQ&PÝ\x0000Ad~áÁa\x0005u\x0012D2ë+ZÃZ$	û*¢º½\x0005I\x001e\x000fÞ=\út³>é\x0006b*ü*Ëæv+ÎyÙ\x0016Þ³3áêàÝåÉû÷\x0017§³)»°ßä\x0010¨Éa;ö<º§àCXÖ¯Ô'ã¥[ Z[
^½\x0014
uëñàw»yx%y¿\x0006\x0016
|rc½õ<g;¥ÎþÞÕÁï./ç%\x0019¹).äYe¦EÚ\x0013lÜLä&k£\x0015¸Áå­¯:ü\x0002¯úñO×?ßÜ\x001d\x001c\x0003æëÏ
L>RqSÞ!¥Q"GkÖñîÏàGùöôüà\x00180|xÿD6ÏØ\x0007­KÐz;h#¨Nmqm)\x0005¢V0}ÙìõVÌ®Äì6cv«^\x00162%lâ¥rvn¿\x0015´/Aûí E@'y:híÈÅ±à\x0014P³\x000csä\x0014­ C	:l\x0006\x001d¤¢	(
4\x0016\x0010c¤>S¡æ"­VÐ±\x0004\x001d7\x0006ý@«Éá\x001aOäóiÌÄ\x0005ZQ ò\x000fòPÛ\x001al»sé¨\x0005»À`\BºÔ6Î¶\x0018­E­öËBÊsíík\x0000«è~ÙpCZ4
¤ZÃ\x0017Ãk\x0016«\x0012xß5lG£þE\x001fx\x0011|ÄNä®¯\x0019
^\x000fÜÀû6}:Ï'®¬Ë>\x0003÷ç(¼ãÛ\x0012xß¢Ï\x0010±Qzº*Ø>\ò(i}\x000cö_6ì@\\x0004îJà}{>E.ôÔþGÞ\x0017dK¿bµÉzÔ¾DÝ·ãÓ\x0007¦CÀ¢  {\x0012s/T\1©¿\x001ex,÷mö¹'¤Äó	'\x001e9;\x001eVÌï¬\x0006þàWõ>§M\x0017EqZ_IqÈñÈN\x001cxUd­Äû´8.P§Ü°\x0016Øþ7=M§3\x001bâ4Òjà\x0012ZÜ\x0011\x001fÏÔßJ­8Qò\x0012x©Z ë
yß¢iKW\x001c|,@ò¹\x0017Ú¯X³\x001eve|dõñ.WâÉîxt¬\x000eåPäõ}æÇ\x001bÞÖ(=duÜ¬Ø\x0013±\x001exe}d§ùÜÂ­BÖãÞr]ºiuð"ðÊ\x0000É>\x000bd\x000cÎ¸òÓK°l:Å\x001a®õÈ+\x000b$ûLÖ4Þå\x0004øXny±½¥e©ê\x0012rU Õg m(XõwtY\x000cO\x0018#Åí@à	R=&ÈGÅ+ä ¬|Ê´)¦)mÙy¼»\x000e#ú,\x0010¸(dpÑ\x000fïQÅ®aêk\x001biF^Y Õg it\x0008é-Ï\x0004\x0019Øè¯á\x0018Z¼2BªÏ\x0008)KôõN\x0018¤é®<(¬`íY¼2BªÏ\x0008IÃ¯\x0010Ñ\x0013ß\x0010¹à37+xCÖ#¯¬ê³B2ï\x001cLT\x0006Àm^Î°Ãn=ðÊ
©>+$\x000cï\x000c4:ÁV+8|ÖÃ\x000e\x0015ì®½ÞàÃ¢Ýá×ICAX_çHäñT]Æ3Ä\fBK¦i®\x001bé\\x0014kjokëÊxê>ã)£ÃB6Hð\}´~àëÔõÔ]Ö3 \x001bJJ/\x0007¤n¤3gBxG\x0007\x0002¯Ì§î3Bb¡<Í(ª\x0018ô\x0006èÈõÒ¤\\x0013òÊ\x0008é.#×Üù\x0004§+ækNyæ¸ØËß¼RåºK 6ehn\x001a÷éò\x0003\x001dhøu¥\x0014uR\x000c.RÒÖF\x0011(óLº\x0010Ânµ¸MuËM×-ÇsZf\x0005÷T@üÃ«It¿^ßÝÇÛ?ýòûÕwÿóÏ×\x000f×»G@(EÂ)	çÛÝÍÃõ¿}ºüôo÷?ßÜÞþ
±â\x0004ÿ´¥Þ!7©ÀÞ4
^bÊcá»àé{szvtzyrðþâêýÁåÅÛÓ³³ßõîâíÛË£«g
¯\x0015N8Tµ\x0011§\x0008\x0008\x001câ\x001a7\x001ch\x0004ªHÅ)\x0003f¿è·é*\x0011êôm$éØ.\x0007\x000b²Á\x001fÁSU©ó\x001f<W¼@ã°jÄª·cM¨U£ç úD¬-4E¿F?VXÍf¬`3Kçª§õP	l`°¦\x001bûÁZ\x0004k7õè\x0010\x000f6Ht&°1¸\x0018ë·À!X·Y
\x00081õ\x001d¡\x001aÀtMz@K\x0002«ÃÐçå\x0011¬ß|²! }\x0016`uÒ\x001dº\x0004UZ \x001a9òX\x0003"
ÛïDöÓ	ªrHÝî@ê\x0002¬ªÈö\x00086n¾\x0003ØÌ¯Òë
\x0011ý´é`­Qta£ï\x0006û÷¿ýpû§@\x0006w2³gØÝ¾ûÔ4àny=\x0019-\x0013|Äõ\x0002ÔâyDj\x0015(ØÛz\x001díGÏ5³Ëï~±æþO?\x0016V\x000b½	ÖÁÑÝçû»ë¦£\x0005Í51\x0015à=\x0000+«Òó41\x000f\x0002Å%ÅnAúÛGç\x001f.NÏkê« Ã\x000bó_\x0012ô?Åë?#tt¦ñçìþîÇÇë_®\x001f>·¡FÈt¥MëáÐ]P8i3¹\x000bJ\x0017
¿}C.Î__¼;¹üPø`Ïâ
\x0010âÏF¼\x0016wèHîÆÞÉ½Q)þG÷Æ.rwù|ÑuÆÍx
nÏE¸
TE²m`:$Ã-\x0007O\x0007\x001c/Î}âÏr¼\x001e[ñ\x0002ï¾\x0018ÈÁ#d¸\x0013}q»ò\x0004Yá¼;Aö\x0019òi^\x0003ùï?ýò\x001f\x000fEàCÚ7Ó@È]\x0013bÝ5	±Ñ
Y\x0000±Äí`¢´K÷Âµo¦çÚO+ÐOöd+hðØ}Òm\x0000\x0014ÿ8Öt1ä¢\x0013Ü\x0019¢\x000bÝ9\x0018Nåt5Âòt5hG\x001a\
_°;
\x0002
Îé;h$·¡Æm#6\x001d´NZ-Fíá¶¹>ÌÁ\x001dÊtÎ]}ìÒ\x0010s\x000bv¯\x00193ºÛ²óFÿÓA\x000b5^ÂK,v\x0014mÔ é`©Õ\x0007EMQ¼=ÀÿðËÍ\x001fïÐm¨A§¿ýÏþ×Å/¯?7yÎpSC\x0007xÎÎh:j\x000boÒ$ÏY¨EÏùàâÝçßäwßßùÛ;Shº7»!\x0012Þ$Æáµp­'8\x000eÀ\x0001ÓOú9\x0018J&û¹p3Þ\x001c½x\x0004ÏøíéóÜÃ\x0015ì¤7¾8ØIuôÀÆhÚL¨qD/Nñ_°Rº³6,Ä\x001bPÃm\x000b_\x001cjì\x001bÄ.Øà,)pãàKH¸U ;b£\x\x001bp£Ã${q§]\x0013nsÍé¼½gÜnÁoÀiÃÎ7	Ñß4\x001d\x0012a¢kLçh`Mô",8§Í¸e:ïÎ\x0003\x0007\x000f<hC^5(\x0013JÒGããÙ\x0000\x001c­ìUÞÁO\x0011¸Sd\x001dñ©û\x0001n0£oÄ.Íé/½W%ÕDÔÄ\x0011åùªJqQV)S\x001f¥ì¾ãÒsÌ\x0008§KùqxuJP\x000b¡Á\x0006à%Ç¿ôx+$æ±¤Ä\x0015{Ú^ÖpÖß}üûî3é®(½½tä¤\x000e\x001bþ\x0005 ï\x0012ô]ß\x0003\x0005g0Åd8vlÓ57Á³å4Å¬ñ(è"A\x0017½Ð}b5DÝ¢<[Ïi\x0000)Eµ\x0010¸¯Åþó§?j÷iÊX"Ç¯ï\x0006t)bØýåúáþö¶)O³S%2Zk^C\x001f<èÔ(\x000bÔ¨+óõÅ[ø)r8úöäòâììù|I)@
zL¢éÃB$\x001f¦»o\x000c\x000e@¤`ÂëÔÍae(\x001bóú\x0005¹s×ê/÷¯KÃwHóúaw÷C{!\x0001\x0007
(\x001cBÖo3=\x0001¤sHBW³ éi\x0016\x000fr^_\x001e=_Vx\x0012\x0001Ç\x0018=@\x00086jÚÌ\x0012\x00148½\x00133\x0013ÊÀëç-^²\x0005ÿ`£\x000cØ
øÕôþ\x000fa£=¤\x000eÖ:=	fi,èVûbß\x0001Í\x0000|ï\x0007|
\x0001\x000fBL	#+THIg¨kÒ*íêþ\x001dRì&)v#.\x0014v|¦ûÍ\x0002îD|\x001a\x001dR|¤ø8@i³Kß\x0002?')¬\x0013ô-XÊ¶IñøçOöñSÎ\x0012 \x0019ÈÄâÕdàL°k{ÇS¡i¥\x0015òú©µÏ\x0001É@&\x0006¯5ÈSÂæËC.qäfúK'vk
5îh¤ÃI\x0016
Ü
Mð±î%àc?ôÝð\x000e\x0014¸hi"\x0006_3ÊOWàBä\x00179ýäÔ¹Rýlü\x0000aZp5}\x0000Â\x000cÅ$@~Á­k\x0010 ØþúSÓ"¨\x0002üÁ^w»Ï\x000f×mÖ\x000b\x0017óÆ<:9-;Ì
<:\x0015\x0017"]ìGxwôáêòY½\x0012¯\x0015_}?\x001bñF=±ÐM~[Ôì]5ü6?\x0016-hCüÙ\x0016\x0019çÒé\x001aï±\x000b\x0017á\x0006!È_\x000en)Äj=]¼Î\x0016CÍq[^ò+­8½2AVN8¥Þ¯5ÿðóÝ\x001fÿúKasJâÈ\x000fæúñ¶±±Æ©Cü0$yÉ\x000f3Ä6`%x÷\x000bW£dü\x0000¿9¹:[%@ª0ö\x000bà\x0013\x000f.
|fÔ\x0019$4\x001d<hÃ\x0017\x0012\x0000|";B\x0010¦Ý¬¨J°ERk¢/àåRDÒ$À~øáæ³-¾ÀÖâ.e(ëâ.×ï\x0016»Kõ/óé/æç\x001bb\x001e@¾\x0001¬~ÀA?´¿¼\x0006¤É@ÂÁ\x001a
nôÉº@<»¤ø\x000eNàh/¯~iqíÔäÌbÀ?ßìþÖV£ \x0019¤×ÜéI£\x0006àÇ¥Þ¥o~?S¡SæÏüóT\x00055`CðçÉh¿½Ä[{püxÛf\x0001}Ä Óµ\x0005ø1+­UÁâÀR:æÉn¿½¸Â[{p|uö¼²þÃßõ\x001fþ\h¾³ÝÁî¾nMaÀM}L\x0006c\x001dp« éµY³¤.ÀËøðæâ-2¿=ÛÇT¢<%´,[\x0001+nþ¸Ò ÿ\x0004"Ö"Í\x0003â`\x001aÛ
ÄÏÆd÷·w»°Ké:0\x0007¯î\x001f?þ´kºÌ`ô\x0012¥\x001e¶\x000fjE'¬áBp·®ò\x000bIÆ3\x001c¸:~sôáÙY\x0008g´ñ?J-Æù¬6åûI\x001b
æ¶¦ê¸äÇsUÏ<<Jb=ÇÊTaMµÏmX}Dâ+I\x0002dÄETbá`ÀNÅñ©äXh«ÑZL\x000fÍ\x001a6kn©"Þ\x0016;¡ãf´
ÐÆÖ@mÛVG\x0013KQl\x0013ZL÷âÏV´ÖO3éèóDOIL«M\x001aÂë;\x0016-ÜYµùÞ\x00064\x000f\x001di~r1£ÎhR}mhá\x0016¨í7\x0001\x001dbñôÊR'\x0007:Är­;Ö\x0016\x001f\x0001þlEëÓ"¢E*û@gjóVë%G¬	-*Ûí:A\x00073-¯ÐN\x001b¢'WW>]È3¶ï¤M\x0007Øi""\x0015m0WÜrÍ\x0011þb7n\x001bX\x001c6Åýò5"o\x000c¼[ò\x0011¼ð\x000bÑg\x0013X¾Ývõåà8e7&µ³Ú`ÙA´<Ò4 ·8þlE+-µv\x0019$\x00001T©P¬\x0010 Ô\x001cùÄpêßmW_\x0016È\x0015­Ác*tR°·(ÃÈ7É9¿ýl-¨/Ç\x0011û.iðÆzp\x0011ÔÀ{+16ýe«J0ª=F\x001cL\x001a'ØÙþ{û§¿üù?bÙ\x001a¼¡AÁÉ!\x0015ËüÚÑ©ÂYKê\x001f²..4W¤\x0002ù
É¡Ý\x0000Ñ:î\x000eGâ\x0011Î[;{ø\x0016\Ù\x0008¢mýz©$qË²ç~=O\x001dìÆ.u3­\x0006É]c[Z®Ü´gê\x0015ó8z>¥Ï]°ÜxºðVcä\x0006±mýÜÏ\x0006¡Ôé E¤7r\x0010Hn\x0006k\x0007é±}Êæ\x0016°À
Sã\x0017·-<îÕ ¹ñkKÿ¡Ñ<Ü_\x001bìÌ\x001d¤ r×WÃ\x0011+µÝ{5^/U¤æA~ÿÓuªL\x0004]:¸|üøÓõíîsc/FÐú\x0004a1¶Æ½²\x000bRnÍPéåÕñ³£gi+Èi>³\x0003²O<0h0e ä´`gD;·pº­-¦¹m\x0007f0Ab¢F0;Ü#8F´Öy©ïy\x001dæ?]üxW9]\x001f|{=%åÿÚÃòÂR:@\x0000~âÈÀ¹6fÉ\x000bNÔÙÉÁ·'S*þßÅk¤\x000e¢*fo(\x0000#½¨IåÓ0ñ½¥çF­e\x00024ØJ%Ó\x0015 ¹dÝ\x000eÒ\x000b\x0005Ó\x0012|ÿ\x0001\x0008¼¶\x001d0¡\x000b¤\x0010±\D~\x0007\x0005\x001f\x000fÞ]¾ù|ðöúÓÝMSÛâ,\x0007µìk\x0015IC(pøy
»KÇ}®\x000eÞ|8ýpðöäýùéó9î,*ÅP\x0003Ä@\x0016 \x001a·R\x0016Ù£&1$¥d£°K\x001düÄÐ¥\x0018z\x0018Øá\x0010¨ê¤ÿ4¬\x0011Æ/èMbR\x000c3F\x000cêdÕC4\x0010Csñ,,un\x0012ÃbØ\x0001b@aèkÀ\x001fIb¸ÈR,õ\x0012oÂR¸\x0001RxÍ\x0014aâ;¤\x0008'>åqÚ$/Åð#ÄH_Ó@¥¡Oa÷L\x001e¨\3"Ü*F(Å\x0008\x0003Ä\x0008J\x001cÒ\x0008\x001a&§õÉ8[)\x0016|M2ÄR8âSx²È\x0012\x0017z\x0005ÒRÜ§^\x0011h\x000fXîÙò~1¢PÄ\x000f$6é]Heùc,åì7IQÛï\x0011\x0006<p\x001c\(C©FG\x0005¥ZJæo\x0012£²ßr\x0001x6é]8Åì\x001bÒ\x001a\x001e;öK\x000eÔ&9*\x0003.\x0007XpdLÁ¡4àXºTÆ2Á\x001aîV)*û-\x0007\x0018ðhlþ\x001ap¿èc\x0004Î\x0014(±T4Þ$Fe¿å\x0000\x0003\x001eâi=ì²ô5<§ed\\x001dÛ$GeÁå\x0000\x0013\x001eÓ\x0016¹ùG(ê@VHÄGßC£2ár
GÂèTË\x00039\x001cUÇ"ô©Kÿ\x0005\\x0011YÙp9ÀÇ Ù\x0017±g\x0012"r}lX/ñÌ+;.\x0007\x0018ò\x0018Ì´;\x000fåR« \x0007\x0007J/µtnCU\°äà×²\x001cFR»Ân"Ã,¥\x00086ÉQÙr5ÀãèV4{åid\x0008äÈïãE¬Ë\x001bÛTVf\x0010ùâ´´Á6û»»!\x000e¯¿áð¾¨Ç+L-\x0019!uüR´#¾Y³\x000bñ%r=Rÿê~é1÷KÌ\x0019øÉ·Ü¢+Ëí\x000f\x0003Äqn/\x0003\x0007a\x001b×4Ëu}\x0000Ò4f¬\x0004:$XL\x0010\x0007¡ÓrL,¶äL\x0013\'\x0007 Ä2h[¶A#Y-\x0003)\x001f3«\x0011Qí\x0000h¹Tçj\x0001íKÐ~;hSØ9!ØÐÄâÌ\\x000bâP"\x000eÛ\x0011«imùØÅ\x0014kÄ4*ðo_pZ0Ç\x0012sÜYÛiëú9ÓÎ3°B;è"\x0019P|\x0011']\x0004Í\x0008Z}\x0011 §îîJáí6k<\ LV\x00143\x00152=ÅÈ^³X¢cnRxÑ\x001eþbëÕ§\x0003ÇÞ3OdnZ\x001aá[\x0005=è=\x0003\x0013tÁ\x0005ùn÷pÓØ2\x0017#1\x0018Ð|Tð·Îs3µk¢­wG§ÏÛdÜªÄ­:pK\póK³7S«\x0014µ¬\x001b?\x0014¸.ë/çÀMÛô\x001c8²v4g=¥S\x00070VÅ³«»\x0012¸ë\x0000®,\x0004âé¢@üJ­«®r 
¶/aû{"-¹QX|ÆÅ+S3«åi(ëvT´\x0001\x000f%ðÐ\x0001\x001c»Ûµ¢\x0003W4 a
v¤§\x0003×cox,Ç\x0013ÏéeR¾³/ñ.\x000bç\x0004\x0015¸è9o¸ß©vg¤³86·W¬P¢^S\¼6=_íí=ÆG\x0007Þs\x0002GNª[âmXUX
»Òà²G\x001bA3^Ö§¢µ [\x0018õªRÖjÔ¶Bm;P;e§mH\x0008\x001cT\x000bµÉ£,	¸^Õî°\x001axewdá1Áó%*pGêÄø¬À\x0002¯,ì1=ÎiO6vÏ?
V\x0005M\x001ajêeezdí±Z1¯|¢ùõÌD\x0004\x0017U\x001fÃjäí=Æ\x0007 O{ì§3\x0017<põ4IlÕ\x0012÷b\x0013rUÙ\x001fÕc ÔÌZ\«|æ.æ{.GÞ\x0016UÙ\x001fÕc\x0000"&\x0008|«IÇì\x001aNÌ\x0003×ÁO\x0001rRð\x0008\x0004õèx\x0005\x0002e¶K\x0003mÈ«èGõ?^Ä|Ï¥\x0015a6ZÍ·eq2§
ye=UõóÅËfæ\x0005¤éÌC@7r¤>W\x0005U=\x0016Ô+IÉM8sMLº6¿O¹
jÃ]\x0019PÕa@£>eT\x000cX7nLwÒ27viP²
xe@U\x0001õFÒB\x0010\x001clyôü<åÊõ\x001a+W\x0006Tu\x0018Ð¨à Ñ	<O¦Hr9­b¬\x0018zæ\x0001U=\x0006Ôû\x0015ÏÈEö¶ÄÐ|®ì§î°Xx¦~^\x0003ÿ2b¶p.äknæéÚWöS÷ØO\x000f>¦\x0007
§\x001f\x0012A°9%´®kt5òÊ~ê\x000eû\x0019\x0013<Þ.£Â\x001aø·L\f\x0016\x000bkmÈëìá>ÔùÔ\x001dæ3ª¨iDo2B1q¯\x0019qµkÊ¬\x0004^YOÝa=á}jÊgipS'eº+ÞR\x0000
¿\x001d\x0019ïëÊ~ê\x001eûïX\x001dqäh½aú8mýÐ;^OÝa>£
DN¤#\´iÁyÍWÜh9Ò¹Õ
Ò]\x0019ÄnB«nÊIéb­Ï\x0006üÞa¢9ÏYäÎa\x001f\x001a"\x0015ý\x0000¦S\x0000e$üá0\x0015òáÐ\x0005+\x0019¿DºÔ
ý\x0015~ÙÿzÔ¯Î_õÿ?Ïb¯(ÅS9q\x001b\x0005¡6ïRÖ`\x0019zbÊ
\x0013Tþ*E¿~0\x000b`J\x0001L¯\x0000¨ï	¿¥Û\x000fVew«\x0014~\x000b~Wâw}ø0ñ;Z\x0016p?¬«c´À\x000f%üÐ	_öd\x0012Q\UÂìi'/ÿºun
\x0002\x0014e¤é½\x0012 ?.\x0015ÕÄ\x0019ûTã\x0015\º\x000bbþi zÂ²ó
\x0007é"ñ(Oß $8\x0007ßð\x0012u»\x0004Õ\x001b8È\x0010rùÔ\x0006ÒBVY®w8¿ÔGÒ.Aõeï3VRÐè×ô
,qK>©Ñuë\x0016\x0001ªw,{\x001f²R¬\x0004e,Ò¦æ\x001b´Ê\x0007j¯ªW¬z_1`¥.»ÌØ8.À³\x0004v]á©EÚ\x0010÷¾b-}~\x00038T®\x0010Ü&ùb¯XU¯Xõ¾b
KnO²Ôwl­bF:gÜèG ªW¬z_1n¶!.H¥4\x000f¦þ\x0013ûfxÚ%¨±ê}ÆF	v¦\x0015\x00186EÑ3lÍÌºüqCQyÔSñäPoö+à.\x00156Í_!^î5ìÉ*t\x000b¢¬cÆ»I@ÌÏ7Ò2ÀÔ\x0011\x0002üGµäc+\x0010¼kN#/Fê\x0012rÚ²§â\x0012\x0011q±`åÎeQ\x0010]
¢û\x0005	8Ø\x0006ít\x0000Ï5ís	×µZb.Ø&)å0#äðyù\x0007Ò\x0018ÄÖÒF\x0016¤aûP ®\x0014Ä\x0010\x0004àFú Ar\x0005CyÊIk½Þ&/åðCä`¢3\x001d£1m\x001b\x0000õ"AÉ6AB)H\x0018!ÖÔ©dÄ!\x001eµoz'\x0012KAâ\x0008A¦rp³<	\x0012y-\x0007hàø"²ú"rÈ'q#T¬	ó'¼ÂÅàÇ\x0019/µ¥$H\x0004ÖmGd^¢c\x0004\x001f7\x0015DÀDÎr/
ÚmäiVdÙ}±Â\x0008ùÝ÷Õ\x0015«·Ùm¼b)?@
;Îaª ùÕëÕ»VÉNc=ÒìiPøæöþá¦ÍÏL46\x0011´\x0012Á´\x0006É u-µÒéÙÅåé2tUBW]ÐÁ\x0013	ìë:ü´ç\x000c¾[ÚÁ×\Èõ\x0017uè¦nú\x000eýi&:î&Ó¹ÜËU\x001d|ë¡Û\x0012ºí\x001eb^\x001b$$O)¿ãÒÀX#tWBw}Ðsëpõ\x0019\x000bóÀU)ë¡\x0012zè.¹\x0015N\x001bO\x001e\x001e@÷ù®¯j)[
½HsORô\x001e;e\x0005ðÆH¾ìyeÏè\x001bS\x0017	'Ý^N¶\x0001FíK z%ðÛoPáëÈZ³cëFV\x0016%ø>MzÊ¬æ_¥Q`ø¿»¹þx}°{üëÁëÝíu£ô©N\x000eúGq"C2a»0fZüÝéÉñÉÁÑÕ¿\x001f¼>:;)é\\x0015!ûmY]\x0014¸·=7\x0010\x0019Ú%nAÅ%Ý)À«^\x00088%ÅÌUûNN,ëOßÿíó?þ¿Æ­PÎ\x001ef=.å¸ßÛUåN¸D'ï_ýþÃÉåÜÜ-áW%~Õ_=/ëq	@*6äÅ%Î­|\x0008
2èR\x0006Ý/~R¨Nð\x001e\x000b=±$\x0019âJ­A\x0006SÊ`úeù\x001eÁ\²
¼¥É¯ê×m\x0013Á"Ø~\x0011àa\x0006ð!Ô*\x0017Ø\x000b«²Ým2¸R\x0006×-1oËòÚ2A\x0006eXÉ=Ó /Eðý"¼§nrHiC\x0006\x0003v/Ö\x0012\x001a5È\x0010J\x0019B¿\x000c¸DP¹\x0002­x¨Gïz\x0008SÁ\x0016J	l­\x0013Ü¯\x001evkÜDKj\x0012«=¨"¦cpÆ¦Õ\x001ap§äR+C\x0011Å¿º<úýÌ>ZÔ©ûÖmbe8º½ýÇ§ÉñõÃÍ§ëÆgGcÚº\x0013ÉY}Ä\x0013KÕGgg'©fr|ryúþôär\x001cªC\x0003\x0002@3ÊÂðL¸öyvF/úmCrè\x0001r \x000b\x0013ÍuàÊ1ª¬K\x001eE]1Ø$)¥0#¤\x0000WCó.§Lå`r\x0008dÅç´I\x000e[ÊaGÈ\x0001n¸{ÚIeI\x000edþ 9mÃr¸\x0011r ¥\x001fM#8ÅÛ§1ïÂr,eO7ÉáK9ü\x00089ÎÉy§oM\x001e§\x0014K\x0003rÄ\x0008¥\x0018a\x0018pòÜÇ\x0007í×1Ï@-9åä¥\x001cqÈµÒy"ÊzvÌ-ç±M\j&Þ"FªIÄ\x0016ýßÃó\x001a\x0003§Ä9aïÎ3i\x000bÞù&Ajc>ÂëhÙ½\x0015VS¥ÚBÁSGq©¸IÊË\x0011æÜ\x0016%^ð\x0010¯\x000fÜ'jòÅä¨¬¹\x001caÎ'Jwr¯\x0006H1r©\x0007\ái A#,:î\x001634¢Ä+Aà#9¾XbÉÙÝ$GeÐå\x0008nÀl0ó\x0004æÄ Nñ\x0002b³4¿±IÊ Ë\x0011\x0016ÝKE\x0017KGÅ£Ë6ZÇË¼[HÑn\x0012¤2r-ôðBÒÔ\x001e\x0008Âû6\x0006î§Öþ%lº¬l¡\x001ca\x000cÑx\x001a*sÓÄ;Î´!wÅxATe
Õ\x0008kè-'\x0018tÊF\x000eþ¸<í\x0008 ·½º\x0006gÍF?\x0015§~ýT^ÂÛ
\x0005eåä7î\x0006Ü1Ë\x001aBåñ9Y9Ì\x0012×p£$ûÛ¾Ä´í+çM\x000enw\x0007¯°\x0005¢9ESP£\x0003ÈÀ¿Viæ¼ÉÁÙÑÁ+ìXA2¨\x00012\x0004já0`\x000390Ñå9%²«-BèR\x0008=@\x0008Ï\x0003ÓÚñ:\x0008a¹6°¸gw\x0010¶\x0014Â\x000eù\x0012:ùó,/~	®U%Öý-BøR\x0008ÿ¥	\x0011ÌÞ»\x000eJe··×$Ä»Ý§O×\x000føÆÌO _3\x0016Ä\x0012$k½@I$ïÞ¿?¹Ä_,£JqÔ\x0018q°O\x00019R×Þr²]®ØM±M\x001c]£\x0007}\x001dÉóZó&kdäcìr\x0005g4¦Æ\x000cú8>\x0012ý
æ[DÅã\x0011¾0¶\x0014Æºi!7ëxCÍòSÖ\x000bS/õi\)\x001b%Ìeg\x00159­='NýÒ\x0008ÃfiB)M\x0018%M¦ÎÃoãY\x000b\x0014\x001fgyRi£\x0016¨\x0007èQ\x0013PgL¿2\x0010Ì\x001e©eÌ¹T¦ëôz\x0005µN£Lvß´y{,v|
îðý]c£\x000c8Ný3©W:XIÄþ¯Á\x0015¾8óí¾'ióÒØÍèq^.VàuV\x000bW£Ðë\x0012½îGO$d:æb\x0012O­kôàÛ\x0012¾í½:\x001e\x001dwvº(Ç\x0008î¯ËN×hø¾ï¿\x001cøÂï\x0007þWk¿Ùýíús[4[\x000c(9\x001a\x001c\x000fúÈ9\¥M@ß\x001cýþäÃ²\x0010º\x0014b×b»\x0010Îdò`d 5úDeÿÄx!l)ÄþÂ
BDC+¿¦\x0002\x00081	GÍÓ+Iù\x001að¥\x0010ûýÚðÜb5MÐ.§ÚµnY¿¶RXÊ°¿\x000c¯] %
°jìûtÄ1\x0018¸¹G\x0015S«\x0010eEÍõ«¥¶\x001b¤Àà°Ôö	ß\x0007»µYÊMo\x0011¢VNýÚ)h§>ÁuiâHJNS©°ê©Q
UI±¿Òv\x0014Fåab%ùBIÍ¯Bµ¬º\)©dØ_\x0004Û.CT\x0012àrÛ<îi¸D\x0017P±eÍÆÿzê\x0006)¬ÍÃ·Â\x0010»¯È¶rk[@[¤\x0008\x0014û[G7H\x0011*\x0000¾<Tfº9¿ùÐaR|/ô´GÉ<u×£Egw¶; %JSç^\x0008\x0011wXL/Â"¾Oß\x0001W¢§¾=¿X\x000ep6)Mm{3õ\x000cÿ»\x001fö\x0004ø¡K\x0002þ\x001eIÀí
\x000e\x0017@±\x0004\x000bz_çÏowû+ÚÝ\x000eà¿½ùñ\x000e×Ë{;Ûîrâ\x0006{©­ÞÐt	¸­f\x0019ÿ·§¯ÏÁ{_AÈ9÷\x000e\x0014ÆÑ²0qÈÃ6S¶\x0007¯î\x001f?þ´kÁ\x0019c°­
d \x0007U°i\x0004\x001dëå+\x0013¶W\x0007¯.®ß\x001cÍ¾åý\x0004§0Åj«ÛÿùÏÿ:ùñöæSkRÃrì	F
ÛõRÂy\x0000×--:;8y}vú~6±?\x0011bYE\x001a\x0016?Øøëøae%©VGù=ó\x001föEÑ¥(z(\x0018E\x0018£\x0008*\x0000\x0004ÔCnø\x0017ÄØ!ÇG[`àÿg~¢fú}\x0008%V¿&Q|)\x001f!Ê\x0014P\x001cQPO1D\x0014:G\x0014+ù2\x001aE¥(q(\x0018WÙÆ¸"\x00151®\x00089®x§Rn¡_Õj·+º\x00089¼0\x001c]ä\x0010iÉ\x001bÜ(J­Àh01|\x000e1Ò\x00066\x000c1L\x000e1^äÙªâ\x0014e\x000c\x0010\x0005\x0003\x0003à\x0015h¼2.wûÄ\x0002¤ÇÉ
ÍL®º ùWprCvÕJKm²|/TòÐY½B*=\x001dÓ\x0007__úôøRýÇà+nat9»s¥<Çh\x000c÷¼ù¥\x0016«+ì\x0019y\x000f¿IÙþct\x001b/Of\x0004Ò¾ª-½Bön\x0008\x000cÎ®?%·÷ÓÁ«];\x0014-ÏÃ\x0005Ðh±4Ä*©º\x0015ÎNÞ'¿÷ýÁ«£÷àË¨Ã§¨c3ú(!Ô\x0010)êH\x0007\x0012\x0010ié¥·Ç}T\x0005xü¯=goZ?ùhI¨Û0ðî\x000b%ýR_ñjøvê2"ÃÇ	\x001e°\x001boï\x001f\x0011îàø±i?{p\x0010¥:*sùx(S]5ÊkwjÁ\x001fy{qdp\x0007ÇWg3¸CòË\x001dãI:õ÷»ÇOv7×Ó+þf÷ëûÖb\x0003JRhÁ¼ãØÏÕº¥¶
ü\x0000ï®ÞÃ?r2=ão¾=¢§ß\x0016
®ýÃîÉyÿdy»{øøÓõÃÍ4-g\x0013~¸a	ÿñO\x000f7>ßÿòÓõ¿}}ÿÃÍÝÍÇûÇÏ\x0000,\x0008½wh\x0015P\x0004shÀ§\x001dèÚb\x0018üøÍåéû\x000f\x0017ïÞ@qñõéùéñÅÕåI·G ]/O\x001b«ÍQÀ½\x000cè#pl\x0007I¸q2á.)\x0005Á\x0006\x000fÆôÂv6µ=Âyûiv	q{
\x0013pÞ±È\x000f\x0003\x000e0v\x0002\x000fÑONt¸fG&Üà*ÑyÛè[\x000fü7\x00134{¸¿Û!ò]ï\x001d'\x001d¹rØ'0]qÔ$^qc\x0007\x001dù§[ý×O±¸â³à¤\x0008\x001e\x001bÓÍAÞ\x00187Ýxè¡\x000eå6¯gý+D\x0002c¢ÿ\x001f\x0013	>¼ýA¤è\x001f?»?Fáþó¿þñß\x000f÷?<Üÿ|Ý&DÄ\x001d\x001e³\x0005\x0012áÙ£\x000c8~<I\x0001nÑ²I88\x00023ö5¹g\x0012±\x0015fl¢Â.Ð1´í\x000eÇw\x000cRS\x0018ÌøùÈ¨U\<ûVØ¨$2éu!\x000f^¥441Ûà`iðÞ(8ù¦\x0003îüý\x000fâÜì3u
Ü?~ ^¾¿k½ëà_¦q00Áv²Æ\x001bþ\x0018@À\x0006ÛeßáòâêCJY¼{qþü
/À'Õú%\x0017üt÷\x001f(!i°onww\x001bÔ\x000bx5"õ5 -\x000bH\x001c3amØ-ëoÎÎÓó0Ñ\x0001~J\x000eÓ/¸³äÝ\x0003ÈvóËî¶ñ\x0007/¦Ýê\x0008Ýè³\x0004\x000f\x001c.\x001eÅ¢\x0011Æäö»ËÓóãÓwGà ;pýË¯N±«\x0012»êÅn\x00049?Fi\x0018'¥®%«õèM#øgo
ã×%~Ýßª4igo0ÎMV)(>|¿èu¶
`K\x0001l§\x0000\x0001¼}Â\x0014c
î½G\x0001¤ö,@IöÜ)P{·\x001açúíÂNÛ\x00030)Ù\x0000®A4¨|Ò\x0003$C(Ãõ\x0019\x0019\x0016ë;¥\x0010ª\x0014âêT\x0010.ºÃô\x001d°52\x000c^R\x0018\x0010ÜrøÒ,)e0#>MÉ\x0007ôÑ\x0014ºkô!BöÒÆ\x000baK!ì\x0000!ä´ª*	aéI»\x0018uv5ãøÛäJ!Ü/\x0011ÑEHÝÎéK8þ\x0012Â\x000cÿ\x0012RTïZ\x000cù/À\x0000C!H»ZVN\x001eÉõGKQk§\x0001ê)\x0008z¶SfBBoá\x001c'Þ×±Z\x0014½«oï\x001fooîZU\x0013²6k²\x0011Zq1{tQU6âë«·\x0017Wg§çËðU	_uÂ\x0007Í*\x0018þÔ3Oª5°³Ë\x000ei\x001b|]Â×½§/\x000f\x0013z+\x0014&tÓás~(lcÐ\x0012½é=|sî>ÆÏ0¡wS=\x001c½+Ñ»þOQÅ\x0000Ð\x000bF\x001f\x0017SskÀÇï>\x0007õË_ÿV\x0004OE=Æîo\x001e\x0010²MÀ#\x0001Pç/SºÜZo|¢´MÓÞjEí9B{.!Nù¶,Ùa°uqz¹\x0006\JTýkÃÎKiÚÑA¸:Õz¤ô"¤©\x000e@g)'#´*ú^[Ñ[óWù=\x0019ÇÉ$í\x000eÞa:MÌÎÀMtBâú\x000fÌ\x001cYKI\x0017¡t¡´\x0012,\x001cKÂ\x0010ôÍs%øÝ\x000f¼þéZ§uv½òKZHÂIs®\x001eØ\x000c+\x0002Á9ÉÇó\x001c\x001cââe}\x0019\x0013\x0013/\x001c÷·÷77àÍ\x000eþéO³Ð²Sc&`¤\x000f
Vë¼\x0013©ýÚHQ®¹LÐ¾½8M¬\x0000o>\>u.ðÙ\x0012mÄ'<|ÊI\x0007*}5\x0013¾L·dà_Y,ÀÛ\x0008Ð\x0000ý¿ ÀX\x0002ÿz\x0000Éí#èöµ!LÆmBë,!Tô\\x0019e#B¸}¥K~ñI£9uâDêÒioü¤N\x0014å)\x0004¨\x001b¿oUT_ÀS%¼ßÊ\x000bÍÀÃÙyÒv`\x000cÒ@\x000e
6²ÁD×\x000bOð~+í3\x0007Ï8T+\x0013<O\x000b\x0000OEu\\x0004)÷-X+<SÂ3mð\x000c\x0018XL
Ä_?5~{çö5`+<[Âû­Ó\x000c<\x0005\x0017njöÄk\x0012\x00194¶\x0014SíFñô6t®DçÚÐÙh\x0013C\x0016~ÛÓHør¥Ìg'÷\x001fn+:_¢ó\x0016ßm\x0002\x0017i0|YJE\x0008¥\x0002ë6p¡\x0004\x0017ÚÀ¡7§èY\x0004EJ\x0005U
û(Òô>XÂ_Ö\x0010ù5ÂsiVÚ[\x0001úáÅ}\x0017ª\x0011\x001ee<X%ÆãsÔ¤øBZOç­\x0002üu°z\x001b¾Úd4Ú\x000c³ÿ¤Ã¤§ó\x000b~tÈùU6C6\x001a
\x001dýôrqB$áSÚûü::¯¬l´\x001að\x000e8î±¸a$áZrÜkûðUVC6
/¸ä\x0005ø²æS½*¥B§ÑbÙ+8®1\x0004r|ÿTT!@½ø*Õ,\x001bu³Ó6¥6àøLâÄò8®øø:
¬t³lTÎ\x0018×Ò×uJ'\x000ed·y`Ô-z_o¥e£vvhÑðë\x0012)>|]érÛ{~ªÒÎªQ;c¯zH\x0017§Uða¶ð¹^í§*í¬\x001aµ3V}
á2[\x000fÇÃNå¢*å§\x001a×êÐ9\x0017ÉéÃÍ\x0001||æWiV|òSÊ/à.ä\x001c \x001d¦×k%ë¾P\x000coW¹ÌªÑg\x000eÒ±ïâ øðtûÀ\x0010\x0013>ÿÿS÷nIzåFæVb\x0003\x0013\x0006wÜMOA**c$LÊ¦ç%-23*Åj&)\x0005ÉêúµÐ+Ö:r'½\x0003îøçD\x001cà\x001cÊXV4FTJú\x000e.î\x000e¿Âùw¯Í8(#EÆÏ¼wÐõ»oo'qP6dû±Uïê2YÓ Ç/àÞýí¤\x001f\x000eJ¿@
÷´~,Óõ\x0015ÛjïHwÂO	¿¤nyöMÂ\x000bAsz´S$ûø:á§\x0007_Õ4%+Æ\x0014ÓÅ%Bæ°ÓtÖiªÇLSG\x0015Ë3\x0015]³;(ª(ë÷÷v¯÷gIglÒÏ3ñE_óiÆ eÒúÙ½ë×Ig=&\x001dP\x001fqö~(/Kî\x001dßNËOwÒYIgGeEñ¢ÛëA¼}\x001aÌÞëÛIg=&]2HÙ2uéáÁº7øê¬W~§m ;ÓT¦\x000e!Ïä(|½\x001a6ZöØ§åS{··\x0013ÎzL8»ô\x0002Ïu\x0008ÏÊåð:\x0008Þ©:L'Í lF«i
ÜÝòlsJUÙ\x000c;ÏéD³\x0019\x0013ÍNy_ ÍÕsQ\x000bÞNÉb:Él\x0006%3Ò£ÒÔÍe³>\x0007Ñ\x0019\x000fvÞ
ÓIf3*ÓÎbÅ\x001b¹úVo§ÝgzOó `¦ñÀÊ±âEÊÈÉÏÖÕó{ïF'øÌ àÓG\x0000\x0017¼â2HG\x0012à0¾Î,5cfiÒkQ<õN\x0006C'É,É\x001ctwwÚU¦ÌfP2SÂzül	¥Vg¸ng¼ÍáuÙ\x000c
fH¢/@\x0015}¬8GeZ¾fíD³\x001d\x0014ÍÚÚÒ×Í>^>cOíÝ^ÛÉf;(i\x001cd8Í®¼¢6õúî5ëm'í pÖ;Ð«(î]iýªO#ººÃv²Ù\x000eÊfDwZ>nÏËÎÛa;Ùl\x0007e³Qî=..×/Óâ!èêÒØ)úl\x001f\x0004\x001c´©\x0016\x0013H\x0012gq\x0018¤w£{Í\x0016Ûi\x000e;¨9¾úâuzÃ\x000eê
\x000cb\x0015xj2#ZWL*4;\x0002Ûi
;¨5ÃúÚÕP.§Å\x000bA\x00021voxÜvjÃ\x000eª
­3À\x0003\x0003ÌVA]?·sý\'öÜ Ø3±Z-\x000e¼½D%ë§¿Ho\x0019åëä\x001b{ôl3S,_ö·\x0006b\x001cîT»®\x0013-nP´\x0018\x0007)ógJc]O».×ÝÉ-ÒüàÂ}É\x0007HÂeäX>Í\x0003æ\x001c\x0017)ôV¨ö\x001a/Æ\x0019<õ|;ü8\x0012ýÛ=ÜQ#ýÅBêáLö(Ì¬ OÌ\x0000¶z×vç»sL3¼ßÖªSÒ\x0011\x0017tÒ¢\x0012ÞWq§NQþÇOw÷-¥ÿ\x0003ýb,I\x0002O¹CNLje¬ÊýÙ9ö|-íðZ¢W\x0012,LOd\x000e\x0018'~{#Õ	òl)íðRæÇg½ßP\x0018=H\x001d*³ÓzÅø\x0014ÃK\x0019ØaÎK²l:\x00055j\x001dÍô\x0013Àç)º§øÃ=µ¡	` uÊ3öÅ±\x001aí\x0016=?¼¢æ.4Þk\x0003nñô(V\x0012·ññôòÕù\x0016\x0017ÃC¶\x0005´£\x0016å\x0005\x001f\x0015Î¼f9¬>\x0004èZ@7
èÓ¶\x0016á\x001d\x0012«a[ÖÆØÅ¬!@ß\x0002úQÀ\x0010Å;\x001d¼cïy2¶=Aã\x0017Se\x0000C\x000b\x0018F\x0001Ó+C×Á\x0007Î{j\Æ/\x0006¶\x0001¢=»Ã\x0014Ç\x001a¸\x0017ÿòáãÇßÿñp2´¥7I¼£^l\,\x0010½$\x001bÇ¸´\x000bý//^¿~0\x0017ù°åÃA>ïkøÆ\x001aWz÷QjÄG ÀÒ\x0002ðéOòY÷Õ5ñ)\x0017¢\x0014>¿xEFøLËgFù4ÔÄ;ô;/Hz$ì]>ÛâÙQ<\x001aôSÞò\x0016¬l/ê(|vQÅð¹Ï
òQD×&z	n¢A±fô¢\x001fiÏ·|~Ï;\x0003*VÍp(WCãÞ«\x001bZ¶0ÊæxÞ^Ú[%®\x0006 \x0006\x0002\x0018ØË\x0017[¾8Ì\x0007¢~-À%rJ¯¬]ô\x000fÐ5\x0019Ç9Áh\x0018ÏIR\x001bí.çMä\x001cwÞÞ%ëe¯W\x001c£ÃÅ /»´jäl-)©¦.`\²¡G\x0000;Í\x0001Ãª\x0003%4lµ-\x0003çIòÕ:Ý\x0019:Í\x0001ãªÃQ­`Qm±ôpNªCëZç³WöA§:`Xw\x0004'ÖUö\x0014>_sòZz\x0014ðuº\x0003çn|ÔïRs5¨«µªzÑµ0t»G\¹Åò\x001b¸(JÒ+-\x0018ê@^th\x0017\x0014nò\x00170Îé} N/\x001d%1=2\E[u\x0013§:7U=ë&suÿËç\x001f?¼ØV\x0016¨Ë\x00071&®Km8ßÃ³PLãerqsqõêo^¿~±^Ù]1±ÅÄ\x0019L£$ú\x0014
y\x001a2%\x0013ÖêÅÕAJÝRê\x0019J¯ÄvMÏöÒ\x000f?\x0017B¢`®lø\x0010¦i1Í\x0004&ñÀIUL\x001cWrÅ³¬h0migV3x)éú°C6ÉÐºG`º\x0016ÓÍ¬&DËGÄËXÎf@É§½û1}é§0
÷ºJ«©Ë<`Â\x0014Ê\x0015Óv\x00082¶q\x0006Òr\x001f¨´F\x0014xð§¥\x000cË\x0016Æ\x0008%ô2sFhRo/JR #ÊýÅÊÄAÌNfÂÐÄô\x0000¢Èñ	jèEjª\x0015=9ÄÙIM\x0011¨ÃÏû±¢ÅÀø a'`F\x0014!=gxÃ©8AVR^­\x0016Ô²e9ÄÙ"EHå\x0008e)C,\úwyÇM´\x0007¬g'`F\x0018¡®áÀ\x0008 }GÄb\x0013Ä\x0007)CG\x0019&(5Ùè}Èù\x000eª=lÜbxh³)Ô"ÛHÍpÒ <ÞuÔn+sJ¿³Äy
ØÄ\x0019±I£k=kÊtå\x0003{¿ø/Lô\x0007pvò\x0008gä6	}Ì4@§Ü"Ð\x0012&2a±Àb³»í8sÛ©g%\x0017ª\x0004\x0015/-g&(võ\x0019À\x0003g§ÓqF©ëhå\x0011-ó\x000c\x0012gÍP0N/exqêîxêãiÒsMóu7RWãh\x0004sRÓÝý#cæx\x001aj»Z0ñÁ	\x001fèkæ\x0008ë]w:SÏèÌô \x0017#)G3Ërj_óAÝbúè+£{¨çÆé>ôØ\x0008°@\x000fLö}xÉâ²äDÕçÁáå¾\x000fE®å>à]nC×\x0011¤0Ã»EóÑîkg]\x0007\x0019n¡ëàåÂN
\x000e©§1\x0007\x001d1:m\x0015úv8ÝÂ-ô\x0014|°ØÕs=P²0ÄëáòÂ-_íl¦e[è\x0018ø ¥(uÓ\x001c°¶VÅ\x001aòß»«¶³cp¾f6g#]&êz#Ûá|\x000bçÇàLþ!Þ*yu\x001bWË¨VâpÛáb\x000b\x0017Ç.«\x000b<4\x0000¼wÒ2Ì\x0018n1cg;\x001bôdP$á1\æÄµTW§[»(·Óu\x0015n«SÔÎS8J.B¦£&Ö\x000fÚ^Ûéºë
c÷5&\x000b6°¥
È¦ÍýÍØäZ\x000eÑl§ëî+\x000c]XJ(\x0017»5¢­k\x0017\õë-¶EØB\x0007çîf°m§Î»\x0017OïïHË¾§\x0014Güâ\x0014,÷\x000e±+\x0016eX\x0011µ^9_Di:yýúâé«kR¶Ï)ã!\x00079ûtÁ¶í;\x0007\x0001Nºtê²d¯VÏ­b&xñ\\x000b¯wVPòxÉî Ml\x001dKím×]S\x000fvWÎ9wçÀÚnÞÇËûÏïoÿöÈ\x0019ÕZä6Åc\x0015\x0017Km8\x0006÷Øq\x0018/_½y~õ_\x001eçÓ-\x001eå£tñ\x0012³¡Q~Nýe
Ù( i\x0001Í( 5w\x00085ÿM\x0006¯«!¸Ð`\x0014Ð¶v\x000cÐF_Kt­6ÀãPÜö½\x00170¶q\x00140½9	O)Î<«å\x0001¥ôB|\x0010\x0010º-Á=Nf¡\x000cÖ\x0000
J\x001c·V\x0006\x001eÔyyï
i³å3âí·ÃúLÐS§e¿ÿp\x001e\x0013Ú\x0018´^4.pÄÃ¸(¯\x0012Jú^
¿>ÿ!ýúa­Ï\x0005¶îñ¶Az%>1D#rÈt£ù0eÃ\x0010£n\x0019õ0£VZ*#Ã\x000f\x0001ãQüa9=t7¤i!ÍÄn×:$\x0004Ù¬¥Ñ\x0015q='`3£m\x0019íøBbí»d¨\x0011-·RµÍG\x0015W<vC®t\x0013»­x \x000cð@Êod%ÛÙÓ¡\x000cãÖò­tmÄ0>òXôßÀÝnóÍè
S\x001a¸í¶ÒûÕ{é¨âJÖÂ\x0010d'`\\x0002itb´ªÎó¡jP)ß[)u8w}ÆhLfíûÿxûî]2Â\x001fé2­£t¦\x000e\x0014bí;ú\x000bÓ¶h\x0017¯þôìæ&Yà\x001b@M\x000bjf@i\x0016\x0016rd¬\x0015½ãr\x001d(Ûà_>ÿ·ÊÄj}ÏCÉ' ß]¤í$\x000csJK\x000e¥CNôâ\x0000 Ùg|y°ùõEÚ÷\x0001-Wã\x00156úÍf<Êïáp0µSáXk\x0014!Ûç*±Á[_6¥;Óñ	©Å<¾öâIÚâ¼Ã×ïyZö9|´ty ä8QIâ«ÅÒöÆµ7×\x0017OÒ\x0006§ý½~¾>\x0011»¬æcäI\x0005cÔ?EzD\x000eaY\x001d¤h,i¢sM3@efº«\x0014\x0007wy¾C\x001e:¾é\x0010VÀËq\x0017êú
We¨øÙ1ìàÂwwö\x0017÷)\x001fÄ¤\x0000è\x001f\x001aòûôÃç|k=?	\x000côûÿøôöîý{\x001eÂýäöþ§ÏôÄN\x0001¢u¥ÇdBE v%é1£"GÒÑlÚp¥ówýü9Oá~rõêÉ\x001bzIÓx_\x001a²¶áÇO÷á×wg\x001bí\x000fyêüÅ¹ýõnÂýY!¢¦\x0017"f¶/,\x0015¡?\x000e{A²çê»õµ=Ñ¤¥fq\x0011¨ÓÉk|N¦I¸ÞW·Mè;\x0000XØ³¾XrT\x0010"¥N«ë¹£¢%gÞ{\x0016'
}èîâÝíÅÍÛ~ÿÇýí§·95ò\x0001Ú¢ñ\x0001¡¾c:5Öñ\x0011X]þ\x0004ñ\x0014]]Ü<{rýêêg«A¯æc°ý\x0018<ècL¨\x001f\x0013rËü1ZÕij
ü\x0018Ý~>æc|.ÊñÙåM\x001fÃY&ºo|1í·6\x001a'ñ§ø2m,íK,%\x000cô-ÞÅoY6:o±í·ØöÅ¸1I\x001f;õå}q/=z7õ1nk?Æ\x001dô1`Jí.}¦Ë?\x0006¢Ü\x0018o¿ÎñíÇøc>&×ÎòÇ$;Â\x0015q\x001c+Ó¶\x0001<òcBû1á Ñ¾\x0004Ï:{R\x0003¼3\x0016Dwû&jsäÇÄöcâ1\x001f\x0013+®"Lú\x0004É}^ÌÀw\x0006ÜWù\x0016~©ÆT\x0007í³,iZ/\x001b\x0013ªQåÌ×ù^ý\x001f¤ÿ)«ÅbÁD'*3"ò×â«|M§ÿá \x0003 èì¸/\x0012 Pöc6ÈB\x0010E£fsG~M§4á ­\x0019¬¡¤ü5*1PäY\x0008ü5ðul3èÔ&\x001c¤7)\x0000Ä2  /ÓäÓIs¥½·%c\x001c¿Ê×tz\x0013\x000eRÁÒ-:I´lÜä­A\x0010U£¾ÎÎt\x0006\x000eR5!h¾5\x0018=¥\x0019ã \x001f{uÍ}M§jà\x0018]¹`'}
MgTÙdnbÙöê«Ø3Øi\x001a<HÓPµK®!J\x001bC\x0011bjF\x001eãHAµ¯ó\x0006ÀNÕà1ª\x0006Uú\x001a]\x001eË>Éi]\x001e÷é?\x000c¼7\x001e¾pÆîuÇ<ÏP9ngè¬/\x0012¸3ø_eîK:5\x0007©Hu\x0002åK|ÈÏ|Êb\x0013@µýüNÍà1j\x0006UàÉ§i_\x0000)nA[þ;ØA\x0017lJrä×t/\x001a<æI*róaDë-¿\x0001°¸gÒ× þ:'­S4x¢ArAÚ¢4]ik¯ã&u1¶½ôüNÑàA\x0006\x0014ç§½Iµâ:£À#û*Cø*[£;U£Q5Xµ¦­A`ë,I\x0001Î\x0010ÉÞù:_Ó©\x001a}ªI±´D!?²XÎ9¯PüÈö«x\x0002t÷ªÑÇ¼jH3%ÄIB ^²D\x0003\x0017'\x0019à¿á¬;m£Ñ6éÖèRÿA·FÉA\x0003ÍÍØÒµù:ÚFwÚF\x001f¤m\x00001·ÆHç,Y7,Ðhx[ù\x0018\x0017üW\x0011hº{ÓècÞ4î{ÉÝJ[£ò_@³\x0012Û²_Å>ÓæÔ\x0007iÎd´°g\x00135%D²æJèì×qlèN×è£tMz1b£iò
°@s\x001c\x000e¿¦íO®¶j×»\x0013]uq\x001a-tï«Óø¯\x0014â8ÿ(sØ7}¥HÇã/ö)\x001c·O4)8ghI$Ïþ\x0001[¡þëX:Ê?ðlÉ¹Kß\x0014\x000c;
¢òMQ\x001f|öºõå\x0017möê÷\x001fÞRÙÁh:\x0002±é"³Îiyü\x001dF¼jaÛsçõÅ÷/QIÂZQó
Ø~\x0003îÿdHó2£8n\x0014Ë¶\x00186¾qF>A· ÿó}BÚYÕ~Bþy÷WìÍføâ#Ö#´ò\x0011?þÛ\x0017ñoû¿C
xòh(	ÑxN<\x001aÛüvÃÛ³{ímSÄûúÓí/£I%¥Uä­¦fG7âÆ\x0010ü&CìÍÅë\x001f®þ¸üÖ°cË»Øié\x0003§`8Me\x001eeé½Ä,Ü¶ÅfvÝ²ë}ëîÄé\x0001	5²Çë®!lº\x0000ÙMËnö­»r\x001cHgÆ\x0013ÏsÏz:3\x0007¯»mÙí¾uÇ Ij`Æ6çu7u±6nÓ~3»kÙÝ>ö å®Òó\x0013(<\x0018>ïi76=Î7³=ìc§ú|>ïéQS\x000cP=\x001czdh¼oú´N²ÛÜ<³Ó]õß\x000eZ»cá;\x0019	ûä?\x001b^¹ÎÎ¾\x001aÒßú'¨p¦_U\x0010ýúìãÛ_>Üß]<¹\x001fQkí9½.w\x000bå8ÑÜÅ)	ý-:öÙëg|ñêúâÉ«þ\x0008l?\x0002ù<©$}²/k4'Å°)Ú9ø\x0011ºý\x0008}ÀG8y%é¯9\x0005\x0005¢J/-'ið#Lû\x0011æ°Üx\x0013^\x0016G qò	Noñ\x0003\x000e~m¿Á\x001eð
1Éß j\x0018è#,çÏ¥¯\x0008Òg\x0007¿Âµ_á\x000eø tjËWh#Ç	·häÁ¯ðíWøý_a 4ÕÆÜ#Ø\x0014Õ<8'mßb\x000e~Dh?"\x001cñ\x0011º^
T6Q¾ÂÕ­ØdP\x000f~El¿"\x001eð\x0015i\x0003\x000f\x0014é¶¢),»)ÓWD{üj¥¼-\x0007|Q¥\x0000¿\x001c)Ë·Ûsú\x0005\x001d©-¯âÁÏèÕö\x0001z;ÉT~,¥ÆMå3¨ÿAù¨6\x0005*\x0007?£ÓypÒ3>v;é3Ò\x001b_ðù!b<þj@§1à\x0000AÑÕâÂ\x00076Æxþ\x000c[w#|CÕ	[8BÚ\x0006¼T,n­¥N\x001få3býMÉÖÑ	*8BRTHÍðógh]\x0015ø¡
Î=Ú Öú1eøÆO¨îKÿ\x0015R`a6æð=^Ü|\x0005¶_±R.=ö\x0015<72}\x0005U¥K®KÐR{g·º\x0007¾B·_±ÒÒa,\x00128$¬)Ô]¤\x0002ñmLÛßø	çT°}Û¿|¸\x001f.Ð³QÕÃ\x0004^â<ËØÓ6à6ßRóüËWß=ôTsw*Ø¾´mê\x000bæS­´e½.FM56\x00039í\x001b¿@·_ ÷ï\x0001ÇD1zËª.m\x0007I/Þ·ß´üf??^\x001a\x0016
W&òqé>ü\x0000Ù\x0016ßîÅw*Öôît\x0005\x0002\x001f /\x001f \x0007¢ì\x001b?Àµ\x001fàö¯ø3¢}ÉO¦é\x000bTÜe³ñ\x000b|û\x0005~÷\x0016øiÚ\x0017\x001aþ`å\x000bàÑBìñ;Üùüò=îçÓ[ÁasÒj|\x001d\x0006I\x0005\x0018ÈHìCÌ¹}a:ûâæí»Ûáê}êÔX
Ìilçú(YAÑ­¶ÅÍ³«Ô9·+LgWÌÑK\x000ekj-±þ\x0018¹	fîÑÞ\x0003ðº×;á]Tf¯rsÿLo¤ÿëmíô¦¥7;é=8Ó®urNòc£Û\x000eþfzÛÒÛ]ôÔT]2û¼AIUVA\x001aiÖØ¡ð®w;Þ*©OpéúryRÔ< /\x001de½é}KïwÒ£.íã\x0011-TåÞ÷(
Cpù¶>´ôaïÚCéCGvr`?dZ{--x´È-}ÜI\x0018]±<­ÉqÚRÜÊ-e£\x001bÿ­ô×Î´\x0005Ç³2G±s\x0005Õw\x0017-Ï=\x001b\x001d\x0003ø²½ÚÊ7\x0002,© Ñ\x0019©]	\x001b\x000b>7ãw\x0002\x001fvK|'å\x001dN5ø¶\x0016\x0012ñ;¡	{¥¦FnSä{\x0017|ejýæ´­«Ï½COë»s\x0003Ò³o¯7Ô\x000b¿l\x0000\x001e­µz9<ítÇ©\x0008(u5äç\x0005n\x0017åQ7ôawØË^µh\x001f>ÿÇÝû·÷ÃV[¼ä§o²ùí\x001ek\x0017\x001aÐsD^¼ùÓõóg¯\x001eÿ\x0000l?\x0000w@	\x0012\x001aZÍq~\x0015´\x0004\x0000T[\x0013t¶~Õí\x0017X½ó\x0013PYä\x0007Æ2\x001c»8Dø°¶åenøú:Íe\x0007ÐÍíÅ»wïî.ýòû?\x0006\x001fÒÇ¤Ø\x0001¡d)Djî÷È\x0007¤×âëëg¼^2
¾	->ÍÙÇïê£ø
ó[nJGOÇÌ-+Vø­jùÓO»ørS]ÐC=_\x0001íc- s^­ü\x001b\x0015ÖZ«'\x00149ãpµÅþE!~u÷Ûß\x0006ïrRYÌK\x001f\x000bb¸½\x000b\ÝoP?æJLP»ð_ñÕõ÷+]§Zøü×¿}þô.;PÒ\x0019ÍPçÀ«~Ó¡Tþ']Qð¿»»ÿ-ýxiÆ4f·§#ÂÍÕhàyÇ uö\x0014\x001cûîúÕ÷é/¹;àÕÓ§ÏÖr
ÍJþ÷÷¿°o="¯o?¿»{Ê\x0018¤\x0014°D\x0015K'öD¥¥\x0013;&ó²	v	(¡×WonÖ¼ø=Z:Rø¢¦ß$Z:_æ\x001bEK\x0006©ûFÑø
ß&\x001a½\x0001Ûwà7Åî'|Swôçÿúé7OÒVQz¯S:ç\x0012¯Û¤ÿ¼LèF]\x001aBû\x0014\x001f7ÌÃc²Ë\x0002
Ú&`Sùr§åç¹ë*éô?ó8cHûJÿL0¦\x0007%s\x0012#pÌh+£nÃ{\x0018!ïqÞäaÈ\x0010s¼4C&Þ\Ë 5o´AÕ
» é
ÿôáÒåÝÖQ\x001aÜ&HP¦@q\x000b§q\x0002\x0012IÈä?f 5U\x0013#æA¬QÞÐ\x0006Ö\x001fÂHEÀù	F9J óÆ\x0017H\x0008¤1\x001e\x0004é\x0008ÒÍ-d.±È+,qJé$È\x0018d·\x0001¹7H¯¶üÇ\x000cdÚã\x0002\x0019¢j¨²Ý%å ­d°ÇÜ\x001b$ás\x0012(XcÚ\x0004i}©\x0017J+É\x0013Þ\x000cÇ@jº2zòÞ\x0018¸,w;!¬ÑÊÔþ«M\x001d¨þÿ¹6.O
"FçIñ\x0013|""sÇ@|ÔB2I\x001d(\x000bIÍ+U9 ùDê\x0018à\x0018H*xýÜlU^Ù\x0004*\x00022$\x0018f4\x0007\x001dÈ¤h~¼-úævêâØzqÒEGË\x0017ÇËÅñ~\x0008úëçÿvgÿÜ<îÒÓÿåq÷\x0008	Þ^bV3\x000e£âë¢BEÍ$\x000bÍ|¹ËéaÿòEúÅS¥\x0007*OºÍ@ÙÊÑ\x0005\x0008\x001d«\x0014\x0015MÉÄO@ªé<\x0005ÄÝñ·¯ËsU	(\x0012K@J	Ó\x000b\x000fò\x0001 Jg\x000fCD\x0008WH®
èdËÚêÁ/\x0016ý0g@?þ~ý¶-Aý¡~\x001eX¨\x00089\x001aCPÔ²Þ\x0016(,5¢	ª­7ú·\x000cõo\x0003+E\x0015¼PÜÎ\x0016ª\x0014PÒBé/\x0015ÔãLæ¯?ßþí¿\x0011\x0013ÅVév:åoûËÇïîïÞß~zO\x0007-rßzc/\x0003täú.f}[ä&íÊ½úþåëï^]'ÑµúPÑ?ÿIx©Ëù\x001fò\x001fÿIóË:ÿ1\x000b\x001c¹\x0003\x001f\x0001C\x001e@ÀÉÖãÇ»wêËk4\x000cü	Â§¿F=ûí/·\x001f?rOÛûÿ|ûéQ?\x0003EìÙy\x001a/©ZJ\x00117\x0003ÐÎI}ÿòêõknÝpõ*Ñþ°îløû_ßþ¹m(E½úüë£\x0010\x001aØ|YDV¹úÖÒû®/w³Wo¾{È\x0015òþö·¿Ú"\x0005È^Irà¶%|yw/#j\x001f\GÂ^ÞLºzañ×Ø*¥\x000cõx\x0000óåõ«W\x000fL©¥óyÿç_~¹å$Üäfã"j
³G{ZE,'2D¬«øå>ßÔå[\x001cÞþõ'ÄO­NNkGº~ÿ_ï\x001eëyö\x0019\x0016\x001bºnB¶¡DÎQ\x0007Xp)¤\x0005£9.×7+s\Z$ vIùíL.ý¿sß¼ìèPò>· ø5\x0004Ú~éDØ@ÿõ§ûwZ(\x001aoJÿÜüþ¿¼}ÿ¨ò\x0003[\x0006ÐÆ)kh\x000fiã¢-mcÑ)§¾\x0004º¹~ùìù\x0006\x0018ºæÈl¤IïÌÜ¤S\x0014nÌÑþ\x0017$.ü0Í_î?½ýh¨9á\x001fò\x001f7\x0003\x0002ÌmZô/_\x001a¯UbniuüÂvÝ´bkÊýû¯ÿn[óàFÄÁïÿk<RO@ò\x0000¹ëZ\x0007<È¦\x0017ÀÕÒ	5´_Ôí¯?.xd§þôám|?ýð[zgmÜËt\x0003«­gÒ©ÏÞQå\x001dÍÈØú\x0002ðO/å\x0010÷Ó\x0017ß§\x0016olÚ¨»¿?¿ ¤Ý¤¦\x0008\x0003uã\x000elRöFþ`}²F¿|\x0004nD|ÿ×ÿxk~ËHôÇ¿ÞþvwûB§7oßÿþÿåº°\x0007\x0005\x0018Æç\x0003ÈÍ
\x00145rdåéîfRí×Wornö³çO_<_`ëgðò/$\x0002ùým\x0012ew I	å7E6A´XòZ\x0005ÇAÑdV/xCß\§A¢lÝêèçÚ
\x001eó@IíyáH\x00148ð%ß1-\x000fËÁÍp¶³p\x001dÖ\x0019n\x0006MMJsAÚÕl¾eóclé=­üuÚÉ\x001b­Ì\x0011¢H÷B¨{-´la-*ö,ÑÈ{úkacÇ\x0008æüòA;\x0004\x0017[¸8\x0008\x0017k@ÓE\x001c#»æ\x0012\x001b.¸æ\x0006Ø@uWU
Á9%A\x0001s Y)¶Z-8»FèzA2&If%Ñ[è<M³Ìtä¶\x0017º}ûZòa+\x001d\x000eÒ¬èl\x0014¦¦">¦\x0003¿àÐ\x001c¡ëä\x001c	:ê20\²p
ÃIb
}2¸¤âV63Èæ)I)Ãy_È\x0017	¬ðË\x0017ê\x0010Z'aL\x0004»ôàçe\x000b£&\x001a­uSK¡\x00118×Á¹1¸ô.(±\x0008ki2\x0015Ó¹2Ù\x001e\x0013ò7q®S\x00100¦!He\x0019^;j´W´\x0017r\x001bD\x0017ÕBq®S\x00110¦#-Ëµ.\x0016Sç!Îï<u1\x001d4ÿ¥a¶Hõ\x0018Í[a[

Àa§#pPG¤ÍÔÅ*É]
\t\x0002ç`\x0010ÆNEà p=þ	ÎÉ¥Rp¡Ûya±S\x00118¨"È÷ÁtàÄ5£A³nÍN\x0015ÀA\x0015\x0011T½°\x0008\x0016Ø.IÀû.\x0004v\x001a\x0002\x00075DÌO|B3Q²>tÂmÕ\x000boØ!ºNIà &×íÐÂ¥·¿f8¯\x0005Îî¼\x0011À1%á\x0013QÉê±zW\x00161¬«~µ°à(\x0019¢ë\x0004)	ì8ÙØàëÆZyâØµä²ÍtÀ1%áÁ^\x0016§5NÒ¶¨Ó¡ì¬ZJ-\x001b¡ë´\x0004i	\x000f1O¤":_zu$8¯äÆ*¿ïØéNKè1-AÕÖ6\x00168ÒfBçxcMÔû^\x0012ºS\x0013zLMxd4Ç­,)!\x001d+Ú>2ÅQÂ&uQ[\x001fÎ³3òÅËT[j½âÅæô;_9
~üÔ»s>
ñ\x0019¨¯ë\x0008eõ@×\x0010Z\x0008
âÝöxcË\x0007þ½M4¡¥<t \x001a\x0000^»Þ&øñ§\x001eï§!<\x000c²»>=g=ût@îoK\x001a¦ø\Ïç\x0006ùhà­~\x001dç>'»©:v;~éoÇ/c|.øf¾Xjd¯¾²mÜg§¤õû¹_¿¿­õsýõp×ã«óéOò)Nj²ÎR\x0003â\x001eÛyy]øÜèáûúãçþr\x000c\x001e>-\x0016¼£hº¬Õ[Hä\x0019Äû©Ç\x001b-*(g¼Sÿ\x0014¤X\x0008¢ù¥÷ä7zÞÍnm\x0010·£î
âr÷âa\x000c\x000f#\x0010Ê\x0017|\x0006Î¢(\x0006$òòöó»§¿ÿãï·ï\x001fCû\x0015\x0012\x001eR,¯$#\x0006\x0015ÙÇàµÇË«77\x0017O¯ÿ«çÏ×\x0013*'¶8Åä%N\x0000¤Ù\x001cS®1u\x001cãÔ-§áLVmYÌÈQ\x000c<ÄªèoË\x0018£i\x0019Í\x000c£uì\x000cBj]Ràç\x0013©q%Ð2Fi[J;EiÄñ&¿é
¦æÈn{vÍsºÓÍp\x0006¤w\x001cq¦¥cß\x001aFàÚ\x000c«}\vÁqúÓÏpz©j²è
r\x000cÑÉzj½lçq3LÝ pY4¢Q5;X	É\x0018sÄ¶71-\x0012j3éCÏ\x0006Tõ\x001a9ä{dÚy§ó ä)Ñ\x0019M\x001eeJ\x0007T×\x00141òûjåy0Ù	%J&=^,_#vy%D®&I·hEav·\x001d¦®{¬A\x0008ÒI%\x0014\x0004»<\x0017´
Ë¯ÕA±Ô\x0019\x001eY4á1xëkT=ý\x001b¥\x0005JÂUòö×q!	r\x0006÷ÓÝ}K¿Àõ]ª­¾\x0004¡å+¥8«Ê7ï,LogA\x000e£\x0014%\x001aKG
:\x0006Ö\x0016]~W\x000cM=)ÎR%\x0007gòPËÒB\x0000}à
\x0001
°°1ä3êO\x0013
¹¿MQQh\x0001%cÂ.£.[ÌIô\x00163É?¶oî>¼¿½ÿÒ£þþso\x001fá4@%P¥¾úK+N\Ô\x001cÚpÊÂ2çÍõçW¯þH\x0019Rzöüé³õe\x0015\lqq\x00167\x0016ÉhsOïLkÐ®¥KÓêVÏÒ:)B¢êko\x0018W¡ä=®äÚã\x0016×Lâ£ÏBúk@Æ
ÄêÝ²Ì\x001aÇu-®Ã¥2\x0013^]P®LhÎë`%\x001dg6´´arqÇ¨\x0010¨\x000e¶$\x0008K=ZÊ¢=ÙY,¨Ù£ëi\x001cyáu#[Î\x0002ÈY\x0008+OqÞN.À¬`\x0000GHÈÙ-)ÏÁ³ëmqÞîªÁì]K'\x0005YÀÉ¦Í¸S\x0004\x0013îAR\x0017º\x0006W
\x0000È\x0005PÒÛÓÃ°ÐòÀmÊn_HBÃí®\x001aÌÞ5î0Í¸Æòa0r\x0018ÜB\x0019Å\x0010ïO*N\x0007?I¿È\x0005ªÉN¸ûôöÓÅÓ\x000fò~·¡\x0008¦§6þ\x0017:ªl'¸`¸¬Ú/PopýÃ³\x001f.¾xóê)µ¢z ÃêTÏ*y~\x0019SVòZÑYNo1vÁübµ-«\ÕÀ5\x0010Ü\x001a`yaCÅ¥~S\x0013°¾õs°\x0014í\x0005p±\x0016\x001dOL°¸\x0010\x0010-lÍm;Ê)\x0008RåOù;\x0002»\x0010Ø­,ý8wh-'$\æ\x000e"»Ò5\x000bµ²S´õÙPy\x0003vyj0\x0001ÛXZ<\x0013põ]°\x0014&oÏo¿E±@Ñ?öYRéQÍ(ÿýßÿçõ¯ï¨5Þ#<]¥a\x0003*\x001c+6c²ÍØ"\x0007m=T\x0008rqýÝ
µÍ{Óê³¶¼\x001câÔÏ@B|hÉ´\x0005á4Ë\x000f\x0011NçZNç¦8miJâÀI\x001d^Âd\x0003»Pô=éUéÕ\x0014&²ã qJWâ¬O\x0005»P0?Ê\x0019CË\x0019Ã\x000c'D.1p@
rK)\x0015Ô\x0017\x0018ø°l\x0017\x000ep\x0002tÛ\x000e0µïÔúï\x0011¹L\x0001­n\x0003\x0008+®í\x0011Ð&\x0001@1Nb\x000cçÓâ4H:AãJÂÐ\x0008¨îv~XQU\x001d1\x0008Pä5\x0002êÅ\x0006c \x0016;P3+\x001a"\x0007\x000b\x001cêZîÇÎpAâBgAPjJßz7µõ»äbê$¦\x000b\x001e¹rRÃJñÄ\x0000¨njvÒ_5À\x000chÂÜ:#ª®\¦ôrªo·_ØkìAñ[\x0005M'¾ñ\x0014ó½¿¹O\x0013@Ó\x001dÇ\x0012Iÿ	/)¬\x0004\x000b6¢ª\x001fûì^çû%ýùÃ£ì:(%	ÈÔ>#\x0019þ¹gÈ[X©b,O_Ü<\x000eÙdªÒ\x0018<5\x000eé\x000cHjOK\x0019ï*]/v»\x0007½â#\x001e 4ÝR¥\x0004w©µPuÄÁá!)¿ÐvëhgÖÑEVÖ{ 'i^GyØ\x0000+>À\x0001J×­£XGG\x001bfHr¶\x0013©µ$"\x0005µâø\x001bôÝR[tÛ6[*ö|È·[^\x001ci¿Ýî\x0013é±Ä¤D\x001fN·¥ÎxÅý¯A	¥Ú}»¡©Í Ç¯\x0014g\x000caF#2È[Key1µd}Pº×^L\x0003\x001d¦	Lïj·\x001e\x001b¨{Æ¬é]>®\x0014ô
`¶fGB97;6Lt\x0001î¿äéÙ9ëJÍü\x0000¥ï\x0017ÓÏ,f²Ü8æKG/¹õ`îÞñè:Èèf.¹Í£\x000eó\x001bécxÞ\x0006íøëf\x000c\x0013UwrAÍ·$01ây¨\x0017Û&÷×÷·?mðÐmÁÏôtuJ\x0007\x000cmµô\x0010\x0001\CRË£ëWWO\x001eôÎ\x0008#¶8ÎÞ¾ÁTHÍ­ÀC\[Ç\x0001HÝBêqHã\x001c\x0016pÉíb|°ÍZ dÑ´fb³ËPxZÈô\x0004
¼Ò¦6íg´-£\x001dg¤D®È\x0011\x001a\x0013é Fp%\x001b{\x0008Òµn\x001cÒXS¸ÎðBZ%Þ\x001d°Û¾ôÃQÙKN1Ðû+kGmÌ
ãªi>\x0018ZÄ0¾ÞÔ\x001c\x0013\x0007¥êÈ\x0006îSíÔZ	è\x0010cl\x0019ãø2¦×å\x0006^PÓïf\x00061Úý·¦
Í´ãÜ\x0014Èóªùj\x001bñfQ^ÿnÊ^ÙkÎZv\x001cÆEù?²0.(ÿ9\x000c	!ôO¡ì®8|£w\x001c»ÛßèíÁîöà·v{8ÏN¡SÀ§MÓt(\x0013\x0000¹©¦±yöDI\x0004àfÆ+³ØÁÇbmO\x0016Ü&pû¶qÁÛ\x0016~ãMfG17
õ\x0007µ¥RÈ+ÎtNÀ\x000ftT\x001dàÕØñÒS¼ÚG.Æ1.YÊ¥¹
\x0015p´ÚÛôü)àÆcHÀä2\x0001¶Zq\x0007HC9å\v§bÍ`X
¸L\x0001ûØ\x0001S¹Ü\x000c°AÃMv
5uráM¿~ \x0015ð\x0000¯1®\x000fßø³±;\x0010ôã7Ë+
«O¿\x0010·ÃÓ\x000f÷÷÷äþ÷ütûX\x0003NçM\x001eX[6hNºHÿî©¶u¥,ýéW¯8\x001dïÉ«ë'WÏ\x001f'Æ\x0018§éØJsIÇMkªn[«\x0014ÀÕ-®ÆÕp©¤v\x0018É5ZvZz½ÒµcØ´ÄfØYÍæÖ¢Ü!ÓÔ\x0013çWÌ	bÛ\x0012Ûibjwc¸5e2Î×Ö+µR\x0013À®\x0005vÓÀ6ÖvI/«â½0(\Ë®	bß\x0012ûib\x0005µUTôd^nLõ\x0018/{[&xCË\x001bæåZ\x0010ÞÄ.\x001d\x000f\x000cÔ\x0005^i§6\x0001\x001c[à¸ç\x000c[nbæôÎÓNÂ¤N­\x0004ÅÇªÔ¼Úó¢ÍÔSl¥ýµÖQWÝ\x0011Ò\x001dÐk»yu¦ñJoGîu*MmX)Q\x0000î\x001dÌk»2ü¢tî\x0008Ò\x0019CWÑ¶ÖXd¸Ów°CáyQ\x001flÜ+0Ziy·Ò\x0003r¸Ów0¯ð(Gµç¾ÚÊ¤\x0011·ÖÛp\x0002¸Sw0¯ï	d .1÷O5§Öx+=@';}\x0007Ó
Ï\x0005wÉ&\x0005X\x001a¥\x00193+½7';}\x0007ó
BH,­#Ñ×ØUQ±P¢0IÜi<Vyô\x000b,*ÔIT©=`VÒ)';\x0007ÓJFé9éî\x000c\® MÔ¢ô`i(á\x00142vJ\x000f§(zÚ©Ú\x0007MkI\x0014r+^þ	âNçá¼Î®¾@Òz\x0007>É¾Úó\x0001÷\x000f¼y§l½zAK3÷$¥ûJñè\x0004q§óp^çÜ+HT\x0008{\M=\x0013æ0ó\x0018;ó:\x000fjC&KI&lÏ» \x001d}ãqç¸Ó!8ÿhJ+Ë
F¬ERÅvãI5Ië\x001döhÂN$ãü+Dä¶µh¬ÍÝJ3ÑqdÝÉ7=oÔ\x001b-}\x001c,ª*ebLZúÆ¶\x0013È¼ÐóòÂZ\x001eRNý9=?½õd¦ÇÚH	âîöéùÛçë¸
Kyú
8éäjWr¼&»Ë§ç/\x001f!¶óùIRÌ!sj;\x0018rwùôôå\x000bTµÁ"X(\x0007éDtËQ'ÙtÏL_¾ ýéCNt;°ÒÉ|·»yfúæôÖcL\x001bÉfRÕg±RË=AÜû6§o^H2M^§¥wBFV¢÷¨£ÂQÈÝÕ3ÓWdi©jÛçd$/k%¯m¸»yf^íÅ \x0013e¨\x0019%OÎ2G=H÷«=ìüiÄ±òÏ4ûîöíãïÈ»Â£;MmYÒIÃÆ¥9Rþæß]={(NÃØ\x0002â( ®ý(cRmÇß8éW\x0016Wë¤¶\x0003\x0016Ð\x0002RÎ*\x0017ÉDÍ\x0011fÑJmXqP
\x0000Ú\x0016Ð\x0002&ÁT¦\x0008&\x0016UM0ú\x0018¿V\x0016µÏµ|n\x0014kÙá`s!\x0002¿'e\x0001×\x0012ð¶óùÏ\x000fòÑ â\x001c\x000b¦^eí¤Y0+\x0016ì\x0000_hùÂ0\x001fÈT` zt-Há^éº\x001d°Lfª¿|;!X
ûeB4§\x0002R\x000e³÷\x0002C'a`TÄÐ³
ø\x0000ª oW\x001d¤÷rR?{w\x0018:\x0011\x0003£2Æ\x001bu	µÄMÌ{%a\x0006¿VÎ¼¯»Á0z½­¯òÌ\x0002\x0007LQ	`Xé'7@ØÝ\x0011\x0018¾$ÞËü\x001e
øB¶µh­ÜvBì.	\x000e_\x0008"¦é@z1\x0019@ÖP¯Um'ì5ñè=	T´*\x0003\x0010P\x001aøP«p÷MÆîàè=¡\x001c1\x0014cVËÅ¶åÆ\x0014Ö«¸×Áî¦àèM	(Ë¬\x000bÒ\x001cdµ\x0018q¥Ý\x0000awSpô¦\x0004\x0013e<3
3ã0¬5§!&»wYw7EÞ$«¯ú,ò\x001aÖáyÉ"Û+¯uwSôðMñFª\x0001É\x001bj¸¤©¨Ë¨;	»¢oJzúIä\x001a4y	2a¬ù\x0017\x001aöZº»)zô¦D¥ê¿h¹ëT5\x001d\x0000ìî5ìn\x001e½)±\x0008Áò\x0006J3-Õ-õ!­÷
lÓ]\x00143zQ"jîe´ÉæÎÔkm\x001d\x0007LWè\x00077Ð\x000bTú'\x001bPåÏ^Éô\x001a¨uOÿ|ûÛ_n}¼e.I\x001aîFMUv<\x0012ÓÉx]\x0003¸"sÒþ_¯¾yõÝÍ}\x0012[J¡Tµ\x0005¹5\\x0001HÕL©Önõ\x0010¥n)õ\x0004¥Õb%ÕÇÝï4zò¬cXm1iZL3³¹ÉQÆ¤îÃ<h´iÓqeàó\x0018¦m1í\x0004¦SRL¤x\x0010\x001fR)wÁ\x000cp\x0004¦k1ÝÜ¦
ZêÙ]ç\x0018ûÀÏTí×+ä\x00070}égV\x0013Ås§i\x000c{sê»c¡¥\x000cs)ª\x000e_D/ù/I\x001f±±Å3Qz³`Òál©aL¨ôx8à¢·Ù|þä\x0018ºé®@)ýÜ¬£ZÌz?\x0001Î^\x0007Í(!jÕÏCÊ4\x0014Þv9z%Sk³ÓB0¡¨(¤xTL\x000cö2ð,&åX\x000f)¿Ò
³ÓC0£Òeç÷"&Í)ë)mXÓ¡]s
qv\x0008&4\x0011MF,µ&z Á¦¹È&ÂTö{Ôi"QEéÝÃç3ý\x0012ÀÓJ2	a%-o\x000c³ÓD0¡¬rì15É2f+Iy	ð+³Þ¹c\x0000³ÓD0¥¢I*b\x001d&\x001ee \x0004¸Õ
ÿ\x0011ÎN\x0017Á22ÑQ¼ÚK¦¹râý£aR\x0007pvÊ\x0008f´3%¡B5ë%µ2CØ)#PF&i äË\x000eQ¢Ê=þÓ\x0007l;vÊ\x0008g\x0011FÞötcrÆ3¿Úd=ñãýhB\x0019\x0012ÏëIùå\x001a)\x001eofb\	Åavº\x0008gt\x0011pÏ}\x001aM-}Q\x0010%\x0011\x0014`¥`\x000c³SE8¡ÓrÙ\x0003=<WÀi0*®\x000fàìT\x0011Î¨¢$ã}àõDIs@\x0010¡\x0004<Ø±ÓE8¡\x000c¥V\x0017]DáE¹í§\x0001hÖ\x001cÂC2Â	eDÙÉ¥MJç 9´\x0010äùFÿÁ\x00038;e3Ê¨öÐ6ú¿ó\x0010¶`ùº\x0007¿R}1ÆÙ)#PFT\x001bkY¹Ó@6v-®9\x0015XNÝ)#=£,p­©É²eø^ÓÚ\x0003ÞÃºSFzB\x0019Y-C5ÒCI\x0010\x001c ¾8ÜzÓ¸\x0001ÎN\x0019é\x0019eT_\x001c[\x00110f>ÂDÖ½nB\x001b¥÷´ù4»mº(q*eWûpvb^Oy\x000bã\x0018IR\x0006>ée$\x0011¿¤KØ÷N|ê\x0019ñ©´Ü£ì¦(6r]O<âE¬;±¤'ÄI2µõi .Cl%ÓÝv3qÛ
å;\x0017!væl\x0015¥©Å\x0008Ñëý\x00078»[d&n1Q\x001e9<\x0011.Ù÷Gìºén¸EÄ	,¨{bH\x0015Rz¬wM\x001fàìn¸E&ªÌé\x0004ðÐÊ\x0018D\x0017­7¬\x001dì®ºBíZ\x001fpÝ\îÃ_0W\x0013ÆÆDR\x0017x+b©FÞ^ïIsòkÓó,$@\x0004(¬ ØBkÏ¦A¦_´-B_ÞøíîýÝçû
YZJòï!8Iµ>§Û´¶¬¯/^¾zñýõóë7¯\x001e\x0014Ú³Is¨¡,©ôöd¦ùLºz\x0000ÆHuKª§HmYÕ\x0010B
\8"¤ky
¤¦%5s¤5Ø\x000e¾¶»4J¼7hÖbÄ¨¶EµS¨eË'\x001a\x0019p&q^P\x001fè8êZT7\x001a´¡êÂJÝ\x0000PÒøU¸j>¡ú\x0016ÕO¡*\x0019[MûÏYÂIÂÊ¢êxÌQ
-i[Ô:[\x0019ÒýÜ\x0007\x0013%×\x0010qe`ù(jlQã\x0014*:êe\î?òR*\x0006©GõFy\x0003¨MÎÆ~.k¬
 Ù¦Èµ6(O<Äc®\x0015ôºjJYåLq>\x00024`YzZKN;ê\x0001Û£¬²)mì\x0011é	Oc²8ûÆêº¬\x000f4ÀÝxæÒKbF\z7\x001f>¿ýxñÝç·ïÞQ«±GXÓû\x0003¹©\x0003ê3Ï\x0000ä=#Ødµ¬ä\Ý¼xóìõÅwoÝÜP«±Gi£oi£¢
Ñ²%èü(ejRD#\x0003³V\x000eÁ ,´Y³é@[wÖÓÚRzA\x0019J,\x0000ißkVªHGqu·¶ '\x0017×Ð9Ïè$¸¼,®]y³\x000cãÆ\x001e7Îá\x001aÏF\x0003oÙªå\x0001\x0011é\x001bÖ¦¾\x000eâ6+¥ßêað¡Ãõanu1òx<O©\x0014çª m\x001dM·R5Ø]Ä¹³KlqjÈÞ·»6Ôd\x0014W÷BWÏI]zl³\x001c£îq5'\x000bÓ\x0010ÓC\x000e\x00036³C\x0008Wfâ¢yÐ\x001eà%G¹ÈFmZò*¸\x001a:É aN2¸ô\x0000çi\x0003HÇ¸ÌIì»â$\x001aÅ5Ýêj3·ºTN(\x0013öÒaÐ¼ºZZ:\x000cÇ¬®éW×L®®ö	Wqár(³ ²ÀÀµ®Ãµn\x000e\x00062­®g\x0001¸-\x0002Mß=æ,¸þ,¸É³`OG\x0017 4\x000eSNÄØÊàÒAZ\x0003\x001830'Æ\z@°ÅTF^Ä
ªNÝ;dmM\x000b@´\x000c0J«¼3¤§\x0019\x001bV&÷$¶2rs\x00187ô¸s\x001aØR%ÁM\x000fB{dº8
ÛÛfÒv¤ä\x0000VhÊJ£	e¥$5ýreí(®í,súqjm\x0003´¶cä«¸ÈÁã{¶\x0017
fR(Xg©â©zAgÓÑË¬XXñ)Ò\x0006ÕÑ\x0006õM\x001bº\x0016:»ÜÂ¤][º$2'2Ì ÌÊÒá\x0010mf±;
\x0016'\x0002%úódk2sN«¡5T°fN*PV3-:®8S:Z¹f\x0008Ü3êÆÔâÚ¹Å5>P&pÆÈ>&Òìòæ\x000e¿£¸½X°bÒ\x001a\x0003V×
\x000f<Ö¾>Ñ`¥²b\x0014·\x000bvR.d7ú¥ìkÆµNÎîJ+¢aÚ~qÃ·}\x0016\ïjr®¦ddpÁ\x001f­#7²S\x0018å¢\x001d´¸Nw¦Ós¦\x0001SGÖ%+·\x0004ôU,¨"QZ×\x001d\úqVSÛV>
T\x001aTÔ/J{ÌIðª³réÇ)Zzïð¨½\x0010EC`\x001d\x0010\x0017VZ[ÒB·¶\x001e&×ÖäAÜLåy\x0006õ\x0005A¾ÝCpû§º|ªk@\x0019\x0011¨(Ë\x0015ÜúPneÜë(®ïô/ý8Ô\x0010AÆ.\x001a\x000eñ)\x0015£¬îJÁ÷(mè^êôã\x0014­ÓârLRs{è^ÈüE·Á9\x001bzS,LbHÉÚ<1\x0019\x0017×yshWJGqu'\x0017\x000bH\x001a'xisÉ´Èi}é\x0013ñxiiãg\x001eèÈïIÈÏv²K"qq%«s\x00107ö®8éZ\x0004åxN¬²\x0014:É¸ \x001aM\x001d³¸±·sã¤\x000bÀ­\x0001¢¡°	¡\x0006/ÃIV\x001eÂê;¡@?Î°*ì\x0010K¸Ng\|Î¸Ç¸Ó
t¸aNâ¶¸ÉLÚq9S¦n\x001f\x001b»Ç/ý8\x001b=«ßD\x0016(±*ã\x001a'Ra¥Ó0­éiç\å#{ÄòYàµE.r9[w?-´	k¹XJM..
=bÜ`)õ7ó*]ÏÂJï¤Q^T=/ÎÙbé-&©K|ü:óz\x0007uÆãJââ(o\x001fÈ?Ïòj9J¨\x0007Ç¸,\x0019Ò¯ti\x0018ÅÐãÆ)©«éÈr±d4ÙvÌ¼ªödq\x000bsò&x\x0001úä\x0005©Û¦c)Ë¼:O\x0019#^§AÖ×®ð\x000fóÚ3Þ)AGî¾\x0014ÑS_\x000ck"'ÝFs\x001b/Á¹3Ø)µ¦©¬\x0017dq\x000c³Ìì$¥Å=æ0ô\x000föüóäâJ±\x001a¡'Ó×WdÙÚ|QÞÞ5[_%\x0019\x0011B=¼²ºF\x001dD«Ïh§ÌG\x001d!Æ\x0003@¢BêäB´ÖKáoÄCâ\x0011ïìôºÉÓ{tGD
MäÅURF\x001fÍÂDÊ\x0019ÜxvxãÜá
4]Ï\x0002û¼¬®\x000c+I&Ù!¸¨{=zJ\x000fë\x0004¯âî©Énpå4hN
\x000fÑÃx6s±?\x001d\M#
IÇ%Ì¼¾ZºXFX\x0019\x00073Ê{f7àÝ s?F^^ §HÆU7n`8\x0006·Ï½Éät\x001c|!×S}N9\x000eÁWÞCòÜ\x0000CÛèç)^\x0015¥{Vð¹{ræµ2æ*Ä²A^múë¦ÍÜuË3×¸KÆeiúC\x0002× moåd3CkÌ%Ã&ó×\x0015Ñ«´²\x0008kó\x0011Gqý\x0019®Ä\x0005%=Ê\x0002ætøÌ2$XÈeÓ¡³ÑÏ³¼r\x0018NvYâÖén¥·û0ïYÊî¿A{t2$××H+úcr`Á^3yz©¶,³¬Ü4´¬ÖYiþ7Êêû÷\x000fý<ÅªëÔ¢<ö¥\x001c\x0005\x0004\x0019Ox\x000f\x000c&å\x0017Ïùr4uÕey©óu(j\x0018¢\x0012Ñ W¦,
òÚ>Nâ%#\x001bSK3Ï¼¢\x0003\x001eÛ{ûa2óÆ\x0013È(Dï­xöÀKä\x0000+ÍyFyuo£[=g£§×¼Ø¼Crìd^q>\x0005u·á,õ\x0002&s/\x0012n\x001d\x001aï­£\x0008fÁ±f~­é(¯?[Þ9¿´6TR¬2OE:ú¢Û±¿£¸áì²¹ËF\x0003¶\x001c\x0006*¦+z\x0002èa\x001fyS8Õ\x001fÜ»h7\x00197rÛ0\x000f¼ËË+f§ÇÛ!¸x;'{mM¿HËºøö'÷þÓ{-\x0002é"JÔEö\x0002½åËáÅ §÷\x0018+Ò³Ó0\x0017v§ðõf]¤|\x000bFp\x0011edt´nrqOøh²«É«\x001b(\x001cXq\x000f1tÜcÚM:¦³µ·¾8EHÿ'²\x0001W\x001a<
òzÕ\x001bôó\x0014¯
Ò\x001a:Ëxëlc\§ÞáI\í¤g¼Ó4ø(Ó\x001a1sÜ1\x0011Aðæ¬îËÌ=ß
%jòiH/ àÕÕ2»Ç\x001dãH÷¶½ÓÏS¸`8\x000bÃºd¥ûPpQÚKSßcxÏNÃä\x000bÈÐÜb¥h(ß¥ðÖé­G¹"¼ýÂ\x0019y;çÝ\x0003\x0019\x000cOÕ·¾¸,J_µ~HØéÐ\x000f>(éÒe&ÃPò!\x000cC)LÙahÎÛ°\x0018ÛÌ
üãÏ·ïßÞÝ_¼úðùãÇ»ÛÏ\x0000;CÃ9Jó:åjW8-ö+Í?¾¹øã7WÏ]¿ºxõâÍë××Wo\x001e§Æ\x001a÷P´917>`liÂ\x0015ÖzBNaë\x0016[ïÁv#°=wNØQz\x0005¤9lÓb=Ø^ZÝÅàèu±LnT^¯Î¥À¶-¶Ý
ö\x001bÊQ8#\x0014j+Á-å×ZÁOQ»Úí¡F6é\x00136\z>#Fæù(\x0017W§6M`û\x0016ÛïÀ¶J\x001a§k~é¥£½6ma:´ÔaÏb{\x000ey¥	uÏ*GDZÑ(·R\x0001;G\x001d[ê¸g­­ÍJÖ¸tÐ¡\x0014Pîàz\x001csmmv/3ÐZq-wZj)ìÇXcÍÊ­\x0006àîõã\x001e\x0005i£xæ®#)HÌ
G
?è4$ìQ\x001a©z¤ôýÔ|HÒzk\x0011ÚvmæÍ\x0014w§"a´ \x0006ÅKÍG»®¶^Y7AÝiHØ£"ë¸¦¼ÚM0§Õ>PÙ@§"aLt Ëí¹Å!R¤{m\x000cÉ\x0014v§#a4"\x0001s`-
$«ýG\x0003_ãî$ìÑé ÷vRÿ´>\x0004³>Ây»S°GOÈó´Þ§\x0014Ñ1õökÝÅ¦¸;E	{4eR:¢)=ò¨ª$\x0004e¹íJhj
\x001b;]{t¥ÅK__7Ü\x001fMÕ)\x001ckãµ¦ û'Ù\x001eä§dd¥ªï\ÅµéeSÜèÆ=¢´cÁF%n¬\x0012\x0011¸è?Ý@Ü#\x0002çî-É.©éÒ~V»äHM(Á=¢zù;æ>ÍAn5ba%s`
[wWRï¹E«gì$ÄÅæ\x0006\x0019,¶ZR>ÇÝÝJ½ëV\x0006\x001aR\x0014|\x0012âb½Êðµ6\x0003sØÝ¥Ô{.e²\x0002ºbíLVGZÝº»zÏ­ÔQfÝ*\x000fÜy\x0014<\x0008÷ZsÓ)îîVê=·\x0012\x00030(Ü\x000cíÅ¿\x0003v¥WÑ\x0014´éî¤Ùs'\x0011$aU%+0²\x0015èNÜ+U±sÜÝ4{î$Tk@Ö8äá;y ¾1½\x000fpÇÔÑKZR¹Å\x001e\x001e¬O\x0005·>gz\x001bÎýÛýÛOÿLîwêþîöâ»ûÛ÷éoúðö±¦èÚÐø\x000bÙQ/ï\x0012T25Ä¸P ùô_É\x0005OmÑo®.¾{uõ<ýíO/]ÿáçÛ_n?~º_\x000e-tØ\x0003í¤ï45æ²\x0012
\x0013ê¥>r«Ô-u#ü \x0008¿ilìâ±4SqLL\x0006tY¿T:ÍÝtdJÜ1Ë­©Í\x0015Çòt\x001e1FÜÁËðH·4,c»ÉpMÜ\x0014âæ¦³!ÜÀ©a!:·<,¸ç¹»Óíw\x001coâæ´<zN\x000b·\x0015î¢iîØï¸ã|k]{A;Drdn¬W\x0017àK£d\x001bú{	{.¦VZ¦£:J"¦«ó\x000b1¾éåVðãß{Ùý÷o]\x000ej<s\x0006ù}R/?¼½'Mùýû»O\x0007ePLn\x0012¸
J\x0000©\x001b_º¬&_¾xö´ä÷/^]ÿð8oìxã$/õçF(!_ËÒÀGIY~X²6Êkºõ5³ëRôC]D(\x0007½ðÊòºuëi\x000c×ê\x0016×êI\\x001aËÀPÒ\x000b²ôÕÔµË95=\x0006×ù\x0016×ùI\c¤%,\x0005;¸Ï·ôË> Ã¼±[Þ8»¼&ò\x000bÀ)\x0001\x001dé¿PIÿ\x0007aC¼ÐÄwóãÜÍ(\x001dÉkc\x000f4`Vú \x0003Ñ¶×M+ùqyv:À*ðôM^Kç¡µôóqà^á¬@£ÙGúÔZ\x00054_m3²×DÕ?QÒ/$\x0005çé»ÛÏI¹}ÿáý£¤ÎP\x0007Ð\x000c
	\x0014ê4[ØâV\\x001cOo®Þ$¥öýç[(±¥Ä	J|ÆÀ)
 n]ñF#¬x4Æ0u©'0ÓëÎ\x0014\x0007\x0006$½ëyú\x0015:~{ ]é95iZL3i¸½\x0005J5\x0017ï§2kÇs\x000cÓ¶v\x0002\0¦\x0019\x0007:»¯\x000b&®$Faº\x0016ÓÍÜ È®{@KO¡2_[r0a¥\x0016b\x000cÒ·~f-ã¥ÜÀÀiÌ2ÈýYiV=F\x0019ZÊ0A\x0019\x0013%K#2a9æä$Â\x0007q%»y\x000c3¶qæþDI3¤Jk.c`¥\x0011í\x0010æ)ë%v5ÎiÁIàÓ±pÊ\x001f¹Ð« )\x001dä%<\x0000Z&'%$åO¸\x0012 \x001dÃìt\x0010L(!«O3ãÐPrx\x0019
,\x001eÓèÍ¼1ÌN\x0007Á\x0012»Bm#\x001fNë«<G`v:\x0008&5¶êÊdå³HJ\x0016WUB+¡Ã1ÎN	Á\x0016² ÄmA»\x001eY\x000b\x0005¬ëéXÏN\x000bÁ\x001a²NÕ\x0019aÆ¬%+Bé\x0008Û\x0003:E\x0004\x0013ÈÒÛYôe¤)ÆS.û!·½SE0¡¬óõ¶;I¦ \x0013,®äRavª\x0008&t\x00115ç\x0002\x001bÐ5M\x0003Ð¤Ü\x0001Øé"ÑE\x001e¤\x0006\x0013¸×V\x0006Ô×y«+@c.Â	]d¥Y¯Q¸äå4R\x001c\x000c¥\x0003n;öï¡\x0019]ä\x0015\x000f¨O\x0002H_\x001aYN)áÊ\x000b~\x000c³ÓE8¡¬Óô¦t<\x0010c°§1+\x001dc2Â\x0019eäóTÓ\x000e\x001b~¯ë\._8ýJ
â\x0018g§pF\x00199T\x001e§Ô%Niv¥·×\x0018g§pF\x0019%åÎ90YtÈZ\x001aË Í,ßÏÙ)#QFVÞnHU1¢2Å\x0004q+=*Ç(;U3ª\x0008k
\x0013\x0018\x0000\x0007ñ×Y­\x000e\x0011J.Â)]\x0014yâEÒÀnñ´ëu¤jX\x0019§9Ä©;\x0019¯gd¼1Ü\x0003\x000b\x000c_Xa%ow\x000c³w&Í\x0008OmÄRB}\x0012J5)\x0010ãJ¾ë\x0018g'ôPR\x001aÈe\x000fì\x00016öÄyÄ¶w]Ïø@¢\x0011K>©ñK\x0019Mõt®ô©\x001eÃìnñ.\x0004w)2a.½ß¤S*ú]¢Sù3¿qúE-Ý¼»øáÃý¼}÷îíÝ£~µÁûéÁr×Ñ\x0010µtñôkQë\x001f^¼úÓ³g×\x000f\x000eúõg¾c"Å)R­äz\x001aÇ	85Ôï)Éì\x0008TÝ¢ê\x0019Ôt»É± }g¹\x0000ÝÖ\x000eÚnu(õ\x0018©iIÍÜö£ô£N'Ô§í"\x0019¿&EGQ]ê¦P©L^Úë DðQüÈ>®´a\x001b%
-i"¥Ö`Lê\x001c9\x00193*Ç.¨öQ>»þF®ÿÇ§¾}ÿéãÅ/ÿû¿ÿÏ\x0017o)#ïÿ}L\9z~èó®Huæ»ZieE\x0003¿þëÕó\x001f^_üñâÅ3ÊÈû¿\x001f\x0007Ç\x0016\x001c÷c)¡¨\x00035\x00012®´ãÖ-·ÞÃí\x0015Ô§r\x0012­uuL¨\x0004 ypÓà¼ÚRã¨y.¹ÑVB¸SÔ¶¥¶û¨½DN4He6>VwÕJ®Ç\x0014·k¹Ý.îdSú:\x0016?[nBX\x0016|­Cü\x001c¸oÁý.p\x0000Wß¸Ôeªï\x0003¹CË\x001dö-¸$ù¦±\x001e\x0014¯d½ýÊ\x00009îØrÇ}ë\x001d¤W\x001e\x00050µã\x00025Jt ünK¹u
jÍ.¸Æá*)!¶u­«s\x0007oè\x0015æ.I\x0007ÃÚÉÚûò \x0015í\x001cx§0aÆô4 ëJlîùÆ"Eêa´9rÉ;	ûtf²L¤Â8æ·J&'\x0011ÈgeÅ2GÞéLØ§4\x0001éå_J¾Ü%[WVZ-\x0002\x0003=tj\x0013öéMb\x0017R$²Xñ¶\x0016Ñ¯t1#ï\x0014'ìÓJQ¬\\x0003ÙÎ¹\x0008Äµ\x0001Ésäæ}ªS\x001bq\x0014Rß\x0002NLÐÔOËZÞï\x0014y§;aò¤^v\x000b2Óke9ÒX\x0013)È<R(vÚ\x0013ö©O»9Ë\x00055"Zj))êdÊ\x0019rìô'îÒ.]K'â\	yv1ùÊ,9òNâ>
ªëÓM\x0019CqÅ"[¢s\Il#ïßû\x001eéZTÂúzÎ}]s½2=d¼S¡¸O¢¾\x000bjÉ/]t¿DÒ1?ò°t\x0008w)¢$Ï¥\x001f¥{,µDýÈç2vÒ\x001cwIóôT0¥Ã¥7|?CÕC«\x001e¶\x0019òN&â.è,T
$\x000bÿðTËkÝ#ÆÈ1ö\x0001!ú\x0008	\x0008=¿ýËw¿ÿãÃÑd(°ÑGJ*£É¤·y+Êó«/n®_<ØÜ±\x0000\x000eÐ\x000c\x0003Ö :ýÕ"\x0003Zj¬ü²Ù½\x0019°-¶(\x0002\x0006äÜ2\x0000çE\x0019\x0017,eå½\x0019°\x001dp\x0011ÿ ã-¶\x0003&ëB¤/x\x0010óF*`ìJLe; ï\x0000ý0`¸äz-5qáCY@»âóØÊ\x0007íØ¼Ù£Æsh×¥Óv<\x0001­x]W°\x0019°¨\x0000Å30°oqÌ£R\x000bRÓ²â
Ø\x000eh{@;\x0008\x0018l)A(\x0007§\x0013äV²-ÜôË\x0016/	MwIÀ\x000cß\x0012\x001dYQ:E\x001dxum\x001b»âéÜ\x000cè:9\x0008nX\x0010bäÞây	­Ìµã,\x001dZÂ§°¿Æ0~\x0011¸ó\x0003­(¹1\x0013ì±e½·\x0001PáYàB!µ:éÉÝ»«·÷\x001aqI\x0010ÚbÅå^2Å)l´$\x0007¸ÞåÉõÍÅÕ³W#ê\x0016Q\x000f#\x0006'®\x001aCc1Jv±ÒâÁª°Z\¹\x0019Ñ¶v\x00141(.á&XÊ)ÈABk³ÏG\x0008}Kè	k\x0001pÚR'¶Ú4Ð¶\x001b1¶q\x0018Q;\x001fS\x0002	Ç
)½\x0011õZTv;"ô·eøº\x0004r¢·=ÕR@y­q\x001fmk×j\x0003Ý]áËgÌûlÑG¢Ü¸Òÿ}\x0004±»+0~YBàw£ÕZ\x001e1¶öäµn%cq\x0013¢1?\x0005
\x0005_ÿõóíý\x001dú§çË_îÞ½{¬ÎßÑ¨â<3\x0001%C\x0019£ç,;\x0013µúRx¿þ¿Þ\½ºæBÿôryy}sóP?\x0003ë\x0016XÏ\x0002+}YBªÆÇÈ¯,Ú&ªÝ\x00046-°\x0005\x0006'Ýw\x0003äA\x000b¥ç\x0010v\x0013Q})&]\x000bì&55\x001a\x000c¬ê
ó3ÖDXx\x0019Nòú×Ï.0j©W³8@\x001aõ)À\x000bb\x00128´Àavé=\x001bê\x0011\x0006né	!\x001ew\x00062íNz\x000c9\x000cì)éé&ÿ'\x001eA¥¬P©\x0007qT#QÁHÂ}s«én7Ï?}È¶cÂÓÈÔLèaÐ\x001a)KLW»\x0003Bz;i±²2v\x0000Q÷z\x001017ÂâÑKI\x001bäê
pZÕÁa+\x0001BÛ\x0013ÚQB\x0015.\x0003Ï
£ÀxÙf§ø\x001diýZÊfDÄ\x000e\x0011q\x0014.
pæ2lÜ¥°qAÔk] 7#ê\x001eQ\x000f#Ò¬Þ²Ï.D\x001e{\x0000¶6Åó°÷¶ í"ÚÑ£¨¥áÝ\x0005Ñpô#\x0005É\x0002÷°\x001a·ÙèúUtÃ«H¾ÓBè%V\x0000I\x0010ÕNfk]q6\x0013~\x0011Ãð"Rq\x0007\x000bE¯oú\x0019ûÚkmç\x001aê¦X;\x0011ÒßPÔMq\x001c!r\x001b\x0011\x001dõä_EÒ\x0010½,#Äõ³|+¡ét6ÃºÏ£\x0014vP\x000b¬2{\x0005µ!Ê/.ÆC¦ép@¹
Ê"j2¦9e\x000c´«ìV£Ç[ùLw\x0019½ËT®eø¦$Û·4³\x0000­jÛ6»Ö$èqÄ´Ãç¾¡Ôûäîý¿ßRß³?Þ}¼ÿüñÑê\x0003G#T2&=~¹\x0003\x0003ö\x000bkc\?ÿ?¯JË³×¯Þ¼~¨\x0000A'òªÈ;\x000cëå\x0005dw5÷¸öÂKÏãås9«[\=Ký\x0011y^5­ËÚÚÓâ®GÓÖÌÑÚh¥zà¤@\x0014ý\x001dÖ:D£Ú\x0016ÕN.¬²FË\x0016¥l"¬YDã¸®Åu+\x001bhÍ<·«#£\x001eéGÝ2ßâúÙc«ë¼Ô(ýØ4é%©X\x0011]ã¸¡Å
óçk(B²à%­EI#Ðó8llaãäÚ Í%ÓO\x0015Ö×ñ£kYÚÃ¸MM2oyÁp6| ,9V\x000fµqP+Fó8n¯ÌfµY2­¸§Þ?¤ê:\x001dÄÛé3Uh\x0018$ÛÓzH\x001b¾i+åòã¸>Yæm\x000cFñ3Okº:³Òjf\x001c·Sh0©Ñ©­¡½¯Ñ/àOË{\x0010n§Ô`V«\x0005\x0019ÔË\x0016\x0019WKQò ,\x0007qÆy;­\x0006j\x0006\x001c-ñÖJg\x0017õ8¸¬¼qÞN­Á¤^Ë\x00152|\x001cf\x0013$B©ª÷z%e`\x001c·Sk0©×èÍI4Å>0oã:·Ól0©Ú¼\x000eRnMÂ;Ó\x0018U}+S¦q±Ól8«Ù|\x0015¾ôM+²¬.ïZÈt·úÌª¤\x001f,T/ :%ª
V\x001c\x001bã¼ðÅYá\x001buí·\x001ek¹å©Z\x001czªa'ÌpRyå$+Ð« í´´V~­¯ã8o'\x001dpR:d
Á~kÊ©)Ñ'§ðAÇAw×MO^·l/0/U-h\x000e29ÊSË¥<
ÝhíìmÁÚãæo?\x0012£ìÜbÿÖ·YÉ\x0015ÝNm´ê9F×\x0006
¯îÞÿþ§·\x001f?¾}t\x0008¸\x000fc.÷Ò,]¿©Æs`Å7ûêúùõÅÓ«×¯=è\x0015S½\x0017(qD\x0001pJWäaÔÊÇt¶\x0014\x0012\x001e¦Ô-¥ tÀ%e :¯¥aÿ\x0003µ²íC¦¥4\x0013^fß9êüXª"\x0014µ+\x001d_	º\x000cQºÒMPZw©L=×RsÌ ýr¥ÅÅ\x0010eh)Ã\x0004¥¡>\x0011\x0005Òr\x0013MåÁËåQ+O\x0011È¦Ák©3úR®x.p,¡\x001eËYCÝ\x0015;n|í_óT§»Ö\x000cl\x0008³»=0s}¬ãHSNüFt0k\x0002ñþs	Ýí©ë\x0013¹¬¿ä9\x000beb\x0000»R=<Ù]\x001f¹?Wøöh*ãþ
ÇîöàÌíI\x0016´v¼áSÓt2ud¥aê\x0010e¯ 'nOPâ%J/³\x000fª³\ÜÊ;j\x0008³»=8q{\x0002:Â\x0012\x000b%µ¡Ö
¬(»Û\x0013·'\x0000²oJ\x0016dòE S¨`úÇ!ÌîöàÄí	ÊñÓ9ÉpÃ¹FiÏëjF¿ãh*íÏ^ùÔ[^ù\x001f>Ê!Ítñ\¼¤ù|¿>ÅÌ£¨\x000eVqB
\x0006ËV±QvÉñóâÍ\x000f9ºY~}ñÆó}÷à¤íBíÂ4¶Ôü/Rí©ð«LnD\x000fe©îjáfMbGh±É/:­¤\x000eZ±ÖG4m\x000bgx\x000e\x001b
R:$¹t[s#\x001dMQ¤Ò\x001c\x00121p¿%ÿ\x0007Â>å/eì¿4í\x001cMPÍË­'¤ FnzaÒÿØqËm|Çmü\x000eîô\x001a¨ÜNÀj\x0003²Þ°ÔpiÛu§~ç¦wk(Ü ØZD	.eÌR÷\x0012ÐÍ@\x001bÓÖ\x000cm¸ñ\x0002ji\x0016°ÚtLbÇþNÆù;éÒáåÄ\x001eMèXrÞu¨ÜzÉãÆ&å#qççVõpSïÉÀÜ¶®÷B¼\x0016Û÷Ø;îdÈó»u4Ò\x0006\x0011Ù06Ë\x0003¥'¹¡çyn§4R2y^îôä,6hÂµr+ÍR[ÂIn£:n£vp\x001bñhr×©r-æÚÿd,Íyäî
\x0013Üa$3Ôr\x0019¡\x000eNzazHserKþ¦InßÉnôó²;YùR/¸%bÆ:¹n)¿{ú|5Üôã47$\x001d/bÐ;nnAÝV¹0%=\x000b\x0016^/sÜÉ¸o¹éÇinÊËÂ<o\x000c½Q¢ãýqò¤\x000c!:qÇ=Ü1pëàÄ­*·7r/\x0017óöæ¸-tjÇÂ\x000eµ£\x0011ø]Î·åç#\x0006eÅôvKs\x0008G¹=ægäI\x000e¦_ü¡\x0013?ÜøÛÝcÍd]\x0008µ\x001891rÖ®v\x0012bq¨\x001f~?¼zñ_®\x001fè$Ë¾£ôã®¥ÖÔe%\x0019¾ó2F	¶£¤\x001f\x00173Á®\x000e©Í½ròCª­Ý\x001a[Lúq\x0014bi	ÔuÍsXK\x001d<d\x0018m¤4®£¤£{®\x001dÑªÓ43<ï¹ÒÃ<ôÝy*\x0010ÉV/&\x0015Úµ\x000cHÙÛ\æ-±)c\x001f¸í[)}OéÇ)\x0011kØG+láê^_ÊÂ\x001aÄ<\x00197\x0019³3n6b¦§áþ\x0017\x0006+fõ¯Ã~ÈÐCqH\x0017Õ¥ôè0rÉµAñµ.F*Æ(5t;®a|Ç]\x00105D@\x0019Úª±Æ\x0000ÜCæøFÌSW¥©a\x0014Ó	(/y%³eó¤Iv@,Õ\x0012QÞÞÿ|÷5D×#ºaÄÜ¨Êë*;\x0004ÑR?Át®ÇèO¡)àgzÒ¶NÄ^\x001aß9i »=\x0006&nOz\x001bDÉ¢ViªòÑûµ9¹­\x000bfÀÒlIÃ¥@\x001añ­\x0003<ð¶Ú\x0008Ý\x001d78qÇÓql\x0016Á©\x001aJ>OKã\x0011\x00071ÏLÌ	\x001bÓFÉùL(u\x0011¤\x0001EûÍ"cû-·\x0013[®4\x001b¡voWÃ>é#f\x000cRúîÓÃ\x0019j}PôAÚ·BÔuúÇC^Ä­ýÑôãGÓÆ7\x001b½¡iy¥ÀÂYÁ|ÈG»
ÓªÎz³jÜz³^rµÚ®ã\x001b¤÷\x001cö´S0Í8&åÃpw¿SJ\x0019X_1åºÇÔ3^*÷#Ö	ÒÒ?;Â~
 [H;®Îi\x0006*$\x0000R\x0002NÆ
Fµÿ\x0002Òí0Çõ$MÇãþQQ¡¤\x001aª\x0016ãR"÷ eotØ	£Ãê(ùæÉ\x001eª\x0003eµ46\x000ea¿Ð´¡{ñÚ0þâµÚJy W\x001a\x000bMd\x0013ÎÅþ fì1ã\x0004&FvÆXryÉðh\x0004©rKí®F1mi'fáÚ`ëÔ[#-þCXj\x00028éT·NÍ¬¦\x0017}\x001e¨Kn¡ô¼ô;ÜO©;
äô\x0006JÜK$¤'¯\x0017L\x0019u\x001c²a¸\x0013Óv{N?\x000ec\x0011qDÁ46ÛU{\x0001²M\x00061C\x0019&0\x0015pe:µ\x0008¬S\x0006AÊIâþÅô½:÷\x0013êfÙKAg2ç,_7"|Xª?\x001dxõúþmá'Þ\x0016T!Ëe6éÒ \x0019pZ:ïí·8éö;ñý¦ÖÒæÆ\x001a\x000e:j%}»½{(_d#¥ëÖ~ü\x0016)}gqÐÃÊ$r\x0014ò7}ç5(wcÆÞ0\x0013vµùR:¬$1Ä \x001d\x0017Ýn?\x0007¨^ûäÇ95=uK_H)Ó%¯Qm»¸Ã>Ê\x0019Î8'ÖÓRY£´Ø\x000c%\x0005(	 '
,FR
bê1aÜ VLÔ¶´ÙÄP[õP\x0018s+çÙ¶ÃÌ¶×÷¹ÀÆQZO©&OÛ¾×ì&E9Ç-wm"O"3Áóû¼&Ú%H³WC}](qb×u(%\x0016ÖPN	çòÑ4ô·ÝgK3Ké¤mñQ-¢£¹8a³çÇ\x0017SI+l¸ÀËiäMiÜÒÛANsÆif8#µgÊ4Bw=ðÙ4q©óÉ f8Ã\x000c3È\x0019ÍIFjIÀ	¦rú¥Ê1Î¦_{æ,
Û\x00079ASjºé¼2îÉè¥ö¿®_ÍÒµ}R9\x0019îD¢\x0017\x0013ÄydÔn{úï\x0005\x0012ý<Ñ]«\x001e¼Åî£çÕÔ~i\x0008Ã\x0018f8Ã\x000c\x0013éeÊ~M¬$.[Aã$gs¹\x0013é°_óÇÛsÏæí¸kFª-Ò#È+½öÛÆïùZßV÷J\x000c=×÷\x000eÆ§\x001dòÃÍAÒó¾¼Õ¥Ê\x001d¢IYÓWõRÎPúúÚ5÷ãÅËûÛ·÷o7Øò ¹\x0002,=*Q1£a#D=ÔCùõÅËWWÏ^=Û-*Î¡*\x0019½d"\x001aî`QËKSÿ2¼:\x0005«[X=\x0005«cäb\x0013¢´bÂ(¬M\x000b\x0015éS°¦5s°éÙ)@yî\x0019\x00118óÏR[Êc`m\x000bk'a
{
MA)íÙ0qKg¿\x0016:\x0005ëZX7\x0007ë-)CéÚ|½\x000c3"\x000båË ö\x0014¬oaý$löÑfXJ\x0014æM4$Ë
-lµÀã[\x000ceÙJÓÒ¯Þ?ÔN}\x0000¶iu»~ÏÑ\x001aÏÊ+--MgbKU[pNÁvr\x0016æ\x0004­¶öAú\x0007´Ü/»`­N±v\x000b&E\x00179OxaÉcÆ++Ã\x001b\x0013íîc\x0010ü²¥¹>Ò°õãÅÕ»\x000fï>}Ú`\x0011j'³=i\x0018\x001fû£<Êô]\x0017\x001ea{uóâÍõ\x000f?l\x0001Å\x0016\x0014g@cí
e
r#Ôd»J7<\x0011ä\x0000PÝê©\x0015µ´eE¥pZQ%ÈµùCc¦å43
V¢
\x0014 ç÷ÕE¾èÅ\x001fç´-§áÌ8r\x0017y=%àí`¥OÅ §k9Ý\x000c§S\AÎ¢¦ÁÐÓÊ\x0001ujµ­þ\x0010¨oAýÔ\x0001\x0005éÀèJuE\x0006¥Æ\x0002\x001a|¦ã ¡\x0005
3 éXFÙy\x0019ýÞ3ÒájÛð!ÐØÆ\x0019ÐSäúEF¾KÔ^Wt¥\x001bÄ\x0018h£ôó\x0014·É%åCêJû/^RÙ{}ÈÞC¯¦\x0014\x0013\x0019'ìÙ¾n~\x001dQ>å5í\x0014\x0013Li¦ÒY£DP&¼Ð$\x0010YÓ\x0007L\x000fv	¦TÓ?iM;Ý\x0004SÊÉ!7.Ikûg5\x0004<gÒÆI;í\x0004SêZÑq×ûô¼fÃ´ªQ\x000f«ó^@;õ\x0004SúÉÆ:á\x0000eº\x000fé' °6u´ÓO0¥ ÈÂ\x001f\x0002'\x0018¤%uÒ1z}*È\x0010i§ `VC\x0001¯)iU\x0014q*S#ìJAÒNCÁ\x0002©\x0013ÎÍ\x001eùB¹è¥s-®´»\x001f#ÅNEáÒ§\x0016oÌ÷°7NÙ©'QO\x0010ÔiRíáÌ©ê!f)öï¦)õ.;R"|FUCzÈvê	gÔS\x0012\x0012|ö\x0010¥U3ò\x0016Mê\x0008¡zÂ)õ\x0004ë~ò\x0008­ÞnS[¤\x0002Ðã¤zÂ\x0019õ\x0004ÎJOZjøW\x001a%íZII¥\x001e@Úé'ÑOà}m\x000c¯x%dÜü:´ÓO8£ÀiîW[îó\x0018MVú\x0012/ÑÆI;ý3ú)ß(ú4\x001aJ.T]R{Èæwê	gÔ\x0013§4~üÈ§°ª,é!\x0017JwêIÏ¨'F\x0012£¼ð¾sRËàýï|\x0002´ÓPzJCyõÒHlNë¨	G~1Ëy³ÓOzF?Að\x0010Ò;Ú1¨4\x0016²á\x0018Yª{ÇÞ~¢\x001a\x0001PÉÔw²÷µªA-ÄúHí¹S×vNÝo~{ûx\x001d?Y¢\°Fã%?"þRJùÀz>½zúìj\x0003#¶8Î2\x0014Æ)ª\x0015àÉ\x00128wÊ¬\x000c~\x0018Ô-¤\x001eL63r+EÃ
\x001fµ¤\x000e·\x0018Ú\x001df4-£`\x0004~Ò;esù¹)cÐ\x0005rmÐÒ\x0010¤m!í0$Ý\x0016éI©\x0014\x0010d·ÕC>ñ­®t\x0013-¥\x0004é¥\x0002Ù\x000cÀCÎG!õùÝÖ§»ýùâå}â¹ûí/\x001b\x0012ª\x0019h<A$8YQ«cï_¾J¿¼þþå\x0006Ll1q\x00063Wz¥FN*T2\x000b!­åÊ\x000faê\x0016SO`\x001aô\x001d é\x0002ÒÖÓòcm\x0002Â\x0018¥i)Í\x0004ezÁAykª¨¤õ^\x0012ó¬!Á­\x001dÂ´-¦À´\x001b³XÐæ}¨§áÇ;®µ=\x001fÃt-¦ÀLl1«)ÎV¦@Xá3é[L?®M± ­«d»FèØóÐR	JÅyÙs`=!Èb¢Z>6\x0019[Ì8\x0019\x000cÕ¦eL<ò\x001a#p^E³;<ÙÄgrwÖMG\x0019É\x0002ÆH\x0007Ù ]ÚÒ\x0015Zó'\x000eqöJhF\x000bBç;Ä5\x0017Q\x0019KyíÃ\x0006\x0019\x0015\x0014B\x0015Gµ£HÚsIpF}
N\x0005Á\x000e¢dGÎÀH·E:®¥Î\x001aÜJ\x0007pvJ\x0008&´Q@Aírx=rí>ß!sÄ¾wZ\x0008&ÔÁ:ÔÞÜ85Jç-amvü\x0010g§`B\x000f\x0019pu=£xL¬ã¨ËÄ\x0001\x001e	EdÈ\x001fSd\x0012¸^Z¡\x000c9Ó«î8;M\x0004\x0013ªÈhÅIWé\x001eEIº¾Ï#\x0014&t\x0008&Tñ§ëNS\x0004¸Rs£YKÓ\x0004÷sb§pB\x0015\x0019\x0017¹;OÚv¤QÙv\x0019«a©\x0012l³SE8¡L¨åü\x0018D|je¹Ñ¦Õ¨vì\x001fD\x0013êÈ\x0004%DÑâ¥Ùè+ÃÀÆ0;m\x0013ÚÈÒ ½\x0012-Bz\x0010s¥¼L\x000c±ä£9³ÓF8£¢4âJ@[\)\x0019\x0004eµ^K[\x001cÂì\x0011N(#*¢ä[DOb®èÒkB»#DØé"ÐE\x0016@^Iüpyj\x0002¶õ\x0012­\x000cÞ\x001cãìt\x0011Nè"«¥Ãbº0Ò9_\x0003HZH²XÏN\x0017á.²Éx·\gåd¬-Ð|BÞöµàð\x0010f§pB\x0017Q\x001e\x000ecjêÏSÚµ\x000c§q\x0010û9u§ô.¢"0Î
Hlµ¦s+yÞö¥*ÀaÎN\x0017é	]d)G×S×YÜ \x000e\x0010\x001dÖ\x001cÆC*Ò\x0013ªzHq£«dmÈmúâ8hÛ{çÜ.¢t_.WtFú©B°#,yÝé"=¡lyÐ -R£ª\x0010JºÓEzB\x0017Q@dáéAF£BosÄ{XwºHOè"Âä(\x001bydÆ¶òµv-ûk³ÓEzB\x00179\x0000\x0019µ.´»B\x0014áÞ¡GpvºHOè"j³É\x0006²æ~µ+¤#¬Nåºñ³Ù-+ãgÇ¼_]r¿øá®$Ó\x001fVs\x0000Æ\x001cKç°s´ÁJ¶\x0012X_L»d<IêN{Þ³p\x0011µ9Å´^ø|ÿó_£$ÿ"\x0007GRGnWkÁ-ÍÿâÖë\x0017o^=}¸d*\x0005\x0012$C:Ê\x001e
Â}`
ÔXy Am3¤n!õÄJFðiUzqJít\x001dæ\x000c\x000eÖ\x0003Ö!M\x000bi&VRá(\x001f)E)3¢\x0008ø¤á×s\x001273ÚÑ3&Ôr$=Cj[YG@º\x0016ÒM@ÖlYECèØ4FÂN­'"nfô-£\x001fgµ\x0007r»çèNa¬°´1´a1]\x0015¹5ÑËCÈXé\x0003n©©ê(dl!ã\x0004d9íJ'H	\x0014@\\x001ay2\x0008Ù\x0016ì?´µ;·;pi±¥\x0001ÝrotË°f¾PöúfBá¤Ûâ8\x001chë<ºß¸Øæj\x0014²Ó70¡p¢ãæQ\x0000¡\x000e\x0010qÒ\x0005\x0005ÂZ
Å\x0008d§o`BáÚô5=t/\x0003¯¤è\x001b\x0004uÀvwú\x0006&\x0014N´ò0R´Q²
ó¨×sf6Sv\x001a\x0007&TNÐò¢Hæ\x000c0Ôð×r©û(e§r`BçD\x0012î®ÚÛ­=F);¥\x0003\x0013Z'\x0018	_Àé­Î¥¬%>û¼²S;0£wâ%/%Ùm^$z¢ïWÐi\x001dQ;¶æ\x001e9¤ìç\x0002)\x0011\x0001Ä¥é¥)ñ¼A\x0000ú&ßìû\x000fß½}ñäþó»ßÿñ\x0008iÒ1\x0012©ÌEde\x0002rÖsß \K(}sñý77Ï_<yõææ¡1fxÞ$\x0000}u6\x0004ëUX`-;ó\~OåùÇÀê\x0016VO®lReÐ±KVz]YÃúÒáb»Å\x0019ZÓÒÙsàe\x000cºÀ­X\x0014
È`Z³Ô?jÖ¶´v6½%\x0015ÓFÇù\x001fÊÕ\x0011Béz­¾ÐÇh]KëfOæ¾þ\x0010I\x0011À!\x0003ZðÖÖ·´~\x001a\x0014sÞ\x001e¾À£Ûáj\x0007QØÐÂùP*\x0007As#)A\x001ftÉbK\x001b'i­\x0004`]ú7¸\x00145ç\x0001]ÔPÿ\x0010ÚæEM7á`äédµ\x0014-\x0002Ït\x0014?\x0006·×d³ª?Ëd$\x0004n¡M/=¡5k5f£´*I]æ¨ÓQQ\x000fÚ*nÎ$÷Ó\x0014¢cp;e\x0006³Ú\x000c%èBvä)ëØmB½¯\x000f:º6YuFÑÏXÏB\x0011b6*Y\³öv\x0019¥í´\x0019Ìª3jj^.Aàö2ér\x0005Á
ëá1ÜNÁ¬>Ó\x001eZyq£dá)*î³pÑ\x0008>YFµ\x0014\x0005×\x0018à\x0001\x0011ÊJ}:ÏkQÜN£Á¬JCq¢:êìyu\x001dÊê5\x0007å(n§Ò`R§Ù 9oéÎÅK\x000b\x0005WáhV\x001f¸Øé4Õi\x0000\ÛïL:ÆN®\x001aÏø¦\x0003}NÃþÁ3«%\x0014ÎnäRtv9;"¥QÓC¸&=&Óá;µvýîöó¯\x0013Í\x0006óPù>àx)ÀÂ¬fn÷ÝÕïÞ¤\x001f\x001f%Ô-¡\x001e&t(3w;ù ¢¸Úep3¢m\x0011í0¢\x0015\x0007+UÒyi|/)\x0011\x0000\x000bã[G	}KèÇ	Q¼mZáqóCçÅ'\x0008\x000bVÀ(bl\x0011ã\x000c¢\x0011ÄSSñ\x0007xµ±ìV@è¯Êø]±NfìPé©\x000eÒ
\x0003|.£ÝeÛbk_Îw+E\x0012\x0001\x0017zµ"v\x0005Æo\x000buc\x000bÓ"râqµáñfÆîºÀø}	ÂÉ\x0012Y>ÇJj~À-4ÛÌ\x0008çDÀ·¬ß}~T¿8å\x0002ç
%Å§¨ÉÝØÙ3àÖ]jß½yH­\x0014¸Ó"»\x0012Á¥û[Rî\x0012LgE\'àÖ+¦¶Àylá<\x000eÂ9n´¬iÚ)ö\x0018i®jÀ¯kæ-p¡[¹0¸r
9Þà¬ô[Ñ,¦ÓÂ­Õdocªej-²}«cº\x001eÅ`D-\x0003^ÒÂ­ã\x001bà@u»
jh[m¤Ð\x001c0]í­­¥{ \x001du\x000b]ct\x0013]cuo£CÎîLûêù)è ®Ús]¡É6'º&Ý|\x0013\x001du¤à+A¯"í4z¹¯~Ý¼Î÷tCw"Ñ!¨ùÂr³qèöÜW8Íp\x0016Æà\x000c1LpQf]¡\x000c1¤K±kcOÃÍ
]\x0018£ÓysÙX+mÆPRÍÌâÅ
p\x0008g,6õôÃo¿ÝÝÿ|÷D1 =ï­O³\x0014\x0005Ö6f] <}ñý÷×¯n`Ä\x0011Ç\x0019­¯ýÏPýÿÔ½Ïr]7¯û*|Ã\x0000ø\x001b\x001eQ2-±\x0012\x0015èèê¶é2ëÊ¢/%vtÕ¨§÷\x0011zv§=¹/QoÒOr@&6°¹Ö^\x000bX»*ä8q|DU¹ÎG, 3Èü%÷´¨"~\x0007óßw=£®\x0019u?£
Tbæ,ÍEKNÎÞõ¶F´ý1$ ak\x0014gcÆ Ü|\x0006}=¤¯!}?$\x000eH&\x0005¹xK2Ô\x0019$\x000cë3éyS³\x001arâOF\x000cìH(§ÆH®Å\x0016r7ûqûJÊæÔÈc\x0013¸ëÂÅ+	Õ8ÇW\x0015í°#P6çF\x000e\x001cFwNÚú>ùäÌ\x0016\x001dõ@6'G\x000e\x001c\x001d[j
QXdp,\x0018)\Í¿7tXÉÝÜ¥l'o¿FC)u]'N\x001f½ª\x0013_ïxvêÐ!Uâç6oN¸¹ªuzXn´å{\x0019e4îd^Ü=~ùõîãÃ¥ì¡BÝüîìË³Bü}ùqtFpõÅùõ×çW\x001f\x000e\x0015¯ºAE>¾A­æq\x0003]SÐ6j·¦¾pÑÁFÀÝHq\x0004\x000c¦\x0017PS*áÐ
©\x0012¢¡Í¨
?½\x0019W\x0003J+/lE'¡pº\x0000"¢8_\x0014\x0011½*\x000b|¶_5\x000eáòPº.¸è­éS©$»pg½¡Ôê&<×â¹^<Ìf&:iôR¢ó\x0014ðX©g´ÝWÝ\x0018\x00197Zö\x0012ÊÀµ\x0018(¥(ò×u1¤±0ë\x0011}û}ç7\x0017R8$ñZ%3"¦÷2âÌ{J\x0007!´ÐM(¨I*\x001a\x0016×,$´<î\x0018et§Ã±\x000eDß"v\x001aêÞ\x0002úÎØ¾·¢õ\Ø&ç^×W#l¾3Èîï\x001cï é´¤¶\x0008\¯ ÍÈx\x0007¢k\x0011;Ï3\x0004ÃjØH%W	Ñ8Þ3å*ë	UóAug¤~0XE\x0008U\x0001\´×K¦]CÓ½(0\x0001µFÍ\x0015\x0002,6qf6ÃzÂ6fÞ \x0001\x0010§do°\x000f;Û\x001bS6Ì6Z
¨Û K÷F]àãÅ\x000f3f&òGw>¶7rFê|=¢jÂ\x001a­:ã\x001aðÚreÖQdh\x000f¤é§fv!ú\x0016Ñw#*_\x0004Z£wÖù0kO¯¡VØI¡}¡q,øcï\x000eÔ\x001b^\x0003´å\x000fMáÐ[÷¢\x0011Í^Ä\x001f{WÑQJ6é\x0005Á«ÈÂ§n¦\x0010j="4çÙ@ïyöBQ?W\x0013|£O:°,èA¶Ù
NVw"b«[.x2\x0001Ç¬fB\x0015x+Ê7ÕV6¢"8\x0013Xí#n@Ln#"x~\x000c
s/>ë\x0011¡Ù\x0016z·¢Ó@Õ
\x0001\x0002N}KÖ\x0017ÂY}¾Ùøc'¡´\"\x0012D\x0012×OÀm\x0001fªÊ;\x0010mh{\x0011b`\x001fw"\x0010!ëß\x00055ó"ºÐ\x0010ì#´Nð"¢±ù8«R"âÝ\x0006ÚjÄÐÆ¡?NFÑq£Ð>æ Tïð/·²®U" @SLëmc\x001d'<ùi§tFI}
¨±íÛÀ/_
\x001c®ï>=Ü?.%À,ö\x0008æò\x0006ì¶Ì)EPÜÝ/ÂDc\x00037\¿½º¸^æ\x000f\x0006ø¨\x000f+þû¬ \x001e\x0001)Ç\x001dãÙ:µ¦\x00064Ý:'t\x0008sð øÍEøùqèkù\Íçzù| \x0001\x0011\x0010¸\x0016\x0014Ïî\x0010nbÄL'`¨\x0001C7 Pô\x0013ÎY~\x001eðq\x0001ûæ>@Ù\x001eî3â\x001c=í&BK¢L¼zhé$l\x000eì>%NR
'íBêäW\x00066Ä]8?{-asJd÷1qÅ/.r<Á\x0017ÀÍ»P6ÇDv\x0013\x0014Â'C\x0008Õ
ò1	\x0013ó\x0005V\x0002F¿ôCSþ\x001cÿ"?¿üõî·ûOY×æîä»Û~ýÛ\x0012¦×eX\x0003¹
4öÂÐÔUÓôü´¼|}þæâm\x0016·9?ùîìåë?/ÒîÒ\x0010HY\x0011Z_/PÊ,{\x0017+hÌ~âàÀº\x0006Ö
ÂFóÈ- ¹å×Ê©x\x0003\x001c
Í>\x0008cû È¤Å\x0016Ø&ÙR\x0005/ý\x0002Á\x0010m³´ali1^\x000bÔö\x000b<@
lé=~âr3@+wÒ¥H?âæÁiÚ%©ëZKò\x000e´?ÊV¨ê¡2îèêFC iuG
YkÊ1\x000bÏ¸\x0011\Ýì\üq\x0008×U¸Ê\x0007Á\x0001']d\x0008pMkÆpµ¤\x0002Õã­·lÛÐ\x0008­m·®\x001dÜºÁr.Fg=pg,ï0 \x001eÁmM®\x001c´¹XÒ'x/ðPÉx/\x0017¹0¡*7»Ë,$\Ì,ôãºxÿß­n`Å6Ç2?ûü62Ûn\x0006?´\x0019\x001c>>J¨_¿\x0013®weu'´FpmpQ\x001a\x0004\x0017(¿hUv\x0012^X[hrÒ\x00144´øã\x0010-6Lñâ\x001aÞº~÷Vu\x001c£[½@'Z|\x001e¡ÅRh\x0017²^o¢u\x000b5ÄDêXÜ¸+ ¢Èñv(\x001a3\x0004<SåA5\x000c¦l	ý´.\¡óÝuqÔ«B¿}úe\x000f|(Í+1Fe	õÌN\x001b¼ùn\x0005®©t\x0007U¬hí]@Ó_Ô®Gn¶Ðw
­±l\x000fVÿ&ÙÍUô\x0019ÕL¡Æ:,_cù\x001e¬¢â%,pÏcP<BÎ7¯Àª[lé}^Åe%	Ïèà=/wþPÎf\x0005M\x0015Uô3\x0016\x001bÁÎÜ|¼=ùþáKè¾,ÕÏi,é4ä¿ãÍ4\x000bo
g\x0010äsz~ryvòýÕ\x0005Ó}8T\x0005ÙMÃn¶±{W\x0002;ã±³ ±óØÃè\x0017æï$\x0003èÖÖèÖnA÷ÂqUµ¤ %âÑõDå\x0006ô kô 7¡cLBvÝ	ôI]q?´Ò\x0007\x0012\x0018ýì²ªK\x0011¶Ø\x0004:\x001fT©hüðÜkÛh>Béb\x0017¦½o¥$u{ßzyûøÛÝÇ%S¢Qö%[^ë\x0005¥Uð\x0014¥\x0018\x0019®yGúòìúÍùå2¨lAe?(8È)Lc£RWå5×[1\x0006î\x0006­ßÍþ%k%¨äÉÍqEÙÃzÅ\x000fx&L¸²nNg\x001aNgF8%O\2¹";²b¡ñ\x0013O;Ý U#z×\x000f\x001aw#O)4:¥à\x0012¨à®y\x001cã¾\x0019TU\x0014\x0002g.\x0001Pl\x0000ÎáÁ2°\x000cê\x00029»¸\x001f&Ê\x0010»AUsðÇ~P<@´¢²t¶:ÇSèOï\x0006f&å¾þ\x0015Ü\x000c 4ùÑ\x0015I\x0008zè>½\x0016Ô· ~\x0004Tñ|(£¤T#(75C5¨nWT\x000f¬¨F¡W²÷ø(ÄsÖL±÷Û1}{üÈQ\x0002Kék£Ì\x0002
JFû×S\x001eÌ\x0001.ê}í{´ïéE({þï\x001e>}@w'·Oÿyrùð´bãbn\x001dLyfåUc?ûØýÿwWo?Ä¿<?9»ù·Ë«S\x0006ô¾ì¼N²ó[À\x0013<tØÉ¯JÏ3Ä\x0004L\\x00117ÿ\x0012¶þ%ìö_"Æ2\x001e<ç\x000c½äÂ=\x001aoþKøúðGø%+â/ah$3HÒ9Ñ!Ld·þ\x000eU\x0011¹ÎJç	ö5ñPÜ*)=w\x0016©¬Ýæß¢9Øò\x0008';\x0018Ò¥ÕX8F#\x0005d _ü\x0016³\x000fèã¿Es²åö£Ãd<m(¥0\x001e±¥äWv9q/Üü[4G[n?ÛñNKuÃ:D7aó;¬Rn¡æ\x000bBÆælËíÛ\x0002\x0017hG_QFæ¹\x0005Bãï(ÕnµýtãoáUþ-¬àú03_è·/¿\x001aÿ-Z·½ýt[Ô\x0014àßÂFNü-$ÿ\x0016f¢ç|óoÑnuÓç~	I\x0013EP9¿ÄÄ½søwÐ>Ï*wÔ
°SQsûøÓ¯·_VQNSJS/p°T\x001eW{öbBVeÔß]¿|}öa\x0005¦ª1Õ\x0000&(zð7Î)\x001aß\x0011ï¥Ü\x0005<ULÑO	5%ôSB¼(C^L\x001fÍ;¥HB\x0019´èçjû0u©G\x0016SPq®ÁqBü\x0006á9«îæZ\x001eû0Mi¾ÚÕ´5¦\x001dXM\x0015¨k\x000f¥\x0012¨*)®¦fý\x000e>J_Sú\x0011J_\x0010YuoEp~ÇjÄ]à\x001bF\x0018m\x0011õ@I-z±óÂ0çñ7ë9\x001b[$G2X 9- ç+<¿þDÎ#lLÙ\x001cs9rÎ%Ð2êc`øm;kf£`6çG\x000e\x001c |\x0012¥Æ\x001a\x001f½\x0011)^\x0006\x0000VÍPs2o«8\x0005@ë)ÓûZóF\x001f=}rúÿû_ÿ}\x0016E)â
ÝR[;Vo®+Õr¨evàñ;úùäòO\x0010þÐ+\x0003¡«\x001a]ý¡Ð¡F?\x0014º®Ñõ\x001f	Ý5{ÝmÛìVSjJ\x000f¥Ì#µ\çaÅÁ2^t±«NIð¢­Né¦±Nä±\x0012çA\x0010¾\\x0010&&f\x000fà+¹\x0017ãlVgíöÓÏ·þåÃÓç/w·OKO\x0016\x000b[¹òN\x0014]jPhGé³·ßÅÿäåÕÍû\x000fçg7ËèªFWÐ¥*\x0013 Q´ÂhÍè:Ìc\x000e¡C\x000e[ÑM©Â²É¹
\x000bfôrFÉuM®·\x0018.[\x001e#H¬7^¹ KÙùÁÏCè¦F7Ð-Ð«=à1NÚº`<Â\x0013E[È]Mî6\x001bÁå5¨ÏNä\x0016xd\x0007\x000e :&¹¯Éý&rGÃn-\x000e±§
ñ\ò<\x000c1?Þi<Ôäa\x00139PC_\x001c-W4i]&üÄøüäµ
`u¯\x0019Üè\x0017]k6éÚsY\x0010È\x0019MQôÖ\x001bmrG:*{T.Ïª½\x0002<þÙ·1ôÆ\x001bÉMî\x0008ÍæC
l\x»$i#7¾HnrFF8.Åÿ
\x0007+´(\x0013\x001c\x0002ÈÆ\x001bÉmîÈ(\x0016\x0017 éí,FÒ¾Äa\x0011G5²qGr?R\x001b`\x0000¥´ÉÄ`\x0005Ev¥~FiÝ6ìvuôødlÓl\x001bË\x0003Ð´æ\x0002\x001dt<ÈÞ¸$¹Í')oö\x001d\x0002Ý5\x0006õÑGvJª1íji²°Ç?Òô®øG¶3î¸ájÃõM\x0006Rc[7ù¥\x0010¸ä\x0013J,`ëTcfÔ&3£½få9Q¯ÏQ/5\x0019ýÈQöæ¨ªMGU\x001a4Å&+\x0002¿½àÐº£^6TsTÕ¦£ª=P\x000e4ý±´e\x0002\x0017ÀaÕà^vh*l:ª:?tåû§@ÜîeÝ\x000fÌ\x001cbo*le/{F\x001aÊéÆÀÙ¡ÇEo*l\x0008¤+Yhe\x0002[HÇåSñ[Ø£
Û¼j\x0008h\x001er@)ÿ\x0018\x0011ð;eæ§\x001d\x000e±7G\x0015¶yUã9üUø\x000cÇÇi§ÊlÜ\x0019qÎ^ö\x0018Ç¤ ¿aËÐ»W÷ùô°8ÎGÆMBSUP´,×\x001a\x0010<\x0006AL4v#ë«ëWo¯\x000eòIpU\x0005'j\N8O>\x001e\x0002\x0016j¢\x0003¾¡ff¬¦s
ë¤Tè\x0015é\x0004)ñ(ÃQ«\x001cÖCg\x000fk:?l¹Ë@\x0017xªv7Øîé@n£s¢¦s¢í\x000e/.ÖN\x0013ÜTÝh\x0017\x001c4pÐ¹t\x0002'½d8
Ã	N\x0004^:=ÑkÙEg\x001b:ÛI\x0017È4FºÀ\x0015$Fñ&3\x0013³¯óÍwõßU\x0018ª\x001bÉÃ·hÓ\x0019^¹\x0019ÐµlAÕlAu²ijnLâÄÙ\x0018m¢±¾MîáN;,²§Hp1\ò4\x0018l7fN¾t-^U}x|\x000bX\x001745`\x0002ÊEÒ&#HÖ>âm[<hé Î[ê¦Õ¨·¹[<2'JL\x0014«öàÙæL\x0014IûµxÖ=Ñ"^³©J[DÓj®°f-^hÜ\x0018þØ\x0007
S£	O\x000b^ð$\x000fjRjf¶ËJ<%\x001bc¬d5\x0016ØÚI«z4¾Ìó<?\x00053Óx×âAóq\x0015t~\	Ü= t \x0017,\x0005XëAx3®×â¹Ææ)×eôLp;4\x0004NÉ{\x000f4\x0005Ò\x001aÛ\x001b\x0006ñ@î×yH|=ûøñ\x001fÿbçw·?¥Ê÷¿?<.×¥¸ùò\x0003¬Á\x000c¦ÊOÇRñS=|=»¼<Oó»³ë©@åý»«ëÃå)r¿ÆCâëë86
	Æt\x0008iõIE#y¢Ø\x001c\x001ajhØ\x0002Ç#%n_¤½¤¦\x0001\x0002FOT¨cë\x001a[oÚ"ËR\x0011[ÒrÃú¹¥\x001aÇ65¶Ù´ÚD0øjI²oÒHª\x000cÓ\x0013)âql[cÛ\x0007\x0014= KàÒäÍ-ºÜ®æv[¸Qò6·R¼KàÍ
S\x0007Ç¹}Íí7qóÄD=Õ&PÏ
÷\x0000&eé£qWOh¸Å\x0006ðè£)Ód@x\x0014\x0001Ê\x000bn
\x001fÑ\x0008ÊÆrË-¦\x001bÛrk(¶\[ªU$\x0019hÀ¨#îoÙXA¹Å\x000cÚ2C'^öX¦\x0005\x0014AÀWâ#qË=3~Þ°Å1ý¥VÕE\x00006)I}-úO·?ß~þòx\x0000ý_Áÿ²ÅÕ{|XMôÅ\x001a²\x001e¨T\x001aXt#ö¢*#*
ëÈ|yûãÃÓãÝÓ¢+h\x001ex®ñ¾khâ¹q¬Äl'ZM¸AææäòìÅÕÍõùÍA¡Y±\x0017KEX5\x0008KB"\x001a§;S¶7{píDÁæ\x0010+Ô¬0Æ
¬)¥±<;ÖÃ®íH¬ºfÕc¬¨Ü\x0019J¿!-	P¼	ÌDÅÔ\x0010¬©aÍ ¬(- ±g&+t(^X5ÑÛ1\x0004kkX;\x0006\x001bï¥VVÇ?Há¦L»\x001bbõ5«\x001fbU!\x0002M¬\x001c´r>ð.\x001aA9\x0002[\x0005\x0015h·ÄàÊ\x001aJ\x000eÇm:ÂóÒò¥J¨§ý!ÚÆpÉAË\x0015¬´\x000fPh%ËÊ$1 M´z¦´Î3¥/~ûýöóç¤çýÿ9y\x0019ÿ|¿\x000fÐNpiu\x0014Ó4nÙ»±7ïÎÞ¿OºÞç'/ã\x001f/\x000eä\x0005ôþti§KÐÚ\x0018ÉÛü\x0016ÿg¸<8Âò¬\x001f=!Þ:D\x000b5-®mQÁ$iN`ÄµåÑIöî(´º¦Õ´Àz)ÅfIíMp\x0015pÊh\x001fÖÔ´f6º\x0006 ©OÆsÝõ\m-¦ôfºhQûªóYØaõ·Ï\x000f_îWD¹<ÁÁHLMSË2³\x0006\x001f	çbEì±úóÕû«\x000f\x0017\x0007£Dµ\x001fx©:ÕÁ\x001aã-nNÅa¦\x0013sÝ Q\x0013£ªFP¡F±eyïkÒ\x0006¾\x001fÀ½Ó
&ÞHFXuÍª\x0007·?´ªü®÷\x001cÅ¨\x0013/\x0012]¨v·ZÞ­w©£þeô^?ÝÅw/w'(\x0008Íª+¨æ3U
×/ÏãO+XUÍªX± \x0002h<\x000fVèz
dX5ubxÐ\x0010*Ô¨0¶¬ÑwÑ»E´R¬$\x000cÅ\ñ?xp\x001cÕ5¬\x001e¦2ÅèÊðºîB®Z!TS£±-\x0010\x0003\x0001GÒ¹Þ¾r\x00158äTßÍ\x0000,ÞçëuÕvp\x001bð\x0018;
ÎN\x0017¿^\x0005s]`vC4ÒÒ\x0006ñuÒ}\x001d
u4êÃûÇû»Ç7\x000fwÓ¤q¸§¹g3a2òrX0QZw\x001b^\__¼¹º>?8Wl¿£Ù@ywÿS\x000ca\x001e\x0016vÑ\x001eäæpOâ³ó\x0002 P\x0016\x0013y³÷Åw\x0017\x0018¼\-\x0013ªPõ\x0013\x0006Nã*\x0014¥5È£»×|Z¨kDÝèå\x0014\x0014A§¹)P\x001cÕ[MhkBÛM\x0003G(©\x000c%\x0002_\x0008§F\x000cô"ú\x001aÑ÷/b`o¥=	çãd\x0000Ùu\x001e\x0000ê<ÀjÄ"/\x0019\x000c\x000bÙ\x0012£
ü\x00142Ñ\x0004ÝØ\x001c\x0016Ù}Z\x001c\x000eBe\x0015\x001d
A3\x001c8G«9{ï_fû&G\x0002·7ÿéîöÓÉ«ûO&x:-3@\x0002]\x000cè\x0001¥:?{{òêâêí
DU#ªnÄ ËqÁYç¤ \x0019¨À\x0010<íE\x001a\x0011º\x0011q$\x000b\x001d\x0017Çµ 
\x000bÎÀÌó\x001eB]\x0013ê^B+
«Æ*T6&Q2Å¹H\x001b\x0013ßØÿL<ü³T»r®µÂr,\x000fÀ#s\x0001ûÊI­ß¿\x0013y>4ïn>ÿvÿñîäûû¾<,¥õ4êÆ\x0006eÏVpPA²´¹.zwvsy\x0012\x0003Ëóï/^~¸:´û¢¬Öó	êæ\x0005«y\x000e^<=Ü¦«d\x0019\x001cägº\x0007¡\x0006Ñ\x0005X<\x0002
\x001f)rg\x0005 \x001a1é-¨iã4\x0000¬k`=ºÂ¨D±f\x0008è\x0015Jq2r®\x0006r×Ô¼ft­ßâ±bñ¿\x001cX `j Ï °­íè\x0002\x0007\x0016h§\x000b_æÓújËë;\x00159
òº×
ò\x001aÔl¦\x0006è^¹ÕYS\x0015û|£Ç\x0000°¯ýð\x0002{\x0011<\x0016/^ñ-OÉÀr$ÞPó¯«Õf\x0019à±3'%LÅ%vX¤Ø\x0015£&&Ò©Ä­\x001bõsÿÊ5n\x001c\x001cõtZjzÌC°ãHÝl´Æ3Í#\x0003Äã£#º2\x0014\x0008GSfC,XËAI=];\x0000Ü\x0018b9j2 Y\x0018\x0007\x0001â\x0000ÅuÌT
\x000f\x00107M6mâÞ¥§Ëì"\x0000Í}0sÕé'V©PÃ¦Âº2¸X³Ä*ºç2)Ê\x001eË\x001a«6Â\x001c>x^\x0015ãf4Ëcã\x0010sr@Ô qsðÔèÁC\x0003CòR>ò*>\x001a\x0017ã61Â¸\x0018¼hO\x001e`\x0007UÑeDiã?=}þrÿÓ¢v\x001a:åÜ\x0002ïb(KJ¬ñÔJ æúuñnÞ¸xy@2@w]é\x0008ZºÒ»@\x0007CC¼UÞ\x0018^â\x0018TO\x0014 \x000e4\x000cÚS\x0002µ\x0012\x00177\x0006AmKÂN<\x0018õjUj5\x0004êIW\x0001|t\x0011I\x0015Â¬xh\x0017)4¤0Bª-÷\x001fzLpÒ\x0013 ùÐøñ'Þ\x000bûIm³¦vdMe°Tl
(ÃË_\x001ftÞ¦1\x001a\x00154î!uº&uzhM5	Äÿ	ÏÊ±NP\x0016s	¤ñÐ§¯¿³ª8\x0017¤ÑØ|óðô1ÿéõíÓÒ»K¦ÌÛ5)ø\x0001Y\x0000C\x0015´zßÞ=¼¼¹º¹Ìz}vsèå%sW\x0002QVÙnàö\x0012[¡\x00137\x0004Þ¼¶ô»»©úãQn]ÚÃõ\x0016b\x0018Üx¬Û¢\x0005Ç)k¹@V*à\x0005\x000f\x0013\x0017ap×»
à\x000eÓ|ù\x0019Üb'?×
àgðø«\x001d\x0012\x0004]\x000bnÌ^7Zü\x000bÌý½»ýüùö/¹vãíÃýç»/÷wÏ Þ8\x0016¤Zîfí²p\x0014\x0013C\x0002±ÖèìU.àx{uñþüÃÅùõ¡§P³×ÔÈ0\x001cwvîµÒ\x0008Êÿ	ÈËÂ¾^äxTR¬³»Ý«¬8ÑL|óðéai_Ã\x0019Æ$>n\x000c¾;B\x000cA\x0003\x0018\x0008\x0013áo3:òÍÕÛ«[9(@Íúl@ê:ÖrG66À©Î¨F³»¡\x0018@µ®Fµn\x000cUQU_DM=[yY)4ñ¿q\x0014Öª+5²:5Äyõü\x0018`- ÎBbU\x0005Ó§¦ó\x000c°f\x000b±-I\x0007\x001a#w\x001fC¬<Ñ\x00033\x0019×³JÕ\x001e-5v¶d /gp^M¼T'Xàñ.Ö\x001f\x0010a^\x0003\x001bìµuÍ4wwO¿\cµt$ÿ+Ì\x0019_°'Æ\x000b;siG{õîüæÝåu{JË©F0:Í\x0003\x001d8\x0008ÍË\x001bA2èÀr\x001f(Ô 0\x0002*4)ûJÅ\x0002PÂ\x001b+ü$M'§®9õÐwt ;ØP¹ëvf};AM
j\x0006@}´÷ìU
\x000fs³,h\x0012½êq>¼­9íÐ\x0017;÷O«©hÆ%î£|vWSºÕôÊ7­ÄI\x001etàEyB¹±÷} ¾\x0006õÄà¥s47~wVõ0§ûÖ\x0005º{uH\x0006T\x000c-©¥1Ñø$Um ÖË'³Âî¡Ø½Y\x001eon\x001fo\x0017«¡\x001d¶3[[:ÉÓgÇîqîú\x0014ï\x0000g×g\x0007k¡eH·ÛJj,d©±§/é&~\x0019Iâ¢âd±\x0017\x000f¸ÆEFÒÎÂ057\x001b(ai
o´R~âÔ_Ý| \x000bùÅÛ¸¼8TìÅÕ2·¬ÞöR`í7cò\x0000\x0008<PÆ#ÞÕ©£\x0019ÂT!ï0¸r
8JFÛÝ+ªàä`ãO=\x000ccú·\x0002Ç\x001fÁqø1	áâg­°¸³\x001d¯ødÞ®\x001f\½wë\x0008Õ¬÷?þç÷\x0008¾d-´óTÃ`\4\x001cäÏ\x0011<J)L¦*¸çï"ï7·?Ýý>XÖE$Z×Í\x0018pÞhb\x000c<Z:2r\x0017¨\x000b\x0013EûK+iMiÍ\x0000¦ee\x001dãQ¢0§|ùIUÓNÌj²\x000c~pÙ	Û\x0010Ç\x0017
¥RÜ¬ì§tc{)¡¡¯R7zàc.(ã\x001fIç"½a\x0012åTê»\x0013Ó7é¿ÒÅôÍùñ#çGBi\x000f©~1QZ¾Q{¤Ú\x0019Å\x000c_çbÊêÕ\x001eQÒãa/f¼>KÞ®Ì\x0015-3ÝôÔÅ¯\x0013Ó6\x0007\x0008ìÇÔ\x001az7\x0012\x0007\x0016¤>#Ç	o¦¦CtrºÆ\x0005áýJrºÇkÁO±ñ<¦UÃD`ÝÇ© Ùøc7§²\x001eSê¼;IZÐÙÝî<\x00146­Ãô\x000fÂ\x001fû1\x0015çÓ#¦%Á{å$äá\x001aoþìÐ\x0006Gøc?§ô¬\x001595¿²Xç\x0013¦j<;9j8±¼ªSFYÖ3\x0014aä²Ûm\x0012¸Æ&\x001b°IR\x001b¼âó!ÊýðÊ
Ö\x001eWSæ\x0010áýRp?WQÊ\x0018S<Ñæ³®eóÑµ\x001cøè"T\x001f];k\x001dooêÖ\x0013é\x0011O\¦|w6*Å<tu^G©[J=Bi\x0005
äoî©×MÅ{}YÍÍ\x0006Ik×b\x000e\x0018$\x0008Õ\x001aÊ7\x0017ýÐ\x0014J\x001f§T¶áL?÷Æï\x000bB¹Û¬&\x0011
@`5	;U1Ø	\x001aL\x000b\x001aúÃN£¬áÉ\x0002Â)ª\x0000ZqÆlº$¨ûvÙ4Ëä\x001bfêé¾dJ\x001a2\x0018¿QÄH/\x001b>ü<mvOêæ\x0015çåÝãýç59HcùÈ£D\x0003µ¶Ê"4fÌLÑ3f!___¼?dNSs!Nîé \x0002Ë\x0012\x0012¨å+{üÛù÷¦\x000ePWº¯\x00184Ô áë\x0005í\x0016\x001dÛ£ÿ\R'ö\x000e\x0013å0½¾}|xútòáöï÷w¿ü²@\x001aÝ:U4B\x0017\x001c©ãYñÛÃÌ¸×gñè¿=ùpöï\x0017çß}·ªjT5êtAÁ\x001eP
³±üð\x0004S©º\x0001T¨Qa\x0008Õ\x0000Ï\x000bÑAQ\x001c¨À«:ýõ{Au
ªÇ>¿;Â©¨-®¼K\x0013¦_F{ImMjÇÔóJéU©\x0007\x0007K¸ÒÍ\x001c\*lª2USü\x0006ËXAêÅÝã_ï>.VDh¥åBQÞAÄk\x0014\x0017ÛOMécù¨\x0017ç×\x001f^_\x001e¬ÞÈ¤\x0016jR\x000b#¤RñË#`3Q\x0006ÕeðQèÑê\x0007
Í¡%ÕµÙp2\x0016ÕÖK\x0016;SaâÖÔ
Z\x000fÿ¥fð~Òhú5õT­²ÌÞ\x0008ù\x0006P}ê\x0007PUpevTð¤Ëÿ
~w@æl=ªiWÕ¬ªÎM»\x0019ÕV·Àêú£Î<&eNÛ.©ýz\x0014_Êë?\x001fü¯Î\x0002¨½@\x0005Eª7}\x00149\x001få×Ûe=d\x0014³\x0017\x0012<f\x0014G>ÇÉÜCuïñ]ÿåë³jÈ\x0015êúo,ghÓxÖ|å\x000f2°ÆU°¬{\x0012&pûhe\x0012¹ªúÃ¤Jýa¼\x0005\x0008g9!¥<Öåþ\x001aGóp¡\x0011-¦tÉy\x0007ÐÏî¨\x0019\x0013d	r\x0000\x0013\x000cÊdÌ@úéÓf\x0011s"
Ùi\EÝ6õªå6\x0010A©ø¹)
	ÁO¼y÷súÓ|õ@¯SòGW\x0005s^=t\x0011óÇøÏæuñEügz]üöî\x0011õ¶îN>Þ­ªx\x0000cè\x0018Y\x0019$=E\x0017¢9@E}ÎoÏ¯Qi\x000bs\x0012¹ÒaNº}ÇùÃÝ\x001eé]7*ªÍ{JJI\x0015©8Ã8V\x0007\x0013\x0013u<ÏP\x000fX~»gIÑP5Zfw??Ü/õ)Ç\x0000~:k°`WÛR»?!ÅZÉ]¿uq°«Ò¶×($\x0011R¬Èp¤Ã\x001a½i<9\x0014<£C?jjT3j
]¤D\x00108u6îômÃD;e\x000f©=G\x001aÿ\x0002?ÿ÷\x000f÷w'×\x000f»ý¸täc\x000c\x001døR\x001aw<ÌH_6èÔëò÷W\x0017ç'×W>»<droZµ7±+õoÎ¾<<¦$äÁ<ä»ñÂ÷ÿ÷äòöÓ_\x001e\x0017\x0005\x0002\x0015V½(sÆ¼¸ªè[¹8gÊÝ|¸ÊYÉøÿé·ç'oÎ/ãõïìäòìí«¸Ì;cÀ(¿H#°ªÍ\x0010ÍM\x001aúÉãY½ýí÷Wwn\x0017«â\x0003ú¨KuÒcµ,n\x0008ËJ\x0007Ñ*ÌL\x0013Å¹¬¯ÏÞ¼;°oÏ>ÌãÊ°·è2&¡úëí§/O~þßÿúï«ûÏw·Oÿ¹ä\x0013°Ý$¯¶\x0004`!aPtÚ\x0012SÏå´z}ööÃûoO°±çìæß¹UÍ­¶q+k6\x0018Ìxâv´Kdm\x0010\x001eá\x001b¶p;!15\x0017¼h}\x0001\x0004VCFIãë\x001a\o\x0004§Õv$Â¬;eêÆ©MMm¶Q»SÚ% ©,\x00005\x001bÊjÏ
d\x001fâ¶5·ÝÄ­$ÙmÇ$\x0014­e
Z q¥\x001fÜÕàn\x0013¸¬+\x001ehÅqf,ïï#rûÛo[pêk1ñ¿X6\x0013¼Þî@»H?w¨¹Ã¶õ.2à*F#dN¬,\x0007óæ{×LÜØ¶Þ\x000eïs\x0008.°\x0006TL¹\x001eÛH{Äý-[¹ÉaâFa\x0003.mµS,L;×ó?BÞxL¹Ée&ÉÓÀ	\x0007\x0010öm
jÙ\x001c¼ñrÓ¡	)¡beÉ[Éâáö@×Y?yã4å6¯+Ù\x0001	mOYÂ\x0015x«\x0019a¦1ðÆoÊmS\x0015©faB	\x000c\x001dÉ¹©³cäçÛ\§\x0010$òg\x0004poMUxè^<µÇ$o\§Üæ;AÓ¤ß¸æª\x0008þâvËQ­yã<å&ï\x0019Ãqðlp\x000eYó\x000b¼æ3JcäûÛü'¶/C9 @æÜë²æ³\x0002>\x0003äªñ j\x0007µñXZ\x001aS`\x0004åpãÍM\x0016ò\x0003­ýä\x000bUÛ\h¼øhòýesP\x001f¼O¤ÇÉÛKç¶[§)ÜÂ¸²Ï]Ys8TÔMÞ¸PµÍ*Ø9"Stí-ßdª\x000e?\x001ayãÔ&OÎYÆ\x0017GÞñnAÕ2¶-3% äù5p\x000e»1æj1·X\x000eD\x000b\x000e
ç1±Â[EÎ(Ã-xc\x0012Õ&hä¾34,Jó&/vå\x0018§S¹½%Q-ùÉÇ\x0008üÿç§Å\x001c'øèðÅ®l\x0012Æ½¦¿Ï\x000cïÉåÉùË«ËóEJ\x00105%\x0001Jç5)^¦²å\x0018}'LÅSü¼ª©o1§7/1êf%õÐJJ âB2tù@Zà\x0003ª{+WÒ5+éFVÒËRYí|Jo'L®	v^Æp-¦j0ÕÈ\x0007\x0017Ç\x0008Å3U\x0004]¤`L1{Å])wv\x00161åÎÐöp\x0006ÍÇ'é$ÑÆ\x0004`0!<ÓÉ©eÃ©å\x0008§³Ü\x001béâõ5^\x0012òsK(zN³ñÎjN\x001b\x001aN\x001bF¶§rØ^8u\x0012HOÎ9~Àð¿û®º*q\x0006;Ä\x0019ïIôX¡°ð^\x0004ù±ÂÌ¨Ã.Û#rIå\x001a­Ð%é\x0006ñü/\x001f£3Z~½\x0002:BVjACZâÅEêÏÙK(2¾ºNèÀZfÎ~\x0017r\x001a\x0018á\x0004QÄ<°[*j,\x00141©>¤NÎ]
rZ;´âTÑ\x0001\x001d/õ\x0019ß\x0002¥êé¤¬ì{xfß×®¦â¹
q	©	:®f©ú4³\x0017øõÁ×ÁpÊ@-6 ôø\x001fm\x001dExVºÙ@i5gÕ¹«\x0002wîöÆNSAEàzoÉc·p®Ä!´\x000et\x0017&P\x0015\x0006@U¨Äí%\x000b¯Ë2\x0011e3$4_=UPö¯¦0Ô1 -A*ÖATbFº¼\x0007t×Â@\x001aYM¾u\x00027\x0010CVIñ\x001cj6ß»\x001aTÙæ³+;ôÙçÖ.\x0000ÃæS(\x0014Ä\x0001Ø\Ñ*PØ½\x0001 (H9\x0002\x001aC:\x001f\x0002ÚâáG\x0019XS\x000cZ6 |&¨\x0016R@â@à|}«é1Y \x001dU£a-õ²3:H	-%\x000cQ¢¸	UL\x0007t	²\x000c)Á¦.HÝBê!H( @i\x001co(Y\x0003ëº7æ4¥É\x0003â]¥ÍZ\x000b¼½ýrÿði¹ÀÇ\x0004\x0010¬~+l \x0002¸\x000fé½U+3+\x000fôöìÃÅÕÛ³Cá&QzQSzÑO)ü©WRsó¦R¦PkÚ]M)woeH)w\x001dÐ«1}pt\x0015Òñ>
¹ÞT\x0001O'Ubj&W'¦×
¦×ýÎç¢Tq5îâ¥z*>ê£Tº¡Ä\x001f»)­Ê'\x001cÒ²fÊ\x0018(±z\x0012è¤4ÍñQ¦ÿüx§ÈZ÷æÅ)%(æÐÂOM§éÄlÏ\x001a8@Þ\x0008z\x001a\x0002¹´Õ\x0002ãÑ×)¡\x001254äòý¨Y!Q|93RV'Å­ \x001bF\x0003IÅ$AÆH.dÍ~¼êgJ9«c³²=â0rÄQ\x000f6Ï@À*SRÛ K­öTýO\x001f¦n?¸\x001eùàRP®\x0003ð!\x0014Ä¨xªÞ
L+D[íhØ\x001fåüé\x000b»ô³Ç~],·ÂR©¾UÎðÀR\x0005²Lñ\x0011ó*Ë8Ï9þurîØ«1çÛ[ÕÜj\x001b·VXÜoî<\x0013(N*a\x0001÷¼y/7ÔÜ°[2
Å\x0010h½u\x0019W¦ÜÁÂó.n]sëmÜ1âyZîxÑÚ\x0018îåõ\x0007´ã;±w\x0019\x0013Än'!ôsc8¸ËiGeªÌ\x0015\x0008\x0007kÒ÷À\x0017&¸v«¸%F\x000c½.õ\x000f%Û§&Zh;\x0017ýG\x0016DãÄù,êÿWWzklQÉÃÀL\x0008öÔP\x000e °Ìp.ó\x001cuE÷qQS\x0018
 ¸oÒäÏoï>~ú|òòá)þf\x001f\x0017³\x0015ÑÀåþImðÅ]\x0002
\x0015eè¸Ç»ºoÏß¿¿yòòêæúåùå\x0001ëüc¼»¤». ñó£«»¼ã	\x001e/\x001e>þã\x0016Ó:M¥FiîS\x001eö\x0014\x0017m[
!ö9/ÏyrÇë!uO\x0016Ë\x0017ñ/ÎeÄ\x001c0Ã\x001e3å\x0019UrÉE\x0011m\x000e\x0013Å"tõ±¡CzÊÛ5ø¡¡Ü%Q?<>üm±Âzë9ñ\x0003ÆÑ¤I\x001dÞr\x001eÍÍ¾|¸¾úóù{:<é-ªÚå"\x001bþØ\x0007çP\x000cº»âÍ_RyVà\¹Õ;_f«ºyÍú^¶]t ±·ê\x000cmé<KAñ oá|/
¦\x0008°C \x0001^À³¦°­kø£l>*ÈÞj=Ðx©øý,¥\x001a\x0001pp9i\x001eMÌX\x000bge\x0003ge/1¥£Ì	.\x0008T¿ªÐó/]Ëp¶³½p(agJc^ í©Å9\x0012ÏVÎ-ÂiÙl9-{·	¥\x00133î_RP\x0005%9K\x0017­ÿ8Üë¶rÑñcVô\x0016deà"²à'"µlÆ4²ÐûUâªÂ­ôUY\x0012À\x0004§g_\\x0016á\sXñÇ^8àÊ¤ÈÁuàE\x0013ñ[²JM#²á\x001fÕ\x0008Pi\x0002Öò°Ò\x0017÷a\x00045q]3!Á\x001f;á\x001c_Â\x000fkè¤\x000b\\x001f3?Sd\x0005oázÏª\x000eËc\x0014R¤£ù­<®Ülü2\kåL·3Ò±*|\x0010\x001eò±\x0014÷Ü|á2W
W½p1\x000cQ$\x0017m KR\x000e«ïµZ«\x0014\x0005\x0011.^8ë)7tö\x001cw\x0010x7î¼¬hV.ûÎÏ*Pß0ÁYË"hÖ¸ÜÀVi\x0017#\x001b@/\x001bÞ
ÕÛÝWU¼p0î\x001f¼n¾ª×½_UG¯O³¾\x0000Øé'ÅÄfÍÔsÈJ6Û¸\x0007o{Ý\x0008ÔùÖ8x£o2Ãl®1røc\x001f\x001bx¹¯´pØ¦G"äk=1É4
\x0017Z\x000b\x001cº-0XÀKvZ8(j%>HV©t\x0013"\x000bëàdÕê(R\x0011è¦\x0003Ã&\x0018éèmË\x0017u_ãM°¬ÚÔ2ìµ$\x0010]"ñD©èDD:VH6zþ=xÎîÑõº/¬ï"ií\x0003\x001d	\x0015=K;ª©§tJ´tª7\x0010Þ%|M¼BÒ°/\x0012®fRJ~%Ö-îèPè¬ÆAW$È\x000fO´£öDîODç»é\x0004«\x0018åq\x0001Å¤Íb%:©ÛS!uï©PÞr£ËHCçS¡í°õ°Dg{×N$Åt \x001d?:Ü×ó½õpJ´\x0002î]:Íá0à¸sCKÇ-£àÕ°1ö{t¾.ú,ê×\x0006\x0007æm§\x0015½i;¯§°&C×\x0008ÅQ.Cw%Ã¢¯¥\'j>ä\x0018E[.s\x0013ó5ó°¯a\x000b;
Ûï\x001eï??|:¹~XÎÃjL2e­]«P¿,Ï\x001fõºÔàÍ\x0015Ü~w}ñþêíÉõÕî`\x0012PÕª\x001f\x0010+\x0004= \x0019\x00134\x0012` \x000fU\x001a\x0000¡\x0006\x0015ô¡T1ºx>2\x001f\x0014>;s<ÖòéO\x000f, "þèe ¼/âÆMÈk\x0001M
h\x0006\x0016\x0010Ï-=\x0005ØÔP\x0000.r:\x001f»\x0016ÐÖv`\x0005u/e)cXk×$g=§\x001e^{ð|ç\x0007ðdyÑ\x0006\x001c-Û9¼Ìçg´}W\x0002îÄ*\x0011#FÆSÍ
Vv¢ød"4Àb#acdä\x0011ørÆk\x0018ð:\x0011*Á{0ÌÜÕÖ\x00126§X\x000e\x001cc¡ÝN\x0016YàS\x0014\x0012:
MãGÑ\x0001Ø\x001c\x00129pJ\x000ctñ'¢L²vºØ9ÝîµÍ9ý\x0007\x0005ð-µM½D(5¯ádçzBÕ\x001c\x0014ÕP\x0000³È
Í­å\x000e2Ë=ôH¸ÉÙ©&\P#ñB¼ÀQÕ\x000fæ2 ¾s\x0015ÊLnt-`\x001b.ôd|þ,\x000f\x001aPK!-¡bQv\x0005Û\x000ejâ\x00055\x00120\x0008MÃÒÓ7dâÙu\x0013l[ÃÆÖ¨~[\x0013·a¼PÈ \x000cWç[î"Psº\x001fk\x0001A\x000cÒÐãUÂ£ÙIK\x0008¥!CÌè\x0003®%l¬¡ê·\x0010pd+½FT¹\x0008E\x000cágf\x0003,\x0012:µ\x0017øc-Í\x0004¸ûôxòæöËýçÅüd
íNtlã\x0016!\x0011ôtXøúüíõÅÉ³\x000f\x0017ïß\x001f$T5¡\x001a!ôã.\x0011²ÍöÚ\x0006Éoáf¦Kd5"ÔÐE®eRØmD-K-ÁÔÔ\x001eD]#ê\x0011D\x0001(Æ\x0010
p÷´SíÌ\x0005j5¢©\x0011Í\x0008"8êC\x000bfð½7{R)¦Fgõ Ú\x001aÑ ¢*íELoqtãK]ÆL\x0002i5¢«\x0011Ý\x0008b¼\x001eÓ"Êt©O¬\x001dÿræ²Ð×~0ë\x0002åE¤\x0000¶D°bN¶a5_¨ùÂ\x0008ã<8\x001d+_\x0002¤á\x0015²\x0012°ºH%U¡ol¹SV8a\x0004}d®Àñ3"K«\x0019[¿2àXRB$Bv\x000cÆèC{à\x000f-§*Ã»\x0018\x001b³-Gì6À,i#G-úÌW36FQXE\x0019OT¥.T»¼CªåØÄØ\x001c9bs°ù®TØa\x001eò·\x000eÀîo¦Ar5as¤åÈÆqG¯6µÐ\x0002ïF;rªÁþðËo\x001fÿö·Ï\x00145ÒÑX²û3ë\x0003å%°ÄöâîÓÃ?þ¿/ÿçóÓãÿy£\x0006¨rB O±^x\x0013\x000cU\x0011\x0012\x0005Pª\x0017/Îß^]|8ys}òþ\x001c\x0007	\x0014É ,ãý6\x0005M·Ð1"S\x001b¡ã®Ì,J\x0011\x000f¸\x001cû
¶zi<\x0012t<Gf#4V|Lò\x0008eu5Q×ÕnG¢\x0001ÝH\x001d¯\x0013.ï\x000fi%w#D\x0013Ákú
K\x001d=¼ßFm1\x001fÈÂq	°¶9-	Ö;sìÆ@¶Q\x0019\x001daÆý!\x0013vÜ!è½\x00126¥`"v}é8\x0012vÜ\x001crã\x0006±43\x000f±qÄgÞÖF\x0000¯6À±7\x0008¦àäÖ\x001dbR3xÆ\x0016\MEH}ôÅÆ´\#\x00179BíD¤ÌÔ1z ËgZ¦æz£½¶N\x00113 Ifv¼¯?ö\x0006ÁÔÚz\x001c½K:-%\x0017a\x0001DÆv¾ºÕ\x001c\x0003ÛDð\x001fþ\x001eÝLü¿ùû6£­@r5{õã¿EG2^pk\x0000\x0013ú/þËFô¬×è\x0001$'ÉÞÆW\x0015N[È5¿=ýÕgrâþær\x0014Yº¤ÍCá pD\x0015Çn\x000fËw²­(ò¢ÒÂ.ûFñM5ëç»?ÝþÇÝã§OëÉU©'\x001bàÑ¬ÊIP9úSÖ\x001eØã<WêÛó?}~ýöêíìz\x0017~Uó«üRê4\\x0014ùcªx±\x000fÄ\x001fÌ\x0001sØÅ\x001fÚõOÏB»_\x001eïþ¶Ü4\.Ç¯ ©à\x000b,äÉ`u5¾wf|x}s}þçedU#«qdkRuB\x000e,³ÓÇ\x0019ÙØ£1CÍ\x000cãÌ*uv&fÐ¨µ85y\x0002\x0016Ê.ºùÕÌºfÖãÌ1\x000et%¯Ø:ËÌãVf[3Û
ë,é :ÔúÕÚ\x0015Ëv¶bÑÇ¯fö5³\x001fg\x0016Þ9nm\x0012ß6(ÃÝ!»ÝÇ,Ec6Ä0t<§´ÎAPI\x001cNfá½\x0011ÂÑölì\x001c7\x001cÑª¥WÆù\x0015Ô.\x001a\x0003)¡#þÑ\x000cl\x000c\x001c·\x001c\x0008-UÀCp4FN\x0004½\x001ci¯nv´\x001cßÒÆ¹ô\x0004ÐÎJ @°´¥sÇ[éÐ@ñ\x0016òÔdf­9zÒÊQôd´?ÚVÍ1TãÇÐàÌÐ¡ÜÕÁZº\x001c \x0016/\x0007«¡[ÿ=~\x000e±I*ßÔ[Z}S"¼G3xª9jü\x001câxN­\x0008Z¡NZñààÚJy´-­\x001a\x000f®Æ]xÜ²tÿ±¨áYkqKóJk¹xY
m\x001ah³	ÚÐö\x0000½æÜB\x000cF·ÒMÜ¡Æ\x0003\x000f\x0005_´ÒÆ±CTVÅ~ñª»\x001aÚ5Ðn\x001c\x001a\x001bíh¥æYHJÛ²=Âñ\x000ebã[Ô¸oÑÆÒCóÑÍPÂL\x00010´\x0013ÇÛÓoQã¾EÇ`Ô0t\x0019S¢\x0014¿\x0014ØãxÐø\x0016\x0018÷-\x001a8ñä|ðE'Jp,}èJÞÜ\faü6«£ãvd¤çÛ¬\x001câ\x000c­£A7î\x0010ÆÝ¡Æù®)êpÔ{V*\x0006é)ù\x0011÷ór^r5t{\x001dwZ\x0001\x0007\x001eA\x0008,ûÉ	·¶aù½n5tã\x000eaÜ\x001dB\x0000¥Qí2Ç\x001dR\x0007Î¤9Þn¼!{CÀÊñl9b,GÚ 
Ûh'ÝÑÌ\x001d4Þ\x0010Æ½!xÉ©`%O¦ é¦BMGn¼!{CÀ\x0017FÚÒZ²cZvÊ\x001fo{4Þ\x0010Æ½!Ä\x0008)Ç\x001déu@ågsAE8I\x001dÏâ5Þ\x0010Æ½!8êcp¥çG\x001aìFÛC\x001fÍxèÆ\x001dêqw\x0018£ÎTèAÏG\x0004
´\x0003~òZ~\x0012X
Ý8D=î\x0010\x0001µïhO»r\x0001\x0010Á\x0013ôñ®áºqzÜ\x001db£ª¥\x001dmKQ\x0010ìÃS«ô± ÛTé¸gAAJIo8G(÷\x0007ZGh\x000bÇ[éÆµè
®\x0005\x00055éé9nnË;Ú\x0016Ûáw\x000c\x001b+­Ç­´ÂvMÚ\x001ee\x001b\x0000µù\x0018\x001eïÎ¢\x001b+­Ç­´R©x;U\x0014\x0001\x0011\x0015\x0014§xðÇ³\x001dÖ\x001b¬ô¿0ò06ãVZaÿ_ÞÓÒÉ"¯\x0010ß@áxÁ´i¬´\x0019·Ò
\x000b0©¶	\x0015+2t\x000cBØäy}´ÈÃ4vÚÛié\x0003\x0017®ÈàèIKÅkå×æã¥iLsm1ã×\x0016\x0019djåOÐ<pEç¡`ìÑ¢%Óø\x00163î[$j5Qa\x001e\x0013-\x0017\x0004/·¥\x001bßbÆ}K"¥\x0006Aq©
²ìZÑa+tsm1ã×\x0016ér¼^iAºgÊ\x001bÚ\x001eNÔ3\x001b¶B7\x000eÑlpÂÑ]+î\x0003ÀiWi¥âR\x0015	G{Â7C4ã\x000e\x0011%Q-Wû
z[V^SçâÿÎÑB\x000fÓ8D3î\x0010cdÁA×\x0016Å¾EH.AµG[iÛø\x0016;î[Öä\x0010¬~4Ó\x000c
Çlã[ì\x0006ßb\x0000.Óöñ^\x0011úQ¼=Ìñ¬m|Ýà[M
R©üJÒî@/¸º\x0018|5sc¦í¸Æ\x0000ªãTÑLkò:p¸\x0014ç[l[ã±ÁLc³\Þ\x001d`,½Ô*Ï)N
}´ìmÌ´\x001d7ÓÒ¦\x0011Éµ8¾\x0001xÍ\x001bZØã­scïì\x0006{\x0017O¡`#íXYÈÓà\x0010ìÉÐG;®±wn½>0oh\x0014 oè9îpI¹õXÌ¹s\x001bÌ§ÙphQü\x000bYn5îg#\x0016þ»ÆÚ¹
Ö\x000eL®ð¨\x000bÏ\x0002¢¬³_®[_ÍÜDÒnC$\x001dC%þµV<:ÌQ\x0006Ï\x001d1æpv\x001b\x000c´â¤´GMHÖ\x001e\x000bùe\x0007®1ÐnÜ@£¤È¶É$hCVNã\x001d¸&$uã!)vRÛ\x000epê,IÐi:J-·E­nL´Û`¢ã5b\x000eaU?GÇñ\x001eÍÜù&GãÇs4\x0002ûû²/48%>_hb¿¢Xvà\x001b{çí	Rpÿ\x0019&ÕsI2ÂX\x000e:{\x0019VC7A\x001f\x000f:pl\x000bÅÑÚk¬Î{n,.©È\x001f\x000bºÙÓ~|O\x000b\x001d0¶r¨_ÐOâf\x0000q´\x000eÍ\x000e\x001bö´\x000cÜ¾j¼g\x0001Kk(î@£¼ÐÄ\x001da<îÀ\x0017Cý!\x0016?RPj5u¹8PöhÎ%4N<\x000c;q\x0013Pe eyj±$Q\x001b¡õñZBãÆÃ°\x001b7\x001aÏpèO®PsÒ\x000eóG#n|x\x0018öá8ó"Éb"t\x000cð4í
ÉG4G»ÎÆÞa{gB)hó8©ä7ÔE\x000eÎ\x001cÍÞÆÞa{g\x0002ÖðÒvÞhqMG8m\x000f\x0014Ã¶\x0003G{2´áhÉ8Ï¦#,·c¯Ö-ô\x0006ÛÇ/CgÁ§\x0004Í6Z\x000bw¼¶-ó\x0008\x0016ÚåëKbÖlî´Znk^
ÝÖÿá`:Bs9¬\x0011
é@iÉÔÇëÑráÛ½púv<4ó0]Å\x000fb<-8ÊÓËÍ¶ë\x000b¦ø±æVæ\x001fËñL\x0012·©fZáPÚ<úñÔñ\x0002j0¬\x0008]\x0015·ÕÐÝÕI<W?i¤ÑÍð+³8^\x0007°ûìv\x000bº\x0017¥Ù,õ÷Q#b(ýDp¼,uÜ,·{exÇ=|Ju½\x001aN\x0015ª\x0003×"C8Z.R¹ý\x0015WnÓn¡é	È\x001e­¡ \x0012N®à´+Ú¾×á¤²)|õðsO_0VØÐÓ±4\x001f\x001aâý¦<\x0018ÁBà÷êêÛÃÍÀ{ÍÌªÆP£¹£°ZfÅÄ
/ÌR\x0014²\x0015jV\x0018bU!=gVÁ6CV-\x001cRz\x0014V]³ê1Öx\x001b4üz/yÇ
	¼\x0007ÜRÙàJV[³Ú1V\x001cáÆ¯A<@0.¶.¯AK5ÿ+Y}ÍêÇX­Æ¨3±\x001aSX½ôü\x000c\x000b÷u¬uÇìNû»\x0017Ö(®JRÑø*z£·r\x0002
^WÂ¶6kÌh)D¢*\x0008ç9µ\x001f8±\x000fp\x0014; \x001b%Ç\x0016¢î
\x000b6J¦Hè¥\x0007ù¬\x001d\x0000Ëx@\x000cQ(/N\x001cÕ4¬fU\x0019ê£Ñ¤á¼a\x0000\x0001\x000c»\x0010Ø¬dml\x001c4Z\x0011\x0016N~r´®LêÝqÌ@c²ä ÍB
\x001cZV\x001cxÃe ø¨ày\x0004XÕìW5¶_¥/\x0001\x0016\x0001\x0015
rá.¯jã&\x0010a/x¿}­Äòááo\x000f_:ÂÃ\x0018\x0013jØ\x0015RÒÈÏ"Èçý¡ËDÑa¹Á\x0018ñÍÕev¨Ùa\x0013;6'å\x001b³T\x0002ËAsµm/óîp\x0003èºF×Û\x001d\x000c¿«¢\x0006t Ù¾"ê÷pÜe75»ÙÆ®<:)ô©%t±Óè;`\x0007Ðmn·í\x0018o±\x000f=w¤\x0004nî¯ý^\x001e²}\x0003ì®fwÛÝ\x0004ê\x001fÄd\x001cj\x000eçÖcÅÝ4æ N\x0007{´©íI±\x0013òù|òáñþ'ü%>¯g7ÑãhMÛ=ðÈMàÞÛålËû\x000f×\x0017/ñwx¿®ktýB75ºùC¡»\x001aÝý¡Ð}î7¡£\x0018\x0003u½EÃB)s)Ï××\x0015+]ì¡f\x000f¤eßÝ\x0014e\x001aê·mÝ#0\x00052y^TZv¾ÙX\x001fßÀ»ØeÃ.ÿPëÞvù²í²1ò\x000fe!w··Än·±ËèpÐÜ\x0012\x000c»\x0018¼]nêoÌ»üCÙwÙØw¹ÍÀ\x001bØ¡w@A×Ë\x0015d=ð;\x0015)¯\x0005}¿âÛeÿIÀÕ÷o\x001e>}éÀÆ!$®©²püáÓ\x0014ø%î7Wo?¬`\x0019Æ±\x000bMG*ªÉsG
+öÉJfS3qæ`w­Qà;F\x0010Ë\x000e«ml!\x0008nÂv£ÀM·Âs\x0017É²åjfW3»af,¥ç\x0018åå)i\x001b\x0005)KÆxE¬²\x0012Ù×È~\x001c\x0019\x001c·'*(²\x0019JêÒSyÄ­\x0011jæ0¾5ÌnkxY^½BQÓÖË5\x0015kekéÆM\x001d`ã\x0008\x0005²¡ÈæIé¹;Ñ\x001cRFînL\x001c·ue³|\x0008mré1ËR«¡u\x0003­Ç·4^Ïøñ.ùt\x0018ck\x0017»HVC7\x0006Z[h\x0003H¨Ñ\x000fÕY5ÆøÕ9,K2­nL´\x001c·Ñ\x001açNÑ«á
TP®\x0018<©æ
ecðä\x0006ç-õ\x0018álZºOv[µ,?½¸1wrÜÞi\x000cG¹ýÌä~JÀaÓ¼Êáhæ®ÖcuÍpNfc|y§\x0006¸À\x001dsV\x001dÍ{«ÆD«q\x0013me!\x0007,V \x000f\x0010¥ë\x001dÂÑLt­!ëè¿\x0017Ú¹Ò¡<u\x0008\x0016\é+Üq@+¡\x001b\x0013­ÆM´\x0015Ô RR2Mz{\x0011¸=àNGw\x0006KÛ¨ÛVHê¨!]yd7ËÍ\ËÐJì]°ðHî¿¿ýô©çb\x0018ÿ{\x000cm,à% ·chª\x000eYÑËõþäû³·o\x000fÞ
	ZÕÐj\x0018Ú\x0004TÏ6Ú\x0018yJ5³^1³_]\x000f
54lö@Zn\x0011Ú>\x0001Á\x001dhÊ/K®§Ö5µÞ@Zy´?â\x001f¹Q@0´^\x00167]\x000fmjh³eÀ)µ\x0018i$ï\x000fn\x0013~}EØ±\x0016ÚÕÐn\x0003´\§e@ddSíR\x0001d\x000fr¨ÃÍa9¾3Rp°$|»c^I-[7nóL\x0010E
R£\x001fÏ{Z\x0007ÞÓjYÛh\x0005µ´û0[\x001bê×·?ßüx÷Øsß{Äs\x0017«ádá9<+\x00063¼?y}výíÅååÅùõ
~Uó«ü\x001b\x0013¹\x0019^;n;$-^.ë\x0006uòë_oå\x000fEÚ\x0012ª\x0003kêq¿¶ôËÍü¶æ·[÷,cÆ´¢	hJ\x0017ô^µNþPóü(¦¬é\x0016¬M©ý	%.\x0014k®î=ü²=¿[\x000f0î¸	M
RÊsy«X\x0001\É¯÷í®Æ_}¼=yùøpß14
´*õ?F²é1¬\x0008'Wt\x0014\¼¼¾ºòV°U­6a¢¾\x0017ï?¼åÞhX¡Í¸\x001e[×Øz\x000b¶)\x001aI"\x0018,3N;](~ùX£H»ÛÔÜf\x000b·ÜH/rÀ¹ébo½Y!ºÛÕÜn\x000b7*ÚelãyìTe$ê&ÍÕÔ²=\x000eetHF[gñHcx*ªX1zl=84à°\x0001\x001c\x0006\x0005Ëq\x001b\x001cùÀ-Ïysayäo\x0007x³¿å
%¾$\x0005\x0010s\x0011?w\Kè¼[\x0016\x0012Y\x000fÞlp¹ekôýÔ?\x0018\x0014'RÄÁk¿Ûv6´áU7Û]áá¿\x0006;OÉ¬X~|?â¢Gø/w-<þÅSêO¡Í®ðîO)µ&£öü16{Zß\x0019ÿ¢®\x0013ÿö6Æ+·ñ_zzì(@Åa©¬|\x0017=Qà\x0013Øõ¬)=\x0011ËÙÛW7×jPÃ^;\x0019þ\x0006zëo u`±\x0003À!\x0002UZ\x001f\x000eå\x0003Æ~\x0003[ÿ\x0006vóo =gabÎ3Ýey9òµ\x001cû
|ý\x001bøí¿âÈ\x001d\4Devæë¡ñ\x000b}¿At°û¡¯l&ï>¼üõöËÝíÓz~	
k¯sªC:Vqã«>\x0014FVUØ/_}8?»Y×5¼Þ\x0008­tzÄúwÒ séí¡Fæ\x001ez\x0015T»ô
5x¾ùæûûþý}Og5fg\x0006\x001bHí\x001bàîUg\x000eÎùþê"1qpÊ1\x0001C
\x000c£À.5Fd\x0017\x000bø2d\x000f{h\ßJ^ØK¥Ç¿ ûÑÇw'on\x001f»e¼PÓëPG.ü¬ì\x0016Þ,./ÏOÞ]\x001fd\x0016dÿ<r\x0015K|ûñ¾\x00077Ç\x0001gZ>(g¤eÐKiô¸Æg\x0017+¡\x0006Q`¥\x0004+^éîÐ¹ÍìòK1újb]\x0013ëqb¬Ô>PË
 
ðb´µ\x001aØÖÀv\x0014\x0018lim4Á±ÀDÜÜEÅ\x0016±V\x0013»Ø
/q$¦g\x0015¥©ÿN\x0005ïø	k¹Úg-pÝ?\x001cvSû×Xx®õÁB(CPXmÎ/¾~¯Fn¶±\x001cÞÇÿJdÓ ad­N6q^´£Ú5Å\x0012hr1C¸¬ônÒ¦\x0012àÉ»û»ÇÇ»\x000eg
ÀMv
%\x0014ó=A\x0017E Ã­û\x001cdäÿøÝÅùõõùòo êß@mþ
¢Ùã\x0007TÞL¿õ\*\x0001\x0004óú~\x0003!÷ÄeíÇþßÿúïóO'/n;rËR²f²îiÊí³ÕcDWþíÉùÛ\x0017g\x0007óÊû\x000fÌ\x001fGÁwì Qÿ¥{u\x0011±\x000b£ÙúÈmMn·Ç°Æ\x0015)Í=\x0001ÊÉR.&\x0016mûÈ]Mî¶/{]\x0008ïbËÀã`\x0017ÞÈûÈ}Mî·ms|| ò\~\x0002@ÅoXbAÎd-8ìOøfç;_><þþ\x0019A¯n\x001fî01ÚîD¼°H\x0007	+¾"à`%óþòêúÝ{L	½:»þö Qû¿ªlL¼F>ý|ÿO\x001dø2\x001avÏzB\x001aïù"Y´ôB©!.~¼DÞ|{ñêí
r¨Éa\x0013¹0<
\x0001;\x001c,éÕY\x001däÂ\x0018ÖNr]ëMäÊq£	ú]s1û|ü:î\x001fcðÜc\x0017¨&{ñ»»ÇßRÚóÅÝÇÛûÇÕÜÁá;JdBð¬lè\x001cPF{\x000f%=¿;¿~Ò/Î/Ï.®gÀõ\x000fö¯þãðx4äòîäÝíãíO\x001fï0=¥EÕ\x0004{öôc\x000cÇ"`<r\x0002rõô>\x0018\Y856Ü\\x0014Ý~¨4PÏn^Ä*®å»³ë³çsé§è\x001f\x0013Óë¡â
åvé-¾\Ú\x000c%N5Îìv[n\x0013ÓmÏBQ5¦ôNÆð4#Ù\x001cjëª±Iëþ\x001e­ÞßÒ³z4\x0019é\x001fwUjk\x0007\x001fÎãYdBá&@1NË\x0003d´GÁçDsW
C ·\x001e\x0008{7ðñP\x0000æ4ãDÛ\x0002\x0019'úÔ}´sû×§¿ÿý÷\x0018ÙÆöÍ7ù·'¯>><Þß}ùrwðÅX\x000fòHB%ÓHELZÛìÞu¨çs\x0011ÒÙÉ«Ë«ëó\x000f\x001fæÌþá/\x001fïq\x001fáë³ËßìÅCt\x0008Ë!ßkdô\x0011Iù\x0004|  §u5n°,Ò«èàâ"ýtûóíç/\x0007xÐTáÿ]ËãËïÔ28\x001c¼8FÒDOí¬g\x000bÔã,\x001e³¸@·ëWÈè¬n,ã\x0006G%Û´@¼<¦\x0012\x0018Æ³ü¹¼üá§´@?­_!l÷¼B\x000e=M^¢üä\x0010W(ø]½Dtû÷¿ßþô×tÈ4\x001e26õ»Ç/·O?ýº°©½\x000b9Ë£\x0004ÞplþhÀÇ^{fÎ¢ÿ¸þpvóòõùî«ñ\x001fé¯ýø÷¿=¥Ð\x0014-H»úóÉÅÇTS8ÏÿY®Æ!Ä»Wò\x001fÈC{\x0008\x001bæ­ÐûøYÿû§Ç_þ¯ÿ Â),_ëÃýÇ%\x0013-#Cî\x001eSXç5vh£µdPrÊH¸¸D\x0013=\x0007ó[øù×¿´0ßããÏ_\x000e(#o4\x001d.!1ã+cãÓ¥ª"Bó=¾í¼ÿN;\x001cü·\x001d¬ç\x0011!
A\x001eTÂ÷¿T OïâG\x000b[x0¹\x0018Öóº²'ºWT\x000cC\x001eMy)\x000f\x001f[ÖG¢@^úG\x000f\x0010}°´\x0015\x0001ùÝV6\x0000zV(~± 3\x0010$Åæ\x0004dó%/\x0002°\x001d@\x001e|Ç\x0016ò\x0006KöÓÔdjnò\x0016bsè9Ö\x0003a]úÇê3æd\x000e"P<cÖ' Gc\x0011Hnã	ÈÓsæ£\x0005\x0012\x001cªbãÏ1ìQå¿X\x000f
?é\x001fk°EÜW\x0014F\x001e\x000cªÇmÚ@¨Eþ±\x001aÇÒôQäX+xÀ:æ\x0013\x0001Ð\x0012P¼hBËÍQÇøõññáÓ'S\x0018¶z:ÿ\x0002ÿ>\x001einÆã&õ~8ÄÅ¨1½¾¾z;J©\x0010U¨º\x0011µÎÖ¨ÑÙ¥õ\x0013¶ >\x000búû\x0011¡F^Ä\x0018¸Ò"zE>ØÄ¿§\x001d\x0017Ã}\x001fÜO¨kBÝ½ñ.XÀ&h"¤IÔ\x001aUÎ÷ýN?¡­	m7!~[©,ßí³å3[¹ïú\x0011]èº?s¼û\x001cF·ÀÞ\x001b«\x00112bôXÛ\x0011}è»WQèÜâ[Q³±q\x0006ØûgÆ¦\x001f1Ô¡\x0017\x0011eh _e´VQ*æ±,~+"	±U\x0014Ý_\x001ao\x0019ùKc131º,î\x001b?´\x0013û>¤\x001f±5ÜÝ[XªKËè4&ÆS\b³\x001aj\Fó,ðïgl,·ì6Ýÿel,·ì5Ý"$9t³i@E
7MYÅ°ý¼ÈÆtËnÛu/éé\x0000Í)ª \x001c#,£i\x0018Mï2âmOÛÄ¨Âó"\x0006y\x001dó\x001dl\x001cìö0\x001246\x000e¥u4~3­#gQj?`ã^d¯\x0011§¥`CóU#^x\x000cç9ôþmµ±ñ/²ÛÁ$\x0005`IÖÛ²ñ\x000e·ßì\x0002Uc¼U·ñ\x0016ZæÆ\x00184¸\x0018\x0007ÜýmLÛm\x0019£ÃÌ\x0014ú\x0013£ÊÏÈh6;AÕØ\x001dÕmwD</®0\x0019Q\x0007FÜ~5PÍVÝG:þk¹µ\x0001Íw\x001aÔÌ·×\x0017~»ÙQÍQ½'&¥XLÞ
u8<¹\x0018Iò\x0008\x0007#\x0003½G\x0006\x001fê\x000f´´ÎÊãù@hÎ\x000bô¸5°îu§2\x0017qûfæ¼@ïy\x0011¨à9K&p&ó]ÔÏÞ9ú	ã\x0002½ÇEø\x0000\x001c)_R5\x0000\x001dÙü¥ãÿD\x001bIt\x0007¶\x0012K:óy\x0011&`ª+\x0007p\x000b:l=ÓÒ´­\x0019lÿ\x0005m¼cú­£§V;¼"\x0000g
M\x0010ì¬Íæ´íMËö\x001e ÷¸¸'uIgB`\x0013\x001eoÝÛ#GQÒvWÂ]WÚê\x001e¥oî0K\x0013ä\x0010ã7wG¸þïú\x0011PorÊL¡åå@Ò)N\x0011\x0007¥·g\x0001Ô>©\x001a U1c\x0014\x0014Ò$î\x001cUtEôâYÙC\x0007©¨Û\x000fò_Tí\x0007ï\x001e>-<®i%¨&#
tc°ñß l
Ô!\x0015ÝÍÉ»«·ó\x0015\x0010¢ëB`ª\x0007\x000cL.`ÁPÜc£%¢­\x0018/
Ë¶\x0016\x000cj0è\x0001Ã!Ùù{\x0002xµI`\x0014ë8\x0015¦3¡k¹tÍ¥;¸Òèü¬\x0004Zã\x001b\â\x0012\x0017\x00031y ÖrËôpE7LùwØÝíç\x0007SU\x000f¾\x001e\x0000³5í\x0001ÃÁHÄY\t0§pÆ)/&ï¢kÁ|
æ{À¬e0\x0014eì/5WLn;YKç²µU'@:z}\x0002ç(\x0001k\x0005\x00182½\x0000C\x001bM
ÛZ\x000c¬V¨ªÆSsò«ÛÇ»Oë0³£lN\x0016çl\x0012\x0003F×;MJµ³©\x0015ùÕÙõùÛÙÂ
U×¨z\x0008UÉÓ|f\x000fühaÁQeXË\x000eR±¿¨\x0016õáéK\x0002}ûð»ï-B\x000cÿD¦´8b2Òóó§ôÏ\x000eÊÕÍ\x0004ùöêÕùá=i÷Í±Mæ¸\x000bP|uÂ\x000cGKñ¡â\x0019ìyö½{ùtÍ§;ù<6óQÍ\x0008H,HG@EÇÙÍt¦¦3½tØ¸Ç«ç0ÇOùÀË÷l\x000föòÙÏöòåj\x0000§!h\x001aÅ·Ngí³ò±n>Wó¹^¾h\x0004)ÀK%¤ù\x0010\x0003õOãú=O\x0018ö\x0002ú\x001aÐ÷\x0002ÊÕðyÞÊ|kW J¹ÛüC
\x0018z\x0001­Ì\x0013\x001cp\x0005=Î0ËçÃò'ÖÏ/HÕsYÚ½Báºå
\x00102\x000bPX>#~ó7®^Ë\x0004©qu\x0011jÃËñ\x0016TÖÐj^C£6\x00136^Döº\x0011ç5VZæ¢ËcPSÑ¥W¼áyDßKØ¸\x0011ÙëG¼"áf´ÓªæÒ\ÚgÕæmØø\x0011ÙëH\x001cF´!­¤%4ÞsaÔ³»G/`ãJd·/\x0011~gj\x0014nÈ´Ù!S£7ãÆXË^kí¼?¥\x0015D±\x001dZAïÙ\x0016Ö£b\x0007\x0001\x001b[({!b\x0005* ô¥ÀTrðïðp\x001b j,êµ4øaéfîb8HI`	Áò&\x0014ÃÇDB-\x0001ÿó\x00191²~}ûôÂëï\x001e\x001eªªãMJqe¾ªãE\x000et¼âM]Ubxýúìæ\x0003ÅØß]Ý\cõ"³ªÕ83\x0013Ì\]KË\x0006É|Ñ ´®¡õ04JåSåï1V(N8=yÇ\x001fd65³ÙÀ,21êV\x0012±¤hçºü\x000f\x0012ÛØ\x0013C\x000eÏÌVÉÂ<õÌ6Èìjf·Ùçê}[\x0018;,34_GvÄíìkh?\x000e\x001d)JÙ\x001aj ±Â9Çë\x001c·Î»À4:1ÎlJÖÃ+Í\x001bÚsÂÔÁ³V­
Ô±ãÖN[QJ½ñ¢3uà²Íx_>µ\x001bÌ3Ü\x001d1#Qó@#¤\x000eG¤n¬Ü`>¬ç¼¢\x0007Ó$V
fÖÏªÆ\x00071»¸÷ ¡ª\x0007\x000f\x001f\x001f~ûñ>)\x0010\x001e¬Ù\×\x0002ñ\x0018m°ÑÐÓo&Ø?~yõæÅÅù|WmAT5¢êGô|ßÂ\x000b\VÎim\x0007Ïï[ÝP#B7¢öy*Cö\x0017·órç/ßû»\x0011u¨û\x0011!~Â\x000fíè1\x0005§\x0019\x000f½\x0019ÐÔ¦\x001fÐ\x00082:\x0005C¯w¢XÕçÉ»nB[\x0013ÚnB/¨Õ;\x001aMA\x000eÖà\x001c\x000ev°sï+\x001d®FtÝÖqÿ\x000c¦zèYy×\x001fâfªd»\x0010}è{\x0011AÆK
¹|¯\x000bbð|Væ^õ:\x0008CM\x0018ú¿sIN`ÆQsÓáEôÓ/Þ=uL`¤c\x0015£QT»^\x001bJ\x0006à\-ö±nfl]K·o\x0001¡rÉ\x0008~iOÝÑ\x001e\x0017>ôöUl<ìv-{ºÒ*¢,F^D\x0013¸`ÀLw\x0003u!6Ev»\x0016P*\x000fXÍo\x0006DÅñC?Ï\x0001t36[vn¾ESW\x0015\x0018¬
Kj\´?Û?uc»e·ñ\x0006OZE\x001b«éeÈ
Á5V³/½\x001díÝÆ\x001b	j¬þÅÑk´ve;Î¼w 6QvFNZ\x0007:0¥5pU¹«'t#úzÖMþvÖÄw\x000f
¤AçºIlh52sÀYG§Ät'K¹¯_\x001d¸ýþ\x0013¯·íT\x0015JÐEfáTQá\x000e%Sö<-Ú\x000b\x00085 ô® K\x0001l^Aj¸0çz\x0004Ý|ºæÓÝ|¢ÄÚ»',GÓÒu`ºÆ¯\x0003ÐÔ¦\x00170Þø¬*©P\x001f¨5¤\©6ãÙ\x001aÏöâ\x0019ÀA ù" 0ZLx\x001dÃò®\x0006tÂÙrà+©qåÆ¯§+#;ø|Íç{\x0017PÛ]J_É­\x0003\x000eáù+y/_¨ùBïú¡ö\x0002÷¬§vTD\x0012\x0002WAøÍ&°^½ÝE¯«WPIjqÆ«h©Å)7=-¶~aÙ:^/\x0012wpV\x0007Ì\x0010Ü!àKÛ¿vÅ=\x0017½n$Z\x0012[+ÏO¼V[~¦ÜÐMØ¸\x0011ÙéGâ½½HK8%9m£-°<Þ¾#½\x0004\x0005]8÷\x0005\x000f
\x000e3å5©lî lLµìµÕæàG.f÷\x0008
Ó9\x001eÀÆ\x0014Ê^[(´a\x0001,/\x001c_C
\x0014g¬ÔÖ¬\x001a[£zmM\x000cyË\x001bª3¬àa\x00047¼ÚZé}°Ùªs\x001b`\x001d?'8^QÓAQÅ^«çE½\x000eE6¨)®n\x0007é¬
¼,\x0016s`èX\x0005t\x000c·G6ûv\x0013²¼h\x000e\x0010%G°¢Ä_3=r=\x0011ö>'\x000cpr+6r*î7´¾\x0004:jC !Üþã«»\x0015î¾Üw¾§ÿX®øÔd\x001b\x0002¦F´°«h\Ìwç\x001f.>Ä{ßÍ÷\x000b\x0012nÿÀÕí\x000b\x001d¤»A\x0011I\x001cÐhà\x001akü\1w\x001f*Ô¨0\x001a\x0012%L\x001cN\x001apÔÝW*\x000fätsv7ª®Qõ\x0010j¼.È]I#Yx]\x0004üÜä£r?©©IÍ\x0010)õ$o\x0019·\x0002\x0015_By&òÏÔ*ÇHmMjH!:VWT¥ :å0Û
ÔêjT7ºS\x001d\x000b&)Î;µä¤¤yPèDõ5ª\x001f[UÐ£
\û
%"VÏ´ÕÆHCM\x001aÆ\x0016µÈxÃ5\x0016U\x0017¡¼¹4Z\x001fjýÈàêGNûÏÞ\x0014<>!æ½º+ß9ÊV­§\x001asU\x0012J6\x001f_Ý©#¥qÁ\ÃX\x001fkã«ä³Òyäw%ºàKi÷G²«m\x000b\x0012ÚÖº\x0005©Ç¼\x0006®l,\x0006¾T5é¼Qÿ¦Ý'®ûk;#¤Â«Ý5+vjÍ
¡VOgBV#K¹²y<ûË_ï~»ÿÄíI·â"ñÒ»£K=
IÝØIÎlúÒ!ªå³÷å¯Ïß\¼å\x001e¥ë³·ñO8×n\x0019YÕÈj\x0018ÙêSÒcvå(¼
dsõóÖqb¨a\x0018¸Iã{\x000bÕAÄ	g*\x001fãÈºFÖ_5²¦ÝÊéU°\x0014,?­Sy\x00178\x0014º-¾ù²äj©ìv¦pþfYí½@B
	½ñ?\x000bxº\x0012d\x001eìr\x0002Zñ5îyIj7¤l e?¥æ@d\x0017*\x000eé´\x000câZ?Ï÷C\x0006ÒôC*Vê«¡\x000c	ûÄÏÍ6Ë>Øí§¬R@\x0011QnJ\x0000ÇBÀ \x0004U\x0011 8UÏ¥\x0007(££ºÏNª;¡\x0000\x0016°yëNø\x0019]¹þÀ\x001eJÕPª~JS"\x0017Kº/^²\x001e\x0004`,¿²9<ªÿð°\\x0008\x0015\x0014t\x0019ô,æý\x0008G Ô
¥\x001eøââ4Â\x0001\x001e$òFh¦ôÛ­¥jÎ¸ê?ã\x0010\x000f¶àö}À 0¢w &4û)mCiû)µbid\x001cgKE\x0014EÿÊ\x001cc_ºÒ
X"ÀÆl¯þAÉ¢Ñð<IÕOé\x001bJßM©ã¥\x0012\x0014(\x0002Ë=\x001b/}Ò\x001d24¡-qxTö=1ÎäÔd(w(5ÛÞA	U~«*&@Å2aÉ*&üÞ®äójð~Ê6"ê·:zHª=R2àÓbþâ\x001c\x0012Éð¼>ª²±DÐo´\x0005~SÄys{\x0018¸¼UÎµW÷@6G\x001cú¸\x0002¥:\x0010RZO\x0017e+K\x001a"®íÑ%4\x0007ú\x000fO\x000cÒ²`¤6)¤Ãcbq)M³è§ÔÍáÑýÇ`n$_}â\x0015¥vQ´ñ?ÓåÚCÙ\x001c\x001eÝxl4T0,°ó#\x001fñ"çyþ<°/¼HÞ)/Ò¹¤»3\x0014ã,ºj\x0015p\x0003¡|.Å3\x0010	ï£*9~¾>úÍ]Á=»ôÓ\x0008ìTöXÃâß\x000cÄrÔ¦\x0002`ù¡Äk\x001e]¡±Uã&Ø`\x0000ÖD$È\x0017"\x001cd¨éôK\x000e<¥|Þx7\x0010Ò=Û\x0006vd\x001bà`4IVß&ÙåÜ\ÌÑh\x0000êÏ)<Û³C[VD+EÞÞºZÐ·¬\x0015zKD\x001fö+PC©@]×ò\x000f£»7g\x000eåUé\x0011UÏÓ37ç+ÑÂ~eg(+{±Ã©§T­¬§\x001d¼/\x0010¹ûÕ`¦\x00063\x001d`\x001a;j8ùfy&\x0014\õ\x0000aò\x0001d5«Á\Ï\x0005ÅÝë.Æè"¶"5£&Å³Ws+tqIîã²\x0015³m
÷srÍOª­\x0005«Þ´Â®ôpå\x001e\x0003\x0000Ã!\x0007ÔIá¸ÞÂÈÉ\x0006ØÕ`²\x0001=`ÑuÐuËx*-\x000b÷yQl_MÖ\x000bÙe/¼åZf£4?ÿ`8	9!	ÕC\x0006
\x0019t¹,Ì\x001e×\x000cç\x000eÑEº\x000cc³ÏÆ®v5öBö\x0018\x000c¼Ú\x001c\x000cF\x0008~\x0013	ÜSdÚ\x0004ÖØ\x000bÙg0J\x0007¨\x0001n\x0019CÁßÒM\x000eÅYMÖX\x000cÙg2JkºPä\x0016\x0004'E&+ôÖr©æ\ªs©åwz#d1±\x000bDµÞ´ÉT³ûUÏîÿ_0´çÈ
`#«aòes5Y³ýU¿T«\x0004µ\x0001ê~Q\x000f'e´ìÖ^MÖìÕ³ÿÿÉ\5û_õì$£Â\x0005
]&\x0016×\x0012l,^K\x0006Í	>Ïd¸Ì\x001cÅB±ÿ,Hé&k)×éÆ3é\x001eÏObt7ÔFN\x0015ÄÄ¯\x0019¶|M\x0019ë@¶h\°:>£P\x0013/¯ÅÜ\x0002\x001fÑé\x0017ë\x0003´}À^¾h7èµÉ*\x0013¿*û)Út¨ñ=Ä'å\x000f{\x000fÉ²mã{³ë\x001eïW\x0014òRé¶\x0005ÅïÞN¸âã\x000fÔç¿?ÇQõ7×\x0017+PUªP\x0003O\x000f\x0016g±F\x0005pAçþC7)Ô¤0Dj<÷\x0013Ûx\x0019¤![
nÕí&Õ5©\x001eûü&O0Â5\x0015\yI^Su\x001cTS£!Ôxe¥ÐÊF\x0003®¸å¯è OÈ\x0005\x000e¡Ú\x001aÕ¡\x0006\x0016U·Ñ\x000b*n_ãS¨=±ÔÕ¤nTB¹\x0015i\x000f°ù5nf(F/¨¯Aý×¼¤¡&
C¤Jå©e\x0012ªqË²
öt1/iuGO·â¯xQeë¦üðz·ª4\x0017Å»#ïSÙ8)9æ¥âç§\x0007Sk8\x0002ßÔ=\x000ekcüåõ[$¬q<2F*\£åg&õv;ÿ6ï+Ñ#]Ä^ìªÊ\x0004÷}ã[yñWÇ±\x0003vx¿Ij},à¸ÓÚb+­±g­e33¦;\x0016Ø\x0007Ö£ÀÖr\x0007¾¹QìR$ìbÀ5¯°
Xì\x0017A
SµM½yxú\x0018Q\x0016"ÁÀíõ&æf¬å\Þ´~ÂÍÉ«ËøÓ"ªáT\x0017)NpFr¢Ñ\x0019~£ÒAm\x001a\x000eúàD2ó	Î«2\x0012Ép¶e®Ñ`-®Ñt\x001fZtFò@úTI&ãîÐ\Ïfj6óU-­Ñl\x001f\x001a\x0013¢¼³\vé]Éë©ç5\x0006}p®s}px)çû¹c\x0001mÇ\x0017!\x001c\x0012¾Í×l¾
5å<\x0017/\x0006~\x000bÙÞµh¡F\x000b_Õ²Õ=KæªgiÕº\x0005Y\x0012iBbW5%éÊ\x0008f®±j-]ë\x0019ú\2/4X#Díü¾\x0004\x0008Ú<¯î£k\ìó
¯¢Y-ÄîÝNrzÔÌõ¤®¥k|ìt\x000eX]×NÇLá 7¢$¼§ï\x0003ëé\x001a÷ ûü\x0003æí®¼<W|	W'àûà\x001aÿ ;\x001dD(±\x001aEÐ¨0\x0013¥zk@"\x001b\x000f!û\\x00046:ÉRÚßd­\x0014<IÜ¸é\x001a\x000f!û\\x0004àäU²Ã¦Lú\x0008\x0019´¾/­§k|ìs\x0012øðCeÙhY4½\x001a(~5P
6îºÆMÈ>?\x0001:ðË1>oX\x0016³ÓÙæÚ\x0005WÒ©Æ\x0014«>S\x000e©­Y+©Ûlì¸\x0014üªâZº6Jï3ÅF\x0006Î&+zØ¥UEÎM\x0017\KÖaÕgµ5¥äÚóã¶\x0015¡\x0014¹­t¥S}NcÛ?­[îD²\x000bÕDÕm\x001fYcIT%AApº\x0015*/ñôöÈgõù°>¸æ¨ª¾£ªqX*\x0019a\x0013P\x0012)Á\x00019¥6úVh*ô\x001dU\x0013ï7Íf-uÃ*²jFah=\{eí;\x000f\x0008GOT\x0008g\x0003ÓÙB7#²®9\x000fÐw\x001e\x0016låâö§f\x0013«Ê`i%a#]s& ïLüÓéö\x0012eéúZ5¯óbþ\x001fýNîí¬8þêñÃíÞÑ¸íZBÐ§ì',\x000evK»/@YÁ0{|¦OR¹«=béE\x0001Î0v\x0004P-`´þ]Éô\x0011_ \x0000´|\`.'(×ð¹}1[×Ùþïý÷ù_>Þ^R·m±\x0013
R¤¹\x0015x\x0001Ts\x001aQ'ç¯./Þ\x001fJvºýbb×ÈÙ®ET¯\x0017Î\x0007\x00163qg:1­»Ò\x00085"ô#âó1\x0011
R´õ#\x0003\x001bfÓÜ«\x0001u
¨\x0007>³:e:Ë¥\x0018®4²Ùi¥ô\x001e@S\x0003~@#ÊÜWÔ\x0014¥5PdÀ¦Ó>=¶F´\x0003\x001fYï\x0010Ë°4_Ê\x001b­VøîAt5¢\x001bXEÏí¾\x000e\x0004ad!"+j¶f_#úU\x0004>*Jò\x0010]4;gµwW\x0003\x001a0\x000c\x001c\x0015	øô\x0004\x00147µù:Tq¤º÷Í¹JAºVÝv5£ÝMY\x0015(A\x0019a7çwëw­cé÷,ã\x0015K«\x0011\x001bÇ"G<ä¤õ
@p KL¸èAlì¶\x001c0ÜØëI/¨N×>S^$ÃÔ\x0000ô>ÆÆ.Ê\x0001Ã($OÔÅt~ ÒÜdüfÿ'\x001b«#ûÍG\x001e&±Ú_\x0015ÀZ¯É\x000e\x001eFÕjÕªÿ©\x0012öö#fËã~¼øí÷ÛÏ\x000bçÙãÏO??,e|1©*w.Ù\x0017ÍNóÌB^¼ywöþ=±]{óþýÕ¡àhMCki\x0015%ÏMü\x0013½\x0011jY`U²\x000fÒÚÖ\x000eÓ¦G}nïàá@ì~xvi\x001dÄu
®\x001bÅõåE,^\¹¯Îòà$ZßÐúaZËm©Æ(\x000e?\x000c\x000bÃë ´sC\x001bFqC\x000câh/ E ù"ãªý³bÚ1ÞZ\x0000	í\x001aãÅ,$Ù\x0005«0\x0014Í¡ÔT=x<È+\x001b^ùÕóªW}õ¼ÍþUãû·Ôg`ß\x0015)¦zWúü³A\x000cc¼Ðì_\x0018Þ¿-¯sÏy7¯¯ÞK8 ÆÈ.­yûx2\x0007oPï¡¨^Á5V/óFº¹÷Ö³ë³÷ËpºÓpEb,F.§|GÞuÀÎ½\x0018®D35éD3ê2ø\x0015ß=¹\x001eë7õÁÙ\x001aÎ~Uëæj4×FÏÀVx\x001e(åE¹è¹ñ¨+áêjnýM]³Î
n ³2pQl\x00196\x0014½üÜëÍJ8ÙÀÉ¯\x000bN5pêëklì4rÿd8ÕÀ©~\x000bL¥ãÆ	V(tU\x000bölýÜJºÆ\x0002«^\x0013üO£\x0013°÷æ~ï¹O^Ý>}ùõþîq\x0001\x0010gºh!«ypOÒ È	ýéÆÅoÏß¼:»ùðúâüz\x0005$ÔÐ\x000f	¥QÚg«\x0017}+1ÎQ÷1êQ÷3
GY}Tû&©¿x'`9r|fÚÌhjF3À\x0018ã¨Ì(I\x000c*"r?W3\x0005õ]®Ft½"8Ã96\x001c)ò§Öû¶½~í\x000c5d\x0018¤\x001e \x0016R\x001d\x0011R¶'»ûh§\x0011\x0019©'Yá¯Ì\x0015¨à\x0007µÎ=u-e«¤lÐ®Ýãë:á°
c¨ªXL_TRä\x000bjüãÿ\x000bé+N±¼H\x0016>þøÍ%Þ>ýt÷éäÝãÝç\x001fÿöåîñ`\x0012\x0013Ç6Üò£$vä¡C`\x001dµ«aýê~­O¼7½}yqþöäÝõùû\x0017þp~}(©öß½­:h^<<þ|wû´°K£\x0003
¬¡eËYÚ=Ø¹ÒÁ\x0017W×ßÝ,ãA\x0007½xåk[tàÙ?B%ñ57c}5©ñL'\x001eÈÒ6m4¿\x0002_Ú¦ý¤hI\x000f«ñ\'rü\x0006juà\x0017\x0013p¦ô ÎÝ¥\x0016ñ¤ÙÆ`ÒÞ«s
·'ïî~úõîãÃ/ãbFãd$ð4f\x001dD$ü¬é§N6¼;ùúüòêÃ\x0003ÇU¬£3W<ÚÕó+½öK1ôÁüi\x001f2ÔÈ0,çN\x0017/E\x0019´iª\x0019hûæhX×Äz8\x0018&VGwiëËðÒg]ãÄ¶&¶ãk,ËÀZYÊØuQ\x0019wð¬ì \x001fYØýj"»·?¼üõîÓÝDz·äP­,eOØ§NW\x0010ÃW\x0010ký|býýI¤}{þ}ôªçB\x0000»_ºc÷vE\x000f°+w&»¦L:ËòæNÎ0°­í(°\x0007.£p8ÄØRÛ:_N¬~¥ì\x0006zß\x001eëdß}¼ý÷ðÛûÅ®_\x00157mQ×(#\x0008å~8c©ä¿»<{É»÷ÍÙÅÁ¦_Æô5¦\x001fÀÔ¢\x0008\x001f*à9\x000e³PRä¶æ\x0008f¨1Ã×¹K\x001a¦.¾:N±\x001f,©`áå¯·O¿-)QÀcµ\x0000Ö¨Üè\x0002æà#àY<Kg7oVBMúÌá®!514¤Ñ\x001dZ\x0005\x0012T²2\x0008ntÏtÆºPÿ3_Uve\x000cÿÖ7þúÿþð)S>><Ýü¸|Mö4åÛÀ¸¹s\x0018l Îa?¡ùïWo3ãõÕÍÅååÁ[Ü¿¥ÈrKp<ééîÓýï¿/}}§9æÂö\x0013 \x001al	¬ª85;âñl¦ó·\x0017ïÞ­`U5«\x001acõ\.®m`É4©8<Ô\x0013³úX£\x0011ÝÏ@úöP}>y\x0017½StO'/n;á6^\x0019\x0016\\x0015.+=pø\x0000§t¼ä.\x0011ðL\x0008¤öTï¢^êäÅÙ¸+Îâ\x0015âÇ²ûûÂîÍsûðøð·%`°Ee'`q4É¹\x0016½ê\x00187ÎÏëúp}õç5ªFT½\x001a'PÒM\x0001\x001fÛh.!áóºµ~D¨\x0011¡{\x0015C\x0011\x0000ÂÉ£t°b$Ì¹*iöwk?¢©\x0011M÷*>åHÐÄäÿOÝ»f×u\x001cgÃSÁ\x0004Õ÷ËÒ/hx\x0000\x0003^óýá(HM\x0001
HÈe\x001aA2\x000eÏ$#ùªº«út\x001f`³»÷>~ãdY yªwwÝë)ñ ¬\x001f¡¯\x0011únp\x0015i=W\x001bí$6çÉT\7ÄÊÔ»lêû0Ú|v	£Ñl¾:C´Ohi»!ª\x0006¢êêRsOPI\x0004t(Û:íð1~'Âüg/R;O ¯IJþÕý÷7?\x0000ÎÝFSÇ\x0014ócn/à0òµV´\x0001\x0019ËÃOOòäMÒð¯.ú-\x0000Ýub+v¢ÝiøoðïÜì\x0004y;sÈÃ³æÕB'HÞñ¬ÿíýÙÅËÓißå\x000ctvsØ3\x000bbß\x001c1ÒÿýÏÿº|ø|s}·ó«#\x001d¬Â\x00153è ¡SÎ\x0000iC\x000eh0á	Y\x000e\x001c$=º¼:?=¹ØõÝeÚwj\Á¯Ò%¨/î\x001f¿Î\x0016\x000e¼¡×h
i40Ì^]°Ûº\x001cp¾¸|ÿ®\x001adútýýõ¯àñ\x000f[(­¨QÂßõ¢4¡ø*xbs\x0004çÓêiÉx\x0000¥mPÚþ³Ä5#¡Ìé\x001a:ËÈë\x000cy²î¼\x001f¥kPº~H\x0012l\:õlxxÉ¦RúI\x0012¿\x0003¥i.¾@\x001ebÔç;K#Ó@û2\x0003¾P'<¹í¦Ò½øLÏôáÓHEAñ´²Ç"M\x0011=øý¶\x0017mðÙN|.éÆO\x0013õ8øªì|}B4\x001b_VäÁ\x0017| È±ç\x0000naÇrå\x00106\x001b;´ãü¸wÌ9º'T\x0000p	ÛÅÊ;0æàAm0opç\x001cD\x000f%ðæ\x001e í	$=Ä¹¹àé4íPÕ`cH?©vB´P2\x0008o.á÷§»0úÔÏX#ü¨ÓA\x000e9V\x0008\x001eÈ¸DJñ(¹æ
ò\x0013Wí|"¾ìSÏ\x00052DÖÉ»ÉEOð:\x001e\x001eîw\x001bG\x0003\x0001.­\x001fQ`Â\x0002m§uc¢Oî'W=Áí¸ºº¼TµHÕÿ]¤®Eê\x0006ù+\x0014\x0018\x0006ú)%e#­°\x000câ©!\x001f@êDÔ~¤"*·Ç)¡¤Ef¦\ÅS4>é\x001cîÚ2×¿H¿{:Ý3ß\x0016\x000e­j2²¬÷OÞ?dó}øªñ\x0019Õ\x000f]a¦ÇÃ=êÄV\x0016\Ù÷þ¤\x0014:\x000býø÷_îÿ¬¿P*c³Åû÷7¿\?|½ù\x0019tû5D\x0015.Ý\x0004¾\x000f\x0000¾¸¹»¿ýòõw_\x001e\x001f~÷áúîî\x0006ÁZð£]Ú\x0000ïE:Ú\x0004\x0000\x0007(ò\x0017WÚÊ`¾8½¸<{ûîèíû«£\x000f'\x0017\x0017§¼äêôÍÉÕ»Ó× ûOÀ\x0018 çÝãF\x0004øsÕr\x0011\x000cDÀ2±z\½ªrCó¶G*m}Åµ®\x0008àéUD@\x0002¯,\x0001çz §m@ªZº®\x0000`ÊÍ*\x0002Ø¬8P\x0002[d¾FÒä¡N@\x001cê\x001bÀ[·«ñVz	
,u·\x00171',@\x0004#\x000f%\x0002¨\x0003·\x0008¹Ã\x0006¿H\x0014\x001dY\x0004Ã/ÁT=¨ë\x0000®_E\x0004À
·2\x0005+\x0004 |´;\x0008áoÂ\x001a"ø{\x0006\x0008>ß\x0008E\x001d\x0019u¨{\x0004d\E\x0002/ËSð17C\x0004_BÕW°ª\x0000dL\x0008Ë%°N\x0000%\x00085*¸sE¨&$×\x0001-ó
¦\x0019dP\x001f=Éû1ÑmtÈj"I\x0006©\x000eô\x0014p¤A®b^ÉæçêD\x0004éËõ>¥	\x0007²l8ø W±Í`ÅRcú\x000c"»sð\x0019H!j³îº"e«Xg¬µ\x0016\x0011ì±3Y\x0004#ù5T\x001b\x0012×\x0015\x0001,³\Å:Ã½GÞß$\x0002æÆè1hS¾9Îº\Å<;\x001cÚ&µ
KÚm\x00082HÍA\x001cì5¢«Øg\x0000Êw(\x0003RÑk ÎtxÑõ~®ue\x0000-W1Ð ÒFô\x001dTîëv.\x0004ÇÏ¡Þå¸®\x000c *ä*&\x001a\x001b¾½§ï óÎ\x000fAïp '\x0019cµvoR6
:.ÓM:\x0008`Õ*&Ú©\x0004<É uî\x0019Ç&F6ouOöº"`ð¼F\x0011,yJF\x001dG@Úr\x000eä­b?­ZÅB[\x0008×\x0002½g¥ù=CÈ@z\x0015û\x000f$\x0003ÜPµvÂ¥ÉËth8\x0002¾,R\x0008ú\x000e`Õ*6Ú\x0006vÐ¥ï rª\x001b¾ÃF'ùCÙh\x000cHÔ*6ÚÍ]Ò"ï\x0004A\x00198p8Ã¾¼ZÅD[\x0017\x00131\x0014 mÞ\x0000"8öö;TìfS­b¢Q\x0006Mi\x0000\PmXr\x000eö\x001dÀ<«UL´µyKú\x000e²|\x0007£\x0003C¥õC¯b£­1\x001b\x0019<j¨$òEµV]<ëÊ\x0000êN¯b¤­A¹$\x0008¹3\x0005DÐå*9} \x0000\x000elõ*FÚj\x001câå\x0017m\x001c}\x0005!ù+\x001c*»
\x0007z\x001d#­\j§NAå®:I%~
6\x001cê&Ö«\x0018il	÷¤Y\x0005íþuð?å5Øx(\x0019À¸éU\x000c\x001c7ì¤ç\3Ýnk\x000e%\x0003X\x0006½uÀ~ü\mPÁk~ÒV{¾Kø'\x001c¨â&yxyº\x001bu¦=­]r\x001e7P(jÅ¡Âi%b%Qþß¥\µ£âV\x0012åµüE]ÿýÓ5ÖðSâ\x0015ÿrZL¾tÔqµåøA@\x0018\x0008\x0001Á_ÊüJ\x0007»ËÈ§N©¦FûñÏýóOßÿÜÀ­H­\x0005ØSpÿpws3\x001b$ÞöHWDã\x001eXG·ÝH²crWÈ(_^^]NöÂØ÷w¿}JgéSü\x000bveý|w÷éóÍü\x0003ÅJ2ß\x0001Ë\x0001\x0013ÔHëpuÚu Øªõúòâòâåùt9ÿ×¿üôÛm¨\x001dçó£\x000fØVôãl 	©k\x0010\x000f\x0015s	*e\x0002/ÜîC=ú\x001dF¯æàd\x0015>3&pS)u\x001c(\x001bÉvâ´µ`Êù\x0006ÿ3\x00023@äêø*\x001c°MwT(ËwTí²-}8Á¢[7ÓøèPGá°uN&» Ø\x00171vOØS¢þ2ôÝ½L³
È\x0011L^\x0007µ¶r6\x0001Tä=ïÉ¿ØOúp{óø·£w7\x000f\x000fDü1×¬iGù1ÕQÒ\x001eB	º·qgAºYúpvúþOGïN¯®v0TâèZ\x001cý//­Å±ÿòâøZ\x001c¿8\x0018$%+®µ\x0014¸(|=9çAíU\x0013kqâZâcéH\x001cOY\x000egÿIûqUqd«
ÖÒ\x0005JÎÕ\x001a3ÿY\x001c\x0017ùëÔ{Ö\x0015§Q\x0005r-] \x001d{\x000eÚH\x000e£¢3dêU»%ò4º@®¥\x000cDÀ\x0019®$s\x0006\x000b+õ¿7ú>2ki\x0003\x0008©\x000bÜÌ;ä1,=66k©\x0003Q\x00045RyjCàë\x0016\x000f¥ÜT£
ÔZÚ@¨cEÊ:Øò|åë\x0016å¡äiÔZI\x001dàö\x0003Òn\x0006Gä¨\x0014è¹n\x0010=:P:P+©\x0003g\x0013Ww\x0007\x0019¨¤æ9ârgh<:P+©\x0003\x000cÅ$\^+®NÄLËaÄi´ZI\x001b¸¨5IcJ8¨4á@M7Ê@¯¦\x000c|Ú\x0018Ê\x0000\x0003]rulG\x001cF¹YA\x0008ìWãß¯$ 2"| uL·Í°ñrgoÃ@BmqH°Yèr}ôêúá\x0006\x0001Îæµ8¦Üy
âQiyºÁÊ-ï\x000bGÆÉÕ)þf/vUcW\x000b±»´H\x0013sÃÖÑò¸T\x0012ªð1Ö\x0005¯kðzñÁ{J£hißñäÉówNïL\x0006÷c75v³\x0010»gÃ.\(\x0003%ÊpRìô»\x0006ÀÛ\x001a¼]\x0006\x001ezoJ:P*\x0001à\x001a\x0017;­ø\x0000xWw\x000bO> âtòA\x001dÓ\x0014²¤sÜÝ\x0004Ó]FÕà#
òÔ¯
è9xwnwã?úFÙÈÚFr¥_+ô.ÌÖì×+k\x001bÙ¼X¹ðÉ\x0002ä@àC&\x0015CðÜÅæØY\x0010ì\x0007ß\z¹ðÖC ÁqðÁs\x0017!8\x0014Ü¿æ[ùâ\x0006}XÞ»#éì­.\x0017\x0007þ	¡÷;³\x0008#¶°;o\x001eîÞyì\x0013(èKÖ4ÔÖ\x000cæJ9Ö»[ä;ÐÛ¹jíÙÉ¹¸yüµçäAERÍ/\x0004î õÂv\x0004ø= /Nß\x0001VÕ`Õ\x0010Ø\x001czT³Ç>Aº%[XÌÎ*@\x0007V]cÕcX§+­ HÌ\x0003Ûp\x001b*-Cnß	ÖÔ`Í\x0018X\x0015iüU!rtuKñû¼`m
Ö\x000e\x0010TÒÖ}\x0013Å\x0011¬ñ{]H]Ô
Þ\x0001£å¹×ÇP¯\x000fÜ\x0001i¸OÆï\x000fÖ×`ýØ±jE~h-Ó¿c¡R®Õ\x0014A¨±1¬Ö¢ËX\x0015nMXCitû"Xc5\x000e`µØàMõ\x0018\x0015}ªe VíÙ!µr÷´Ël°#GÆÐJÔ«<"\x0015³ÕNó¼àîV¢ùX[Ó5b»¬À ÐÑ
ÈåX­RÜ,¤Wº\x0005²1]rÄv\x0001X\x001bËDopTk÷Öz>YµÖ5h\x0014\x001cÑ\ð;¶ÔR¦¨íØ;%\x001cÏ\x001fë´¬lü°äÆ°\x001bÖmÃ(\x0017¨Ð@XÍ=\x0017óZ\x0012;^Ù\x0013Äb\x000c²Å&Òe\x001f8[ØIÊôÒcnö>å_T;7
£Øìþ¼ÔGõ®dÀðyÒ'ì\x001eë¦eUel/hUVã ±ÿ§\x0004ÍÒ»\x0018=\x001b¶(÷\x0006\x0017óAë\x001a´^pÒáXn¼G>hN:\x001aç÷só1\x001a³\x0019Çì${\x0010ØRk)\x000fZï¬mw¶5h;\x000eÚ;\x001e
\x000e6lx
¸Âcä'íjÐnÁI{Jë\x0002hG9.Áu\x0002³»Ó	Ù×ý8ähØ\x0017Æ)rk\x0001Úï&åè\x0003\x001djÐa\x001ctÈT\x0008ZÑ\x000e\x0012CïnâíÃ\x001ckÌq\x0018s\x0010>ñ£§^9ÁÍ"p³[«®úz\x0001h÷I\x0011Ò JòDXöµ\x000b{ýóQ·æp=û\x0012\x001dÆÍiZè¬ÛYìDÝØC9n\x0010ñM¶âÞ¥µÉGá³ÞÝÜº1rEô©Á£Î\x000f$\x0019£·(õîAéN3Þæ\x0007ío1nSk(FÆîM-w¸MÛÐÕ"èØ\x0001QF}ÈÒ\x0008&´2V­¢\x0001knýü\x000bôR?ÜßÞ\x001c]Ýÿ\x000cøzRÚ SxN\x001b\x001e¿#-¸ç»2\x0019\x001f.ÏN®._Ã?ÞéX×\û\x0004YBÆ\x0015UþÁß+#<lÐØyµû\x0010ë\x001a±\x001eF\x000c\x001e£R\x000f¨nb\x0011ëõÎØÔÍ0b\x00119=¯\x0002\x000f|]dÖ´fw-È¶lG![/sGËÀx\x00103m;}]
Ù
?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=zu~ù\x001es_]_¾=9;½Ú\x000f¬J`õ\x0001°.õÿ\x0005À¦\x00046À"Ü·
CàüeðS\x0006`;eê÷\x0001Û\x0012Øv\x0003á\x0010ó/a\x0010µÒS¾^\x001f°+]7ðP^à°.q( eó_Mûö\x0001û\x0012Ø÷®a%¹\x001eÑY\x001b6bº\x0000'¦açÖ¥C	\x001czµ\x0019Þí°»,½xk?\x0000O)Úô\x0001Ç\x00128vÏ°Çzß¼é¸94Ìp\x001c\x001e\x001a§\x00122ºàùs}ûeªÊÄ\x0013¯^\x0002\x0002æàM¨\x001bÑ\x000b îÝÝú\x0013*\x0018¯\x001fïnüöõsDt´\x001f'¼¶E\x0007+~ÜS¥'ïÎW¯PÉxuu~¤·ß¬®ç.Rî»­\x000eÀµA©\x001bY
5gÓûáågÊ4ï¦Ö%µ>d²%\x0001"vÞÒG\x000e\x001e\x0000ö»ÛmJls\x00006\×N\x000eØÈ®ã\x001fBmKj{Èd[ÔÊF'½1±ddL¥vc»\x0012Ûõc\x000709\x000e&\x001dË3\x000c\x001d"ý¤iÔMíKjØ1âè¬Æð-W°á]{ê½«\x001b;ØáÉ¶|Xz>X~É3=\x0015èf%s<`ªÍ õ\x00063§[y(tvªév/uñªüÿQ÷6Éq\x001dÛ¡îT0\x0001#òÿ'Ø\x0002I\x0002\x0004\x0018 ¡8§¥( #\x0001BÔr÷\x000eÁÝ×ºÇÓÐL<·VæZY;«víÚ»|^\x00154¯ìûUVæúÿA=#\x0016\x001cµ´\x001dë×¸Ë\x0004L'"£ÙånîZ?.QZRÕ<\x0016¿pÓç²\x00127ZÊØ]éG¹@A\x0006ëÊq²÷1õéÒ\x001ckæïæ®4¤\¢"Á¬f? ØÒîa£*6Ô!Ï»Rr\x000cN\x0016Ó/\x001aÖ`·®å!¯w¥$å\x0012-©Jñ¦\x000baÝÈÔ\x0007T²RrtáØÆRßGÎ¢¼ÒÍ±N°nîJIÊ%ZRFTè\x001cFÈÃÍàr\x0017\x0017ÌMéæ®´¤\¢&}(\x0015`Uq Î§#×ñ ç]iJ¹DUÊµ\x000eþ¦Û],@;¶²\x0017[UªR-QÁsaº\x0003§=pË[á\x001eÝæÚÍ]©JµDUÈ¦+®òÑd\x00184èì!
*Ué\x001cµDç\x0008-{YWr\x000f
ø7ÎL#»¹+Ù­Èn!xÚÇB	ææ¾\x001alâ<\x0004·0\x0005\x0013f°Êâ§Û¯¸s`x\x001c¼\x0015e\x0001L@9ÅC>wd\x0000®¾¹>{«8}\}Z=~}¸)Ù¤TCJÕGIS\x000cx2·Ë²u\îä7\x001fS\x000f1u\x0007¦ó8K=w\x0019\x0007þí\x000ceãóÄ\¼ùfi:0½;¶4*Uò^S\x0019´(»½w¦}Z0í\x0010Óv`¢¸òå4\x0003ýèVÙ¾c!fL7ÄtÍ!¡Íci\x000f¹§!n°|÷à ù~é{0#gVG\¾Gp¡\x0013Ó|çc!fèÀÄ
¼¶\x000e¦¡\|SsÈçcÆ!fìÀÄ\x0012]\x0012(hè,«ª'V\x0012Ì¦\x001cVá^ùFñek×\x0019§2]Öê\x0011gó9k%Ô®°5\x0006oÑÊ'\x001cËÈÁ5kÄ\x0001t¬tlWBJø²\x001cë¢,5\x0001ë'¦wÏç¬l×Bi:ë \x0006ÁyÎZö\x001fB ÉJ\x000bÉv5¤\x00048«öÒ¼8^Æ2ÂÄ\x0012½\x001f@¡U\x0016Òsø\x0007*?x~³z\x0002Óîæ×9	$'@Ä\x0006st¹º0Ä2\x0014jtGÆùéÑóÓkÜ,ùÝ\x0015fr\x000fFúDD­¾ÿtïÜWD´³Y=>Þ¤%~þO\x000f7O·w©ÐÃ%@¸}\x0019ðÕÿ¼»ý-áYÜBQ^ë"\x0018k9XàÏ3à2Ã-9¯NÏÏþöììÍÛwïNÓþ¾Ó\x0017×W§×gçj¥i5dÞèÖ\x0007il²æ\x00012bNw\x0012\½lÍc>\x0010dÞØ\x0005.\x0007&c\x0011Òp\x0004ÃÁ\x0001óQÁ\x0008£ey_\x001f%N·\x0012\x0007I¤ëè\x001c­ÆÂÖ {¨³çg{)A\x0007>ËH¦°\x0003LÏgi\x000f\x00047KwBf	RQý\x0013@Zt\x0007{; Áü\x001f\x001c£H)9g\x0006'éøZ\x000eº«Aæm×Ýo\x0007dÔT4o'2äÀÒXF	o0ö!ð||\x0016C\x0006×ÄLi\x001cÿàÚ\x001dWpwKKK\x0012=ér\x0012,Ñµ?\x0010$ª~½ãqÌN¢Än|-á¯|R\x001fè^¢±&{5*9AL\Å/&üÐ1\x000fõ|pKîýÉ}ôi'a:RãFÓ´óDÑÈêÓ\x0012çPî\x001bÀRäy³ð\x0017\x0005)Ía ñ\x0015ºî©r]`zä²lÎrz0ëm	%æt}¯T\x000f8º)TÊ\óYj\x0018J¸ñÏB·Ýfe*÷J¢ÈQ\x000cÆYiØØPá \x0012ËôÑ	\x0002\x0008×g¤Ã4 tV{ÆÔ3\x001fù>L\x000c3¦Nõ&9f%i#õã&×ó\x000cÌ}(+ÒG.\x0007\x0005ãñ\x0013fÀMÑ\x0014L?OKîÅÄÓ´½§Þ\x0015CXO\x0007v£\x001dlæ©É}\x000e)]7¥òÇd\x0017á\x000cd2Þd7ú0\x000f\x0008»nÓG'¥K±V²1sÛ$`\x0016Én\x000fó°ÿåYúè4Øó*\x00172Ø5¦-Ê|X>¶\x0004\x0013ã.é£\x000fÓær1r$5ù\x0015vàH.¹ýõÏ\x001fw¸\x0015ÏïîV·7{\x0018tyU\x00030ºÈ{J]ddºáÈ²mÄç×ç'gïN÷#¢®U¡\x0011~ã_8Ö|+C\x0010$ÖpS^ä|H|º\x001bR¤BLô!¹àY÷Øè§Î|Hì\x0008¶½È\x000f\x0007\x000bãs\x000c\x000b \x0015ÝHëÃTÐ`>$ÊÉMY9ÿ$ÓX¨\x0004i\x0014U\x0006ÀÏÍA"ëü\x0012È\x001bñøñÓCºpµËv9\x0000|û°º}¸ÝÇçÉ»Ú\x000fË·òfÌ hÎ	NÛ\x0012z1÷J½;z{urvu6\x0003
}¦²Þ¨\x0001m\x001d#pw\x0004açâ7_J;\x001aü¬eáN\x0003Õ©42¡iÌA%4o\x0002£mÑØ_hEÃaæ5µ·\x0007\x0011´ã§+\x0016£á»
º\x0003-¦-éÁj\x000b\x0011DÌñÁnÅSZÑ$ê7);Ø|d-ì9Iu\x0004)è\x0007µÆn43ÑÌÓç¿ü:\x0008ò\Ý?}M=	âèõÍÃÏ«4zJ ]HÏ\x0014,\x0018
ú\x0010\x0015ó
ç¨\x0010ßåõûÔÔþñèõéÕ\x001bøË^J¬\x0013I\x000b@{0C´hÀdLS0\x001dÛ¯6lÅO:1á¥=Ã?}>M%É:}\x0016\x001f\x000cG\x001f\x0007ÂD§\x0002ÿôab­{yÉ\x000eS\x001a~.QnF&z)á }÷a\x001aC½T×©3¥ÐEJMÿ¯Rb0}tazÌ#Ñoîì±I&÷*²"\x001e/âDÉ>ú8uä 3ræ¡4X\x0019æs+\x0015ÒÉ\x00193ösÊ4zÌÅm©2K8\x0001>ú8ÂSó4Æ\x001dX$%C.}tq*+9ôìE ÿ
l S\x000c±­0~\x001fgÀð^úèâÄ\x000c·¤ó\x0004ÛQdÖGWøV$¿\x0013§Ñ>K\x001f}yavâÔÏÞÚÈ÷î'/ÏÒG\x000f§1oÍNG	{NX³®ëÄÄ\x0019{¯'8|£ä8HPÂ\x0017ÛmX0°Sââágù³\x000fT\x001a\x0014î\x000cê(l
\x0016'úÍpJ'(âòg\x0017(no¡$|\x0008\x000760\x000bz½íyu*ì$È} :¯AEPë¹ÎÁÀ\x0001ª¨\x000e"A¥R	Tõ¦¢\x0016
Q4õ\x0004ª-'\x0019ÃVÔ¢\x00134$ÐÐ
;Üé§\x0017ò8PQ)\x000eó­XZ\x001fhÚÉ?û@µM}
\x0010©\x001b\x0010Aµã¶ú ÒI¦/?û@E\x001e/
 8ôÂ,6ã\x0018ÊÃ`¢-?»0ËcÈ\x0010Ó9.{P¥(î
8\x000c(6ÝåÏ>P#¹¨@{íÍ	ÔÈ ñ0ÂÉ$+Ôô¡Ö­Íeø\x001føÍ+\x001døÊ­Äh\x001fhªõÈ} 2ùÃ	ÔhZC³;øDÅa¼9@L2ÕýÓc\x0018P\x0013%qM
>Qõ$é³\x000b\x0014\x0014SZtNÔp´_:\x000fj!\x000f\x0003j`óg\x0017¨ÁùÙ$Q\x0018-DN\x000b<OµhÂüIÇ»\x001bjTÚðõçÿùáîöñf_t	óöäÂ\x000bv¢lD¿EÈó²N_½;ÝÆe\x0005íh *Ibâèui3[(9\x001dµ\x0011meCÙ\x0013»-DJzÅµ¾>®ÓMzÛ$nCÉÄ4\x001dçc\x001cøÎy/È=\x000fByÊÑ:\x001f¶ÄM#\x001cöG§v8Üú#[AÄt°D[E©Íp\x000eá\\x000f5©Ô<Á\x0019\x001a­\x001dwô³z±ôä«T×Ïj-çDÆÝ¤-¶«põ±a6DéØÃæ\x0014»Á\x0004R\x001cA\x0004®\x0004ÁìÈ26çæºÎ
ÜWCðiåD\x000eïsÍ\x000f¼¥?*Ö)¤v¸¨HÀYQ\x0004 HÅ)BïâxÆf6ÆzúèøQ\x001d§«£´Ô"\x000cØàçÝr©\x001aÙ0Â£7Æ»Î\x0015#CºQÙÜ%\x0010ãLWÛ~#ÇòG/:Ø$Î%6ci}\x001a\x0010Yz\x000cA/}
\x001ac9é£\x001dN\x000bºp\x0011\x001c\x0012A\x0017Îó\x000bKÑÒÖ£ôÑærW,²Y^ª\x001eÌ¦ÃBÕ`°§=}4Ã)¡é7u
\x000e\x0002h«XÎm1B6ÕspTÒ\x0018\x0001t²±Ü6»P\x0018\\x001d>ÚOM6ð(0ðpZ
2/ÚÎ\x0010Í[?îþHÙ@üI\x0007ÙãÑëÕÃÍ/{Ó¾8°Kd6Ü`KÙBT\x001càpÆîòsß\x001d½>¹ÂÖ¨]ß§prOúhæ\x0003Ôá|1ù\x000b\x0016&ë-´Aóaf!}4óE\x001c'±¤2^d+Ó\x000fíöâáªÄgé£\x0015/À¿²/\x001b\x0005w?ÌãD/®xXÌçðu=?/¾ÐÔµ¤¨ztF\x0016\x0015¶U¢ØÌ\x0007FNªCNR¥\x0015Ð<JÁz´\x000c±û	\x0001#z6\x0008¨Åp½P7 K®\x000bÐçI7\x0008\x0008º,Wª\x0001`n`U`Xì\x000c«Ì\x00074)¤b!Ù>èì\x0001 îjÂ¸\x000fVÄ\x001bæÛ6 æò}Q?Ý}ýaÐÕÆ5/ßÝþ°ÿéJgD¢h±\x0012S\x0011É
`\x001fÌÙ8.ß\x001d}wöz\x000eTª+ÍTÓ^ón° K¡3nÜàÉ
åZ±t=d_ßRÏ\x0000s|Zz«|¼\x0011k³\x0012mæi*\x001c)ø´Ø<w#aÚ6¬RgÓvZ\x001eA\x0003pð\x0001k"¨\x000e×;[³©¸ÿ£ñ°\\x001a\x001c*\x0001\x001c-n\x000cØ ¿»\x0012 \x0011+eÖ[±¼A\x0016¾Qå\x0019H\x0006.¤ÛñÁ6,T±\x001d+\x001ckª>r\x001d\x0018¥Ýº\x000eeÙÕ"µ\x0013V.ô
¨ÞÈZßí<O\x001b\x0013+é£)Rä«5Ç³\x0014NaÎ\váÍÂÍëÏÒGãohÓF¦T[ (°F\x0011s%W£ë§_~ÿ^\x0001J¬ôQ\x0007Æÿíõÿ|X}ù´'ªmBÛwÌ:À\x0003¤+¦çTá\¼Ü\x000b\x0017Õl\x0017hÌT¹Ð	 ­/¤'µÐÛ£\x001eJÁôÑEE«ì ãè¹z«Ø\x000c\x001aÓtPÊT×?»0qr\x001bN¯´XBM\x001bìÀÉ1dNhÑ\x0006JÿÓo¿ÞAJD\x000b~¾øñæçÛ/8Ããíí»}\x0011ý_/V±Áóá",Ï\x001dß ª·ñÅ7§oÎ.p|ÇÛ³çç»\Õ¯\x001fåÿô<âý-OG\x0017÷¿ß<\x001c½z¸¿Ý{|à/¤f;8¾X-#÷é©6êë£Ë¿^\x001d½ºº<ÛukÌ­nÕ6L£l-%öhdJúÙ/5AÞÝº¯?
ZÖ¿ñóû'Üü÷u\x001f\x001f\x0008C»nÊ\x0010T\x0012¥&Ðm¥8×?óóËkÜû÷~/\x001dJ\x001cüÓ\x00074Km0Ì©î7\x0008»SjwÐaL\x0019ÿ4Óa_*ÕxÛ¨9í\x00154G6­Üô\x001bzèàüñO\x0007H\x000b¥ñð\x0004Ç6} Ý@§¶ÊgÛñÖ-³í|`±;êöóÖ xl >±UæÙÁÑ¾ôÑÎ§D\x0016Ð¹ØËd=â½¥jùåK\x001bKÒG3\x000f\x00139\x0016T#	­Ê´\x000b»ÕbÞÎ*ïÒGûù	Ç3b4Uß"æ¢\x0004»5N`6ßÏOúþ÷§äy\x000cÆ\x000etð\x0015{Ø<|#ì¢ÊÑ°l£ê\x0018J(l»uï\x00130\x0006÷Ri4×ÒG\x001b\x0016XÇÜY\x001a§\x0018'\3ÍÙàÝ­-3Á0\x000f>ÚÀ°~*4=ÆÁ²\x001b½TäÇ¥GBJU\i&N3Ð\x0012Ó\x000bÊq8Âí6÷&É>XñÃ'Ä\x000f'Ê½]=|Ü[r \x001dÅÒ±úÓES[Ì4øìíÉÕ½@Uã< Å#g<Øuäï\x000b]"\f»ã£Õ{\x0003ñ9
@FÐ¤\x001e\x0010\x0018c[v<	=\x0013¨ª±\x0007äuÉ~\x0018^\x0001\x0012¤àÌ\x000cü?,\x0000Â\x0004Ï3)Àhç¡\x0017 3É»:J¾×£1<x8²í¤,|à_ #¹Ç\x0018gÆô\x0013¥ì\=\x0008\x0007Ýæ(ÔÕ}zbyµ\x001do ÂXSúh ß=VÉ*\x0019d\x0011çÐÆ»tgòøôêx\x0014îX!}â\x001cZ3'p\x001f/Ë\x0004úéIÂ]\x0018\x001bOðttuÿåÓ^-¥9¦D\x0014vyÐÅ¶¶$zôÎ®ÿë£«Ë;Eö\x001a
ÅkT\x001dl@D1w\BAdÇ&³7[)f¶u°¯ýà\x0002Wy¢wn\x0003ÑqÁÓ/4íþç_~ÿ9ùºhÑâ\x001f6ö°½\x001fl½Û¯ûb`T
bý¹*s\x000bb\x0001\x001aqLö¸µÍý`ì¾ß\x0015e+\x0012ÕBúh'´Qp~L`p#\x001dKÏ¡É¸-.z\x0008ÑêK\x001f\x001dà\x0006Å\x001c-ÀÞ²\x001c¤\x001cñÆÝ\x0016ó~Bõe%Õh'îãÑUº¿1NOp¹L+ÝÓ«rWéî»£«43u/TÉÐR=d&Gèñ§
loIaÖoáÜ@W¯N|Î¤s¤9ñg54±\x0017«\x0001éåF³³kh6\x001dN·}>é¤Èµ\x0018yüÿCÏ»Ë*æÂáÄôÑ\x0008\x0007*"b@\x000býT¨áR»ÄB:2>ÚéhÈ\x000eÐaBgêc5ÜÅÅ?¬ÁF­ôÑJ\x0017ðzJ·\x001bR\x0017ÞÓäz¥åDAÊ4ÜOîËÓç»ä\x001a%;r\x0018\x001cxym\x0000É{õ°úòqå¢ÏUn9ñÛkÀùåú©ÝQØ
|¹WW'\x0017/vÖn\x0015`´çì2à 2-xl¼ðfÇ!ìêîë}^[Âµ\ÃÐË-h\x0013´\x001aö\x0018\x000bÖ{Ë\x0003\x0008u4$\x0012\x001dØ/Ü
dìTpò\x000cô	Ú\x000e»L5$ÆÖ6ãkó!5\x0000u\x0010TS\x0003Ì¨·¦§u1J¬¿L\x001f].bh7Aâ¢
\x0014<FXm\x0015÷AâwM\x001f](\x001d¹±&ÒSÜÉEGÃ'\x000eBÖ¡\x001cM1r]<ø´\x0006w
\x0015\x0001¿øTÈw6¥EE>:(Ý`\x0010\x0014\x000eÛÏ5\x001b¸Ú]ÂNf\x001dfSz\x001c'>z(\x0015P«\x0002¦\x0004Åt°ô¬
á¶2-?ýz÷³µÉ3Gõ(\x0007/<OØÿåþæëOº\x0005ðëlÒyÍmzm]Ä­Å¤M\x0013öß^¥ùú{(\x001dz²é£2¢
$)(Ê\x001cT\x0008gµe¡uQz4\x001fÓG\x0017¥Õ9¡94ÂÑ|q\x0010;ý«&DL
¥.D\x001f\x0010D¥¦áõÁSRVoU¬µ0Þ¯\x001e>ÇdO
´'ÅñjõÛ\x001e6\x001c\x001c\x0015bv¸:\x0013<ÇBâÎtØéÑÕÉßöBa¼!}4Ai«´¹"N\x000c¬ÚR®¾3ÿ:Jc\x0019Púh£Z·ºøP¦jÇÀ1\x001a¿3³9
ýØôÑD\x0005ö!õÊM\x0012\x000f#Å\=\x001fv&¼¦¨ô¿þôå12
µF\x0015aëðÅ«¯«½Ùþèó\x0000ðôà±J2f\x0005Ç¶àgÝ9,rm ¾øæäýÉÕ®ÿ\x000fþ#¬î¥®ëê/«}zÃ¥@n\x0006\x0015'S{uT«&»¯/Þ½;Ù¥2ìÇ»þqXÁ¹þuÏo\x001fVû<Q\x001c	\x0010cI2å\x0002æ\x0010Jô
äÈÎðÇÑùÙÕÉ.¥¥Vp[Ëß9dQS).º¡<\x0003 V\x001c-¶Ò'`\x001ej¦&°¦
).
O"´¢æ¹ð¿ÔÇuÿÇÏy\x000f\x0010¦
c\x001dÌzýpûùóþ`\x0016ÚÊ\x0014\x000b×ÞN\x0005ÉRzÒõVâ õúêìÕ«p\x001b\x0003ÊT0ïT\x0017!öôÓ¸{\x001cÞ\x001c3¡'oN÷¾SÌ'T³M\x001f\x001dXÒO)tïr[\x001f\x0018(e÷ÏVWÿ|¾§?~øz\x001f/ 2
ÃÑ\x0003\x0018®ü}_¬\x0012§¹R7:¸ðF\x000e\x0008\x001eã{7Ä\x0008F*ÿ¾+ª?Ü?~OÒ\x0018*\x001dÿ\x0008RøÏÿÞ[ë	¿ H«se¬XÓ[Í#IÛªº\x001a\x001büuw¹§¸¿ÿýs\x001aq%\x0011®®8¿ÿòÃÍÃýÞa
BP.\x001däYäiö\x0016\x001f*\x0013îv\x001aîç\x0017¯O¯.wM@\x0000ÑS3òÙú\x001fÉú\x0010ï¿î\x0001*b)yÆ*µ¥Kn`¶;\x0007xïñ\x0000Ëæ®qB5$Tí`¢H\x001ab\x0008Fªµ²\x0014ôÆ²o.¢\x001e"êvÄ¼Ë4\x0017`ÉÒ\ª¹Ãnwûµ"Êê\x0014eó1bå8¦ródM!\x0014Ât\ädÃVÿ6ãäUÔ¶:EÛQVú¥sX²*.QôS¥9®z-®ç¹X\x0016Îè\x0012Ä\x0005q«x 0Ä!a\x001dÏE	á`Ìä5è`>R¿%®Û\x0010e¨ENh?E)]£³À81¼®WÜL\x000cÏDü ò"Ã"\x0015Ã?¤e+\eøxÿå\x0008tß\x000f{"¿!X[(1Åi²å\x000cÞ\x0007V\x0017R\x000elË½=?Á-ï./@ù½^G|9\x0014\x0004\x0017§\x0002;A£\x001eÀ¾YýK\x000cï}wwóëÓþ>vÇ:Ï\x001b{îrâö§íÔá7'opar½ÏÏO¿»>\x001dß¶8äTCNÕÃ>\x001ck)G\x0019[í¸Lo
ØéáÔCNÝÅiKðÜ/"c¸®Ä¦ìîá4CNÓÃé\x001cûL.N.Åñ5ø_Ý\x001a£ÖÃi¶\x0013G§\x000c÷lOè´õ[Ò§Ò
)]\x000fe\x0008<ðÆ	ï\x0008oëä¬\x00161¢\x001eN?äô]¯]W¤-\x0006r\x000ff)çs8Î0Ä\x000c*Ð=hHî}äQ\x000cNnµdö`Æ!fìÂ,	\x001e\x0007\x000e\x0017?õ°î:<\x0000¦\x0014\x0017=ðrÈT³\x00074\x001cbSÍm
@èá¬UQ.r\x00078TKd(ÎÃVíb\x000fh¥d2Â©9v-ä=oü(ÂSÉ\x0003<wY)#Ù£À\x0017^7ÆFjEÀ$9\x000bù-¶³RF²G\x001b	ëyH*8±<¿I>#²= 6=êHàÜ{\x0002Å\x0002\x0004\x001aå$ÊSÚjíèá¬ôìQHXÌ+£õ\x000cXvUql-öé\x0001­\x0014ìÑHXÆÁ3ÆÀ1\x000fù)¹²keË6\x000bªü÷êö§¯?ýðýzö:Tµú=eJe¯à'f¶·no\x001eþínõo¯î\x001fþüï¯HêîóÌ8/crÇ\x0015\x0006K\x0013!®C[[/Ï^^ýÛùÉ¿½º¼:}?\x0008]ü\x001dþÇ²,ÿ²Í\x0017Uwrb±n\x001aõèÀ2PA9å\x001dã\x001cî¬\x001by&V[vÒð\x000cä\x000e\x0018ð@Ö¨)\x0006mÁÜ1KYEüÇ§_~ÿ~½Äøüöæéèåí×£»£«§ÇÇ\x0014tÅ\x000bÊGä©è^
K=ZKOó|ÁÍ\x001b\x000cÂÙä=?;\x001b{öþèüôèêú\x001d8v;¼ûéË y¤Ô9øÁ¯î\x001fó¦¬y°XVÆûÂ\x001c\x0004Àb3\x0002\x001e\x00186nÁ[üêò\x001d®ÌÚ\x0005ùëÏÑý\;tèñùêé·¹i\x0010X*Â\x0007µ\x001fC\x0003k«©ì×\x0018'v¿*\x0004|~rý·9xy¥z34y¾\x001b\x000eqÐL\x0019ÏêAI~3Þ?¾ÞDûqxzëkù²æ³AS·!MoÆµ¶IÒkã#\x0017¡4q-ß¥Dúß­\x001e>Þü?·ié0\x0017Ð¢§Af8\x0017)\x0019$\x001aþÆ¡\x0010ãÂîG?\x0016\x0013'ëÐ\x0008ýÃ3j2zñãê\x0001¡AX½^=Ý¥föyà\x0006îå%o"q×F\x000bËqá.-iu³WÈ
2ëõÉ5è­ÝB¿\x001e~\x0003½ô\x001bXáx\x0007\x0001FlÓ.8ø\x0006æö»/Jç7°Ão`\x0017\x0003¸1¼îÁÚ\x001c\x000cÐÆ\x0014?FëÝ\x0002¸ó\x000b¸á\x0017p¿\x0000N\x0002¥Î[§s\x0006\x0007¾\x0000¼
Ê\x0013B¯ó\x001bøá7ð¿A<Ý\x001auìó3°ÅþUú\x0003}0ü\x0002añ\x0017ð3£VgéMÜwïvkÅNü8ÄKñÑ\x0010´H$×¥ó/oÀDuè7À\$HÅò+¤y\x001c9î\x0014Nµ.xTÙ\x0012\x000e}d­\x000b\x0016+\x0003ãaèWÀù\x001bx\x001e°jB<ô3ÎAò
Ôò{Çà\x0017 ÍcxTÙDì\x000fý\x0010d¥Íäbuæ\x001cÝ!!É<3¶\x000cm3áàÚ8G9
¿Y~"ý\x0002&Æ<V\x0013ï\x0010OÃÃÑ³þ\x00066Õ±Ãü*\x0005ÉÚ8Å½ý8ûÐ_¡ÒÇr±Bv¡\x0004ò\x000cN\x0010§¯ ×Ëâ'Üå¾oPéc¹X!ûIÅ©S5Ö¬ðCöþàú RÈr±FÆ¦p¢\x001b\x0017s&
\x001c\x0018ëø\x001aÙ	\x0007¦ó+TJY.ÖÊ\x001eµ2}\x0005ü6ù1ã¾Lþ\x0015\x000eý#¨J£©Å\x001a
\x000b<\x0015\x0005ËíáG(î
ü2V\x0008ªR\x0008j±BðÞð^\x0007h\x001b²Nó\\x0004j9ô[\x0016úûUí¢­\x0016;\x0008¦¬\x0008´\x000c\x000bxÎe\x0016é¡¾Â
á^ò	ºÃ¤ÍãÑùÓ×Õ×ù1'ðs©×F<³LkÅ%éN\x000c\x0007èmâ î»£óë÷W'ïwÇ
»\x001a²«EìÞ\x001a*ÑÐ\x0016þ]Kði?î ß­{Øõ]/;wëò&u8wM­2à
\x000bò*Ø-|zÈÍÜ,"ÇY\x0017¹¤\x001c\x000eZ¤*d\x0013\x0001rèÊ)9\x0011¤ìA·Ct»ìÐq.hF÷É=5\x001eæC·E÷Ct¿ì®;}LW\x001d;\x0014M¾êTäê¤Aô!yøÿÕ}Cô¸\x000c]I\x001aÑ\x001dxd¨i\x000bÖ
±c¬éìòû\x000f·µpÇXråµÏ=áÊ\x000bMÆ²\x0006sß³|\x00079~ôµ6"¸ànñ¨ÿùÏÿ:ùùÃü¼
Øõ"§láïJaß=¦BÀ2ÈØVª=nÊË£7Ï'\x00126W
yU/o\x0008©=­±ÅâºQB<Vû\x0010y\x0013¯\x001eòêîóîØe^\x0010"y\x000e\x0004/MH¶Òì1¼fó!¯é>_lp×ù|qa¸¥ó¥Ì5X\x000eu\x0010^;äµýç«s
G+<U\x0019ilÛäãuú@Çë¸®ÿx¹%VaoyZÒ©q±\x000f]_3¬1[Äë¼¾ûxAåFcxZ\x00021J+\x001aue°xÃ7t/²'k\x000fÎTQèN¥	×¥¼Rn$Ð\x0010lX;ñÝíÇ\x001f9G¦¹\x000c_åî<0Te©æSsê'¾;{ñÍß÷3«!³êg\x0016¶TE+gÖD³e\x000ec\x0008\x0013Ñ¹Ff3d6ýÌ 'xË§áh¹\x0017è\x001fOÜFd;D¶ýÈ -Oò5¹\x000e®Æ:d§Ts#³\x001b2»~fåq(JºÎQäópÎÀ:k\x000fwýÙ/8çÀ;°\x001aÂýÚÎfÂøle\x000eCæÐÏ¬u)PÇñf¹®AEW¶ØL\x0005\x001bã9ö3c\x0005\x001b³ÍË\x0018ðyUÕ;æuV.Ig±àÍ1¥R\x001cÞ
OçìË
^1\x0011ùk®UÊ\x0002\x000262ç\x000cäÃö¥Cî`²NV*E.Ð) ­\x0003ëA7`\x0005I\x0011\x001cj"dÐ
­+h½à 
Wâã`\x000eµÚÉ2k=\x001eL\x0011ÊJ\x0011Ê\x0005\x0010Ó³Tõ\x000c\x001eI*ØD»ê<**\x000btap\Yiqª¬à\x0000$.Â9Üí¨T¡\ \x000bm(Í2UG&fUêYQÂ9\x0013ºÒr2ÄMC4_\x0004N[jÇ¿qùâÁ +e(\x0017hC\x001cQN¥OQsIk>hç\x000fftÈJ\x0019Ê\x0005Ú\x0010Í#:gÁ\x0006©v¥Teª^¶YUÚP-Ð.äX:Ê;[,R´HÞ
cíÎµ»+U¨\x0016¨ÂXô·ñ3wÚ¹\x000f4\x001esí^-Ð@J\x0013y¬\x0012\x0018Éú[i>f5û÷BWºP-ÐÑå¢¨ö\{¥½/js8èJ\x0017ª\x0005º\x0010],®\x0005ÚÄRmu0+ZUªPõ«B,é¡\´\x0011y´\x0015 \x0007ÍçÖ\x001c¹Rj*\x0004RÊ>#~©\x000fæÙ!&ØÃI»J\x0015ª~UrYì\x0000i'É\x000elÝ\x0019é\x000e¦¿U¥
Õ\x0002U\x0018JÐ\x00005ô¤WÔºàýPÌºR+zZ\x0001yGµ×ÉGô,ïJÙûTP´\x0011º\x0012ÒzÎ]9Y³èÜ \x000c¥¢Y\x000e\I;½@ÚEÃK]1Å/ô<¼Ö\x000c\x0007Ã.®D^ :¼â¥ªFÒI\x0014Ñ¥'BØÃÝèê\x0015ê%\x0006©âÉ%:øµAÊ7Z\x0007u°\x001b-¹L\x000e\x001dà¿ü£\x0007"lv¡\x0014D/#\x0002o\x001eÞÞ<ýr\x0007|³S°Îè²KÅvËÁ\x001a®ÛµÊíVebàé»£·§×oÏáÿu*\x000b\x001b6Bêø
ÔâoàJG2.­|oÊf>=Q÷Úù
ôð\x001bèÅß@h.ö³Vp\x001cGYWz ânÁØù
Ìð\x001bÅß@òL
¬u"~/KRï~¹üvÈoòl)álø\x00021Û´¸£|ÝÞpç7pÃoàÀ£©¬\x0013SÛVÿ\x0006~ø
üâo ×ïØYÿÒ­Ç¨í¡_ \x000c¿@Xü\x0005ÆLbÕ%½\x0002áK+Úmúv~8ü\x0002qñ\x0017ÀuH\x00140t\x0003G¢~8ô\x0017\x0018t\x0002sXø
@ùÒ)\x000b\x000e5¥x¤\x000f<õÁLt«w~Z\x001f/VÈ\x001a{A9)8³&Õz=øD¢¸ó+T
Y.ÖÈ py&\x0005K4×ïàp²ò+Lø;¿B¥åb¬°õ¾åH£,++¬¨îü\x0006FU²¾iÀAÌÃ\x0005à1ÛõèÝKçW¨²\¬ÁìÉó\x0011ð+d¾¼Ñ:±;®Þù\x0015*­,«e)@
»Ó¥æ\x001dÖMt\x0018÷FCß&Gø\x000f\x000b¿HLK\x0004³}¡°ç8i7S¦sêRÍî/ò5ù_\x0011ü¥\x000e*Y1cq´lvx\x001bB]úE¤ß,;õ¥ìôæè\x000eKµ¾|º¹»=ã\x0004\x0007¿\x0016¢çXë`í©5<=:?:¹xyz~91åÉÕ\-"×V²b&pjO\x0006\x001e "Ý\x000eÑ6r=$×ËÎÜÐ^2<snK\x0007ÁAM\x0010|\x0013áãfr3$7ËÎ\É\:	g.\x001cZ§Y	ðë}}Màv\x0008n\x0017\x000b°\x001b,]óÈ&.3DðfÚÁý\x0010Ü/\x0003×´Ú#àÂ¸lBk_6;
}Ð«\x0012àaÙ%Ç
¨®É3ýàÄ\x0003ÎRíi¢o#Cò¸ìÈãöük\x001aQ\x0005g®\x001cçâ\x001e\VÏS.{8ÛdA\x0005KnyÊ§P{ÚÛÐ]î¡Èî:\x0008[ü\x0016éÔ#ÈBïk*hSDQQ×þõõÝ\x000cÛZ±¶\x0001\x001e¾YåÝ\x001a3ókÁqé³Ò>¯-Ã5¼[Íì\x00197Ë7'¸nc/°\x001a\x0002«^`k¼Ò)c;-Å\x0003Ç¥ÀÙwMf\x0013ë!±î%NCó	+Gmx¸q\x000c,¥Ý>98\x001bØ\x000cM÷\x0000ÉA9W\x001cÆW&¨}#h\x001aí\x0010Øö\x0002;¬Ì¦\x0013VÇ2?<'å\x0013V\x0007;a?\x0004öÝW\x0002gtRjJ\x001aÎ§aë\x0004¥¦äD¤8\x000cC71hå,ãL¼æ`ªû\x000c¿ÙÀq\x0008\x001c\x0000S\x001eJks,hèæf\x0003½o\x0014×|âAÐÑ®Ç\x000fõ 0\x0017èlÅ¸£§gö4\x0010W²Xv\x000bcÜeÅ\x000cBòïÞÄ²fh¡4¸\x0012m²[¶y,M¤\x0001D¤Q\x001e¼9XáªùÈpÝÒÍ\x0007Ï\x0005Î¸Ëå\x0000QS%0mÈ®Bv½ÈØöE7Ù\x001b@£²|Êr¯\x0005=\x001b¹È²[$\x0007\x000co®Kv\x0002Í¨,\x0015]þp¯È²[$\x0007Ì	ÑUÆz®¬öBiÑq_Ûå|äJ&Ën¡Î\	j,\x000fpan)~9ÔëS}¬z
d+\x0003mF1âcàó õáðçÄµÜ-qÙfÙý¦ù*Gã¼Ø3\x0001±\x0001¹ÊªW*{\x0001&\x0005Í4¸ü*![a\x000c¿>5UÝ\8Õ+â<Æe<Iek)3hEàÆ@s0=¢*y¡zåOk?ò!£q\x0007ÈØ 9C®\x000f¬+H÷ZD>ÂãK\x0019p\C\x0015é\x001c(aª\x0008»
¹z}º÷õy@*û4s)³Ó,8-\x000eöò¬r\x0019)\x0004ÿÐéñpoH\x0015O¦ÌZÄ\x0007x0u]Å]²Ê^\x0007^u`\x000c¥j5òËPöàéÃ\x001dø&ø\x0002n\x001cÏééÄÑV²4[Q°mûSRl6É\x0012(únuwwûçÿ}h.
2Ù@òÎ\x001fSAÕExéþîä\x001c[§»zNÄfw¼(A¢\x000eXÚtä­+K\x0014órªTu\x0008º÷`õU÷³*^Ç\x0015àV@Pã|²SuJmÀf\x0008l\x0016\x001c.»PÞ9\x001eèJ¼\C\x0001Û!°í\x0006Öå±\x0005ô¥¨zY°\x0016	{"\x0001óyÝ×õ\x001f°áE\x001f,wà¹Ò\x0001cü0Àa\x0008\x001cºfó-èÒ\x0018ZÆ.)\x001föd×f\x0003\x000fzÊÅ:ÔÒCÌ£m
l"«È¥á¸Ýå@À@ý\x0012Í\x0018\x001e
\x001e¹]r/ZØ3¾h>m%!d¿p\x000bcà\x0001Q¦lJ\x001fè\x0002ËêÅÉþ'ç%ÍÊCK°´\x0019\x0019®\x000cî`ÄÕÝoÎjYÖ£Ã\x000bùS,(J\x0003\x0011«êÍ©î7³L>c
\x001e\x0013M¶Wí\x001e#s>pmDt¿9«-Í1\x0002gOrKá\x0006\x0012­öM.O\½;Õýî°ã"enpÿÍéÑ§øÖÊ\x001d¸zxªûáYCkÕØ	Îðî^Æü«w§úß\x001d\x0000¤ÀÁúÔSV|\x001aFÒB¬«w§ûß\x0011yª\x0017iR\x0014åó\x000cí\x0002ÐvrRT\x0013qõðtÿÃT
\x0000ÄAóÀ\x0002ìt<Ð¥ÐÕ»Óýú.\x0014!pÀÑ¤ =ù¡Úy7Ó;ÚK\½;Ý¯ð\x0000SæÈJÄ=»dÄGÊè \x000eu'ªw§ûmL\x000eI\x0018KÜ\x001cH}eðÜr\x001a]Ç©ë6AQµòeaÁ~Ïë³¸l\x0017\x000fÚ)ÅyÈµH6q:yÓà®G}gtõ×õHÅæ\x0000?´ì7
Y?|Xý>\x001bÚb¨;íIð Ñ\x001c×T
I	\x001c+Ü\x001b«oã¶¾ýÜjÈ­\x0016qµôiÇ ²tØ*\x0006ªë1Q\x0007ÝÌ­Üz	7®·ÊÓQ¼ÑÌZ-½*ç\x001dçÎä6Cn³ì¼-
h\x0006¿IQ\x001cÎ\x0012£]1îMô5pÛ!·]ÂËXhF°Æã4Ú8
¶ÈÔl®Vn7ävî\x000b¸25ß$WÒ=	¡Ü=»3æqÍwi6:îVG¯î¿|\x0005Ô\x0016·P°×\x001e"\x000f1\x00079Lùº´ÿèüäèÕåÅ{øÏf|\x00053ü
æ _J\x000c¦Pè\x001bp÷1\x0013E½_Á
¿[þ\x0015æ*\x0013£#×lh¸E\x001d\x0010Óû\x001dÂð;åßÁ*./P¡L\x0004e\x001b_aÅ­Cåzïb½8ãÛÕÓÝÕìY\x0004ðB
OCô\x0001]	VryØ}ø4RýÛëóÝ£\x0008
±\x001e\x0012ë~â@ó¾\x0018Wâæyß½J\x0005ÿ\x001fí]81Ù\x000em7³ö\x0007¸"T\x001a¡l -Ó2Ý­Ì~Èìû¥BÑ\x00105ín×e\x00041 OØ31`¶iq\x0005ì/~¼ùùöKJ½5îw\x0015iÂ~é\x0006móTéã5?E;3|ñÍé³}ËÛ]÷r!·YÂm\x0004÷ày	UPE
úIÄ³¹áMáa[w^Þ|¾ùòiö%ñ.Í?H\x0011\x001eUú@p\x0004#\x0005LäDw2àZW§\x0017/÷s«!·ZÄíii\x00008ÝÊîÒ`Qþ¹!\x001aíÜzÈ­p\x0007jCÀ¨%ïßÄÍ\x001c´<äi!µYB
î\x0004Å\x0001±"ú\x0012\x001ckqßÎmÜv\x0001·Ã&\*÷p\\x001eV\x001bQÅGÔÓÎíÜnÉygS´fûòÂøÃ1!sXÂìe.l;\x0012Å±Ë\x001dBÆÐX\x0018(3¶wíå\x0006àzï\x0018þÃ 6ñöîö/) ÒP_£UÙî,/¶6ªl~³{Vié÷öüìõ\x0005FU&\x001bõ²\x000cz\x0010èB¶ Û@mYÆ¤VÒì@ìI)4¢ë!º^xê¦l\x000czF¹²:sGY\x000bº\x0019¢èñ8Ð Oë0°E©§â¶íÙ\x001eÛnèv\x0019ºIþ
O{¥Ò&`/[\x000e÷6^4¡û!º_Ëkhà4\(\x0002\x0015_ýÅ¾m\x0017¦\x001e¬fÐØõ
¬^\x0007,LÉ
ÛÒÞ05á¢å\x001bÄÍømÜ\x001d÷p\x0003_ \x0001ÞIB=\x0015Å.ÍwÞ*ÞM ÜÜA5W§ð
æà«!þæf|ð¬#|GõµÆr
³ò\x0013]h}øz¿9¢¦\x0019\x001fü"§¨$QRz\x001e.äÄ¼f\x001f¾\x0019âoÎ§i¿<ë±\x0015
O:}Å>?\x000eM?0¿\x001dòo\x000e§iç\x0007w#ã{Á¢\x0007ì\x0006Ï·g"ØïøiþÂ_È\x0000\x001dH!¸oïV\x001fKúô»ÛÇü­åË\x0003'^fª{¾<`Zî>ý·ç'/(L}úúüìÝ®\x0012W\x0002\x001ft\x000b\x00028°-!·²L×>­Ìæ¡\x0008µj:ß&ßwêÆAW\x000bá­Êë\x001aqB«(y~ÃåÛÚOt¶uÀ
Þ,\x0017\x0007$jÜÑNw\x0006«ó\x0008~"®1\x0017Þ|\x001f>üúé¥®Ëëû§»Õ\x001f\x0014r"5DúâîÏþ|ó%\x0011Z+\j\x0006,
lÅãõRFü<¡C\x0018<Ê\x0017ç§oN/Þ?{}y}~rñz\x0016\x0010 þ\x000f\x0004\x000eDê¥\x0002 G\x0013y\x0011(ï\x0000§N\x000e¦ õ\x0000Áÿ6þ
$%Ux4ä?¸\x0004\x0004Â*)=\x0001öö@éõ\x0000Áÿ6þB ºÒÄD<!µ\x0018ËÙ2t{\x0007Qà\x000e ¬ÞSMw\x0008M\x0001:\x00161\x0003yé\x0008hXQÖ\x0003\x0004J\x0019ÿüe~2,\x0017Ä?\x001d ¸Ðê¯t©±vNµ\êÿm ¬ÛÒ-rè\x001d\x0008\x0005ü3\x0017\x00080|lafÈÖ #U\x0006RÞL\x0000\x001bC\x001a\x0014àùo\x001e<ÇTZ\x000c\"öp<2x:\x001e£&Ð>\x001aP9ø§Aiø\[\x00074æ\x0002%-Fg£mP\x001a{hpxm\x0011?\x0002[å2
"
ùlD$\x00187XíÐ\x000c\x0003wØ6Ýc-rm\x0005À	â¸\x0000\x0013ùdõÉÍ0ð=lÓ­îXjú$ö@&\x0018Ç\x0015ãï4¥ºFiÜ\x000f¿|?S aX\x001e¶:zñãêÃêã÷_¿î]i5\x0004Þ +½ uÊXnìósw*Ü .=99zñÍÉó\x0017ß\¾¿ûí\x000fHQôÚ¼\x0016Î¢Í±3$ÍEÂ
Çë-\x0006ÿSº\x001bT¹¼}\x0016@1É\x00143¨p\x000cê?\x001c)¼	ÓMêhá%\x001a]; µ9±$ÜpÿbP|3Ý 9í AH\x0006Õ´8\x0001@Ã!|¸ð®\x0014£[/T\x000bC¤ðÖ\x000fø¾_áZõÂ\x0006\x0013tùñkaTåñ/=ÖÏ¿\x0007õÛàXÏoo^Þ~EÖo\x001en÷Ræ¹\x0003ß\x0017N7Sª@CºÁ \x0010rû=^\x001f½<{ß^_í¢\x0003<0"B\x000f\x001eVJfO\x0012ðBÎ¼ál\x000cå\x0018Ïn{ÍxìàvðyÖ=Àgsq8N<Èó´OoÿÈÍ|ì\x001a4óÙ´f>á9«r/\x0018ñìAè@Dâ\x000e:û«2ø×'\x0002ýºð_l¿çv>òc:ø\x001c^6\x0000ðr}z\x0007x\x001bØ_£{.\x001f¦Òùq8¸6\x001f Ø'\x001e=Àña7î»|&y\x0014Èç s\x001e<\x001cáo\x0018Zîæ\x0003g¶ïüpA
\x000edô\x0000_ ¨\x001dÌøØ·_8³yÝLhpò®ÖtL(¥T\x0014H³Ql¶] mþ\x001d".s}×ð_E\x0008?±ëÿ*BøÝ_ðW^}\x0012+÷aÌy³zøzûåæë>@\x001fµÇ8³ÃÀ¡gCÁD»BÀÝ\x001e\x0016Wn\x0011¾9¹zvqºkøípËV(ã±ÉQæò8 \x0014äb¡ãu\x0018@x$Rõ\x0001Ü1&\x000f=ò)ÏfÛ]íB¤ø}\x0007¢ð¹Æ\x0003Ü(Aóý@ÍÄÜà/Ð°hZ\x0010AsâvÄ\x0000niÚþú8_Ä`óRY$\x001c,Oj'üã§?¾Ü\x000c"\x0013/\x001fn?¾ØËådTÇ.{ÎØ\x000fHÖ\x0002ë&Dm°Wg¯^]^ÍâÉñ¿\x000eO\x000e3üux²þááÌ_\x0007¼ÿ¾<ÈÏ¿ïáñdYâçùêèêþéñq¯¢Ô\x0001R%ñÚ<\x0012ÚEçlfR)¬²õüO®.¯ß½;}öqõiõøõá¦ü @d\x000eG»æH\x0002Ëú¾»y!\x0002N\x0017.É'ø{.\x001c\x0006õÎ9\x0008øÛH¸Ëø¯¾;½O\x000cJS0	\x0014­fPå\x0015Å$Eð\x0012K\x0010\x0014\êì>À¯>\x0012êk\x0006¥a\x0007\x0004Xû:GTã:¼éD£('\x001a¶ïa+¨¬Ae\x0017©à%P¯L\x001eP\x0006 "Ï\x0015\x0011p¶s@Gý1õá'uó\x0007r¢LI\x001fEu¾¸ÿø´×Õ±ÚcQS\x001bµ\x0017\x0016çèåHJ\x001c	\x0015½ùâòÅ5¥Ïm*ÔøÑFåÌM@åä±Íáf§\x001c\x0000\x0013\x000eØ~ªd«©f*ådk<\x0016·Pá³òzÂÜO¶²ÍTV\x0002\x0015¦Îè¬Ê/\x0018¦"û¡<Bùf(ÏI¼Ô)Z8\x0001*r)$£
^ \x0017Æ¬ÿ!y\x0005¥É
_ä×Û»;0
û6\x0003eÓ,%°@0Ýmt0»\x0005Ý)>Ë÷gçç»Ç\x001e¬RÙVR¹
Ø³·eÒÜ5j\x001f\x001c\x0011;\x0011\x0012\x000bå\x0006¾ù\x001fÉºíá\x001eTòã^\x001c÷,ö\x001c\x0018çI'{zü\x001amF\¯aãÚÕ%èæ]\x0003V5dU}¬JAD\x000bË¬l\x001aTÛb°U\x000fYu\x001f«!13\x0017Â1\x001d+õ©\x0001ª\x001bÉÆô !jèCu1\x00018Vã¹"Í\x0008Jå[#G¢\x0003\x001d¨kn«ècõ"Ï\x001eFVEù8`e\x001f×é\x001eØúiu¾-¬Í²\x00196¼d\x0006`C`X#¶\x00134=°ÕÛËÇ\i\x000e°^æ^?µO6\x001eædm\x0005kû`±¬\x000eÖc©-²ÉËF¥Ñ\x0007aU\x0015«êcÕ&äzZ+¢MãB\x0012¬wt\x000blô\x0007y_4üa]\x001f,®ËÊ¬¸oXiî°n¸Õb	«¯X}çÁÒDVõàZx:X\x000ek:y[ «ç¥û\x0017Nþ£r\x0017¬
ùÊªÈ\x000e\x000b#ù¨\x001eØêÊêÎ+~­ÄØÙc3`'x\x001c\x000c× - 55}"V;d\x0013¬`Âæ\x001c3Ü\x0001
)87\x001c0µ\x0004¶2	LM°©\x0000`³_¤IíA\x0017[©YÛ§fµ¥¹âV)é9,£¡cõz$·Ö\x0003[Ý\x0001Ûu\x0007,N#T\x0014÷¬¹à\x0003\x00190¸±à °\x001c°}r\x0000O6U\x0007ÂÉ\x001a1|²TøÿÅ!X}u\x000b|×-p>D®¬`\x001e 9\x000b¬iTõ2\x001eD\x0019øê\}×¹:\x001czímåA/YÍË+\x0011\x000fakÉ
Kô-©]ÓÝ\x0017>ïv@©Ë!6?\x001d¶¶\x000cE§i(BnÙÆ©C*\x000fÜ\x0002;*ö\x0011\x000f£h%õ\x001e\x0016ZÓéÑ*² TuÞÀ\x001e­¢$Ö#ùØ\x001eZWÓö\x0019\Êè\\x0007bQª\x001e{G¢ç°£\x0010\x0008²v\x0014ñì£5Å«õª~ !\x0015ö ÷vÃWìu\x0016­*÷\x0016k½J¼o0\x000eäÿÕë9jwÄås#\x0006#Á¸\x001eX]Ãv7ð®R(FZÌêd?Üë\x0012-?ÌÑÖ"Av\x0004¼«\x00145\x0010ú\x0003\x001c¡\x0004c¶û8zXkÏ¶×µ\x0005}\x0010(hP®\x0001×ïA\x0008ybµ@}\x0002AÃ\x001f)j \î\x0006sF«\x0002{\x0010Í êK«:ío\x0011ó\x0008]Õæ|\x0005eø\x001aà\x0019\x001f\x0000V×ÂKw	¯ ¥ËíPù\x001e8JEª\x0012A\x000c\x0013\x0019¾&Ï&\x0014¯}U¯s«OÀôÖXåAþaÿÆ\x001cÄe\x0010\x001b¼¸8 Þ\x00053×IÒd\x0005µ\x000bÅ­ÝzÚ¨çQCSÚ$É=Ãú=£³Ü3<ÓZ§\x0014ö6É\x0015XSÁ>XÐºSá¯ÔÇ'1Oaã%Þ\x0000ë*X×\x0007Wa\x0003UYKÉñd\x001dÅdzi>l¨`C'¬<fÖXzî(è©ãX¹\x0007ªªn¬ê¼±85[¦#\x0005\x0012A}G>W9a\x001e4°ÊUö±Z\x0010¹{Pà03êÈç=`J5Àª
Vu\x001e¬É>9Â
2\x000fà`C(\x0007;!·\x001a`u\x0005«{`ÁÐvyª'ÂFrs%xâ\x000c«F:h{`m\x0005kû`=ù6ùÊæ\x0008\x00028Jz}e\x000fsg+¹¥ºäQr70\x0010RI¯D'\x000e6\x001cæÊúÕ÷±:kzòÁÒpwÜ\x0017aù}©8R\x0003l%cUM\x0007\x001bIp\x0017Æã9\x0004çz¢\x000c¨\x0001VWªVwªZ°¾]¾\x0005J¨¢½4÷\x001aÃÿ/\x0007\x0011\x0006ºº\x0006ºó\x001a`2AQ;½ r!)(þmp\x000bü!XM%¸Là²"D*m¸önâ8G\x0011~\x0008ØJp.Á\x0005°&×\x0002âd\x0000u\x001cûÍ'Ì
¨±B}¨ÞgG\x001cÛÑi ,°ªRÍ3\x0019ä\x000fk+»ÀvÚ\x0005 \x0010¢*S\x0005\x001c\x001d¬\x0012|²Ã)NK`+Q`ûD\x0001¸±¹6\x0006aMú
°Áp£¿;È-°Õµ½\x0017Ö³$°X\x0017Gã\x001a´+C	¦G-6ÌÀUÌVÌªÏ2\x0008<^"m9Òd\x0019DÖ	rª4b\x000e¯ÊÓÓÖO\x000cLÙê=ÿþæó}Ë;}¸XÉç²¶Eî<µDáhï|¸~dÓõùåÅÅé«Ëx×°Ã\x0010­ÜplgÓ:Âq\x000cÁbécÖ©h\x000b¬¬`eçÑF\x001c³V@Ë6¬P¦`ñzdtW\x0017®ªpU/®£r{\x0000÷i94Òò+Ã`þAhuu¸ºïpÅ\x001dµ9¢Vb.ÑàÞò]SQÚ\x0016\Sá>\\x0013lyfNS¹¸\x0016´q\x0010pÅ¤\x000ckÀu\x0015®ëÄ\x0005à²Y\x001bM \x0006«héêâ\x0012Ãà
7tâÂã\x0018µ¤\x0002/-dd\?iÍÇ5\x00143RÌÀFº\x000c¶@\x0000® q\x0016{\x0018kªf:_±ÅTe"-\x001b·ÎMÚ
óqm%Æl¯\x0018óªÒì>Òv
6SvfüøëêOÿAB,®RAÿþáÏÿþuÿ\x000b«ÔqÈÙf©\x0003%@´ÀÄ\x0017hi|uúÝéX\x0011½yú`xàý³!ÖùýÇ\x001fgÔÄàÈÂ\x0014ÝX?_f:³eãHZfÝ|	ç÷nJhû}]w\x000eæEu\x000b_ÜÿüËê/«½í6X¬ÛmÐ]Å)µHè\x0014Mté²ïþ]_\¾y{òúâd¢5aÝ\x0010ÖõÂÆ¼:ÛJ#c^M\x000e´·Òø½CÀ!lè\x0005Õ\x000bN%.¸ÊÅ[ÒÑ¬w\¹8UpÚ@;0\x0001õfG\x0003nLã/2nÌË\x0001×R\x0018xA\x0006\UáªÞÓ<\x0011
q\x0005á\x001ar\x0006\x001cÎ:\x000c®©pMïéº<\x0007\x0005pó\x001c³|º*ùÄT[[\x0013®¯p}'n^¸V
vµ,v®'\9Õ×Ø[½4ÙýÔ\x001cµNH\x0003\x0007\x001d<]"\x0017âdP«\x00017V¸±÷t}ÞÙ\x0007§«\x000cVIåÓ¥©[R\x001dH©J0¨^Á`pb3\x001dn ò\x001d	\x000e.³B\x001cFE¨J©^\x0006ê?ä»`ÁfUt¶ÆðáN\x0006	\x001ah+1¦zÅ±<+ÐJ®GÃUå¡M&½\x001ap+ý«z\x0015°µÇ>\x0017¥[£ób[xhY'õdR¹\x0001·\x000bªW.x\x001aÐ¸:ÕÀºáár:\x001c·Æ\x001dµZUWÏL÷>3LÏdT'©nCb?¡{ÕÕ+Ó¯Ì\x0008ÇÆ
\x0016{;¸<ôÎÉéRý¸Duïý÷!\x0010Åö~þðô{Úürôööû/ûim )\x000cJ\x0008OQ\x0002é)(ë¦g¸=¿ºþ;.|9z{öúôêòbÔ" ²î\x0004\x0005GëöñèÓÿüç=>®\x001eöº[Þ8EÕôð¼Ø;4Z³\x0008Sÿào½;zytöîÝÉÕ(7\x001b-eÝhÙ-°.&aGK\x0016:`óDQe'ÅoÍ½ãÕ\x0011´\x001bB»eÐ6OÎbº\x0019Á\x0006*:cRÃ5\x001ev\x0018rEÜÞçW(3hE\x0004v8IÏâmªì¯{àeÈÍ
ª\x001epGÒ\x0003wÍÜºå)ë²[UÜj	·\x0015¶\x001c¸ÑäÏCÇ=Y8\x0007ü0·[U§­\x0016v\x0001Ý¹LíÉÜ4>\x0016Y=mo¶\x001d·ª¥Zô.½u¹º\x0002,O\x001cª\x0003½ .\x001dL\x0004LGKÛÞå K^æjÑ
/Î¿\x0005V(&ð
Wö\x0010/SÅÍ¬JÜÈªà@àÕÏ·÷ww{ch\x0001ó*2·ójP9|ê4m3\x0014\x0016WÔN@ã@à7gçç)¶¸áT#²éFv\x0001mæ¬h¥ÇîXFjê´ \x000f^$ ×/²\x0005Ù	ÃÕÏZhLdaé£gw
ó\x0018SÂ¯\x0005YW\x0017Cw_\x000cÜãJUQHÒ3pøÔÔe>Ô½\x0018öøÆºÇ·\x0018ä\x001c-±\x0008Ø@MÄ\x001c{\x0003ãj²âm\x000eòÇ\x000fÂojÔ@½\x0003Óô\x0002Åûþòr'DN\x000eZøÂ*1@d{\x0002ÁMÌ~9\x0007«ôâäêÅhøãOÿx(9â­ÙÑßá
³½bL 9d\x0008ÏrzÍ{Zé`ÅXÄu8Tó;\X6j1[³ñªÀÚÚ¨r½}X=íOL\x0018ÐÄi6\x001a÷«\x001b½âÞcø/&k.Î®N®§,Ú
Ô¶ DNþY%­È`\x0011äÊü8\x0019SË\x0019*ÎÐÃ)#õkÉ¨5EÓDlå©>Þ¹ºúáuÇ\x000fÿ/âÔ\x0015§îàô`â÷©%½*@\x0018in6U¢3A]\x0005êþª\x0007jªdz\x001e\x0012
Íìd*x5¤°'VSCôòµ Õ\x0003Å½\x000c\x001a\x000cÿòÎR3!H)}\x0008ÐêÉ'ïå®!ìÌs|¢¥Ã|ºxq\x001f§\x001f.ÕÌÿP{ìoVw«¯\x000f«ß÷\x000eÏo	.+¸\x0004¹áQàÁ\\x0003&ì¤Á÷æäüäýÕÉß÷²\x000e¼]`­½Ý\x0006Ø5\x0013ÀJCY\x0014a½S\x000c\x001b¦¬ù°ªU°*iBZ\x0001&	Ö8|ýóaM\x0005kú`sZUêhpÔ\x000c5áà ÁÀÆ
6vÁbg®Í\x0003\x001a%ÎýÎ'ë5×-ÂqOÙÏ³a\x0007ù\x0013/6ò'5Øa.lÕ¥Ûp\x000f¬ÊsgÖ2SñJH\x0011¦\x0006%­iwÄb2ªõí;X\x001cëGS\x001eqb£\x0006{iå&C\x00023QuªûP±ÔÇ\x0010ª¥ká\x0002¥S5n4^Z_\x0000Ów\x0001pÌ¨¤SÕ¼\x0013\x00144,ÕÿééÊÕy¤¶Ö\x0005¶O\x0019`-]^4¢Ëø1adùùÇ¦Â7Ö7ÕöÝTóH¸f\x000f\x001c=\x001a¡¥ôRöpÊÍ<Ìyází«û\x000f·_öV\x0005ËÃ\x00044úÌ©H¥<\x0012ÛO¸MûêòùÙÅDç°Ü×Ë\x001c¯ïaÅr
Y<Öy\x0005\x0013ÜÍH¬vdºH\x0007ë`Ø+Åè{`A¡jõb'ª\x000c\x001e\x000brÌ
\x0018¼\x0001kERT¾\x0014kÀ<Z*^ÃäIGäTÏ±
ÖtÂê4@\x0017Y%-®@°°.¼\x0001yu÷zÒ\x0010\x000e"Þ½ÃÅõþsHÅÜweÑ>P÷]pÉÝó£wiQý~Z=¤ÕÝ´\x0011}ÕD+\x001c¥ï¤&\x0008NM¦	\x001apÍ\x0010w3h=\x0017×Jû0q§áb¥`h=dprdkt\x0017®\x001fâú¿è]X}ýlV\x001f¾\x001f©±ÅÚäÛ9³­×e"±\x001bg\x001d(\x00118s¡Ä½Nð_^\á çí0å\x0000.¯\x000eéÇ4cÌ<íD	l¼Ïhz¤Àv\x000eÚÇð5|	cçöbõðuQ\x0004®à\x0014\x0015þf\x0005ªAfJÎ®M½8¹z?Z\x000b1àÊÛM¹*\¡ÔÅK©=s-£Ê;N©àîç90pZt\x00161p½éX\x0015Ü~.¬Î¯å6ë\x000fäöÓÑ«\x0019{F@ðù|É$nËôÙkS&p¦ÔLL+º>\6ÂÃ\x0011*ª
Ìd4JÐ+\x00055bö:/q%È059c.¤¬ e\x0007$Kg,½£\x0002\x0016ZÞ
:|"\x0003:°ú¥eûO
Zf­JÜqíPðûð\x0013].s\x0019]ÅèÚ\x0019uàB}ì5æ­ÒÒÐ@*?Qq0QW×Q·_Gç$\x000fÄl8%f-&¬î¢n¿\x0018ÜÖ4BQ\x001b¾^ij¢|q.du\x001duûuÄ\x001ato\x0010%X\x0010\x0019Rù ç^H\x001f6#Ç!íf¾úzoV¿ß|MÞíý¯«\x0019)M%¬TÎ,c¤6\x0014QON\x0018,quyýþ\x0014qßüýô}rt//ÞLZaÄ>wä<,QrTj
\x0011©R
Kf¶\x000f{\x0002~W4!ÛÜ.;vci­ðQó±¯\x0007o\x001b?Ò´ÛM^Ý\x0017¹ìÂH\x0013C.úÂÀ8ÅAàò»\x0011;iÁ\x0019¤Ä\x0001\x001eSâ\x000bà\x0005z\x0018Eµçb\x0004\x0011Bìa$]ÒÁþé\x0007ñÈku1ÄÕÝ\x000fÀ?c\x001b¹Xww)¸Ü`-@Ûà¦j!Þ¿\x0006ð÷c¶òýÇ\x001fº\x000bd\x001f$« à}{ÿe¿õ§½T¦!¸ï\x0016ÑL`2;2T¯}{y1jû}}úéæé§1\x0014Ü3.rÞ\x0006oJ4$ZÎ´ÍÍs\x001f\x0014ØÓëw©¼yo{uû\>#à§ä9ö8?/á\x0005ö\x001a\x0019öØ·½º}>\x001e\x0016\x0016Ò¾(ò>\½¤yÌ~\x0018)nj\x0005ÜÚÔÙD\x0018$õ\x001aÐW©\x0001_E©9M\x0003\x0017\x0002ªýèó\x0001A´SÃóy6\x0000J®k~ÏâÝYpKªÍZ­WÐ«òDG	¿q¥Nzd\r3!üÀ?}R£K\x0008\x0005íÐÀ[Èk"Á\x0017®³C8¶Å}¾\x0001ËCRçOsÈ\x0013¡¡EóN\x0011ýÝL¸ÙýÝv\x0006\x0017OäVª=t ô,i¤\x001a\x0019VÐL\x0008¯XwjÜXL5Á&;éx{:ì\x0001D5N\x0005ÓÝ\x000f\x0005+ÅÐ:Ì\x0003ç#ô|N-Ö\x001aîî~(ýà\x000cC\x001ehêÄñS¶#YÔVB´çL÷5Ä _(ß:+¼(l!Ô\x0013K"ç\x0012Â\x00154ý×0âº,°-\x001a\x000fé\x000cáÑ°À½\x0002Ûß~~ü­ºØ¦u·Ú Ñ\x0011×tå5\x0017Áõó .-¯1«¿}Yç'\x0017ãs\x0012ÒG5ÏÉlÌsz¸ÿ4+ke	
ÿa¤\x0005}`íRcw¸ß{¢¢ÿêòåÙef#Ê\x0006$\x001bm6ói½&'\x0017þCKEæBqM,ÐN\x0016t\x0015Ú\x001d^\x0016¡Ê
Uö¡J\ËG¨8ö5\x0017I°¦b>/&ç}ÎD5\x0015ªé½\x0003>\x001b:\x001a÷ß)OW\x0006hz/\x000et\x0005l\x0005k;Ï\x0015\x0017ÉÙL¥1t®Z#¼\x001bÛuÚCë*Z÷×>Z_ÁúNØ<>\x0015i±ë"\x0002Jò®A
«*Q zEõ\x00142ÒZp\x000c\x001em Ú©

°0PÂ@áz¶dhPõ\x0018WLÖÓB\x001e\x000cW\x001cäÒ\x000e÷VõÞ\x0003OS2´2Up\x0012ÑÑÑÉòÞù´ôR½ÒË\x0005Ê`i\\x0017Añn¥Xy3={l6m%\x0010T¯@øWm¨hC'-Ø.LehôÈx\x00020e'ûýf)1]]\x0003Ý}
4õ°jyè\x001aH¾\x0005~rdõìs5ð2½ÂËÐ4\x0007Y\x001cD¯â`á%°a3µ\x00196wâ¾~X}ùô\x001a¦VOöÛ±¸Þ$[¸>\x000cÇe\x001d\x001b¢Wt\x0017ÀÍÜ\x0018òúêäâå»Ô9urýrrµEØL(Íµ³íðw#:O['\x0001ëë}ÚÚ\x0000¿ãBÛÍ\x0004
;h[Éq\x0017­ÊÇîÌû¾Ü²ST:=VðqÙ±+[à\x001d5\x0002|Ô\x000co§ª®ÛáUuáÕÂ\x000b¯t.ÆÇB¨\x0000OM^éYÍð²ËàqG¾ðißr\x000ey\x0008\x0016`êMî}kf¯®¼Zvå­T\x0018\x0001É\x0007_\x001cy°¡ÈÄWzd®I\x0007¼ùaõÃ/cUP/îo¿|ã\x0008\x001aÓjU4ßÓ\x001cëDjÄo_ªg.Ï.^Æ\x001b\x0006d\x001b9ÙdXb\x0019JõÎRÒÌP¯ãH
i\x0013ÙV÷í\4\x0005¿i^þ¯æ3Ái&\x001b©éA\x0006GÛ±ÖÏ(\x0008, »zÊIÆû§»Û½)10\x0016#	KìÇ£Ê{£Êð82éåê:'\x0016/¯ÏÏ.&\x001e\x000b\x0011ª!¡j&4ÐFO½Õ8ç^ÄBËFB=$ÔÍ ö©ØÈ\x0006Ç¤\x0011<}\x0013~ì¥f\x0008hþGh¶P9ÖG\x001aÉ"àÕò/\x001f·­­FB7$tí\x000fÅqî\x0018»\x0017#×B\x0004^\x0018éOo$ôCBßL(xÁ°\x0004sÚ\x0013\x000ee\x0008r\x0018\x0012öâòdgü\x0015\x000e£È\x000f¥Lhò#YÚFÂ8$­:r·\x0004¥BCvv%ÇhF\x0012Ým\x0003/%äÔÖ§¢¸pÐjÉUÒð3á}f¤´¶\x0011±Ö)ÍJE;S&q	Þ\x0003\x0007ÿ¹.yÐÅòFVJE¶k\x0015\x001a¹ó|Isd\x001e\x0017\x00053âÈÜÙFÂJfËf¡F:\x0013!hf\x00128ZñZ".F¬¶lÚ8l\x0008Áè¢\x0012V°[9\x0013ª\x001fb%´e³ÔÆ&=º8RVf£¥/8²à­\x0011±Ú²Ylÿ+\x001eK%\x0014e»TüßDt8Ïr¸	ÞÙ¼	êånÎW¿<<ÍªñÃiÒÏò&\x001cA£ºA«Ú²\x000fi$ìLerØãòöêzº²Pmj»P]*\x001dHû»¬çFRa({k\x001fé{ì`õ5«ï;V«UÛ\x001cM\x0002VG\x0015}`þÊGÔÌ:f ë d²Õ\x0006EÛ\x0002\\x0002ÚÜÕ¼ÜUD¾:Xëëªº®«Ã¥ÄX-\x0001;Eã¹uÌØhg­ï«êº¯\x0018\x0003¹8aDVs´kL\x0007¡GËvÖú¾ª®ûêæÎç\x00119O\x0005÷Ô£=VÉÞNªë\x001b »n@Àåbù¶º\x0018s9\x0016\x000eF¤Â^mÇÊ\x0016;XuÍª»XÁµÍ»\x001c\x0003¶ëge\x001f\x001d?,»»|ºÔÔ§júÞU09±MúÔ«\x0007??U2bjú\x0010ÏÊÔjº\x000e\x0015{CRµLFÕf4PÜ
Y\x000fq\x0001L-\x0002L§\x0008°¹àXI\Y\x0016WÊ\x0004;XcÍ\x001a»Ô\x00129¦Ã\x000fh4­ç¦yüÁÙ×jke»4\x0016&£bß³¢À¡
°²Fê	;Xëe»^Åþ|\x0005Ð(ÈJÀD2øµÄåm\x0007@55ªé:V,HÊ°

å\x0011S8ý\x0010¬õË²]/Ëê}\x0012éX­æ"\x001fËÑk-âÈÒ\x0006V)7÷à \x001eW%-æ?0Xr£`ZâìøLª<-íÃ¾øÉÄâþQ
\x001bËet#\x0019:\x0017\x0015ç	äB	lø¡À»vÀµnªdf6ªCÔ4ÖÌ¡\x0012¦4WèPîªôÊó`8ôº\x0016WjE\x000fj\x0000\x0017KÑX\x0011¼\x0000¹G\x001fþó\x001c¨
bÌbi@\x0005È¬MY·w«éQÝýÏþ×é\x000fw·3D.ÍÞNkÚÖ\x0003.à¦\x00105²UðíùÉü¬N_½,;ØÌoØßèbEKúkÊ\x0006\x0011ÜuG¡Q%Gz:XõU÷«£cU\
Ç\x001aÊ±\x001e\x0004Õ\x000cQM'ª¼\x0001É	GSp)\x0013¼ÕyÕj¨¶\x0013UùîNû\x0013o«\x001eÙ5ÛÁê¬¾UÒA`5¦tßFËí`z$åÕÁ\x001a¬±÷\#\x0006HçBIÜ\x0008nÊQccF·YwÀl\x0006Ìm\x000ewÀû¯\x0013´lX\x0018Ía65VrÔ~ª²º­²÷ºbõ,\x001f«ç\x0000ºAD\x001d\x0019Û\x0001[]WÙ{_\x001d×C¥;àÙ\x0018ä±\x001fp\x0007\x000e\x0002[ÝWÙ{aàÕWÎi\x001a$ç\¨²#¥ôí°ªº³ª÷Î÷BÙ(øCË\x001dÒ~a5#ë\x0011;`+½¥z\x0015\x0017î6ElYÊ?\x0006\x001eá¬Æ6­tÀV\x000fLõ>°P\x001aÖ\x000e%i\x001f¸ÏLíÇî±^¾ÿpûX[0ø\x000f½F Ë\x0000KÈá®.5\x0016#+i¥Ü0\x000cá\x001f\x0006å.oï\x0001\x0007ÿòíýÓÃ~\x000b\x001dXL\x0018\x001eé«\x0004ßZåw¦Êß^Â?â_¾½¼¾²¹7CäUÝ¼ªÈ/lU \x0001©²\x0004\x0019·EB\x001f¯\x001eòê^^%¹¿ÏiÉÓD¬
¬ÉÔîQ#¯\x0019òîóÅÁ2H\\x000f¨\x0012F^;äµ½¼Ø4É¼¼\x0018CXÇrLlwïÃuC\×ë\I¶c\x0019i4_2Ùc\x000búpý\x0010×÷.Z\x000bì4ÀÅ éäÅ\x0010\x0007â\x0003á!nè=]ïi¾Pº>ãz\x0015\x000bïHX\x001fo\x001còÆ^^ *>Çé<jH¨¢&\x000et\x001dd­,zµó÷O:Y¤¯W¥¯Ø]#9\x0013\x0018\x000cP\x0002Ø8\x001bKÎ>íOÕc\x0002Fæq@OÌç\x0003îl$\x0013ÇÚ¸g	ÞõËÉl=qê!§îáÄ\x000fy(VTµO<\x000e\x0003þ2¹íe.¦\x001bbº.LAS\x000c\x0005Vïæ9ê\x001a\x00050sîÙq·SoF»ôÚ¨É»~\}X}\x001574_\x0004|\x0019§d.Ýàq,ëy}Ê{¾9y~r1\x0019ïÖÁ.½¶g\x001aQÂÈ1¿'tØR/«äÈ\x001cå\x001eV=dÕÇ\x001a8z`£Aï!kÙ=\x001bGfàõ°!«é<×P¶ve£F(±®\x001dFL#ª\x001d¢Ú>TMù¹¼xÖ\x0012ª.óÆÄT\x000f«\x001b²º>V¸£¼.\x0012G÷\x0004:Öhùr\x0010T?Dõ}¨>\x001eÛl\x0017¢¯«iàñ.bÐ\x001a¨¡óaÉ2ç%\x0004\x000exÃsã\x0015F\x0002\x0007=¬qÈ\x001aûXçJ\x0018Pæá\x001eðØFæ0t°\x000eJõ 4¸õ`íú`AÐ/3Ø9<2&©\x0007¶VZZ\x000b+öh,ÕÜ·\x0003Z\x001cqávÕ[7ÂVjKvê-½®Èõ&·&¡U\x0014\x000eòºd¥
d§.Ðëm±`ÃÐ\x001200cÕ©\x001d¥ö°2Úà_u\x000b*m ;ÕQÇÔÃ`
\x0007éÓvB\x001a\x000c4²³¨µR\x0007²S\x001fü«\x000e¶R\x0008²S#`×)\x000fÒ´[\x0001·Aq_ÃH\x0012¼µR\x0008²O#80aiÈ%öcðÂ\x001aÍ>¬P»\x0002Fm°ªÒ\x0008ªS#ø²Í\x001d­\x0002Ö\x0008!®­¬ª4êÓ\x0008\x000eXJ(èXÊ¡æ­#Ã\x0002z`kG¦S#ÀûÒ¹ÂÀÿEy%ÇCîÐ#Ãê:`m\x0005kû`½Òe\x0002.fmr\x0014#à\x0002[ad^XX%\x00144'\x0014:MÔ%%\x0013\x001f
ÕñÊs%Gò5MÈjÓÿVÃ¤\x0002n\x0000Ô\x0019\x00171g§)Y\x0013x/0ÇÅ)¿ËèºNÛ!\x0000trõ¢Út¾Õ00ÓJÏ\x0017Öá&`Þ´¶:RfÒÎ©ºÓÅ¼f\x0007lªÒ°j#·2êïª	SV75ýôå¦¶ýú»\x0006±öïià\x0000·òcÅÑ³q¥ØL}aèíÿü2c½Ñ\x0018gÔ\x000be8îZj÷\x0014»(OÞ^Lî°gD5DTÍ8Ú\x0001\x0017!òT\x001bî(ÃôçRD=DÔí§(cÞªÊ4²ÈWÁrlH#¢\x0019"S´Ç´ã\x0004gq[¹Äê>MYXFh¶ã\x0010
{RhÐ\Ãa\x0011q·'5Ð\x000f	};¡àiÈ¸\x00042®\x0010îê¥O\x0018±0MØËò\x0014\x000f´\x0007;j·½<\x0013q°NTñ¹X'FEâ¢?ªÁ
Tm}ô;í#bÜQ
 6\x0013<¢AÌ*eîq+Brì -¾²z*²ý­fØ\x0018çéãsfhwÇôæ"VoE¶?\x0016Ðo4÷Hb ÍûSóÑbl1b#cõZdûsI\x0003)ÉcSieLfÅR_zªz-ªãµ(|\x0013ùµ¨°®ª¤øõ~d|æ¬×²fzhæ¾ûºú4cõ\x0007ý7d08üç¤V´\x0019[BwïO^Nõ'læ¤\x001e·3ùâ:k\x000f²\x001fz]A=¶ò´O\x000fùt+¼\x0010-
Å5\x001b\x000båpeóB<3Ä3­xÁby0¾©qVÛRÒëÆ\x001aøÜÏ5ó	\x001c\x000b®Ôeºa\x0019£w]7ý4Â-´²yÇýñèdSgæfî±ÝM'7ÐÃÃ¼À_\x0006¯z·²ùázM¦\x0007ýÆ#\x001axQ­ÓjWæz6_õ0dóË0V\x0014Ë\x0008Ãòª)+&5½5ñÅ/6òá\x001cãôSÚ\x0006\x001eÃ¡JÒ/}?ðäÓPÖP­jCmêó<x½\x0011Zºã\x001b©fn:>í+±ìÿzÕï«ßÿu@[ýÄö/ô\x0013ÞÙ\x0008|9µµ\x000fùÛ§Û½häâox°FPÍ/î( ±\x0000ieàîRó£o¯¯Îf°º!«ëcU&ÛüÈ*©¹B\x0005E¶\x000c°Tõ°!kèbE\x0017*XbU¹\x000b|\x0016Z\x0007ª}Zµ\x001cu\x001bwjc£Â|VO{G5_Så\x001dÉI8ÔÉ©ä³IU}Y»n+Øú
ë\x000cÒ´\x0005p\x000brIII!Em¥Ø³^z&¬©`7·aÏÅqsùia­¤ãíÈa'g%7ÀVOKu½­\x0004k\x001dÍ±ðÇQ1,½-«GºB;`uuau×µ^'`Á\x0000ÎW\x0016çCðÁNUIÎG\x0015ªìB
^ó%°RS(\x0005þcò°µ\x0011\x0013\x001bm[`«ç¥;\x00177àà\x0015Z@\x0004\x0007«ik¬[rçe«K`û.\x0001®ó±</n¬,ú\x0015Ëf\x000fr
l%\x000bl,0¸Hä\x0011\x0011^°5Z\x0006ñj\x001b\x000f£\x000el¥¹lê² Tø`½ð¸ï)±*gaC<ÈuÕu]WÖÄ xH\x00040RHZàyVP\x001c)ï­në¼\x0005Þä<#Â*j¨\x0001X\x0016\x0006ö@ºÖU×Àu]\x0003\x0013qk-'¢\x0012£Ó\x0007j3â¯\x0011ÿÌôúÏâàð½´	§{`Ó&º<4L00#m·\x0014#Lÿxôú\x0014çï\x001dÖU\x0015Zo£µÚ\x001fçùFØ³D\x0005H¸Þhí\x0019Ó\x000bæÖf
_=«÷ÖÀ?kO\x0005h[c\x000bÜ0çp(A]ÂVÉÔa±ÿÅÅ¾¥\x001aÞR]\x001eóY\x0003NN¬8.4Xà`±Ò#ñÄ\x001eX?õ}°.®\x0014xm¤\x0014 t¾#Ùü6ÔPg%q\x001fÝ\x0005ó\x0017ëìrÖy\x000b\x000c.B/ÙI«ö¨0Þ¬·\x000fXVÀ²Ø(¨F_°^\x000fÍ)i5¹&®\x0001xà-\x0000ð·Ð°]ÑPÄ m¨y]o,#D¤\x001béªè#ö\x0015±ï&ÖÃÏg
âÆÊ²ÙL]á\x0016àX\x0001Çnàu3¶\x0006é¼Ï7x®zRK<pt09¹iã6,´T¥'\x0004 ï¦åî|é÷\x0005=f\x0013ËxÓßiÚUëåúi\x0005§?ãJRè~I!Tyx Û\x000cÝ
[×õ\x0001WïN÷¿;8b^©3ô³uÀ¸ºø0ÄÕÃÓý\x000f\x000fS·<=MäßXS=2z°\x000bØT·Øôßb>FwÂØcÞÅ[´Ç>Ox6ouM¿~EýXÎ\x001cÓhãËÞÛÉ\x000e×\x0006`[\x001d°í?`Á&X?º"%\x0016«g³ÙgÄ\x0001ôâáþö·\x0019°¡T²\x001a¹ÞanÊ\x0018ªIc
Ën¯.Ïþ¶Õ
Y7Cy3Y×\x0018I6æ1d{ãx3AÃ\x0010tÓÃ	èÊÜ@WCNYM¨ÃQD\x001e2°ÕïV_>þ¸úº\x0017U
Á´"//k¤iYÞÈÉãóó\x0017ß¼ßª¨ª\x0013ÕÓ¼,3©ix.\x000e|'V1²Z©Õ\x000cYM\x001f«¤x>²ª2ï;q|Gv\x0008V7du¬\x0012Mrf¥JÔxÁ¬S:w>k\x0018²>Ö ×¬\x0000G»%10D÷uÒYÍ:H?I±¹Ð{.,îÅ
®ÀR\x001f©¤¬\x001e²NÆ\x0017ö³°!\x0006L¨ÅÀËÛÏï\x001fö¢:\zo¨º\x0014§\x0012ç9\x0012¶¸;¸gS¨/¯Î^½º¼ª¨ª\x000fU\x001aî\x00121ð×\ï¬¥0¥ch¤®½U\x000fYu'+¯I¸&Ñ×²\x000cy\x0004\x0015~sµCVÛÇ
\x0000Mó2ÂÒè\x0003-¢Õå\x000eLY\x0002³Y\x0007=nfcå|X\x0005§)d¤r8\x000c§MÌ\x001eë­/lßàéR) Ó\x0006²\x0010Ö<%G
&z`M\x0005kþÒ°¦Z¦Ol	¬2O\x0002\x0016+hmÎbÅ`fuc+ÐÚYå\x0015]°\x0016KåâsåÀH\x0002æ\x001dÀê¢ÕJ/\x0015\ÊoÆ=
Ù³Y=>Þ¤¹ÏÏ\x001fîá¯{\x0007?;\«Ì\P¤º´³4³\x0005×!oÛ/goÞ¼{w\x0006??¿º¿NM~&X35]° ¥$\x0015³*P»¤\x0012,{xÇ4B\x001bl\x001b'\x001bäP}ñj¥D}òðáa?´ÕØ²³h(äqÕàSbG\x0015àòmà=KþäêùÕ\x000cøA\x0014\x000ccÜr!½Ç¹ªBàÎ-á5\x0017×)ùÛFï6ÇO¸Z¿Àoï¿Üïí¤1×'³£\x0004ä.\x001aOúÍ\x000632¤pýü¾½¼¸Ükµ9\x001fÁ\x0010ÿLÌJ]\x0001¸Ë;Sr8É\x00065òð\x001a(ãÅ\x0008/»:Ëóû?ÎøùNùóÜtÆ5ÆR¹càíNzãð÷©\x001f=nZáqÓ
¿¸¿}¸ùzó0#{ë\x000c\x001ccëT>SP\x000f\\x0010íÌ\x0014ìÅåÙÕéûÓ«ÉLÜ¼¥qó6\x0001«¼zÅb\x0010\x001c­²\x000c\x001c¹ø}l=j#°ó\x001bÁ|\x000cýÔ;\x0002Îoÿü¿¿Î\x0010\x0006X³F#	u\x0002Û2ÐÑ¶¸\x0007Ê\x000b
ÎÏN¿Û#\x00042­«h]'m\x0007®¯¦ö%ô\x001f²_\x0016Êû6ÐúÖ÷Ò
­ßÜÆ+±J!ÓÚÉl_\x0003m¨hC\x001fm\x0014Ü¶\x0001¾\x0019O*³¥\x0012`ÆÓhÝtxlíð¼xzøóÿÙoé\x0010si(\x00161Ë|¬®,b²"áÅõÕ´c¾±\x0005!]\x000fdy\x0012\x0015î`¦Î\x0014KÖjl K3f\x0018bÞ³äUQ\x0006£õt|n²bm\x001f¦OÓ\x001d\x0007ãF¼®7¯\x001c½Y=|1Þ1JN\x0002n6T\x0018H²4-¢GFÄ\x000bkÎ7'Wï'Ç;zµa\x0003Àµ¯m7«»\x001fî¾~Ó¢("#|<rFQä\x0000ë¦.èó××ïßOi\x0000Ú½3\x0008"Û
õüþö1»öã¯èsÉ\x0007Ôt¤<\x0019VØ)\x0015pôüòì]xMT*ÙÍî(»i\x0014Ü­¾»±É<·\x0001q±á6k,\x001d¸\x0014ÐÄ0i\x000c\x001c}w6½Il®\x000b\x0012õº §£·p°GpÜúêi\x0016Lg{\x001bjë¼ÅEÏY;pÍ&ªm¯ÞÂÉ\x001e½<:=¹º½BËo\x0008­üÊnöÊ\x0003áù<EÕä{\x000b>.Õ0ãÞ©0R~c§ï}\}Z=~\x0005cÿ²Á9°
½Ý¸\x0006óAµÊõÖp?A6äp2\x0008\x0007º\x0006Ø\x00016ýÊæÂª
VõÁâ\x0008ÅÌ*4¹ä&Jªð°2xëa5\x0015«éc\x0015ß\x0017Vç\x0016µ\x0017#ãdµÚ|V[±Ú.Öà,µÃu%k\x001bX5
üLq°%°\x001fôUàó9¶àcà3É×on\x001f\x001fg´û 4v1å¼½À9\x000bé#·]Ié¶E@«ß½{·î\x0016Oh®BshÞ*Êw\x001a!£ÏdGMÅ8èØO¦*õô\x001c\x001f\x0011ª§&¥$ód\x0014Ü©Wf\x0000ÐP\x000fôaw`eE´\x0013j\x001d\x000fÌP¢Jâ$¦¼_Ù:ÅÃFD ØÑn$ç:KÕ\ª\x000b¬8A{ÁØ¤µ [²×isÛ1y\¶æ²\
´Äå4Ï¶\x0014SF5ÿÒ»ï\x0005ÚÏá\x001f°@ûüöæéèåí×æ\x0012m\x0019³TõìY\x0008Þ<¨\x001fñyÀÑ¹>zyö¾.{ÞÍº~\x0007Èï \x0013\x0016\x001eC.$Î%Úw_hÖÆd¦çÓJW\x0005JÃ?` ´À¾YÝ>Þ9º¸yúuF¥¾\x000c¹Õ\x0019XÁ¨4¹a\x0003?ªÔ7j$\x000eRXß½»¼8º8½þîtµôì$VìÙé\x0005E\x0017ðnæ\x001e#lqO\x0011±\x0010×-F\x0013ç:ÕT¬¦û`±kÇ~¼ò\x0002»vJ¿Æ¶Ækf
\x0015kè>WEcxq}v¤Þ-ÉÛ\x001aYðÞêªëêúï«WÜÇë=çÎ$øoÜslÅ¶\x0004m­îë¿\x0003L4µ&r\x0003,åÑµÓSbk.lu	\ï%\x0000X\x0007°\x0002l^6`]àk F<÷FØõ÷\x0004v¼÷Ñ\x0006pØE(f$c£¼<=ì¡l¦Õ5­î¦*×Ô`Ó©,´Þ0­ë~böû_Âo\x001fþL:¡Ò\x0004w7G¯o?Ü?=Ü|ÅÀ¢ö\x0019Ò\x0012äË?ÿùxûðç?áÿkg\x001dZ¿iÜO¸P\x0006N\x0012JàX\x0013\x0004KÊ\x000cÖû¾<}wvuºf<?}wôúìùåõÕéû]±Å
\x0015ÎR÷£u*\x0011UcI]BU¹è\x001aQ\x0007\x0015«Qá[ÛnÔ(B»¡z{ì\x0013h9l\x000fÖV\x0018\x0014Ô-\x0006\x0005MíûAÁj	H2ú¼Ú\x0017I\x0007¦ébRøÒ±\x0014uÊ¤.EÀ\x0013*MõB\x0013v0\x0003o)*F\x0012d÷£ò\x0002Ó\x001fôûcx9\x001fk´n*\x000e<>\x001c+|miúYÎ^\x0013²*pë\x0012*EÔAïîò»úý
oëªÿº\x001atóu5ü°¼+ïJ/dµOÞýã\x000fÊåb\x0006÷\x001cË%nV÷\x0003xì3\x0014w£\x0007%ÓJÄ$¤¬á·¯\x0006-YÌ¥\x0012§'@ö\x001aöYp$ó[á°Ðf8V%¸\x0010Ê½<\x0008\x001c\FÓ\x0001çU¶\x0001NË\x0002G¦\x0008À÷f¸ò²[épXZ¦3i.,Â¹òLtô\x00078¹ò[áÈ.RÄºã|ç\x001cmºÅ\x0018q8\x0004\x001cÈ\x0001üÓ\x000c\x0007Fp$a!Ëüh½)¯V
º»úéà\x001bâV:\x000f¾º§£Si'M:;\x0011N\x0011µ2NýÇ½^é¡0)RouôÝêînµÏ\x0006aòÔ´Æ¬ètñ\x000e$O3vû·-2ïäè»óóY¶Ù\Dl($
\x0012pC¥Lv\x0002§R\x0011¢5\x0013¹\x0005qÓ&}8ôÁdDnoz!ÊÉ<\x0011£ zBËµ Â\x0011ú\x0010Qüñ)*þ¡Ðå\x0014åaN\x0011S:Rt2Æ¼Z$\x0018¥¡cTt.\x001eè\x0018·í¯6F\x0019¥ \x0007]1Nø3-[f×|ÄH;ßS\x001fq¶bÀDèÅ¡\x0010Yb·¿ia<N\x001bI\x000f&Zþ¥±É\x001eL<Ômd¹ÝóK\ÑGÎQøpðGfk¨ÌÖ\x0006JyÌÏ:bU$Ã\x0001ú\x0012ÈÏ?ß|¹Qc*æÕê÷}p\x0011+Ñ±V\x0016\x0017í\x0008¥ÓX\x001c¡MvT¬2b[53Ü«¿ïÊÓW\\x001báY\è5C)èV°ìîË7\x0017kCÝÍ;.\x001bp°*raíTù¸<sé w»ËsÁÈzn\x0003ó©0 WÀªáÄEóáá¼&¼ø¹X\x001bºwæyÅ´_;W*\x0011Êçe\x0014_\x000e\x0006ÏÇµyçÒ¦\x0011<0m±ø\x000fÁ,-\x001c\x0003Ój÷«\x000b¶\x0011ùCº\x0014C0\x001cBK¿$5\x000báÍ?À
Û°Qf¡f\x0007*Ù\x0018l\x0001*_Þ#åÇµ\x0011\x001dE\x0015pQ7ýàm °.gÈá¸¤Ú\x001d\x0011	¶e/Í sØá
¹ñÈL\x0011aÁ8ºúNNæ¡Èoù\x0018ò\x000fô&#®XJ¿%ÎÄÏo2.?±MëmÞL'æÓªØtb!\x000f\x0013³\x0013áÝ¹dðÝd³ØÇ\x0013£G	\x0007\x0000éÈX-~[Æä¼\x0013s>\x0015\x0005ã9É'\x0016æ\x0013\x001b¶î÷Áÿ\x0005Ù,ø#ÈWåò\x0019VZ>1~ÚÊåg¶iÝÎ#Ã£¤*-À<h'¯\x0007\x0010\x0018 õe³äÇ´¡/wLð\x001dËám¼d\x0013\x0006÷\°M[{Þ-Ó2\x0015ÌÒé,ü\x0007<1\x0010²YøãÅ@Æ«Ã\x0001ctdÅx]þ0G"Ö3õ¸HMQÈa¥@\x0016çSSµþ\x000fññæ÷Qé¡ô\x0017\x000f7O¹³o¿ïd(i"\x0019þ
Û(ìåÄt6åÅÕéõîÖ¾sSæ¶p\x0006\x001c´$³\x0001õ¹Ù×\x00027Q8ókàÜò[Î3è\x00125\x0004\x001e(yIu=éæµqnyÌ-ZäÁU\x0018îtdÉ)k\x0014uNøÍçÄBL%z9ÌK6S`ä=q
Ã¿»Þnà®6óg=÷3¾ÓýäðñplûBN\x0010j3:\x0013Ó\x0002&ßO\x0002Ó;ÑòïF£-áüÑ~r\x0018ë\x001e´>®~Ø+0-FCr­EÌ£\x000cñ e\x0010Y`bgô\x0016à°oàõn9@ËN+1¤gD\x000cJ$´y\x0013 i¿eÊ·£eÿº\x0015Mû4³\x0003ÑÀ\x0002\x0014YKc\x0019M.'cÿ§\x0011
ÞÆ±R\x0019M\x0019T&HÒXáÝ²\x001bÚÙH\x00166²\x0019¸a&\x001f[À.\x0015_È³\x0018Íè-­2í\x001fÿ~÷Û}\x001c\x000bÈ}w{wwóéþéçß÷ñ\x0005Lsû\x001cg2hr%©2=Éx\x0010ÁîV&ß¾¼¼~ó÷9\x001bÁ¹\x0006FìM*3ê´\x0012\x0019á¼"áÜnÍÜ\x0006¹\x0011ªk9H§ËAbµ³Í\x0007é"ûr8i\x0019äFØ®\x0005R¥tO4\x0001$HIX	?¡Û 7xMWÒQ<CáàV\x0019è$\x0005ù'ÒLøm\x001b\x0001½&È\x0014aO'é5ö¦gHv¥Ø\x001bÁ½¦;\x000bð$A³\x0008Eüp¤ÛÖt\x001b¾¦\x0014\x0018\x0000£\x000bGf	¤ø$U<ÔInÄýNÒã¢\x0004iý1\x001d¤Ï¥iÌøn\x001f¦q+ Õtô üÜ\x0012Ë¬éá0¥ÛÖ5½Â\x001c}U5ôU[8¥-¢ÒxÌ8W,Â"Î»÷¿|\x001e-\x0000;öÝýÓ/7\x000f÷_ö[²^'
EMñK¥¼
lòèé"°w×oO¯./vÛ²\x0003ÔÚÚù¨8®, ¼\x00152ÈÆå7Ô«6ÆTûPcjQJ¨T±¨\x0013fÔ
\x0001ß
BF\x0005i\x000e¨ì'\x0018"uÓ~L\x0013èHim\x0003¨O-{\x0019TÆ\x0004Ò¼©\x0014Iÿ_êÞd9¯#I\x0017|\x0015,û.\x0012\x0016ó`ZA\x0014D¡\x000c\x0004 A»U\x001bÙ/
)!\x0013\x0002 ¡\x001cVõ\x0006½®íÝtg¿Þ¤¤Ã#Ü\x0003\x0011ÿ\x0013Ãá5»V¦J\x0014Äd}\x001e'Âgÿ|¡·¶\x000bêvßI\x001fT\x0017	ªd¨£Â×ÏÁã+ê6à\x001e¨\x000e%\x001e"búüÚôå|P\x000fÒ´d\x001fT\x0018­Òé\x0002\x0004Ï\x0003\x001a/c\x0004ÄBe^íi¶\x001cº7ÙÒ\x0003Õ$ÁµK9!î½% Ú¼\x000b\\x0006zûYº\x001f:¤üßl\x001ea ¸¡ÓÌ{jÖ3©«0vyjW×j!Ëöæä
FîQý\x001d@%¶¦\x0008cs\x0002\x0007}8ýÛsÏLE;Nç5ÂÔÙpÖjÂùR'R'Î­\x0000©\x000f'$\x0013°ïÛG]\x0015JKË~aô£\x0007è\x001eKÚ\x000eÔ2ê¦7@¹ò\x000eùýÂò\x0015î1O\x001d'jhîGÃ«2x¢*¨YïîÑøí@¥HCÀ\x0001¨ÕÇxEó|
®ÉZ8÷VT2Aíh@+\x0007³±\x0004`¤£\x0016ñõNtï|J;Ò`îEJZ+\x001f\x0007*"RghF!ÖBVBº¯úÓ4\x0011r¤ÆöØ\x001f\x001bJB*Ý\x000b
jMH~ýóÆ)äj\x000c
\x0015Òó\x001a²ë1O>©Òê8%Æ±¨Ì¹y9"9¿|ýBf½@\x0018ü\x0005±íåµ"Ôä6ÅR@:HtE8w\x000b\x001f¼\x0015!²rû\x00055"Æ¢ähDM\x001dUB\x0007×ä¥nÎ\x001eáÝÈí·ÓQ9G~²æ&MËq\x000fÝ	"!Dî\x0018\x000c¥Ü6­ÇÈ1OÇáV
t:\x0005\x0016¹Pk\x001dc°rÛN6bt\x0012ÓïÜ°çOmè½\x0008ÿÒLC\x000fÆ \x001cä¶lÄ\x0008u\x00010\x001aS+\x0001#D\*·Ò9\x0006Ë(·­c#Æà
¹\x0014`À\x0018\x000bêqf=ÞÇ`'_0[1ª\x0010Y¨íè¢\x0011£ÄCtÅ!E@\x0012õ´{FÚ\x0001Úüfö6?¿y¸ÿ|÷ôC¤®{9í¥%èL`s¶öIûB[ãË÷ç×_\x001fä­«àmùèíð\x000c48b¶#ø\x0017ÉCo\x001b!ú\x0017Å]\x0010·Üóv6Øh\x0011¹Tcá¹Ðçä\x000b%ð.[y£VÁô\x001cü±ßpØáBÃ\Ðë@Üòt;NQ§ùBè,d¸à\x0014ÃcÆ\x000f\x001d.êaÛÒ\x0003qÇ!kÇè`à"öÎ\x0005aÙ\x0014X~1Kèù9ÃvÌüSzHóèêáã¢hÃ\x000f£íàÜà¸µö8\x000cÌ¾ùÇ£«ËC¤%\x0016èn\x001a±\x0018.pò\x001fx±SUT*¤\x000cwí\x001bbm½«ÖcaÇ2CI7JjÇ=AÙÓQ dÆµ-({UÓÑ\x001bì@Y\x0004\x0003[ç|òä¡S!¥n¤Ä}»Ê;±Û\x000e\x0010\x00176AÛÉÁ³)\x0000aº¦\x001d\x0010w\x0010õF@Á9VihV2Çã8\x0003:¿\x001dfÑ+T>!¥E\x0006´{uºN(:\x000eI%oÀd±Q
ï2¦=Íf¿ýx(\x001bøúqóÛ²ca¹7x»\x0005´\x000eÅÛ\x001dqºOñ}È×W'\x001f^êg
çöñq\x0008àíÍÓß\x001b<\x001eO^YÜ?@Ñ ¦tªÙ3½\x0014\x0000½=½>´\x000c8\x0019u¹,ý\x0002`]=<}NK\x001d¾¹½»ýéæþcK\x001cc(ê<Ì\x0000h
dp(Íïé¹º¼~¶:|sv~öúôâÕ\x000b§áÊ\x0012®\x001c«½uÞ\x0000×iK\x0015ÎpÜ\x0005ó½ó­Çàê\x0012®\x001ek¸£I^'ãBÔZ%\x0002\¶ûhÆà\x0012®\x0019=]¦\x0008à2\x0004;!(5Iu\x0017wÝ®\x0002×píèé
Ä\x0005SFUU®\ÇY¿\x0012\x001aëJ¸nôtÊpÓ\x0006 Ô\x0006§ð©9½\x001bëÁõ%\?zº°gÞâé
È\x0010ÇÓ54(oÝî\x001aB,Ã¤ÇØèé\x0002oeBk%
×²´\x0002Ø`vcô1´µÖ\x001dU»F´\Ë[úÜ­h­Ñ;Ñú\x0018ZQ¡\x0015£gkS[\x001a\x001cn8fl\x0015g	Òº»-@cx+#ÁG­1:-Ë\x0008§ûÜ¦+ò¤µ
>Ã:xUW
ß\x0006$QÎB³ÂÛ@Á*¿Ò[«¬\x001a\x001f6k0ú4Ivl\x0011A¢\x0000w·¦9\x0006·²j|Ô¬Y\x0019ïl\x001c¼÷¬°ðôÜL¹ëe
oeÖø¨]³Ò×`»\x0005×<sk¬t}+CÁG-\x0005ôa)¼\x000eÀÅHçAwÀ»\x001d6!n©üÍ¨)fXD\x000e¦8\x00180dÐ\x0007S¼Û\x000c<èõÖå(âØÏ*M\x001aMänjm\x000c1¯\x0011óQÄÊ3rw`\x00064ù\x000fÜ[b±ñÏÞ
³\x001d\x0008\x0014\x0008=%°§\x001f\x001fî\x001aØN¬[\x001c"wéúzÏ)Qãö<·ë\x0004óôÕåy\x000bDQB\x0014ý\x0010!\x000fh\x0011¢Â\x0019=Ép!+@\x0014Ó\x0010e	Q\x000e@äTwÜP\x001fØå\x0010âî0y/BU"T\x0003\x0008=\x0011\\x0002ÂT\x000fq\x0017\x0013"\x0014»O¨\x0013¢.!ê\x0001:í|\x000b\x0010¥I	"ÇïlÙ\x001e7¶\x0013¢)!~Á\x001a¼A¦\x0004ºd\x001c?³å»\x000c_½\x0008mÐ\x000e T\x000e\x0002gU >LSY¹'AÐÏø\7¾ð=\x0013
\x0010\x0010*aD²ow\x001c¾\x0017/ñù\x0001|\x0002\x0003?¥(ÓÇ\x0004\x0011\x001cÂ§IEÌg0æëýÆ¸5\x001dÔ;\x0015~e\x001aZ¶bö\x0014y¥²y¿ÎL'Ru¸\x001e\x001aÿÓ1\x001a:FµUîÅXélÞ¯´%÷9©+9ö¨I¦\x0014ÎZ¿ÛCÝ±ÒÚ¼_mKÎÑ{\x000f\x0004Õ=%\x0019£ÙWíÅX©mÞ¯·¥P¤\x0014!9NöY3GÉñÝ^ä^Þæý[rå(Ø\x001c$ðSKYrkw[{{!V\x000fhF\x0019sa\x0012Îâ§V^µ6¢Ò<¢_óÀ±xÜ\x0015OÆ\x0012Æi\x0003#joq@õ\x0000 ÍÏ\x001a½\x0008-m~ÕÓÇX½j1ðª¡½\x001c\x0011f\x0002wØZE\x0010w\x0007©!2¾\x0015\x0016\x001fsX\x0000|}¯7Ë\x0005/\x0001Ü+I7Æ¤\x000c9´|n-\x000f@\x0004²¾×'W«^\x0019¢(!~@5!3D£\x0011¢\x0017\x0004Q\x001dP;í\x0010e	Q\x000ebúÎÐÖ]©=¨î\x0003º»\x001d .\x0001ê3d\x0014·Ø´\x000f2!$n³§äÑÐ\x0008m7B	\x000fD`õ^fcd®Þ\x001fr$Ú!ú\x0012¢ï(hx øÿpé5{\x0011Î>\x0015^¿æþçü¿á\x0014yõVxÿc:Ï@"
!>Ï´x5|\êZ)_ÔJñíÃ§ÏË\x0010U8F!ÐüùÔ\x001fL¢ /Â\x001dò"\x0000âÛËw\x0007×¥\x0016\x0018EQ\x000c`d\x0006IuÃ3&Â½àþXòÆ~A-6%H9\x0000RàJ\x0018P×ü1n}v½wW»Aª\x0012¤\x001a\x0000É\x0019&úõ\x0011¨%7>ö4\x000eu4%H3rùe{Áp\x001eNRæ;yÀ#ë\x0000éJnäÝ0b<\x0017X«!^¥Ïív[zzA>GÕñq³\x00116ÇæÿÂó¦&àeÌ\x001fe`NJh3p/óMlÂ\x0017nò\x0003ß¥ÉhéÄ¦\x000cÒ¦|:úp{óô÷£W?ÿþ¿>ßÄ¥Â\x000b*Ý;d\x001ett/$W´\x0000Èy±ÿ\x0005]\x001f}8;½þG¯¾;yx©pWxÅ(^Å©\x001cþJÒï\x0006Û¼Ûer\x0019C+K´rüt5\x001e(\x0011ÝK	Ýî	®ßÓc9WxÕðé\x0006%üQp\x001b0yÊ½Qù6ìÖDð\x0012¯\x0019ÆË4@§>5"r­©3Òíi\x0002\x0019ÂëJ¼n\x001c¯Ìç«4\x0016!\x0002^×w¿ûÔ\x000b¶Ð³ \x001aØøí5DtÆ¬ \x0004W4&è÷¬C\x0019\x0003\Ý^>|}%¬»IJ\x0000öÀ\x0008XXìúflwõM'`¿­Ìü®2{ýðûÿw·ù¼\x0004\x0017Hÿ©Êk3%\x001a^©OAî¶_Vp__¼_F+K´ÛÊ¬\x0015-$4VÑC\7¸Õú­ô¬M/ZU¢Ý¾\x000bÍg+U±\x0005$ñ+ñ\x0010µXê\x00019à¾ö¢5%ÚmEÖÖjêrµa~\x001b¯ÌÊ7ÁhýèM\x0008\x001cî-¸[gé"p¶ß»é\x0004ûõ\x0006°9ëÝ67ÁàfJB\x0005¸¨s>'ë[Ý\x0004>z\x0015d°\x000bØH\x0011\x00172æÓ¥U!vwsÜ\x0010\[Áµ£p¥Î§+5Ý\k©·&üU.àÆÝöwÛOc!Äi!0\x0013\x0014NWäE,\x0007
!ÍpÅVÏGøEá¿yxº[\x001e_2Ê(¸cMÉrXä\x0011\x0019$q3Ø}]ï	æËëó&\x0008 (\x0001nå*»§\x00160)XÎ³: \x0015 ,\x0001ÊnP.¤ê¦Ì¡gÀ\x0007\x0012Aí\x0000U	Pu\x0003\x0002Ì'È$e\x0005(Ý×âÕ\x0007P\x0000u?@Z	8;X7¬ØåèÄgJ|¦\x001f¦Ü\x000flÉ\x0000nÃªé+hK¶\x001f £ñ\x0004\x00195RpGDÆV\x001c4<­\x0000]	Ðu\x0003d*F§±'¸K4¤eø´x;@_\x0002ôÝ\x0000¹Dxîå¡\x001c¤ GÌ÷ô¡w\x0001,B%ÁÊP©\x0011!¤O$\x001ea¸%¥â3¬S\x0000kCÒoI Ý	BRÇ\x00167Ô,cü.oR'ÂÊðnS" #´Þb¯+\x0004mÔg\x000fÆ\x0015­\x0008+SÂûm	\x000cÜc\x0003&\x0017\x0014²S
Óíé}ïWéiÞ­¨!É¤¨ùS­+" 7vú\x0013WwkBé$±øÄedðyÔØìöu"¬\x0014
ïÖ4ÒZà\x0012Lj~LwçBõÖËf¢zÇ¢û\x001d{ÕAólyV»3É\x0000«G"º\x001f4Ô²\x001e,/¶ä\x0015uôÙ\x000f,ªG"ú\x001fVT\x0001\x0006
p\x0002{¨ù|;X
¢C¸éV3yû°s&«jMÐê]\x0016În?Ô\x0018èöiÝjÇ¨¯1Ä{Ôº£wéº1þXcüqÀ1T"c$)
íêj\x000fÄ\x001aâÍU¶èØx?°Êä\Ï¼\x0000ñc
ñc÷)Êò\x0014©Ôær#ð½X\x0018Ü¬ØÃñêæþóãæn17Pê'J\x001cò½\x0004¸TY½Ë¥«\x0011^^¼¿:9_(Jb\x0000¢B6\x0017æîæ«S¿<ìãØí\x0003î(K²\x001f¢ ÷ ®eX\x0017 ªÝ|S/D]BÔý\x0010yªúFvj'}¹ËìÔ»Uþ^¶h\x0007 rÜ\x0008È\x0019Ô~q^3¸\x001b,7#4[1á\x0017ðZÞÞm>¦ªôÿçþtwÛ@!Ëý\x0012ÁãÁ\x0005÷ì¹^&wiáÞ¼J¥é£Ó×çg/ed¨¢*\x0006¡JEë eæ8Ì3éÉ\x001aHeT!U,\x0004÷Xì\x0007Î\x0007Tæ\x001f'vGß\x0006 ª\x0012ª\x001a<T¥pãx8TG',\x0018íc\x0019jJ¨f\x0010ªV¹kF=·Õç\x0014Çvµ{?ÔrÐ#µ¤\x000ca
o\x0018`rÂ\x0007Fes¶Ëü:µzV|ô]yCyG÷]B´{Svk¤\x001dX°Ýí\x0011
çÙ/¿n>}ªºÆ¹Ê-\x0014&Ïs\x0001c$\x0016¡ùnáìÍÛwïú
ÑÛIg\x0017é8ìàHªóçü3Í¡í«ÃV%l5\x0003\x001bËçL¹vd\x001d<Ûâ\x001cÇìJÌn\x00063\co Z\x0004M<¬zCÊÞ0ÀÍ\x0019\x001e·Ñ\x0015\x0001ú%Â½K\x0011ß¹mgÛ±º±öÛûÏG¯\x001e\x001eïÿWú\x0008ÆÎÐ½ö9æ:Xöð°?·¶}{yñþèÕåÕÅéKên[0Çê6Û>Ä0>í2b·Ó`ßCú8XÕ8bcÐ\x0015*®qF\x0013e^¼ÐfÝ\x0005ØÍ8ààöhÄk¨Z	»ô\x0008ïþJQ\x0007ÞíîpÝá8ø\x000foî7¿ln\x0007{â:ª\\x001a\x000cÉÂ¦LÐ¾Ð\x001b§þá±ýÇé³{¶Û¯\x0019¶_\x000f 5Xö`Î5Å\x0014P\x0004¦\x001a«ÞÓÍ4\x0000UPõ\x0010T]T\x0019TÜ&È÷D®$í\x0019\x001ajJ¨fìT½¥<¥\x000bØ°5WXêÍµbOªr\x0000ª-¡Ú±Så.§``Ú^#ï£z®Ï\x001däYéêK¨~\x000c*4>³+`\x001bq\x00087iJÉïÒÖ\x000e@-Üuê \x001fÀªô1&ª¡ùÙ#y%Ëõ¦Uî*¯uÕ²\x0002¨Ô\x0007Â\x001c
Jé3õÇîÞ¸\x0011¬¢Â*Æ°
ËPÖæ¡Ì{{Í
Å\x0000TUAUcPÖ5!Õá\x0006$ æ¹²»zq\x0004i¥¬ø¶
ÿ+gÁ%7HýjhH\x001fÒ$k`u\x0015V7Õ¦5«±ÆâQ\x0005ØL°"Ô\x001aUT*@\x000cªà\x0008\x001a<VèÒÀwåhÀðU®¨¼\x00001æ\x0006\x0000¯:×\x0019+7ØÌ\x0000ëA¢&¬nÛ·rzOðfóø±)ªå\x00184#[ÜÃ&£å÷PÖÞà«W\x000b1ÍvÑé=\x0011B+dÍGÝ`¬\x0011\x00031'©\x0007ÖB,KÄrüa³ "\x000eÊý9óÒ´V\x001fdUBÞ
j!'§ó¹8
#´È©Ç\x0003%â\x0001Èº¬Ç!\x0003C\x0018Ò\x0014X»\x0006¥0Tuò@Ñ}\x0000²)!ïFbÍÂqÊEkÊDRW¦\x0003þ\x0000»\x0012°\x001b{Ræ\x0019\x0013Æqõ$­S×°µ\x001e\x001f¯5Ü¸ÓÁ½ÑÏ#s\x0006
\x001dÓ4$uð¥\x001d2÷ÛmÄ>fmvM¯\x001fnZú(\x0010¡· -NÔ&Mö;©¦åNííÔ¯ßúmÆÌKÛ²LÐ§\x001d\x0019=«å»13±mü.Úµ_\x0005àáÏß,5Bð8G	\x001dRú&Ò4àb-å£ö@¹üU|yqqÚ\x0000S0Å\x0008LØô0A!##\x0007Ó¨!´9 !º`Ê\x0012¦\x001ciss´É{æÏh­\x000eöUvÀT%L5\x0002Ó\x0008¢ÐÕ2\x0002?ºå´<Ó\x001fP^M0¹ÚÖ\x0001ªl\x0008Hß>Ý.o¦Ó:<xvX±L7\x0000K²©Âïw\x001b¥±8\x001d¾½>{a']\x0006)Kr\x0004$ì\x001eMko8ö>\x0005êçnwGB7F[b´\x0003\x0018UbÑ\x001b8\x0011q\x0006/\x001fwóX»[hh\x0007¹Ý\x0014Ãe98ò6\x0018¨åû(%ùX\x0016\x0017c{)s^ã`ÃÎÛ`É\x0012ìC\x0016·ÌªÜ\x0001TøÎQ9Ì\x001c2ó\x0008îÐ\x000cNàt'8ëû >c\x0004g({©\x000f©Ä¶s³%4Û	ÍY\x001cµFc\x001c¯\x0012ÎRµVïKVõó%8ß{n\x001eBçtnè\x001c
kä°\x0011\x001b¯Bï[`\x000c9Ö£Av¸56\x0017`µÞ:ëz\x000e%M\x00042'w½\x0008\x0001Ã}éEHÚç\¦ï2»;·Ûðm³\x000esS*w7?¶\x0011X :\x0013®¥>OF~ÂÁ!ÄwïO¾y©?`ÍR4¢³´.Êäå\x0004RÐÜt\x0000wpnå%tò{¯¾û\x0005O¯Úöóas÷ÛÍ#|U	(È^ýüxûéóÃ¯?ßÿVIX¢
ÇÂ\x0017VÆA[HÐ|!ÌI3+°³\x0018<~õÝÕÙ»÷o¿+6þ|89ÿpzuè\x0003Ëï!\x000b^8é\x0017_=çl¾~¸ý\x0004qÍÅC\x0003`\x0001dù1Çlg1à
up]ãE\x000cBèBÅ\x00141Çt}ôõåÙ;\x0008n..\x001b@Ë\x0012´\x001c\x0006\x001d7ùù\x0004:\x001c¸!]ÁÛ6Yõ8f :	³{¬#h\x001cÅáÊr¶"h[¶ã adZ$ÐNÃpI\x0004íÓ°w\x0000-IÔiÐ®\x0004íÆA;\x0016+<\x0001s{E\x001c.:^\x000e«ö>À1Ä¾Dì'\x0010ëDæhxø;±eªIÀ"äb¿ç,h4¬\x0008º(Mõ¢½;2\x001a<Ï\x0008Úä»a¥®Ó U\x0005Z\x0015]QßqÎ
¸TZÛd=¸rÀ»\x001ajS¡6Ã¨}Òv+\x000e\x0005!l\x0019>@¶EÅ4äJsðqÕá{È\x000c\x001e´YxÐZ\x0011êp«×C]©\x000e>®;Bôøs¡®b! 5±¸òL®g\x000ey¥>ø¸þëÐðcL\x0006\x001e]¼ r½\x000bBPÐñ`£ %\x0013¸% \x000eÁ
Ú\x0016«4¾DÏõz¶ETJO+= \x001a4xÖÁët­ðt­¡Ey5Ô¿$Æ\x001d&XqbQë\x0005ëÈÇdót­ph\x001au¥«Å°®ÌpÒÕÅ\x001dTñx÷Úï÷¥@ËêÈá\x000b"¹Ti/\x000eGmÒctÈà\x0012@{³\x0006¶ÃÚ\x001afÖSÊ5Ä-AÄ°E[Á1lQbEÐ²ÃÊ\x001aÚÀ£\x0017\~\x0006\x0008:5Ð\x0006Ìz=Èªzjø!\x0006ÈÀ0`Ö,²&Ì\x00121ûõl¢ªî¸\x001b ç\x00103p?%ÿÃ\x000bCd*Ó¨+¨m"Ðm¦lh@í8\x0005¶>åC\x0003h³§+Ý¡'tU±½:`6L#\x00121«4\x0018\x001a@;³!gòû\x001fb\x0003J\x0011Ã/Fc\x0018á%&\x0012´Ýæ1TDí\x0010\x000e\x0000ùÚ<ö`)ý¢\x001eÛ\x001c}ýøôÈg½Y\x000bÊv9 àN7\x0005:aÖ~?æç£¯¯®ÿýô ·u\x0001YÅ0d&S[0@\x0016\x00192î=\x0005ÈûÍË\x0010dYBÃ9nT\x000fÓXq\Ò@6»ße\x001a¬JÈj\x001424R05dô"dEGÐØ{cÛ!Èº¬ÇO\x0019c\x0000æÂyK<c[ô^m7\x0004×pÍð	[ZUày¾ÇBÒ	;»Þ	Û\x0012²\x001dz&kð
-==¶|¯\x001d\x001cìJÈnø\x0007m\x00112°)%Äç[¡V{y¼VÉÃ:Y¥m\x0000Ù:Aþ3ã\x0014Ì\x0002]æj+Ìr°~t¡©ÜF
\x0007E\x001c:g³?¼\x001aÂ\)e>¬ÉZ\x0019vXç,1Õb¿¯1¹ÒÊ|\-sEjÙúàñëtÎ|ðûõÎ¹R\x001a|XkÀ\x0013ä9ø\x0018÷\x0007.\x0003Ä\x001cÜyÌnÛ-Ú\x001eó{³¹}¼mÀ«NÝñFò\x0010s'·Ù\x001a\x00111RïOEç\x0016·7'gWg
XeU\x000eb­x0è9DD¬Ì\x0013Ö²áq
«/±ú!¬@áÒ]°¾\x0007³¸Vã*pØóY°~ÛÑô;æÍãíæþ¾épÃcý¯á&¸4\x0002F\x0006¹£EâÍÉÕÙÉÅE\x0003f[b¶ãEã\x00110³Tû±F[º\x0010í½¼c}ÙcÖØ\x00074Y\x000c\x0006\x0013ðÅ!ærYä,æÂHû]#Ý	ó\x0004:h5'ÍS\x0017l@­Ã\x0016ÔzK­ùzðóÍÃ]Zç¶¤e¸\x0018\x001c½ µM+ô¤z©XuzôæòüðZ·\x0002ª,¡Ê!¨á\x00120 Â~õ\x0018H+\x0017nqª{)íÙ\x000eUPõ\x0010Ô\x0010Æ.\x001b\x0013¼`¡*¾2/ÆüíPM	Õ\x000cAµ\x001eÂÖ(ÈÇïÏ\x0014yÒ¾¶oGjK¤v\x0008)7\x00113\x001cjðÑI*(ö\x000c§ºÎ÷w%T7\x0004ÕàFÌpªA\x00029Bu|\x001b~ÀYèêK¨~\x0008*ÃeáT¡\x0014cÔ3\x0012îìKIÌf¨Uº
a>]Åyª\x0015IGA\x0003¼\x0006lÇZëÕ!Å*Àr\x0007ÓÌB£\x001d`EF@\x000e5uUTPÅÐ±
X>A[±|¬ÂIÒV|ÛZD;~kHµýX!¼AÍ*-Ì©Çc6x]åKv¬\x0011àCV@("\x00032,ï\x0012VA)IÁ÷GeÝX++ÀÌ\x0000læf\x0016ÕêbÄê)\x0017	\\x0000«`­+\x001fÒ®\x0002YwöJw@Ò\x001dà/0¡êº±ë
k+\x0012q^5Ý\x0000
KÊýéÒn¨u\x0015Cæ5ö¢'¬\x0002È7S®Æä:\x0005çëx\x0002¢º\x0001bè\x0006ð \x0005°Ï\x00116ô¥£ò\x0010¾,ùb\x000fM3VY\x0019-9d´ #A^Q
\x000ch\x0001\x0010*{±£\x001dj¥\x0004ä\x0012`©8@U\x0002\x0012w\x0011ª!ÝÊõ:^«¬n\x001c¼\x0001Áþ§ª\x001a8ÛÊ!V\x001b\½Tänªª\x000b Æ.\x0000PËá
	A¥bÜ{7k©Ó/¶&\x000c{\x001eâÚØ@\x0000<¨\x001a»\x001eÐÏÒ\ìo»,æ\x000c\x001b\x000b®å²j\x0004.gsý^°²O%ÜÎ(j2vo0[¸Õ\x0004nfrÃ\x00154ÐÖ;êØ°l¯\x0018Å­KÜz
7Ç´\x0012\x000f!-uXW[s³¿×d\x0014¸)\x0019àÜHèñÂ\x001c¶\x00064wûÛ Fû\x0012¸\x001f\x0007\x001eS¤\x0012{Nåc\x0008Y¼âB½>e7pµ8WUâ\x001c5?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==î\x001fQÜAV]d5\x001eÙ)Ú\x0017Á8ý#gTpÃ\x0016¹Xwõxb+~\x0001.2<=!{Ã¼/¼ÞlºÈf42<y9\x0001ã\x000e\x0004%¦%çÛólD¶]d;~L\x0011DD{ÄRÑÔt(;l/\x001a}Ø&¶Î°µ0¨ñá¬³ÎÆ,Ä¡K\x001cÆo\x000b#R\x0017\x0012\x0012Ã\x000eÉKl5E¬4¼{í[#qì\x0012ÇÑÄ\x0018\x0019ùì¡4Fn\x0001}ÌlöeWÚå¹ãí\x0005VqsÁSÍe\x0007ÎÊ=¾Fâ
k!Ç\x000bMº\x0015¸Ê`.ò\x0010LðØ#Ò^ÌuÈ
s!ÇÛ\x000bp+R_80£\x0012rn®³Á°³zOâªÙm0»ñë,}\x0012 M»Ùåºj°p~þ½¼aâäx\x001b\x00076,%FpqV=yqÑ³Kdý\\x0017Ü0rr¼ÓRæ´\x0014:Ë<\x0015×IU©j6\x0017Cn99ÞÎ	T\x0004Î\x0017¶·!U;ã:[Av\x000eÐ¹ÖY.³\x0012ãm³|c;\x001cøY(ÏÏ¨Ü|6\x000bò»¬FûËðºö\x0014\x000b\x001e®ìÜÃb½à#h£yÓ_\x001eï0+ÿ¦\x0007¶LÕ@¸Î¤\x0019\x0011\x00017\\x0003ÔÈ¼q¡¨ñ\x00174ôòZ3àyíK`kOÍl#ðeVã-³T"uÃ!sÌ#:ñ6Zò­­g[ä
;§ÆÛ9\x0011\x0003\x0017âyÁ\x0005Õ6¸\x0012@Ôb®\x001bPoØ\x000c=ÞfÀ¿)½R\x0013Ï\x0004\x0010\x0003?X1Ò5\x0017óÆ\x0001Ôã\x000f \x0000÷Â\x0010³³ÔM
¶9ò:ÏfE\2²ß¼\x001c	&\x0019Kô4£uv&x¶lèàE¶UÊ\x0006O´
èÃâ×¿þuýxý×ÿ­¯\x001dÔ8$GsJZP?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=yýò¢\x0001¾ÂWðáJ*#\x0018\x0005WÂãc\x001d\x0017:}¬¯§ðu'|¸$å*
s\x001f)V£ÄÂ1X\x000fßLá~á\x0001Ô«$\x001e&ÄÇ­vøÂÉYÐÒÉ:hùáþë¿O?^½¿þøñúäéþæz\x001c\x001a 47¨ä'ºæl¿ç'§/<;{ñâìäééùÙ"£X1Ã\x0018Eð&¼ÊDQ\x0014Bq8V¥ºÂ¦À¨ÎÄì£$ÍN\x0005J\x0004ô´IA\x0014×[/ËÙLIÖä8JÊQK\x0005 $\x000eXÙºÒ_÷5()]QRz\x0014%îøÍ^\x0018Ké!M\x000eÉôR¯±­&~-RªüÚ>JV\x0014J*ÍGIZ^pO&-mãËñZJ¾¦äÇQ\x0002ÏJQR­Ô\x0017(ÍZ3!×Rª¯p5ì\x000eOÉÁ,wq')\x001cä8Jë&ÿ÷2º\Ab¤ë\x000bO\x000f»ð,¾*\x001bJß¶¢l7å(é¯#wÓw\x0004¤¤ÉPrzGÓì 1OJÖ0ËjJõ.©q»S×yT¹\x001d¢ä£¤\x0017f¬l¦dkJv\x001c%£Ëg¹n\x0000ç\x0003²ñ\x0000zé«P2®\x0012<ã¾}Á³µñ`\x0019\x000f\x0016çáXºð\x0002%ä\x0007«#Û\x000eÊ\x001dE\x001bcµI1\x000eÛ$\x0017"\x0019­ÆÃ&å°@\x0014Â¾5æ«CRÌÖq86SáF\x0013Xù¡3'Y5øÖ»µÂÓ8Uë.}n¥$´x0[k}_§kåÌ]Jß\x0007qÂî²üd\x001c¾µ"'ð\x0006ù\x0011Ã´æ¯¬ß§I¸wêjÔVùIá]¤hzûZæ\x0014ÚõÞ$nH¦Þå0ó5Pg]¸û\x001c'\x001b)Snó¯äd¤ÍÚßÙ¬ý?W
´.ïÐ\x001aµ[xkÎn\x0014'RÈ»ð¢+j¾[jàf	\x000cy\x0015õK_\x001bTq7\x001a#¿Í¤Roª¦_ØçrR?s{òúúãõåÍûöeRÇÊ\x0004Ã\x0002lËy»8y}öâìñù³#\x0005ßÄÀê)\x0003\x0014é>\x0006Îíre¢Âs«`¸×ZlU}Á½j\x0019Øíf ©N7Å
õëÓ\x001cWh\x0001eà*)rÝRdy¢80\x0008;I}|5\x0017KKÙtÂW\x0008Q¬\x0008Än\x0002FqsÓ\x0010=Zlä*c%ÚÊ~Ú\x0019HQ1¢\x0002h\x000fj%\x0017ò\x0018kPþÜGNÆ¥`«ñ«\x001a¿êÅïòºç+;z[\x0006¢-<Em``k\x0006ÝçXÃ+[¦[ØXEµUy¯ `ëM°Ý\x0010\x000eBd#÷góÚ¡Qqô.¸z\x0017\ï.¸à0}'SpÜÐ2Æµ=.¯ P_F²û6rÖPa®	`ßò\x0004\x0003Á ´mïÊí\x0014¬((ÙK\x00010à4¯H}\,¥%£U¶¦Ð-Hò HJñqvVr*½nË0\AA×\x0014t7\x0005a)f\x0005qz\x001dÊ¦ÕjmÁ²PõqVÝÇ\x0019¼¢C-ÙQÃÈÒÇJ-\x000c¾]¿\x0007¾>	¾û$³êh\x000fÝIE\x001dy²^j§´z\x000b|½\x0005¾{\x000bb\x001f\x0001\x0007ÃQ½
l\x001cÉÆ>+6!Ô\x0014B7\x0005m¹Wm¦´:0\%&u[JÞ

µRPÝJÁ\x001aUÆó\x0001\x0005jcËØ/ÝÖù£®/TÝ}¡Z-J\x0012\x001eè\x0004\x0015h\x0013J\x0016nËv^±	vÒ\x001a-m\x0008ÀVÍ&w×"=%x\x001cÆÍ§¡­aÕ4cáE7\x000b¸r³x¼ó­Tfl¦®GýþC<ÿËN;\x0006«QrÑ¡\x000f_HÕâÄ¡-[q5ß«Þë5\x0016·\x0001¶[ÉÛu±9ï\x00063c&OÚöÊÓW°4\x0016åiÆÂvø
\x0006yºËSç©É\x0013
÷©\x0004jt,ÃÍ¶\x0002½¸^bMa4gFzÉ\x0015ÑÒ¶=ª¯Ù\x0008;ß\x0008Û¿\x0011¡\x000cJã¡\x001cm\x0004Ï?ª-'eÝ¸Þ;ÖjN#cw\x0007Å Õb·ù-b?S\x0014Ý\x0007Ûq£(JÛ\x000c\x0010-_bÄÍ?<\x0012Wó#Ñ©()Ó£\x0002Ø³<)p¾0>1?\x0015ûù©èµ<0¥K1¸JÉcË®b?\x000f1\x001drÿy/Þö\x00065WF§Ôszu¦$?·µÄYÇârÎ¢óp;çË¸rcéÕ»ºgGÇÊÐö¨ïYÝÏâ_n{ ·s\x0016\x0012õïaq5gÑ{Gý\x000bY\x0008rè'¹ÌF¦eO~¾þËûTÖðäæÓû¿¯yÙ58\x0010rc¹Kh8\x000cËÐr¡¨äÉïÏ¾öê\x001a¿|ö\x001f\x0014LEÁ\x000c `q\x001e{Òw!ÐäµPÚ¿)¿ î6P°\x0015\x0005ÛOÁI\x001a¸mQîï\x0015·ÏÐrá%b\x0003Iú!\x00164~\x000eDJÄAó\x0016ã	\x001d[8Tûàú÷\x0001Z'\x001b6xÎÝÐjáIk\x0003\x0003_íïß\x0005Ë\x0013d¬\x001f%íäÌð¥DÉõ\x0014¦BJ¡èã ½âÖÅRj\x001aà\x0013\x000eã\x0008uX¾D¨I\x0001$$§m¶ÁÑDSV£\x001a-LJUÂ_{¥	\x001b\x0012QeäY¢Á9Q*«\x0016\Ó
$j
§úUËÃDP|19Ã\x001dúµ]¨Þ@ÂÔ;aúw\x0002d(P[D\x001f5qð!Æð£ªõ´\x001a ¨-yéÞ£_HX\x001eW¡íp
¡jM­\x0006¨j4¨Ã)vBÌé.òÓ^ÊqÞ@¢VÕj®V^Ry¡ÉÎ\x0005\x001eø ÝBg
$jM§\x0006¨:#)X\x0003$4IÕ	.H_z±ÞÂ¡¦~U\x0007~\x0003½6¦®<Î3x{à0\Iz\x001fÂ}Ü\x001c{Ù\x0019ÚN¦ÝÂcÝz\x0012¶Þ\x0008;Âæôp=S×ö«©k°«6&Ù\x0019ÂßôúCu±\x0007\x0019mGÉjÒra¦Î*&:¼©JíÓÚt3|º½¹|ÿqU©°\x0013"áNc¥\x0002¹Õª}´YÊË:0xòòâüñ³\x0017Ç²§\x0013I\x001f2µé´åÎXÏÏ+\x001e«É\x0012	°¡Z¯§V\x0012Óª` ªûHX\x001b(SÔÉ\x0010\x000fÁi\x0012ë©Uc·Ðº"_;Iàý$Ydéqï)î§á¼´ÞOÍ$LMÂô£N
M\x001aÛ\x001bÎ
Òªý~j%a&8êÚ\x0012ßDÂ:J¸´1Ä\x0014ã\x0003w%o¶:9Ø\x001dÀA±Õ\x0011Áåé²^ÓFH?ò3\x0008LÏßpÒýª\x001d-7
Å\x001f\x0003Ý±2r×.½æTkôåtÈt\x000c\x0007N\x0014\x0016wlõD	Ô$>Í¦á\x000fÚp\x001b8³*r¶ÈÃê7U_",ð¨ú\x0012ýÏý÷Ù»\x000fï?¯ëÉ¢\x001cÍý2Ái
aú(K#c·7wè.sröôù³WÇd)Lç("}7\x000b\x001eàs2²$ÜGÅÃ\x001fàÄ´6XZÁâªfq5\x0005Q01ºü\ç\x0016*61¸¬\x0019\Ø\x0007ê°\x001e°õ¬c\x0012%¯}!X°\x0005\x0002oªfýh\x001bTuß¯÷·ÿ¸½Zu¤±´Ç1K~úÕÞn§­]\x0011_^üéâÉ"úiuyTuX^cJ>'B(N]Ô\x001cØæmè'MÒÚ¾Å\x0007[»¤y0²zÓÓ8·µ~ècµöÓrMèSNY\x0006_R\x001fT(ÝY}ëø6ôÊVk¯lßÚKTú²ö¹½\x001407w}j/¨\x0017?®Õ×øvEy\x0002
Ì¤¢h¡+]kï &øZÕðÓ÷\x000eø
ÝÎ<æÎ(m¨°Ï@38rCO.â\x0006\x0000
ªéz\x001a\x0016Àf!Rh\x0010\x0011\x000bp~Eë¸æëg5/ ý·t\x0003*½!\x0013xÛG@aO¦Üú]ò-¤EéÁ¿àùo p9'pùíì\x0000^;ós®¢ÎsÆ$\x0012©|=YA6½á¦s`\x001bët×lÃÕ|\x001b®zå(ð\x0008\x0012\x0007Óãµ 2ã©RFvÎnqjÔëýí
øÎ`k,E¨Øg\x0006näõÇ"Å\x0016Ïì\x0002F½>;½X"0mÇª»\x0019xãF	G·ÆÈeÆ@ 1øÕL`úZê7Fl\x0001¥\x0016Káèý\x0016ö\x0012À÷_\x0010¡õ\x0014|MÁwS°çÃKiÉ&G^aãôa\x000cDöÈâ£Ã/\x001eÅIâóÉéÕþêý~M\x0018\x0000ÕÜ.À`^LÂ¯5Å¤÷­\x0019V¯NN>yvz,I,3¼\x0017bôVôR\x0008>Ò\x0018\x0010\x000b÷PÎÊÐ#\x000cÍ\x0001Ôf
Ó\x0017P¨C^Û¶ÁInl°\x0006(÷Û+÷Á.8\x001bHÄDì'aKÔN»@¯T LT"=æ\x0007%1m&\x0008$R3Á^\x0012[)£¡#¨1e&e\x0003Õ/\x000c±Û@ÂÔ$L?	Sê¥\x00019ÕK\x0003	É$\x001a¯¥\x0015\x001c\ÍÁÙ\x0008â Ìa#\x001c»kfaÞÁ\x0006\x0012¡&\x0011\x0006lá^f*h
·D-©\x001e¸;­ïlÍ$L}$Ì#ùä7Ñt¬)ü+\x0018~ÁZL·49axVÂª¬$\x0011lîÙ>ë9¸ë?\x0011ÅS\x0019\x000c&!¦Ã\x001eº_\x001bß\x0012Z((\x001c\x0011/&O¶J<¾Ø&kéòæýÕ§5öõ`çÒÛ¶\x0001nqÁ¶½ôøüÙGm>1³7\x001b@B+\x0000\x0017B¤0|\x0014¥Áñb
,*ïAü÷°<ó \x0004I\x0001¥(%WbI·Æün¤áj\x001a®\x0006Öüðà\x000cí±Ê/ÙN\x0008G{
PÉ\x000cýB\x0015ðDSµ\x0006àf+¶´ÊÑx\x001b\x000bã±×àdìñÒ÷Éçwû_>}\\x0013Ó«\x000fÉ³±Ú\x0015\x001bìBýôá¹ó»Ó\x0017¯_¾Xf`g\x000cl'\x0003\x0011¹ì\x0018Òsþ¤1d\x000f÷Sk\x001eC#\x00015Û\x0002Õ»\x0005ø:E[Í\x001ee&àXÑàØ
\x0002ÁÎRàº¥&=¿þõÝí\x0007s~äth¥\x000cÇÅBêAçÀ*Ó7yöÇ§\x0017§G\x001aÙf\x0002¡&\x0010z	8³\x00139\x0003W0åÌ*9
D\x0000û
\x000f% ¦c¡h\x000f.;7ÁS?k¥#Ea\x000f¸fÉêNµw(,\x000bÑä¹(ìûåH\x00179Ê³Èk9jNnãPMµ"IzÛÅA`\x0007¸Hû )!	[Óò6ÈæTÉf
s
ä5e·YPaøcÚ\x0006]¶aaú\x0016
Ws
W}\x0014ÀÄst qÐ\x001bI¥TI¤¬-\x001cös\x000e§\x0001T\x0001MUª/%³õRºÿ¹A¤!ábà\x001dÂuñì/ÝþÌ\x0003®~øôùËºA\x0008.ì¸½LäR\x001fmUi/³\x0010Zzöý\x000f§¯^ñ«\x001f^¾z},mDç(ßá\x0001Wc¯Tþx}óñúz\x0003§\x0002&Ñç7\x001f[î$ìÿCÁâ¥«\x0007÷ãÙù³³cuÅ2gq\x001f8à ÊN=¿ÊDÅ$N\x001c\x001fÞ\x0002Ed¬Å	ðÙF\x0015\x000b½¾\x000f6êù³cæ)aw\x0015v×ÝÛÒù:\x001bEpr_b\x0011\x001a\x0003ÀC\x0005<ô\x0001\x000f¦,ºò|÷\x000fO\x000e6u\x001böi\x000fPÀ>sÐV×R¹t.xªe½-\x0019/¦Õ5kÁ>©	CìUMØ\x0006ìÆðÓó<Ñ\x0010[Zñ\x001cbå¯\x0017^u.|à	màq\x0013e¸0ùy9.L3kÅ\x000e\x001bRÔ&n\x0018¾\x000cÞ­wùÇÛÞ© \x000f/rì¢×gµfG2WüéXªcæ0Éì\x0007\x000eú7
ÖqÐRð\x000ez\x0014­Ã\x001eÄÌa!Ûk\x000b\x0007UqP#ö^\x0007%f]Ð>\x0018\x001aO\x000fÊxaVÏ\x0016\x000e®âàº9¸2ö\x00053-rûÛèy8\x001cóØìÍ´rðÕyø­ú¯\x001cÀ!£\x0016¾"\x0006\x001e]ã¢ãó`WÖ7p\x0008Õyø­B¼\x001c¼âNÊ2gð¤}PÁ\x0014YZWùÕÄabIg\x0016ûoÆåÆå7E#¦\x0014¤Im4ä\x001aÛï÷ï?Ã»\x0006È«t²ÔdOGg(\x0007ÃzCý¤^Scñýé³W/_¼8mÏ´
øè;eô\x001bùà# >RÑì-\x001c>CC\x001b5P²['#°fð\x001f9¿MÝÎoßë¶¿ÍÓ¹?Àý|ýþÃ
N&ÈPJHÍ0Qøv¾Ðôí"5":¿x\x0006NÜéEÓýüÉË\x0017¯Î=_æ¥¦¼ÔP^\x0012{Âs?fyÈ\x001d¤\x000c\x000bI¹}Äô\x001eI\x000cÑ8Êî+ÉÞpA°õëíWÝ13%fF\x0012spñ\x0011/Ï
´£;\x000c[xgéäå¦¼ÜH^Ø\x0012(\x0014?¦\x0007EÃÃ/Yè#ÒI,L¡Ä\x000c7ÆÃ©\x001e¼cº"T_õî¼á(F2\x000bÛÑ'ft)\x0006\x000ej¥ÈâVf6\x0015OÙðHÖO÷7û_¿¬Ð)ÏlÀ.a)Bg%Í\x0004×bi¬çAk===?ýãëEüºÆ¯;ñ¨q"@Æ_æ¿OØB7Î6\x0012Së¶`ß¹\x0007ô±M\x0007O1·"t\x001aþÖ8oó&L\x000b\x0004ó6\öí\x000b\Â\x001c¥}°ôd k~\x0001lç°sèÛ\x0007LÍÎ¹kx\x0004vÔ7Å9Þ\x0006Óm´LÁÛå\x0006Þæ¡ä÷öä\x000fû·@ãÛË\x000fïWå÷c·aR(8Hi£B\x0011á¸@u\x0017'8=ÿ\x000eØüpñøù³cyþDEM©¨\x0011T\<¸ÄEÎÒö\x001eçÞðE{|?VSqÉAÎP\x0006\x0007áNg¤§7ûï®ñYdÝ\x0013¿æÀ$\x0015JQp%ÉÂ­é\x0005óôüôÅÓ3|\x001aYd\x0013j6w"\x0002\x001bÙ¨÷Ý>ó%c\x0002\x0003Ëà×ètê'Þ\x001b\x0018/ÒL«ó\x001e_ß¼»¾Y\x0017í3_¨\x001c]ZÑ³7m:VbÇgçOÏÎÀOj\x000b\x0011|]Z¸\x0001¼+7X\x0012éS¨\x001bì\x0010.%Q\x000b¶+ÑOÚ\x0003úz¨ý\x0006ôÂò«\x001aöÈilÞq¯\x0008cÛZ»7£÷5zß^\x0005Ã±p\x0012Îæ\x0010+½òcdc!X\x001b|c+øÆvÂÇ´úÊÛ\x0011½$\x0007Xê\x0010ÊÎ´e )=ð­¥>\x0000_ìHv¨MêÖ\x0012¶Fì¡Æ\x001e:±\x001bY^p¶]t\x0013äµ\x001f+øVUð­ê/È¯Ó\x0011Û¶;o©ZDÛ±£*S\x0015oM-¦¨\x001b.\x001e}/}iyR\x0004GïMÑZÏßÎ`?g°ïc`w¢ÀÖeS\x0002\x0008p168\x000eµÀK\x0004¤\x0008µ	'S3õÛ÷_Vu7Çûå§Xvr¹òN¥yñM6Ý\x000f\x0017Ï^\x001fK¤ èj
]uAwúi \x0015wË*}h\x0016f.´â\x0016\x0012\x0013qÜÄ\x0006ÅÄÖYúûOoW¹\x0004ÎPó\x0010«C,.Õä\x0012¸öìýÿë»cö¦E^@ 9òVæÛ\x0013øi
p0\x0007Ê\x0017àAÒs&.
vº8K¶åw'ðÓ!#¨[!*äéûfìVËÔrÉÑÔES¬æ(ÑRêV#t)Ä\ÌE
Óíòùä1üôþúfUÊ\x0013,·ÂÄÅ¸\x0015\x001dÎ#H²\x001e\x0015Ï¬	\x000b^$_1¯N\x001eÃOÏÎÎÏ^-tÌA\x0012¢ç'\x0019+ÐÐ7\x001c©ã´¢m\x0008Ò:\x0016¶baûY\x0018ÖW\x0016
\x0006¢\x001aM©\x0015\x0017Â\x0012[Xj/Ì½Àf\x0003Ô@TR¹\x0007ÜûFþ¢Mg­"Qm\x0019°\x0015ÚQ¥\x0015J\x001eÚ¥¡«l\x001b¦º¯Xø\x0001,àjâþÀ`j:ÜüR©tù³Ã$h\x001c¤\x001c OBï¸?0L}wÂ·Íü[Ãb:\x0014vìgá±\x0003gN´\x0006ß\x0012¾<p´\x0015Æ\x0017(m+Ò¶_¢\x001cØÑ4j\x0004\x000e27+É:ªÕ'XÁÂÌn¨\x0001WÃ4¬.´uÔJÞ{Å©N.4ÎÞ@ÃÊj3¬\x001c°\x0019èUf}ahØ³|Cyµº¿óÕV8ß¿\x001568~M°!R\x0001wMÖ°T\x001d¸vþÂKª
Ïmå\x0001Z®rØ+DÊaOZê°«G[ RÕç[ª\x0001\x0007ÜbÇ¦y¸HÅäÞ	ªsÔÚ¶MÄlâq)Rjí¡"þ±À?RÏ¯\x0011ÿÕÏ×_èýöÿgU¡ÁE~âÑÞ
y!b ßYºÙÃÏÏ\x0001¸D¯éÝöìå{è7ýó?öú\x00129^Oéã96¤ÝÿKÈé-T\x0013êóO"èç×7ý±î=¦\x0012

zÎ¦÷Ùä´ðÑá\x0014§÷üå÷ðOûüìüWRóÙÓ\x001fï­\x0018\x0000\x000cø.>\x001e(À¹þéã¡\x0002Äk/}<Th¯¤\x0007\x000b\x0010·8>Ø-è\x0015=Ê\x000f\x0015¡M\x0008í\x0003F\x0015\x0012ùó¡"\x000ci
\x001fÞ]ø\x000bh)û"%)>òâúæ_\x001b±IÛ6\x00038\x0019eÈq\x0004\x001fÎó\x0000£Wâ\x0008º\x0017gç?þ±\x0001\x0019Þþ!"\x0018BM\x001f\x000f\x000fZ\x0012¸ð0¡áiÅ\x0007\x0003íãÇü¯oò84\x001e¶ÿÇþC\x001b6\x001d±\x0017~ê ©¥qôæï½\x0011y\x001cwtàZ{±Á	ýÓé}9z\x00158û+Ù\x001e\x001e8T\x000f4Èå\x0001Ã³\x000fjå>ìù«p)ÇA\x001et×uã\x0000\x0007Ãæö½Zx¯r.\x0007{;§;Äé\x0008{\x0014Ã}©1\x0013x©úP¹\x0007\x0006ïòû¸~[\x0017æ·Ïýí÷û«V>\x0018Â©÷ùõÙÃÖç\x0018|¼ÿ^¼z^<vz_"Ø\x0004±C°î[B\x0003\x001eyÿ
!\x000e¸¼á\x001bZc©Ó- å·\x0004\x0019Ó¬óç·\x00039­²þV9y_Ú~K«\x000c<\x001d¾¡UN\x0013òç\x0003ìþô÷?PÖjÎUýÓí
F_\x001bqjðä1·\x0010qb-\x001eASùüö\x001bCðá~ º8ÇHë2¼Ô#%}<LxÅÒð9ý0á¡c>\x001e$¼¤ô½tÍ¤\x0004/ÄÛ\x0013QóÈ¿»þ¼÷ñº5R¥±<4%i\x001du
Tá¨ \x0002\x0017§¦çà¾;{uúôÅ½M&èR;éôñ Ña(<}<Dt)O7}<Ht\x0018ÚH\x001f\x000f\x0012\x001d\x000fÒÇDñÑôñ\x0010Ñ9¼LÜ\x0003»Qö?ýíÏo?U÷ÝóëÏÒ¥æ\x0000}\x001a®e_J,\x0008Â½Yî\x0012=?{5©Tj@k1Ï)}<`´NúôSnÜÁ\x000eøßïiWtðÿÊ]ÖsÆèü U\x00006ÞI³°9Æ\x001fýxLÍ\x0015hÎ&h\x000f\x0013[Z¶\x0007µn_þæõÍÛ7¹!\x0003¶ax¾ÿµ5\x0014(Ô;Þ°Tv§kÇ×g`ÂûcÁÀ?Þ\x001f\x0008üùËË\x000f½"½DWþÛûw·×_Z½7]ªÓM\x000b¶39Z	§ÂæcáSÿ»E÷íÙÓ³ûjt'h=\x001e`/¿\x0015¸\x0001\x001f\x0006úvàÚ/ÿ­ÀE?/Øodu%_{?¿	¼©0PÎÊ\x0003\x001f\x001eÞ_Ô[ùË;ªvI5.Ï¹úËöG\x0017ESÆÁ`.·ó!Àµ F1­\x0011ùg¬Ý_ßÛ\x0012wÓà}>\x001e(ÐÞßü|ó&÷sL]\x001c\x001fß\þüþúöï­ú4õÚNoÎ
¼kh¶±¹wfÄÞhú^ÏÏ^½zvvñ\x001f÷\x001fßýòçÛ_ßäiá«÷ï>6G\x001cµ\x0012ËhRÄQèÜJ+àI.\x0003Ørò^x¯=}q,4ÊØd?Lp
/ùôñ\x0010Áá¢©\x0007ºré©)}<Dp%÷\x0000Á\x001dî½\x0008\x000e\x0017Í<¬³â?ÿºUØ\x0018s	þùÿ6k\x000b)Û\x0005SVM¹\x0004!°Ó\x001aõý\x001a\x0018³	^\x001eQ\x0014ýéã»_<HBäðëö\x001fcÓ\x0000_­\x0004¶øñ	5¹$0z\x001c¡y¿G}òøìþ¥+Ð\x000cjôñP ù_þ3^sÇ!,à=}|sû\x0011ë\x0000sºpYò\x000b¥\x000c.7ìÀ~n¹ëBtÖ\x001cE<>¿xiÿ÷b|'â?~¹¥2«\\õôÓíÍÇvZ
\x001c%/\x0000Ä¨Ò
F\x001b\x0006a{\x000by?Æ§//Î_\x001cóªÍë/êÝd\x0011³\x001dU\x001a¶ ôàê{ö8M¥i\x0011Áï§Ä8ãâý^6£rOÐû*\x000eðà¾9]Î¿¨Æ._¬»mT\x001cÖÓQgã/hr\x0011vÄ6e÷\x001fçC{pK]áº\x000b¸$ÕFéX\x0001×ê~«u-p¥*àJu\x0000·¸ÌÙÜ6þ°â4Ë\x0014{ÿÓÑjàõ«\x0015ÇR­T\x001e\x000bÀ£ÉmU\x0011¸"Å
r\x0001×²\x0002®e\x000fpíro.
>£Ë£\x0001A£Z^qgì@à×\x001d\x0010W\x0002Çæ=\x0019wT¹A\x0002à6-p$@¼\x0016·Q\x0015n£zpÃ*ç £v\H&Lî/\x0010ê~\x0013f5ðzÁM×[Ûe"pêZ
À\x000c|Ìeè'­\x0004ò/fó\x0019Î?¥
·vÍ£ó4X
Âæ`&ÅC£÷&´HÊùËT\x0011w¿\x0016gè¦nº ;/é)\x001d°ë<ÀÆ=$Hiz+ïW\x001b°{1Å^÷;_ÝQ\x001b\x0010ÀîD¾\x0012±\x001fsL\x0008Ø½½ÿ]l\x000böjÝ}ßº\x0015zõ`oóÚa\x0002tj\x0013\x0000ÐÝPè²vÙ'î6R§\x0006Àn\x0015Ñi\x001bxÝGB×5tÝ\x0007=ÜZ1\x000c\x0015OÀ5é\x0019ºo¹\x001bÁÛ\x001a¼í\x0004ïq\v^÷¸\x000cÞ\x0016y?\x0012~Ý\x0000ÞUgUº®ÃjuÄT@\x0004ïÈC|´(ç	<\x000e%\x0018
¾^y×·òFjl·ñÚ\x0004>\x0016±IãÀ×·¤ì»&­\x0006ÄV^åëØ\x001d&?\x0012ÒØ\x0000>ÔàC\x001fx\x0015òo\x0004O¯ô\x0008\x0019jG5øØ\x0007\x001eë³²Ø Ã$ó \x0018üH»@ÆZäcÈKKf;,¼Ä¶\x0019»e¡±-\x000e^+vî\x000fÁæè\w'¹\x0000v\x0013(Ú\x0003Ø\x000bx;TE)Yà\x001dy¨ÊÁµãXh<iWt<¯
aÙ)5\x0001=<VQ.JËúu¤È+U¯¼ê[y\x0001.¶)+OR£+\x000b?Täg\x001eH§M&==Í*ìRDÞ±M^Ô@ðº^xÝ¹ð!\x0018Gl\x0003\x000eÊÀÊ\x001f©Û\x0002¾^ù>Ò`ûtºãib\x0005`¢((=ô®1õÂ®7Áí\x001c+¨Tãjcà»F5Å8ÁÛ\x001a¼í\x0004¯ø®qÒ\x0013rÃªõþ÷è
¸kKXuZÂZï#î¸#a\x0005F79±×¶¤ê³%
\x0016°z²
,iÙ_Å\x001cSµË­ú|nÇÈùc\x001d\x0006ìÊâ\x0004¯C\x0005>Õm\x0007¯á\x0017\x0004>ÈÜ!×GEq\x0000¼8òþ²IlÞ\¾ÿ<\x0017\x001düUô8æà¤á»Ò\x0004kXzFÙev:¨(ÿâÑ$Ëðöäñõ_þùÞþóÿY\x0011²\x0001ÃL
Ì\x0003çØû>RrB©O\x0017'ÏÿxöÝ±:®*èª\x001bºÏ])\x0001z4ì8ç
ö#\x0019ä[ÐÛ
½íD9¼²,|Ì/\x0010¢×ÕÚëîµ\x000fù\x0019\x0001Îä¸slUFqäÒÙ\x0002¾ZzÝ¹ôÞ)\x001cÓ^Y\x0016Àï|¨¬îwF6 7\x0015zÓ\x001e\x0005î\x001b'Ñ¶OèU1èÍýVÂ\x0006ð¶\x0002o{Áë\x0007Üâeió°d|Î\x000e¾\x0018CÞUè]/zõàH×êÜ\x001eÚ\x001b"Ù>\x0013c×ÞWgÖ÷Y7\x000eÏ\x001d\x0001½ätàôý!³-è«µ÷½÷¥Å\x0011HYêiÝiøHrbÞ¡Z÷Ð»îàv³Ioâ.\x0012zUÌK;TäCµì¡wÙÙ0ÆnÜÓjÃÐk>Vë\x001e»×Ýæ!y¸î¯y¯\x001cû$à\x0012\x000eE_-|ì]xD%¡KÓdû§\x001d#z;ô®\x0001kcÞ÷¢×%<oè¹\x001e_`}Yû#\x0019)ëÑK13»EóRpvJ\x001e¹\x001eÙ/1GÞu¶À·5ünÙ	Å\x0019×Ý*oØ¾1G²ï7 5zÙ>¨bà¨Ò\x000bÎ\x001bÏ¯ÝHÉµW"»Ý\x0012X|Éð
6sÎðK\x000cGÝ\x001f	Ù¾^ün·$XJÞ\x0003ôc½Å6>g³\x0001~íÈn¿$È<ç\x000bíKÇ7¶Äþäem_¯~¯g\x0002vLn¢h´ôEr\x001fi(HS/½é^z¿ã\x0007ÙYµ\x0019½æ?\x0012íÞ\x0002¾^ø^§ÊE\x001a«cÆlcWâJ
½sj¯JöºU\x0008×D£yçØÄC=ZYö²×¶÷\x0018¢0 ÷8&1Á\x000fQò;Ïrw¥5ðkKMöj`\x0010£}Æù7â	3åüÇõèUmë¨^[ÇK'\x000eàë¦Ã\x001a->'Ëy1RôUmë¨^[ÇëX²XàGÃ	ò%OÑ²£êð«ê¿zå9 bqP"§Yªª¸\}º\x0006þ,\x0004Ûkìx­Jö\x0016üh#Áç@ 7C#Èª6\x0017T¯¹\x0000'ó·01Z\x0017\x0004i
|9Tök«zU.\x0018åâÅÃ
ªÜ<úHë\x0006øu<Jõ\x0006¤¼õè\x0019"|\x0013à
%áázpñ\x000c
ë¨Zk©n­ee\x001e9«O3\x0010¾äì\x0004\x0015\x001eÝ:*¥zÃR\x001e\x0013³ÒÅ',27ál]\x0017ýXøõê÷\x0006¦À¸aG\x0005eßr\x0002\x0008ÏPÙ¯cSª78ðÉb38Uó\x001b\x0004\x0019û`MtTôì\x0005¥û	\x0005ÜHð±z3\x0007Hc_ÅÙ#¥R\x001bà×\x0017§î¾8½%_%\x0015)èðÓ3f¤µ¬k_E÷ú*Arë\x000bÏ¢\x00135\x001bû^é¡k_¿¡èÞG(ìNÁÙ\x0016¹E\x0015\x0018<v¬ê\]+-Ý­´à®$OQGÏ\x0001à84è\x001bºúµÒÒÝJ+\x0018ÎÕQ±§\x0018<_©j`\x001c|S[û¦ÛÚ\x000fã;Ú+Nà
^ó½#Ì ðLU±Ð&¨õ:ôÃþäÇý\x0015mQ$ åd\x000b\x0005$;Á\x0011zÛT§ñüôäÇÓçG»£0üXÁð\x0016¬r\x0015¨\ZüXJ5ì±\x0000Õ\x0016üÓ¸8.¿è%\x0006g¾9U¤\x0019 XåÀE\x0003V\x001fy\x0001ÝD`&?½\x0002\x0014@æ\x0000\x000569ÁßEZ½V\x00108\H NÝ"B
ËÓ\x000exÏ' *öÖ­ô	é%\x0000;@i;*Jö×S¢\x0014Ø±¶­	Øn\x0002\x0011ß³ò!¶\x001d\x000bWh`\x0002£Ï@¬	Ä^\x0002°ìô¾¢\)½Nw& 
ÆÚ	¨z\x0007Tï\x000eD\x0011Pï&\x00022¢6Î\x0006\x0010ça\x0018§ÇÐ4Ó\x0017	¸N\x0002 .H"½Ë3Q\x0015\x0002Ç'çl àk\x0002¾{\x0007"{/Ò¹\ÛvD\x0008ËË\x0012fÍ\x0002YÖì3àøW4yMg_xuS{\x0013~aÞÔI§Â<ªZ[&'¯~ýðËuê/ÒAhY\x0013P\x0014®Î<Ú6LTHÿ÷É«?=÷êõQ{.óP\x0015\x000f5\x0007¬<ðàTHë\x000f<\x0016ýõ<tÅC\x000fàò¯³^ÀÀ\x0016Uâ\x0004Bâa(¶Í<&®1\x0006-í\x0008\x001eS7à\x001csÙS\&\x0017\x0018ÏcÎÇ
±«º,\x000f\x001b6Ò-\x000b6XôÔÖ\x0013QÕH5bG\x0014XªyCprJ bWGÚ"6<­çQ\x001f\x00109äh³6Äí\x0014Õ0:nÀ,ÄúíDê
Ñ#6ÄÑÌQ2¡óK½+o6 c_áÔ']\x000e9êøø$éÊr¥ÝI¬§¿õDl-Yvdyv¬4¬\x000ba$KÖrLi=P\x0013	\x0003\x0018°\x000c)³\x001e$\x001dl«¸\x0018)Æ#õ<ÛÔ¢\x0015F\x0016Üàä\x0000«-	»8:r<X³\x0003X\x0018l¯E\x0007\x0004óºèÆ\x0012\?\x001bÃª¼­D¢«D7Ü§\x000flt±Ë!\x0014§û½»G|SçYÀÎÏª÷WÏº\x0000\x0015S\´\x0017\x001e»\x0013a[(l	Em m	|,\x000e¾ ðÓ =×u§Õà\x0001q>Ö\x001a[NÚÝPA-Î>k)ÃnÅnUÝª>ì>PÀÆ·£1#^\x001b¢0G^97`75vÓ=Û²\x0006ôN\x000e¸"xËm´Í©È\x001bÀÛ\x001a¼í\x0002FkÎ­0\x0002\x0007½¤öÚÔØ/ÐTRÛÜWgÕú¾³j\x001c½ëhé
\x001d\x0016¼ÇÐÔ\x0018§\x0001¼QoòèçÃ/x\x0008t\x0006z¯¿=yüé}ó\x000c\x0018	·~®Ú0øÄcsÌÐÓl4²¡vÿ"µ`ÿîäñËgøµªðkÕ?Zza3
\x0008Oø=\x0011@G{(iB\¥iÃM\x0004À¾Î!ðWy\x000eð\x0019I]eÁk¸sÖ\x0010°¶"`m'\x0001ø\x000bñ²A\x0002\x0012c3Y\x0014\x0015ÖFy$-g\x0013|_	õ\x0002$<Äc\x0013b|/Lð¹±\x0015àoÐWk\x0008\x0004ã¦\x0004ðk\x000f\x0001\x0019]¤\x001e:
K\x0008°\x0014ûuG0X¢yó¿n÷_RçäÃF\x001fH¿í¦ì749ÌvÌÒ¤#oÇ\x0011sz+ß ò-ñPIM;èGõ»Ã\x000f×¿~|ßªÑô;gHåÉ:ò¬{cCË£Ï\x000fg|ñl\x0011u¨PÍ¨\x0015dAH)\x000cµ5\x000bI{B­ÞËPKY¡²c±\x0005?Há|®\x0000ØÁÐ@\x0019#ç´Á®\x0017[ö¬¶çÀ©\x0004ßFÇIìZaã\x000fP«z±ÕöÅ\x0006\x0003A+"¸¸;H;­DI×Â65lÓ\x0001Û\x001aª	\x0016ø££\x0003))íÛiÑô\x0006Ø\x0006»\x0011Õ##\x000bàEDó^ÒjsKåd\x000f­­U\x0005[«\x000eØ[´à(r\x001b¤
T	ì:2:o-l_Ãö\x001d° Öm8EìH.×wêXü%h3í\x0007×l§²
t:w\x0006\x0001	¡Þ\x001aYÓ¼\x0002§0¨9
u-!¦CB\x0002¶Ðõ´Ô6ÇÄ\x0001¶¢¬>Xì¦Î°ëÅV\x001díLä\x0008r­ó-"#Õç;=\x0012u-×¦C®ñ¤ip\x0006
µDÒ\x0017\x0019ÑMI@M°§¾\x0005ÚP~ûb{ih<\x0008*æ dé
3Á\x0006¿uØíj\x0019q\x001d2âÁ\x001cÑ$ÚX¦@3\x0016í'}SëÍ6Øº­·Ãvóû\x0001¶ÏÓc\x0000¶µ$$r\x001cj/*Ñöb»hÛhwtc\x001bzÈÁ±\x0010E²eSÏÇ%ÔÚÌâÓÚÌâÓ\x0007;ã¨\x0016-e\x0003D"È\x0002\x000cþÈÄ¾m0°²"ae7	+\\x001a&¥I×\x000b\x0019=\x0004Óq$dòx&$¤~T[³\x001bfþ`\x001b9î>aã:Ñ;îË\x001d\SvÒtøÏ\x0012\x0001]\x0011Ðý\x0004J$¸¥§;:áÔ7¦Éº]ÃÀV\x000cl?\x0003-Ùr\x001b\x0004Ï}ª
¥CíµÀäÁ\x0006³\x001bm7\x0001[\x001aZF\x0016 ^~Ù\x0010@]ÞWËïG\x0008\x0010w%.ç·¥å?ôTl±"×0\x0008Õúþõ?´å\x000c^,a\x000f¸P\x0001~nÑ\x0004+\x0018ÈÙ-4à\x001aÒ|\x0006le¬Ä¡Å¾hQ\x0007«(é¦ äN\x0010\x0005|ÔáPÃÝès,ëHößDª¤TX-8¥ÂáD/*Q\x000fs°­ç	Û[(h~NP&*I\x00148 æ½82 ~\x0013i\x001br 0kC¾æ\x001enÆ\x001ev¡´\x0008ýhqYÖPÐ5\x0005ÝM!:\x001ez\x0006S{\x0019W*¿Â\x001e!Û(Øí¦\x0000\x0006¦ºMsè¦\x000f»0úFªRçõ<u~^æKÕ\x0008\x001fgñRå\x001c8+5ª5êWmBðqÖ.ã\ºò»Ç©V\x0006z^{­©özâ$Wno®]\x0004\x0019¢\x001aH\x0011°\x000c/QJp&/­%Fõ
ÿÃ//Î\x001c÷r5\x0015\x0001kú\x0008(\x0011¸DDÐp>¿\x000f*©9\x0019[r\x001b\x0001/j8Àôð\x000b\x001ce:ÿäúíMûâc×fj;\x0010¥a¿ ÏèQ'Ha\x001aÁ«'gß7\x0000ª\x0002®:ÛÀ=¢´Åª6´èØëÿ£î]ó8<ßWÁî¬\x000e,î\x0017Ã
¤ 
c Á\x0006AZWmdD.PFªU¿Fog5u^£Þ¤ä¸G¸ÇBæ\x0017\x0019ÖBµÍ \x0008ÖE¿»ûß\x001cËVp[Û5S®
§\x0001âs2oXn+m\x0014\x001b¬ vòP5Sî-?KSòISu"×b&Ãw9¹®æ\¯s,mÏ\x001e\x000c¾>dmq\x0003¬ \x0006¡ÜTäf
¹-­?ðmº6;CáÂ¶fÍÜ¶â¶«f\\x0016\x0015®h%W¥9OÒøÞ³å*w\x0015¹[»?³P­ÿácñXfÜ·´6m\x0006÷\x0015¸_7åÝ«h,kþ{eyÊ[úó4Ç<®rMÛS\x000b]J\x0018aÎi±¨M\x000f\x00169:ÌWæêØåìDa4×ÓuO'\x001b®J^TzlöìÐ\x000f\x000b°ä%-\x0017Oº+ØThÃ«_Ö;T®Û¢`«kBÇx`ä\x0014\x001f.±%¤Ö^ïQ¹nÂ¢èt\x0001§©2©Ð\x0012ÖKKbG3úP¥J\x0012RzÐ\x0003Íz¤tT[I¶¢Ú¼ô°vÒ³*¡¢HBºÒ\x001f\x001c¥·C¯4\x0015UÖTü×0su=ézÝ¤\x001bG\x001d×0¦´}ÈmpL\x001bÈ%¾\ùadÀøß\x0015Õ¿üq÷Ë®=gØ
Rá\x001410\x0006æ¬jz¶Ò¦)çüâôèå7§\x001fN\x000fâPá°\x0012_ó»':¤&¿{*ÏéLàw4\x0016¤·ÑÇapÌÄ:8¶\x001eÑË>\Lüin\x0008{µ©óZ;¾¯&?þNÏ`\x0019¾p´äD\x0000 æÙßmj1 \x0017àÇzö§+´\x0010\x001f«	_:Já\x0003Ë\x0017iÓ°\x001eãjòÓï«ð1\x0017\x0012\x0015TÈU¨!Õ»æÉ\x0017M	Oíøfÿ;E¥³¯(,\x000c³¯³\x001fàK>xdlj¤ÜÎoGü¿SYÈÝ9ODñÁ\x0015%+gS|gk|·rñXb2µPÌøôÈ\x0006øM©íüa4ýë\x000e~°{="Q-æå#\à¤(¯·£Gö¥\x0019%<?\x001e½»yx\x0000¼ûO?4ò\x000b/\x000c÷Y¾Cúu°åü°ßAþ÷GïÎ®®`\x0014o^\x001d\x001aÕÕ\x0000¬^9\x0000)9Dj\x0004Ñ\x0013\x000c+×'Û\x0003¸d\x0000~X­£O|]­³|\x0000&H\x000cìe¯PW¾ û³¶áò]2 «\x0001\x0004¹r\x0000\x0016½\x0014C¶¾Ì\x00063\x001aøÅìlÐ£ZÄïj~·\x001fn-EAVÍï9AEJ¶\x0008
ýCàÇzúãêéÇ@~Lâ	©ËJ¦o1\x0017ñë_¯å÷\¤¯\x000chJ$~gi\x0003ëØP*»h\x0000õ\x0006k7°\x0001ßÓ\x0000%·\x000b±ÉK7
=\\x0017ðÁVñ§ßW\x000e ò
RàBzú\x0002\x0014å®Å¶#£\x0011¬Þ\x0003p	äl#
ö\x001a¥êÀÒwt\x0006ißà-\x001a\x001a@­\x001c\x0001¶JÊÊ3HQM°\x000c/"ÝTò¸`\x0004v4\x0002»v\x0004V°"&­ñ1j,\x0017m¶²å\x0005#ð£\x0011¬ÝÈÎ²\x000fl,ß pÐÊÌt®ê\x0019\x001cmd¹v#»`È\x0015Ã¬;zØ\x000f\x0016\x000f\x0008\x001a@Séû\x00116²\»1Iâø	$³qC\x001cöÆ\x0016 F\x0010WÀ\x001b\x0014KH#Ð¼y\x0018\x0001ç«eÚP%±d\x0004Ã<x\x001cA\x0008ß5\x0002Ø½¹ì\x0014þÏæòq\x001f D©`â@y×\x0008Lý
F
\x0010\x001d#ÀÝ\x0007M\x001eh\x0011Á5\x0007`åLcì®\x0001¸Ñ'p«?AÈuMZûe é\x000bH*3\x000c
ùïðý\x0008ß¯Å\x000fÉð
¦¾©Áá+ñ;±­=¡FN±Zí\x0015{K2ëÚ(~3\x0001ð\x0016°¾!KmÙ\x0008F[ ¬Ý\x0002ÎQ66è9ÚÄì\x0016[»U-R\x0003Õ¡Dª<©úB½½ýÔ\x001aOAw:gÖé¬K)è\x0002mÝÒ½ðíù°C¥Q/û%°Î²,\x0017õÜÜhVó6-ý°[xu5¹ºwrå^ß*º]±\x001cõ÷CKï\x0016^Sñ^^X\x0004i)Eé\x0017`ÔõÜ»Ä"^_ñú^^¸wâ^_\x00142S¿VÒi3
Í%x«õë»×¯äN³*DNÆ
»>Z5\x0013;XÄ\x001b«ùÝókJ\x0003\x0006°Õ5÷ûâ~Ü¶¥Ëc\x0013n5½±wz­+ÓëÅ~z%o7ÙÒ
·WÎÞîÃ\x0017\8Mó\x000bSM©\x0012AqW#1±MëóAv\x001f\x0010ÆSèQÁËÔ¨êHùðÆ\x001fÖÐnãu5¯ëæ5Ük\x0012y%M°4¦\x0000o´"B
\x001cºÄ¬\x000cáy¹\x001b²Ñ-\x001dê\x001ax+±ÉqSÏE¼b/Í?h'é4ÿL4w	°®·îÞr`^Òû\x0008¢4çà¡×¦¥op\x000b°­m7°áÚV\x0001ìdó`À6\x0003«ØÒo´\x0005ØUpÝwk\x0011°ÇF1	XR÷ÃQ\x001dø¯·ôùk\x0001®÷îÞsJó\x001aÿÑ}CZºIZÂ;ìM%Æ½©\x0016ñr\x0017N|+Ç\x0008ZâõÜ½XÍ¼.â­\x000faÓ}\x0008ú\x001d\x0019\x0011=ãZÞq8éðz;2Ò:ç\x0017{ºGªèÇ\x000eTÔÜZR-¶Úo³ã|¨C7°£\x0017MéÀ\x0004R9¹\x0018m,\x0012\x0004ðÆUÙkVj\x0007\x000er\x0016,SÁ t%òjröëµ·6+{íJ¾PÖ©0ðGÊóCq\x000cìÍ6vp*|úÞkYkãY\x0012\x000cKgEÅM÷
{R\x001c\x00026©áÛ0¢\x001eNÊÛ/ïú®=\x0012n``	l\x000c5X¥.·
{îìèååë\x0017óú·ã&{&7Ùë£V\x0002;òæØ³p¡$Q*~ÉVê°ÿÙL=¹J=)µ£\x000bZ\x000b¿OýÔk\x0011´Ú:VÔq
µ/y':#µã´rÕÒ
£ZªZªuØ¹\x0018LÖÈ­.\x0019å3Õ\x0013K©]½®Ý]\x0014³àÈ\x000b,\x0008Ë"AÁ!½\x0019µ¯çÚ¯k]\x0012cPGÛÐ\`*Vï5Èö·a\x000f%%\x0001[É\x0015Ø¸é\x0019TÈ\x001ce\x0001l\x001b\x0018ÛÌÀ-Å®g[­ml·ü´­9\x0011&\x001eö­\x001b±Áä­¶Wýk\x001b\x000cVË6\x0016¹òH/ÿQ\x001d6G[±©±Ym¹\x001bîØæ¬e\x000bTÊåáØw#·\x00125wú½\x001b#\x001aé\x00004ÆÚñð\x0018©ïXÊíFÜ+@\x0005w{N5VÅ\x001c(Àù¦w\x0011ÖùVË[U\x0015Èí×­\x0013CØ:·ÛDlz\x000e0í¦;°Ã\x001alÇm3PvºlÂ\x001f\x0003O÷Ë$¸ã:îü\x0004a°«'lª\x0001v»M9ìùoþ³;¥Ûø²J,-nm\x0018[Ï¼V.å®Ïn%×Ý°)UnÕ`á²'Ó\x00156%¯\x0012;óÔÎ-ÅèÍ\x0012n÷ZÒçëûO_v­îÒ(C5îBfY\x0000÷'-nøcSS¯/ß\ÎùdÛTÜf\x0005·ÁÚª\x001c{\x000c¨Ïn\x0017%÷	[rûÛ¯á\x0016¥k;ÜìÜ®ÔQC\x000fßTßs\x0010Úø±/éG¾ä»/7»Çïî\x001f\x001fZÓ\x0008¤+ÊÑ©<<wÇ­$Ào:¾¿9½>;}ÿâòýÕl&\x001f-søÇ©Õ#\x0000NzÓò:f×ÁG/TéO:\x000cÔ7a¯ö}\x0005´i\x0004*Õ¾|	\x0019AÏ¾\x0001Øj\x0000võ\x0000:ù\x000eßè\x000bXY¾Àm×\x0000*Ùýå\x0011À\x0014*ÏM\x0019ò+M\x0019BÛ."9\x001eÂê1(¸BIEXv¬a\x001f\x001aÿû\x001b\x000fA°v'(p£©RRE©i\x0008ÿa\x00083'iß\x0010Ìh\x0008fõ\x0010À¼!Å\x0010\x0019¸ÒÖòf\x000e"¹d\x000eÁ°v;+­5
Äg\x0005+EÍ
oápøAmá\x0018\}«BI]cY¥\x001f\x0010¹äÖHõ\x0002"Î\x0008ôv
¡ÊÒõ¥»n\x0008TÄÀÁ¢Ð3,j!çJ6ú\x00060²,ÔZÛ\x0002+ÜX"62i\x000c\x000b¤\x0014-±È%c°£1ØõcÐq/´Ê\x0002«8\x0006j\x001a\x0013d°\x001b_\x000cnt$¹ÕGqâØSlUqDØcÙ\x0018Õï\x001dÎRZ8Ñgp«?	®Dµ\x001dÉÀ\x0018B©Aÿ·ñ\x0018üè3øµ\x0001ì!.\x001cÀ:>rn\x0002ÿ(Z¼ñ\x000e#\x0013#¬61Pô-{\x000bhlS-8KYIÇ¦7\x0005c£Ý\x0010Wï\x0006\x000f\x000e1ikiGKáJ5ÛØÔSÖUcH¿¯\x001a\x0003¶\x0003§\x0001y¾ù>D\x001eI_ï\x001aC¬¯·ôûª1¤Î\x001a\x0006[M>³Â×<\x0006ô6\x001e\x001cA®\x001e\x0003L>=IxØÒùÙJ\x000bC	 !`¿«mÇ FcX»§±jrnÓ\x0018r3X]\x00178Í lµì\x00007\x001cu#yøç?¾ÿq÷ðé658lÛ\x000eÆsÂ39\x0011v ¤K\x0007\x000etS+«3\x0018ÆÕó³«CC\x0018êQÁ\x0010j=ª®!\x001dAa]	Î\x0002·\x0002t\x001e·\°mU\x0016ÁVAÙÕ\x0001\x0015Li\x000c®x 2Òä1´Ô5-\x001b«ÇàÖ¡$² "^ÞÐðEèP!´µ­[0X\x000f!®\x001f\x0002xÎg½\x001eY\x0008\hësØ>\x0004­«Ý õêÝ/Ô éÉT\x001a\x0016RÝ°ù\x0018Lõ\x0019´Yý\x00190ëÅ;\x001aá|ÆÆÀchimÞ6\x0004RÂ\x0007á\x0018)O¤®ðêvAvÕ¬xtO©3\x0006\x000cC³î©iÒ??ðì°mm×a\x0007òú±J72¶+ØQÇ:® \x0006§ü\x0002Ôz²9ükäÉöMMî°U½FÔ5")¥Ë\x0018~6°¥³
eÜÌz\x0010o»MÔp\x0012\x000eú» z|¢æì¨\x0018z4aÛ\x001aÛ®À6¢ýãvÌ	ãÆr¾Î\vÔBêaïF|uSýÔÖ\x0006ªÒ©ØÔpEÑ\x0010
r\x000b±EÖï\x001fdÞªª¶öíí÷Í\x000f\x0019JpA\x0007C@±Ä¶â<ÝTÛÿöüåAàayªZª-$öÇ\x000c¬ñ\x0011Ú¶ðóV-¥äMÀÕ\x000cËþ)¶Ü\x001eÁ[,%k$\x0013°mRcj\x0001VÕ\x000c«î\x0019ÖÎ\x000c\x0000.õ0Ø+°\x0010·\x0014»·\x0010»Øu\x0013ãÒÜÎsI4©;4ð\x000e=\x0008aÛ
ì\x001dI\x001c*ìqM·I©Ø@\x001f¢EÏ¡\x0001y(Ç+Fr¼\x000b5áHlø\x0011\x0019\x0003¾áLnCÕ,ëØ=ËA£®wV\x000f\x0016Ü±
\x001bò0rh\x0011Òk@6õilÄ³e\x0019¿­\x000bVe\x001cwf»ûïÿü¯³o\x001e~¹ýçÿ}hí#$`÷q[\x0012¡TN1óh%Ñm¢åL¤q \x001dytööìê\x0003x\x0000³­p\x0014vx{Ç\x0013[ßÞ}£@û.NË¯iÙxg\x001cØ`4é§.\x0018®G¡·\x0018°Ç:\x0000ù(è\x0014÷6:º(¥yÇé\x001aÅP\x0011F\x0011äêQ`t½øÅ©\x0005iÊ´\x0000KEjÄö+Û¢þ\x0016aý·Ð1µ;&Ï8\x001aj\x001dãµå K4ºÅm\x001fE©»{ä\x001b÷
\x0003Ë\x000csâ4NSï\x001e¬.¤\x0011TØvcÈñ!µÁ)¥£wFziN!°T)Gmj!¹`\x0018UÏ¹8RSê\x001dÃgAKÐ0\x001eÏ÷ÎµXiFaâèÆ\x001b\x0002\x000c\x001dª\x0015(»óÀrS\x001442¦)ðÕ>\x000c5Ôæa(e6Øá^\x001bÊ\x0014\x0001\x000e^\x001a\x0006ó`T{Û¡¦h\x001aÝb\x001bÍÊá>üÚé±Ú6¸\x0002ß`ëa>Ýâc`a\x0001ÉÏ\x0015¸a\x0018|Ã×\x0011ýX:\x000cµnX'N\m²¾¸ÿÜh\x0000j\x0014GæXv´,½
\x0007æÃÉ5©W¿¸|7k´¦¨ï°xW¨ZôÿÅÍîñîv×j¹
8z8+5jÌò\¥ÉXKã¨£\x0017g§ï/ÎO\x000f²»a\x001d/åõÚbö\x0010¸>L¢NZdu7\x0016[5M­[ázÛb¤·½\x001c> .\x001aÅÊ\x0002¥¾£\x0016ä¨iÐ¦k\x000fõª	ëVMÔßÄu(bíàæ°. jpÑáå0²
ðr\x0014Z]¾nØSÐ\x000e\x001fÆiÝhî9\x0006^Ã¦ôzD¯×ÑÇSá`ÕË,1ìì \x001f¡%\ÙL\x001fFôaåÜÇc\x001f\x0011|nxèùå£©½K+º©Oôûª7¬d\x0008vgnÐ\x0013ÏÝ;Chzún ·x9U\x001dßÄI]\x001d1ßþó\x001f\x000f»ßZ\x0014\x0001û_IR\x0001£\S\x000fØ¤M
×ïSV2(Ò¿}\x00047ìé\x000eÀÔ#0kGàcu§\x0011HÃÏ})ó#*¹aÏ\x0008ª~^"çO¬þ\x0006¹èSIË\x001aó0\x0002Cv-eï\x000bF \x0007{\x0000F «t¨Þo@a\x0008®¤oàu`H~×\x0008d=\x0002¹~\x0004,í,±?)Eq\x0003\x0007'|v-¶\x001b\x0001üïU#H¿¯\x001a\x0002#\x0007ÃtY(zÀ.\x0010R'8,u´h\x0008ÆÖ\x001bÁØ;!Y4\x00040øóE\x0000æ¦`m\x001e°\x001aj(\x000cÁ×_Áøµ_!\x001aÁyD\x0003Õ8\x0004n¹\x0003+©!CsÑ\x0010F_Á¯þ
\x000eÓÐÒ\x0008Àÿô\x0011\x000cwüòbæ¹g\x0004v´\x0015ìê­\x0010Á ÈY	R;Ui\x0008\x001a:çå¶[ÁÆÑ\x0010âÊ!ÀlsDõÞ\\x0016uÎrr¦sYÏ\x0010\})¤ß×\x000e!rf#PS.Üükîa¬k\x0004v4\x0002»z\x0004°óµ¦¤¦:\x0016Ø\x0014t­¹T\x0002¾é\x0008FÇ[{\x001cÁ\x0008\x001cu\x001f`ÉQÞ>
s±¸ÕÆ\x0007ª\x001bm\x0004·~# \x0006¥¤\x0011ø,à#àäR«\x000eËs-\x001a\x001fm\x0004¿v#¨\x00083o©}(üOT*<pà.oû\x0011üh#øõ\x001b\x0001\b\x0012Íp\x001aiú\x0008d¡Â_·\x0008µ@Åoë\x0006î¸|+÷òÃí/í©©\x0016\x001bT\x0010vyòµæ~\x000bsºÌ{\x000fíÃù\x0003È=,\x001eJÜýà)«Ú\x0014¹4Êæu®HxVâ­Ü£ù^1áZe£!Û;ì\uÖô´t\x0010\`êk¥ÝmOêg\x0017·?<Þ|iuåQ\x0007ô\x001b¤tÜVAJËzÍ¢i¡¼8õþìú\x0010·\x000f\x0015·\x000f+À±\4g%Iã\x001d7\x0019Ä\x00177~Ëó-\x0013Þ\x0006>¬Ë\x0002ð ÖÇÃi\x001eé];\x0008{\x0003S¹¡«T;·­¹í
nïù4ÔÎóJ\x0001G+0xSÌ§ÛÖóm×Ì··\x0008çÛpVXÍîU[\x001eA\x0013¸¬dê±R&®q|çÍAqL=[ ¦9®1FØ\x0004>tk\x0011ÜØ\x0015àÞ\x0014OÄyEÏp`Ä{N\x0017¶åMô ¹qßôU\Js<ÿéçÝçÏ7Goo>}¼¼»ýÔt\x0002ÃV!\x0010µa\x001dW£-ÇtäLHùüõÛÓwïÎà²óÕåûó7³Ïn]Uìj\x001d;vmt\x0014òÇ6GsÀ¹g\x0019p3#GÖÁ®+v½Ý\x0015Aå¨\x0003Õ\x0012»)
Ûs\x0011Ù\x000evS±ó^Z¸À\x0001@ÑpwFÓè@·\x0015º]\x001e\x001b£be\x0013\x0002/\x00197ã­v°=¬b·<öTE*\x0003+ª÷3¦b\x0007ûðÜ%k\x0005»\x001c¾Çfç\Õ Kà5l»Uc5ïqår·%Gr¯?e\x001c÷k1£Í½½RÝqY8hÅÄ[]z;xA}è¢åÞà^ëôÔ\x000ex]ÃëuðË3À\x0007\x0007*;â6\x000fZùi\x000b¬ÝÔìf\x001d;Ü¦¦\x001a9¥%ZcJS4©Eð:ée
\x0012Öð>¯ÓYn`\x000c­Æ\x000cøpù$¾ÓRs\x0002\x000c{í	¿8\x0011Ì\x00193[
\x000c\x0002àVu\x000fÛeà6J\x0001Hp¹õüÂ¦¬Û\x000e|è!\x0001xP+f\\x0019nú*mpl\x000cHG¾´ÃN,[qG[qG»[³¶DÓz5IÃ\x000f9¡¡±\x001bëÜé÷^p\x0011r\x0017§0R`\x001b¹v×¨\x0019AàÊÔàé÷np8ñ¨'ÀDëÜ\x0003
åÉ\x0019\x0005à"mÍa,\x0004¯|Ò?îþ¾»kãÖØ°Î\x0014¸N¹\x0018ÓëP*Qiÿ°ôòÓ?^\x001c\x0006·5¸]\x0007.è­Ò\x0005j\x0007àì6%É5rÛzÂíª	7¸:\x0012·utï\x0003·¦-AÎtÍZ\x000e^O¸]5á\x001b¡` 7\x0017H{n\x0007\x0008ÜMeÝ­\x000bE|ûÝíçñ*Ç¿êÆ\x0007g.·ã(\x0008åiÞ½ãõbf\x001aÏ,àWcSQ©¸\x0007¿Ú}×|²\x0018@ä:&Ò)\x0003Ü¢ß\x00047P\x000bõÕéËÙs%Q\x000fÏ\x0015 \x001e+\x000b©Q";C+/òÛqYçâ.Ü¶æ¶k¸ \x0018v"E1\x0012¸áÞ.Î5Õ\x0002´ëzèUËD³t½¶ÁJ6J\x0010·éî²[×Üz
·t¤î­-JñØÌ--¥NÂWhÉ0o\x0004¯W¸^µÂ³ò{\x0002ÇÔ\x001f\x0002/
<ÑoZ\x000c^/q½f£
<e9Oºä_ÕõM\x0017P\x0013w%ý[3%^é}%pù¯\x0002®Fàÿ\x0002\x001cGB¥\x001bIÁßí¾¾yø©ÕÉW¾Fâj\x0002#\Y\x0002Õ³½t
Z\x000cgG\x0017§G_]½óñÅø\x001c\x0017¿;ÇÁNùôåæç\x000f·¿¶\x000e\x0000[¡e¥Aé]\x0011|4ÜÄÃl5Úåo®±öæ««ó?8\x000c[\x000fãwfnÇ0`ò©è\x0014¦?\x0017Ð$\x001fê±âbóQ\x000cKB`\x0014~ló.\x001f+ëPÆ¤+\x0017?FÓ>X6P°þc`þåjlkgñ¹×ó×
\x0005Q\x000b\x0011Uõ5¢Zÿ5Ô>g^æ¶NyMñë\x0012l\x0016Û²u\x0018ZBZKüÿüøðeN\x001c\x0017ÿjÔºËÆ1\x0016e³É\x0013j\x0003ÿüþêz>E#¡\x000feà#Ù¦¥èÂp×2\x000f[;æD$\x001b¨¦.ø Zæ¾\x0015ÝÖèv
ºÈMì\x0013:¬~Ê±íµ\x0014ªåà¡\x0006\x000f«À½¦õÅú¼\¬¡\x0001ÏôY®ëå¢W-\x0017a"õ¥\x0002/Öå\x0016ìÎÕ!è&\x001b¹\x0011}X[\x0004t£Ò¢ÅèÎ¤M)Ü
\x0017\x0000z®L;ºªÑÕ*tíH;\x001d\x0018Ã±¤lÁÈ=ú0Il\x0013tc¾\x001dµU5'\x0017= ¿Øý¶àåÝPÓL|ìåöì_óB	\x0019ð»L2Úþ4û¢j¾&)hõBcf&5ÿ0ß~¥zWä?ü~ÚL]Í´\1Õ`ÅP±3ûÞ\x0018>\x000b}°3\x0002K©U5×jÅ\@±\x0019 NQ<×Üo\x0008\×Ã©\x0019ÍÔÕ\«5ËZÓËr)h9\x0019Æ2µ8üÐÛJ­«¹ÖkÖu ÂJR^Óò P,>q\x0018Y§TãAò\x000e,?]?3Þß~\x0006òÏG_ßÞÝ-èö	\x0006VN&c¼4PBr«cø_hy¹<\x0007ÃxwôõùÅÅ¬`\x001eÉ /\x0003F2\x0016.è\x001bIÔ,cÎ»\x000bh]p.oK{°%\x0003Qcõ;U«ßÝ\x001c½¹yø¥¹¬\x000f\x0014JH°âIéÓJNQMî³«\x000f³)ë	ÚWÐ~\x0005´0\BJ°`âÌ;Õ$ZÕD-]E-]?¶ÁgÇü \x0016¼-	®<¶
Û\x000c;ÔØa\x0005¶ü\x001eí\x0006ùx\x0014çØö\x001cÖHmkj»b²KUL\x0008{jÉ]û¤k\x0012[8­ÃèPO¨:W^<Ü|þ|{óØîE\x0007Å¹Q\x0017/\x001aîR:#eKº}9Z^\½{w~ö~ÖN£1ÕhÌF£,ö§¢aíulm\x001ay4M\x001a\x0007c«ÁØm\x0006£±p¯h:Ó)\x0006pF,¸¼\x0016ÅUcq\x001b}\x0018Ô²ÉÖO´\x0011ûð¤Ñ\x0008^e
á®±Øj,O\x0019\x0015\x001dc\x0001\x0007ú]F0êB\x001e\x0017j\x0010Øê\x0019M¬¾ÌEÇh°·\x0019©\x000cEKEºÂðå\x001c0CqãÑH?ò½à_¿«Üí^=ì>ýpóåK³<#\x001eÀ,\x001d£\x0004Æ\x001bj\x001cØË6¯ý¯®Nß¼:»¾ÕÚò#w\x001d½\x000fµ~\x0010]_Z¢
¹I\x0015\x000c\x0012Í"ì&í¶%c\x0018¶°1øñKÇ\x0018\x0002éÈ\x0018X¨¬ý\x0004ÿ-EMòI\x0010a\x0014h\x0013a\x001ch{yß\x000c/aå#/óä\ÈAY;-QåËYhBûÃ8Ëú\x001fÃ¼³võ\x001bÃ­
{\Àe)ºælh8Igsº7ØÈØÈnbëIi\x0011}°ãè21\x001b{z®÷Ô2âA¢9\x0012GÛK¬\x000c\x001fBe\x0001ÄÒ²\x0010o[^ß,°\x001d[yvlåíîv¿Ý?¶[§5±=\x001c9\x0012|ÒÙÇ&êSpà/ßÏ\x001d$©'ÓP¬Öb\x0013ÑÑAòòÇÝ/í$ãGDl.eHûz&:íÚ\x0014Oñ}çÃì!\x0000UìÊ­bGÝlÂB·¹1ÜN´T\x001c«oÃ®Çnº\x001e¹éÁ.¸ùÔ\x001egÐÁP\x0008\x0015¥?¦ÞéÆqÏ÷ \x001b¼°w`\x000c½\x000f¨Ql
ÁíZp²/Ë^/s×ß(\x001a"\x000cÍà¦q³fÆ
öÚ\x0011¸)ÍA\x001d]Ø(·á²l&·ÕÛ5S§¥\x0016¿RpPÊK\x0016»\x0013¾%\x0013´\aHsØ\x001bWaø¸n®tûýß\x001ew\x0013ã}(UÚ
öÛC©\x0007u¡)Hòöüå¿½?}3[\x0011Zæ\x000cl,8·¯n¡\x000f÷é\x0015ünAhVÀð¥Ñ\x0014\`LlñÜ_^]¾£wð\x0003qZ%Æ*1T½Þ=üp{ww{óÐ¼´U\x001cgÓ(Õ~1Â
Í&Î^^½:¿¸@mÙ¹Ådìø\x0005ÅV/(¯o\x001fvßÝ4¦\x0013\x001bá¢æn¦05¹ó!òù5Y\x0019ïCä¯Ï¯N_Íe\x0013gêá\x000b­^PR\x001b*Ð`ØR!N(/(\x0005xø-â\x0010õwô\x0006^Öþô\x0006Ö~ß·Ñ\x001dÓµê\x0003×ÚÀÊjr¶àjï
Ôd¨È­Æ­ô^Ý?.éß&)XFÃZÞ_=*%6,ìWï\x000f¶#tø\x001f\x001e¡ÃÎü¼ûÔ\\x001e§3n\x000eö\x000c%@£Ì:·Í\x0013]ªvå»Ó7oÎN¾ß}Ü}þòpSþPÃ\x000f=\x000b<Àä*ø(\x0004VçÈ:9Z°9 [üÏftU£«uè{\x001bÁ&4E¸.²= }S!N\x0003¼Îk|`ÊèQÂgðúîf· diÃ±Ì®?VCÛ\x001c´t¤ÝõÄMÆÌËË×(Åúï\x0007éuM¯×ÒG¬aEzcI\x0015éiÃâcmá¾\x0000ßÔøf\x001d¾22\x001f\x0006ß¤\x0010+UB¡vÁ\x0016¯¾ÝÝØûßþF¾jòP/`ß?ä!5BýNCL8M´È\x000fT\x0016kÑàuøiaÎñÍäwG§:¹U}y5}\x0010\x000eÁÐ*qÁ¬Jµ*65õÆjZ\x0004\x0018\x0011M`âd¥`ø\x001eé\x0017\x0005:-gå$`ç<ä%2-hVI<qÓ%hR \x000c"4ø®Ìax$=¡ð¸ÌähÂ22,°#0o\x000fH\x001eìÎKÉ0~,"Ótý­V(\x0014>§WRÑ\x000epð·kÑRz§Zº7¥\x0011e\x0013ZÐ¹(\x001ef
»ze4ýÄ3ìR4|\x001eK?\x0016¡IÚÐ%4\x0017²À4|Eì¦H³öDTe1=ÉÕËÐ¼¦Ca\3\x001f\x001c1\x0016'2©ï\x0003,$KIøzù¤\x0005Û :\x0016ù°\x0005+Î4'ÖÏ_~,BS¨ÆHhÚ\x001eë´	ÀÀ$2\x001b\x00101XHº~¥\x001fÈ°×\x001cbIGN\x0006lNÄ¥.åÂ>ýXÈ%1Y?£é¬_høHÑ/C\x001e!òÏ\x000bM¦\x001e¢ùRÖm>l±1"ûôù\x001f\x0004ú_Y¥oo~{Ø}ÿã®é8Cyµt;©\x0018<ÜåK@Óº=ÅõöìOW§à*NNØ\x001e+ÝâùqáYa#\x0017~Ægø\x001dqÉgÃõÛÝ­»O\x00179^I)\x001dòþî\x000e_b?·¨¢r¿á2»2pÚ+/r¯ªîD²\x0017\x0017øè:\x0015C\x001b¢¡\x001b¯-C\x000b¹!£	Ëh± =mþ,AC\x001b;ýx~³oÓùúÙ¡¡)V=7´Ôú<÷?vh\x0018ÑÌåÏ\x000e
~Nk-~üíþo\x000fÃûéòîöÝ&ÑDÕ\x0002Ë/C²\x0004>½§Ó\x0016\x001f\x0010Äº¼8ÿp:õH3dbïü91ávÄÿÿ¤H6Ïó¨}\x0000ãYAqìâúÛããÇ»ïÀÆO9dùçW»Ô\x0005ò U\x0012pMP\x001eãwÉÒñ1Zº´2Oû¸_^Mw{Tßþ\x001a¿ûËçÊþúp»;ºúñþS\x0001êO6P\.½\x001d:\x001f\x000cMU|*y\x0019©>\x001e]}sùfÚ\x0000Ûñ\x0006\\x0006]\x001eb\x0002ÃdÄ\x001c²óQ\x0008²\x000c£rO\x0007\x0013\x0017í·á24O}®`ÎÍ\x0002N0g.\x001bx6^Jî^ú±,
Ï1§MN¬u(FÑ§¨ÐYwNú±\x000cMÉc"KoL[
ÙÅ§tÝá=~,#3ÉËMB\x000cer3ÙDhx	X	s.\x0003³1\x0001YP¹ú
È02'Þõ\x0017¢¥4\x0010µx\x000bD/³ô
N\x001aÕâái\x0016ùsº'z+-FCcZ,5\x00170Q/¡ÅýÁ\x0011]µ'Ä\x0019¢á~,5j¤\x000bw\x0000>°¦\x000f\x001a\x0004b|¢n)\x0019\x0019jùÁ\x0011\x000c~ÄL\x0016ó£)IÇ·xâÑt)\x001a*Ñ¤\x001fËÐ¢?vùòxF\x0011\x0002/äÄ£Ò\x00122|éO?)¡4ìÀ §]\x0010ÎK¾Ñ×ï$¬~,#\x001bJåË35ÍÎs&UPöÀíR4/½xÒPø"`¢\x000eñ@'\x000cÛò¬$) ÿ\ùêY¤Ö\x001a¥eî_é¢å\x0007\x0012oì\x0013"\x000b\x000bÙRCµüs\x0019\x001bÊý¦/jàÎÌ¹ÀfÉæðÖ=Ñ\x0000k!O\x000e@ú¹
þ/=Û$åï\x0002ì¸JûÀê'úä´¡ù¿þv0zBíô¾ÿñ¶Å	W:ÚcëRl\x0011£°©ÃÌ²|GYïH\x000cE®«Ë÷/¿9vÁ÷Tì?+ªýñ\x001c°þc÷ó_ÿÆ­°R\x0001Ùë]J]»~¸ùé>K¨\x001d¶¸±`,\x001b)iÖe»6(27lp\x0013Ï#¯OSÎÚõÕÙëËié´\x0001åþzÖ\x001aÍ¢ôã9bÞÛ»·²rcÞÞí>}Ùµ,E	þÕqn[\x0011P)7yïJg{Ü{\x001d^o/Nß\N¯Ä=\x0015~ÞôãYQ¥\x0001<\x0003ªïnÝOþ>x4¼¸ù|t
§I[ü\x0013ßr"qYs\x001f(<\x001a\x001d\x0019+LX\x0017gïNá<îÉ0`ì'\x001ab\x001fZÊð9­åù±á¾ÔÏsÞL²)ç¼óì\x0019²á´ÏM}ºýéóýàl{sÿåáæè«ÝO7G\x001fÿû?ÿëô·\x0016@\x0014µÎöR,\x0001\x0010§çk7Jòæ\x0012®Ï£¯N_Ã£É\x0006¢CJÎxîéC?{LA=&'y<sL¾9&ÆC÷\x0016úØï9uN\x001eV³\x00135¦¶mÂ\x0007Òç={³þsbjMúñÌ9}
¼<{Î}\x000eí3ßHûÚç	ú î?ý`·æËO_\x001e\x001fî?5ÅÛÀÕ£ì\x0012ø¶¹(\x000e³¥éiÔ[7áõ½<{sýþêòM\x0003JÏBÏkÿøø<À~µ÷¿Þ%1\x001el\x001f\x0003ÿïôîîöÓ}K\x0018FX¯ñ\x001d4¥üjMo.NOÏ9¿OHb ÕéÅÅ9¬´ÃP{gïa±÷¼°J\x0000æañãñsÀúôówîcÎ&×p\x0017¤$÷W·ß5\x0005\x001eµP!k3Á¹êEV±F\x0012ÊqøØ7áÕ\x001d½:1\x0013qüù§¿ý\x0014ãð@ýúþáñ'Ò\x001eùfww×£Ýìé K \x0015òà´Ôm)e\x000eÙt¯/¯Þ¿&Ío`\x000e§óuö¤ìôbW?J>·@\x0007R\x0011y*Ã\x0013rÉ½¤\x001c¹ï#\x0005ëÄ\x0012hàÂ\x0006í9ñCø´uÒ\x0003ÊîH\x001f¨\x000cY\x0003>¾H\x0012÷4Ð{®Óq5éí­
ö¡\x000e^\x001e½¸i\x000cÜkØ)¹Ç0¾´\x0019JUÞ\x0008M÷x\x0004ýóâl6d_ÈöI4Ï\x000emÿ6ó\Ð~ú«úUÿe\x0018¤¹@¥£Û¿üåôÞ\x000e§
cW·Iµf9½Á	ih¤'Þ'éPÝèüë¯/fäÝ)1Ä>gB>f/aÙµÏp÷Ëî§_ÿ7:>hì¥\x001fowMû\x0003þH
\x001a¬R!Rfª±VÇòôûôþx{ú~nsì¡ð£¦\x001f<Ôçáâ\x0006ê'âÒ¯v\x001fÉY­Æ¦Né"\x0002»?{\x0012Ö<%\x0008ÇqéW§ï¿\x000eKÿðñöö×ß¢\x0000\x0003Åù×\x001e\x0004¢YÌ\x0013I-E ^\x001d%×Dý´Q0ýþÍÌ»`Ü§Î>oJ´\x0006í¥4\x0014\x0006Ðt,C\x0006Õsh¶ÝÉYRïõl¦ÒÖðlgóö£Îý\x0003öâ\x0015®\x001f\x0007rZ\x0007\x001d0
\x000c÷·\x0013Ô`Ý¡j	¥h¢c5¹¿¯ß\x001fÏRßþ%Ü}ÿÏC?\x0005L·7_n¿\x001c½øç?Z-\x001aø\x0012¹\x0005¯5y\x001c²\x001be(cÙ0­\x0019ñöìúüúY£î?Ë_R	\x001a[éÇëÇû»\x0013\x0012u_LþÌ\x0016|\x0014³"t\x0014;\x000bS)	¯ß_]Nia©o?þõþN§ÃªTx\x0001ßµ-ü#Ë],À°WYMÒE¹\x0012\x001fp¾:ï9\x0013üùôùãO?|JQ©T\x000f\x0002?þ×îîþöSS=\x0008&èû\x0013l*\x0017ÃÜ
k¸\x0000fòé«ä^\O
\x0013¡\x0006\x0014Úÿ\x0005Æ¦^ßúòÏ¤]{÷ßÿù_g?ÜÝ~nóÊW,ºÈ¨OM\x0019é\x001a'Þ»¯/ß\å\x000e&Gg¯.ÎßM0Z
©Õ\x001aj§XYEø\x0015-\x001a[\x000c\x0012õÄ6é¡¶Cj»j®%-4×ä/\x001bÉJ\x0000\x0006Õ
6¢\x0015µ\\x001d°gSÂ\x000e\x000eN\x0007~ì2\x000elRÜâ%"Ö`cw\x001eòùC R\x001eÇ\x0005\x0016Æ=Ñ\x0015¦\x0013ZWÐz\x0015´ÓX)	IÍà\x0010õOtÑìÄ6Õ\x00121«\x0008r°=j´elÁeyñ	yùNl[Í¶]7ÛT¤\x0001]\x001d#q"Í¿\x0007»>FÖÍv¤ª&©\x001cåó\x00025r%SL\x0004;¨]5ÙnÝd\x001bÕ¤æÎ\x00136~VLØ_\x001dØ¾Âöÿ*;2TØa\x001dvÈ]%\x0001Û²7V¥a='ÚJõbWK;¬ZÚ.²9"y;ZÇ\x000bÛ<¡\x0017ÛÇ,U}?ªUÐ^r=+¶\x000fæ§\x0005Ë\x0001{»Ùý(u­×\x001d#\x0001%µ3¶ 5'<G\x0002cOÔ vp×ç\w\x0004Ë\x001a
co9àf°!sO=;ôp×óíVÍ7ê)\x0012õÒå$ñw­ú\x0000ëNÀ(	;ú2ÝÁ³"ßS\x001d%;±ë\x0003P®;\x0001£:v´L£R\x0008à.r}f¢$³;ÖÜñ_»^ÞqÍòvÑÞVVdW<§ÓÐß\x0013ú°U}
ªu§`,l*<%#MÂÂîéGá\x000eèÚÜVëìmX\x0018DO¥¢¹6X3©ý\x0013\x001d\x001d:±ks[­³·cà¹6,nk"Û^lvß¨úüS«Î¿ ¨ïÅæâØ\x0002¹­à°ª×e/w½HüªE\x0012cn+ZÂ¦ø	1ÒÚör3»D×Þ^åÞ\x0004\x0011s»\x0012«ä\x001a6g%\x000b#±ë®ë\x000bG¯ºpÕÇ!G
¶YÉá\x001dëY\x0003Àû'$í\x0017søí¾;Lþôö{uÿøå\x0006;f|¸¹Û5¥BêX\x000eÔÈ=Ù6zÚ;¬F~÷êòýõ\x0019¶Çøpv1	É¬ðHÈá\x001eÖÈ6\x001fÖÇ\x001a\x0014'ïxßBT[¡Ú>Tï5'\x001aIØhù=\x0018Ëp7`\x001dº\x0002\å°
Õ³)~\x001a5hÏq0\x0011ý]ÈjjVÓÇºW>À®\x000bÙ=´AF^\x0004Ou\x0003êµ5¬í\x001d%\x0002
øðµ>è\x0012¤y¢«g\x0007¬«a]\x001f¬¬z$E 4síC8ÆñôEÑÌ*ô(à\x0012t\x0000õñ&«ùße)ÿ\x0006õ½bdÂz W\x001b\x000e\x0002vµ±\x001bøÓ¨ïÏ²ÿÅédûÍ=©­Hm\x000f©öuéb\x000e8\x0006ø¹Ñ$k{5éÀ±Æä\x0005ÑE*°¼8:Ò°ÑXÞW\x0013×Ö"Pi+Ðç½\x0014e±Ë×7ìmaWÔ¨©ãj\x0011ª¯¾>þÚj\x001dG;\x0005XèeKñ\x0013 \x0013o=Pµ¯f\x0015]*d{KhGYk½wÅ\x000exÚ	jEu,Q½ÿ\¡ÿý
er¾ÞÝ>Ü6YYÖyzúS¨l¤²U+Ù¨ÕSY:o/N_Q&'üíÕùåX½z@,E7²×Çª¤FË\x001cÖTuæµHèA®&YöÏ2Fe;ã,s°\x001eN·Í¦YUÌj\x0005³¡\x0013\x0017æ9°v²\x0012¬
©ýDºL\x0007³®u?sÔtöªèL)ðRli7qu0Ù¬`ÝmÉ\x001fN=¯2óSM±;m}h¬X\x001b!÷ÑÃ\x0016\x0005>§RáÚàC«D\x000efW1»~æàPG.1c³ZZ\x001b²¬
=¡¾\x001cÙWÈ~Õá\x001c¨ºÎ&Ï"\x001f\x001bK\x0017¦d¶:cÅ\x001cûÁm×´4BReLÌ¾ä\x0010Þ)-&¦J±¿QàNuSëW\x000f·÷_¾´ö°åé\x001a[_¨|©ÄòêÍÄa·onùêêüòúz®óEÁ¶5¶íÇ\x0006\x0003Ä%u°üT\x0016eip¥&¬â\x000el[Ï¶]1Û\x001aiÊÜ\x0001Ãhßø¯pð<'dù;°e-û±\x000b\x001c\x0000+9·úsp\x000brä2PD\x000f¶®\x0016Iê,Ó
'tÌk\x001bs ÍãNeì	´\x0003ÛÕkÛ­XÛV+6ùmîbØFs±v
¦ô`«\x001a[­À¶Ò	'JÌzÇÆ\x0015f?\x0011Xë`\x000eõT\x0015Síb1d«#§ÞV\ÁN\ç=Ø¶ÚÁöïGL[@k¨w­\x0019{ÃÙö5¶_\x001d|YØï\x001ap\x000fËégÂf\x000b;Ö§_\qú\x0005i¸¿\x0017\í9¶é}ä§½ÊVVS\x001b=
\x001c\x001b]\x0007\x001f\x0015
\x001eþÞh-µ·Ô\x0005\x0006{ãò«q	ÇËHgrÉQ¨àêÏ3×D?4K>%kð\x0016å%\x0018\x000cÂìÁ}t0®\x000eDáË\x001a_®ÅwU¦±8_?Út	9ÿN|]ãëÕøTxá?Dç¦KNOd4v²Ý¬e·®´?Å\x0000º¦©çVi¨¾\x001d½ªw­Z»m±>4À5Ú-¶zøoNÄQûà]
ï6XõzÿêjyÝð£ëÁW«Eôz
¡s\x001dÊ*zªÀÄÆÊ<ï±ÜOz«ãÒ§Ã~P}\x0001ç\x0004*üróé1¡'}ÏÖÎµóªð¼Ï\x0002.EÛi½L\x0014~8{ó>a'©ÏùëíØv\x0013\x000bË'£ö£(èÕ3òD
o\x0007²¬å
f¹ÿÅã\x000cÄ\^åá¯·b6\x0015³éf\x000eQ°hÀ4Ï­rïÄfÌ\x00033\x0011ÑJìd\x0006\x00073äåltà*\x0011'¹\x0004À?ÕX¾9TÌ¡ÙK¶\x0010ãÎ%ÎF~¤
b"ÊÝÁ\x001c+æØÏì47:5FçNæ\x000eßìymÍöàÐ°òdXuBkG_ÆDV4±\x001aè§: v GU!ãcP/2÷t2±D2-:ht§è§#>=ÌõQ\x0017»Ï
o-)ÇÀ½\x001dKª®±©æ'\x001a+-VõY§ú\x000f;/4ÕÝÃÁ\x0011©sûWGðÓ\x0016A\x001b7zÑ3.½èå×R\x0018¿|¸¿ýõèÃÍCìÌlá==E;©e)Ós\x0008\x00183~yuyþïG\x001fÎ®fÔ\x001f
¸­Àí\x001ap!x¾á0ÉØM%3£Ö­ªùVkæ\x001bw!eÏc\x0011GäÂT¥-çÛVóm×Ì7ñ%#a©\x0013¸%Í.L´Çê#w\x0015¹[GîJ*½h#çØ©ÆA}à¾Z+~ÕZ	)ï.\x001bE.<6å\x0013ªàÕûu3.èÉ\x000fß\x001cÈÿÅ>ô\x001cøQbÃµR\x0015A¹\\x0004ÕîJËzì
¯iµ\x0014}5k&î>t]£ëUèÆs\x0002\x001aìPÃ;ÔNå\x0015vú\x000e2«\x0016º+©ér\x000bÁ¤3¹P3íCw5º[n%'H*©¨\x0013V)®âò\x001bnRYoR¹n\x001aÁÍûÒT3"øÛN%Köp+aë\x001bt\x0015·,¨,7\x001dtBñ¹èñt¡×6Ze´à ½d*§%k.x¨xî\x00027ºZæIr«ßÚ2²\x000bÀ$7¼Ìe{|e®Â·u^
'pìÐp÷s[\x0006,°tªØ¶t*ü>}¢Õ(ÅÓ°OÃÅÛ\x0019©\x001c¦\x001dÄ_v\x0010~]B\x001bPÌ\x0012m±{+ÑF»Ï·H_\F+UE´Ü{paFéð@5
o(æ 0ÅD=ùR\_-|â-ÇMÙR¬WÉé{ßÝx¿	®Õìâ¯\x001d¸``GB\x0007,òUîK\x0019,ÝÙ´ûV\-ê&ºfW\x0017ÉAw\x0011\x001d/ UÝ¸¸ÆU¸Æõá*W\x0004 àò§85ÂwöT%ÜBÜ¨*Ü¨úp\x001dÆ@èÒÙù]\x0000l"Ç´S9Øp¥¨\x0017Cú½×òú¥-?<ÚrWLY-Ä\x001dõ\x0010wø`º\x0004\x0017;£ÅoDÈw²wÑÀúD3Þ¥¸£s·óàÅ\x001eh sP]Qò0û¹ÙW¢f^;âí»×¤\x0014É+`+°ïíý&W°´¦^ºÖt-]%æs×éPºÒ²´A4bAFWÏmt]s«°£¤\x001e×¸é\V²\x000b¬¡\x001eÍüa#/\x000eÖ·éâÕ\x0006¦\x001b_\x0003 ÈÚ¤!Fæ2laãhëFöcßEaðî¥ü,ìH\x0019³r¥t%îº
x]}¥ß{x±D¯ðºl¥{áµd\x0001K1¡_µ×æ×wÎ¯ÆNË7Zo
¸ÑÈ¼SU0Kyý·Ï4ZqiÎeÉ_TAQ®å5ã¤pÂ9yìæèå»Ç/»-\x001bN"VÌ
Á\x001dë%V\x0012\x0016çä±³£ß¾¿>½úê\x0010ó0»Ú:»z)´§\x0002Y\x0015°úÐ\x00114y\x0016SÞ}\x0007²¬å
äHQ}\x001b/+e\x0002²#R©äû\x000eh_Cû~h0&ÉÐÒáa3q'§|¢åÐª^\x001cjÅâpde\x0014
\x0011ñâ\x0008V´4\x0013`\x001dÐõòP+\x0007Þ{¹6Ã{QGä\x001c\x0019ÌÜ
ZÕÐª\x001fÚkn­<²¡\x0019­àÕ!&">Ëõ0Mäö]}Ì
VÈK\x001aÎeªé®hn\x0008°å¶vÕDã¯½Ð>à:ÎÐ\x001a£É	Zsy\x0003X![\x001d\x001eÆTÐøk'4Ø\x0014ô\x001c¨<ÆVòvOiq \x0000¦ÙÖ\x0013mû'Ú0\x00050\x001bÔºKæg©#\x0011ñ@eC\x0013´ÅHCm'ë³¶\x0013\x001b\x001cG\x000b$ÁÉ'çTE\x001dÙ6_F´:àû\x001f±\x0016ó!`_\x0003û^`o¸ý@@$=7¦SAÍ»$ÍÀ±\x0006ÀxN°ÈµW$gç\x001d\x0007W\x000b¶âjYájÙëâêà\x0000\x001e*%ÚÀÏ6JÍ'¥·\x0003Û\x001aØö\x0002£\x001a-\x0008\x0019è\x0011Û[\x000c\x0002e`q \x0004Ð\x000c<H§Cà :.§D4THéñÁ.¾\x0010æ­À¦>#Lï\x0019á'ÝNâ´DàÚy¯º\x0019ØT3lLï\x000c/\x00198pµuäV;9Õ¼r1p¬c/°C­¦Ä
S¤\x001f9÷V\x001e\x0008\x0017·âÚzËÙÞ-ç¥¡ø¶Ja!>ÒX\x000f\x001a®Ômæ×
ØNàÔ³&»OÖpî\x001c8éd\x001fÛèæ\x000b&ªê\x0004\x0006×*·\ÔTlm£Ô,		{n\x0008~ï[ÂZáe]\x0010K¡Bo¹	\x000b8{«sgA(\x000bî¤ø\x0008Ú?ÿÏÝã¢¶Áb\x000eÔåÖ\x0014É\x0011ífR·Þ£µv}vú~¾Óm\x0001·\x0015¸]\x0005\x000ev¼¥¦hû*ËO ÚL([öë
\¯\x0003W«á?\x001aXo[yÁ3.ç2·\x0016»
Ü­\x0003õaÈ\x000b\x0013\x0014T\x0010lwÆ©Px\x0007x¨ÀÃ:p\x0013}d\x0003'ï«¼¯&/ÃåàÃ7(\ãjÝîÄ4m2Eåtx-ø\x001aWz"èÕE^ïNµnÎ\x001dg\x0010\x0001¹à"\x000f-Ùè©ÑÃ]oN¹rwzGÉf`K+<a\x0012·â\x000c?¥¦rD:ÈMMnÖÈ\x0017¦\x000f%H\x001b.q¢Ü£<Ö«<®[åÁ²1åÄþ`\s¶jÐA®DE®ÄJrì4]ù\êðÕ\x001d\x0019»ÉÉ¢Ç×¾>U\x0004ïnwôâæ¡ÉN\x0011°²-7\x0017ò\3&MòªZÞÇh.N^]Í*yx¦è:Rº¹Ô_	°\x0006IýJêÀ©[aâÒì`6Õ<þyÖ_º%XYÔ5AZQÒù'Ê|{«y6ýó¬5?\x0017âK'©îÈÒ\x000cÄÄ	s°9Vó\x001cûçÙ*RìÒ\x0012#!\x0012'EÉ5(øXÎ<¬À×Tß	ÛH.°iV6»Ùßµ~¢h¬¹^ÏrÅÞËê*p'cÙ<Vªõ\x0013çô"h\x001bF®
ÉUØ·ü\x000c^ÙÃÇÛOmY¨¤BÈý\x001b\x001bJQ¯O3ï;N¾\x0003Çìê«ó7soÊ\x0019ZUÐj
4·\x0005\x0004ÿKP\x0017¨9@æåDý2ê\x000eû°)øTÁtzwwCõõ÷ñ__ß?´\x0016QÃ\x0001B9¶ÊjÞð¥¹ÃD\x0001[¦Sýå;ü××Wóz>Tôa%½Ý¯pð\x0014HPÞÀyuSÉð#\x0010þ\x0011©Ôw
¼+j$X§B	¸"91qßtÒ\x000fÅ`Ïb0kð#[*áS.9æ\x0016üMéeM/×N¾ä\x0016IJq#OX9¬dñªMñU¯Vâ\x001bÏi7
Üü6**\\x001e\x0014'dëzñu¯7ÀeíPv4ªdµ3Qß_o\¹vçþ\x000fã«Pá«ð/oìè\x0005SWå3?uâ\x0000üû¾\x0003'®Õ©È{VEpA\x0005Wfs\x0011¼\x000eSâ\x0019ûòõ\x000bðß\x000e\x0002\x000fËálÒ^ï\x0003\x0016¶h\x0000\x000f\x0004H¥eÑÔ0Q®º\x0018ØWÀ¾\x0017\x0018³QÍ^ÛSÑ!'Ïê \x000f*­¼Õð½+ÂDÉOëÑG,mÊÌýÂÀRàP\x0001nàày\x0005«}Å8Wh?!âµ·J=´9õ°\x000fX«¢¡ë})\x0015W§¥ý$ôbbY-a¾ß{6.ñzÜttJÈ"\x0016¾Á¦³òÛZ-
þ'e-Süõý§/»¶(aÍ¾ÿI"0	ÙIðèt§¡Pñ×o®O\x000f¼ÉQ\
±Å
î\x0002íX~IîÛ§ê<>h[AÛ5-)Ç\x0013\x001bdÐ+&üa!ëflUÍµZ5×ûÆè8Ý%¢fÊt?}ùõqWÓ=Vî_6ÝE\x0004F¯)ym\x0008j\x0010;oæÖÕ|ë5ó­%÷
X1ÔÔXXzhMÜ}ÜÕ|»\x000e,oÅ[W?Ô¶$n9QÅÞÅmªù6«æ[sÍÐÜ®QZUßpyÛ
Û®ÂV\(´dA\x0012YÔ¤R[4sj5ËÄêcz\x0014­Q\x001a
§8ÑÄj!¶Oo8Cµ±x¢¥<Gÿö\x0008|7vMq6lö@^»Ó®4NPì\x0001Ä©+%gãßÞÃ¿uöæt.Ì¡\x0007a6®2\x0016A»ýÊ\x000e°9II\x000bÉ%SV\x001dH¨l\x001eV\x0003c.¯ëöØ\x0011=R\x001dRi\x0005bXôÏ+;¥(±\x001cÚ×Ð¾\x001fZ±¬Q\x000c¥\x000b)Þ/\x0019\x0019EÄ·A¶õ<Û\x0015ó\x000chYçÅ`«ÆÀMè©xÃkµ\x0019´\x0013Õ6t¢{\x001bzëèéÚ\x0008W®
§\x000bxm\x000eå6C\x0007]ÍtÐÝ3\x001d¬ Úàæ\x0000=uóÖ\x001c¨Àn'²"²\x0018\x0005NsÕ8ÚÒì{ñMR¡\x001b\x001bRÖÌé÷>h)d F1°ý\x0011D¤Ó\x000eU7V#hÕ?Ó.\x001e«¼\x000b­\x0014¨*bÙx~fh3\x0017°Ú¨»Ï\x000eýR5QcëÔ\x001c\x000f&2µjD¸ZæZuÏµ\x0014Aà\x000fLjÞ!òµ\x0012Ô|óÌ%ÈzÜ}tHTðÈ¡ÁTx×t»è9PôÜNmëC:ýþ¬©µ\x001dÅ\x0014´=\x0019Æn°_áÍÃíçÛ&jí,g\x0007(¸ÎI(^I¶LhÆLø\x0006»\x0016]¿;?»:\x001d*ì°
Û±\x00185ö²ôDÍÞ¢jÚÔA=¡ÀÉ¶+°QteµS$\x0002äµ.Ãb"}®{#
ÜÃ êrn	:\x001bÎ\x0013ã«ýüÃo#¶\x001a¯meéÛ\x001fno\x001e=zûxû¥ÍyqR0aCa°gî'/(ùìÃùÙû?zûþüú0³ªÕ
fwÌ²Ü\x0019¹_ñsºrËu¬ûmñ\x0011±ñ5õOÕV¦yNÜt\x0019³©Í
fYÄ­¢.©g¾¤øù9¡ÊeÌ¶b¶+Õñ^>,RàÃï3ü¦5#»
Ùõ#ûíMQ\x001a¦Æ\x000cØ©E°·ÙoëZLøG\x000ek1\x001fÞÞ?|Á¿xh+_rEÙYb\x000b\x000fª\x0006E	oê«ôÁx{yuÿ
q5\x001b°Aøac,\x000fUû¥ðJ	ÅÅx\x0018ÿÈ
Ó\x0003\x0016vsöâF'¼«áÝ:x%)N\x0016r¹Pbg¡ä¼ÛRv_³ûuì& aR³È^
ü=gGÉ¸éªõª+W
YÈ	ã6T\x0004\x0012tÉp~¾Ì{\x0019¼\x001c\x001eå\x0000~_A¯æ®´\x001e«Y2=\L¯'\x001a#ôÑN\x001b¹î¸QØR$#¦Þ[j¢yF\x001f¼Q5¼Q«à½\x001e\x0008^U\x001f\x0008ßÝzÙx±jÙ¤´\x0016]
­ó9\x001f³¥\x000cxÞ=n§7ãg'\x0006ùÿüÿ>µÊGÚãüæ¤¼"OÓõÅ"¾S²ì\x0003sü³7ó*Pã÷&ß:\x0001bòÈNìD,ÉS²k}5Å¾ÑÍÉ\x000e\x000f."\x0017sÕ',mp«¼\x0011Yç,äÙµ-"\x0007rï¡¥¼\x0018YUk3+;ÁÇaÍVmJsFiJBnÏkAÖjô¼®UUfóxôâÿ¸¿»ùÒ\x0000²úóQg\x0016¸ \x001e§Ã\x000e\x000eoq¨î³Ë³ëCÀU\x001dªë(\x0011ãsAº\x0017ê8°å¥öP»åFbS\x0013nbìNBÄp-Ê¬ã8ÅÌ\x001b1q¡,&\x000e5qè%ÖpëYñ\Î^\x0019~R\x0013\x000bM\x0018EFL\x00184Ýù|tö=Ð6|Ã=Ýu\x0019-Iù:+XÏº\x0004³,£þîèì%°Î\x0012aäC¢MÜÇZá4\x0018þ\ÃnK\x001fh;)Î¸µ\x0012á\x000bY¯\x0003\x0016ìNò\x00191*¹ÏUé8\x0012'\x0002©\x000baU½\x0008TßÌ¢H,÷1\x0005@l`\x001d*§Ü&°õ*Ë\x0000\x0012ëµ¥F)rº³\x0013O\\x000bYëUàúV\x0017\©fõ\x0002ËbYÎMÉs.cõ¼Æ¾y\x0005ëº}\x0007E½¿±I\x000eß¿³ÝZZY+áÅ0l¼±\x0015ÜSê­a£Qz\x0018\x0019Ù¼Õk
9ô5(²'µÐÛõÃ?ÿñSã­ ±õCn@¤\x000c°Â×"²>ËÁbÀë«³×\x0007î\x0004=ì \x0007ÐÊôSã!F)ÿàZ°òT\x0010ô0k½;XwÙB\x001dF\x0001è\x0010Ntüawwwÿ©C\x00048¨S`\x0015*\x0016q\x0013\x000fp%\x0013ù\x0003üéòMÖL\x0018_s!*\x0017º\x0006á§|Bð@\x001c\x0001§ã^¦`óA\x000ck\x0004Ã(Ù¾o\x00102â\x0016Í°eki\x0010\x000b1ÔÁR»Å¨ªíB©¶[5
«Ð
\x0014Hõ®t_Wª3:\x0006aëAlð)àdçO\x0001B\x0012WQ:SSÙp+F!ëO!7ø\x0014ÞQÚ\x0016ìx[j{UôåâDÖÖAÔBnð)ÀÉåØv`!ÍÒaL©ò\x0015cPõP\x001b|Ú°Ò_.ôlÃ\x0005±ý\x0018êï 6ø\x000e°\x000fX¨I\x001bª
ò^òjRS5ï+FQ_vrÛÎ[¬M	yÄ\x001eØA¬
c&dJÖ¢þ\x0016zo\x0011©u;\\x0014÷7ì(1!\x001c¹b\x0010¦\x001eÙb\x0010²:\x0014'­ÇYÒ2Ì'uô\x000cÂÖ°ë\x0007Ý¿ø\x0001\x0008N[I;\x001bðõ\x0014\x000e(\x0013,\x001f«Gá¶ø\x0014Ö\x0013s67å|(ìZ1\x0006_Áo0\x0006_Þ\x0011ñÊà½Gî[1Ú\x0004[ØÎ\x0015U¬ÔPtÊ²\x000c³Ê´î\x001aEÔ#ó)êßEÓ?Üþð	þ\x0005ñúñáþ®e\x0010Ñ\x0019\x0005Õ¨\x0004IZÇ±¸\x0014QNtyÞ¨?¿z\x0003ÿ\x0002£xýþêòâà\x0018d=\x0006¹Á\x00184»ùÖK\x001c1x\x001a\x0003\x000efÛ!èz\x0008zý\x0010|TX[R\x001aD¹ëÂTÐ²\x000c¦\x001eÙà3DªõÖ6\x0017ÉÂµÁm7(¤é\x001f­\x0007`7\x0018ãu\x0016[*Ó\x0018ÊSo°^k\x0016\x000eAÕëHm°ç²Ãdÿ<\x0002Ç¹®QL4Zë\x001eVÕ\x0010´Z?\x0004ìÏ@Ë\x0008m§|ÃE¥x\x000c\x001b\x000f Þ\x0007z}\x0000þ\x001bïeSì(9N\x001eìD\x0016}Ï\x0018ü8£ÔS¶ô/7r#Ú·\x000f»o\x001eZ¥<¼V¬ÿ&à,%\x0001$Ãñ1|\x0003¸Ô>½É}hß^¾=»: ãáÇY¥>gvsc\x0008%zAî4*ì\x0011÷DUp\x000f·\x001cÍ÷	wºôç\x0012¹/z\x0016Õåç*c'
»Àë	kf\x001cìe~a\x0011éM¥6r
¡:kzÀm
n×£\x001f@Ø®È_*#ÊOtwì\x0002\x000f5xX\x0001n/b\x001f`;5>epöÇ\x001a<®\x0001×¦42öÜ]\x0015E%=\x000bNd}÷\x000f[Já¡ìË^pTùgI
SrÕ^#aB8º\x000b\Õàj
8ÞA,6 Øbý@£'ZÄtë\x001a\¯\x0002×¥¦\x0001U\x0012h©È²Tô?Ò\x0003njp³\x0002ÜDÏ}!áÔ\x0019ìàÅ\x0017§x\x0018í\x0002·5¸]\x0005.©5ÆØts\x0018VÌDvG\x0017¸«ÁÝ\x001að`:°\x0012¬EoÔ^]\x000fµ¯©ý\x001ajr3¸á·~°Yxº§\x0012\x0013zÀ½Ç½Í½Ç»Á±Ö¡È®>¬"s3Ñ\x0014p!·vßÖJHÚ¡\x0012R©X|ùãîîæÓÇûO
ÌZJÉ.©°?Sâ\x0012\x001c!¬Üä¦ZDpÁâËoN/ÎÞ|uùæ0±\x001d\x0012ÛnâTy"õ^,u:Ì§\x001b/A\x0015²ìgV\x0014I\x0006ÚLlØó×v¢Åe\x0007±ªU?±ö¨@E¤Ð]äêl@>$ Ñ\ÕVºªÃ÷2fe
ç[Ä ÉlNre¥V\x0014\x0007¡ª êûî2E¦PT³H(íÖ5´îÆ´]j]\x0001óKáéè\x0002\x001ab¾Za	³©M?³Ta]mÞ^®\x0015qâÝr9³®\x0017î_\x001cFòsq\x0004È,ì\x0010C\x0011³<ÔÄ°¸^\x0019ºe\x00184HnÑ\x0004L3MÈû¾ÉqÂ:í®î_\x001a@ÇÓlù\x00195È®\x0000[]ÎTçsÊFêcö{h\x0001·\x000b\x0006CñåßV´/[\x0002íkhß\x000fúÛ²Ü*6·WÞ`³û­ c
\x001dû¡áh%ÞÞ¹ßºPÍm¦z¯,öõòðýË#¨Ô©,C»¤íæ\x0005îNf>ÔQ´¹¾¿}ÿý\x001dÆlÌ\x0014#\x0013´ö¼\x000fÍD¶U\x000ft=Ñ¶¢Á\x0006å°ªL"Ï	º¨ºCòhíÌ®fvýÌVÊFí Z\x001cÞ±´Ùz\x000eµÍ\x001fD?²Å\x000eÙ\x0005÷Âý\x001eÜÌâ\x0008²ZÏAö¯gÌ°wû=O;\x001d}çC\x001dFÛ¡k»?ô\x001bþQ[Î²Æ\x0016y\x0013Ò
D\x001fR°iaöØR[\x000c+hÅI¬Þ6ö\x0001ýEö3\x00162±ö°\x0000\x001fôÁgÕ·ó-@\x0012l%×%~÷&ßLF¨§B!NvrÂRgCoÌDaþBZUÓª^ZÊÈ<·\x0002_\ê¦çÓ\x000f³:¬a\x001f&Ã?l\x0016OmÊKF+ÃË\x0016ûL¤·\x0016/q&HñÑ\x001f=zý~^u)Á\x000eS©SÐÆ\x0012ÃÖä\x001c% 
õ)ýÎÜRZ[ÓÚ>Z¯ù9(b\x0012®Ë´ÎðÜ\x001eè|ÑJ+ë¹}skdä×ñï9¤\x0012Ep%lB\x001bê¹
}s}ô~\x0002Îè±ÎëV)jIèå¦(i½\x001f\x0005ß`\x001bWÕ!W÷ßÿx³ £
«ý£
¬ö£ð¡0ËÄ³æ¾@äê\x0012þ|¨¥_\x0006\x001f>$ûQK¿Åä?U,.Ø«ô=Ô\x0005m	x5ãrÝõ\x0013(H\x0004Î\x001e=\x000f*Q\x0002.\x0013Ý]àªqµrÆ\x0015wgJeë\x0018\x001fd9&®§¤È»ÈuE®Wã£\x000fE¸>æ.\x0017Ü¯\x0005ÛBnÈ]-\x0015½r©ÒC\x001c\x0017À¥"L!ß\x000eÜT\x0013nÖ-\x0015Ë\x001e«J~¬\x001d]	Ðmx¬jÊÍº)wjßõÙ\x0015½}L#òCM,\x0017ÛjÊíÊ)·|c»jn\x000bém\x001eêrº\x0000ÜUàn%¸$ñX\x00150]ÁKí0\x0011\x001aí"\x0015y\I.¸\x0000\x0008þÄÜÀCÙ	»¯[n W\x0010ØRºUkÁ:ðÒsT	C¥\x000b]Õèjåþ\x0012?¤! 9v ÄDRP\x0017y}Ë9vK¡\x0004ú¨è\x0016V\x001aÊ\Ï.òzËë\x001cÖÞ\x0017â¶4\°\x000f§ãvËELu6)"¾Êá\x0003³\x001eÝýÂo8ëªuµnÖ±×UV\x0000R\x000el]nÎ\x0015HÄI±á¹hêóÅ¬?_t)´õ,ÇÉ{TOd\x0004/\x0002ÿ\x000eVJe'¾@E¤d'b³«Lûð÷¶$æ¯Ä\x000c¦-A\x0006®3
zª¥2¶ºBÎ«?Ïä-3ª¯Pý³Fµ\x0015ªíCÅf\P5<jÌ\x0011«¨\x0006lcË\Â8ÀÂ8eérJ{\x0003®Bµ¬õ¡T`ýª\x00007&±)Q³²n9ý0²­m/²)%íp³X\x000c¬J\x0001È\x0007lfdY#Ënd!I:\x000e#IÕ\x0004©(nÐÒ6Èª^\x0018ª{a7C\x001e»ÂzÐ¬b
¯dä\x0003ª[íÈ¾FöÝÈØÐ _\x001e\x001a\x001c\x0003ÃÈ"\x0010òDåÄ±&ýÄ{g¢\x0018¼æ¥ìy)ÇC×]+²ª²ê_ÊØ
/\x0013GA\x0012}@,i%0ÍÄª&VýÄI¤>©ØH¹G¦p
ú\x001eL3²«ÝúI6%ó\x0015=\x0011Û	U£åÄ¾&ö«N8
r\x0002|Ajêù	na<à£´"ëP!ã¯ýL&ëE9\x0003	§ÚÍ6A6õR6ýK\x0019Ìãü4 pdd\x0006e8×NL\x0015ÿ-G®\x0017é^\x0018Ê
¾­Á{Ê\x001e ü5ÙóB>ý¶¹××nÞPÂ\x0004\x000eî\x001324\x00078ÄÔ÷rb[]"Öö^"¨zM[\x000f\x001c\x000eêÇ\x0001&1w`Æ(ÙVÈõ$Ûîu\x000c\x001eª&d\x001f(C\x001e\x000edVm\x0013S="\x0016#»zë¹î­§e<öYÓÊ\x000bÅ§)=`ÅT÷ÃåÈ¦Z\x0018Îô.\x000cT?£>Ì^
*v\x000eF±®R\x001cZ,e½Óï}ÌÆsûs\x0014Dgñ|§¸@\x001bNê\x0003±èVf%Ær73x§É\x0008G1½\x0011\x0005[Þ¬?ôÖÒÌ¬GÌº9úÒ2)pÙ[Àîv,f­7gãjfãº\x001d·\x0010Ô\x0016Ì"ÅkãZ°\x001b7g;ò¢l·\x001beLI\x0018ÅJÃÜ
\x0007×\x0006«>(±Í}"GÇì?7æ2 ZÀ´ùl\x000e\x0013ÅK}}4§ß;\x000f:#èlÖ^±Æn0üâS¦ÖV\x0007Ý·ßÝ~þÝa×yv\x0004tûÒ>T^;ãw {P«²\éQ\x001eÒ\x0003áeì\x0002|ý°ûåæás&^q\x001b-|G±9ù\x0012Ì\x0017Jý\x0011~*37]\x001e]_~8»z7§UÅ¬ú\x0001Á,Êï\x001eë9	y^}w\x0011²®u?²\x000cd\x0002²-	£ìh\x0003óTñD\x0007³­í¥_5µ6¨ÀÒ0¸\x0004¶ópð"dS!~d\x0017QQ>!\x0007ÇÓlå¥¡'\x0014
\x00171'8\x0014Æ4'ûFÜG×·ww7-ñe\x0011¢'k\x001fósñØK"Â»äõÄ³\x00145á~t}~qqö~.Âi\x0002&\x0017]¸!u²I¸$Ã°¯gó\x0013ëa1«ªXU/+.ßH¬!l¨Ñ­¹ýÄT*üb^]ñê^ÞÒ0\x0008.@¦~Öéæ§\x0006o&ò6\x0016ó×ôòbHy5çRYÏKwªàg1®­pm/.ÚeviñÂa\x0016\x0019wÂ\x0013Yë*\×k<\x001f¾:D\x0016k±û½x=\x0011\x001bZÌë+^¿bõ*nÇi¨Ý\x0015¶jÕÌ;Y·7Ý\x0015Jsp-eJs½Éä×7\x000f\x000f»ÏQþ	\x001fùîîn?Ý·\x000bVÖÈ7Ú\x001fSZiT\x0013&º¤í3Ë¯Ï®®Nß½C	¨#øÛó7³jãy j8\x0010µÉ@03\x001aØ\x0018¥0å!Dñªê½½n$ÃËEsïßÕCQE$Ð\x0018[Òd,§lMr¨
pÏXâ¾ú*\x0015Ö\x0016ÉIà\x00060NQfÉ¨ \x000fvBê\x0019«>Ûè³\x0004\x0016eÅBCjCRÑº|C¨ºÆR}\x0016·Ñg\x0012õÒX¬ä\x0006)Js\x0011¶ó¢ðc	Õw	Û|\x0017\x0007^3©{\x0001?§ò¡ò\x0000\x001fÀê å²±øÔÜlX4%SÑÔ>çæííß\x001e±ÜëÿçË®ÕÖHÒSXd'¸J­Ô¢LIaïSoÞÿÛûTøu}zÈN¨2\x0013å83±o\x0014)Gnµ·ÇT:ÊÉÃ^\x001eLjX2 Æþ¨K*2äÛ[X[-n\x0011\x0018\x0012'\x0007[Ü2\x0006Ü¨\x0010JPà\x0000|ú÷`\x0008° f\x001d)1rþ\x0000Ü¬$OI:\x001cþhÈg
É\x000fõC[ÈnëI_ÉîØ\x0017Ä~§Ti£â\x0018>Ðgl!ûðz\x0010£\x000cèy\x001c+ W«´b\x0014³ÇMçÝUóîVÏ{ÎÑ\x001eîioyÞyÍ¨	NöP±ìÅ°@ukohÞé	Ù\x000by°0d\x0011{¬ÖL\³ftÄZ3wo,d\x001c¬Q\x0013ò½}ìJVìJ®\x000fL\x001e
t%4vèv\x0019¹ªÉÕ:rL\x0004O9?I!»Q\x0007^ñÁë\x001a^¯\x0007Gás¯°,$QÈ÷ê"vS³Uì\x0018D¥»É\x0007Ëýx¼oºfêªÖmÕ`\x0014ÉèÀ:)¯\x0004xÅfã\x0012%Ú6×õ×k\x0017¼åóÝÀç».Ýç\x001bú-¯ïU½êbMö\x0017E&\x0014ùÅ\x0011¥0[\x0008\x001a4ÚWökn§¤ B>	ºZ\x0005µAÃáÞm\x000bàå0\x0007\x0007àe³ønMºþTåj}N@\x0005÷ÃqXHùö#é­\x0019ÙÖ²q^í\x001e?¶É$(M\x0019\x0017øÜÔP\x0007Õ*Ð\x0015\x001b<A¾:}ÿÕ¼RB\x0002Ö\x000b\x0015µ\x0014ÝÄ²<¦Ä\x001c_|5ïPg¶Ö5´î\x00064­\x0008Z\x000ck0øøHÐ³á¡m
Ý½6w\x000c ÷«\x0003o&b\x000eó:\x001bÇþ¨\x001dù£_ßÞßÝ\x001c½¸myÔC!¼Ru¦ña$Â­\x000c;@NõÜÝïÃ¯Ï//Î^Ï>ëE9
/G9\x00102}<úp»»kÉâ
I[b1Z\x0016oh"\x0017TkÞ\x001f}8?½¾dØa\x001a¸\x001c
.£UÅ.Ao_\x0011-k>5;«sÕJ[50¹I\x0007®\x0013\x0001k\x000f×¹&\G¥\x000c0á\x0013º¶\x000bq]bá[~\gÁ#ErzÔóÒOD~Â\x000eÎb\x001d¨D-Õ*[tå
\x00122®\x0013}Ã\x0016ãÖsÛ¹rS\x0003¤5ú\x001a\x00038_`Ü6¸ªÆU\x001b
 I\Åpv\x0010öb#·Q	b)®®\x0017î\\x000cÂóì¢
\x0017	H+/\x0018WOøçKqC\x001búpmNø@u(Ôs§/Ãqc­â¬ºY3m¬icçä:¾Ô\x000cìº,\x000b\x0004;Í²6\x0013Ù¼\x000bqu}0èÎÁúu\x0002@ÿOóC	Å³ÁØdrMMkºiÁïÈ:a»V1mh³ÖêXÀ_û\x0016.ëL\x001a
«\x0005,=õ{¬6Þ\x0002×ë
×ëÎC\x0017Ý|G\x0018#TßÂ&ªËÃÊbÞTkÁÎf\x0003½ñ¡\x001d¿kÎbsn"b)­«'×uN®ÔMÃ Ør.zD¥p^\x000bSmå\x0016â\x0006WM.þÚM$áº@ÅxÎ(RlÁÞÌn\x0014\x0015.þÚ\x000bæM®\x0011C¡³ÌjX6ÎëmNÜè«\x0010}ßJðx+äSÁ:Ã}U\x000cåmÏ\x0013Ö]¾ßÁ%Y6/0/,6\x0017»£W\x000f»Oà¨¥Ìç¶%\x0019\x000cþ7ì\x000b{?QÒqzôêêô
¸h)ïyO[Q« é÷çéFîYb\x0006ScâïÏ	\x0013÷¾­ó$`ù\x000fÌÂ£7÷_\x001en¾Úý´DÓ\x0003n)j<¯Á.âP-\x001d÷X: Ùûæòú
þpúú  Iâ×¶â×võ\x0000<Æ¸­§ðÓÂd0ó\x00074Ö\x0017Àj\x0004F¬\x001f
Ç4\x0000ðs3d§#÷w\x0007[b´@£P:E¡\x0006º³§ßÿØÎ!bð$9j\x000cÖWeÒ»r\x001a«	\§ï_~3Åy}Åë»-;òpTzNó\\åQx\x0013àa\x001byøcÕF~\x00191ølù%Û`¶\x001cõò½Í0ÕÔj1°­{§\x00183^ÉT³Fñi*íò\x0014ûJÏÄ¦&6ýÄêf\x0012±gbU7Z\x0013¶\x0006¶ýÀªf°)	j \x000c\x0013\x0001	\x0001þ%À):\Ä5oÅöbw÷=v\x001a_¢\x001aÍ
½\x001aOï\x0019°å¸G·\x0013\x000f¥ÑøÓØhü ~\x0010ñÛß®æ×¥\x0004VÛEå\x001d¬}9%\x000bØo«é·«§\x001f\x00167½Ì(X6ð
ÐÛ¸1¿¯øýz~Ío¾ÊEê\x0005	ü_iä¼dôrþjùøõË'ù÷XÔgçç<9\x0011çìå\x000fÕüõó_â´Ê\x001b6Hü¬Û®¡ü\x0017ð³û\x0001Ü[J£ØSîM\x000fëÇÒöuSÏO\x001düaldÊÈÂ\x0002¾?î~¾á4ÙXqOú"~ïRÈ"Ë0Ñî¡ÈoñòÓ·gðûAìagpRë»/å\x0013ÓÒ¡Øª.\x001b¶ÜwE\x0003öÖ"p]ëuàê\x000bà¶\x0004";qâÝµ\x0008ÜVàv\x00158é,&ìÐRQ\S!ÜTÿð\x001eðPUàQ°ê»Ã®H9òo\x001ck5\x0008;á.\x0004wéh\x0019\x001cí\x000ea¯¬ÏG¯ï?}ùÃR¿ì\x001ev·M©í¨1h¨Ã	\x0005ç\x001e\x0004­2øÛù62ï^_¾¹~cT\x001fN¯NÏg»\x001b¤wA,\x0018a½Õú¡0-\x0001¨\x0017å¿©`ºä&m<
©Uý1´Zÿ5àD$í\x001dø#×	F#¹jÔ`näÖã£qÄ
VÐ¥o\x0015v«y\x001cùýü£BÏ0R&8\x000cãV¯ª4\x000cº\x0007¢÷$\x0004Ãà²M=\x001f\x000fï\x0019\x0015õ0¬X?\x000c8ñH±\x000e3ßrjST¡ô´\x0015\x0013Úk!GÃ\x001b\x000c\x00036G îÒÒSU4»Áu½ý8Ôh\x001cjqH*
ÿ(S[dÁ¹ÊNTW¬\x0018\x0017£ClpX	ÃRÖ¨Â[®ãºb=h=\x0000Ñ1\x000eåC5ôûê]nb\x0011ÍUªé{P\x001fTWãÃp#Ó	\x001cÚ:³õ\x000eË;\x0018@ËËTà^R#ö\x0018ÈTõ¢\x0014î\x001bw°?ÄÅÑå\x0005pÏ=eh_AûUÐëáuô¦U:ï¹CÙíÔÃëÍj\x001aRs5¸ÕHö\x0005¨\x001dKfÀ=½Õ\W­ÀÜHCz)¶S¥§¹2\x0014Úô`¹Ò-fÄD-i\x0007¶¬&{T{¹\x0014»©\x0008EÌÁí\x000få70ÜÉb?ÕÆçÎ`tÜ\x000f÷ooj¼².\x0014¥\x0006fmU
³\x001dV\x0013{yuùçÙ\x0000g&\x001e\x001cH<RYm'V¡Ô°Àµe\x0015	Ùp;Fk\x000eõQhF5rìG\x0016\x001cÖRGs	fä)%ÅÈÚVÈÚö"Ë@½ÁñÍB¬\bo°çá6Ä¾&öýÄ¢ô\x0016ÕüÞd±D¨¸!\x001b,eÌWX7Ø?jô~óòþîn÷é6j#RûÀ2(9\x0014\x0006C®¬ÒÞ?0¼¼¼¸8}óª{àm ·\x0013ýÜ\x001aCcêè83\x0013l@ÃÜvBÕ¯Û×Ü~
wP\x0014ØÓ8Ýdcpô¨&ÊÈz¸CÍ\x001dÖpKSRK±ÕSÆ\x0016û\Í\x0003QÉ%Ø±^ÞqÅòÖ¹oYJàzbôj­â.o\x0007wuö|öõ/\x0013MiZÀ­ÉüÀebû@\x0013Ê%Ü¾æök¸±¥ 5&u">à2	<ï&,\x001eìzuëU«[í§;\x0018ê
\x0001Üó¼ÃD;¾eR)nÒRÁ¿êÆ×kS#/´ÈãE\x001e6u=n¢©ÇM4_þ¸ûéç£\x000f7\x000f-¶*Ê§\x0015Ï@YÊÿ°Þ¹/¢\x000b<ß¾~{ôáìjÎ`ÕãzÜÑq!·\x0015Ô~\x0001®OK~XoÈ\x0001®p°\x001bÕ\x0002îá{Á¸»àBnì\x001d\x001dÿmª¨%»4:úC.Í\x0002îPÍwX3ßR±HØâðÝ¹7\'r´¾W,pGIä\x0005\x001e¨\x000beTßg´\x0008v×\x000b\®XáXoÈ\x0005[\x0002\x001f\x0006rÐP9Ãñ\x0011yÈ+[\x0002nª\x0015.Mÿ\x0012WÑ\x0004NÇåÁO\x0001Jq³\x0003#õ¡Æ\x000bÀíè(\3ã6ò½)øÑ7*ì¬ÅACõø·ß\x0017ùwëVyYä9\x0011\x0017¹-üPTj\x0019ún¾ëGGù\x0015ö2YÈm\x0010ä7b\x0013ñ;©}9/ONVã£.#Øx$	ÝHI+NkùôÚnªÀÿCh\x0015dêiö\x000c1Õ }\x001b0*ÉóÃ\x001c<èäÙL\x000f:Ï\x0013}Ûoë\x000cVåë\x000cÖrv£JÞãÑÜÏÝÙùÐ\x0006Ñ=5¾í¯SX
 :®÷ÿ\x0014Ér¥\x001c[¡(8»	q¬c7±ÓÅ\\x0014jæ4aUTOûh vcMS7\x0010Ø<z}ÿ\x0008´MA1¯8'<	$[8bKDzBÕ"¿?z}ù\x001eP\x000f\x000e
²`i\x0007¨=¦Gë ²Ü\x001frÃp=¼´\x000cTW º\x000bÔñ{
i\x001cqÁ³Ó4U=°ÓT¦ÓÌF2\x0010(ëöfAPò[\x0006j«%j»(8ÏÔ\x00179:s]ø½"\x00177øòÃ^¡i/uM©ÖT\x0001ö¢¥N¬*8'ÁMÜ\x0005ËPe*ûPÁU%}Â³Nó­å&ìðVRïF±\x0008ïF±»]nxÜBë¡\x0016ðpxr§cÍYtS­x÷f§¹ÕñA^]ñê~^Yf×Ù}ì>ÎO¬ÙåÌÃZ`\x001e¨-6!RÄ^Y¼\x0015²i áÄÖÏÀúv$î¯¸I%~\x0017M/©\x0018\x0012ÌM[á¨ÿ#¸î¥ÏÈp(\x0019Äï°ðbV
YÎÚ$\x0015ÚGë\x0004÷°±(\x0010`,|jbA,µ\x0015¬í-m¯°,çf+Å\x000feAY«\x0019ÖUëÀu®\x0003Ô-gìH\x000f6@ËzQ~ªM^;­Ç\x001fr`ÄxìVGáßÞí>}ÙµD%,]\x0012ÀGÅ<j\x0008¦á!wPüíÅéëÓYÕèÄljfÓÏõ\x001eTæ$
ËEqî¸÷SéDK­ú¶NÔ\x0007ã\x000eÏú\x0019ÕÆé8ûúþá¦ã,ØÀ\x0002ÑØíÁÞ\x001fElüiâó×oQ`\x000e´¯/¯^ÍÊâ©Ñ=gUºçº¡=5ÖÚ\x001bÊÍ\x0004h>½ç\x001eê¡ÌJ)úÔ\x0006\x000e7O\x0001wmX(FØÈ	¾jÂ©\Bý\x001d\u£(¸>RÛÿÛ®ÔÆ<¥%\x0007«­Ä\x001esY©-N¬\x0006}6F´5â³bÄWþÑUÙ4\x001b?~¿ûþ¶í`UÄí\x0014F¥³ÕPÒ°ÜTw¨AýãËÓç³\x0007C&6\x0015ñ¸Ât\x0001±òÑµ
ù\ðür
)g\x000b\x001f\x001a¹½FT\x0017F®È¸ýË_în¾|iÛdXq¬(GÈs¡©ð¬\x000c`õÄ«V]qþõ×\x0017g××s\x000b$Ã»
Þ­\x0013\x001e@Ñ'ÓÒ)Î"³M¥GÍì¾b÷+ÙåLCôíe \x000c\x001c\x001f9l¾T°\x001dÞu×kýjþöæáãÃí¯-ÏrÎ»cI
à+5a\x0008´ÐÁ>óöìê««ó?l+dÛ}\x0005#«|À\x001f*È-£FäaÑQ\x0018\x0018,AV[¼ \x0016@¬9§3º:åÈ¡åÐ?ËZó[\x0016Îrî \x000coFX\x0017³¥\x000bcE\x001cû¢B:8äbV`ÏPÖÅú9Ö&=\x0019\x000eÞ:Í\x001c=çß|úòøpß\x0012`ÑÚrgJ£1\x0016Ý<Þ:qðmùìÍõû«Ë¹0ËÈ$\x0012d\x0012
ãÖ\x000f7·Mï\x0018JDGb\x0011:XC\x0002F\x0002I©RÏg¾\x001d^Ï¿eÄ±å\x0011+Ëc!®¤\x001aEÀUÜWr\x0000àÎû}q\x001c\x0005Ù<\x0019æQúe÷±Ie\YN\x00002J°r\x0008n4[£\x000e(ëz}úÕaÚa°B\x000c\x001bÕ,¢ìì¡©\x00115ÑJÖ©\x000c\x0013\x0005{Ki]EëziC)ö4©µ\¢µ$'îµh·6T´¡\x0016\x00052¬È\x0006°³b\x000f\x00043\x000f³ú±\x0011á³\x00111È¾ºüþÇ¶\x0012Tã÷ÅîQPt%\x0014\x0005\x0019°?'\x0014é\x0006IÓWïÁü
V­\x0008\x001fêLªeÌÆ\x001dk\x0012prùAÖcÍ/0"\x001en4ß¬ëiÖýóÑÌÜP\é"-\x0014`\x0018vù&bn ]\x001c?\x001bÆ¦ÀÛß\x001evßÿ¸k1#\x0018sb¨Å\x000cÊ!yvûíDfI1ßýéêôå7§\x0007mlW \x0007îö
ÇÈQq\x001eÏ¼ìÄ\x0012d[!Ûnä 0Á+g3êcÁ2YhÕ¢Ú\x0012äàÆñX7ê¶]®\x001foïînÿù[îgÌôâú\<8²×\x0004§K\x001då!ó\x0007\x001b]¿?¿¸8?½¥\x001d>ÞA,\x000b?jÝÁçíîñ®%¬"6¸\x000eùYæÂ\¤v¬'ma(\x001eÞ¾¿&Ûøm]ec]õxt±û¾aiSÍí\x0010![l`÷ØÍ­&ç÷·ÉÅéË	Tñm¸ÿøÛ÷?~\x001b\x000e`w»ïv\x000f9\x0007*.\x0004gË !\x000fLÒcÚT$)ùÁD´wO\x0001ËÝ
\x0013úß¢IþîôÅéÕd¶C\x0001\x0006z\x0006\x0018ðßÔÏ\x0000\x0003\x000eWó\x000c0`\x001fÛg¡RÒ>¬\x000fü?Æ>üùüy°aþíq÷ðåöæ\x000eÐW»|tN!\x0005	¾Ç
­\x00028Ï¨¸HXÝÀ\x001c\x0018\x001c?	éßÞ^]Ã	I\x0007æ«ÓÉ³²ÂË\x001béÙâå
ölñòÆ{¶xyC>[<wrâ1?9ñÏ\x0018\x000fÌÓðñà%>;¼ïíß\x001f¾\x000cåW»ß¾äÂ­ÉËÁ»£KðoF},\x0013Ö(Í\x000f@Vk^þéz²:«bÈgï\x001fË\x000fØ?!¢,C>*ÿX|\x001eþ±\x000cùÐûc\x0019òÉö\x00070È\x001f>ßüõÁùðz÷ðÃ§ìM\x001eYØ¢6\x0005ÆÀ?:§øY¹QD\x0011\x00075âõéÕ«73îÖ\x0000#\x001f\x00118F>%þp|Püá\x0018ù¬øÃ1òqñcä\x0013ãÁ¸ýò³¼
{öÝÃãos\x0010\x000e³Á0yBK\x0011m5A)öõ¢ª	Î^\½\x0012î¯þùy§þqÿü¼Eÿ¸~ÞÿÃÿü¾×û(\x0007ßÿêþñfÞÙÆgñ\x0017¬V\x000eÇÉ×\x0007¯?ÿÓÅP\x0011(ýó¯.ßOÆðª~þþÿÃÿü?üõ\x001eÿÅÍçÏ\x0007\x0000¬%½t\x0005¿ôèo¢Ð.#\x0018åÇ\x0008/ÎÞ½kcÈsðÇ2ä}ð\x00070ÜÅÏýõS²CJqx{·ûþ)ÑÝÉ\x0003Ò8yl³÷¤øM: eÄ]Lz\x001cÞ^¾lÙ\x001d\x0010¦ sú±\x001cÑc§2¢9ÙÞ
ª\x001c\x0013¢\x001e¼©­AÄÀ}ú±\x001c1È\&Yc\x0003	­)q\x0005aÜ}üÅÚásóÃ'ðpç
U\x0005Hø <¶ÊJÕî\x0006«ÆubÒQ¸Ñ¬]½z\x0003^m\x000b\x0006<\x0008ÆO¿ýÇÇ_\x001f
Õ½Ü}áîaÓg¡\x0014(é¾\x0014>²t\x0018Â\x0012sô©¢=yÚÙyz=Ó0,5§Á,Gu<ù/NÜ°ç¿ÿó¿\x000eÞV\x001e¥ÂÉ¢\x0005j0§vÎ&8\x0015óaI¨\x0011ùEåhþæ"@\x0016.%À¤[º\x000c\x00100t\x0006\x001a»À}y\x0019\x0019ÐÆ¸\x00060ð?9\x0003¡,f\x0013 PúØ\x000c\x0018è=\x001b¾±Vtå\x0005iWðIQO`ú}\x0011 $\x001f\x000c\x0006Ñ½\x000c\x0012O\x0011'\x0017üø@[\x0008(E
(\x0017Î ¶9Ï9o@\x0008wDÈFC\x0018vYN¨øµ\x0008ÓïË\x0008%¶¾ñé\x001b{CªÆë$´\x001ePä@â­0\x0008ÃbB¸¤¨»6¤T\x0010\x0012n±\x0010ö~eÚ§
¾2ø5ÃÎµ7G\x0017»v¿ÌG>½³>·þ\x000f::?BYï~ío\x0018^Ó¥õúôÝõLÔ\x0010M°CD3\x0016nDÄÃPçë\x00036M¾=$\x0007'Â`ÅZÆ¨*Æ¨3FûÓ\x0002#Ü.2u2IUeÈ\x0010ÖB\x001aÒtAf#*A¦Ep\x000f£EAq|\x000f/´5¤í\x000c¶@ÚÀe&Ç¾ÚrÈzIÆ%\x0019enû!£&Hi\x000b¤]\x0007)® Óï)õ1nÄ\x0011RóLºµq\x0018"\x0006á©ó°
pçç,e\x0013½\x001e^¢Z¹$%>3¥\x0014K\x000fÉ\x0016	2äÚCdK äÊ%)ýh*ýò©Ô2dGaQjnÖa1Ù®XµÒ¬£T>VS~_H\x0019´%_  \x00123
s0N¬½pt¨wwú}\x0019dL\x001d¦\x0010]t(\x0018\x0006\x0012Ü\x0018\x0018º¡JØbJgûÿ{×$;n$Ïw+¹\x0002\x001aÞ\x000fã§$bq,ù¤RÖÝ_ddÓ\x0014YdÖtéÓÝÆÝÁìcvrWrÝ\x0001w\x0004\x0010qN\x0000"§=Ó2\x001dv=~B\x0000\x000e?þ^\x0019J8Ù®Õ\x0006ËoÎ÷/_ÎpÕSPÛEäùÇxy+~sÖãZ\x001b÷\x001fÏ._¿>ËêCÃêÃ\x0010«E!oÍ-X&Ä¤ôXý<Å:Â*elX¥C°
Ü¢¼\x0015&Ï\x0007çÃdÃ	¿­\x000bV\x0016V1Xx@Ä\x000ck¬É\x0008\x0000k±æ1ÁÖyã´<`i\x0017hn¢¨2ÍÀ¿Kï2zØ\x001a#\x001ee\x0017Ù.0c»@\x0004»&0P`±û1ÁY`zâ\x0005Ô\x0005\x001b}»®Ñ\x000f­«°*\x000fÍ\x000b¯û`	¼´`\x000bÀ\x000fk`Óï\x001f\x0017VÎ`å\x000f\x000ckB\x000bkÂ\x0008¬\x0003ã\x0015.Ár\x0005M/\x0011eL'Ì9c\x001eÖ«æ¥ß\x0003´Z¹'6\x0007M\x001dúÖD#\x0019ïä#Ý
ER¹¾\x0019ðÏ~ÀËAÖê¡ù\x000fZõÐ×_ÿ¹\x001euÅ­'tbM\x0013V¼'ç $©íäµJ§cÞ^¼~ó¯+ÑW\x0006-`ì\x0005Ä\x0011¢ù\x0011sÀRÚ\x0001ÜêÔ\x0008"úö\x001b\x0001h\x0000è\x0006Tt|t>Æ\x0002@ôÍ3`8\x0015£Û
([@Ù\x000b¨}\x000e/\x0001 Mód3 ?L7'.¨­ª\x0005TÝö 8æ'ó9M>p§\x0002t[ù*|Aôñ sk=ðÁIf@\x0017#\x0011Qä\x0018\x0001´¦Y@k:\x0017\x0010=\x0010C©\x0013|.1 áMg÷}a/\x0015ô¢s\x0005qÂÍA<Æ\x001b­\x000cÅ`uÔvß
zÛ\x0002Ún@e+`\x0005-`\x0001Ðpø0\x0013÷áV@×\x0002ºn@_ÂF`Ïv\x0006´\x001c¦ñþD®g\x001b \x0014¡µÓ"ônB'òð\x0003x·áS6¡3¿óØG=HØ\x0008ä?xºp%Î×ï¢±ù®s!\x000f©ACcÉQÇÆÖ+yµz\x00180ZÌ\x000eÛ\x0000ýí!ïÄ"\x00029-¥:ñ¡·Cª\x0016RõCáÌ\x0004\x0019Hl$Åº\x0018Rè5gw\x0013¤n!u?¤¨Å=\x0007ÅXUd³\x001dV\x001ff }\x000b¹xD}SGwå¨¡sånqk~ø\x0016FÕnI5°%µ)\x000e\x0004N8¡m8ü*Ì)\x0007b\x000b¤ö3Hí[HÌ¡}ûðõáÛ·»/Õ[,ÉQ\x00034Ý¨«\x00119TÌ\x00119LHJ¤½{þæöÝ»«×'\x0005
«u¶fµÎ\x000e±Z\x001dðÝj­¤Ìõ\x000eV:Î³XØ§'3§a¥
lú=B³aRA\x0016
üÉô±R\x001bG9JÄ»i¥l¶ó|ôFZ\x00053Ã¦ð±O°
õWòÒÂûw\x0007ì{©j0¬Gþgð\x0007Xmóöëïx¨¶ÔâÔõülÉùÈåT6	µÒÎ\x0013çoß¼þ\x0005Ô¢ît¥j,õÃ`é\x001aKÿ0X¦Æ2?\x000c­±ì5\x0016	\x000f±\x001eUþ§ÍÃmEUQp\x000b17E`\x0004ÞÊö¤\x0015¹ÚPU\x0011C\x0018\x0006\x0010UVì\x0005D\x001cÙêKô¬<õ\x0014ØÎ\x0018\x001bÆ8Äèr@Ì aVÄH\x0006\x000en<qâÉ¼QÊq>Áh\x000bd0jE£ÀH°#7VÛ\x0011°­ªT\x0003â	3F\x000eÒ£À\x000biäIo{\x001b£TnÆèz!]\x0000\x001cZB¤*I¤Ö\x0007Jê]ÇÆý6M\x001dÌ0¸Jóp®¿~ù}u1áAµ¹\x000bü/\x00135\x000eÉMO@QOWs¦	8×o^¿8ê[T?\x001a`çÒDåSüÌ²j3Àp® -¨6³M¨(^Ûfînîþy®*6F­0\x001a\\x0019é1Lë*¢'6Dò¥usõ¯«õ±\x00052¶ñG´íJÚ\x001fr%}\x000bé4H7{³Zß¬Tøðpñë§Ï\x000f¿¯?\x0007­õXDl&Î9ÈUöZR©\x001djC\x001d¯Î¸½øõåõõåIõä
Ñ¶¶\x0017\x0011¼\x001eGw8NäÒ\x0019Q\x0005Ïó\x0007@/¢
¢½pýåA*Àe!ÔNá)"?;	Uóñg'!\x000eaÊ2ä©f\x0000è<­¡^Äxú	Û5TÝkhh&®aä2!éâE´~'¢n\x0017Qw/"ºgT\x001c\x0000\x000e¯ ®\x0019Ë\x0005{÷"¶«¨»WQÒØ=\x000f´×ÐÙ¦]CÓ½(\x001dÊ\x001aÚlp¤q¡¬áÞ³b[DÛ(\x00155{\x0007¥DªW\x0001Bå\x000báñ*Êí¡\x0005\x000c½(\x0019\x0016é4+Ík(8I©Å¢ÞíQ6Qö\x0012â\x000cK_Ù=¡ÂDo&s³óV±±=(±÷ h\x0017)\x0007\x0003øJ'\x000fzùhøòîÂ^­õgÎn¼ÃÇõ Ä\x001cùûJ8ÅI\x0019ÞDo\x001cÕC¨E¼ËnO·Y\x0013]ÝAOõÐ§#¦Ã¬³Ë %·7\x001a\x001fâ.@[Å6\x0001ÐJÑ\x0007X\x0018ce\x0006Ôëâ<1´\x001dPÉôN0ü-þy¯wÿ$Yé\x0015¯&dÿU¥ª&CÈ
9ÊNg ûzõ¯§¤+NÛr.¼ì-&7:#§É±ä}\x0005\x0006=\x001dØ\x0002jÒºÎ\x000eÁºÍ\x000e½:|þëaµ1\x0008\x0004ì#j\Øü\x0006\x0007ÑúdâåÕåõÏ«­AhLhL/"&\x0003rº2\x0018¡(Z\x0016áõÌ¥þtºr\x001bbíß\x0018òoú\x0010á61¥\x000eKSSàE´nî=ô\x0012:Õ,¢SÝ\x0008+G¶\x0007ö]\x001e(\x0000i\x0010[ªÆkp'¢n\x0011õ\x000f(e{Z¤ì=.>ÀIv\x0014&WÏ7\x000cNPá®}\x001fZv+¦ßÅîD,\x001eò6FrcCØy¢¥±3FÛÍè,v}åæ\x000b§­â2\x001aGQ6ndtí§6®ûS{\x0006Ôl\x0016ù9\x0000|òdèn\x001b_}U\x001b\x001e¸ÜÇul1g`ÀBæÆbpÂ,«?×ËFÄØ~f\x001b{?³÷.+6+Ô§ÊZ£tQ§:\x0019gÚ\x0006X{³\x0008èD? ÈaT# e
áNãÜÐu\x0013Âñ°y	¥5\úIÉ,âó»\x0008\x0016D ¡ÐFCpT\x000cÂ¦Þ\x001fYìMô;ÏJmÄØ½\x0011m\x0014ØQVQp6ü­ãu<Y¼QéÖn§ß}\x0006'd\x0013£ä2é\x0010¹tÌÂSü¼È$QÝÐ°\x0004ó\x000bzCÒ×¸'*ÐÕRÒ×OíWLÎº\x0015#Ö%öé|3n@iÄLZE¬ÔÉO\x0018^,}éy__7c]'í¼\x0000o\x0013$É|dÀJçO
&°áA}ª;\x001b µ¡69°<2kªcò¼@ê°²\x001f·A¶\x001bRìHMíî\x0000\x0019²>	@:>3Æ¬ø\x0011\x0018mv¤û:[dß$%3¢\x0012ª°\x000b\2\x0006ÿ\x0014'[K6BÖI@<Ù¦ÿÜ \x001eN¾g+°ÑÓÑV\x000b\x0001nH#\x001aH3¿­7@zÊ\x00012lÆa%%µZåÄÊu¸
R·s3¾eKFª?(êC*6À§ 7BÖY
´ª\x001fR9$Ë¾@Z*J°jåÊÞèls´í>Ú\x0006vd^F£döaÁedBT²\x0018gLbiuS¹©æÇ?ûúp¿ÝWÊr/\x001e¶ç\x0008Ko~Ç+\x001dæÁÐ<1þÙÛÕ\x0002V·b\x0002ZÊ nF³iSkSî\x0016pd¨ÛE\x0019=ÏYu iÑ iÑ\x0016Ý\x0013
Ðb´)¿û¢\x000f%&6ï´ê"-ì!K
\x0014­Üü\x0000Þ0çùìü&é"S-ê#Ë;é\x0012\x0019&ol\x001eí\x0002³-XÏ\x0011Ð¢Ä\x000e%=¢}\x0016¹ý\x0010,Ý\x000e2Ý.îZ2Yê\x0007PÛÐP¦Bp\x001brjÏ×Ôí¢é®E\x0003\x0007ÕQX\x0018<~ò¡SQF[È\x000ft¡ù\x0016Íw¡Én`usö\x0001àJäÐz¿6»ÐBûAC×\x0007u¬\x0018\x0004h>[[@slÑÂ"\x000bßEÖ.ZèZ4«KZVè\x001c±xEó÷óBØ.´Ø.ZìZ4¸\x0007,\x0015\x0006ÀQuÐÊªÅE¾n\x001bÄúáP?ôÓÐ>^Ü\x001f¾üN}ý¶zÑcD\x001d¦Ô[*¬Ñì0ÓÞÈË×/ÞÉ³7ïV¬[d=lPe+{Ë\x001aË\x00052±½§Sí¤Ä²é{ÕO¥j]½\x000ed\x0007Ü=\x0003oÏÜZá½¤W±\x0012§;Å7\x00039«N¹OåB;àçÃÃý§uÕ\x001b\RMÅ\x0018!æÙc\x0018þ\x0008\I`WûÓ~¾¼½y¹Ú³Ni@Û\x001bA
`\x001de¦"]3ðæä\x001aicO?·Ú\x0016t!v²\x0005\x0014\x0007ïRâY£MÈMK9Ýé\x0012ä\x000eNÓr\x0001NÇñØ\x0004J]5ÆÒÁz$ÐØ.h\x001cYÐX4\x000cÊfa&Ë½²\x0000:\x0017\x001b\x0000®\x00019\x001b@\x0016X\x0007 ÁF¼CS\x000bXààæ¢} :
,­\x001dïðt!nòóÝý=üÛîÎÀ\x0006±»g£KA(zóy\x0016óÅõêææÍë×W[U\x0003¼èNÝ\x000e¬È\x0003Rº<q×¦w%\x0005\x001båêân\x0007V±\x0005^îÙÄ6*\x0014­N7\x0017¸+:û\x0004:P=£EeäÇA®í\x0016 \x001f±[\x001b\x001dÜX¹\x0013%*ðIrÛXLÙSÊ\x0003ÝÄµ\x001f\x0018²\x001f8F\x001c\x001c'mód\x001dHÀ*ó\x0008»ØÙ;\x0004üÎYÊ\x0001x_¡\x0016õºL°ÙÎ¦¾¥ýËÿyÕÞ¾B5êU\x0001ÌiZÎ¸Ø\x000fÂÙTªy¥ÊFNãTí²ÀY~½$ V|Ã\x000eTÛ¢.\x000e×\x000fªêw\x001f ¦ßÝ¬\x001eK7óJ\x0001ÔYX.Xö_c«s\x000ejÝ.ª^¬
¤.¨/1-ÀÁÆ·~ê¤
2[XçT\ë·ßÈjDËj\x0016=÷X|\x0012r\x0017³Ç\x0017-\x0005e\x0002\x000bWÛyEì\x0000«©5Ôq³6"êw@\x0010\x001eó;©=\x001cv+i-ßÍíá~ÕÙ>Ï*Õ,ì\x0004_L×OÄ4kÕß\x0002#Â\x001e¬Ó
Õ\x0010ñLEÍM\x0017Î*O¼½HÓ¹Î\x0002\x00160ô\x0002ºReåPì*\x001fúèXþÒØ\x000chZ@Ó\x000bèX\x0017Î\x0012\x0007þ#Wâ{yJän#_]\x0019gÒu. z¦Yh(¥z²C
>_\x0011;5pà<H\x001a4µ\x001c½zÚâë\x0012°ÖÜ|b©1iÒb=éEß^\x0019ñBu\x0019IlBt>ð\x0003\x001f,;\x0017BÃ³¹\x0004ÛçÐ½u½$.¢êE\x000c&ð9VYÝ?'m±\x0011'%×¶!zÓ zÓèáQÏ2Ë´uÛ~Â)Mð	¿óLumË*Í¤\x0001	{Ñç\x000fí4Çá­?õúÜÊèb»\x0017]ì\ÆîYT*\x0015CÇ| ¥dQMøw4\x0018U­O\x0008j&P¸Ñ)Ñ¥$+Ú&¿â\x001d½)Tnß·VV´Vô2b;vÈ2C!ø¬ofÁóäxrLÇVÆ [Æ {\x0019=m²¨Ó>×§£:0íí©ÜüYÆ÷2ë.Ô-\x0006\x0015[®ï.ú5<uQE5V,¬\x0011¸lrQãp}u±Aò#Ã©\x001aNý`pºÓ?\x0018©áÌ\x000f\x0006gk8ûcÀa¥ÀomªÂ@â©ù3çÒ\x0016BGÂ\x0011-º
ä®ZKhöTíö\º"Ñ:+\x0006m»èà\x0005Åµö^\x0006\x000e¬Ë\x0012\x0000tæÔt§MxR´'EçêI%ðBK|:Éâ$gÕÒ=ý¾ÛÆ×(¸§RÊ¾õ\x0003W|Õèá³9\x0019\x001e\x0003×\x0018:sJ?o#m×OÚÎÝ§\x001cuGo$v>&>C%\x000b¹º±ç²eé/µÞ¤xjfâ2\x000fßï>ú?ÿ{]<ÏFøÊT\x0014ÁmÍúÅ®Ô®Ø$tvJhäúò«ëWë"é/ºeÕ¬\x0012Åµ\x0013«5Ù¯FVV\x0010.á1ÖØ²Æ1V#\x000eÀêx\x0002\x0010°FÊG`·Î.V2¦uÏ«« ½½?|GÁ?\x000fW£#x|r\x0003»\x000b:ÉY§\x0019;<àK\x000b:óöæò\x0017Tù·Ëës°Á5°ÁÀ\x000f¥\x001eKé!J=Òº6\x0018){\x0004ÒZD>Å6jCPï/«Â£7îõ´ë6Vagù3aºµí3?-\DÔmÎj©\x0016YÜ¸0\x0001©ÔcÛÈÏBi\x001bJÛO	7x¤NN-(\x0019)x^=¶\x0017Ïûïû!C\x0003\x0019\x0006 QTÞÕ¨ìH{òM°¼s!é~J©Û¥Ô\x0003Fs\x001cO£AöÙ\x0014\x000e:ËÏÿt?f\x0013\x0000°Ul\x0007&N£hV¹a\x00120m+\x0017\x0013{0-õ¨ZZCãÛµéÖ>?Ú*¬ÛÊ2©ý`³R2ß-d!ªFíÕñÔÌç[>ßË§i>F±Õ\x00005¸O	OÎ2ãËJuú^'óóò¿\x001fà5*î?}ûúùîÓº¡Ô\x0018ðEZ2tG`\x001eÑxùêí%¼¨SaÑÍËwo®¯^®\x0019ÊLj\x001bR;DÕE¬£\x0012³P¼\x0015N\x0017Ô\x000eºÔ*,ÕÊ¤[Ò+H¥ÜEjâìôÀ½<;=¯>}øÛÝç¯_ÖÄp\x0015ì@Å]W.¤\x0005UpÓ#Ã®`¿z	ýæõl¯AEäX\x0017íø§±-Gî·3r\x000cNy2D\x001e.\x001b"M~'ÜAz¥×óæÝª\x0014¿µbàuI?Ïr?ÿÛ§»?×s\x000b(ÓsÜÖº'y%eÑÃ²&\x0012\x0015&{ùòêßV«\x001c\x0012gl9L¤:Ïi8®\x000b \x000bß\x000c\x0005ôtçìfÐzj
*1\x0002ê\x0014*nfPK
©47rc·ï~Ðº\x0008@\x0017åD[@½â:@=´¢Îº5át÷ç\x0016PQµ<xªÚ8ôÛ»ï¾_<;|ùp·þÖ°î¼ÇÇHÛ\x0014ÎÔ|èèô*~{õËË_.]¾~~µêÂã_êáàëÅ\x0018.ª®æ ·¥A9D®¸×Þ\x000cíÄ-®\x001cÅ5<ªÆ\x0006\x0005M\x0008¬Ï\x0008¸~ïê\x001a=ï×³îù\x0017>\x001fþ8|ù¸n÷¤j2o°ÆfÓoyü¬Õ§ÆÃß^¼x#*_ÿtÓÍ8]?'XSðdD \x001e¯(zsZs:\x000e¶³Vt@N)\x00068
Õ\x0013\x0002'\x0007bªóót\x000ee;çì»ËïBÆ	SGç° &\x00159Àg?U±¿	S§\x000cnmýÕÓ¶Ã³¯\x000fÿ\¿ðcÄ±ñTé\x0008?·oÊc\x0014î?eQ½¹ý×uñ%33§°Ôâ&Íåù_ÏÎO\x001dih¡¹âh\x0006ÈÍ~}HªÏ³>ÈÍÎ' [>}ø_?Ý=üÇ¦$\x001aÖæ\x001cÒOòê
©ôy:üõåÕí¿¬'Òäoþ¯ÿùïþ\x000fJ¥a\x0002í/?î\x000e\x000f)jsø~ÿõ\x0001°xX$¸»?þÏÿ\x001b\x00167'ø¢6yzðzÑæa´peå÷»ÁÝ4}÷«WxoþåòÕÕåmÚ\þ\x0002o¦-pðO©~,¸û?ÿüë\x001f ³µ\x0004é/Ï\x000fï\x001fè®a ÒÔ6ÀJ3m¨J¦Æ\x001blÔs¬çÏnW?$\t¿;÷[®¶ÕXÃ³âðùîË¹ÕBí\x001d|«\x0001\x0016Ý¤ø\x001b¬È½ÔÈUE\x000f«~\\^_:Æ5 \x0016Q!@úYOG\x0012\x0001ÖÊäuàsÕ«bÏaüÚµAìm(CôÒ\x0010Ü\x001cº¡µÈÅ894>
 j
¥¿t\x0003F\x0011ÓÕ[>`»ñ'6µÄÍ8¡Ç\x0002Q¯\x0008­LJÏ@\x00081ºí´4ù"1\x0002[êö\x0013æqðr®&²m\x001b¢ß 3"vöga\x00048\x001b\x0010]x5\x0012\x0003óù¯ý(O2f"	Ð8²{®\x0016Ôê&üý?þùÇ¿'Uo\x000c¤¿lÄÂ`¹ÉÇ\x0003\x001502'É9\x0003.}XØ­02mü×\x001f¦úxÿu4\x001fý?Þÿ/U_	×wß.þrwÿG¶´njÅÁ[hj­ \x0012(­h\x0006*Z¿¼9¯¯Þ]üåêæÕÉAK5\x0011ß\x0001?\x000cÑdõÿ«Âáð÷¿Æ±øéë\x001f\x0014ÈD\x0017÷{áKýø¸(Xä¨º\x00046VôÓW\x0014ÄDçö,\x0018Î/Ýþú£¡óÿú¥\x0011«ù¯?\x001cId?Þ×ôFÍýÑÈ|"ó?"YLdñ#\x000bEÈý1ÈþÇþOZüé/×w\x0017Ï¿>üþåÓ9&ÒÃR¢\x0016¥H×µ\x0006ÿªjì,¦ÿâùÛ\x0017¯_\x0007ÒèÆ¤¿l\x0007Ò\x001eð/\x0013¥¸ËfñJ}Äã;ÏóHýéT-5¢Ïîî?¬`w\x001e,	 &8êÈÎåGÆzÅ\x0007{vusªzKþöÏ¿þþ?õ?«\x0010ÅÀ\x0006¦»{Jß¿5ü<·ÌMW@\x0006WÌ#¢¬62?-tÀa=s²ÿ~LW7!¿yöæõë:#ùÛü»ü÷¿>T´×_¿úöíî»/ß/>ó8«þvXF-L<µD]î\¼ã£4y)u\x000bàë7¿¼|÷\x000eþþõ/\x0017×<Ú*å¦ß>|ýëÿý·¬Ùó\x0014ÿ·¬ñ¯\x000f÷\x001f\x000f\x000f\x001fÏ\x001eRì&O'ÂY£HãL:Ø
yq=ê-ZÜ\x0017ono~º¼=\x0015¦¬\x0000S^*ýå\x0007#ü\x001fýô·¿¹c»ôÙÝááþî÷Ãý9B©uD
M$Tð\x0006È\x0005¤JS·\x000e&,_çðÙÕåíÍÕËÓúã\x0017ûéã1Æ_?}¿ÿúùü~ÇyÌð4¡ÚÇ\x0018tVÙ\x0013äÝâq^\x0000}ùËÍõ%ò·÷ávõÉÉÃ\x0014~ºû;@¦ó\x0003ï¨\x000bs1D¢úh\x00081æk­2d\x000bF\x001a¬põ\x0016PÓÑw\x0015ü7"ÿüóîþw*ÒJ¥Y×\x0007\x000c>|<»ÁÇ¤Hæ\x0011ûuHèSz²Ó°5K__þtõôÃáãáÛw°uü7$àãü65Dä?HX*Þ~ýöý,õYÏ\x001cð°úúÙ¤ÊÙFÓÉjÞ¾yw²å®bT5£êg\x000c1é\x000b§/\\x000b¤±¿ð2ÌÖÍhjFÓÏ\x0018\x0005~Û¼ÂXÀèy\x0017úå&Ü(Tª½³þéô\x0007OQ«îÎùü»?ÏE¢sÁ¿É~\x000c~±¬¹ô¹m=`{\x0016)Â&ë_áON\x0007¥\x0019Õ©\x001aÕ©1ÔÔ.PS{z\x0016±/çFÅÆì'ÅÙ¼\x0015)þìG\x00053ªWó\x0019wyÔ*Õ\x000c¿mGÅ@\x0015*þ\x001cA\x0002Ë\x001f\x0012ªÕ¹¶\x0004PEîõ\x0007oM1ÿ\x000eV\x0015\x001bV\x0015GXÁA{\x00125±ú`\x0015BdV'\x001f$ÕÚ!VÇs!«\x0017hR\x0013«Ë1b`nñ@\x0018`ÍvMBÖ\x0003¬à
EÚ\x0003!§£\x0000Uf\x0001S@­Ò\x000c£j)kTü9ª\N¨ðÎ  üèx¥¥nQÇVUù4(0¡ÚüDL¨¼\x0003ôédP\x000f«mYÇv«\x0012(@¬pIñMRï\x0005®«}\x0004ãªM»®fl]â-`eäa!)\x001aY|\x0004UJ\x0015k*Zêg\x0012½Þ\x0006N\x000b²r\x0011À«îdªh;«k÷\x001bÛ\x0003NË')©å\x00119u	ÖÀ:º\x0008¼?\Ý:º\x0015júZ\x0001Á¨ó6ò\x001f\x0004Ó\x001f<mÒ®[B6ÖûT\x0012®.ùR{º\x0001L8}ü¯.V7PÕªÐÉÜtî´3<\x001eAzMA¥#\x001cµãçÖ~ßÆ5$a\x0003$\x000c\x0013¡´Ú¸âM&ÖíTïMO¸\\x0007_9Ð	×u!é\x0018¡k¾²ëþÌ8ÝFeDìk ·»´î!fÃïBô®Fô®\x0011-;v
§6Òp]\x001c}\x0011ÃIgi#!ÕÞ\x0013a[z¿P¤a$4C¤æqY^Ô}ïµ½Ñ¦ßâ8TMÁp£Ô¼Fû®üFÆúyó´|7#J#ÑÛ\x0018õ1é	¯\x0014Fov14\x0011vëÀá\x001auâô­­\x0008l¹O?ß¶1ªönÁ\x0003·K>0Ú
RCOíèLs¼s;*ÙlGüÙmw|ùÔ(ÓÇ£Ñ\x0015?Øk®AÆÐ2î+\x0010Ç)kbtE®¦ø!ã^Ë£l³\x001dñg÷:jªòF\x0018\x0014îÊÛ±\x0004>ÙÉÈó0ø\x0016ýæ\x0011.j2=Æ\x0004Ê\x0002\x0001cà@RØÍ¨ZF5À(RW\x00022º2zGR\x0013"F:äÎ3£Û[F\3÷£gR|W[~&\x001c¼\x0011ö2bÒ,ç\x0002pÀV¤\x0019\x000b#ÅÁ¨ñu\x000cÔÆ±\Ó\x001f<Ícº*ñ\x0003\x0015Ã¤ßÃÇ»3õD2àdI¬¹Åà{r\x0013P=)áâ\x000bbåÆyQãwñ»ýéª*/*À6&/r²ç¨ ÒsLNÇÄÆrK\x0008;ö©gÆ;Å\x0016=¬\x0017bFòêtõ\x0013aêÊÙ\x0005LÝz»Û8Ñ³ L´2Ôf,\x0005ßÞJ¬\x001cóm¬\x000bËkÙ6sn`2
A
ê;È©£ìOÚc´3´a3\x0014-eøs_Æ¹­Äy¤h½³z? gûØÊ$÷3'U8#§æ¹_«ÎÝÆ	f¥æÄýÒ§AéE+1RÎzå5¶ú*<\x000c>ênN\x001fxÎºÃÊì¬\x001fây6¯ÒcoÅÄ#\x0015f\x001a@ÒzxÙÃYW97\x0000ÿÀJór®õ\x0006lä´ÍrâÏnN\x0014þU\x0014&°RC>b\x00048×n¤­±åì·\x001ek®<åXQù2÷\x0010TI¢ï¶J¬nÃ­ºÍVL¬ÈpyÊ¼F\x0001§1»¯¢à\x001b\x0013ösúÈÖ\x0013Çö:ZNoè³«°Ì\x0007÷s¶ÇÈ\x000f\x001c#!-É(i\x0014\x000e\»¥íþ\x001dço6#»ÓE¼äp`zö\x0002§SS(kÿö\x000cíö\x000c#ÛÓù4\x000f$vGßÀYöý±ýìqä³Ûr¤dÍ\x0013¼ãÌ)Õîí\x0019eóÝñg?§6ìÏK©([íÑü3§^	wläTÍqjä¸kÔYé6²´?¥)·ÙíÔ©\x0014äÔýNÇæRG·¦Wä,Q\x0015\x001c*tû1ÛK3\x000e]°'©JEx\x001e(î'#\x001fÄîS\x0014­m1\x0007N;
¨ç\C@¢4FîvAb{gÆ;Ó4\x0004;}tEsÓÊ)²öÊÜÂ)EkäÓï~PXD2ò(÷×Óù\x000cP§sg9o9Ãõ¬SÂJ¶J®XyåÖZ\x0016·Î\x00164\x000c,h\x0016³7yö\x001fR?4ÏeÕz7h´-h\x001cØ¢à¬s\x001cQà\x0004½¼¢Ö\x0019>ñÖïöQMæC\x0013cO?\x000cÄBBM±\x0010q!(Y"Ç»ßGHú~Fú~4\x0017\x0017'Rctq?Ê\x001ef¤\x0001RóÄS:ÚÈÆø\x0012×NÚ]Ç)\x000b\x0017Ú)Ò p¦wµG¿]\þþðqK÷ ç\x000eîKM\x0017Zù\x001ca2ø\x000e;ýéß]\¾¸ýi¥\x000bµ\x000b¨Ae3%i+iÒÙ34º\x001c°³Z\\x0011RéÓ+zT¥qBh-Jä©&X»±¾Üj6P.:«æ,Æ1\x0014_¡k©Ës\x0005æ\x000cªU
ªÕ\x0008(ªoD
Ä\x0002\x001a8©úÕw\x001aW\x001a7\x0002jÓÜ\x0004j"}zð#¸´CêµúVP§kP§G@¦K4FÎZ\x001bU@W\x000céVPßú1PC\x0011\x0017±zS×WT­\x0005é·\x0006Y\x00069\x0002Ê'IOå(Æ\x0016ÊÓUr\x001d±¡\x0003N\x0019R¤pQºRÌ\x001f
è±ßÊ9ù$ÈÙz$[9á©]páát\x0017§
Ìû^P)ý?\x0007¾»OóiÒ4Û7×-ð£NÄ¸ÿÓKa[Ò5µyÌ\\x0002
Øè@eYÒ\x0018ö|{©Ò¸)\x0018
ð´nm\x001ds`ãµ¤Ö16NÒø,ÿ«q¤ÃÊ\x000bôlï\x0018¡Ê©¢\x001fQ¥ô#¬\x001e=û¼ª6r\x0007\x000f¦e©GËÇÓåÜ\x001d¬Þ4¬Þ\x000c±ÂkÞÓºZAó&¤S[òìÚí´UM{\x0015YgÒ[YÔ\x0015°M^WçòD<`õ~åy¿U7ëªôÐº¢(}~?\x0001+ßú(>à5}¬>yûU³\x0019øæÜlÆê8\x0013å¬\x0005P\ÔS	xÚ¬°^s×ò2«ú¤X}\x0011ç¢çÔ5§\x001eá\x0014¥O
»«Óh¾¥Â²\x0000uÓÖvÓr\x000c|l.Ê\x0010Ce2,Mj\x0007'¼$Úï\x000e0ujâäÅ×ûßÏ¾ðà³«4ï
?»÷OÈ)µ%Rv¤[4ßÁö¼y±öÂcHUCª\x0001Hx5åækØ¥RH,R.ÂOýºÔ#+I:\x0004°lq\x000ccÆeý_?¤©!ÍÈJrz\x0001VR\x0015\x0011pîÈ\x0005#ú\x0008¶´#+iÊK	C%Ùm\x0002·®lÊe\x000e¤R¶'gèè\x0008*j\x0001LSÖ²Ée5e?eh(ÃÈ\x0017\x0017%\x0014\x000eû¼eaÊkÎ-c·ÝªÙjdc4 c*®\x0005\x0014¥ñAZ¿\x001fS7;SlM,\x0006£oî\x0004Wù¦Þ/6,\x001b\x001f»1§@S:å¢\x001fÓ»©BÞÐ\x001d)#\x001f û\x0008¶È4\x0006Ó\x000cXL\x0013¹RÄEëÊb*]B7já\x001fwcÚ\x0006Ó`b\x0001Æ\x0014\x000e¡\x0000\x0013æ7)\x001câ÷/¦s5%\x0006ª»)ýä¿@	Ä\x0018£æûG/\x000b§»1CsÎÃÀ97ÖM1@ù\x0018iæ\x0008FCüRÕ \x001b36q\x0004ÓSqªÈk\x0000&{orY~Ñ\x0019\x001bã\x001e\x0007»±êÀÎSgkTWS\x001cq;1QI©¾ÄÈr\x001aAN;
^bJ!q
eYO?\x001bål/!9r\x000b\x0019eyG¦ÉÝ·±(7å#¸\x001bÓ´Ëi\x0006S£|RÆ\x000cQçQáÉî°\x0008Ëäa7¦k.!ü9)ùí\x00016w\¨óHü£Ó·ËéGÓkÉ8±a0ïÎà¸5Tì?C¡]Í0²àc\x001a¢5\x0017\x0002;H©èl7¦k1\x0007î!jD¼7é}©Ëb.òý3·xÀtbçr3\x0017®\x0001'\x0005fÓî¾/e{\x0011É\x0008×Ó\x001aÚúIYN²ðÂ/[E{1+ýä¾c´³\x001bÓH~¢\x0007Ü¨¹¿>(Î\x0017¢lînÎÖtª!Ó)Kr+8 YÈÛ\x0008tc¶¦SNºh
¥ÉÓ{Îl	·ß&©Örª\x0011Ë	#Ü¨ãGªxz\x0015f·c¬Ú®FNº
b\x0014Xp(i\x0014\x001fbî6H¸ÍkÌ8\x0010äR>pú-hÇóAyÀ\x0004`êý.§?û9]ò8\x0012'ª~dçÃ«È¹¢#%\x000cÝº9Bø³ÓJw\x0003N®¤_êà9ì>éº5HzÄ )#©ëÈ\x0015ÊI"À\x0014¬û©òÝ¡
nW°\x0002ÃIu\x0016\x001eý¥üÙs,8\x0018\x0005¿½¦=ífä´K%9ÞåÊE\x0001\x0006gQr(êe×Q/§uÍqÇÝ©#aÂSÓ8Î
Â?Çn«äT?{1\x0003N\x0013ÊuÞ°8ç&«Q$)Àgß}\»n`5Ct%.çl1Ú8J\x000b§2ÀÝ¦åì7!Úã
3§a12m(ä\x0005û/v¯\x001aw\x000eösbÆ%vðYNq×\x0011x¢ûO·ÇÝ*k\x001cN
Ë6øÂ¸û"ò6´ý\x0016	¾©¥êÄIG]Ya
çîgpÐÍ\x0019Âý²D\x0010\x001dN`Íë)­çon­\x0012Ý¶	ÁãÏnN\x001f<\x0010°ø·SQë	¬ç\x0011ÑÑ^ÎÐ!üÙÏ	\x0016?{¹0â\x0018~öÝ&)´\x0017f\x0018¸0\x0003v\x001cåÎ\x0013àTÜÏtÞfÙ¯ÙÍ\x0019£ç»9\x001dO\x0010í)s"\x000b>;÷kâöÜo²qðg?§æ6]'\x000cûs%+»s·\x0014Û\x001b3Üàm²?çòÁÏÃL\x0015s.µ7ú1cÙï\x001e\x0007t:¬*1CYÎ#²mJöÁ¿{A½3\x001aÓ\x0004\x0008Ô¦\x000bO\x000f* 2Nî^Pðà¦¢~vé\x000e\x0003>]ªîd¥(yMãþP"xq3T7
>ÐiB×Dq-µ\x0006TL}U}?_Õ÷\x0003«*<óªZ~\x0017£psq÷'àbhW5þEÅÉO´+e©[ÊrFSìwôý´{MÔrê\x0015Ç j\x0002å`\x0014Ë>¾ú~¾Q\x0007¾¾\¿\x0000ª¼¬¼Qw~\x0011D*_DxxÚÖ#>ÿúÇû»4xõLI¢Ä´zØ¿%Y\x001be\x0011YmzóêÙU\x001a¾ºRHÀ^ÔÀ^\x0002kOöÊkï9µm\x0003çízd\x0007plã8°ei	zf´ÂSY\x000eg\x0018\x0002ZÕÀR«Qb\x0015¨RÝ\x001bìüÉW-ùn\x001bVúúuK¬¤Ñ3ôpÞX/?,£ÏcÄÆ7ÄÆ\x0012ËÀÒÎ\x0006\x001bÖ\x00087\x0013«z#\x001dÀx\x001c\x0002·âq]Kl
²pGpüÔ5%Ú\x001eÜªM\x0015qg]ª=ë«Y²\x0014Ë´TNXË\x00033\x001c\x000eGy\x000cb%S§äð©\x001dáX@\x001b¼¹¯ÚÙU%§\x000ebÝ¬qÐ\x0011"FcáÔE2Å\x001cË¨[ÿ8Ä¶1ÅÊ\x000eÛbp\x001cò6¶ì0û9G$ØvCØñ
WfZÃC@àoy®Â±CÄ¦%\x001ev&\x0004KZ\x001bIM\x00079{áâª\I\x0007phwp\x0018ÝÁØvKF¿°)­êåªXÍvZ]) «6S.é 
f0{lÏ£håf$\x0015ñ(Àfæ[î\x0007p¡X\x0017\x0006ÌX\x001eªÀª×/\x0004\x0011·\x0006B\x000f\x001b\x0008\bRÜqV®ôz¿|
\x0011»ÆJh7j%\x0004
\x0000f#\x000c¯b{\x0013L6Øåâ!`\x000c­TÀ)Ò2\x0006ì\x0015\x000fÏó"%\Ð\x001fÌ`\x001a#-±\x001c&ç\¾5¼\x000c\\x0011f\x0005ë\x001e7ü8v\x0018»k`;l(¤è\x0003êÇð£ÎDîà\x000cîôDNbÓ\x0012\x000f[
W¦Sb¤M0¼)Ü\x0008~\x0007±\x0015Í\x001a[1¼ÆV°1Fñ@ª¶5ÕVÁø=5¶º±møsX\x0017eà@\x0001)Ã\x0005\x0018E{\x001cZ×\ÍÖ
_ÍÂò;\x001fGËÐò*.ÃÄGêã\x0000·/\x000e;úâÀ\x001eO\x0017CÆ@+,øz\x000eñü	×ú\x0013nÔ\x0008\x0011r$g
71	\x0006ci)]Ï!¬ÍÆè!6Í#ÔÁGhÀE\x0002>è\x0012¬¶\D\x000cÿHs=Ã)«´}èØ½\x001fÜÉ*²n\x000e\x000e
ª;XòøÑÎ\x001e¸=t\x0012ùA\x001fF
²B[Ã4µ\x0015¬/\x001büªØO×ó¹eÆ\x0007ô ³`éý1²Á\x0004qÂ,ÛIwÇa¾;\x000e£÷¦ÒcÔ÷ã`	,8\x001cåªÐt;ÔnitF·´ã¤\x0001¸DS\x0010\x0016£@ì\x0012­iêõmé÷ó-½\x0003ú?cK#óÇ9óÇ\x001fù0g\x001eÝÑÿ¦ãýÜt\x000cîÿ´à\x001b.ôÝ|¡ï~ü>Ì\x0017zps`nÁñ°P¥P³ÜB\Óê´Ñ\x001fæ6zô2Ä$\x0019ÙhÔE"ßyråãx\x001dh¢\x000fs\x0013=z
Ä·ud°ÿ\\x001c%d"x'²OyÜ4ùÅçÃOw÷gõ\x000cV=SräP}äl)\GoÊPæ\x0017×Ï_^Ý¬
\x000eePS!Pðä\x0002zÍñ,l\x0014,MþÇeQ:I]MêH¥çn;TC£R	¬äÎÚµYÜ\x001bH}rZ¦8(\x001dVõíáûý×ÿ8´â\x0015e £)"×?¿uk>ýÛË_nÞÜþËYÒJ¿\x0007IÛ|ùVRÏs®
k;kÖÒÎ[)­l(Û\x0000ÐæõLæ	Tóqò¥f¬\;ù[AC\x000b\x001a@±\x0012ãJR\x001f°\x000fÖñÄ'±\x0016ÏÞHjD³Eñç\x0000©R&Ð*\x0016ysÁS\x0017¬X]²\x0015Ô¶ v\x0004Ôá,S1³$IëÚ³@¯	rÿÇ¯ÆÖdÒ0B\x001aXDZùX\x0014Î-7\x001a·6 b+è\x0014cO m}+¨+óÝ\x0014ø[¼¤¥ÑØÓ\x0003î;HuKªGv©ÐT¦7f%a0\x0007<-À¸µIt[I}ûñýÐÇ·ý)å\x0004uÖ{\x0019A¤fMGz+éÔoH[\x0019ÌÍk:
Ä´ü:G\x0013Ë\x00031W'm$­æ\x0016!élnÑVRx¶P\x001eHaZNTäQ&F¬½\x0006Î\x001aõ[+-\x0007Û^Ö®É_\x000e\x000fßÏËu\x0006Ï¥E"hÖ½U|×+»\x001c¼=¹%¹¼ýeÍ'!DU#ª~Ä(8?\x0005ÿJÖîR¥ÃYfÔº\x0019uÍ¨\x0007\x0018¹\x0012\x00161°(XRf´ÀhjF3À¨XÕ\x001eû¨3`Q×zYUÜ\x000bhk@Û
\x0008Ïã"\x001e\x0008{1+ÜÂ¿¶¬árPb7¢«\x0011Ý\x0000¢áG\x001c<ëY7PÅ2Â`ÅßH\x0018jÂ0@\x0018xºð2Ï.@BËKûØX=2Ðæ~F\x0008¥Uô,¥ÔÌxDÈe+£IÍÖU­7àÖT7\x0017¿\x001e>þúå\x001cc0j\x001aõ£x~µ)J\x0019ÊBºøõòúúÍë³u¿yZ·øoT¶õÕ¯z\x001cÜå»\x0019ëædó´îMÞÌ(9/+xÐ 0j?Aì\x000cÚ\x0008)ëtóTÖ
é\x001b)1{EÙMø·³p)Ê\x000f\x0010e\Fý{)]Ké\x0006(­Ç\x0019à\x0012ëw2$Þ-	\x0012Þû'{\x0000·BzÕ@zÕ\x000fiXö
\x001cHû\x0002Ò	ê´@äVÊÐ\x001cïFbf+¥bA\x0007/I^«2ÚG.ë z\x0011£k\x0010£\x001b@dÕÅ4½MæÓ­§)^§\x0005ø6B¢t\x0005?{!],\x0013û¤,N®¸\x0005,êå\x0003·\x0017²î\x0006Èºcz+dV\x0012C0äZ°\x0014^ÑBÙ
Y«W\ÃÛ\x000béC\x0019Úf\x0004ÍI\x0011à9ò¹\x0011»M2íR¥t½qid¡4¬Â¦Åi\x0005©­¾Ý~`W\x001aVÉ\x0003ÛhWJ®|Õz÷ZjÑ|qüÙMïB^ËÀÊÉ²TñkØ¬{)kM\x0019ÓjÊl¦\x001c\x000fÆa&_àÒ©2\x0007mY\x001fØMé[Êþ}iÑ\x000e\x0005²CÝ\x000céD1éËâì^ÊÖ\x0010é\x0001Cdá¹mÈ\x0010YcÁ8nÄ/¾,]ì¥ÔÍÝ?»)ámh-±\x000efxhÅ³¡õn¿RöôþÓc]äj)üâ<iDÉ2äòt\x000bÿVJÛX¢4Z§\x0012Ç\x001eÑR2¶E²GÞc®=â®ÿÛ¢2ÓÙ\x0011eWÚe.¥\x0017Ò7Î/þì4ª~¥#RÐT&WëÝ>öíÑñ\x0003GG{~Ú\x001dç©Git7_<»\x000fxû$Ó\x0003o2«e¹\x001eQô¼}ùàêH £²Ýa`WjÉñséI\x0004!Q²»/ØnË8°-ÁK×<\x001bVðõ(\x001c'"\x001fÃÕ²¥\x0003º¼\x001c-#ÜrbûµãÀ×ÆY\x0017üµ\x0003\x0007®c%omöïÉØ^àqà\x0002¾ìIKOzã¥6B«#qÔ>J#µÄý²<%Xï3
(''ì½u\x0008-å­\x0004Ç2ÅùÖ¾ØÊ½ï[#h\x0006þìÔA7\x001cÍür¼O+Æl¥Ô-¥î§4Á°á#6)f\x0015|ÎisZõq+¤i!Í\x0000$¸T±¡¤¢èU0fH$¾ß\x000bi[È~¯Ò¸4·,»\x0019\x001b_bäIKZí?:¶=à¶ÿcÓ·¦\x000b<\x0008®Ú¬\x0000\x0007\x001f|÷¥c¬o)û%êôO\x000fGjGQ/kõ2úö{ûïÒüÖ±4ë9Âs²ÊÓr+[)CãdÐïd\x0018íH.5}ïÈ\x0015yüµw\x001bÊÖ§4\x0003>¥ÑrZH%ô¹\x0016oZÈ#©äNÊ6¦j\x0006bª8)Ây!ÀæÜVçßHiEó¹­\x0018øÜÒ±¥DJÞzÜ»Vµª\x001fR£P\x0015\x001dïÀUX1r\x0017¶fïñ¶m2Â\x000e$#4\x0016P½(=û¡¨\x000cè#58½¡IãÙÐÇÃ*6r2\x0010TÏ\x001cTyÚºeCR/dlÜ5\x001bûÝ5pÇh¸§Wª4±²)ÃîïíZ\x001fÃ
ø\x0018ðråQ\x0005Cª\x0000)KyÐ^g­ÑÃ5­\x001eîFFÔe§P¥ògExÏy\x001d£µv½m¸Å
[Pä>Ðçm'ýV¸ÛO+Jo\x000c³$}ÿT¸ú$$OOYQoÝJÙ>mÝÀÓVOIÍÔ\x001a·&QvÃ\x0000Æþ´2´AÀ0\x0010\x0004ÄÂ%ª\x001cÑÊ\x0014õ\x0018¥¦ZÕ½k\x0019cã¯áÏNÊ\x0010m©ËP¡èàjËA9=\x0019d\x001b¥\x0014ºñ|ÓïnLi8	®Qã\x001ac\x0005ïK·T;ê¥ô3JßOl%2¥mP\x0019ífeJâFLe~÷bz\x0001öê½àæ	Q´÷²÷«ö\x0012O¿{1±29P±7¥Ü\x000c\x001d"çoÍ²ª\x00172ÎÖ²ß\x0016\x0001¤zÂ]\x0013*}(ìÞçNJ-·DúÝMù[j°4& àly\x0016A<=mcû[¢\x0016ëÌ¯C·£\x000e2\x0012´¤þw87ÅSßýÄ\x0005Î\x000fsÎ\x000fýÝ`é=k¼D¬k´\x0000\x0011¾¾ÿ\x0016TJ*,§2tp\x000b"ô¿~ù~ñüáýÙ.pC*ENÍ.P} 6å¶ÄÏÉêîß¼þåâùí³õ®k\x001b\;Ê\x000b_uE}$§\x0013xË,é`#-Æ'Á\x0011\x0004nõFº#+\x0007pÊ\x000f\x0000\x000e`xÃ=\x0012pÕA\x0001ÿ-m\x0003E\x000f°O4µÿÆ@	J
fõFì2=\x0004,«¢\x0000­dN\x000f1Üù&\x0008+;4F;¹aÙ>Î&S}G"nzmiÿÀ1L.¯±åº½\x0010üÌÁ6`of}\x0015ð\x001fYçÛÞ\x001e¾méÿ8;+à¦Õ9å¤\«ÄfSööòÝÙNÄ©tÍ©ô\x0008(`\x001b*»wxæ\x0012¨
¥\x0007äô°í ¾YPß¿¢
+\x0001©ØqÃ\x0005~*\x001bO»W[)«iªé³×ÓT·cÚHl\x0004×¶T;\x0016ÅÞiLÙ¸Ô1q¾3/hÌ½Ó@\x001aÄDºJï\x001bÒæ²\x0014<HÎ\x000cÃJr9RPeMWR®AC{àÃÈ\x0006ÅÂóÜ0 ¸5$(\x0016oRGÔ\x001fº1h¾¼\x0012#_^¢"ùX|,\x00135Ô\x001eÍ³tªÉÏI\x0006QJÉ¥äÖ¯då\x001fqM]KêFH%b/S¿7bo\x001aÇ m­½ë7÷@
\x001cAÆFµ\x0001ðÑù^òK¼nÒFÀd!\x0001{o¸À\x000fcS>×Z¸ÈÂ8\x0012a?¨lAGÎ½²ã{îyðöøËeïl?¦²
¦²#^ÒmÍ\x0017½Dõ^îqYIun&ÕJÂ\x000e\x0003¤úõ¥\x001b'X"å¬
Ë!\x0008\x0003¤¾%\x001d¹0\x0006©§jxZÒRx¡¨çôÚvÚ¡=ê-+\x0011`wARWÆ%åêÇ!m½<=äæiiK^ÑÐÈ+ ­ú Oë~Òö¾×C÷ýÊö)?\x0007ÖÔ\x0018®\x0005[m>x·¥ê|¥{;gh9Ã\x0008§õ4¾\x0016@
æD\x0011\x0014ü©Ò©³Ôé'UJuý¤®Ä°Ë-\x001f|©J\x001b|\x0004?¿ 1Yd`I«Z_zTè²¤+U´ÛIÛoÇ>þ\x0006i­Ab²\x0006É\x000fJêÛ5õ?îv}jTQ\x001fÔó4.£Gðö\x001a	\x0012%H\x0006\x0014\x001e%ÜÒ¡øä\x000b£Ðr%¾\x00194¶F?\x0018}\x0003®\x0013WT\x0007g À_êïö/hh_yaèçç
¸Û)´\x0003Fµ(¥èá­¤14\x001e4þì'
¡¼µ+®IÒ!£¼ÔJ/ûFR©¦¦£\x0014PM×Ñæ]\x0014.)¢wpåO½v\x0017õáð\x0011ÿûN *!gá\x00089pJoÙ\x000eXsy*\x0004®°N\x00035v.ªÒmÈ,ýî&Eß\x0003æÑ{êîÑJg½AÃH{Qg\x001aò¤ÄÜ"¹ê8^Ãö£Ê6 aä@DB¥Y\x0003*C\x0003ÑÊó¨èVr~ÛIãtÀô+Ô|LªÈá\x0007T<\x0011íJ3ÀfÔÖ=UCþ©Â\x0019\x0019\x0014:Â }%TÖë·+Õ<QÛiú=#¸)
\x0005\x001br\x001aJÅºV\x000f·\x00195Ú\x00165\x000e\\x0000Jb
)¡\x001aKj\x0007ZÃ?\x0002% VÊz¶ÚÖëO¿\x0007Hà)`VñH±[%®\x0015:oµÿ¶uQÓï\x0001T\x001dQÜ"¡zñH\x001d\x000f%\x0002§b¿Qu3£êª´»è¼áLÖetd\x0010§§\oGmCé÷\x0008ªç\x000foh:+¢².Ç#\TN·GÊé¡#\x0015$)ãzt\x0004²\x00086§ª\x0005¹ß¤ºÙíïn\x0013.\x000c}Âô¶|úý·\x0014\x0001j8ÝÐ§\x0007Eg#e4Ç&|Ü0\x0003GBµ¨aà!­Ð5å\x0003%eÑ\x0002¨Ó&~:CêE»M½\x0018Ù¦J¥\x001c~&U¥~Æ2:m¥w3ªn¿?þ\x001e@5eÔ¦$Z´)y\x0013oOÏºîIèOC\x0015(¥ÿq Çu²/÷\x0014\x0010è\x0008lP\x0007ëx¥N¥iüN}?òPµçA5ß|§ÂCÓz\x001a\x0004\ØÃla\x000f#\x000bë'Ù5ö ×Kp;õ£,,ì©\x0015\x0003\x0015\x0003°XÈMYJ½$&ª9R±ÒàÖ³	\x000eóM0À\x0017¿$EÞ\x00046r¹Ì£õÀ\x001eø0Û\x0003\x001fFö*j°\x0007Hm\x0006o¯²\x0007v»«i\x000f¼ïÃÑ*=mÀ DÔ×*{`?Ìa\x0007V\x0016\x001dKÿm@\x000baÍ$óñ8&öýl\x0017\x000c,ìÿeK th\x000bæà\x000f¹g_\x001fî_ØÉ¾\x0015ü+I\x0012Ôz\x001eº¤ÌwõìÍíÍ³V×Vw\x0013¦\x0010j\x0002tuî\ÚÔòôQÚ\x00068µl!`Ó±µ\x0001Pá7àÛ	g!ã\x0015\©æÚÄ'EÃ'E? Zy\x0012IÆ\x0001.ê9
árjK/bl\x0011c7¢)#¡P\x0014\x001cÃR\x0013wdVC'¢j¶¡TûPa\x0007"?ìÒ*fD£cYÅ&4&t\x0013zË¡G1i©z[ÎXyÐoc\x001aÁ\x0013cÓ\x0008¾\x0011Ã#ôð@ûHå¤Ar G\x0006·ó<W²ÈØÊVncÄ¸8\x0019nirÓ\x0006Öé±v\ë¸ÝÆ85Ü&Æ¦áv\x001b£3EÊYhzÀà8Ì\x0000×Öé[{\x001b£o×Ñ÷¯£WèNäuå[³\x001e­\x000c+E\x0010+)HDl¥ 7!bwFNÕ¹/\x000b*"SÑ­4<mbD·´bL^j\x001f#ÖäÂA\x0017+u9Qð°%¹\x001c	ÜÉØ~jÓÿ©µ\x000bÔ\x001dê¢`\x0015H)%\x0019GáW\x001eh\x0010}èû\x0011MÎ8\x0007NO¸ ÓS\x001f\x0019CÐ+%.\x0018Á£«\x0019ñg'£ò\x001cÎÊHÁC	ë-xðzï-\x0013ucy¢î¶<\x0016|YÏj\x001e7Á«\x0015-²\x001eb·¶Ý.\x000füsð°Sxoç\x000c\x001aV\x0002¶ýï4®u¼ëô½1§a¸¼#\x0011üI	¢\x000céWRE mhWÒÞx\x0019æá\x0010\x000e%2òçV"0ãºÌ6ÆØ.¤Ý\x000b!£S$\x0013,¬/©\x000eÃu½Rg·\x0005RiÓ@¦ß\x0001ûêòBà©qQEM%và÷ì¼\x000emßéw/d\x0014ôT\x0000JnNÑðÏO;¨\x0015\x0019ÍmÊ¶ª÷ÒÆÙ|i'È\x001cg\x0017ì!ä>ÿLÕÃÛ\x0013¤ë\x0004¯,'W×àdä¸µ04l\x0003\x0016z%¿²
Òë\x0016Ò÷¾i\x0000RR1¥óVsëdÒ½Ì;\x001f¯°[f[2toI,MP¼¾0:Ák"ò ÝlKºî-©ð½¥éÜÀá¶ùÜ`3"mI»2µdë¹©)óÉùØ}¾Ë8L\x000b=×ùÂùÅÁXQ\x001cÞúl¨F·ÒÃáÐûrÀÊ\x0004
\x0007A×ù±
ÛÝò·wZÍ\x000fÕüÐ}kv)ñ\x0002w.pÞÆ¯4vlæ|¿à|ß»;ÁO£«\x0007\x001eôÐ2¨âú®èxlæ<,8;?;0yBpèC.*\x0010&<"ÆOºÒ)ÖWòÑØÁX/ÿøûáÛ·Ìxwÿá\4\x0012×th1yâh\x000c\x0003[ÌhH½|õöòÝ»Lyuóü,ä¤(Ü\x000b9<FE\x001e.ç¹²Ïú¥ÉìºYIüÙK	\x000f\x0005îÛ7¨\x0016C\x0018iªA¦\x000cK
©^ÊIK3Qb[}/¥´<9À8Õp\x0018\x000cWÉØ¸,çÝN)ã,\x000f\x0017®l\x0018?\x001f.áßãD¡iMÓútÉ9	WöäêÆ¼¾¼xUÕ¬jÕq9'ø\x001a<ËD8[XAÀ!V]³êáu¥z>°k|à\x0005+5\x001dL\x000f¡\x001aÕ\x000c¢Ú\x0012·Ä÷$I&»²ªË[³\x000fUÙnU¢\x001d}¹
SÛ\x0012ë×CÂ[¤#Å·ªfTCeÒ'÷SJg?®ùt?òÔW\x0006w/\x000fÉ\x0013eÔ1¸\x0017ÑÔf\x0000Q|	0RúSØh
ã2ºÑËhkFÛÏ8µ<
Y\x0006\x0001	Ë\x0013\x0011e<ÒßËèjF7À('ÆXïTzdìeô5£ïgD9\x0003Y2&ÖÑpo\x000eîÝ¡f\x000c\x0003ü \x0007FË\x0006ØùX\x0018W&±nd5cìf4(_G¡þÈ}.¨'ÏáÈ¼QÆ|,ãAðcóà
ì8ç\\x0017»\x0011²½cú/\x0019"f.¯d\x0000\x0017VRpºVzµ2`y#dsÉÈþ[ÆD[\x0014p$\x0019\x001d\x001bÅ\x0012\x00062\x001e[öB6f\öÛq\x0013Õ\x0013Å®ØHUÞâáHIs/dc#e¿4AÑeòx4\x000c»ÏÊÁÙ¿\x0001ý\x0016Èx/m`TÅC/ÕvÒ¯ß=ëFÎä³ðÃó±y\x0000¾ûû=ØØ\x000fHr\x001a²èÓ7Æ7ö1E
\x0004¼\x0005º=O§j:ÕI\x0007\x0006Mò<é\x001b\RSwÂkÜ\x000c§k8Ý	g§!:JR+
êî²Ëx¬A±ÎÔt¦NÊ¢L\x0015%¼ü[e3­ál's¥S\x001a>q.BEå:¦G\x0014|ºè\Mçzé&Õ\x001ea&ºRS±vÑùÎwÒ\x00055ÍW-ÚWRs\x0008EÅ½'6Ôt¡ÎOsòùDÇÓ\x000c?Kê5\ì®X­Ëµe \x0005\x001a=td¢{¿¬)cqj;}ØbOÂN¸öè¼(ðÓ¶³ì\É2ë×²\x0019®¹&dï=\x0011
vÝæ?¬âðBpÇýÍx)¶8MueÁ²X\x0006S:îeP§Ü©Íx¹ö\x000eGãLqh\x000e>m,\x0017ÙN¼Æ¢ÈNâåy[Òq^¨hU¨p¤aµ\x0007N5gVuY,+b"ÑgNQwaâ#\x0019cÕºOç\x0002¥½\x0003\x001fZÅÞeãÅ#\x0003¶ºðs¡zÏqEZ³¡\x0008¦\x001cÉQuá5çBõ\x000bk¸:i¸ÑÇUÜ/uT\x001c«\x000b¯9\x0017ª÷\8UtÆuÄGeÒÇ\x001ad·áùy@Õ§êÛÏ\x000fïùß\x000eßï\x000e\x000fç
f\x0011<a\x001d®x\x0003zùB{{}ù<1>ÿËå/W·ç)MMiF(}I<È×n)ª(ý®ftcVÒøâ¹¸â0«åVì§\x000c5e\x0018 T'§á÷fK]\x0004T2vCV.Ï¡¬~JWÄ¢±ÌÎ.\x0014½ô³ú)£#GÎ\x000e5À¢\x000c\x0006Å-SdZt\x001eáàÈæàÈ\x0003V»`¼àX\x0016V\x00063æR½\x001f³9;räð\x0018ÉS7H¯\x0019®íWfYcÐi\x001aL3©\x0004+\x001dò]]\x0016sYc»\x0012Üâ6V
@Ó\x0013àç¯\x000f÷ç¿vàüSÂ\x001eÍ\x00129qÛüüæöæ<ªÉT7\x0019Z ^yAãÇrGHzØtÍ¦;ÙÊ$uaÉ$ªTqOïáS®õ62[ÙN2Ãh\x0014Ñ¦$\x0013*m2[<å}mcó5ïdã
d`+±­­¼÷­[¬Ùb\x001f*³'¨3ß\x001fE6\x001c\x0011uî`í\x0019í<¤Êá¥Êäº\x0008Ç\x0002Oj
ÎÕ,r\x0015\x001dÓÿvwørqùåû×O_î.~zxÿõÓ·³¡´[I[:<ãsq¬Ã\x00130ÿÛÕåëË×¿¼yù\x001a½yùî,rõD\x0001d~¢0ãd>]´\x0008iKÊêxPp\x0004Ù4Èf\x001c\x0019\x0015è²È£æ­ -ÇñCÄ¶!¶;U\x0011$ö.A-øÅpt\x0002ø ³wÍ^vãÌðÊf5Í¨Ù hÍ
eÚ\x001e)	\x001df\x0007#tÐ; õ¤Y(¨ ^è¾×6<Ö~®»á¿'w3\x000fRch K^R;v8µ;¢\x0007:\x0008]5M!´VãÐ¡\x0008ïÀc\x001fêº¼t8\x001e<\x001d¡n\x000f¢Üs\x0012c)ÃiKä5Iv!\x001e\x0019U3Hí[j?N\x001dd`peKÅÑì¥\x001aqÜ\x0015\x001cÛÖU6mì÷ã;[â!t¤!ªyks$QcÔäñÀ\x000fsðÃ8x2yåL!q.<æÔ~ö¬\x0007\x001d¾y²ÕCª6ÿõáóÝ÷sÄ*y¡x\x001eeð^Ô\x001a±6~\x000eÌ­nSÍ9üïõÕ/gië¦txÒøQZÍeIÁË\x0010mÉ¼ø¥°Ì\x0010®Ó5.\x001e!\WtPÃ-y\x001d8w\x001aU¾¬¤\x001cÁm$2|¾TxÁK¦ÊTC¼®LÓféq\x000cñªWò
_x]ÌµÉÀë8ý\x000b\x001eÒ£lú&A^cÇx%Ê\x000cóx\x0011ý\x000c-\x0015%Æ¿,e\x001câ­e*|©\x0018âÕ;ìË¼Ö«¢¾\x000c½ð*×¬¯rë+b\x00194#ò\x0004§<IZ\x0014Å¡eÐuW«Æ<àÏ1^£J%8¶\x0019g^cÙYViÉ#ðúf}ñç\x0018¯0äófe^ñHë\x001b[Þ8Æ\x001b¢·\x0018åòf\x001ax¯}8eFr×Èæ¼áÏ1^«Ëh<­ØþâìQÎls1»xlx\x001cäEW^_yV·ì¥6å\x0010¯n|\x001dü9Æ«Ã\x0013}ch(û:Zy6\x000fr9Ýi\x0008×6×[\x001a2VÜ&äy;\x0017u*µlh\x0019áµ¢1gøs7Ls¾PÄ*u<\x0018L|\x0014çãl\x0007Ûº¾vÐ÷
\x0001Ü3\x0012Ó\x0013¦}¥)ô%Éð(Ëë\?\x0007w¯Æxî\x001bÒ¶¯(
\ñQ¬/\x001c¯ºç6·÷\x0006Âbç>q1wd,Rx²%k\x0014ù0G>\x000c"+wñ¨\x001bG\x0013ËµVÿ\x0017?Î?þð\x001bãÃ\x001cùÃðMÇY*Ø\x0018tq\x0018kË"?ÎÅ\x000cÄwsâ»\x001ft¥Ís×'Áxøï³ÍTðÏëÃÃç*í\x0003<³f$þOÎf\x0010±Ôï\x001eÝÊ\x0008óëKøÿ·ÿ¶6«ÚÎçÛùüòÍ¤'8\x0017h<< FryàéiN.k\x0007jlPãà¢æ\x0006\x000bðÕs\x0005rÒ<+Ø\x001e§B[8áhsÒ( Ié®Wûïúüoû?\x000eß¾}ýrÎOG*®=Ñ¢Ô\x001aYcOû½\x0018zuyó\x000b\x0000?ÿËåÍ«ËwïÞ¼>Ï«k^½¤øÑÑá\x0012\x000fkJññÖ´\x0001^[óÚa^ÇU¬@¢b8iË»B-k=\x0006y}Íëy-g-ÅÔV±ß«§7\x0006pc\x001bqÍ\x0013Å¥S¥\x000fGÚbjõñw\x000f¯\x000b\x000f¨Ø\x0007¿¸?¯¿+(¿¨Ìi"·Tkò'/n.×b¼jÞÀ¯R\x00037\x001f×2ÀÕÂÀW\x001aV&±mã35éå\x000bç\x0005`oI\x0017\x0001Þ}yß¸#E\x0017}|¾æó\x0003ëG£l°($ï;\x0015¬Ö§ÛÄ'Ûý×¿\x0001Ei0\x001aµôæ\x001bð´XÙ&>Õ|_Õÿ
×ûàè
þ¾ÓÄïÓ*Fðª¬5~^×ï?J¯!ïàÓqîCÅÓê_øBs|C÷ùµ§~I,£ý\x0017Ø\x000ej½¢q»\x0005°Î\x001bàþ\x0013¢0cÊö3 %ÔvEpy\x0013 í\x0001½fª\x000bw¦Ñ	ã8b©Ô
÷\x0011VuëH¨B÷\x0019.BÆðèáê\x001føå#¯(§m"¬gHØ(nûÈê	åÜáf'ã¹þVû9ó\x0000}ceðg/ x\x0012\x0010>²¡\&©ï"´-¡íÞ\x001e6\x0010¾·tDÈÊäF­\x000cïØD\x0018Ú5\x000cÝkèJØCiÃ
ä&\x0012°LEt\x0011*ãÚ»¤ÛZûÒ8\x0006÷\x001aOj(Õ£F­ÌAÚ\x0002¨Eck´è¶5Ñs±Æ*("Ô\\x0015gÂÊM¦qgÒtÂ.Â¨J«±Æjÿì\x0010ZÏÅ7¨>¶Ð´\x000e\x0017þì$\x0004Èòr¢XÃârY»ó Ô©\x001a$½Û0\x0006Á9\\x0003N¡ÉõÕÎ\x0018ÖC3;jc[§Úö\x001då<×ÐHv\x001b\\x0018fýö&ÂÐ¸
íØíM(\x0011 ¦ä\x001cì7Øàw­¡4ºulîE4eiPp®s;\x0004ÃÞNFh}äßèZÇ\x0001w"÷ÉAÃw\x00164¸(dñ&@ôGª¤º\x0010ýl\x0015}÷*âXMIêI!L¸2\x0010p\x001b¡\x0011ö97H(Ió#à\x0001Kß9(þÎÇDIz\x0010Cl\x0017\x0011÷!bGKç\x0019\x001ckC3\x001a¤Íåÿ`båbë\x000eÂÔÔÜÌºÏ&*aá\x0019\x001f*\x0011\x0007Jd@¤i¤´+\x0005¶\x0010Vã^\x0013a;îuÛ\x001aR@\x001c\x001fMè,æ%ÌÝ«à\x001fîó\x001d
±\x0005\x000c}Î\x0003\x0000ª@
O\x0006!íWiI¯	\x0008W¦f¯\x0013ÊTø\x001f4ýÁSø5SX|ûéîþþðáoçÂàÞ¹ÈS³µ0Tdã½aqUsdM+³øöåÕÍÍåó¿¬í3ô¤:Ðf¡\x000cº\x001dÚ³ø¼×2æ'\x0002@Ñ@(z÷hÐ®vãÐÁqm¦Ö4T\x0004 \x001dûäöÈ»f\x0014Ú6ÛÃîÙ\x001eµwµ¦i`\x0000­¹DÓÊe
Ë(ôdZ\x0011z&\x0014Ü\x0005m#éÀ{\x001dU~\x0001´*nç¦¹aèÐ@qhÍ\x0012o°º*ß\x0000´Ð¼=t|¬¾Yiü9Jmi$ 
>u\x0000\x001aï$K¥\x001b\x0006v-ðø)´\x0014S°1Ò\x001c\x0015 6ÜBfüR­d\x001496Æ.¥Gw4\§§\x0002ç=Faz\x0018¤VÒÖÔøs\x001a5]
=ðu~û\x0001uàò¬eÖ0³kwh%ø2T¨NûÃs\x0005²1ËÌå0ul©wØhT\x001e§þ
0×.ÐJ³6öÑ¬ÕðÛìx\x001cö\âÙ\x0011ö:ëæK5-±\x0003ñ\x0011¹?Ì¸?\x000csGÇÇQ\x000bGu|\x001e\&Þ$aÝÁý~Æý~Üÿ\x0008\¬¥fãçËìQ\x0013sfú¹j3±ð\x0007½üÇ\x001dü«.^Ü}¹»?|¾¸¾ûðyò?p²
\x0003
2PË¯¦Tª\x0015¹üõêõ-xÑW¯¯n.¯/®¯_¯Ö3±ªÕ(1ææyV²4©KHË£ã°"í±uM¬×\x0018\x0003s¬_\x001e¹ñPNs}å2-:Jljb3LÈr²æî~ét>~¼]akb;¾Æ®T®cà*x¢,\x0005rË95£Ä®&vã'ÏÚuØ ¤î*}¤Ä\x0017Ê(±¯ý01v·°ÖCIç¼ÆEÄC-ãõ£Ä¡&\x000eãÄ)()O\x001a3I\êºñûQâX\x0013Çqb+¥XWÃ1ñÄ× ñ$n\x00101ì0ª_JSY@EE^¾\x0005GÛKoüÖ3²¨8YÉB£JòTõhæM6\x001c¾õØN.¬y!¦Î¥\x0018ß(rsëÉñkÏ9ìÖ\x0014¹bÕrPî(pséÉñ[\x000f\x000e\x001c·chÃB `ÔJUå2æ5ÜÜzrüÚÃ\x0017¾ö"çÉaûN¶ÊÍµ'Çï=[5éX¾E\x0014GRR>û&kOß{6Ù.°§£"­DU¶ò2B7ÜÜ{rüâ¦4eå \x001a\x0014UM¤±f.Oß|ðX-5ÂçfÑ\x0006°\x0017!AbÕ\|jøâÃºöèËá#eÞ¤ÜÎÈuñ©æâSã\x0017_ð¬\x0012\x0017\x001fËv¹É[¾PGkD_#Q=q|W+0\x000b[Ùbìå@­QäÆ*«a«\x000cÿÇ2\x0002Ìº²1BiSË@ó(rcãÔ°óÜVíDQ\x0018XJ\x0017öñc¹Éª±\x0016jØZx\x0011Mê\x0014Õ$U¶Ô
\x0019¾E~{Lê\x0004ÿdp;#m¹K\x0002\x001d@í¦»d·ë	ß0\x0015ZNe1\x000eeDMÕÃó
»\x000bþøû7p]cxëLl\x000bd\x0014&+Stë\ÑÕñ´ÈÕ;l1xõö]
rakµ¯'ÁÛ\x0016ÞîÇ¹«Ejõ<GpÚîc²ûÝïd÷Ùà	OÞI_àO¶WvÁÃÅ\x0015c\x0011ù¼þúðéÛÅÍáï;|¹û¼%NÀL\x0010<y\x0005¥¬hÛãâO×on_¾»¸¹|ûË×W×çIUMªÆHCh\x0004S¬(\x001eÿ~\x0001PS1PWfãEQfa'¡GYRWº1ÒiB^,Ó\x0014*ÑRw¤0c4Ô¤aTy[¤!7,ÅYni¿4Å\x0003¤U\x0005\x000f\x0018C5CTj\x000b¥û×\x001fºï%m\x000e\x001c;QÒÎ9rÕdàÓäëöb6ÇI'©K8%zYÉ¢#ã÷{n&U©VW^»}ª\x001bÑ\x0017_\x001fî¿\x001c¾};à\x001clj¶!\x000f8¢2¥Di«Zxñæöæõå»w`þÏ\x0002;_\x0003;?
Ìjó(çE´:\x0014\x0015Í\x000eXYggìSÙptÐmªEd¨QÝ¹"\x0017,ñË1bå\x001abåF×\x0017\x001e\x0015TR
Ë\x0013\x0002\x0016\¯,+\x0001GÕ\x0000G5¼Ã´\x001dÖ«\x001b\x001dSeJ%ªî\x0005ó¬¨lG
¿¸ËÂ\x0005çs_bj\x0002Õ,])§1´þztJà¾¸Ê²\x0005çIUMªHÁ\x0015kU\x00191v
Â26BªkR=¶¦ë'd.µÍò\x0008Gz\x0000zHÃ<'\x001eT%PÿöÓß¿CÄ©rbÒ¶áD¸,wìq!JØo_¾}s\x001eMÕhª\x000f-Hnk\x0014Nò\x0013@ê	íäªmlºfÓË\x0016K \x0011[ÉhÙT1G\x0014ÙºØlÍfûØ°\x0007gu8Î@Hå9>gqÛ.6_³ùN¶Rtð7åAÒÊ\x001c}>ÏfÃì(ØG\x0006J¤cûêðéþÓù±½9®C\x0015åq4:2ÕFJ¤SûêòåÍËU¡0;\x0018\x0000ªFAã4ð"Ç\x0012ëfé>\8s# º\x0006Õc a*¶
Ad¾(¡Ì\x0011RS!RëÊÃXB*8å!ã²zÔÖ¤vÔ«)äÊ%¨tIÚ-3`#¤®&uckªX\x001dAHÁ¦²\x000cUqùÜ\x001c\x0001õ5¨\x001f[ÒX\x00068cÉ\x0007&¾¬ÅR¸i\x00044Ô a\x0008Ôèr1
ÍÙO\x0011XþQÇÙ¥±&C¤x³` \x00055ªæclÑ*Ð&_\x000cqj\x001e&\x001f8Ï	ÿ2¸{ÿ\x001eál¯¦±»)èIt®\x0014pH]òÞÁÙÜLrìjÂ6\x0014\x001e3^\x0014åç\x0014éb\x0005#¨ÍÝ$Ç.'ïY\x0014\x0000Ç¶³\x0003¬JYåR\x0002m´¹äØå¤\x001cJÿ¦E
úûÙE]öq 6\x001c»À_×Ó"\x0017JpD\x000cNÔcRÙØ|9fô
G\x0001¯&^ÏG9ö\x0015cfT[Ê\x0005Ã\x0006Î{ËwèNí.Ô æïHQ¿#á¹{^ôÙ:QªH¢Iû85Kì-<rWÅ\x000e¿#EýÜV\x001e¹8	¼ìGv@íÉb[ùtÍ§{ù0°\x0015\x0019OW,³öôRÛ°\x0013ÏÔx¦{ù\x0002+jÈ=§¨¹S\x0002ÜG¤gúølÍg»OaLé,ªî\x0010e\x0014³=zÙ§ô<h¥§ÇÚ»û?æâæÓïç(Õ\x0010\x0014
ü¨ÔzY\x000fð«\x001b8½¯/n^¾¸¼ýé4)x§í\x0011FÁQ:Â	æâòËÇsYW4ª<Õ°¶'kiËë÷xÌ%ýÁÅåëÖR­Ì¨jF5ÀXf¥²
r.b)<²ÝºfÔý:<\x0010IQO\x0004Q*KìQ%Å.DS#eSMá\x0003ÇÊ\x0015°EÛ\x001c\x001fÓÅhkFÛÏ8µú	Wæg©nËèýÚÕnàS»S\x000b¥DYh=®IÚèkD?°ºø¸¾4G-Ú¿¡f\x000c\x0003±L\x000e£½ÂrÉ\x001cOöv1Æ1ö3J_WxPï
8<|¬U½²5à\x0003\x0016\
\x0016Ë=È¾`Ù!â³{\x0019\x001bã(\x0007¬#N\x000f.l6=¦äElØ¿é\x0003¶G(\x0016\x001fªjO\x0006ä\x001eOlóëZæëzz\x001büÿÏÿ{õûçOßÎsÆi8\x0006ÆPBêË3=\x000e.®^\¿|·TÕ¤j4òÌG¸­KBÇ\x0006UVt% ´T×¤z\x0014Ó\x0014´AQwQÎcK)\x0001P[ÚAP_ôñ«.öh\x000f§Ð¦=Ið\x0007é$5èÏ¾>|>|<K"¾âÐUÜáeå²8¸\x0011FÇ\èåOçq+¡MÀUs	÷­¸Z=¡r\x000e\x0015Jý¡±üä6jÙx4\x001b\x001aÜ0k$+üê¬!õK¹Ù\x001c¯<\x001bÍ\x0010\x00077÷eb-*ÖÐ¨j\x001ddËX:$#¸R´{WòFÉ\x0013`´	<\x0016Ø±Àf­\x000c¸·X\x0003¼õÄ¾íP^ìÚë"YìpÞ!\x0004qc\x001b\x0007wj¥ÔS­Ö®(b.SC¼Um8ò6µá=Ë\x000bVªða-9Mh%\x000b5X-O\x0016öôñº×
òÊ¢ë¯\x0001
\x0014lï#\x001d7­\x001b^­\x0007÷µ2Ô^L#9 få#í_í[^?È;i}j\x001fYX\x0018ë{w)Ü1ÄkËB.¾t3ª\x001c0Bó;Æ\x0008VÐY>chhh\x0018¥Uj9{\x000c¨¼\x0015©Î1VÙ²ÊAVæ1nÌ\x0001\x000b]$¦\x0001wçI6U\x0003ë*ìêZç0¥\x0015>Þ}¾ûôå,/xPL\x0013²t\x000bØ/
\x0002°ôr`J,ütu}õòõyÞI
\x0016y\x001b%Ø>Þó\x0001\x0012/\x0006\x000c,ñÇ\x001bµ§{¥h\x0016\x0018\x0011ÈýÎÁY£awàíò
¯H)w\x0001\x00168\x000c\x0003cYQN6aÆ¶ñä\x0005Ô{\x001câØ\x0012Çñ%Ôwè¬4eS\x0008r\x001f¤=¡ë
#8tÂ\x000c\x0003{J\x001aN9ã9F\x00135§E<·\x0001Ã3è7\x0010¬\x001a,\x0010þ¬¬\x001aÅBÞ<;iÇEgxúXÇ\x0001/\x000bMÎdðË`ÍdÒ(\x001aòì§Õ);L[Í\x0013$Þ÷À\x0016\x001e\x00186±¢Ä.p»}ðq)×;\x000c}C\x001fF¡%\x001b·\x0004m\x0008´#\x001e\x0003ZúyÅ°O\x0015ÃEùëáâíáþûù\x0006=lÎ	%¨¬\\x0011Kº\x000c\x000f[Ææê×íÅÛË_Îtæùyë¬Ï­³#°z\x0015~êx³¥Æg)=<\x0002;
\x0000GXcÇ`.éþhØe%6?\x0006¬k`ÝðÊ*®M0r\x000fw$K·, éÿ$<gfr&á?\x001aVìÙý§ÃßÏö\x0006ðvrª&¤ü\x000cØ4Oå\x001e\x0006\x001e\x0003§&_]<»yyùúÅyLßbú!Lm)ò\x000cÀ&·½Ix\x0019^»4k£\x000e·JW
\x00021èð\x0006ÓO*ö¬n¤Rseb Tã\x001e\x00055ÌPÃ\x0008ªQ¤}\x0004¨*k+K¤tåÉ¾44\x000e|~ eùÊ&z#§$}oà\&à\x00078g\x001f?\x000e}|Ç
dÁxCU^
|qFõËÌç\x0000ª¡º\x0011T«ÐzGê\x0003°¨yþ\x0019nÄÚLZ\x0000\x0014,ª\x0012iQ£¦>,ªgÔ¸l\x0018@53Ô¡ïo4Ei	¢J
g\x0010êZþfÔ*DPÛ\x0018ÍVT0ü9\x001e\x001al\x0011vTpºèôï½âYmEõ±Eõq\x0000U\x0007K# à-kIÕY\x0010\x0008PMÜ¿WÃÌ¤1êñÝPá%C=\x0008
\x0000É\x0000IÝ³WóÂ\x0002ù4Ô­7¾\x000fÉ\x0018¤Í\x0015\x0001nSzmaõyvPDXJdN]7/_¯Ec1Ö±QfÃáP©z\x0012\x00105W]\x001dé<è%Ô®&Ôn\x00001PÎ\x001eõ±U43rM¯pKÑ^H#kH#û!5;x.Í¼¤Dá
\É¾Ñ±\x0016hÙÊh\x0004M\x0017²&\x001c1ò~<"\x0013Ò\x000bé3ã\x0007\x000eå!xè»Ü
\x000c.RXè¥ôw/dÐÍÁÖý¥¯\x000c c®²Ã©«åÂâ^È¨­\x0006Î¢-ÎGRèEó\x0013x xÜ½'¥h ñçÈRæ %æ¼æ¤\x0017':á{!o ïkÊ¸]P[Ô-ß[-Ë¸{)µm(µí_J\x001c\x0003æéûR³¨H	\x0006>øé\x000b|+¥m¬yÒÑî¦t\x0012t\x001eG[Q\x0011­â@z\\x0015×ØFé\x001bs?û¿¸(k	;&+sÚ\x001d ¡è^ÈØÊ\x0014î¬\x0003VJÿá\x00084'}ËJ4»Rþ]-$t3zþØæ?\x0003á²Nh3¢pú·vD°ÓyDp5N\x0000º¿Û§»³Ê_2à\x0005Iýx<ßÃªÈ=nR.§UWÓ\x0004pªû³7¯_¿¼Z,KÐÕÈ[ÆTÌ(´T¥9ËFj#SQó­.Åê¬.j«\x001bjü\x000f\x001e¦æÄµ*äÑ@HMöôÈ³x9´Ìa\x0019×UU\x0014\x0005\x001cU\x0014Üý
Îòéc/ul©ãøJûHbF.íïtwilÝä[aÙC3JílCíì8uew¡\x0004ÍPèÝe\x0007ï(tl7u\x001cßÔ\x001e\x001f\x0001ì`K*.S¡(1-{\x000f\x0007nl\x001eþ\x001cf6I6ojM!\x0015\x000c'SÀ\x000f];×Em\x001a£?ÇWZ¡×~"Z6_±Tâé¦ÒýÖ\x0016 KÆ¨|þ|Ç×¿Þ\x000bWäVOC]vp¯\x0004rÌâ¤=²¼X.¯¯¯8íúóµp\x0005sÓpÂ¡ãöþ IõN"iì6ØC9/<©ð|
þ¼8ßË\x0016"jåDeôÙã1¨\x0010ÅU\x0018zYr>\x0005~Ö\x001bÙ\x0018PÕª\x0017\x0010\x0008)
\x000e\x001bK\x0012¡%Ë\x0010ÔZ=ì6B]\x0013êþ%T|õ"a­\x0005k¨&Â/ì­±&ýJ \x001d\x000e\x001fÒ\x0008I\x000f\x0008O?¯7\x0012ªP
 zJê8ì\4ô=f\x001fÎnÄ\x000foßïO"N\x000fÂôm÷N\x000c\x0014Ö|ñ\x001b´5VQ,ç6u®â\x0014"O¾\x001fQú\x0019/³\x0010"j> .\x001bh{\x0011\x000f­»?t\x0008
°\x001döfH>ÏWQ®ÕÕmBÞÔh]7¢cm\x000egñoÉ(*=Â*½\x0007:4{1ôïE+Ki\x0017¼TóøR\x001cTC'Ú¯fì¶ Êö¸Èó"yÎÃHÏçE:
×\x0007ðö2Úf3&¯¾ÑcM_ö{L(á2É£×kõÉ\x0018«AªÈØÖ\x0011lbÄIÆ\x0018r»
 J\x000ex½óH+Õ\x0010âÏ^ÂÜ`\x0010q\x0004M.Û\x0013¬ã\x0018àõ¿éÚÄh[/Âvû\x0011\x001e^Åü¥\x00155R\x0000£áÈók)®m¶eì>1øÞ¡{ÚHjT\x0004F~¥ann%¹¹Q·ë¨û×Ñ9O	XcË\x0013bHÓ\x00172¢Øû©µÝÓÝËèÐ×ÎZ+5\x0002càÚ®fÞ70J\x001dUk\x001cã_«\x0019\x0012»)óQÜ\x0018q¬¸û©ææKæ}/# Xòla!%YÇè¹\x001c×\x001f\x001b)ïfwÝ^Yp\x0017JÝå»pÁÜyjòÃòÃÀZ\x001aYÖR(^KYÖò\x0011(ÿ:£üë\x000f¹\x001fg\x001fHÊÃò0ðÅ½*_\Yþâ¶|ñqÿ'¸Ùã\x001fNâÔuþpñöëýïçå¨\x001cÎ©"µ"[¯É¢\x0014}ämM]Ç·\x0017oßÜ¼X¢G{«ÚÍ7#b>çäL£}Ì4'g9êfÔ5£îg´©\UH%M©2C/c~Ý¦f4ýA\x0014F~½âà¬¢ÊaB6Ý¶f´\x0003ë¨'!\x001bm$®cÑ,:¢ÅÜÍèjF7°\x001fã\x0013íâ\x0005Å\x001eÓê±JÌ)\x0015Ôí¾fô\x0003ëXº\x0018Qg4ñ\x0003\x0016¾õÒ>v31\x000c¬£}ÂÂ!®|j#ºÉ²¢\x0017±Ò\x0013Eë(\x0006\x0018%ºâÇaªÞ/\x0001ÜjÇÛ\x0019\x001bó(\x0007ì#~ëP %O£TÓBî°áÒÌc>¦ù|»øùëïßÎQ |¬/ê\x0016ðO_tV\x0002Sï.~~óúwç0«Ä5bÊ¦jw+'öÉñt3Éqh¦¹º+aÈx\x000c+NüÙÍÍÔYÇÌXö-ã\x0002\x001a¬\x001dçÈÖ»ÀjÙ$>\x001f.n¾>¼¿»ÿ~vj0å4úIÚ@ÍPÀÊêÿZ-­z[º¾¼¸ysûìêæÕê
Ó:\x001bH¬Æ5kçIç¸\x001c-8\x001e\x0008­õ²WyØÔÄfØÆ2
ÊR\x00057\x0010[ÎÂ\x001a¯\x0015\x0000t\x0011»Ø\x0013kl.Áw´-+\x0003è#¢­£Ä¡&\x000e{)'iÆN°E÷Q,\x0007.
âN×V:vbÏ\x0008$S©¨T>í	¾¾âÒãëEÆá¥@)ßfjÍ³Ã·\x000f\x001b\x0006¬xTÃ\x0003Â¦¶¾P.ùãì¨×þòÝóÕù*Ì©kN=Ä)Ê&Ç^¨àØE="1>ÀikN;Àébà	®\x0012«Úx=[\x00103¡\x00068}Íé85\x00068uü@_tÐãqAÃ­b6L\x0004Á\íòóá÷Î\x000e>Å#ÎæGËÍ©SDÏíÓF×åõå«g/×¦Ù<\x0011dë³mdEíÀi°\x0012×1²*\x0008l"ÛIuM:×gÛ¼ª\x001a\x000fáà«R\x0018*@Ûÿ\x0011VS³AÖ@Így\x0008\x0014¡¦Ë /ë²2°\x0003õ=<\x0001~«¥á4u6:üñw¸z¶ëT\x001bÉOTw@zêK1i\x0014\x001fíº|õ§¬V\x0007jÆf[6û#±ùÍÿ\x0008l8~`\x0016¨SqÖ¦ÿâþðåã\x0005¼\x0000ÎËM;ZTti
\x0016eû¥ÚOÕýâæòõO\x0017ð\x0008XÇPó\x001d\x0015\x001b?º\x000fW$IPGC.Ø¸£\x0014M~¥ÄªÃNbS\x0013ñ\x0005Ö8Ü-\x0011KY"y\x000biå\x0011õ½^baæw	ÏôíâÙý×w÷î6<ª=K\x0005JUÄÀÄ¤æ\x001e.t¾;ß]<»yóÓÕÍË«W sªS
pZQfÿ¢#ÊÃ9T\^G\x0003ºæÔCëé¨Á\x0007$ÅÊa9yþ\x00078MÍiÖS²æ">HSÙ1Z.\x0000z8c\x001a¥ª¦õKY5M]?Ýýã<f4ÓOkXÉÒN²äj)\x0012;õ*ütõë\x0016HÓ@!HÊ(?1r\
ÿ\x0005{\x0019«Òs`´±Ñ\x0015IPx\x0012²¿²Ì2S+M\x001fÛ +7¬\x0005Þ6/¤-âépK(lä\x0011¿`8Wzg¶1úf!ýÈB/LµÙ¨`ìx!YáÄïÞr
î!¤Tj`%\x0003©1¸h\x001d\x000båÙ"Ç#õÒ#ÞN©RÁN\x000f\x001c\x001aÛ
?»;<Üßý~¸?áTRã\x0000òU\x00164\x00167\x0018¯Ö:Ü¯.oo®^\Þ¬ä93®¬l¦Â\x0019äÕ%\x0007¯Ñæ6w-¹jn¥_·\x000b·Ò~U\x000bí×\x001eÜÀ¥Ïpõ°VÔ\x0004¯5­Ú\x001eÞÐòQÞR}
kJ)FX^k÷tWg\x0017¯j×W®¯\ç	õñp}I)ØUÉ\x000e\×âºq\ª§Ôµu\x0011ËÌf\x000fo»\x001dÔèvÈ¾^æÕô\\x0006ëÀ½\x0005vµþ³·jÞA^-F×Eí\x001dJYç)¬JkÇÛ×¬i\x0017÷ðú×\x000fò
Ë\x0015hÉ© Ëö]NÏ\x0019ãm÷\x001eÝ\x000fRqw­6<í[©(x?ØÓâ\x0018ÛxUÅÀ\x001f´Ñè­±sõMÑh\x001e\x000fRÆx-cýSLrK?aN:h2h#4Iái%¹Æ\x0008ÿVË36j\x001bT;ê\x0014tJû&Îî²¤Ö6v\x0013yÓ%-CDU\ËDlE­Õi±5ç\x0000M·Væl\x0004J¹È/Á¥×=ÂÚ\x001e(1v¤¤%·\x0016^­
^£
\x0005u±\x001e@UºAUz\x0004UGÃ³8$\
$ô!dA]ê\x000cõ J6«ª¥ÀsV\x0012À«¯\x000fáï\x000e\x0017¿Þ}935Oáô\x0002~0\x0004'¨OJÇãyÅ1ñÓáÕÛkø»Ë_¯^¯
ÐChi&umN¿\x0007±%ü9ØH5\x000cV\x0005\x000e_\x00058q+ïNl=ÃÖãØ°yIPÇÉ@\x0005`*¬Wê\x000eZ	\x0019lÄ\x0016*e*TõLOÕ,±úýûÝÃùÁ2Þ°¸_ª´"YO­9¤y¬@¨Î°ýòËÕíêlZ;52µ®
 :.Ü÷¨\x0004MukÚI6½nÙxÕZ3D³­¬AMËê=Oº0:r6Ð¬'X7²ÊU±jËµ\x0016"\x00041Gà!]ë¹õ¨J4¨J\x000c¡Rrg#W$)õWk\x0017ÚyT%góqá\x000f¦á\x000fï¿>Üüúð\x001fç0ñÙÀ¬¥\9Íêø\x001cÕw×ÏÞÜÞüôæö_ÎCª\x001aR@\x0006.\x0000\x0011ÑñgWJ0¤;úÙû u
©G ËÐE)©ÂRaÃA\x001e=D}¦F4\x0003¨ÞÈ¯\x0001Á3xà¥Ån©\x0003ÕOéjJ7BYD\x00110çOÓãð½]*SN¯ì¡\x000c5e\x0018 t\x0007Ø`.Ès9¿-ÞµØ¿U\x0005\x0015\x001eo1²BCé8µ±7Æ\F·c
ªÝø_=ýÁSüY½«{Ô;âÔi\x001beÈ±w-d\x001dÂ#S§õVÅ\x0011DÖ-²\x001eG\x000e°Àg\x0015Tþ­ÀÇæÌ°]k÷ïA6µ\x000ej£ÛQdì\x0015vä¸\x001cÛÄÔKIe¯ôo\x0004Îå)rò¤"­U%áÏ¿>üã¬
»·È¹zØeTþSZì\x0016
ðçonÏ¸¦¹Ü«%ÒöczÉZ¾.N£î´àv\x000f©Ö¿s^\x0018ýr0ç¯[jþ¦Df\x0014¥æor ó\x000eëÙÏß¬V¨\x0011¦ª1\x0017S97a*[¹N<j\x000bâ©yF®ÜijÌy\x0019ÕFLn¹OSN){­dÓz²«\x0003ÓÕn\x000c\x0013c\x0014ùÇ2þINO°Vëu\x0006SzÑfQ\x0016À¶}\x0015ð(½?|<.T\x0002î"nìÒÅ»eÐÓDÃ&Ýwø ½¹üi-eaqNN\x0005?\x0007h%Ú£8
°Ë_\x001f,\x0016k8µÉ(\x001bhß_Ö\x001cûgð\x0007I\x0016éë\x001fïïr)Ð¹O=Sâÿ§îmë¸Dí­p\x0003Í\x0000\x0012ß¡_ÕA}\x000c%9¦çØ¶¦iÑMnwÿºÛ¸;¸ï:îNîJ^$\x0003bSÀ)i;ÂÕ"Ý£y
\x0005d&ò3¯hÔ¡X\x0001§\x0010q¢Ó\x000f´Ì}ùüñyÎÿy 	ÌnÝ:pZ\x0011Eg7èúøéúäùÕýÝÇ}Ãeâ\x00029>ç8¸%\x001f)4#1W$wv©g/ÎO½½|¶k¸Ý2î\x0011X\x0003\x000b.§Àù2T%Bd-¦ß|ØÔÄf8§ÕP]\x0019³\x001eÊ5TLKwG]MìÆKÀÛ>µDóçTi?p¨Ã!À4U ;-17i7ý9uÕA,·g$IØ»«ûßO¾ûxõþnAfÕdúÙhµd\x001fvUæJÀ(
g,ª³·ÿyòÝ³³';%,qBÍ	#Ç±ÛC¤\x0015Å­Ó\x0017í\Åâ2No¶Ö3n¯­SË\x0016/ÉB>7¿@\x0003Õ\x0015ÔôB]O\x001aÚ[Zi¶3bÂ\x0008fdcÁ\x0015\x0000 NîFÀÎH\x000b9UÍ©ÓpZ°Ä~~t[-þ½\x0007Òp\x00060u©Ó\x00080<;-"qî3¶ÓÔfh9¡ä
w*x{ùÂ´å¶¦´«Yü=bSÐ_\x0004¨6õëáÔÛ\x001d&t\x0013Kvô÷·_®oöÊyë¹>\x0019\x000b|\x0002+PÎPÞØ£{òýË7ç\x0017û\x0019UÍ¨F\x0018e©AÑÅë,%;P\x001a|\x0019\x0015jMí6§\x0007\x0013÷]=pòñÇ½#\x0005!Z±Yÿ\x0000~ö¼#1ºÏkSýSæL>~¶{úaR>rã3Ãtü±Nò¸ºÛ«}@à£¬}¼vsö7Ç\x001eh6»:Ï.w*\x001f¡ùa«Ñ<âm@\x001fÇ\x0015%Üwû«=¼àÑßñ¯¥5Ó}¢®/IÓ}ß\x0010õã¹þéî\x0004
´qjMùzF\x0019	r£ÝçïN}øQbTÑÉosgß~úRúß^\Ýÿfy£ÖÉ¼¯î>þvõ%,é%õÀÁB>
\x0012-p.""Û(­*äWÏ~8{SÅs¿|ñ¦´Ã½8{û_óþ³\x0016=je8\x0018\x001dS­	\x001d»?øî4£ªÜo=ô(hÔÁè"$çjPQ"R«©¸èÈ\x001d|
ðøwê5ÀS³Hn¨Â\x000eÉs+ÝH^\x0007×C[Ð\x001cî²\x000f>¢G='3¹É­,6_cÑ£á`×Øè\x0016ÝG±\x001dh£çËMD÷5¾\x001ezÔúîðE\x0017¹m9î\x0017ÌØË.xÑmÐ½\x001ey¼úÉ1D'r)m\x000e k)ÜË*ws=òøwÃE:¥\x001cÆ5\x000fp*\x001ctO\x001eôWXt´G¤8|ÕCöäc\x0014ä\x001c4lmïhÕÕWXtLÙ+RerÂA$\x0007Ð\x0017W=XF¯ \x0018±pA\x001e®H±\x0012-ºIjiÕI\x0019yS\x00151,$¿º{ýë\x000eì¸\x0014òp%ª|®²Ã\x0015\x000fÔbG&
M+^\x0015¯®·äQKÈÃõ(Î6\x001ddH\x0007pÅ\x0015\x001dÑÐ¿ä\x000bÈ£
«Q,r \x0003êqÇX$r¯õ×8¢ñCÊÃ\x0011\x0012f\x000b *&\x0012-9g4;ø\x001ak\x001e\x0017C\x001e.Ñ±±¥ÝbÈH¦ÕãvÑ_Ãv\x001fß}ü:þ×\x001fÓVÏo Öxof²ßþSýòî×êtquòäöó}8Ã6L02\x0017q§Á°6\x0013+1â<yùz.\x0015ºeÉ×£`a\x0019|\x001c0$V\x0003&þ\x001fã?G\x0001éÐøÏÿ ÌïWöóßª³TuêÂ>~¿\ßÝìá\x0002~¨,}±,*	_ÌÕÈ7\x0001ý\x0002·¹ª.]ØÉïùùå\²AËÏØ\x0000c\x0000s6"£ðÔ\x0016\x0011\x0014æ=æÅsSb\x00142_iG 14\x001blX.KZÀJ\x001e\x0004éáß¿ºV¾±ðô<Z¤?çHÝë»¯t\x0017+zìSJi÷X9mb¥%;:´øÅJêÓó³Ë'ßçÝóËg¯ç¼¦-rÞ ãÈÂ«â&°ÁK%\x001c»	ê±Ñ\x000b\x001f4â+Þì\x0008;×Rpä\x0015§"Ù\x0004ñ¸9Ç¼rre:7\x001f®CxS±Yv ¥>\x0005W1¯²«òf§×\x0001[X\x0007¶\x001a\x0005\x0017ÿÇý@\x001d\x001fp\x000b»©~\x0008o\x000bðZ\x000c9f_Q¹âà\x000fâ­ë`VàÍþ­CxáÔIhu.A^¾Q8;µÊ»y¾¹¿ûJ¤UaÈ\x001f>þôéêfV
J³ \x0003'hnÀw0Ó{O\x0015üáÙÓ\x0017g3Ñ³\x0016/n¼ ù"éf>ã\x0001\x0005s£v}@Î\x000eáåÓÔ\x0017ÿ\x0015\x0015?D<.}\x000c s­iÄ3SÔ\x0010^ÞÝxQ\x000eÉüq5\x0004#98â\x0005=¯Q{ð²_ò¸VÏßüã÷\x000f²:\x001a\x0017×'O®n®>ÜÞMwq~òäìâìÏ/ß.\x0001Êáòö?" ¼á\x0008¨ñ\x0015üOsý¬ÿ)~ýPïí«W×_>~¹>yswõÛõÝçý\x001e\x0017ujBö¸àÀqÐ=.ð\x0000ØÙÉ«ó7ÏÞ¼¹<ûáür®P¯\x0005¤½Þ
(iÎ \x0002ÊSK\x000e\x0015Çx0qÞáÑÎïÇS§2YÓñß\x001b\x001a&N²¬\/MÝ|ÎCN)Ãå\x000bè¿O| éÆ\x0017·ÞC×åmÀ
\x001d\x001dÓîÕ\x0013i²r^=}ê8îÇpÒ®´zY1õ¯^.\x0013É|\x001cÝ\x0013ñ\x000c\x0007\x0006ô\x0007\x0001^ë_êhÿï«»\x000fûË\x0014Ä#¹\x0012µhù\x0002(\x000e´Ç\x000bý\x0004°NÃû_g¿vVùÚyÄY¾\x001c\x001b üûç¿ÿôKu±¬\x0000_ÝÝcÁÚ^BL»7{#i\x0013âP"\x0016ÑVL¬·ðÕå[¬WGüÉüòåÚUkøæêîÓÇ«}X6\x000f¦Í÷\AýU *2\x000eÚ,Ü³Ë\x0017ÏÎ\x0016¡äÕ:
,zÿçP>Üþíýßß?`ÿßÄMôôúÓÿýÿ~»[²\x0010 D¥m$ÈïãýT±}\x0011÷ÑÓó\x0017ç?\îÜIÿþýò¢1$?<¾}ÿóÇÿûîö^}Î~Mq7+È\x0006\x0000Æ¨þä
`_>ù\x001e#%¯7£ù\x000fS.R£=\.j&rì\x0002f¾Òù\x0013n\x0013V8tqýzÿéÃ§ÛäoÿDòñíç÷{ÔÅñ+ä!õêÔç|\x0019çø:gÂ\x0003@çõY\x0014\x0013¼É\x0013¦_¼ÁûÇ÷\x001f÷¬S4%©1TS\x0003íÑ\x000cENÍäÂ¼=yüöÙü®*hP£ÁQ¡©\x001aM\x001d\x0015©ÑL\x0017\x001aæ¿\x0011Ò\x0005Í[eÖÌ$«,Es5ëCS0\x0006©R\x000c3êHfíÔiÙæk4ß÷A©\x000b;iòWã\x0007üA§b¬\x0007Mæc`\x000bÿ7÷W)v"\x0005££|¹úéÓõ}!½ø¯¨1rÐQÆÚ-\x0002ò¹T¨\x001b\x001fT1½³×oÎ¾8óæ|V®Éüôùï¿5Îh\x0019^}ùùãuê\x001e±\x000b+*G2¼ö2×\x000ek©CîjbT\x000f]Ú£Mxö&
þ·ÿ¹\x0004Âå=P>÷\x0000
Ê\x0008&
LdådÛw\x0012qÞq­\x0013'ßõPéß¨¼§á_ÒHÃ.\x00173q»/úéîï7þ}µPOn£¹¸ïø9CÃÂîc@\x0002Uä¡CVE¡õàB=yùüÍ\x000e3Bþýêöçi<3'±\}¼û¸?GngóÕ-g%m\x0018¤\x0001åÌ³gÑ2$/AzNÑ¸e\x0007ö\x001c®\x0004ÌäóëÉÑ`
W.FkBR}«&4­\x001a\x0014ý\x0018\x000cÇLê9\x0003=höoûýæßujÏ5öâ¸¹þBxKò$¢v.ß4\x001a\x0016$ëÓxêL§üäÚ.Ço/Îß\x0010aÎØ	È\x0002l\x0004Æ^`{KÇr¢\x0015Ë©ÓA< Ëñ	å·¬YåkköÕí§/'?,\x0010"2ª#M¶<¼¤´)Ù&J=Ðy/ÞüDÉ¬JW~Ë²U¾¶lcJÉN\x000c\x0010\x0001\x001eä4\x0004öâú0½u\x000e`ª\x001aS\x001díjê\x001aS\x000f`*aÚ|Sö8G&­¦³,rÄÔé<ijLÓ\x0019ÁJ\x000eÎsÈV{ÍBÛL5Ü\x0000¦­1íÀjZ«pQ\x0003öíOÒ³­r2éjL7°F°4\x0002§x5±/;¯¦Xc5}é\x0007VÓä(PìÅ\x001a<\x001f¡zÜæ8f¨1ÃÀjâ½\x001cÒ\x0005/¨\x0000,^?ú\x0003I\x001aý²r@pÆõää"Ì&äÍé9\x000b«zVàl$\x001c\x0010IX-LI/é¬gNC%÷¸S\x001fÔ\x0000g#äLú6ß½Ir@(Å;	f§ËÒX\x001fVPeJÓ \x000fçl\x001cJßf=\x001b©$\x0007Ä\x0012\x000e.  J´ê(§Ðä\x000c\x000eXc9AÔ \x00060Î£,0\x0007§¹}}4Dù\x0002&YA³CkÎ
¥oÄÙ%\x0018\x0010Kñÿ.÷ÓÁÄ"ÿDÎ`ùígÊÂû8\x001b±\x0004\x0003bIå\x0010¸Â\x000eëNn/¦u+\x0018 ÐÈ$\x0018I\x001au\x0011¹Q,äÑÉñw,0×`\x0005ÌF$ÁHJ\x001b¾¹vLæ\x0004Ýz\EtBcÀ	¢£±[\x0016(\x001dIÄ;ãS¯awªF&©\x0001.3º§\x001b\x001ao 'Î\x000f#N?ÍÐ\x0018àlnÂjà*¬Ñ*öÄYR|ê\x001f9WYÏFvª\x0001ÙùÖ³½\x000b\x000f\uÔç>ïOì¡F¾\\x001e\x00109ÃL>ÎFÆ«\x0001\x0019oð
L¨2¦¥;{Äôk|öFÄ«\x0001\x0011zJéV¥ld¼\x001añF3c îsÒ\x0007þâËp8d#áÕ7\x0018åæ/ns\x001b²ÈéY\x0013Á4ßd\x0000³±9ÕÍ\x0019%ù)\x0005BlÔC2(þä fÚ]taêF¾ë\x0001ùn<"NRÅ¿\x000cä¿V8no\x0005ÌÖç5rÌãF\x0016Æ¨S¢\x0014ë\x0007h
#I7\x0007H\x000f\x001c +ä)ÐWGµ:\x000eÔæå\C\x000béfsêÍiQ¤gÇÅ\x0014ÑÌ\x0012­DZOÐ³Ö\x001eÎÆJÒ\x0003V\x0012®gÆ4¾\x0014aGoÂ\x0004³Âî4Íî4\x0003»Óã\x0010ïìÅÑ\Ú!>ZN]r\x001açlD§\x0019\x0010ñ äy\x0003ù³çÃQ^r¥\x0005¬âE4Íg7#ýpÚF«Û\x0001­nM:;\x0013g9R:òdÄcã±\x00158ïn\x0007¾»wÒÀÇ`s^Ï¸@û3¨\x0015»Ô©ø õ%\x0005=w8AsÒ«%·7ÜXä@ô%òã»-[äÝÅd9fd¬ ¶1@1æ2}úP¯¶P¯\x0006ThÀÍ\x0019U¡Ê:´lV1­üìA\x0015ÛQ8açÜ(3ÆÛMÆ¹ ,Èâ¯j>ãÅiòù7
\x001e/N¾OñöêT*A\x001e&\x001dÿ>JuÄî\x00194
¯É×\x001f!55©\x0019$Õ¹Û|\SÃè3(5ÖJÏ#ï µ5©\x001d#5iø|&lTëi©#RDu\x0013á?ºITCÔ¶\x0011i×÷Wôù}Î«jÊ÷f 6gJ\x000e\x001eªx\x00035Y¨\x0006\x001fØi+Õ\x001dyú\x001d¬®auc¬\x0002èR¯\x0006NÙÂ>GÄª§Éà=¬ñkµù\x0017ñ\x0017qöÛõ§Ò_çõíþ\x0014Å³\x001fÎ_:¯_Î5G®1¡ÆnL4HØ\x000fMð)*\x001b(Sjè×ÀÔ5¦\x001eÁ\h_=×º ã\x0013ô4¬0ikL;\x0019?ºÒTC\x0011Ø\x0011\x001e­)n¢¤Õ\x001a®Æt\x0003"Ef\x0012&\x0000u¢¿ÖÜû\x0003üDÝ\x000f`ú\x001aÓ\x000f`JÇ¡ãjÚSE{³´bÕÓ/\x0003¡¦\x000cý\x0007\x001d%&\x001d hP\x001bMé«²Jê§Üh¤$ÄÈ7·¥ßRäf\x0004ö{ §n\x0000³\x0011G²_\x001eÉ\x0010\x001cõQKUHTQS9s\x001a4À©\x001aN5ÀÉ³Ä#§ðå³\x001bÇó\x0002Ð\x0001ÎFnÊ\x0011Á¹QíñªÀ\x0016\x0013\x0000'¡:=Í»\x001eà4
§\x0019XOcÊw\x0017c
R\x0017N4\x000fçl\x0004¼\x001cð"àM.¯§>´è
ås´Æz6\x0012^öxôÒrYöÔ;\x0014S\x0001y=§ÍÆ\x00068\x001b\x0011/ûe<¶+M«¡¤HËUÞ\x000eÜ\x001ar©\x0011òrDÊ£\x0002"s.8JùE\x0013í$áVPÐyè\x0017óQ.AK8\x0001Î\x0011^Y\x001d­ÁÙXÇ0`\x001e\x0007\x0019ððäõlÐa\x0016¯ç\x001aû\x0013ZóxD\x001f\x0019îB\x0010×Sý©%÷\x001ciÝ\x0000g£`D\x001f(Ü©âÍ^XÕ¦} \x00082Ù¨#èWGQ,\x0001\x0007èP:nÖT¤ü\x001a2\x0001e
\x0011-\x001dvgRèÀ­1ü´ë\x0000g£ _\x0019E¡´i\x001d\x0000r~PÜ\x0000íÒ\x0000g£`@\x0019¡c9»\x0017ãzzvÚ¦b_ÚÓ\x0001ÎF\x0019Á2\x0002µ1BJòZJ\x000bZQiB£`@\x0019y§Jy«\x0003®F\x001dðþ\ã6¬\x001a!¯F| ñ´ç¿4{9K?LëÖ0æU#äÕ\x0017z£Üu\x001e\x000fÂS°1/¦±Ä\x0001ÎFÈ«\x0001!Ã\x0003$-§ÂT¶¼|³nÚ\x000f~\x0000³\x0011òj@Èûh 	Wt{ vû®ôe| 
e³\x0011ójDÌ+WÚ\x0018ê3WÁiVn
ojÄ¼\x001a\x0010óÞ\x0007Ê·ºÝ^XYL¥©wv\x0000³òjDÊC@;./§á~W¾t@wkXJª\x0011òj@Èãî\x000c$<\x0003PÞ¸;KWK\x0014Ðs6B^\x0008y)1)/§ØL9¡Æk`­]AxêæÆ¡\x0007n\x001cÞz*?»S°!\x001eOvtO[z\x000c`6ºHè¢(ãK·´\x0003rÇ®Òî\x000c¯s6ºH\x000fè"ïô©'¡ä!O+DÝ\x000eÜYl\x001aß\x001eÀlT\x001ePE.þgA+$ÎýÅ6á5N»nã\x0006#ºÈ\x001aÊýÅÔ\x0000*\»S°Î\x000ck\9t£ô.r µ,Eì
Ø{ -Î\x0000d£ô"Òâ$
Üó.\x0004\x0016H~
\x0017nô\x001eÐCÎ«\x0012ySá\x0002oÀYkÜ\x001a\x001eÒ#z\x0008sUÙ³x£F0Ìé§íÛ\x00068\x001b=¤\x0007ôÐ7YNÓ¨!3¢Àjó¨1ñ&/'\x0014c.¬ L£Ì\x001erÑÒ\x0014tÖñúõ\x000fÅL2Ói\x000b\x0003\x001e2#zHSÂ´PlcS´º[âPz°ùfal\x0019QBÆQL+­%µ0õAÙ²k|óF	\x0011%©ªlÊYþæA²7Wùæ|7\x0003ò\x001dûÅ9º¸a&5u]¾ù\x001a\x0017
ÓHN3 9£®<\x0005:êXú¬X]²N·+¨tÓ\x0008N3"8¥*\x0006<¶¦ÉúÒ+ncbõ´²£Ó6\x0012É\x000eH$\x001bBHQf¯ð²x;õ\x001an\x0005ÛH$; s\x0014ÊL\x0016<Kx¹19×°àmsÚíÀiw¯\x00192)#¤â£n×0l¨2rÔ­ G|²ßÓ\x0007¿ªýn\x001bcÎ\x000e\x0018sVnú\x0018{{ê³w]ÜV®áK²Ía·\x0003Ý\x0008WúAG+ÙäáN¦t#7n
N×InÀL\x0018ÅêÖ$óÃl:#NÛ\x000f\x000ep6BÉ
\x0008%¬\x0014´H9æëz\x0004^AeºF(¹\x0011¡Mi9\x001dczåÊÍm
]ä\x001aKÉ
XJÚqö\x000f .\x0007£\x0005ÆV¼±ÓþE\x0003ìt\x0003²Ó\x0006êÆ\x0000\x0018pÏÙ\x0015Q\x0015ña yÀ\x0000esYw\x0003u\x001dÙlµyV¢öv³9WÀld¼\x001bñÑ¬¤iQ±\x0007*@\x0010®Ì\x001b²+x\8 áµ\x00006°c^.è\x0011ZóHdã×\x0008º¹Æêt\x0003V§)\x001d#¢&R4½)j8S:êO\x000b\x00068\x001bMä\x00064æ\VìØ~=×\x001dÅåäXñÓz~Lß("? \x0002ê\x000b\x0004\x001ecY"Ù±`Â\x001aËé\x001bEä\x0007\x0014Q\x0014åì7FOwNB\x001b5
a\x0005é\x001bEä\x0007\x00141\x001aé\x0001s.@´f%\x001fv±Ä Ûya÷\x001aò\x0003jHYn£\x0017!\x00057NÔ¢\x0008x±ÆÝ7jÈ\x000f¨!í<M>ÖGàn\x0014ub@kn
ÎF\x0011ù\x0001EôÖ³ÑD~@\x0013EñC
ò\x0001®ÔôZ\x0007ïlÜt\x0012â\x0000g£ü.úFëÙ&Æ\x000fè¢¨ÅyöQ4ÝÙñ¥
GØÍ*	J¡\x0011òa@Èk¡8rí±ó?}wÍMÀ¢_A·Fx\x0001á­\x0004qbÂ\x0017Ù ²xÄ\x001a¶RhäR\x0018KßSËºX\x0002®ø~bàx¶¥\x0004J»2 `C/Ý6lÔx#°A\x001bÊHU3éTÉ±k¸>µ,¬\x001dbõZb6\x0015Gâr0[¦:+\x000eÅ­\x0011ÕÔ\x0013\=kàbÅNS\x000b\x0004l]"]ÓRø`&\x001bÁm\x0004\x0013¸O=fURÙ,Þz'§-\x0007²\x0000Õ6.¨±ÅÅ5N\x0018Üþ5^Lø^\x0012¦mZ\x0006V7LV7­.8Îaà|ÐPwSöÍt ç\x0000íä É±\x0019B<bØlò*#§Dn\x001e¶ª%lÏ­M§o\x001eós½`ÊO¼¡P{3ìÿKR³°Ü\x0012AOS\x001cRñ~3égvI\x0019\x0013jL\x0018À´+MqN¯Ë}e¤ãäZ,é^\x0001SÕj\x0004ËùÀÂ©$Hö\x0005µÊZê\x001aR\x000f@\x0006A
¤À2WMp!¨¦é}¦¦4ýÞHný\x001bE&oLØôÉ ¶g\x0000ÓÖöh1]é\x0016Ó×þh1C\x0019\x0015³x\x0004ÕÄ£ããluÐ\x0012úF\x0012\x0003Zè\x001bmOùãßZ­þ·~\x0019÷\x0011\x0012òÁRD\x0011¤fï}°êáÆa½¤×-éõñ^µ¤WÇJ
?¾o¥÷Çj-A»¦0²¦ßôCKúáxIÿÖ\x000eýoEú®%}w¬¤²=QräD}+)õ®%\x001dXÓoCÚøK²_:ò\x001dFVOÁúV§ê§ô§c%­L#2õ[iÔÛ5ýùèÖTo»Itr<¿ýôå=N\x0007Ê eâGDÉ³\x00031\x001d.w9ób\x001a\x001dþòÅsö;Õ\x0013F÷2ëY\x001fÀ,¨sp\x0016\x0014ÐÔËC¹0]áqh[CÛqhÁÞÞ\x0004MÍ¸±Q_¯qhWC»qhß{KâhIh 5\x0015\x0011(ÿÀÔqh_Cûqh\x0003ÔiVC)\x0019Ãf\x0005¡§ûÆ¡C
\x001dÆ¡µ¤~?\x0011Úpë\x0002i¸	ºÇVkAWî\x0002Ý\x0005ÃKmOsA\x0006\x001b\x0005	0¦.©^O»ÀSËZ\x001e°Özûj0e´¢¬õ4rº\x0011Ôò\x0000IE(´ÖX*EÔ&Ð*o§ÎØqjÕP«\x0003ÖÚ³~zE5÷x÷f:Ác¹Q/ò\x0000ýb\x0005ïj%Êh$cT>©1\x000em\x001ahsÐB\x001bRÎê­\x0006Wq©§}`Ç©\x001b¥(\x000fÐ+´RG%a5m¦\x000erM\x0001ÒhEyZÔF,h\x0008Àfi
\x000b\x0010\x0007+R7jQ\x001e \x0017m .>\x001aó¨]\x000cÔ\x0014IiDt\x001cºQò\x0000½È!ýx\x0014í)Ë<Áò#¬gB£\x0014á\x0000¥èU¹
î6G {*¶¾^OC£\x0013á\x0000\x00185yÎøÑ
ëJè :S\x000eâ4%~º½¼\x001c \x0013¦\x000e0:ZÕX>º$
JBVÁ¯hêA£\x0013á\x0000\x0018õKÎþÓÊIªÈFýâù N3)Æ©\x001b­\x0008\x0007hEgùÖ¥æ¹2 ¨#¥âu <NÝ¨E8@-ZUÖ:xªëB\x0005\x0003|\x001a×3õ ÑpVt\x0006\x0008j¬O¢ñÚ è0bCòõD54Z\x0011\x000eÐØªÖÒa\x0004,DÎKÍêÅõ\x000c\x0010h"\x001c \x0014±O\6è\x0000á~ÅÕ¤Å\x0003meÆ©\x001b­\x0008\x0007hEë)/7n\x0010nÑ¬cÈØÃ\x0014Ýõ6j\x0014£:D1\x0006OÖ\x001a«®XZ\x0007ÞÖA®§ÎU£\x0019Õ\x00011MyÒ¬Ö¨Î95Ë8¢6v=ojt:DÇ\x0004®
6À¤Ã\x0018èæ¥\x001f\x001aé:NÝHku´vkhL)ØDõ\x0004½¦:WÜSãrÏc_Ù|]4x\x001b F_ºNj¹¦:W\x0008Qã"\x0004rÊ¼¶Â³\x0011"xL\x001cÎ:ZOèæ0êñÃ\x001eéjnÁb~n³TÖÚéõ\x0010Õ¤ÎÒÄß\x001c°»É2Ø\x0001ÔóÍ-(¿7\x0004ìV\x0000ë/£æ}öË¯W?_ã¼¦§Wï®oî÷Ä1¬\x0011<\x0000^\x0018GÝ/ ÚîeÆÄ´CØ³ç¯Î^¿>ÇyMOÏ\x001e_¼Ý©kL=)ÑªKVÒ\x0010ã©8Ñ×LOß\x0000¦­1í\x0008&P»µi°4>cr\x001bg¦ÑË\x0001L_cú\x0011LuJß<nÖ\\x0017½É\x0008ÎN\x001bèöSnÜÏHîç~LMESÓÐ£Èéø£ÛiCâ\x0001Îæ\x0008Éã=CPË©|Üñ\x0017GF«ÔÖÄ£ø~rq{³\x0007P`¹dÎ\x0000:fa(.FñnvíÅÛ\x0017ûÁ \x0006.0\x001b¨\x0002^Åk<\x000fÂv<67\x000fx\x0019ªÉTß\x0005E/Qýh^3F{;;ªx\x0019®Ñt\x001fà!\x0012ï3\x0016³Ë½ñss\x000b¡\x001aÍt¡yAÞ0%95´h,¬ýLÚûR0[Ù¾5Ô*Iº®rÉ×SwF\x0017«É\ßIºý+©J{VÔÉ3íÔ\x0016j´Ð\x0006åkJÁóî \x0001íàç§N.B«Æø)±É¾^øA'bJ\x0005§¿§ãU^.»ÐZaÛ'mã\x0017e%³§XÜò\x0008T7;0~\x0019Z#ne¼u|
_Ôòô&\x00084L\x0016!\x001f¶lTbMñüm\x0011<»Á°Ñ\x001d-[zÒ»Ø\x001a±&ûä\x001aÛhj\x000bî3ç>ÎLË¹»Ð\x001aÁ&»%£
8o¸.\x0016Bñnb»Í7l¾oÙ,¥Á$snøà
n\x001a:ëaF@\x0000Á:2\x0012n¨ë%\x001e\x0015¼\x001bT¼­ Ð'At\x0019\x0012Ñ;8\å\x0016¦-Ð»ØZ­ODõI\x0003E´{iÈ\x0001¸2pÇL\x001b©u±56\x001bô\x0019m_{Ý\x001añ\x0006âMs\x001a.:q=ëR]É0õat¡5Ò
ú¤Û×^¶F¼Axóïÿ&#Tì­Ó3@MÛæt±5â
úÄ[½|\x0014¢¼8õÄ¦è6­pNç!lª\x0011oªK¼I\x0011N³V°qãQª2TÒ\x001f¿óaZA5ÒMuI7qòÌ}\x0012\x001cÁRÀKÛéX.¶Fº©.é&A³ÉëäÆvs\x0014¬Uq\x0005\x000fÒôª9¦ªë~õuk.1ªë\x0016\x0013Õ\x0002y\x0018p>\x0002M7Ó"TJibO\x0017ZsJU×)]sØo-Ë]Í9¥<HÍëæê®3\x001a\x001bÌf¹\x0017­Ô^1Û÷eÝú\x0018ºÔU\x0014°ÔmEG\x001b\x0010û\x0017 QÇ£ãuæ\x0010¶F'è.ðµÙL#ÜLp\x0003\x0008|/ÅÆ\x001f\x0014«5BqÊ©/°ïbZû,érZÊ\x0016[",8WF;BàyîA@}þ£mDÓK¾#¾7\x0004ÎDêï[n\P\x0013>ÜÏ\x0003Â\x001f5þ\x0002ý¨eÈýç§wW~Ú[©b¤Ae*UDY@o\x000cû\x0006§\x0011À2áþõÉÓË³\x0017OwUª0'Ô0Â	@9\x001aJzÁg¼åk«·S©<\x0002ªjP5\x0004Ê	\x000e
Ð¢\x0005e­\x001bÿÚé\x001e\x0001Õ5¨\x001e\x0001U%h\x0006F³WØ;n,-R×\x000055¨\x0019ZQ²'w ±|¼åè^ÐS÷õ\x0008¨­Aíà\x0000¢QCî\x000bï\x000c7Çvb¨º\x001aÔ
j\x000f¥.Ê$ÓS½Ôüé(ë\x0011P_ú¡OïØWí\x000cÐ\x0002ßæ¦þä\x0011ÎPs\x0005
Ñ.£['öÍÖ/B\x0008k,h\x00154
ÙÉ< ï\x0003\x0015FÅ\x0015µeZÉâIû5T6\x0002_\x000eIühSÔJiÅe#^\x001b²(ãg[´ørHäÔ¶\x0015I5vpe\x001dJ\x0012U4V!mD¾\x001cùÀÃaÖ­t_\x001c7b:\x0006j\x0004´\x0011ùrHæã\x0003OKª8Ì\x001b/=ÀK:-\x001b!md¾\x001c\x0012úñ\x001d²,5è{$¢(z\x0013­iJô\x0008i#ôåÔ7Ò²\x001e5ºLÈ-&T$ÆFH\x001b©/ÇÄ¾Æ\x001cËLÊãÊpMÙ¿8ì6b_Èýddiª7AxÈÅ"a\x001a\x001d ÆÌ1;ÿ|üö¾->üÅFå¢°Ü\x001bÏ°Fe=¥¦ñÚ![j×
òzG1ã%Ñb²pâ\x0005î\x001b]ÅHõÛ¼~÷\x001bYVz\x001bWãR¤\x0006{\x0014;\x0000Ïò\x0007ê\x0003é¶îÓñ\x0017Õ}úÉÏW¿ü¹ß]ýëöæfO'\x000e¬ã\x000c
ôù\x0003%Q\x0019\x001eÐãpÃÃ´O¾?{þ
S=¿;ûëË]	ªnëjÈ0\x000cÀ\x001cVW²þt`7½»ô#«\x001aY";ih\x000cR4\x00078\x0002Rège=d]#ëaä¨/4å\x0005x6kâæxã´<w\x0018ØÔÀæ\x000f±ml×Ø\x0019¶q1@R[U_xÎ«Ñ\x000fìj`7\x000c\x001c7¯¡£\x0017\x000cY;\x0000¢\x000c	÷Ó\x0005ÃÈ¾Fö£È\x001e\x0004çxô¸\x000fSÉ·v³^Ã~âP\x0013qâ@Ãã-Gú"\x001eÍ\x000c>z~ê\x001dE®Zk¸æÞËl-¦fæE1¹ä0
É\x000e#·oXóá\x0008lN2* ÊeÃ\x001d¸\x0016s£Fä°\x001eùÌZ5Ú\x001a<þ½6g+5ÞB£\x001fG\x001149[B5~ÖK2|Õ"_ý\x0001$][jL£ÊXîÕÜÁâxÕ\x000c.èBIÍº¯§UÌ6¹9üÚuæÇ/×w-9þb\x001cã(-\x001bTiûf8öãüì-e9y´¾¶B¢jåªÑn?ï­CsNJJµÄ\<º-È2l@Ï¤\x000cæ"´¯wíò3Qµñ_MôÐÓÜ¸=Efz£î&T5¡ê&TÀÁS¡4|\x0008o9âôLNh\x000f¢®\x0011u7b\:A7\x000emÐÎL^\x0014Çé0ÎnDS#nD)°ÎWQð\Ó¢\x0018ôtq7¢­\x0011m7"XN°:'îzã\x0018ÑÈSÐz\x0010]èz\x0011­+cÏ\x0005L£Öi\x0000'hëg|z\x0010}èG\x0010Y°ÇUT4_ÙË¤Ã?t¨\x0011C7bT8çñ\x0008j°&<whÄy<\x0007¯¢lì:\x0011\x000eýuù¼ppÚ\x0015Ñ=-ëïfl¤ì\x0016;VSW¾t®Í\x0010Nh·ÔÔÝbÇ8\x001a\x000e\x0014¿´¡ a±%\x0002}é©ÑØ\x001ciÙ}¦á&tJH@9\x0018f\x0015\x0008Óá¿ÝÍÝÚèP\x0018AQð32*fT3ÕK=Í¡Ý§\x001aCÉ\BÚbÂN\x0003ÓC)¼ÚÂ½ÐØcÐmi\x0013¨1\x0012%(\x000c÷½\x0000ìÂu(b#x [ð`p?µ\x000b,¿õ&ÙîÖ\x001cÝànÁ"Ü¬c4kj\x0013xÔï\x001aV#4\x0007ú%HÉA¹ì\x0013Úãv,×\x0004;½	w36\x0006\x000ft[<:$;_edJ»)	Ó<nÆF<B·xÔ>J¶Ü%1\x0013äð;\x000c4â\x0011úÅcüÖüÄu,ùjÚ\x0011«±\x0011Ð-\x001eµ·d:FF­Òò:Z®¤Ô3õ<\x001dútÓ\x0012ýjÆüÏ`Èßjta&÷½±\x0011áª[c>5Vô&,\x0017Vï¦3º\x0011+µê¾Sel/ÕÝjÆ\x0008íîrO\x0000á'ÒÖÌh÷Ûà3YÓ\x0004Øè\x0018Õ¯c°\x000b3ÅÎk\x001dD¼õsì\NÛ¸w/b#¿U·üÚKi!·ôÈæm(ñý\x00156c#¿U¿y+\x0005%\x000b¾Å\x0018ï8¡;\x001cn7ªFx«~áãNi\x0011±s5Í¹\x000f,\x0018)ÎX¼\x0013\x001bÉ­ú
Ûx)ª\x0005 7ÇïYAº\x0017Q7[÷Kî¨¥s1\x0005ç\x0007ÄE\x0014¼\x000f´ëêflÄ¢î\x0017ßq+5J´3p\x0016_¬½¦NñÚª°.9(\x0004këáÇFÈmR9@ú-<Ì0!\x0011Ôop÷ÚêÏ$¸?Ó7¾~TÅ["#ÓüÝ>y4YO5´8ÉÇ4Ùry°ì·ðÚï5zgæ\x0018Ûí9Æ¶\x0004?:5iêÏ\x000eS©©Ï$`\x001e'9L¥}\x0010²#Æ´ÝOÚ\x0012\x0006éõ§2íÐhF:nv¦\x000c7;1þáÑGý°ªU°â\x00166jÍ,¢âÂÒa²öá²ã~T]£êAÔ@¡¨Ì5	þ¸®ÔK\x0012[ö=¨áûaM
k`£mÄ\x0001±¸\x0007r@\x000c°\x001bIix÷à5­ÕÖ¬vxa³¯\x001f°\x0017~ö\x0000ãÂò&xØãÖÏêjVwÜëêkV?¸®->\x0011ÿeÄue×0+\x001d®P³£^×*ßÊn&\x001f÷.¬â#6IQj	ö\x0011ëoÆý´­î\x001aS^ßli\x001bÝ%Ç÷}`Dêhiå¦\x0004Z=x_î§m4\x001cS	ß¶ÍåÏ"m­îÍ[:<
¥8\x001b,Ú2Ì\x000c\x000f·Ó\x00188jÛÌñ¸
Bû NU)ÝW¤!Àhð4µjÐ¤ÙfVÃëü-(Ó[ó6þ¢Îíùÿë{ÿËÞ\x000eÙØdßS!²ãÆï\x0002û½PñÌ´\x001f2Ûß'ß¿|û|\x0001"ÔÐ\x0018\x0004×\x001b\x000e<ëNðkPÓî½½ªFT\x0003ãìÑ\Ò#6C<Ý¼o)¢®\x0011õ\x0010"û-â\x001d6\x0018Fd'ßlxx) ©\x0001Í\x0018 \x0015F\x000bÏ³½ã.ª\x0001ú\x000eD´5¢\x001d@´\x000e|Û$M\x001f\x00043\x001d´²øð]ù\Íç\x0006\x000e3ÏWTÑ\x0004¡>´¢\x000c\x0014þaUß³¾&ôÝAD¾1PÁÄ48þÆòà£\x001cjÂ0°L¨©æY\x0018Éuäa¦3Ñr¼ªù+Êk1´~³ÆN\x0010f\x001d&K\x0019[2¢T\x0014vÖÏh¹±I\GYÖqÖó¸±Q*²_« \x0011Os\x0015\x0008ªòëÈ×£\x0010æ3\x001426ZE\x000e¨o°Zýz%`î+ý,¼¢uTÞ\x000b³\x001eÑ¥f\x0003ªÅf­Kç"Aù
Ì¡f#ªÅq)2b\\x0011¼Kñ¨Ï4î`l´\x001cQ/7\x001a¯\x000b
­¼{B¨iág/c£_d¿ñèOÎË\x001dYCs\x0003H¡\x000fà#\x001aFp\x0011v¢\x0018èè¦e<XMC£e _Ë Í\x0011\x0007îÎ\x001eï^Ü¦ÄL\x0007y÷"6J\x0006\x0006
 1¥Gñn¤æÒLË7{\x0019ÛËÀÕÅ»H\x0019æ!Âò§\x001bóPe
\x0011%#°ü$µ{\x0010\x000eãpy\x001d\x0003oÇ\x0007Ê¹{\x0019\x001b%\x0003\x0003\x0017¯9J;
}kkx\x001dýÌ,\x000eÆFÉÀÁY\x000by\x00197=æ\x0005oÆ\x001dQá¥\x0001\x0015£Fh3*3gó"Ò\x0008¯hMÌg\x0000,elT\x000c¨\x0018ÉîÔÆ.\x0008¦¬£\x0016Xö26*\x0006\x0006T3|CÀiå¶õ()Õ¡ª\x0011ßj@|oÆ¸\x0018´sy3Àgz¦[yÏE¦iw/3uü·ç>ÏR¸ð>Ã®M
3\x00015# Þþ\x0006i -«íÒ\x0016G\x001elè¶Ù\x0014Ù¡7BÍÃÙMá(²¯fZ[Ø­u¶IA
¡:¶3Ò8UV=|v¤Aî\x0005[áÿøôóÉ_®î>|ü´¯\x000cDAÉA_¬æ¢^ÅAX\x000eúÎ\x001dö×'9»üó³\x0017;:É0"ÔÐã\x0008,U§`F{ÖP2íã\x00168P×º\x0010'S\x001e=åI\x001dÛ3íXÑgk<Û'11S\x0015W=÷Ú7ÿhÝ\x0001ÔèkDß¨ô¦bO\x001eèCänN+.'¬\x001cSÒT©cZEÙ\x0014Ù}T¾ÉnúXåó²\x0011I\x0005÷à\x0003÷\x0008Ã\x0016¬D:m\x0012º\x00184\x001eÈ­Ä(Ø\x000cÖrûìó¯wûºlEÁíyø\x001fö²ÕrÛÂð3E\x001f'g¯_]îì¯\x0005ÛÍª`3^o)^s\x0007öÔKÉM!AÍÄ;\x0016ã©\x001aOõâá4lá@R²Ï¤ñäI\x0007ÚváÉ\x0006O\x001e\x001fnøt\x001f\x001f`·&jåLé®Ú'+\x0015f\x000cÅ|¦á3G·~¶á³½ë'\x0004÷±qBS¯®(u\x001c¯	",æs
;:>ßðùcÛÐì?èÜ ¢1Mã\x0018¢iP\x0006*áyýf¼Éùï\x000b½ßW20Ó£IHë§yn¹.Æ\x000b
^èÄ\x0016+\x0019¬é®uöÔ\x0018Né0S¾\x0014O5ªWuêÞ¯\x0007Û}"ÁúBò\x0014gßØ+ý°á\x0014ÅDÔäZ:*zÏÏYOqfùÛ?/T5¤ê\x001c\x00171]¶´Gº®t\x0003+é0,­¤F×XZHàùLjnÎr\x0017c¨\x0019Ã\x0000céeï|ñ}\x0002ð|\x001atì©Øn\x0007®\x001aÚ(\x0015»>OM­³Ìæ&öz¶HÇ:VÍ:\ew-ßÞ"A\x0002\x0015\x0000K¡9\x001a/\x0003ïÈª_«¬¯s\x0003<°Ä+Ë#|¥ã6ûÚN§VôS6[ön/Í©Í_<(È\x0007GÄë\x001e}pcVøÞÍÙÝ\x001b'}ðJ\x0006ðäõ\x001cÁ2sñÔ\x001eHß@ú\x0001ÈÀõcè\x001e!ÆÀ\x001eyãfFèö@nBªI)~H°§:ËòãèÉ,4Eø­c×EÙH!èBßæä@£»¡[yÇµÔÐ\x0011pú/I!A£I	³þ°å¨\x0001Q©4ù 4öîàì\x001dI%ÁÊÚ97|\x000fe#`@\x0008a{-*ç%wÏ\x001bOñÜ\x0005ÙH!èB\x000eæ\x0014r\x001c\\x0015q¯òx9,¿=H}C#`@\x0006\x0019IþøùJ(\x0014uF&¬ðµ\x001b3\x0008ºí 4á\x00123é=hü³rv.ºR5¢R
JÃÅô\x001a;ÖzN×bÈ\x0007ÆùôC6RõKÊo³ÍULõßÅ¾ÉR6R
HJ/È\x001cÒSçI)x ðìdÆ.ÈFPª»X¼ædËWC\IªÆÿð\x0001\x000f\x000f\x0017¡ôQ6bH
!«(\x001a#ùÆ\x0018õ\x000f)\x001d\x0007f6ÞÖa°5µßÙh«\x001cí6Ëí<£ö¡ºêh¸q¶1s)ÿK`¥Û.\x0000w)\x0002|vss1ü|ýi¯/w ùßÙÅÅy¦|òýùÝÃD¶ë¾]
\x0001÷2Z*¨ÈOhîEi
'GÈÕÖ\x000f©jH5°ü\x0004)úf©\x0017áÖ	ÖOû­õCê\x001aR\x000f¬¤*7·é£È)	`\x001f°4ú!M
i\x0006 Ó@¶\x0004©Ä©¤=i¸ã} õ±\x001fÒÖ¶\x001fÒ8*T;eXÍc¢ù»Ât5¤ëT\x001a;PWf+JM¿zègô5£\x001fbÌ\x001b\x0002(L¶'HþÚz*%CÆ;S+ð\x0012µ\x0019\x001eÿøöóû½*Ç:JÎT=©ñ^Ë¡`1ûøöäñË×Oö£é\x001aMw¡E­ÂC\x000c£zñX\x0012Äì¨ñöð¹lÍe»¸â ©ªC¨IK\x000böëF£âa³l\x0011«¹\\x000f3Wë`hÔ\x0008ó¾å\÷Ó¥Ò×h¾\x000b
Û-Söj¼§\x001e\x000eFðü<}à.\x000b5ZèBÃR6NèçÑ~ØÉ?å&)\x0007¡JRÎ2ª¨$¼¦o\x0019Pä¦Je§É¼Z¸`\x001bwb=l6\x0002MAâ>îr\x001eÏåAh0]ÒÌYyÊ³\x0012\x000b\x000còªÉ9;ã¥[¦\x001a4Õµjx7¢/\x001a?.Ù&^ð>S3Õ§KÑ\x001a9+»\x0004­\x0006ã\x0018t\x0004<0Û-h÷²5CvI\x000eAR\x001cq\x0005\x001aµWã\x00102h(t\x001dÑ¯LÖªô®S`¢b\x0006\x001dÏ£\x0006%Ç\x001dfâKÑ­\x0006][-Bº\x001f\x001c\x0012D£\x0001å\x0012\x0001ìÀ\x0008[£Ö¡K¯'6Z7mNí\x0004Í<ì¦\Ö\x0002è;\x0005_\x0017M5Mõm¶¯Öz+H~\x0014oÅÿäAU°£\x000eÉCñì_¯>æ6z\x0017·÷ï®ÿu··G\x0014Ô÷-þ-ZÍ\x0002ã\x0006\x000f\x000c\x0018~öüÕÙë×ÜMïâåÛÇç½ÜT\x000fÛ\x0019ëÜ\x0015ÀPÊ\x0014L8ÍcH\x0000Ûç0ðDÆòªW
ózÊ\x001eVsàx¾Wéåû@Ýæ(°®õ(p¼-R|\x0019°\x00186·~\x0002]:j¨©ów\x0014ØÔÀf\x00188ðP¬¸m©ú\x000b;\x0017\x0006=õ¨òÚ×òÆ9uX\x0005Ï°¶´MÎV\x0019¥u5­\x001b¦-s-ãÿ¼ì8U«¦ýàFy}ÍëGyµå$ËÈ÷ÄËµÜq§×QàP\x0003á\x0005öe\x00109K\x0007«Ëæµ¤CUª\x0001¹Tc\x0010k¢<³e.¤)Äjj³\x0012·\x001anXÅáÔ\x0018WT\ 5Ö¥Y\x0015L§"\x00127*Në8Ã\x001d<°w\x0015ïaU\x001aCÉi¦Â(q£ää¸3ÅÐçNR¾\x0010\x001f\x000c,¶ÒLã/ÐxusõþúËÎZÇ2tSt\x0007ÍQXQn*S+âÕÅÙó7o\x0016<n¥"¬\x001a
¥å¡2þ¯Ùí\x0007ÓF$C°ºÕc°aC®ãÖ¥ºBÌO+>ÊÉa\x001b55¬\x0019\Ùx_¥Hbº°nuæ+;M\x0001\x001bu5¬\x001b\Y¡YO ¬§pwe\x001bL«C`C
\x001bFa-",·Ù\x0008ª\x001c°©Q6\x0002[7Êù³cVsW'\x001d5¥ô5¡ø.	òÀ¥u[ÅsÊ¥â¹
öóÉ«ëÜ_ß\Y{ev\x0010\x0012HG,jà]âàõÉ«óÿx{~qþfWU¢ßæõb¿ûýiBpRÒÑÂ±4äx\x0007\x0011X¹ioO"ìýhP£A\x000fZÀ&|¹,Ö[A\x000eQÐÊ¬â1©}^¦j4uT«fj4sTh®FsGæk4T{-Ôh¡\x0007ÍkY\x0008X\x001b,_=\x0014¯ÚLþóB´ê¾ÂC\x001cÓ²ÉV°uI6ÏNî´lú£\x0003[ºÆÏºõ¡5M\x001edkªÔ½¨\x001a\x001dÿ\x000f\x001fU°[\x001a+þ¢nÜñÝí§/;J!Óð\§ÎCõâúr©¡Ü9üÝË\x0017o^/)³Û\x0015i¶©Hë%\x0006Ï£Â\x0005îL\x0019
\x0004.\x001esÍ×úu¬ÇU©w6Ç}¢ÍÍÈ°Þ*\x001aÙ#\x000b(\x0011Ë(\x0007\x000cÿq\x0000=®ÝKlkb;N\x001drh+\x0007Ë
\x0000øB\x0006«m\x000bÙ½áÃ'I£ÐR\x001d<NK¢YËÑô(:fsf{¡aqæ(0(7ÁjÏ\x0005\x0011\x0012ç%QíþÔ7Êì\x001bf?Îì\x0014&0æs=\x000c\x0016oñ:Ïi-fÞ¾IoäòÓ»«O\x001f><¾ý¸Ö\x0006Ï¥·Æ(~é\x0015_Ò@îÈ÷¾<{ñç×'_>[jjT3J\x0003&-\x0008ºObs[Fus
«;QmjGP]´\x0013r\x0010Õ:WJd$ëTêï\x0010©¯Iý\x0010©ðÜéÝÆ?\x001aúþ<NKÅÃ°hQg
z¶íiðmÅðrNSüùÖs¡}\Rv×EQpènEûÀ7íµ\x0010õ§½zA{À3ÄÖ\x000c'\x0013¢\x0011-1?u×Oã¡õáêó»YÂª 7\x0012JÓ\x0018?iqtX\x001eà\x0011Õ@à07T}¸o\x0011«JWDtÝRI­¶´\x00185S±ÙÂ¡mo¨ü±²E¤©1&}oô~g;À[ÅãPí¼ZLê~|WsºGïzw¥HIi=ã×Ï\Æ[\x0003§#¹¨K(·K;Àm%NtõRZhS=vö\x0018r«\x001eãvÄ;ÕÌlåLÛÊXÎ*\x0003Ýe\x0002m!ç&pv®	rGø«UÕ¬jÕ
^WQÖUrVqÓÛõ\x0018¬©aÍqo\x0002[³ÚãÞ\x0004®fuGÊº\x001dJ\x0004Ñt¬yrûË\x0005½ì¸²O\x0019%Ê\x0008\x0003ã9½ËÏWö=yùüÍNIµ\x001d>\x0004Ñø\x0006\x0001â\x0014ñP\x0018ÀµÅ\x0001ÃÜ¦åº\x0006ÔÝöÔåÔ\x0012õ\x000cTE'æZÚ/\x0007´5 í\x0005T¥ç¾1¶T\x000fàÊcV\x001b-\x0005t5 ë\x0005%ÙÅ\x0018Ís
nê\x0004³3*\x0003ú\x001aÐ÷\x0002b\x001c>±õ<M:ØâÇÊö\x0000\x001a0t\x0002:ï¹ÖÇ Ek
vd­78\x0016\x0002n\x001cá\x0008R÷H]F\x0018Ì)7¥\x000c±\x00082°\x0014èùfÂK	eC(»×\x0010Ðyn<qC*ê¤¢KÛL;72|9a#ªe¯¬v>MË\x0017r $¶H\x0018x
ÝÜ\x0008®å¬½Â\x001a×ÐXZCÃ¥\x0010Ø\x0003×ðð}h\x001aBÓK8î)X
Ø\x0008kÙ+­\x0013ÅA½£{Ð(9£]
Ø\x0008kÙ+­¿Á
6ÂZöJkg\x001d7³q?z^A®IS;º/%l¤µì\x0016×_}	¡Ð/\x000b%\x0015Y+\x00174{)Ci¡\x000f_BhÍÖ~YXðÄ0 áæb¾íÕRÀF\x0014B·(´P\x0010\x0002eÌÇÌ#zfçE-\x0007lÌVèµ[]à\x001au¹¥û
F¤f>
´°ÕÐ+«½(»ÐÛR¡\x001e,\x001b®:ÌY;\x0008\x001ba
Ý¦5:z6\x001dÃ¨Î?\x0012\x001es3\x00136Â\x0010ºMWL
£öp²t"\x0008£fkoñ>üñËõÝÖ^Äß\x001cÝvl]\x0019´öA.¶µ©/öªä]É
(ó\x000eÝå ÿ¸¿.*ýòhÖUn§É*öäçë_>~Âd'?¼þ²P	Í\x000er\x001dµ

á\x0002Ã¢\x001c+ ¶\x0001|þüÙ\x000bÌ§xòý³ó7û	MMhº	ÑûÄi!8/Üð\x0011\x0015\x001eXÃnDW#ºnDÁãoµºJ\x0011\x001c¯	Ó\x0002¸nÂP\x0013NB\x0008è¯ÏY+£áRZåYká8m/¢l¾³ìýÐñ\x001e3Qó*úSªkR§\x0008\x0007òt36\x001fZö~éæ\x0016h3J«\x0007ªÜ±fPw36ZvkÌÛR´)z2¥\x001aC\x00197&.2¢ÛÉ¨-\x0015ÜéhIÐ\x000cÀ1iyJ7c#\x0019¡W4~\x0013FÕ¬£:Êu\x0014¡ÖÜYüà/:%b7Æ8TB¥9Q$\x001aEãRí\s#¶£rÏ?Þ]½»¾¹Ù\x001b?Ä¹Â9ø\x000eÖcfNÎäÔx-¦óeêÐÁóggÏ/.jÕ½Í	5'\x000cs²Û\x0011°?Gva¹fÐiÛî^PUªQÐh\x0005ç\,Àî\x000e¹R*ÊLK\x0001Y-§ã\x001f{Au
ªA\x0003M\x0004\x0004\x0016óaV:ej5u
ô\x001aÔ\x0002\x0017ô´¢\x0014×zzýîÅ´5¦\x001dÆ\x000c8)ajÛ+DJK
úfÉ½®æt£6õÛK\x0019ÅFbï¢,(Øñâ%¾ÆôG\x0019jÌp¬UU\x0011[UÈGÅÙª£a}ôÕ9\x001bu$õÑWçl´\x001cVG_³QFrX\x001b}5Îh\x001al%1éP{{¿)z<ÿüþîã§ýf4¨KK¶\I¶ÑÓ^/ßrÍãùë'Ï^ì2í\x0015jV\x0018cÅØ\x0004Õh\x0000ÔL\x0007ä&Ô=­Ø\x001ebU5«:îu55«9nV[³Ú1V	ëä4\x0006Mmö¢y/Øi¬ìÔ#7\x0002ëjXwÜ\x000bëkV?º°e.§WØ¸:¯+§VkýÀ÷\x0001VÙ\x001c.yÜ§«\x001az¤ièÑ\x0008,æ0;åÑô <'À\x0018ý@
Ñ\x0008m#\x000bä¨0\x0000Ï\x0013à±0;\x001aQ\x0011¬} [ê\x0008ls¾äè\x0001Ó%e"@Á\x0001\x0007frà:*¡
Yk
YÐzCÑ\x0004\x000cyÐÄzÐÓ\x0005­óÓ×\x0000-4\x0001Z\x0006QÅÊìðÁ\x0001\x0010L[\x000e
\x001e²íqÂ\x0000M]\x0010¼Âb¦=J
ò:+©ËDÍh]q\x0011z`Q)D\x0013ÿ?`
Ó~DU#ª£DÔ5¢îE_O½ÌÍb\x0013"
ë\x0002¿#\x0014»ÐÔæ(\x0017ÑÖ¶\x00115§UH_&C\x001aWÊ+¦&7¡«	]÷"â4C"w@9påº×óI\x0001\x0011}è»\x0017Ñi,¶Na\x000eaËN4äh\x0006ïçGt-F\x000c5bè_E1Â¼á>³/EOÃ½UÂ(´	£KWQqý,\x000e}Í9Hq\x0015\x0005¯biÝÃØ
înÉ
Öñ2Æÿ\x0019×\x001aM¹ßñKÏÏAZÌ\x0008
#t3*UÚ°Ô&51â\x000e¢ÆqÓù(ÝvÝê\x0005°ù%·<_H\x0017É\x0018vdÄ-flÔì×/Jr§^0çëÀÁøëÙ®ÅÝ\x001a&þçTøò­u®åÑÞB¾ù^\x0004\x0019\x001b
#ûU*\x0013\x0003p\x001dis\x0008¥1ët~ËbD\x0019¶,ø\x000b´$8NI37·ÿ^âû\x0002ã¹­C0
\x00106\x000fæ2vËÑBL¹xù_3¾/Ô-ä±RÚÒ\x001e\x0019e¼µ\x00068ÞÊd\x0003ùøöþýÏ{ûÅ[A\x0019Al#_§ô
å\x0003¢¼b|üòmüi×ÞdTU£ª!TsI]à\x0016z.ðXÚ(\x0004Ö!Õ5©\x001e"õså¬\x0016ÔIzàüHpÓñ=C¨¦F5cªi\x0016h*®àÊbÁ^9°ÓÆ\x000cC¨®Fuc«jñ.P±L\x001fhU=WY`Â5PC\x001aPb\x0013êà\x0008 JVS¿Ñ\x0008©lÏÿ\x00000Ò³îtÊPÇpé\x001dwSÅm±\x0006+4\x0002\x0000$À·bUÍºªã\W-·0ñ\x0017\x000e8ysu÷éãÕ^Pçð,!¨Ð\x000e·-r\x000f\x00047u\x001f\x0014Ê7g/-`t5£;NÆP3ãbTz{j6[úþùÕ?^ßÿ¾Ï&Á\5jD\x001bU?5GÛäôJ5P]mËçgo¾vþö?÷£B
GªjT5ªl\x0019nå
\x000f\x00066"pãd=\x00086ªkT=êÊ|<Lû%oä<þ¸À»tÓrT[£Ú£Þ\x0000¡F
ÇZeàè<\x0007`d\x0007\x0018\x001eÂ5\x0000oÖ²Wg½»P[a5&­|êBPµ¤$[i)Ã\x001cå:ËÚH+yÔâJ62@	¯Íª·#D:Gß~úrúþðñ§OW7»9e4Àó*déí­xÈqü÷\x0013'Þó/Þ§¦£?<{úâìb?¤ª!ÕBê\x001aR÷BÀT`j\x0018æ¸³?*\x0003öØN3Wû\x0019MÍht!]
éú!q\x000c#5
Ã¹\x0019ÜÞ§{iG?£¯\x0019ý.d¨!ÃÀBÊ2uD8î/Ë\x0000s\x001f¦cë»!7úRS4¦{)mãZV´\x001b÷÷tlo?e+&\x0007ä¤tÜÌ
À\x0006¦Xm)å´?ÜòáÞz;\x001c£)\x001cs{R6¢\öËrLR£\x0016Á 4õB[>Þ0õÜt.d#Èe·$O]Öh\x001dç¾RÆzêWXH(·dd.ÙÜü|usõÛÞ«°Äj\x0014Ö\x0012¼\x0018íàE/;?yòýÙÅÙ\x000f»nÃr»ôD6Ü±Ó+»'H\x0013¨.£Â¼ï³ÓÔfÓéSIÇ;\x001f£Ä\x0003nhA§sÜF@m
j\x00164\x0002
\x0010ÂÖÕ\x0014,Ôz\x00087m3\x0002êjP7\x0000
è¥\x000fïiØ­ÔÜ¤\x001a3¨ÖÀô5¦?âõ\x000c5h\x0018\x0001

"¨)\x0011XË]¤[å(m\x0014¥¤Â\x0001ÙdY\x000fi(òS3ç\x0003í	G8UÃ©3lMm¿hûÃÝÜ`¦áÞF\x000bJÈM.HÎLÉ##\x001bwô\x0002¹¸ÀLÃÝÝ\x0016\x0008Uþøk
+\x001fýzÜ´w-íÝqÓþ£¥ýÇqÓ~ji?\x001d7ímK{{Ü´_ZÚ/ÇMû¹¥ý|´ ¶Ó¥U.}þþöæãõÝþ«
S	Øó@Iª\x00026®áEó<>;¿\\x0000	5$ôC*S®y KÏÐP&fËùôÅåªTý\x001aUÒ¤ÌP8³¹Ë!u
©û!Ñ¢ÙÍ\x0000¥­Se%§1¥~HSC~Há¹7'îÉ<¸\x0008Û,ñ­~GCºå¶´ÝNYîi¹sw§`ïÈ\x000e\ÎèjF×Ï\x0018¯x\x0014ÁÌUAmX¡xp°öÁ¾ôý\x0010
$ÖCÑJÚr\x000fUóS\C\x001a2\x000c|mÏiBs[{ÇÏmóápÆ*É[µIÞK!Eày8`,¹\x0015×WrG_àå­Âé×8.jFêó\x00078I b\x0004¿\x0002d£pd¿Æù6KÙ\x0008sÙ/Í­ë½ÝJ(n~\x001aoÅ¬¼½=\ËFË~qn½À\x000eei-\x001d,Î½à±Á,øâ33zÔv\x001aµjÓ¨"jÃù\x000bÊ¤R´\x0007\x000c\x001dÔ\x0017\x0012\x0003ý'Ç\x0004,ÄÍqkA-\x0013\)å\x001aÒ\6}\x001dMY·u<&³RÊj¸L\x0016FïR\x001aÉ\x001f¯¶8¯ú\x000fÑf8SÜ¬9¸\x001e\x000f\x001173òzÁ>|ÝÎ\x0003³fs8¹¹:yuýéÃõÝÇ=C³ADõ­7#¾ix:X²¹ñ\x0012'\x0017g'¯Î_üùüòÙ®ÙvkP\x000b~Pé]à\x0019MFXj;*\x0015<\x0007c¶=}\x001f¨­Aí\x0011¯¨«AÝÀ\x0006\x0010§ÂR\x0002.qWYFÑ¹Á\x001d} ¾\x0006õG¼¢ªîã°ªjãÛ¹°¹ìzkaaÝmçø&ÞØïáÅn´¾{$oR\x0019¢ð\x0012ñmae]\x0018÷Doø/¿îÙ\x0008\x0001\x000cSÑÂ£^\x0001Ê\x0019vËù¹R\x0018úDøóWûA¡\x0006\x0011P¥yEqØÄ;÷à´ª\x0008:Ûw­\x0007TÕ j\x0004T*\x001c\x001a@½¡\ePs\x0000c\x001c\x0001Õ5¨\x001eúôÀ%TÊ{ndç¸oP4Lg§IõpÓp¢\x001f\x0012\x0015ãÚJj¾a8QQX3	yÚ\x001aÔ\x000e}y_2*%ÐØæøå\x001dG\x0014í4¥\x000b4l7Ú\x000c[9\x0004( î®>ìN8¡Yó{Çã,¬7t·bÚÎd\x0013\x0001C\x0001uyöç\x001dÒ	¶óÔ¡ÍS¿?ùîúþ§Y3ìtÜXZÐxü\x0015\x0015PáÀ\x0003º2Y3\x001b¨{{òÝùÛ§ÑÜÛO©kJ=BYËãâvè òN6\x0003¦Æ4\x0003!ªPê¼æ\x001djÓ©8MÑÊi\x0001L_cú\x0001Ldój
 lÊ¸\x0014\x0005\x001bï'cVN¦­\ïåÚÖÄï(}\x0000GÂ\x0018^Îi
ü\x0000gsäÈ\x0019¹6:þ{ÀÌdr~\x0016Î©ôìçÔÍîÔoO\x0001í¹\x0002¥k(ÝQJ»#fK(éø¼þín/%¨(§V\x001cs¯¬oÉÓ\x000c\x0007´>þÏó\x001f.Ê\x0006T\x001a'HvFRGÑ¢hí«PH\x001fô(÷ÚÔ\x0006S"Q¹Sï`,÷7ñ\x000f÷¼XJ
Û%Ð\x001cÞ<¹½¿ÙÛJD\x000b³¸`Ùã\x0014¥R\x0019³4_sþöäÉË·\x0017;SÉí@¦\x0014­b_\x0006©$7(Ã®zTz\x0002Øü3CÚi\x001c¡\x001fRÕª\x001f\x0012$Xµ4:\x000cæññÞ¼ÃúX
©kHÝ\x000fi$ßã½ò¹=_ßt]\x001b\x0016B\x001aÒ\x000cíÉÀ­þ\x0014f[æ=ÉC\x0006Í49aq|Ëí ¦l+\x0002:ER]\x0005)¸ú]IÅ
ó`:Y«\x0015}
é»!ãW¥Äß \x001cõKqk*f^×ú\x0019CÍ\x0018ú\x00172	eèXÙ£\x0018µ#I\x001fßüPHÙÈ~\x0019)Ëì\x001d	ßþ§¼(ó}\x0019\x0016PngzÃt\x001cÂw\x001fº_\x0012>÷\x001fÍá·#Ö>Kz÷0ï=}»+l´ë
Ó1\x0003KI­:¥Y¬à\x000cú@\x0013©2\x001cb7ÓÏ\x000fî]V[ÃÚaX®èËJ»T¨Cÿ@Ts\x000cÖ×°þ¸a«+Ñ\x0003
èÒFùNF\x0012ZÊ4Y³j¦-y:v«Ða«/O\¸©^Ý\½ßtñüéæãçýq\x000f[Ún©À¦\<V%a:îèÕÅÙ\x0013îáùôâÙëÊû±	smùdñ.\x0003H77\x001c4Ô\x0016UÂså,©\x0007³,..fø¦á¸mï2tÍ8FÎ:\x001fÄp>ÈQj±õáqpV=\x0018á~a\x000bm\x000cWH	Âf;Ä9Î\x0001r\x000fLø,'èíV\x0017v»&ßN&b,­rÖÜÕ3Þ¸\x000bÜµWLû6ü÷V9Ëm÷±4µÛ«ï>¬
M²ÃYÇ8
'Ý5\x001fxo¦ó\x0015Iáo]ßÞ_}¸úüåîºüaÓÉnûPvôÿóõ
¦Íî½¿\x0007®I\x0012A#9Þß9ÏÊù\x0007¢]Uá{y³ûqM;é½\x0010W\x000b}*3®ä\x0002h'92â®B\x000b¢Y\1ë¡x\x0002¸\x00108@#÷ÛÈ\x0007&\x0011\x000fñ¶at7¸¨S\x0003
pÂî4àAQÂ\x000bh7µ\x0002ÇxUÃ;éB¿×G3%_\x0002Ò$Z_pg=ÐölWWMú/ãU\x0016Øfs<5\x0017k}I=\x0007:uònì 
ÙEàï0Èôüúîfßêb{ØâmÆyqï«hiOG=l$ïÉw\x0018gz~~y1{ÙOu:Ä\x0019ª¶x$.n¿|¸¿\GÔ¨*^]Ç\x0015Þg\x0012¦ùcC¨¬-\x0013Ý¬çðÝ\x0003\x0017×oEàçç\x0011ö"ªW¸ÈÑ2Üìkd?¬e©]µî]è¯<Yâ>bóã??}¾ú|\x001d
N\x0008LÍ-6´T¬lHæ\x0019¦ÊîîúOïïþôçÛ¨¤\x0011×D6°ÖñO\x001d\x0014"®Cßt¼\x000bãk\x0007TbçzýöòO~\x0019ÕïæZ\x001b
Ü\x001deà\x0015pT\x001e¥Ç\x0001ÀâÔg^	\x0014~tBâÖHÄ¦NXØ"±=8Ù,-È\x0016DBVu±èáÈ\x000e\x0013L<hWD\x000b\x0012o9\x000cÎËWrDÖMãõaä_?ý·¶îÁU¾>y\x001cïf?'ól	r´\x0014l\x001ae¤u4y55LuÞ¼ÊÑþ1ûÏO\x001eÇ»Ú÷³¾v\x0014ÅÙd³õñÈ­HúÓ»«OñOWév±hÍ¥\x0014\x0014ÔÚ+\x001cÞ^ÀÆ¥O/G\x0013ï³§g/â.Ïf/\x001eå=0¤Q½l?Áà\x0004wöÇJ£\x001cÜ´\x0006Ð¿ïMB×\x000f×|\x000féÖø Ñ|6ùDOÑOkXÔ\x0000¶hZÿEBûAÂ\x001a\x001f$î,A_\x0004ÍmI;\x000b,½©ÇH¯ô" \x0017\x0001¹Æ`Ä/\x0011\x0019ÐYï¡½ç¥¿Æ{¨ö=Ô\x001aï\x0011Yz	¯èök!ß¢ñ(¬õ\x0016íùUÎ\x0007äfºø"X]ß\x0003Ã\x001dé=0e`õ÷P­¼RkÈ+¼wb\x001c\x0019ßCrQUÞà\x0005ëÖÝVöG!ãa\x001fIØê\x0019\x0018mú\x000fO\x001e£ÿy©
tèHÏZ[{V^;È/"3\x000b^ä5Úù~}ò\x0018Íþ9Py\x000f¥Ú÷Pêð÷ÀhdÖ\x0016[aæ7¿@ïQÏ^é5´i_£NC\x0019}
køs\x0018l¤åók\x0008Eo\x0011ôóÑ÷\x001a&´¯?¯ñ\x001aÞÂR>H|\x000bL¢Í¯¡Vÿ\x001avëpØ\x0015\x000eÇ·ÝT q.|µ©¢9~Þ¸\x0019\x0012ëÉãøK^Â;áSí±6Rx«Õâ\x001f
Ù:»ó÷µâwHÿúäñË\x0017óÃÄ6ïà¶ÞÁ\x001dú\x000eXËf\x001c½C\x001aèÞ\x0001¤¦wðrÞ>\x001c{\x0007/ÚwðâÐw°i\x0002Pz¨=$}\x0007\x001cOß!ù³=ø\x000e[ßÁ\x001fü\x001dLe\x0011ô\x001dRú\x0007¾C(ßa\x001d2ø\x000enë\x001dÜÁß!¤ä\x000bz\x0014Ãw \x001bäk¼CØÚKáà½d\x001c\x001a¼Òg\x0010!Ðu	·ÒÊG:¨v+áÏ\x0007¾B¼UÐ\x001bD»Ãä7\x0000ÍoàÍü=iä
\x0000=HÕ\x001b¤\x000fz\x0003\x0017dÎz¯\x0010ÿû%\x0018LM¥\x0003Ýö\x0017\á\x001d0Æ]¿Cúù°wPXC\x0001,Ù\x001b\x0001áÃ`ô¼ë~¤+ã\x000fÌ#ü1;aËÄ«ß%NÝ[5ºlô©´ù2aBv80ÊÍ³¿¥\x001e\x0017\x0017gOwYÞ\x0004mZh3\x000c®^¡½<%fÌ©ÈÌVìXï>æÐ.t\x0018_h\x0005Øo8"c'f¥è
²s%fÐ
3èqf!SH\x0013¡\x001dwQµ\x000fHÐzº\x0013Ú¶Ðv\x0018:êÑTÐ\x001e]|«¤ë±Üá\Ì,|zlã¡÷ÛWâ'w·\x001fÇ??EêR~-\x000e\x0011\x001f#´æN¥ùCñG%^Ë.ÅO._>ûOüóSô¬î{\x0019¿õ2+½G¿WÈ¯c5*:%C>«Qúîc¯\x0003fä«\x000b\x0019Gø#\x000bùûW\x0011ôãb\x000f·6%\x0015cI\>IðXÁv
;>	É÷·'¯âïçÉ\x0019\x001clÀÓÏ£ä\x001e3»d^ýx_Ä6\x0011h¦I¼¬¤ÕÇ6\x0011k+Ù.yúy<D´lé`@çÛ¯BäS¬´õ;ôR'9\x001c>\x001c[1$p%13(Qi·×ª\Â-Trõn¸£\x0012\x0007Ù8\x0017/¯þ\x001b/ê\x000b¹µW:õ\x0000ÓF`ÎbÎJ·hXf+&ªÕ%nÅË³¿à\x001d}\x001fº«ÅzäZqÓÓ}&öWnpd©Z:½Ä¸Ü\x001c<Ü	º\x000b
ÌjÌ#-x)	Ý¯´èèX#»ùÅ#ü±öî\ÞFÁ¾Ø¯c¼9Õ9¶á¹¯ÇÐ|v¦\x0007» ê÷úäòeüa§C'Û\x0016Ü\x001e\x0006î²%æ±¥On<£\x0008\x001d{· L¶Üµäî rçR'/D·\x0002Úñ-J\x001cÆ\x0005\x0011¥èõFíÞÙ|\x0014ÓCK8oôh 	Ã¾~»À¬Y.U÷òUÇü"Ã\x0014Âxt{¤\x0000w\x001co\x0011;\x001c\x0005=è*¥ÃT¾KÌÅ3MÆQ;»0t\x0007)Ï\x000fïJÒ\x0007úúòeIì¸`W9H{2j\x000b¿¬vMäÇ\x001f\x000f{\x0001\x0010©\x001f9¾@¼íQGEk\¯2¸y\x0003r_6ë?\x001eÈ/Ó\x0014ÙÄ\x0001¯¬"½\x001aùw8À;_\x0000#u®ºfcçÅÆÉ\x0014íøï®îs+E¶/vÀÊvXÜðò\x0018\x0014bñÑ:[à%æûwgoç£0¼ô¢O?Ó[g\x001d6eDcL\x00037JñF{ c\x000cv\x0006èA´ômºk?}î.ô\x000b3¼1R\x0011½Ú!3»é¡b·\x0014\x0019=^@\x000e_Å-\x0002$w¼N}5\x0010ÞH9o
À·»>ý|\x0008¼\x000cØ¯(Ñ\x001bÃFB<\x0003èõ.wM\x000f=æ@ÊÚe\x0013mðôsD¸«xÓMÒ<n\x0015j¹\x0013¯6oºf3ÈÒ»©A·Ôéç1j-pò¢Êb&Þü²4RSª\x001eº?öð\x000b©ý\x0016µ\x001f¦Ú\x0012®\x0002ð\x0000n#m ¥÷³%)\x000b ±ÂµN?\x000fB`I&zöd:Ñ²dû×ïÐ§¡\x0001kVlmE\x0013Dn\x001dIL\x0019Yî×Ã¬SÍ°xYÂ=ô¨&=
Vúe\x0008Ev;$\x0013¼náõaðÇoKFK
æG#â\x0010ÿ¸L,w-¼;\x0008^\x0006î\x0004oK Z`\x000cï\x0016jÑEðà¡O?Ó[)Bê\x0015¯Ø"Ú¹\x0013s`)J\x0016ÕÅ\x0008S\x0007½ß¢÷\x0007ÑËÜk#ÒGSÖ>ÒÓ=[\x000b-×Ú8h<Ú:b/\x001eÙV6^^/ÎdÆ|´·RZ0¥\x000c¢ÃJÊ
6bÞ·\x00113ç;²ÙÙqf\x001b3Df+BN<EhïJ*ó¬ü}ÐnÛ/à²_ ì«_rýÁÂ\x0003ªH3ùð*5v<Á\x0003êSÓù\x0014òpzÑ\x0016~öúÍåÎ=Ð}î\x000fE'Ù&rzF·¾H¨/#7u4Ï=2Mä·\g§£v!^ëò­ÔÛDöú§[hÀ-\x001c\x0004\x001eÜ?\x0003;oK^rò\x0008H«wDÈºÑu³[Z=Úú'tP4\x00043ÌÈv^-H;Y.E»ÑÓÏãìQÃS0ÕëÜ\x001fÙaû%Þ3Vd÷í²o¥Àõ²Gïr>þÏ©Å¸6°é\x0005v\x0012Ú.}/U\x0012¢¤ÚÐÀ?ÞÝ.èÎx`»\x000b;¥få\x001f¯td¢Ç+Ë\x000eòz~Ø³Ë»dºÔ\x0008^\x0010èG*´\x000eÓ××¿Ü~Zêu4!¤©qÜ8Å#Yf_¯rß®ò:¾>þòÅÎÄOD×Õõ\x0019}<Ê£[¡\x00146ÏMèQêl³4\x0011ÑÅ®$½~tÝ¬zs	íG\x0007vSGtM3f<\x0010-H³ßlY¾F[\x00173Å\x0005«Ã\x001a÷'Ïïï\x0016ç a|÷Teud£b"\x0013 Údoyí\x0014={¹3ûHÁî\x000eù\x0017[]GN¢y÷¯ÅW(	ÉJô\x001bGZ­X²Ä9®£QÈ<þë^îêb\x0011¹Á\x001cÀ(mÊh.QÂI³\x0019»éùp(¶o°ý\x0001Ø»\x0003HÎcÂ åÆXÊ¶¨­WYnØÞ&\x0000&uH)¡dñ\x0005\x001a\x000ffÞßqSu¯E¼è\x000c9d»%¸µ»%¸­·åÕÇOËåIªöFo\ð\x0017Îr)\x001bv[TÏùìÅ.Yc»\x0018ÄØnüúún©(1\x001aåÎnMr\x0017T Qba/îõùå.I"·\x0003Òr+ Ý	\x001dud.uÖK®%òÂ3ô"¯Ö>f´¬ f\x0015lEÑÏÿõÓÕR}ã\x0000ôi¾p*\x0003D\x001dE9S\x001b\x001d\x0016\x0015Gÿõél\x000b´Sç¥*¶i4ÂlÛUËë
x*­ÆÊ\x0007j\x001fYg\x0013q©]µó®Á¡\x0005CÀsï\x0004\x001e\x000fdn#g"o\x0010x»(áb?8J@¨Î¤@Ó@lQ~÷ñv©,ÑÛ"sH"\x00005D2)Ë*\x0012+DÐSÏòËg/wÉ\x0013Û÷6ïmÕ.|\x001dõÏò}®#qÎÐô¸\x0010âæ¦\x000c\x001dåv\9«}þø<* ;=±;hØ\x001d\x001cÄnT\à5O¢w\x0008i\x0008\x001ev$ÑuÁË¤6kù\x0002\x001aéRåaöÇxAKÍ[Q<*\x001acM°äÙòÊ÷eîØý©ÎµáQú¹þ\x0012Onn¿,ý\x000e\x001e"x>º\x0001\x0002e¿ÄOÂÑPl;¼ä3<¹xùfçGÀG\x001doß9´Æ\x000buH¸½_é\x0015Úäô:\x001d/Ó@Í\x0016]\x0014=ô\x0005`k±tIxùv>ÛËþxýî÷ßß»\x001fs3£ºÑÿû_ÿûìæ]8Øn\x001bæß>ÞÜ\Ójk+ÞrðÂä³\x0015y\x0007ã'\x000b¦Mó}ÿäìâñ¬©\x0018q.À£ô\x0018*îÑöÍj(h£	2\x001eÓm54\x0004	x3K\x0001È(Jsy\x0008^w¸\x0019dP\x000e\x0014­ä4?\x0004i°Z:=ú!]\x0014À9Ë\x0006»\x0016è<\x0012Ô\x0007ì|A_\x001b¶½
C\x000eÿ\x001aWDz\x0018­\x0014Yå\x00049ÏÓ£û Ý$\x0017e\x0008Ò£<O\x0001È¸j¹ 	»
dB\x001boDh'îì\x0011B]´\x001eåç\x0000¢ò¹O<4Âaf{J+\x0011yT<4\x0010ÖØR <ÎÏ\x0011H'Ó\x0014>¤Ä\x0018X¦Ô!·w
Ö8Ú2Säç\x0008er\x0016Éx»S4ýÕG
ë\x0008QNú\x000c"8$~"bJ\x001dÊÛæ²_LÄ1?÷$ÿl\x0012 Þi\x001fåg?¥ÿ9%mu½!ß£¥´Á®!ÀaËü\x001cD'óE\x0000wP`J>ÞS/Ä\x0008¥èôÊÏ~J®@Gb\x0012,5¢´Ñð`YÞ´ò;\x0012=­ù9@éÃFNjA5|ViÇ²|bÍ
A¦fÛù9\x0000iÌ&'\x0016JJ2Ú°],FÐ\x001a\x0016\x0015b~\x000e@*gÐ\x001f\x000e¸	4\x00160Ú²\x0011t\x0000%fôççñRj¦z~\x000ePbÅ£eÒåFGÆÒd\x0008©W:Uêäç\x0000$Fm\x0003ïJm5c,RÈo»0Æ ±ów~öCböaÎ Äü!ÀEEJtóDW\x0013GË\x0018%^)u]ÄÝEéRºDÒ;\x0012¨÷Ù(Çiïº!2*\x001fßGL'\x001e½\x001fÑáÉ)è;Nð\x0008¹6+KK¹\x001d\x001aæ|9ß\x001d;çUæ¼\x001aáÄ²+ÈW2\x0000G³C\x0002\x0018¾Ü¦®Í+q~È\x001fp=¿Ü|þýË?ï\x001d`U7\x000f¾¸þWv«î=C8²(Å\x000b¢ÇùjÉÞ0Àwp/&>ìñüäâü¯óÎÔ2êzÒKuêT¦\x000cú­¢_äIÿÒQÌ÷ Ç0ñFæi1\x0003ùiXlú¦Ïõ!)\x001d·ÍÉ]iR;Ãb®Ó'wÆtÓ®\x001d£h¹Y=´q\x000f
ºT¨22\x0006+ÒIQºipyô{@y\x0014ÿk#º¾:wÐWG»|û\x00184 Íiv*Ë>ÒwôÝQúßþ[©¤TÔ\x0010¿¼¯\x001a>yrûË»ë«ë¾_µGS.Õ]I\x001eüì¶Ç¿d»Gá¼S·£«øåóÇçg³î\x001bX©À¡\x0000\x00057Jíø!­+6r¤IQÚ\x0001äs/ñÖ¢\x0015ÁK4GâmÌNÞä/L¸
½3y\x001bH£%áj»ÓÑÕû!ã~øà¾Ë¸ïþ ¸W\x0019÷j\x00187ää\x000cäµ´y±Ùª&ÞÔÄbEÞ¿eÞ¿ýA÷:ã^\x001f/î»?ýþß_R²QT~cbÝ<¸0·÷,Ö\x0012þ\x0010V\x0007~\x0016°\x0007V
Ví}{ò4þá,þêåÛý´\x0012«fÒc\x00107(3þ£@\x0003\x000cìÔá(áºIXî\x0010\ÌÝU\x0016q7nT
Ae\ai+\x0004PÎóêîvHõá¦\x0002Ðº
´\x001b\x0017-@AÆh¸¦\x0019×ì6f{q-â\x000eo\x0006/¤É9D+©Ö\x0006û¸\x0001ãª5W\x0017¿\ãb¯,u1è\x000bù°ýfÜIÍäA¸\x000eqÝ\x0001¸\x001a{ÒçÕõ4\x0017>âÚ²w'YÁàbK¼ô\x0018ÅU©ÒWWÐêJºáêî¼Övâ¢\x0017\x001dô\x0001¸\x001aÒ\x00142ÂÍ\x00118mF2.¬¹ºXO\x001e£¸FZ]&\\x0015dXSM\x0000\x000e>HaÜJ«),AI¸XÃF¸Úp\x0003â\x0003pévU¹\x0005U¤ÕE\x0005ÃÎO'ìvjD7,&Æ8¢5×\x0016Ê=-âNÒ«\x000eÁEÇ^zâ:GÞ®´¸9£7(§à«¬.&Ù¤Ç(®7\x0014FO«KÉkÊo6Ã;7%J«qÁËhÕä\\x0019l\x0008Km|\x0008nÒwá\x0010\LQnü E<w\x0006ÌöXÎ§\x000fÚ¸²\x0019Ö4\x001fÓô8\x0000\x0017|Ù\x000cÊ0.ÓN²0\x000f¡EG­ÖÃWLËÆ®:
\x0004kC¹I¬¸s5
\x0019]åüÐJ[h%0®ÿ\x001arAcoE\x001dÆ¥.â
UÄ+«Ëæ+Ú\x000b\x0006»§Ç0n\x0000q\x00055òA\õ5G¾¶ô8\x0000×úr\x000bÎÍñ\x0010·Xc\x0011-àâ¶5\x0007í]À\x0004OÆFiø¨íÉsXûñßÿø=ÕëËÎ4\x001dÉð§¿Üß|¼þô§\x000f÷zzµä~Mðrz\x0016Øe+ç)åéÌ\x0019-v»x©éö_Þ^<;O\x0005 OßíÔ[\x0008¦ÍÛû_@ÆÕN³Ó¤ÂzÏíSÏ×ü\x0002°û
7ú\x0002¨òÀ\x0015^ î\x0011¥ó§û$a[wz\x00011)[ã\x0005&vÆø\x000b¢x
\x001e¨ÿ\x0000î\x001cÞBrÒÃg\x0017H'Ý\x0004\\x0007_@¤
è{Í_@\x0000e{aðc·wpð\x0005Ðs\x001e\x0007¿\x0000^QÒU0õ®Ê±x\x0017\x0002Å¸¥þ:üÈ\x001e\x0000y#ù\x0003\x0004¬\x001eÎ\x001f}rIê\x0017Hy/ÓÙ\x0005Ý/`¤\x001e´ñ\x0003(A£t±±>}\x0000å&c¸Öx\x0001mwÒc\x0017Èá\x0007å±+ä\x0017ðü\x0002û¢Ñ/\x0001Jq¸\x0014µÁ°'\x000fÛÔ\x0010rñÚÃgX¨¯¡ÇpDý£ô8ô\x0005pTU*ãÊZE\x001e\x0007ç_\x0000`wJÚè\x000b`+»ô8ø\x00054×h(\x000b\x0001+éS¥ è\x000cÄç×8\x0003\x0001wOXc\x000bE£\x0001½hø\x0002\x0006Kaó\x0019pÖÿù\x001a/:8¬ -æçd÷°Â¾éy\x00079\x0003_zÎ\x0018?V\x00048Ü³\x001eã1Ä/Ø\x001bïRIzø­¿Â\x0019©ö0?\x000f}hîÓ
Viô\x001aåZu
\x001cO\x0010nÒ£n7Pé
\x000e·l´óèø\x0006ÑP4lÂ±-$öT1õ½Áß?Þ¿ÿÇG¼ÐTBR½Àçÿ¸¿úrw}òÃÇÛÏËv?õ\x001bÅÝ\x001fÐ"ÍÛ?í¿7Yå?Þ½¹<?ùáÙË¹êÆ
9µOad\x0013i±m qrq±=åJKÌC^\x0011\x00194fÔåç(3d ÌéxIÔT/\x0018\x0017ÜÑu\x0005;\x0004®Ë¬\x0012ó\x0001[CcÛefæ¢ï4ê(\x0003Oæ¬\x0000øøÎ_q_ _"=ÊY|susÿùóÕûE\x0017r\x0015È1Q²-¬\x0014Ý¦À\x0019¹G\x0008¾9»xûúõÙ½¨ñj\x0019ÿªü\x001cc
êTåT0=`^\x000br)\x000f{Ò*zX±cF~±r\x001fkd\x0015\x0018HëêcVØ\x0015ºÕböG~±bSÜ\I\x001ao><}UI®ì	j"\Î5´òsp¿²C<²ºSIÛU*FÝ]>ÜÔ³Ã¨Æ«È\x0018§¸O¡Í¬ÓÔ\x0007°Äj·k
Ý$V/)	È+ë4³Nº
³¦íêÆ·«O
í2«£&ÎQI^×½þå¬Þ	ÌÿqbXd\x0001\x001f-++wµàåvW«,@½þ×í/¿£	½Z5pÿïûENé<~Yªø¡y\x001a6J¨|uûÏÿÛÿz»1~\x00193Æ±¥lë\x0006ã¨\x0019£\x000f¬VqÔÄ:\x0012³D¤´Cib/9'µ#«Ð{ÃÉtq)÷\êb\x0002vãM\x0001LcÄf1-MÜó6°%¨ýZ_<õT^\x000cab¾:\x0019¬ñ.F\x001d-¼\x0011ì&Ò{*Ò\x0016cât2LKÔC_Ý§\x0014Zr(\x001aà~\x0011C]zO\x0006e\x000f¦O~\x000cS@ñ\x001b8%JM¥±RO[ÉbbÛ¤ü<fÌÔc9?G0¡úè,ç`±Ì¹/\x0012´\x0013\\x000eþ¸0ÄÃKsEZ<D\x0006?\x000bÍ&Ôr¥Ý\x0019[,7vJp\x0006«%'öâ¼©t\x000c\x000e|!-dÅ>WÀbN8õ8'ä¼=&±á$Å@q\x0007&Æjòs\x0008SáôÈ\x0014iÅÞK0©ÈO\x001a·Úr¢æÍÏ\x0011Îø­5aÜÚÚ¤©iÃJ»3u?ÊÏ\x0011ÌhÌ;ûbO<$Rqý)F×Â´	sH\x0013\x0005N^ñxðyÊ»â|!å÷ßbú9øÑãjz(\x001düd5÷8Ïrêd\x0015çç\x0008'v¸ÍQ\x0012ï,ö\x0005M¬ØÛãËYJ(?0iPÄÔcú&\x0005vSïwâ,äÄÜÃü\x001cá×àÜç$Å-Ó-3rºÂ©Ä:§\x0008A`O1\x000b\x00043©¨§\x0004_^O¼­£t:a3Åe\x0018ã4ÁÊ;1ðzFKÖ\x0013ô¾Tå8\x0007\x0010§"\x001fw'\x001dþ1qzÁ°Çñ¼\x0013\x0014&9¤çÐwwÔ[BYLÉÏÛ³\7`25r\x0012Mü\x001cZMG\x0006²!÷áÁÅô\x001bÊ\x000eB·G~\x000eaJþèÆé\³Ä±!þZ8\x00077§ôäúRÚÑØ»tØÃ>ìõÔ.åÔsð³KÉ[ZSô&}÷,¢·2ÒI\x0019éQe\x0014/\x0019¹âM¥>¬|Ø9ÃZØ<5Ø\x00139G÷güî¼8¿{ùìûb\x001a\x0014\x001bù9=2äø\x0017ªÌ`\x0019Ó¬$âÓx§ü\x001cÀÄÙ¼8£Y%N-¸,\x0013sWÖâ\x000csè6\x001câÿ\x0002;\x0013òz*ÒÀ³iï:(Þòsä³\x0007Ë\x0016²¶²t\x0018áÊ§}ozËbNÌrÏÏA)\x001fè»ÆÚÑ,åéÆ!¢mº\x0016'ÖÚåç©$©R4\x001aÃqÄi)[Eìi;Û,%3h)\x0019t\x001f*\x000e\x001dã )%vXk{z´\x0012òsSaL8ã].s \x001dsîm!´Øl\x00156;À;×Õ\x0000©SÁs¢÷#[F°!^V
\x001c é»Lún´x»}\x0014úI7º\x0003/Åö»Oÿø
Ã0©[¥ÚjSþêæêÓõ/×KXCË:\x001c`oZª\x00137l4ù*ª¦1ù«³\x0017çoÞÌ·ÅÞ\x0000c\x000bCüg\x00148\x0015X\x001ajÉKå«Z\x0006\x0006¶\x000f/î ±DïZz#;\x001fké:lÙÐ÷v&»k\x00109uJad©-Y\x0001Ñ|\x000cT\x001d\x0011´\x0015\E#gÄ× ²ÂhZz#Ç0a£9¯Á@)\x0002±¯\x0001á\x0000bìäEå·;^\x0006£T©liN>ºÁÖC8µâý!Y\x0017CªpæfnÒÏõÅë£¾úüßÿ\x0008ïÃ¸c3Q\x0007H\-IàÂ\x000cJ®i\x0015ÇCý¶µ"XãgÚoæÒàèÙÉ\x00115§t©»:c\x0008Uj®s\x0017^dNàPÁîzWójÓäkL\QY\Dê8\x001a1\x0013É]Lúî\x000e®íçcùµ\x001e]\¼º]Ô®'qÚ\x001b)ÌÆ/é¨9±µ/ÎO^ÍOÕnrnÆq1¡\x0011p\x0014Lú÷ÿ¾û¨Ó.Ã0|üçÕUÜX?]ó\x0000¯î®ÿu·È2Á\x0013e¥ã\x0016ï¾¸ôLô\x0018'¥==ç)ß]ÿuvòeú\x0010dèºDhsûoïC1QÕL÷03ºLð\x00035\x0003\x001bN\x001f	ÊqÂ)E\x001e\x0006:I\x001f\x001d¥Ï\x0001[Ã[ìþÀwY\x0007yoY\x0008i=£\x000eÁ~°ßýÑ°ß'ì÷4ì\x000f	ûÃ\x001f
û:a_ÿ\x0011°oÝïÿw\x001aë\x0006XS§ÉÝ¿ÿùz5\x0010Å\x0006\x0016ýåÜ\x0019níëã\x0005Ëçü@àë³·Ñ47\x0007
§Ä&B²ê$Ô\x0007ª<\x00071B$yY5p1í&\x0015GA'}nº@\x0001\x001b¦Rh\x0015]Y@°EìÎJYÎiBTFé1Ä)-]^wu\x001dØ°Ô\x001dÓµ ¨4pI¯|M\x0011õ]F}w¨ÿºR~¾mÍëMË%Ö£\x0017ØÛYs\x0000¨Z-(à¤ðp¼%\x001a^\x0015;Úw~þ]Ú&À¸|=q÷óÉ_®nn®>,[Jc$7éÃ\x0012RSn,\x0017vYñ° Ý\x000cÛ}}ò³³?ïXÎ
-úpða\\ÕPp\x0005áz\x001d
îÃë:Èz\x0004©\x0003xeà\x0006L\x0002µ\x0000¥\x001eæaVÌ¤M\x000eòb­1þ3Ê«ÑÓI\x0017ìx²$ñJ_Ò\x0012ÝÃGk×bß!¼rl°\x0007WÒ\x0013q\x0005ù³ì\WêAÜ<&#MÉ\x0018ß\x0011@!¹HìÉ\x0003\x0017w\x0004gX9\x00130\x001eG~ßý¯\x0012òÕ\x001f\x0006Y'¦í!«\x000cÀ½s»q5!Ït®\x001fG¾JÈ\x0007¬ò7A¾õûõw])ãW7Wï7]ª#ï2Z+,§2£W.\x000f³öÎrªq3©á¯.ÎlúTGÜe°Ù	v\x0000¬'X\x001dh"1Â²\x000bq®Êb\x0010\x0016£âã°R`kê\x0004kx\x0002q4x¡ÀÎ8é\x0007a£Â°\x0007À\x001aª\x0006°]fÎqÑÒl\x000ev\x000fìO_þ-uÂ"¶Ò&ÞuóÞ\x0005´\x001a'¼¼´6H·"$\x000f>vä¾\x0019!g4wÞ0wá\°
W"ê}^×«ßn?Þ-[U%¨Ë\x0016°Ù¯Û\x000b\x001a=×Çóm^Ó³\x001f^>ûÿ©;·äº#]O\x0005#`Ôý\x0012|\x0002)H\x0003\x0004x\x0000§Û/\x000e%È\x0010@\x0003\x0004-é©_{\x0008=îqh&=SYU«j¯½.U\x000b'Lw\x0007·¸aúX×¬¼üy>óz H\x001e{\x0001õQ
Òr
¯\x0010,P´á\x00110UlÓ\x000c	%¿¢\x0013\x0012\x001e9z\x0000ÚM\x001a\x0017(î&5%5ÒN	Uu\x0013Ú!%ny¬©\x000b\x0013©\x001bÍèrîâl~KýBó|b
¶ÖSEÉí>&nxx}·jè?GS*:A\x0015&¾i5U\x0018²\x0012§_åß@AÁi\x0000DJò\x0013<\x001d_=~¾¾½Zç~sÐ·(õJTN[ÈÅ ¬Ë+T\x0008;Dzyp~xñîèäpÎ÷vÿÈ\x001e?¹ä2\x000eÃ:\x001c{~óÃJo!ð¼H=ô¸YÑkë±¿µÖ+±çÇ¯f]\x0005nêôãbE`àåÐ\x0014,ñ
lò¨\x0017â¼»±ãf^®òí¯9\¨)s\x0003¥OÅäÒíÃåq5lY\x000eÜ8l\x0011\x0015Þ\x0018×L`Sv7Ñõ¡\x0013XÄ·AøG\x0011ônfÖèÕ(£³z¯Ã5\x000cJNÏÌ|¯þ¯\x0013óõ¿\x0012óÄüá_ùcbþø3ó/Lþü¥þ_Üüp\x001b\x0010W%q@FZNGcÙõÒXÌ 3\x0013I1\x0017Ç¯b\x0007¹'ø_\x001f¸ùí/ÁDL:½PïSxÊ¬isgÂë=ûAµ
gn\x00122\x000e{(H\x001e»IÌÝÀ¯ÏfzÜ\x0011!¸ÏÒg;¡\x0004§w$4*7«	\x001c	ç{\x001bÎ\x0003þþWÏ\x001fcº\x0016ÞãÇ6ÛÅÕÓë§Uy\x001e¢^Öf\x0015HæÇ`¢p\x000bQ¯¬Êvqxùþèò|\x0005´0iÿl¶Áü¶¹\x0018ÎY¬ÐU\x0002û&\x0008¿T\Ø\x0008-!e^VyóíÐ±+\x0017AB1U#haP./¥Q·1s\x0016\x0019\x001eË?®\x0016áMÌscÖXZnS.½s¨®§r&\x001b©­w?y(1¯¯À\x0011\x0017·\
¯Ë=3¤\x0019\x00151©e´s\x000cµNõT¿×à[/ÅÅgÎ°\x0002\x0016\x0014Bûa¹§x\x0003(Ëæ·®è±\x0013mú`ãi!úiÁ~a\x000cÎ4t\x001f\x000c´\x0013)Ê]°p@À¯î¡UY²1¦uüöµ»sâ\x0015Ñ\x0005+cü\x0006X\x0006°8²
r\x001cFö9\x0016Ê_tÿÐ¡\x001bÔ&lîGà¬T\x0014Õ\x0010\x001eè£í_µÚ	ò'y]\x0008¬ÄúnÃÜöðñó+á¯>4ïo®#É
N'cÀ1FÌ¡v%EÌþkj¶¦îýñQü¶\x0008(`ÆfB\x0013¬ÖÜ.\x0010ô¹ræ¢Âpï}½0`¼g\x001d¨½°\x001ec¿tYbÖ\x00182|LÎ¶[Ë(b±Gúle\x000c¦¡¦V4åÔ\x0008ãr\x0002¨`bÖÞZ(\ì\x0008èlÏ02\x0011R \x001e2¸\x0011ùð\x0014LÍ
Z®eÑ>\x00199Üé7g]|mdÎ\x0010á?ß2\x000fLø¿\x0016a·W×á_ýåi]\x0001ðY\x00104ØÔ\x0006ä%TjU·ä\x0013k¯ÂçûËUX)Àöu`Ýëú15vO¦²Ð0Ö?<ÜÜß>\x001eÜ^\x001f|õôyÍ&\x0011Zæ¤AXwáÁ\x0004¨e%`Á¥[(Ø\x000egö«óã³£ï\x000f/ß-²Ç®"/Óç&øð&@\x000cð>,Í´{Â¡ýÃÒúÚ¾\x001eøhìëÊØïçØ\x001cÉ\x000b[U\x0006ú¼õ¥[\x00122í\x0017\x0011^lWæ\x0005²ëì5Jæ\x0005\x001eà\x0017Rãúà£Ò±VÿBðòîö÷¿ßÅ<\x0008(´fu|öíÕÝJOVRùI§0·*=·4(\x0013åÈQK\x001aPéux:ëÈ"Zåb\x001d³ïÄ\x0015G¥¬"'xihÑqíB\x0003Ã6ÜX¿®»G\x0017\x001eß\x000ekÓd¸îLrs8º\x0015v¢µV\x0000­è¦å\x0012èòàú\x0014nÔà«á8¸K"+p\x0015»¿}\x0015Ø\x0002\x00027¢\x001cÜ·OëZ¶;ÒÉ\x0005Âá
\x0019¨hH¶oøTïÛË¹~í\x0008	ú\x0018QÃÓvPzÆ\x001d6¼¶´XÃã-§O\x000b®Ú¶¬¦ôÒwQ³*ÕA{,È4&\x0008®'ÞW+)Å?þê?ý\x001d@
/ÔÈ\x000eÞÜß}\x0006ãóÕ2\x0012\x000f\x0018\x0013EL;9oZz·\x0014·}svú.Ó'ë\x000b`_uÞmÄU(\x000f\x0011p%&lqpÀ]èRØË£\x0016/Å´\x001ayÃ\x000b\x0006uM¸Ì²0®\x0005«2ò*fæO«6^\x0017ÍòøÙÉ\x001bÔÌkÃ£,Ë\x001aX©³h&H\x0007,\x0004\x0011x£\x0016¾+´ðy\x0007¹þÄëMàEÿ1\x0004j\x0016ï®àýíééþ·uÅhkgv	ÎäÇpyÙBgvj®É÷;2ªÜÿi³ë'þéÇ«â]¶VsC@¾\x000fÝ¦B¦>^á6X\x0000uU{É\x0016¤6
¤ô&ûªÒ4~UHÉÁÿU!%©ú¯
)¥y~UH)?ò«BJõ?_\x0015R
	}MH<\x0006\x0002¿\x0006&þáËÏ¿Ø¨4\x0002Ç·/¯ïµÊ\x0004ÐbZ¥G\x001c´\x0007ÑIÌ£§ÜÊ¥vÈ³ú\x0004HÈ½Û\\x000f"(äåü\x000eçS\x000e\x000e÷aç\x0008eä¥¹\x0016QGDÝ\x0002dyY0Zd´\x000b)
ë\x0018A+ýeúlg\x0004\x001f~b\x0014\x0010ñOÞ\x0005ås\x0016ÐvÉD[Ç¨}l\x0000å}Ïj´X\x0017\x0019=Jbº¶ó¢xk\x0019M´w\x000cëÚ1ÿ\x0019¯»¾w¿÷\x0017¢ñ#¯ï¾\ß­zê\x0018¥1²,¬\x0001YÞ\x0018Z\x0012\x0002Ý2SÂÁf|}vùþètÚ¢ýYØ«/\x000bñÍÕÃç»UÁC\x000fyý©¹TP{r6$ÏJbÌ»dô7çïOg"\x0005V2\x001a¿\x000e,yõëß~~ä\x0018c¬<Z¾
ïß¯Öä?)\x000f=ëãcExèH\x0010gTK[ø·à¼íåÁ·á±òçÃé$(ýÉÞü\x00103òÀ,áiå~}µjLM0%²hU<\x000fyr¿ZËq¥ôÊýújf\x0011]2\x0004Â&ýÞkÙÈÝYÃ}\x0011yc¡±@fÈîg8mLõ¬Ôjì ×>¬f7Ü©ZÑ\x0018+ð\x0017Kr²}ô?$ú\x001f6Ò\x000bGùê©ì2Ñg\x0019<¡[^Mýùo-\x0007ß'yÊ;O\x0007\x0017µ*\x001fBª¼Và´Í¼.,\x0016òØ»ÙÑ¾<¸M Ê±2v*d±SaIùæúáö·5Þ¸|#H©$6Ü\x0011,ë!2/f\x0003ùàì8:?ù÷iÛø·ßþ!\x0005¨q/ûÓ=\x000f0ë\x000eâ°ñr\x0010:¬$Å\x0000\x00071V.´]¹\x0008Ó\x001d~8=ã?ýþ·ßû\x0014MxMÖ\x0019F÷¿¬Óï4Z¡\s°¨l/Ü®xè'$§\x000c³73B|_>ýþéêCì[\x001b\x000bÚM1ã¯îA×b+X))uO2Ï¡^tp±\ô	Âµ÷ê\x000c-æÂ^ÿ~'#¨\x0006ÐÚn¾û\x000cgÀûßþøïu[)fÁ¥(\x0002é\x001d\x0002b6Ø\x0014ÛûùØ\x0017XU§ïà\x0004xsöïG³!\x001aÂ¶m7bCIxN@\x0011\x000cDn!ÐC·Ðe5÷Ï?\x001bm¡Ú\x001a\x0012\x001a_º"Ó;l²wWnÖl²ð\x0016U\x001cÂÐÑÚ	KÙá[T ì´[è\x000cwqðî0ü|¦<\x0019-Äá\x0007E­uØl·÷+-YF\x0019`eE:FlzB\x00145×­vrV,à]@Q\x0002.@ûBaá¢Ä@Ç\x001dö`\x0013Ò,+\x0001e	(»\x0000qS1iáõø0³[ë%*ùT\x000f\x0016¨l\x0013¬âà½\x00038QO·\x0012Pºk\x0000ÝPõ©Pü\x00012\x0008±r" ·\x0012Ð¦\x0007ÐHªå\x001cÛP;\x0011\x0002-&{V\x0002Ú\x0012ÐvN1æ\x000eK\x000eÁyi\x0004'rÈW\x0002º\x0012Ðõ\x0000º,°*½W/<Ê¿á
ä\x0013Ùy+ñ|ç»ÆÏ¢	~Ä,¤\x0006M¦qü&ÒÚ×\x0001rVÒ¬Ð2 I\x0014=IS¢pèTwñõ=Òu\x0018Ê!×ÂMâqÈ\x0004öÕ9Í»\x000ejËI£\x001bT\x0013pj \x0014³²\x0017KÕAÈ»NBëañ%BSÙ A/Ö\x0000	9§ÕAÃ»N\x001aèTÍ\x0005\x0016N¼SÐMÂ!7i\x000baµy×^.$v½\x0005øÔ£FTûDôìØ\x0006ùÂ>É#è,\x001d¬g`^W\x0016á«ð,\x0017Ú­
:ÃÓ&K\x0005\x001bÅæw¢Âª$\x0003å×\x0013\x000eÎøÜ^ÑñE,þ%e,¿fdØ±Ó\´ÓPöâèÃýJ)°yèx²\x0006{Û\x001bùrÚMå	gÕ£×gs*<jx
¦K\x0007«QTû\x0015\x0001TâzP\x001eWèXËZ
«é\x001bWñÇ6³>WÒ\x0004ÖAÔqâÓÈj]É\x001a[â¶³:>(:zÈGJÕI\x0018Ì4lâ\x0002hdu¾d\x0019´\x001d¬2{:\x0015ç\x001a5o¤GqÄÉÂ6T/JÔ¨:Ü\x001aîU¨\x000c\x0003JVy<	¦îÕ6VÎ«­ÅyßÞ
WlÎâÒ¼È\x0005jXm&û¹¶¡
Y¡êL-¨ÆUÙ\t\x0013îZT2S¯óFXÉ*XÐgiæ¹¢\x000e`]Þ[Ð|\x0004a'<ó°õ"ÀcJ2×d¯°ÌÚè)¯|\x001b«ª6\x0017W]»\x000b\x00066××ÛS¹*\x000e¬\x0011Ï²
«a»NØ¡E¥
£8ÀâSÏ	§r\x001b«¶\x0015«¶}¬è\x0001WÜ±\¾è@·-³º©6ªm°¶^±¶kÅ\x0002l~»«\x0015Æ8ÁJ¼fýÆE\x0013¬`ÕÕ%X×Ýe·AÌ0¤ïHPÒ©\x000e m°õY úÎ\x0002\x0010ËÉWB\x0013ÙZôàÙxM#«ªn\x0004øÚÅê \x00148²\x001aêþÖY,úÐòY`M
kú`)V«\x0004ÖäÇ,\x0018óÕö\x001c0õ5}K\x0016DBò
W~Ø2t\x0013ìY\x0006ÖV\x0007\x0017|íbÕhÂ\x0008O-\x001c\x0015þ,È÷­Duõ\x001ap}k@:¬R\x0012^cH(\x0003É°nA\x0005s%¬¯a}\x001f¬\x0012xlI¦0Xï8ú_¬ÐajC\x0005llAÔ\x0001k\x0005º,Ã;«;\x0012{ê£ÖªkTýU¢×E\x001dç-4û\x001e\x000fÞ_?üx·öÝ\x0015,ílÁ@EnÖÛÀÀ%Á÷Gçß® \x001e\ë@ÌY?2ÃF\xÐ\x0012ÈÏZ4ºä4v\x0007³¨E?³ÅÎ\Ù ·ä=\x0013õ·=Ì®bvýÌ\x000cSÃ.§L8+PÖÈ	ïg\x0007³ªÆYõ³&é\xîfdØ,ù½;ñxèAæ\x00152ïGöàòJî\x0004KBº¸Å³-fÎv6àQF<H«{!²ÁË°IÑ\x0013û\x000eèScÃ±a\x0018zîÂó!\x0010qÆÌ\x0014³Ø8t=´0\x0015´0ýÐ ÃvÄ\x0007&8Òvâ\x001dÔ\x0001=ì\x0011ZÉ-#>'pëáÆkã÷®¢¡À\x000f¬Óë§/ë2\x0016SÓé\x0014÷ôÄjÈ©\x000bñ\x001e]¾ÎQ"HYBÊvH«²àctôt\x0017xHh=QòÑ\x0004©KHÝ\x000eièPDQ4B\x0018É¹ä¶´í§\x001b¨r\x0013\x001eGZúf"­n\x0019ÒþE~øáËO1æºÏÿç	\x0012ï¯\x001f å\x0017é\x0002\Xp\x0011Ñ"âýÝcLE\x000b\x0018ÂH2üÆæh¨vZ¦m£- \x000flg§\x0017/ÿÏ%¤Ü\x001f\x001fÄ¾¨u
%\x00196ìl#Ó\x0016Ä¹\x0000LÉ\\x0011à4O9\x0001Ö	\x0006.HøÕ8d:ö¢\x0001²pÝÇ.\x00182ÁÜ>bNÿåÇ\x0008\x0007ÿläÑK\x001cGÎd-À§\x001d\ù\x0018h\x0002|üí3ÿùÓ_Ò\x0002ì\x0011Ío¯áð8Ë\x0007MôÀ)\x0007I³ØZa4K5òNó]@rùÉÑékøù
ÌTÒÉ|LÒ\x000c2©óFLd ´\x0007\x0001»gÃL5Í]"=ü`4ÃÃDdÌìZ\x000b£©ý³Q¦â.J\x0019cV\x0012|*Qæ\x000e\x0003\x0012º?\x0013&xyïÚ.Mº2"ËðÁ´2q
_*läÌâ¥}³nb¤\x001d8Aù#\x000f'Ï[HTe\x001b1s{¾áÔÑý\x001f1³\x0004$\x000cg¾]\x0002çÌ!ÞÊ	å]ÝËSÆ\x0007À\x0019N'7g8íúÙ¶:vèõ¤G\x0004ç:á°×\x001dbªé§\x0015\x0013JÐlïh
:9½Î\x0017P±ÙAøëÙ8¡ÎÕ÷sc'r:|
Ài\x001dr>ßê\x0004/`½\x0017¦}aEâ\x0014ÅÌi|ÆäöÙ¦\x001d2ÖDïÙ)tt\x0001¦1IÎ%®NÏvtB¶­è=:9\x0005
©UV-·\x0010OËU\x000bÏ¹kT\x001f§%ì\x000fuÊÃp"'÷òù8Ã\x0002_}vÂSBºZ²²¹\x00198ù³ÝE`¸Þ3>l¿\x0004éS[\\x0018LNi6\x000eæ­üéß\x0014¦qz$ÆÏÏ±¬m\x001a3_\x0014^3\x0004tµ5¹Ow°¤ÛÙáée\x0018?ßMÖ±UPe÷ÂÕPÖf§¢ª
JiÙ\x0005õô+ÿáÚÿ8xs5;
Rá\\x001a*\x0010ýó Ã_J~\x0008TU\x0006ôîãæÍd-ª/h\x0008séü¯?x	_KÔáííÍw÷·³\x0006|\x0011ññÁP³Ùîq©\x0003»*a\x000f(\x000b/ÔáÉÉñw§g'Ë¨¦F5]¨Á¦\x0000E{ok\x001c)Duz;ª\x0014\x0015ª\x0014\x001d¨ÚèC"µ)|¬¡×É \o\x00035¬ðí¥\x001f¼ÌÙ\x000e\x0017O\x000f_nîóÌ vº\x0000!\x000f[Z£3\x0006¢o\x0017çïÏ*áæ]"Y\x0012É&"\x001b½H§v\x000c(7-×`E.$U"©&¤°5ò\x0018yÜ´áT±\x0006¸]Dº$ÒmD\x001c´i#ã)Ô\x000fý	´ÇAÚõG¬D2%iB
ó{=\x0004$_\x001eb]H¾DòMHÌ½0ù:°tÍ\x001bi,\x0012ëZJUûµ1%?z9º¢,G¦ÝÆJ&Q1\x0016&¦\x001d>*Â1ã\x0014\x000cÇw-&^í8Þ´åÂÿ\x0018ïL8XFÊ\x0015²p0yÕÅT-pÞ´Â¡|)¿i´q©è\x0014$Z\x0017~×äYÉä*&×ÄÄt\x000cf¦$*d5³\x0003Sßii¢3·:\x000cà\x0007
\x000b§,å¸¨\x0014úQf¸Ð9smdÌì\va÷bjßSÔømÈÄÍh\x001c\x001a\R\x0019Æ¡ãc \x001048<?\x0012±(¸DÉ%Z¸´ ;8N7É\x0012\x00060R[°T¥\x001a±²K¤<=½\x0018¶à	\\x000f¦K0Ý:\x0019Lû\x0014åD\x001f¤
`¶\x0004³M`æW\x0019L_;ë\x000e\x0000Ø>Óe=+Á\\x0013B×+\x0004öx¶ò\x0018¾w¥Ý\x0004VÜ°%Yã¡!#Y×\x000edäd7ûNõdÕ¦äM»2½,R"Ü@\x0006Ép2«Âv²j_ò¶ièºÚlüùá»\x001bXI¦LÊ~P§r\x001d¼½O±ûâÌ{7<½³gZBÖK<ÏËBwàTÛ5»o ÉÓdÛÅRë\x0012QÍ6*O\x0003%D÷D¢t\x001aÝ+M½ÍVSrVQÂ×vLÈÎ\x0002J\x00116±Ë\x0012!åîTw@ÖCÉ{Ær°B\x0004wùA\x000eÉ\x0002y¯0/ÔfLWcº±\x0014hp\x0012Na]âË2\x001cn+¥à\x0015%|m\x001fÌo\x0011)ÃN÷y,u>\x00114v3¥©)M;¥7^2ÃvN%ß\x0001Så¸ó~÷JiÇ¼:$o?ñ±#`2ÐkÏ£Éóý\x0002¦Íæ	ÝsKLÙ1ölSèLÆòa{}iNl>d½ÏeÇ>WÇú8À,ö¹Èþý°\x0014äfJ_Sú\x000eJ°)â;ïXÎ0Ø\x0003\x0001|»o¢vLUßªãTZç9\x0007«\x000c\x000cGÀ´>ÇÂM¤7\x001fGªsÕ3ç®f\x0012¦P9â\x00085p)¶Súz0}Ï`¢é\x001dþO½\x0010;c\x0019l)çõ\x001aJíA'´\x0018Kí_ÆïEOß\x000f×WObáçù¨\x0019+}ØÚ>îÂL§$\x0008#Ø
P\x000c\x001d|_\x001f\x001d^¾Ö)\x001c8í\x000e§mæÔ h\x0014ã¢SaNCµ·À)Í®YÞÂÉ!¢Ô0ëQ¨õ×?]=Ý^ßÍû\x0018Â9\x0014³\x0014£uÄ\x000e³\x001e\x0019\x001eËU÷Oûëï\x000f/ON§c>\x0019\x0013ÊP
ÌXÒ	ZéId±'S8¦´Ø)ÀcÃ\x0003I\x0003p§áÕëû_\x000fN®>ütõË§Ù­äÂa$sÆÓèæ\Q¸j÷.*[G½>?;þ·ðÀýæí"´­¡m?t°@9B+ôAD wßD½Ðe\x0008+@Ç\x0010V\x001f´w%¦\x001aÙÔ\x001eÒW%&s8½ëÈè.m\x0000-K\x0019È6h\x0010252ç\x001d9\x000cü2Ã0µÃø]?7´«FZºî6ÁDÍy\x001eáBC\x0007Ht©ä\x001c9-	Zj¤ák'töÅ§Ô)÷Â¦÷·dv>z-äîZ9\x000ct¸-¬,\x0006úñàýM.h9\x0015ËÎ\x0012\x000bÏôä·.£BùñÄð^\x001c¼?©_\x0018\x0008mMh	Ãu^U1·Ý%@:j\x0006B³\x001bÝn&ô5¡o'´±ô
\x0008ÁÃÃ3"ÏiípclCt¼Bt¼\x001dQç×},¥¤8íq\x0014ýn<»\x0011³z\x0014ã÷6F¡|¬l\x000bñ&£\x001c¤?y¦®EÔÅQ
ºÔ]F\x000cömìÜ
Æ*\x0017YÀECëö4Óa^äfF»Ãh\x001b\x0019Ã\x0003>V`¨dÅJiq÷uÒÎèw\x0018}3£]r#£ÄÀ¼Äw\x001e\x001f¥4"JÆªÕ\x0018¿7!\x000639æ·\x0003b8\x0011 \x001a
\x0001\x001e'|~1[1ò¼70îfXV\x0004ÄÞ_ÝÞ^Í]ìÁQ>æ<§bÑ*\x0015ûÂß\\x001e¼?<99.¸ .QrF.¨IÉe"·³´LJ.Sû=ÜkÑT¦Ð¸\x0004/RBc\x0018¬³\x0006A¤{â÷
h®Ds-h<¬5\x0013j^°\x001cK\x0014à\x0014~Äb%Zy{°2Ì³£·\x001dØx\x000e¾
#mOvH\x0003[½	v\x0001·\x000eÃv
¶kF\x001bÒóä¶a\x0015lB3.ß\x0014aØl6\x0001!¢;9\x0011¸[ËVm\x0004Þ´\x0013 Õ4n\x0004Gå1\x001cS§åDØz-©ÈL\x0013\x0016±\x000c4¢Ee
1\x000c*Ê¥MT\x001bA´m\x0004É©
&,¶¼\x0011\x0011\x001eWÚlÓÀVºMÇ.ndC¢jÒø·\x0006+_$·\x0016¨¦T4M)hs2Kïû\x000c
«\x000cmÓj\x0013Õ©+]f9:¡Ã\x000eÑ\x0016¼e¶/ñ­ÍWl¾/$²Yû"g\x0007å*^ÑÑ³·	MV\x001bA6m\x0004fR\x0017ø8l.»¿mVQ\x001b=%ÚÐª\x000bA6]\x0008sôõXn\x0011Ð,mMhÕ\x0016M[\x0014Úg«\ìçE®}\x0006\x0005\x0012ºGÝ6¶ê²M\x00153bp\x001crxË&6:>Ü¦}P>»\x0002n\x001b66ºd\x001aiþpÇoÛ\x0008ÕÑ&Û6\x0008\x0004\x000cu¦9qVC|._¤\x0013éLkÙlÅfØ OÑM:ZMeÏþ}\x0007Zu´É¶£y(¥HÃFG\x001bG7¤ÔbÓ\x001d¯ª£Mµ\x001cmá5eò»ÔkÍÑjSJáù±ía¥ª£Mµ\x001dmL\x0003O\x001aµÜ\x0012\x0010òE1»@FoÆ\x0006¶êüPmç\x0007ãX=\x0006\x0019W\x0016sY1c4ìSZå´¦iÅ¤Ö3\x0004S"ÂØÒ\x0006ïzÛk"R6>ý\x0000ßÌï¯>ütýpýø¸p«,¦·E]ÜÆ)Ê\x001c½?|ýýÑùÑÅÅ\xÉêðL6QI5x61çÝQ&éÈO³M¹¿0°[_\x000e?x\x0019¿\x0017^·\x000fW\x001f¯¯bÖø13	ÑsåY®:1Ö{*u¸ö\x000f¿=?üæèp²5ëÀY\x0006ãSëvN%?)p&Õòv\x0016 pîÖÿ6q2¿sÓã´
\x0015½º~øýÿþe~¾¡ø7«Bà\x0005\x000b\x0017³¯Ý+1å;xutþç£7s3\x0008uE¨Û	ÎNboD3ÊÒfQã\x0014ÊfD[!Ú\x001eÄü¬\x0008/0 M\x0010ÍTÈj-b\x0011S	Uðu\x001d"H¡$cÔHÅè\x000emQ5¾\x001b	y=Ï¼c¢A\x00135\x0012Ú`Êä+Å\x00030"êJ¯\x000bÑÖ¶c-&=\`\x000c»\x001b\x0013=ÏL8Í7\x000e£¨7´èÙÑ\x0006w´õ±ô,û³m\x000f#¹±jÑ³§S\x0013\x001a	Y_tP\x001cÞÍM\x0006¦×1r¹3×²}²\x0015g±óô\x000cR\x0016²Ð\x0011S6Ý3á2\x0015)]	)¯vuüÞ\x0008ÉÃ¦1¹\x00148¬HW¤ÌÜ±Gt=¤.5NÓ\x000fjS\x0008ß\x0007ÃâàõOüÏÃÍ,«þ-YIZá!C\x00041vKùÜÃó³ðõ\x0000,ã\x0015Ð¢\x0016\x001b 9zê¥Uî	
Í\x0019z2\x001f¨YU\x0003­ú\x0007ZY\x0007ê-¤<\x0013~å ä2Þ\x0008Íó
\x0006ºN¨m£æ\x001a¤qRÎá\x001acµÇ$
7YÕÞL­ë5­75ÏÞ'\x001f¶\x0006\x0014³³±ÌvÝ(ýÄ¦&6[-ÅPÎ\x0001@íÉÓøL«\x0013\x0004³ëÆ\x000eVtöx{\x0016-ëÜÊuÒ<`í&\x000bl \x0016;ÔÝÇG 9A6SÍ\x001bè¤ØÏtäq·3ÖnÓX³tR{\x0006v\x0010:\x000bL;ðÙ\x0006Ûï,lß¿²¥s±Ä*ÞØïN\x0010.xÆÖj÷eÝ-ÊH
*Ú¬ûà\x000bÇ²N¶9`ûlh×Xz\x0001ödAA+µ`5µØ0Ø¥ý@-Eê\x000b\x0010¨µCj½ë\x000bíÅ¢\x001eìø½\x0017\x001bÚ%Ç0ç\x0006,e²<T* \x000fÅLê|´cÛ\x001dl»\x0001;É\x0002µOâ$\x0001:å\x0000ô¤J+´¬\x001bQ>Uá{nÃétï´Ë¾&\x0018\x000b»iýØj\x0007»ß|\x0006úIÉ\x001d¶&s\x0019Ûg)\x0018i§Kä±õ\x000eöm\x0013³â9O-¬\x0010¯y×ÝÃÌw³8e1½º½úr3¯®¤¡¬+[x:¼¤}\x000eQ8a'³O½âÕÉáûãYe%¾ÄÄ)i\x001d¡¢~©ðU\x001f\x000e2*l6{¢:«±d%[°\x0014eV÷²ÏÁ&ëÉÿ¿	KXª\x0001K3ò«s?G\x000e
G7lú
Tº¤Ò
T ¡ÇÊ@çÍH¥QªE¯µÊT¶J*T#\x0012\x0012Z|G*EÎt½Oh5+©\\x000bð`Aó«Acµ/coJÃA\x0015âõ\x001f\x000eÞ¦\x000eÅsg&6È±\x0007\x000bÞÊ!,¢÷êÔ}syð¶êI<&J4Ñæ°R,\x000e\x0006^\x0016ÒÞÚ1o$%l"ó
ÓÎ `	]i
ÏTÅÔ^\x001d½ÕhªDSmhÃ \x0005´¬|e\x0007Y\x0019¶kØ6¢é\x0012M· \x0005\x000bò\x0005JñP\x001e%ñméw5Ì\x001bÉLIfÚÈÌ\x001côÕ\x000e\x0005#\x0006'HØ\x0003~\x0013-ÉlëJ3¨LÂiÐ\x0014Æ¤ÝuÐ·¢U1ß\x0007?h!\x000c\x000f©¼\x0017\x0014©mXª\x0001rTï´Pø³Møâl\x000bÚÿþÇ\x001dýx{³\x0014]MwS\x00024Xa´ÇsÄîfêgÀ`¤\x001d\x001c}wr<\x001baÍ¢\x0014=\x000cE\x0015Gí%£9ÅÍùþ³®Q²\x0011\x001cò(KÏá\x0011!%*K=qêµ@ª\x0012RµCw1eä+×d=Ùæå¸«bÕ\x0001©KHÝ\x0007©=í\iàÖÈÓ½S·0Ñô0
Ù\x0008f
\x0016_\x0016\x0003ù\x001cÛÆ¶\x0003Ò\x000fÌÊÁFH>äì¦ûu@º\x0012Òõì\x001b÷Bå}\x0013\x001eçYâÝÈA]Êoß7¾ô\x001d\îbxl¸<ÞcnÂÚj,Zp³cSRÛP¼f4e»ÝF--:¶v/Ã\x0014î¥.£\x0005ÎÒ<4\x001aÅª\x0004¢]\íÝ\x000fê\x0000ð³ø³%N_qú.NW·Ð\x001aóP$æºñÉ¸úzÊRá)PF§VLÁ$&
\x0019e/¾ÌïÞ;= ¼\x001aNÎ{Æ3¼¥¬Ì ÷\x0004Ö>1?ÒSí\x0000\x00155¨è\x0002å\x0008ô\x000eAñÌÜ®®\x0017h=õ¢cêa2\x0004åx[a3f'ó\x001a@M
jz@\x001dÃ\x0004\x0010n%=£¹!UªÉäõ BUS/TÏÔKîÀ¨@²£Ê.Õnòm;¨d\x0015¨d\x001d Ì£°\x001b\x0014ä\x0016TQÅA1U©º0µÈö¦óÖáë"\¡*ËÿÝ·cßÄWÏ´<ù17·uþ¡ñZ:£@\x001aÅº']²M\x001bJú³4ìÔº×æÁÉõãgHåÃT1\x000f(?	>ä%¬\ã¸çÓ®£wÊ¹©kLÝ)DÎÜ
,\x0017ù\x0019s\x0011\¸\x0010¦\x0013UÖRÊz0eû`J§s\x000e\x0013P¥\x0010_Ãs;ã±L©R³àÂ/¤^ÝÊÛëß\x001eæ!A\x000cI3Xó9¹§¦g£¬Ø*òöèßÏ)\x0003TíÉöYAiñTeºéô\x0014JG/·\x000eH]AÒdÖ@
²YÜîrÐ?È¯ôÕ|ûùæ\x000eS¡t×£¶\x000f\x000eä®xr;c¹¿ÚÝß« M°?röò\x000e-pNÁÝ"Þ\x000eJUS+(
Jzù6ø
\x000eF\x001cUHmÛ:PàPÉê\x001dyÑGh?³¨<\x0012u©\x0007A?ËgÁí®Jµ\x000f]tû\x0008ï¸\x0005µ\x0007\x001em¹"g»¤U`¾þéæáþé÷\x0005Ý\x000cÉr®|èÆ8½Û¦©\x0000}ýýq¸2ÿ¼\x0002Õ×¨¾\x0007Uøül\x000f¨Le%\x0008cLÎ¾	\x000bu2Ur\x001dªÄ®>Ã\x000fª\x0000ÓÉÕû\x0005\x0004Ó¢ß\x0010Ë[°ëÔ»F<yO\x000eß\x001d/ã\x0012Otà½Dµè|¤S\x0005ðhüÙdÉ&[Ùôë\x0018><\x000e\x001dú;6*éT#tØðAyOÞ\x0018K>£-xnwÝ¹B»åíU0zn\x0016,skrÏ\\x0010±Å«§ú\x0010¨·ßWöö0\x0018<Ç³{Âí.:Wè·¬b\x000fØVHfÙÝðº1\x0014@dû\x000bGá8\x000f\x001f®0\x001aÃQàj£ñÕÃÕããõÁé\x001fÿýãÂÍ\x0012þä(ðÂ)µ·\x000c6,\x001c/BêÝäáfyu~xq\x0001­®¿½]\x0012¯ªyÕ\x0006ÞXÇ\x000c¼\x0016Q,i\x0003înÛf\%wÖe°Xu¹\x0018-³fðü£ªº*GèUß_¾\x0014Í;K2`\x0006,p\x0008aÔÄ½pè
d\x0014ÄÛ×ug5,±d\x000b¢ãO9,´CÄÉN~¯Â*ÍC\x0019ûÌ®EO\x001d\x0006Â2S8Ía÷e	­\x001e.^Çda\x0015e¸+è\x0014¥t5]ùá)¥¶­1±{×
kìëëõ~|#Ëg³Ô¸Þ\x0019¿öUY\x001f\x001f\x001f¯\x000b8ìÞ½BáÂkfU¶¬\x001c\x001awlÙ[ÒÜÎªJVÕËª²\x0018uÌªËeÁ^M\x0014ëÕ%¬îÕQ\x000eS¢$õõAÖ½5
¬r·f\êâP|sÿt{s7\x001fyHcÂMbè!­h'íë²\x0015vÒ³ËãÓe4Y¢É&4á&?\x0006
¬£ì(7¡Êµ\x0016MhºmÔ4IÀiî\x0007ë5µù\x0019¹DÛÐ|æÐ ÌÑÍ)eàa¤\x0014¤ýÝtÖêäË­8¹W\x0001\x0006kÓ´\2ÌÝ0­ûoeB»kP[2\Âsóìá¯×_dÏµðéIÉÉHÝÞTbxi{ô~^ó<ó©Oµò\x0019]úPi\x00042änt¸Ïð\x001d·W¸âGn¯ëÛ/ó\x0003¥XÄ¥Â®\x0006Îð¤fcw³éù\x0017G'ïgÅ(øã+P\x001d_+0¡GNa£d{#M.qÖÓ\x0006Ì|VD2Ã\x0012*k\x001e\x0002âÃ­¯ÃcF\x0012HRPeënÈ
\x0011/\x0003ßù¬ølÅg\x001bù¤èÎf=c%ªd	\x0010¥ØÄW¸ä\x0002_é[Å\x0017ÞJ\x0012ùX\x0016*7ãå&ÔT\x001bªõ|uÄÈ\x0008?iÂ´±V=Õ\x0002G%É©\x0016xªÈb\x0019SÆVY\x0003\x0016Þµu\x0014èêéÃOKÞv½i\x00141ÉH\x0010\x000c[L]
¨r§\/Ke\x000e\x001cuÉZC(\x0014\x0003JþÌ0ÑØ\x0010P¨Ý×]\x0003"\x0017;Þáð8Ûõ\x000e¿º
¦áv\x000b$åbS\x001eL¿¬Ð£½Cí\x0016±ÛS£pe¾:»\x000cvá¼xK$ÕEécø7è\x0006Û«H\x0015\x0003ÇWr\x0010$YÞÚRZT1»r\x000f]¨õ êAUÔ»\x0016{0Þ\x001fÎqKï¸ìO³\x000eUÅ{±lñÄ_Êê(ZêÿîG\x000fÏ!tIyá£Çô°Áç¿'´2Æ«pÚ2\x001b2¹¢\x0003"£\x0019®k7\x0015²XÇfªa3MÃ\x0006·\x001ak$\x0006L¥"]M³ûØÆæªqsmãf85·ÂÌ&¨ÜÝ°ÄJ6Q±&6(sä{ÈÂ¼{bÛ²Üª¼>¬W°IiàÜ'3^%\x0002%S'à:4^Íh±\x000eÍ\x0019ª#L½Íÿ©\x001aÞy¸\x001f¬k^\x0000hF BcN´¸Ú\x000cH\x001a¡°+\x001a3Ñýc\x0017IHò\x0004k~çýÆ( òêjIa9yÒQ×a6\x0015:ÜÄ¾`È«Ãyu¹8J®\x0010&`áUÖÉÂwÞ]\x0019lO\x001bæXÈ JZc Êz7]Eû§ðè÷¨îg(O. \x0014]¸y¼3ã©¸&mví¨\x0011À~F­\x001f_Í=ËÍn<ÁÄxÂñ/bÌ#A¾\x000bWýÂÃÿ>\x001c½$\x0016LgÚ(]êøÍÛ\x0018ïHïÂE¿\x000c)KHÙ\x000e\x0019È,§z¾¼\x0008ÁOÞ\x0017µ\x0001ïzû¸®§úõýÝ_\x001f®\x0017*ºS[o¤ÔY\x0003¼Tv¸7n
~{¾TÎ-wü\x001c°*Ì«Û.Í¹\x001a\x0002¯T¥l Im·O®71\x001eÌçséÝºM-
¯éùõ§û4\x000fa©¶ÆPoEÛeBKøüèíÙÔ=áþrÿáËk\x000b*càsMeß¨ï®\x001eâ¨±Ôé\x0010,Løãç\x0016Î'\x001e½k	ËY¶4yXvñ\x000e³\ÐÂ<^¼«F}wx>9t\x0005¡\x0002û7}¶\x0012
4Ð´ç\x0007"Û	OTîÉ~<°\x000bÓg3^¸<2¡\x0008]*D\x000f\x0003(Ùs\x0010F!ÛôÙL\x0018ltÂÓ	\x000f8\x0019¯ÌkïÅ\x000b/Õ°öÒg\x001b\x001e\x0007yÀ\x000b\x000bMfY3Õæ-7Æm\x0018¼\x001f?þ ý->xÂÄÂ¯áx~<øã?¼½ºû|sýð8?J»OÆ1tFg½\x0008\x0013Þh2aU\x0008(sú\x0002¢2§ïÎ­üáþ_îÆ¤Ð©Ùôj1
IÄù¤Á\x00171Ísa\x0003\x0007~ub*Ó$ä¬ÃEiÕèÐé%c\x001f~õ¦JY µ,W¡E:[ÂªgzH3_¤2éÅ1µ4¦Fáì[9ÚJ¤\x001cøÑ
åÇ6¡*r³ºÜÈ! j÷\\x000b\x0015ÒR_ÆÞQQ¦	P%Ï\x001eaTEÔgÛú±\x001a(~ô.UF£*\x000bÈ\x0014c\x0004Ô2x¼
\x0015§âGï¨z\x001aUT´´¥mGqxPÆÞÓ4Z\x001c\x00113§BO6¼8ísQ\x0010_x\x0019?z9
ÝO ª\x0017©'\x001bNÚg\x001bRp·Äþ«Ô)ù\x001cÌ-¯R¥Ö.ÒL8IjÔö4lÞM@ù°ïå3qBsüèät2¶I©ÀÃÔ\x000b¯ýÚÉ_$\x0011õý#
Íæò\x0005Ås\x000eñ9B\x0010@ñÏ\x0003\x001aÕªãG\x001f¨ÄÍäéÆ÷ZgLÅøsm¦X­\x0018?:9ù°ï\x001d]ùÞÒ"õ~í"]F\x0015Ú}B§Z¼£UJþó
)L½Ú0õ\x0002_sÐÎ4_¢^§\\x0004ýñs¸\x001bÕ\x0000j·Á'Õ0¤Þ£@J0#h¡Á¨\x000eP»w¾4\x0012mÓ(é«q$Ï¦â~ô\x0008íEhVüx\x0006TW âB×ô3¡BùøÑ»ýeÌÜ¨"\x00077#*¦»TÀTô?KÃ»ÊsÔ\x001b
»Ê
$UÏõ6\x0011`Å
¨é:
wh\x00074Ïv\x0000@lüè¯h/\x000c¹%r\x001a. >Û+ZBíEüè\x001dUKKU³\x00176\x001fÿFà¨êµ\x000f¾*!\x0017?zï)ªW®Tð$Påëi\x001a\x001do²ÿ\x0015
¨<ÝþÐcJàÊpû\x001b¿öüß?¨_®¼¹3q¡ÂZÕ
\x001e¼\x0006ÏÞÝÕ\x0005ç\x001exG¢¸Õù8e&\x001bSá,\x001dÛ|C(ë5x÷N\x000f_O:øP\x0001ê"\x0004ß<\x0012r-\x0013¦tª'³BûñÝÔÈ¡çeúlg\x000eÒQº1uY\x0005\x0005±ß(,xÁãg+"d "øóD\x000bãó0B\x001f
\x001f®®ý/¿äTgHp.òå>_-¹Àa,\x001fÁ©l¥Øx;î\x0015Íôä:¼<¸x7\x001d\x001e*Ñ ÷%üê`\x0013MúMe´ªßP/\x001aäU\x000e4/C	*ÀYMf½Q\x000báÑ
ÓÎ\x0006v®MÒ:÷\x0004Êà\x00044«úÍ}ùû)\x0007¡Ç¡ç·\x000fW7)d:ÇgÃq|\x0004íÂCBà¼Ú\x0019'\x0005Ê\x000f«Ài}<\x0017a\x0012t/¥\x0012þx8ÒÑÚäaTVÍ<ÊKÊýwÈ\x0000	ÉÑ¼2\x000c Éö£Å«\x000ezâ­lg\x000cÝ\x0016HH¸\x0016¬\x0013Ò¸\x001c* ·\x0013®ÐÈÕb¼Y:'\x001cÄ¢w,\x0015ËÓmi ÏrsO¿«ì^>*GEkJ¶´Æ'f3M\x0013døs¤ín\x0015Õù£¥è\x001e¼¸q^9Û`zû~HÉ÷@òç¦\x0004ïuíÁn;*}\x000e\x0002\x000fîpTâ\x0015Èøs\x001d Ü­{1eÊ.\x00163_w¸ÁÙ\Øªe0AFT»NJ\x0000ä;\x001bÞÚ)aR9A¦Î\0 \x0012m.J¡¢ÎbÜâÆÒ¡×Zé¹he\x0013eøÛ
3\x0003@^\x0017¹u¯×\x0016wÏ8µ£\x00132ü9¦sÂaÙ¹"A)'U
¼Á`+ïïÅ­\x0003=\x0002lït'OzºwH\x001d^[ºÀÝ³ípØÎô\x000fe¶Ù8d8æPÞ_£äÊ½³	osß{õ8T6¤óÒÑÞñ+/ñ	Êoþqý×*$=ô\x001c>¿ùðSx\x0012.x'\x0005Á Wä}\x001eó;Øph:|~üúûð\x001eÎ{\x001bøÀî\x001fÍ|Æ£\x001fd·ÒT\x001eý<\x0001z4Ó=\x0002^½ñ£\x0010øi\x0004
-FåT>Ç\x001cÅvú\x0000%\x0000Ê\x001eÀ`ð"`xT§e¨Sy·ð=Æd\x001f"ÆtÚ\x0011%Ów´´\x00111;%8×îyf\x0019 è[r\x000c\x000cT:¤­\x0002å¦yÙøÕÐ(Av1~4#j\x0017Gwzi\x0007;çÈi¯\x0018ÈÐ3eÛëÕB[Ú\x0018¯²×^Ic1MÔðgÙ-Q¹4~´#:M³ù\x0014Ã\x0000Øc:vñA]XühæÜ
³ì\x0008QI»y:Ó¶\x0005ÑÂLÄö!\x001cÒ×4ËÊ\x0008eñ,{ÅB­Õ=Ðk&oçðß|Â£+OÀz|\x0006¾8\x0013ñ£Oe88vÒ\x0007'ó9»e\x0015ÞsñøT\x00197'÷oqóËõÝçÛë·O7\x001fÁÒyss·hiÞ`qç\x001bÔÒå"8´Ûa=9{w\x001c7G§ï\x000eN\x000eÞ^\x001e¿»\x0000çÍñéL
3R\x000f©[°\x0015#7¸ð9~\x0004ZÒ*c«±×o#vtÚÛ£m\x001dú cÔ½%ÍÄÍÄÈº\x0015\x001bÓ³¶`Sb6¨q!¶q9¥(`ë\x0005²
[@
uüØ4ÚF\x001b[_øQ\x001anqöFf8)âÇ&f¯LëC\x0003s^\x001eÌ\x001fÂ\x001báô\x001f[==ç\x000cô|Ïþ\å¸\x0019ÛóÛ
\x000fäø±	ÛàòÐ\x001eË
@\x0010\x000fW0Ï¼\x0019\x0005ìC±q3z¦\x0007lKg¸HÄ3\x001fØ\x0002&ãÇ\x0016j®ÚI¼g¬RHÍÇq¤mØC.ÅÖÁN'\x001fäÑ`£Ï{÷ÜØp3Ê×£\x0017]#A=,{.¬ÖùAæÇ)k\x001b©!»2~l¡Ö´9)ÐZ/uîíØîÜ­àå\x001c?¶`\x000f&\x0014´«b(:&
bÓC·b\x000bÀ\x0016Û°áRWãhc^KÀ\x001e¹47bCx%~lÁVèð
;\x0012\x000b)A}Îâ\x0014Ï
ËZm]Û\x000fØ\x001a
Ö,D\x001dÏg÷}üØ4ÖXê\x0002­ké\x0018±¹6C¦Í3cC\x0008!~lÚùè\x0003ßcîå\x000fà¢ync$J\x0018ÅMgF»O£%\x0002J%x¥?÷	\x0002\x000e¹ø±i\x0005\x001e|f8õ\füy\x000eë\x0007ñã\x0007õs%r\x0012Ó÷¾\?~¸
Dsïpç£v/ J°RStî±Z/¼ÄÇ´÷þèâõÙ¤úPE\x0005\x0019û_\x001f\x0015äH}%T×\x000f_¤¹.f0»S\x000e^ÿtýåê6.¾¥XÃÔ\x0014)\x0015´Ì¡\x0018\x000eÇÆqÌìR¹>÷ï\x000fOâ²[Ãæ³Ñú(Ç\x0006Òdm®\x0000õÖÓ¯;!Á)£l\x0017eÎl4¯\x000c§¡äSÎ³VH\x000c\x0011ö@j2\x0005¥1(ãÇqlr÷\x0001rREû\x0008¡ô;]è ³T­\x00089Î`îÅòJÖ·&£w´®pÆpSï)	èÅ\x0004å\x0004&û0mbT©\x000e¸r/qç&¥\x001d\x0019!ÐZtlbôdy*Ð\x000bÌE¾¤¹\x001fçvBB«¾\x0007+îng\x0006§\x0006N·´#ë¸\x0012þ øÑC)\x0005¾O¥§·5'ìöäKubB\x001dYüèÁÔ\x001e7bÃ[Ã\x001bÂ\x001c¿£û0UÊëR=Q\x0007\x001f \x000c¥QÂë
cÁ&{¦£HfeüèÁdtñ\x001baÒÓLJ¤4bj8ÓußÁ\x001e0é`\x0007
ñ¼6½#ßÉ3m ¨h\x0010?º¦\\x000c/3:Ö½×ø0\x001b§nöRBÒsß\x0019R\x0011¥Áä0
\x0017¦\x001f¿kz1AyuYDQ\x0006ÔùÌ\x0016\x001fè-\x0013Ï´\x000cwâG\x000f¦sä°qöø\x001açãP]'&(½Ç\x001eLVD\x0003(1ÒikS©4VLÈn\x001f=g»\x0017älLéh\x0011\x0013µ\x001c¼\x001f«x4Q>|¾¼»*\x0013ßÜß}¾\x0019h¯®oo¯î\x0016K/¸ÊÃH©\x000cÆ\x001aÚâV¢7g§ïbòÙ«£ÃÓÚ\x0001\x000f{Úñ@RÈäç?&â\x001b\x000b]|óD;\x001a\x0008ÿö`´)^ßÝ?}¹~¸»Z*Øóåq	ÇdvÙkw³öc)ïÎ.ß\x001f\x001e^¼üpõñêñóÃnª^\x0001«aÂ¥§sÖ(+úõ¼¥Ý8ÈÔB\x0003fÃz\x001a0aU2nm\x0016®·\x000fã²û\x0016pL±Ñ"ve¶ªÀ.,ÖYÆêØ;ÐL$U\x00164á4´_\x000fMª§ûJh¢²TË2þÿ\x0003/\x001eùõàD ¯\x0007't}%8XÍ³úÐ\x0001+:×sXz0Fbu£\x0019{CgoJ?ÑD\x0015ôø±\x001eGåÑ\x0011Á°{¡²ÿKK*r\x001bQK8··7OæS±ÍÃ\x0015\x001a¥}ç@¤¬\x000f\x001aMYWÂ£@Ú3MáÖ<;:\x0007
¢5\x00186\x000c\x0002W¹Å£ê¬6T\x0018»'<c,\x0005Ôa¹vqéf¢öÖÊñl\x0019ÍG6ø:
H\x0017_«(¢ûB\x0013\x0005i¦\x0019=öDÍQüðñ7y£
\x001bæäæÇ»ûÛ¥¡±î@JëAn7i£Xô:ßÉ'ÇßLíÝ\x0002#\x0007+þÙ\x00189:ñÏÆHÖÓ?\x001d#Õ\x0015¯Á^k,\x0013ç¾pF\x000b\x0014J´fOjGâ85
d¾­ãâEv3B÷H1èYPÇè¥HfÛ?}R ÷÷+ÀH÷É?\x001b\x0003íÅUk# \x000e|òîÊ\ì\x001e\x001e±Ç\x0013<ãl«\x0003M³Õ ÚæÀÎbåFâÛË³qµÂjl­ãP&6í\x001caß¤M+=yå½ëÞ.<¦%¯\x00051,-J\x0005
Ç¢\x001fgÇ/öµ\x001c`«+\x0015þæ/rPÊa¹4¼=q<ôHsæ½gÁù\x0004~@ø\\x0007\x0012,\x001eæ1Ý\x0016j¸#Ë:"\x0018¬S{fbD~¿z¸r¿Æ\x0018-d;ù\x0014\x001f`®+Ñx\x001e\x0015Átª
Ö*ú-A8Nl:º8x\x001fp¦\x000cÓ_Ùç\x001bñ9Î\x000fÜü;"Ho®\x001e\x0016©7ÀR\x0014Q¢´\x0000=¶RKù£7ç§Ý
K@HËª\x000b\x001dðCÆÄzq>W|ß@\x0008q\x000fÃº\x0008\x0015f?\x0012¤=N­Ú\x0018Ð@È~ýásl×\x0006\x0015IÜ\x000eÑo®¿,áÕf©ÀP«À¨µÁí( Ýß/ô\x001bHÿX\x0006\x0007·Q­h<×ìiÌtÖð*È\|²ðq5èøÑÄ\x0015(|»\x0019ohÈ$ÖÕ\x000be¦}ñkÑH¶´\x0011mè6«Ö
å2Ä\(}-\x0017éé5®2|³\x000e%?Ã*ÃK0\x0018Ûg\x0012ìÛÌÌéZ¾§\x0014e«¹@Öðeühá\x0012\x0004;\x0002\x001aRÂq\x0015¡RÊéé<Úãï~¿î\x001cðv\x0017¯îo\x001e\x001fïï\x0016Õ¡@G$ËVY\lRXòm«É:7(uv|qqv:'\x00115`b­[\x000f¦ðI¸5ºZ¤Å9¡\x001eÏ\x001eMä^R\x0001TüèB\x0005o\x0019ja\x0008:Y8é)=ß(¦	\x0004\x0007ûP\x0005æ\x0006T\x000cBkæ,	\x0008Í¸~ÔÝÒï6TCË^à
¬c£¼\x0000&³w:P±8©\x000fu¨¥÷"ç`j¬¤\x000fÏ·PIÂµÓ»R\x00165çÜÖv³=eZPãÕ Yïì{I¨P_b©Z\x000cbÃ|ºl½\x001d\x0015|[¬wöá
\x00149IÐ£#AÉÄÌvH\x001dÇ¾©OÚ&wëÈÇ)\x001b\x0004ÑídRáZÔß\x001f¾üðc<øÁx¯;û½¾ü|s{»t7E\x00054ëÁ\x0002GY­0éñíYHe]¼;>9YA(@\x0006WpÖ\x0018Û²$sM
ÌÜ2Rç\x0002\x000bæö(Ë7 >Ý}øòÃ\x000f¥ûy'Ùÿ!Nýºr@>û\x000e8<ãhrTrqv|îæû§\x0005°ãsÎÎê
ÐRd»\x0000
	±!³t±°¢\x0011\x001aC¨unÞ!\x0015CdãlÆ\x0019]È?ÞþüË?
kê\x0003øxðööêóÕ²·B1*{ãäJÀ±=éHéAûöäðÝaõ¤Ý\x0011o&6ÜýpQ^\x001es@°eÒ\x0014M\x001aä¶£¾Uíhªf8Ïê\x001fÎäÙ5{ÔJÛÉ@¦ØwDs°]¾ÑU°%ÂKáxôàò\x000e:æ\x0008-4)%\x0008Mí¢f4R¦hD\x0013Þ\x0019GC8À9L«fû¬\x0016"a­t$)À\x0019\x001e*EÒGFÛtÐ%Më\x000e:9¢@'óÌ
Ec·ÇâÝ¥P«'8¸èãG+SÕÄ&Õ(Å\x0005§íº}äÀÃ\x0013?áÌp\x000cÛ\x0015µÌ¾<Ëv8\x0003p¦\x001dÎR,C8(/:¾;£ö¼\x000eé@v$~´Ò£çB÷.\x000cÝ3Ì+ÈWÅV85&\x0002%y \x001f\x0006\x000e\x001e?VVÂ}úñö\x001f»®à\x000eooÿøÄ÷§ë¥\x001aAeÂhé\x0016nØÜ]êbàF&õa°P\x0013Ý.ÿmb«Þ]}QÿøG\x0011\x000c\x001fDÊÏLîz¡1@¡Ag;\x0007Nô¸âw(?¿´\x0008JBþwüX\x0015-rú+zóa\x000b`K°ò&úç±ü/þï¶0ÜgÇOW·W¿,¦¹¸AÓÝ1*\x00122Ð\x00193F½\x0004\x001f[!Å³ãûÃÃ7­Å\x000b@\x000eCÆËq[è\x0019Ê¤Ik,Õ­Á$ö8²\x001b\x0010ù¯ê¯¿Ù)*\x000eh¿__-ÖÉzÁ^è¼?!Ì\x001fê\x001cËÕ\x001bßö\x0010¨\x000bP>:©- â6\x0014\x0013wâ·ûXð\x0005÷TÙû#l?þçñúáËýÍÃ<\x001egYV^;Ü	áöÂ\{¾G\x000f­Ø	G\x0017GçïÏ§\x001a°ðZ\x001f=\x001eKj\x0004W¤»^8R!æ{2µ[(ï\x001e~·Ê|«w\x000fW_®\x001f\x001eUi¿
O"m
¼ì\x001e¡¢ÃwçïÎ/¦Ý\x0003W_~ûò/6A¸\x000b¨\x0002`9}Ñ;êà$©Ù¡Ó8\x0000ï4·\x000cÚ×md6w\x0016r°èé\x0017µ¯û°\x001eüûõ1V;À\x0006=¼ûøpõ´,@ªÝ\x000bÓ,\x0015Çè¾Ãè6û÷çáé7çßL¸LÜ¿"_©Ö9~u³´¶UT£%\x00196	V\x001e\x0014rÑú°õ«ã%F|ÛNèÉÑ %yoáN$Æ\x001e.DísÓ\x0008\x001dA±\x0018\
4A8\x0006;a\x0016¢g	õ§+.cù2<Pá\x0003÷ÃãÁ·\x000f×Ë	\x00089jZí=Þ¦RQ»-6Î-\x0019ì¶oÏæÒ\x000fþv÷ô;ÿ¹N¾y}÷ñêE	\x0011	R£Ù\x0004®d#\x0019Áðñ·ÏÿyvúÍaT\x000c\x00192pòo2ÐÇ_¯\x001e{Ü¹ÜAÏdi¬
\x001b Ù\x001c\x0002#ÔV\x001b	gÇøôãø\x0006]¦\x001949ÖÐ8©Ñãj\x0002eh¥)Tßá{Ô°\x0016i \x0011(Ìð\x0003\x0018£¡ü+,ù×W?\-­)§_¸,Æ5]J\x001a³ÃÅ9ZôCùWXó¯\x000f/^\x001dNoK\x0004\x0015%¨è\x0002õ¤áÆböl\x0002Å÷Wãô\x001eP_ú\x001eÐAG\x0011F4ïÒðx04¢£]Ú\x0001Êu5õºÔò¡xRs|@ë\x000cçÞo\x000eRQÏ}Ïä[jÞ\x0018&
¤XÚ;nÞÁ)«Í${vM\x00138Ña\x001dL<RÐã\x0000u\x0007i0f\x000bR\x0007k'UJ\x001f£ÂY-HîN«¥ÛI¹`Õ*nQí¨Â¡m\x0013&c\x000f&l¹åÜ¸oc\x0007§t\x0015'È\x0010µsJrG)Ar\x0018ÛAyé\x0019HUMªúHý@3OÑ4;.äêàÔ¢>º¶½"}\x0004ÅH\x001f:,R\x00149ÚSsÖjê£Ôt¥Z\x000c"#¬\x000eð\x000ea2ô3¥áX¡Âê\x0018UOYý¸H±Ï£}\x001d¾ºD£ÖF;¥Áì\x0004PfJ
k äXõ¹\x001dS°j+Á×y·\x000e\x0017õ£Ô
(Âå\x0019î&È\x001f-QU×9j\x000c¡J74\x000eÃèõö\x0019.'ájT×jÝð%«4¼®
ºJÆ}ÅÛQ!¿§¼ñÁ²oGõÔT\x000cÈäÓQÏ\x0002jkPÛ\x0007}O\x001c_ßaíz|¢A§-ÒÅ¨ðp<3\x001a¾\x0016M\x0017Ö½ÝhO\x001bQzïû±
M\x0017Ò£i"ja?ZÓZF#QÁÅ\x001aì/\x000c
\x0017\x0005:µõd\x0016âZF[3Úöq¤hqþm\x001aGI÷éüÓµ¾fôíãhQ\x000fmÎ0\p»'DÖÄ(X5×µÏµâÄ5ÕQ{I
µJWuÛ¦UR\x000fM\x001d\x001c-F¸Ì\x0012#kD³ÑÖíQj²q|èõJlìùndÔ¬bÔ¬QP¸6>àó\x0001ÉÅqÜÒÈ(kFÙ>×ì±4<_5\Sß±Ð.ã\x0003:#\x001a^!Ö­Ö\x000e#ª	ÖtÞÓ£Þ\x001f7_o\x001cF[Oµmj»`XÖ\x0006ð\x001cE÷ø\x0012ÚÆÐÖ[Ú¶oiArc\x0004ÝÌ ¢Ô$];®ftí\x001cë\x001b¤\x0019Z\x0013(ï¾,3ÍV1úz-úµ(°Ù(jÍ\x0014io-\x001f;óSíëaô\x001dÃH¦~\x0018FòÛf®õãºaô5cû5Í
ªM\x00199¨i`\x0001ÛÓZªi\x0014¡\x000bGA(Eû¹¨è©¨\x001e\º\x0003-	¯ÏµÜ\x001fEÎb\x0004SÒL\x001fÄVÝC.ÄùÍõÓããõ¥@\x001e*pmVÏ¡ÎñÚQDðýòââèõ@¹§*<Õg\x00195d·´\x0014µ¤ï3N
j \x001c.h Ô¬P¢-ÆlÑ¿¡$\x001c4Fé'´¢$§p;¡×\x0019V¡eÔÑ^ëèÖã!0\x0001x±Qq+f¾qRKÄ~k<ü~\x0003¢\x001a\x001cèq\x0015\x0007½\x00191\x00181\x0006FIM3I\x0018;Öýk@t¶Bt¶\x00071\x0015÷HA-ë\x001c·¸\x0008Í\x001e\x0001éõ|zðH¤m";øÂûÂØÐ;#!
YDÚ'SÖæ\x0010Ãê}â7~°@]ö@¦ìÃU\x001dFS\x000c%©½â+ìÆñÙJp²ÌíØ½Q""/^\x0003\x0001\x0011¾63rJï\x0007\x0001î¼å ^\x000f9ë ¬ ák+¤V¤x+\x0005ùrÅ©Q¿g.â°
Òò
Òò¤Ù\x0006ÿX¶fS«×9ÞÐ­²íì°¨ç¦sfF%¤=Ò\x000emÒU#	_!\x001f<Ø\x0000>(\x001cÉ9çý\x001aHUO·ênË\x0006w¨\x001f¢ß­ô\¼n
d¸¤JHøÚ\x000cIuÄá\x0010§{P+¯ð\x0010ÉyXÅèª%	_\x0019¡Éh¾\x0008y*Ø¢qrãÎÖÎ×¾Ðñ\x0017BÓUíÐ7á8ûx\x0017qê]\x0010	
¯æ\x0019¾¶\x0013RP\x000e\x0000ñ%mÐ$3³áø5Ãh
\x0007\x001e@*Ý\x000eéé)ÍÕ\x0010qX' ÆÝ¹Z\x0019MÍØ~eÛ!§«!Êe©àM,ÈX/CÚ\x001aÒö@º¡\x001cÄ\x000f\x0003I\x0006¸\x001fû¼[!}
Ù¾i\x001cóC¹\x000f\x0006µ»4$*ob´EªU`¯íÔßyNN<\x000c`¬m¬·íØ6NP\x001f
¦©\x0015\x0011\x0018#Öj¬\x0006Ð\x0008©«C<F#Z!I²@ÿOR¢Õò	9O\x0018ýÊ\x0016\x0017\x001dÃ¨
	XC}¤´ÆRãfò\x0016VAjAÆüûfÈ
®äÐ$\x001c\x00017ZÎ¨\x001aOµã\x00195hhP\x001e1C©ÄX\x0013©	3[MtüÞJé\x0015v
\x00151$kqV(*eú7×+/,3åS¿òAâÿã¿\x001e?<ÜÜ]/4u\x0008ý¡¢TÙÐ\x0015\x001e[?N7?::898ºx}~|z4ÝÒ\x0001a<\x0005u¬\x000f\x0017áúÖ	Vb\x000fû=MÕÛicþ~5´ÞwáB#â:±8è_¥\x0012¡	Ä3ðzf+^Ïl\x000f/÷°å1.§xoS	ÝÏáÕ\x0010øü\x000eo×ør\x000f9ÞÔM\x0013ã±\x001c\x000cvL÷\x001eçÂ·óª2a\x0011$\x001ccÆb\x0007¯i¯ùxpAßUÃ\x000fí©)ïÕ¬Õ]{
¤oÓsÃ[N\x0000«pdÃé9FÖzdá{\x0017¬d\x001cC¡áÈM;MyªNö{\x0014@Úp¹®ÿÂH	gOÙoîÕÕã*©\x0012Å\x0005)Â0ÔØ±
5­tÓây¯\x000e/F"%£K,¢\x0016\x0011½ZuüY\x001a^6¿9A}6\x000eOü8H±\x000ftòá8mÅiû8%¼\x0013(GõdË1/ÐÌq®\x0005å¬\x0002å¬½È­y°öSÃXc\x0019Õí¤RT¤Rô²\¨Â\x001d>Jq(`kÌX}¹}«¥\x0000¯~\x0007ÉÀaHII*;XMÍjºXQ¤»\x000br¨y\µÇwéç·ÕV{¿\x0000la¾n5å\x0004\x0007#\x001båß´ÓmèVJÆJPøÚ\x0003Ê\x0007\x0013¨ÎV1\x001cÃ\x0007à\x0000\x000eVS³.VA\x0016!3\x0018E0\x0004çõøYÐªx5ÿðµ\x001dUzuJ9ËºeÔ\x000eý&=ª¦T]b¤S#B£H:dÛ?\x0003«®Yu\x001f+åÛ2B\x0003E8®ã¼\x001eVW³º.VF¹¡´¡\x0018ÎÐ[j°\x0017Ûð\x0003è+2\x0010|÷´cÍ®ÜP\x001e)£3jOÆè >ðÝå\uÂ+Ô\x0002^\x0019b_Å§H¦	Gç\x0012Ih9£f²ÏU|®$Ö\x0007Ñ&¼Ð×ãÇBx²Âmx\x0015»\x0005æQ\x0005Ø`\x0013\x001f¤r\x0016|Q\x0014©mýe7Tê	h4Õr*ÐéØ&xµ1àk\x001bÎÂ½Ú`\x001a÷¡Úó*n£\x0013¦¢«U~VÐQöðBÑÆ VÖj,\x0011ÖÈgk>Û:z$î\x000fºÙ¢\x000c\x001f*
«ñ-½\x0016Çô'^Ø=þ%è \x000eê\x0004t9\x000bç\K¥\x0005î\x000cG\x0007gÓz\x001d _3+MEºe@`N#¢\x0006\x0005Øºi\x0019:Gê§{¤\x0001Ú)MEiÚ)ÅPR\x0016^:)ØfÜÐý]ãü­¼ðwÅéöíj¥¡ëØyu¤0ù[1¹¨0á)Ò<çz(ÐCe0ç\x0002³ÄXÞ|=&ç,\x001a
CÚVØ9UÒÖíÕÁùý$43$Ì\x001bìÜF;|ÅéLÚ:9<8?\x000b_§^á\x0019SÖ=vh\x0006®Â:Sp*ÉÝ\x0013ÀlæT¼äT¼CïT3®sn\x0011\x0002\x001aÏe³®Ä´\x0015¦íÂêÉF´PäÔ$\x0018 Æõ\x0012­|Z\x0003'|m\x0007uSu0"unÂ¥ñèô~ì"l\x0006\x001dB2\x0011Ô±\x001eÐðôÎ	ÁÚ\x0006m\x0008j±÷ã
ÂVP1xß\x0001\x0014¾vj½2µ5¨j­@c-g­DÍ ª\x001aÑX7Ü\x0001ª¡¹W\x0002JÜ	\x0014\x0005uÂpl\x001fQ%jPÑ\x0003
\x0005\x00194¼¾ò\x001aU£D\x001f§Ò4\x000e¥3\x0011Ôé.P\x000fíãR(vLM \x0018czÜ$ \x0015TîÜI¬ç´'·Èµ\x001f\á1JZÒ\x0015±9%¯/¥c\x0014\x001aÀéi_8½\x0018\x001ec°fû
ª:Eák\x0007§rèk7Ü¡¬¡Ð\x000eA7ròÂ\x0011\x000fÑØ\x001eµcF\x000eCðÂïn%7NÜC:YU#À¢Óbzá^Â×ôÝÕÃÇëy}Vî"ÙXh¹£\x000eëÃ
Ùòï\x000eÏ¿9>Öhe\&Öá¸\x000fïÀÒyõþæööêÇ%åGc¨¨A;t\x000bY%Mö\x0004¹<x|rrøÝð]f\x001c\x0001ÀXÅ\x0002VBæ\x0016\x000bÁ8Æ$`×c­\x001cl­´\x001eÑÚ\x0012ÑÚfÄ\Ý7QNCÒâqÄg­¤äRðµ\x0019Sz\x0006\x0001íS%Ä]Î'\x000b\x000f×c\x0016%_©t\x0017&¦!éOá¨V\x0017\[1M5çðµ\x00193É¦[\x001d5È­\x0016Jù(Ú#ËßY/MÞ³6\x0005\x001dDZRb§P\x001e_\x001cvH×é"08$µôS°Ñ¹ ½%\x0017Ètdr-¥©)M3¥ôÆo!Ç$4(©dÕ§q'ÐVF_\x0018ÆÑWý\x0019W2rJP¤\x0016j\x001bÚ\x0001o>Ô½R5eóY$§ÚXx\x0008gÇ¡ÒØ3ÏK|+¦¯îGøÚ©ÉK£¢Rzchz\x0007ïñFÌÊ2MÎXÇpfí,¥\x001dz¼ÂbU\x0004¹õ$â\x001f6Aòö	YÇX`§Q ÆÀsOcVN³ÃiÚ9­§BE¥\x0015F¥À&¿ùþá|\x0010ÑíÓ©á\x00061!AO6\x0013Ì_Ëéëëûæû\\x001a7h@\x000fÞmîPÊÛMª¬Æ;Vl7;¤\x000c1Ã®\x001ds*c³3!çáà¨­#ÖÎ©\x000ba/ê\x001ac\x0018ì`_;§Ùá4\x001d&W²Q¢	³¨nùX¬\x001dÒî@6[G ß37\x0010R;í0µ\x0014\x000bY\x000f¹s\x001e©óH«°'\x0018M7£ÂÅi!¥ÕÚÕÚµC*Ér®\x001ej\x000chg\x0018\x00169÷\x000cb\x0007²ýÈTÒUÍ\RËcg1èbÕ¤´W\x0003§Úál¿Î£2aÑ:
¯L,\x0019³f¬ÛÊéL}\x0016Á÷VN®±ë¶ä\x000eû¨hÍü :°õá\x001b\x0015á*Î+\x000b:Û¹ÇNZ\x0015ê\x0008Òx«9=«7gíg_,´8ÁÞm¿|áÕ7C274òó\x0006S8ÂÜ>Rî`6û$3êW-j^ké±Õµq­MÁTõ¤ß\x001b9·îs©°p\x0006÷º\x00142ZÍÉ]Í	ß[9c\x0017Ìi$îuNúÌvó.
¹¼Yêå­Å~\x001exÄ;ºb]y\x0016\x0018§5sÖGgüÞÌiHØO®Qj©Ä°¿µµép<Ww`
º©\x001d\x0013áp²­N\x000f!©9E³µ)l6ä\x0004½0T8ÓiÎ7_ëá}°3=s®É\x0001\x001bKê5CÙÂ1£p+§ßál¿.Ãö&\x0005ÔØi15¦t\x0006³¦Â¤o=âÁãWqªöëR!FP@àÄkÝBçÛÍ~³ýè4B\x000cZ3hÎ)§°\x0010×nw\x0015\x000b¥vÆ³Ýu(\x000c\x001br^Jä\x0014\x0012;
±ÍÞ.¡êPüÞÊ©m>à½ÅÍn1<À­)aZ	©k÷LüÞ\x000c)ÅéÓHZ1£ÛÓÌ(ë\x000eß\x00199U
«°\x0019(´YÃ[hó»M\x0004Ó°æÔÍï¡`\x0007\x000c·Iý\x0017x\x0005ÙÍ±°òë	ï­Ê\x000cÕ\x0002u>ù¹]
áë)ë\x0018`üÞL)IèC$ÍL\x0005N®(¶Ì7ÓQöª(SÔü%|-R¿½Y(§à¹6\x0005\x001fÅ\x0011MÜ;ZNËÄ]\x001e|{<Ý>\x0003J]\x0001Â×6À¡£Wd\x0000\x0018æëh\x001a\x0001}
è\x001b\x0001­'@\x0012	ÿU7Úc\x000eµ\x0001\x0016zÌ\x0000hx# 1Õ®$5Ã´ê\x0015¶Nq¡K\x0001V·®AsÚ
*'8mh~7Â¹\x001aÎµÂ©<·ÔE.¼Í¨\x0012e¦g³Á*\x0003¶ø½qj±\x001dZêÆ\x0007Ï`%ô|7Ö5EÛ®H(Dëö¥
í\x0005õõè?ç{º­%*,\x0014Âôê%/Û`=\x001e\x001c}øéêOKÙá±âq\x0008çX³¡.ÝÁv¿¹88zýýá·siìÔU¤®ÔÑÕ,Aþ Ð8B99\x000eävÝ1à\x0018ë!õrÐ\x001f¥$7Ëðõåötòî -º6AGVÝC:4&Pt\x0002Ég\x0014Â"]Oê«1õ=c\x001a,\x0007´&@±#Ï¾Ú Í÷¬&åEC\x001cX§UC\x0016Tì%\x001d\x0015¿ã¶w~Zôj=èÎêÚQ¼è¦Ð\x000fl¬\x0019HÇ|\x0007ª¬ÇTviÙ\x00022\x000fH{6~Ø¶ r¡wò\x001c~Yê->\x001d\\?<ßüïü×áÏ÷KÌZ]ÌpNÂgT+  1æ\x0014íåÁÅÑùyøÍÁáÎæ\x001agdéKdé70Ã=JÌj¥Æ\x0006jºGR+v\x0011­\x0004	M¶m¨\x0013³Ä¼\x0019\x0018jJÐ\x001e\x0017Vv2\x0017
\x001996dè\x0016\x0002EZ¤P«ç\x000e}ìX)½\x0013ºLXõQ	
6C\x000b
È(ÇrU\x001eªù\x0005»fr\x000b¶BÛ\x001aÚnfCWJ: BÉ@Ó=\x0014[¹\x000buuàvv\x00037wÃ5b\x0004Æã\x001d\x0015FñqAi'¶ÑÕÂ¯[\x00166\x0014Z8\Ø\x0003:Ý
®\x0011Ú²jÀ×-\x000bÛa\x0008O9W¶#!q¿'4ÖË-kn¹mm\x0017k\x001b\x001dy¼\x0018'ôr«jmÃ×-kÜÊH*\x0015èO\x000f{û©\x001dÞÖ;\x000ca:Aáðö6ËF¾}øã²öÆÁéýÃÇyìXZ%O¥´Òp¿\x0019\x000f7Ò\x001e¼
ÌIãàôìüEn/Kn\x0018
ÜÌ|¤ÀíðgÇB¬ýÜªâV[¸Õ\x0010&È/Sé±\x0002Ç\x0019ûlÍKo\x0004\x0008±-ÔHâ$)#=\x0016`îiïÐÏmkn»i\x000cÙ¨ò¹%i\»=-\x0013ûÁ}
î7S²\x0012(k¤£\x0016´{TSºÁyµ-áë\x0006pCÊSJPbmØ¢TK>Î¾ê\x0000÷I×gpgQåËzûtóyá\x0005¦¹Ã«\x0016Y\x001d£¬U·'3x³Þ^\x001e¿{)FD(^*\x0010c-S\x001b¤\x0018â1³-\x001eÐsT\x0017÷|Îß»\x0008\x0019{Ï\x0017z\x0010m+uåKðÍõÃëð\x0018êP¸FÉI%9¾h\x001d;H\x001e3ÝoÎ_\x001f\x001f/\x0012\x0017úÓØnbrÀq£³?3\x0010sêÉ0ÝN®¸TKô¢RKlCæÊR\x000cú§+1¤ImÇfdS#^ä"saãÚp¬á\x0012¶bRå¯\x0015Ù¹
Ù¹^d°B©S\x0007Fó£{;'MfB­GÑ¸\x0010Û+<Á]qø>\x001eüñ\x001fîoW4Ë£±ÊX¹\x0016\x0018ÞW\x00104è¡\x001c½>;mI¥ÏKG¡vNÃ2¤Ç
J­\x000c>Zù8´\x001dRWº\x0007Ò\x000ekR§¶ /C6ÃTÏ"§ñæ\x001al`\x0006\x0007KáííÕë\Ìýæê&ð,¬P¥£º²ÙÇHê¸¶÷íÉáë£\Êýæð8üp\x0011ST¢S
j3¢1\x0007_iïIãulu\x0016\x0013\x001fHaâÛI\x0005©¾sBu\x0011éøúj"ÑhÑÅ~7/uqB=\x001e¼~¸ÿ}i\x0006Îáe\x00185
\x0006/-1vµ
­1_ýy~#EÊ²#¯yY7ä]G©¨r%Ç\x001a,N\x0012ËëÞ¹\x0016W¼\x0003Mæ<"bÙ\x00053ÝÔ\x0011£nX\x0011oþe\x0019m
g·7_ÂM´\x001cÎ,.|l¶f Iõ!Ó²G\x0017\x0007g'ÇïÃ5´ÌZö8ö/Ë¨\x0003«¤òs\x0012C­G5
VÌ(I5°\x0016µ|l`\x001df_hò|\x0018ðpæ+M«sµ°ÚÕv±jr	¨ªÍz¾Z\x0010ëøîìbu\x0015«ë[¯T×"4§q¥vHVÓm¬f'°\x0005aãJ­é»û§/×\x000fwWK¨>«³1g°a¥~l Å8ÉyðÝÙåû£óÓÃeÎB;0pzÓ\x0005jÝp/å\x000e¯$Ïfø¸ë@\x0007¨(®Ð\x0000*êÈ+I5Ó~}LÍ·^0ÌÞÜSOÝ\x0003ëjX×\x0007ksHf±õ¢'ýRkæÔùV\x0016M@º£Ù´Ô\x000cmAÃ¹U	µsÚ=k`õ twõÁzôåúñÃ¢'\hEíG¤ÂèTx£8£\x0016D
\x0006ôû£×\x000bNð$(¨KT¥»P\x001dµU
\x0005>%¿¦ÓÚÎ-¬»\x0002äÎE\x000f«¤ó,\x000crÚSNÓ´$ÒzN®|ÉÉ+=¬õ zÊ!cß3Enµga-\x001aÐ\x0000kÕ~|5«\x001dòE¤ù²RÞcÇ¹`[M\x001fW«`Uº¬Å\x001aVêN^Óo?^=>.Y«Ü\x001bJ\x0017 P¥÷\x001csïf¾úïß\x001d^\ÌÚ¬	ÕW¨¾U0
%PCO)Îs`íSíë`å\x0002s`¯=°T%\x0015Ä`\x0018âeÅøX¦\x000bÓ×¾kþ-%þl\x001eSñÅp'nee;¦µb/]Ù\x0014;%=ür}5¯à\x0006ÁPzJCïe\x000côs­Øæ=ô¥;98;st8£áXyÑ"°Â×.X\x0002õá`õ\x0014q\x0016ÔgVÁzXQÃ^XzµHPÓÏr×C#ø¹¦ÖË¬<-¢Ò9°ÊªeôãÁÿ½ú1ü®B\x0017ÊZ:\-Wä´9'H\x0017ö\2Þÿ=üîìôôh.~¸ªÂU¸ª_-Ã|L«]®Ü\x0013\Lgz4á\x0016úi\x0001×Ø>\7t¥\x0003\x0001gìòÉò²
¸Ó\x0019yM¸C+vÀ­;±7à\x000e=ãG²`cK\\x000cÜÍ]	ëq]ëºq©²Ü¤¶D5ß\x000b"Ü_Ó\x001d}X«ë:\x0017®ãxg,:.­á¤è:»6\x0018\x0005Ñ\x0019N0æ_òÊÞ:¼ûøpõôqÙåæ_ð\\x001f¢õÔÒ\x0002d*-Ö`CA½uxúÍùáå7Ë¨ªBU}¬^Q¥NACy1Áó¸¬\x0006\x001dtõ\x0000Ôø\x001eP-Ä\x0000êè\x0015}8üø\x001cè åCl}ÅºP-©¦\x001b\x0011ß\x0006ÄDôtG\x0016V_³ú.VÃIf)\x0014ÁPY÷4üê\x0015²Z«Bv-Vm.ET \x0011\x0006\x0016Õy\x000c\x001f÷í5¬ìY\x0002\x0005ÂïÙ= P³ÃqIj\x001b©w;§U8ÿè@2¶¾\ÿ¾()ãÃi\x0015zä\x000b\x0004z§äIÍÊhj]¾?úólà*a\x0012Sta:öBån.êºGP-\x001b§tÊ\x0012Tö§\x0005Ùi\x001cÐÌi\x000c)]Íöý]ËiKÎÝ\x0016Åë8-½\x0008bl5Ï¼D	)cc@y½@ûV¨ÑÇ
é	i[4vRá¬´(Ë\x0002\x0013Nw\x0016QK\x0004[£ÐªÔ\x0013Z	EâåZÕÃÉ¤0ú(Gé#,\x001e4rRªg=iÙw\x000b6=ï!\x0015Þåð?#ý=á=*4íÉ¥oæ
öü¨Çó*Nç( \x0014*(ÒÄ!'?Ý£zû®W¾:Fák\x0007©¥äÅ0¸$ÓÄ(\x001dLó\x0004¶µ¨ÚW\x0007)|í@5Ö\x0013ê¬à\x0019f¶ªiiêõ¨¦Ì\x0000\x000b{·Ê\x0000[J\x0019 ÂSñ rjÇ\x0001fT/ª3
¾v JmiT9ÆÃ\x0005\x0005¿A_}+*/ká\x0002ÚYE¹\x00028Zý¡\x0010@\x0018áÍ\x0014gbUt²\x0016K\x0000cÂJz´NÔ\x0010\ÅÊc/²!µ}	\x0019Ç¿|\x0002×jJ	¹^*É\x0014Öì\x001d£ô\x0005ÍP,\x0005»ÇoÞ_5%\x001cõ£®©©¥*\x0019á.idtqtF\x0019jíëÆ\x0007+dQ_\x0012 ¡¾¤u ¶aNþAý@fPghônj&\x0015¡ì"ÄKÉ[£è@\x001d\x001dJÍºÔísÍ9
£W\x0004iá:º\x001a\x0019yq\x0016qÐ¨¶íCv/óØ\x0007Tó!ãè­ªÚ5ðµRSP\x00124hÒû8Üç2ÒÆ÷e+¥®ÇRw¥\x001bz{Gc\x0019.{JJÛLiªÍ
_\x001b)Ðî\x0005Oþ&(\x001fËÝ\x0017=VèÅ¢ð%È~GaÓÀÇ {\x0005i>ZÕN_®î>®HDRÔ¯EavàÚóÌ;oÞ\x001c~³QuªûP\x001dEu4÷â#\x0018õC1³9\x0013ëiKÇX°X\x001fmÎFÒC®y\x0014ÃM\x0003;£àÔÊ~|Ê¥ëcU¹ÍDs.	ýäÚÝ±|~\x000f«`\x0015kLqê`Î\x000fíf\x0018¶ÁÊ)oÇz\x0010}°¾õý°X\x0014-	ÖR
º\x001dvá\x0016n\x0012Àå¼\x000f×ò¿rèu\x000c2}¦Û|7áÖçè<\x0010¤\x001eZsJtçZ\x0010ÇË¸n¬LÐ;Ä"#®±}¸\x0004yÃ#F©ý\x001eÍÆ>Üz£Î¦¨º'vÉJ\x0003\x0013ºd=»¸<¹ø
»%a¥âàëÛûÇ\x0008ýæéa\x0005r|9gEnÊTlUô÷±Ô\x0007_]Dò7ç«¸W_à\x0016v\x0003· 2è\x0001L+Ã*Ê^g3}ÓÚ¹}Åí·pÓYÌ\x0015K6µár¦çÁ´Øc3¶¬°å\x0016ìA¨	Tq\x000cîË\x0017ÍØw0`WzãÍ£=\x0014	<Ö
_´Ðé\x0019¡u\x0005­·u\x001d%ÈK[R^öd\x0019N\x0013¶ÂF]ÓR¼ÔÕ9
\x0015N¯\x001fîo~b\x0015g\x000bµ\HExV\x0011D
©Ìi¾Gñëó³ã;øæàl¶¶1Qûz·¿j\x00035·TZÂ4\x001e\x0015%Eó}WQ«ønçE\x0006$¼ãÂ\x0012y"×Ñ·7~DC¹ºPüEo´\x001eë$_fo×Ñw'Ç\x0017sÞ®D)+JÙC© ðÕ¡\x0006\x001d}cÆIåÍ®¢t\x001d$¼¸A!ð¸3\x0014ÝÜÈXÖè+jô[!AM2å(Épi=](Z\x0019eÍ({\x0018ùp¥áËM)\x0012aão]¥\x0004`ò\x001eL7ôQè©Qj¨ÂÜãÖn¤,Êò2
·RZ]3iU2A§èX¦\x0015SÖ²\x0007Ô%\x001frX¤'G¬ÙÓ*£\x0011SÕª\x0007S\x000f\x001auZ\x0001@Ql56nWSz\x001eMÃ"Å_¢\x000cëéàÍÍÝõÃÕÍÂ}o\x0005õ\x000c4 m\x000bÃQ\x0000\0=§Ä\x0011þqt~x¼ÈidÉid\x0007çàê\x0004Îüº\x001eÈ9]¹³P*\x000fµPùJNGï³!ßvÐf.\x0015[ÍYénð´A[;>\x0017ÝÇì5¦r·}âK\x001f7*Õ3¢t\x000bÅ^Ú:¨Â\x0011eã\x001eí ¦ÚIðµ\x001dj\x0019¤Ö@©3÷Ó5¢k@u\x0012Y(dÒäËJyçÛ«ß\x001e%eYÕÀ\x0007{¼cÑ­\x001aJØõùá¿_ÌK\x0011\x0017f\x001c@Uk1õ Î!\x0001S
?tëÚ\x000e*\x0006yS\x0000¯Í Ê
=|\x000b&ùÉ\x0019 ÆíGAUá´ÝÒ\x0019»\x0016Tº"È½CÚQ¾Ê´3k=%¯æ\x001d¾¶S\x000e;Ç~:@ò%èì²\x0001Ë¸Êö°²ª³|:¸¸¿½^\x0012\x00078
µ¦Æ]\x0010/8&\x0015ZÏÌúÅÙÉÑn|¦Ô¶¤¬ÛR¬£4ÆàO5Z¢?[ÏT\x0002.S?4\x001a!j8{)ÔîsøþîãUøº£&\x0006ÏC\x0007ËùÎa\x001b\x001f6#\x0007\x0010\x001fÃg§ß\x001cÂ1ºLl+âÛa-1SÔcã`PSN>W\x0016ÞD\£X^b1È\x0018$_`$öT\x001e.fbGmÄK*\x0010W\x0011æUÍ\x0010Ý°*0yÉÊqzm'q)½Â¢ôJ'ñ \x0017bð~
c¬©\x0004Ü-¼ØW«Â÷¯¢é\x0013¾\x0001´zL<N#è#æC\x001bi ¯½L
×Âëa!£ãl_¿Vd"-(ÕK]Y\x0008o¯?ß|>x\x000fBw\x000b¯Am¨z\x0014jcyAcÆ¹Û÷íÑ»ãw\x0007ïACòt\x0019WT¸¢\x0013\x0017DÚÑçN\x0012ºPv"^ÅÄx ®;ó´\x0010\x001bN§± Öe8
-×G#°¯}7°3t\x0018sª\x0019ñú¶Ï¨¬%fÐ&ò0\x000eÿF]æ~{{õá§?þûa±VÛQý»²\x0012ÛPÈ¨o\x000e¼³±¶\x0010å;~{r\x0018ØÏçå¥à%¦m!×Ã_Â×"qó°4®Ê\x0019\x0015\x0011\x0002+2U\x0016@bár¼\x000cÂñùüh\x0006BåËæ#aEÕÚ&Dé\x0018¦ÆpÐ1ÏÒÃ\x0002=Xà~ÚLÉw(y3¥u(-º\x00080BfJ9Ýv\x0011ÒAå\x0012Ãû\x000bÄÊD}º^=Â?Nî>Í2­dõ¦M-\x0004§jw>÷hx{x\x0001ÿ89»|»\x0004lÞ\x0012\x0000\x001cc	=ÀÒ\x001d+L0Ò>²v,$ÑJ«¢r(\x001bLó`3Æj¹"³àíõÓ§Û\x00151A«±÷ðe\x0019N¬Ã
+u.ëíÑåÛ``fu5«ëd\x0015Ù­%¼äÏ\x0014ë.f3bÖÓ\x0016õ@»Sß¸v¨Æå\x001c}\x0007\x001ajò\x0013ntã?\x0007®¬qe'.uJóðöÉ\x001e®p{eÜ=Ý}ºp]=º®st\x0019µs.ùA\x0015$\x0019ÇFV\x001d\x0015\x001br°' \x0001\x0013ÕY*ñ§%qòO¥täPPØÃéñ\x0005Z/KñËBa|7\x000f5\x0002óÒIc^Â×~b©Ð,\x0007Y<(.BqFW'µT\x0015µT\x001b¨µ\x001d´¼$ùn$QïIï¤.\x0002\x001f@mä\x0006jG1)ÐÏh aY¾5ü¤ì+µõ\x0015µõ[¨ntd\x0004jÏZ7Nqè¤ö5µßBmå\x000bý¹Ý\x000bW\x0008õ"²{ú²OQO%ã²þÞ]ØzÃÊV/\Þ¿È-,-ìË¼{7þÅìb~l14·þÎý\x0015#î±²\x0015'}Ý¢Y8ªMÞuñùêãbðdh\x0007Æ4%Yjª¸Ð{²
Ð$¾xwøÍ¬»!¬Ð% \x0017ºÐxA)ETêk\x0015-]½/·¤
q(¶·"Ò\x0003M2ÚTVqCS5~+	Å O
ðµ0jÑeCÇ
âB\x000fKû¶"J-KDøÚ\x0018ÃN¨Bú8Ð9\x0003«:Ç\x0001ñVD]#¶.Ee}öÈ\x0008¯¨O!w\x0018ÊQzlÝ6"zU!zÕ¨\x0006êMqõ	Jm\x0019Åäº/Nðxb;\x001eÏwO7·×\x000fK:î:äû0Ô¤Þ0Îy©\x001cï.OÎç¤Ü3¯\x0011%¯Ùu*¯åÕ,;í-ÁJI2þÓ]©`¹V%,×»Á§µ´\x0012º¥@Ù1ÇPÀÉîi×Ç;XV×îæ®æ¥ôA©±QcØÏÝîòêâ\x0015²\x001a_øÚÅ+x\x001e\!p¥SÛ'9N~ë£5¦¢5»Ñµ´.ùØ'`ÝNÛ=µ\x0002\x0018àåE¯>\x0019\x001b\x0017ÏÜ«»Ï÷·7wÍ=\x0018\x0015ÍK.\x000cõ\x0006·\x001895ÜÍ	Ô_\x001c¾;;9>óÍ"¯«x]'o¡HÄÄÿ\x001djé\x001a1[m×À«*^ÕË«}È
\x00004Fô\x001a×~÷ñ
>åKÍ{yIã\x000bºä÷­¡¤r9ÝÏ¾
·8Í\x0002®õ¸SÖ)XØ_\x0001µõÃ»ë¯c%¯c½¼ª¬È°\x0018+ÎE[ÊRßå¢@Pè¨£\x0014\x001eW×XÍüq1Z£\x0016Cm ª\x000fk\x0019k\x0003Ýd/I(gþf>V(b@©Y;åpñ*Mî\x0001/q8ý\x001e·vJ]QêfJÉÈÍ¥\x0019ªT\x001by\x001e^Ï«fH[AÚ\x001eÈ¡õº&yb_´Ë\x001aíúfÈAÚ\x0013 ê$9Z%-Aüóãú¢\x0006J<²E¢Ê¹¥\x0016À«ûÐË\x001fÿ½¤ô¢´£"\x0003éq/YusNcá¥6À«³óo.Ö¾:=-*ßèí\x0003KÍrè\x000b\x0012ÎÛ¼Ýã¶¿BÑk§^K[ÿ
¬2i©zXÿ0ã¢ËM²Ù,7©ÙìÖ¿\x0018<Ï&\x0005{1s°Çìéý\x000b¨Pd_G¹?\x0017\x0006~}÷°×\x000cfx\x0010qP fý·|ZR&\x0004~tz>Ø`\x000b¡\x0000[é´À*jÕ*5&\x0006Yé±HÍÍ´ñº×u\x000f.­j9a|ñnqcEÞ>ÜAð\x001ap­ìÅ¥ViT-;\x0004\x001fY\x0015¼ÕÚµ½k×P¯äøPN<%°\x001aÐSVqÍ®½f¢½6\x001c\x00151±í§«\x001fîïnÂu¹\x000c­\x001a³ÈÇ2K«\x0014ÕñË±3|8&bnÛ÷ç¯ÎNÃ½¹È]\x0014\x000b\x0013Ëû¹\x001dæ_\x0019n\x0006Ç3
ã³q¢f?¶ª°ÕFl,Ø¤¡¡\x0014iêìiØÁÍÓ­X¼@Ââö$\x0013?Ý¿ÆRË\x0004©­\x0019|\x0014\x001aßxjù\x001b÷ÊÜM\x001e;¿<\x000eÙÎ	»\x0017!Ç°\x0013Û°¡Ã=µÑ1\x000cR¨ª¦=ë±Ï½B\x0017HÉ]] ·7w\x000bÆªôPH+\x0018j|BXJ£Ñ¬ÜÒÛãÓÙLX)c*FnÚ!!Hþÿ¸{·ì(®l]¸+ês¬ûeð`\x0019ã!\x0010G SõÂH@\x0006\x0019!a!Q§z=MØ=Ø»
ÿ£{R-ùç\kÎÈXÊ\x00157í¢Î8r²]®ïXyý¦È	?/\x001b¥½2é5\x0008Û²®0ÉºöBhn\x000e\x0006+XÎ×¹&g\x0006¯qo%F
HS4ýA:¿\x0010K\x0005	áÞIU\x0008­*\x0010ZÕ\x001baM{Y3xÄyÁÊí\x0011.á eýËÅåÙíé£\x000fW×7×ýw·jX8M5BjaÉWÜ7~WIÓz\x0004éÃåÉKtñÞ¬Þ®>ß\ï\x0002ªZuä\x0012öGª\x000cüÊã&Ê±\x00108KÊÝH;^i{e"Rc mÚ6/\x0005xCÓUwL\x001fëÔHí ¤²©½õ¶Y¤¡\x0019é§î(AèTÛâëãÏþHå:9é°+}\x001f
96Jì,Áí´%íH]\x00184°`¦\x000b£Ok[å\x001dzo½Ö,7\x0000?û\x0003\x0015=teµm*"7À;l¾H¥,·~úÝ\x001bªöÍL_e£çwª4k{I³=¸§\x0007TbZ½ºØ¢]ÌrÆ\x000eîYÎÒs¤Ù.x^K£\x001aqGCñ\x001a$¶\x0006Ô`Tmª7F\x000bfÜZr6ä>\x0011\x001f\x001b¹íÐXº
Q÷\x0006®$Û¼FÅóyx¼\x0018¼Ç=WR-HÓ\x0006i\x0006¼GGc9ð=:ê\x0010kéÞíp}o¾øÖ¾ÿÇF½-c\x0005B\STëÜ¶>bo±Ø5±ÿ¶Aó·tÓ	äÙÇpv÷øZ­Áwik«\x0001(
AÌ\x0012DÝL
1ÛÝí}1*S`Ä}1:ÃmvÊ	A':,\x0002N*ÀÖ\x0019ý*U»ÌHeqÉ¾0}\x0013OÊÜZ¿"\x001fb»Ö»/L-\x000biÞwO\x001e_r
ü6ÁâhTÎwjÛw£\x0014Òl\x0004Fðxí\x000cÍÃÕÇ×W·UóR¯[S(^\x0016ÖGå¶\x0010û:?ópùôáñi7H[´C@ªfäVª0¢¨Mãex±-[Ó\x001fgK\x000e\x0006pbMMoV®ÛyÜ\x0016+\x0012¹©}ËiëS²d\x000b¥Ê­G\x0017«Oçg×\x0007\x0000iÿòLóÀr-UU&\x0011±]e/Ï\x001c\x001càîÞJBnØEð·\x001bÍ\x001d×+T;íÚL@4.T\x001eº\x0007ú"3KF/JðöÉ>?Y¢ÚéÞ}O`U\x001b¬úw\x0006\x000b¾·hM¿à¥)<pG±ÔòÙ)­Ø\x001b¯é\x0006+\\x001a\x0013ØR1\x0002Ç\x0000EÖÛëÉõy§¯\x0019ê4F<R.YGÜúm³n½·<éFØ\x001a\x000fÃ§DOZ4Ù\x0012ÊKQÝ@Ðï©n¨BØrÚ\x0001¡5½ßa\x0013=tMº\x000cÞ¡cq{ÏW#¤¦VL§<ÙºM GZ/4\x0005Ñ6I\x0011ÁþZ¸C¿é\x0010¨KãlT\x0008	ª\x0010\x001a\x0002Ö5`ldú×Òá\x000em\x0001`Ûùi¬Æ\x0013\x0003Ñ\x0006Ñ U¡¹ò9¬\x0018î¹4\x0004l+`¥\x0019\x00066RIY'ó\x001c×°§\x0003ª\x0007T]¾W=ì½zÑÌÝIõ8t¶DS³í\x001a\x000fAÛA´F
DëUàÖk6¬ë°vwàÔBoÞüº_¹:89½ºí,Ù\x0007_kAó\x000f\Ðä);OëUÉÝ\x0001\x0007LÖ<y¸<Ý[µO@U\x001b¨\x001a\x0006ÔãØÊ\x0004Ô»Î§¿·<TBÊÝ^I\x001f¨­!j\x0007am\x001c½ôR9\x001aê©ý\x0014\x0007YO\x0001u­íP[Ò\x000e= ba#\x00087¦¹²°ÿ#CÝ7Æ²\x001aª\Kk¦ªÜ0¬àº×\x0013KQ)¥¤Ý7Ð°\x0007ØP\x001döb}S1
»©©rÔäìÃÝÎÓõ\x0007+Û2®-3\x0000­\x000e¶ÐwÊÌ®'Ël·\x001d\x000f@Ú\x000e¦ñÐýß«
ëÂ\x0008\x0011ÙvÑÚpÙ7*°\x0007Ú¸6\x000eAë¹CÀT[½F;våxikÉª\x0007a£Sãäìru\®(ÚzL¸¼Ãðîegå\x000eýç¢WãäðÙò$9,[ÍF\x0000y«×¨\x001es3\x001b\x001c¬Àc.]`?;¥Þ¦\x001c
Èa8dÁB¾Ñ+w[bDTû{xj0\x0003ÒFÀ"Rø×>¿X½9;H \x000e~9[uéÿ`Cj\x0016aåØ¯óQ5j±Û½\x001aÏ\x000e\x000fÒ\x001f\x001dür¸Ü§ZC\x0008U\x001b¡êpÝ°c\x001dU]E±\x001aa8H³\x0011dA!7xO¯.oÎø0HU;g\x0007®..ºÕÖ¢oêßM£Å
þ"kSøíá
O½<ä3!Õí\x001c\x001e<:>:Ú/\x0012·ª\x0010\x0010¹\x0018\x0005=42ÇËc\`ÁoÇ\x0001Þ\x001ay\x0002Àñà\x0019\x0003¼\x0011å3¦é9@ÝmÉ¸1ØMñÒÍn\x0004¿qÝxÙF=ÍÔ\x0002¸\x001b­èTz½yÄ]Ý~é>àà6n\x0012ÂÆs9\x0000\x0016\x000eó\x0001g¶·dyÀ\x001dþÚq$ËÂÖwëH®Ä+E7ÊF³1råp\x001dÚ£\x0015xs!nËeS¦\x0014~qvÝysYÙ4£­\x0004m4ë\x0008ø\x001e±«\x0017'5\x0010u\x001b¢î\x000fÑ6ùÂèÙ\x0000Ó¼ÑqÝîöï
1¶!Æþ\x00105\x001fcJYÂÇu\x0015\x001e{	\x0006â[Á]S|å%üArÌÏ>¿=»kíâìóÁá»ÕåMÕ\x00142Öò\x000b-Ýµ°Ù\x001d}'/üxø\x000c®¶£Ã\x00178ö`ùìe]j*Àøo6\x0001«6`õ\x001d\x0000ÖmÀú;\x0000lÚÍw\x0000Ø¶\x0001Ûï\x0000°k\x0003vß\x0001`ß\x0006ì¿\x0003À¡
8\x0000¬\x0017ªZX\x0018\x001a\x000c*XYÉ¨;r÷AÇ6èøïÿ\x001b=_\x001eâ;@\^wßÁ}'ûN~\x0007\x0017,.<ù\x001dÜx²¸ñäwpåÉâÊßÁ';O~\x0007,.=ù\x001dÜz²¸õäkï¾\x0010\x0017Wü\x000eî<UÜyê;¸óTqç©ïàÎSÅ
¢ß Jåz¦à4\x0016Ô§h«%Ix©ý\x001d\x0013A\x0007C.\x000ed5ü@\x0006ráHÈZ\x000e:\x000cÍ{\x000eÛY£Á¨\x0003C80´$ÕD»ðT\x0015y|¤ñ\x0013\x0018É¯Áè.½èÀ{~¸úL£]ÑI¥\x0016¤G¦åõàD3ÚBmø<\¾ Ñ\x001dÀÌ+õÇù§ó7¯²>f¡yvðüìk
ñpFÑ0¬sýüPâ@\x0019÷`ý\x0007?¼=ûáùÕíõ÷«ë3åCÀ1c(^ª½×R.ð5K\x0011l®Â\x0017í¢ì'\x0018þù!ÿHy&Y÷üðo;\x0003Cm:øÑÒc.:Z¡äk¢#ô\x0002'û \x001f\x000fêÕ§Ç\|¼Z(â£Å\x0002]Dä\x0013räÞ ÄÂ»'=fâ#°àÎ$>XÇª3\x001f%{NQ\x0016<\x000e¶¥¨voÊÔt|Íè8³DÇ\x0019Znðÿ¦ü<æ ÛmSó\x0011r\x0011òrS)Ã%Ã\x001aþL¦Ðz\x001bMÆ` 9=æ!ã£\x0010¼wpü|
uKaM®\x0005>"L¹Ø\x000cß¤ÇL|\x000b\x001bÈw
ð\x0011.0¶hÑ\x0004|,ò±óñq¯\x001ei#mVhâãc;\x00151OÀXR³m\x001e;ÀHHG¸E^nÊ:Þ>FL¸}dJuåçL|©c4\x0006\x0002©1jÚ?\x0011U\x0017F\x0013ºýpöîÝ[,9Ç,=\x001a>?}ºº\x0005Ëñf*NÎÛ<\x001c8E\x0019\x0017(ä	d5ÑD]õ~<|~|
¦æ®ö\x0016-7@zÌI\x000bÌï!Xeó§\x0012i\x0019Weõô \x0015ð\x0016
f^Z\x000eÛ©e¦e\x0004Vê&Z&7\x0004\x0003/Õ\x001a5
/¬
vf^(WOò í\x0002KH\x0017ê\x0001^2NÍ+ÕTÅvké\x001c¼\x000cX«ywyìîEZ!zÞ]p^T\x001dè}h¡Ì]zÌIK{t@\x0013-Oâ\x001eÀËeùSàåüD¼Þ_ùo+®0s~´:x~þ­úLßü¿^ýðã_ÿ\x0003\nÊÅê\x0006m<eÁ\x0016RÈFû\x0018²\x0010\x0000ÖÜåô±¾í±nÁ';å\x0002Í«/«Û?¿}k3@9Ï«¯SØT$¢Ñpx§Oúmºl±¸,0^}\x00079Æ\x0007\x001e\x001d?}¸³±¬ NÄ÷KäêOóåßRY\x0016|\x000e³Ñ'ñ\x0014ÿþæfÒ\x0015&uVX@l¨:Ç+\x000c`Õñ\x0006kí)þýË»×Û\x001dßÙûb\x00172;8
LdvØ\x0015bÈãØÏ_ÿøö\x000fjyÊN
½#øgYÓ±C\x0007]#;c\x0004ÐñÙ£5Y@\x001bÜ5©«<Ú£'ÏöÎèlsÃczÌÍ
\x0018¸tò\x0019\x001d\x0004FD³ç^\x0018§¢Úwô
ãæSÝÈüÝÀ¤p9N$É×uXk;5µíÐä
5\x001c.ò =æ^]zØm\x0001´"t¼ÛBKß[z[é177§Òü0äf"\x001c[ÌÓÖ5Uá>Ü°a1=ææ\x0016ÂÂÛÌÍÓÔ)8%µ2Ä­D7
7¼3ÓcöS2¦ï¦rR\x000eOIÃßÍÔ]oÔÖg_¯R­{
k¶¯îýó¿þúï.Î³\x0008kAb¢à\x0013¾O~!\x0015\x0005\x0007³\x00028\x0006tÝ\x0017Ä<Ó¬ßÚÙPÑæ®³¹oÎ&¥\x00013ìHO\x001b«³þ¶Á\U@g8g\Âþ9§,Câ¦6\x0005M¤\x0003xt3s\x000f\x001eÝs÷ÀÙ£,HæìÈ§\x00108^9Ûºw(çmSü\x001e8'%ÌÙ,h;kû:\x000f}8cø×[}Ïõú+Ó$!¤Ì¹\x0018+8\x0007eØ7ÖÞ3e"°²n³:O=\x0000Î.ÖK9ÃÕgÃýrN4ÞËäK[eT³ç½§ÐÀw÷¼13Ì\x00192O\x0003/íÊxÛ`Îx%ø{^Ú¤eÈ\x0002\x000fÀYr¢ßÛP\x0018ÊYbÒ_\x0016ÿ{ %39m!Zè\x001cJ1^óEef½%~cyÏ\x001fÚÇ&ë)AÇ6q9KY\x0017`éGú\x000f¯>ãÎ\x0007\x001bº\x001e?¯nS?æÇ×ÓFÊ^È#eÒ.r \x0019|#MæºÚ£åÁÏËÓÔÄùôáîPÙà¶71\x001fC-,\x000b2>¦3¹ý\x001e'%U:K}9n_Dóq\x0014aÍ1`Þ*q¹Ä
9VGsûqÄìQ\x001e2#G©0ÔWj\Çaò\x0014I\ª¾îôíÉQbI@zÜË\x0014T\x001b\x0007\x001fRsíã´O!\x0000=âÍ·O«\x000f+¥áêÐEÜâåÙõÇúEgÑ\x0012ö³Ú\x0014wZH
ÈÃ%jm>Q¬Ë~¿<<yº'\Ñ0Jrºé1\x0017#\x001cdS Ú)¸.¤Ì$Û¹iVñ,Æ¤Ç\³Tåðo)¨\x0014ÍþÁUy+ÕpÁÙ9Wrqa%1R\x0018KJ"\x0005\x0016bÕýöEþñÇ§»ÒÏ\x0007?]]¼yë¨'ËG
'\x0016.ßÙ\x0006üh7Sä\x00185Ê×ÐzqðÓñ\x0011ÆÿjáDáàçgôG\x00133#\x0016Êgf&wæ\x00033­kÇ>Ì|XzÌL
\x0007Jé[)(È%££ÊMkbØBfj~f\x0011ÝÄ\x000cìOÂès\x001b\x000023SÛªé\HC\x001f- O?\x001a\x00157Y+t[Aí­üãÏËw¸Ó°?®ÍÆÛ§g7ï¦+\x001f¶`\x000eûdF9\x001c4wÑÐ(|ÅÇ:=xzøòñnË¢a¤éÚútSÓq2
¡@:Âû\¦\x0005ÞâK«\x0018W9\x000eæ­d+yõÓÁ©Té1\x0017\x001dkñ\x0010Ot¥` 44¯ÌxïlÅMÕÅG¼ýðõu\x001eB\x000bk×»\x0016\x001dTC?ûzz&3Òá¢\x0010§À*gM¥Í\x0012tÆD_S z\x0014Ô\x000fÿvr|ÔMLb0-=æeæ¦\x0008½VQõ\x0005\x001dh¢\x0016cQÛÂ¼²³SCµ@)35\x001fÈºZ{2-ª9Ê{QÓ¨ª¥["sQ\x0003ÏXçj'Ø\x00028Ré@\x0017°¨I%õd¦ú\x000fdé\x0012ÝÊÌÄÌD\x0001äÌ,\x0017&f\\x0013`VSçÔEÁðôvX\x0000¡pUbü×ÌÌÔ´(õcò\x0018é133\x0013\x0016Få3$ÈÆÐl\x000eÊ®ÓPÃ»$=æ¥¦¢^¸©å¡OÉUv©éJ ^Ô\x0002\x000eÜK¿\x000eTÀ¥áþL)\x0014ï´PÓnZÃ,øßÝ|§E¼Ó6B®¯ÎÿL5AgÓµ\x0000yÜnÙÆÞ-|\x000eák/(\x0010å´ª>:9~òÓß\x001f>Û©ÄØâÆh!î§dK¢ú\x0000'±IxººV´!<qizÜË÷\x000b\x001b4À»Ì-]ÈC¥.Ô\x001c2\x0003y\x0006ä\x0019îg®ª÷\x0002kØ&Î(kS\x0016½ib/Öò~h¢$¼$qk\x0003´ãô©Õ\x0019¶þ41É¶eíkzxÍ+>gSê"dm­7O§¿§SÈ¦±H38îWÖNpfXËºRjç\x001f^ÿ©ÎS{\x0001:ë\x001bFÎÕ¤e¥V8*ÄÓÀÝ?x)Û&D¥ûw¼;Òµ&çµtzNB2R5¥FS°K9Ã|b­ÏWÇ\x0007»}2äë¨À\x001f"¯ÁSèÁV¥@«ù`¼_¶þsðÑlE+ó4Yü@¬Î(jj´k	),UI\x0019	EjCL"êNÑ\x0007òä°\x0016²ùcùh|Nùøh8\x0011h\x0003YK¥mR\x0005ëù\x0003Õº\x0005UÐÏÑ\x001bÎÎ´pÜEö»\x0000B:G\x00144h\x0003B89`:B\x0018È×qÎ/\x0004ÿ&jä3Øñ\x000b¥\x0014buàçT¤Ì:\x0008Ý8ýöö\x0003\x0004£4ðV!ÏA=xzv}1Ý\x0015\x000b;\x0007kýC£à¶µYÓ@°eh÷\x0016>yú|ùâÅazðôðähO\x0001DC+µîÍÍ+øÆQs<Ée\x0018(ó\x0002´öjO\x000cäG¸W$½ °Ù].rF^Ê"mØwÉ\x000eã>
þ5+/0r\x0013)|/É
\x0000ÁS5\x000eðÚkº\x000f#æÀÅ¿f%f_&æY`\x0003ÜJ&¶¿¯¦\x000f±Oçï¿ýÅ\x001e
Íÿô(¦\x001f<¿X]¾y?\x001d5©-3:\x000ccå¥h½§!gÂ¾Ó½\x0018ðühÝQ\x0015ÔBZ³S\x000bcp4ºSDg\x0014Å\x0005¬Þ[A0ÃÔ}zÌÊÍxç<r%«ÉQÆjûÞ«\x00025ZÄQ\x001cqk\x001eÇÔÔ¬Ô\x0019ë0æïr#MëJÔdÜ[¬3Dî\x0007ù9+¹4È\x0019p.q\x0010=³{{cÓx>æç¬äP\x0017!\x000bÇ9éüºòì\x0010\x001fÅÞb¤ä\x0002Ö»§ç¼ä¢£t¨aÓ&óü\x001bèOEîÂ½y÷û;ÒØ­Ë-\x0015ÔNwÃiÍë2ëvàcñ\x001e¸\x0007*Ä{Z÷[*§­à·á1ÏÇOZêDÉü²èR\x0010¶¡×\x001d\x0007¨¦÷ñO¯å·T.ôlQ\x0005\x0008È~¿ºÔ£Á6\x001bË+<7æL½dwUUë¿8x~|úËñÑnfÍ
c&é1/«¨©JNy)¸\x0014ÆãLØ,"ã«z\x0010Óxüë¶Þ,Ä"X$#iz<ðb¹Pà<ñ\x0007Ó8+=æå¥Sûu"\x0006w¸\x000fcbÞÔÔbõ!æ°tÉµêæú`nás\x0016Ûå¾=ø\$C\x0007¬|MÚ¥\x000f+TÛNyYE¹H8ÊØÔ¦¼\x0016ÄË*\x0019º\x001e¼<B|{íÂ×ò¿HyY¹<ÉËb#E"ÆÂ#ð¹ªt_û\x0010ÃBh_VCÏAL8²<p´.öò$b(Ù*m¦nboýÇ3yE:ÿIÝ¿°\x0017ºº¼Y×'¾êz\x0005\x001dkyl$Õ\x0011#)=Kµ6ãOÇÏ^.w{,ø\x0019Úß\x000b?.\x0011ÔÞÛF\x0013M3=So\x0012÷¡IMs\x001ezDc4fkI6Ì\x0019Å½ûÅoòÃj\x0005³9¥s\x001e~¶ág\x001bI
§9âùÓóOJ¹	ú¨"Åí´*&¬ä^]¸c÷\x001d-ýø}Ð\x001fÞ|Àá°\x0016Í7[Ô<¼ývþnº6-\x0011ù2pðïZdgM9vÖ\x0012U]\x000fOÿþäñ6-¦ùzh7#§C'r¿£Nõ<Sdy\x0004°&æ±èüñ;ñ\x0006s\x001aèÙH\x001fÛâÜÈCÏ,=çûN2ÍãN^È\x001cUUü¤UÅV]®.?ÿùûÇ¤¨úJmçåàùêë·Õ©\x0018\x0005\x0012$:\x000b\x0017\x000bîN\x0010ÑöeD\x0007´J\x0012|ù·¿/\x001fu3r¸æ\±ð&fôW³\x001c\x0003ì¦\x0005åÔi2JÖI\x0016×\x0012X/\x0019UPÔ\x000b\x0008v\x0014¸-²ê,Â¬TM@5#ØA¡p1ÌGI{ßì£\x0018\x0006oEJ¢N\x0003§ÇªÓüR\x0000Ï\x0018ÑØ `dD`FÓ~$¥.ù9\x001b#ì¡.üh(\\x000f\sÚÕÝ´L®\x0016\x0010bÆ³\x0001Î;ÊY§\x001bo\x0005õ3\x001aQWFÚAÉ½¿9»øVHs®\x0007z?z¿úøúªZ~¦ÆÔK\x0001ì\G$
)ÐÀ\x0019nÉ?\x0006£o¯ñz\x001aø£O\x001f\x001eïÖ9·+X\x0015©¼\x0010;5e¸Ã?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ùã²\x0010P
\x0001;\x0008\x0001Ü\x0015 åÐp¿1°æ#l\x0014BB¨~!¢+\x000fli%M³D!tÖcÌ\x001dBèR\x0008Ý/\x0004d\x0002b-s]\x0011·ñìoè\x0010ÂB\x001d®¥I¹áK$Û\x001bÈéÀ°Jn\x0014ÂBØ~!"rIoBivÜâøÊºI\x0016Ù\x000e!\)Ûá:A&ÄîS"	ñSÙNr\x0005v\x0008áK!ü\x000e_ÂòÖâÈÒèyn\x0016pÌó\x001d2R°\x000cÍ\x0004.ÃáÛ4ºÒ»0F1¥\x0013ý2ÄØMµËýîBg7CNV¬;¤¨íõ\x000e\x0006Û\x001a^¿¬.ù]ç®U¬9vHQ\x0019ì§MÓ·0ø\x0014\x0007
ÉKêÀìïvÈÊØ=q¤\x0008ìw\x0018$O\x0007"S\x0006êÉ^Ü\x000e)*k÷4ÜiºQúÈ«Ü+O¡Cq£ÌdK_\x0014Â=í,vEg1®jøæþýÛµîwt´Dª_["R®ß³÷êâ¢oÎ_>÷õÃ»_&áB	\x0017Úá\x0006æ¾µQ££ê£­&¼\x000b\x001d\x001b«áª\x0012®j\x000b\x001aL¨éÐ\x0006FëçK)«áê\x0012®þâáú\x0012®o«,§xb/ã¨ÅûJUwé¹Éêeû\x0011«Üþk­\x00181\x0013ï\x0005>¸ù¶»-«cíçC¾ôè0Z'\x001dt~y\x0003r3f¨õD»¢À\x001eYO
åÞ2ëwaùfÌJTÊBô(7²éÖ\x0008ZB\x001eßß¨wC\Ý\x000cÕ~3¤â¹Íh\x0006\x0016ÏkÇ§l\x0017ö:nÀ<\x000eÉ\x000e:Îô¼ÀÀ7CãcL/\x0010ò\x000b\èwÚÙVm3fáóÈ¦Îa×"ój³·\x0004ÙT~iw,ËÇ\x001cO!+f©÷f2¯·\x001ds¥4L»Ò\x0010
;\x0006\x0012æÜ\x0010ê\x0015³<z3·Ø¹ò0L»\x000bÃéj(I\\x0006\x0011³Ë'÷2lÇ\©
Ó¬6prÇB¾\x001b\x001fò
·Þc¹\x0019s¨0ös¼\x0014Üã¡Ìíèõd"e3d[]gÛ|U0\zDê\x0008ÍÇm YèMÝ¹º\x001a¶ãj\x0008^3ÃéÔtÏy½¿¹º\x001a¶ùjà(£ »ÃQä\x001f\x00013Çy­vó\u7\ûÝðFw-(^Céó¢;¯w³¾Bì;\x0010\x000b.rY9>À\x0006Öp7ÿÈWvÛ7ÛmÜcÇþ\x0011ò¯ÑG\x0008¬èÔ<È\x0016Ì¡òB³\x001dÈ\x001cU	 f.Àõ°\x0019vÄ\iÐ®5l`N0+\x000cóÜ9Ïä¤^ÍSZlÀ\ðù\x000cQh¿\x001c\x00162¡E\x0008Lè\x0018òÒJô
e
Y¶CÆ
-Ñ+¡kì\x0004;\x001b0½T{3è:zm\x000f_Q¼Ô\x0004I¼ÎzVurad{\x0003æ:\x0012í¡ ÒÙt\x001b¯òxáY\x001a+Ù\x0000ZWè°k·\x0015´äÜq\§ ¹­/ê½Ý^¡©´ÝÀWÛ\x0008Zin£46Oô;\x0017 ýTGÑ/ Ç~ùÍ !SÜ\x0019­è\x0019\x0002°.F{aöõAûöÆÝktÐj3âöfçöS\x001d>ÔÛ=;	GtÌj|\x0012¸ÙÓNv\x0014lÆ\x001cjÕ\x0011ÚUÐ´`ÜèLïDÆì\x0016\x0018\x001e¶`®Ut»ýhÿhq±A¶8Ú\x001exÚÙõç\x0005Ð ªG\x0008¢ù\x0011"hÅ\x0014I9\x001bAóIÝ²2Åvî\x0001´l¾\x001d\x0010\x0004÷/1¾ÇËuC;O¯»	´©A7«\x000e\x0008×A¨E6Æz\x000blûp·\x000e5èfÝ\x0001Ý©¨|àf§÷

¡v; Ýí®\¶àØrÍs|&×cwK5èæL#xà¹\x0019#Fåá-¸^ Ø\x0002º¾\x001dªývàs*ß{êÅG\x001aÌS¶\x0005:q\x000eísÀ5CÔf\x001a_d`î\x001duvj·z\x001bèú uÇA\x000bìH %\x000fäYcs»ÇäìÀfÐµS
íNiÄÇ\x001d\x00058eBk¬áÕ\x000fnxy\x000bh[¿CÛþ\x000e­dÆTì ¦ \x001c»\x0001\x0019ô<=í&ÐõõhÏÝ\x0001\x0016\x0007Ç&Ê*Yåòò\x0005\x0012
 ]}=\ûõ0sþ8Û\x00104Î¾ônÁ!¦#*Ìí.\x001e¨ö\x0012fCÛrÁBîÜ÷°\x0019³¯o´o¿ÑÚåÆC¶óÌ··Ô´·\x001dríúv§T+&\x0000ÖVqÝÛÈ£Rû9¥¡>çÐqÎb<gÞe¥Íc\x0017X@ÖcVuÛ\x0012íc@H1¿D×y`ìIÝ\x000eY×{O\x0000Æ1]ÃK*
ò?'&;7º
JM\x0011ÜÁûy\x0006Ì9³k\x00178Ï7av5æöG\x0008Ñ&£¢\x0007ªùtÐ!\x000f\x0015ïæ()U\x0019\x0015üµ\x0019´<¢\x0005_Z\x0003GÐÜQ\x001aÃ­ý@Û\x001atsB\x001aÄH«\x000cÓYl~·ÀPÕ½\x001cª½CÜ¶U@\x001bn\x0017µn¾o\x0003hSë\x000eÓ¬;d\x0010¼à&Þ\x0014¦­4fØ
rÝÔÞe ½Í®\x001cêC\x0003d/ÝïB×]ÕÙ^\x001e\x0011¥Z\x0008Ys(.VX\x001dvÃ\»IªÝMBÎ\x0013¦d5D\x0003\x001d1ëÌ)»Ë¡êÌ®jÏìÊ\x0018Ë:f ä\x0015 `çøíäÑÍk7Iµ»Ix¡
sË¸YgÎI³[\x001f¦
µý\x000eÍö[ºÜÐÔP4gY\x0002c¨µ\x001fèÚ\x0016¶×À£ëÉ)%å5±DÐÌ~oÝËSÒuÂQ·'\x001c%®ðb\x0012.EE!#ó9/m\×t{MHb\x001d¨xqCVRÑÚ°Gjö\x000b±t}9tÇå\x0010k³ÑGä\x001b½°\x0004Úï1µwgÚ½»ß\x0013t}Òæ«8iéÃ\x000foV
ß6
=¶T¥\x001aÜØ&\x00019Q:¿g[pXQxxÝ\x001cÒê<{l}Î\x001d÷9ìV
\x0007i~x÷´:ô®£\x0010ÇÇ
¬øÊ:Ün\x0005üxI®^ÖÓV s/¹P\x000b\x001c$âòºýZ5n,k5ã!àÓ64í\x0016;gLMØ-c*ÍSÜ¦ýv]¸ ØSÈ3Ý2VwÄýö)îfe"4n\x0003Lçíy*Ëå-çnj|S÷\x000foo\x001f+ííáß´6Æ:Î±>7Æ²y÷f,\x0019(óC5\x000f\x0019ÿ"ÏC~:¼þùþÓ:´ÑÆpFO\x0008eQÑÊôó`ß\x001c^wþf\x0019'8¡\x0005§Î#¸ÂC\x0011O ÍDjiCî: ª\x0004ª\x000e4pÇ\x000fvÏÓ~ Ì­sý×\x0002Õ%PÝt¢Ø\x0019H\x0000-7÷ÛiþÂM@M	Ô´\x0000\x001dëó8\x0012dó/äôÀ¼\x000e[\x000bÔ@m\x000bP¬d®\x0003È\x000bÄ$å&®\x0004éZ@ú¡%;fÈôf#\x0001?.\x0015Þ\x0001¨/ú\x0016 Áã\x0002Êt 6+¥2Ç¤çÙ\x00044@C\x0003Ð¨Ú9Ø×¸~M\x0011qYÞm3Ù\sl\x001aT½h\x0001*\x0014ö>¥\x0013µ¼JUià$æ»sÖ"­RUòJe%\x001aÔ\x0010R/C>Ó=´½¬Ìl±KøñÝH}?¾ÊI]¬Ô½lÑ÷^»\$HÄ\x0013Û\x0019é.÷´Ò÷²EáãZv&!Â+k\x001d-+|µ´¬n\x001dÒJáË\x0016ïM®j¨¡·)\x0001Íõi^ÔM@+¥/[´¾·giq\x0008*
¦"ÑßÈo½ËÇ¯©lÒ¦6÷ÓãðSjgÊu¢ùjí\x0002Îkx²¡ð\x0018ÒÂ³û·7ïo>|<ÜÝ<\x001e.n>ýrw{ó°a\x0008\x0000fÅ]m¼\x0013\x000e×¨Éa³ó×§WW'/O^½>\\x001d.NÞ\\N»þY\x0004(E~\x0011dîFÆ6=*Ð9É½*FM¦:P¥\x0010ª_èÑH !xYx\x000cÓCþ\x0012MB\x001dBèR\x0008½\x00103bØÀ%¼\x0018³S¨c`Y§C\x0008S
aºÀã§n-CR\x0017f\x0006`3íkt\x0008aK!l¿\x0010Ñ\x0010±\x000ccÒG1\x0005\x0011ã]»R\x0006×/\x0003®{JÆ4Þ!
óâ½òü!¦\x0003ç\x000e!|)ï\x0017ÂäUéàÍ\x0011PÃ"ð\x001al3ÉkÒ!C(e\x0008;ÈÇ5±yÛñmâ%\x0019FORp´\x000b£dèÄ\x000eïZdåä}Þ\x0005«y¸×h·ÿ§µ¹î·×ØÔMÁ:YðÉ+¸\x000cìoìde±e¿ÉÆoAÜö¸ÛñøKØÏ de°e¿ÅÆW¡(&\x0005 öìø*²\x0014ÎûTYlÙo²q¿­§ì$\x0018"&DýÄoÛË)÷ºCÊdË\x001dl6ÎßR\x001fôL\x0012dsj\x0008÷¢²Ùr\x0007£­\x001c\x0013v*)Ð-¯TÌ¿v\x0008Q\x0019m¹ÕÌ}\x0004^Óø¶	z´wA?UF[î`µÓ~L\x000e)$uÁøÑ\x001b\x001cpì¢2Ûr\x0007»\x001d\x0003#âuz)7\x0010{f
1Ø\x0019¿·\x0014PÙmØÁn#M;Å\x0014\x001fEü\x0014ìÊÊ°¿±ÊlÃ\x000ef[\x00035ád'5+9-\x0018\x001dòýß6Ôö\x000efÛ\x001c¤j\x0007YS\x001cFL&;¤¨\x000c7ì`¸cG)Zìü¦=¸ºMRèÉ­\x0017\x001dBTv\x001bv°ÛÎ2\x0015/½6ø+\x000b1\x0016ë¢²Û°ÝFG¥@Ø4\x000bÊ&OÉJ^\x0014Ý\x001dì6v'o\x0016cVª[ÏR1Äø\x000cß¢2ÜÐo¸\x0007"\x0002s\x0006<ñ\x0015
\x0015µ¿\x0010á~Ã]ìy\x0007ã2IàOa&k\x001dBTv\x001búí6Òè÷Hë¢ÒR9¶c`!ÊOí\x000b~êÇÃÉ»û»-
$TTp©´\x001aHx\x001bFPëùx\x0017åÉó³ÙÎ\x0017ÿÚ\x0017üÔÛàj\x0001G!3\x0017]oîwQ<k\x001cÈëÖÃU%\Õ\x0008\x0017$c|@kÀ[®\x0004½¸és-\]ÂÕ­p
7p9Ì£\x0012q«å-pñ-.­V]\x000b×pM#\Yá2é9pE,,E¬kK¸¶\x0011®òä\x0015;­Ø\x0013ó^åÃ]è[Öh]#Zwý8\x001d4íúáò}Ïv¯EëK´¾õ*\x0004N<;e3É~\x001e¼WaiÍýZ¸¡\x001b\x001aá\x001a`¯ÜE|DN\x0011\x0004³¼\x0005cvº\x000bP.´\x001eo"(C@hÓñr²&aÕxU¥ÇT«"AoX!£f°ù­í¤Èt¥\x0019t³jP\FÅ\x000bÌm|V¼;¯\x0011â\x0015­Âó89öJjæ~ç¾C\x000c+wÂ[Ý_Ózgþ°cr4ÃÙkLH¬+ÿ¡¢}G®.äß~ñóÍûÛ\x000fØpq\x001f}ËW7Vî<Á5qt½æíX00
GÐ\x0012\x0017\x0003N\x0005½/¾;yyú
\x001b\x0014.Î£[ùêäÍÜÎÜ\x0012yü­\x001d¹¢U\x0006\x001e7ÓÓ´#.ÂV4\x0014M°u\x0005[÷Àö\x0015±%Ìs/uR\x001a|/´\x0001¹ÔÕUÁ_; Ë¡N9\p\x001f¨}\x0011b<Å~æôW\x000bôpxÃÍÐ1@\x0005#'fKã\x0012_pã¸
È¡Xa\x0017\x000f½
íÈ-\x0013L9ã2Pæ[	nruo\x000br¨.:þÚÜ\x000c±HÎÝØ`uví$v\x000btUCW]Ð8\x000cÎ\x000cHÀ\x001earwã&àB>°å\x0010a¿`où9~wýîözí
Vd~HörØøì¸Å4\x0014Sªüe\x0004{LÐñã\x0017§Çs&S>
´å\x0010h7£®\x0013=M¯@i¾©äR\x000bfUbV\x001d!nNÄÌ
}À¨NöD­KÔº\x00075\x001cùd4ã¤ð\x0005;&³.R%-¨MÚt v!{VãÈÚÚðày°ùÇ\x0016Ø¶m;`ã{È-£ö9k0\x0019Ù¶ v%j×\x001aI\x000cÝ\x0018SS-v,0ì=ï/aû\x001eØb<l\x001cUÆs`>õh\x001dJØ¡\x001dvÀ±y=¦R§½\x00119 SM`
°\x000bîY\x001a§Úq[(¤H\x001apKËORLvU´à®íc\x000cc\x000b"¤ä\x0018âf\x0005\x0008ÅÖ\x0016Ü\x001d&2`!Ö"Äð&2äxýw´ì²²²ÇL\x0006ËdCÎpÇlÔ&&+A¿£ê=2jAâ)¶èt+ÆÍë>¬Þ\x0013we)e©\x000cÊs\x000f CªâtÞ&÷\x0006Ü\x000b³\x001fîÊTÊ\x001e[9Î\x0017cæD±t<o\x0016åÚÑêÈÊXÊ\x000ek\x0019"XÆ-4/\x001dÚI\x000fNö4µà®¬¥ì0ñ\x001e0¯S\x0008\x000eý×=QWÆRöXKì£ÅAAò\x0004ÉûþÂdv¸\x00016TF\x0007ºNfj·ÖfØBç­;Þm¨t7tèî 3Ï+.8å7\x0019\x000cÛ\x001c;YëhÁ]é@è	\x00170 ãtÌãÞvÂ­'©\x0004\x001bp«Ê§R=>\x0018&¬ÓyK\x001aV:I[¼\×Ô»ºÞªçzGÜDk\x0011\x000fm\x000eÎd37Ä$ÅV\x000bîÊ§R=ii[â\x001fÅÖÑåó,·à®3\x000f=>\x000f#\x0017§o1Ôá\x0002¯×ô\x0016-¸+JõøT>'\x001f¬VÔ¼a<ë\x0013³ëyW¾êñM\&\x0016Gî\x0013M¾`&ëÞ°·\x0005¶TO\XÜ9Uo§þöúáfeMGðN@gcàÀË|uNóe2¶o/O\x0016áj(ájh\x0004ò7=\x0000^M\x0000þÈF¼ã\x001bÄ[¯¹Ù7ÞdN6D#ÉZEÎ\x000eO·amÃ+ÇÌðp\x001djë-ó}\x0010!¯\x001f£uXA´
¯¬Î÷Éª·
xã£û Çv½`Öµ 'ç±6âÍ
z	/V¼6¸á\x001e9\x001d²Ik\x0015àQ­
k¾å-Çå¬Ap\x001f\x000b¼\x001f9\x0015û°Ö\x0001v5`×
Xcý(%@ØÉ}>áNÕõ\x0013
Ü¨\x0015òîö¹gÖñH\x0010+¸¾Öá­n}rÑPxò½¢\x000c\x00138uÌ0m\x0004l*!M«Ñ°{õ­\x0017Ä BÙ,ÉÁVÀõ\x00156ÍWXrñÜFýFÝ!ñÍq\x0018\x0018Vì÷^\x0005ØÖJÂ¶*	«¸cÚFì´øÝyàÕËt¿ëàÖJØ¶*á\x0018[Ó}À9õ&ø¼hÓ¯XÄ´
ï¸ýeÀ[oÙ7/q°ñ¤ivÚyn¦À¼\x000fÞú|]óùªl3b|ÊÍ\x001f>ß_¿bmó*À^T½h\x0004l|¶\x0019*f\x0000ì¸Û¯Ù8±
p¨\x0001VÀT\x0006sD;*ãÿ\x0011\ç\x0006Û\x0000WÕpUë\x0018óZ\x0006¸»Ô¹¼\x0013{\x0005'ä:¼µkvÛâ!ZkdÞjër\x0016n\x001fýP6ÿ(ÚàÊ¼r<"Ô¼îx9\x001d´\x0011oí´C³Ó®î¤\x0014'\x0007^Àår£·rû\x0000P\x0003fÀúZ\x0008­\x0002^7a½çc[WUêáÉVÇ
xE\x001e06¾7òx2\x0017uØ)+\x0016:&¼­QgåÍÏçksÑÒ¬Xç¸\x000e0Ô[]Jìá&Õa¾\x0010ÌÛàÍ»«\x0000ëúuó	Ë\x0002§
9\x0015¸Ó	×Q\x00064G\x0019c}Òâ(\x001bé\x0008\x001dr.m²o`#`S¿9ó¥¿9£k¼­açï·6r¦ÕÈ)Ë©?+
o#Âåq|!&»[7\x0002¶õ°­\x0017B\x0019æ§±2olt:\x0017óÔN/ÎUQ'¸æ¨\x0013rjÊË¼Á \4Ý+\x000b~¤xg?íº
3²º\x0013Qºw¸)'yÂ
ìß|kÌx\x001b1ãÃsôð\x000c\x0016Äèáñ\x0012\x0000<ñTñ\x0013Ìºù\x0005O
xK8!9¨ýNO\x000foÆÛ§7ãmcd²Ë&\x0014ñ½Â°®b¤	eÌ UÝ\x001dÿâYe/ï\x001fopf{%fëòÌ \x000eÒ§\x0016\x00183ÕÊôàù\x0008ùòüê\x0004§µWà\x00127ôàö·\x0000\x000fd\x000c©Î(\x0003d¦\x0015ñÝ\x0006àª\x0004®º\x000eÜòÔ£B7ÎÑóüâÁ\x0006Øº­{`\x0007A\x0004OÞb<lö]tÛÚ¨M×aKæV¸ÙÒaçÍ>aE-l\x0003p[\x0002·]×Ûe¶ÄÄNÌ°MuGà®\x0004îºN\x001c8ñ\x001cò4/\x0011O	×,\x0006Þ\x0000ÜÀ}×k&¦Aàî¸÷yÀ²îÞ;¸C\x000fn\x001b¸í\x000c\x000bëõÈ»\x001aVÓ×\x0003/HñÑò®\x0013\x0017\x0019÷\x000cÆ\x0013çE°z\x001b+ðÚdvÙL;.\x001cq¢ç#'Ü+\©
°+)»L¦Ë­9Z2?K<ov\x0002­l\x001bÞ\<\x001bQû(\x0017÷\x001f×6ÄÌåP¢IZÏä!>¬X&}q~õz\x0005`(\x0001C+`íx="4¦ñ!'\x001aÃu°+\x0001«\x0012°j>á±=À
tiì~,UÊå\x000b½\x0012°.\x0001ëæ\x0013Î\x001eõ@× \x0007+òJ+\x0001\x0012°i>aÓ\x0008ñùíxÀ»áµ%^Û|À\x001a\ð|\x001d¯ÏÕ\x0015¥ëp]	×5\x001f¯b'o8^\x001aYwÚäó]6$+\x0001û\x0012°o>_ÅÛ6ðYEÅà0ÉÒ¹\x00150Ô:­Y©)3£1Ú\x0012Øeî\x000819¹±\x0019qõä ùÍAÞ\x0013byO\x00088ån½®\x0004Tw\x0018/1¢#XÍÔ\x001c2ì\x000eWÕ6£ÙhD\x0007ËÎ¼\x001c¼Û\x0015©ò%Ä ø\x00111¸~Äéû_®\x001f\x001f\x0019ôÕÍíÝÝÍÇµÀ\x0007bZ\x001a¦4w:Ác\x001aÆ»)à§//¯®\x0018üÕÉéÙÙÉë5\x0002@)\x0000t
\x0000s¤\x0000ËtðÛgíÐ¹¯\x0000ª\x0014@õ~\x0001!½Ni)#²d&¹.ñë\x0012¿îý\x0000aØ¢>\x0000d\x000eø<<\x000bÙ_Ú'\x0013¦ñ/Êõ^/¯úpw{½òÍºÌ¿àbèZó!ä5XA{³o\x000e/¿}u~vz¼X\x0012±
­ª>éE/\x000c§Ú\x0004¦\x0010ór
bPO£\x0015%þ¹ÿôðnKîÉ\x001c\x0002QF Îd«Á\x001brþæòÅÜõVOã\x0016%þ~Ù\x0002}¤\x0018öBæä¤O\x0013±+õÊJÔªDý[¥²\x0005u\x0010\Ê÷:ÏÊ\x0000-RÂ\x0003¼&mÐu	ý·úd\x0013tÇ+A}Ãh¬
p/AllmnJè¦ï\x0007.ïãR6ú§®k2NhnKè¶\x0007º¹×*ºäo)Ð¡É$e\x001btWBw}\x0017FqðKû\x0018º´ÌÏe&]Å6è¾î»N\x001d\x0013\x0010µ\x0013HZ:@7ÉþHd_[éz­\x001eJè¡÷Ôù®[ÞÓ\x0011OÝ\x0005>õÉ:u\x0013ôrõhâÂè8v$ûKÐ$@À9VÉ6äµ\x001dí2¤H\x0012 øÂ(æ1\x0002£ì\x0017iÃ^\x0019RÙeI0"f¤k`íè\x0019\x0000ýdv»
{eNe=Efìi\x0000c\x0003vëIÇLÒpnC.\x000cÔ\x0017na(\x0018¼_ü|ýáãÍÃÍÝjËqµ:n?É÷Åñf#Xh²¿:¼øîøÕëË³yZNB\x000e%rèAnpy\x001fq§Gc*Ó+\x0015DüïÜ§Û «\x0012ºên1¦J¼¹Æ*ó~2¹PVØ
]ÐõW\x0005ÝÐM×U×Ìµ\x001f£	¦\x00017VNR\x0000¶\x0001·%pÛuæÀ«\x0011\x0005e_âóq/oCíJÔ®ï¸5çÁej&°¡ÃÂ<ÌVè¾î»\x000e\x001c\x0007\x000bK®Ì=ñï\x000b=ÐC×©{£s©ÉÒTÄÎ«=\x0014ìª\x0015\x000b
24E¢ëØãý6´$:ê@ÇnÔ¨[v½ì²6£}vÔç\x0002¸¤Ø\x0006:w®X\x0019»Ðj¾\x0015{eHe%ÅØNñu·Dëª g\x0017\x0017[WÆHvY#\x0007<\x0007\x000f6dùh\\x0018ÓÞ
½2F²Ï\x001a\x0005Í­\x0005j`\x0019\x001fî\x000bd;jw¾ë9]ö\x00085»\x001d]\x0005ÒìÕã$	\\x001böÊ(É.«äqóeîLCÆJY\x001e\x001a3J/\x0011üo^\x0019%Ùe<¯	©	<©|ÛarV\x001böÊ*É.³ä5p\x0017|`\x001b5®öSûZT¨Ì\x0012t%\x0017ÄÉÇN\x001e¯ÊÚqçSÊ(AQò^ wE:uË7F+^ÒdÔ¾!\x0012ÔÑ]QòR2ë\x0017 {\x0008\x001d{,^~Ü\x0006½î +¼\x001bø©?\Pµ+:ïvÕ\x000bé­È+{
]öÔëLÛ>;ÕaT¦\x00114°Ð\x0019¹\x0015{e Ë*y\x0017\x000fá.5¢SÁeg`aÈd+öJµCj÷\x0018e°EuìùjÉØ¸¼cGèªÒªK;z§Ì\x001bY\x00053cæÞ	\x0001Ué\x0018Õ§c°YeGYßÇ§*\x0017&·b¯ªê{ªQ¡SM}X\x0014¯Ål\»ëSUÕSU}OÕÛ¼\x0015gØ\x000cc\x000f'ë¨ª§ªújÄNS\x0008Wë¼\x000b~zOM\x0013v]½UÝ÷Vã}§\x0018U\x0000±Z)ì]dË´¸=l\x001bôê©êÎ§ªò¬\x0014KCÈ
ìªÛu0í{¨Q+JFnó¶\x0003ÈÐ\x0017Zo·B¯Þ©î{§Fñ¸b:M\x0015Y \x0014Û
¼z¤ºïêLµ¹^ö\x00052ù1vWïÑTÔô=Rb"TBqé1\x0002çøTO.dj´¦?¼½}|bQñoú\x0014$äp	XÉlSÝNîïÓ.$¡ÆOç·7+W\x0003aC	Ï ZîÔÅþ\x0000æÏf¼9<?=Û	ô´åH¨qTb\x000bN\ÌÀý¹H\x0005ÓtÜòêÔl¶k-PU\x0002U-@¥\x001aÜ\x0002±X(Pc÷þü éZ º\x0004ªN4p_%\x000e(9\x0006?ý.\x001fÞ0M\x000bLì\x0002ÉlÔa\x0006k@AÎW®Öâ´%NÛ3'y"ÑSËöyg>¹¶\x0016¨+º\x0016 Èù@[\x0015ÈßÝæ­!\x000bÙ¨µ@}	Ô7\x0001µySÌLó1DdZ¤>ß\x00044@C\x000bP­yQ¦Îy\x0003pãZÏ=4SQk¢\x0016\x00069Âqaª§Ôµ7y£çBwì: µMj1JÎÄÆã¸j\x0002\x001aò¦ß=Þ¼¬l²JVçÄVp\x001b\x0012:ï\x0004l®ß´Rö²IÛ»ü9\x0003R§¹qT\x0001ï?\x0008nÂu-ÒJßË&\x001f\x0003zÞ¡\x001dãcÊK(éÆå»i¥ñeÊ\x001f;û]ÐÈÛÃ(\x001bäç9GÖ"­T¾lÒùhèLSóóTñ(/®¿Ø\x0003i¥Je.õÂ3¯¾9¬¬æ\x001e¾é]\«Ê§£°Faï?}LNÿÉÇë\x000f?­]L²Ì\x0000¦xB"SûÌÌÒ¿y\x001cþ×Ç¯¾ãÒ:Z*i´´\x00151Á\x0005\x001cîHx\x0005OaéiÒÞ­xeWv\x0000\x0016XV*Þ¢\x001e$q¼N±nÅ<ÎæIÍkÃl\x001dË'b\x001fÁë£«Êç<MÎ¹\x0015²ª/rûMitÆ`qÞ0d~RClÅldue;fÃ\x0015¾¨×<Oûðë\x0013ûÝæÐ\x000e!ëvÈ#U½Ì¼ÎA¸L¸6mÜ¶b.³q¸Û6c6\ÑC\x0012>bv\x000eÙõ±_y7ÈÕ\x0003´\x001d\x000fÐò±¨+âÕP\x000cÙO\x001a­CuCÇev|3ò¼6$B&W\x0012'}wÂ,kë7ìQn\x0005M\x000c\x000ePÓÝÈ
wÎLÓ\x000em\x0005-«\x001eúÛA+\x0002-=/ä\x0008¼¶\x0018%í¥éä\x0013#Øa\x0005#fÍ5S\x0016§Y¶b.6\x001a\x0008ÞhÐY³IÑD
\x0011\x0015\x001d3\x0008Êéxc#â¢Z0Euó)ÓØL\x0019\x0010j\x001aÕµÓIÆ ¬,í&\x0005G\x0017r}P;»ínOPÕþêp¼çfWÌô[\x001aÔUc]h:Âß
ZUo\x0010m\x0006õ\x0006\x0004½g{ºõôtñVÐ\x0005¿+\x001eø]\x001bA«²]Qs[¢Áìå$é1üCÐzÿÚ@\x0007Ëç eÖvÛ°õu/Ð¾º\x001eøk#h#äM×Cê\x0018nÓIç~
-Õ^\x001aO\x001atè\x0002M½7\x0011^ö:4{\x001dZLn!Ý
ÚÔ\x000fÑ´?D#\x000c_\x000f«%HMkæÃQvz¸b+èú¤MÇIÇLK¯\x0005&¶)&4¬òÔL«ÐFÐÖU&\x001cm\x0006
á²Áøl\x0010
óøÀäB÷Í½¯0cõ©\x0015sÔx	²\x0006"ÛÃs¦|\x0001¨iîÑíZº /&=}Ý¬¨§!\x0006\D4\x0013áæ¦~¯\x0014¤ý¡Z¡uÞ´B0\x001f\x0006|ã\x000f?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=Y^<×N:\x0011ª"c\x000fÌ/ÓÍAv8
ÓrsM\x0004IP¹­Ò&B]É°n{\x0010¡N¹n\x0000(púo\x0000Ì3\x0008 ø~\x0004PO7\x001d\x0000F(\x001aÆj@\x001bû+Í\x0004¨µ¯ù|34Øë¡h¦/¸§X:O\x001b ´ª"´ªÐpÊk¶aº \x0010"\x000f×ÑÛ¥\x001fm¶&´­\x0002zÜ`Ân-Á8Rùh,èæãFT$~n\x0003tJH\x000c]åTØ/HrOÁ	\x001a@f§E[\x0008\x0010Ãÿb-á\x001fil¢\x0015Ã\x0017@§¼Ø*;\x000cÉÍaY?\x000c/nÖ¿]?ÌÞ_ÿt\x001bpöfç`\x0000ÀÐ0°¿ÑÍ|;dqºü÷ËÙûwgá/\x0011êP7\x0013\x0006ÿAùD\x0008\x0019\x0018	ÐÒ'ùVÞV\x001b­ùl3_æC\x0011êÅèdnªª·\x0013\x000f\x0008MMh:\x0008\x00150ñ51k(\x0016'Pf²\x0010~ÐÕ®}=n\x0013xa¦®ª°\x0010òÓF\x0008]Ñ6\x0010º¢3í©x0Û2U©Ç%F\x0001re·\x001eÅÛðT§Zñ\x0017ç±5ÅßÆ\x0019\x0019\x0012ïÈ~=P2öCx\x001e¾\x0011\x0013Ïon~ÿÇzv\x001a¬àíì»§ÛõÍÞÛ³WÓë¡\x0017ijun</p><p>Þ\x0016üÅéér9;]Í¾ûx¶<}	O¾\x0002ÁÇ\x00164ëä\`<'¨vÁÒÓÅÞ¹­l¶\x0012\x001a·mb³0\x001a\x000eP´ãé\x0001Nf6ÓÍV¶¶	l±µM\x000b\x001bw±Ãu¬ÁF¤§ÜT\x0018«ÔÍ¦mÅ\x0006É\x001b-lLPS	èO\x001azZS[&fµ²Í´±\x0019;¥\x0004yG¯Á_¦Ç+kûõ­\x0018$\x001bÙàu MåENs`cùù¼`ÜÎVËÍ6ÊM\x001bl\x001a\x001dË(PnÊÑ@@©Ë9\x000e\x0007³ñÍ,\x000e²8ÞÜ=Ý¬ÿººÿ2[>|½»]?îµ¼\\x0019ªü\x000bIjZ© ~Û¦ððÞ<]~Z\¼-/ß-¯^$+ÚáÂólB\x0013\x001aÍnÜ °]*G×N¹"g®\x0017ý\x000ccð7¡aÿÌ8õÂP\x0015¢vÔÁ:\x001c\x0013Cl²fk\x0013ÒTÈ\x0005\x0001\x0017lp<
\x001a(âUídÓÌÓH\x0006\x0006¼\x000cÆ'csceS\x0001\x0014´EÍÝ;\x0017m6ýfncN*{½]}}n\x0010uØ¤\x0012]a§ÇÇx.ºÂfg_òT\x0001\x0017~-Þ?;N\x000c9MÉiz8¡\x0013¤È.»Fåtç1ê\x00150]%N×%O\x0002Ï3\x000f×¼\x0001ä4ÛI¯­eð4pÆài3hÐÀ9®»ÉÓZå$PåÆ\x0005*¦\x001er	Tõ2éüð´8§i@Ô\x0002TJ³sR\x001b¨«\x0014T¸\x000e\x0015Õ0ãÄ¢HpEÒQÉò­w»F·\x0019T</p><p>T½\x0004Ì5^Ýtn«4õ¼\x0016rGÂp3i½Tßnb\x000cSW!xE\x0017ue¨ý°`»çN\x001cH*\x0005«­høFaEß¯îzZß_?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<link href="https://unpkg.com/template.data.gouv.fr@1.2.1/dist/main.min.css" rel="stylesheet"/>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
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

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://stats.data.gouv.fr/piwik.js`
  
  
  * Evidence: `<script defer="" async="" src="https://stats.data.gouv.fr/piwik.js"></script>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch`
  
  
  * Evidence: `<script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=Array.prototype.includes,modernizr:es6string,modernizr:es6array,Promise,fetch"></script>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure JavaScript source files are loaded from only trusted sources, and the sources can't be controlled by end users of the application.</p>
  
### Reference
* 

  
#### CWE Id : 829
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/](https://adresse.data.gouv.fr/data/ban/export-api-gestion/latest/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales](https://adresse.data.gouv.fr/bases-locales)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 11
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Next.js`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `X-Powered-By: Express`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
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

  
  
  
  
### Strict-Transport-Security Header Not Set
##### Low (High)
  
  
  
  
#### Description
<p>HTTP Strict Transport Security (HSTS) is a web security policy mechanism whereby a web server declares that complying user agents (such as a web browser) are to interact with it using only secure HTTPS connections (i.e. HTTP layered over TLS/SSL). HSTS is an IETF standards track protocol and is specified in RFC 6797.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/cgu](https://adresse.data.gouv.fr/cgu)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf](https://adresse.data.gouv.fr/data/docs/communes-operateurs-obligations-adresse.pdf)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-5rxPdPnn3xSQ1T0Q8BwzciPJ73c`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-+wPQTnR+OulO1Xln9EnU1DHHs3I`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8115-6KTeliCYEoDHqZKs4yeDWa0w8Pk`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-/YmNnMsCnKQDN5vStff4qRiH1CU`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-gxl9fRm+lkzG1o0kGZgGnMyi2rE`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `95ba-11MHKgmDzLWNLMDFq02ggz73Clo`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-lWzskkVBBj7jqyYkAI5Y7nn1ros`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-E8Oy+RiO4kKRp+entqRCgPJkyEs`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-MutZDW51uMJKvur7DjzBHYC8FSI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-+wPQTnR+OulO1Xln9EnU1DHHs3I`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��\x001f���=��|RCT�C�p�ȏ'��</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{},"isSafariBrowser":false,"__N_SSP":true},"page":"/bas", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `<noscript data-n-css=""></noscript>`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-store`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `302`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
Instances: 8
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `366405469`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1611761132`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `273111588`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1439655420`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1919628686`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `912784966`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1838188997`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `831362559`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `1745640841`
  
  
  
  
Instances: 9
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>366405469, which evaluates to: 1981-08-11 19:17:49</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
