
# ZAP Scanning Report

Generated on Wed, 21 Jul 2021 08:54:09


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
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/gerer-mes-adresses](https://adresse.data.gouv.fr/gerer-mes-adresses)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://mes-adresses.data.gouv.fr/new" class="button large primary" target="_blank" rel="noreferrer">Créer votre Base Adresse Locale <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" style="vertical-align:bottom;margin-left:3px"><path d="M17 3a2.828 2.828 0 1 1 4 4L7.5 20.5 2 22l1.5-5.5L17 3z"></path></svg></a>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://blog.geo.data.gouv.fr/de-la-commune-au-d%C3%A9partement-la-collaboration-sur-les-adresses-dans-le-gers-c0d83fb20950" target="_blank" rel="noreferrer" class="jsx-2674135937 jsx-4023173407">Lire le témoignage</a>`
  
  
  
  
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
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-03.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#rIFq`
  
  
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-09.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ÙZºè°dÝ\x0017ÌW%\x000b3Ø¯\x0004K¾ÖÁ	°è'\x0014:Èk£ ÌIT0½\x0014i¿ÿeùå·Ëkó{\x0011\x000c3¬_\x001c=½¿{øóêóçí\x0011[ð<ì}\x000eT6ù\x0004Ðjð|¿xó·×¯O¶Pòw0ò_!èÙ0\x000c¹Ëe­uÕ¡\x0019ãø59?
d¯<4yÊÏ<$KHÄr$íZ\x0007ó\x001c\x000bd '\x0017p%Û<,Sn\x0019\x000bo~ÊXt_*\x0015ÄrY°\ÎK$÷ª¬s®y´Óíý\x0010ñö",ÅÃ
j¶\\x000e~[~þý\x001fÎmôxá«áyvqûöÃöÀ>V\x0013ÉGBk¾³\x001fF\x000cé\x0019£érqÏ?ýË,\x0004Y©¹Y\x0008²ËY	q1³íß *"7È\x0008bX\x0000#½Y\x0008ò­Ô\x0004 RQ$D"±\x000cÞ*¿ìû\x0019vw\x0006sâÚkì\x001c(\x0008\x0002Íð\x0006\ë¼\x000cAv;ã,\x0004Þ>\x0004À°ã\x001b|à#°\x0016\x0001°¥ë>_Eüÿfàp@PÀ­\x001dª:Bùß¦v\x0017\x0000È/oÿñÉ¼§>\x0005ìN8¾ù\x0005wï²i¸£>J\x001c\x001a©!N!Ò{08>{ËÌwY³Í÷1ü÷}(õ~ü>n2§D\x001bñÜã~\x0000\x001fÿáÝ' vÓÒdúôîáöÝÝÃÖï[(\x0013\x001c4²ÛT}`¢á»¨Í&\x0008zúâÍóï^l\x001bÔî>\x0010þÙûùAäo\x001c/@5Åï\x0007É.Á×3dü³ÿ/¯ø\x0019d?+ÑÇC»}zpÿuÜ_ö~ÝûÒUQ>°1\x001c?o±¾MKþò¸â"ÍùËãÈ0Þ\x001aÌÃÏC³\x00040p-\x0005²GZ\x0008¼z\x00173\x000eßí·E\x0000<g\x0003¦¥:y~y\x0016ËôÇûÈSøeöþéÅýÝÍö\x0000Ô:.j\x0003Ü\x001cMïômµqf\x001e¿Ø¶ëjðe]n}¹öÿóÆ+_îüÎOgÍÂFÜ·FÙeÕLK\x0003ó?÷Û8°]~ö|;ZRuåÛßU¸B¾=0{»¿mì½«íCè+ÄR\x0005ýÍÃýÕûÛ»íÚ\x0016Ý)*°dÉ\x0007ÚY\x001dØ\x0005S!
|ãWÙà¼9?ùáùí*w\x0000\x0005­o
E\x0001¹A\x0019ãgb&ÉPú<\x0017CÉi6\x0014k[Ù)x¤ø`Tè
Äs ¼³þüeH®pvñÛõÎâ¬2íbªD^a\x0014hOHp¸\haÔ+µíëå%½ß7Hû\x0014ªO¼Hÿ7]§Jýþ¿}utuö
¹ÒÊÎ"\x0010^q¯\x001ff$÷¸3\x0017\x0017h\x000bÇ¶Nnß_Ý¼Øúu\x00177öÈ·2½sM\x001d\x000f\x001dãç??;ñuÒÂ?{?Ó6¦¹åu|
\x001aéeö\x0005}Xòy¼\x0001zÆç³ÿIÕ'\x000cKt
\x000bnÖØ\x000cò¡ÏÃ7e kÿßÞQ)¼xÂ${Þ\x0012yXòõ¬ÌñÏÞ¯\x0003\x0010\x0015*\x0006Ç\x000c¶A·l`\x0004GÃ`g|Þl\x001c\x001c\x0011P­×F®Áx£\x001c={Bû>ï³÷¥(\x001eÃ5¬Õ\x001e{Îk1ø/_\x001c!lgßû÷o\x001bè0\x001f@ýµàkwoàKN¿ 0s\x0010dkt;\x0001*\x001a\x0000À|\x0019Ü~øíýÇÅ\x000eå»\x0017kÖÙÃGL/Þo×~.\x001aZ{äq3p )8"
:ö½zgoavñ|»\x001d\x0018\x0000Éè£	\x0004÷èÄY*ªÉy`{XÚ÷&Ì\x0008I45i4C(ÁZÊX×6\x000bÅrE^w
Cs°ü©~ºÖ\x001fqDwUÑà«O¿>\ïÊ\x0018$*\x0017\x0005léK7ÊRq\x0004e»¼ÑËWÿëÍé,\x0014ØÈ¦Â<\x0014Ø0D(òõõdåk\x001a·ËP\x0014+¥Õ<\x0014:a"rÌ\x001c\x0014gò¡\x0004Å»ÛZ.\x001dliÁ??Ü=üùÇöòDÂïqv+ROeÖÜ3Â\x000f/Þüí?ç|\x001a³WaÆ§[\x0003\x001dD.[ÅÖ\x0014$ÿl¾½øgßgCS
ÙQÓíËÜ\x0018åÂOg{ö\x000b[éövÿÎ þrÌ÷\x000cÿìÿ²wíË«±5é
þÌOïò³çÛÆÒêQõ^]}Óìg\x0017É/økcò>ÿÅ/çÈÜÐ×\x0003+M}\x0014æK¾~Q¾~±÷ë\x0008Gó×iY'~µ¿}ÍùãÃÍÇA\x0014ôüâáíÍÅ;úî\x0002µû\x0014 \x0005\x0000@[,õNÙçÇo\x001dÿm»^\x0019|¾¦C÷~\x001e·yþ¾Å\x0012y	Ñ\x0007éA¢}ùÝ|Sbû\x0001\x0000S ú\x0014SÝ|Å+Ç
)!Úe\x0002ÀÃÇîÇý\x0010|¢\x0019ã\x0018e-OÍÁå@(e4=\x0007
@4Æ>\x0007 Ì×\x00118æ#HîçÏ7Ë\x000bÈW ¶¦ý\x001dq(ú£»?u¥öË¡kÍvÜ´¿#\x000e\x001d|ã
îû>u%Õ~qú¾jþñã¡ß\x001fú^{ 8Õl,XNVá\x0003i
p<7°\x0003ÃÕ¯\x001f~ÅÛAý«hzéâúí]Î\x001fø@Ñ9ðOO¨=Ês²Î$Ý7î\x001f>ýË.×ï'°oC©]"xüs|u}û~kÉ\x0012[s\x0014»ä\x0006¸t4ü\x001cu\x0018¤¨ÏONÿ0ãã\êßýñü
\áó*EþM\x000f²qËüÀßþt­~-\x001bØÙoÞîÊVfg*\x0015O|ø¹òqÎß\x001a³ýñÙîtåÏï?ù;UR¥h\x0007 ä£²Æ¬l°ÛÄ§¦Lplý=\x000cËÇ¯^\x0017þ×­\x0017ðç·Yå2bGçW\x001f¯?ínG·M\x000bpS*4\x001fÀöµóóg§¯¶\x000f0n ´¶3 d{\x0003mf#%\x001eT°:\x0019¾\x0003z\x0011\x0004$Õ(?û¥e\x001a³Ñ\x0004ê$Ú6MàÒ2\x000c%5\x0004s0à\x001a<êWóÑ·IFhOA\x0018P\x001ds\x0014!^\x0012ºÒ~SÚ\x0017\x0012WËT\x001cF={1\x0018ûÎþê\x000b\x0006LRAÉR\x0015:çë«í©j$°nS»¯>±<Y\x001cæÉ
óéÉ«­(þ¸\x0005ûá§Ò7/)\x0017âÝýõï;ÓRUè«\x0004¶,BªÉ\x0014¾;?ý­\x001fÿ\x0019Ì/oUÿñ~ª´tÛòtæ\x00124®·ç4\x001d\x001b¥®X{vüý÷ÈI·íë6þüP¸òJzþóòj»Slâ[{<êtc\x000c\x0003ÇôåÉÎø*¾>ü³ó«Ñ/×FôÁ¨\x001f8\x00023¿õ\x0005þÙõU«ó*?~þªiS\x0010n0´8ó³èÃ¾ÏZ\x001e\x0015
´Â4ÕB\x001bü\x0018¤g~5	þÙýÕÄ\x001dàAW>yüjl×3ó«Ìá¼ë«àÈÃ-¥lZ/\x001bÆ3?¯\x0002þÙùÙü_îx\x001aÖqÍÛ\x0014æî:ê\x0000â\x000b}\x0010ü³ó³F\x0015Þ·rCû¬×m¼c`Æf~èªw\x000b¹L\x001c×rÝmâ¿m\x0008â¿m¾ø°GUX\x0013éFe?c#cÕ¦9ôF%,`íûªuÜIª"ÒWë ß'+ûjIâÅPÍm^-5qhÓÞO÷Ùüÿ¹âJ\x0013çÿþmþÿÊÖ¸Û£×ÿ¸ÛÕCäZ?\x0001NTÒ¹jÞAvä¥«£§}±£¨Añ\x001d\x0014?\x000foãÞÇ[36Kd¼\x0004V©ø¬`G,þ#ú+¯¯ï¯¾»ºÙ×d\x0016-<¼%]Ë<¼\x0010õ iÜõ]¾>=G³}Ýf\x0018\x000f\x00196"t!X4|[\x0008i\x0006&"\x0003{µé¡\x000fNÊ<\x0015Ú)f¿\x0005oc>Åïoîî¯nwÍ«BO^M mmÌçØFc²Wì\x0007ùýÙóìnmw÷\x001aØÁ3ánL&èÿR*tà\x0007\x0004»\x000cNêà¤¹p6MsùrEJG·\x0004ËÐx5DãÕL4:PpÍæ^­Z×@ê·\x00028º£gÂÁXÛ|,%´\x000e|T	\x0016Ý\x001cMÔS\x0006ÿq¦tl\x001b°ó§æ¸Úè\x0005pìßy\x0017þx¯
»»½::ÎqË§ÛÂ\x0015öíõû»ûØÑDæh¿ùñâþúæÃU¡	1a·#t¡V²e-Ï~H%	r©R\x0004ý%\x0007/{ñüäè8\x00072¯\x001f\x0015\x0002±oOxq¾5Ó3DÉÞØ2(¼\x00022êXëò\x0019e¡oÉ0}%b9\x0008P­}©Làï2¨\x0010J#/qa=°b²¾`Õº&l\x000e5ja\~ø©r©æÃwuWo\x001a*\x001bÂäY	5^ÿòÇÏ\x0018×FìD.?g×W\x000fGß]>:»{¸ÌOæâóvøL+ó¬öÖPöÉã\x0012 zAMd~mxvzòæè»Ó×Gg/Þ|ßÏñ¶	Ý!4\x001c/?2h¦ð}\x0017hÑÖìpVòó\x0005Z¬\x0011Ë
hÊdø+Ã
Å¡b\x000bÄv±9Ý°Ñzh9¶_>ØO?\x000fjI§\x001f¹øôé
©ìUÌ^Æõ\x000b¬\x0019T0>T\x0016*o,vt (ëë^Æé³Ç¯^ ©=þ\x0017\x001fÎÁTûÝE²Ã^¶YèP¦ëµÖ\x0018ý\x0016;a]Ü¿½úe;&ôXñ\x0008T>µè«¬\x000cU\x001e3¨H\Ö{¢]!+tzð\x0008W¬V¬àJ¥

iu\x000fWÅ¬+`¡»D°|a5+°\x0002å\x00043._9¡mPj¡´þ¸¼uîzpÛÏ¯>\x001dÝ\ÑfÁO¨f_^Ýß^<üy}³ã=¦ìYÒ\x00158iSß#¦Ñè=úÔiÚóWG8¹X\x0016
¾BEûòäüùñ¿nKîwPku\x0019Ô/\x00045@ÙZ\x0000BÊû´\x000e´>×Hqb\x0015pY9P \x001a\x001dYÉx@¨u²méù'z6ÞáôtþôqÒ`\x000f\x0008µÀ-
|\x0002ï²¯Uv\x001fyä¦«ÿçáPë¬ÜB¨\x0006P\x0005jöº\x001c½ªè\x001cCM\x0007DZ§ê\x0016"µß¿ÓÝ\x0018ôq\x0014àPëøÝB¨è\x0008òù«\x001aSzlBe¨Ú\x001eòªÖðP=æ òª¶#C-C\x0005ªòîpP9ÌZ.ÖB<U"~"ÖÈXõ\x0001\x00157/Äª\x000bÏU+Ô\x0015\x000b¸ËÐú&×\x0003ÞVîLÿ·ÀJ}ìK­\x0000Ôu\x0011hZC\x000eúÉ
Ðâ´l°Ì\x0001
\x00167½½X¯ßßØ»n8çýý?ÿ»LêmÁ
!.^
ºNgxd^®o\x001eV»óÆ'/ÞLûè\x0003\x0000Õ\x0011\x0003 Ô,.\x0002ðéI
b°"Êß7fÉ÷ij}ï÷q1:vY\x0016©\x000e	xSø\x000eK~\x0001lïõÌ\x0005@Cëû\x0001ä¿aaÌA"ãkjÝC±`E\x0002ÑbK\x0002°÷\x0016¾ò3\x0007\x0005n}Õ\x0015\x0005èÚ\x0018Q¾¨rÆ(¦{\x0004\x0007(BaÞ\x0008³nc>Ò&Ï\x0002G¦BÒJC{=\x000b×Cû@|~g®Ô°Oóìîóu>^Ý½ÍßÞ=Ü¿#nm\x000f7\x001f]¨¡sLaùá*PÕ)²¸Ý¹Ãôâõi</ë¿}ñæü»\x001dd\x000f\x001dÈ\x001ag,\x0001ér<T­!®®¯	=R\x0003Fx\x0005HzÙ\x000b@ÚP÷J"ÈX\x001bn2È\x0008\x0004ÒÿîÃ$Ú\x0005 UD^È\x0002\x0012ç¸+ÆBØW0jw0Ac4e7R\x0018míñ:^ÚÑh·
£
ïo/ï\x0006rüöâæêvG~,!Û\x0015hJ('ºÙ¶9z¸
 {$ß\x001el]«8\x0000\x0010°¦P~öB	Ë\x0015³êQö\x000c-E\x0004YM"Ø¦9bºy÷ám§¸~\x0005	Ì<½¹+?×\x000f\x0017;3Â­¸×ÜiO,/VÙXüÓï°Di§g/ÑÏçõÃñ®|ð\x0006gKR,Â©5\x0007Ô¸­Þ\x0013Ö@î´Å¡½Cmye`]a\x0017A°NÏ+ÃYÛ:¨d[¦b\x0011X«Ë\x000c$Å"~\x0005Mf\x0004Vý¾UX[ªb\x0011VWú³\x0011*Î
V\x001f \x0000-þµ Ü8Wµ
kU\x0017`
	©È¨T¹öò%ÀyÚ
6ôu¡Õ7\x0016{Ì±Å|)Þ¤Ñy(Â
\x001b¼¶\x0018ç\x0017vXuÐ¦\x0012¾fùúßÅÛw\x0003õõ×;\x001c¡Øå§bfYW¨Ðe\x0005òS\x0015)ª\x0000¡/`ýõ\x0005QÌ\x0001P_ù¿\x0010@\x0018þ\x0000jë_\x00073Bÿ2\x0004¥%§üìà5&H\x0011o\x0019¯Ï9û}µ ló7\x0006\x0010ìÓÎ{
±j\x000cÁDN&EK¶³¨\x0000BúüÇ¯¿
©=Êö¬,>\x001d}wõËÝýçÒ¾½
ÆI\x001aÆ#
\x000eåb¢ê­E¾!²"«\x0008T\x0013/_¿>ÙÖ-Ú\x001f7î\x001d\x0000+µùÓÛw\x000fù¯q}usSú±>_\x001c½zx·+Ñ\x0000%Q\ó4þç1ïÂÕy§º\x0013+ÕùÓçß½yõúüôä¬ÔçÏ^\x001f\x001f½zóÝ\x001c¨õ1ý;@åí\x000b¬ÔæýozÃÿ-°\x000e»¾v¬Ô\x0010þoúªÿ\x001d°ò°Ê¿\x0005VZ6òõb½ºúý'\x001b\x0007Vëé«×·è|=ü¹3\x0011\x0001\aFËnS\x0013ÎÆÔ\x001b¶ì£¶§9yvú¼8Üoþ¶+±òá½}ûÑt\x0015£óëßvÄ\x0001ÉàJ%(²RU\x0001Kí!ªMBöèüôÇmãÝ÷)×¹ÿûÆPj3ÒÚrôAyi£]B0C\x0002\¢ø×! ,å¿\x0010\x0001Iþu\x0008¸N²\x0017We\x0002\x0001\x00118Kñ¨5êè.ÿ_ÀÂ«è*#.·ÿaYüþç«KlNÄ\x001bYÏ0<¿¹x¿3Y\x0013t¡vÊ\x001e7¶SOb ïßZ7.ØäPüìøí@Â»WÚ
×½
¯	WïÕÍ>,)RlL¯Í¹#EÅí­Å³Í÷Y»ï\x0007 k\x00158\x0005[mxµ&UïXoüýý"à}\x00173dÛHëÅô.\x0015Úi´%\x0010)ñì_ \x0002¥Ñt\x001cU\x0019éÀ\x0006é\x0018(kg"umyíÂ#`þ9MÏ²±Hâ½Úµå=x\x0016s\x000b\x00000©Å\x000c\x0000D\x0002\x0000GwÀH5¦]}3Ñ?ã\x0006h[\x00161Ú©©-~&úÀ¥\x0007Ó§£g\x0002À4Dùs\x0005\x0015ÕÐ£ËjRÕ6ÒXÆ\x001f\x0011A\x0008&,@8ËÏ3p-H5Z«¤\x0006Y$*\x0000ÛwÌ\x0005-\x0017ø3ç\x0016\x0016æýRÊ¯4Q Ï`\x0004Ê<@÷\x000cuh%°l<\x0001°äSzµè\x0008Ñ¢üÌ\x0000à¨*Xf:L½!yþ¾Zð
\x0001A9¶À\x0015r'tªò»Ø\x0002vªTDÛ\x000ct\x0003Q\x0016©Y/!_øDC5H¸\x000bNÁ[hÝ\x001c\x000bÞ¢A×¢üÌ\x0010ÕÔippÔ°\x0018X\x001f\x0005úØ¡¯X~æ ($¯\x0000Tª3Øh\x0012\x0019eãÂ¤QÜ \x0016îaüÀW\x0004ÙR{vá\x001a5­\x000eö]\x0005]µò<µ\x001c\x0013nd­9$\x000fÅ\x0017Á)E=y\x0017f (D'0O1!×O\x001d\x0008Ð&\x000f"N\x000bÔw©ÍäiìG\x0011»\x0018æèçìñ\x0000\x000bÎ\x001càFÄÂ6\x0014£W¢È"ÌTÒ©Ö\x0017ôúK
\x000e«£0­¢f`(S=ø;Ï]I4û\x0016#u¹\x001b¤beK\x0011&\x0015õ~\x0014±,ùB@\x0017pD\x000cÙt+\x0002U]J0é5îE\x0001«¾üÎ¹\x0015¡¶[Eä_!\x0011]b×\x0015@ô@>ûßâ[\áÁ ü ëæÝÎ\ÂüB\x0001tä»÷gMFÑÔÉÑË\x0017;\x001a7\x0006\x0018\x0012bH³0(®Í\x0006[í\x0016\x0016f©M#ÄQ[Òl\x0004\x0018Â½\x0008B¸" êOlwãjkÀxb	PÇ\x0005\x0003"+D\x001aU\x0008Ö)ò¡\x0000eÑ"LØ\x0016M¥Ï\x001f.oÂt
ìâýýÕÎ¾P5VíÈ\x001aÛUêjlLõ\x001bCûaÚA\x000elOä\x0000VM\x0001I`)Ç\x0001giA¯*,ë\x0014Jéõè|TpóÛÍ¿MÌ\x0001>»¸ùxqÿù\x001d 0ô­®WØ<dë£7LßdÂóZÏÏ\x001d¿ÞFtÙªùº¯\x0001Ôím2ÿð\x0003I=ûçß\¿Ýu±sXX_WD
Dëh²Éx\x000eOB\x0017">;9;}ºÿû\x0011ý±ò³\x000fAÄµß\x00148Ü\x0000Põ}åÅ)\x0008@°íu_ýö!\Q[\x001cJ(?¸êïÛ»O¿>\}ÞQ§
àU-ÒFnÓËÆæìh\x0008\x0012ûÏ¿}ñæÕÿzsòz{yÖ^ÝÞ_\x000eË³ù\x0011=ä/^|¾þçï\x0010IþZ¡
ÊN"¶1Ö"¾ÑÂö ì8öÃü_oe\\x001e`	ÈZ]~f¢Á±HPZVôrS%d\x0005(å\x000eýDÙ\x0010Í¶c\x001a )*íl4¸E\x0015©\x001fJw\x0001TöÆM
Vé(Esç>}Öÿ7Ù\x001eãØÂ:IÄfX(Gä³\x0000(±¡=§\x0018óÿY'c\x001cPøn+ÃÂíïïþë¡Km[{ñðû\x000e\x000cØ9éª\x001dðÈó@Ù\x001dK\x0003)6Ñ¾øîÒ\x001e¿ÙÆÎÖÁ(\x0013\x001dv\x0016|\x0014eÃÕÍ(Íç ZÓmÔ*.¡+W_%ë!P\x0010Ã}&ä¾æGD8¼\x0002\x0011÷¿Úÿú­x
Øk?O/>þrUþwwã¨ú\x000c\x0019ë4¹òª\x0015b*O½<yõú|;ÿÆ\x0000\x0007¥\x0007?\x000fG¾\x0008<=a<°à,ÐüKý\x001c\x0000HD¯©üÌ\x0012³\x0014÷g·9T>\x0012o|¤'Rf\x0019\x0010­M¡¥ÀßY"	é®\x0011ÍN®µÐs\x0015$èÒÉÄ_>gÏ±ôccZ\x0018ê:ªË»Û]þ\x001b6XÕ{Ù<á-î¯«Ò(-ýôøüÛ\x0017Ïç @vwüÙ\x0000¹Î\x0010Ð\x0012ô\x0000bb\x0008>,`ñZ?\x0007Bþn\x001d\x001eÉ*vbf\x0008^«s#F=\x0010@ý>~èR³Ù«ÍÉÕÅ®±\x001a§$,iªÒÈ!ÖÈ´\x001c=Í¦ääøÍ\x001c ¢\x0007ÄàW 47é\x000eq¨µ\x000fÉ»·?ËKÌÑ¡E,?gÿïÿ÷7ótk¿\x001aFYD\x0008¡M% Å\x0012{bWÈ¤~âèä³í¼§öïîRßß¡y\x0005\x000cÊÏ÷×7ÙÐï
ÀcJT\ÏoÄc¶ªL-\x0000¥D²?fºWòýéYoã·Ðe7výÝ\x0002²GêjÊ\x0012Õ)=¬Çhz#Z\x0008PàÎûoêï\x000c\x0014¸\x0000¢&
C~¹ÑU\x0014¸	®¢0ÆJPÜüùÓ§wÊ{ÅZ\x001a-¯ÿþî~W&Àb1­\x00164!h\x001aG:TÊYÕsªä\x001búýómd¬C\x0010eYyÝV¾\x000f\x0004à\x001e[[ÇàæÖkÜªJ	Ü\x0011Êl\x0010¥¦üÌU¤ºw­fâ
\x001fÆîù\\x0010	½òò3\x0003Dö-ji/ágWõÆ\x0014z\x0005A<åR\x0010uÓOýÝÂ`$¨¨àÉ
.³IÑ÷ã´ÈN\x0010ï~ÿãÎaJ= -Kùù¾ð#ï
a\x0015²¯QÏA¨Dy9ª.ëJ-½ó}!H~:\x0007\x0003¶<ãÏ^\x000c\x001e©,tÕÑsaA\x001bMS^NJÕ"\x0010e?%`HYta\x001dès\x0006F$üþùSá{,µ\x0005MÝ\x0017;],í\x0015º$ ?DÇü89\x001c\x0005u\x000cb\x0006\x0006æ&ý×a0HHS~öcÈj­6ªi¤³¬Tò>[/R9B4KA\x0004\x0004\x0011f	Bsýß+`j'mF\x0003ºs1X|Råg?l¨ú\x000fÃpùY5w\x0002R_k
\x0002{\x0012¿)?ûA\x0000\x0000%<NCj \x001cá\x001d¯E§ñá÷ß¬¿Å÷YÈZ\x0014­c}z÷ðñâöºn\x001eÝÎ+
w-Æ©Æ×%ÈÙ§JÔ®es¸4Âòêèé7ÏâþÑmî>ðÇ»RÄ\x0005±¼!\x0016w~|Þ'Ç\x0003e|ßâôNê»t\x0010\x000e®þx=\x0003.ÄµèkçI(\x001cS]lÖ<õk\x0000M\x0019{$Ã¢qÞ}¾Æ%±\x0001Ãò`°mg>0\x00075ýp \Öï4ó
\x000cq\x000c\x0005ÛÙf\x0001A§Ä\x0006ûø\x001aùU´\x0010\x000fYr<\x0013djÆûø\x000f\x000f÷¿ü@°¡üÝÝ¾ÿå~wêÍ¹ÂÛ.yru5¿d.\x000f&dBé«ÿðrÇ\x001b\x001aÀÐ\x0019f@zúê\x0000Âf²Ç'
\x001b½ÁêØ2\x0010\x0018=ãÏ\x000c\x0010·Ê\x0011²­9\x001eÈÞ yQõÁÉ\\x0014ºP)×ß\x00190²2#FÍ[kÖ4iC\x0004\x0003\x0012\x0018ÿ¼ùÝ_\x0015Õé{üQÍ°íZd?ÅWöso³^'ÝBï\x0004¶*Æ~\x0018øBÊÏ\x001c\x0018ÊQÒ<8íhNÛ@Ì­6Ú¾>\x001bF\x0015Ë\x0002\x0019üSÜÁq/GÅ\x001dî÷²^9ÎÊöM.{aüúëû_.
q
\x0007þy Þí
\x0018\x000b[JÍAZ\x001bébXdÀ¤<Wì©c^"ï¶_?ÍúmÕðûåç%Öu>}ÚÉYârÈX	¾\x00126^QFÖhJüyìÊì`¾zõb{J£áÀNoÊÏ,\x001c\x000e&\x001c¼i;C×D(.àáê\x001fáïC¦Ù9<GH{N¼\¦2 ãkµù\x001a\x001fIYö\x0003i¼²óx\x0017k\x0017xC\x0015\x0011.qg°Uªï°\x000fdÈ";K$ù`\Ebc i\x00130®$õeýHâ½ºyû¡\x0004NhëI$÷\x0017\x001fw%#³K\x0010¹M\x0015Y*©'äA)ÙìÃÆ\x0011óãg;ÒïÞ^_~ü©ÀÀ&\x0003_W*Õg»Ú\x000c¼	ÈrTpxâ<ÅTGë×=ÿ,ËÏvÄÓ\x001b\x0018øn½\x000b°]äDy]{#E»\x0018\x0008R¼	Ä\x00017PgP\x0003qX½T Z\x0017^~g\x0001Ñ­U-\x0007Ô\x001cH!a\x0019\x0017uL!Én\x0013\x0017ê7ÿ¢Ð©<ÔÉâ§\x001f®~»¿z¸¾Ùå£lö«­	ÖQî\x0003WW#®Ç7u®8CûñüäÍéÖ=\x0014\x0003x0\x0007_\x001d<3gð"z5\x0012Ë>CÝ15²µ
_\
Ð\x000e\x0001Z)@Ì9W|\x001e0ÑVð9ri\AâZ|nÏ}uçëðüW\x0007/\x000cá¯\x000e^\x001cÂbx[ÿp	9Õ°3ñõ}ûrHð<_\x001epÔÐ\x001a©#\x0006i«-G\x001e0"byp[KÈû_6ºvÁ
7W\x000f7\x0019ÀÝ\x000e_\x0013=*JÂ"}a=3V\x0011©±uq58z}òæ,ÿã\x001dåî\x0006f°@q\x000e\x0018¥pê©ÑÆ WUÁ<N{Í\x0007\x001d¹ß\x0004d\x0002\x00103qÀøø4-z%TW\x0004·\x0018LDß¦üÌ\x0004#$ÃTüJj9>\x0002¦qI\x0000\x0006Iê¿)?s	(\Ãý]Ôae¸ÁÊº\x0010W`ÁÕÝåg&\x0016\x0008Ä=2@;
\x0000øÊ¸°øÊhmJzÃ¹h\x0002¶YU0ùöT·Ë8v\x0000­×rÇ\x00020©Ä*i¶h\\x001d\x0013\x00084ERÎhÕ­Uz<Úº\x0017þ5Ä?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-08.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?={?\x0014.ÿñæÕ«Ûç}s}ñæêæå\x0006pÓ\x0019à>ñ«.nñÂmAUÉØa\x000fÈnn×r»	Ü9Ó¤þ¼Ë\x0013µÊ\x0007\x001bø\x001aÖ»aænðÐ\x0019àXÊÂà\x0001k\x0011<éÑ¹aÓnðÔ§\x0019àÉÂ3LE#½ÿ\x0007Çc\x0004½\x001d\x0016Wlç>v7!Ö¨ãü¤\x0002GïòØ\x000cÍo)¦:ªdTB´-¡8¾ª\x000f±¯\x0015ñò\x0014èu={øÚHf\x001dô»]\x000bìÄÀÀr]8öÀÐ\x0002'>¼\x001bj\x001dí\x0003îRÎ\x0005C&\x0001·ã§2\x001c\x001ePT»\x000c\x000e¨voäk6q«\x0000Çý7ÐÞba:ðÝû/\x000f÷êú¹P5\x0008ón.í­eñT
'e#c\x0016ðÝóë·×oìqã\x001e\x0017ho±Î\x0007·\x001aàxb\x0013ªòÞ OÌYÜ¾åö3¸fÀ³¥¼ÕZ×õ>6ygqÇ;Îà\x0006Ûn\x0014\x0012Ñ³
*¸lÁõq¨»\x000cñÙßî?ç¨õ/{\x0015½cEïè\x0012©Âf·RG\x0004®è^<ûñêM\x000e\ÿôö»ef6-³À¼\x000c\x0008(-GoMÐ<\x0017X¯h/ìv-´CGÅW	X©Jó/M¨\x0013
ÁoE6A\x0007sìÉMI\x001cßßÿ¼`¿þüxÿé§_\x001eÝm\x001dð¨7sP¨uª½>>¯_=[¸_¿¹»zýÝíÛ»\x001f¾Î
-7Lá6Ìý;{\x0001ÅNý´\x0012ñ\x001cjÛRÛ\x0019ÔÞóø«rfPªç@GÞÙöÄµï\x0002GÇ®Ú\x0019¸Í¡%ÿÏÿúï«î?þøîq\x001f;äÈésÈÄ±ÉpÙ»Ñ'ÝuýùÅÕwWoÞÜÞÜ}Ýwìþ\x000fÅ\x001e;öøGb?\x0006Dv\x001c
ø\x0007`÷:\x001eÝ§éØt¿úøáóÎ\x0003\x001a 4brcy\x0000\x0016@¬÷%~mÜËíË7ë öX
Ê\x001eÔ ßÿûý>|þ¼SÆ§Úëîª@6çk¦FÁöó«ï¯þzýæÍõ¿þ|ÿËý§Ï\x000fõ\x001fQ¡E\x0005\x0019*pë\x0006
ÚÕih¶ñ\x000cõw°ÚÕX³©çÊ6j~3Ãéòô\x0016?\x0014£ÞÁê[V/cµÜ¢]\x0012W8ëñ\x0010å\x001d¬¡e
2V\x001d¸fÇåHd÷°7\x001f¥á;`S\x000b\x000b«XÒp\x0011æ¤³\x0015}=	öÁ\x001e\x001e«m8¨ØKë¡\x0008F"í2G\x0016i}mvÐø\x0016 ¢íÍÌn\x001c¹Q\x000bÓHY_U¿t\x001a*_ì í,®\x0010e\x001a°2µ\x001c1o8\x0015É°#°\x0003Öt°F¸\x0011t\x0011ìEXGÊôy#ð#³NC\x0019ò\x001d´¡ÕBK\x001bãÁ"º\x0011Ü¡ºsx1·Öu´N¸\x0011,_#:.é\x0019ã¹¨ú¤\x0016d'lç\x0017´Ð18Å2\x0016\x0015±M©¶¨¦Q\x0006½6v´QDWï²dÎ8ÿ!\x001cÔG_vø½\x0003¶ó\x000cZè\x001aP´i¹W<ïZÎ<á´i\x001f-t®\x0001d®!\x0002×|c÷\x001euB\x0006\x001c\x001dKAâpÑ\x000eØÎ3Ì3à> !è\x0018ÑÖ­ìÇ@l×B\x001fÓÊ<C4\x0007a\x0003\x001f] Bv
Àe\x0016\x0001:×\x00002×\x0010a¹\x001a"\x0003\x001ed¦\x0015îÎ5Ì5 03UÄb¿!uDæñN\x0000%\x0011 s
 s
Iòði½ÃÇ1¤\D\x0004V	7Bç\x001a@æ\x001abXÒËÒ\x0006¾
Uw
`¨:³¶K\x001a@5$tis$FÓø¢å
@¬FÑv\x000cd,)ÍÌi\x0012JÊû ÂÂPßo\x0007lçÈ@æÈPÌoÈ.½\x000cÄÈq8êóhMçÈÌá,F*ws^±ýÕ|¡®ø\x000eØÎ5\x0018kXZjØ Xj\x000e³ÆR0Ã²Â\x001d´k0"×à\x0015Î¢K:|Û/AB
üD\x0004ã\x0011Ç;h;×`d®!oV¾¡Ëù\x000eG1ñzì\x000eÑvöËìÇçeS]½1Ï1]'BH2`:óeDæ+ÿøº\x0014\¡E>ætiÝPØf\x0007mg¿È~y,­¢àsBVú\x0019Ý2E§ÐFaüe;ûeEö\x000bK\x0005ËP¾¼¶ÉSMåkÀ\x000bo=l\x0017[Q$îµ2lm}\x0015gr*Õl7
Ë\x0006wÐvæÖÌ­ÇfÈ\x0006,ÑÈaÿ7Øá,¨\x001d´¹µ2s-\x0014dz\x0013I1Áe@;ÁHo\x0012l\x0017.ZQ¸wEAè6§\x0010Ö69Í§l8>g\x0007mgn­ÌÜjOÕ<ù_Î4ÓñðÞ$µ	½µ2{®jÁ\x000c×Â8¼¶uÊ:{keöVc\x0003¹2ÇÓÀ\x001cpû¸ÑÃ®í°®3·NfnQg"XZZ\x0014(YVÖêº²If\x0011\g¿Ì~iëJÝm±\x0008Ôn \x001d÷\x001a%|Ës]\x0000æD\x0001_
øKÞà­¦\x0011`Nûº\x0011Ô°hu\x0007m;Qnî\x00014¿6x,Ë)Q\x0002ð\CmÌ°\x0018{\x0007mgmÐÚæE7	Þ:zÑs:@äµ
ÂCÖY['³¶`îÙ6g´oáÐ\x0008fù®ë¬­\x0013Z[\x001cÍ@§,ã@¾!T\x0003&¼\x000buµu2k\x000b©J\x001c\x0004\x000b8+\x001diã&ÁwÖÖ\x000b­m\x0008uÛ: «\x0004§¹"|\x0013Áv±­Å¶ù_ØèWvm¤{[g4K\x0019/º¯"ÚÎ7x¡o9YàÆáë^ñºAæFf¿|ç\x001b¼Ð7$Ë\x0019$Æ\x0008,\x0002Ô~J-Ìw}ç\x001b¼Ð7xÇÊ'A+ª3u\x00068J0Ã:û\x001d°}©Ì5Yê\x0005K/ôÒÖ½,mH\x000c\x000bCÁÜ\x001d´±õ2c\x000bN×´!.×KËÒªÚ¹m¥)¾3¶^fl
6Ðº\x0011(m0ÉÖ\x0000²&t\x0006,È\x000c±ª¨\x0012dZPt'îr¶Ëæ6\x000cõøwÐv\x0006,È\x000c\x0018\x0000\x0002[OÚ\x000fùqlk4¡ËÍ,778h¼.ð-³¢M8),ÞIÛYÛ ³¶¨ÀÂ\x0019Y2TWç¬æ~=c%U¡³¶Afmÿÿ©{×$»r\x001cMp+¾v#Á·Í/\x000fWÂôÒ#ljþ]wyeª[!Uê5Y¿z\x001b³©uäNf%C\x001c\x0002¼ä
\x001dê\x0012çÈM²êÊöÎÊú\x000e.\x000f\x0004\x000fSÑ´\x0012\x001d;¢9$ÄÏ\x000eUO íÂmØ\x0016nMÜS\x0015PN¯\x0004\x001b¸1ÞÏ.ü@Û÷ÖmËÄs¢Í\x000f\x000e!ß|Ëækg£­¶ÝØ¦\x0014:r\x0008ÛÈÁ$À
\x0012\x0005-09ØºÓÖÄmÜ\x0010:n\x0008\x001b¹!En\x0000\x000bÖÓæ\x000bT/`nHÝ\x000ep>ÚØqCÜÆ
V\x0005^\x0003Nn®éâÆ¾ØEÛ¸-ÚZd/2mNÊË^XÔíåÅ2\x001b/d±\x000b_q[ø²un\x0003Êÿèå<¯Z°ús\x001a¦ç=Ç.ì\x0005\x000e\x0017\x000f¯?¼{{ñÃÃÛÛ¿Nâ
>2sPK\x0005l\x0001ì\x0015kjþóóÈ£«ÇW\x000f?}rñÃ£«'\x000f~>\x00034´ á;\x0001mZÐæ;\x0001m[Ðö;\x0001íZÐî;\x0001í[Ðþ;\x0001\x001dZÐá;\x0001\x001d[Ðñ;\x0001ZÐéû\x0000Ý\x001b¸eÜà»@ÝSâwÂºãDý¢îøE'\x0004£»X­¿õ`í£éC\x0008\x000eñ¡O\x0017Þ}Ü¼ÁjGùªJ\x001b\x0010jS
ByñèéÏ­døÒ·\x001c#\x000b~K³hrÉ?¦ALå\x0015\x0017Õ~xé`P+\x000b\x0012§>&ü\x001eÿöûW/¹÷ë»O\x0017?¾þxñÓ»\x000f\x001fînP,LÓI@ýîíÿøðéýÿx|÷éÃ]Æ\x001b§óÕ\x000b\ä.±|\x0019\x0015xµEiV~\x0016ýíaöç/]<¾~ù<ûÏÃë\x0017?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-02.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=þü\x0000e\x0001\x0015vçÕ4édyølBÝ²Ôlçg\x000feèE\x0012h4UyBv(eô´`|«X@\x0013\x0012â\x0001e\x0002`Ð\x00055õCeCÃ¯.AÜÕ¹F¸Ö>·\x001eç¦^?âC8U"E\x0012\x0001Ô°\x001fñ\x0012ñüêâ³\x000f\x001f??¾¸Ù*²2ØËRñdaÌ-Îüê"²W¯ß=5"v#ÚD\x0002;ÕÁ£,èKªcÎ	é`Ô5£î?F*x\x00076.\x001d\x0005±Ñ\x0005ÎÿSÄx&ÖÖÁhjFÓÉ\x001dbIëÐÐÔýé·\x000eRa§ÕÜ
ë\x000eF[3ÚnF;Áçèuc'¿\x0019\x001bSßÁèjF×Ê\x0014GÂH±ó"ýu"_èkDß¾Ló"ÉÏó
¼g\x0001dfÇìv01ô?ÅS<³Ãy]"§8W¨Ý\x0018kÄØ^KI@°^&è\x0018-Òú¸×2V1GØÅ\x001c{ÎF@\x0017\x0001=qçKá`à3º¦±U2ýZ\x0006Y~àËÆ(+¶=í$lt\x000cô+\x0019ÒF\íÈ½ÔÝ'-¸þ\x0010\x001b\x0015\x0003ý:\x0006¢ò\x0008ªUÑ¼ß\x0017\x0008Ø¤&W#6\x001a\x0006úUÙmÆRdY|'=hµ¶úQC#¾¡_~\x001b­Å\x0016®²LN*Ý´-ÕÁØÈF\x0018\x0010» ´½ºôgQ2q.(±\x001c\x0012\x001bÉýGGSÒ\x001cnj» ë\x001eÍêÄÖxìØÚ#\x001bâA9ù±­\x0010\x000b­v 6¯\x0006û_
O"\x0018ÑlôA'f6aÔ\x0001Ù¼\x001aì5:Þ!ÇÕi\x0004\x0011'UsCêæ$õûOp\x0015\x0000\x001b?1«\x001bq\x0014»\RäCyMÍbh\x0017*µs9·\x001e9ô\x0005k\x0018bMr³ÜÆæ\s¥¸ÄÌ@ìñ¿öAõ\x0010'¢\x0012\x000fVÜn§KáÎìÒ¶\x001e´C¿?MæD| l¸%Dqu|\ïêè¦¬k:VimíúùËDÒF¼Y\x000cNÑFsÑ£\x001ewbÿXÇnj,ç	ûhÈ­\x0010kxn¸k\x0007)|ñ¨HC©Î¡T	Ë*%·ë½\x001d(Pï@éýö4\x0000+¨ \x0003\x0013¤~ãù\x0012T½\x001fÈÒ»Ò½»O'\x0017ï?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-10.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=z\x0008O®¾\x001a\x0011jDèG\x0014\x0007\x000buR\x0007ìK\x000eÅÓ	:\x0011±FÄ\x0011DiM¤\x0012\\x001eI²NCïªçï$45¡é'\x0014läõuiï×jWô´\x0013ÑÖ¶\x001bÑ¶~\x0015AïjåJ\x0017ìP®FtÝÎrH_ÆWë²îAí¬ãèDô5¢ïF¤!r\x001bDQ¯"W\x0012â\x000e½Þ\x0018jÄÐh\x000bá¨\x001f@*'=çjçTNÄX#ÆnDZÑÆ×%én.ØQ\x000e\x000bâ.ëØXÕ¿Méû~FWÚ÷¢\x0000¶mµ«o¿\x0013°5-ý¶Å):Y+jqÞTÄÒ
·kþQ'cc[t¿qqZêiç\x000co\x0012SÑý]qNÆÆ¸è~ëâÊ4!
%A«¢+\x0006pü0¾'\x000fÎ¢(Æg9¹Tã÷wnÿzwûôX\x001c2CuTë9¤ÄM×z\x0014¿?»8=zþãÙéÅw\x001fn~ºùüåa\x000fÞ»¶\x0001ê"ÔAb
ÉØsñ-\x0019=';Ü
pþ\x001bëí\x0011º\x0019q÷ñþáîé×.*	$D\x001ehä\x0001$_8\x0017=¤Ñ³óË«³§ñ Æ^<ª
\x0002(õ±Ô\x0006Éc!ÌÕXw bÝ\x0012ô¦$]CQ6>H(Æ¹N\x000eDS#n)æ©\x0014ÙK\x000cÒ5Í-\KhkBûM
ÑÕ®[Ò8ëµ\x000c)Pº!Ã\©J\x0007¯ù|7\x001fÊO e\x0013Õ¥*5Î
ôí \x000c5aè%L6­¼üËÍÅ^qSE\x0013æªh:\x0010c\x0018»Î Ë94ÜäUº¤ÈXIX·º¶\x00034JÑn\x0017¥Èª\x0013\x0014÷LøYÈØ\x001an«T)	å,òmÑåCGØ3`!bcXt·e1é- ¤_åv>=Åæ9Ê»gêØRÄÆ°ènËbì¦ÐÜIkª¦iÍOðv06Ew\x0016\x0013¸«l*6Ì]âÉG*Ý%~{ÓØ\x0016Ým[3%ë\x001cÐ
K1õ\x0018¬ellî6.4\x0002kM¨Àó9\x001a$\x001fíöÌ¥}ÑÝ\x0006Æ\x0004(¥T\x000féø[oã\Î©±Qßº[¨å8:ÍAE­<nnõê\x001b\x0003nnÝhµ)MnIñä\x0011ìþù_Z-Fh4\x000ftk\x001e\x001bK\x0010ËQË\x001aªÉ_Í¨BMÜ\x0001Kå<FÉz\x0014l®
§ÇV·mØ½®ú°BÕÛ´Y>\x0017]	ëµ¤mT\x0018 \x0005cx\x0018ëä¢ñSoDU¹\x0002Ò% \x0010·ó\x0006q7 nöô¦¾yüüù\x001f²}Z\x0018Ã'Pâð	FlÎí\x000e¥C\x0013ÔÉ~×'×¯_îkfg`¨a\x0018¢L\x000c^\x001ea\x0018eÛWú5f)½ÄX\x0013ã¸eÌ\x0011¢q\x0012\x0017§²|&ù\x0014M/±©ÍCÁc:Ñm¦µE®~7hvUÁ\x0011ÛØ\x000e\x0013'\x0017ÞèB¬øT\x0004Ià$âÉØÕÄnJ8s?=YÄ gÂîÚ(0Æëk^?Ìk\x000cíÇäZA6\x0013he\x0018>îÜP:F\x001cjâ0~&ø\x0008£s\x0016g5Ñ®?Á\x0008¶UÄHýQBûêîö\x0003%ÿïÓ 6zYÃ¥i\x001dh^Û\x0010|\x0019:/ÙWg§Ï)áü¿\x0017pBÍ	C({\x0006e=\x0003ÁÉv\x001emæSS= Xâ\x0008¨7²6[ëiâÙ\x0004jd|³]cúAM
jF@DµÉ-ÌÝ\x0006$Q\x0004\x0001ÝUcÐ\x000fjkP;\x0000ê\x0014ò`ª
â#\x001aJEïxæ÷sºÓ
\x001dÑ(©IV\x00167\x0004iOGtÖéáô5§\x001f'çþtzaÉ\x000fF8Ý®Úèå äroUm]?\x001f=»¼ûøñþÓç§YÝ¦~\x0003ÙGH[$}µÏIwy}v~~yñúi\WãºA\ãOOVò\x0015'\+Û\x0005´ÞµQy\x0008××¸~\x00107AI\x0001R9¬B»©¥$AïÌl
á\x001a7\x001e\x0006,¹LÅó%è0 .¸n¬qã .­Æá±R1äöýisdÙç3Ø}´u8Z}·)\x0006èÄM\x0012\(Å\x001fª\x0014\x0005ìJ>\x000cáê\x0006Wãòòô\x000f*\x000b\x0015Ê¬äyuÛÉ\x000b
/\x000còÇîdÄd£¤-nÁ®\x0001ôCg×¾ûÐjÞ\x000f\x0002VTÙÍ\x0004ïÀÄüùò\x000c\x0002-WF\x0019[eF_üãïþñ÷ä}¿¸yüøqÁ?z)p2M?å4©´{X¾8½8½:9''üÅÉõùù>\x001bg¶\x0006BwëÐ©GÛkÀÈ´(¡0ïö$\\x0006ÈCM\x001eÖ§ãÁBwÔ	ì\CÒ~@òJÛ\x0019['ßÆÐÝq\x000eäÒ0©\x000brZ`Ï¼í\x0001rÝëUä\x0016,ñ:J°*äHàÖ\x0001ðfOo\x001d\x001avX'õRP
ÆaAQKëÕ\x0007=ëU\x0012Øq¥ÜÃ±YîÆHK±\ÎnÀ¥7#ìíö¿

ÓG'l\x000fõ¸ù×_n~ZðZ¡eëÙ
yS61£,\x001aÐ{2\x0004¯ß|¿\x0000\x000fj<èÅ³NF]jyõ\x0019yü²WPÏÎ<[\x000e5 ö\x0002:~$ób®TËî|ôÁ\x001aÎôÂÑÊeöè]Ì$Ó\x0012VñüÜîÝÅº\x0001Ô½ÉsÐ£¦1ÍÜã Êò\x0010·g\x0012ùBBÛ\x0010Ú^B[ªóÓuÎß8ùieØª\x001dl³Ð5®Ð(r
$à ®¸ê³íBË	}Cè{	³Ã	±øº¦C77\x0001x9ah\x0008C/¡Mï\x0014¦ÇÙ¦\x0005ÃÍMÚY\x0000\x0018Õª¨éôdxsûðp{óø×Ew\x000bß
ø2öW\x0003ëB£f÷
¤\x0007ÃÓ««Óë{\x001a\x0014jP\x0018\x0002EY\x0006kÈódj%\x0011°\x0004:w©»@±\x0006Å\x0011P;]	4=r¹ÜN Û*g\x0017kö\x001aÔ\x000cº$FÇ\x001eÕ±æX\x0007löªÎÍ¬ê\x0003µ5¨\x001d\x0000µydÉ\x0004j\zÛrF\x0001çLb\x0017¨«AÝ\x0010häi\x000b	4\x001e\x0003szÙü	nÎ2vqúÓp&¸À\x0002
:ïSáeu³\x0003«ú@C
\x001aF¨*+\x0000i­&fO2Ä²£tö­×Å\x0019kÎ8"ÐPÆæSÙ\x001brxÞñ\x0003Ã\x0018-éï\x0001­ÑQmÑ}\x0012õ<>¹»ù%D\x0002Ø¼=ÌUÒ­]\x001a1LNiÑNÖÀ±ç4Z5[Ù\x0005ÚØ%=bÒQd½?fw½Ü¬9Ä×YÒ#v¾<§el49!?}z\x0001]ÑGÚ¨{=¤ïÿEêÉ\x001e#6M?
°&÷#ðwêQGDàiúAT~\x0013QÔ~	(tá&GÔòB]åJJÞ(ñ¢üìÛ¼Ïª\x000c'?êfÀB	®&GJ\x001d\x0007éxôâG©¹\x001e¤>Uµ-Z­\x0007e\x001bõ·¨Y_9q¦b«vî\x0012ì×´c°>L#âS\x0005îl.Ëu
ì*ëàÕ~ëBÏ=Q\x0006TsqóávAäË9\x000c²ZÙ\x0004®â¢IrÅk\x0019
s.Nî\x000fy1*Ö¨8
%Ùi(\x001dÇ/]Hg»úHMMjÆªùijbÈKKÉõ\x000fâ©ºùÓÚEjkR;BJÑN®ß$T+\x0017K\x0012ÈÆÏMéDu5ª\x001b\x0012ªV°¤\¡Dî)¨³Í-}¨¾FõCR]a\x0007ºPC\x001aP}àÁÚ	59\x0006N^U¢YÃì.à.Ô:#ï+çºÕ Õ6N¬R¥iÂÜPÈ^Ôº½\x0019¡EÙ\x001ehcîþ¤Æ1U$;ÿjYaË\x0008`hÀ\x000fw\x001fo¾<>,(Î¤i¿±\x00029üXXílGòÄúÃÙùÉë½v\x0019\x0016jX\x0018¥j¬\x00080\x0019Û¨Jí«Ý\ß	5,ÁÒ7Ç§@Ëz\x0005X´ÖìöËNXSÃAÉNååÓ1 ±v -NáÜ¸^X[ÃÚÁ3\x000bRLdAÉH;ª/û5\x001bCïu5¬\x001b<\x0006Õ\x0013\x001fJ´\x001aÁHÝ\x0010Ù	ëkX?(Y»¬/\x0017¬\x00086ÎÇúXcÍ\x001a\x0007Yc±_èd_\x001d\x001aiI/Ã\x001cYÝªÙA=k@²**çåàIç¢Ä]æ£\x0004g¶yÉLçvóé>ºÞ£Ë;BÒÑuåè\x001eèéªLk2e\x001fÆxuQb®L\x000fC\x001d$ö`¼ï[Þ÷ß:ïMË{óòªí}«
ëôÛÉ§\x000fw·>\x001f=¿ÿíýÍ/7¾<]»\x0017\x001dRt°¢ÓtI¸¢Þ\x0013@8¹x~vzñúèùåËg'oÞ\¼ÙWÃ§¶°*¬srcôN\x001e\x0014
¢d½tP²uvqì0>Öø¸\x0012_{\x001e@ðô5j'ÁQev([oj|³Vú^´¶"sÃ\x0015\x000f\x0001dË¬y\x000eâÛ\x001aß®Ä§6\x0001\x001e\x0010ç@\x0006Ä¥£Ïá\x0008å÷åvð]ï\x000epsyx2EG\x0007##øæË@GñC\x001fÖK_óÕ¥h¶lþu Ò?´æ©Új³	v_K;r¡4
¾\x000ci<0}£7õZÅ\x001e	°ßX\x0014g«\x001bfk\x0013Gù\x001bÍ£×ª\x001eÊËÊäÄ ´:j9=³Ëù»«×^^4\x0012³M¨Ç\x0003á\x0011¢ôP\x001cXsêæîêÕ×øµÆc^\x001e7-
ææÂêëyæ{ryTþëè\x000bý¾$ï\x0010ëó¬¾»AºÈ©ÓMîn0úN9,swaõÝÇ\x000fm;é\x001bK·\x000fWöâÃv:\x0008|5âÚ´ûóÑÛ%\x00032£5e#(¥s3¼ûÔ\x0007>×çrM­Ú/_\x001d½8½zb§ßò\x00132\x000c#;<¦ kX8)_S»²\x0018ÄX\x0013ã¸A¶\x0018{<\x000eV\x0002\x0001eÕú\x0001eljb3LìËÞå$m	
U+×wåâ\x0007mMl*\x0003ÛldíXfÊí46Hìjb7L\x001cdhw"Þ\x00089Ø¼§¯\x0017Ù×È~\x0018vÊ0±¢.ê\x001c\x001dÚl8ßå\x000f\x00128\x001fäP¢,6¹w
\x000e\x001d$5q\x001c±ã\x0012ÍDìÊ´\x000fØlj
ó³Èº5"ãVÄ©2 Î@edË®\x0011·kK/3n
ýNÖ¡Ùç\x000f÷w=ººüeA\x0017V²t.*Ã\x0013­4­\x001cad\x001db\]ýÛÑÕåõ½Á¸­ù\x001f\x000c£ÈN9\x0019í\x0019rÒ\x0001d¯Ox"'Ú52\x000eK98éê$\x0005
¬6+rç+¸»Ml¥\x000c\x001b§³gFi°eºÝÜvÏ\x0001b[\x0013ÛUç¢(\x000cëøXlP½µ\x0012]Ä®&vÄ4H½ý<tsB\x0006\x0005¶è8µ7QÚ¬¬²7²ÿ:Ou\x0016³)~òÜªº\x001eb\x0007[\x001aV×MÀ\x001f?Þ\x001eß<¾øÛÊØ\x0019/ñcCn\x001c×Î(\x0015I3áãós"½~võ§§	¡&nBc_\x001ae\x000c·½i+i<5Tè!ô5¡ï&LFÇ\x0018\x0019\x000cyæ=UÊI\x001cÒèñK\x0010Ñlu\x001c¡QõÜûûO_è|¾¼ÿx÷é÷»Û'fúÎ<Ò\x0006\x000f&Aßà¸KÊi÷\x000c=¼¼xCôååùÙÅÛ³Ó«§Á±\x0006ÇUàXÀ³\x000bÁe8¾õw+¿½ðÉkø«Ï\x001f\x0017ø8Þ8ÍÓbÀ¡¢\x0017hely\x0004¦ósk5_¼>ßïÙøíMJ^\â%\x000beÀ++U=\x0011ÊæGcgªçÄ\x0003»u^ÁÖçõÅ#íãxüðëíÃýÛ$¨co¾)7ßÉ ³sO´^_ÓNëç?^]Îox¯uKûLëöüæèt@ohñÅÍã_¾¿ùíöÉ¸M\x001fUJý!D\x001e\\x0012¼ÛLéÜÕ@Ït:Oh	ÆÉõ¿\x001d}òòt>¤³A®òøM?\x0018%WÜ\x0002ä\x0015dnÙÍ\x0002;ëþû°iñ÷¶C\x001eå\|\x001cc¶\x000cë\x0004\x000e1b¦F¶\ çÚ<wÕ(òÜ½3wè>Þ\x0011;
q¡¿Îo?\x001f½x¸ý}bô*3ºÄøéöËgb\x000b\x0011Ñ§²9Úýh]\x001ek\x0008*Üãg
(~]¾yýÝùéë£\x0017W§okF~
E²%ô×Ó\x0014!ú)­4Q$UqW²27QhwRìþ­,ÞÝLÒ¸Y"\x000e\x001drà@X\x0016!\x0017å(`·(æ ÞÿÇãýo£âS,üüöèíÝÇ7c¶ &×+P×\x0015åË§¼ÛTsI;¸'\x0008´`\x001bI\x001c½=;??Iî×Ü©Ø@Ð&gúk\x0001\x0004rÎi ÂÉ\x0017\x0005X4qÌô×\x0012
\x001b½Ë\x001427Qp[g¢@n=\x001e Hr0\x000be¡pÊ~\x0012ER>>Ë6¿1cÏ³J¨ý2
G{ïíDAm¹Ów ü\x0007ä³¸.­\x000eñü\x0003Ñs¯ûrôòö·ßîöT3mcOD6\x0017K\x0007ÕiÇDÛë'"Rg¯"{sôòôåË³¹çBÅ\x00055\x0017ôp¹ih\x0006Ããü½B\x0008Q¸x\x000fÇ \x0017Ö\ØÃ¥§[ù\x0013Zî\x0001M\x000eNðò	5®\x000135é\x0004\x000b¶Ü±Æ<O$qÙUX¶Æ²\x001dXäôów¤Ç_îíE\x001eÎ°\x001cW\x001d\x000cr¹Ëõ+Ùp­3Q\x00184ÈUtv\x0015¯Á|À\¤Y5\x0013÷9#ô¥3"±\x0010a
X¨ÁB'\x0018fsâ\x0002ïÔÀäJÊB³A°XÅ\x001e°ôR\x000b|%cÌ¡	\x0006nWq®à2\x0016Ñ­ªÌçKIëÙ\x0015
X\x001d\x001d×\x001c2Ýjý\x001eµz\x0002É%ÊêÂE+¾\x000c1\x0018$kô¾îQü¨\x0003û²É_H\x0016É0YÎï¿`Ý\x001a²Fóë\x001eÕ\x000fÉ¿õLFG\x000e2\x0019Å¬2á5±dÕ=J\x0016(ÃoØ»°Zr¼|M\x0017V}ÍFËê\x001e5\x000b\x001e¦?"³!G&Ì0?ö\x000cí\x001a²FÍê\x001e=Þ\x0004ÇYÿ{Ú§\x001d\x000cË\x0015ð	Ì5nÔ¬îÑ³é4ÍS>f<æ©p­\x0013X£euÕ\x0001\x000b\x0017-ÏÍ`Vþ7aúFËB\x0005\x0007ÇL`ú8ðé·â\x0006A²FËBÕÉ³\x0000>ýÑq\x0003núZtY\'³Ö»îÑ² ô±\x00159R\x001eÌ0\x0016Å5Ç\x000c\x001a-\x000b=ZVk%Z6=ÚsÊ(ÉLûòvÆU_³q°¡ÇÃÖ´ßßé­\x0014,f2¥V5ú\x001f:ô¿"ç"¿n=\x0015O\x0013\x0001BP|ÎüJ5ú\x001fzô¿\x001cþ¾¦Î©$3#\x001e9®dþ\x001eý¼'@dQ)î8G\x0008V¾f4«È\x001aE\x000b=V©i~&\x000byMT"c9µêåÅ\x001e=þ»Ç|12c7vÔÀÔ\x001ae2Ã\x001eeÌÚÔ'H\x0002ÓgÞÐæ\x0019¶åN¯:dØ¨\x000cìP\x0019\x0016\x0010	\x0019Õ\x0018d0.JJ`¨ÖxØh\x000cìÑ\x0018!ÉåéÙF¦ÈÒMçéÂªÓÍ½Ä{©Ò¿¦Áz¤ËTÞ\x0004´«C´«ãa_¦èhåØ\x001dí\x000bµùi§Ù.9»êÅ¾À\x000e}¡<
¡cí\x000fç@D±K^«5/&Óh\x000cÓ¡1hÐx9eÉÉfï¦w³ÌÜ*»d\x001aÏÌtxfé§®ÈÌèà%ÈâaÕ#Ó4îépþÙ¦Ü4*Ãô¨\x000c7
¾À¬Í£\x0012\x0018çUÐ¯Ãj<\x000cÓáa¨ ­¥O{ÎË¡RVtl\õ3Â0=
ò³Úó½|\x0018DëåSê5<Û\KÛs-½vÇ¬aOH|Äè\x000b\¥/´-©âM,Cz¾\x00173üÔi7½\x0004§l\x0010³i\X\x0003Xå²KÂ¤&ÓrvÏ\x0017ÉÉ	\x0012	\x0013÷^©<ÈÉ]xFCy©tëÕÃ?þþùè§ÿþÏÿ:ýtôìf.ñ\x0019µ¥¦Öl£¦éz\x0013\x0017í\x0016Î\àuån¼º:}}ôýÑéÅÑ³ùLð¶7\7=`¹ñÀ¬aåT)d\x000eçÈæ?gS«P·g~¸ÿ8%Ú)#ÁY\x0003í4
·$ã¶] ê9}~y¾'[\ °ÂÅPÖ£Äe\x001díP7\x0019ÊhÉâ\x0018=Îdj&³ÉiR\x0012\x0013SÇ 0ùm¿¿ÉÕLn9SRõVbþ(i¸èï^!(_CùåP4sJÞÉ;$z]R7Û^E\x000fT¨¡Âb(üiþz4©<°R\x0000ÚiãL±f4ºiÚ\x001b=%C6ØÆâ\x0008?~ª\ÙäjH6Dpp\x0013\x0014lÄBíDM\x000fT« k¨ !åbr¡ó\x0011Ì®C\x0012ÒÁñk§\x001bý¤+(ÚT#i\x0013x\x001e\x001b\x0006¯%i·=­\x001eªFCéå*Êè©\x0012+g\x0018\¼°IKú5gªQQz¹Bë¦©»S\x00103oåmQ1¬ jt^®¤ÐçEÍ\x0013\x0017ÊWÙN-÷@5JJ\x0003Z
\x001a-\x0005Ëµ\x0014)½1\x0011¥Ó\x0005%ÓÍ\x001fÏê\x0015î\x00014J\x0001:\x0002¹ë\x001c\x001776OH\x0007Ý\x0006ùx_ez¨lCe;¾âpMzÖ\x001fkàÀ³$\x001e­Û.
èÂæ\x0003âò\x000fH©*²%²k¨O»Æ½ÃFQárE¥Ó«AbôÁ\x001e;ÜÑûí\Ð"*W÷å\x001f´ýeç¿>Þ¥\x0017Ga9ã£\x001b3­ªt<§\x000fLºRæÜWG
nÏ¼>{sµgle\x00055 v\x0003z©+t$;\x0006,¾q¯¼«^>Só\x0011>~O8Ìí\x0017Ä'F\x0008=¬\x0016 ­\x0001m/ ÅØJR\x0015sÈ\x0016A\x001cy¿Z®\x0006t½.Ní6ì?ç\x001a\x001eZ±)Úm»Þ¯Ï×|¾Ï"Ï5Gï\x0011Å \x000bk\x0001C
\x0018z\x0001*~\x0010È\x0003ÄèàÏ¨¿z\x0015õ\x0002Æ\x001a0ö\x0002Òþ5\x0006Dà>
J8oÚµ\x0012¬Þ%®Ú¹Ð«\x0008=IÆD\x0008ÝvåQ?¡n\x0008u÷G\x000eEé¬\x0007c(\x0015HÛÙ~ÂFQënM\x001d­/ú\x0000¼\x0013:#JaÍ×\x000eA/a£ªu¯®¦B<\x0017Ø»ãNõDXtµUÛ%©ý®ÖÝÊdXDÈºzj.©µÆD7ºZ÷*kXDh¤j\x0019E¸¦è'l´µîU×^Çi\x001a÷Ô\x0019b¹¼%}d(å-ë/J£®u¯¾¦­:²;è9\x0003e GLÒXAØèkÝ«°©úÒÃê8 	Þ\x0017í·kÊ»\x0001¡Ñ×Ð­¯½;vöO\x001f9d\x0004G8½Ãî\x0007lÔ5ôªkªÅT+&\\x001e­DßØÔrµ\x0006\x0005\x001au
½êú_AØ¨kèU×AO³´r¡¤ÑÒ[Xnß.Ôï'lÔ5ôªkÖÊQëóH\x0004\x0018E\x0019z0«\x001d¯Ð¤Ò&ï°\x001dï¼ÈÿrR\x000bj¿³(¾
|ý&^L\x0019¶1A1Ôpÿæ×ü¿ßo?Ý}\x000fmð´^ÖÖ\x001cX4AÌ	lù]ÔbÿæÇÓ·§\x0017gsmÀ\x0015©±L\x000f-\x001ekp }\x0005ÁÇ(q\x0004ô+¸lÍe{¸¥b¾´&\x0016N\1K»\x0006+ÔX¡\x0007Ë[éÙ\x0012\x001f\x001aèc\x000fã\o\x001fJÎá\x0000\x0006\x000czÀnc\x000b\x001bÉYFérb§­¤Q'W£42\x001bk¥×RIÔ%hC¦6Ö]n\x0015üõò}\x0006DÔ|ôå|´Ó$!fûa£Ò¶*R\x0016ÒzÆTþA5å§Ç£\x001fî\x001f\x001föÜM(ÉÉ`¥~-D©_Ãh¾Öeß_\x001fýpy=7½\x0018`»Ï\x0013ªÅ¿4©ëÓ»/ó!mê:eØyÞ3¡¼)¬ý:øHC¹.Þ\½y\x001aÌÔ`¦\x000bLKµkvL\x001a¶xÁv
W¥4 NT.\x0001³J28FZ½ÃïdÿT/Ý.§(£4¦ó5ó\x0017\x000f7rïI£Ü¼å;æO(Á
m¾¶\x0002Ù¦¿¸:¹ ØýGÎn\x001f9«ª9?\x001dÔÍ]SÉZq
lz7Èßq#z@ý6¨¯@¼yü2]Û§ºÆ=ÍzßX(ï\x001d­ÅJ¯µñ'×o¦û+-äóeG*aZ%ÿ×ïQ@rú{jiv÷¹TE}ÚCi%UV*¢Ì\x0014³áÐo¦.\x001c=»<{]Ê¢.f;Üí»÷ïyøõ'>t\x001c¸}ømúÊ/î~¹º\x0004æ±ß$ÿö·xyóð¿øõæ#±\x0005åÌîHoWgù¨0õkÐðô\x000f°¿t~þ§£D÷òäê4Ýóï~8½z9}ó\x0017g/Ng'»Ô2\x0019a\x0018\x00132fà
{ÂÌ*:aJíó\x00010ÓïK
abàq>\x001e\x001cÇ©T01\x0007ti\x0019\x0004·¨­ÇäR=.Ð\x001b<²2}z~¥\x0011lùòaÝ\x000f?ýõá¯®¿|\x000fK/\x001fá¢\x001c¤ïÍÍÉ]àiÁÛl4we*$þÊ=H\x0010xÌ~z\x001eÜLä\x0015$¾;¡Þ+¬ç\Ù¤f°Ì¹¢)<¤ªßOYÊ§ }\x000c¹w31F
6\x0013bRèõÌ7%[H\x0013xHm?Í]V¬P³Â\x0018+µ×å[aªÎ÷ÖñD¹à=Ï\x0013\M5-\x000eJV³\eZ#	G+äoìÖ?Ý¨®Fuå¤F\x000f¹7Ñ2«\x0019©«Y}Íê\x0007Å
Gý¦c0© ?M%Èb5Ü7¸\x001a5Ô¨aôn©,SË5±$S`ÔÕXÆQ¡æFi\x0012*\x0005D2¬Ñ¹UÓ¨¾ÃÐ²³.:K
ÖN$[À"#Ùòê§@]ÕÁmUì¨¥1|d'ú&éÊÂÈ`¥¯b5n£eõ %}\x0010mîæ$ÕÅû=a¾«i\x001b-«GÕ,&/4Ó&\x001d½$[Þ\x001c\x001aì$k\x001aV3j\x0012rà`½Î95\x0012­\x0018\x0005Ô»½½nZÛÐÚQskx+\x001c¡çf8rHË±uî@\x0007¡±azÐ%^ÜÓ\x0000êXpyÓi°Á\x001eH)4fL\x000fÚ1o\x001d¯éö$èiÐHÂIÁÚ\x0003iÜÆéASFSï\x0010³pµÉ[\x000c\x0012­\x0017GÑÊNéµ¸Ð\x0018\x0008\x00184\x0010ÉûwU\x0002£6|toýh«q[¿vÔ±µ\x0007ë{\x001ana\x0018Ñ¥f\x000e$ÜFÁ \x0016ó(«Ð§\x001b³\x0013\x0006±¨\ËÉ°õ\x0012Ý.\x000f\x0007Iõ\x001f`C'!\x0004ÒÂù\x0000³Çþt ëf·«½~\x0006ÔúqÈEÊ\x000fi\x000ft?¦§$ýÏ½ýíîSW áæ\x0010F>Æ^TqhÊ9Þ-äç?¾<»X\x0010"(¼PóÂ(¯±´*D´øeç\x0014'ñâîÜÏ5/\x000eñ¦Ã uÞ\x0000ü\x001b'/\x0008¼I&\x0000¸¸é\x0010í×º©r\x0010¯nþ¶L²ÒåÓI\x0008Ús\x0010SÑ@]v\x001d¢ÚóúùUÿi\x0001¥©)Í\x0000¥WOH\x001a Ï\x0014J\x0004Ê\¬§´5¥\x001d ÄéægÊ(Æa*\x001dbJ7\x001fJXLékJ?@é'å\x001aè²_ë
!îñe\x0016\x00130ô\x0012\x0006z{NÓð\x0008\x0012y`ôâpE\x000bófk1e¬)ã\x0008¥JÆÒéIQ²+Äyu¿°~:]¶\x001cyX.æyÊ{U.wðóöbÌF\x0005én\x001d\x0014ÔÔï
ÍtççøKÌ3×R6*Hwë ôSGð\x0014·¦v6rQ&J£\x0004\x0013Ô\x0001Ùè Ý­\x00083\x000f¹$LTÇ)£cJ)Ý_Eé\x001aJ7@Üþ<Æ?$ç9\x0017$LÇ\x00162*t\x0007Àl\x0014\x001eÐDFQå;VS·\x001ea\x0006Çÿ%L)îY	Í={®\x0004&MÒÍ\x0017(`\x001e\x00070ý\x0007õbÌÖÕ\x0018¸ç:=¤ó>àéÇìk\x0004Çû£¸þ¢CsÑaà¢k3\x0017FÅÜB\x0018£cQj­\x000eÀØÜ\x001f\x0018¸?`tÞØ\x0013lÒE\x001cðIn=ßr\x001dý\x001a\x000b©ÝVÖ.üwßq}Ab]æ´§'g\x0004Zÿ\x000cùs\x001b¡\x0005ífj¹Î ¡>\x00085"ô#º\x0003¨Pç9ÝÐ\x0007\x0010ÄXI\x000f"ÖØHnáE¶tÏ©\x0002,;CÀÞºÝ¡È\x001eFS3n1ÒÈ«À_ÚªcÕ¤\x0005)5 zÕ¶f´ýÄ°\x001cÑæÍwô'¯÷~&ñÜÁèjF×Ïô¸e9&Ûí²a*iSÜ­Ç{\x0018}Íèû\x0019½,(®S»Nø]^Ã\x0018jÆÐÏh
7\x0012#\x001cg\x001dn£\¹yåô Æ\x001a1\x000e\k/¶;ü\x000eó%A.MÑ+\x0010«÷Ãä°
|j[®uÒBÊð§\x0016
î­ßm\x000b{ [#ÓkeèãQ&·	Ò\x001bG´ÞÝ¦°\x0007²13ºßÎ$
Éi{r}¹\x0016Ë;\x0014ýHáîµÑ\x0003vÖä$R!OGNÄ Wë\x001eÝØ\x0019ÝkhèÖØi¶â$GÌmZ1åc¯flìî54é¦\x0000ïù¢,b^@¤(\x0015#v\x0006Ö»=º±3º×ÐükäØØ\x0019ÝkhHãø©Ru*uñ\x0012M\x000b&Êy\x0003\ÆÐè^KC\x001aGÖÑ\x0017$_Ûk'h×íÆÔè~[\x0014¶¤\x0004#\x0015ße\x001du(µc«=\x001fhl
ôÚôG-5úÚ\Øä}ùØ¸Ú\x001eBcj ßÔPm WDê-ÓüêR"ÇPy\x000fcû éµ4¤}4»¹ISÀ*«\x001f#_ËØX\x001aè·4à\x0002otö\x0014ØÏ.EAq¦\x0016¤\x0007²15Ðojh\x0010\x0012ÆRoiKLE\x0004iÖ36j\x001cúÕ¸¦X\x001f§J©ÓU¤÷bkT\ÿµ\x001b\x0015	ý*RGGMqùÖ¸cQ>ÅÓU3Ó=Î¸nR¹S´~Ð\x001b
Pü]\x0012°°*p\x0000\x000c+¡­Áù\x0007ÁGÏï\x001f¾Ü}:úþþaéñ,1sTK¼uäÔ~zÏ<\x0015¥7æòê
e\x001a/¯\x00160CÍ\x000cãÌ´K"Ëö½H²èÏdöfñº±fÆqf\x001bK'ª\x0012\x0001öZâéÊÌVõ2Ù3Ó\x0014\x0008Î§Ðüv>\x001bVÂ\x0008Q6.\x001eÙÖÌvc\à±èÚÈáÌ\x0010CØ\x001btí\x0002v5°\x001b\x0007\x0006Ô\x0000mÁAJã¾*Ü^`_\x0003ûqà(»½\x00038%5\x001fQ{ÉXú\x0003Þ¾P3qfeù
\x00104íøÊ'ÙK4>¸§­9ÖÌqÍIÔ\x0016õ]Ã\x000c¢åötjt2\x0010ÏÖè×nh²wÈ¥\x000bÔ\x0005££Þ»\x0013¼=Ø
Ô­	\a\x0003-r\x001diºyª¸?N^±ÑèÃA7öD¯0(({á§"\x0011C\x000784õº\x001e\x000cºQÎzv¦\x0005
¬ìÈ :É²\x000ea&¨Ñ\x0001ý>Ù­²¹bìæ·?\x001f]Ý?þ²ÌsFqy´J\x0012&4p£¼ÒæjÛN^¾:ºº¼m\x001c­ ±Ä\x0001Hl\x0010¥F)Í\x00001ÑÎÏ\x0014wA\x001aÒHÒN}êÓûÂPwÿ$J/Ýë\x0019ÑEéjJ÷Q¦÷Ïß\x000eaòÛÏ~ûóÍçÏyÖèÛÛ_n\x001fUÒv$®Ï FÒÈù¼\x00121aFi½|uòúuCúöôêÅéÕjQ\x0008[^0ä!0ÃÔ`òwÊ§\x0014k¨\x0000Ò\x0010²­í
d£§9#çîáj¼<¡wz!­§~¯\x0010·ë0±øúßÿù_\x000f¿-|ZÅO	xcµÇç^[v~tyõrßecN¬9q\x0013J²¥ÝÄ Ò!?\x0004«©YÍ(+LsÕYi0¼ÀSÓO÷¾ß²ÚÕ±zòÐ¹kÖh±\è­(²0c¹:Y}Íê¿mÖX³Æo5yü[Ï÷ôlnséøãÑùÍï÷w\x000fË`%xò\x0011¸ø\x0015Q'Ï1Ë¥ã×Gç'o/ÏæFtÉÖÏF®ÁFÑþ«ü-Ñ³µ\x0019ë¤/ÐXCã
èÚÿ2\x0013©ý¯Ý\x000em\x00174è­øYúÁ°q \x0012ølÎ¨xûÔ\x001a ã\x0012Eö$+Ö¬+\x000c\x0004´<#\x001bÂªö\x0007 ²uPÌê\\x001e\x0004O\x0006\x0002\x000bëÞÍRT[£\x000eÚ\x0007çý±çp\x0012Y\x0000\x001d6¥\x000e{û\x000b²úuÐ>8;M½Î¬@£|&­\x0010äÊÌL,½5Ö¬ö\x0014\x0018p\x00127ù·A\x0014¸3h×VÜÖ\x0002¨¶Zu\x0016z´0­°ãV\x001d.@·¶\x0004è=QôùúiLSc\x0011L³±`Ás\x0005º
¾\x00048fJú0miG01Ð
-	ÄxiÖ³~º\x0002}\x0001¦¯1ý\x0008fºôy\ÎÔ±#m&`å«£=ÄW\x000f5gèæÌM;.¦\x001dm¤iÇ¦'KåæÜ\x0004<\x0001g\x0007(æ}_5Å@\x00174Å,\x0000mn»î¿î\x0007iYÀÙ\wÝß¹1\x00069\x0015éó*­Æ'Ê\x00166\x0017^÷ßx\x0002
<j¬mÀÖ\x0005®át#Ô\x001c\x0013Ks\x000c÷ xg\x0005\x0014Ý\x0001\x0004
­=\x001a9¡£ïè]^q¡¦¿aÊ ìÉ\@ÙO\x00189:¤	0N«É§Äb
\x001aµ\x001a\x00075ï¼ùðÓOÿÁ®39Ì4?ðæËÍÃO\x0015ÙÀÑlÁKS$\x001d§1\x001684A3K',kÛV\x001a\x001e8
\x0011<ysrõýÌëÎ¼ûõ··ÿÎi)¹Â\x0003ä\x001e^Ý~¹ûrôìöæñÃ¯·_ S¢%Ýq\x000ex'³¢ÇRv6½UímøxÜõÑ«Ó7go\§wéÜüMóÎ}øbJ]DÕÍ?Ý|úéèÅí§/w\x0012$êij\x0013	fÌä\x001eæd\x0017óèYmiÌÈW¨ü^NÄ\x0017'\x0017ß\x001f½8½x3;Ö¼³þË_?}áDÐþ9¿9:¼û|ÿåËí\x001f:ÊCI¹é6Ê[Ó!´\x0013
ò>9:¿>{}ùæÍgiÞ½WP7êwÏ¦¢­$z\x001eçi	Fö\x0004}Þ\x0006$è\x0004\x0003ì8'G%½sMÿÉ¬ô
(Ô 0\x0000
´Éo$\x0015\x000cæG\x0011BÞ¸¢Ö`\x000fÁikN;À©\x0003¢\x0004£ÏGÆse¦¯ÿõü\x001at÷â
Ô× ~\x0008TZ\x0007
uÈä\x001cj\x0002\x0015-\x0014]\x0002ú¤DC
\x001aF¾|\x001eÎ7}zëÙ¿éêð-JæÆ\x001f\x00024Ö q\x0004\x0014%²d5"5yL £N[õµâ\x001c\x0000õï>´\x001fÿÃ\x0000«¶üJ·Ip°1\x0002rsS²¦jí}â=ÚåFÝÉ\x0015}¾RÉAr|\x0000\x001cÏ\x0000±²unµXjÅúÓXã´².Uò8Ø ÑÆQ\x0011«Z£¦C­\x001a½O?ø®]²Ð4\x0001Ð|\x00006u\x001f\x0011,;ívHµÚG!&êIT¬Qq\x0008UÜ+¢\x000eå¬²PÁh}\x0010T[£Ú1TéL^)tL¨Í\x0014l%óQ}êÇP\x0015×´'ßÄ\x0014mZ|\x001d\x0006u4Ö¤qTÅBÞí9ëH\x001båðkK5Ê!\x0006¹Ujô¬æ¡²ÝQXùíîÀÃaX[
0¦\x0002h^Õô|·&é­Èz\x0015x¢¨3*|m\x0003FX\x001b\x0015 \x0007ub\x001b0yÒE\x0007pb\éÃ\x001c×MAyÑ®[+~\x0016\x0013{9µ:ðBìÉ\x0014*ØJô\x0012¿O×*lKV´\x000c=C?ç\x0017ßç\x001bûü\x0014©.%ÆYÃÍÇ´ä=Á)9öõôu~ë½Î\x0019±¹J\x001a´ò\x0005&Ô~V0æn!ãâ\x0018^\x0004SXã®'ÕbÖdU#TúÄÂó^O_îï>-°¯yó\x001d9X`yþmrZ\x000c_.egV^\x0013prñæòìbÏy\x0015PWº\x0011PËû	# \x0004\x0014ânÕ	êkP?\x0002J\x0003"QST\x0000uï³Da÷ê\x0004
5h\x0018¨ã.'CÔÀ7ß8\x0001Ua·kÕ	\x001akÐøíJtcW±²«Ý"õEjËPHmÇjøúÚ\x000fBC
C÷ÞrªÖèLy¼è\x000f"Rl@q\x0004Ô\x0006®1^\x0012Qá
{ÌÖn¯º´Ñ¤zLzöS\x000c­èN*AÞñ 2µ
©ýeÚ(}=¤õÓÕ·ÙÒÄk-1\x0015ætú\x0010ÆI7:_\x000f)}ë¹Óx\x001f¸Ä7IT@w½§\x0007@\x001b¯>õ³æOO;0\x0002?§<J \x0015Ã!H¡Ñ¥0¤Kõ\x0014HÖ×Z(,S\x001fà\x0010º\x0014\x000f#\x0017?I\x001fþÆQ«#rDÓÛµZ£¤Í1±cú/R¦õë\x0015ª<Oº
jä¸¿1ä\x0005djä¸Æ\x001daêåÀÉç\x000f[	
ºcS³Q÷KrQÔ!½hç\x0015à\x001dQA*_|òR¿vNÓ¿s\x0016êro\x000eJ u\x000b9Bé¸íÒ¹ää®ö ñIow<ù·\x0019çâýÓ´øM¬úy§yBIó dy@²<³±¾¯\x0012\x0012[©¨\x0002èk@ß\x000bØd#¢èù&\x001b1¸Õ_dJÑ¹Tß<>Ü|úðô­}i0u¾5\x0008yMâtkv½>¹fôüäúêäâù\Z\x000fÞ=<ºÿóÓgF%À·÷w·G\x0017·¿\x0013\x0019°\x001f
\x0013ÙÝíÃç?|¾üüW\x000f7?Þ}"Âdoâ4ùßyoÐû<\x0014)¹É<NC9,\x0019ï³Ó«×G¯/¯ÓÓøêäõùÙÅwo/ÏN.N¯ßÎÝë0ý¢fn\x0008mzzB^l!¯\x0001SÎ»!B¥¢»ü¯\x0006\x0004.!E5U5%AjÍ[×£1)a³ûákÌ'§\x0002TXcnOÔXéyæY"\x0005n(K¨6Ç\x0013ª+-zëPMº=Wc\x0011ª\x0006O3\x0002'Tyh\x000e¤·g®\x001c¡ml¥\x0005r\x001dª­Q·'9-D\x001chJ¨VåàhBÕyí_B%·\x000eÕÕ¨Û@¡ºugBª5(x\x0003béÂ+;ã{8CÍ¹=\x000cä\x001bâ5çöÈ¤E@cò2oö-'#'|ÓEs\x000b%,\x0019õ«1}ËXÏ¥DI¦Tâ4¡&s/¨\x0008óÚ´\x0007U7¨Û\x0013¾-±6ÿ«}ËXIQeío´§-ï\mÓjÂAn¿nÔÿW³û¾-¹6úÿ«\x0019~ËX¥BæÅ³V\x0005ÍJ\x0015iþjÔ²ÝWô?ýý`yêW.\x0007\x001dI°\x001d\x0015\x001d\x0016ÁîvíkØw?ûó\x0008o©K áz¤péF\x001bÃJãÚ<E`û)òñæè{êÈ¢\x0015:Ï\x001eîî¿|^ê\x0013FçóTBoÀ@ö«ÁÐà®£WcÙ\x000fÔ EKu]]¾KóT¿
Ô¿
üþU°þUðÿs÷nÉÜØÁîTö\x0004û%ôÄ*Q\x0012;X¤~VQaûEAIÄvl³mÉOßþÇãqôL<³\x0016°\x00166°¹@fù´#XÙíÒ\x0007$°nX­B\x0005\x001f¬£¥X\x00122èy!¸f)¶^Ýd)Zäb`\x001cé²{©·\x000eiõ¼\x001c[;¼+®\x001eÚô¼{{ûüáÃãýâ%¸èOÈ\x001e\x0005¹äó
ð¦³cçç¥Ñ¾DôíéÍÛ·è¾H®jrµÜË\x00132ûp {¾\x0011F
ÇF¿w¥FÈuM®×\x0007Eì±hMæDmeÔ¤Z¥ó7`\x0004ÝÖèv
:×ãË«MÎD\x00027Û\x001aÏrhSp_ûUà6î\x0005¨KÁ4\x000c\x000fð9Wb³Ób\x000eo¨iµÙ\x001f\x001f¾ÿùîiqd#\x0015lQÈ ×&y©¤*ø<ú^Èüùê\x0012Ö1Û/§BW5ºZ.l~fÁ;JSì@> *yôÛÛÜ®!\x000fN(\x0002W,\x00163¤nÁ8^"ØûÜ¯"×\x00145FôÓZ\x0001]«\x0012\x000c1Ûnz¬Ñã\x001aô4:\x001cy3²á\x0006\x0011Ù?bÆ\x000fËö®º¤(\x0017u(\x0001R£I.\x0006õrt\x0004]7èz\x0015ºóåâ,¼¬H­)Þ\x0013|MÙ[*W]S/hì\x00138'ÞðÁ\x0008°\x001dj¿È,^À®\x000e*'p=>\x0004øÿùÏÿ:}zº{ÿþn©BÒRx6\x0002dÜâ«Q³EoÍ¼_u}uó\x000eàw§××g\x0017\x0017³c>Ó\x001eC}\x0014H\x001f\x0001-mûåãbwPE,-£\x001edN\x0005\x001e¢çã"Ê\x0017À¥]¿¼:î\x0016C\x001eH¦kéÆä\x00024\x0004\x000fE\x0019y¹\x0019øÿèÙÿ^ïsj\x0005\x001cu0\x0003d0¾l»=\x0012ï¡wöà¼8ÎK>èw»o\x001ezºûmñ
Uæ\x001e<,Øºl¦\x0007v\x0011Gz>æg»o®n¾¼>«`H;\x001c\x000fyl¦Ù~Ø}sÿÓÃòë©Í5³\x0018ö°øZa\x000f-ù´è\x0018_6\x0018±á×ùÇïg<4ºb3Ö¶\x001b\I>æÆ©\x0012\x000b£J1\x0000\x000fGL\x0001pS\x0015àø
Ê²\x001cCú9¯ÊÛG^q\x001fÔä©R÷úéöþ°×Ç"pgi¨×Xò²4õ*ç\x0008¬Í\x0017,¯¯OÏ'»~ÌbSº³Ú>Ë
\x001c\x000fy\x000eEzÓ
ÜØyY~H~ä¤ØÃb¢pàÅ\x0017s\Òâð:¶¸èEÚì{\x001f9-(\x000f«×ßé\x0017týmü·àß\x000c\x0016Ø\x000füÉEÐXûüt÷S®Í&Ckzâ¿{øÓ»§G¸\x0007\x0011\x0004FÎ³ç\x000cNui@æÒ+0m«\x0011Îg»w×Wp©\x0000\x001aë¯Ï¾¯ÓÖß~üëwýá×\x0008ÍÔuÚo\x001eß§¢çãà¡ç\x0010\x0005\x0016Da\x001fç\x0013\x001dS0"!\x001aUÍ\x001e9D\x0004çøÍÕÍÅlÉ³þV<ºïÿC×Øµ}:äÓ¯äù9\x0002öÏçòq%¼©Ru÷pÕÎÍ}Ü\x001fT?Ö;wq·|Ï°\x001cËÐÜ\x000b\x0000öÌFÃ{VµWÛcaW¼[sT?¿ÿùÇç§D\x0005\x0001þ¼\x001b7åÕó\x000f÷@ð"Ân9iÊu\x0004£[æ±áÚ[jÂ¬öb
.]\x0015¸\x0018¯nÞ¾=ßÌ2µnþE\x001bìxõt÷ÃãÃ\x000f·9wì\x0005^\x000bþjÎ\x001e^ÓSNý\x0016rc\x0005\x001c¨0Á»·ã_]}~uùùé|\x000eY\x0005­kh=\x000emc&ÆÞÜ1\x0013\x001bCW\x0006{®lGlkb;N\x001c$e½G\x0010üÙÏ\x0006hoéÌ
5u\x0006]ÍìÆAØçÄbØhÍH
Ö<o´ßp£}
íÇ¡czãMÐ!\x001035W8iNoÇ\x001cjæ°9R;q8\x001c>Wm!tä³QeF®e­Ü\x0018\x0017\x001cÆKc¢ò$3K!ù\x0016\x001a±Ý¦<\x0000VãÐZQé\x0018¤Í©@\x001açºñV;¹Ý´ãâÎ\x001bGãc#ö¶K½GtÐ4\x001e\x0011|Y5\x001a_Mm\x001aj3¾×v¿×èØ¼×©EðSÖ× u#óä¸ÐsÎÑ(Ê\x0018Ï!" 9º\x0005^Øò26\x0002DK\x0010À¥Æ¢i\x0000RÊ\x0015ÕA@·Qn'ô¨l\x0018g\x0006K)\x0004DìÞ\x000fµRe£MÜîP«Fê©q©\x0017à*lÞáÐR\x0005Ñ6\x001aæv\x0002D5\x0002D\x000b§ñ%jlX%3µ´×j¬³\x0001uc2©q	\x0014KªÄ4ÚÄ\x0015¹¦Qáa;ÓT5ö\x001a7@"\x0016Ó	\x0013n³yjµ!«I\x000b¹ØS±¡ãÔÆçÒap[DÌE$@í-¹ÊZm¨Îus\x001bõøm^\x00104\x0016êf
ãá¤µòµF=R°S¼¶@·CÀv*¬ÂÍG­ÐèÓ[lx,Ë½ÌÆÈ²¨CËw\x000f?Ü=ÿíén÷áùi÷êöéÃËðZbË¡\x001cWQ(º³ºáQ2pT¤%´|vùùÙÍ7×g»·7×»W§×o\x0017¬A5kP«× ÝI¾¦JaÁG^\x0002uMÂ ¼¦«`%ÕK°.wÒ5\x0018ê¤\x0006k°.­ÑnRï¯¡äcÒ\x001ar>æªU(©È´u&wYÂ\x0007DÁ%îþ\x000cÓáÜz	\x0014Î­\x0017q»r\x00151R:lIÓÒ@\x0016áKKE3þÐØ·hzÒç_PÖÈþ¡ëõÏ·Ï¿.ñò]ÖW8RÐ°ä\x00073Zº9%»ÝzýÕéÍ?½L\x001bjÚ0H\x001by,bÔVçè9Ð\x0006\x001ecã±\x001a{q+)K«n^]¤WÆÜD\x0008ÝdK#>1]q#Þæ0ÈÁÓmBsCí¨\x0002Å\x0001¯¢®µ6õ§¡N§Ì¿¨ãÿóÿuöÓûû%wÎ«ÀíßeÊÓ,ÒX\x0017¾þ^îÎ¾¼8?~ËÜá-s\x0007\x001f\x0016\x001aEs\x001b£Óö$\x001b*`¿Rwe\x000c¡lAjjR3F\x001a¸\x00058ì)M×AFÐ±\x0004²\x0002ÕÖ¨v\x000cÕzvÕ\x001d°qTú\x0002i[ºÔ
\x0006\x0019hØRtVrôWGI×*JqÌ×]\x001ajÔ0j4\x0007ªµ9å\x0001\EnU\x000f¨ú»\x00185Ö¨q\x000cU\x0019jw\x0014¹\x0004\x0011w5Wq\x000bTÙJª1Q\x0015\x0000\x001e-0ÂD¢Ê`#³*},D³µ¹Vrì^\x0005g\x0001\x0001ªÍÝd5ö\x0016áÃªÔ±`ÁbÔæ^É±\x0015AZ\x0005U¤\x0015\x00056À\x00034,\x0003&_ÛºY}ÃêÇX¥ÃÀ\x001c\x001fWK.¶Ò|\x0004dØä\x000847K]-ìÌÄÕWAëµ)\x0002k«¥«¥®\x00168QÄ\x0005ÌÌê¼u\x000b= Z3`È\x000eÐB\5\x001dÀò¹
\x0001X©å]\x000cK´ÀíÓ÷w Ôff³
Í¿§Çû_w¾»}Ø}~ÿÃýÝÓËg@Ew%\x00122×¢kóuÈ\x0014Ó\x000eòM6\x0002¯¯Îÿi÷ç³ÓËÝççÍ2«ÈUM®VTÈ
rR\x001b< ·4\x0013Îöl,k\×äz
¹\x0006\x0019¡òYÆV>£{A½\¢Á.é[¢\x001aÝ¬ÛtÇ¯Åx^,\x0017°ÌÊyÙv×mnWíº\x0016xJÒ®[P\x000e»Nå¡°ë~Ö<\x001bCw5º[¯°ù¬K8õ1ozÐd­}±í%
5yXwÔ
[ïÒ	r4à¨KÍîç¼·!ôÚ×ìÏ²ã@ÒÎ÷R19¨÷mÈµ8éX­Mçy÷æöãS®Æzñ©^³d±$""«\x001d©f-ÝSø¿gË¯*LUcª~L\x001b\x0003Çv¬±1UÁ[`\x001aÓ\x000c`ú¬\x0015­"À2ÓÇÇÙ#Û\x0003hk@;\x0000hsIO\x0000u!r¹ Pjj°\x0019½·Ý:(]Mé\x0006(¥*ÑÂù¤ô\x0000a\x001cÙ\x0017Øêj\x0003L_cú\x0001L\x001cL\x000f¥q\x0003x`eÓ¡ôfþ©\x00033Öq\x0000SÓüÖh¤0\x001f#ÏÉöj2Óµ²\x0012¡õà¶.LÇG3·H)¼æÍõ,;([q9 /­â\x000eåÑ(»Eh\x001c+ÉGóH\x000c¤³rD`\x0002ÊÂ\x0008OIþêÏ¦UD=À#\x0012Sh¶j´©³
`:\x001c½}t`6bSÈMIÏ \x0012\x000c©lD/Ë3È\x0016ÊG6RS\x000eM\x0013âÉ:¤fïÓÁç¶¹BÔ\x0003bÓD{0LMiÒñ³ÏÑíÀl¤¦\x001c\x0010&R\x000fÀôO¦-¯I~û£\x001a©©\x0006¤&ø\x001fl*c¥QÎ\x0015(SÜ"6"Ù\x0000³\x0011j@lâ7§4E
\x0016½ÑüÑË7ßb7[+s@j\x001aã9ã]á`l¾P®\x0010\x001bÜô*w\x000b9õÈMwåéP§6ôi;y\x0000Qtz>\x000eÛÁÙHw5 Ý±2ð±m\x0011m§¡F\x0011\x001bænÙHw5 ÝwÂ_b-öþLÛ©4\x001fÏMºj\x0004¼\x001a\x0010ð:::¥Ö¢\x000cÆ0¬ßd?\x001b	¯F$<x\x0019´
sîsÐ$DOûiã|zo\x0007gh8ÃÀ~æðÓ\x0012Üñ4\x001b>Zç6pÚT£Ô*\x0002«#xâô¨ãÓ~j>ÖÏ§¦/çÔ2Ò\x0003Ê\x0008gö\x0010&æ\x000cRðCí´víÔ2Ò\x0003Ê\x0008Û*Ð«\x0000vô6t,}\x0003©\x001be¤\x0007ò²NLH£\x0000±\x001c«6v\x0003!¯\x001be¤\x0007\x0006w¥\x0015\x001còòe7í\x0016\x000fÝè"= þ¶³QFz@\x0019imø-0M\x0017Ê§ÓãÃ\x0004qn)Õ|ßKÊj\x000f­4¹\x0001ç´ä	\x0018ðä\x0010;ÃÔwF¿ýîà~×On°/¤H­ÙnáÅÅÃ6²±&ZzbÓ^S¤\x000eÜ\x000fÁ\x0016³[\x0008)]¥;æ½\x001dØØH[qB\x0017¥z¸YecíìÛå\x0012TuXP§l"øawñøü7\x001cÖ¶\x0000Ö£LV\x001a\x000e*ë9Þ\x0010Â&ÍIlow\x0017W7ßàÄ¶\x0005Ä±&ÃÄ!0±5¹\x0001&]\x0005:\x0008AMgÁ\x0010WA<e?kò\x001aû½ÎÎ\x0018­§qÓÀ¬h(^\x000cr®\x0012fY5Ìj\x0019ó°È(°.ñ\x00124Ödf=§Æ\x0006MÃl])í²Açi4:\x0018Ëqrð´¶c¶
³\x001dfÆÄts (g;	f¶s¾Á\x0000³kÝ0sPd×ÇÊ%
ÆÌ¹'à\x0001bß\x0010ûQâÃT	9FRvàm+\x001aÓÙÿ#Èª¹jô\x0002j\x0001ÙS¾ðü\x0000à\x001c;9\x0001§Õ¯fÖõüö>oîßßß-É6gÀ@\x0003oÜW\x0016¹LÇ)K­jóæüâüìhB´>ì mÝë´\x0007W;Í¯U8c+bø§<³\x0016Ëß'_zGp}ë\x0007q<É§Á\x001bV{ÞE.ðKçn\x001bÚPÓAZ8¼J¶lÊãÊ®¯å³ '#3\x0003¸õC[ÖÑc»k07o¯å\x000c./dÙ^=õt9ÂÛ\59x×þ×NT­ýñ7#Ô
ó#©\x000f\x0002xTÁätiì±P>Ì¤õ\x0015â)1¥&Æß\x000c\x0011\x001bESã¢\x0007½a·yÒ[\x000e,\x000fÛÓÈÔæë÷·ßw§¡:¥¹DÜz~ø\x0008\x001bí#§Nð×\x0017§¯\x0017'w\x001eê
tÅ .àu)NdZ¶z¦ï\x0000­®iõ(­)Q\x001b]j
¸¶$£ºÉ½\x0001\Sã\x0015Ëg\x0001_\x0014-W&Ù²»S6å\x0000®­qí(.hbJfr2âF'ÜE\x001fÂdúì\x0000®«qÝ(®UüØd}ä¤é+^Æn\x001bÀõ5®\x001fÅ\x0005c]p=U Ì ¨5\x0000æýoD\x001bjÚ°â,pª\x0013ø\x0016\x0014ã<Áê)ç¢\x001f·ÎqÌvÃ\x0018¯ç9â\x0011ë-}¤ÝÕ,\x0018¦ôð\x0000m«#Då¦\x0019Õ¹\x0008Ég½\x0001ÚFEÈQ\x001dáuêùåCk\x00169j2éÿüö¨òÀ£\x0012×Õ\x0014ÙY\x000b,Âá ðÛè\x0007Ù\x0008\9*q½¬Ï°\x001aÔÒ90¦Ô\x0002M6%\x0018àm$®\x001c\x0015¹\x001e[*Ò¹U.OO\x0004^gÙ¸	q­0¶©Z\x0005~Ø}ýøðqQ^®âÚ59æÔ"0Ø"¾\x0014Y½Ý}}u9;^¥T5¤êô¥\x001dSÅ\x0008ëÊÅ:Òâ!ç;\x0007CÃËTý\x000bC\x001a¹/XvÜ°AÈ°¯\x0003/«Z¼¦4Ý\x0018uÎí =WqÄý%ªªÐÖ¶\x001bÊc2\x0003¦å±c²µ2¤OZ\x000eéjH×¿NîÎaû¥´UZÍÉ#ý­\x0016Cú\x001aÒ|ëÒ\x0012\x001fM\x0008ÒpI¢?RB½üfûk{·íþà\\x000e"Óø±\XE\x0018Ãßqu\x0008¿ã¼JÕ! ÏpTðîõíÓÓ²¾P
<
4\x0012Aç\x000cvD\x000cb:\x0010g
ï^ã<\x0017ùJ:YâC?²\x000fÇMäDa
)\;9oøÄªYÀGðàJÃ´UOWO÷wï{:©h\x0019r"LÄP9§\x0011zrú\x0015frMª\x001bî¤òêúüìbQ\x0017\x0015B5z\.Áp6Ô\x0004FÆÜ\x0013Ó[Ã=´Q×iÜ4äf3tË¦ÀN}xfÚ¦ÎÏ§ªÑÌ9xsûÓÃíÃÇ\x00056¿(\x001e±ý?\x0011\x001d×;\x00189ù(Æ¼oN¿¼<½'dö°ôÊz\x0007\x000eÃúîñã¢j1g,§¿[©ÙÐEùÙ>véÑ\x0003'`½ºzw¼RÌ\x001e`Ù¦!P\x0017®Ö4¿==sTÍq!8!3æÞRÜïÈr/Ôìg1w\x0001Or
»0!ÛîìaGl/\x000ba,(LB\x000e}\x0014òZÁ@ ×
¼ÖI\x000bf»§\x001eL\x0007ÿÑû\x0017\x000f¶û`DOG#'N¨¢Ì(Í%áóé&\x0015GÓK?÷Û¹q\x0004\x001ajÐ0\x0008
\x0012\x0012\x0014\x00058±rú=\x001fãéb	Ô¶µb$Ù<ijÚõ½dks¦\x0016ön¬lN\x001c=\x0002!r\x000b.8£y|Xê\x0005ÈëHå$Ë£^O?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-06.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=|õýÓ?ÿôþÇ\x001fÏòðDþÑ%±r\x0017$t(ÿC\x001a§o\x001e¾úüÙ«?óòë¯?EÅÓ`ß\x001e>gÏ\x0000Vh¶é\x001f]
Î	ÍvÊ»\x0014&Ãg\x0008ú\x000caö\x000c.F^ñ|®ëºè\x000cP¢v¢;Wÿ\x000e¨\x0007þ\x001d\®s&U\x000eâæ\x000fÈB%pùïpKe×3d>C\x0002Ùùá\ánjßâ3ìwR\x000c!é3¤ù3pÄ72<X¢1ù\x0019`·T<x
ç<\x001d¡rÎO\x001eÁuÒ¡\x0008}¹»\x0007Ï\x0010ú\x0019èsö\x000cXÙé\x000cXbHÃ¿\x0003ò,Sù?ÙõóÇÕÒ­7G\x0014Óéó	-È¤!8\x0016¤¯Öâéþ\x0014O§\x0000çh¬\x001eÌEÓMÖH¹-çÝ<úÀ1°êÍ£À?mYT~\x0006¨90:\x0000¥Xø\x0000à8Åbm:\x000ew¯À·\x0016¶ð­
yGð\x0017UÔ:\x0008R¤áñÖ¢\x0006\x000bÓÖ\x00068tó.á¿\x0011ÂTü[B1\x0003íeQA1t/)_n(÷8Vt
¿O
¿Oø³ã\x0006¢TÂ0\x001a\x001e®NeGÏÚÃa¿kðo
;\x0013:äã\x0019Çb\x0013ô8@~´Âô\x001a|eÑ°Y´9øÙ\x0012±(ð¨\x0003\x0011\x001e{´Ôý*|¯áûIø6óB\x0014n^ãÅBÖäÃNêkð¾}7{ûVÕ\x0012­\x0008eçÚA\x0012oÂ\x001dr\x001c^Äo5~;¿Ü¹co\x0008e·H	Ò|\x0017Ã\x0008ó
|\x0007
¾Iøh\x000c§\x0013Q¦ú¦:½ç\x001d/öï"ü¬áçÉÛÏÀ»ì\x0013úJ¤Zá\x000b\x0008\x001bx-®áGeyésòúA\\x001fÒ=\x0015¼\x0003ñàà8ûy	T×ÅIË´{ñçH\x000c4
?å\x0018â´]ßë×ëg_/¶yd\x001f\x0002qTøS¡Ùù¥ºÓ;Ôè'
/:ûÈ\x001f0\x0015ù ÅììRá§æË-|ð=pe<y\x0014SVüù¡\x000c/Å\x001fõõÇéë\x0018øñ\x0006!ið©ÄÊã]ë·aP¦\x0017Ã¤éÅìy«xMF\x0004\x001eË|ÿéøà\x0012þ`Â\x0016?}Ná\x000f\x0016Åq+¾òcàQÉàdWg>.Ö]Ã4þI·?ØÈÛè\x000b~K\x0011LÃ/ò\x0013óÑ:úøQÉOÀIù!ªVn\x0000²Ã?ñq¨\x0008Ôuüi¦¬]?1hððd°LêkvWÉ\x000fÊòÆ0iy\x0003-ÉæýÉã\x0016ºå%*øQ\x000f}Îá/ÞfÅÇVv5vâ,\x000bÒÚ¨1Yå9$;é9\x0004pP§EÁ\x0007ACß3\x0016\x000f'Ì®á×Ê?M+ÿ²ùý`¥!|\x0007Ñ=æp^û\x001aü¤|\x0007ú\x0014ÿÀãIE| \x000f³\x0016ÏSÄç¾ø\x0012þìøÐç¤ãéeM\x001d´lqÌ·D\x001bOêùÒç\à\x0005YþËKBî\x0000\x000cÎFiµYã\x000c\x001c\x0003­Èañé®\x000f\x0005òz\x000bÃà'¥ýsÔþÞGöü\x0001mO âþÀ\x0018ü¬o?/¸}w»~&ù)×ß\x0017\x001b\x001er¡\ÁoúQ\x0019OúÌ8³ßCd \vA1]ÄB½\x0014}¶\x001a}µ]ä0ð^ÉÈ\x0007m×oÅöÆCî°K\x0007°:ieílÖÊ\x0019#»¢¡xþ\0
Ì·¿Zy\x0016\x0005w\x001f'ñC4<ÚÊ[î\x0015/'­Lq­ófÁè?ÉÐ\x0017\x001cð(c¢rpÃkP¥x`)~§ß/}Ïá÷²u)¹\x0010¥-Å ¡/.
}-àÝ\x0001pú\x0000b¿\x001c\x0010gÆà_Zñ² ½Ïú=¿8
\òrÅãNz9ö×ô\x000e\x001dÀªºÔï©\x0003ØXY¥jòÇ\x00027õÑ~Ri
2<òWKÖÛÊ{-Z?Í)Qx&/ÅòY¢Aª¦Ëm_ÿ\x0019TßÐ/QwÓ·_ÂI\x000eÝ4´æÃ 7w?ÄÉ\x001f"·Üö;øûêûÚ@ð¿½Ãÿv\x000e¿7²Ý\x000e\x0000â\x000f.H«Ú\x001flÛzx[¾GónwË÷Þ<}8Ë\x0013SIé:g'ap1¾FV\x0014À\x0019&æg~öêSD1\x000c;-ìl&`ç¾4Sê*7ØÕ}ù<
»8\x000b[Øô9;æPç\x001bw¾çY¸" ²tÈ ¡?:kÔSBb8VÏR¶Øn;\x0004¹íS´Nâvú¶Ý\x0018Z\x0014Úma\x001b\x001b­ìÂq& p:\x000bÛjØvâº{dÙ¦þÐnÛGyÇÝòçaßè+ì;&úk°£íª$ SN\x0015&à\x0019Ê©¸£Æ\x001d'pC±>,$(ÌµÑ{Y¸æÜ\x0019bµs°Á()\x00013%%¡\x0013Â¥ØvÛv"%§Öø}>*lf¤\x0004¹æëfÖÜÁËÒ¤pfyêYÜYãÑhnÜ·¬\x0003EHÇâÎ£F§P£¹íÖ1N¨Ëm·\x0005¤¹³ØÝEØ\x0003¸QãÆÛß¨+D,÷tÛöL_ç+§q»ÛöîêM8ãT\x0012Ò\x001b;îÜí{>³¶à$î ,¥\x000b\x0013\x0012°Qc\x0012nï»\x0012,Ï9\x001aMZæ¸¤q§\x0019Ü)É®*ësÛê\x0013Ñ¢À¶÷\x0005ØVÃÐÝÖºËþ\x0013ÿÚuc\x0014ÚqfCðYØ aÃ\x0004lp´¯¶2bZÓ#\x0006+ûOÂa»ÊyØYßv¸íb\x000bk¥²Þ¶¡±fáH	\x001cv9]Àí4î	å]4hÍR×Í- Ê¤ø²Û'eJÐkåígw1íµ­£	2Ai(&¾È\x0013lÒ'qëûö3÷íJì\x0005;dîd-¯r³Qd!n¯qû	Ü¾ï^\x0000\x001aRµ
w¥"EbáÞ¬\x0003 Ü÷Û\x0000.áöÍD>qÞÖËq|æó­Ò'qgåÂÒçÄ}§ù¬ëP{>#æÜ¸à2}9kÜ\x0013.,ÉIn÷M¢Î®7fÙ©q]ú!h9	Srânìô^6XÅhdù¸_çÃ\x0006\x001d ÝïÝº\x0006ÚJÚ³tY\x001aûcÈ<5KûgÖÅÃ>Ür\x0012É¿°<¹Ò\x001bÅ4\x001aåA	\x001bÂºÌIQ}·¼¾èÂ§q!/F3\x0007fív]©tÖn8MqéÒî/}\x001c9uQ1râ¿iÔ+ThgyqpfËÒi÷j[\x0010\x0017ëpüb>\x0002Ä9$
½,éÔ}ñ3»*Ïßüû3wó¼;¶èHvÇ]~=³§÷´bÔÐI5C'\x001b²tÄq\x001d7\x0006)#\x0002uÙ+ºõ¿ßßúßÿ\x0010ònÝÏäR´sòn\x001a$çhh#nKQôíß§6R\x0017§{¡\x0019×4Þ\x0019Ée9è:²xåÐf4¾1\x0008tJddVµî|ÿþçÿzöáíûw\x001f>¼{øìéãYZ\x0014"É\x000b\x0015Ü*7{­Za\x0008Ü¸oáPÕ<|þðìÕó/^½zñðÙ³×à6iÇÛÄ+\x001d\x0003ÔÄëð1Lâ\x001e\~\x0015f"Â K­y«çp7Ær:\x0007}Î#ÆøÈÓÇYü³â\x0004#Ð\x0015Oç°öê1BTÇ\x0008qÅ1×Ó*\x0016}Ô\x0008ÿ+oD¨à¸{õ\x0018úq¸%À\x001bikð"UØ©áx óâ1üm¢áÕDïð1@f»¢\x0007êo Søä@Nq<\x0018xõ\x0018Þ¨cx³âÓB\x000cËoÜ<öÄé¿Óx8\x0015¯\x001fÃêc,\x0011ª\x0012\x0006`\x001fòu¹ý\x001aØ	\x001eüa³ùÅSà­ÂG§Àmoø\x0014´é[0\x0019îYB 3·\x001c¶,]<\x0006ùcÐçc\x0014ìÀä-6pû*
é»5ÇöÕc$£F2+FJqÜxt\x0012G\x000cå3%µæ¸ñçê9¬²\x001bô¹à\x001c!Ë\x0004 \x0006Ç¦ªP¸+Âazâò)@9#ô¹@QA"©Ê /ñ)>,\x0013\x0002y\n6ÓBå\x0008\x0015-é\\x0016]\x0011Î¹Ø¶$cé)2(>WX Ý¡D5Ý&ghDß\x001e§F/Cÿ\x001ayÉ¯QD\x0012_XÇË\x0013/ÿ¥N\x000ct<euí\x001cÖ8e8ê÷üA²L¤XÞxd\x0012i¤	b>È	²Ó«\x0007Á¨\x000f+\x0015\x001d$tÁJ®#@oU\~\x000e{[(TÏAß\x000bÎ\x0011÷¨`°³õ QzF'ç¯\x001eÃß\x001dÃ/9Fãlú:Úë)\x000bÁå_b\x0017@b#º;Ç
ëQW\x001f1\x0001Hcc\x0000æ²¨Å~îvMZ=H]¶ &G9Hp2DaÙÃÌ÷åsè¼-\x0011?\x0007Í5±`¡í7IàaÝñ|èÕ»%\x0007éûµªÈÎnp /Ý\x001c\x000fÙ_>H¼;È
ÍKkÜxd\x0008³à#X×´úlÈêA4[Ò¸Q\x000fÂyDÔÏ¾ðmíRó"Ýb¿KS»M®{H³Ôí¡{!~¢tèâä»ä%ª7&fTõAvµ!:^\x000clò9üçðw&Ä¯ÉZ¡7¯l8\x000f#çð-hÏ@#­Î\x0005N#Ò\Tf¹(d6¯þ=ð6\x001b^Ïj8|ø\x001cEIqÝaz^ìIØ·\x000fw«\x000fü Û2MÿQÔÔpÖÄDÞÿ\x001c­¶h¾£¸\x001bâÊýì<äÆ/9\x000fmàØ*äê´Ðyµâª¬L-F\x000f4Ásk 5\x000fdL~j\x0005¨/~øéû÷\x001fÎÁ\x0018
ÒÛvjN¼Å\x001cx|ß´ï-~ÓÊO_|ùÍç/_}¢ü$a\x0018\x0011\x0017Õ\x0011\x0003/\x0002(Ñ\x001fO	Øâ\x0000ï\x0016\x0007®"v[Än\x0018qò´\x0015­!F.ò;æ6ì'×®\x0002ö[À~\x0014°Í#º\x000cÙpÛ ô2ä¾¶¹\x0017·xqü£L2@2²*§[¾àÝuY\x0011Ç-â8¸Ü°á\x001bNuucE¼\x0008qÚÝu\x001dñVñ5ÔUëFñ\x0007Ú´z\x0006\x001aj\x0003FØJø`pÜ\x0003Ç	à¿\x0014C U3Yè¢¿úþéí»/þûû½ÿððâÇ·Oß¿÷ñ,ðrã-7-é4c­\x0002À~Oß}õù³ç/\x001e¾xö¿üâå«\x0017_?öùË\x0017¯ñÃ\x0016?Ìâwø±á/ÆÑ±ö\x0005\6ìæUFá»-|7}ý·dKÕ\x0005Ç×o\x0018>îoÊ\x001eÅï·øýôõ3ø¢fÚ~\x0004Liýììö­Ç-x¾ü$6îXIÊ}béÏ(þ¸Å\x001f§ñÇ:Tñ[)\x001ed)çØÍñâÏ[üyÁýçØñÜ?¯9!üßjÝ9¯<#×g3±d$¶³VR\x000bÝ^õfô\x0000JûØyõãÈÅ­\x0007 ÐµwÅpjô\x0000ê\x0005Ûù'\x000c\x0001ÌÌÎV\x000eÀ£3\x0014!ïÕ\x0007F\x000f °Ã©]éÝ)ã_@ÞpÜ-d\x001e@½a;ÿý£ü\x0000¾ÿ\x0000VÐûUòPÑßØmÊ\x001fþ\x0004jæ³\x001f>þãlodq%3iZ\x0006§IÈò\x001b<\x0016ç\x0007OmÃ$Á×\x000f}ùú³OuF
æ¤0§qÌ(+$ZÅ'Ì\x0004ô \x0002\x001d&@§LÌq¢c¨u@G)P$8¤\x0000;\x000bÚÞ|K\x0002m
\x000c£\x0006ºmrm«ácW¹\x001aÌ®ßs¨áfU«|<\x001b;\x0008ÇÛE;©ø\x0016czÜf}\x000e±¿Mö\x0012b¯'{¯!¦Ù;W§­
f\x000f,\x001c@D¿Ë@[
Ú\x000e¦^¿ÆÉ½©k+jÏÁÀøÃ"èYÔ\x0008
5Â8êâ¬3
VFÓ\x0018±H>,oÎ\x0005ë\x001fNÎ\x001at\x0000í~5û\x0008u¼@£\µ5'fzÏ¡Z@âÄ$ãr aÓÀb-÷´«|\x0011ê
Ý3¡VtÏÅÚIu0PË\x0012Qp°JØÍj£ª©Á«\x001có\x0016÷ò±ÝuHQ&cÒakÅ\x0005K¾YÞlùÓ¸1O­Ó6WÆ\x000el\x0006¦«ëyÞ\x0001±µãk2¢vÍøþéáÏ\x0005ß?Nï&8j
<\x0017oßÎ~çútîáóg\x000f.ÿégÜ3+¸a\x001bfpS¡ä6w7Û¢$\x0016Ý¾\x00132Ûmq»Éû\x000eÐïÛÉuÈÝ}\x0003°ý\x0016¶»î\x0019ò£\x0004ÅÒí\x001b<ì¶l
`Æ-fºjä%\x000fµ,¥ò#\x0012÷F\x0007`-ì0uÕûò@éÿÉÂO^®ûÓõªk°Ó\x0016v\x001dj\x000e¼åD\x0005v\x0016ÉÞd®Ã¾5Uýg¦pgæl\x0003\x001dbØÐ\x001f$îO\x0016\x000càVúÏN)@´¼E#\x0003q.e\x0006.»lÃ'6_\x000e\x0000W
ÐÎi@¬Eµ$tË{Þji(m!p¥\x0002í\x000eL27
\x0018yó.J\x001b_i*­ÒvJ\x0011RFÇv\x0019¢Q0w\x0019_¨R¬ÒvJ\x0015bàÆZ=Ìü8eÇ\\x0011ý¡\x0001àJ\x0017Ú)e\x0018Mï8`ÏD¶*\x001eö\x001b\Â\x000cJ\x0011Â"}jÌ\x000fØ/;í\x000f'
\x0000×à&±¿KÚ­Â.,vË÷'é\x0007+\x0002S
E6y\x0014ÿÄ2ífA-	!ï3ø\x000eàVÏ\x0012¦eÎL ±¤ZZ7äèÉY\x0008\=KyÖ:)ê;duPq9\x0005¸Ýç·º\x000eÜ©·éfÞ¦-Î\x0015·\x0004ÑÜ¿\x0000÷ÌLÉíaSoÓÍ¼MÛ'\x0005³³4¤Ý\x0008Î%JvÛÂ\x0000nõ4ÝÌÓ´ÎK!°\x0004ðt
Ü­ä ®\x0003®DÜM8
\x0005q±¬ÄÃm¦hZ×áöJÂý¥dRtx\x000bç\x0003ÈV\x000b\x001bãþb\x0001ÜJÀý'%{GMÜíÂ­ýOe}\x0006+Añ3ò^8\x0004EâÒ\x000cÐ­9kÐ\x0006\x0001»Ùó
\x0008¤21\x0007]'ñ£¹Ë·¡éù¶\x001eþüñÝÛÓN¸á±Zâil$^Ã°ORA¿yøóë\x0017ÏÂ\x0016)\x000c!uî1p}ÏîÃe35}Î+HÝ\x0016©\x001b»SìÍV.t!Z5îO|]Áé·8ýØÖ5
gdB9¬{V\x0018é§c³Hq\x0014ÇnÔI¨H&gk²ÞcÄOÇ¸g-Ò0v§ÀÎ³%R$Q×qîSP]Á\x0019·8ãïùFÓ\x0016i\x001a½QîÕµxïôÿ§îÝ²ëÊ<ï©p\x0004\¸_\x0016(%3S^º\x0015)æêïÉè´l¥ä¢D×å©§Ñ3è\x001aGÍ¤GòE\x0000\x00118\x001bG¹ÏÆe§ËÙ½ÌÒaÚÊ\x001fp@ \x0010ñ\x000fÎ³ëâR=¤qI\x001aÇæTòUU#). 4g9Ó\x0001FÒE\x0011­¾\x0018TÏï\x0014jyR#ýf½v°\x0007µ> ÆN(læCVJú\x0012m9X©\x0013âÖ=¨Õ	%\x0007(\x0004h\x0013j,»³ôÌ._V\x0007\x001c;¡4×À\x0002¨¤nË¯?	`Í£Vg\x001c<¤J\x0007)\x001d¥êã¤\x001aÕ]&µ:£äØ!\x0005{JíSÔR:\x000cMêz\x0013È\x001eÔêc§ÔÂRÁ¤tF]&u½%L\x000fjuNÉÁÊÄ{Xª$\x0011\x0005\x000b3ÀR=éQ·¢Væ_\x000eÚÿPÎT)¥üÔnµ=yËmDUýWö_¦[Äè\x0013ÿÀ1>«×Um{H+ó¯ÆÌ¿\x0015ü $± ÏË\x0005E¯7\x0016îA­/(æ_QÁqTC\x0006k\`V÷8©Tu\x0000¨Á+Jä÷~)6a,Ú\x0001öD¢\x001eÔê\x0000Pc\x0007UÔÚ8íªùëØÿÓf\x0017Ôê\x0004Pc'MÍúò¬C¡c\x000f@^´¢V'\x001a<\x00014×J\x0011ñbÍª=Ìê\x001e\x001eªN\x00005v\x0002À¬
òUEùöË¡*vÙþÕ=E]TàP¾T\&#t9¨v!­\x000e*5vPYyøò%\x000b¬.
zÔ\x001eß½®Î)=vN\x0019µ:Ä`ÙZ\x0001Ýã@ÕÕ1¥)Ojw¹*)\x0006]W1é!­N)=vJ\x0019åÔ±lL\x0014¡ îrÒu\x001cmìúLª
U\x00148ïÿ\x0012\x0005îÞX7VÒi=ªôSë#-ÄÎÊ£Ò\ØÆ¥º,G¬xûßÿõp÷õCk»Y\x0017a\x0015½T;O}jl\x0010â pºº&­?{ru}ùæÙ©~³<\x0000µ\x001c\x001e/åeØ°\x001d/ÅwDgV{\x0017\x000e@/\x0007 \x00030Ë\x0001ù\x0001X®SJ\x0014í\x0010ÅåeN¯fO\x000eÀ.\x0007`ç\x0007À
ðQá5#ók®vzÕ(ò»%¿æÇºL\x0005®§¤=¬\x0014Zõ>F\x0007à\x0003ðó\x0003%Ì\x0017=e \x0007]òäjÎ(Xòyþ:c\x0012?©\x0001\x0005Ã7ªß`\x0000q98=\x0000p\x00068Î
\x0007ßòÓ[/Û\x0019ä?Ä±Ó)&&\x0007àÁ(³ÿ­\x0004w]±Áq Ø­+¼ >g\x000fb\x000fSR²ð±.0\x000fÀs\x0006êi~úê\x0010³§0ÐG·Ìô\x001e\x000b0sPI±\x001b¡Vo¿£#¨Na9{\x000c{¡Ì9Âx'æ\x0001°	RvïõS\x001dÂrö\x0014NQ=>¥:\x0004 Øýtj5\x0002=:ê\x0014³ÇpöÓ) ¤Ç?Ò\x001dZsx¯] EH¥¼Å
Á/.d-DwöôóÇÉ\x001fèä¤þ*òµTj'
ùÑ\x0008ÿôÕóç'r?[ÕÜjÛb\x0015a\x0016JÊ§hûyz¿æ£Km¶þnç®ânÛ[MË=8µëR¡)?¸iåvo%«ùVrb¾eµº\x0010K^C*¯/QÍZävl]M·ÒSÓ-Ií\x000bÎÔÔA%O·'l­Å¶Fv+·Ó\x0015·Ó\x0013ÓÂ\x0000yy£\x000c>+0XÍ9¹þØÙÏ\x001djî0³L4E?B\x0000dN"/\x0013¹Ùû»\x001b_¦\x0016Üé¡j;ëÀ»Ô/Hç¢u¬|ÌØÆ4Èb6b\x001bYa\x001b9í\x0004ù¿\x0001n){\x0012§»Hd\x0019)÷ãVÕ21jføHêRÁ\x0005<à\àKn¯ëÉÌÝÜÑVÜÑN\x0013\&d½ÝAù"ð\x001bôÇ²^l{¸«"6~\x001cÇÆ,IjÎbBz@+Xõµ[Õb\x001aà\x000e5÷Ä2ñN²Z¸3®XoÍ·#í\x001aôÛ[¹MµL¬Y&A¦®Iå<&AÏ,ÌÀÜÛM´Û¹muÈãÇßÅié\x000eÙ\x000bÈZtr\x0007+¤\x000bÎ·OãIAóóÛ
oZ±UµLZ&§Ûb\x001eN eÂgå\x001aTË[¹mugÀ\x0013Ü±¨Æ,Fâ\x000e\x0014vQFì7ß6ÔÜ\x0013æ$\x0008I\x0002
ÁrgÐ+Qà\Úoy×Î q\x0006Q{ÄKâväè\x0010J\x0017À>/ÍØõòv\x0013Ëû\x001fí\x000fQ	ÄöÒÌ`äo§^\x0002Yö qs\x0019;\Õv;,½ªv¥W\x0013»2HO
5©u\x0000ß,Q$5sûõT¾nîú°ô3%¶ÇÜ5'¿£ñÆP_æv«J©ýÜ¾Úøq[ËÂ-\x001cJugnÍëÄ4´Jmæ®×·Zß¥)å#¯\x0013.÷ij\x001cÜÌíjî»N2'Ä\x000f_÷%w\x001fÛñJ\x001cLuê\x00043sê('l,#tGfP¸\x001eÍØ±Æñ©àÏoC0ÝÛx.ar?_0Ôe:,äÎ¿X,H¨Kp[la\x001b\x001a1·rûÊ\x000câÇ)îß\x00147¼-àLl¡Ö¥z¹c}G3w´ \x0003 \x0013i\x0008v%ö"Ü	[.dsüØÌ\x001cpFæjÓçBñ:¡Î.ñDo~py\x0004.ÇÁ£fí ±;M*´\x001e=\x0005Ü{öZàI@°\x0006Ø\x0018§ÏÅ`\x0012=\x0007}¬$9zØ¡»Å\x00014\x001eOÂh\x001c¥ÈÂÙ\x0019
¸VeÆw3©ô\x0012\N¸V
sóë&¥\x0016½¦÷}\x0011Ö5¸ûÁÝ\x0011øÄÕ\x0001k§¹M\x0011@¦÷eÔ-ôt3n¿¥¢j\x001f<}\x001e\x0007/²íAXÃÊÎJî¯ùª;ëúy'}\x001e_*ì¥xÌ¬³V
%sÁ\x0005kUì¼ûhÂõÌKÅÂ­>b\x0004¸¡N|Â»õJËnps4áffÂÈ\x001bÌxàXwÎ\x001f¯Ö_úÁí\x0011øQ1\x0002û %p|epá\x0008ÜìwpÂ­¤\x0006\x000fã\x0017\x0008[ÑÞ\x0019\x000c\x000eû4ò\x001aßíé\x0015¾Ü*z>\x000fë )"á\x0017T\x0011kZãNïu&ÖK\x001c?\x000fs+àÎ5>\x0012@Ù\x001dâö»Ýì\x0001Ô\x001dO¬\x0014-5=vûàbZí\x0008îH7\x0012&Üï6ãö\x0008ÜÎ'Ñ®lTààä÷@nîgÃzÝi/¶µKëä¸K«¼y6)\x0001+çS\x0016\x001c6Íö\x0004\x001e×[[õ#ðñËÒ`\x000bE\x0006÷¤äó\x001dÙ¤X¿å©ÁÍx\x0010\x0008.\x000bO\x001fÊ*\x0014I*Xø\x001a¶W0Eú£Û¸ý(©æ[%eèÄ\x001d\x001dsÝnÉÒ×/kéó8·pç2\x0012x MW!<½\x001c\x0003øno\x000fÒ\x001f\x001d>~æð1U­Á7q4Ý\x0014s\x0013Æ®×ÜöR\x0007[_Ùðó85âej\x001b<\x0015`E¡¾ BûuY^ð\x0018k\x0016?\x000f[í¨ç
,·\x0015/Ñw!\x0002¾ò^û\x0012þ¦Ê ¤ÏãÜ4ÛÆI*ÌLrZ\x000fê§\x000eGÔ\x0013öÛK\x0013\x000c\x0000\S{_Ì+'s¢Ün/J\x0004Qe\x0012\x0003Öê'p,áÌÜ=B¥\x001bú+7rË:ê>\x000fs;a)ß\x001dNÆ\x0015\5ø\x000føíVàøy\x0018Ü\x0019\x00146»@âÖ\x0002Ì\x000cùV(7¿\x0017¸>J$Ô\x0013ñp\x0015\x0004çþxT\x0018õùò`
·Fb]¬\x0017ÜÔ÷Ìôy\x001cÜ{öe\x0015f&n§èz,Ün9\x001dpÑ>Â	]\x0005ð\x0003³8\x001d,\x0019IõÂY>èÞí	fµ:2Óçap¬¥Éú*^Á.Í­÷|ÖÃ±¿×Y\x000fßgâGÁaU\x0007öP$ÌxV0\x0010>fµ
½eöãöGÜã&\x0005¸%\x0014¸\x0012-\x001cg°Ý~6Ü«z¾½o\x0014Ë¹É©#xö	£bî°ÝS¦[×\x000b\x001c?s\x000bOZË^\x0004."\x0017QäÄ\x000e\x0000_í\x0008ÚÏíeÍíÇ¯<ZbL9\x001bB¸/PªÀ\x0017\x001fðÝ®õ
\x0015Õ+ð8î]iì:IÜ\x0018¥Íû2ºÂ}B°§;èºÔ!èñ»Q§\x0006OiÂ\x001drKÜeÂw;{ð¯ªÀÍÄÎ\x0004·\x0006á\÷ÔðY
'yÆÕniÕx<×à\x0013L\x0019Ëu-È\x0010©MU±<°íJ\x00033P;WQ;W\x001aõry¥\x0004\x000e\I©uÙëêYÝàGgO9{´µ¤ùOôøG\x0004W"\x0016[¸Ûa¯¥®lJú<\x000cnÀùÎª\x0003I».-ã\x0006ïMí÷:5µRÕ\x00059}\x001e\x0006·ÖSÚUÒÜÊî46ë·ãÞÜ­v\x0000&©²éó0x\x0010Ä\x000c±Í\x0013u¢Ævª2{ë÷ZãÚÔ¡ôy\x001cÜs0\x001cÀ\x0003÷\x0012\x000c¬cp»U\x0001P}\x0004>aU|é5\x0008KÅäË=5þÆu²®\x001fÔKídMòÍG©áÚÀ±\x0014X×$Ï*££é£ÞëìÑG\x0011e=\x0013Q6(¥i¶Eã\x0002Ü
\x001fKhÂín\x0015°Ú×yéó88Xb
\x0005Õ\x001dc\x0014/\x0012¸Ø-\x0011H{{4ãvbÆ%^/ÉM±J¾ÔÁÕn!	=Î+ð8nÃ
8"Ñ\x0014©²G«H+\x0013Õ@vËJÑAW1ôy|ÂÁ/¤$	å\x001d\x0018{½ýÈ\x0005ù_¿¹"\x0008\x0002i\x0012Rô
+§\x0003EHT\x0008;ï%qè`Zò$îÙÿ\x0012Â#vL\x001cfO¥2²:ñ&qTÁ&¢ßÍcð§fOá avË]ô\x001c\x0008øDÜÍ,¦åþîåþnü>\x0000t\x0016EAr$IèÙw»N úûoÐßO ûr\x0015\x0002t¥\x0019½ï¶Ø÷G\x001dÓkÆ7ª)©>D\x0005\x001bá\x0016'8MÅîVüfýí7³þöÛ>JiC%â¿H"ÎOÿ|ÿËOgØßù§\x000f?jíïì<öÉÉ©¸X¨A-AzõÙíéW/½<Ã\x0006Ï?=ûáå\x0006ÏL\x001dì\x001a-F©QÑ \x0006JîÜwÆZ~°q5.Ô-k°ñã\x00047;\x0001ï\x0013$t\x0007\x0017RÎ\x000bò«a¡~n]së\x0019nk¨ák=uDÕOJ>\x0010«-æ¾Å¾{xwÿ·Uf_3û	fÅ=Jà\x0008UÜLÛ:ÎÎ\x0007þ5\x001f±®]µ!ñã87,@y´Êæ×6X!w`Âªdq7¶ÕÄãØÞSs9¸_Fn´â\x0014)\x001b\x0008³*´ÞmªU\x001f±#æSaà`õ¬\x000f.Ìj3Ö\x0001ìXcÇ
©øI6
¥±yG*Éé@kM7¶.:ü	\x001b?cHò\x0000>bqoÖ´!2öj÷ò~lW­mü8
¾\x0008-\x0012ï\x000c«3ºRv².ÌÞmJ\"aãÇñµ
×\x001e/ÉVFîÓâ<\x0012cµÛtcôtÁ\x001f'Làôp0 Ô\x0008Çr\x001b,!×½À\x0001l_cÏ\x001c8VrrxJ²ÖÄ-Ëâ^\x0015èævEº(qãÇebøvlÁ?±´L¨,\x0016n\x000e«e±½ØRØúÄÏãÜJ3¶æ~)®äâÃâÞkºs¡ò}`Çß
ãkÍÉVIÊCµÎ`$ìÎÕðòÈr9æÇ%3ÿ\x000fX5X]V+ã£ìAaÿõÝ³«/gOï¡c,
ë6`5[©e`\x001bÖ:³ÂúëË3\x0000zÙ@­Ôj\x001a\x0013~È\x001eb\x0005n
\x0011lÑOÁë½¨õZÏPó£OÄþ½\x0005u\x0015·3ñ[­z¨ÍÚÌPËs]¦Zð\x0002qªLõ\x000bÄ.¡í\x000ct,­¬ã.GÁùB½Õ4´Ú-©Ý\x000cµåþß\x0012N¤¸l·\x001aõ@û%´¥¶´#\x000fÁ+î}wBÛ¥:,©Ã\x000cµäæöÒ6hÁ2ÕzÇ\x0005\x0012ÔqZ%Å6¤v©*Ïµ`ê°\x001aÑM}Ð\x0013OgY×FnØ-º\x0019¸rÈH'ìÇ®Æñ³\x0011f[5âú\x000f­l6"!lt êÁ®L±}2P`>µPÊØEç\x0014ýïilíZfÃ/#\x0002®ÓÓÏ_¾Þ}ùÒî>yVMFçCÏ\x000eK§£ë	b©Õ7\x0000¿º½ysyssÊbnµäVSÜüF\x000fÜºôÑÆ\x001cR{^Ø\x001eáÖKn=Ãí\x000e«;:JñµA*\x0006O*	»q%·âTDý\x00037Et:Ýj¯Û.¹í\x0014·¡É6\x0014.¹.­\x0014Ö³6\x0007ÝÙÍ0cõ¿,{RÓ)Éeé(M|Òtrû%·â\x0006f[q7NÁº?N®Ë,
P%u¢ç¼!\x0003_\x000f|ô¿ýKê8;×´´³\x0018@Æ¼FÝq\x001ctÞ\x0019pLá\x0006-¤\x000b\x0000\\x000e3§÷Nðú :)­ÇtÞ|À\x001bÊ
õ]:¸ÇÓ½æ;Á+\x000b(§L ,\x0015¾\x0000ÇÃµ]\x0008÷lL³ìCÒnÐ£ïê¨!\x000e\x001dôE\x0015Ýú×\x000ezå|}`*T?\\x0004\x0005Ó;üïþvvs÷áÓ×³ËO_?øÔø(o
Ö\x000fPH¶\x0014>èX\x0012
¬Ù~¸L¯ò?^¾>»¹|öòÍÙåË7¯½<^@#:è¥àÛkH\x0016%í\x0014ìÃ\x000c\x0011¥zÝÊÍ¨áàb\(ÆýFd¸N/jyKÛz'|GaÜ±\x0001IQ
\x0008?î5"ìæÅO¸\x001eS Ò\x0014)\x0008
«ãZÀnvL\x0013#IÝÆä#§FT\x0006ñyL¬H\x000e_ÓjdlvLTÝ4¦êIlÎ<ík³¥w=RÚüf½"08&W\x0019¼$w½Ótàz\x0012|¶Ì\x0016/h\x0016S´rÕ?\x001c
ÕvÂ;
IÃAJÅTpzbg$\x001c×¾iôöKÏØ´¬ÆÚï4&%)¶åQ6-´ÔÅG\x0018ÔßyLÑë:\x0001¿¸X¼æ?]~üåþçÇ\x000f÷\x000fÑ\x0017ÔJEÛ­Q«AP¼ÜE~\x0006q®¶=áaÜ]¿º}qõÃí³«ëmvµdW¿/v½d×¿/v³d7¿'vyè\x0013Ö»²¿'zS¯\x001aüø» \x000fN\x001d½\x001f¾¬}{ýáþìùç_ÞÞ=¼o¼/E¡G¬-ù\x0015\x001e\x0014EÛµ©¯Õ|õâÉåõwì\x0007qÌÄ.æàÁ³¥,~ïÈÇµÆÔ»H·Â=ÙeÅ.çØâ¬ÕT@Ü\x0010{\x0010ì:ñ\x0007I
¯\x0004)Fà-\x0005~2\x0011µl3¼£l"¿- ØÁ.\x000fjÇÈ.+±ã~x#5YaÚrOQ#9GÄ«me\x001ezk*zkæè\x001d\x0017ÚÂº\x0011ÔV\x0007Îóf»íH\x000f¼¯ôsëÆ¡|ÍðÂåÚ\x0015«QyàW»Ú\x000fÁÇ\x001a>NÂk.\x0001	(¡Å¬6Æu³YÐA¯\x0016\x000fÕÉT9zé¨\x001byAq+`-ùúìÕ®s¯\x000e\x000eB¢¯\x001aI
ÐÃßF9vÇÈðZ\x0016ýæíÒÄ\x001ex]\x0019\x001c¥ç\x000cõ·¬T¶¬²¬Âæüzt{\x0004ÞUö\x0006?NÁÛxnhÕ[MÏNÊð\x0005cºç²Ñ¢ò\x000f´s\x0010\x000cØwKËF9î?´Eiê·ÕªzèmµeµÛ²&\x0006u\x0007,$¦gJXêL¿Þÿ}ÞÔ¾tÎÀá.J_\x0018°MÑÝsËîI×sðJ§ÖXIL;i;#½plëí¶JA\x0007¼­áí,<zªãÆs\x0012,øg\x001c »:8\x000b­ääZÊ9ÇØhK½j}êù_xDQÛ4b»m`\x0017½©éçÌ¥61\x0002öjL\x0016ÇDÇ±ih÷ÕCoª» 3s·A-XD°\x001e/µ^R\x0012£÷ô.\x0017]\x0004ó¥dnÝk8\I\x0001
¯äæ^G\x000eÿ©mE®\x001eúà+úà§è\x0015,\x0017ÅbÛ\x000e¿\x0006¤\x000fÞµ×aõ}c~!ÿôµúó\x0000½pwê\x0003Ðgx_f>ìjì½«KïæK¼SØØcÇib§ôd¡Ý¶(q\x000f|¬'>NN¼ü,æ±Z:Ó\x0007¡xÙø]\x00038ÁTæ29s)åWú\Me<÷¹ß,«ï\x000f\x001f§àU$ïÒ{cI^Ù¸ÀeÚnKEvÑÇ~îV"aAT¸w³½Á\x0013è\x001b4ò{ècM\x001f'ée!q\x0002zEs/Jõà¶êK\x0007}ÅrÎâ\x0017|îÈÖk/UÆ9~O\x0004ø=o±6õqÎÔcLÑp\x0016\x0013n^b\x001a, ¿\x001cÜO/â r2\x0010báÔ'ðÐ$	y\x0019ØCüíîå=øVÔøvêZe\x0003\x0018\x001dOÏë`<s\x001cÇheø¨«Ù7CøuÜ8}Ã·¬®\x001b:÷ñ¹\x0017ßV
ê»\x001c\x0004IøvòvîzÂq´t=®'EJ@ìlôÃA\x000c\x000f­»\x0001\x0008\x001fJo\x0014\x0018K.¶1NqT\x0001vÂ®^2|\x0003wÇßÀÔ\x0000´
¥uç"{<8\x001aÎ\ØÉQ)Áö.ÎÑRy\x0017K*>}~øù±5ÿÏ+«=Âµ²¡\x001d?=È°\x0019Â¯®¸=ÿGà®\x0002wSàÀ'\x001c\x000büc\x0002çI\x0007òMaÒ\x001et/è^L¡\x0017ý£\x001dÏs\x0000'-w\x000efÓÉìB7\x0015ºC·$\x001c\x001c±¡Y·dì\x0001}Sü½\x0003]jÁ$!	vôk\x0013»õç´Ò5\x0017"\x0006½)ÁÛ^ÔK2ºñ3èÒã-0Ïz \x000c6\x0007ÆÿS.Û~è®u75ëX®%2»R =2{ØläÑÃ~\x0010OìK\x001dø\x0011vGO
`cXßÛ%÷5³ûõ¤ô\x0011özÉøÉ%#Iò+Za(\x0017Á¡ü>Ïûf¬¾=ÔìaÝ
r)=¢Êmbw¦°ov­éamqÊ¸£\x0008?Õ;[\x0014\x0013\x000eÝ;:Q£Ü|Öì`W¢Zï©tiÝ8*Ö±:b\x0001tvÊ£\x0007ô\x001dg]\x001dªÐ2¹#Wä\x0004Gkì9-\x0018KmêdT{\x001aH%ëIsI\x0013ld¸Å\x0013R³\x000bæ7%\x0005{ØUÍ®æØµ§×ÑZM'ïR<ï{©JÅ=N±cÃÎ®\x0004½êà´\x0013ùvªV\x000f¹©ÉÍ\x001c¹2$¸\x001a­×ô(âRh2³]W­®\x001bÊNÝ7P:k\x000cF'"õõrÉ]Êìaó1­½>RÕä*\x0014á\x0000»`¿\x001du}û\x0005¹=TÇ
sÇô\x0019-*à\x0011»Q|,ÙÍÎ\x0019=ì±^ïqn½GIO°²SwÌä¹KUÜßu¹_aÿUiJ\x0002×õyªçÎSl<\x0011ÉÆ\x0004AÝFE\x0002¦0é{ú1ZÔq\x00011µQE0Ôñ0:\x000cmç°\x0012\x0017ÀÂ/·Bª=ä²Z.©\x0000cÜE¾q8°&g\x0010£hÿoÂ^G=g\x001eÁÇ¥"o\x0007~dn­fËc½ÂQ;¢»*2 ÝTh\x0000¥nyÁXI~\x000c,vªõ\x0006ö=ÝÇð#±O¹ØÏ¬£3úÀN\x0017\x000ep«7;Pu±\x001fÅÁ¦.ØÈ_,±a:ËVFåÝlæ>w°Ú÷5S¾¯Qpñ´³ZjØàMY3;Æ\x0006®\x000eTü8\x000es­ó#e@kÖµ
¾ýÞ×Ãnª­jÌÌVuQÆsÚ©o\x001cÖÀ³n÷\1j\x0019oçûÒÝÔÉ\x0014ÉF ËÁ\x0014\x001c\x0007\x0007ÜºÆËÈ¡*\x0015÷ì\x0014¤ûeoøêáwZô,u\x0010õºÐßPÐý\x0001¸9~¯´=§@ªw(Ñü1çù\x001b°«ºÄ]\x0003³´_ãáz\x0014¿\x0006Æ_\x0012c\x001bºöàÖP×¤tJå®IÞs*¢ö-a1ø§/Ò?Ý_tµd0\x0007oK\x0013XäçÖexÌ\x0005ÓpÛnf_Dßý8úÞ
Ýyé¯HJÏq\x0013\x001aÜCð¶\x0008¿Ì`\x001d\x0017\x001eCyiæÁÏ=Ù\x000cª\x0011»Î{½àåìW³#¼âä[éÅ!Ò6<Ù´Ó\x001f"Áþ(\x0012ÜKµQò±\x0014ëûKWVÚsê\x0017wn?¾sìWI©p¹#Qz#9³#6TÍð\x0007	÷\x0004¯B{Ý3\x001fiæcJ°I3o$'mU­ÿ1z]ÓOnX%KN\x0008\x0014U_\x0004\x0012Z.R\x001dð¶·ðeÝ7C	\x0005¸e¾Á+î`w5ûÇ.¤LáÑ»Ïk>ÄPÔ6Z¼vz[íXm'w,
6R2J\x0006î\x0001©z¢LMC¯>Ôë&L®\x0005§¸\x001f$ü\x0017k¹Ã¶£Ç\x001a=Î¡ãl+¦÷¤	¤gÅ#g÷´FWÞè¹E\x001fe(ËFG/£-¥E²å\x001eÛ\x000eojx3¹c]R8f-\x0019M\x001bVr\x0002\hyänw7nÒÎÃ5&>êsMÎM0Üþ'n&÷À/\x001b¸¢¤G\x0005)JÝ\x0018=Ë¶Ò\x0016e"§w=¥®éõäÔkNxZå«\x0008¯\x001aç×eïFÐCå\x0013ãÇ¹\x0003¶ù\x0018\x0003¥K_ú¡5å¤´ÃÇêrqîrà\x0012äRÀ\x0000é¥³\x000b§EK\x0000¤¾^5qnÕÀª#5®­	]òªñ-®Íä~Ñ\x001b#\x0007NM\x0007Ê\x0014\x000eØz¸;°ó\x0004¯wõË¨.R©gÅ­±¶¨Õù@
\x0019ÒJz\x0000
»ç~
µ©	¦ÆÂùªJÝqÎeÆóùêí®ë&øzæýÜÌ éq\x0001¾CK\x0005QÒh\x0016\x0001óØ\x000cf?z<ñ\x0016ôé\x0000¡¢´\x0004CeÙ>²Ò_Un\x001c B\x001f\x0005&=3\x0015\x0015¤\x0016 <7¥·[¨\x0005ÙoÐo´­îàéóÔAe\x000eíUàjNPBÅÞ}NTæH¼LjÏþËãý§\x000f÷\x000fÍ1n°dç£\x0014%ló55-7gÿr{õòÙÕu\x000bwXr)nì7EéX
PAÈÃ	\x0005å\x0001ò *r5ýÈHEÞ
\x0016ÛÖ\	"]XWïG
4DÒÎ.\x0017ÊiÒ9³?±Gî~íìvCWQ.Ññã\x0004:ª©xj`¢¹ÂjÅ	|Ö7<4³ë]O²\x0003!5¨\x0010`)U~Ujo¤U
ñfvs\x00085!»©CM½ì(A'Stó<¤¢\x0007Q;nT£B>ed0\x0013ÞÑ´c«!RàÑäJkÓð\x0018ÒÎ~ðg\x0012{íÏt³Há\x0010ñõÙ\x001d³õÞHýìÖTKÆ¹%\x0013%k\x0007a_Á\¤kà´&\x001d×û°}jÍ\x0010Ñ}Iì"rû/%øÝ[Äòvv[\x0019k§Ì\x000c&6çW²Òæ]rÏ
#öe·5ûÔÉd¨\x001d¢àH\x001d;
i»Ú\x0002q\x0000}\x0011`Bô£\x0000Sÿ±¬¥\x0019°F,d\x000c	§uCâd\x0007»©ÙÍ\x001c»¢w\x0004wM÷\x000e`/ËÝú\x001dM¤ó5»cw\x0014\x000c\x0018
\x0016¤4ÅªpånÈ1hFÇû×\x0002=]Ç&Ð½ é\x0011l®Emf\x0016è~S\x0004´\x0007ýðxÐëÇntcÎ\x0005¡ËÀê«`\x0017]nÊ\x0000t±Ë}Î@Zó=)\x000b&v\x0013i§*±YBÜÃ\x001eë%\x0013§Eeó¬«æ01(ç3)Nü\x000bvÃëG\x0007»­Ù§;jÂåê<\x0017øYIÉ@Rb{7òPoÔ0¹QQ5"ÛvgK"©Ùû\x0005×}WvS³OÙGí$óðÚG\x001d\x001fâÅ.UCv\x0007º­Ñç\x0016\x0016¼`¡\x001f\x00168¯uÑPðÔ\x001ekG&Î92ÚiÊ\x000fVpÅ¼e]&)dØïª'\x0017M­Rt@È)Û®à®ó¯\x0002å3%Q)G\x0012/Rm+©õÀ;YÃ»)ã®°$4oU\x0005G\x0012RãË^ê"´\x001f»?x?7ñØ¿<ïUã#¹a0ñÜå¯¥L®]ÖñÇôyjÞ=eÆ\x0007ô&I~\x000fo~Ìî÷;¤<ZñrrÅÇâÁDy4à\x000f\x001a\x0016LÍ¦*J\x0017¼<[ñÒªHÀ\x00136WÁÚ'\x0000]gÞ\x001c-¹U@J^Á°À°Áf\x0004Ì¾clFÊx\x0014Eóg¤5¬gn!IpãmxÓ\x000fÑ\x000c¯d\x0015àH§l§r¹`"K\x0016Cÿj±-\x0013Û\x0003¯êýªÔÔ~FRÝHÊ(yÙx,¾É3\x001f\x001b
,ÛáµªáõÔË\x0001V\x0014ÓÕIÃ­/\x0017C\x001bÏdQ7dÙ¶³\x001f®jît\x0005KÈ'¶]\x0003\x00179¯<
µãªÑG\x0013¯§&Þb\x0004æÝX\x001c\x0006²[ÃJ!îøL&õÑÄë¹\x0017¨Cá\x0015¶Â#ÅCvãÁñÞsâ¯á\x0007è9*ó\x000bwy®ëýÞðBO;Á[5sB¥U\x000b¢\x001bwöä
¶\x001fà4=WL¶_Â'a­{\x0015\x0004¶Ù
4óò¶§[\x0013BumM'Î0>
/\x000b·èy¸.ÜêeÕÜ×]ëH©(V\x0007:¤¤ßóâ
×ÕÔ!ß_ßÎ\`D+\b'¨îÌ\x001eÔFß3ä\x0001>\x000ciÏ}\x0001à\x000ep¢`\x0015i\x001dZ	ãáü¾ów<ÿw3ó\x000fÄ\x0002\x0008Ø\x0002\x0008:°{Ë®\x000fÝõòÁ§îåÂ@$u(|ªUÏoÝüp	ÆÇ\x001cÄ¿;Æ}+<Éd\x00064¡ê5§\x0019ô&=/¥EësxÌÁÌú-çÉýCjG×\0
v²ûÓH¤t*X\x000eß4Ô\x0012=¹ºNíè\x001aàM\x0005oæà#Ø\x001aÇBæâêIºjGvW±»¹gE¯\x001dÒr¸\x0012îSü$"[Ô:Ø\x000fï9È^?çôÏû¡½Wüzéðå#Ü2ø]ðÞ.á½\x000b¬Ê±'ðI\x0001)$?mSß\x0001¨3FøºÎx`æ\x0003µâM¯Q¹¡ºã$	¹Ý\x0014­\x0007]êÚÒèÉÝYAØ
¥ö»è©¦\x0002&¾!·¿ÞU\x0013\x001fçè
»8\x000e3W³\x0018\teÍM1í.úPmX\x0019&w,*zEzò\x0014\x0003qÑ²ò\x0008ZÚ=ôh\x0017ôøq\x001e\x001fÉ½	ÄwÞ\x001d\x001eHö\9ÊúÞúI£¹¤q©}H28K+boÙAï«]«ü¬ ð]$Ï='Ä¹È\x0015¯©LmOúXíÚ#}²u/ØØ[gÍÑª¼ð4d¶ÓkUíZ­æv-¶&¢Ü\x0003Y\x000ffÞlvÔë¢·Õ®=\x0012Ìê¦¥sî²c±º"ÁûhÊÂÙ\x0015]×èznâuyh°ÖPç\x0004\x0017,\x0017\x001bÇ¸«w¦}=ñ~râàþ¨B³Í×\x0017½ÚÓ¥×¾z?7õàâPGºteøÈÅÒè<ìëã\x001cî²ìå¼u\x0014\x0004yöRSü²vsv5÷Öÿñ+õ\x001f_\x001cXø«)?Óp:®õEp8z[\x001e|\x001aÚ\x000fô}\x000b?\x001f\x000b?Ï:½|KEu0\x0000Q¼üÍÞ\x001b½\x0003xw<wÓËHeô+ÎòÞÛàþÿþ÷Åÿþÿýï\x001fwñ"¤É»¸\x000ei\x000eìbË\x0015½è7\x000bÞ\x0004,\x0007&d\ßpwü%ÜM~	å¾(í·_ÁÞô:¦ÿÓ¬
r\x0014Â\x000e\x0017l\É¾ÜÇ÷4A¤\x0010Oñá\x0017\x0017è×>ýóý/\x001f>\x0001üÙ÷?}={þxÿó§ûFx\x0019\x000fZ­EÁ\
¤òjãÓ\x001f¯^<{	øgß¿zùæìùíÕ\x000f/¯6ñ\x000f\x0017^ÄÇûî\x000c¾²0÷\x001eÅ©\\x000ek*AYJ¬gK\x000fÑË`+ÒãÇ9|©(Âª+9ÓÅIKQY%õj\x001fð1üÃ\x0013nÂG\x0017k
_pW\x0014\x001f,åLÃÿ#\x0010Oz%ª¥\x001fçè½J"O\x001aV%\\x001a
-\x001eK¾Zwà\x0006ñ}ï'w.\x0008H}ÍV_JW\x0016ÏjÔ ¬ùg-9ðGÎ×q×Y­j\x001f£?\x0008%z\x0014\x0008£wô]÷Jw\x0017O
/õâ;Æo*Ë\x001fçøµ¢ëKÄ¦uÜ8Â	æw«¢Ccüõ±¥¦Ï-0÷ÚÐê9td2$W¥¤Ýyþ]ÍïfùEéR\x0013,«_+Æ_
\x0016áÊòãÇ)|\x0001;6Kà`\x0012	ÛNìmÉü«ÅaüªæWÓ/\x001dÕÐÆ\x0010méaxû¢Ní¾ü®æwóï\x000eüXáÆ\x0012ûú\x0005ÛwUäo?Ögo<{QÉ$ç;Æà\x0002eä;|\x0003¤ùÇ\x0012 \x001dù\x0017m%?µâ·Ëö0eþ\x001d\x0005N\x0000õÞ8Æ_»ÍzÖoÆÄ/éiý\x000brÂo°þwÝ¾º6?zÚüHîÒ&\x0005riøðZMÚ\x001cu<\x000f\x0017^v=ï&=ç6?ûæó}Áõ\M¤\x001a½·,ã\x000e|wÁ_Í]\x001e5É¨c\x0007èrwä\x0013rµd²s\x0010`nj\x001dr´?~é\x0001}9{úñî±½\x001a>rÃÛ¨5·\x000e\x0007­Ëõ¶\x0007üæìéóËÛSêï	Z
\x001a?\x000eSã:÷Ï%ª¦\x0008»nÏw+µó\x0015µóÃÔVS©¡\x000f>Ò\x001a±2*V`¶«Ñ^èÅý\x0010¡ëûa'´ãZ\x0002ïuà¶\x0018p*Ñ[nÒ\x0017n^ivµ­µf²é=Êh£`Þu]¿ÞYÖ¢bÆ3ÌÖµ¥3Z^ÐZ6Oó\x0016µ¬Ö\x0006~\x001c¥Öàzå¢6ï\x000c<è©\x0002\x0015nj«9¼ÝÔªk5>×ÆFÊö\x000e»ÀZpãIÁOí\x0013§ÚÖÔvZYêñâ×¤\x0006máü¢\x001eì±\x0013µ9<-#5~\x001ck¹ÑÙz\x0014÷D\x0004J=¯u5¥ÚÚÊPãÇajì°õ)M\x0016á¦äbÚ"nGd¶¨1ß1å¶rÙ\x001aþâ¢.ZûéÃC@\x000fp£@FÊW¤'LiÙmPGüéÙõiy>æ.y\x001f»NûèävAq×QT\x000b§\x0014?o¸k\x000c
ÝºÁK_\x0002¯3üzÁ9§\x0003V{å³W%rá\x001b^Ì¹Zr\x001b5³P°tÈ.7ÞÞ8§´x6n;»¬\x0019ÜV+ÜÎ¬pì¤ )TýÅ\x0002gØp¬%®Þ\x0007ÀËM-\x00079\x0003®\x0005)\x0008Å\x0010<çx\x0004Aù|Jµ\x0014\x0006¶WK%Ì,\x0015\x0004§%»Ô17_/cC>V+·¬·¦Úô\x000c>\x001f®ñÔ£6½	`¤fÜ4ä<·û\x001aÜÏlNä\x0001\x0015WD\x0016"7DSë\x000e÷\x0000¸¯VôSVEW\x000c|\x000767Éf\é´fòP¯0±V\x0002ø¬h½ÓZ±\x0001Enq­Àâæµ¢\x001bÊ*ZÉU\x0011Ì'g-<Ù;çZQ¶'ü?_Ytä#?6h6ëXë8EnÊ#¸[t\x0004\x0019º\x000cÃZY}ï\x001d\x0000·õÛ©)7öÜ\x0012¸\x0014¹¿Ös¼ª¡\x0010¤;ÔNVñ²\x0002Ê«flÍºåÀÍaZ­\x001b*)ÚÁe
>svâJÁûZ"W¥\x000eÁXöVTÈg;¹ªÉg,"8T)§\x0001í
\x001cGùÎÊìkPé/ä¿\x001a>!l-ª\x0015®ÅÔ
\x0007/K{èD ¸¨ZÛâ¾ÖùÖ®oíæN îÈ8ß"Ò½
N Ï+eOoEæ1D®gÜ,ãÊJQíxàîlÊH³ß	¤CeÇu²ãÂ`Ú\x0011®\x0015ï)m'J~;×X-´\x001bw¬¹ã\x000c7OZqT £÷È\x000f':ý\x000e #*C\x001fg®ù¹ÁSZ+§\óÃRÙÏ\x001c\x001a!kð©KP©¨)¹YéÙ!O9Uü+côvz`;¹®É§¶g~\x0018ÌEq;,\x00166±AV²\W\x0017fü8³==mO\+÷§/¥¡áf+¸ÕÕ*·zfÃ½!t¤³SSÍªáíiÜ¦ÜÚ\x001aÜNÃ¥-\x0012¸|è\x000bL"¢UÞ ÒJîjÃâ¦\x000c\x000bÜ\x0015R¹ªNSic~\x0008_\x001a\x00149ÚÁm
ngÀ­8Ï¦\	M\x000fkX²Dq8ã{Ü¬Mp_ÏÜõ£U|ì«`IÐ\x001bÅCÈa±
-UÚÁc
>qz\x0006¸Å¦>Biw:ªñ©=Ûý¶§èä\x0008äY½3mOK-ÛÜ{Þ
-\x0006[É}mXüa	"¥EçÝ)pÙ¤ såô\x000cûM¹w5¸\x0001*b§ý\x0019é\x0011ÈkÅ)\x001eÆ«ý\x0002C¡¶aÆ"§UîúJjjrîul\x0011[:´7«Êc	jÂc	"æ\x0007ådY4é¾{\x0015aÙ1¢\x0015j%Ì8,\x0001-8YDçè
ç
¦]dpÕPEÛ
\x001eMu\x0008E3q\x0008Áö\x000cì°\x0018£Ø°¨ÀáO\x0017v\+x]û)×0å>;:Z>÷­!Q`åtU#¹<ôÇÊÛÔmc|µxtÿpÒ%×]xª«\x0019\x001dûî^Céó\x000czÄ^\x0019]S±õM¶ÅíhÏ¥¬½ôy\x0002Ýù²è`!óû!\x001cníæ¥ÙÍS\x0004Ôp>µ`\ÄW¬î5ÉæÁQä¸`Ðo¶%[_mï&îr\x0000\x001cò067às1RÒÒº¡¶±ã0ªÑñ8\x001ag\x000fðßIE"hc0»|\x0000Ã'i m\x000fúÛcô·3î)N:*\x0010eó¨%\x001bv\x0013ö\x0014¡lRJO(Y,¨£¤«Ê¨wgOî\x001eiÌIuØZåº|-$w:r.~«ú¬ÔçgO.o_HI%p\x0006ÊàFÌã{\\x0016sõ
B,¸ý,)rõ{qË[NGÃ-ì\x0002x*Ô\x0002ÜâÙOäëíUûÉ\x0017IH~T\x0004ØK\x001eñ)+»@zCÖ\x0007ÇUÃjkÒ\x0001pU«)p¯X­G+Ç}¥`¢)/.èÕ³hü \x0017È­rÅ+\x001aû\x001df	K	\x0010¹o(\x001am&\x000fõ¹Å\x0012Yç\x0006%ºi\x0006Ao"¬·®\x001b!×5¹!\x000f=À\x001bweGj<\x0002>üê[b?¹>t{I¶ÜØqr\x000fóp®4ijqÜÂbK\x0003R±n¿\x001dªmµZðã8¹\x0014åaà\x001eWJT°¬,UGw¼^çzfcÚ5÷}³ÂQE5<\x0016EZ}	í'7\x0007\x001d°tÆ83çp£0Ô\x0007K\x001a>ú#\x0006ýHýnU_¶Ü\x001eT\x0013\x001c?N\x0011§VRà³ä3\x001b=\x000bã
o¶Ë±:6è²\x00167i]\x000bÔ»fd,-\x00000\x001fö)Ý/À9]uõð{|®CE
jS`
Ô#¸¸g/>?~ú¹}G*]BÍÅ\>Æ¢¬8ók¾í-x¶·g/^Ý¾ü¡Ô.Ií8©
*ù¬Òswã¸Þ½¾Ö-iÝ?ó¼ú%©\x001f$µ%;\x0015¥\x0014èT\x0004ZÇ´«gK'mXÒqZÇ´|\x0004Ú²\x0008VoÁ}¬qÉ\x001aGY%ÊQdVËM~#g\x0016J<\x0006w¡=\x0014õ mj÷4k\x0018×à;	á\x0006Æ]OSîÃU\x0015®úg]8öëµ\x0002ÿ³³ï\x001f±T\x0014þðúñáçÇFpmrÝQ*æÑ*5¤\x0016¡\x0014©­o8
)}õ¢ð×·×?ÜnAÉå\x0018\x001e\x000e>U\x0011¤ADÊi¥_»Ð\x0002»Ýc\x0008a9\x0010¦Ç `ÙäB\x001fç\x0014µ\x000bµ\x000f\x0011©½c¢ú\x001e¤ØáPâÜÒ÷À§¢òõ`1í>E³­¼æ¿	|j3´%l ¿I¦ËW±\x0015Ýì\x001eÅ¡ßY\x001aÅ²ÝÙè(0yOçQ |vÊ»W¼'6c½£Ðå©6B/jGG\x0001æ)+\x0001z²\2åT±vï­mj\x0013kÄ¼ÅÞyù«°ÆcWà´ ¬-e\x0003_Åò>Á_ÇRÓpp,Éó¥Áx\x00169KàoDoæù\x000f\x0018ÛãÁÁÝa,Ê»sM«\x000bõµ\x001d\x0019]Ø\x0019µÑ<\x0016økSÿ"yxè5Øóª*
ýéþáçûæ\x001dÔ\x001aÎÕJ8\x0012\x001b
Ámw­oÑ\x001eøéêú«ëSo\x0019\x0019Ü¹%¸sãà\x0001«\x0015èò\x0014\x0003UY¢ø\x0012ûÍ.6â¶rÇ;Îq\x0007ê.\x001d\x0015þ1s'6lë+5sË£2³RÀ\x0004nÀ»È¹\x000cq¤Ã<¯ÝÈuM®§ÈaI.¥,gaoWîX;\x001b]\x001bý»rãjò©UîX\x0001\x0002îXº\x000eø\x0012Úp«å\x0003Üê\x001cä®$º¹£Ì]}bj-Ms4SÝªðú\x0000v\x0011ÞÊØQLa+
\x0002·àQÔZ$pÙ¢{ÓH®ZãÇqrðìI\x0008"bö\x000b-qe¸-ÛËk\x0007×ÕÞÄ3àÎ}\x0000\x000fÜ\x0015DPÀ·_0:ÈcM\x001egÈ\x0015uFZ(LcHà6ðZ±Û
yíà¦Úøq\x0002\x001cË·òÁhÊEAP4Ý¹UAé\x0001òúÌWS¾\x000c\x0015m"Ý@¼.
æP7p]\x001fúzêÐO(Gä\x0013tq\x000f]\-Ï\x0019!÷5¹ZåÜ\x0002\x0004¹åÅ¢\x001c·¨wnõî:@njr3E®\x0005A:zn\x0001ø\x000cîÍöK;¸­l¹¶3¶\\x0019ÎÐÅâH}Í\x001bÎÿÅ²Ú"}ÜW&\x0011?Î§["·,ý\x0004ä¡lÐÕ6C\x0003äµÃ¢§\x001c\x0016e<5úHäÓm$U#ù\x001b4è|æ\x0000MÜDî\x001cçt\x001bË>âVËCÞVéïQü­wãð\x001a{áQ»_k¨\x0012Í[á\x000f\x000bf_ø»cø»ß\x0011üÛcø·ÿôðàQ§\x000bt±ëð\x000b¹<\x001eÏÞ<þ©1Êôô\x0012\x0015´åJ³\!aèÛ³7·ßoòZSñZ3ÆI­ñ \x0000J\x0002?èô²PÎj?â>^'+^'\x0007ç×ÁeÍææn¬J\x001bU\x0004öÀUÒ-qñã\x0018nð)Y\x001euN¤Dák#kËÕ¾NÞPóAÞÄ\x0012¯\x0011,ê¬\x001cí9¥Ö#è¼±æ£ó«)âDH:NY.·UvS\x0003¿÷Pqx)q}¼\x001a¾ÁúU×IV3Y\x00153éÞE\x000c¼Lñ2A¨Ï¨I|¤NÔ°éTÖ\x001cP\¬¢âj®6j\x0014\x0012­Ó°øB\x0019	þùîo÷\x001f?Þ½¸{ÿñþC«Äq\x00106\x000b5c\x0001­¹ÖF	®?HZ\x001bqûçgO¼|}õüùÕÙËï®_=;©vÇ\x0013Õr<Qí5 ¸,P@ÂÀQNU$ÂØ¬\x001b\x001e\x001b\H°Â¤\x0014;(µÈ\x001e¢CåMº\x0008Ñë£Ûå£\x0003õâ^\x0003\x0006%Ó¼¦\x0007z<¼¨W\¿ Mh¡#Z¶×\x001b\x0011xîä9çy\x0017iMY\x00132\x0006³ù¶:6"g«\x00119»Û6¤\x001a]\x000cÅ.X.í\x0011Û\x001a\x0013£#rõÜ^ß\x0011J¸Ów¤K)§¦ÃEÆm\x0001¤Á\x0001\x001dz\x0003¤\x0001-e³¦\x0006¤åÐ\x000en£H.ð\x001bZÜ,5\x001c\x001cPm¹ån¦\x001b\x001cIôYÓPkê²\x0015o¢ßh\x000f\x001dâái<)\x001e¾ÏxP)V:SH\x0019\x0007.\x000f¬\x0003rÕI¤Ün'QÐ|\x0012aÂB¤È³!á\x0019\x0019âvvØØê%§ö[r:ðÔb\x0012E_$}E!l*¸\x000eÈ×\x0003ò{
\x0008\P÷5,¦ë
ëêÉàW;ÌÈøj\x0017\x0019¿×.\x0002
·NöP\x001d\x0017*laO"»)ÎØ="ü\x0001'Üa\x001b\x0001¡\ÖË<=½ûòåîSã\x001d\x0001{÷R\x000bMmR_e¼#8O!a±®}¸#<½¼¹¹|¹\x0005­¥^BãÇQh'õ9õN;¨Y¬_Ëu2~óå \x0019úÐ|,A»8\x000emøq,X8åó\x0015Ò	z\x0014p&n=1µB\x001béÐ¦\x000eõA\x0018&u:w´<\x0004Ý!¥X¯¤î¦>d\x000c'j%§¨
M5\x0006©ùQ\x000cþ\x0005ÛáVêz®ÕÄ\c7À\þåLdt\x001b8pÚÐ\x0006 c,íxÔî)÷e(^Ý¦,ytãTX\x000e¿¸PU?+°æßß?<Üµ¦ô;\x001f\x0014¥\x0001G%>¹þËF>6Uó~u}}y*±ÙUÅ~\ÎÛÇRôfíLÎS³\x000eNY"ß~±î!/\x00020Ü¹Y÷éÞè&×æY'¥\x0000pætSAo+ü¢\x001bÀS£Ù\x000f/5ÁGzq\x0007xja\x0005ðm%ÍðÕ	skÆc\x0005\x0013Í¼$CjSÁ\x0015Á7´mn_\x0004\x0001\x0010>\x0005\x0001&è-É\x000eÆ\x0019Ò$³Æ\x0004ö 7.x_ÃûIx!8\x001akÁ·×¹êM\x0007Ã.#jÁ\x001bé2µ­9®íz\x0005\x001b¢
¾ZcI0\x0018ÃH{\x001aÊeÏà\x0004?9õDS-=<ÑsEµé\x0007lÂ³¿\x0017Õøºô\x0008Ü}~luÍ%Âeí Ø«¹ë\x000bw]lðÍ\¾ºÝ\x0004>Ä\x00108ÈA`gS~`
*uXb*l&Æ´\x0001Kå«\x0019®®\x001ebX
¤µcPÌ;?£bo<"^}í$^Ê¾Zö¥Xg$(åÎ\x0015µ¤QÜùÝ§¦_;\x0010«¨Äøq\x0018ÌZ:/\x0018C\x0000Ù54Z\x0007À«Rã}ÀZTS¬Åè\x0014Ãyÿ\x000cì¹Áµünæ·\x0013G\x001b¥ª¥\x001a%Ö\x0011\x0008iQH|¹NÄ»[xÓp!>Ml]j\x0004zè%\x000e¿¸¨[üÿûÿüxÿðË]kß3|µ¦\x001ct\x0001×|M3Ñ\x000b®\x0003\x0017ÛéÜgÏÏ~¼º~qyBéÐ\x000f®\x0008¢\x001fy"Ýèøç\x0008=PÎr)°X}\x0018@÷bîÅä¬\x001b®o\x0011\x0018ñá.o+·sÿÑe¨Ðed×\x001a±Fpêó£ÂpmNC\x0003ÈvôCd7¡G5.$ÝÖPX×gôà8k\x001bºn·ûÜOk¼($t°Ê3:Wéë\x0016]·föX³Ï\x0018\x0019so\x0011Z09ÉØ\x0004ãÝ´\\x001bÙµ
Kötw\x0014]4TAÇMZ
J"ä<ºÍ\x0018V\x001b¹N)\x001c*q8Üê|×\x001fï\x001e¿b\x0016àÝÇ\x000e\x0019C8#=k\x000ex¼¶¥ªK®soPÕ¹9ûñòö
f\x0002^>ß2ÌcFUc0jQhnV
{ \x000bÕJÔ¬ËÃÕÕPAÒ=\x000c]\x000fCï0\x000cì÷÷^Ì¯Fb~z a\x0018l£\x0015\x0014<;Ä<\x0010Éâ^Æ«lêÎ(å#QÊï1\x0012%¹é«\x0003594÷\x0014·²¥ÁnïH|µGðã\x000e#N½¤\x0005«óJ¸ð@ÔêÓëø@ôB\x0011\x0002\x0006¢ã=\x0006RKMo²þÔ´ú5-åÝ#õHâ\x001e#ÑàlÐw¢ÒÖOK,v iÈÁî\x001d\x0012ÕHØc$`®¨ç76fËÎ\x0007\ø
'v[A±$®Ú&©KØ\x000eß	µÂ~Ø,4ÞYmØ\x000ey÷Ã×ßßå\x001b1Ô»|0ÜÏ\³B¯¯Øpï\x0018Y
ÄÈ]\x0006"¹¦Èc³Ù|ýJÐQâÄj>Âø@¬¨\x0006bÅ\x001e\x0003m\x001a^¤\x0004Ò¥à9XöS¶Õt\x0007Fâëìq(¢à5uÇ¾ÅY\x0019Npð¸~CÑPd³\x0004.]tSMí,é\x000b9>Kkíè\x001dI°ÕHÝc$ZðêBQ'O\x0001N0%x?Ù}$®Þ'n}"ÁðcþN¨Õ±L\x000fÊy ~[¤´ ºòÞÃ\x000b\x0016Y\x0010\x0006¾\x000fI+KD¥xemVþ\x000c¢ö\x001bÝ.~#
+æ;Im³^a«p(¶÷@¼©¬7;X-|dµ¤¨\x001cÖe¥HöQ\x001cLî?Xd\x0007¿1$×¹¤ä\x0006a(Ü_\x0006²¿\x0012êØCR,\x001f\x0008¬­aà#îú¼¸¼ã\x0008óÏ$\x0003#±ùÅó#Á¹å6\x0018­pnòWbCY\ÑìïÊX\x001døqè"@/\x000e\x0007Eÿ±(açÈ¥\x000e%F!ÚcyÁý\x0010\x001døô¥  É_eõ@¿ï42\x0014u4\x001d¬0Þ¤ÈågéyNp5\x0005°»\x0015Fã4\x001dNE¬Æ£ÄJêù½\hK¹pßßQÁTÂ£¡]\x0012H4 H))Ç\x0008õþ¸o»\x001fòRhQ\x000fEïàt¥¡¨½ÀªZOß
kÏ\x0006¹Ú²yÜ~	!KA>E´ïv0`&\x0016OØrO\x0004ð·8WÚßÂ\x0013öªç\x0017çëí\x000eÞ\x0017jèÒQ/ùÒ\x0008ß\x0010/1u¿ÁÆ¯D\x001eyóW\x0012øãLPQ\x000b/Ü÷\x0011L[LÙv¡¯çîøë_kÿð¯'È£g p\x0003NÊÏ\x000f_[®°uX\x000eÓG­æS¾U\x0011Èqn3i\x001cÙ_]¿i VKb5NleÑÃ½\x001fô­+µ¬Î¯Öxõ3ë%³\x001egÆú \x00173s$ÉY©ª»1Û%³\x001dgª(&FjDYó;8*mN3GeYÍð\x000b<1ýò·»/_òûõçÇwøç¯à^\x0019>Ç´\x000cnP¤d±fü½x}ys\x0004à¯_ÝbûÕMøC\x0006$Âc\x0002ä\x000c¼\x0017¥ÊÇ\x0005,qNi¿J\x0008·n¹f\x001aGàå¡Ô'Ï¼¢wØ",Á\x001bØ¥\x0004¯c¤c7ºUõ!x\x0015*x,¾ÏèøÈô ¾8ØÑgÍª\x000c¡ÇzÅÇÉ%\x001f]J+K\x001dÃâynw\x0000«=·°ªà;\x0002¯©V<êÖÍÌ»U\x0014\x0001\x0000ÓÎ¢âVR\x0003$ÝS\x000fk~éÙÁÁßÌ\x0001.dl×gµå\x000bØg\x0008à×g)¦®\x001cd<\x0005À¯\x001f>¶AÃ)/s%\x0010¶¡û¤¢ÈnuIúÜ$ã)ü£7Ïoãê%®\x001eÅÕ\x0012Q2¯-
"gò­+áöâ%®\x0019]\x001fÛ±]\x000e¥XÃì:Wh7Z\x00125ãÚ%®\x001dÅÅ
\x0019æ\x0014½ÙÕ¬~·^!Ûë¸nxv\x0003§É¨¹F#JWpWM^/¯_òúéµ¶L/\x0015ÄÀôå°\x001a°íåKÞ8Ì[
¿03/2¯:ÌïänpÏH\x001eÈAX\x000bÜM¹è\x0018òxvóõî}kÏ\x001f\x0015%+ÂhÉáW§ã\x0002A¹ê|P÷íÙÍËïNô\x000c b­*b­&ÝA÷¤ËXªÂùÕÈd/o=Ãzf\x0003Ý\x0015±ãô1ïV
}+ïAè8ñ\x001a9Ì\x001b)·&b\x0002»T,\x0015HÀa«ÏG#°\x00150~\x001c\x0003Ö`Ô+gF$à\x0010J­]x\x000fõ\x00177Õ_ñ¢Ú\x0017µÙÓNK\x0016³ãÜúÍNõí3\É­Ñ,/ztHþrT2+á´á.(\x00177ÅýVøÔG²¼)?AUMüxñüþì\x000fw_Î^Þ·KH¢ÿ`RÈu9p=<è«­YçWg¸¼9{yuB\x001cY~fE\x0015ý~Vã\x0003%Ï{ð%\x0010\x0005
Î(¹~Ìu \x001aQ¡âÇ\x0011Ô;Ï£Ò¥â{³Ô9GaÆù\x0004*¦õÔ®:ü\x0002]õrË¸ÿröäþáçÇ\x000f÷\x000fÍ-çaìÜ¹Ý÷NÖØ\x0007\x00055¶/\x001aW7gO®®¸}vu}*ÐHüCä\x000frv\x0000Rò\x0000\x0014$?ÏpdâÄú{ÉØ\x0000\x0016\x00158T87\x0002\x000c/åo\x0000¥Ri\x0000ë²1\x0005nß\x0001\x001c\x001e{Ò\x0000ð­gr\x0000$²²¼¦\x0011pcôÛQ¾\x0011\x001cºó¥\x00110=\x0002IÉ\x000fÁÂÅ;P§%ÏíPiß\x0011\x001cJ,Ó\x0008¢\x001d\x0013X\x0011F½*ów\x0015\x000b¬1³\x001ax\x001f\x001b¦²CÒL\x0007\x001eÖñô	p\x0015±´Ïªþâà\x0000tõ\x0015$µÉ¯ÀSY065¬L_æÌQ¬®\x000eÀT\x001b\x0019?Î/"
:á\x000845îRp\x0002#X{y\x001a\x001c«¿\x00037ý\x001dxîÓ\x001a$K*µç5$6cÝ}ü¥\x0011IæÇF$Óß\x0000É\x0017iïðM3
@\x0006û©Õ¾Óc#XNã\x0008ë>7\x0010¨i]0"\x0005Ó\x0008¬å\x0011¬V\x000c\x000e\x000eàPD\x0006E\x0014\x00030èº¥\x0001hN²\x0001ði\x0016üjûà\x0008Tý\x0015¨É¯ Õ}(\x0012IÁdq:\x0017täÎöjµ}t\x0004²\x001eÁ´S\x0017X«&\x0018%Ê6°$÷\x0002ÎÑª×?8\x0002[mdü87\x0002)5uý
xÛ4`)=èUÅçaS´|`sT=C\x000c}\x0015ÆÒë8f\x001e>wOµà¶\x001f?\x001b\x0007\x0002&¯~þÄ\x0017oô_^ßýíþëýÃÆ«¹ÂF=¢:<°'Xp\x001e®©«Z%\x0001óúòõÕ«ëg'D`h\x0000Ö/\x0007`ýä\x0000\x000clç\x001cö\x0016\x001c£¬z)§ÜuÙm×Aõ
À»å\x0000¼ý\x0006'%Aïuîä
nF,µuÛºðå!c\x001dñ¥?ÖÍêæwÔ¸\x001b¶B\x000eIaa(=þ\x001b½Ý\x0005¯\x000b_\x001d­ÿù
`\x001d½\x0014xkT\x0019\x0001\x0006\x0012òú1Û5B½#X"\x001eEé56\x0010Î'\x0018tçð
A½¾
p¸²)*-[à\x0017\x0017Gù?}xèHëò\x0001\x0005e²D\x0012¾Ý|*§{Y
\x000fiÕR½ñÓ³ëÓù\nÔ\x0012ý¨"¾\x0017Ý«CèiÃÈ1*FÇwéýÐ£_¢G?\x001ee\x0012/Óø
\x0010Ï#]*
\x0005ÀÁ¶6õm$ÅKäò¨\x000c¶\x0017\x001dÕe¨³\x000bøCØ½àÆ9Aî8ëR¹ÝM±cÊó."5UÂ¤\x00170ë¸ê5°/"ûqóÐNöDZ\x0012;JJ¾\x0000\x0010»«Áü!vS³O\x0019(RN»$±\x0001=éWéuéð\x0011ôP£ß\x000f:Xöåû\x000fY÷£\ä\x0001\x0003ý6p\x0004ÚQü\x0007\x000c¼³làcK»¿­\x0011Àßíê]øÅEîõôóã¯wÜàï±ÒR\x0004Ý\x0006Ç¢Pf;è\x001eçoÞ\nC«%´Ö\x0018±\x0015¥Ü\x001d¾!âU±!AªZ/©õ0µCÓe&¢Äâ.J0®è)­>\x0011õPx´@ÀØ\x001e%?ýº÷0\x0017\x001f?~hÔzvðÿ)´à±\x0010tÛ¥2B7j\x000f?}ª÷0\x0017¯n?;¡üÌcñË±\x001cß¨FÇ")ÚÃÍ´äa,î%àn6iÊvEêú{Ñ;}3øì\x001cè\x0012¨÷¢\x0001ÿãíÆ´Cc	õXÅ¡GÇ¢¸Æ.Ý¹²ì\x000f\x001csP
Å¨#£9\x0004ÒhìñÅwl42\x0008ªèòøÄÊ£Ñ´éQ)ù7\x0019\x000eË[\x0018?ßÜÂÆ¿¢hÊrË}~à+"mOl÷Ò\x0014h\x001e\x0014\2j£\x000f6GqÆ§w>?üüØ|b\x000bgÎs¶	^-)%-6ñÞ®v¹]¶^¾|uýÃí©#áÕ\x0012^MÂ[Í	QóÇ\x0010½V¦Wk\x0006éõ^OÒ\x0007Í\x0005,¤¤r~sjßéS¯=éÍÞLÒ{ÃMBµöT¢e#\x001e\x00184÷ÛÞG\x001f½]ÒÛIú\x0018ØwÂØ£<í\x0010¹»³mÊ8è ÷Kz?G/-Ì1É1ÇQÀ¡ç]ëW\x0011ôaI\x001f&éµ(ÝÌÁéÈò\.I.ÓÜ»÷±fze\esä\x0007»/%õ¦Tãþa;/Ce^<wó\x001f)\x0016\x001d±®Bæ\x0006B(ZNóïV\x0008FíNÕn%ÙãGþ
ìÏÙò®\x0018ø\x0016áSÛú=Æ
ÂñØ:d<Eqq¤øôîýý'\x001cJóÓXðè/d\x0001eÉ7}-©,\6\x0015¸?½üîê%\x000ee^%ýQ|¥Þ:\x0001¼ü°§<%ÚµZ\4/\x000f¥\x001f§øå>§!b\x001ahüÈ'v-5íøj_kçHÍ©\x001f_S3\x0010\Íi\x0014>Jø
\x000eá]ñ¥­ð¥ÃG_"\Ø¨Ë¬\x0015|ôjÑ"ÒÁhbø]ã7:Ç\x000cÇ"½¥zl>Oø~5?{\x000cß×ø~\x0012_\x0007KÒl!Àé%%½µôN».\x001f}ð\x001dí9ÒëçÓ+w\x000c¨[H	Z&:Z>XÆ´+ÿ¡7ñK=»|\x00145\x000fð] \x0008nZ?M¿R«ÞO'Hiþâã\x0017°0¡\x000eÝ½þðîîá¡½)\x000böß òFp\x001drÃ0\x0007×_ ·«"ràÝëgO/¯¯Oõ[ ôC\x000b"D÷v\x0006=\x0018yN\x0011^%Î}v:CäþVl_tÛÉåAz\x0014Éñã\x000c:j§R¦ÒÉØ\x0003çK±ép6¡{Qß\x0012á\x0017õ-1½X¼ûÔQ\x0015bçÖ´:\x001aJÊu\x0015láªÒàl¦\x0017ëç/O0ÿ!¶üZÎ\x000eÀú!
ßóÂ1Å^ú¸ííwñ»ßMó\x001b¶ÀïQU%ñ+nê\x001eÄê\x0013êè\x0000ª\x0005ä¦Wç´îhÐÛÔô\x0005èrÙ]=°\x0006\x0007pèö\x0003ðav\x0000ÖqE\x0017¶Y¢NVFSc(\x001cÀ¾ü®#È\x001fÄô\x0017PºD\x001a\x000c<ÐüsA\x001a¸ý;ïàC\x0013\x000cäq?Ôæªêúçç.\x0018A4DKz\x0006 e5\x0000)gG%%ZÑ\x0008"eR:ø-·Ã\x0016
)Ñ]#0¶\x001a±³#¹9ZÚ\x0003©M®\x000b\x000b¥_ç¶Fß\x0008lµ	Rè¹\x0011 &E\x001c°\x0006FPÚ/z¿ú8?8\x0002WÀMïãà©F)jØÒt\x0014\x001b¯K¼yUÀ­\x0004Gïóð\x000b|©¸~\x0004\x0019Ýf@ÿz÷©Õiv\x0011¼\x0008*\x0006·3G\x000cÁ\x0000qÝ|Xm\x0006s}\x000bÎ2:ÌÀüæòåIwÙ\x001f=Ï#³\x001ag\x000eÑYT^QÎ*¶é.Ô«u¼ýÐf	mf&:;.GTº`½\x0015\x000c\x001dW3ô:¨?*ã_àT\x0003ì;^ÜßµÝÜÞE¸\x000b¬`S+ã¤\x0014Ià«)Àûö÷¯`eìAÏìzÉ®çØ ª)`³6/ï õaÒ×Ê\x0018»Y²9v\x001fèZf¹­
ã09x\x000ft)mmQð\x0017G\x0019??}¸üwøùñc{oT\6®VS;¼Û°í\ÞýôìêöÁÏçÏO5H-cÐË1è\x001dÆÀ­5`\x000c\x0002k¿h\x000c|)ÇN{Á,Ç`v\x0018,ß\x0003¸Ë×\x0011{8¶áÕ=\x0006»\x001cý}®%¿\x001cße\x000còð5\x0004þ\x001aüoð5\x0008£ê-	Û²hëÜ|þxß*­ãb\x0014eî æE`þíAwkC\x0019êæÕó«Ê:D«´jÖ±/)±Äv¬Üú3®Ö×uÒê%­\x001e¢õð·à¥\x0015TØÆ;Yæv5y§Ö,iÍ -VÑÜ\x0006É¢¡x¹N¬K\x0016õÑÚ%­\x001d¥5T*\x001a%,a2\x0019þ ¿¶ªBÒ	ë°nt!8Öµë\x000e'M\x0004gLY¶k\x0006®Ö/iý ­T~Ô¶Ø«*\x0012N¬ÊztÒ%m\x0018¥µ¬\x0003\x000c\x0018Íí!È\x001b·´ÁZiã6Ï­`sëñ18ÓªXLÂ>´¥óU>\x001cÄ8nd\x000bf¨±\x0012.»\x0013m}e\x001eÅPX&n¡É\x0018üAq'Üê,c\x0019&orp
W.ãzW\x000e³ö¬\x00079|>DJEM¸×8l´
ÃæÓ¬×J'Z\x0012×\x001a\x0016\x0007!IÅòËÁÅ¢\x001c¸Z Ð\x0006
ûÕ\x001cI ksñÍÛÃ\x000f\x000fwÞÁ\x0008\x001d\x001dCÊU20)×?òsaC#Þ\x000f¸¾|ùÝ\x0019\x000ce{\x0000j9\x00005=CìXâ+\x001cûô«fíê\x0001=<\x0002½\x001c\x001fA,O¶:k2Õ¦¬w·ªÚ=`\x0012á\x0017\x0017\x0007á¾û³×w_ÞÝ=ÜùÒZ-"b9Õ(`<²L­§\\x001d'Zõ³ªÜÕ\x0019\x000câéåõÕÍÍzL®\x0016/'@\x001f'ØciaÀá\x001cÖ)Paµ_{\x0017»ÕéÕD.Ö¸8JSø\x0001(\x001bcàÅi26A(MíÜ\x0014\x0007Ò\x000c\x001fà\x001f\x0012ÖÏÐ\x0007µqVa\x001c\x001aµÑ©;	ø¦YBÌ ¹ÃhSRW\x001bô!¡\x0008¡òº ?çæV:§\x0019\x0013#÷\x00125«[ÝÌ±è81ÑNÒ¾ø\x001eNÐ!:2X}Îì.8´¤ ¶$÷èCàyf)w³\x001eéG65²BvÜ ÕÒÑÔÜF~·](\x0017m\x0001\x0013´°\x001dnß\x001eß?²¢±âÐj}5\x001eÜM\x001dkê8L
\x000euÀ<ÊD-=%Ø\x0018ë\x0003÷U-­6¨EH\x0011;U\x0007üâB}ó4üäîË×\x000f­ozØÈ¯äÆq¹µ\x001c~\x000f~U×¢>Ü\Þ¼yvêEèLs¢×ßøWôÎðkñz\x0016¡Ke\x0018µdo\x000cÿp¾#þ·\x0011½øKY­Ð$2\x0005ø¤"£Økö­D|¹h\x000b+Ý<J$þáþÓ}k'\x001aØ*©ÐhÌ0¥ÀOåS¡¶]¯ÞY®ø«W':ÑH L\x000fÙ%@Èø±.¿{óøá#ê1µ¡ËèRO÷$wjRÝ3jéXRîÚlô8éon=G5¦SøyÑ\x001cÞk\x0004,\x001aøJß<Üýýþ*\x0017z[[)]Ã³Y\x0017Ü§+XU<µÃèÍõåOW×Tº°ÙÕð\x0017Zð´à§øá\x0012uÉ`
sêÌuèì¬V\x001fÆð\x0017".*.Sø¾¸/xªæd \x0011/ÓïÖÜ>~¼L¤d²²gñ:qÔ\x001eþø	ÇpßÞB
\x0005riýDÔ\x0007Ï·
e4KI\x0016§\x0011þø\x0012Gqu²\x0014\x000fAVCóCÐ¨bà)\x0005Ý*í\x001aVÎEß\x0010t5\x0004=;\x0004\x0007\x001eC®aó0\x0006R2âD¡ýjC©ñ\x0001,Àò\x0010îfÇà-\x0017e{øF"urF²jÉDo\x0019é\x0000\x0013îð|\x000bà¸ì\x001förû9\x0010,¦Md\x001a,F%q \x0012]RZ¯ÍV\x0007\x0001låsNß°âø\x0018ë¤ñ (e)6\x0005¥Äê\x001bà\x0010½ò\x0015½:\x0016è¤W9eE§vgtaYò\x001f´Ûö\x001fzè\x00172;H_ÉìôÓ\x001bXù¤Pß4K3ycyåíæë\x001dôJTË^¹uÿ¢\x0007gÿ¨ø\x0017~qñ­¼Å§?}øÒ.a'õüvJ7crßa±÷)lM²	/¿vsZ/à IFPk¡hÀDcU\x0012>Om(é+ØVöê\x001d©Gp¼þûG \x0003¿(\x0018çÓ\x001b4@Ë|\x0006+)L£xEë\x0018®¾\x0005¥wù\x0016èñ\x001cÏ\x0002oò\x0018¸UëÍhºÇ TºÊ\x001cnïð\x000byt}z÷\x000bü±9#×Á}»\x0006ÈÆ\x0019zô\x0015n»êêìéå\x000bøãÉt\?$\x0014'ø£â^xTo2\x0014&Ö\x001e\x0002%xïc¹È4¤twÐûÞÏÑKz8´4\x0005çÔù0çu»¼ÞÔ]Å\x0016\x001fÚ¡9þåË¬Ë\x0017@þñ¾9íÒ£p\x0002Wõ8îç´¢p7\x001c«£y/\x0000ýùÕÉÑ\x0010Ò«:¤EÃá};úü\x0001¦ýó/¿<~+ØÙëÏ¾â»flÜ¿±Ôµi¬ÉËÛ·hpD·ú\x0012ûÓ«g0ù¯^¼¸}	÷°³×¯^¾ÁGÎôÏÞÝ½¿ûò\x0015NSþ\x0003ä­@eVü÷ÒH\x0008ÆÅÏØèæéï¾Þß=\x000eÜ)QÉµ¢â#øÊcÙÆ«õð\x0000ÿôÇË7W·õ­rc\x0010X2´\x001cD*!\x001b1\x0015\x001d*\x0001¥\x0007\x0014!%ÇÈÍjgâþ1Ô1«Tw>_\àÇçx
üò6íáröÝÝ/Í>)\Ä\x001c-'\x0019(\x000fÖC\x0003*»Ú{3\x001d\x0002/¤mñòÕkøÃå«\x0013#¶º\x0011<_ä\x001bA?56k÷äÍ\x0005ÜÔÉ\x000b=é¸\x001aDl!Bþ\x0011\x001d B
¿¸H/^Ãþ}\x000e³}÷ð¾1º\x001fpÃæØ	ø Y^Í"\x0003
¿]³9°]Ã\x0004_^w
ÕW1Z@õ)Fu.gO>?~øòås£8WØ$·MvÊÌ +-\x000cà»Z
écyËÙW·Ïnn^½ÜÀ¿',qÓç!`
n1uØÆ\x0002\x0006ª3Ug×ÕÛl\x0017°.®d\x0006ÆÏCÀRpû ÅÃ4I°ö¼b5U¸7$
7wà
\x0017ø±Æ\x0005CÑº=X¹óC \x0012qÞ.1>Ø´(ÀF\ÈÒW9OÐºd GNI\x001fJ{\x0004'²k¹ø/jÿÖv4\x0012q9ä\x00131\x001eò£È¥ E»Ô\x0005.#S&¼\x0012ë\x0019\x0004íÈ
³¬\x0016Í\x0000á\x0017¥\x0019àk°Á]Í\x0000Kò¥\x0017
Ã«Érl]µÁÈ\x000bF8µ­Ûb=4\x0003L¬Ô\x000c°\x0015\x0001æÕà½*ÅÄ,|¤À¯Ý\x0001uÑ\x000c\x0010Q¹\x0019`/j(BSAY\x0012\x0017SC\r]\°Õk-­-~\x0004üâ"}\x0006Ø\x0003ÎÄÍÝ\x0007XÅ¾~nc7
3\É§C×tØ)­=½¾;»*Ñô|á\x0004¡Cqsù\x000c\x0016ôåË7¯N\x000c%sÈÅ
Áò¦¼BRT÷çû/g7.H#Ø\x00176Rj	\x001c\okÕjÞÔó\x001cÍýáêúæìævÝÌÁO_ëòaÏ#]¾?sñáSsõ!¶m£j2£({Àú\x00189eÛ®>í-U½þ\x0000nÆ³7\x0017w\x000fïîÿv¸Vüñ­»ûÛÃ#¥§}+\x0005üðxÿñ#FØ©\x0015\x0015è¾y|xûá>ÑYcµL1\x0006
¹>\x000b/\x0019¡©ÄÄj¬G½¸H/×O]\x001dÅ\x0018®o¯?_Éâªñ`ÿê!¼Íñ\\x000e(#\x001eiù\x0002_Ò¥ç¯ öói
n´OÇ
uÀË	,hkáðÙ\x0005\x000fÃVæðXËüIRfÀg\x0005Ê4ø<1Öæ&ó°EÌqC\x0016@\x0013³_0.E\x0001\x0005uv³\x001aßv\x0000Ägof\x0000ÁPÚ\x0001UÌºpp=\x0008\x0014\x0011\x0002Àô®7\x000f\x0008\x000bÅ}#LÜ\x0002è*t\x000242W2! \x0000YpVì.p¬¹o\x0014º[\x0000ñq7ó	ëÂL\x0012;$>½Ëüa
C\x001811°GRÀ5}Á.K·\x0001\x001fWÃ\x0017,ö0\x0012[\x0014¦\x001fý*+\x0002#¡4å\x001bÅH·ìá|n¬Ò¡DúÑM§EHÍé5æÁ¹\{`°\x001d0Ù@ãö0I`°V\x0019lµÑ&¤ã\x0008(s5+Øè.\x0006\x0008\x0008ßºl01§ç\x000fI/ô7ïÿ<GÆàlúÑ\x000fèr2\x0000TÞæ\x0010FÆl¢MÄ<ÜyÂä¡o\x0018\x001bå®40äbá\x0014 rúËÔ\x0017l0f~to\x0010\x0019:ÁÁd¯\x001bÆÉo
ÖF±Ç7Z\x0017îÛ®\x0003
ó§0?\x001fÂÖ\ä
ó'(Nj¥OWÛYÂÔ`ÓûSX:C~ Âà=\x001c÷pk\x000f>O\x0018ð\x0002~ô\x0013Â1·±ÅBy­L\x0014Ô§ÁN/A|ü³û\x001b(
é\x0014>q%8ì¦á°\x0008~\x001eO'¼3XGõÜ4f=Ã%/á9¯É	¹\x0012l
O¢vrþÙçÜ¹Ë\x0007gIR·ß\x0005¾x´4ÓO*ÌqË?û\x000faÜÁù(gïI¬K°Ó3¨ðm5ÿ\x001cøeþvá\x0000NÅ8§ÜJ\x0012\x0012³Ó\x000e9xøÿ&Ú\x0005"\x000cQ³vI x\x0016\x0011¯`\x0017\x0017ùçÀ)®Ò),óS\x0016Â\x000fa·ªÜ\x001fïÒ·¼ÌÄkß'Ò¿,\x0002
ÚÇªfmÈ}º§7\x0013|GKñÝ\x0000¥Èå\x0005:\x0011ç\x0002üA\x0002Rîp'Nïò}?eÀ\x0012GKNy\x0000J¹Ñ\x0001Ê·Dùv`.H¹êRdù5KË_ø>\x0011\x0016S*;ÎÛûÛN7
 ÎxÚá&¦·lp\x0014\x001d¥¶Z+ÃDá?ß¿ÿ»[\x0004á~ºûøñ>×Cß?<|¸8M¦\x0014n\x0005nNnWkÔçå¨ò5ÜOÏ_åúç«ëëgW×
d\x001c@êD³©Ú)¡iÒÆÐQ
º\x001akeFÃó\x000eÿÓ¦(n¤w9O\x0016OR(\x001bn\x0004qkÖ~õ´;p¡Ë\x001bú§,fU\x0006äÂ\x0002·ümJCé[\x001a³L§§\x000c_yñ?½h&î\x00026_Ô\x0001ÍÒ5	3ÝÔ¥6aéG\x001f\x00172u~A0árÞ¹IÀ"ô95g©Æ"ýèd\x0007Ê*\x001f5*Å\x0004´£Ëï\x0008\x001b.ô£-ÝÆ3ÊúbÈFuäÀæ·¾ÐM¶CÜ¥ÍEláØàäó)\x0013yÞ/D½M¡éI?:ÁPjÂg0¼\x0014y:\x000bØÜêã#kdÒÐn¨~ã\x0011¤¦P$M©«4²i\x0014ÂMlp>ÈY6TúÑ9o^oçf\x000eÔÃ¼ÁÙÉlóTcjhúÑ9oØ<$oRp6Ë¼i
kc7\x000f\x0006¶lÝÆ
ûQôÀ'¨iØ\d6/¶æíôFÀ×Ûô£\x0013Ì8>©<X]\x0006³$b\x000f`ÓÆ\x0003.Ò^4u®*Ìð.ðG÷Å!2´Ð?ia\x0013	-æ&eøm²Gd¶ÝM6©üéG/¥ 
&^å*dó´Ò¬PÓÞA¹ô£Í9r¿·y\x000b\x0014ÇG43Ï&­Û²\x0005\x001b\x0014¼F»\x001dËFàByørç-ÁþléGï¼ù2oÎ\x0016¶@*º0oÓÞE%÷ô£\x0017-g²½ï,²Ó\x0012zÓhø¤~ô~£¦|£°)è¾§=¥jéùSÔZ\x0018\úÑ;i:¿*üf
\x001dTÁòRSb\x001aÍá_áú\x000fxDóÙ|U\x0017Ò\x0017JÞ¤Ë²\x000bsl¸\ÓN6*pF¶Ã\x0017Z²tá4Þ¡©º5ýèDS:UMiô¬\x0004ßª4W~il\x00026Í\x001f8\x0011ÇxBbCÍ©|I6|áÃÈõ<\x001aNê¶ ±Ý@BÓ£\x001e\x0006\x000bí3³ólh9üù@	=bÃL\x000e{p+I\x000fîhRcáAþÙéc³\x0012M×\x00173ëáÎ\x0017ùÊ·5i§}I8=1üèÝÀ)ªÊAeÉ²y^kpPMðïÀX%:o»w©¢47åeê\ð\x0014=i\x0013Ü4\x001eØ\ÄCÓÛç©so²½7µ \x001cA´½»àÝe¼îïÖ©TTx2ä>\x0004xlQ\x0016vnúªtï3ÝûîÉ|£(íF¾¥\x0010eòÌô}\x0001þ
<üú'OlLà\x0014ãó!r\x0000)Í=ÛD÷6Óõo\x000c}ßæÀÖù\óÇ\x0017C¼ß\x0018¸oßå}û®û&è©Hy#ÏùÊQ^+æ¯hóÞg×»ò0%5Uq*«¡Ñ£Ô60z;\x001cb2¯<9°ò´£°\x0008ê1d)'¼\x0010JÂó¹rÖEÏO3è¦ã\x001fúO
x\x0005\x0013áÃ[4ß½¦ïÓhZÞeÓÒ½üá·¤\x000bH\x0017	éÙðy5}ÉÁÍû.oÞ^¼ÑrU¾àHN	ìài?í{Â\x0005
·\x0007ü~Ã\x0006N5\x001bø-DIJ}\x0012æB_øÍÞçoö¾;Ôêøö\x001aS3Ç\x001c1\x0014üÅ¸uÙ9ÛömÞ¶Ý&YÚ$ÏÓ\x0006.â`¦ã/ÕÌ=Ó Ú»Ö»à|´äFáñZN\x000bj\x0000\x0006eìÑíîïÿj~ùëâ\x0005õÇ»_RÅ/P}\x0000¾¯§ à~ÅP&=Ñ¤Ü\x0017¬\x0017¡ì?|{[Býxù"õ\x0002Ô3À{³º\x0007\x0016X0,Õ\x00057üªeàÜg*ÎzN\x0015\x0011§ ¶&*\x0017Tt\x0012ùB\x0014TÊ²\x0002"Iy6¿+Î0á#s÷Ç7{[ÍÕøåqâ\x0012\Àæ0ÔÍäR-2Á\x001fS9IÂÍ%%w	Sý»"¹à\x0006e\x0019sº\x0014Zò<a¯î)(p\x0005|'\x0014²?eçÑÈ\x0014ì¤­7\x0004ÎSèE{À\x0018ÈÊjÒë7#éÉ//W
õAï`=A\x0005ªbÂLNÞyÇv³\x0017
{Hà:©Jâ>V)¦"ßË
{ôÖM2.{©ÀiudÍ5ùÔ@å\x0017TsV
ýe¯1ðïv´ý´Ém&ÕÅ\x00133ç\x0018Z½ö\â}23\x0019EIR*\x0012\x0005¨£Ôn(s:RtBe
¦Deù44
¬pjÎPá¢½&\x001d;¤82\x000b&P#PE>³UxLÉ^£-|è\x000bÄwEú\x0002MYUî(G¢\x001b
þç²Û¨?ì\x0003QY*\x0019ÄNllAíÝT%Ôk×°ô:\x0001T1çº\x0000+g²Ü0&Ùk×\x0015ê-­r\x0006¯b	Ê\x001dèý]W)ù¦ÊqA eùlïlA\x001cYëñßþþÁ[N­\x0004S\x001fÏ>|þröþÿýïÿsùåÓÆ\x001d\x0002Ü<y¢©XÇ;2¥¨Ã¢)Ù_O\x0012¾={zýêæì»³Ë§®®\x000bPøB}\x001c\x0007µ2í©nÑQ°^ýzp?'D7ÎéðÌ:\x000b= ¨!N\x0017~=\x0007·3i\x0001U\x0012¡ý Tfd´æZsåH¦ØÄèvQÎÓe»NR\x001f\x000b) \x0019Kk´8!ÂþzÂp?)äI;¾¼Âä×|Ë\?­¬â{^Imî'EáôcôÛôª\x0006N°Å°\x001a}ûLz:3Lª°\x0008Né9W	¤¾T\x0004;ÍÎBX©\x0008\x001e õHêGI-Çób\x001a¹cy\x0004JÊ³Ò©½H1u6ý\x0018$\x0015¥Ù\x0006`Nc \x001d%ßiï+ThTfxN1\x000cáuñ$×«Ó\x000fÿ@5®"=nN­Nýãñ»*+]\x001bÔ·æ¢Mk~½¬´\x001f\x0014þÒAPÇjpÆ\x0019\x001b½\x0001ià;¹<Nè\x001b&Å²\x000b·\x0014RîÒH\x0001uÓ\x0012qN-Oéë;ã¤W¸(³\x001a0§tD\x0001ª|Dy:L×JoFÌi~âAº,¾é\x0005V\F\x000e×±söR¸FÛï\x000bi*a³r|n]àe\x0000±ôo° Ã5+\x0006­¬?ÿý!¨Ïx7¶ODÈ»¯_ï>}ýrvù§\x000fÿ[*\x0010ÜòrÉÉn©²Mä\x0007æÀb\x0018¯¨Ï\x0000lÂoÞ\¾|ssvùýõ³É
\x0015\x0004\\x0003u\x000eOQ»iÔø\x0000c¨\ÚQÜ\x0017]\x0004µ7u\x000eOQ; \x0014Íµà¨(¨\x0015åv§Î\x0001ì9jAÏÔ0×\x0004\x001c\x001e»\x000céfíJ£ÉSÔàÛx¦v$êòêÚî
C»SÐ6Ðå\x0016ËÑãIÐp0ôîÔ\x001ceÂö³@°ÿ\x000f´\x001bIÄ`¤j÷ÉÎJ,ýcÇM	W)\x0002¼äÊÈ\x00050ç¿Á¦¤¤yxì\x001e3¼§p)ZoÉ\x0016E¾\x0005ó«±Oÿ×_þãíR'\x000e\x001bÉ]~|{ÿðõLn\x001dÊP­¥ÞeÝ=\x0003ç¬ç\x0013&\x001c½ã?Å¦qgÏ\]¿9'\x000eÂ\x0005W>Rº¸´\x0017ìQ\x0008,!Ì÷4\x0011\x0015ÍG#\$\×7_ähtÄ\x001e4æ²¼=\x000e\x000bpå·Ö¾ù
\\x000fÛÃçt`àâ/î8\x001fc+¿ÙõÍLz\x0012W°|ß0O4_ñønØÏÅ/d`"5DJ`1§#\x0018oNw,\x00140ÀE¯Q\¬£±³a.\x0016 vßs`ôøÓ\x0007¦\x0003à`cö\x0000ÌR\x0019X\x001dÀè¥¥\x000fÌ²%Q//²>.`z\x001aÞ5úÀ\
g0SbM"²\x0013oñý`üÐ\x0005fB½îlÄ\x000c\x001b}ì¡ÈFÌL\x001b1LSÝk,ÄrßÁÆ¬\x0015-aÂõ\x0004¹N2YnS\x0001\x0017Ø¤b¦K\x0007¾³\x00035mñ±\x000bÆEúÑÅ\x0005+<R\x001a\x0001&ô?=÷ô1Î\x001fËkvi´\x0012ºÛTD[ÞùÖ¼¾"ÙÀ=\x000eo	Ó\x001e2\x000bgkÙp]Ê_%·.Àèå¬¥H-\x001bÒ..)%Ô£6\x0016¿÷©0nò»¬\x0004þ©V?¬/\x000cêà2»ë\gØPä()«+Â*;V\x0016\x001bYe	
ÖY'Úo?k>û ÚÛÎYÃt3v­\x0015l\x0003\x0016zÑ.8\x000e×¸°ù\x0012erPñÃÏøóßôßïÞ\x001bû\x001b2Ýùòùãýi/\x001bëé./rÙ°	¸Ñýz<îMn¾tusóêùJë¢¯
ÂuðÅÀU\x0001ÁYÔÊ·@×e8_÷áË7\x0001¾Hå<Àgð\x0005>óÅÂ\x0017öáËYý|ð¥:G|\x000f.°Â´öàdÛ\x0005¯ uàiSðÊZ\x0018\x0006ÕUu	(¸]øòE¯\x000f ¨f\x0001«z£é£\x0005Ì¸Ý\x0003ï{ý|.p7õ\x0003ÊË/åÌÐü}\x0000éâ7`_äùÏÐ÷ë\x000eßïQö(\x001fÝÿ\x0006ø\x0002ßæ÷Y¨\x0010í_ì\x001fô\x0002Ò=°\x001f\x0010\x0003Ë\x001bm`[b´â(Ãt\x0014îcß0 á\ñ7lË\x0004îb\x0000ùZ80ãHX*-i	ZY Ýe\x00021Í^
m\x0011\x0015K8;w£LºÜ]³\x0005¿a%\x000cË8ð?É\x0017}oþþåSêuyj©ÒüÝÙÏÿqÿé\x0013b>|úðîÏ÷ð¯÷w_Na&Â<J;ÉòJ(Ë~r§¾eÙÏÓ³\x0017¯þ¿«/\x0011÷úå³§?^Á/®ß\]®tÓ®p1¿ÂNâRý\x0014®T\x001b\x0008Ô¬µtGyí³¸èþ§×æ\x0019bªN×Ö,&Øñ\x0004\x001fÝRFÿ*ùú\x001fÿú«\÷_Î®ïÿþùÃÃ=¶ãù\x001bv«}<}\x0017Õ^Q<MaùµÌ\x001f(ßÇ:Hö×3%®nÎ®¯~zõìú
\x001bñ¼Æþ´·ëÞøgùé/o±a@YéJZú\x000bÌìãÇÜg}yÌÞËiGJPGT\x0003¦Iï×dso`BocÇM8La»p®ùÿ<Ý_¢p>¦©S¨¹rqqùËý§÷·Äê¾Úå\x0011Ü\x0018\x000c×\x000c»#UË\x0017W/¿{uB\x001dµpH¼\x0010¤\x001fÿÓ %9ô\x001a¤èeþÏ,Ã>m$V\x001d
Ë#U¨r\x000cLCøuÒtëã«{ïÒ»ªF=ôãÉÃÝã\x00170'Í&Öz\x0019J¿Ô%©U¬$ªOù'×·7°Öc\x0013ýÏ·©U\uù¿{xxüùÃç³»Og¯??nìiìÁ×k¯³"2º¿Îòýæ×\x001et/¯¯oxöêìæòåÙëW·§¬ÎßÜ_>\x001e3r¿å¿|~¸ûtÚçP1rÞp}\x0012D\x00043æ¿Áã¾Êxu}¹ÖV¹BÃ6èZt³¥Ã4Î%J\x0000æ«\x0017¿3#ñ+l¿\x001aÜÿ·ûÿÓ2¨sH\x000b»ùðó§»§ã®ÖcmNÜ1)hXÑyò'ÔJk\x0007,§øáååóõ|?¹/â?±õ761Ë?/\x001f\x001fî?lYã\x001b\x0008%T¢\x0018\x0006
(àékQåZ¯±ËÛë«gÏ[pÙ÷\x000eP>ê¿¾ý9\x001d´\x0018\	y\x0007~ÞÞ
UÊé\x0004óÔ/\x001d¯}eéÊwa\x000b¾Ê{p\x0004_\x0002.ÒF\x0014-Ï9½<P\x0000«öäqYI\x0007Je\x001aP\x0006\x000cS+Å\x001beúÑâKF«\x0010ç*dR\x000c¤¤éeùð¿Ü¿ÖU\x0016\x000fð_iH«$Í\x0005\x000374¬ÒÍY\x000bj¾)ÿ¸¾üî2%R®NËý/áñÏé}\x0000ó4ðÇsÔÿüøï§#ïpQ9 ½¤ò\x0005QkÎÐ\x0008êè)å9ÊÀ¿ºý_«$þãÞÿý]}¾~üôîÃiYzìÏ'r­\x0016¦>ö{tÜ\x001aÈ\x001cmä×·/>[ßÆÿöù¯ÁâI6ó"ýø	
Ü/÷§o ÑDì<\x0016ÅaßØi±kH\x0010;.n hÚnnÖ:¢\x0003þ÷Ï÷ùóò÷»ÑõÿW¾ul¼ÇiJÈÞ¥\x0017ôI\x0005¥
¶Uí÷|s3â\x000b\x0007\x001d\x000eéç1¤ÄûJú1HâYQÄÂ:Ï¥Ä¨\x001fGtâýG\x0019\x0017×åã×Ï°Â¿Þ]³K\x0000;ûá\x000e~¼þïÿºûù¤1©çbÃÊ^\x000fNp¢1þèÜxó
ý«ô¯\x0002À³\x001f.áÇë«Ë\x001f®~\x0005Uh#\x0008ôð\x000böQþp\x000fþÓ\x001fî\x001e\x001fþûÿnxPØ\x0010!S7%î0ÁLÑòW"ì¸\x0002Ïé\x000fxÎ­»N\x0005O/ñt/\x001e\x0018\x000còïË;\x0018üâ²@cý·Á¯.:³¤3½t:b\x0005`Æó%ôUì7RØÝxvgÿé¾[·Äs\x0003³Ç±k%ÎËä9<õ­\x0003ÚEçt¾\x000e{^Pè\x001fÜ
j´hIßÙ\x0000Þiº_õ\x0019MjÏñKF¢þ¤ë\x0011æÛg©\x0003gÉ\x0017ºù4UµÃýÔñÕBqâ>Xï¹m¡ªéSýÓ§I\x0006\x0007ð$:÷ÿ?uïk×¤	OE#8`\x0004\x0019¼ÀOJ*ÓÓ6d;ÿ)qtI§ªVÁ³Ño=A×8r&=AFp/®}Ö9äà®D\x0019ZÇ¶ô9HÆ=¾¨øh,ã{ ô\x0019Â\x001d>\x001cÆç´(Ë\x001b1¨ÉOß-µãÅîÝâøÃýÄÇÛÝ>üýÜ¾´7¸©\x001aÜâ\x001fäøöÏ\x001fxEüOo\x001f
qQZè³ÏâyKL©¹£,àsÙËÚõÿ\x0017§ ¸þ×ÀÿñÅqÛ0â\x0016#c¤\x0012_Ä\x0005µMÑF·ð9O»\x0015w3\x0018í\x0016£\x001dÇÈÛRk·Ff\x000e&*Ä´\x001bÅH[4\x0001ÑÀÛp\x0005 leqa¿î}\x0006 ß\x0002ôã\x0000\x000bYZ\x0011a\x0008:Ò\x000cÆjÏuuq\x000b1N@wI®b\x000cº\x001eìôÈç¼ë\x0011Á¶\x0018ÓÔ9\x000b»\x0013ò.>ió±Ú_\x0019ö\x0013=ã\x00107.C\x0012aTíbd\x0012?é\x0005a² ã¾N;\x0001²Wãº7\x0019JN2kq\x0003ÚkO*0ëìT#LèÆè4©¥§M+\x0000j`\x0002X¿\x000c²Ó0®\x001có=T#É1û{mÚ\x0013¶8\x0017[Öà:nBô%OÉT\x0000ù#K2¬ìT8ëp¤¬¬/ëre!4AîÆÔg0vZ\x001c&Ôxô2àë<Mß6j \x001aÜ~*o\x0002dè@qAò®çÈÓ´^HIÔr§áú³él
L\x0018º&¡.nR$â	\x001a²³40njø:Ê\x0002{^C'Ê'èüeLû~\x001c#v¦\x0006gLØ9\x000b²$eA&\x0015äº=ÄÎÔà©É\x0014åcmäK$\x0019µb\x000fönø­i\x001bÀ\x0013K*I§ôqùJbgkpÆÖ4º8ëe½H\x0006\x0019½Ùu­Á	[ýÛún Q\x001dËgS£O;'\x0015äAFGðuf\x0006gÌ¢s\x0004mî7&åÁØo\x0011bggpÆÎ´°\x0010
*±\x0010 ÒÉd×¯cggpÂÎ ®1È\x0004-!6=3§âºöé\x000c
N\x0018:ù_«ïAx\x0003³Ûgµúî×LgjpÂÔ8í\x001ewõD5¨öÀîiCÆAÚÎÖØ	[Ctg%\x000bQYI#7èOÀØiq;®ÅÁÖzæÚ` 8í\x0003Ö.ßHÛ)H;® st­q6F¬»SÑ\x00086î9[g vêÇ«\x001f6Ùµ)+\x001b\x001aUÚêÜ¾\x0017\x0002a÷¬íø³ÎY6m9Þ/.\x0003!\x0010IMa\¢ë^\x001b1Ù\x0000ÊÌT~áÐ\x0018\x0000b#\x00127~ÙtÝmt3¡¡UÐÙ,+\x0007$Iª¡!Áª$}è\x0014$¢ä¡B'´p)i¦¾ñÄ£µ«±!ó«mAÆíusµóÌ÷2úè·0,\x000c¡Oòñç°(³\x0015\x00107ä$\x001b¿6Úu¡ó,J\x001fý(ÈJx\x001f\sÇ¹?BPý¼Ò8ÊØiIþ\x001cG\x0019ù*VÈ\x001bì
Jp*Ë«
È0ÊØ§,âDÎ9ÿÄ\x0003ÊæE	R\x001c)w9ýdÐ8ÊÞ3Îd~<u\x000eÜù,K%f eSËµd:ü9
2T*º"J\x001fxKDmm\x0001\x0001Â\x0013PRwàü9û9\x0005dÒ<¾\x0007Ô·³'ß\x0018\x0006	Ð{å{\x0014eÊÁ¬Äa÷xÕÇ\x0013­\x000c¬5«!\x000eÓ»÷0'(ÈPö\x001e£°¡3q¼q»ß»;\x0016ÐfLqq\¥'gtc	ï\Da u4¬1/\x001cÀï`ú	\x0014µH\x0017RP-\x0006¯ê2­Ö:\x0001zÓS¾aÖõb¶YÞ¢ï
q\x0018%öåÎò=ÔEÌd&\x001e))Ê+N¾±{¾âü=²fÔ5H¼ò\x0010eåÑ
1Ùk[T\x001d\x001efíäËùGi¿¼p\>ð°«áØÄ¥b\x0017aÍYdiU«[Ú\x0013\x0008L t;Ã>0otª\x0018\x0017WöÉ®³¸î\x0008Àèw\x0018Uz>o\x0012vÂ|ÞI\x0019ö.(Éç½ªÚ­eÅÜ~aé\x0007\x001e­r¼$õÓy-ÝÊû¶½ËV¾\x0005\x000f¹R°æ;é¥¿+ßI¯ïÛ¯e\x0019VÚÁ\x001c\x000e\x001e3Ì¨/'Ô\x001fx\x0017´[¹
Òöåøe\x001a\x0005FK9Ñjfjþ¯Å§Ý§PºÞ\x0017\x0006åA\=V«Ã\x000b
E\x000bEB.»\x0014WaÒîíÐ¸F\x0007²O<»Aô9\x000f ¬ºÀng\x001fÝ}K?eû\x0008²ÓFIux8rU_ú];\x001foh!ë@FÏÉØ¶\x0010(?\x001by@Y¹\x0017aºþ\x0005ñ÷(Lt:£È5\x001cF\\x0015×CË^°wv\x0007s¸ÝÇ$ë²!ÊqO\x0015&¦&Ì=UÌ^÷¡åü=\x000c1X©G¨­,xFÏÕþÊqIÆ¾¬\¾\x000fù²ôÀ\x001d\x0017'êt:nì¾/ÂL»@7\x0007ºìK<!¨\x001c¸\x0013jGbêUnr<YÍáöÈ2 nmkûírl¶ªRÚL\x0013 s0^	ÜG\x0000mÝ\x0017j[hF~½g]®/½\x001aNªóæÉØ\x001a\$OÄ©\x0019MªU\x0017\x0013\x0005ïÝ¯WÁO¡lù}ùìù:þõþêÞ\x000f\x001f>ç1Å\x000cÅT©óù!µÃw'\x0014÷vHí8Nÿæ\x000fWBI_¼net\x0001÷³TS8_ïp¾\x001e¿¤N«ÎÀ\x000bëõ6\x000eZu¹¨²¿¤\X\x0019¿£L_uW#
\x001fH¬YîCßý\x000cÓLßîdúvüì#\x001fx©E]µ/¬¶¿ØýÄËåÜ½&¶Ã¯éÓ\x001bOn\x001dÛ>ÂÌá»,Ubo\x0000]®\x0008IûL,®74Â_?AïMîð\x000bþÉ(TëÝQåVOJ"\x0016q5KÃ]\x0012;\x001d\x0013:*ÆIÁóëJ¯mZq½\x0003¯>N½|n%ÅÜP¦í\x0012¨}Á!®7bºÂ¦.ªóZ\x0010$ÞI#ä·¨¾^\x0012{Ë²z³SSoÆ{yÊfe©\x000e\x001d¹Ö¤wÂ-5ýi\x0007ó§ñÞ-'2öÒ_æt6*^íoùn\x0007óÝø
5m+a\x001b6ï±>\x0001`¯\x001ezL¼B¸¸\x0017WGâ¼2"¤=qÆ*Ý;¦sZß \x000f¦ãç!\x000bÁêZ\x0007¶YïñAºzø4g¡RÛªÛ¸k²Þ'5QË\x0015¸rUÿ¶»ª\x001b¾ªÞj	¹Ù')i+vHg4\x001aþõý\x000eæûa9¸K¢\x0014¦ÕÕ)\x0001ÖO\x001e®T>Lªü$}&\x0011g\x0004\x001dÿI°RãV¾«ïç\x001eÑÎ\x0005VW^¬hÛÞ®H\x0000\x0006Ë\x0001\x001f\x0008Gq&\x001c\x0005ã4xær\x001cH¾^¹iR¦ÔÏ\x0015ó¶µ8ëí/¿¼{ûË³oÁ°cj\x000cC	Ñí*Ç
&iýÉ¯ëpò÷/^¾üêÅËúg\x001c^SÅJ[¬4g8E ²lS%âl
!\x000e"\x001dm*\x001dÂz¥+rµS¼KU8\x0003*ÕM\x0019£\T·çÒ\x0004K¡\x0013l\x0003kÛR\x0000¾ød°msbþ¯9Z«;\x00046¥-ØæÀB¯XYJJÖ\x0006©Ý\³!Í\x0005è$Ësh\x001fÉz_ëa\x0019¬W¬öu\x0010«ë±º9¬\x0007Uÿ×qTêÈl\x000fç\x0002Ì)hûk\x0000÷ $+¾õ¼\x0014¦ª\x0003]@«;\x0001+^*à?§°r@UWbwÊ\x000eQ\x001bú»\x0018O@k;ÉòçQÐê¨%²Â ZúØ*X\x0007g¨.týâÏ9°é.UR|d´B\x0000é®ÚBgÑb\x0016'Ñ\x0002g(\x000bZ>)öVü,ÜïÇ\x0003\x001bú[\x001b&o-Y\r êN#\x0006+\x000bì99Z`?û,6hùsVÓÖ^kë¯®¬\x000f¤?ÂAØïD\x001b{´qN¶ÙúÆoQ®-*Q\x0019X:\x0003¬ëý®BX8\x0003ëÐõe1Ö´u\x0006ë@Ñâ)oÌõ\x001aÁMj\x0004n2°ÛÙS\x00103&ãÙy¼Íõ:bDV´Ô£¥IýÅÓõÚZÞø#L\x0017Ö«M~s¢¥Ø¼µ »Ö:\x0019Éç[KR\x00132çØ1Îñçh$´¬Õ\x0015´|m5¸1pÀà>ö2&[Ðr\x0016J¶e¬PHÈ#ÓJ\x0006·Öc§\x0012øsNYÖ\x0003\x0019ld)5T\x0008ò/wchm\x0017ñç\x000cZ¬P?Yî©\x0016\x00081í÷\x0019N¡
±³»ü9'[ÆNL¼%Ê	ZÑ_¼râ\x0004°\x001c-oÀàyF´T´ùuZ,
R×°!Ð\x0019\x0017!ïÑN>²\x001c)ÔG¼-hw\x0011Â¾?q\x0012mèe\x001bfí®Ù\x0012L>ÕMzùe\x0019«dþNmèe\x001bfeëå&`V²>´ÈVT\x000fé\x000cSÆ\x0014ýÛ,BU`ulAËÌ\x0002\x0004ë~\x000c|
+lX¸J¨[6MjÛ*Ù\\x001dþÏ`£\x0004»9¦Ä\x0013"2Øp\x001f	ÚYÑ&ÆÈpy¦\x0003D%èêw{½~\x000e®ÛÁu³¯LÛ¿t­\x001a\x0007érbéÖ»\x001e-/\x00042eQè¥C_§úÖN \x000b'¸`\x0019^ØÁÌ)å[·wµ®À7WÝ\x0004²gälWuhÃ\x0010ÐGg´²g´ÂøÑÆ\x0013,/é¯BÙ»3s\x0015Bø\x001c\x0003sÊU\\x0002Ç9gÜ\x0004èñò=ç(´EeY¿j|\x000e¤7\x0001ÎÈ*mG:+Z;§q½GiÑD&õV9³pí)WvÂ¥Iár^©¢eî\x0010±f ;Ê\<Å@`N¨\x0003S\x0017ê\x001e}~gVàZáñ³Ìp\x0006\ÜÁu>\x0017\ê\x0018Ï=4¥ÆüÿµyÕlê±\x000eü	^c¾[;éNæí8Ëh\x0005nvrDéÖ«tÏ\x0008{\x0001ã\x000eí¤ÛÈ¤­Î\x0002eKL ZLMÄ9\x0016Âb_ÛåïÙHÒÊÞ\x0018k?GFëU¶9:;Ã\x0013³»f§
IúÎ¼ÑNömÄFd#qN,IÞ3}ßÌ:c²Ï9GÿM3$Ýf\x0019èÂ)?­K¯d{l÷³¯
Ó\x0003¯
N|mÒ¿4!kRÿíT2\x0017ñN2Ï^Æ¹Ø+mýÌõs\x0012ÜW{¸¯æAÓúÌõ\x00135÷,ùQHñ\x000cñæ\x0017·íR6\x0005þÉdº¤øOæ¤QAûR\x001d¸²MV}s¯g½^©ó\x001c\x0000y1o^­q,+uO\x0001üj\x000fxîNÔí¡UI\x0008	"+	µÇLEvN­§W\x0012\íÓ\x0011Lø%h\x0019¨à´yhµ©SòÒÕ%Niö\x0016\x0007RFcÞv!é\x001ck´7\x0008=R\x0005\x000e¦1V§õðg¨­höBæ¬ô¬A8Q­3-&Â¶§§X»WWÖnîéYÝáÌy$O\x000fµ§9ÇEpFJÒîí³5Ï1\x001b
#ö.Ø:ñÍEl]å\x0002>\x0001Ûý^¹Mê
Ãýb%°vbsÚ5åfÎ\x0002üq\x000føãË¦zm¾jSd´ºBg$'ÞLâæLè¨Å6®h\x000bf§\¼ã$åöz¯Ü¦Lôçk\x001céýx~vS~<w<©ÛÆ²öj>¢\x0002§´<\x0005Ók¶2éú;°¹¶Ñó&×¢yÛ\x001a7A\x001cM[ciÎ
^_¹{\x001c\x001cwæ`Ê.Ý"eßÌ
g\ìcï<7\x0007sÚs¬Aj±¢ØUM\x001cÍ\x0019Á³Ý×NK7Û\x000b#~frêÈÛKWÑc}þÑ½Ù?º¹h¥[\x001f\x001d/yNÒ³eP;4nLO<ÖÕÏâýÛ^¼ëæ
>Ñ6~ø,]ÛµýNI°?íÁþ4\x0005ÖGáAæ>­;éåå~cq{ÒMFù\x0000lvûyXö°}÷þþõÛg?üý_ÿýáÍ_Ê2ô?ÜÿüÏwïß?±	IReÃw\x000eNGëº
Ú\x0007tß}ýüË\x0017Ï~øÓoÿíÛe+ú\x001fó¯¾þúx]{\x0003m· í
èÒ+_@sÃaÅì
ygNÃL[Ì´9I>cNÜ¸QA[Å¼Ë¦¬`\x000e[Ìa\x0001s6\x0014$]ÛË`6ôß\x0015\x000bV@§-è´\x0000ÚËuöØX>¢6õQ8OÌÐ¿ÁG\x0018WiUÔm¶N¼Ñ$i\x0005s÷\x0004aå
¨íÉûêÇóX\x001aÎCÝ=BXyÑêXHºl¶:îòm+ »W\x0008+Ï0Ù»v©½²E_VÑÞ\x001bZAÝ=CXxeÕK-\x000c\x0001z9Â®¿\x0018»g\x000bÏ'±¥\x0002Â
uº\x0011Ò¹v;Òi·\x0003»\x000b\x000fÑÕÈ¿¢vÊx\x000eÎ6õqÆî\x001dâÂ;ü¢îÇåZóOæo6\n¶TÊÊrS×Tßiþ\x0007+ða\x0019¼%\x0001o²i³ÆöYôö\x0015xZ\x0002ÏÄ#¨FÇòp¤@3ït©¼\x0002o×Àgéjíi·¸­)5¥èn\x00060÷Íá\x0015¶_\~ð\x0005ê¼÷Ûg_ßÿô÷·\x001fÌ\x00148Ù!í£yZMÛfOöÁIÿ\x0017Ï¾~þÇ?½øáX°\x0002o³R
}ì <r¤ì\x000f\x0012\x000bmè\x001eD¿\x0019\x001dõÂ£QáoûËyÝÄÕÞµ\x0012äÃÜm7ãó½ôü¨ôr¼d%ýÊ-R3oKz\x001cÆ\x0007	\nÆ\x0017S/¦1|>\x0019.mT|é°jM¿Á[;Þ-Í;ñ~G\x001a\x0017H\x0015\x0010ÏH=±qK8ûð\x0012ñAwýøs\x000c\x001f\x0018ÉòÙÈÓïÚÞ¥l"G,R·ãó=>?xýL®Rå\x000cò<HÇ\x001cú\x0007IYnÆ·¡Ze|\x001b¦ÕÛä\x0017£°dQÝý^®â£é³oÆ\x0017»çËç2\x000fÈ-Õz6Yõö¡øìf!\x000b1QL\x0018Ã\x0007Ù¥\x0010Z8\x001bÅÆÙè/¼pøðRõ[ñ¹
wrþãÝ:ù&|\x0014R5û\x000f®ò\x0017eñ\x0019Ý\x0015ìááÆ7ÃÛp&3¼
eòMð0$²°B^\x0011´Bøì¢ø¨ÇGø([\uÛ¹ÌT­ÑÑÿüï,¹\x0006®7¾nÔøòZ%\x000bÍ1OÚÐ¨c\x001eáqãö[EýÙÒïíl¹msÏ\x000fZ^\x0017.ÿ1<u\LGL'Ñ?L7|3¼Ø/\x000eÏù¶©Æ©+`2¼Fe\x001e&¼\x0015ï½R?êòòC¡\x00194ùtk/mLýÙÖ=~º]=o©\x00077èµp»¡ìË×ø\x000e¨ómuíÁÖÃ×[5?lÕ4Á\x0015­t@"5ºiÍgö©S+ü9fÔÐÊ\x000cËA¾L{D"¯û\x0018\x001fæ<¼\x0015^¾º[xü9\x0004Ï\x001aT®CÈæ­öÈÇ\x0010ÛúÒ7\x0016Ü
/ÚîáF;ª÷\PbKÞ¬ð¸ÛUxMÍÞ±sIc\x001ctI\x0019\x0014p\x001aFá³^\x0017Èñ\x001a¥ãMí´ùOõ´¿\x000b»zù¥aù}j|ýëMÃ¯y3³Ò{=_Òåâ¼ë~-$¸a§\x0017§þÕþÃ1)W\x0002xhÁµ2?
9±¼ûA¯^)\x0007\x001crÏ½<\x0011åÒJæáõk\x0003ú¹GÈ\x001az\x0010!$Ý.\x0003L¢äEE+\x0007M¸\x001a÷\x001092\x001fÈ¡GÔAE	ì;\x001bÍ«\x0011®e^ìî\x001eò½\x001e¼AÈ}3.ß:L±\x0015OýRl	\x001dK¶\x0000\x001caÈ\x000fØ©\x000cí\x0011,-ý²xÌù-Ü¿åc2´ª\x000e\x000b»D^]@kù«¸!\x0003\x001c¡7öÎzq¶¼èY	¶Âí~\x001at<\x0005ÓÑJ\x001afÃ:z\x001bLGé`v<\x0012â ±¦ó\x000f¯\x0018äë½$_\x000fBÚ§\x001f[ Ê\-¯u^
\x0019â=Ä7\x0010Õ7Ì/*\x000fvY×|\x0011µÃÎ\x0010ßî!¾\x001dN	^9Ò v?¸øðR½\x0002'÷·=¼¿
>\x0017ßú\x001c\x0000ZÊÈ©Ú¦µ×7ãûiï§ÁGâÇQÝ\x0007Ô4hìÄÝ\x0003\x0013ð²üû636\x0002ÝÜæ\x001fïÿçýÏ!s{\x0015¢¡ÈÛ«jÛ\x0002zd*î\x001báþøüÿ{þÍ\x0013Ðp\x000b
\x0007¡\x0005MCS\x0004Ô
Â
;ä×»\x0005ÝB³ÐxI@ãYma¯¦pÚQcæ-ÐÜ\x0016\x001bæL\x0010æÏü:©­R\x0008Òé­;jl¼\x0005\x0019mÑ¨Ð´¨M	Ë&6-ÿÍÍ·@ó[h~PhÔ\x0016·yvï«Ð,HbÈ\x0003ú£¹[ -´0ú
¬DF|Ô­Êh-Ô¢YZÚBK£ÐÇ¦@ý
¸A6ÿ\x0008\x0000º÷ÉCØÈ´h(Y^T\x000e\x0014QJ\x001c\£|\x0014Û¡I­ðÐv×?OµTï³å
w*8ÙtåyõÅ´äÐ\x001eÚè#ê$å0¾&Ò28#Õ+ïW»hc\x000f.\x000eC/Ì\x0018>ê*ôFLåÉø\x0005pu\x00053£K\,à¢iVÁ
\x0001¿§pØ®\x00038ê\x001eÄ«ã\x0007Á*·<\x00082Y\x0011ûÚ\x000feu¦(\x001e\x0012ÑÝö"B/TS6Û'á\Í°ð¢\x0005é½Î\x0006.\x0008/P\x000fnÐtat\¦¯×.êz²2\O\x0016`áÁþÁÁ\x0007)È\x0007i\x0005bÁ©Á'ïæ
í-¾5c5\£/ÊÁë«OÂZñ|Éã!yØM·£->\x001aô0jS7e;Úú2MÅ}®bHxä{pF\x0002¹ÏAÀ±R\x0006m)\x0016	÷K£ÇÀ\x001eÜ¨pF-)p¿¶ô;¨à`Áe²\x0014{p£f§ëêØií¶Nýs{4­x\x000b¸Ô\x001buljq
Ç­*¹¤àlx\\x0013?
Îw6?\x0007
¬P1Pä\x0008.¨	Ã}ûã\x0010¶Ôü9¨L\x0018\x0017ÛÔ©«ºÄÆ£é½TëU\x001bUu.è
K¬UPWm&Ñt~>îrØÙVþ\x001c\x0006Bù­ÑÍª\x000c´bcfê%ÑÙî`ùs\x00102éS¡/[J\x0012ÂS/âI|}DmGcêlöMX1\x0014n%×uú{G£÷.«\x0013Ù2O¼G£\x001e.Fu9ä\x0017¸Ix\x001e;áñç\x0018¾JäÏ@uÇî\x001eNf)\x000cóýÅó3\x0017¯Þ;\x0017­¬ÅÎçjåÞ%\x001e7\x0013OÀ\x000b}j?\x0007E\x0017D¾àã¾t\x0011ÊÎ>{\x0012íÑzì\x0014e/\x0012Q¢6\\x0016¥+»ñþq[ñ$>ßã\x001bMêpº¤ÂC£éC\x000b²¦R8¤`¿\x0011^ìá
ú(Î!Oò\x0016|9ZÔD¶ryÃÓ\x001e³J%@ç\x0006\x0004\x0018t\x0003²¬sýÄ©u¬p\x000b³Í¾\x000c:­Wxá÷¦ðbÿjãè«ýÔï"õ	4àqÍs\x0007éÛìZöðT¤ý\x0014¾ØÉ?ÇðAâôDÁñO\x0014?¤\x0013½
_êiÔ7FV\x0018fÇDÈÑy8K*ð\x001eÂ!\x0007ã-øÀîíïß\x000c»¢Nù\x001e\x000c1PNQ l#ÐLû1Uû\x0005vöò=\x0018q{i¯-O7\x0006þ\x0002Õ{O]Ú\x0001\x001c¼{%%P=ì´k>\x0005@zã9ï¸t÷®Òî£ywÎò+Ï=\x000cµA9%Ó3\x000fY-\x0001¤\x001dÀAëÁ}¢u_\x0006H:\x0016³7 \x0000Ã[\x0001ù\x001dÀÑÒ@ \x0015|\x0002È5|üf·áë3ðå{\x0010\x001f\x0008\x0013\x0014y®µKú¨\x0001<dk¼
 Û°û½°\x000b;£Z\x0006Ö	rhªûÙò\x0010yw¼\x0000âi\x001díä\x000eÝ \x0001òúS¾XGK\x0013Ét·6N\x0007»ÀÍ6\x001dº0\x0018M~êÃµ;ãkG/:ÝhN1o¢¡M:Ç´p¸íUt8\x000eØ~h5ÙéH?§
µf»ä\x0002;\x0019=ÀAç\x0000¢Òªf «\øÿ\x0014 ]\x0002õÝ¥£¬¸×c\x0018´F:,Rá%¯oë\x000f÷\x0001ß\x0016Xn5B\x001aChIÊËÙ	Z¨%¡ì\x0017®z	.Ö&ÄWC\x0010Í%]ÊÄaÒá\x0018eàÀ£ÅµÔ\x000bm\x0008ÁUoÇ\x0010Z+L£Äû~euWàM`Uáòðfoö\x0010ß\x000cºÒNú/6\x001a*5o´aøj\x000fqìókPV'\x0013´`øN©\x001b\x0010Þï\x0011Þå\x00134;ÎLÎVû&;ð\x001b^ËýÕk\x0019ÃøÍ\x001e'y·ýÀèí7oÉ§:­»¹·ÄòòâssOt=Uîõf\x000f+\£0­Õ];\x0000ë\x0000y©]ªó=\x000cqÃÃ«\x0010{"Þ[4¸\x0011XbV·ÖÓÚøèpÝå-]8~/FÎy\x000f1PÍ{\x0013M5Õ\x0019b+²º=%Úm\x0010\x001dÙÂìÒÂ(0Þ\x0006Qo}öòí??¼ûåí¯Â\x000b$ÏàlòÚQB^éÒ~¦Mñ½øþÙË\x0017ùö«/¾?¾\x0002óRYbÛÂÒÍ0ó©é®Òñ*,\eÈ½Â<Ú¯6\x0000\x0013.ËÄ4·ËÄoÆ\x0019Ä}åý¤z#³¡&æ\x000e{\x0004g´\x001dÎhÇq&¢*\x001df\x0017×U\x0018¢Ê3âAëß\x0008ÎÔË3MÈ3f\x001f-\x0008N>÷ê¤\x0005eIGT¿\x00030ñ2\x0015Ê0ùs\µR\x0002	g¢U.xôÈG`¦îÔùs\x001c&'e«09\x0000«o=x]Û\x0012Vp\x000fÁ¤\x001e&Í\N/ÇñÈ­ô\x001bèuõ`±×\x0000Ì\x001cBmaòçø[ç¹\x001eÑI¯o\x0019Æ3pb§:\x001dÎèÎ\x0006EÅgÉ¿M£ÞÎ°þ\x001cú\x001eç)re-Z9vNþ¨)ÒëY.À2ÎþÜqêÜ?\x0003Î^Ç»\x0019\x001d\x001fÚJ¬;MÝ\x0018Ã6Ó7åy°Mw\x0000']2A¶ ß<ºûI4s?6¸8DÔ·óËÿ \x0004çeÁkÁ¹Ýïz³ÍÌñ®0\x0017A2umBÆé;&\x0007BËÖBg4ùs\x001c§EõA\x0018§útAéù8î]ÅOg?'ÞQö×Bû M\x001e\x0016 \x0004»ì{úÐ½#þxGþNØ\x0001 °×TÕ¼ºaOD:\x0001\x0019570\x000bÁæ0LS<¤Bá­»ð´\x0016¿\x001cg/×q¦\x001eçÌ±{i{r\x0010P»;(¡2Í¸=\x0008#0SgÝùsB(3Îp\x0000'Ö])9\x001f\x000f\x001a\x0015\x0006pn=\x0018g×ìq3NKJÊ\x0004¶
¥\x0010)ß`\x0000Z\x000e4£I=ÎcHµ©'+%h=¦\x000eòÖ#0ûÀ(Î\x0004FÁ\x001aÙ¡Åc\x001d¶ Û8Ë\x000f\x0006U\x0006`&Óù ÉÌø «ÀMÇ³î×ã\x0006ø\x0011ÐéÎ\x00043ºó3(¥ÔgkÒTºÆEÉØD©\x000eêó+:\x0005Oë¾RòçÏqDâ+ñþ#6VR\x0002\x000eLË±Q]¨âD¨\x0019(Èd·M¦¡âJÃì\x000e*i·ãÍª\x000710åÌG]¬\x0010#TB@6Gº¦ÉÅ>×\x0011 }pT¾§Ì¦,í)è¦ì¨DÍ²÷	Æö%c§RuN\x001aÀ,§K\x001b\x0013%?Z¹;\x0002ÓS\x000fÓOÜPÞ=h/0xóHJ\x0014\x0013\x000eÊ#@Ã\x000eh\x0001N\x0010º÷V9Dò[[U¡`z©|Oä\x0014àYÌ\x0015û «u×3É`ÒN3Y°hÛÒÉ\x0018@Ãbïuyj¶­«ª\x001eÀô@ÁÌ\x0000e
øÓ%­\x0013ù¨i³®_~IÙ\x0003ïq©\ò§>wßÂäïq>ÜE'3¢<¦ë\x001c.§m\x0000w©yÊÍ\x000bÑ%o,ºoìë`{\x0007´|'½í¸¼NRüä\x0008\x001aÆYOËæÈî^zEYgÊ&0ÞÃh%ðHj7³Ã´|ìÖA\x000fÔÍ¤m¢×U­ÌR,iïM¼\x0000u\x0007c£C@w\x0012u3\x0012FøJlö;ï¤Àô,\x0015ç\x0011ÑÀ\x0008NêíQ7Z}ûÉ\x0007=²@}ËÓ&Ë*çE ®ÏÓï	:\x0019ð·Ä<·bá\x0006\x001f\x0010Ã²
u&ìÎ¨ÐäeøÀ\x0012¯9+
ºí
Ø9FÂ®Z\x000cS*´í° \x0002-oú \x0010×½PvG&>AQI¾lÇ;H\x0008V©eÍrØ	´Óö4«í%2N-\x001d&ãì²\x0016%H=PI3å{)ü<'i;Ï«æ*P³\x001c \x0003ùþäÉÏ<j16[$­i\x0019_Ð·Ëá\x0007Å@ã@y\x0005TRCÐZ4vb?9¨_\x0005ê±·ü=\x00014èbìÃW;¾¢bx©ú:N»Ã9ñbH¼Õ¤%ÂvCµÉ8ÛÏuÝäw\x000erH>\x0007PêÍ§	³½ÃªQPÈ\x000fòÉ\x000bPÞ½
4ì´hÓ¢-ÙÄË^¥%DÙYxWÁ*Î>i\x000ba&kËÚ^¬uQRC\x001bÐUqç8Å\x0019Ç©¬É­Ê\x001e\x0019ÈÓI\x001f·M'ø#±ïÀ(ß\x00137d*×r
\x0011\x00084
Ð\x0018\x000e~FÚDíD\x001dÊx®E\x000b_\x000eZW°1­Ûù\x0018út(O\x0000µºÆ
9°¯8	¢<.§m\x0011ú|}ù\x001eÅIC¹\x001a`â\x0005 5\x0011°XoËs\x0008»Þ0H\x0011\x0017\x000f«¶ÇÈ;\x0014«¶O^ì|vø\x000f\x0006\x0007b¯Ê÷\x0004P\x001dÅHmÂ=yÙGCÅõ£·f×»8QÍ@u\x0018\x000bcþeL\x0002T\x0017\x000f,\x0003Å^¢ÝLÖÈ\x001d­Ú	Ouåã­\x0014¢î\x000f\x0019!Gö½Êå{\x001c¨óRE^()Ç\x000f*P\x0017VNÈmG\x001dÐ4î\x0010oY£\x000f¼ä¸ª§l6½\x00005Ë®S6xýÑ»	}FÃc >#KÅBa\x0001.@ó%]>zÚ\x0001¥) \x0011¡\x0011°ÄÊ«OÒ$f1-\x0017æ¨×£D3z4%É ·<¢P\x0004ªe¥|íi\x001dgì
\x0013Oàw	E ÊïÇ{îP\x0005ºÀEßûNå{\x0018(²WßgòX\x0006ß®è²7ã^¢&$Ê.¨¨Qï.@£°e \x0007dÉ\x0003@\x0003ôÚ¿'\x001exZ¯\x001e½\x0013=ÈQR{KiÕ\x001bÅ@}[} ñxÐd	\x0001<&\x0017ZÐ®\x0001 ±ï"(ß\x0013wÔr~¹è{é\x0012\x0006«ú\x001eÇ>²\x0004úÇÄß\x0013@I²Nèy7²\x0013 Â5nmuöÍå{
h
í
Ð²®§\x0000ÕW\x001f\x000eH \x0006¦>\x0006-ßã@³ò´b<ÕåQ\x000e\x0000QõhX\x000eêKÍ¯\x0007:ñê·bËÑ;h¦>©@Ý	8ýnHe¢1#?zhW¤Ã'U£\x0007\x0014\x0010C@ý\x000eèÔ[Â;/@£j\x0008\x0014Þ½
t9¦Ç]Ë\x0018Îô\x0015tÁéÅÒr5G)ì\x001eÒDu\x0019\x001aLµJ\x0017ËÆÝï\x001eæä©×¾¡\x000cÓÝ^òBl¹Gg\x0019gê£Oþ\x001eÆi¤+#û±: \x000b\x0010Hâ\x0011SÎí@ífï\x0005\x0003-ß\x0013\x0002\x0005Ù\x0018¼[Û5ê{_ïxÈá;ö@'\x0005h¥NFÞÓa\x0002Õ÷`õrl\x000fÔM¼¤¬"UÓç£¯ç\x001e/Ç¾j7í®ÿÎÎôßñRÒ\x0016\x0004#9æÓ©Ù\öA­éã¤ò=ÓÊ¶\x001dd
	qí²<%#ïÒª9²Ð\x0017\x0017Ê÷8P\x0000ÎëÉ\x0002­×\x0013|Ðw\x0014Ç~,¸\x001dP7åÕ#kwUôF\x001e¼µÍn.·;Xèç¨Ê÷8Pß\x001e|ðÊw\x0007 # 9·«Îr~ý[Â©·ÄL$\x0012JÐÁºÞèÑ\x001f-Ã\x0019\x0000jû8©|K´qYg·Y{\x0000¬0p¼zôd®F'gê Ô\x0016÷qu>hÁÆhIÑ/ëzþ¹P-9ÿy=\x000c5\x0004Á\x001a\x0013¼®V¡¤CÝ~9/Æ}w\x0017"Ö÷j\x0018)oCH²·ÀhnÉvæ?r¬åº\x0017jiº\x001ej´:¸RÚÃ§Ö\x0013µ®ëõ¬ü\x0008.Ü<N'\x0003îÇo@VNµ\x0015WéÈN®À\x0001ÌXOÖ\x000e(we\x0003-ó\x0000µ\x0005Lãõ ¨Í9n¹u¡[z ÝòËÜ¬®à\x00129¥K¶Äy5\x0000g¼¬7W/ëÍ¸ºâáºz[/ÓéBÇl8 º\x001aÄúú
ëÄËÊZJ°\x0016?íº\x001díz3&ÜßÒ=q\x0007Jÿp%b+\x000bge)\x000e³p$pe½°Å5ÛúvÜ\x000bÈOªn¸F^Î,\x0019}\x0008Âei}bkõ;SÀÕûqSxú¦ï© [\x0013±ö\x0019Øõ\x0002YÈýûU\x0012úï\x0013Zd_3Æ6	ã>§ñ¸<r\x0007ÑîÅjg¤VuX\x001d×U+ÑkSa\·\x0005\x0005êÇ=Ô\x0013¯F¦À³jÕé«\x0010uº:âÁÆÁ»úæê®N(×,Ê(­&ÐJL1¦Í;ë5R¾«ÿquWÿcü®¢Ñz.\x000f
IÁÄûV0YNöqûî®rÓû7È¼SÕ\x0017°¦aÅ¨¾_\x001fÇagð?¯Áÿê3s2+ØX¨Í
¹õ	Ñ\x000cô§+ ?M\x000cÙRºÚ²IRrdÒ)B}{uØ\\x0015g\x0010\x001dÕ\x0002¤6I§¼ªû«W5ì·ÖL¿4Èd\x001f$3íZÛÉzÑ,¿Þ»*m\x0012ÃÞ\x0015eXÒ\x000b\x0001@Wj'ð­\x0012y@Ý8h\x0002î÷&`"\x001a
µl\x0016¼@VmÀ\x0011;ë`äÒ;­\x001c¹L\x0004ÙÜ\x0017)]ðÑ*ÿ ¶\x001bºuD\x0003þÊeõS\x000ek°A¶48P7üQÐ}ïÉùå~	~Xo®\x001eÖ°i%HV{;(\x0003I\ñ±i'Âz»i¾Rûà5G\x0018\x0013×5û~2{!+gt\x0019~Òq2s\x0002¥AØÇ¬[Ç]\x0016¶­(ÙüÊä?\x000e=òÌî\x0019îUo\x0007Ø½\x001a·\x0003l\en{\x0015çÅ½òö\x0004Æ«+50á³dD:W×£\x0015ûª	\x0001vZÎ ¨Ûk\x0002n¿]ÇW\x0018¶È¶>~£W6®s\x0003kðúê\x001aL¤\x0005j\x0018P¼läfõ\$ÐÎ×x9Ð.¯ë?®^×°]Hse\x00006Å²NU(¬4åvR }%Ö	­å­\x0004\x0004cÇT©®\x000f?³Tÿ~%Õá0»Ìo:Ù:\x0010\x0017Q5\x0016.÷ \x0017¤»Bú·	r\x001b`¶ÏrþYÑª3 \x001dèN
\x0008{-ì¸?ÈiÒ2\x001d\x001dÜ¡ø®\x00114"ÄåéÀê°\x0004Ö8VC\x0016/Õ!gZ+2Id¬çÈõí\ÇmÁs)r}u%×a«UÊR\x0019fò\x0013éü\x0008ZuÃeê "×ÿ¼ëp¨]Û¥	È-µûËjÚr#eI`ìb\x00023\x0011j\x0015M#®\x0016jåÝ!â\x000c,3\x0008\x0015±¾»\x0012ë»ßãu-!l\x001f\x0014p\x0008;\x0011\x0014\x0018\x001díÊ!lbPCX1\x00056û2ËeBv\x0008{ç\x001dÂqç5@ÔqsB¨Ý`ÆIG\x0010»g\x0008õþJ¨ã)\x000c\x0000¥nÀ`´9Ýd4/°¾ó\x0002;WpÂ\x000c\x0014\x000eýú®\x001cw`&Ü\x001a>¬»\x0002ì^õ®\x0000»Wã®\x0000×1\x0011£¯c¸Óê\x0018¥ðÖ»\xq\x0005Q\x0012nes¨2#X­»-÷Ò\x0017ue°&òmìUk\x0016\x001b¥¢
@Ð\x001cuZ\x000cï`'U\x001eu\x001cjJm\x0010ÕaT&Î®uSÒÃ»F0s\x0003B\x0000$ã5²x\x001a,\x000f\x0007{|\x0006Z:¨ÜÔ24ûªAæË ü¦¤ÕsUó\x0004©¾ºêxR)$a/r&\x0019îÎáàú$\x0015û\x0001] ø\x0001Ã\x0005ÏpË¶µOb±m\x001dObü¢P¹PY«R«2zT:Ååö»Í
x3.vâôJ5¯IÝV\x0008²6Úr®ø\x000c¬÷WXÇµ«eî`q\x0005²}­=xh´\x0007;Îp±÷9×	¯ÅÅ¨Cé6¿}£
FÛð`z½hwWZ`ØÃv'§^ÐE\x0001b\x0007$aÉì\x0012xu¥\x0004Æ/+7àj\x0015£pqs\x0003®Î¨&Xn¾`¿õ\ù­ÿcbäÛ3XæÀjÝÜÚpC{ã#«¾Lß_ÉôýDá=±æ/.1ÂðÁ5Bm\x0015K7¼ª§þã
è?&ú;©\x000f\x0006#J\x0015\x00123[çÝÓ>Àc8³G¼»¤<¿1qI\x0013è8\x0010e\x000f \x000fhµY§b\x0016ò
}uuCÇ\x0002opÔJ\x000c[¬¬\x000e\x0008ÜÐ(ú@__	t"\x0013\x0018¸)è\x0011yö¢\x000e*ºY¹!¬z\x0018¨Ï\x0011á\x001aæ\x0017\x001f|±m¸öþþÙ_îß¿{ûËý£J\x0014y7Ä(Ìu,\x000bÜ6ÝÂwò,ÿì/Ï¿þêÅËçc¼lp/\x0018i\x0006djý@ÁÇ¶e>¶Ö`sTbß¢<Ô\x0002ôBìÁ@;Z\x0006uö,ózºå6o@flÚ\x000e¨\x0001\x001auYb\x0006JÌZÖbc¸ÛFÚîzÚ©û\x0019ÔÖ-ó±º*o_¾\x001cýö\x001c\x0001Ji\x000bÒ\x000cP\x001b«ÏÚ\x0007êJ¥\x0013²ó3®h[)ÎàÄ\x0016;\x0005ÊÃE5Ý\x0013`ýÑê¼\x0001 °SLfêè3Òºýgäk\x0012½,ÁEEz4?=l¯¦^S\x000e@¤äç¹ÇJdª¼á\x0016ã	"½ìýª@ý\x000cP\x0000Mù(\x000b \x0018hËHY·~KÑöÔÎhR Pâ>¶ñbBÒZ·¥'qRsÆ4A\x0000IYCfSõSDl\ìëG®\x0017¨\x0012¨õÒS\x0005\x001akÎ×7\x0005G~ý\x0008Rß#õ³Hù\x001dª*
WÔâQÛÏ\x0010RèÎh(F
ÊËmj\x0004ÊHuQ5G)þ!¤ý5õS×\x0014´O½0.
¤²ö&?ï	¤Ö¸-Rþ\x001cGjRkNòäy¯IAju\x001f£>õ\x0011¤°óL¦Nß@{Q.Ô9@FJíôZGb\x0014g\x001a±Oµ;nxÙ\x000fiPGÚÎ9áÏ\x0019O?ÈFùì0¯\x0017Û´"à	GO½@iN Ú7a=:W\x0005ÚrO\x0018hPöÏ¦S6¡¦t=÷ø  U¦^LGiÒ\x0011¤¡SQ6Ì¨(Ãd^yL±îáÈH)]\x0006¿NxN±G\x001a§Úöð)º\x001f(#u:TÉ	§z¤i
)\x001a¥ëeÞ1S>'$\x0004)`ô=t÷?g¶yJn÷\x0006)êé\x001f\x000f§ Eì"N!mFßq\x0013½SêîâãÃwI©Ë÷jÆêãÅZÓË\x0016Ê%µ¥x"\x001d\x0004û=ØÌ\x0018þ(ÃÙ4ÓæIã-éÃ©¨ìtY³Pù\x0007_dûôòÃo\x001fß2Æ?¼½ÿí×\x000fïß¾{ÿDÉ!ÊXs&jóAl¬Ûeô^~ûã\x000f/\x0018â\x001f^<ÿñûo¿~ñÕ×Çò\x0014d¶(ó×(LÊ7]\x0008
²¢ììÉèzçäv½3(/ûË\x0018%ÿg\x000f£ä\x0006i\x0014^ë7É\x0007yòi÷â'PÂåÁ3Jþ\x001cÉKEYFØªÒ¤\x001dMó\x000cNÛÝLþ\x001cÆÉM\^Ä©Ñyk8Ãò©ã^qòç8Î\x001c1Ë²lçH÷\x0000ÒiâR@»\x000c3¥\x000efþ\x001cNIñ\x001ceG¿nMæ¢m\x0014ã*L\x000b\x001dLþ\x001cÉuúz;ó
ànBDf×\x0018?\x0001ÌN!Mh$¦g®NùÐ½0sC#â\x0012´3Nü9Ó¡:¡¼ìO:áÀY©Pr\x001fÑf·s1Cf\x0006g\x000c<YPpäH8gFz=_Qî±óç8ÎÖ©Ã\x000bheÙkþ\x0007¥HK¥¼¶Ó÷8ý\x0004N\x001buO\x0008OìÖY¬ÅûÌ¯=-ëøØ_Ï8s=	Ûx\x0011ù$Ë«((Nïmfr8ùs\x001cg]ì[pfÉ-òV_\x0011g\x001daÆ\x001eæÉ¤:¹í(aísà(C_PÜ17c\x0004sY§XÌ:\x000fô¶t¹2N\x000fºÆD`hUÅÃ¦H[Â\x000cPJ²·ª\x0000\x0015¬0\x0005ç²\x0004;¯³nÍ\x001d>uoïänZÝZ\x0005ÞH\x0001,«x·ªâ³ý\x000e'ãl4ìÎ\x0005Wß\x0010\x0005-Í§\x0008ËçÉ÷8ÓéN¦\x0011\x0005\x001d$\x001d*wO{Jm°I+WçØL\x001cºsV\x001dÍÑe¬(yç´ LëÒ´ÆïÎHÓvêÙ\x0012Õ¨\x0008\Ôý	×¯§5»pÃL(Oç}\x000bßÎä\x000bIca´«\x001e2X0=Pð=ùè+k4WáEÑ;í\x0016ûm´30ýîú\x001bÊ.ÄE:W\x0017Ùz=xïhùài§hF/1G¸\x0006Y/É¬@\x0000l¾¼_õåv\x00011ÍDÄ<vC\x0002¼\x0010G O>\x00113ípNxu>»\x001f2$àxÇs=ùà; y»ê.m7SV q\x0002hhûQ£#¶ô\x0017o5X\x0004\x001d\x000e(K4Ãq"QÊ#Û\²~ù-\x0005ëv@'\x001e=WT¢ÆêÒ\x0005ïµ<ö\x0014§Ò\x000eès\x0017xm.I\x0000ÚÅ\x001aÚ\x0004~Ú3òL\x0001
; aB¢9ôP +\x0002ÞLqâ	8Ó\x000eçÌ£ÿ\x000c8]¯íË>¹ñ÷:\x0017Ä@¥5$]ïö\x0005\x0019 ©×öü=á.Ç»X3ad0\x0014Èë¦ì¸ïkÀÉ\x001b¶8Ë"q¿	¹«qBÐ0p\x001aÃ»\x0000ë\x000e^ô´\x0003:ñä\x0019h-È\x0014 ¢í¬3È8i9K¾ñü=~ð9Øt3ÚtO\x001eµÜ\x0011pY¢¡NÙïdX\x000eè\x001b\x0006}\x000btKpÆå\x001c(Ð'èKcôx@2\x0006æ8½¬}Å5\x0019èr6\x000cMÜ	4Î\x00084\x0005!\x0007rÜk/ÛªÈ(±m\x000eVC\x0010\x0004ìÞ|ù\x001e\x0007JI¸­3¼¨ÃjcÁ\x0015Ï«@wG\x000fSGÏþ§\x0014»ÑVb:%ßMìê­â;Æ\x0019:Þ@[\x0006@3Lá×p\x0008+Ü-?yìË\x001eå{¢ÚÔ\x0003wuím\x0002\x001dRKËÖ3\x0003Û\x0015å¦Ò\x000e %ãÓ4QwÎÅ¸ZØF·ÃéæÒ#V8²²·up!¼×¸¬	; 3VÉ Ì|:¾\x000e\x0004
R*à²jr}!©|ã\x000cF\x0005Ê¤P\x0012µ\x0015\x0001Áå§ä\x0000z 0\x000eõ¤yp´bãÕe¢´.L°;\x0013j)zÏo§æBËê\x0005tW\x0015\x0013Ø,?w·\x001d÷k÷óÕDñÃ52Ð¬õ\x0005«GM=ÿÛw\x0019Lo\x001eÞ)WTâùlÖ\x0010]QÛ|ÑS°~¼Âúq\x000ekêÓ\x0015Ôå\x0012]úê
êø\x0015`¨\x0012Ô3V­v\x0006¡\x0001h9¶³Þ]\x0006Ó[vô~Â²ÌþX³¸-\x0001á¸áLò¸Ë}#E®o¯äúv"\x0014\x0005ÎßV#\x0015O	²Ó¢þVm.¡·+§ôÆåÊÌ4u¾ds«bÊ^=lXnÌ°°Ê.ãH9\x0016\x0003·º vºhQy?À2\x0017>õHK\x00005qY\x0013¶µ\x0000ù²V2ü\x000f¢ÕÀÄ¢¯^_]Ö×sùÐp\x0000nÂüe±\x000bðz\x0001Æ^§Ö£!N¾\x0000ÚKç\x0018û+¡N\\x0000Î¤;*ShuÙæ»úêê®\x001b\x0001DÒ\x0016\x001dcö7B#\x0005§pF?^þÜ7qþÎh©×Üçõ\x0002PrÝ»ê¼â]{\x0001Ä{\x0001ª²²9B
\x0004\x0013\x0004\x0006Øw3OõÍ^¬ãÎ\x0015¯{¦"ÇÃWVÄ*ã\x000cY¬áPeK±ÜÂ\x0015þÙ¸h½¬´+
\x0007²#riÃÁz¹½ÞÃb¯eüqYßÒ`¾\x001a¬}êÎûåN¨re__]ÙñçEmM\x0014÷Ai]RRÏu?Í8ye_í¯ìÎb\x0006ótÑ\x0004rc	NS\x0004Åf½ÚÛ¬	¤Ùf9¸8- FËæµ\x0014¡Þï:á_eõ\x001a.ê5\x0006U¯\x0017©.d\x0002¬gp\x001bÆü/¶i?¿ýùã\x001fC\x001dÿ¨\x001c¢N\x000cèÆêüÜAhõç\x0017ßüðí7O³[pv\x000cã\x0016gj\x0014W³Ð6æ÷\x0003áÝ¶ØhPpÉK±Ñðþ×Jõ^Ú~ªàâQ\x000bá­àâ\x0016\\x001c\x0014u­ÎÑ99ÕK]$\x001cõ\ß.mÑ¥Atd"5Û« \x000b\x0008ÀaKÝ\x001fUÜîÒâT^\x0019\x0015^IT\x0007ÚÅÊÝÊ-\x0003\x0007æ­èú÷:ø`³\x001f){±¹Ù_W\x000e\x0001AóÍAáVxØÁÃAxL/ )0\x0007ÒNm\x0010iè\x000e´[áu
\x0005F5
´\x000c\x001ddG\x0007UzºW&\x001cµ\Ü®S)0¨Sr`s'Gk\x001b³)÷Ñ
8»zó|Î\x000f¢ 4Ñ<â¬ëî\x0014^\x000cpàÌÜ
¯Sy0ªó"	·Ërº³Î+ºÃÜë­è:\x0007£:Ïzu¯²ï¯â ª\x001d\x000e{)nÎÃQ\x00154 ZGÊQÊ¨çÒ"b\x0018^§ôpTéE#d¥Î\x001fäpò\x0016E{Ô\x0018{+¼Néá¨ÒãEÐÒ'ceÔô´­\x001c\x0016ß-v:\x000fGuª!;-(ðöBèÖ,\x0006º\x000e\x001b\x0015^RoÀ\x00066r&vÔ\x0002¹=*äß
¯ÓÉ8ª½\x000e|;DÇÞ|5h¨Y=ÿÜ0¼N)ã R&K)ÀlÐ@ìmR¥âêË\x0008\x001d¼ð{{¸VÆQ­ì£,q¼cF\x000f×\x001aÐ\x0008#¬½\Ûie;¨)c´\x000cz¢±Ê5Ïþ(={+¼N+ÛQ­\x001cÞ=d<"<mpxT»\x0015]§í R&×^\x0006¡Îs\x001a«9-2ûuâÃðúÐvT+GÔ,FÖuÍ]ÑÀ;\x0012­=\x000cÛ)e;¨)ú;\x0019ä#§t°¶Ín¦#N[Áu*ÙªdÞ¹	Í\x00115 ØÚ=\x001dQÛ©d;¨}éòª\x0003¥^e§Á-ÁÂj\x0018\§í¨Bæ´\x0005«Bºï\x0007C70Gµ[áuN¼\x001dtâ=\x000fèð¸Ê'»h¼,ûËQîQ"úVx½°£ö"5x6{UI¬mh¥]Hkð\g/Ü ½ðpa.ðêò\x0002U\x0015ÞQgÜ­è:sá\x0006Í\x0005\x0019§ô\x000f</(+È±%¥=J1ß
¯³\x0017nÐ^Ä\x001c4\x001a¡1	Qí|5>x§iåÅ\x0000ÒuöÂ
Ú\x000bæN6R´T[\x0016ö´¦ÅÃí\x000c\x001b4\x0018sQ2ÓÕ³ì;ò¡Í§ãQÅëVxÉp& Ý=ÎPÅz÷ÃKáÙ5gÀu&Ã
È\x0004	r÷R{\x001a>:zö¨Nt+¼N+»A­\x001c´÷³,^ö\x0006­f¢_|¸RvJ ´bkö¤d÷®5Q\x001fîQgÐè¨ÓÉ4¨cñëÀ$^\x0016.·ÙãÅ´\x000fu*FUrhÅ*ý5âçqÔ#\"á v+¼N%Ó JNL\x001d#Ï\x0002¿Ð¨[^²Î[|\x0016Ô©d\x001aUÉ.ÜIÅ´5x3Ò]\x0004X\x0014^§iP#§à=ãq*»ÐF)®Ù\x000bê«g£
\x0017ÍIç5Òt}[£ÑÅ\x0012\x0010uúÆôqvÒònðÓå2¡Íc/Ö	¨sâiÐ÷Ùyå¬A&ó¯k1ÆbðH¹ 1sQÛ.g+;:bÒÀÛ\x001dµÀÞ®3\x00174h.|jÝùJ¨¶Tçù£®×\x001báùÎ^ø1{!Ñ$
u¹\x0019h{\x000b{*kZÅw\x0016Ã\x000fZ`"óåhJJ2ftÉªÐb¡Àw*Ù\x000fªä\x0010¨ÖrJöCbRî6ë×îï´\x001fÔz\x0011\x001b'\x00169q¤RcH2~Í
õ^ñz%:/k ]\x000eÑÚ"PP¾Ðc~[áu/×\x000f¾Ü\x00183\x0002ëÌ
ó«;°Ñ\x000bÝÓ\x0008O#!ÈJ\x001c¡E]¡\x0018móüGC³·ÂëF\x0018{\x001adÉhO\x0008ES	¶\x001dX\x0017ôiÄ#R¡Æ¥»KÌÆ«1\x0001fÍ\x001c/Þ¨ôÄD\x0017Õ·æÉ»Ô#ti\x0010!'äÕ/H^ÓS\x0016FBtÔ{x»\x000c_ïdøzè
¿[¨îÎàUsÊlf\x000eÍnöú¶M§âùu-§7eË5twVRó1Æ¦¥×®¢=ÊlçFQòr$\x0019gYJF\x0003®ÅÂ\x001fá(q\x0018dr­\x0007ck\x000c\x0012­Ã\x0015Z{2~³\x000cY\x000còýpîÀè*E\x001df).¦­Ì¥¹\r¦\x001fÇ9Gq þ Ne\x001f³ù\x0014\x0016SCnÎÙO\x001f¾\x0011[è\x001co,rt ñR\lûÊçãNó\x000cÉ1Àt)Vú¶ÏÛæz-Ú\x0017gú«èÌàUôùþ9Ah}Ûq¬<É9æ<" ¾9ËvuÒqø¤yÃ¹fRCl\x0019#{é\x0019^¬I;Ò£üÔ\x0019Ë¬Â?¾ýe§Âù'co»Õ÷¹Q@ÞvDFðo¿¯vWrÌ¡\x0008dó£Ký³xR0Ú\x000fØÒ¬;zÖ¸
®î#
ßÇO\x001f6ÃÕÛñ·Í¼ÂMFÍz¡o_æ\x000cäæ\x000eÏ+ão»l\x000b@Æ8m1F²Úò\x0014ÍZÒÚ¥ÞËuiÌËuÄ±f!H\x0013`@m_t Á\ÉÑË1\x001bjíáw#\x0005Ï¶øûÉî¢)\1a?öPÆ>~c`¿>ûÓýo\x001f-\x0010?ü±~yÿËû\x000fãä5\x0007¨¤ÌÕUF÷\x0019ñ2ÃÝqÿÈ ¿ö§ç?þð}ûí7\x0019÷Ï_~ýí\x0017¯ïßÜÿúñkÉ*lÜÂÆ\x0005Ø\x001cd×`ÌÚ|	\x0013Ü¢;yIl<\x0011·Ýâ¶K¸³Î¯»,:-ÖDPz(ÎÃí¶¸Ý
n¦\x001dO;	+qÉé\x0008ì½÷´\x0004¶°i	¶\x0013]a3n]Ýb¼¦e\x000cìí×\x0012n¿ÅíW^%ï¨×\x0004\x0003Ôå=\x0019·ò\x001cå[´\x001fx~\x000c÷¡ÂSÜa;¬ÈÛBb·\x0015¦\x0006î©Ò{\x0002ûÙ£%yÇ-î¸ÛµØÖ\x0006ÍÍfo»ÝÝ²´5Üi;-á6íY:Ôw¶`R«2W\}+¸/£UÅê\x0015àÖ	UJþUÐqÒÒ+À÷÷\x0012ðÞ\®ØKÖ~zÃÚîô¤;J¯éîw\x0006\x0013,f67²\x0006ÖRªÑ\x0006\x0003\x0017·Spg\x0002ï,&¬LÇ­(º0êT\x0019 U]xÕ\x0008ð\x0018ðGÝ*èì%¬\x0018LFMu¥%óÌ9¢lågî¬%¬K6;¢N®lÛOï­Ø\x001cèl%,\x0019Ë,j/>U\x000eÿHÆqsÌ¢>,\x000e\x0018ËÇeÝYJX1:¨G\x0000¼¸TûrÂ<êÎNÂ¡dÔQâ\x0005Ü<Fm(Ý
'¡î¬$¬É2§n×$\x0006heyÖkÄÎFâdY\x001bÑØ\x0019&íE
ûfòyÐ}Ä5ûX¶\x0014ÐºR\x000e7OÊí\x001b}WÌ\x000cö\x0001å}\x0004Ç\-\x0005xpÍ°G\x001dÊ0´ç\x001a\\x0002ÞÙG\
)Ð [æs@\x0011x»%´ozXÝ\x0019H\(9#{_³÷-\x0013Åù÷\x0015à\x0000ûjå¹ÁÎHâRLé\x00140­FÍM>ÑvQFLû\x0012ïì$®ØIKNÚwòMñìSÕàL¹^ó
?\x0013xg*q-ª4wINÀ\x0016
[Î:åÄ`\x0001;kKa¥Ïa¥HÜ\x0007¡Vâ¢`\x0003î\x0006<'w\x0006\x0013âJ \x0011SÐ¦oã.QÎ~ì
pÛÙL»\x0014Wr) 4m(¥)ãcS'Z\x001fÛM»d6n",W¼n¥3&\nJ8QÛÎlÚµD¬¿Ø{-ñ¨)Üz"î>\x000f»\x0014UæH\x0001Eà\x001e¥Ó 7|_\x0002ÞÙM»\x0016X"¯¥­O\x0013\x001a½\x000f:õeq¿.jÚ-´Ñ´K%saCË>4\x000f\×ñµ?\x000bug1íZd	BkY\x0013íe?ÎBÝK»\x0014Yb\x00142,T{,%G*ÏBÝÙJ»\x0014Yâ%#È»|\x0000\x0007ÃÅÐHêøqÔ¡´K%h[e\x0015®7\x0004Dàº?ÚuVÒ-EPöÏTÔ'ø­å\x001eüH9çqÔtk¥Ê$Íû¶T-å\x0008ä0z\x001crg\x001dÝu\x000cB²oyÿ\x001a\x0019e2a¤ºúTã:ëèbÊ¨;,óRYÐ2¥àûÎ%Ü}r)¨äýØ\x0012TÚ6qÿ
¹Ø`ö³;KÀ;ûèÊ`Ô\x001dá}p(!\x000eµ`\x0018\x0006üí'qw\x0016Ò-ÅdÏ	\x0007ñÂ Yâ1
âOÝH·\x0014Qr\x0005Dî7Ê'Í\x001aV¯	ì9.pwFÒ-\x0005dÕÜ8rÍkÕ½GpÕ$¿»3n)´F«!ÖKW\x0011\x00174Ùu×É\x001eê,%­Õ)4\x0008[n±\x0004Ãd
b)÷\x001c©+a\x0002uÆ\x0002J\x001b+Ei6<®õk¦zÂ~\x0000t	vg0iÉ`Q[\x001e¾\x0014B°2¹¥ðDBÅ¤%I:¿¬(àÔ\x00064Mx¢\x0006§ÎdÒÉÌ¾ æaÁÔv:Î{ÛfëÏì¤¢¾µgÉdr±R}xgD§êI#e¿'w6l&s\x0004\x001f[
ÜjTÎ,Pg5iÉj|?äól¯H¼\x0012º9³»:³IKf§ó¤@lëFK¾â®\x0015ãMÔMZ2@ê¦X\x0013ï\x0004w\x0010nÉüË3k¾³~Éj$
ÙÖ4dóE\x0015¢üßpâEñÕôKVÓ`káy )¦ù:1{\x0016¥%àÝô+v\x0013s ©
l(éLn¥ÖMpf\x0019ÐwvÓ¯ØMLAµ+>\x0003wºâ\x000bÞ'\x0002ïì¦_±È»q]ku4
¼iq\x0008'z¾³~ÅnbDá\x0006±ìÝ:\x0001~©¦¡=\x0013xß\x0013»b71x5?ÌS\rÈ\x000c\x001c\x001að3;Ø|g7ýÝäU¤){l­w¨Ní¹Õ4ßÙM¿b71G÷Zêæ\x0015&¡\x0002x©J)ñÎpú\x0015Ã\x001eîÀ]RàâÔB«\x0002Ù¤\x0019:Ã\x0019V\x000c'z£Ó\x0018<v°ýHü\x0014ìØ)ñ¸VL\x000b2le$\x0012;»Ï\x0004Þ)ñ¸TLãmÇUà\x0010RÚ¢4ÅÚ\x0018Îô°b§ÄãZ§f¦\x001f¾ê2K¦U\x0007Ü}w	v§ÂãÚ\CÔy\x000cäü´j\x001a£\x001e­ÛO-\x0001ïTx\ª©å"á=¯]V|Q|kÝ\x000fï­÷±\x001flX*«ñG}Q\x0007¥Ày½áñÌÆØ©ð¸TY£¤n
$ÐN\x000c<(p81JN\x000eOKÅ5
Â\x0013k!»ZÂ)\x0000Nj\x0010¬SNT©\x000b~ÒR}ÍÛ¦Ån06ùÇ\x0019½?Q\x0019¦.øI+ÁóI{PÀ'\x001d¤\x0006
ø~=è\x0012ðÎn¦%»ïUà¨Û\x0019@Sm\x001còz\x0012wg6ÓÙÌÎT« «q#Ý\x001cA\x001b¢ÛSY-\x0001ïÌfZ2±
Á\x000b:/ëÛÌAÄÀ;Ã\x000cg,\ç\x0005x\x000eÚ´§#jC{¦£:Ã\x000cgôBu\x001aNPfe\x001b¯¶Ì.\x0001ï\x000cgZ2.©ÄÙÅÒ·iSsUÜw¼\x001f	\3VV5Ù²âY\x001e§sÍUÙ3ä/\x0000Ï®Û\x00168® o-á)Õû,r\x001dê¾bYBÞ\x000f\x0005%ÓI £\x001a¼
CH­ Gö\x001c÷d#KÈû©@³d;	Û¤1O$	p
$p¤Üö$î~(Ð,Î|Ë+µE\x000cÍ\x00049Ð\x001434\x0014>¼\x001f\x000c4KÆ3;¶Ab7pm2Ð%9ã¼\x000e4KÖóUaÂ'ðê ¢èòt¢g\x000bý4=® oYf^ë(+ÎÚâÄ\x001cLà÷¼\x00124kö³9å,sÙL\x0000!¨ýL'\x000em@?QÏk.K\x0012;d\x001a[,D£¾VÚSd/!ï§\x0005Í\x0005Ú;\x0001\V\x0011kE<_\x0019Ç§ïê¦êyû¦³K£Þpb\x001cöCõk¡g\x0012êÞ\x001c3Ã*¤åÄR
ìfêê]\x0000YºCfhí¿^í~ôx¦Ä{û¹6U\x001f§×p]¥ê¨ç\x0019DØÍÕ¯
Öç"jì\x0019.PTän¿Ua	yo>×¦ë³Z©ÔZ9øLmN=¤|¤WüIä½ù\°IÛ÷²O[ë\x0012*¿Úä·¼7kSömiS\x000e?
3Ù\x0015ä	õâý{°\x001b´_´g&;I\x0003\x000e=B"µBW\x0014´KÈ{ó¹6m\x000fù55\x0000A$Zubdêñ\9ô\x0003÷°4qÏ¬öªÎMÐd\x0005 ÷|á)÷C÷°4uODâ±ì\x0002xÝÎ,°CÜ/N[Â½ã¤Y±¼EE
Ì|Éu=-)çH\x0013éç \x001fº¥©{Ê\x001a<Jy\x0002^;MÝÂ¹[èçîaið·È\x0000a¶g<\y(5þæÄöCè\x0007ïaiò¸\x0007AÜ[Ñ£ ¿¤ËÍ±P?y\x000fK£÷\x0014¬\x000eÆ¢\x001aûÓtff«\x001f½¥Ù{U¢ÜsôÁfÛï\Ræ½\x0001]\x001a¾wX¨U)*Õb\x0002R­8b@DÞ\x001bÐ¥é{
N\Üü{%õÍ1 ¼PïÌÈûé{X\x001a¿ç\x0017ê]EÎ\x0013ItöSxwâ`
ôó÷°4Ï\x0016ÔÌ\x001d5äZ\x0018ò4B\x001cð$ðÞ.
àÞ\x0007jw¼nK!(¯µ\x000e
¹¾O-i\x000c¼· k#ø=p2Ü"?ó÷\x0016tm\x000c÷Ò\x0003Èã'AÞ[ÐµQüÏ¼· kãø\x0017yoA×Fò3rÀÚ\x000bM
ùyÃXÐOåÃâXþçDÞOæÃâh¾»{\x0000¸ÿ$¸{û¹6ÿ9q÷æsiB¿ÇíÝ\x0015î\x0013=­~@\x001f&ô\x000bîx\x0001N
\x001c>	ò\x001d1êõü¬È{ë¹4¤ÏÈíEËöÈ\x001c\x001bòÂÐÈ{ë¹4¦ÿ÷ÖsiR;{A®ÉDí_=\x0019yo=fõ?3òÞz.Më\x0017ä\x0017¥(Õò\x000eùyô\x001fÐOëÃÒ¸>#§\x0007»O\x0002¼7Kãú\x0017xo?\x0006ö\x000bðKø\x00195ül3ªç"ï-èÒÄ~A®vÈ^Ã>(\x0006úq}X×gØÞïaûO\x0002{Ç,¾d;M!\x0003Ö¢\x0010è¤Mj\x001eùH	ñIä½í\\x001a×/\x0002×·i9¬ØËüLà½é\\x001a×§äµuÈ .2Ï¿vtÆFÐÇ(³ Õ¥a}·öÇuò\x000eBÞ½Ù\Ögà:#Ô\x0001\x0000x?­\x000fKãúÞµá&c¼\x0016É­We\x0018ÌH-ëÑÒÏêÃÒ°¾çÉÎ±õÿ\x0003
jå\x0018ða$Iþ8èÞ^.
êû\x0004¬üjn?rÓ\x0013£v Ñ?\x0008\x0013ú)}X\x001aÓ÷\x0011\x0010\x0018\x0013ÇoÕð¸¦K<4ó=y¹{{¹4§ïSàV\x001bF\x001e=èÆ\x0002\x0007B=eéÌ,s?¦\x000fKsúV©\x0002C*ò¨ÀÓñßíãX±·OË\x001d6\x000el.äðx"Û\x0017ôú°4©ïÉH\x001fÖ) Ý¶YÌ³J<oÌ\x0013úI}X\x001aÕÏ\x000fP	v³W¥ý\x0008'&DpÜ<¼7K³ú;³îÚl¨Zúa}XÖÿÌÈ{Ó\x0019VÃÍV4Ü"O\x0004yo?Ãj¼\x0019[ÔVÉ³vÈO|¡¡7¡a5ÞLþ\spá\x0000ï-hX8?\x001fðÞµ|-)EO\x000f\x001c>	òÞ¥~!\x000eÝ¤×²J7B<hóG½ÄÐ\x001b¡°Ô³}­æ%\x001a]TI[Ë²:/=ýè!.\x001eR[i)º6ÚH\x0012ä>,R|LàØÏ\x001dââÜa#oÌ¿qå+ãI%\x0002	8¢Ç\x001fÝ¯ZZ\x001b:Ä¤ð9'íîa\x00064'\x0005AØÏ\x001câÚÌ¡±\Ù¬°vN\x001aM\x0004\x0018H`?pK\x0003\x0014[a;à«Ô¤\x001aÝ£?ÏÖc?oKó¼zÆ7HYÐMÚ\x0000#·äIàý¢¥¥qC^ö##Ø,qiT5Ø®÷\x001d\x001fØO\x001bâÒ´!ï0i}¶\x00119éM9]\x001aûQC\\x001b5\x0004Ð²	mi½	\x001aã\x0013³âØO\x001aâÚ¤!7½WÜÖ\º\x000flÓ('òfa?ikÖ)ùnÛæjZãD\x0016ýy®\x0015Ân?áÉ´GRªÌíÕê\x00147²LöIÜ½Í\\x001c5\x000cwpé ÙN\x001aß§\x0013»±4ÄµICOº¶ÃpO0*\x001fE\x0013ù©W¥7k£Ák\x0017ÉPE­\x0000\x0005½ägVÛ°\x001f5ÄµQÃü&e
\x001a#÷JÐ£xpþLä½é\\x001b5dä2ÊDN7J\$\x0003P=ê\x001aös¸8gè©µÂÖ=h6\x000c­\x0013{Ü£
}µ·ø¯þß0ùð×û}ìs¿ÂÐÓ¨í\x000c\x0007\x0014º\x000bU±Ø\x0013\x001dÛüê{ð\]\x0001ÿ\x0019«ùùüõÕ»_û8ÿ\x000bþÉÒ§BeÆS\x001bV 58ã}¬ýO+W'd\x0002/NØ\x0002\x000b{bößëýþ½.\Ïù^Ó\x001eyZºò¼\x0003Pu$6>£³Øk·g*W{e³rg>§²É¾ùþÁ²»¾öb?«Çnpupíê\x0000/ø¨Ò'
¨a{íÏ|±¸¿:¸tu>'ø\x001c\x0012\éz¿zs¼ìøâ+ÊWª-S\x001c!ÜxØµ1ÿb.9FÞv¯ãó¾ý¹ÀÎ0ÿëÙÿû¿þ÷ówï\x001fW\x001cQWÝ\x001e3<4ÂD]z×géÿåÅ7\x0005oÆ÷Ý³{öü«¯E¬0Ý\x0016¦é4(9ò×T"JPÄU~\x001d§ßâô³8k^ÜFÜà´²Á=\x0001gÜâS8!jY0ðó¶§Kö_dq^\x0012(ó's@mU\x0006!\x0014\x0012ß©¶*Ð\x001dEÓ\x0014Îî\x0019ÁÜ;â\x0001\x0011¨
ug«+Ê*Î°[\x0011:\x0005´{H0÷Àk¨\x001b0rì(Yâ\x0006\x0014Öqv\x000f	æ^\x0012 2Ñ\x0004\x0008mÃw[Éýõ\x0004ÝK¹§d\x000b<3ËÒ\x0007íjÈ~ÄÎµ\x0002: iN¢Vcîà¡Å Ff²Z\x0006ÝÇÉ7\x000fêørû,\IAu
ëOéÂ&SpÂì\x0015á@¦ÙN^\x0017/J\x0014ÖO\x001e{\x001b?§S>*\x001fMU¢¼ÐK\x0005qý)]Èb
N»xðÁ\x0001Çûòæ*{{Â
í(Î)Qº\x0010ÚËJ:ÝóbÑ®+Ñ\x000b\x0013LÁIs8³+*V)ÿCõ\x001d	åNÖ vÝvb§êqNÕ\x001bÐÕ\x0005>\x0008éXÙ7'8!­û \x00173LKS®§±m\x0013TÒ\x0015VÖ ÏÎ"á¤EÒ®LnÀ¼K²øIy-yM^X\x0007ÚY$²H9ÚÒ½wGýeíP@5ë\x0012µE²S\x0016	³\x0019=Â>;M©-è\x0013Mñ\x000c I²S&%ªÎ\x0008w\x0003è®LTUoâºI²I²S&	CÒ´7º.àCQNèÍºª·M²S6	CÐ±7ÏKmD¢ºå#\x0003µëÉv6ÉNÙ$\x000ceÁ5\x0003¥\x0018Xí×\x0005{ºÒ\x0010?\x0001hgìQâõn¾ª{Êïª\x0001Õ­ÜHæ;ÚÙ%;eÐ'}õ	²OÔ
é«C{Æ\x001dí\x000c2L\x0005h£\x0016Ø\x0018ôèaÝÚÎ2Ù)ËÞkÿ\x001dyÓ6ûYõ\x0011ñ£ï,³L\x001b \x0001Ú\x0002övE-® ®Ó÷nNß3Å|I©råMzC÷
¤S8;uïæÔ½Em 'ð5öä=Â\x001a@¤uÙuêÞÍ©{NVÏlªi,Q£F4g\x0000í\x0013¢sê\x001eRõB\x0015h¤¤\x000bÔi=¦s¶wsÚÞz'Ë\x0002­\x001esl!\x0008¤¸ftªwSªë¥æÀ\x001bàP:#\x000f\x001e¬[Wõ®Ó nJB6íRHæ:co/\x001eÀ¬k&ê\fr!:%LçeN.qqÝ&Q§hJ5\x0001o\\x001dÖÑÜyP º
Ú/_Ñ\x0018:UÏ\x0013@
3¹×!hÞ&ï%\x0015
UZuð \x000eiù\x001eZJI±\x000e6ºìÙ21\x001cCÅl¢NðEa[¹2¡¤. ¼Ãð¤vtß^2\x00176]áÅi¼2Êc\x0012Ç¢Æ$Aý½3rãH{¸ÙÆÌÁåÄGÉåû\x0016>'§5\x0007¿yFªU±K\x000ffuËûw?3ÎÿðóÇ¾{ûîýû·ât´Ñ%kã!ARovVàË?½øóWß0Îÿö\x001fþòÕ¯¾þúÅH©CJP5~f¾Ø»$P£L²8¿£0C\x001aÒ\x0016)woN u:*ä\x000cù¶Q5©LwûìæFÜ\x0002å1µ	 Õð\x0017 Ùi\x0011\x001e~4zKý®í`\x0012iè)¤9:©ê5#Ú\x0019 ì»4®CÝ®ÚÉ Êª	¬¼BÒ
Ö\x001cò	9³´ì»+þI¨®ê¦ &+;Ì\x001b Ï\x001fy¶WÄºk2Äê{¬~\x0006+¯^HEUeO\x001fjþ\x0019Òei»jÌÃ:\x0005À3XÑë
\x0010tX\x0010½ªÕ\x0000'<,\x000ej	|g \x0016æ¹\x0002ÕQ»­^Ýë«¶µ9¬¶³\x0000ü9u\x0005Ä,Lr'·5Èd·\x000bdNêz¨S/ok\x001bàíðpåÛ\x001a\x0014+Õ÷Xç^\x0016ª\x0013PC\x0003¹\x0002)H'\x0013|\x0000Üì¶g¨\x001c\x0006Ï@µB¡Fm5Ã¤\x0015ý°k¢Úë\x0000Ô\x0001Ù¢TÑä\x0010¶Òm¤B2'@µ¦s\x0003Jzv\x0002ªSÂUÎG*áªm&+\x001a{\x0019°&ôX§<\x001c¾ÊÈC{!`AY¨M\x0017`^-ô¾5Lê+&­¯:À·¥;Íc
äNð\x0004­ëÅêæÄ
e]gÁ\x001a6"`Ô,`ð'è\x0000»aO-Pã\x0014TòRrCWi´¶NºXf±nÈ;\x0019+'AgÄZZ
«X­6ó¡nÌb=Á
X¢\x001eêjÍb­	ëìôÎ\x000fZ*V\x0007·(¬É$\x0001Ú_U»ª!©#Y¦Ò-ãl§@Ã\x0019Ï*ôw5ÌÝÕtÉal¤6JZÈÅ}Ñw\x000ekìµUÒVÞ(\x0019JiYcgH/@Ä\x0013"lz¦,Ï^u]°QJQ°Blõ\x000c¬Ît\x000f?§°\x001a¡is6[W\x0012¨í]pY\x001dv>+N
5ÔËjmfÍ
@MkJ'DX.t\x0017?g°f¥öy9?i?Z²'8Wù\x0016uHãTyQ½ M<¡]zu®\x0013`¬Èt\x000bþBª»j]F¨\x00196¦\x0019\x0014¨gø\x0000\x0004
àÏ©ã/¡jÊü\x0019rþÂVïR\x0013?a¶Ä9µÊMü*U_?\x0018*éUõöWõèf$I\x0014ë«\x0019¸\x0001¤[>K666Ì$4Y´ö[ßÒfüK\x001e×ýt\x000c­qó1×ßªtµo!í[k¦¥{¿î\x0014\tÒ	TZeÆ.û\x0006Â\x0001O^LH=Ü¦Ð:'\x0012ùâ.\x000b×\x000e@ïí\x0019n¶éjD\x001aÄòæbÃº\x00117ÜF·³ZÈ§Ä±.^AÎ¯c\x0012²w\x0016[0#:×>·f	²	%«¹i·\x000b¦.7kXå	¿_Þ½ý%ÿêåÜ¿ûùí¯aÎ¡bÔ\x0010¼Ì¬\x0014\x0006&\x0019M\x0017Ðõýgü^~õâeþÕËoÿüü«o^|ÿ$ö\x000b¹rÁîq	;U';G«Ø67Æý4Ð\x0012ö
g\x0014c/g9û\x001dë.\g½Åæ66ÿìÈ@Oa·Üùs\x001e»KÑ\x0008\x0013jiÛ´Õ
¾9ì{\x001eº5ìÆ\x0013ÆÞ%\x001a&°Ç\x0016lðZö
=ø\x001d£S®;bÑÝ\x001bö¿H^üã¿2Þß~yöü·~ûõãã:ÅÆ¶\x00057±\x001a\x0014n6G\x000f,¾øów\x0019ç/=ÿñ?~ÿÃcZPpâ\x0016'Îà\x000ctgà,\x001d²"\x0002\x001bNwÍX4ÓnqÚ)yîéI<\x0005¡T\x0016ÂoÊùó\x0013`º-L7%ÎÖeÌ ºN(¦&ÎxMý0¶8i
g[éLiB«âTw\x0012N¿Åégpò²ÔÚjj5§rÆé»'û\x0000Õ÷8Î°Å\x0019&Ï]úõSU¼|î¨8áû\x0019·8ã\x000cÎì6\x0018§oó­\x0001<\x001f U¸sVî¨\x001b\x000cU\x001axy¡j'ÝGÃÇ¿"V0á^8½¸\x0011º\x0004Óûûg_þò¯ÿÎ\x0016êýûý_j±­C\x0002­®\x0000M3ðÏ\x000füÈü³/_¾ÈÖ);/F|	\x0019q\x001f\x0013\x000f"n1¼á\x0019M%òÒ\x001c	ç1È\x001b\x001eà\x0002¹Ï\x000caf\x0016`ñbRIÕt~K\x0006<å\x0007!_F£ªa\x001e²E0xp[î±\x0016aD¼QÌ\x000f§ö\x0015°ï\x0001ûyÀÙE¯îKi£\x0018\x0019â
YÈA\x0019»þZ¸kÃú$a=$MdôZHp\x0014ÅbîÅì\x0016Ä-ò´Ü±®Á²v(d\x001fâ(\x00151ùÒªV0÷½jcÉ¶l'5!Ö©gìañw\x00143õç\x00153ñÆ\x0010Éªû µJ\x0015òaÓâ(Þþ^Ä{á­ÌÒf\x0013èÐÅR\x0008998J\x0000b\x000e=æ°¹5\x00050f\x0010\x001dGí^8sÎ½°\x0017þ\x000cÆÌÓò\x0010å{Ú]\x000eZ\x0017Jû\x0001yÌ©Ç¦1ûl@¬æ²QI,\x001døV!8éýYÛ½?þÄLà<\x0003­Q\x00127#ÿ
ÙUê(¥£
Üý³6ôç/3\x000fÝ\x0013![½\x0018ùÕi\x0006Þ\x001ffà\x0007ì:W?§1ç\x0000)
ä¶[È!¶\x001aÇI¶dÓQ Ó¼_ä32Úä.ú÷)ä~Rè0óç,æÄLÉÒ¬]f¨èôj\x0004çÎ±'º«Á³ïÏº$IyZ7<ðHOËò\x0002ÙC\x0007ÙÃï\x001frè!\x0005È\x0008¨7)G&eîÐ\x0001X­\x000f§x ù/Ým.ßÓ×çM%±^ñ&j#O\x0004Oòô#]êaêÏÝÏ;t$¬RL\x001dÖ\x001c$×\x001c¤Ã\x0012ÂÍ°ÝíÐíÙ\x000e3âïÞýü¯ÿóæ$\x0006ós	\x0001V+æ\x0002@#À:dñÈ?ûî«o^üÛ
(Ý\x0016¥A\x0019NN,\§K¥íIx4,5ÒoQú\x0019^Çzc¼­D\x000bðnïÌOÁ\x000c[a\x0006f e=¦û¶©ÑÝ\x001d¡\x000eÀ[qJ¨c½YÚÁaÚ\x0000¢éh\x0000q\x0000fÚÂLSÒÔ\x0006N^C É¬pø*\x001e\x0012_Ý\x000eó2vä®h#oÆ\x0019u;@&L¦\x0013`B\x0007\x0013¦`¶µ\x0003Á¶Q\x0003CVzðë\x0013:µ	Sz3ã\µO©1\x0007NÇg_ùhFz\x0000§ípÚ)¨µáôØ\x001b?d?\x001aÀÙ)xÒð¤IÈBp¨¯Ý5C\x0002Lê`Ò\x0014L£¾\x0000 Uj£©R&ÈXÙ\x0019"²DÄo*W$0m3üîqv\x0008¦LQ¶?*N&dWä|£\x000b'È³3E0e\!\x0017¨òtuxå\x0019ÖÒ\x001c\x000eï\x000fàìl\x0011L\x0019#ç¥8¿kß*§m¨Ü\x001e²oÞ\x000e\x0013;[S¶È\x0006)Ee#_\x0002VaØV\x0002±\x0010Ö'vÆ\x0008§Q\x000e?(%ni\x0012O}äØ\x000fùÃ\x0006pö>ü1Ê8\x0018×~Ji/ËÓ*}\x0018 ÏÎ\x0018á1²^}\x0010ÏSZR0GRû*È\x0014ÎÎ\x0018á1rFYl)
NåºÂ°sSô(8ãÔÁóä¨\x0017\x001f¹,Ä¬>²²^Ø}Ã×\x0017²-'Ò³^Ül=A¦\x0000Ô6/7#O'<{ãöhÝ$Ø\x001c(µ)acÞõ¾Esæ\x0004´¸G»ç?¹\x0011-/¤!qó¬î£\x0001\x001e R÷~ýe¸\x0007\x001bgEkÏ¢\x0015}å\x001bkl2' Å¿~|ûK/ZþÁhì`zkés:¨ë\x0005'%«Âqé¿ÍÏb;HòÛ³?ürÿá·__ÿýQ\x0016]ÔÎqäx¹0\x001eÆ\x0000®{Â\x001eÍ:ýøì\x000f/ûã÷ùûiÔÁ¤	\x0010[*yÏã$\x000cÓÇV¼>Ï-Ì\x0015 1v\x0018ã(\x001d§Îëð­Y1\x0016e«\x0016\x001e5t\x000e\x00126J2LØ\x000efß×\x0008Iz4\x0007M%ÛeÙh¢}ZOÂt=Ìic\x001b\x001c
A¸8c0Êw >\¯\x001aÂé{~\x000e'êÕLLÑRqÆv5\x000f
C8csâzreG²â6¦:6ÝI\x0011}ûî\x000cNo:ÞLÈÓÄ;©¹ç )UAyCRL\x000f¢FP^j
\x0005å¶Ôp³4SÙâW
¹¨-Ì\x0013½
\x0012û'3O\x0008ò9\x001biyAxw£'ñ©LÝ,ãô=Î'ôYpB\x0013fpº¤=,e7\x0015UFZ¡©¤Wqb§áùsB¾b¬,1,Oab$³_s?3ô÷3ÌÜOkU%9~EUT#¥\x0003â\x0011\x0019ö\x0002s;Ãþ{\x0012çÅqv,&7ãÌ^±Ðnqäzê'*)\x0015'iC^P@\x00193Ä!Gí`\x001eXÍ\x0010ÉN\x001aÊÁÇÃ\x0005å\x0011Yö¾qæ Gµð]x0\x0008LaX pËGîz
ïf4|ödý#ÒÅ\x000fH;\x0011\x0001ÔkNÑ&¡vÒÁu)¡\x001b¡?\x0018G\x001c\x0019{\x0013§5Nyºv;\x0014i\x0006¹ÒvêìzÏö)_*L¬ÃÉ\x000cS¡\x000có ]|\x0004gè\x000f=ÌKã±\x0017z>u!ÿ¡Òù²Ó»îÔ½9õÊþÅí\x000c\x0012\x0010>uÞL´\x000cº·Î\x00130Æm!XÉJ@ñ\x001eUàô=N?Ós%®â$5C¼Jq\x001e0\x0013]ÏKë^Ðûq¨QÛ\x001cW>lT¨bððc,vë¡²=\x001eµ°öÕ:oÁ\x0019\x0010
ÚÃÁØü ÒW{¤¯&ò\x000b¶yóñó\x000bØ¨I\x000efn\x001aJºfC¯Ýð.ûòÃ{ÎÓýñ··¿<9\x0012b¤§ÅEÊLcÑéM¥C¡~ùí×ªûã/^>Öq¥hí\x0016­DËû\x0011\x0005,Ý)APKþÈ¹\x001bÄJ[¬4/Y\x0010¬î.öÄ<âv\x0012Ö°Å\x001aæ±:\x0005á)Ø¤`\x000f_GÁB\x0007\x0016¦ÑZeæ¼²Î$ WÙÚÃí\x0018ÜÍ^²\x000c\x0017Ó<\a©|e\x001c\x0008I«=`&\x0019K\x001d\kHÊ7.¤¤}YeÏ[\x0006a\x000cnì4BT	·U´\x0014yiU\x001diój¾â)W\x0001°\x0003\x000b86ê\x0006\x0013fUV\x0002s\x001aûa8\x0018ó\x0018Æ\x001b{¼q\x0016¯ÑÚ\x0008·í\x0008á\x0001ê$)¡;L÷\x000cáõ¡»»>L^Þ,¿;+#)$rnÛÖ.84á±Çûp\x000eìÎ>°uììÃ÷o\x000b\x0001Æ³ïû¯ýwþÕo¿<×ä\x0018[\x0016±
H\x001e´ß\x0008â¡æýþE!Àxöýß½È¿øñå±\x0015vÜÂ+°ÚZV0(Y«äÛ¶ZØï¥_}eØÖÏãæMäÚß_XÊÁCöq\x0005·óp_\x0016Ê[+¸#	`6m\x001a%Ê\x000b\x0004Çjc\x001c÷å)2îþ%âN
C\]¯«Ï(¶aèð9ãNf;%y[åOáå\x0018µrØ®÷äSg\x00027¸îðç\x0002pÞßQ/xÙ%/\ÒanO»àp\x0018+À	V{+Y<Ë3\x000b²¾ÚÆI\x0013\x000eæy'ã%\x0016¡R¯±+À³þ«Ââ²\x0011\x0001Nç©B´ÝÓäÏyà16\x000e]UUât®É\x001c±\x0001Ì\x0000§\x001e8-\x0001\x000fI\x0012©Ö4AfàNm<Àa\x0012h\x001c¸ï
ú\x0015­\x0012y·X\x001f\x000e»£\x0000W105Óaà\x0016;\x001f?\x0017×\x001eÎj6AÒnÉ¡öÂÃq¶u\x001cøeÜ·\x0000·a	øÅÞGÔÝê®Ñ\x00162ËY¸{³iìf¬«¶¤KXÕvy\x0003¦	àÎtþ3+\x000eVäy³;ÛM\x0014Üm¸\x0003\x000f¸£g`cg}øs\x0001vvNtE«*o\x001b/;ZBÞqÜ¡Ó(ü¹r¿][ýB+ï²µÛúÃþ qÜ±w\·szMg^L\x000fèD¤Ã¨r\x00187\x000ewYd³ô.AÆCxõ,\x0006×½\x0013xÄ:2\x0003\x001c;/pÅK\x0014qR¬£|STàá`y\x0006wÁié'£LV©InxR*\x001d\x000b\x0007\x0013Á3Àc§\x0008).E¼KÑ·Á\x0017õ®^qùßaàÞt\x00117K\x0011\x0004(Ó¯õÞé®U2Jãjíaéj\x0002xê¯ù³Ë\x0017\x0005x æ¤D§ó¤î`çÞ\x000cðþmúµ·
E[=²ím\x0006uÄ-g5=ú\x001eø±OV§g|¶>²é³Æ
ü`\x001fã\x000cð>\x000bäÒ@1!gëÌ¤Ð\x0016àm¦÷`áÝ\x000cp×\x0003wkÀAý` ²Á0påúµ<Àr\x0016pê\x001cqOKx\x000cÒ\x0007QËry\x0017ìeö4OÅû^â~Í¡M¼Æ¹US]3ûö8Óa3î8ð>ðk!DÖ:¾,\x001cÛ´éútÞMé]C¿æ\x001a\x0006d\x00026w­Y\x000bcÅi®¸ï3~)eø\x0019/J6Æ½eÌ\x001ar£©·`¡nþc_Ø7\x000eVi
!G*\x001c§\x0017fHä\x000cÙ\x0005÷¿ÿöáçÏ¾ùðÏûÇ+\x000fÙ{Uê`f\x000c­\x0019|\x001e1\x00106\x0003¦ÿñÛo~xöÍ·yþ4DÛA´£\x0010Á$-d/°^ÐHÑìÃ³\x0010\x0003\x0000½ß\x0002Ü¨·ehy#±W\x0016s'2´*Cûpx\x0000bì9\x001f³÷Â®\x0013Cé<.\x0008M\x0010sAðp§Ç\x0000ÂÔr\x001a>eãuù\x000cÏfÜù \x00105ÓN<òµ\x0004\x0011\x0000·\x0010KÊg\x0010c[;ÄS.\\x0018-eº¨S®düÊt\x0000#ö\x0018q\x0002£¹ÈÑJ«\Æ¨«gÉÐj\x0000ãvílìVtÜÑ¡TKÆE¼\x0017\x001ft¢Õ¥÷â`L=Æ4Q\x0014#÷FOë?Ü{²±W0®\x0019y\x0015ºðèG\x001bën¹Q\x0007x·Ü"DêÅHãb´îÎ(D«À\x001c	ëÌjx¸3Ñ÷OÆ?\x0019 ödÀ´ê»Õ¸Ë\x001d¬>\x001cÁH=F\x001a£m0\x0019£o×Q\x0007[\x001c¯[Ä\x0018ú³\x000eãg¤ä$\x0011tif:M]VÉ-aDÓÙÁ-?ú­\x0018³3!ÿhÏºÍPÓÃÙ#\x0018Sq\Ü'Q)ÓI0ú6çí\x001eÌ.\x000e`Ü®¶Ë\x001877ËÑëY\x0007öÔEõ XBgqñY#Ä\x001eb\x001chµè\x0013bÔÚ½?\x001fè:ÇqKq~\x001bÄ¬a¨ñ\x000fä¨Áæi\x001b7Ý²\x0014]Ðnü ?¹âÉ\x0001B¿¥¬\x0004	%e7»áº\x001cÞÆ\x0008\x0019¤ºá\x001a)Àª©ÉâÛ®.¬ò|5|æN­
S¥ ¹®\x0005wðp·í\x0018Ìû=Ìû«)»Z\x0002\x0013h'\x001d¨s\x0001«>ZÖ;iæ\x00079(MæÞç\x0013µ|äQËÑîd\x000cãý\x001eã (>×iZBÖçêî\x0012<\x0010\x0018ùz\x000fóõ°(L\x0005eÝêK|xrÈ\x000bê\x000fý á\x0003áá+*÷²­Åsn5åçózÿ|iMc\x0018ÂÀÃ+Umjö*>\<\x0019\x0013æý^Ã7dmf¾®©¢dÔñ%\Di¼ßëvïgt;7\x0010ê#_yï²n· ¤Ñôp\x0003Ç\x0006éQ\x0007²/&hÓÝ\x0003¼Ãÿû\x000f\x001f?~xöû\x000f¿=
1ZÝïZRò²@ÃóÛ
åA\x0011äÅ³ï¿ýáoýáù·?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-12.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=;ýáð§åIÔ,\x0017{ÇË`jÁ\x0011û7ÿê>_¿ÃWº½Tðî÷UÚ7Ñ\x0019v00?	ÈÃ5	:="wÞ\x0011òHYE¾Ù7uþÏE}·\x0004û÷Û«kg\x000bØÇÃÎ\x0019\x0018At\x0002\x000c[²½}_\x0001°M=£U¼Çå\x0011§k\x001d~2¼j9\x0018e¸
1BÐ\x0002\x0017ÛÓ@.ÒMO\x00023¸îz0Lî\x0004ì®\x0019¢^î­0\x0016\x000f\x0013ø\x0015&Ø`q§e<M\x001eÙ\x0013"L\x0005Îi\x0007ÆÃ2	ü1ô«k\x0011;Îá1qIÇ\x0019¼O_ÝÉÖÇÔ\x001dg8K>ü<\x0005î¯ód~óè87ÓÀ\x000cOûá0mlr·ÓÄaâ\x00003xÖÓSg\x0013ÝÎ\x0010ª\ÝÃ{?
E\x000b'.)\x0010¢\x0006K\x0015\x000fÕ2:U\x0008\x0002£}ÅuI7ÁÕÕ~Ã\x0014óâ*x¹ëÎp8I¡\x001eå\x000c\x0008\x000b-ÀåÁA¶é®:Óz\x0007±}q´<?ßÎ\x0017XEU<I¬ácóÌé\x0017 ùß­n`öñ¡;Òð9½,\x0019B$4É4¸e¢
êóóÅ)\x000c=Véª
À¶\x0004l\x0002æùÖJàÜKÊ0²ÿB¶:.\x0005ÞÇûOJ¼ÿ¾m"¾\x001d
ÙÅ¦r<cî\x0010²³tÆ¢Õ\x0005ètÆ¦ìL¿hR8ß¾~×\x000b5ØWlð\x0019µ'ÀÛVÐ\x001b\x001eÀó³à-¶ ®èöI¿nrEá!\x0008`ûÀwVÅ5B\x0001¾µVébëH_\x0016\x000f]·ªâr\x001dá!¢\x0008ÿ\ë
E2ý&ÛOVwW«½çwWïW×}\x001føíi66ÂÄã\x0007¢Ä?­ç²8?Zì=??:Y\x001c·OHì¿`X»`åDûÝ×>È}b_ã\x00059?AXôÐÛO~3¸~þkÛ}gEïKúEÙSz·¾õõS¯\x000bãX\x001cÈ\x000bÃãÂ°xa\x000cÞwaÚýtêÙ;_^\x001cüúrYâ m©a\x0016á\x0017`\x0016s4·wru\x001d¬y\x001f7\x000e\x0016\x0007¦»¢]d\x0006èKÄ®¸kÅ£¹½£ã`ÑËð¹@,KÄr\x0014b\x000ed\x001f	°u@4\x0016\x0001K\x0001V×£#`]\x0002Öã\x0000\x0007NGì#á^Dì\x0019ª\x0013%\«Ü«­#æª(I
xAeÓ\x001bô\x0006MÌõ§7Øê ö£Wø½s\x0001«\x0012°\x001a\x000381S\x0011b­\x0010±sYk´Þáîu	Y\x000c³W\x001a!G/ùNVçCnUÑ\x001d [½\x0005Ùê\x0006äÕë»¿þóÃÛõÃ]\x001fäVÇÄèDEm\x001dÛ\x0013åZãÓübqx¾Ü;<[^·á7%~3\x0001~\x001aü#~\x0001þ`Äo¬$üºÕ\x000bì¿±¥;ý¢I]\x001eK\x0012=[ma(&ùn\x0004«Ø|AßªG6nU¬J´%h9\x0016´O `\x0005hº.uÊ¹í\x0006ÍU	«1¨\x001dd^ð{Kñ­rÜç£nU»PóWk÷¾H\x0011¾¸½\x0011<ðó$æ¾ùw\x0019äãõ5äÆE		[÷ü>P\x0006O\x00152\x001bóÖZ$
­üññåéòø\x0017gÇG\x0017\x0017UÇ®.\)ñtÑ¥ÄåSE\x0017î zºèR6õ©¢\x000bïË<]t)Åû¤Ð}\ÿ~ûGYtXX&q	t@§½i¬\x0014Ð\x0001ñ\x0013 SÎÄò\x0012ÐñMag\x001b]Ðt/ÎëÌ\x0007
tI£<UtX
y¢èFyZèÔoß>ðâÞÙ=X¥öæNð$¬eðTøGS/rN	|\x0016ÐuY\x0007ö`qQí+jàK7ïéâKwïéâK·ïéâK\x0016íáÓkýQR/ß~\x0016÷ëOqýJ$køåj}u}Ý\x00192ó±­\x0004 \x001b]åÊ)\\x0013\x001bâ]ûX÷\x0000¾è³Ðû²<}¹)\x001b~9Z\x001e\x001d\x001fw\x0002õ÷ß\
ÔóG)^}ú?\x001bu\x0012ü¿þ7­èâp¥=L²\x0005ÄNð´\x001fAseRg6Px¬!>	~HË\x0006ºtS*ºt\x0003*º¤k*º¤i\x0014ºß\x001e¬µªÑt\x0013âþû×\x001d±	Ø#\x000eKk\x00028íDBÒ\x0002lñ\x0019\x000b¯ªÏ8\x0018³Ã.ØP{>\x001dlï¾Ü}ú­8·Ã»Õû~ÕJ\x0011wJà`i¢TsÇ\x0012\x0017¶A\x0002Ywx¾8iÿ°\x0005ÀtxO\x0018`Ò)O
àÛ7LøëæÓ¸XÝ¬¾Þu4rFp«"´tVr¤²Ò!@\x000e·ÜÀÅéâ×*\x0017E\x0003a~ O\x0016!uË=1¿¿¹úMÞ4\x0013\x0000\x0017·\x000f\x001f\x001fâUìêÍ\x0000GQ,¦8-K K\x0008£ÖÕUÍbïâì\x0012¸»ÁÌ§
3§\x0004 Ìw7_n^ß7òÈ\x000foV7\x0015Ö\x0006V\x001câñQÓDÅ\x0013\x0014\x000eÞI¦ëçÅÙå³Eu´±²ÈO\x0011\x001bå"6Ê ?El?~2ØÌúÞ\-=Û7\x000f¯ßýõ¿]á	¡)S\x0016ì°Þç"9ZZ
²Ã¾ª¢\x000fÏN]\x001eþÔb\x000bèÉ<]èÉ<]éi<aé}<a©ÄòÔ\x0000òÏkÝ\x0018 òÃÛ÷ï\x001fnV\x000f_º\x001aß¸PUÅ¨ÃRù1Æ	Lëö´^P9;9¹<]\þW\x0017¸ôòß\x0002î&Ûü·»I>ÿ-ànrÑ\x000b¸I\x0017ümà¦úëß\x0006®û¡$W{òpý\x000fÐEýwKLO\x001bïíÃÝ7ÿ®¹ßûqõênýöaýéSçT´FQ.ÃèA«ðkªV\x0019-jpaîæÇÅÁùòùåòåË\x0016#\ ¥|Ì\x0013Fû¿^Ý|Ùv\x0019òìÎÁº´iôÆ©\x0010$?å¹u2auWýæBì.H\x000boá#-\x001c'´ð\x00118ÒÂ=xH\x001fþtòóýwN8\x000e\x0003õh=^\x0002/\x0018`.\x0014«³\x0002k\Úª\q\x000e¨­\x0005¥@[úàO\x001fmé?}´¥\x0007þôÑ\x000eøÓG[úßO\x0014í»·\x001f?®J°þøpuÿ©sÿ£ðÌÆ=½Òià¼\x0000\x0006}-óIq\x0019ãEµSâ|ùóåÑÅË\x0006È\x0002\x001fj'\x000fßýÅ/ýiásß~W«OµFªuðû¯oß¿ºêüh\x0004ç`;cÛÒ0I\x0016ý~E]ÕÓX¾\x001d\x00029>;98ª¿\x0002û#íS\x001bì4Mým°cëìß\x0012;\x0012ü-±'Ëö÷ÄL.Kì)çô÷Ä\x0012P'ì¯õ«¯¿?V´¸¾}è,Fd±ÏS"
v
Ü8q)¨ª¨ã³Ëz¢¤¹U¬xª0·\x0014O\x0015æVqâIÁüãÏwoÞ½jö\x0005ý²úzß£Åpå¨CMZÁ©CM3:Yà/ë¼ÅÞ/_/.Z;Y
¹/èiÃÌ}AO\x001bf\x0019zÚ0ÑÇy0oüÇ;·5[w~ûj}÷i}×Õ Áp¿?xé\x001blV\x0012÷Ü\x0007{¤]õ©Çðü`yþryÞb
ù
=EBò¯¯ËPîd}uýnÕµ\x001f\x001a\x0006ÈÁC éTÚ\x000e®¹äZ[ft\x0015àÉòèø§E½\x001dºã\x000bO\x0011\x001aÎ.<\x0019hÞ~¹iäõý®7N¸Ï7V
ô±£D:\x0003\x001dþÚÕoÜáâäE\x0017dô$\x001e2²$O\x000f\x0019\x0019'ìÓ··æ·»²Åou÷êöæª{÷\x0012¥j¬É"KK5÷\x0014\x0016X¡u\x0015Ýáâüàìô¨¥\x0014Y\x0000Ä\x000eº'\x0006ð7ñõó\x001bþo&\x0019,N?Óÿç]ýU\x0019©Ûã×u\x0012ø¢Á_µ>ÑÏ¯V\x0004>þuãÏÇù­ø¿_1A}_é\x0017\x0007á\x0017T*\x0007úù«ðç8ÙÙ¹üÌ\x0004@Ê£q§°J¥µ§\x001a(ºZÏÀ7\x001fÎ2
xnï;+ð\x0012¯xúxeW>}¼ªÄ«>^]âÕO\x001f¯)ñ§×xíÓÇëJ¼î	ã5zKÿ\x001a6°\ÝßÞì\x001dßÞ¼}è\x001cEÀ¬g2cÊ+\x0001¼'\x0000Õ;ìü1ÂÔ²ÅÑÅÙéÞñÙéó¹t\x001b§(q§S8å\x0013Ä©Ut\x00086ß\x001d8ô¢\x0015\x0001ÑÓÛ»7]á°"1ÜÁ\x001d\x0016k©	-\x000fAf
mü%.78=;ö¸ÃÀý¿ßþ&ß¾/\x0007>àa_}ï'®/î¿ãúúÎ®?\x0001Ho$l^Nv+E\x0008z%<'\x001fÜÓ´ðB8÷Q
ã½³ãñA\x001fýRsµð6Mt½àéHÖ\x0012áY\x0001;\x0000\x0002\x0016Ô\x0004OmÆ~GÁC/¿7<ØZ\x0001\x001e\x0007½\x0014ááV(ç\x001e£Òë\x000f\x000fKH}á9\x0015÷ö\x0000<\x0017Ù\x0004/.ªð\x001eeì\x000e\x000b-=Ñ)î
\x000eÏ¥ÃÓ¸×-~Û)Ð,ÿ½àÁÒ\x001dà¥m6\x0011\x001e7ô2Ô£4 }ñÅåuñGÿ¯Ëöñî9\x000c!|Ü´Ã0à3\x000fÇ'Í×· -É5\x001fü8¿}ø\x0014s{³|Ò\x001d`j\x0001ä 	g\x0008öauû¾WÌót	æý1ºÌóüìòeêÍ¹<}¶¨Hp\x0002E\x0003?Âv%c\x0005\x001d«bVG·\x0010\x000cD+\x0015D jøáÛ­4°¸>næ[p©ªïþp\x0015è¡øc(\¦Ó¢\x0014XáæÒæ^\x000fö1½©`\x0013ëúr\x0000Üèøc \\x0016^Xä·À¥Z·\x0003\öT\x0007¸¦n}\x0006À\x0005øc(Ü`!Ñ\x001aÁZme\x0012\¦ñ2pýèæ¡p7þ\x0018
\x0017&
þ×AGøÒ¤u.ÃãÌþCáZ8];âtaæO \8²\x0002\¸±	.ìÑ\x000c®\x0001ÙãapU\x0000\x000cï\x000bà\x0006©÷ÓÕ5Z"Z\x0016Ü½	Ñ©?¢´nPZ¸\x000b,è\x0008¡\x0010.÷\x0013Þ\x0005ã\x0000®\x001b\x0001WÁLD+Ø>O\x000fÍ(,¯\x000f\x001ab:°Vü!þ\x0018\x0008Ö\x0005\x0017ß'\x0017\x001f\x0006PPé*JW[­Ç_Ü«?<ûx·\x0015,ÞG¦ø/Ý
ådäF²\x0011r²¼!\x000eóéÊZ±ÃáZ$røÊ\x0000R\x0013ã&\x001aé1ÙÐÓ\x001eL²ú\x0000ðQ\x001aûA\x00007ûÈ\x0006\x001cb\x001cM¶Ê\x0006·\x0016\x00182Â\x0008\x001b6'Â¸úb\x000cº)y-\x0005!H¶\x0015ÂA>º<i\x0010ÈMäÔ\x0017d°¦¢8H\x0004)Ñ<Mxá<ÀgÕÃ`\x0006Ñ«+}"Lc\x0005¥\x0018\x0007suû^Ý4©>¯ï:\x0006)"®ê>AUÆI\x001dÏ¤wx\x001fóU;t¼üey^\x000fQ
`ôû\x0000\x000bFQ\x0004Ì
ÔLqw\x0010ÜÿñÀèô\x0004&\x0011ç\x0018´\x00030À´ªÆKÝÑ³è\x0003\x000c\x0016ÒÆl\x0002´Bì'õ¬¤$\^µ<ÚV\ß^«ÕmyÅÞ¤pl%ûçêîÍÕMG
\x0012F.Ý7Xì\x0012Máá¿\x001bAÂñÕ@\x001e¼¬pì'ûçâüÙQh¥8Ý½\x0011M&ÄÞÀîô\x0008Y`\x001aÄ*_W\x0003!'ã2æ9ú:øRMÙ\x000bH¼\x0003b3õ\x0019§g4\x0002°r\x0019°Ç-\x0000ÖtÆnòk¹F@\x001e2]dÞpVfÈ¢ª\x0006\x0006BN:a\x001cädB ÏPs\x0005È
µµ\x0002òê­zÐ±\x000b\x0008\x0000þ Ïø~oyÿaý:­rì\x00009Äò\x001cfÅ¢N\x000b\x0017#6zyøwÐ
@ÿ×.ßøboyñbyXÝâ["æ .âáC|Âæà·;/\x0013øú\x0016r\x000c\x0014ã\x0011\x001dæ¡µM«=#d©J\x0007ûÚ&,\x0001²\x001c\x0007ÙV\x000e&#-0\x0007Èéõ9\x001e;ô§Cì`ÇXü1\x0018qðô\x0012¯X@\x000c=G	1¬ûÁC¶lgn­\x000fd\x000fÿ¹øc8d¦\x0013ot,É\x0007\x0013!\x000cÀSfFì\x000c¤{A©ðøc0d\x0013Üm§,4Üê\x0008Ùjõ£ËûB~uÿÇ«7%eúf.61t®\x001f>wÍ\)\x0015L^\x0010\x0018l\x0017§¬\x0004Æ\x0006cýø\x0002à\x00049Æ&bîÓåå/õ$@z{
}\x0000jkÃm´qª\x001b\x0008Å+£½¯ë¹¡°·ÇÑûÃáu
kUª\x001f`\x0011°ÚÔã±Á°·çÒ\x00076ãûÆ¤Óæq3[ÚÃ\x0018V÷î\x0007ÃÞ\x001eP\x001fpÚ!¼LEÐ<ÍÛzÅ­ K¢[RqCaoOª\x000f¹$¸\x0010\x0011NaÝ86µþ¬K\x0002¦\x00117[¢\x001eZpëf?º|m\x0014ê&±Ñ@Ø\ Æ°}:kÎÜ\¨
tLÄ\x001fãNÛ¥ê®\x0002÷?eÂaS-G»\x0016i(n	¸Gê?\x0015<á3pk\x0011¸Ý\x0000¯{N½ÿù§v¿]=5(×\x001eï½ù¿ÿþÅÃ«ë¯\x001dE0áIbOóáòD\x001b¯ )DPÌVÊ&)\x001fï=Û[\\x001e\\x001eWvò6ÙN(\x0015&\x0015*<St3X\x0005
²j&d;Ï0N\x0012mÃÍJõBo\x000cYV%9}ð¹f\x0014f;\x00071V\x0018
<e\x00086°ï*\x0008#Q-Ô!#1XíP¤0Tlø2<_3Y7£LÝU\x001b*ÌýíöëozÈ\x001bAÖ{«W«8 Ô)ê\x000bp9f«µËé\x0000C¹¸àòwp'6B,÷\x000e\x0017\x0007ÓÚØPSmy\x0018!ÞNuªB\x0016âíB®·\x0006\x0016cÛ\x001e!æ\x0014«\x0010k¥Î¡ð5¼C1Ü£j§\x0011cÛ¥äk\x0004ó~\x0013|
Ê1z&o´\x0018Û.ö¯á .O_#©_!lÚÀ\x0012¿F\x0007Ã>Pm{\x0018~_	Ìøy
àÅÌNb¾Qr¶½Szó1ð]8*ùO2*QÇ	_"À|¡<](_w³ÆÁÁfLe4BàéQMi]bA\x000eì]±×\x000b8ÃäXÑè[\x0003Z\x0007\x0015\x0005H\x000f{ÇA{e1'\x0014Î\x001bsB"8Û¶]µ^\x0006Ì\x001d\x0000rh-?z#tcV\x0005ÃEÉAÉ©Ê\x0014þª=rë
\x0011ââþ\x0010-NÝÇ"\x001dú=A³£{
ý6¢å¤ñGQ\x0017¦Tù\x0012ÊHRv­Ý\x0011¢\x0003´N\x0011®¢C]\x00161Ñ]¤÷Ãd»·Ò\x0011¢\x0007ïò«ï\x0005»}ªÊ):E\x0019¼+\x0018øi j¨@\x00146k!ÏÉuFÓ)ª.¯>\x0010!}\x0019\x000cøÐ<­\x0002
þ'sØö#$ÅÕÖ\x00196É)Âûû!þè\x000fQÇ¶.\x0018ã}¼\x0003Å4ö\x000fxÇ¦P:A\x0012$ýì1D[èÁ\x0018gÓttÀ¨\x000cUM\x0004¯·vöÁ(#F9\x000c£¡^\x0011¨¤¼¬P\x001aÛèÃni£ï»hÈÝG­Éý,\x000bL\x000c
-±ê¸¬\x000f ôÁ(À/N?ûcôd\x0014Éik±ÜÄ}½å°\x000fF\x0015\x001d"5D9ª`Þ1\x001dâdCÇ(<F\x0018Ü\x0002b0\x0013\x0001büÙ\x001b¢`± 
\x0010µ\x0010XÝ\x0010aï¶³VùÔoû²z×hÛâm»¾½\x0007À\x0017«\x0000¨cú×\x001atðÃÃ¶©}[qGYTèû«6[m1·\x001d]\x0000\x0017ð¿uàqvÎ\x0001\x0012°W¥\x000c6h{"@\x0003V\x0012ÁÔÕÔH\x0011\x001e'é\x001c"Øô\x0011\x0004¶f)N	ð\x0015ZúTÇð8Wç\x0000\x0011´¥JSÐlù+\x0018ï\x000c¢Ô«"<NÙ9ä+´"|\x0005ÍÒ\x0006A¸H.R½\x0015c¤\x0004\x0013w\x000e@	ô*`</K3ëð\x0014Ä\\x001fáqþÎ\x0001"8AÕx\x0005m^©\x001aÏ½Æä{Öæú
Óx\x000eù
\x000e\x001b§\x00144MÓkÖT+öz6\x0011\x001egó\x001cò%\x0015×àØÇ\x0018DÀÆy\x0013I\x0013g\x0011!OÑN"\x0003}p©Òð\x000cÈ7ÉK;Óg ¤Ï\x0014WImSÒ&bUxÐVÑk¨÷Ü\x0013\x0001Ú\x0007§1ÏÂciø\x000c\x001eêQ\x0004AWÉ+U\x001f]\x001f'\x0003¤¦1n\b¡6èU-oPÚ·ô¢Õ\ßACZk\x0012\x0019$OñàcldÈUMÏÝ\2?=q\x0010!4a(}DqfÚRýÏ+3©tóþ«¼-üí\x0017\x000f_SÞöý¿þ÷õ»n°ÃsE6ÈG°Tçw!,0TÑõÉô\x0017¿¦LíÉåáO]â\x0002à¿\x0001R\¹ûd®øíÕÇ2ÚºZ?ì=»ú´w|ûð­s+gÐz!*ÁÉ$*2R*Fÿ¯ri{ÏÂ=»üW[\x001fg\x0015ãªaX!½Ù=É5Ì\x0007E°T*1®^*éõ÷WúõU¹È\x000fÖwo»²RHçÌ¦\x001aÂ¡a,¥ísªµÌÌ#óÁòüy\x000b7E\x0001´ÉáÝ\x0013¨ÅFM­¤ÚÇdäfÌÊ×»Iúãlx÷ÃH3Ò*p"Pa\x001cv4°õÁÙdñîSÒôÚ¤N%$#ñÃ³\x001dM\x0007}6ö\x0002ê@k¥Áâ¦Æb!¥È\x0007º£öÕ\x000bhs­hO ~ß\x0019¼¡\x001c]4\x0011IKWtWsk\x001f Í¢ýrOÔª4\x0019\x0018p*NÕ)¿|shÏ\x0003UÏ\x0001\x001c\x001aR[º¢nG\x000bC\x000f ÛK9{"ÕY9i?½¤\x0012¿ã;òç½bP1\x0010©CvÔn.i~ö;\x0011»röõÕ[½m\x001e\x0005íè\x0010ÍíÓ(Cæ\x000eá%½£\x0010î,ÓÕ½Ñ\x0002_c£ew|Ð3\x00100\x0002x\x0005Ïcs;ú\x0007:Ãk¬±ì\x0003Ob\x0002N3#6ðò(¢®»ý\x00006¶Wö\x0001èÉô0c©ì-£\x000flÔÎ
r7¥=.`°©þ ÎÅY¯9\x001cHHM\x0003°07½N+HEÚQÃ	Z\x001aéU»Û\x0004º\x0001,ÌL¿\x0013äÔ$À¤¢gpi°[ÕS¨ý\x0000\x0016ö¥ß	zj\x001de8-wR\x0013ÀÝÅín\x0000\x000e¬~DáøF\x0000(öñ\x0018\x000f°NgÑ\x000b_£µª\x001f@C6IM5co,éÁ\x000eõØn\x00081y3è CÆBÈC¡Þ::C1J\x0011þqóJÜ¿)\x0003ÛÕÞ³»Õ×£\x00179©$	Ô¸©Ì\x0010t\x00166Òh×\x0016Ñ.ö/~­O[\x0014àòb^à¬Äj{\x0008	\x000cVÛI²ÈEiëC}°åU/ý°)W"¶àx%ªÇÍ!\x0013e[Sh\x001fpXOêûUæCÖà'ðÄ\x0007Â\x0014¶\x0000h¨\x0007ûýÛúµx[\¹Ãwë÷W7iÓê\x0001»À\x0016©äÃ\x0008Íå¾
sFÿ¥\x0006óð§åÉÑiZä´¸l23×\x0001§k8\x001cpÐÒ.~t\x0001£ÿ\x0016\x0001\x000b,îj®êýÌÃ\x0000ã:Á\x0017+\x000c\x0002¶8EÏ¹%.\ÞâD\x000c\x0003\x001eÓpÀÒ S!Tð»\x0013\x001fD8a)	p=~\x001d\x00068¹gÃ\x0001;OW"(x\x001c8àÜc\x001e[s-'\x00064ÂpÀlz8aºk\x0011°¬w\x000f\x0003Ü·¡e5÷-=:\x001d³á_u®­jÚa;7ü=ñ		e$üp%$\x0001ænâ\x0013NîÝð\x0013\x000eA¸§\x00136è\x0004paó\x0000²Õ)\x0001Sc^#Eì¨W0è5b©æ²Îý8\x000c1z¨ÃÏØúÍ-6È\\x001aþE"M\x000fg<í-¦\x000cÍ\x0008Í¦1C' BÇÐv82Î°ZgRÀXã\x001dñî$\x000eMEël\x001c¾;¥g²Î<N\x0001B¬Î\@¸"Ma³.®×h!\x000ezÐm2ØK\x000cg\x0002b³QÆDÀ\x001e\x001e^µ´0\x0008±\x0008jBP\x00152ü\x0017Ç+ª
ì]¦å	·¢Îq3\x000c18#\x001edª°Ð*ñÑq¡éR\x0000+\x0018ñð$døÈ~\x0004\x0002ÍËWb
=ñ_¿_¿y,êØ»þ¿ÿþåÛë«û®áQ\x0008j\x0013X&SN\x0001+zBËL½%ÃÝ;Þ[>?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-01.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¹xñ§Óë5\x00181©\x001f
\x0018µJymÄè´¡ÜÊ­\x0010ÎÍ´¶¯\x0003éÿõýO¿i¤q·{stq{ÿóÃJµ6TÎ6ùâ¸´tÌÑsRm¯ÏO^\x001e]]~µ Óæþý÷;1w}óéËíÍ\x0003Ç_\x001eoïînW\x000bK»qÔm\x0013
U#}:éÔm3c-¯O/Þ^ñÉüÓÛ³óó³%qI¡ãíßÄ\x001cÏÕÍ§£w·\x001fv\x000f«6VjxpØ´±F	\x0016\x0012ÃC¯ºÇÖÙ4ÏÕéÅéÑ»³'Wó»ûøëíÝÏ\x0015´v¾»yø|\x0004?þ-	÷­ø5Â\x0014¯)Á\x0016WÜa§Y¹/
ðùfú±hw¾;½º>\x001fÿ%iø-IýÞï\x0004DÜÃ®×ÝÝï\x001f×Ý-ë\x001dÄéÍ\x000cwÝüll¦¼Ô3äýt·ÎÏx\x00057ëýîÃîó\x00178ü¯Ñå¸s3:Ô\x00130\x0019á¯\x001f+ÐôõK;\x0013snDãÍ­è\x0013Ä
0ij0¢3ø¤¢D³\x000c3\x000367¢Ëqææ½`÷ÎR~,¢6\x001có3äàòÝÞ
\x000ey?U	àBæÞ\x001b!5u}zéâßY.\x0007lÑHY\x0003W8É\x0000\x000f¼w3ÝHÛÀ±ÁÙ\x000e®¬ ½CBB\x0002§å­³3/è(ôÙNRb\x001eÐé<V\x001dö.\x001aÞ»\x0019)Ðè¨ì¿\x0019\x001d\
«\x0008\x001dyï$Éú¡=\x0019²wTÙß~îÜqþb!¶É=°uÄá½3Uåè¨\x0002¾ýÎ:*\x00063VØ/à\x0019Þ<À<Â\x0018s{3<LJdOæ\x000c5ýà½ 1GÞÍ\x0006Ù\x0008ª-6%?\x0000\x0001ËO~¼\x0017ÄxöðÛ!_.±Ý·Ã\x000b$¹g·9wðJÑÔ\x0011¾+êÛïm ùP\x001chåCáËU"óss\x0005·¡ã)ÑÀA\x0014ÜÜ(\x0001t\x0010\x0000\x0012º¹Î§ðh>ãfxZ \x001dN7CÐ¬utgÄ
õÖÏè\x0002lG³\x00187ÃÃ®ÿX.®5dW\x0018\x001ej'G3\x0001·Û\x0015ñI>z&\x0010ÒÅõ|ôf	7Â#aûí_®*Ñ\x0000ÎoÊèl	UÂL\x001fÁ6t\LÜÎí'wA,Ùß:ÉþÖwDÈÿö\x000fáv:°ëü¿ÿã?O~»Ý}¹½_YØ\x0019Rb\x0015E³?1lLð)¶\x001f¼;;ysvy1îÇøûï\x001f±9\x001eÝNúx	oÊç»Ï7G'	Í§b)Ji"É\x0019£\x001d
Ï\x0014AÂ7ôíó÷\x0012^ÏOP
\x001eÿÁEQJIÜuóQþ§©íÛ?_ü²ûù\x0013ÀùëªÄ	k°XÚK\x0017\x001d8ù6Êý«÷ÅN¾¿öÏË8©±©\x0015'NàÎýÈ¢¼\x0017E%Ã¼Üf d­Ûâ\x0014AÞÏÜªç!,çf\x000c3S}ßìb3NTqÂ\x0011p4[¥!\x0018´xB\x000fNK
­áQç\x0014\x0003¥þ\x000bãfê[²­l\x0006êKÍ\x001a»°\x000c¥è<Ïë4sSJ6\x0003eØæ\x001d\x0015x\x0012P\x001c\x0001CCj\x000cÕÖÒ3"NOhVÉSd²áJ.­kpKàZÉûêgÈí'ð>¼[Ü´j\x000e4ï¯¡ð5àM^7z5[Qð\x0006OúCïW\x000fXõO7_Þ?a\x0013\x0001Âï\x001fv> Î¿®Â(-ß-ÖÈ8&z®ÊØÞÐÔ6xzôýÕÉÅKDúêõ2Ê=s¨	%'e\x0013ÊgGZáö(ç;· ÜmZP:~2*ü¾}¦dYÉn»Ð½¿\x0001ä&Ñ2²p²Ø³·ÒÍ(\x000clE9¡\x00154 T"F\x0015_æìÁbK\«
0§má-0½§q\x0000SñPp¬Ûg\x0016ØI[`ÒS²\x0011¦Þ\x0005óÔä\àyóVÇyþ×\x0016úÞ\x000e\x0013BQâzÁvÁt^FÞM1Ó\x0011º\x0015&
wkiy°\x0008îf\x001e\x00130¹ÜSbGÀ¤@´\x0015&Æ¡dÚÉõ\x000eç-[v\x0013\x0007Ý 
C[Q\x0006ION¥¬Èéq]ày3Õ\x0002£b\x000bLjWni÷ú\x001aSF\x0019f²ØöúÌ*¿ÿõ'ûãCÕ^ôjwwôòè|÷\x0005ÐøÍîóçÛ?­\x001a¾x5¹\x0017ÜHWHp§¯ÃCÞÍ
D:zzôGç'oÞ\%èoN®¯Ï¾¿øa\x00197\x000f ëÄ­Øìçb	áDô)S2\x00127×M:cö®\x000cxX\\x0003&%b$\oÔì|¤FàÄ8ì\x0006nY!\x000b¥\x0006°\x0016;.Tá\x0006Íôj4ã¦jF/î\x0010ÝqÝ0öÛ\x0012Ý\x0005ö{&½ÒUs{÷;·@$àÂR\x001aÃDÇ¸åà\x0003Îi¬~Üñ8Ò9ñÄ3à (¥¯Ã,[£\x00118¥F\x0000\x0017\x0004<Xz;À¸&\x0016\x0011GÜÌÇÇü9Ñõx~(z¼Ù}:zsûùóýÊ)\x0010Dæn$å¢&ÉB\x0007{QZ§fÄÁÑÍüãéÉÅÑ³ëëË7ß\x0000ø·»_ÿöË¿UüßyûåèîæóÑóÝÝGlu_Ù\x0006VÃ¤\x0010H`~¶\x001a>:½6BÉ²ÃOG/ÏÞ\x001caBûùÉù+ìy¿^Ô\x0004ÓG\x0007^Ì\x001dæ2·9-\x0003\x0016X%zV´´\x0001¬Nºî\x0002kÀcçü6,Þ§\x001aÆ\x0011(àÎÑcWÃýËò7=mà}qó	¯Öû\x001fo\x001eÞß¶\x000eÁ\x0011x×¸ESê\x001396Ê³yºoÀY\x0002^Tø\x0007!÷Þ¡ê&B\x0017àYHpª2
¢¿QÀKq\x0018ðÈuji\x0014ÍY\x0003\x0007N<pâ·£°T°C\³0Ò¦;Á-Á\x000eþ°Ë\x0019Ýã\x0006ìe.Õ(ì¨ý¸ôf|)á¶\x001e-çÒü
Øy<Õ(ì&;`÷Ç"ï;öQ\x0011öÙDõZì`êÌûßÒy\x0007Ã­m!4¿~¸ÿéæóçÇ£óÇ÷G¯pH\x0002¦TWµÃó e´"F\x001e*-é
bipÞ=¾|{ôúêò»ÓëëÓ·WGço_\x001c½Â	b½úÆ\x0012µxLû_\x0014b{Ú÷«¿ÿ×¯?ÞÝþûã:\x001e~\x001a\x000b)Ú¹\x0013Ñ{G=~8Ïq1õ\x0006»~uúúíóó³z»ÐfÌ¸õ\x0014·îÂÂ;ãÀÂÖTñÅÌtµ\x00017Sà¦oÃ\x0015\x0013Él,ïá\x001d±\x001daÇ\x0017\x001fí\x001bqÛ)nÛ\x001bÁ9Ãsåh8»\x0017d\x0018mð3
mÀÝ\x0014¸ëÛðÀºÀ6\x0006<ò3xÁ.©$l\x0006î§À}ßk\x001es\x0003á eÅÞSv|äÕ\x000cSÜ¡\x000b7\x0016q-]MÅÅá5V®æ\x000c¡³
x\x0002]Àe(\x001b\x000e{OyýA	bàK1ÅÍ¢d­ÆÐ<kº|Ä%×¢ÂÂ\x000bm;pY\x0001};ÎQ°ã<ÖË:®N° \x0001·\x001dxå5eÛÔ§§985¬¸ånÎ4*´!¯ü¦ìs{kÃ¶4²*Ian\x0008r\x001bòÊqÊ>Ï	.\x0004àJ|RrùÅ\x001c<,ç}®\x0013¬ 
ßtpn\x0002Ù\x0015/ùzF1\x0012yå:eïK\x0019T±¹\x0012\x0002Nß\x000b:\x0010wå9eë4Yï5á6EÌ\x0015	Õ\x0010\x001bW¾Sö9O\x0014­¥
÷Ç}>Í2
\x001f[U\uYrTú!-k\x0013q	¸a	Õ8ÇéoC^?ºL9vúö«ó±Ö)æùÇ%úâvä)W]¦Ü8Co7ç\x0002ò\x00193pºQÍ(r·á®\x000c¹ê2ä\x0006Â\x0015rA`J(ooñ\x0010òoNU\x0019rÕeÈ
N\x0017#³\x001289â\x0005Ê´N\x001bòÊ«.CnLà\x0011i.z~½9ÁSãÈW§ª,¹ê³ä\x0007p;=éEYW\x0006\x0000G=ò1¡*K®º,¹ÑE1\x0006O¹âS®=ò\x0019\x0019ú6äÕ3Hu½q¬"ã£ü­E\x0000ïùîáVäºòBºÏ\x000b¢ü\x000fÏ6~z\x0002`®UåN²È+/¤û¼(þ3\x0008£ÓbÉïÇ¹Rf\x001bð:\x000f×çò Ã|Ì5é\x0011Zëc1æ\x000bÚÆÛWnH÷¹!é¸7Ò#Ô\x001c'!§<Îtï·!¯üîóC¨@E[.
ðP*²va´Ávà\x001bÒ]n\x0008É<µõ9áÔP\\x0012\x0004Ý\x000c¼rCºÏ
)[Î
< é½o½-Æ|f\x0002R\x001bòÊ
é.7¤Á\x000efa\x0016å­&IKØrf\x0000äæÝaÈ+7¤ûÜR<D\x001deo(f\x0007?\x0007¸N\x000c´¦ÊÇ®|\x000eÅP»]¿âÙ^b`ß¼r ¦ÏâÀ¿\x000c\x001cG*ÒaqÅ»I~SùOÓå?5<ÝtV÷ñøGº \x000eó°®aÈ+\x0007jú\x001c¨´\x001c³xéy®\x0001¼ã,ïùHàu!«Ëb¬ä-WÔÁ
§\x0007\x0003
92h*ÿiúü§(¼âÉæØ¿ÏÖÜÏ\x0014ÊÛW~Ètù!´æ$¤s\x0019\x0005Y\x0016]\x001e\x0015aF\x001aª
yåL\x001fò\x0010\x001c\x0007EV¥\x000bÊ³¯ZîVÞ¼òC¦Ë\x000fAtR<(*¿ÒiQåÕ?4_a+?dûü\x0010¶îÑVIÚr¢Ñ¡-[¹!Ûåtà®\x0004µC~«lÙñiP[¹!Ûç¬§¦>\x0015 N¤ÐÜpO>D,3ýfmÈ+7d»Ü\x000eE×[ü¼ç²Ä#]¿­\x001b\x0013º¬¹ö<I\x0015¢-]¢-ÉÃ)á¿=0ÂµÕsÈö=LàäV\x0013¡&ðH=ì\x001b\x0007¼rC¶Ï
a\x0013\x000by~&ÈÀß\x001aËl©°-·}¶<ã\x0019¹ËfÜòýT#O¹«l¹ë³åFs%À;.3¼PW÷<L÷»Ê»>cî\x001c\x000b){Ôà¤wÅó\x000fL³¸Ê$º>èÊÄ1_f\x0015ØBDFÿ9ð~º*4w]¡9N^¡ö\x0010,\x000f×3ÊNª\x0019\x00016ä1w}Æ\x001cG·SÌ\x0012-\x0017µLÜÇ,#ë®²®Ï&\x001aÃÖ \x0005ÍÇ\x000b\x001aØõ¼Udîº"s\x0018i\x000cq\x0011ð´ÚÑkÈ%\x0011ªqÈ+kîú¬¹UÌz
ÄË3¡ì·\x0019YÓò)÷]¦<)ÐC¨ç
Yí©±ÏÉ0²yÈW¦Ü÷rSÒ AD¢¸Á\x0019w%¼U\x0003C-_\x0005æ¾+0W¨$ÉÓ#¿4û}\x0019GÆå¾rB¾Ï	Á´åÕ0`Ë6\x000b[>2Wá+'äûfþ©Þ\x001cçû©âñbdFÎW>È÷ù í¸c\x0018ÃrÏq%HtK-ýW\x000f
ßõ PZ±ZA\x000c(¿\x0016ÖÃ3ºåÈXË×½Î}ÞSKâÝ¨ |ñû<Ç
ÜÆÈûYyOßç=±G	Q,ZSC{B|å=}÷Äþò¼ãpà©GÎ°T¬CþÙ8à¡ò¡ÏÂ>gb\x0016JrIKãC1oùÒôíÈ+ÿ\x0019úü'\x001c\x0016êK\x000c\x0000Uä\¿Ñ,ada(Tþ3tùOÔ­\x000c4À\x0019~Q`¯\x0002í9NI\x0019¼rC¡Ë
I/Ë\x0005õÆYìgÍÈµÑ·lC^YóÐeÍeïÒû¤ ²eä3bÎmÈk\x0006HQDq,eÆP=O±p/yÏç¤'ÚWF1t\x0019E\x0015\x0005w\x0006_\x001apð\x001c(J;\x0010y¬¬bì²ÒZê2×\x0000\x0012+çyÏy2¨Özà9U]V\x0011<~	q£9±VG*°89ÇýlC^YÅØg\x0015­DÆgÚs-1\x0019iÚs3£iÓ¼zVÄ®g\x0005ªQ+kÀ±ö´ÄaÏG¶âÄÊÇ>{n¹·\x001föÜs§\x001cfviÏíÂ\÷íÈ+{\x001eûì¹ñ¤Â³å¨¹BijÛ\x0002àqä\x0005­Ìyì3ç(ÂK[n\x001d¶¶däÅ\x0011ÍID·!¯\x0019}}æ\x001cÇãåtbDf\x001ceZ\x0014çAÍ@\x001e\x00145Ç\x001f»ö\³ó8LÂ\x0016ÅY9T\x000b\x0019\x0008½&õ>{\x0004ü~*pE;êÙvr`YKÖ\xü±kÓYë\x0006\x001epY,(ðI>7	¼
zÍ1\x0013]I\x000bµ\x001fi\x0015ñaGnx¹´[:Cbú\x001côd&úì¢f¶V.\x0008]ùë~è®×<3Ñ¶PR°ØfT¥GQ\x000bN¸H73£
z¬¡÷F#Ë-µãv9\x0019Ô¸ÀE>¥\x000c÷Y\x0017-9Z(\x001cÊ9.Ë[\x001eg\x0014ZÚ ×\x0004Ö>\x0006«D:%«E\x0017è\x0018EÒA\x0019ÝÙ¼¶.}\x0014Vùð9±¨8ñ¯¹#Ç)9°X>¡°öqX¥2¨{ì¤¸(ñ¢äàÅl\x0016ùÅÚGcE©-*·Ä([¡e(»>0HÇ)¢\x0015ô>ëR8Ï\x001aþã%|¡\x001b9.»(U\x001dy©¾ÈËå°K£A×sá×U\x0003Ë¸²fàÊ>
®Ä¢ÉJÊ\x0016EëKVt ]¬y¬²È*KÒE\x000bmÙº@ÔEWTÙ½¡²fÊ>J¨\x000cX~ð\x001a²Åº¨r#_\x00185%TöqB¥\x000c¹×\x001fNz@%á\ðÛ\x0008S¤\x0003×v±\x0014
a\x0002@Uá<æ\x001eðré"mÿ8è5½¿\x0015©9M»®#6[¸º\x0019µsóÚÛ ×&½\x0016*½=ö´é[[Á2òI\x000fbà%ÕµE×}\x0016\x001dÉyÏ­ãW]\x000eæ°Wt òúAÚG\x000b"p\x0011\x000e\x00063\x0015däAH#9ÄR?é³é.P\x000b\x0016^Ñ¬)ðÜ<§FÚÅ\x0016*ûx¡\x0012Ë¸4}Ê\x0019¬z¥=\x000f±\x001cç¼vF}¼P,»ÐCZ_2Ë.\x000bFf`^ó+e\x001fÁ2U/xæ¹æ|4£\x0008ºÔ#w½6é}\x000cKCÏóqÉóÕòqaäÖ\x000fl5MQöñ\x0014E,å\x000b\x001cfËÑÓØ:#=\x0007B¯Ý>¢"NUÎ.Zá\x0007Lç*\x001aX\x001b5SQöQ\x0015EÔþÍP,8#¹{\x0001sF\x0003×6½ªóÝ-¥G\x0001¹çDæôHy\x0005Y3þd\x001få\x000fKE/ØíB\x0015iÅ¥}Q¨·[\x0001ïÒÉy¦Ó\x0002Xmu%NìËÇE\x000f^\x001bÆ>Êp
ñ&è8X&gèrÒ¾HkÊìãüáñ\x0016t\\Ùõ2¨Úi?°\x001fMÖÔ9ÙÇðø\x000fd\x0019ÁÒ?RBrM:\x000eì\x00035yNö±ç\x0015ÄAÓ&(î¥\x0005Ñ\x0013\x0003þoä®?øë³/Fá¼ðÚUð$%ó\x0012y\x0012¨\x001eÈA5#JöQ¢Ð¨S\x00105$º¥Ø @Ð\x0007ê·È\x0011%û(Q8¸lºÕ\x0005rK«O§q\x0018òú »¾\x000eOÿ,m\x0014K\x001cv\x000e:f¢3ô¡¯£\x0013%ûHQð¸¢\x0011^àx4K¶bO&\x001d\x00177°\x0011PÖ¤(ÙÇ\x0012ÒótYeþÓy	4\x0002\x001e\x0007<êµyé£E¥ÊQ¼pÒ°£K*9CjÂÌL¤6èO$D{\x0002\x0018\x00191åýEÊeD¨h×Gú£Ñ%û(]RXwqâ#5\x0003Ê@ªy\x0010¿,OÕÛ\x0008½¶ê}Ô(\x0002Èj!i2js\x0011Úr`¨^sd\x001fÉHJ\x001eV­QZÙqßÓr¤©©:²«#Á!)YGôÈÑâÑÈ=¯Mc\x0017WGFé¸2í\x0014§Hqv\x0019Æ8v)k²ìcë`r\x0001Z\x0007¶ê°"N×é\x0001LÍÖ]t\x001d\x0019±H\x001dËÌº´ë\x0006å¸ \x0007JZKÿD`¹Ë4
\x001bù<\x0012\x0012DûâÑÀ&LYóud\x0017a'Mé³ùA
gzÓMäÄ\x0011J\x000eD^Ûô>Â(ÍZ\x001bÉ\x0015;©\x0005\x0003#s·A¯\x0019;²²\x0003®9àuN`æ.o:÷2®²¦ìÈ>Î\x000eÎÞ¢BÆº#
øñ®äwB¯\x0019]¤\x001d´Ç¹\x001cà!É¨s4¸ýF¡ö¤¡ËbfÍ\x000bv¾'e!:\x0007ñû@ûRÓd\x0017ß\x0008â]ÉY/\x000f"¯¤w=LbÚ.W*°µ+Ç»FÊrÔ-\x001b\x0018Ù´SS¥d\x0017W
þÛ&à\x0008dzePj¼Á¹	P»ÒÐçJ½á·ØTà¿ÈY/9P_L'Ã
ú|)D\x0001¹ýU{)(\x0019`p65íº\x001f(^(kì#za^]PrZKÖ»*¢QØF:\x000eyÍó]D/ä\x0002\x0019\x0018C¶ÑÀVK60\x0003y$²¦KÉ.¾\x00148HÚc\x0004C·Ô²òE\x001c)"k¾ì#L	çPâ2×aJ{4¬ÕåÔÀa(²&LÉ.Æ\x0014j[`­\x000e¡\x0007¡Ê`jÃiõ8Pn\x0004Ü_¼Ï!A¬\x0005^´A!@
\x0003J×-Í\x001eÞ\x000e½vH]d/ÜÌ15zÇz&ó\x0012\x001bhÕk¶ì¢{A¼\x001e\x0017	z\x0008Ægèø0ÊÐÍÈ^î%ûø^\x0002l£ä£*\x0007Fi®ä\x0000U³¦T\x001fkJÒ§n¼¥IÅVJö¥\x000eyßã ×shDm4¢ÄA² \x0014Lÿ\x001b¹ëõ(\x001aÑe\x001bQ,\x001e¦¨;¬ºSOïÒ\x0018fF\x0015·!¯gÑô\x0011¾°SÚSc@Ø7ï\x0008Ö5p~ %CÕ/ÕEø(\x0017Mþ\x0008¥vr\x0000ã=÷\x0005Ä8|¤êÉøc\x000fr§ \x0008Ï8²/Æ³4OµüqÐë¡.}|/T§ÉÓ¡ñ°&p¬É\x0000\x001ei\\x0018 êñªk¾¥ôÖ\x0013UM£!åI½
¼ëz`³ª§-ª®qØØÍÔ\x0006çJ|\x0012\x0001/SJ¬-Sªf«©.¶Äq\x0011T\x0013ÀDµ!Û\x0008?Ò®Û£ª¦«©.ºLâWÔ\x0018`¸÷X\x0014\x0000/\x0007\x0004TÍVS]l5\x0019LÉ6FÔ××ô¸ËÏR/ÕÀ\x0019´ª\x001e\¨º&\x0017JR\x0002NÈm \x0007\x0012XujÇðr¤´ªÉjª¬\x0006¾â\x0016\x0018\x000bÐ©\x0005F\x0014¡t?ò¡j²ê"«Á%µÄÕ(²G\x0019\x0018p¥v]\x000e^\x0007¼]|5x\x001a*|Ã¢Çô*¥}gä\x001d}:0²+á±\x0019#oyÔ$úb¼"\x0002²OMüÃ×Î¨g'£öÜ¤³çsÓ´¾8#7Ú L^ìâÙÉ¨JVÝHMÓ\x0006§£\x0010ô0°l§L0ìb«É(-«§à¬hÇµu®ú8°WÕãôT×<=\x0019¢á7\x0003Ç¤<íó5RDé'£Q»z\x0008@RCK\x0013°\x0012rYê\x0003TÍQ]L\x0018\x0019ò,\x001c\x001e§y\x0001ÄÌ\x000ef`SªI\x0019ªºÅ¼éð\x0012"á\x0017\x0003ÿ¡»s;TMmP]Ô\x0006»"÷zÙ¥Ì´çtÝÈ¹:ªf6¨.f\x000c:I\x0003&ä9%sê¬V\x001bÅ@icU\x000f3R]ÓdP<sDc\x001cc	zO©<\x000cz\x001d2v\x0011\x0004d@  HÑà9â\x001céÀLxSüùËÍÃÓg\x0006þªçÜ\x0018Ô«IaTv4Á\x00129\x000eäóÂÛâÏ?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-04.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=ºþ·Ý$)ÊØ@"P3ë\x0004Ý\x0013\x0008{Ún\x0014zÊ\x0012\%ÃQyê\x0003\x000e!XeHMÍ`C²Eé\x001cE\x0017Xr|\x0010¿ka\x0001\x0013SÙé,°\x0018\x0018\x001ecyYlL§ (ÁP¾\x0001E\x001dâãèÌ\x0006\x0014C\x0007×Ùþ\x000bZP7ì\x0014F!EË4°ä\x001dò¬ÿ´\x0017f\x001aX¨«L`	ÞÇÓbòÃ\x001f8Ó-,ÐJÅ6È\x0016!óYP#
÷ÈÐC\x001egj\x0006K8i¶AºàKJdÑù]ØhN,­[äû²¼¹Ç2Àªøoñíîæ~Ç{p
Ä8n±¼\x0019X\x000c\x00176\x00083c]ÔÑÛó4ð8-t\x0003M¸Óø\x0002#L<\x001d^ºÓbý\x001eMfd`É\x001aX
)\x0015¾U8\x000c!\x0018}\x0016î×åËdüL1\x0015F3z¶çÞÅ\x001cø>.I!	»~f¦Ó\x0003£Z\x000eri^\x0000Ð¤Î7\x0000Ã)YFø\x0019û\x0004\x0001##\x001a`Hm¡yax\x001cÒÐlP3\x0006Þík¡Ñ\x0014I\x0011BdË«Lã\?M¸©ÏlË}8>Ú\x000e"y\x001fÆe;F\x00194a]­m \x0007\x0006²d\x0018É`.rÖ3d
¸;¾å\x0010;\x0016\x0003pÑI£þFæ$
£úw½\x0019?&ãP»dÀIÑ%ÀQ.VLÏÀG
Ö²W\x0001QâLI·\x0011Äß O¨
\x0007\x001e»8o¸VÉÔ,\x0017p<åHp#éè8ÖxtÌ»G¿tOð\\x0016ìÇ ¦Lùäï\x000e^/n\x000e

)¡\x0006 ß?=üýiù\x0008\FA\x0003ZHVJ[«ðÌ+\x0016w-¸ùÌ ðy~q}ù¿®¯V\x000fíáßqtþ\x001d»\x0000\x001d\x0000º>@\x001dK1\x000fj\x0004>\x0004\x0000ðQ@°ïãW÷íÛmeu3úòæÓír+\x0019TÆ7Ææ·'àþI\x0010¦\x0012à¤E2Zv@_¼:\x001bL.© \x001eXÅ\x0004'P\x0005¡vöÓÃÖ&&©95	±L
»á)í¼\x0002=P)Ï9n¢§·ÅN*n!\x001ece\x0013òZÄlÀ2iìxÀ·\x0004Ä²\x0014\x0004ïÆ(Õ­X,Î3X25
\x0001,%\x0008KêyX\x0010Å\x001fMXÁ\x0019ÑSÀ²©Å|ÀRÊ\x0011wÜ\x0005¬\x0015K¦ )`è:\x0002ôy\x0013í¼Õ\x0012 ¶âG\x0013\x00168÷´Ziø(`i-	Ï»\x0012ÎfühÁ².=í\x0003\x0016Ì>7\x0011\x0014Âq!zÞàÆ6,BD	K"åj|ÍuâG\x000b\x0015<U¸X\x001aßø%¹,0PTv'\x0001o.~´P£RT\x0003\x0015÷IÂ3ÈÏF*Íç­¸Qüh¢é¸V¥ô\x0011	Á,T<Ðir\x0016\x0016tax\x0016?Z°$CÛ\x0006&\x0012GÅ´Q¸ðp=É\x0002S6\x000cL©çLÄJó	\x0001K[CXnÖ\x001d¢ßh6\x001e,\x0006\x0015Ùi¹4Ç¡`ô:\x0006
½ç\x000e0è\x001e^x+\x0016\x000el\x000eXÊ¦A\x0001+\x0008\x0007\f$\x0012¥Ï\x0006.éLe$K§h;p)Eë\x0015S\x0013gpÅºôÙÂ\x0005¢*fÁ)-¬bõPx\x000fo-Ë¸yæC¸Ë<fÚ´©\x001e	bÁ&#\x0010TcqàdçÄÅÍ,û!(±Èå\x001b¹l\*/¨¯Â;Zg¾\x0013\x000bÊc¥Ï&¬p¦Òj1\x0010ø"QI§Z5¿¬\x0011G,Þ¥S^Ö\x0012)w=p)»¨å<S[ÈÀMM\RÆÇ°\V§w\x001dèþN+ÀÎ\x0012õÜªHMX\¦^Á+\x001c®X~ |0w

\x0012ÏÛÆ`\x0002@¦,oS×KÁj\x0014\x001e|\x0002\x0016¤}ÎÂ\x0002[+}6a±4Õ3báZ\x0019Kk¥ÌL¨êd«à©]öÿ§îÝ²+½3í©ð²ÿ\x001b.\x0000ãÊ+*ÅJ±\x00163?\x000fZ.ßhQ\x0012[bw*SfÕåºò4<îqx&\x001eI#\x0008l`coî¶ébÚ¥|
\x001f\x0010\x0008Äá\x0004E-T¸X¹2\x0016¹Ì"×Fz¸\x0006}y\x000c7ævÞè\x0012bÕxÆr@v^gM¥\x0005X&}C3ø
­Ë¾\x0003b<m\x001e¹ÀåÒ%	2É\x0015RÉ[\x0010[\x001e¹R\x0005ªÆðSÚ]ÔM"
8·ì+t-Ñk\x0011\x000bc\x001daIp#\x0017hæZº\Øv\x000eqÅWkjk\¢\ñ,0Yx\x0001\x0005HQ\x0008\x00184ôÖ\x001cßÂþ\x001c¯D,	¥\x0019zì-\x0017
»G.åõ#\x0012e¹Ä¢Ï¨R7j{"\x000eàÂé\x0013©\x0001[£Äl®)S\x0001c\x000bC\x0012¸PçàMþ9´^Òå:u­5Ö¢æí\x0015yó
¤ÃÂ°ÒXëq)c,û7Vå;H{ï\x0016¹7Jã£ ÿ\x001cÂR\x001cAÅ\x000eT\x0008.lí­[t\x001aUÊêå£Ë\x0015$qé\x001cOÂå¢XeäZf%\x00159µ1öhLÛ#Ê¢©ÂÍ\x0004Ê#.;^¦Æàc\x0016ÒXÌ%@§Èeèn\èH¨Pùç\x0010!eY
È0ÙF\x0018D¥]âúýó\x000f/ÿ\x0012\x0019\x001e;õ
ÕËÉû//_\x001f\x001e"Ân4O]I9Èï4üÓ\x0019FlñqîNÞ_ÝÝÜ_\Ç?ÛªOÖãi¬Ôù5"É½¸9\x0002\x0005.Þ\x00163\x0019áéI¤fÖ/þWî\x000cë§l6ÿ=b\x001cÃtÛìÙ\x0010 zéÇ8 qyÔ^\x0004\x0004K&\x0011PrøÞÃ:\x0004\x0012!éÇ8 6ü±j$YÞ\x0008(9Z'Ã¶´Ç\x0010 \x0016¥\x001fãÑÔùhð9A*<8ÎBns<ÆøLz\x000bLñA¡£ô²pî¨txÝ¼QUÂÀ	Yß\x000f±AäÑøyCÉ\x0001ê.¿<\x0005YÏ|^¬Ç¡í§¨]\x0014pö-çã\x0018|øÈSfb\x0001£%Q\x001c\x0010Â*RC_X\x0008N\x000bú-ö!>ìVV~ÂDC\x0008SKÎÓû
0aÌÒµ\x000c0 `YÀèBIºâTñCI2é#\x001c´IüÜ
ìJ¤\x0008\x001f6n`ÌQÐ\x0015\x000c[²\x0015C¸t~jý\x000c\x0000v½\x0017:\x001e
¶e\x000eGè\x0002f\x0018Òq:AÏUã½ÉýÑµr¥\x001eC\x001fãþ
#\x0008rêó
{ª
	ÄÇ§7ò\x001dáøb\x0005Î gn\x000fS¬Èÿ\x0001¡\x0014ÙèmÙ!@,¦\x001fãøìq«\x0015Ìq%#LYÁmÎó\x0000 \x00144Å`f	£u8ð\x0004ûTÜ\x0019	5(ºâÝVæ2Dj]"ÄòEúÈ\x0001r}|ÆD­²rKPg0WãÈ)ÂÔ@F\x001a\x000b¬ò\x001a*§ÊCd9_É?Çù"¥olò\x0004ù´b?\x000bpH2l*Ì\x0010FG%÷/`\x00005Æ]US\x001cc\x0017B¹)SD¨\ Âü6ÇñÕ\âp1Âõ&ÿ\x001c'Ä¥ìMcÿ \x0010¡\x0004vVÁ\x001dc
ø
ø)Âè\x0002z"Å\x001aÀÎ 87óöPBÎ<ç¤Ò418=â´¢Ô©ä»j)¡I/v3õd\x0017ÔØ"Çà\x0010U÷3¡ðË]\x0006fûæSy	q¬µ\x0004H\x0015H&ø#x8\x0018\x0001§îdád\x001eà\x0011	M\x001e\x0015êM³^ÅrÂtNÌÔ9Á%¤¼p\D¶×ØnJayÜH¦Âüs\x0002P\x0017@­N\x0002, °\x000bÓ½Î-!+	\x0015©â\x000b,PhË"-»\x0010|\x000bÌ<Ý1\x0017TÉSÃ»°\x0000\x001ec\x0017¦®ùçÄ\x0012\x001aö\x001a4>ó\x0002-a(%_Ûj_\x0008±y4ÿÛ¬L\x000e\x000f"!gÐ\x0019;Â\x001aú¤\x001däåg(è\x0016ÑKÌýñ+\x0003§áÝVy2DØ.\x0010ÊÜ\x000b\x001e	ãA\x0001²3¹Në#\x00184%YC)ujÀµ¸llâÛ\x0008ñO\x0013ÒÞä\x0013~
ç¹"¡?¥%täxE@}\x000cÀT·\x0019ü_\x001394dH¯©ä×ø²G\x0008S+G$ÿxä\x0001e|ãA\x0011y¨
æª¸¼Çé#Øk\x0015ÿ3#aYC³p³9TÚç¶æøPÖ\x001c\x001b»µDd0ÄÌ?'
½×xð\x0003@ó#Ê°­DjÐ¥\x001cõÔCY{EÙ\x0008)Hë\x0001£!ÔNfÞÖ\x001f\x0002Ä\x0002éüs\x0002P³o(WïP#Ë=5,?ÊÊÔ8>e
±øÚçXC4ä6\x0018M©k£Qúð\x0008!\x0001NE\ÿ\x0008ÀTÇ«ìT¬Áà7¦* Jv,z¡g¨#x×
{fÞä\x0013AuE-\x00110ë]  ð\ÅäðÆSiPHþ9NEÇT\(ô)\x0005Õ\x0015{¤T\x0017\x0003bQZþ9ñ\x0003k\x0019z.Ô)usFÍÂ¿ªÿù·ÿñ%)\x000bD6Í3áÀðíËã§§Ç}5\x0015Ñ\x000eJªSÓ¥NÚJÉå²»³JÆåÙÉíÝÅåùõÅ¶²\x0015\£40\x0002gi,Â4*.U¡pU2È¾³inMTäp:#éé\x0019é\x0014×rG\x000f\x000fès\x0012ãtèey1A§ÂpB\x001d\x0007åJs\x0010¦3.Ãt2©M\x0019<Å}\x001aµH(zdt©C\x0014a\x0019§K¯v9s*dÖ\x0017Ë_J£;ÈûNôÍ\x0003Ò}ù\x001cþö¿x$Ö$£vòýã/ïþãÝ]\x0003\x0010ÀgQ(m£\x001b\x0003(j	]ø\x0012ç"½ûpv}¾YB¬ÁÉS\x0015^
\x000eög¾",köjp¢Ãf^\x0011\x000e\x0016¦½"\x001cÔKyE8XÔðÿ\x001a\x0007W¥Cÿ\x0000OØj¦Ñ7÷Ï_îí®:\x0010g¸\x0012ÉàÔi*ô\x0001ªK¹\x001eU_6úæìöâævúma®yÍ¿S*ÅÁ$\x000b¥ 3\x0018NfeN5\x00188\x001cÆ\x0017ÎQ9»ªKÏ<.ÌTë/ùaÊà\x001aÊøë0%vãSu\x001cRÒZà\x0018²+\x001d\x0018¥TügJüuÒÚ¸ÿVÔ[ç9s+ p\x000e`JôWÂÕ\x001f¼Áæ³òï÷/{ÒßÆs/®¤-©Téý\x000b°î/Ö|ÿ|v·\x0007®:6\x0011nýÔìC
àîìõ(a$óu¯1>\x000b5Q>ü\x0000ÜR#½çM\x00179\x001cÃó¢Æób\x0018O\x0012]ô\x0019½&:²Ùqõ:ö`¼4\x0016\x0017Vç8îrpõèÅ·8 ë9>L\x001fOÞ¾üò²ïU\x001aíaÉ\x0008\x001cs\x0000Y\x0004FJ\x001dÆ\x0016X\x0014~º¹9¿/ÔóÛ·wïî¶?O	]ÒømBoF\x000eÎ°£&v^é%YàE{.Uf«iw-üÂÇ\x0019dÄ\x000e9ì\ßE+«vÙÕÂe§9sî¨\x0004\x000f$¶\x0012:\x0016ã\x001d\x000fÞ\x0006ÞeðßêñæÏÂ\x0008¯K}c°ÇO3q4Îê\x000fÞ¤I9ÍT\x001eþ´KÔÅpãMÊ\x0012¹\x001e8\x001a;*¯è\x00033Í¨ÔíS V^7^OPZÇþK\x00089ÐÒ3¥\x0008\x0004ú~öaÌø¸ÆÄ@æøbÊ,\x0016©qÚXR5IÉ\x001ftW25²v\x0015fR¹\x001bÆü,\x001cå{Y#&°¢\x0016ô]#@¢Ø«?HòØ=%Þx\x001f¾üëÃÓî\x001b/Í\x0016Êáëxûq:Ô\x001aÊåiÔß×ß«¿o\x0013\x000f,Ü¦á^<<Æm³ª*r+ê°¶¶ô\x0002Â\x000e[0m\x001bì{÷`lGu\x001aðúæ\x001e³²Ú\x0007\x001cµ\x0003±!4«
Ý\x0014ê\x0011îàX\x0008
S§Zkxà\x000ccqÇ^sã¯ÓÜZàl\x000b¹q¶#A\x001fJ~ ¢Û6n\x0018Ü\x0008Qã¯\x000bÀ'G^k!JýK\x001aàhÛÄU/HíÌÆ\x001bä@j\x0015¯h\x001fJ§uÈ
lÚZ\x0006ï\x0013%SàâÖ«?È\x0011ì³ÿöËË§<áO_^~úõaw¼&\x0015ÿSw±AÑTCénO¾?jymõýß^Ý]FÇ\x0002\x0007àþéêî:þ/¶pTz\x001fÇo»ú7ØNÑ°ýºï¥¬PäKäÊHÉ×¡Ñ~«sxonv<3cå¾EF·¾¾\x00070*Cý
: B~&MÉÌh·º\x00072¢kR¯£°ã²´¢ÀÅâEÛ¤«>\x001cºl'£\x001f¸Jnâ\x0019Ü/i\x0016Z~û»þ0HÝ|müu\x0018R³¾¯\x000eÊÓdð\x0005Rn×íÌa%±rÊ#Ü8Í}}ëÅOf,»×ùýZþrÍø3³c¤ûOBÃ\x0007ãã_.^¹N\x0013`QHî:\x0007\x0001U³jb\x0005=)î\x0018gMºN+è¹¦½KI\x000e\x0012BC\x0008ÃNin\x0012u¨áeG/\x0002bGn\x000f¡ÑéÍµ"\x0011þZ!â´¢}XA]ÞZ*Ç\x0013¨ài°Ôv×Móñòlû\x0019IxPÝ\x0011\x000fÚ{q?\x000fÕR\x0004¸<¹\x000cÃÙ@ò\x001f\x0006ÇÀ/ÀS-\x001aÆS\x0005\x000fÓã\x001cmg\x0017Ú¸­ÿ>¼\x0014¢ÓÕÇ5iÐCE÷åó3?{JL»«aQä\x0011 ]#\x001ft!´nûqþxõá6Ï?»Nÿ«ÝÜFÔÜF,âÚFÑ¸oäV,\x0008hMW\x00151Áme2H«\x0004Lô\x000fÔ*ÿrsÿ\x0018©ÿü°oC\x0008T?Î°ñª{!Ã\x001aêj6~+ìÍÙEDýóù=AºaÔã*_lð\x0019"¨À(*3ñ}áö(cå¬EÆÊY;\x0011\x0005\x001f¹%MÔKUá\ð-9ÁC\x0010sJ°BtY"cõÒøþþ\x0013F\x0003wÛö ó \x001bÀù!3b\x001f\x0018§Úâ\x0006Øþ0úþì\x0012#û U\x000b©¦ )P%
ä
qk
f?£\£È\x001cG¹øíw\x000c§¦÷Î7î÷>w´À&SR¼*k¡(~\x0018Gò°~j.ÞÄ jzå|sy¶ó9AÕèºs:Íj\x0003k2&Kzä^Õ¶,çÄjÊÒ²E ¼WÓ/âTaífBPVÑAa Ýñ'Ô½±$Ñ\x0016¸[ÍF¯$ÚtWW@£~Ç¸Ô\x0014Íï\x0004©¶\\d\x001cô\\\x0016zë	Ò jÒ æHÕ\x000b£seS")=¾±i\x0006Ô7 ~
\x0014gPä2Öxß
^R§´\x0013\x001d'v¹&Å_'PQ¬<K¼§¯OEËÎXþøòâ\x0010)$©*£O\x001a¨Ï=\x0006¾Þ}yyzÚ'Ì£©í£0Ñã\x000eü.\x000f¢ë_\x001d|x½»º»¾Þnï3¨Ö5(vPMb;Gî*28Ä¯J\x0019xPß<Cj\x001aR3E
*1æF`'²åvÐ.7<Aj55skªU:E©;Ùçêaüúë¨L7áb´YS3·¦Êò,\x000e»fÒ\x0002ÚUÿLzUz5·¤Ûó¬\x0004VºæÏsÃw'ò8CÚ|?wôUÖmH¤Y90ËÖt½Ý:44¤a4°ÒuôDr\x0018\x0016¿¾a#\x0015:\x0005îqR)EM¿N}GUÆbð*\x0013]	\x0012,Bu:ù¥«\x0013åô\x001b0Í
õîéþóÏ'\x001f\x000f:QÔÀç\ö¤\x0000'=µÞì¸¢Þ]}øöäã>ÒúÉ\x0014I¥\x0011S¨Bç±¥ÚH\x001b
*°1
á,Gµ-ªDÍ-"	µdÏãCG\x0011øNKu\x0008\x0015ÂÚ÷¯IX³¨ÿùoÿþÝË÷?íñP\x0014««\x001a!µ}\x0005rùûw©z£|w÷ÍÙÛ=ÞÕ\x0018àÀÄé*ùì+©Y¹\x0018~T¯]Aý
3ÅøgS|éãj*½óèäS?ìÒåuè; øÑìgçælky²H|BsHÏw\x0019Î\x0001PÊ»aÓï2LõÖ\x000fÒ÷_^>=~>$\x0013«Ïu~çéÀ>ö] ¤~¾¿º»¼ø°ýA9«ÇSä\x000cb\x0013£a4ï îTê12\x001b¢5\x000fcÖyâòÄã
8í!à^c­¸][»®`\x001c´ró\x0011´õó\x000f\x0004\x0005¯Y©D(Ã­àJÃ¬Ûnë\x000f\x0006­æ5\x0015Íâ¼\x0006V"\x001dïP\x001bîÄ
'8Û\x0005uS\x000bj8[\x00139I4\x00189\x0005'5­_| z3ãoÞÌ\x0007*MªXe·(÷1ªnRÛ8¥i\x000e\x0012¬GÊ\x000e£T¬@\x001a)5
\x0012QÞVÕ®\x0019y3¬=âJµðèÕ§Ç¿>><íátÆqyEàAv¾d\x0011Ûñ°¿9¹º¼øþâüz\x000f)¶¾V¤©\x0013v\x0006Õó\x0014V\x0015ÊÍé9#«úYC¤FüÐÖÀÅï®lww^=Ý?yÜãßéTVOïP Q	\x0010 ùu'w\Kñö¼º>»½ºØáßeXëkXëga©D\x0000amn±Æj&Bt:3¨Õ9¢®¿\x000fG
%y"º:G"´\x0004^XÝé¤MÑêVOÓZVÚÇ¸·D[Îz·Wz(m³gýô
ñJ%ZT]uDËCÛÙþ&96%ðªJ&¼d×ÓÇ\x001fâ¿Àôí×½CÓ<Gzð\x0005E×¾¼ º1\x0001Õ\x000bêãù7×ñ_ÝìÃPãBæ×\x0016·SÏ%èP³Ãb¶%Gp+ß*õBMã
Á\x0007M
wJ\x0003§JEÑbGVb\x0000·Ù\x000czz7XQ$r¢cHÎ5Ú­¬ì\x0014Ýçp}ëgq\x001cýñ\x0015X&\x0008QY7¶×m5\x000c#¼¦á5Ó¼Ìn¨Ck\x0011·
­½J^ÛòÎ\x001b³?·®ù¨ö:}Üâþ\x00154ê\x0010SÂoh¾\x001aw¦®ö#ðº×Móâ
AâJ&Å5Ò ±"®´+sy8®U
®UÓ¸¨nCËk¢9£1h-\x0019xGtð``Õ75Þ0wÉo\ç¥`f\x0015Ê´]¼SÉd}Þìõãöåéùáä|_ë«Á &U\x0006h\x0006%(²¼²W8­Q¯®±µnGÿ+ú\x0006ÔÏTS  yÓ@C""i7§i´*ù¤JOFß6Ï\x001bÒVùÜ|¤%-;1Ì	R×¬©[S£R	\x00106?xU&\x001fXA@¸¤>}ýÕ»<^¹²M»||z 
«O{êÌ5ª}kKUÜò4\x00172$It³°kÖësª³ºÜQly«JäÈ\x000brW\x0015hÔ7(\x0015É$25ÓSà£ª\x000bp½.ìãÓ¯\x000fO¿?~Þ[Í\x0014<OõÆAJ"ç`QÛ"
¢Ó.©#
\x001f¯¯nÎ¯?^|ØQÑyuÃ«çy\x0005íÞÈëSª\x000b«¯Ê\hÀwE\x000fá\x0015)ÅUmhcd³#"ðõßîöFÀ\x001c6¯R\x0006Á\x0001·\x0000zP3\x0008;\x0003×WïÏ®wÅÀ\x0008\x0015ZTB¦T!j´º¤?æÕ×mØ^s8jF@Ôõ<Â¨q)9Ïå9àyòqbGû\x0010Ò\0´2µñâ^\x000b+ÝÜÜ?==î­\x000f\x0005'Kæ\x0018¼ãz1/¸fÈíKÇß]__ì,\x0013\x0015ë¥ìÂ´\x0005C¼Ú\x0004?xÏq^sÌîh¸¾]Ýéå5ÀE9ñ:cÝZoØérý¼ñ9Þª¿6ò®.ç`^O\x00131#¯+ö^áü¦ÝåNûy-¬Å\x00140IÝÃn\x001e~ùòùóÞ²<_¤°·äeRi89´aGàîæüÝÕ\x000f»:\x0002 ®SÂ\x0014(F\x0018IRÔ\x0012Ubj½k\x000bìÅ\x0014éG¥)"ì\x001b×\x001a­ßîÚc²¢ùäq\x0013)8£Øérý\x001cÚfÝÜ½?{»ÃbÙ5 B®{\x0004\x0007Q:Á³tP/\x0014"%\x001fÿ¾óp²YJ5³øð&ó\x001f\\x001c§x
G´¹»
°\x000f¢¬¤RÝ×\x000c¥æê&sM¨úZqVÞún(ï0¥k(Ý\x0014¥awJÅw\x0001Í²\cÝ¢¥Ì\x0019ºêÊ\x000f]É=*ìík×ö^Ó¨J\x001c\C\x0016â(wèg5Ô¨³·ËÛËUì²tr\x0006Òð¸@üô¤>\x0010·{àÌA×Ç?N©\x001bJ=A\x0017Ðj-iR\x0008³1ngNö JßPú)JÅrô&\x001awO¾`qÛc?û)ZK\x0012¤TTKù¯û"X_gY$q!þß*\x0016XÚQd}sòó»}u08B®ÕY\x001eH	@å\x001fxÐª×¨\x0019Ç4-¦\x0019Ç\x001ea\x0011&Â2¶\x0005V\x0008Ûiö0ª\x0006¨\x0002hðâþyÿåóóCnTøòéÓ>/\x0003(aEë\x0008Ý,ÁÐU«¾¿úp{»\x0014®./w5S¤Ði-Á ³Ö\x0018¢Ö¥ö3XÃ\x0013_5\x000eÎrDJ­{lcªz\x0014Ç\x0014þ:\x0018$½/\x0002
àÄØáJ\x000b.ç3J\x0008-!\x0013\x001a\x000c\x0014ßiEèu¸ÓFXhM­McñÕËnZðc¨Åvýª9\x0018Q§çC¨jUà
v\x00072áÃÉåýËß\x001f\x001fö&Ò%P4\x001cÇKçË\x0010åy}No[D|æÜýóÅù\x001cº^:hz:\x000cCZÇ\x001d=ÞQp\x0011µ|%mÛ\x0007SV\x000fG¤\x000cfR	ÉÝ<\x0001+gó5£e\x0019\x0011ÚMª\x001d¥T\x001eH¤Ä_Ç)µçñ¨PI÷\x0011ÅÛ.8YÕú &Þ¯Ã\x001eH·Ä\x0004CË«i´.CkÃºk1\x0019d\x0019äÌjR\x00161m\x000esêPnm×e\x00060­ZÈ¢û·Ú¹üýãO¿>|Ú÷ôÖ1^\x0014HFG­((Ñå\x0012\x000837¿¿xûÝùå\x001eÎª\x00025r:5Áé£¯KOFo&ËÄË=µ.f<LY÷Ål*ïXNCÝ¥i(µTÄ©8\x0018ßHV>¥%r|=ã
äy8µdõà ÈÑv:Jã ª]Q5³¢^\x0001k${\x000c\x0015À-aËM9À©¡áÔ0ÅiËM\x0014Ä©¦õ\K\x0017Ë?|%rjIät3\x001a#ªäFq\x0016pô~dL¹ø¸K×bº)L\x0007<ÐØG\x0013å©\x000bN²j9¨o÷§ÚÿXP×\x0008z´ò\x0018\x000eý\x0018ßf÷¿P)÷ÃçÇ¯{K1×Â\x0003é£÷vI½æû]ôñ,|¡½£jîó\x000fw\x00177»Ë¤\x0013¬j`Õ\x0002Xòâ\x0016Ù&Zî-t]âm\x0016\x001aZ¥Õ¥ï\x0000K$Uv½Ñ,´åº\x0019
S´UHç$Ñ\x001c­b\x0017ÊE³å	
z­°]Aï\x0014lÝE¦`Ar\x0002\x000eÛÎ\x0000h#@¡íÊ´æhUC«&i¥ONH+-÷\x0019ÇË·­éZã\x0006iMzßÉª¨,¾J\Eûròñqoº]p¬\x0012\x000cßW²}\x0015Î»\x0017»Ê\x001bTªÇ¨¤¢ORQ\x001f?ÝÿD²\x0012?½üë>}Â¤©\x0005dI¼'uÆ¬pÔêûxyö$%ÞÞýe:¡Z³Sq/%;\x0001s¹ùù/\x001e÷Ti\x000b¿¶ÇF3ZEÏ{Sênê&Ab©ùù»Ë\x001dÕb±ÖPô¨¡!ß½|}¾ÿ+þÏÇÝåBÚXÍÝ(fçè¸³/ûªâÌøîîæöì{ü\x0017çÛ2eÝN\x001e)Å«Ã´¹$ z0\x0019\x001cçÄ_üëÉíã§O\x000f/öÄµ\x0005æ×ò±\x0001\x0003\x0014[òì>Eð®\x0006¿÷ÍÉíÅååùÝåöM¡f\x000c\x0013Öó\x000eL®pM¦@vyaÈª1Bb
ã0e¼1©#\x001bö4e¤´e²³ßò½G(]CéfÖR°Â'ÄKÔê<78×ÅéÆ!}\x0003égRò° ¬I°¼¾¾k~\x001a¦¬t #¥\x0012s\x001f\\x0013%p¯+~ð²Ó1\x000c)\x001bH9\x0001i,·4@äå©ò~\x0005ÙÕPSªRÍ,%°h*\x0000µez\x0012¤Ýv5\x000e@6RÍÊxª)\x0008`é\x0002÷Á)[¾÷úx2_;Õ\x0007×NóÁ¿¿ÿü|ÿø´/m¥MH¡ÎôÎ°9+\x0014Í¼¡\x0001îñUÔ;B\x0005óû³\x000f·g\x0017»FÀeÎª\x0005\x0000\x0003èn\x0013iÈ\x000b6ìWº¢S\x0018ÿ¹\x0017<)å\x000f÷k\x000bz?A½\x0014ª¬¨#Ô"Jâ¾ó¨*ÂèÊ»\x001e!\x001f¢çgÊÁ¼Ü?ý¼{x{r0½æp·äÂ³ÍËy{K)»³ëo÷!\x00061L Æå3ù\x0008EG\x0005úWU\x001esÀ\x000b)«æªHiü\x0004%ÉVÚ\x0007ÊÁÄcÃj©ñ,ÍCÚÔ\x001b
Õ\x001d)Þ@\x0003N_öíJø\x001aSäª\x0012G\x0004ÅeÇ²ªZa¦¢Ó»\x0007(qVYÈ©Å\x000c'&\x000büêIAJ\x000bV²¨xè£4\x00032}ôª7¾§°¦l#ÍÃÿ¸Ç)OßÇÇîýÓ¾W\x001a\x001a!	 \x0017\x001dx_çR\x0017·½KXÓ¬müó?á'ìh?»Þ5	0U\x001eW>gÎSg©1üEÖÔ\x0002zÿHS¨×\x0017y\x001a»"µÝn\x00016\x0014abg\x000c	âã°·òFê¼yìÐb\x0005ØR³¥ÅP\x001e±kèm\x001c	»
!6FÈ¦±(\x0011HÐ<iK\x0018SÄó]7Ï{\x0016»J2#6&g±½\x0013%²\x0003"w\á¸XÇ\x000eMèd\x000eg±U5Ú*bã¯óØÑG´ÚÊ±BW\b\x001eyÚ\x000f\x0000¤®õ[âßô[f©1")(8)|ûât\x0000ê(|×Þ6íÅÆ_ç±dl\x001b\x000cËò{¡9\x0015`»¬Ú,¶¶ÙÆ_§±­4ÉV#66ãä$-É@Ñy\x001aóÔ¾¥öK¨eJ³\x0011µ`jÉþ°éF\x000eOcûfkã¯ÓØÆ\x0017çÓFÞS6+õÛ¸YÖ\x001d¦Yl'\x001b«r%³ØêÓLô¿òT(ËÒ\x0010\x000cbíé	âMCü-\x0016Èü·ã\x0005òÿíÅÄ¥ä\x00065­NÉ÷­Õ\x0017\x0005ø[¬=ù6þ%'{P­«Q­B\x0015Ö<¼Ñ¤õ(´EÜ½+Á\x0018GÃUmlÜÁ¬:ÄýÊ9YP$/%T­ÔÛ¯À\x0001VÓ²9VÔI\x0018ëì¤\x0016fÕ\x001f»TUz\x0014!õ\x00018Ìè½'§Y\x0000F
]FvÕ´¬«j\x00145\x001cxÈ
;êØ½7]èi\x0014t³Wñ×\x0019Rç}y\x0016/3¾DxÔ»4Ý\x0000¤qVSÅ\x001c#k@`e\x0011°TÓ\x0006Ü!áW\x0015ÔÇ°\x0001\x0016Ý¿Î°jÅíüÆcQV\x000eBqóUª@­<IDm<É\x0001ÔàN\x001d\x0005Ìb-ÏB\x0019ñ5Ú
\x001e\x001agõº9Xøë\x000c+ >)½åÊn:\x0008Ô\x0000cgfûËyÕµ¬SWVÜ\x0001EFÝúÇAV`\x0007¦¯\x0003\x001fFÒ7»5ý>Ã*ð"}òøÐ4:EBié\x0013Æak©\x0014MZ)ã°Ñ)\x0011¿ÀæUH(\x0003|Wó4\x0001[¹à	¶ñÁÇ`©cWG£EõÂR jß±0\x000ekd\x000bNÁ\x0004¬\x0007ÉÞ@ü/îá\x000f:pg¼Þþ0;\x0018Ö5/KL]]àB4`^Dh¼/OýÜ	XÕ®,þ>\x0005+KGðÀ\x0012¡Î³x±é;c'`«Éé	6Ø)X\x001b\x0002º\x0011Dô_t^YgtëjÜÇa½ln¯ôûÔÊàÊW\x0018VHà)EZw\x0012/\x0013°­\x0007~[YÁãÂªõØiîÿÞ#ÀBû8ÄßçVVQIL4³¥çÜ\x000bVÞÔÐé\x0004OÀê5X=	+-iYkL­érÞ0¬èJ'`ÍÚ60Û\x0000[¥³R°\x001bíà\x001a\x0019-»ò÷qØ Ú\x0003¿OÁÆ\x0017ÍéÆi;ß\x000c\x000f¾¾c\x0002\x0016ZÓ¿OÁbH#³*Ç\x000bk¹\x0011Yê×Pç®\x0004«$Uï¥·­%±2K\x001aL7\x0001y\x0002¶}&¦ß§\x0000
\x0015i|Ïä@³³\\x0004F,Þ°JúfaÓï3¬ÆÙ\x0014/¬X_,,¾Ñõ¥v$|\x000e6¬~Ú\x0005X¦KjjøfÌ°¨Bjj
\x0016Û-¥­n`ñ÷)XaÈóÖ\x00104÷¶ZI
\x001dÄ1`}\x001bI÷÷\x000cl\x000b¦\x0001&©Å\x0015ûÀ\x0013©÷Ý\x0010Õ\x0019R¿F:¹a½¦\x0006M
¨ùý-\x000c\x001c\x0010¬ëZìÇa}ûúJ¿Ï.EÍÃZ`õ>Éÿ\x0019ï.Lû-~*âÌ\x0006\x0016zÐD¿%·\x001b_Ï\x000e@jñOm\x0003÷\x0003*¬Vw\x0017ÎâpÕÝõõäÝËÃçÇÝe\x0017
G\x0019å÷7ö@ÑøáYó&tíÌysòîîüÃÅIé.yÛÐ0âïI0ªÅá\x0016T|lx|!&Ú·­åAª£é÷AF.+E^çùÎ`8­úòQF½Æ¨§\x0018=e]K##eÈ1[>Ë¨åZrHË69ôé\x001e\x001b?ïÖÆ&gºÀóDÍø©É5\x0011°=ùvyýÃ\x001fvô8ç1Ù®fTnÑ\x0004ª×¸¢ÌÈÉ6¡¶¿Q\x000fDÔ
¢@Ä¬é\x001aß¦i41"r\x0013IÕö\x000b\x0019CÃ\x0018Æ\x0019£¹É	£·ä«¦BD\x001dv\x0010\x001cÄ(ë	j¸\x001dñ÷AJýÂ9ª\x0015¶\x0011æêm\x000b¤{§ßÄ>²ütÓÅ0¥Ã«1C\x0016Az\x001f/FO×¸\xj¤\x0014k'[\x000cmurÒP¯`¤4)E×44L©Ö(Õ\x0004¥¥\x001cj\K\x001ei-©\x000e1®e70s\x0012Ö(á5®¥Z[K5³YÓ¾Ìî¥_¹Â©Lm\x0016r½3\Sg81¾ àþê+/Oih
qh'f_söAl+ã¼C¼]Õ\x0012Ï\x0004]óá¯c|8\x0004YyR_TteÇû'º9Øö8\x000cÐV¾9Ö2W®ùyà\x0001òÅM²«EÄôS\x0006ñT§\x0006ñt\x0008Üñ\x000b¨sNH8O2óméÐ\x0003\x0001«!ò\x0008èÂ0`)ÙP y\x0010á\x0016&Ûkï\x000fñ9Õ\x001c\x0010üu/~U*ËVøTÈ±"]¦±Û~ÌõÁY¾¼RÆñoªÖ\x000bjûúüðøôð\x001c\J©½1R·\x001a0h(\x0004'XÄn³Üw8²íæöüâúüöäÛø7mweèª¶\x000fû{ì4´VÁÓ@\x0003Ì\x001eæ
¥
FI³Å\x0007\x001aEªYg©æ\x0017ZGÏL°1§le \x0019íVn\x0019\x000c3nA/aæ7d« >% \x0008ÔtíN³Ôuû¿ÏÓg·tp<E"iÆ\x0007ZjÍE2ql=}ÔÕ°q¤ö°\x001a,Ë~y\x0010«\x000e£RÛå·ÕJSÚ, \x0016«\x0006\x0014\x0019ÊLwËjeÒm\x000b1R+Ý¬µÒ\x000bÖÚc\x0014­5\x000eýe\x000f\x001bñÝ¶ÊÏaèZ'"B\x001bµ\x0000ÚÈt\x0002SM¥§:Å<\åë¶\x0004õ©}c©ñ×i\x0013bâ+\x0015h\x00083\x0000"\x0008®\x0002Ð	rLS:,Xk¥Jõ¢\x0004\ÄÐ9ïm¡QjßRû%ÔF\x0019îNõº\x0014êG¿5ùd§+3I\x001ddsÉà¯ÓÔÑ-bâ\x0004Tä
\x0017M$l\x000e<\x0012µo©\x0017øM:^24¯*®oqAUQìëu\x0013f©uc®^`®µÍq­´C\x0003ìFÊÕ\x000e9\x0016µmö5þ:O
Àº
Þ:'íV2d[#CÐmìË·±¯ajzÐ
ñ4\x0000]ø"F×éÏb»5l·\x0004{ÕZåQYyfE\íp\x001cÓ'å\x001a¶\æíÐîJrw¶>Ò;Fª:^\x0002)\x0017`ÇKTÖp\x001e\x0013)$+h\x00127É¶æaì°\x001d`\x000bKcCÈøÉ ×§´Ø ×^3Kn\x001aIPº'òP\x001a=Ü.ølßøû<5\x0018^k
\x001cñ¢hoÁ¶xà0µ_£öK¨iÌ\x0004V¥Ñ,\x0019GT£¾­ÖsYËöÝ¨å£ð\x001f(Eg\x0000¾huÍµ°Y\x0010W\x0000#â©aPÐ\x000b\x000c\x00058Ïft\x001e\x0007ÛØ\x0016ÛÌ¿\x000bPÜG¥áü@2DeiïRÎb·Hú}~[Ç%&ATÌhü0ß\x0007jlí\x001dÆ^;fÉiD
 Jb#vêÆBy\x001d[fªl«`\x001cÅ¶k\x0006Û.1Ø8Ç³&ÇÏcm\x0018ao-p\x001fÇ¶kØKö¶²Üä@âUgëmKu\x000fCC\x001b~²° &"*k\x001d_¿4O<zÀ¼E`[rl\x0018Û¬m\x0011³dà\x001bYºK\x001cíì 9\x0019%\x0014¢Ö©\x0016Û-\x0008æ t\x0018_ÿ?UÄ'óÇ%\x001bÞ\x001d\x000bÛËµh\àeÇ\x0017Ñ©#\x001d>U\x0006z\x0008\x0008ELl[{Ì06´îj]\x0015?±·\x0003·#Çÿ\x0008y¤\x0014b«Ò(Ó
Ä\x000e¦]mü}ç§J\x001eS\x0001\x0017¦½\x0019ÛØã\x0004²ep­ù\x000bnù²Ì+Qø\'lSÒòH1a\x0019|ëý\x0005¿Àûøð¥¤<|Z8WæÌmkª\x001bÄVª=é÷ù÷º]¶V*"f[£õ0v\x0010-vX°ÚZÊ²Úèkç'¤<)ÕíIð1lÝ&ÄÒï\x000bBQE$j\x00136ð¨2F{\x001clÓZôû|dÙÂY\x0016	3À\x001bÛ¨#%\x000e\x0014\x0016E¶ÌK¢Ù2P©XÇ¥nÜuJÏÇÁ¶mh$ý>PÎ\x0013÷ßhr\x001f©OÄqïEØ¦Ò1íê¢Ìíª²ÌñÕ0*,\x000cj%à"JËÛÖñ8
mvÉÁ»ÆXÅ\x001e\x001b5\x001d×â\x0013µî\x0006ìSK±V½ E®^xy`ùï³'\x001còs¿Gë\x0012\x0015ÙÊÌ$ENñÚ)2\x0003\x0018iX£½Ë]'g×8ãçlV_¦ô
¥¢ÔÒ
Zf	à\x0017®ö³;vÕä»\x0008ï& uþQ\"fG
UºÓZ\x001e¤¬Õe$«Ë\x000cc:\x001a1A[)\x000c\x0015ªHÍ\x0003~ ôwÒ´fÒQÞ\x0010\x0015drì\x001c)\x0019r!£2
£23(ÃIa®øþÏ\x000f&J\x0000Eë]áAJÛRÚ9Ê¼\x0017Ó¶4¬{$QD/S¾ípLü!*ßQÚ7(ßþzÿÛïÈúþþó/\x000f{0\x0001ë§\x0004g\x001d,\x0017}á,\x00026D}\x0013vÄ|ûÝÙû\x0008ûþìÃ»ó½¤ÕdH2¾3¤\x0007£yé¨\x001cI¹l*ôÑïqÒjþa$ÅüÖ\x000c)\x0014i&Ê;\x0013¨à\x0008:\x0000KAëÚ.üøÉ\x001d'µ
¼sÇ~Ç?EDhí\x001cCÿÙkTüu\x0002UbC\x0018iøÅk¦°Ê¬\x001côÝkÃ¨\x0000ªFÅ_gPgw\x0015ãðóJ2ªì{×ÆQMjæP#\x0010Ç'ã®\x0015RJÀ¡¾à;\x0017u\x00085×¨V\x000e\x0003ì0½ ìóÃýî\x0001\x001f ¬N\x0005,TÃM!T_\x0002M:l:÷(\x0011ýÝÙíùÙöÙ\x001e\x0019®vAüÊ\x00059\x0014N\x0001k\x00054¸Ï\x0007\x000cCáÚM\x000bx0]ð5]ðt°\x001aEèL\x0008¨^ö@º4ð»Ê^ÅkXU>æ}\x0004|ø|ÿ¸§ÉzË5a\x001e4¬®Ròl¢\x001bqÊ·äYd<ÿpv±½Å!3Öª­!7Z
2:Hæ&ç\x00023 <E*ô\x001a[U\x000fF\x00044r\x001cÐL\x0014¶z\x0012¢µ\x0005Q/F4
¢\x0019G4ÅgÃÎ~k[a\x001a´é1ºÑÍ0\x0016Á'g\x0004\x0007t\´óí³¾^×^O0\x001a\x0016WuVr$Ä"\x0011¹¡eQVZô\x0011\x001d?0Ü¶d¼ mw<Ô,\+m/æ1\x0008é]\x0003\x0001aË£ãMB$\x0012Ø=\x0017¬ÿ0ch\x0019',7lypx-\x001d ¸"Höri\x00073Bn8®fd\x001a\x0010Y=tÎúòi\x000f¡\x0008EÇ\x001auÇ¨$E(Å#Üö8ÆùÛ«Ë}|J×|J\x000fóÅ\x0015tÌç©¶ Ä·r\x0016Õ×Á\x001eÈÇéUÒ\x000cæÕ|¿ýþåéyÏ(8\x0007­Þ£w¢PåDwC\x0015Wï?^]ßî`LC\x001bª4< ´}q!þôååi7\<¨§<ûG(¢sÈÕñÝ`oò\x001eþtuw½Ê7T~J\x0017ûâ\x0003cBòÍ\x001fõ ®ªá+r)9Âålé\x0010#Q¢ºK\x001c\x001a2Íe\x001a.3Ä%¹\x000f¹Ò¬näâbð\\x00008Ëå\x001a.7Â\x0003ç pIZ/Y^¸BÃ\x0015¸TÑ*
F°K,®-Û~«ÖGÑo\x0000F¸L ¦åÄåKØÞë\x0016oþ\x0010®f½`h½ÌªàVä\x0007\x001aæÙ\x0003cm\x000c\x001a\x001e\x0004UE(cG  \x000c-öÂn\x0013_>"ô©\x0007sUoÆÈU½\x0019\x000fàR¦4Ò¡s5P5ºpÍDß\x0018/?d¼âË\x0001È³D]a\x001eìZÂkª/ú9K¯\x001b{Ý\x0018ûËû¿~yÜMêz¨SAÇ7"h.¡ü°7ÛãåÙ÷W\x0017ûØ¨Ù\x0018d³Üû¡AP
Ö.\x0016¶¾Áp­î÷ûÃ\x000c²¹Sª+\x0012Ô±fP\x0016ýÚ¯CÉBC\x0016FÉ²K\x0016\x000cåéªrO¯6\x0006ò\x000e\x0005«+Ê¢ÉÐc`ñ%@#É RBæ$\x000fwS}NÍ5lnx«\x0019IMïiÝ\x0000
Û\x000fj\x000fjF?h)\x0001ïò¤&dS|\x000cäÆ÷¡lUú@ë>8Ü|¬ô\x0015xÍ¸þ(ô½Ö\x0003\¾áò£\æ!:hG\x00161ì
Ú\x0019\x0007±	Xó3â\x0003¼ø\x0019i$ùW\x000c
ïÉ_IWÆpjGÛ
DÊýeÛ°Äaä7\x0018\x0016Þ\x001e\x0015&BÛ\x0010ÚqBÉÕ\x0008Òµ\x001f¼Ûº\x001a ¬®ùH¸ÊN\x001fJ¨¢Ý¥\x001c Á"§Ü~®U1u¾ïD\x001a$lÖÐ
¯¡Âx¡§ÙÀìZë2q³1>Ð7kèÇ×PVkèØ_Ò`Ù$û°ñ\x0008\x001fL(eC(å8¢Îsæóì Öà/{®M\x0017ó:aÕ
ïÑ«^=\x001aÞù|ÿõùáé0\x0008©ÌÒë)d(Wî\x0016KóþêÃÙÍíùõ\x000e\x0019¡Ìç\x001a>7Î§¹ñ\x0017<é4  r,$4
¡ \x0004N?\x000b'ÇÂ{¶Ö}må\x0018¡k\x0008Ý8¡+¹\°<¾=`Óðv©C	KòÊØÄ\x0005T«×ØÇ§·¾<ï>&É\x001fåú|ÅbQ
ÂnSswòñúüäíåÕí\x001e<hð`\x0018\x000fÅ¶,á\x0001OSQF:ü¾l¯
¬c¡\x0018^>ÍS\x0013pù¢å3+S½Å9Ï4|fÏº&\x0019
UÚs6\x000có\x001ds
\x001bB cò\x0015HD\x0005]n~\x0002Ñ\x0018_³ùÜèæÂñ	ä#gK½·Aôx\x0008Ï7Ëç/z/zµ|`ou	÷2[c|ªáS\x0013|õòYâsò8|µ\x0010ùV>ÂÁØ¿\x0011Jo\x0012Ð\x0007ò@r£ü\x0007\x0003VÓ\x0011\x0010Ü(`ÄpdmÈX>Àª¬^o]\x001f\x0008¨/¿® IïÊ\x0004èÊ\x0016äí\x0008¸9©x0 mWÐ\x000e¯ \x0011Iþ\x0019\x0001SÄ,\x0003\x001aeÙÉÚQ<\x00180´a\x001cÐR÷x\ÌSz-½/áÃèêù{è\x001c\x00083L§>¤pIÆ:ó­ÜI>±.­,HZ9â}|züüÓãï÷{ò:^®GôZæ:\x0015ÊYÎÒ¾I/â}¼¾øðöâãÙ<b¢«g':;ç,K»'"ÊXH(C6ñ;/À«æ5#A<L\¬
\x0002À\x0013,ÃÞ{ý\x0011¼*wx¼8\x0018\x000f¿(ä%y~ÑÆQj£q>\x0018O·«§GW\x000fx@NÂSðÊ\x0018tÕ÷Ç\x000fá¹\x0016Ïâ©¤LËIâ<Tðä\x0016Ä[´zU#âqãÁxJ%Ù9¿.¼/{oãÃíp<ßâùA<éWGCÑû'JÑÑ"»RG°$Nl\x001b¤#
1ýÔfÝ\x000eé!6Ó²Q6Í+çpÂ¬'<Å+'{é¾\x0011<ß.\x001f\:\x001bXå>âå2\x001eÄ+
3ª×p\x001c¢k¯3?x!\x001d×ã\öéøÐÊ±ÓÃñÚoë\x0007¿-\x000eW,Ï#hZhÄ\x0005oc>á`¼Ð~Û0ümÅª@@R=6p\x0017Úû"\x000cÞ\x00178\x0004P\x0012÷¤/\x001bñ¦¥\v_öÛÑoÍy¬\x0018eO¹¦È\x0016:½äÓÖ£J#£6>~È
u^Ó;\x0008kRøºØXÍp8\x001d´t£Ö:j"3Î¬Èt¥x ×¢\x001c¢s-Ý '`-Së<¥°n¦Ì$wKl¡Å\x001btó,Ê#q³Í£z°|ÆðÎ\x0013½ôÃ\x0008j\x001c4'z\x000cÏpü\x0011¿-W¢%z!¼vëúð©ò·¡÷·\x0014+ñ1±±Òáp<ßâ
úQV\x0007iÅ½GÉÀPªWDß³<D×n=5ºõ´ç4sºTHqó§Ü\x0018:\x0018\x000e\x001a_@Á¨/ -;ðØ\x0004¦©òÇr.ú\x0001CxíÆÑ§UÊX%< *ÁWP76Ø\x001cN§[:=J'x¤µs¢*Á«É[d¡µÈ0jÁº²t@_Ö­Xv×êvãéÑ\x0007¥w
O\x0005ÐuPn³^½\x0008¯5ÈzÔ «Àa\x00014È4\x0006>X¿2È¾­6-Þ¨\x001f\x0015ñ¨,\x000e
²ÔWJ¯a9×n½Ñ°\x0000Ö9
Wð\x001cã©r_,2Èº½.ôèu¡
Û\x0017\x0014Rp¥8t<ö\x0008iM\x00195yÒrÍ\x0003\x001a\x0015Eµ«F¹ãÜf¶=\x0018vô`ê!ËÎÓ¡rckûáx¶Å\x001b\x000cZ¡JSsÄ\x00139×\x0012;ïåæöÛñÚ\x001a©\x0018\x001c©S¶\x001eÐâ\Ñ-Úz®õTÜ §b|(½ëª3\x0001åÒË±]äÂ·A\x00155\x001cT\x0011¬¨\x0013\x0017\x000fH6\x0005?mùèex­3à\x0007\x0001ã
\x000bfWÎ,aEhí¡ðÂxÚû	Î\x0014ò(l­1ö£ÆX\x0014Ý2üª¿j1w)&=×ÆSÔh<\x0005§R;S¼(AUöïÆÐ~Ù0úeÑuÒ+7%X¿j¿ØØµz(\x001dÆÇ\x00031èã\x0019k¸HÓYÏæÎW
Þ1\x0008hñF¿­-s2\x0000F`¼âãm¬Ð<\x001cÏµxN7ço+OÉ\x0017®ì¼%I\x0007Óµ±2\x0018\x0019ãR_
\x0005TÈò®|Û%F\x0005Ú-fl&³,_VÒ]Å¢zíµ!ºöÃÊYÙ\x0014ë¸;[ZðÉ½ä\x001e\x0003Õ~X5üaEQ<@' \x001bdoÃ*Ì¸hßµ2\x0018\x0019¬·uåÝ³Ý\x0011o\x0015ÚØ7x8^kSF#eF\x0007ÖTIÃPéX¬òfbQ\x000c\x0019T»õÔèÖÓª<kíêãU¸g\x0007Ðî=\x0018Ý{\x0007ZÑm\x001bèdU¸gÑÛ\x0007Úh\x0014F£\x000cSº/¬&}´HW\x001ebcWÄátº¥\x001bu@AsP2z¹\x0006Éëp
èöÛêÑo«òÇ½î\x0011\x000f\x0013-\x0003Ý®\x001e]=eSé áQ
U\x0010Ù-òUÚ\x000f\x0006|âó?½ÇÒÞ\x0003rá½f\x0017^eF¹÷Àh¼ÇhÃ
ÕhV\x001c[½U$tM6íÎ3Ã;OòPtCù`Àn£xÜáx­U\x0019
øü?­iÏ\x0019>\x0017#\x0016¨$@®\x0014£ñ±X¶v¡¥\x001bXüc×Î¶\x001bÏNl¼àÚÙÖ¤Ø×eRÚ@\x001e\x0006òþÁk×Æñ`4\x0017/Õ\x0012¤ÅÖ|¹\x0010üqm \x000fF\x0003yÚ³³ÁòK
9o|\x0011.[äGµ%40ZB£ãËV@¹.<ã0(þ»æñtû´Õ£O[ÄAcaQgÔ\x0010fµÉN²VEÖjÐ"kmÓ¥ë³ìRÄ+ÀaÒ\x000bðZ\x001f^úðÿèÕ3ÕÓfÐêip%è£³¨,â)[Äè\x0016å¦?üøøµF»\x001aÿd¬â\ñóñEä¹à¼ÄDÍlèÇ¥¶Üê\x0011\x0019ÿó«F?íæþÏ\x000fÏû«,N\x0004§E,\x001eUÐÔQ\x0015\x001fãÅ¡8ÙÍÙ»\x000fç·;«2d_ÆÔÛZ\x001c&Õ¸,ËkÙ¬1Di\x001aJ3³%\x001b	«<¸.¦ÚmVv\x0018²ùÞRN}ð@\x001fÜÆóíèóp¥ÍB±c¡e\x000c3ßÛq	\x001aÖÜpvÍVìÐOµ\x001dÅTÍ®jj[ºS\x0012\x0008\x0006È£ã\x0012%/¦Ûh¾(«\x00049Rj?Na@\x0012÷ÃÅä÷°UE\x001cØ,Þ¾ýæ~âcTÿpòËs5®ÌmÖ?\x0014S­Ë\x0019{©KK=>ðGw¡H-ë\x0011é!Ìv5ÕÌjjk¹\x0000ã¬YÚØÂæò6k­,¦Õo`e1o\x001f\x001e¿~}ø×§}\x000b9ç\x0018¡çZDi\x0010ÚVÕàÛóó¿\ïP\ DÛ ÚqD§9P¯dFÔ«×ÁF\x001fc\x0004±
ÆáðF1±²\x0016\x0006ê{Z½\x00106ö´ VÒÆ\x0011±6>\x00181\x0014Ù\x0005*ÇèTa\ú¡Mó¡ÍÄÆæ\x0013"TYG6\x0011²\x001b´EæpBÛ|g;ñ)OÁèkFä\x0019Í)ï´Q7z\x0011ö¢¯é\;.YÝÊbx\x0019c<q5#þ:\x000c\x0001b
hÁ3=\x000coÜ<Ùa\x0004R¶r\x001cRázY\x0003SÚÚ{Fl\x0016ò\x001b\x000c-d\x0018\x000cRñ¯\x0007ê§\x0005ÅéYáäÂ-YWEGÈR\x0015=\x0002i$+n`"/Ð&ôÆiO.5u\x0005-Bê	ÈhtÜªÀBæÃ
¥<:\x001eî-nÅÁ¦ùÜÊL|nWå\x001c\x0015\x000f
E¡ÞoLw0úÑ\x000f3ø\x000fa\x0015'þ\x001a83\x0015	\x0017lå¡%qBåXe\x000f+}D>4(¿ÊáÆê·!HÓB\x000e»fi\x0019©dÅãXD^IÇ±-\x00031\x0006 [ó£ÆÍ\x0011Ò\x001e4ËN®Ô\!\x001a¿öÍ¡u\x001eýÇêÁp0£Q\x001c_ÏÏuå?n\x000e!ú\x0016Ñ#b\x0012|\x001f\x0008\x0014FüÙ0\x001dæ[j!È<æ7]5pJGÛ\x0014i±E x\x0004Rµjâc»ªf9\x0013
à UØµ\x001f"Ô-á°fåï2cÏ`?\x001f'\x0013\x0016ú\x0014°öà\x001aqÅ5\x000c%(î\x001d\x0005¨"äêU¸±é@È\x0014É­!ã?µ\Ö_On¾<~=ùæáé§Ç= \x0010ÍK\x0019h¤m~¾¢\x001c«=Å7í6ÑÅÛë«oÎ¯ß__ìÇu5®Åu®!z½<é\x001b7\x0004án^ÖQZÙÐÊyÜ\£\x000by
2Ó±ä5åGhÓ(ª3+úÓÞÒ÷\x000fN®qx)\x0006\vÃjc Q<-Ï"×@¨vs\x0013Ê·w'ß__\\ãÔR\x000c¸ì!­ßaõ~\x001c$ ¹Bbq\x0005çÁ¡.Ç­D!l5Åg\x0014\x0016\x0005g²½(\x0016'Ð¦hcñï9\x0002mUø\x001ei½¤ÅÁÖ³<'°ôz\ÛmêC´R¨\x0016\\à%¸m} Å¥¼|ÄÝ&8+­ åì^xµò^P¹d/â*Ò	{aÞþ\x0018m%´:æ\x0018­4¬ä$m\x0016TÄUÛ£»²E\x0007k\x000c·~\x001dGÜò:\x001eÆõ\x001cÔF\x0001¯`\x0008×³
\x0013Û\x000bÇpM»\x0017Ìì^@\x0005 ¢5,Ê³LØ\x001cª\x001bfmwÜ	*zý\x0010ÊÒjÍY6Âæ7Ê(­m7Ü\x0008HK\x0001øHÉ\x001aZHËÊùfÃ¬ó)Üv#ØÉ Vs¡â\x0003:;´\x0011×Ø+·Ñ\x000eá*Õà*5k\x0003ÇôPÉlâ\x001e*c\x001fÖ¶´³;×*\x001e%\x0012.é]´lpQ¿ñ\x0018´ÐÒÂ,­±,Í\x0019½\x0002\x001e\x0011¦¤åÅUÛ\x0007Çpmã0*;é1âV ¹6ñÑtê%m\x0005\x001eé©Ã6%Û1\×8\x000bøë$.ð\x0005\x0011ÿAeçò,Ü¸\x00176Oë\x001eÄö ÁôAs@)o\x001d§Q
xÆ\x0006¶Ç\x001eÖ¶´Ó\x0007MÓ@¨HërJ\x0019\x0017\x001f(V¹\x000c×ô2[.x#¡¢ýåóýþè¯à\x0013\x0016}-V®Ñ\x0006S\x0004&:À[Ä¡¿¿x÷ál×³<óUíNOQ>%\x0000O\x0005C\x0006À
 6§¼\x000fç³
\x001dæsÔ6\x0011ù<KÉù`\x0019_å\x000cF¾Æ\x0017<O²~Ñ$\x001cM\x0005#Ëúm\x000e\x001dÎ×¬\x001f\x000c¯_äsÖOS­)òQ|
6ëµ\x001dÎ§\x001b>=Ì\x0007<æ3ò©<©)òYÎ}Â÷ßA|¦á3Ã|\x001aHã&òÙò}\x001d§@m\x001d;Ï6|v/Ñ¶8ð:k?I(µÄqÿm}\x001cÄç\x001aûâía	Òhÿ \x000f?F>\x000b	°mHØ|¾áóã|«#_àZ\x0015\x0008Ö\x0006½m²Ô|¡á\x000bã|j\x0003lJÐùeñþøç°èüÖ\x0001x¿a@kÈÉÏsÁ\x0017\x0016\¬\x000bz£RÐ\x0000 k\x0001ÝÌ	&>}Js\ÁY> \x000fç«B5È×j\x000e³b4\x0016§ýq\x0012»\x000c\x001f\x0004ì`\\x0004Ø. \x001c^@à{áp\x0012^"¶\x0003Î\x0017\x0001ªv\x0005Õð
*HUúÄg¼á
0\x001b5y\x0006\x0000Û\x0015Tã+\x0018\x000f\x0006\x0019\x0019\x0017\x00114\x000f±Ý&@ `ëÄÈ	/FPX\x0013\x000b®I6(zY¸\x0006»mÄ¡k^ô°\x001b\x001d}àÊ\x001e?±;Ò\x001elÝ,9îgyC\x0002ñ\x001eÉ¥h\x0006\x00157¾ÃÖÑ¦\x0002ú\x0016Ð\x0002\x0006A¬ø-YéPê2ÏzéE'u{èá\x0004N§ú\x0015\x0001y\x000fêí\x000fº\x0000M\x000bh\x0001K2=bÊøkÉÒ\x000b`Ý²\x0015¬ÔÞ\x0013 \x001a\x0006|ÓyÉm3u£Ánå\x001c×zrÜ\x0015t4\x0015o¸ìM+®(\x0003¿ÌS­'(Ç]A\x001can3 T<
AKV°m
ðaÊ4÷2£÷/Ñ:Ìç³\x0011T¶øÒaú-"Ó$"±2\x0018f{óæöéþ¯\x000fO_¹þí¯÷¿?|Ú×½¥âÓ®Fb\x0007ZhÖ°îÂ^·×gß_ßp)ýÛïÎ>_îèãÊ¸U}LÄÅòWÎ+\x001b^9Í+~½·,÷«M)êÚº&qÝ\x0000óÛAp\x00056Îg[TõLwuOòú×ÏòJO\x0011ÈëéÅ%°4xm|ãÕÍöÕÓÛ7Ú*ÉëkYµPëÀÝÄ¦«úã5
¯æ\x0015ÔO \x000f%<Ô´(gé®>a×5ÇÍÍ\x001e7é
gtpÆ\x000bcS\x0019[ãl\x0007§\x001b\=ë¸S1\x0019³L+0®öÇ¡õ
­¦µg\x0013â\x0015³ \x000boWÖ;Ê«\x0012o¥¨¦\\x001aµÎûôåño{R\x000e^°Îº7ËçAX
ºôÓ:ìõÕÅ?í!­¦µFR\x001cW1Aj
%GhóçlÃT?Ë}44¤aT'AÎÔêmOSóáRûï²½R­}{5ùõ-v ¾ð4}}lÛ$ÖNë`VóÃÿMË¿ÿë,±º2þý¾G§z7çs¦Ñ\x0000(\x0015\x0016aâ3&¾RË\x0010¶@\x001a\x001cßyÊc\x001cêM$ù\x00109"ÓÏnÞ<~þéËçÏ/\x000få_¬ýÝZ`ô/ÿÜó×+:jL³x
VùãÌâô×dfÚ¿þ§ûï¿>?uýßÿå\x0017õ^ûëïOn_\x001e?=þÇÿN£7BHA\x0005¤ÑIö8?ÈD~Ë#w¦8;¹½»¸¼H£~ÿ\x0005`´ñU©kþ7«`J´iÏ\x000f÷/Û?Jpys4³\x0010ò\x0010\x0010¡Br\x001dpYIÉ*""ß<\x001a°Ûó³»­_§@©\x001aJ\x001d\x000c\x00157Hö\x000fdäá\ûS¿Äg+BÉ¤3\x000b\x00055\x0014¼\x0012(]CéW\x0002ek(ûÿ\x0016êÇø·5+õÀ8P:ö\x001f\x001f\x001fO.¿üòøõëÏÛ¸ðôå&Fu.Ü\x0014à<q¹\x0010lLÀÇóÛÛË«w\x001777W\x001f¶AõCxÖáoáèm¢\x001d0d¾â$ÍdÈkV\x0011æþåoÈ\x0012,*à\x0012)3è\x0013á°^*¡à´\x000cQÎîþ)ÜàØÌ-\x0000úßý×ðë§Ú\x0012yÆ"üß\x001e>?ãUñíÃ×Ç§ûÑ,9Jh´Wß<=~útÿ9ZöÈ\x0004
S\x001a{"½ÔzaÐ\x0002 \x0008!B)ks8ë,^\x0017\x0017g\x001f>¿¹¼ºÅbü÷ç\x001fnñ¾øöüæâúìÛó-±Aö@Í£\x001a¯ãhº3ªöJ-AGBV\x0002æQ!\x0003DT\x0005îT\x0005&ÍSD\x001a?'UÙ\x0005¤ñ×qFÅp\B
y4äP£
0ó¨"§ð"jE¢T!\x0004ÚªNc~ÿhûì4*ê\x0001éêqú\&¥êdÖÝ9\x0012hüg¹iPår\x000bz´ÔãÃ&£úc~þ¸ëý4ª§\x001e\x00085`1¡Zí\x00185\x000fß:\x0012j|&iTAÙú
&£¦\)¡\x001eñüc\x0003:þ÷,«È\x0019¡Ì\x001aß\x000b
£7ØXñ®½¬âª¥I	5\x0005Á\x0013ªòªlÖ#\x001a\x0000¼LäìePS90\x001a«ÔY]1VY\x0016ãH¬ñ¦³·Ud9çw=¥\x001d ,£\x001e3ÞSrö®J8qP:\x0010h~Mâ]%¹¦ñ%g/«Ä
t¯\x001a@lbì\x0002øc²FË'go«È\x001a/Vº­ÊÞJD\x0005W¼c\x001e«¸äì}\x0015M¼Mzã	Uâ\x001dXSõî*J\x001eÈÙ\x000bK­¼¬:o\x0001\x001fkí³ØXãm%go,\x0019P<lµ]e6­\x0011°x¬á{\x0000ËÕì\x0015YÍj»\x0002ªãgVQöÀ1M+jÇ©ù\x001bëeÅçÕüõÇ²Æ½¯æ¯¬?5Ú\x00145maÍÇ$V·ò±Í\x0011\x001dW¬!Só×Î:\x0016Ub»B^WW<W}Dw\x0000ËìÕüµeò6D\x0015\x000fÏæ5\x0014o\x0010èd£\x0017¤\x0016\[¹fXU^Ö Ë\x000ePá¨ñ?¶¿µâÉ
´¬Va\x0001VÞ\x0001Ò°å\x0016ïÖÿùëßý©\x000e\x0008üóÏ\x000f'gO÷þóý§O\x000f_O.¾þô)ÅÒv½^$P\x0007¦ôñ\x0006Ä®+\x000c_H6\x0003LZýç«\x000fç'g×øìÃÙåù	FÚ.nÞÆÿq\x0000/¿_æ1òA<ªX^ù¢U¡w
\x0011Ó3f\x0011±&`S	Ø0°;.0_\x000cÓÀJqÈ×«`0\x0014Ä)
ô1\x0005Äu\x0004xÁ>ö)fö1æÃó"\x000b2»ÊwVwX¿(÷ãs\x00152~ûëÃoSnñ?ÿíßÏùôøuÀHóþÅ)À\x0001#C\x0005¿á
þö»ó÷\x0017\x001fRvñäüÝåÅÍvËP!æ¨æ\x000c¢¹BSzl&·dl5¿gé6ì\x001ca¶]3^H6Þ\x000c:\x0007]\x0006¶±Ýu0EÈÖj
QR¬UZ,2LÚñóÕ¨ã|f6Oã\x0012»?½¤ï,P\x00060}g\x0008¿³8ÎæèÊ\x000c#Î\x0006Î{QÅ§+ÇW%ß¦fCtm"+3¾D\x0000Osy3£åu\x0004Ý9Rs\x0014Qa4ïy¥É>ÆÿG×¼\x000eÇ:0\x0014G"×$}i#QÚ*{ù¿´8Ò"Rüd\x00061Þä9®°G|{\x000bÐ¾¿É\x0007\x0010\x001fþU'ÙDÎîOþüòõùñ§ýJÉìH)±¬1Ç 	\x000cÜpùÙÉïnn/Þn+h8<v P<\x0012:×®Æë8~WÏGB\x0006eûpÈ\x0008Qyý\x001eJä½æ\x0008\x001aõgÈyÏkd}ÿØOôûËóÿe=}ò1þÍ{oYÝB\x0019ãí\x0013\x0006\x0010\x0007½>kp~ò1þ«­,¿þÝ}zjÃÄ\x000f'·¿~yÚçïÅ+m\x0016%NÈßK½É%	²³Ü~wu½Eä\x0012\x0008.±É°R;y÷\x0012ßRûHzY²Ñh	rËÃßº>^Mrwïîâ\x000bêÃû§\x001e~_?h
j6x]l¦f3lN²©ÁR¢7¤fªI°;Ü²m³Q\x0005ÏÖxv\x0010/>%½Á`%UÂÓÝx]\x000cz\x0010ÏÕxn\x0010/¬ò¤ñ\x0019\x0008Ï³5µfñêù\x001aÏn<Ç géùu&\x001d¿'Qùu\x0019\x001eÕ\x0001ñ\x0015£Ë'J¨Fz¶&ÑÅT¯3ý|­My]FEª\x0006NÁaÑ¼¥4B¼È5cJåÕÐâÁÅÓ
\x001eås|¯kõ é¦\x0010O®î=ÝA¼ÆîÉAÃµ»\x0012ÜJñ«K¡Æ3¿ºò5O¾BËWær\x0015ëÇc¹^\x0005¥«j\ó\x001f`AÛÅo¿ß¥*íè÷òãýOû(ã#Aä\x0017\x0015\x001cºzæ\x001cH	¾xÿñìê´O¾»ûæìí~T¨Qa\x0012ÕóÓÆJ-¯	Õp9W}Ìr\x0006U×¨z
5~üÜ{á)Î\x000fÇ\x0013Äo\x001c/z¿t\x0006ÕÔ¨fnU½à+®jö ãEÃkÚ\x0008ÎÚ\x001aÔNæé)¸QÓ³.DY"~Ç\x0000u5¨\x0003
!wé ©£P4ï|5ú
Á\x0019T_£úiTkizª\x0010¨ yQû[|\x00065Ô¨aòH<(G|éû«Ruå¥:Æé¯½6¼¶)VÃL&»Átüá¨Ç_\x001fî×hï_¥µ2ëX\x001e±ñyÿ\x0013ÉvyyúüðõË§ý	
Ën1Îðä\x0016\x0003U_ ©\x001a5¾ößn÷ÕÝõó«ËíÉ\x0002«jX5\x0007\x001b	+°.,E7\x0008Ûy\x0000s°PÃÂ$¬Ìíz\x0008ëÐ'H°(óa7\x0014ÎÁê\x001aVÏÁFc\x0000ùõáA×ÔWÖvÆ`\x000eÖÔ°f\x0012ÖaeHÕi:uU¼²Ð§Ýç`m
k'a
\x00177zíO\x001do\x0003Á+\x000b}EË\x001c¬«aÝ$,äF\x0011Ö¤z¯ô\x000c«»´û\x001c«¯Yý$kÆ'Vì\x0001$c Êù2}ë\x001cl¨aÃô¥\·"á\x0018w\x000e\x000cÛ\x0017µLÁV×­ÉA)Ó¥©½2ÒZ|#d;+ùR0ýý5GÛÞ`³W\x0018\x00172xëñ2Ë°Á0ìbÓ\x0005j=f¬Úëöìñiù\x0010TÖdâ\x000e \x0010*½C®/^XQ]\ïÈÿ\x0017@U\x0003ªQ@T\x001a \x001a\ÅBt <Û>2LhjB3NX²\x0006\x0004Õ0EBNß8³ËY9\x0010ÑÖv\x0006R^8\x001c´¥"l­?ÏÕ|n\x0004\x001d1£\x000bå-wÛÀ\x000e\x000b ¡¯	ýð9"i\x001b¤\x0015T|aªò5tqÚaÂP\x0013ñì©]Å |$@Å\x0005¶/D\x0019%¬_MjÍ\x001fe8\x00101R)¾n"â«ñ@ÂÖ\x001aNCe\x0010Ñs:CRjíâ³,\x001b(-¢\x0012ß\x001b¸\x0019¹35.ãâÓ"¡aá\x0003\x001d\x000c7z\x001a\x0003Ô\x0010°I\x0018]%\x001dcTZ4»1ý>q·\x0018¢¤óÝ\x0006é+áÆÏLýzWùõþz
kwt¼ù1
óåå\x0000?ý¾\x0017PØR\x001bã·=oqµ@ØàE\_ÝÝ\x0012áåÇC\x0008¡&QB|I\x0017ÓòX¥2*nÌåºFÔÃXÚ
-\x0019S¿¹	Ônæ7ÔÀ
\x0013ÚÐ\x000e\x0013:vi­r\x001c\x0013÷¡×ªÏt\x000c\x0012J_\x0013b¬w\x00101ä)ÌÉ0\¡-,çSî«ôF\x0019h\x000eadû-¹J\x000f\x0019ù<ë^Y`±=Ðã':\x000829:\x0000ÇßåÈ¦SrñqQÍqQãç%¨Ò:Ê£duBaîyík\x0019MÃhÍ\x000e\x0016\x0007¯qÈ¯\x00158NZ16\x001f26Zêø¹¹)«\x0008Ó:®\x000e36ÇZM\x001ck]RÕVR\x001dxH<©\x0015·ÏT\x000f"BsªaâT\x001b®kT9\x0001FdF×K\x000c36§\x001a&Nõ\x001fÀØ\x001ck8Ö\x0006_W9¾º\x0007-×\x0007[';\x000f|±920qd²¤db\x0014\x0004X-ô%1£Íyñóâe.Ï\x0005õ\x001d2®I8/¡ó¢'Î[Uf9®HËè
ãâ½¨eÃ(ÇÍ·e\x0005è{\x0012Öq¼\x0013õâï¬\x0003­'\x000e´ç0>Ê¬\x0005¾§K	\x000fô¡ñaÆÆóÖã®7Ê\x00001zjöÆU\1._ÇÖõð½=×S O«(Û\x001cÝ¸\x0012zÜÀl\x001dõXS
#ÐÊB/gt
£\x001bÿÔ,Ë\x0016Qp5£ð¢0öUFÃiÔ\x0013®D©ß\x0006#Ptì\x000e÷\x0004µØÝÑ¡a\x000c3vR`,wA®ÜF³|\x0019Mc¾Í»#rè\x0004j\x0003»\x0012\5màJÆ|	óíù1\x0008Z®ì7_1Æ÷é­aÆÆ	\x000bn1U\x0018ÕJ\x0011Í*nä±½ÄÈ0ccÁÍ\x0005÷Y\x001a×1¤@\G_L_à0ÌØXp3á6J®\x001bÂ\x0011Ä-¸å6\Û§\x0010\x0019\x001b\x0013n&^Àòg ²0ÂÒ)z#Óx¶fÜ³õ{E\x0001[n¸Wã'ÆèåÍ-c&n\x0019q
:®Ø\x0005½\x0010QåÇº±àfØ£w+¹ËÑ¬µ´ÜåØçF\x0019mcÂí¸	`:ôâ{ûu¹eTßç8ÌØp;nÂàöøË©#\x00132at¬û¬Ö0cãQØqÂyÎ"Ä5£Îà\x0010\x001fl\x001eÅr\x0007×5ßÚkt\x0019sË#êµÓvìôÄöâ#ãÐM$\x0011àTå\x0010\x0005ðy;Jò\x001du_=5LØÜ1nü1.\x000fÁÑ\x0010¬^JgZ\x001fÁ\x0003wývãöÛH\x000e¢3.H´.pþ\x0012\_v2ÌØØo7l¿ã]$5ÆÇ\x0016·»\x0006v'xzã"ÆæL»ñ3­
\x0017$ £%MMÏqùiî\x00187~Çü\x0001ë¨CÓ!_3©Ef<\x0006À¯\x0005ÇÕPÂq}q}¹áá¨"ý¨
¡¢í >·wO÷÷b\x000b\x000f'â\x0011§s-MÑzu½d\x0016¶ð¼»>û°Cw¨A
\x0006C`u±\x001càZÝÈµ¹ìP.Ss!.Í\x00133Ò2fU%±Á\x001d\x0000s5\x001b\x0001+u\x0011Ün'µ+e\x0011°\x0008*ÔPahµ\x0004³\x001að\#äíeüÏ(Û}?´ñ
p\x000b\x0001]*×4wÇ:c6vw\x001eJÖl|9´ó14CÂ?Êcgn\x0000(êÛfÃs¬Ùúrhïë\x0012Î_Ã¥5\x00013Ì\x001b;v\x000f%³
\x001d"3\x001cô7(öE§\x0012J-§î¼FÈS)¥\x0016§Ò\x0011A¢h¥yÉ
/\x00012ßù\x0011²x \x000cgJ\x0000}M¥JáádÎádU©@$Sâ\x00155VC
Y
0\
©s\x00140×Ò\%6¶ü\x001fJ¦\x001a2õzöjì\x001a²g(ÑO`²Ã)U4ú7Dù\x0006Àt\x0003¦À\x001cìQû\x0014?jÜ\x0010ð\x0019 k\x000c­\x001a2´qyVÜÔeÍ¤/k¶¡Lf¬1gjÈä+@;¹ê¡â£iCØ¨;pð5>w^7nK?\x0010Pü´gA!lòâ¥ëÕ¡\x000eâ£¨+Ó\x0011oh9Îþúðù}û\x0012	÷j0¡èJÈ6ÄyQ¬ã$zÀQôkgß¸ã±aßÞEØ·\x0007Àª\x001aVMÁ*$\x0012,\x0014\x0013\x0015ø\x0004#Áê\x001aVÏÁ*Å\x0019\x0017\x001dO
Ö+ð\x000c»¡ñd\x000eÖÔ°f\x000eV>O\x0017xn\x0001
^qå¨ï§lÌÁÚ\x001aÖÎÁj\x0013ò6PTåª8Z\x001aµ\x0007\MêæHÁr
M|ºòV\x0019>ÿÁô9Î9X_ÃúÉÓ\x0005\\x0008âPº¨ÖXØàèÌÁ\x001a6ÌÁº=vÖð\x0000+¢¬loú§`«V\x000b\x001bÔgh}É#;¼B5ÑR}Ó%Û\x001baîJÀA¢le±6a¹æ4x×¹s´Í 'ï\x0004ïN©%U*RO\x0006ÚûD_ ;\x0007\x000b
,L/­âvúRkcÜ¹é»/ñ£m.09yÅ]«¹7YqÎ\x0007
\x0005w}÷Ñ¥9Úæ\x0006W\x0018^¡ÞdÇÅÜÀ®\x0016\x000eE>Ò\x0019kn09yÅ]KB Ñ~±\x001e8ðL\x001b\x0010\x001bBQs´ÍÅ 'o¸\x0011²\x0017\x001bà\x0001xR\x0010Ð\x0017xÏÁ6\x0017½\x0019Ê®
¥ÅruÄ¤è»t¦`Us1¨ÉÁ9\x000eü¥¹1h\x001dÓB_ð6GÛÜ\x000cjòfÀGV>c!ºâ@k+(Ñ\x0011i{E¨9Úö±0y38Í\x0015=ÁynXÒT\x001fmíh«AM^
èÅd\x0017\x0001\x0015®©²\x001e\x0004ÂDC\x0016s5¨æjPWã~\x0010ÿ§Ý/jãJ\x001bø(°ÍÍ &o\x0006\x001chá2¬,Å¹ ¨Þ\x0007Û¨clUs5¨É«Á&
«D«\x000c¿\x0019@8Þ\x0008GrlUó¾Q\x000f\x001c-)¥\x0012p¤(K\x0017:*ØMUÇ¡mî15ûÂñ4-`	\x0001îâýE´ª\x001b2E\x000bÍÝ\x0000wCÜ¶YÕ
h \x0001Z\x0004Í´}õé\x001cmcmaÒÚ¦Ü-¶§¡LL~»BÛ+UÏÑ6ö\x000b&í×\x001fFÛ\x00044	R\x0005©Üa§8=\x0008I*ô(´Í)ÉS&\x000c¾\x0015ÖX<öÚ6î"Ì¹ñ[.\x0007c¹õ\x001cËX¶¯W¢ÕMÐs6Aº"¿\x001aEk/°G
ÓéÆ]Ô±e«Ëº*\x000e,Ó\x000e¼:³guã}é9ï\x000bËÈ´,´<ÉÈr3ô	øQZ»\x001e³·\x0018³ÿþËãÃÉõ½ÿ´?\x00108dÓp¦UæaA~;ûýÕÅùÉõÕ_Î.\x000f 35\x0019"Ó¥8Ô9Yä«¶eÜ¡\x000b\x0014\x000c¡Ù\x001aÍ\x000e¡¹Rêí:E\x0013\x0003.ýé\x001e"s5\x001b]4`\x0001ÀPj´`4Õ§ÕÐ|æÐ¢\x000bJÅç\x001eVBN\x0017!Å^Gb\x0008-Ôhá5­Z\x001dîµ)Ü;²l)>Vq£çqyË\x000bÓ¿åÐZÓ1h;VÊ}ñD\x0004:\x0006P\x0004æl/<;Ä¦\x001a65ºlØBé\x000eN\x0001±9»èÖ["·\x0003lÊ\x000fM\x0003E®[Y^·°p»éM\x000f±\x0019ÅRâA®J³çâÐ÷\x0010[s!È±\x001b\x0001ã\x0014ÍÐº+®!±©eÛ­¹\x0010äØrR´l¦¤:¥±\x001c
\x0000Ó=«Ø+AÝ	ñ;ÒE\x001ap|8Y\x0010YâkËn+Ù\	rìN<$µº**\x0011\x001fÛ¿AØ;A]
ÿØeSÍ Æî<F/Ç\x0003eRÒT\x0010\ÄÖ\
jìRø\x0007/[cwÕÝEõVM»m5Ì¡høÆKuÑ!UÝUcvWI*ºÆ^·2iGØ\x0001ôo!¶Æîª1»+Y_\x0012Ûky (ÑøäZöE\x001b³«ÆÌ.ÊçgB\x0002¿\x0011mCçÁ\x0010[cÛÔm\x0003q*r4\x001bËð\x000cW¬Kþ¢¡\x001baÆÀ\x0001^.E\x0001¥3¥LS11À\x0006Æ!¶Æs1ÏM¥ÎTdCYNV×T\x0017íG?6|Ìüð°fC\x001e\x000e(I
£Ë¨
|òq\x0008bC\x001eñ~\ÃûñuáÝ¯áÝ\x000f`a\x0008ÏãÌ§Wa¼t?­Ñýôzè¤ùáùáiÍÿÅ?\x0019»&Ø=°º&H!ºÀËâ5R6Õ©ùI2b÷ô)K¤Ó2Û+&L/G<ø^ûÂ?¿¢/\x000cÝòÁèòÅÇ¡¤ä}åØ²,\x001fÌ²Ç¡é\x0010Í0â?ö\x001d\x0016:Â0JørBÓ:Þ
¥\x0019ñçoöOiN\x0001K\x0011\x0012ÍQPËûù\x0001iØÝÉY2KÕ\j\x000b{²¹¦\é1Ò\x0014$Ø º0\x0000\x00065\x0018¼\x0005Ó5\x001eY0m¹\x0001\x0007ëÒÂ$ztÁ\x0000©ÁÌ\x0008³Tº¨±-î[>¤\x0016\x001b»]\x000får5\x001báòº¨­ù\x000bq¬M¨û{k\x0004Ë×X~\x0004+Ø2øÝ*.ùEÛËê7}òk\x0004,Ô`áÕl|ÙX
9b*p\x0017]P\x0010\x0002þ®:· Ø
Õe#dÍ#g2ú¶4í\x0002BÉÊ$V¬¿9+°m£LõZl\x0010VQ¤\x0010Ü\x001d¯Dù\x001b&\x0007¬Ws"åÈÄ\x0002¤»
(TUfÜ\x0005Û D6@Öì}9´ùã\x001es®Q\x001bnüSUÈ\x0016U¡7Xõm¾Í¯\x001aÇBx\x0016Ò6&ÐiüS6üÜ»`úHê\x0008XëY\x000c¹\x0016ñ\x0003ºÕþç<n`0ù¢\x0005dk¡F|$À°R¹\x0013\x001c´\x0017,íã\x00169=ª9jìdj}\x000c\x000eX-G2vVô±£\x0011²ædªæb²¦`%6\x0019 õe\x0003dÐ\x001cM\x001898ZÔ±52GÌi&S\x001b\x0014ÃGöY;M8íµ2Nø\x0015l7aÖ\x0001Í\x0018ß?Æãø\x0010mÊ?aåE´l_O>=|=ùóýÓÏ¿ReÍÍ§}52xIHê\x0002Êí\x000e`ÑYµAEúòêöäòüæäÏg×ß^|¸¡
«»ë\x001d\x00056\x0005^Õðê¿\x0018<Ôð°\x0018>OÐqÁ;lÇ'xºí[LÁë\x001a^ÿ\x0017[ySÃÿbð¶·Ëàµ¤êM/@Re¬÷¥éAö/Ëà]
ïÁ+àk\x0001¤
<J]1ü·¼¯Ùý±]\x0013jøð_\x000b¾Ôiå;J,Üó¶sTTcCÉï
¥ËèÛ\x001bvá\x0015«<'\x001aá¢`ï5«"ê3«Ëè+V.¼cµàf~aÃi\x0000²7|bu/­¶\x000c¾¹båÂ;Öy~ÉI\x0015O\x0000íz\x0016\x001cÎmç-o®X¹ðÅ²ììD¢øuîñ¾¨rõ]<m\x0019}sÇÊ¬\x0015§!¿!p,1ï\x001bÏo\x0008ðÇ^ûæ\x000boÙxPií±\x001aBÐuÀgÖ#ÛËæ\x000b¯Yì\x0006§3ëY\x0012+ÚKÊ*ÅÓ5YFßÜ³ráE\x001b\x001fO4&\x0016\x0007©yr\x0012tÙ9ý¨eðÍ=+\x0017^´\x0002H?8þßQ\x001d¯÷\x0000\x0000ÇWÍ=«\x0016Þ³R°6¼@¹JºgKH.¾_»ÕeôÍ=«Ý³Þ\x0005®¡Æ~<¢wÜä\x0000ºÏ¥.o_²Ë®YïÅJGW£åÌð<öè.jîYµìM\x001a	¹\x001c0MrË\x0012ç<_U®/¹[Fß\´jáE+4Þ®ùUb±>/o{ú\x000c²¯8^Fß\´jÙEû­}*xhSãñÅmÿö×ß\x001e?\x0013óÇ§Ç¯{;\x0010q"a¯³ÊJ\x0017e|_´ÿö»ó÷\x0017\x001f\x0008ôãõÅÍ\x0001ºæÔ\x0013 ,ë)õÜ=
Ê\x0008m¯Y2\x0003jkP;µ ¿SÛý9"úºÒ\x0019N_sú©\x0005U4\x0018\x0015ãÊ%ÃH8EûüÅ\x0004gÝ#dÒÛs\x00184þ1ÕÄ÷2Wk±
Þß\x0006Î-iPlN9FÑ	eµ"-\x0015·ÆÆk®¤ÜQ³9Grê á¬zõÔ\x0013WÜÝmÝ_1\x0003Ú#9sþ PÝe¥UÅ?à-"\x001a5]éDñ3ÅâpÒE¼~­H+úöq\x0005.~ûýþë×,kÿ1ÞWûÒ5Úp¦Ë:ÂJ¹\x000e\x001ac}_)xñþãÙÍMVµÿ\x0018o¨ýªFT\x0013çÙ[k¹)^j~2y×JCB
	ãÍ§×â^Y#\x000bcwÞÇ\x0019uÍ¨'\x0018%¿­	ôrÆQñÜ\x0006m{}§qHSCaH¥\x0004×\x001eXcø¾DG!û@ô8¤­!í8¤<¶ÂjJ\x001bªìÈ
ú¤ã¾fô\x0013\x000biHÁ[0¼%£ÏIÏ\x0016¿aüÇ0¤lÎ¶\x001c?ÜJ:vðñsSI¦R¬ém¯+3NÙ\x001c\x001c9~rTdácUÑ÷´\x001c'¶s	¥Y¯k5«ºÖtß\>þøðô¼·\x001e8¾1\x000cé9ê2L<È¢ç\x00186\x0006¤ëæòâóëÛ]\x0017Y/&5«bÒWGikJûZ)}Mé_)eå³GJ)Æ1qô9b·§yØÞpºé\x0005Ú&8ó#'\x000eP\x001aÑN.õ¤IÄ\x0006¬.Çl\x000e8Añ«òWO5Å"<K\x001a	/6W\x0019a6'HN\x001c!\x001cgI\x0012¨ñ
\x001c,c2eïÿNP6'HN\x001c!\x0011\x0004êôr'
MöÜ-B/¡0Î©3¤fÎ\x0010f\x000bÓò¾(ñ-Õ¢cí\x001d4s¼£)\x0011(!jË¼qnÚ½Æø\x0004fsÔÌ\x0019ò\x0015»±l\x0014âsÜ<³arû8fsÔÌ\x0019ò\x0015A[rEJîåV[*$Ç0C¤f\x000eQ\x001en;4úïÓòW-}"CÐ\x001c"9DJ\x0004)Êp\x0015a\x0008XDÀlÎ\x0010Ì¡?\x0004³9C0sþ\x0010Ìæ\x000cÁÌ\x0019úC03\x00043gèÀÔÍ\x0011Ò3GÈ	\x001cXÖä\x0001¢8n«Ã\x0004gsôÔ\x0019
§¤Jç$'2ÊLrPºWmÀl\x001fCSgÈÓxD\x001cFÎ­ºeÈräÜ<Ui³9Dzê\x0010¹SE-ÅÑØ;lË\x0017x9×Í)ÒS§(Þë¤ü\x001aýOE7)Úæ\x0018O"Ó\x001c#3u\x0013ñpÖs¶]`NÂ´ý4	Ìæ\x0014×w\x0013XaÇK=þ\x0003?~ºÿéáäæþñóóÃÉÙ/÷Ï¿îo\x0006Ý³\x0002xUôÝ9"'û¬goÏOnÎ.>Ü½;»ýî\x0000T¨QáU£\x001aÕL¡\x001aU¦~æø\x001cyçßd\x001dG5B\x0006\x0015¡\x0015\x0002«zòÂ\x0006î<\x0011\dâU?\x0005n\x000cVÁÚn\x000f:ãòròþñùþó¾X"Î©'Í>[OÛ`]<Ó÷.XâÝÉûÛ³\x000fû!U
©Æ!-pð\x0018\x0018èy¤\x0002GCµ=Up0$Ô0\x000e\x001a\x001c<	DþI\x0013XkÓôÅ!ãºÔ\x0013Üp%çXi\x001eW¥!M
iÆ!ãy¡b\\x0017hÂ\x0017ýÍ~ØÖ8¤­!í\x0004¤+ú¥¾¤¯ÔJ3Äõ­[ã®tÃ2xn/óÎÑu²(Ã\x001cåsû\x001aÒO¬$?\x0016QtUâÆn	ÒzÍNê$\x001fò1"Þÿòprõòã§Çÿø?û<\x000fã91­µG
÷dÍ\x0015§¦­ïeìðìÝùÉÕÝ7\x0017%_'S5z\x0005d[\x001fgþO4ÎüýÏÏÿñr
Ðözlª\x0014FQÎOHî%1¶\x000ff¾¿_NSQÍÙ®"¹\x001cum0åëåt
§âÄ1ÔÔÏ1Ô¨àÒ¨fÃu=\x001a\x001aÔ0*C\x0008,ÏÃ\x0004u\x0012i®p6ªO³\x000c b<sÝ\x0001²mÉ	>,þtÿé~uLÒÏ"ÝÀx$ëßT
èu²W\x0019U|]üéìò¬©YÇT5¦Ä4\x0012mxÆ×\x000fÉ
ð½\x0008\x001búÀ\x0007)¡¦IJÇg)`±\x000c÷Ñkì¯ºÔAñ$\x000e,:2,vÁbbW9ÂA¦¦4sqcÒì\x0005©5\x000bL(mX\x0011oÜe¶Æ´ñøhÞÀá­ø\x001a/Ç§\x001f|(&ÀZ2:])Mùå%>Å~þÏû÷«§øe¯+äVÂ4\x0006±à*\x0019\x0003\x001bD®îâKìÛ«ë\x0008wµËÉ J×Pº	JT^Éæ]ÊR\æ
\x0017<~[BÖ²"j¯p)k\x0011È\x0012#©&ÇÁaaJ³òC_§7\x000cÙìJõJwe÷CJ;³ÌP\JÁ*OH_\x001c¤åÛÒ7þµR¶\x001f4)~¼ª\x000f/ÖÇÊ4V \x001fNþôåé§ûOÿòò¤Qwp\x0010\x000e\x000f<\x000eñ\x0005ÎjÅ\x000fHÕ#Ìó?]]¿=»üÿï.Î¯÷³ªUÍ°¦¼/=$-¹¬\x0000Ç2U?ïx\x000eV×°z\x000eVI(°*7/\x0006ÏÊ/þh+kkX;\x0007Í\x0014%Æ{IgØje\x0005ëkX?\x0003\x001b}8II¬\x0004«<=<4Ãö©¡\x0019Ôª\x0010Mäyâ3¬ªH!Z©ÎÕ\ÊÙOjm:_©o~¬Òüøô¥ìT÷Í.s°ÍñSç\x000b×\x0007òZ\x0015²>Îl/EÑ}ªh\x0015Ó\x0005SÇ\x000bËxù2° ò»..vYØ
å*X·´\x0011ñ¢67W^ØêæzUk\x000bëÝ$àäïÃ×ó¯\x00114bîm10¼i#°\x000e,]±Àú§\x000eúÈXN\x0017ÞßDÊÈ¸+þ\x0000ëý$àWuÒ\x0003Zq\x0006N\x0007(Úûª`Ê~æÚ\x0004¦®1õ\x001cf JYæx(nÅtr[eÀ\x0010¥­)í\x000c%·ãi\x001fN5«dSg¤ÜVæ9DéjJ7³/wÂÉc*b$jÃL	J_Sú¹µ¤\x000c¦ö©Ã\x0016<\x0014'6Ü¤ã¡Æ\x000csi
a®&>\x0002Í\x0002Ù·ócV·=Ú"1Ã	Tªäµse9!ð	\x0012}Fx³µSFÓ\x0014íP¯W=xPì8Âî¬f¹!'LpbÍ
ÛM_&º\x0019JÀ)×Æ&0\x001b³)gì¦³4ý bº¢@iËYß0çpÓ4fSò12Â\x0010¸e1\x0015§úB\x0011N\x0019Ö®t\x0019êhýÇ\x001fòûùìqoP´LkpÑ¿×/dùp¼¶E\x001b?sOè³ý¨ªFUs¨ÑM&M,\x001bÊ`	\x0005lB±Úû\x0018¨P£Â\x001cj<ö$¦ãP\j,\x001c
ÃRAô%3¨ºFÕs¨°êÃØ	ihk\x0016ÄDý¥E¨J¯'Côz2\x00049_\x001e¿ìÝ\x0001¦\x000c)Ìy\p\x0001<<Fïêr=¹<9»»>¿½Ú\x000f«kX=	+4gAQüF{)U&*Ú^k
ÖÔ°f\x0016û\x0002V­Ò~UÀC3ûÛt
ÕÖ¨v\x0016Up[ið¾&W\x001cE½ÖÓ\x0014««YÝ\x001c«\x000c¥Ò%VÉÝqR÷A´)X_ÃúYXàsðëäæ3iúWÉ ¬Z7\x0005ª6\x0005o?Ý?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-05.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=m\x0015
ÚÃ	âÆå;Ñå»¯\x0005ùV´þÆoàÚÇZ\x0003æÀy@U\x001d÷´ÛG¢FüÃã7ãµÏÂ\x001aú¬a\x0006+²1k:¬»C5¡»½Î\x0016Vëû¬Ö·ÃÖ2m¼«q³AË[U\x001cQXA\x001b\x0006´ SháÝG	\x000e+\x0015Y+3\x0015´Þã+·ÐFÝ§íI\M¦Åqè\x001c\x001f\x000cI6-6I\x0016Ãì¾¹7ÐêÎÛCZ=Pókpä«ÌÔÌ"]!]Ô`ÕÆ\x0006\x0015´ã.4L\x0006Açv\£QFp­Ã¡\x0005¬$Ñ×w_[p»ì0áZÕ\x001bc\x001d¬Ó
Y`#p¯\x0017z4ë­îÐ,\x0019v\x0001Uyd3`
\x0011\x0007°¹5Ô\x0000¾epé\x001cÖáNØÔ0´´\x001cÕÁ®úÈbÁ°´¬Y	K·ÖA\x001bÜ6¸fZ¼±\x0004Þ\x0008^ñM\x0000Vdmµ^6\x000e×6¶¯­Õ\x0005qi\x001f\x001eû\x0018Ø0ÆhíÐI Ñ­´6\x001f
¬Ã,8nµ\x0007X»\x001aìÐ"Ø\x0019\x0016Á\x0006S?1ìÞ)ö6DUG-«¼\x0012mV\x0003¿m¦õº\x0014\x000c¡Ø¥âÒÍ\x0018Ü\x000c\x001d¸gG-½}ÂtÊ/\x000bÃ`ys±¼Æ\x00179x\x0000V±`.s\x000eVW#ÖÙ\x000f,\x0003ý¾ÙÃ Ê\x001aGSFY{Ycø/¸R7ýþW8%î~Û¦.:Ù<t\x001fñ÷Ì1çX
7³vÑbbIßq­Nòç\x0007þøøp÷y8k\x000eqÜ 3m\x0019qµÇªiNÛF
IÞä´\x001eqvCC¿o&vâË:\x001bá\x0018\x0014·7\x0014Ö#v(éÞ#v\x0003÷©Ä8¥S.<Aì°Þ$áI½&qØ n¾µÑl9*Ê\x0006ïDwáòp_wÓ\x0006q»¿EË\x0012{\x001dDKH\x0005>>à\x001aÙX¼~|Xb&¼\x001e~tôûÖåõp¹¤>\x0003ãy8GCL\x0019î\x0019zðÿt`xk\x0003`ü};°.½\x00154\x001fe{BI?9Æì×\x0003\x001ez\x0013~Æ\x0005\x0003\x000c.·´£|S:\x000e8`±½nE`³\x0001Üì¬EÜa=e\x0013Øk\x000fIt?s¢KáZ¼^\x000fy}óu\x001ev¨\x0005Î]P´u\x0000\x0003M\x0002X\x000b8lìv\x000f\x0008¶p(£}qü¼Â:úòÍE+Àyß°	ÀZa\x00015þÁÑ`\x0003¸ýãþvWM\x001a¶{J8¿|wTã`$ÅôÞ»ü¿¿;\x0019+H«fÀhÚ\x0018³\x0014\x0001%å¥0\x0011îò\x001a\x0019Ïg¬\x001aÄè}\x000b#îË¹\x000e]Õ£ªUèywV~"a=\x000epp\x0018L 4,\x000f&ßÔÁØ2m:û°Ê®"X\x000517!j'EAð­TÄ¬¥LÞ\x001e61êZ3GøÛ\x0016HS\x0003â±4±Xk«VYHm¶	2¥êïE1±>\x001bfYù,Südë¼ÞiØÍO\x0005V>26\x001c /õ\
bï\x001ew!&
Þ©Ôoc\x0017u¹rY8 $F;ú²¯K-ìñéÅ^>çú|xÊ§ppâ>\x001dÃ}q±NÄÀ>±ø|\x0003_'q|¨p8/:.¥t\x0013$>%BííÍÄÇ)N\x001a\x001dCñmNÏ\x000fÏî:\x0004­53ØôPÊ³Q¦aD7:\x0013	\x000fàWç×ÿ1z\3a§\dµ§#ê,Â3JÕ±&XORk vö\x0010½Ìhrfå¤à6Zr\x0019ÁØ,úCÖæl`LjÀTÛ«Ö<w\x0002>\x001bÍ=m\x0001¾ñ$¥íã3b§3öë¦\x0006×§3Æ,í4jPq\x001d¨ÉÀÑ2V}ßÃ\x001e"Å\x0011§#:LYK÷Uõsmªrþ-cÔí¿ma4®tJ<\x0001#8eØR\x0018HhKÉxªð\x0007GI\x0008©ìþëo$¤ûx÷Ë
F\x0003vH\x0017iFÔp¼	nêR¥xÛ:-	
ðß¾'MÝÓ7Ç?\ìÆÖÝí\x0017±µÉ3¹á¼á\x0001\x0019ËmJ
¶m×Ø2ÒÎ:\x0017Ü\x000fÖ[û¹\x000b\x000e®¯â,±qR1cSjïÈÊ++ç®¸Ïµ\x0015"8¼m xL5½Mz[»g\x001bãúäøÛYä^Î
Hr9JNÀmö}Êmõ\x0000\x001b;oÁ³/^4&¤\x001b>&\x001bkSU¹m\x001cpÛ8[&¹3X$ã¬TÛ\x001bÊÆ¬ÇNp|âYÛD{Ip`q\x0004'P\x0016¹S\x0018IÐ5sÖ©Þz{XoYîÛ®]JVl\x001c\\x0010x"(lx¾±Fd\x0008w÷_nî¿Ýlú·|v|ðátGÐq{½¾´õ7ã\x001a-:\x001aXÑe8ªffÖ\x001cU[\x00057
pÓ\x000c\´\x001b¼¸VºFàRV\x0007I\x001b¿\x001amìBÚìÛiáV]ë\x0002.Ön3®âá!¤ÖÂÕ½O\x000e'ë'×Â\x001b\x0014;\x0019\x001d&V\x001f=gaBf=Þ®åxÁ\x001bMÇëÊÜ=\x0014952Á;$·\x001a¯\x001bl^üm;¯ó"\x001fæ´¢nðñ+¯Zmûj?Ø¾ÚÏÙ¿!JðÍiuD\x000bÙ±-\x000bÔ*¸\x0016o\x001còÎ°½¸\x0017\x001c\x0008Ñó®á£@\x0017+áÆáös¶/v\x0013\x0016ó×¼$ñv\x0019C\x0012J'Ï:¼ipTt7å\x0016^_ZpS\x0014õØXÇ» ¬Ür\g7{Ö-5\x0008wîÃ·Ûç]\x0011º`j&Æ´¹Î\x000f£Ð{úë;§áêäøz\x000f`O\x0017\x00073ª\x0016B\x001dpRFi²6:¶ÞJf vGM#ä X×M%1\x0005ðõÃóã·ym\x001fºy/.öµsKFÎl{}~}q5þn\x000bXO·\x0002KÉTÉ§\x001c¹=\x0018\x0003òbÓhBe?Y.KÖuÎguÔYÌ/4ånWr],~TÆA¬êÄÇÛ0¯%qöúúb\x001f`'FF5\x0011Ö\x0006­S@0e)×u£½¬-!ö	Cl!3ÜJÛ|äùQp7Q]Ûü\x001aåFÂáBX-6\x0012r
±±µQÃïÚÓ	ÍÐ4\x0011ZÑËIwõ-ûÑÎI¾X?Óõå È°-'ß\x001e\x001fîvÃÅÈò±º­\x0013Rs\x001a\x0011À@¸«óÓñOØû
ãâ}g\>Óm8îö¤Él,\x0017N<<´b[\x0015÷¥O~Äì÷é\x0014\x0014sv*gÈib#§³U}4göÌ`%»þ¸óSiàÌ\x0003ÎÜÈéeþGÆ\x0002\x0003SSeYz/|0Ù¹\x0011Ó\x000e^»m}íÞ rV±\x0008¹Úm:2«,g\x0017²DÎ\x001a±Ê¥õ²ùOÀÐ\x0013ÙåÚ´`¦\x0001fjÄºbÅ¢\x001e¥jàzT+g\x001c¼öØúÚc®Gb½ïFD*C6ð2Î"rÕHÂ\x001f\x001cuÑÇ\x001fqt×\x000ek®ëDé\x001c(×Àô\x0003ñ\x001að®G#^Búdi:©MkÁ£òR!óU»Òîö²' uz[¦ýd6%ãe2~0,\x00107JAÛeÃ'¡u~\x000f=?l\x0002«®T, ct·j»\x000eÀihV÷Ñ¬nA«{MUÀædÙFÕô\x001bØÌÍLgË¢\x0016ßAÝmZ\x000c_¾ÛìàC°
_ÃFíêµÊ7Ú\x0013{Ú}ÛÅ\x0016üF;,ø0+ã~w\x0016\¯\x001fùµb»\x0000ãe[sDj§\x001cÞ[8FìÂØE\x001f§1ªÒV\x000c6r±/\Mªj¯ÞçÍLc4\x0003FÓÆØÓô\x0002FÍ[0ÚK\x001ew}º\x0019»~\x0018ô'1ê(¡\x000fd4ZjÒ¥øGï4/\x0019ã1¶1ªT[rm¨Æ9Å\x0011Ó\x00001µ!Ö08.cÕé\x0016g=6º£
±7¨\x0005ó\x000b®\x0001FÈ\x0007P2¢ÈôU\x0007Ëì¹¥L$\x0003ÂØD\x0013\x001dº÷,7¤ëÎ{
å&1j3XEmÚÑ×\x0004Bv©ªE»z[¶£nMv\x0008iÛ ,óËvU&\x001c¼ú²ã*~pÈhßrÌÀÅÙHÑJF\x0001:¾\x0018±fljK#ãp!}ÛBÚ(Á\x0007ï«è¶nO-ÓÏæ2Fµ\x0011Dª\x000b">\x001fü·Ûgá¼¿yþº;D\x0002µ(ê:\x0000G
$U\x0008»]ÿv"\x001b\x0007ï¯ß÷\x000c°\x0016¢íjÛÚ¸'%nvUj0á7³ö\x001a2Tïâ<µ¬¥HÖp¶¡
?åÝ·\x0016Öá\x000ehß\x0002ÉJARÊ®®k"^V@Õ\x001b·¨{·\x0005øÎn¾ßÜÞùAy¥ù£'\x0017®:¸ìd*¦\x001b\x001dP,_ÔÙñãw?ìø¤x6ñ24RÂñÃ%Ã2xË-ééÆFa¶aêN[\x00141µ6m¨\x0006Í#;ÁÙd\x0015 ¹¸È;kÆf\x001d6rÁröRï\x00139Eq\x001bÖ3ÈLß xwÂzòb9g\x001eræ&Î u÷Þ=§\x0013À_7u=GÇ;7rvÇ;qö÷Ikáà½{©
\x0008Ò9è\x0019|ÚÈÙå3©6NX\x00068-W\x001bÂi¤E	Ü¶läìµkjoãÄé¼Þ²8\x0019D]åùÒÏ(qÌ¹\x001b®áË\x0000\x00186óïï>¡µ3UCÓ¸J,(æ¬eÒ´\x0005o;
$?\x0002z}ðþô5ÚùW;ò5i³\x0018$
A¦²ZíY\x0008·ÌÀ+¥\x0015Æs\x001cß[\x0017Ç&l4³v»4
*\x0015¦²\x001a¸\x001b\x0015;J\x001ef\x0011=-Sn­³k±®®\x0014YM¯®t"+æ´}aÕÛaNÜNäIr\x001dVk\x0007{ÀÚÖ=R¡ìW¸Åq$)Ô\x001b7v\x0005Ô´áB§Ôw¡ßßýrûp¿»hTY/n>æ¹9Pã«èÛ|@Ì7'çïÞí(\x0016eÊ®\x0004\x0004)jÄÄ*¾hiÔ2¦V@ï¼Â·P\x0001¥i¤D\x00055¹4¥\x001aÝÔ\x001dç\x001e_t:§\x001bpºvN|Á^"ZwË¹ûÖ4\x0001³äæ;\x001f\x000fþà¨ïâ½¿Û9G\x0003kÇK|=Á½;0Á[æ
~ë{¥÷§ã\x00134®7ï)³H÷4:\x001cgYRv@×
3·ÒÃ#¢Òè:=?¤\x000b¾.pá$Ðå28 C,KçWX»Nï\x001aéN\x0007H\x001b |\x001dùÊ\²xa£9\x0001¯\x001bçxYOÇº\x0018\x001aRÅ,\x001aàËÉ\x0000\x0017Øw;íö$:Ý]ÐgÑ¯»Ø"_vv\x0019WËu\x0003ë°znùêõfÑ\x0013Î\x0017tÔ\x0002_\x0012U\x0004\x0019Ø\x0004xz\x0005¼8Ä
xàâÜ	à\x0005\x001eÒ\x0016Bâ!]~/£ç\x0013]þá ÓPaó®O½ë÷Ý\x0015÷ó\x00193ø4þml1M"f§\x001bE\x001bgì\x0012º¼!"Ð%=©ëâöéîéÛÍý§5]\x0000döbMZZ\x0018Æ\x0005v%]\x0017'§WÇï^z^35$=
àäCøâáÓ¯»\x000e`ªÎä4£íú.Ü¿;\x0014xqþú§ñÃéz\x0003í|ïð\x0007¦EÆCa¨Zbè53\x0016v'Þ'áu1Êì\x00071ÊýxÆ£\x0014Z)ì	|×u(VvW%ÊD¾NÞ\x0011ùbná£I2%"iê=UÕýÓ"¼â\x0001ö\x0000¦2\x0004?Ëç·ßQña§6ë\x0014^uÕ¸°u\x0012\ÂäÐàïÚüR.Ï¯_]|\x0000/püòÏ°·°·0\x0015\x0016\x001a\x000cËzj*
a¡Jëw6°ví¦ÈZ»M§³b,·=*\x0019\x0010­\x0011¹\x001d\x001dw64°ö\x001c	dí9\x0012a£©é²qiQ0ò©ÇW6X;µí°ò;|WZÊÆe\x0013°ÖÂ®à¾®®ât"kD½Ä\x0019]ðÙb´(\x0017ë°Úí	²\x0015ØÖ-\x000bÇQ¬éçäDJFû:I!,ß²Zñ¸®N%J·÷ß\x000fù«=\x0005D°\x0007¨c\x0014-*DØ\x0003òu¥±â¦ËwW\x0000ÈgüÕx\x001dQ%
\x0003ÒÐJ\x001ahºölÉÕ\x000e¤±Üd3©\x001d¬©m^SÏ
$õFyb!\x001dÙªAU`ï®îÔÞ\x001düüW7ßo\x001fy\x001eðÛûÛïÀ½Ó\x000bµ7+\x001c\x000brpëì%\x0016G\x00154®.?\ðTà7'ïN>\\x0000þøç\x00157ÊQá\x000f°\x001cµ2_ÞÜÝûÛû;¹Ýyz\x0019\x0019q9\x000bëêO©1aý
|y|úî
üçp ÿÙØ?zäv°£¾Ôì3k\x0006ô\x0004øËíý_ÿë;\x0003$¸T^QU·Ê;Rë<¤A d]iÝa\x0017\x0010ZY¹NFêÇQg¹ÇE^#=ÚÈ\x0012\x000eÏÈD\x0006+C L[+dx[J,7âC!-YèC
FúBé[DþÎÍdYið!¡&\x0012äb\x0011^°Ë¸è\x001e?\x001c,0KgÒ °L^<eÇï2Óä«Ed`\x001bèÑHfº]\x0016h\x00149eÌ.\x0005CUz4a "\x00160ðÙÁy&0«ê&ÃÈå2²d©\x000c|\L\x0006ö¸¢ +±¼\x001b~\x001e~¡É ÁÙf ö=,\x0016yr$4ËÈBé\x0005@­\x000c¼Ï-"ÃéJ&´¿M\x001c¾nÙdxJ¹Óe+\x001f@Zú61\x0011JF²äQ¡¯|~d¬åF#,4f\x0006ÇºÔNç§ç5+m­Tý_¿\x0000µÔa¼ÅäV2m\x0000^WsfÊ\x0017àì30Ã\x000b¿\x0000¹U­Ç9i¼ \x0015sf\x000f-ò=´ffá6³ØbBF°2Ì»³LÕöHf\}y)\x0019VþÐ£\x000cÎ&ù\x0000Æ[\x0010É§IZbÈð\x000c±¶}Ípò\x0006\x001fçà«ó\x0007à])ÊÂ³k©¡EQ¦#z4\x0005O\x0001u ó8µ¶x\x001a>Õ5\x000by¡¡µèªÐ£,;\x001a\x0000BkV*ï,è$d\x001as±\x000bÈ4þ¿\x001fg\x001b\x001aft9\x0003¬/ã\x0012\x0010-W÷Ì`}È"4\x001a)ÏF4XµêñTN'æ!g@^v\x0006vòl#3&P¯6.Z¶\x0014´B´T\x0017-,<\x00044b\x001eg\x0013s!R\x000b\x001dÜ\x0001Àò(ïa´p.ÆÖZê^f\x0003Þ#Ê³	Í[tB«f1¥nÉÚÂ÷ h1Ì< þ¼ùz|â0I¯;èà\x0012/Ã\x0007W¿Þ}¼yþ¼gáÐz(_\x0016ÎzC\x001cæÊ\x000e¤u´t\x001cpÂðÁÕO§¯¯Øv-Ú9\x0016£¢_-)~!aÌìzÀKv/Öo\x000e!º\x001e=Ñ¬&BìnI¼¤ëD©ÔÀÃ"bÌrD1PÝ\x000f¶¼hPC\x0018\x00017eLºDÑ¿üxg1¢qé\x0014ªÛ\x0018m©0$FO¿DFÇWSëÜKÏ|:ã]tú\x000bEgpªî¤	ß><¹»ßÍ¦pövq\x00004ª¢äÌaH>\x001d8þ±\x0008l\x000bÛõÁÛóë³Ówû¡(ÌÐ\x0008¥=\x0010
\x0017¡¢±\x0002õÒkÂ¤ÑP¦Ä\x0011
Î2\x001cìCPO0¯·n´éL}k7ùí\x0019\x001aTLÁÕ·ç%èAeMK È­ô­oÏR àNªyK¥ÄP8§v\x0011\x0014úm­ûÜØúö°:\x0015¨¤*{áN¶AÁÿÜ¶îsèL'(*/PÑ	^¶Ïq8y0­{Ê\x001fòBá \x0012ÙRoQÎ\x0017w&&¼¥§Ö-²ºòöÊt\x0014
,\x000b¥½½Á)9\x0015
^Y¶u¥\a2JËB¹EÛ\x0014?u³éé´\x0012Ë\x0019\x00044ÍË ðÄ§GëJ\x0003\x0010Üê»B*]÷ù2ÓIed]-ÙD¨±\x001fb
9P\x0002÷¹Õ\x001c`±v9µDv}×Éai/­5%êëdxÊÜ¼\x0005T\x0018g£G\x0013U¦/D\x0015\x0015É«!U°òöÔ[\x0013TÄ¥­Ki(DYªx¨IÂc6¾B5Aeº±5\x001e2Ësh¥,iÎ\x0002UT*ÊJ¹9»Êþãî\x0017ò\x00110h"è_n>ÄæÉÓ§Ço\x000fT]·ËÆóMÒDp.>(x¤ìj­\x000fÑÞ\x001d¿.	ÍË×Ç\x0017Wç#%v\x0003@vbf\x0000êÒÄ6µ\x0003@\x001c5Ã/\YHó\x0000
_xq\x001cDñÿ"®À.­\x0001YøÏ\x000c@å:@ÇI\x0013ØsÑ
à;ï,ÀpDMVóV\x0003gøKÇ{P\x0007\x00014/\x001cÃé¿ünÿÁm¿ðô;Ò_ÿzóåë-	ï	\x0004d
Q±\x000f{Å\x0014^\x0002Añe0ëO_ÿt|ööäêj¤H¥7ðÉð\x0002X\x0017 Á«.¡Zèqêe\x0010y\x0006\x001dü\x001daÖâE]CE\x0015\x0003él¬y1ó"RÕLGUô\x000c<Lpr8\x0019³\x0016¾\x0017å%\x0007µÛ\x001eËhá£ñÆÏâCoó!Q
ò±Þ\x0000Fn·_yÛø°ÏôûM'óa\x0004à0\x000cIï'SQï
dx²¥9\x001bÏÙPW\x000eKyåå\x0017S^áÍ&:7Ò\x001c>EEzÄ§HÜøò¸ý:ÜÆñÍæYo6ó\x0001\x0005¤\x0006\x0006\x0003öµ:gëÕª\x0011Ï Þ\x001c«g³¢ð-ò%%ÑùÄÓk\x0018\x0016f:2yÎöÃqðºTw 	4üq8Ásnöwûx\x001fã-\x0005ÑÐîõ\x0014rÿÿýÿøë~zøRX\x001d=í=Á¶;)ÄÝ'\x0019%¬\x0016ÆN³×çg\x0005ÛaÉØ%\x001eÄw÷\x001eîïÇ±\x0007ùØÁS#1a+VâMMó÷\x0013üö+í\x0018õ¾µ\x001eÄ'fCG\x0014¯*Û\x0016\x0015-G\x000b$£Ãôå\x0012jÜ»ÝþMm#_`\x000cFü9J\x0016X´\x001d©ÕH¤z\x0016µFÓ¢m^¾Ø¥}\x0008°µ
¥(\x0007\x0017;¥¾õ°ñ¦ÇBllß.\x0014*¥R²á?¾ò·ÇEfcãj»å«mµ¸ñZs¡\x0011nÀ$fÕRìç¯ñ÷?=mmXè<\ìóý×»§ß÷%Pqèa*¶\x0003åCäÔKâ$[PÛ\x000f\x000f@=urvzùß¯Çò\x0015F2vs\x0019[	M:äüU\x0019OL¶h.¢ßµ=ÜÚFÊ¨º/SßDèaá8	íÝ%
bÑGÄ\x0017¡9¸fî":ËÅ\x0005V\x0019-Þsò&\x001f5µÓùpO÷ÄØ\x001aùRY7äÃ¾2rbÀ]3²i{`¨
\x0011ÝSÝù¨m4Q7\x0017D>\x0005\x0010QÜhpc_ÖB·#b¿´Î3ß2ÚvÇ)sÏ¹JPõëÝRxÓåbGôèQè¸dz5×k\x0003Û\x001bgÇOýé\x001b·¸FÂìë×\x001c\x0013\x00079¬rY*#ìË:é\x0019\x0011\x0011ãLÄTê·\x0001QÁñ\x0011äËýËªfDõFôhàè\x000e\x0008GL	'à;gÂ¼Â¹I#zÌZD8\x001ecQç"²\x0015\x0013'ö­§@ÔBD\x0012¯gÏ\x0012.§Âµå{æ³\x0016#â 
zÌ;û\x0002ÇÜ,Üy+\x001aÎd¯ñ¥\x0004,ò£Ç¼sE¢ZX¾Á\x0015ü¥9¤\x0000Úñ\x001bÝtD|¿aîKFÄTêÄ°{¥ðY66>"§\x0016>L8\x00043ÓCÄCÅg~Ãks{ç\x001eê©-GD\x000f$l\t\x001afMw\x001a\B|ÃçW²
ÃËúùvDK\x000e.\x0002Í&[¬¸±Þ\x0004áÚ\x0010-"Îü\x00111F^EC\x0004!ºº+*\x0001/ôç=Ôb6\x0003WZ>÷ôKZôÅ\x0017$\x0004Kh©o\x0000©\x001bqôÂ:\x0019\x0011µ\x0006¢ëÞ$Ë9²\x0011ù`vZÞ²³¿_û\x001c©¨\x0012\x0005Zû"­Ç\x001foïï÷Å
ÁZi71\x0018\x0015.á\x0015\x0017$ÔËV0\x000e\x0016\x001e_¼:y76à¤¶ý\x0006_\x0007§_±\x001e:\x0019
JZÚÒ<Ñ\x0006C_\x000bk*Ïålð»õ\x001c%1ZºôH¡l\x000bY:\x001aL×J±ßT×Y;\x0013¢\x0019;¥\x0011\x000f¡\x0005
¾UÛÑ\x000cÙÑªÙ,×\x0019%üH\x000bk\x0019Y Ï¥Ì\x0019n  Qº,¸Õo\x000bÉ°\x0005/ÎY³À5Ô¨\x001cÊëtØ\x0004\\x0016Íù±TÃT4ñSz4\x0004\x000654-¤Z\x0012«knÚÞ\x00066,y\x001a¨æNeCõ\x000cIÑRÊ¥TY2Óq$ÙÀ+¯ý\x000c\x000bw\é$ÕÅ\x0013¥rÆ®aÙm?\x000fZØ0®:ç\x001bÍ¦6`=ä\x0008Òzl\x0006o\x0016FÍøJá:ù¨
4ò½¬[Nò-ä¥ß\x0002M¼¡G#\x001bU=ó~cáVªÄN¦~§KM\x0008é²þ8ÀÉl&\x0017ÝM\x0012Ò¢Ðd~	\x0006eéÑJ¦­\x0007\x0019\x001d$lïäv\x0012Î_È	3\x000eR\x001cøP(UµôF%\x0007=ÂcèÑ¼lY6Nzr\x0011-sl\x0019þÊ¥\x0007)Ê\x000c\x001dÜn?úh(?È5ío×4\x0018`\x001e[Î_ÿø\x001eIñ\x0003ïÖ}©¼¢IrðæñáéioÏ\x001f\x0000r³|ÄY
¥ñ;°¼5ã¢cV$9xsq~y9æwX¼ãÌ\NÒDåàØÜY0¹Â\x0000óúkabFV³1m\x0010\x000b¬É¥B\ÔRr±\x0005¤\x001aAi~OoO3©rÒð\x0005é¥Ò\x000fÞ¶­/~,\x000cÞ
ú"\x0015Û\x0004jp<RÌ\x000cZôÊQ\x0000=\x0017ú®V\x0002Å4\x000esW\x00141dEQ\x001cC4\x0014ªµ6)Þætû1a\J.¹Ñ×wï<\x0003©ZÔ`Àè¹ßÉÆ`@\x000cUþÇ\x0019U×ÔEZIQáÈØ4\x0014\x001bÎX©%¢,tYS,ê¼Öoðnüì\x000f*ÅH\x001a\%\x001d²>Ktrc!¢VRüÌü/
n%ä:"©	Rík½,i\x001c¹ìµâ<+zÌ\x0004û^âÒ}­DØÅºZx\x001eVû °áÁä8Vq¨H¬lS-%üi¥]jñ¬·³\x000f|³ÑøV\x0018Ðßd}!Ë%,V»Ñ||+)\x001e ÖÛÙ¤¨ãÆKª#W·\x0002^íÛ\x0008#!ÃvRýÛ0MQ²ÌóJJ\x0014f±ûÚ¾\x0006K½!Ï'UrGFP\x000b6ÉÜÚIñ«·ó?ý\x001c­Tlb\x001bFqOô²W¯þýðôÛ7Ì4ûL\x0013k@À\x001däËÇÛÇoû® ÎËU\££gÊíÈX)[wæeí
«@À%äìÕÉÅÕØ\x001d¤Òy,\¢G3]üñPf(k¨äÍt/E Zápþá\x0011=Zá¼\³¤³+q+[\x0010\x000eàÅË\x0016ðrEf²@#Q\x0010Ì²¾
°E\x0011\x0012óþe
¥\x001d\x000eSyÞÎ3YZÞspå\x0001:Ið\x0018^Öz¶ÒE´©±¯¦4.\x0015x,é4®fxj6¸WòVº\x001e/=Zép\x000c\x0000Á¯iXI¥p%Ä\x0001Çv:t3¶\x001d|ERÅ«ÀÔ\x001cFV.½l¨n¦C3æØ\x0012
rZ¬«8|f¤³:ä\x001dÃít\x000eéÜ7\x001bYsÁ¨kpÏ8ÉªlÉ,¶Ó%¤KóÞ¬ÀT\x0001½X#+÷²\x0001¦
\x0017\x001eÍl®6%ê"mZòF\x0016îeým3\x001cÎ\x0011¡Ç¬c8[$1iå¸f\x0001®XË]ÂÀ\x0001=Úé¼l:¤cU\x0006¯%3\x001bíò²ôhÿ$4\x0017S\x0000­Ù\x0015êÚ½ìÌi§\x000bH\x0017æ\x00133Ìf´ÔY»ü½b%0=ÚWÎJïöø1õÀY"ËÐ4×g³K\x0007\x001bM±.¦+úÃàÑyNÑ¢\x0006äÒª§¢ñV½¯Wõ²cÿ\c_s-É_Õ·Ò\x000b\x001a\x000eÃë/7\x000fÏ{\x0013Û¦®P¶8ìØö5A»=p}ðúìøüz/\x0012nÖ:Pg"ÓTÊA]ªº"ªö»¦í½ÖðÚÝ¸J*K;ÕJZ¶\\x0010·G­§"
*9&"Yékï/\x0015ét<$ùµÞ\x001a¤\x0004þéQLmH!KÐÔâøYÎp:1úÙ¼4]-HX×Þ5:
)IäÁúâ¥\x0011ª"¦cra»ì\x001fÿüçïüÜ©Þÿtóõöæ¹½\x0000Ö&ÑeÎ<æª¨¿Õ\x001e¤\x0017Y°ß\x001c_o\x0016¥ÕvKùÅKP°Ìq6¨ÆMÏ\x0001R\x001di³hý½°«³!ñXZ\x00008SL5ãkÆkÉøKe¸Ùð©æÿ\x001fpâE\x0010ÿùÿ(¨û×7ów£¿h{ÓäÛÇ»ç§\x001foÊäÛ\x001a"VÓnø
ÒÖà÷±Û®WØ5\x001f¾=¾8½¾<øñxlþm\x0019ë÷üÖfà&fG\x0007\x001c¥Áõa\x000eÌ,áÆ4Þ¶4\x0003\x0019o\x0004\x001b\x0005ÈíÈXásÍ\x001bÑq]\x0012oO#p\x001bsD7zé2\x001f!ÙÉ÷\x001f0ë±ÊÂYÌ´Ï´Zº7à4§Û:AW]\x0012lÍT\x000cÍ6äx/FYbÞÐ%enlÐB<^`=\x00198iïÍw²n\x0008Ü+\x0011{ýëÍãã$Ù
Ø¶\x000c.K¹¿¶b(T\x001c-`{ýÓñÅÅ.a\x000eo Ùç¹8\x001dñB©A<\x0011ê³`vwèFLÅÃ\x001b\x0007¾$È¢/\x000bç|Kj$÷Ð\x0007~K³ð\x0012µÁðêüÑ<1Vo\x0005¼¡ñoÄc\x001f9$Ñ\x0004\x0001<é\x001bÓj´X·\x0001oÔD<«äV\x0011niäiÕhs\x0003\x001eÆ»¢¤$$KÁ9ÄË58¦æÐ\x0000GZÍâÃ~\x0004ÃI9_î81^rf/æÐ£\x001dÏ\x0005*» ±@£¼];Ú/ÑÀ\x0001~­gí>ß¢ì«ã¢@X=ù6\x001d+znÁÃj+íæà¥zn </\x000b%\x001a/VÚÉ¶ð)
sørå^\x001au¢\x0011\x00158À[nY6å"¾
#b\Ñzº#\x001d-\x001bÆËQoíx(Hv<Ä/×\x0001;gåÜÐaDä`\x0002ßÇ?þüããÖÙ\x001f\x001f\x001eÙãS)\x000fçX	éj£\x0002Ü¿%s¨Ft®0ÛÿãùÅ1=¦\x000eÚc3Y\x0012ý%
Ç*K­:m¢$\G\x0015J\x0004lß(g#WL\x000bL²Äë?û´£>b\x001aØÐ\x000c\x0012\x000bÌ¥EYØÕ9D>n×\x0016ná\x001a8NÓ_d`ÅcpáK÷&¾HQ<öa´Ý~*\x0017&ôµNS¸`k³ÞÎÎA\x0000³uaGÌ20ê\x001c\x0001&±NX±TÃù]­AØ®ÏÞ\x0002°\x001f·\x001d,rÐFãÜÏÄqa+¹-?fg÷}KÿôÆÐÅ\x000bOÐÞ\x0001úãã_ÿ×v«2àê\x001fº¶!#baL\x0007î\x0017'ã
	\x001d×`tÃt.\x001cìÃ\x001arÖHk\x001f-\x0013×etùOæ\x0012YÜF®d¤ñ&pèÚ&\x00003£\x0007ÒD®Í+à4.,4
,M¦c¹=cCk
fÔ\x0007ÈµÙ=:KÉ¬&¹{Zæ¤S(¨QÞ©\\x0003K1«ä"	«ö/\x0005]KWT\¸½ð\x001f·W¨
Õ©n4ÉÕÀA5ækOÄByÔl%pw9Æ
F*ÌÀ9(¦V\x0002\x0007ê¤öå±±ÌÊÍ\x0013\x001bª\x0004\x000bå,f`üíöùë¶hÖÇû_öbù\x001cùF§qhç¢2Q0A6s¿¹8~÷f\x0002ØP©s*XÐ\x0007²T:_­ýxc*\x0018^g\;ñ¤N`FÌ\x000bÕ|©í3\x000b\x001aÀ0À\x0014_%Ê,È\x0007	;ÌñE±÷>´ñL\x0007Ûl~\x0008æ<ë\x0005Ó\x001aEBÓ¥TÖÑ¨ÆT°á$²É`>°~\x0010êp\x0001U\x0005VçpDüf2\x0018ÒÖÚ6Áe7?Ö\x0017IG~Ìâô\x0010L\x0007ÃI£ôh\x0005\x000b,K\x0001Þ¡\x001duxò¨\x0004J\x0003\x0018v¼öMx\x0002¦Ämõ¶úÓã^ØT2\x000cÆkÛ¾ËRä±98G\;±cÁF¦ÈM\x0007sXDàt3\x0018jR	\x0019GX¶^°ìh,j2\x0016¹ù®\x0015\x000bgM8vxL*#il¬×¨{8\x0015l8Óg:Xír§½/5±Ûü£±íÉdC%ÐédZZ%àM\x001eò»\x000cµªÞ¦,&mêPL}JæµÁ~[®÷^^¦Yè]hôóuh*×\x0015S<7\x0011,ÈlB\x0013nLPè8ÌsBcÏ\x0013U\x0011\x0011öz¤×i\x001fÙ\x001fù×\x001c)%nH¸£\x0017ã|xP"»=ªÿÅÈS\x0012¬¼}~\x00147Ï¯Ç\x000f;ªMwl\x0012U0\x0012\x0014\x0000§'ÊíÈùÜ9=£Q×iX/F¾LÃòõô^J\x0010]0¦º<£y¦iXÃàÎd,[£a6óX9çë;\x000c£b:Ó¨HT\x001emX¸DÜw£C
9åê néliãzRÄm|\x0012½°ì)©mõv¤{:×`\x000eßd.\x001c\x0000Æ»Kë*T{m¼\x001d\x0015÷È¾6¡ËKs²õ|¬åÝ~\\x0018l"¥údÛêì®rM\x001d×hVu\x001a\x0017Íàn·]9pç=Xú@w7rÁjL@(:ïázxVÏÿ~Øy{{ÿ|÷tûx7¥J«L DÑ}J\x000bRÅHFj32\x0007ÃÀoOÞ]^\Å{/ò3
Gù\x0008Ç.µ\x00066×¡dv\x0014H\x0003"º°ÎÍCLFÊ!¢v¤²1ºãQþ\x0006Dtf;¶
\x0011nt¬æn$ëÛ¨¤_Ý¶ý¿Ô½[v&·±ï9\x0015NÀ\¸_X%ªD/ÖåE­ã~ÑúªD(³X2/Þök\x000faÏ`îax&{$\x0000"	~_f\x0002Zz°$RôK$2"\x0010øG\x001bb¡ÐØh¨4ª\x0014à\x0000i\x0018]ýkÂ\x0006Är@Y#"Ë\x000fp~ÁÊ5µ)ÄÌá"â¿þúðáÛ[Å§£w×7G/v·\x001f¿,\x000c\x0014\x0007æ­eIÂ\x001az\x0008k81@òÝéû³÷G/NÎ_¾\x001a#9\x0000\x0016¹«F@MÃ¬`\x0010o*e± $b\x000f\x000bN7\x0002>k\x0002h\x0000\x000c¯0×\x0007ë¤t\x000ff\x0004y\x001a­\x001c\W\x00012\x0012·\x0017ÎdÙ\x0011K¥aá\x0013#^ø@/ÍU|"7õÅéÝImÄ1G\x0005Öö°Ãk\x0005,\x0007.7\x00012ºÊs!Ær8\x0007IzÃþð86ÀgõamRQ\x0011\x000cLeG%\x000cG¡ÃoåD?J\x001b!Ä¥Ì¯#dÇRá\x001a:\x0012jqÔ¦\x001eÖðpRµð¯;þ÷øÁëÅîæáaét­\x0014\x0014Ø%\x0019l\x00180\x0014/E­*ØÔ\x0001\x0001\x0002¹^]^N®3à\x0010Ñp×J¦­ÆN#ÉÁ!µPOICRö'6ÅÁ\x0011ñF2\x001d\x0002 \x00142°|©êO
õÄvr¼e-\x0018dü8ç[\x000b&¨«H9Êð\x0001\x000cï`¾QçË÷~¬[[GÆÁ;n©!I£\x0014áÓMfKæÉ~r\x001føåzT	F£r±ÜþÓíÍòKªðÐC!\x0005(jÃ|¡ÐþÕùÙ¤ìa?ÿíg5jl{·{xØ}¢pê»ëÛÛë£w_\x001e\x001e"*\x001dXÒ\x0018Î"\x0018hKÙþ\x001cw''¯(ªúîìôìüüôèÝÛË÷Ó=D7üGíþ:IüÍõýçë£/²:,ê²%Õe\x000bgL³½ÃoûÍéÅëÓ£·Ó¬·î#+$ûÕ\x0010#|\x0013agÞín+2\x0007Jæ,s¤å@·$þð\x0011ýêèpâ\x000c{óÍÉùÄ«×\x000f?>`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz](https://adresse.data.gouv.fr/data/ban/adresses/latest/csv/adresses-07.csv.gz)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=¬{TÇÉ¤v\x00068mfúÀ;KZKß½9<?^ß\%¤\x001cvÀRÞWägUµsÔÒÜßµªTýx(9år'Öre[j¦[ÉhKF;° sVð¬\x0006¦\x0003µËÇÔ\x000b¦%¤/!ý\x0000¤0<A\x0019·$¿ô{íÆ3e\x0017d5-c\x0002ÍÇ¼Õ
^PÌí\x001bÚFQ%\x0013:®¬­Á\x001eü££Ú9T?Í 9yè§qH8 ï¯÷\x001f¨Yòt¸½ÿíËÏï\x001fþïU½\x0011\x0018°Û=\x0012 $Ïð°Üm¤i4\x001e\x001eºzAýÇÃíÕ«7Oo®ÿíÍÕ\x0005úYb¢Çû\x0016z±Õ\x0014f	\x001b,Ðz\x0007\x0012_1-Yð!x)«¥Çnw4]\x0017\x0005ï­¥7ãxûj$C[ôÍgî_ï\x001c¹uçÄU¦\x0006:w\x001dVóôºi\x0000\x001a\x0013¯Ç\x0016ßÖôvóâ[Êw\x0008ÌR¡5¤\x000f¯}ûþÂâ\x0007QáÇnÃOº¨¨Á®Úr\x000eOÆÝb\x000c=Ã$tüç6ôh#SND`ÖJö¬¢Ê(\x0013­ä®øPãÃV|å°d|ÂWR:Ê
ËøéÂ#^É]neG\x001bI\x001bGäÙïÖñM_´;Æèk£6\x001b\x001cË¯å\x0002SÁTR\x00177\x000e¥~DK`pãø\x001aßo¶8\x0006Ó×\x0013¾²ì«¬¡K\x0007ßÐë\|)C]{\x0015ÿ0Õ^ÍáïNï\x001fÞ>Ü¯Ñª@Kn	°YîÄ\x0004òS(ðs!5üÝñæúÙõU{F+A\x001bWB\x001b7\x000e-±4ÁçwF\x001a\x0012\x001f\x001c\x000fõ­(¼\x001bÚ@

\x001b¨Tí\x0006r\x0012\x0014'ác|~éAi%tß\x001a\x0011:ÔoK\x001d\x001cM\x0004\x00158i!IÜJ¡9Ã¡Z:>\x001dÔ`Ï®âñ\x000fÅUüÙûímJk¾GkÁ¢ô1\x0000\'´|9{v³ô¾Ï²¤\x0003ÑÒ¥\x0007¤øã(\x001aB­4_Î´\x0017\x000b©ãK!\x0015ÍK\x0019° (A¾¾|<}ú´Î A¼á¤ß]Z)Ò$u\x0005|Õq~A]íõÕííñînI\x0017Æ'¥ÆYÇ.Úßú\x00151àW\x000foÿ×\x001eî\x001f×!k#X£BXIÉNeR\x0019\x0006nU×XÙy«F\x001büêúYüãë«ÛË\x001f03üú|<EÀ\^¬5Y\x0008Õ\x0004?ú\x0001EÜ=ý\x0002vë\x0017È|eIv2m\x001b)ùÑ\éÐgÿ\x0017óFS17\x001e\x001f~ýûÿ\x001c¾ûòëéáÃJpÇ\x0012=q»k\x0012úTJ\x00197|;w¼~G3Þï_¬\x0000V%°\x001a\x0007¤LÎgäRtç\x0016Æ0ö\x0001ë\x0012X\x0003k®I·Òð½&úÀ+\x000cí\x0014d\x001f°)Í0pªnÁs÷n\x000cÓ%¯ðÂI\x001f°-í8p`5fÜÃ©4\x0002+÷pûõ´\x000fØÀn\x001cXðP@\x000bGXÄKå\x0015n´Ñô\x0003û\x0012Ø\x0003K¹1\x001d:ÊþÆ\x0018:¹¶Wìã
%o\x0018æ5*\x001b	l$d«f\x001b%AÝÀó=\\x0014Ý­\x0003ÄZQÚ,n\x000eÏã86rv¡P¡WV¼r7ÞD,ó*\x0003\x0018½I^á½¶0T~\x0003Æ\x001d\x0006j°3ÞS·¶\x0010KÀ	íý¼Ûq¿¡\x0004÷Y!8'\x001d
Ð¶ÎÌ0T~\x0003Æ\x001dTÜ\x001dÕVd%$\x0017hÚÝü\x0006T~\x0003Æ\x001dGôÇx-Ïß;YPgï\x0003®ü\x0006;\x000epO\x0014­0%$»&aC¬õN±\x0004T\x0003Æ=\x0007XÊXÄ]\x001c£|&Ö:ÛÖXVX[baxÜiº¦Ê¼Ân/ÏqV!Êâ\x0011ó&Ø }³í\x001bÇ\x0014zAse\x001d¸±gâ ñ\x000f|ó¸ùøåáS×8\x001e\x001c@.­:\x0008\x001eØk©C\x0017+âÚ!ÅÍË7×w_Xiáª\x0012W
âju \x0011¦4\x0019C÷¤È» öÑÇ«K^=º¼Öñ$,\x001dm¤åµ\£é+ûxMÉkF×WI¾@ktÏê\x000b¬Ìû¡½}ûxmÉkG×WYªÙëkx¦¢¤·\x0013y\x0017Ê\x000bûx]ÉëF×7Zµ\x0014\x0011Oë\x000b$)Q\x001a¯o;Âìã
%o\x0018äUñ¼ÑòzÇ£Þµôù¸-ÙìÂ\x0003øÉÑõõâái?$©}\x0015ÿGê¼\x001fö\x0002®Íï¨ýÕ ¸5L\x0007Ï\x000fÝ:¿9«Û\x0001|\x001fpeaÔ\x0002+§)ö\x0001qbM\x0007J±¹¥9y}ÀEQ¦ãÞ\x001f\x0004vÉ¤)gÙD,\x0015Èõ\x0001W&\x0002FmD¼nr¡¤A5±\x0014ù(Ë\x000b¼tiîã­L\x0004\x000cÛ\x0008pÜ/¡­æGëè4èÑÚ©\x000bGM«;SØÃ¡Z¿ëðkgu\x0000¾ê[¯gS¼\x0015[Ê³'ø\x0007|²¹þõ7|\x00089<hôA+\x0002µm*ª¤þã¦àÁÒJ6\x0002Ëëç¯ð5äð,þï<½¾»L«JZ5Hk\x0002@@<@~ÙåbJ¬ÈØV´zÖkK&Âlp\ÚIë5%¬\x0019uY«\x00026pQ\x001dg\x0001UKc°Ö´vÖª¬ä\x0015-<¢4gÊF\x0007@7­+iÝ ­Ïé4 ÷;7\x000b	*ómGÑêKT?º
\x000cEê\x0011\x0015¨W	[ê¸\x0012X5\x0006MöÒÎ\x0019Òbd6¶²S& d\x001e½\x000c:\x001bF§B¿ù*}D2aø1\x000bx¾\x0012´ÍåXfnÈÂô\x001bsh3\x000emy~\x0010D|ÊXýjDÀ«Í¹`!Á ìï\x000fÏ\x001fÞþr¿²¬YJ¤\x0006B»'T4á¸PU²ûÉ
_\x001d_?ûájA\x0011ç÷~$rØpÓ~\x000cBø¡K;NBÄ\x001d²\x0017²ª\x0016Y
/òÔqã	YqÔ\x001e
\x001adä\x000bÁÎjd/Jd/\x0001(ñ\x000e"Þ¨ Ú	ÛµhÈt#\x0003TÈ\x0000ãÌ:7:ã@ºÞ+Ç½Ã¨îºY¯73&ÏWþ÷¿þûøøóº¢	pZp	\x001eNäNJ\x001f8tò¥jä¢\x0018
?]®HÐºÖ\x001b ei\x0014bd,!Aç\x0000SÊò\x0008«¡m\x0005m·@\x0003_9B\ôq\x0016e×¬l
?\x001fö\x0015´ß¶Ò&1+C\x001a	¸Ð¬¸\x0003{­³\x0012%²\x0012\x001b#(Ì#\x0019èhØ\x0007ÆÍ±×:\x0017Ú5\x0011º®é¶Ó}	G"òpùV/?±¯ý6bRÏ\x0008\x0010ð\x0015éÚ\x0004¡1¦«9TG0l9háhTN\x0018£\x0007`h×xâï\x0006Q-ô\x0000]'µÓyüU¤v	:×%DèKE°«¡]
íÆ¡±ïº<ÎRÖÚÒ¨<\x001bÃÓo_ý\x0006¨CM\x001d¶lêü æb\x001bÍ×Õh ÷Zi];üçM­SÈ\x000f^:ªcÂa	¼ÐÐxTè¢b\x0013´å¸\x001f\x0007U¤	^¸\x0001i©E¸(×µZÕK­6-µ\x0016¬½à´§&a4ªäZÞ¾ÖZÆ?R6ß?þúpÿ¸î:¨ .vo
ô ­¸1^U\x0016^D°ýûÛãO×W·\x000b\x0017Bæ%¯\x001cåMå¯×òòY?6Èeqõ¼ªäUÃ¼À5n¸¾Tô¯ü,k¾ð\x001eÒÇ«K^=Ê\x000bÇeh0\ä­Ëë»P\x0007ÛÇkJ^3Ì«¸\x000e$^ªøÅ_±0~¡Î¸\x000f×¸n\x0014W8î®Ðb\x0012»M7yfo¸ê~^_òúa^ANz\x0012¼§Â eH4\x0011·ï^ë[=Þ$V
sôaG3,xf«Ío¼\x001bÙÏõØ ÏgðÊ©Ìæøþýý4üêÃçûÃñýÇ/÷?¯ò\x001dF[ÏÅ
\x0016ü4ðÅs\x001f·r«·öææj\x001aõâõÕáxóòÍÕë×KÓåù0^9
ãÝ@nõ¦¬áG_\x0012·YÀ­Ñ\x001d9F®Jrµ<§pÁb×[\x0002÷*+Ï5zRÇ¸uÉ­·qKTäMZ@b\x000f\x0011{q|ër5HnJr³ÜcS"ÏcC\x001dK 2M£uÜävÛ.Ò¤]îIJ\x0007'zåÍÒÈ8vÇë,F¥aNÑÄk(þsJ?á\x0007üúÛ*cÕzdÃÅ¤^?\x0019C©IXI;q©Eò\x000eÙ¿Z0	ÙÌ¹]DÆ\x000e"ã&IQ@Û$Ì¤\x00042(:FÚ\x0017ÿµÌÖVÌøÏQfÉÓL"³åew[ÇÌR\x0007«ëu¶\x001bÖ9õñ¥¾ð@Ïn\x0012\x001cX	}¡,ü
¨·/¡Eq·)C"\x000eàÆ±hß*¯îYueÆAKoEÞÑ³è yo\L+]FÖhð ÐåÓ\x0018à¿ë¦É\x0018H}øË¤#ðÓéËºk-fíxo[ ÉÉÎ\x0005V\x00113ñè_Ì{\x001c1¨zñý$&ðÓñÍmSD }\x0017õx±ýC¢\x0011Å¤SÚ;x3\x000béC§\x0017è\x001ac¶\x0017?$ÿ&/1g_rÞÇ:ú%>éiàSXß_¢øK\x001aít[¾dnéH_RkA\x000f~ÃÙOä¢=rô%ÎåßDîø%\x000e ~9^Nù1ýåûÿüõ·é\x0013¾ÿøå/ëÄ\x0000Qr\x0004@`\x001bµ#\x0000\x0017r«z!?«¿¼ù÷ç¯&üï_¾ùþjá§\x000f¹:\x000f?\x0000ÿ¹ñ\x000b\x000cÕ\x0005@¼|=±Ô\x0000â/¼²7ñßÞ>}~lâKUáKµ\x0015?î\x001cÍÝõ@B²J
Ã­Ý­\x0019\x001b\x001b~òÂÊ?BY1ü;\x0008\x0008Ê\x0010Hãæå¨õ\x001f\x0012ÜÙE\x0010¥8p@Z¤?ý¥fzt\x0019\x0014Ä~z
\x0001Küð	\x000f sXÁñMv$?~Ï:3\x0015\x001a\äj\x001byÈ9AyY
\x0001\x001b&vá\x001bU\x001b£ìºd×ÛØñfBìÎcÚ|bç^p\x0007²aAGÙMÉn6î\x0018&?m\x0019.mbçqÏìÌnKv»]9\x001a¹\x001aÿÏzz£À'8Þïº\x0011M²»Ým\wÉã\x0003:kZwÞ1Í\x0018¹X¦ÝO,[­¢ýn²q¼Ý¡ÑÕÓ\x000boÏ\x000b´m*Ðþ·/§\x0007\x001cñóöpwÿ/\x000fëÆôaÅI}¬
Ù@¾õ¶ñpñoo×8ßçÙáîêû7×\x000búÎërmªË\x001d¢E7Äj
1>cµ\x0006á\x0018W7Ý¸¾Äõ£¸1è
D«Èx+\x0007ôyÝÐ>í¥KÁ,U»á¢Ö\x0016wDíXm_Y¼l¤Õ»y«­\x000b£{W©èdâµ2?[páÅÉ3ûðêWòç³f£otüHH¯B^}6/Tg
F\x000f\x001b>Âfñ\x0019ÍB¸+ËãMûÛÆø+ÜÒ0/n¥4\x0016\x0018ÿ2¸'¦ÚÖ	:\x0006ªüPÈ3Þ#óFh\x000fõ\x0003KüÃüÌ}xþ1^4WåmU®P3`¨ÇVÛ<÷ËNoAç/ã½²½\x0011Rr2®!eôt´\x0007t.&QC\x000c¹\x000bSj\x00043þêÔÞ'\x000c%9µ\x0015ób.>\x000f¯¤?ÿ\ÿè?\x000f\x001aå\x0017T'w«­õ\x000cª\x0017Úä2è¥­9O>H§ß\x001dhæº¢Òï\x000eyE\x0017:</Æ½]NÆ?L¥ùêôåýáûÇÕ½¨xÊI¶8º[ÒCÒ©A,É¼:¾¹9|}
qË°¾õ£°\x001fk\x0004Js@J\x0000<\x0010ÄÐB	ÛÚ«ñF^/müC^Úw_\x000eß}|ûùþËãáøîãûß~ÁX\x001f>\x001eWÁKç9Ã-½
¨é4%\x0015¥å\x001d
¶÷ÄÃw/½¾<~÷òæÕ\x000f8\x001dëÅãíR'bú\x0018mËÑv	\x0015r¼FgM\x001fcxºe\x0008\x000bb[>ÆW\x001fãwúe\x000cg	¼æ
~ÐT-å\x00044®MÛ¾¥OÇoäÓwøà¹B\x0006Ô©Ms×l0¼Íâoó\x000fù\x001aWÛék$µÊË¸£¨\x001b\x000bx\x0013KBL[>&Ô\x001f\x0013öø\x0018%`\x001a~\x001aEÒhàHw%þ2KÃpÆ?Æ@õ1\x0006öù\x0018e1I©5EêÓà¸¯Á	ÿ0\x0000ØáQ}Úéc\x0014Ý4\x0003\x000e[	ô-ÏL£w`ëÇÔ\x0016Àìb\x0001ÒS*3ìÀ¤§TOò\x00121_hrßò5µ\x00050»Xxh0t¢¯<`Ôåô³P
ö­_S\x0000³	°´Ñ¼×Ty\x0016@óO³t\x001f\x0018ÿ\x0018'«qr\x001fã,\x0005*\x001e'\x0013`ùkâ©áæ&½møú§q»ü42èè_²
ÉYí![çDx&}mý.Öyz¨ñ6§\x0006°ùÐèÆÃÙÖ©­³ßÅ:ËàXðIzË5Z`½ã(@.Í>Üð5µyö;\x0005hñæ\x0012È ¡¶+ý4<)+~M£<gë×ÔæÙï\x0014 ÙôôÖQoUÜh]§´ÿ\x0010æk\x001bà÷³\x0001@o\x0010Â(H4\x0002y§-I«nøP\x001b°\x0011P,D\x0017ÿ'NHÓ×(Ï;Í-Ïd\x001bþ\x001a]ÞçkÀÆÁ4Wn\x0002`²³Y*²\x001fþ\x0018%ªë3þs\x0011«£\x00175$ô
&ø\x001c=ÿ#¾EV·güç\x001eßâ½Ëa\x0000p+\x001a Ì!o3ùÐ©³4f4
¶-|­IEªqå\x001b§oÌCØú1²þ}"4ùRÞf-Q-@k\x0008ûÆ¯q\x0005Àîõ5ÔÆäQi\x001bÅ!ù\ µ«â\x0000üç.Y'«I\x0014Ûë\x000cÀÖ{N\x00076³F?F[_?\x001ebé2|¥!ñÃýã¯÷«¦Ê(\x0011\x0014Mz I&;Fÿ\x000fÑ8øe_ä\x000fW·Ï¯^7ËFíL\x0000B-\x0013Ð\x0003í¹\x0019<î'n²À\x001eZ×ýr\x000b*A7\x000b+\x0013µ©¨Í6jÅZÎ>ÆZæ­?ÅÚ»PÏóYÚ~ÕÁÞC\x001d\x0003wNyã^¡R\x001a0ùº{y¸ÌJjçJj÷U\x000b{\x0017µæ6\x0008AvDëñf:TÔ_µ°wRÓè\x00104tõ¡\x001bSÌû¡çK\x001eBã¾\x001b×9ËKm¨À\x0013k©ùj\x001a\x000f:\x0003ÔÕ\x0006ñ[7\x0008)Æ\x0005Q.5\x0010»Bä`\x00155ÊÀ×½÷]6$Wÿ\x0004¬3g\x001bâø4Æãþ\x0000¶©±7\x0019\x0011\x000f¹.\x000c$É¤DìÎl©åöcÏª?É7~¥9Ò
Ø¢êó}\x001e¼å=â/5;­ öÓÛêüX:óú+#rý~Ì\x0001¾ýkp ]ª·rÁ\x000bÒa.2;\ß,i\x001c$^+K^ûU\x0004²7°(¦6órÿmV\x0003ô\x0002{]\x0002û¯\x0014¬V\x0003C\x0016De×éù\x001ayF\x0013}ø
ÞBÚ\x000cy'i³Qà)\x0011:\x0001ãliEÀ\çBCy¿ØÔÄ_ÙõÄkÚ\x000c¶Ð\x001a"ÎsE.»5¼ÊU¼ê+oÒ³ÂÔÓn\x0002ìVk\x0006Eã³X\x001a[\x0012ã?7¬0mbkmr~Xr]oõdt\x0012\x001b]íbóµËJb£ç!ÅX7ÄsµÄ^M{Y¾eØóé\x001c!É\x0006äé¾7ÿùqU\x0001À=G*:\x000b\x000e>\x0003Ê?ÄK×Å!èÿþ²]ãÈ¨²DC¨Óì7P\x0015OI8ó-¡JÓjîCU%ª\x001aBUÀ
¤ÄÿZb3¡Rûo{ã3ÔÆ-IuIªÇ~'é­#þ§")\x001c\x0008ÜØí°\x0017dE5%ª\x0019ÿý=-jÀ'ç¯~ÿ\x001dÖÔ vlMµ¥@AAd6)ðÁ$ÿú-Õ©>R_ú1Rcò>EYêáPWúFB¥\x000b´P>
iìÆÐ\x0002å~Lí·\x0013)·\x00128Õ[ìÛ§PÙ)\x00183Tñþ`GÔÀ\x000fnÞÖ©)nGÕ²Ê±eÅ]I2;n\x0000A=\x000fr:¯i\x0007¸Æ\´Î\x001dPÍTH»\x0000ÿ2´¸\x000e3±É`9NÊz+³Ãj<­#vúÌµÆ? kåvÌW§O]ªæ>q©â\x0005FS\x0006`YS#Ôr\x0017füÿbÎu¡TyW¤´øOÅCàáµ³«V»\x001aL7­*iÕèÚ\x0002wIÌU\x001aZ[Ik«­ZP°V´zÖNO;ÓN\x0010[&µ	Z$ûÐÖ\x000cÒªüU.Py
"Ëù\x000b²ÿ«imIk\x0007ib\x0002­mé
/\x0008º¡*Ñ
ëJX7ºmsÖTYC©¼¸mY¯Ô¨\x000b-þ«iCI\x001bFMB~ÎÃN\x0008CÛV\x0001oV!L/í\x001c"LæVî\x0004Ç\x001dP8OeÝ]\x0003<i7ní\x001dFÝÊ5SÊ3ûeT#ôêf­|\x0003:K±-¶­ÏÖ6¨eiÕ´µAsëcØ¥,\x0004 q\x001f\x0015B]ÙN\x001b¡2`0jÁ`ùIlâ\x0003\x0013ÉqBCñ`5®ð¦~ÖDîòYóËáÙéñÝÃÓª\x0019\x0004\x0018 r¬ã\x0008&+¸ÛÞKBDo\x000eÏ·ß]¿8. HÈ¡B\x000eÃÈI\x000c\x00169Æ\x000ei2<\x0014Ú¸Æ\x0016î.\x0012¢\x0008]%D{©±P\x001bð¦ÀÙ}D­\x001b¯ö\x0003Ô¶¦¶ãÔÞM
q)\x001447Hðwt\x001b\x0017ë¡e½¥åø\x0006lÅ¡Ö\x000f\x0019£\x001eT¥Ê®Y6føõS;/Kjüç(µNDó\x0018\x0002x¢)¡«¨LÍJÙ¸\x000eõP\x001b;½KÈbX"ætËY~ß?¼ÿqÕKÖç¿
ë
iB½>Ò\x0001k¹¾y(Þ÷×77/Û\x000fUÄ;ï
äUb7F\x0010ø6ñjN=(-iu\x0008\x0017çÕ\x0012oëlÏz\x0016\x0011×âj\x0013ï\x001aÖ\x0001OÅÓ\x001b,\x0005,4Êt¬n¡-¸¶ü\x0010/>«ÑêÆ[¤iË6«ÂÁÅÑëv\x0017s£--ðit\x0003\x0003N-NKìÙ_G÷G]ÖB^Ít	\x0019àL=\x001c}H9&ñÓÃû_VâZ©Ð\x0004£ðO¦\x001dá4¿ù\x0008w!,~öÃñúæ\x0012÷Ü@0¯+yÝ(¯q$J\x0017yYþ>^DUæmô\x0013õó7òZGï\x0012àHò¿Ê\x000b\x000e,kd&»qç°\x0002q«)y]¼ÁÑ½\x0003<Î­Msº¼¦÷)+.Ív\Í++^9Ì«yV-úh®uxýÈûa\x001bïÏ"Eó¹\ù)¦:¦yF\x001f?ßT:o\x001fþúñáq¥ü\x001a?#Î òóO\x0008Tùbb\x0004ÚxÇ~ùúên\x0012ê¼½þéåõíð\x001aACN\x0003OÐ0)¢\x000eR[\x000e%§©b\x0002è\x000eb 1pØÖÄv\x0003±¥Fj
âÒ\x00134Ë@jh8uP\x000bïU\x0011($DÞ\x000e·÷\x001e>}>}x»ê}X:¯xL%VÎ9nÿË\x0017§9 êT\x0004¾¾{}|ñlá¹eÉ-·pG;§}®»§Ì;¦¸î~©É«[Üj\x000bw0¹Ë±¦2h\x0016CÄÎ=¹uÉ­·pÇØZê¢\x0005ô´Ü<£\x001bËB\x0017µ\:±mm7-· gÚ©tu'LnnV1c}ÜÎ?Ô¸é¡f¾G½ºÿüðùpwzøðùðãO«´65<\x001a\x0006\x0014øY\x0004ìÒûÕÕëë×»ãõ×\x001fßÜ-øIw®évæÖoÀéÍ¤©Äú2Wø4Ä%¶ð«_mç7ë]­æ©é \x001d\x0017ÚEWº\Ë8ò
ºü\x0006½ý\x001b\x0014ë\x0011K+=VfNßÀÃP-Vîþ
¦ü\x0006³ý\x001bä|\x0016P°~\x0007:äEã­bË'Øò\x0013ìöO\x0010ÕIð?n\x0017HÈån
Ù-àÊOp?ÁdQ·,\x000e
c_\x0014
Ýý\x0003|ù\x0001~ûo\x0000â	fMÃ âOÀÓpÞîî\x0010ÊO\x0008;l#® \x0015!ª¼DàoØÝ\x001e\x0015/b.½mþ\x0004Å*\x001dÖ»lT\x0005§7ýþ\x0019jß¼Ý9\x001b\x0005,ä¼duø\x0011ô3\x0004ã/åðû?¢rÎ°wÆY$t¤ãM\x0004bàÁºv¹Æyä\x001b*\x0007
;xhËÓÉc°á¸8Æ{¿áBGÊÈGT\x001e\x001avpÑZP·µû<$6[Q¤g÷?Õ\x001d\4=sZ§YFHêÙ*]|\x001cêþ\x0002UiµÃöÀÒÝ6\x0000\x001dÁ\x001co»F6jË7Ôñê\x000eÇ\x0001\x0007Ü*sô\x0014Ô{#\x0005?àzß\x0010¥Øò\x0011SÛ}«OÑÃQº\x001cjðKRPúÚ
\x001f¡«Ý¤wØMAású\x0018Sn\x00058ó\x0016wØþa·®¶Þ¾ÐÍéìå¨S\x001b?½ÜÅçÓþo¨\x000cÞn°ÑDSöbÖ\x0013k\x001f\x0003ªéìý\x0011Uä­w\x0008½q¶\x001cí&Ô\x0004¢#aC7.4\x000f|«â
·G6ÀfðxÄS1:
±Ý1!\x0010ÝCAçYb~÷øëéÃ»\x000fë\x0012¼F¢¾GÒµ·\x0004:ÎZ{-1ñnÔèN¦åa÷øüøâ»ë\x0017K\x0019^¦%µÜBm2µ4dI#5µ¡Gê¥±ÐªV\x001b µ§WyùN­\x0000ñÏ<Å-Æ\x0012ß¶:CÔº¤Ö\x001b¨U 2`$'h®°6ÍÉ½CÐ¦6\x001b c°.õ¥H)Ç¨
)Y\x001a+\x001aýaCÐ¶¶\x001b ­çõ
\x0002öMÐFñ¦ö
9á!jWR»qj¬\x0008\x0006:&\x0006ù¨\x0003eCm\x000eQûÚSkgXÆ\x001dÇ²å!¾<IËì¹«C	\x001d6,µ2$å?íjÖ W¤Ì\x0016·µÚo\x0014\x0015vèaÄïc­¡ö\x001b\x001c£²\x00167srÔpu¼Ûì\x0018÷Û×P9FØà\x00191²M31\x0002¡ö\x000eÙ¶ÚâF+¿\x0008\x001b\x001c£;­ç\x0018d¢v\x0012 ûÅ¥ñÎÔ_
1z>I-¦\x0012L\x001dX0Ýàÿ³\x001fvå\x0019akÔ*×z(\x001c\x0015O#©-Õ¦ÄÓhv<é
¶ï-®/ÍØó¨gíFðñV\x0010o
Xë¼
;lzhÞQR%&Öìr$"&Ü¿þø&Þ\x0011¦ÿ\x001f6\x001b\x0019ZUÐêw\x0001]êeë?\x0014rÙýÐs®Ò&I`úÃÆ«ò·[E\x0004mu	mõ\x0016hOB1¸Ö¤Mï9Ùò-*\x0014wAW+m·¬´\x000e$w\x001b·§ ©x·Þo©mEm·Pk®yF
óR|Ñ]\x0016éí¡vÕZ»Mkmèu\x0015bG°q­%Ý	¦\x00014{Q:l 6ÜÞ\x0008\x001a\x0007\x0011%c-=
é4Ö.Ë;÷PûÊìù-fÏ8JÏ\x0002v\x000e¦Yz(LW]«Ä¢øy\x0017uµCü\x001d\x0015z!\x0007OÖ:pj1PÛ:T§1l9Y&n2|©~3RÀi<Y÷Sð%5þs\x001cÛ)ê#1\x001fCj%hw\x000c°\x001b\x001dÜÝ\x0011oÍ%5¸
Ô!\x001fG¥¸Y\x000f§Ùqì\x0014lõ-ö¬0aK±\x0005\x001bJç\x0014ïµ\x0017;4¦E\x000e`«zµÕÕ\x0006\x001cq\x0017;
ùÕÊäYhä&\x0007¨M½ØfÃbCÊ8¥ÅVT\x0002®Í;;Àn{Ä\x001a{§±\x001eµ¦O«-iµ}Îê\x0000ví\x001fa\x0018V\x0007±UÂÆf½,AÈGâ_Æm p³JÕR8mc?Xª¬^g\x0000}\x0010gåàAÌåà\x000e·\x001fßþ²²|\x001d\x0015WRc4Ê²â\x0006\x000e ñ8±8µïîpûòÙ\x000få±*KT9µ<\x000c¤c·é\x0015ÉÆ@ùNTU¢ªAÔÀ*\x0000\x0006»©iF2\x0017\x0014DÒ¥²éÕ¤º$Õc¤Vó\x001b©A¿#P.³aé"»Ô¤f\x0014XªÓ³CÔ¼¨j!d^jKT;êÐ­M¨À#P\x0015\x0004®\x0011kÖWu¢º\x0012Õ
¢z²UqU\x0005Ý¯qÞ´bÔñ\x001d¨¾Dõ¨;º'	IFåZ`ënzëQC\x001aÆPQÑL\x0015\x0018V\x0001_ì?X:¿@L\x000e@\x000c²*\x001e6\x0016/\x001dÜ	ZSâM´!¿ÕÉZ;«Ao5«cËn* UR\x0000¯«[
\x001d×³VÞ
\x0006ÝsO\x0018Uà\x0010ï*tq
òjÒÊYÁ ·ò!KÞ
ÍÍ®\x0012\^Õ}vkå®`Ð_9Ïb\x0014:x6\x0002RpÅ$ÚÖ=X+\x0005\x001eËë'V\x0011«¡±q]³mµºÂNÖÊcÁ Ëò\ ¨ÕÎ¨\x000bCSÖ£V\x001e\x000b\x0006]VÜ®^\x0012«¤¦4Ü®ì\x0007lCÒ®µrY0è³¼äê-í=»×¹âÝ.ÏlÏ¬Ë\x0017\x0001¨\\x0016ù,)\x0004w<¡z°O¬2\x000bmY»4 i5ª+/[´\x000bòe«sqCXÒÞP\x0015»\x0014mKÜåFp\x0001ï²¨\\x000fú\x000f²,]¿?¼z¸|\Õ¨0íÆQÄ]PÔnâ^6\x001cí¬Éüêúêöv©!1\x0011\x0017u¹H¬Â 1¦ÅÒ=ÖHÅ"¢ë'M+Þêæµ5¯\x001dæu@I(\x0002v,áã¹\x000fñ<Yc"®Gkô\x0010Gû@\x0019<J¢4×S@cF&¬%®×Ø\x000f¯1Ê\x001f¤|Òd}i«&©CãZånÝÄ¡>waôÜ'¢¡xÂ»8\x0003ËFñD?p½)Âð¦7]*(tÜi\x001b\x001b~súg×\x0013×"o\é¡£ÍÈ\x0003}&¾Pi½X)]\x0012ã?\x0007
*Ù¶iÎ/FâK\x0002ù+uµÆJ\x000f®qüq<
ñ\x0002\x001cýDÀ:\x001b\x0014­qCT©ØÙØÙQbÏ3l\x0001s\x000bT\x001fãÀÄj§f¾8aâü '
ÉKÄ]±Öº2nZ\x000f\x001a·8åï¢\x0003\x0011O$01\x0001Û3ÒVoãYº7òiðì)Î\x0002Þá\x00029=­ÅÅù\x001f9Ó@øj(Ìépwúò×ÓªP\x0013×ø¥Md9beT®L¿Ð4iJÜ\x001dßütÌ\x0001ò\x0019¬®aõ\x0006X­)Q\x0006
+QRöIyÁU°êò¬®\x000b°®u\x001b`%¢éu^\x0014¹,©1ãv\x0005¬Mb?³Ò!VwB©txx~z|ûñËª³f%Ð°(\x0011f=\x0005ð@öLéÆ\x0003ÄúüxûìåÖ\x001d)ñâ\x000bTÁ;
\x0015\x0018âa\x0002ÞqiOHãÇxK¼\h·^«\x000c¸øÏA\\x0013è¶ïÚ©¸$aöÈz
OvÀ5îènðXV,¯Ðûu0\x0014W*ßPàëå55¯\x0019äE\x0015°Ôó
Âóè\x001a0\x001aÈê¢dê.¼®æu£ëëX½\x0004ð^GQ°\x0001a÷â\x0008£u¼¡æ
Ã¼©Z\x0007£÷Ôx\x0010/¡\x001cêhqqBÔ2l\x0008ÓXÞùÉ7 Y\x0017åYût@´U©\x0018+LIO)_k¨ã@:çÈ©Æ\x001c£Ì{wÀÿÍfºGê³\x0001!R§\x0001!<Eøôå·_"ö\x001f\x001fO\x001fþþÿ}|Xñ\x0011À\x000fkÿÑ«\x0007ä\x0011Ëo^ý\x0010Ùÿx{|ñìåõÝWîuÅ¬ÿµ:+\x0005àR\x0000jÒüøéþ·_Öùba©5BªÀÁÊ*ÖLv\x000bÁÔùòîêÕ\x000f\x000b:+\x0007@\9\x001b=Fº"¾é\x0005×6*ÞûyUÉ«FyQô2áFÛê¯c\x000cÉ]°Ø/±\x0013®.qõ0.ð Zå¸ô:Þ¸Uæ]\x0010ëã5%¯\x0019Þ½fÞE^ÅE\x0017îÇ\x0011·5éÇµ%®\x001d^^ËRÑØÎË\x001bø´é\x0005\x0005ß>^Wòºáåõy E\x0011=²\x000e·n\x0004êý¼¾äõÃ¼,­¢/ÝØXk_5ÂÉ~ÜPâQ\ÈÏ/ÊØ'tÁ´mjt÷ãBù\x0002Ü\x0005?À\x000clbC÷bÕ÷FÓ&¦Ëh\x001b¿M<ç\x001fÒ6>.´æ22e=¿QËHpvæFdiÏ¼\üC.zqÄÇ·8ãðìônÝ`eýY'"í\x000e-G0´\x0014ö9xù\x000cs\x001c\x001d¿[­ÌØªÄV[°u õP)Bµ\x001a¸`ÏÀR]A/µ.©õ¦Å6X\x00031akw¦iäÉ-F.\x001cÅnlSb-Ø\x00108ºá#\x0003â¸æ0.ö[ÄÔn\x0003µÚä-"É©äYÀ\x0006\x001ayµ!j_Rû-Ô>à\x0005:a[.A{$GØq±C\x001d¶`K>'\x0001JÃÚJF.U$u2ÏWd\x0006±ixLk[¨¥icË<hGÓ7\x0017©MØ°\x0005\x001bÌ<PÉ\x0004qü¿0/÷r»@\x001fwåi`«'\x001fDnO:bñDR\x0002.÷~Ö\x000f*W\x0003[|
\x0004\x001eÎ:Ym¡©*ÈòÄBÝ¸+g\x0003[¼4YªzríÉ\x0002Ê øÚ²ÜÛ]9\x001bØâm°\x000e··
<â\x0005B6Ü-Yª!n[qÛMÇE+$>7PU¦ÎãPa¹¯¤\x000f»ò°ÅMb;\x000c\x0017giÃ¤6
.Ò5~OkRùIØâ(Ñ;

¶¥Ç¦è\x0014Kq{ Ë\x0008·¬ãí-V\x0010fV²&­	¨\x001c\x0002º\x000ecÒJ\x0012ue\x0003å&\x001b£_h|Xð8à!í\x0012Ç6Ä8V»²r
\x0004Ü%iµe\x001aL1qça~Ú-¤\x0016:[?ÿ\ÇS?o°&Å(U\x0005Ùéä\x0006\x001a¢cqàßÖäo·¸\x001dà\x000e\x0005\x000c¼=»\x001dÈ÷Ríd?ù©&?m \x0017u\x00158j\x001fUè\ìqe\x0008ö<¯nE=qåîãûÏ_Þ­*yÐ\x0018JYÜ\x0010¢\x0005\x0017×ê°0\x0011¸_Þ\¿~óÝRÕÃyÚ!\x0014i\x0011fàaJ
ê@Ç;Î\x000b½T¾ÞÇlJf³Yq+CtêÜy\x0015ÉßhÕ¨-\x0019av%³ÛÀl8o-ñYyÒµnÉÅ\x000e-sûz.¾\x001e#×D^xwN	ãfß\x000eºÊïà\x001fÊfÇ×÷\x000f»\x0006äÃç\x001fVºà\x000c\x0006<GSóÝÌú\x000bã¯o¯®ÿt\x0015MÈ×/_´Õ=ß'ö²Ok\x0008\x001eØçèàp"2Áç:ýFåb'¼\x0008âl²JüCÝ\x000fûie¡~pÂ"V)w\x0005ªª\x000b¾1«w®Ó¿[Ò¤bP]ê\x0001P|¯'ß\x0012IÝ\x0013A\x0002'Ê9&½Ø
½Ô¤fT\x0012¦ÔI­Æ12ë1mi0ãñJC§\x0005eÍ)\x001dòz^êÐX\x0005êJP7\x0004\x001ay4/)ÏmÇ\x0012*ªæ	~c5¨/Aý\x0010hu>K8\x001d7\x000c\x0004o.õ\x0015.z}.- ç¸çË\x00014j!¼¿2VÓÅ«±\x000f\x001e\x0000Bî,½  Q
áææjAíyeÉ+yE~Î7Ó'xenÚ\xÍê\x0004V%°\x001a\x0007¶ÜdnA\x0013°ÊÀ»ñêWóJÎ\x0007\x0018tÂôåçfã$ä\x0000±)Í\x0016b®\x0012<D\x000b\x001f8ÙÝ:µ\x001b±-í(±W\x001a¢`ËÏnoÓÖ]P\x0005ê v%±\x001b'\x001e¬\x0012±á\x0006díuÞ\x0015°¬\x0008ÔAìKb?N¬©øs"¦»v×²n¹®«8ÄaüF\x0004\+¥½ÈQã\x0005\x0019 õÀ*®Þ~zqD\x0014ï
ÍQº¶!<±\x001bríîýB\x001d1Íó#¬vY£Äe¼\x000eäÊãÁ°ËÃUö!#sfÂ\x0006»?råó`Øéa¥	ºÑqWÓ\x0013v"#7&\x0007+·\x0007Ã~O9 .\x0007\x0019\x001dÕ\x0007+­¹e}qj\x001fqåD`ÜÄ(2)\x001au\x000chµd|á§\x0007¹ò"0îFb0DÑFÕ%Å\x0015jDÜi0@\y\x0011\x0018w#V¦\\dÉ"!q3²Yê¹ïC®Ü\x0008û\x0011\x001c»Fì\x001ce«b Ï\x0016n©
°XV~Dû\x0011u¢¿£ÆÉ¸È9HÖËõ<=È\x001fã~ÄøìLv}
Ø^èÝ¶²¬²\x001c7Ê&\x0017ck¬é!\x000b'³*Þ-êUd/C{o $Î\x0011í³ Ó'ùõÆê\x000br¶\x001dÈã&.y
0¢æU\x0006Ã{Y-iàõ!W6NÛ8
Ù*ÛÀodZä\x0000C]ûì@®l\x001c·q8;|\x001fvÇ\x0018Fæ\x001bTk\x000c]?²ª\x001a7rÊä\x0000Ãê'¹@4/òn÷jUÙ85nã0ÅÄj^älU£;|\x0000¹Õx¬¬$¢MÈÔp\x0012²[R ì#®ÓCãVYz\x001eôªÑ§(~\x000fËÄ{\x0001W6YÛd)sxa¦ÇõÔ»l\x0018X6\x001aÓ:8oê\x00119\x0005ØÇ\x001fV±\x0018²QéTÓ]\x0015Y]ÈE¬½}ù¢ý\x0000-Î\x001fFEÎbuAº<@]\x001a%r\x0008ifHÝ©Ö\x00019Gj\x0008ÉZ\x0017etf@Ï¶ßô­\x000fùÙv¡
![ÑTf\x0011§4åÇNH³³Ù\x001a\x0016D]W.¤©í\x001b°\x0012$f+³uÀu\x0006jIÈ|-¤­ íÈJÒ©\x0011ü\x001a\x0018O
G]Z,¤uÖ"ú
Ñ :R[¿¶¦'¶H	¼#\x0017´FWBÚjGÚ¡Sc¹\x0008sZJ:5¬Û¨ÅB\x0012r-¤¬ åÐÍ.HÊ¬ìD.î\x0002ÑÿV/eU×\x000b\x001búV4ñx|\x000c¯(I&àñÙ~Æý9kÜC¬qR`u#îp"WûÁB¥ö%Xqþ\x000e(wÀûO§§ÇÇÿ\÷ú¯¥ÈQS\x0000¨w¯¬lf\Ý\x001d\x001eooÿ½-Ó'Î_Ô®t»{P%I®Ñ9~\x0000Ìyº¥0z=j(QÃ\x0010*L3b Ä£ããå[Â¬åàu¨Po±\x001d4\x001cb'\x001b¥3 _´á\x0018.±6<¼8O/2½Ü\x001aãOjzÿÂÈ)þda\x0004+*:×/«®Xõ\x0018k°9åâsÔ¤}Ö\x0018nhNt¢º
Õ¡bÑ&%:qF®äöV*%\x000cË­ëHçúo$r4úTVµEÞ\x001bæ;ÞrÉÊJÖj\x0003ÈÁ
Å?
ùMOå×&Õ»ìCS\x0014¢LQô«hùU¾×9ÉæÊå{Ý\x001e¨Õ\x000eP; (:UÓ$Rßjä\x001e{UU¿¿\x001aüýq\x0016(£JnéS!¿Ê¥4ñZ»ª«ß_\x000fþþ ¹­L£Ì\x0017%"\~â\x0017K¥*«UWËª\x0007U\x0000U²\x000fÐTølò«ÌRZx=ª­Pí\x0010*HØÙ³jÖ¼\x0000^VXê\x000bZÏê+V?È
Üx\x001fÿ_6óûÜ¦u5ò,dàõæôóéóÃ:yB§óH\x0000Jì$¾¹LN,=ÊÝ\x001c\x001e___]%¤\x001c¿¶IÁ¿{@ø\x0004iè! ^¯\x0016¦6¬T%¤\x001aYIÁ¾4@ «¤ËT\Ç²ßµºDÔëHñØ{Ëë¨\x0008R/\x000c\x0007\\x000biJH3²ÉÈ\x0007iI·MZ®vÿëÂ5o-¡-	í\x0000¡U\x0014ß)\x001a´tf¸ïÂñí\x0013C6Ü\x00103ºÑ¬¢å\x001e \x0004=÷I,êä\q°v!}	é~jvé!5:¥_Þ×ã~\¸,¯\x000b´&\x000b)F~nÉÍÖñn
µ\x0013¥÷l"íÂÛµÕM	äÇcq\x001aé\x0004Ib¸xëÜüCõÃÈ/îó-.\x0004IÍÒ±\x0000ª\x0003ÙPkí Õ/.\x0007~q/\x0014½u(¬éWé;.\x0007r°Tp2\x0008wÖ¸\x0016\x000f{t×¿þvúô)WÈ?Ü¯S74B+î:°ÊÎ±\x0012#\x00034
>®¿:ÞÝå:ùë«¶¾!#«\x0012Ym@W
MÈÁå9×Ç\x0006\x0006ÙØ«ßb¾´ÎºÖ\x001b ³ó Sÿ\x00176#\x0010³\x0012ß¶\x0002#Ì0·í"5üáçQl\x001d¢ÆF°h"ÒFð$Z\x0015÷úvâ¤Ûú3æyæ§ç\x0018HL\x001a<·\x001f¿|Úí^½?}^'×	^Ñ«(DÐ$Ì\x0008ArÑ\x0008-ïúòÍë©ÓîÕÍñõ\x0005VðóÄÄê§'nØHeR·Wü\x001fÃ:¾(LÝ^\x0010\x001a«Û\x0007;Ï³H°(Ú5\x0002\x001b·pja\x0014Ö\x000bÿâa¤'}#\+VÓ¶¦Þ ¬Ôóµ\x0014a§\x000fÀCI;6ÚTE*¦¹ä\x0013¬Ô-Ù¡\x000eX[oÙéß#°VOC
\x0010Ö¡p6Za\x0017"õ/\x0013ýZÃc¬Ua\x0016FØéß#°(È9IÒ«\x0010íZro.\x0018G:­Ø¿ÝpÂë6m\x000c§wª|\x0013ÀT¥«@¼Cÿ|z\%np\x0010O)\x0006Áh\x001eçë¹
çÞ4Ýp¼?Çÿ÷x	Ò\x0012Ò\x0001H¥Ù\x0005THH\x000e8äÂ\x0008Ð\x000bo\x0013+)Cµad)Õ4Dv¢Äôir¹\x0001¬çµlL²YO	¢ZKüg?¦aí¿ø{jÑAq\x000fÌB¬½\x0016SÖr\x0004Ó³S
Väß\óc\x0004bµºÆÔ#\Â\x0015W37¤\x0006Å¢\x0006`\x0016j¸VbBý£ÃÈÇ\x001câ\x001cè'*EVÁ\x001aÊëEÕ~ÛY)kL9©H\x00136þèæqê`òÞ´\x000boûk1M9rÒmxbè¤£1­¦áä3,$¢VRêRP\x0006®:\x0010,Ô[-´(­T>£²öM\x0012\x0017\x001fô\x001ew\x001aªU\x001fw½Ãq7É[æã\x001eÿð\x0007¬û\x000eýíTUøýãúB\x0019oÕ¤./z#×6¿è}{Y£G6Õ\x0014~{¡ ymÅk\x0007yQÇ;²,ÐU[)[õÔ·ÝR?¯¯xý¿úúÎCg\x0017gÎüóÊWþËóVçÍýë·àÎÅÜôÒpï>ßÿöËé\x0003\x000eïxÿþôøëßÿgÝ±\x000b¹«\x0010C.AÍÿæ¹X\x0007îÛ¾,qß½¾zõÃñ\x0005Îñ¸¹9Þ>_\x0012ãqç:Mnz\x0003Ú\x001f/$\x0011m¢£²JÍÎÃ©Fú0½*éÕVz¯yò\x0004^\x001e\x0002-¾Í{&4\x0004÷ñu¯·âG\x0017È­Êv\x001aJ\x0016ßñê7zéMIo6Ó;\x001aL+wøFJ^èNéðvWz[ÒÛÍô¹ñÌhûH4K~Å;ü·#a|_âû\x001dð©
Æhçi®s¢Ñßo¯\x000f.
E\x0015)ëç§¿\x001eß­ÌVóEþ\x001cÍfþ(úsòÛÐA}~üÓñö»Ë¬¦d5¬Æ\x0005/I>\x001aç:ª\x001b\x000få½¨®Duc¨1ÜK)3)Ò\x001a ZBã\x001dh-¨;÷ÎU%½¯î??|Æÿåq\x0014
r\x0012þE\³é}Ís\\ØåºÞWW¯¯_ãÿr{õõ`#wîf«ªz\x0007h%eÎ"-Ï¨Þ³óÆ/Ê,âðÓe5»ø?à?abÏ~9ýüqU\x000c%\x0006ÖÉÁárIShÇ
uÓQû\x0016ì<OìÙ\x000fÇ§/\x0017¨Dlç\x000c\x0015\x0012ã?\x0007=ëoI²>Â¦ ¸'.Íj»+\x0003LH³õ4a>gW¿>¼¿?üøåÃÃÿý²N¾Ð Ö \x000eÑíQå'M£D#Ê\x0007.¢ß\\x001d~|óâúßÞ´\x001f7\x0019ÜUàn\x00138ÎßIï\x0000!\x0008ÓÅSÙãÖX¶\x0013}Ø¡Â\x000e°½Âj;Í£\x0004¬Ë\x0013\x0013[#yÈç\x0001$Çw
ä8"fSJÏÁµõ4'7ªÂÇÈ«­b6m\x0015+é1..¹ÏmLÂU+¶\x001b\x0003¯6Ù´Y,öÚÒxM|PLe¸jmÿ6yK\x0014:Ûj¯ØM{Å
À
2\x001dN%YâÌ\x0006M{E¶hºÀÍô,^\x000cÛ4XP\x000fÛüñô°îÊ®\x0000[Æ'ã\x001d·7ðüöxõMÌ:Ò_r7?\x001e¯®ìÄ;§p&Þznðz^©\x0014%t£!±émÑCPôÀ¤\x001dNnÜÆ\x000bpVº\x0017\x0003²ø?óøþý}$½?}8¼aÝÃªV-bCòýà$Ë\x0008\x0005ùÂ76s\x000cê¯"ëÕñÅáu\x000cî®Û
[\x0004<\x0017k#0\x0016k\x0012ûT\x0004\x000fñÐÑ³øT8GÀ¦áÐ»]\x0005ì6\x0000\x0003\x000eÏE@÷8\x0011\x0003ëôFd?°ªÕ0°Í+\x000c
âQ1ÂýiPñ.Às¥\x0004\x0002cÄ °×Y\x001c7d\x0019_m¹ãL@£
åkâQGS\x0004\x001eM\x0007ãY\x0013D\x001cÍã5Ö¼\x001bÆ½K\x000cµÀ\x0012Çpv±ó¼^\cÇk,\x001aE\x0013ÝÈµ¡
\x0002s8l® \x0018Zg9(\x0013|CÄcõ\x0010îLÜY¸IÜùUtÏ§¿Ü\x001f~üÛß\x001e><¬r\x001bx¿\x0016©\x0011P85Àæ~9'[âðèß_\x001d¾üÓ®_\·½\x0006Ãº\x0012Ö
Â:A¡øÑ''VàK)Z\x0019Ñ^ØPÂAØxòT\x001eê-¥\x0010ÑL0m«Ø§vVØBZìo\x001bÂÅz:p­£×Kð2ã6
\x0017{igU\x0014¤Å\x000cüØ¶¹¸Þr\x0007}Ü¶\ \x001c\x001aï½´®¢u£´ÒRà®b4ò\x0004Ò(tgHÁÅEðÆûO'n¨pÃ\x0018îTs
´sµ'}\x0014p 3nC¤º\x0013·ð\x0011;ù!^¯f^A£@£
æ\x0006h"vÙ»PÛ©C{h;àTfj\x0015ð>Õbcz\x001bCTC~¦\x0017·>j0xÖ$¦³y÷Æ~:jerñ
p\x001f\SãQÜ¸eÊeùtØpì.ñÚpN/¯¯yý(¯4¹q\x0004'T%?a%Å7\x000e\x001a÷¶N\Y\x001f69|Ø¦Và]\x001aiób\x00107ï.WÊ\x001aW\x000eâú¢$\x000cI¾\x0002#\x0005Tl%i¼C®çõ\x000b\x001e\x00169Øò\x0012ÿôã·¿\x001e×\x0005Ó\x0017u\x0006\x0017\x0010\x0018d\x0005h<#Í×ø§/ß<ûáx»\x0010ï\x0012rÑÅ\x001eØÀ\x000ca\x0016®@èè²è~C­|z\x00162Bj,©\x001a¦Æ^qj¾õÔ*\x000eq©YÒP7¼r?4ØjwLÄ©åô¢;m\x0010\x0010tK\x0006\x0010¬ÆÐªÖì§ÖÒ	Z#ü
©ãe\x001aÏP<vu.fÀ*îÕÔÍkÑ\x0004]\x001a\x0008cËRç\x0011eÔDâRsel\êõÔ\x0017Öz7°± m\x0018Ûi)§;>á	ôÚ6²\x0012\x0003Ø²\x001aÅ+\x001a_ô@÷ý¸è@ùù¸è*¯ù·
v\x000f¼=\x001f\x000bgç±pÏ#éO\x0008ý×ûÇuùm£X\x0019
§Ú¥¼¼ÏJ£\x0006\x0016\x001a\x0001GÐ7wÈüÓõÕíÂúù$z;O¢\x001fAö~Õ,ô]Ä¬\x001bOf#Ì¦d6ãÌÎr\x0015¨2yU,©\x001a®q\x0004ÙÈn\x001cÙF\x000b##½5ywÆ\x001aM/q(Ã\x0006bÈ¬XEAy¾üÅÍ¼ öÒÉ<û\x0017[Ì\x0016\x001f:RWmG\x0007ÙM#w1\?Øp\x00005½BN®*]à¡ý¬^/suþ`Ã\x0001\x0001"qÅ\x0000YJÓq§]£\x000e»\x0003:zWYÕäà\x001f¸&ç§û\x000fï>þº²=\x001b'ì¥z\x0011¯\x0004É+Åÿ$ß\x001dÜÈëOW/¾{¹P8ÆY^kdy­>JÏòz^²`®Ä)í¹ V³\x0016Ó¹\x0012Ó¹±Å\x00140³lI\x0014æ']¢\x0014\x0006ÎUj WaýøñÓýo¿\x001c^\x001e?¬\x001f¦¹²\x000e¨ð4\x000f,£®Eë\x001a\x0004ýñåÝÕ«\x001f\x000e¯·/\x001edÎÕj \x000e\x0003°R¦&K¬°æR¼ø\x0005<4)ÞþÛ?ÍÛ~Ü8W®\x001c8¬®|BC´ë9:sb¡o¨W¼z|\x001dÇ9FC^à ¹\x000cYì¶À¦\x00046ã\x000blX}gê\x0019e
x\x0006¶Á·c>`[\x0002Ûq``m(c³i}.S_ãÓÇëJ^·Å>Ð$\x0003#í,fçøÚ\x001f\x0016úû}	ìÇ5\x000f¸0à\x0018Þ\x0011\x0012²~Áøv\x0001\x0017*80«à\x0010;·5(ÂÌ£½ó<^×(±ê_b(¯ÉopïÞ±³ëÐ¼Y\x0018>:­Üþ\ìÌË¢ÑåÝÃ«+{\\x000c\x001bK\x0001.U<*É\x001e-ÆbOÑ«·KC\x000cÎÕÄ¼,Bº@­ffÌÍOÀÜ^4ú"×\x0017qûºûöþýÿÏÜ»%Ç\x001cÚ[Á\x0006\x0006\x0016÷ñ©ÈØ\x0004\x0007¼^Ú`5\x001b\x0012Ð\x000f=f\x001b³s¶1;üî\x0011îQ\x0019ÊBz&dÖ\x000f
²0£î¯<n~÷Ï7»ïsG3\x001blS/´ê\x001b\x0007
/KÖ\x001c)4.}PÎ.Î_½?>`
  
  
  
  
Instances: 10
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=ÙZºè°dÝ\x0017ÌW%\x000b3Ø¯\x0004K¾ÖÁ	°è'\x0014:Èk£ ÌIT0½\x0014i¿ÿeùå·Ëkó{\x0011\x000c3¬_\x001c=½¿{øóêóçí\x0011[ð<ì}\x000eT6ù\x0004Ðjð|¿xó·×¯O¶Pòw0ò_!èÙ0\x000c¹Ëe­uÕ¡\x0019ãø59?
d¯<4yÊÏ<$KHÄr$íZ\x0007ó\x001c\x000bd '\x0017p%Û<,Sn\x0019\x000bo~ÊXt_*\x0015ÄrY°\ÎK$÷ª¬s®y´Óíý\x0010ñö",ÅÃ
j¶\\x000e~[~þý\x001fÎmôxá«áyvqûöÃöÀ>V\x0013ÉGBk¾³\x001fF\x000cé\x0019£érqÏ?ýË,\x0004Y©¹Y\x0008²ËY	q1³íß *"7È\x0008bX\x0000#½Y\x0008ò­Ô\x0004 RQ$D"±\x000cÞ*¿ìû\x0019vw\x0006sâÚkì\x001c(\x0008\x0002Íð\x0006\ë¼\x000cAv;ã,\x0004Þ>\x0004À°ã\x001b|à#°\x0016\x0001°¥ë>_Eüÿfàp@PÀ­\x001dª:Bùß¦v\x0017\x0000È/oÿñÉ¼§>\x0005ìN8¾ù\x0005wï²i¸£>J\x001c\x001a©!N!Ò{08>{ËÌwY³Í÷1ü÷}(õ~ü>n2§D\x001bñÜã~\x0000\x001fÿáÝ' vÓÒdúôîáöÝÝÃÖï[(\x0013\x001c4²ÛT}`¢á»¨Í&\x0008zúâÍóï^l\x001bÔî>\x0010þÙûùAäo\x001c/@5Åï\x0007É.Á×3dü³ÿ/¯ø\x0019d?+ÑÇC»}zpÿuÜ_ö~ÝûÒUQ>°1\x001c?o±¾MKþò¸â"ÍùËãÈ0Þ\x001aÌÃÏC³\x00040p-\x0005²GZ\x0008¼z\x00173\x000eßí·E\x0000<g\x0003¦¥:y~y\x0016ËôÇûÈSøeöþéÅýÝÍö\x0000Ô:.j\x0003Ü\x001cMïômµqf\x001e¿Ø¶ëjðe]n}¹öÿóÆ+_îüÎOgÍÂFÜ·FÙeÕLK\x0003ó?÷Û8°]~ö|;ZRuåÛßU¸B¾=0{»¿mì½«íCè+ÄR\x0005ýÍÃýÕûÛ»íÚ\x0016Ý)*°dÉ\x0007ÚY\x001dØ\x0005S!
|ãWÙà¼9?ùáùí*w\x0000\x0005­o
E\x0001¹A\x0019ãgb&ÉPú<\x0017CÉi6\x0014k[Ù)x¤ø`Tè</p><p>Äs ¼³þüeH®pvñÛõÎâ¬2íbªD^a\x0014hOHp¸\haÔ+µíëå%½ß7Hû\x0014ªO¼Hÿ7]§Jýþ¿}utuö</p><p>¹ÒÊÎ"\x0010^q¯\x001ff$÷¸3\x0017\x0017h\x000bÇ¶Nnß_Ý¼Øúu\x00177öÈ·2½sM\x001d\x000f\x001dãç??;ñuÒÂ?{?Ó6¦¹åu|
\x001aéeö\x0005}Xòy¼\x0001zÆç³ÿIÕ'\x000cKt
\x000bnÖØ\x000cò¡ÏÃ7e kÿßÞQ)¼xÂ${Þ\x0012yXòõ¬ÌñÏÞ¯\x0003\x0010\x0015*\x0006Ç\x000c¶A·l`\x0004GÃ`g|Þl\x001c\x001c\x0011P­×F®Áx£\x001c={Bû>ï³÷¥(\x001eÃ5¬Õ\x001e{Îk1ø/_\x001c!lgßû÷o\x001bè0\x001f@ýµàkwoàKN¿ 0s\x0010dkt;\x0001*\x001a\x0000À|\x0019Ü~øíýÇÅ\x000eå»\x0017kÖÙÃGL/Þo×~.\x001aZ{äq3p )8"
:ö½zgoavñ|»\x001d\x0018\x0000Éè£	\x0004÷èÄY*ªÉy`{XÚ÷&Ì\x0008I45i4C(ÁZÊX×6\x000bÅrE^w
Cs°ü©~ºÖ\x001fqDwUÑà«O¿>\ïÊ\x0018$*\x0017\x0005léK7ÊRq\x0004e»¼ÑËWÿëÍé,\x0014ØÈ¦Â<\x0014Ø0D(òõõdåk\x001a·ËP\x0014+¥Õ<\x0014:a"rÌ\x001c\x0014gò¡\x0004Å»ÛZ.\x001dliÁ??Ü=üùÇöòDÂïqv+ROeÖÜ3Â\x000f/Þüí?ç|\x001a³WaÆ§[\x0003\x001dD.[ÅÖ\x0014$ÿl¾½øgßgCS
ÙQÓíËÜ\x0018åÂOg{ö\x000b[éövÿÎ þrÌ÷\x000cÿìÿ²wíË«±5é
þÌOïò³çÛÆÒêQõ^]}Óìg\x0017É/økcò>ÿÅ/çÈÜÐ×\x0003+M}\x0014æK¾~Q¾~±÷ë\x0008Gó×iY'~µ¿}ÍùãÃÍÇA\x0014ôüâáíÍÅ;úî\x0002µû\x0014 \x0005\x0000@[,õNÙçÇo\x001dÿm»^\x0019|¾¦C÷~\x001e·yþ¾Å\x0012y	Ñ\x0007éA¢}ùÝ|Sbû\x0001\x0000S ú\x0014SÝ|Å+Ç
)!Úe\x0002ÀÃÇîÇý\x0010|¢\x0019ã\x0018e-OÍÁå@(e4=\x0007</p><p>@4Æ>\x0007 Ì×\x00118æ#HîçÏ7Ë\x000bÈW ¶¦ý\x001dq(ú£»?u¥öË¡kÍvÜ´¿#\x000e\x001d|ã
îû>u%Õ~qú¾jþñã¡ß\x001fú^{ 8Õl,XNVá\x0003i</p><p>p<7°\x0003ÃÕ¯\x001f~ÅÛAý«hzéâúí]Î\x001fø@Ñ9ðOO¨=Ês²Î$Ý7î\x001f>ýË.×ï'°oC©]"xüs|u}û~kÉ\x0012[s\x0014»ä\x0006¸t4ü\x001cu\x0018¤¨ÏONÿ0ãã\êßýñü</p><p>\áó*EþM\x000f²qËüÀßþt­~-\x001bØÙoÞîÊVfg*\x0015O|ø¹òqÎß\x001a³ýñÙîtåÏï?ù;UR¥h\x0007 ä£²Æ¬l°ÛÄ§¦Lplý=\x000cËÇ¯^\x0017þ×­\x0017ðç·Yå2bGçW\x001f¯?ínG·M\x000bpS*4\x001fÀöµóóg§¯¶\x000f0n ´¶3 d{\x0003mf#%\x001eT°:\x0019¾\x0003z\x0011\x0004$Õ(?û¥e\x001a³Ñ\x0004ê$Ú6MàÒ2\x000c%5\x0004s0à\x001a<êWóÑ·IFhOA\x0018P\x001ds\x0014!^\x0012ºÒ~SÚ\x0017\x0012WËT\x001cF={1\x0018ûÎþê\x000b\x0006LRAÉR\x0015:çë«í©j$°nS»¯>±<Y\x001cæÉ</p><p>óéÉ«­(þ¸\x0005ûá§Ò7/)\x0017âÝýõï;ÓRUè«\x0004¶,BªÉ\x0014¾;?ý­\x001fÿ\x0019Ì/oUÿñ~ª´tÛòtæ\x00124®·ç4\x001d\x001b¥®X{vüý÷ÈI·íë6þüP¸òJzþóòj»Slâ[{<êtc\x000c\x0003ÇôåÉÎø*¾>ü³ó«Ñ/×FôÁ¨\x001f8\x00023¿õ\x0005þÙõU«ó*?~þªiS\x0010n0´8ó³èÃ¾ÏZ\x001e\x0015
´Â4ÕB\x001bü\x0018¤g~5	þÙýÕÄ\x001dàAW>yüjl×3ó«Ìá¼ë«àÈÃ-¥lZ/\x001bÆ3?¯\x0002þÙùÙü_îx\x001aÖqÍÛ\x0014æî:ê\x0000â\x000b}\x0010ü³ó³F\x0015Þ·rCû¬×m¼c`Æf~èªw\x000b¹L\x001c×rÝmâ¿m\x0008â¿m¾ø°GUX\x0013éFe?c#cÕ¦9ôF%,`íûªuÜIª"ÒWë ß'+ûjIâÅPÍm^-5qhÓÞO÷Ùüÿ¹âJ\x0013çÿþmþÿÊÖ¸Û£×ÿ¸ÛÕCäZ?\x0001NTÒ¹jÞAvä¥«£§}±£¨Añ\x001d\x0014?\x000foãÞÇ[36Kd¼\x0004V©ø¬`G,þ#ú+¯¯ï¯¾»ºÙ×d\x0016-<¼%]Ë<¼\x0010õ iÜõ]¾>=G³}Ýf\x0018\x000f\x00196"t!X4|[\x0008i\x0006&"\x0003{µé¡\x000fNÊ<\x0015Ú)f¿\x0005oc>Åïoîî¯nwÍ«BO^M mmÌçØFc²Wì\x0007ùýÙóìnmw÷\x001aØÁ3ánL&èÿR*tà\x0007\x0004»\x000cNêà¤¹p6MsùrEJG·\x0004ËÐx5DãÕL4:PpÍæ^­Z×@ê·\x00028º£gÂÁXÛ|,%´\x000e|T	\x0016Ý\x001cMÔS\x0006ÿq¦tl\x001b°ó§æ¸Úè\x0005pìßy\x0017þx¯
»»½::ÎqË§ÛÂ\x0015öíõû»ûØÑDæh¿ùñâþúæÃU¡	1a·#t¡V²e-Ï~H%	r©R\x0004ý%\x0007/{ñüäè8\x00072¯\x001f\x0015\x0002±oOxq¾5Ó3DÉÞØ2(¼\x00022êXëò\x0019e¡oÉ0}%b9\x0008P­}©Làï2¨\x0010J#/qa=°b²¾`Õº&l\x000e5ja\~ø©r©æÃwuWo\x001a*\x001bÂäY	5^ÿòÇÏ\x0018×FìD.?g×W\x000fGß]>:»{¸ÌOæâóvøL+ó¬öÖPöÉã\x0012 zAMd~mxvzòæè»Ó×Gg/Þ|ßÏñ¶	Ý!4\x001c/?2h¦ð}\x0017hÑÖìpVòó\x0005Z¬\x0011Ë</p><p>hÊdø+Ã
Å¡b\x000bÄv±9Ý°Ñzh9¶_>ØO?\x000fjI§\x001f¹øôé</p><p>©ìUÌ^Æõ\x000b¬\x0019T0>T\x0016*o,vt (ëë^Æé³Ç¯^ ©=þ\x0017\x001fÎÁTûÝE²Ã^¶YèP¦ëµÖ\x0018ý\x0016;a]Ü¿½úe;&ôXñ\x0008T>µè«¬\x000cU\x001e3¨H\Ö{¢]!+tzð\x0008W¬V¬àJ¥</p><p>
iu\x000fWÅ¬+`¡»D°|a5+°\x0002å\x00043._9¡mPj¡´þ¸¼uîzpÛÏ¯>\x001dÝ\ÑfÁO¨f_^Ýß^<üy}³ã=¦ìYÒ\x00158iSß#¦Ñè=úÔiÚóWG8¹X\x0016
¾BEûòäüùñ¿nKîwPku\x0019Ô/\x00045@ÙZ\x0000BÊû´\x000e´>×Hqb\x0015pY9P \x001a\x001dYÉx@¨u²méù'z6ÞáôtþôqÒ`\x000f\x0008µÀ-</p><p>|\x0002ï²¯Uv\x001fyä¦«ÿçáPë¬ÜB¨\x0006P\x0005jöº\x001c½ªè\x001cCM\x0007DZ§ê\x0016"µß¿ÓÝ\x0018ôq\x0014àPëøÝB¨è\x0008òù«\x001aSzlBe¨Ú\x001eòªÖðP=æ òª¶#C-C\x0005ªòîpP9ÌZ.ÖB<U"~"ÖÈXõ\x0001\x00157/Äª\x000bÏU+Ô\x0015\x000b¸ËÐú&×\x0003ÞVîLÿ·ÀJ}ìK­\x0000Ôu\x0011hZC\x000eúÉ</p><p>Ðâ´l°Ì\x0001
\x00167½½X¯ßßØ»n8çýý?ÿ»LêmÁ</p><p>!.^</p><p>ºNgxd^®o\x001eV»óÆ'/ÞLûè\x0003\x0000Õ\x0011\x0003 Ô,.\x0002ðéI
b°"Êß7fÉ÷ij}ï÷q1:vY\x0016©\x000e	xSø\x000eK~\x0001lïõÌ\x0005@Cëû\x0001ä¿aaÌA"ãkjÝC±`E\x0002ÑbK\x0002°÷\x0016¾ò3\x0007\x0005n}Õ\x0015\x0005èÚ\x0018Q¾¨rÆ(¦{\x0004\x0007(BaÞ\x0008³nc>Ò&Ï\x0002G¦BÒJC{=\x000b×Cû@|~g®Ô°Oóìîóu>^Ý½ÍßÞ=Ü¿#nm\x000f7\x001f]¨¡sLaùá*PÕ)²¸Ý¹Ãôâõi</ë¿}ñæü»\x001dd\x000f\x001dÈ\x001ag,\x0001ér<T­!®®¯	=R\x0003Fx\x0005HzÙ\x000b@ÚP÷J"ÈX\x001bn2È\x0008\x0004ÒÿîÃ$Ú\x0005 UD^È\x0002\x0012ç¸+ÆBØW0jw0Ac4e7R\x0018míñ:^ÚÑh·</p><p>£
ïo/ï\x0006rüöâæêvG~,!Û\x0015hJ('ºÙ¶9z¸</p><p> {$ß\x001el]«8\x0000\x0010°¦P~öB	Ë\x0015³êQö\x000c-E\x0004YM"Ø¦9bºy÷ám§¸~\x0005	Ì<½¹+?×\x000f\x0017;3Â­¸×ÜiO,/VÙXüÓï°Di§g/ÑÏçõÃñ®|ð\x0006gKR,Â©5\x0007Ô¸­Þ\x0013Ö@î´Å¡½Cmye`]a\x0017A°NÏ+ÃYÛ:¨d[¦b\x0011X«Ë\x000c$Å"~\x0005Mf\x0004Vý¾UX[ªb\x0011VWú³\x0011*Î
V\x001f \x0000-þµ Ü8Wµ</p><p>kU\x0017`
	©È¨T¹öò%ÀyÚ</p><p>6ôu¡Õ7\x0016{Ì±Å|)Þ¤Ñy(Â
\x001b¼¶\x0018ç\x0017vXuÐ¦\x0012¾fùúßÅÛw\x0003õõ×;\x001c¡Øå§bfYW¨Ðe\x0005òS\x0015)ª\x0000¡/`ýõ\x0005QÌ\x0001P_ù¿\x0010@\x0018þ\x0000jë_\x00073Bÿ2\x0004¥%§üìà5&H\x0011o\x0019¯Ï9û}µ ló7\x0006\x0010ìÓÎ{</p><p>±j\x000cÁDN&EK¶³¨\x0000BúüÇ¯¿
©=Êö¬,>\x001d}wõËÝýçÒ¾½
ÆI\x001aÆ#
\x000eåb¢ê­E¾!²"«\x0008T\x0013/_¿>ÙÖ-Ú\x001f7î\x001d\x0000+µùÓÛw\x000fù¯q}usSú±>_\x001c½zx·+Ñ\x0000%Q\ó4þç1ïÂÕy§º\x0013+ÕùÓçß½yõúüôä¬ÔçÏ^\x001f\x001f½zóÝ\x001c¨õ1ý;@åí\x000b¬ÔæýozÃÿ-°\x000e»¾v¬Ô\x0010þoúªÿ\x001d°ò°Ê¿\x0005VZ6òõb½ºúý'\x001b\x0007Vëé«×·è|=ü¹3\x0011\x0001\aFËnS\x0013ÎÆÔ\x001b¶ì£¶§9yvú¼8Üoþ¶+±òá½}ûÑt\x0015£óëßvÄ\x0001ÉàJ%(²RU\x0001Kí!ªMBöèüôÇmãÝ÷)×¹ÿûÆPj3ÒÚrôAyi£]B0C\x0002\¢ø×! ,å¿\x0010\x0001Iþu\x0008¸N²\x0017We\x0002\x0001\x00118Kñ¨5êè.ÿ_ÀÂ«è*#.·ÿaYüþç«KlNÄ\x001bYÏ0<¿¹x¿3Y\x0013t¡vÊ\x001e7¶SOb ïßZ7.ØäPüìøí@Â»WÚ
×½
¯	WïÕÍ>,)RlL¯Í¹#EÅí­Å³Í÷Y»ï\x0007 k\x00158\x0005[mxµ&UïXoüýý"à}\x00173dÛHëÅô.\x0015Úi´%\x0010)ñì_ \x0002¥Ñt\x001cU\x0019éÀ\x0006é\x0018(kg"umyíÂ#`þ9MÏ²±Hâ½Úµå=x\x0016s\x000b\x00000©Å\x000c\x0000D\x0002\x0000GwÀH5¦]}3Ñ?ã\x0006h[\x00161Ú©©-~&úÀ¥\x0007Ó§£g\x0002À4Dùs\x0005\x0015ÕÐ£ËjRÕ6ÒXÆ\x001f\x0011A\x0008&,@8ËÏ3p-H5Z«¤\x0006Y$*\x0000ÛwÌ\x0005-\x0017ø3ç\x0016\x0016æýRÊ¯4Q Ï`\x0004Ê<@÷\x000cuh%°l<\x0001°äSzµè\x0008Ñ¢üÌ\x0000à¨*Xf:L½!yþ¾Zð</p><p>\x0001A9¶À\x0015r'tªò»Ø\x0002vªTDÛ\x000ct\x0003Q\x0016©Y/!_øDC5H¸\x000bNÁ[hÝ\x001c\x000bÞ¢A×¢üÌ\x0010ÕÔippÔ°\x0018X\x001f\x0005úØ¡¯X~æ ($¯\x0000Tª3Øh\x0012\x0019eãÂ¤QÜ \x0016îaüÀW\x0004ÙR{vá\x001a5­\x000eö]\x0005]µò<µ\x001c\x0013nd­9$\x000fÅ\x0017Á)E=y\x0017f (D'0O1!×O\x001d\x0008Ð&\x000f"N\x000bÔw©ÍäiìG\x0011»\x0018æèçìñ\x0000\x000bÎ\x001càFÄÂ6\x0014£W¢È"ÌTÒ©Ö\x0017ôúK
\x000e«£0­¢f`(S=ø;Ï]I4û\x0016#u¹\x001b¤beK\x0011&\x0015õ~\x0014±,ùB@\x0017pD\x000cÙt+\x0002U]J0é5îE\x0001«¾üÎ¹\x0015¡¶[Eä_!\x0011]b×\x0015@ô@>ûßâ[\áÁ ü ëæÝÎ\ÂüB\x0001tä»÷gMFÑÔÉÑË\x0017;\x001a7\x0006\x0018\x0012bH³0(®Í\x0006[í\x0016\x0016f©M#ÄQ[Òl\x0004\x0018Â½\x0008B¸" êOlwãjkÀxb	PÇ\x0005\x0003"+D\x001aU\x0008Ö)ò¡\x0000eÑ"LØ\x0016M¥Ï\x001f.oÂt</p><p>ìâýýÕÎ¾P5VíÈ\x001aÛUêjlLõ\x001bCûaÚA\x000elOä\x0000VM\x0001I`)Ç\x0001giA¯*,ë\x0014Jéõè|TpóÛÍ¿MÌ\x0001>»¸ùxqÿù\x001d 0ô­®WØ<dë£7LßdÂóZÏÏ\x001d¿ÞFtÙªùº¯\x0001Ôím2ÿð\x0003I=ûçß\¿Ýu±sXX_WD</p><p>Dëh²Éx\x000eOB\x0017">;9;}ºÿû\x0011ý±ò³\x000fAÄµß\x00148Ü\x0000Põ}åÅ)\x0008@°íu_ýö!\Q[\x001cJ(?¸êïÛ»O¿>\}ÞQ§
àU-ÒFnÓËÆæìh\x0008\x0012ûÏ¿}ñæÕÿzsòz{yÖ^ÝÞ_\x000eË³ù\x0011=ä/^|¾þçï\x0010IþZ¡</p><p>ÊN"¶1Ö"¾ÑÂö ì8öÃü_oe\\x001e`	ÈZ]~f¢Á±HPZVôrS%d\x0005(å\x000eýDÙ\x0010Í¶c\x001a )*íl4¸E\x0015©\x001fJw\x0001TöÆM</p><p>Vé(Esç>}Öÿ7Ù\x001eãØÂ:IÄfX(Gä³\x0000(±¡=§\x0018óÿY'c\x001cPøn+ÃÂíïïþë¡Km[{ñðû\x000e\x000cØ9éª\x001dðÈó@Ù\x001dK\x0003)6Ñ¾øîÒ\x001e¿ÙÆÎÖÁ(\x0013\x001dv\x0016|\x0014eÃÕÍ(Íç ZÓmÔ*.¡+W_%ë!P\x0010Ã}&ä¾æGD8¼\x0002\x0011÷¿Úÿú­x</p><p>Øk?O/>þrUþwwã¨ú\x000c\x0019ë4¹òª\x0015b*O½<yõú|;ÿÆ\x0000\x0007¥\x0007?\x000fG¾\x0008<=a<°à,ÐüKý\x001c\x0000HD¯©üÌ\x0012³\x0014÷g·9T>\x0012o|¤'Rf\x0019\x0010­M¡¥ÀßY"	é®\x0011ÍN®µÐs\x0015$èÒÉÄ_>gÏ±ôccZ\x0018ê:ªË»Û]þ\x001b6XÕ{Ù<á-î¯«Ò(-ýôøüÛ\x0017Ïç @vwüÙ\x0000¹Î\x0010Ð\x0012ô\x0000bb\x0008>,`ñZ?\x0007Bþn\x001d\x001eÉ*vbf\x0008^«s#F=\x0010@ý>~èR³Ù«ÍÉÕÅ®±\x001a§$,iªÒÈ!ÖÈ´\x001c=Í¦ääøÍ\x001c ¢\x0007ÄàW 47é\x000eq¨µ\x000fÉ»·?ËKÌÑ¡E,?gÿïÿ÷7ótk¿\x001aFYD\x0008¡M% Å\x0012{bWÈ¤~âèä³í¼§öïîRßß¡y\x0005\x000cÊÏ÷×7ÙÐï</p><p>ÀcJT\ÏoÄc¶ªL-\x0000¥D²?fºWòýéYoã·Ðe7výÝ\x0002²GêjÊ\x0012Õ)=¬Çhz#Z\x0008PàÎûoêï\x000c\x0014¸\x0000¢&
C~¹ÑU\x0014¸	®¢0ÆJPÜüùÓ§wÊ{ÅZ\x001a-¯ÿþî~W&Àb1­\x00164!h\x001aG:TÊYÕsªä\x001búýómd¬C\x0010eYyÝV¾\x000f\x0004à\x001e[[ÇàæÖkÜªJ	Ü\x0011Êl\x0010¥¦üÌU¤ºw­fâ</p><p>\x001fÆîù\\x0010	½òò3\x0003Dö-ji/ágWõÆ\x0014z\x0005A<åR\x0010uÓOýÝÂ`$¨¨àÉ
.³IÑ÷ã´ÈN\x0010ï~ÿãÎaJ= -Kùù¾ð#ï</p><p>a\x0015²¯QÏA¨Dy9ª.ëJ-½ó}!H~:\x0007\x0003¶<ãÏ^\x000c\x001e©,tÕÑsaA\x001bMS^NJÕ"\x0010e?%`HYta\x001dès\x0006F$üþùSá{,µ\x0005MÝ\x0017;],í\x0015º$ ?DÇü89\x001c\x0005u\x000cb\x0006\x0006æ&ý×a0HHS~öcÈj­6ªi¤³¬Tò>[/R9B4KA\x0004\x0004\x0011f	Bsýß+`j'mF\x0003ºs1X|Råg?l¨ú\x000fÃpùY5w\x0002R_k
\x0002{\x0012¿)?ûA\x0000\x0000%<NCj \x001cá\x001d¯E§ñá÷ß¬¿Å÷YÈZ\x0014­c}z÷ðñâöºn\x001eÝÎ+</p><p>w-Æ©Æ×%ÈÙ§JÔ®es¸4Âòêèé7ÏâþÑmî>ðÇ»RÄ\x0005±¼!\x0016w~|Þ'Ç\x0003e|ßâôNê»t\x0010\x000e®þx=\x0003.ÄµèkçI(\x001cS]lÖ<õk\x0000M\x0019{$Ã¢qÞ}¾Æ%±\x0001Ãò`°mg>0\x00075ýp \Öï4ó
\x000cq\x000c\x0005ÛÙf\x0001A§Ä\x0006ûø\x001aùU´\x0010\x000fYr<\x0013djÆûø\x000f\x000f÷¿ü@°¡üÝÝ¾ÿå~wêÍ¹ÂÛ.yru5¿d.\x000f&dBé«ÿðrÇ\x001b\x001aÀÐ\x0019f@zúê\x0000Âf²Ç'</p><p>\x001b½ÁêØ2\x0010\x0018=ãÏ\x000c\x0010·Ê\x0011²­9\x001eÈÞ yQõÁÉ\\x0014ºP)×ß\x00190²2#FÍ[kÖ4iC\x0004\x0003\x0012\x0018ÿ¼ùÝ_\x0015Õé{üQÍ°íZd?ÅWöso³^'ÝBï\x0004¶*Æ~\x0018øBÊÏ\x001c\x0018ÊQÒ<8íhNÛ@Ì­6Ú¾>\x001bF\x0015Ë\x0002\x0019üSÜÁq/GÅ\x001dî÷²^9ÎÊöM.{aüúëû_.</p><p>q</p><p>\x0007þy Þí</p><p>\x0018\x000b[JÍAZ\x001bébXdÀ¤<Wì©c^"ï¶_?ÍúmÕðûåç%Öu>}ÚÉYârÈX	¾\x00126^QFÖhJüyìÊì`¾zõb{J£áÀNoÊÏ,\x001c\x000e&\x001c¼i;C×D(.àáê\x001fáïC¦Ù9<GH{N¼\¦2 ãkµù\x001a\x001fIYö\x0003i¼²óx\x0017k\x0017xC\x0015\x0011.qg°Uªï°\x000fdÈ";K$ù`\Ebc i\x00130®$õeýHâ½ºyû¡\x0004NhëI$÷\x0017\x001fw%#³K\x0010¹M\x0015Y*©'äA)ÙìÃÆ\x0011óãg;ÒïÞ^_~ü©ÀÀ&\x0003_W*Õg»Ú\x000c¼	ÈrTpxâ<ÅTGë×=ÿ,ËÏvÄÓ\x001b\x0018øn½\x000b°]äDy]{#E»\x0018\x0008R¼	Ä\x00017PgP\x0003qX½T Z\x0017^~g\x0001Ñ­U-\x0007Ô\x001cH!a\x0019\x0017uL!Én\x0013\x0017ê7ÿ¢Ð©<ÔÉâ§\x001f®~»¿z¸¾Ùå£lö«­	ÖQî\x0003WW#®Ç7u®8CûñüäÍéÖ=\x0014\x0003x0\x0007_\x001d<3gð"z5\x0012Ë>CÝ15²µ
_\
Ð\x000e\x0001Z)@Ì9W|\x001e0ÑVð9ri\AâZ|nÏ}uçëðüW\x0007/\x000cá¯\x000e^\x001cÂbx[ÿp	9Õ°3ñõ}ûrHð<_\x001epÔÐ\x001a©#\x0006i«-G\x001e0"byp[KÈû_6ºvÁ
7W\x000f7\x0019ÀÝ\x000e_\x0013=*JÂ"}a=3V\x0011©±uq58z}òæ,ÿã\x001dåî\x0006f°@q\x000e\x0018¥pê©ÑÆ WUÁ<N{Í\x0007\x001d¹ß\x0004d\x0002\x00103qÀøø4-z%TW\x0004·\x0018LDß¦üÌ\x0004#$ÃTüJj9>\x0002¦qI\x0000\x0006Iê¿)?s	(\Ãý]Ôae¸ÁÊº\x0010W`ÁÕÝåg&\x0016\x0008Ä=2@;</p><p>\x0000øÊ¸°øÊhmJzÃ¹h\x0002¶YU0ùöT·Ë8v\x0000­×rÇ\x00020©Ä*i¶h\\x001d\x0013\x00084ERÎhÕ­Uz<Úº\x0017þ5Ä?></p>
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/download](https://adresse.data.gouv.fr/download)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/api](https://adresse.data.gouv.fr/api)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.10.3 (Ubuntu)`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
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
  
  
  
* URL: [https://adresse.data.gouv.fr/sitemap.xml](https://adresse.data.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/temoignages](https://adresse.data.gouv.fr/bases-locales/temoignages)
  
  
  * Method: `GET`
  
  
  * Evidence: `8f3c-gfG+P67yFyIFmwt7DJcFE37xcQc`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/robots.txt](https://adresse.data.gouv.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `3e15-MEJs95Z/omxn3TXvSLWyK5wtscM`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/](https://adresse.data.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `8105-2RoW8oHR+2wMO/pWUtvrTE3i1m8`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/contribuer](https://adresse.data.gouv.fr/contribuer)
  
  
  * Method: `GET`
  
  
  * Evidence: `49b5-bqOfxlX6Z3R5FCK8Jng0x6UaoD0`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/tools](https://adresse.data.gouv.fr/tools)
  
  
  * Method: `GET`
  
  
  * Evidence: `4f26-ebdq7wY3Xcn1wH754ARs29ueaEo`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/guides](https://adresse.data.gouv.fr/guides)
  
  
  * Method: `GET`
  
  
  * Evidence: `5d8a-KtJk4IeM7iemyszqJCGYUuf9nck`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/donnees-nationales](https://adresse.data.gouv.fr/donnees-nationales)
  
  
  * Method: `GET`
  
  
  * Evidence: `6a20-fp7mACB6YwkvUbxVTPtMSTkYQAI`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/nous-contacter](https://adresse.data.gouv.fr/nous-contacter)
  
  
  * Method: `GET`
  
  
  * Evidence: `4bae-RNjp9qhpApQVLInQSFmngEonNM4`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/bases-locales/charte](https://adresse.data.gouv.fr/bases-locales/charte)
  
  
  * Method: `GET`
  
  
  * Evidence: `R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7`
  
  
  
  
* URL: [https://adresse.data.gouv.fr/base-adresse-nationale](https://adresse.data.gouv.fr/base-adresse-nationale)
  
  
  * Method: `GET`
  
  
  * Evidence: `39cf-lSMIckl4Xohky11p57bEWwets/Y`
  
  
  
  
Instances: 11
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>��y��	��Y����t׽"�Ȯp��\x000c</p>
  
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
