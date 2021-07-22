
# ZAP Scanning Report

Generated on Thu, 22 Jul 2021 00:57:09


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 6 |
| Low | 6 |
| Informational | 7 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 12 | 
| Reverse Tabnabbing | Medium | 12 | 
| Source Code Disclosure - Perl | Medium | 1 | 
| Source Code Disclosure - PHP | Medium | 2 | 
| Sub Resource Integrity Attribute Missing | Medium | 12 | 
| Vulnerable JS Library | Medium | 5 | 
| Big Redirect Detected (Potential Sensitive Information Leak) | Low | 12 | 
| Cross-Domain JavaScript Source File Inclusion | Low | 12 | 
| Dangerous JS Functions | Low | 5 | 
| Incomplete or No Cache-control Header Set | Low | 12 | 
| Permissions Policy Header Not Set | Low | 12 | 
| Strict-Transport-Security Header Not Set | Low | 12 | 
| Base64 Disclosure | Informational | 12 | 
| Information Disclosure - Suspicious Comments | Informational | 12 | 
| Modern Web Application | Informational | 12 | 
| Non-Storable Content | Informational | 1 | 
| Retrieved from Cache | Informational | 12 | 
| Storable and Cacheable Content | Informational | 11 | 
| Timestamp Disclosure - Unix | Informational | 12 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="https://inscription.snu.gouv.fr/auth/login" class="nav-item__link" role="menuitem" tabindex="0" target="_blank">Votre espace volontaire</a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/2021-01/snu-d-pliant-g-n-ral-2021-114.pdf](https://www.snu.gouv.fr/sites/default/files/2021-01/snu-d-pliant-g-n-ral-2021-114.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `$#AtNS`
  
  
  
  
Instances: 1
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>$#AtNS</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Source Code Disclosure - PHP
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - PHP</p>
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/styles/445x265/public/2021-02/-g-n-ration-snu-pisode-5-juliette-et-l-ehpad-simon-b-nichou-nancy---2-148.png?itok=mX0Q0i_X](https://www.snu.gouv.fr/sites/default/files/styles/445x265/public/2021-02/-g-n-ration-snu-pisode-5-juliette-et-l-ehpad-simon-b-nichou-nancy---2-148.png?itok=mX0Q0i_X)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?=óóß~¦í;~øá\x000b·¼¾¼p\x001aG¾× \x0008DF"çÈñøFÎÝnCÛzÅòôüÊëë3ðûû;ßqw{3"\x0006}~~âoÿñ\x0017®¯n¹Ù]ÛÂ\x001cfæyÆ{¡ó^_]±Ýí\x0018¶\x001búíF\Ûç\x0016Bt\x001cÞ<=~çåù¦muu\x0012VYNüùßÿ\x001dÈüá i\x001cË2ó×¿þÌÇO\x001føÃ\x001fþÈnw+:Àñj\x001ddÝ[ÎB]Ùµhpãjèµ8\x0010Ø°Ë!¬v6¿ãÖÂYÏJmÃ%\x0010À¼Ñô\x000b¾ëQ\x001b¤CC*
]¿e·ÝÒ´²]E\x000c\x000b\x0019[²xò\x0015íZ\x0014"¤Ç­\x0018x\x0015çi»ín/û\x0011\x0015E\x0002\x0008ÍO\x001f>²Ûî5@d%jU³ZéæªÖ®ÔæL!}q·Q4 (á`2(Ü¥\x0015oÕ¤¥\õYçdëYæ<\x0013©\x0018\x0014pJÎAl¥uGÖø\x000bw3ÜZçÒe]\x0011èQ)ègBKµ;+ºBLÐ\x000e\x0003Ò%\x0001&ÕÛ «ã\x0010s¼>÷\x0014\x0003ó<ÓBc²Àª\x00192yµ3Z`R(Y¼y}#îHu\R^c
8\x001f\x0019\x0007¶1ÚUÔbJÄÉ2S\x0002sÙ\x0002VuwH\}SéÈ\x0019Æ1ñl¶[®o\x001búM«\x0005Ua×çgÞ^^9½½±Ì5 ¶^fÜy.XªJÞÃ
a+/@È\x001eù|&\x000cZWý³vÞEF6ÖÊ\x000c=Ä¨få²U¤P\x0004]Ê	k")GI¨YÄñ¨\x0015WÖïm\x00149K%VÄC³ò`<dc	¹¬{9³æ\x0012s\°Eõ'¦à\x0014RPÉýp^¼=S®°²,\x0012®¢þy×\x0015a¹dñäÄ\x0002\x001erD\x001b
ÉÂb2Ó\x0014éÛD»dìq^fÁ'\x000bØdIÖb]\x0004(*g(\x0004r	R¤\x001a)¤Àÿ¶&½Hz4æw~ØêÃZÔOÛÀ\x000bXôÜyU#Þ\\x0005ìN\x001e4¼\x0004~\x0018¸»ýÀÐË¼H.Tdº1ce\x0017e¡\x001fzr)ã§§g6ýÝv±\x0018\x00131\x0004¦iÂZË4Í<>=Prf»ÝÑ4=o¯/\x0018cØï·l
¥dº®ÇÚLL3ó|"À0´@á·&È~¿åîN4wP`»Û¬\x001b¶O§#OÏOlëÝV½8º¯PÀ\x001b\x0019NW<Ý\x0019Çn³e«É¬ñÍpËõí9\x0004\x001eç¶|xàõùÆ{î?|`¿Ýa0tmÃ¿üé?ñ?üëÿHTF¬·\x000eï,\x001fî?\x0019nN\__Ñ\x000f\x0003>ÿÀ?ÿçÿ¬¦Æu¶Vï©>\x000fE\x000b[cViÄ\x0005Ú»Br\x0015r^ÚìêùáìÈBõõ¸LUP_Èy$,òÌ0ÌÂ\x0006,\x0016]¨ð´\x0014ÚV\x0003\x000bõA\x0016F(ºo/%IõÅ©ö±Å¸\x000e×ôtý¦í\x0010\x0015Ö\x001f0ÅÂ²\x0004æ É¦iÔñG3\x0002\x0018YbPXP;³º\x0005»È*ªÇ«ZM}Ê.Ç\x0008½YçÈÎáæ\x000cëÙó\x001e4ëÌ
±:dÃI¦Ûµ[¸,`¥ËD!
IÖ2.Ô\x0003P[\x001dZ\x0016-\x001atQùXTòFJýRel[¿tîVJâ8¾q<½Át\x0012\x0001;YÌ&\x001cx£[\x001a8ÃÜÎY¶\x0011Á{I,afZ&J)\x0002£YC"ëz\x0019
¶ÎÝ³\x00128ê57PM(©$bí/IYÙd\x000e§·Ó\x000cÆs{û\x0001ßn9\x001c'_Þx}}f:\x0008óLç=WW;>¸£õ\x001fH1òòòÄt:él*â³Ãe¤£]?\x000c1fÚº%¡\x0016JV¯©s\x0014s^\x000f&Ë`-Æ6êR",áyZtß^Ö"JºÅÆø5§XBÔBTgÂ\x001aÎ#sêÞ"aE+Ö\x0011\x0010+8@!§"2§fe3Ê\x001d\x0013©¬Iójáç½eÉÒÌË"\x0005ól7\x0003Ã0\x0010S\x0012\x0012^\x0007¿:ÍØ\x0015O\x0011¢&½S³D¨ó,³nw·j`-nhÁFL³`Ûb'¬[°.;LN¢éS1l\x0012_[ß%ÁI\x00198¹&:«±¬ÕaÅvÏ³3¤r­¸qÐWw;\x0015b\x0019=aOã[\x001c\x0002?¼<?ó·¿ýÌáõýõ\x0015í èB&\x0005©\x0014Î¢ q<\x001e)òúúÊn·ãj¿gØlXEtZÉãDßwl\x0014#Ãa\x0018Øívô}§´ÄfÓ³\x001d¾SâÛ×ß8\x001cF^RÀ{Ïn»a³ÙðýÛw¾}ûÊçÏ_0\x0016ú¡çÓçÏôm5¸\x0004é\x0014Ðå¸F¶\x001b§\x0018õ\x0001wl¶Wüá\x0002K¼½\x001d8\x001dO,ËÌ¼ÜÓ
\x0003¥\x0014æyfa³åöæÍ°aµ× \Øo\x001b
jF¬VH×à:ÏçÏW½ ¿\x001eÛ6P+÷ó3\x0001H²;¥÷Pc\x001c\x0017ó$¨É\x000co5\x0011JÇ£\x001dÂæ)×'õxuÈä4òRX³ ô÷Deoªq\x0016O\x0002óY\x0014YÈ¬\x001b\x0001¤Â¯×Hâ¬P½¯½k\x0018
íýîéøJ)bÜÝ8)V~ùõ7r»ë{ú¦]uó"6fs\x0008Ì1aüHe§¡N#¶°
Â«LÁ¸Ê\x0012>'1cí
ûÔÄrI±«è]G	FÑ:=XÐ\x0012,çû|\x001fx÷ßò¹çí% 3¬\x0015êRßúl¯yíâþI\x0016¥¾\x001fxKÑÝo\x001a`C\x000c¼<?óôð@9h\x0011ÍZë<¡Ã4B|ZG\x0012zMN§\x0013\x000f\x000f\x000f,AÄÉã\x001b)'eÄ¾1\x0005ãe»\x000bÓ¤]ª\x000eX¥D¢¶[1\x0006í
óC`\x001cG\x000e§¦\x001fØn®\x0018ÇQöV"Áv;p{ÃÍÕ\x0015W»\x001dsØXæ\x0013ãéÈ[)ä\x0018È1ÈyV÷\x0016Se!JTË%I"«\x0005c½«ÕíEf-8å¬\x0017^vóÆyÙô²\x0007Ñ"	kÏì^IXgX¼èkÊ³-\x0005§uVJô\x001fVÑbiXÏh»ÐþRóAE<Öù3ª\x000b\x0015¹\x0003Î3Í\x000bó\x001c0eÄ\x0019èºívËáx\x0010_f\x0010È²¾ÎdmÊDkIQ¼%\x0006²±ÄTX¡

Î'L\x000e\x001a+8é\x0005\x0002ãQV­¡UãjùYÖÞ
ÂzÑÊ
SJâÓäWñàË\x000eo½e-\x0004+DZ\x0003`Å­\x0015\x0017\x0016ï: B`'Jô}K\x000c\x0013/Ï#Wû\x001bú®\x0013Ø4elÝn5\x001031\x001a\x000e¦px{Á;9¬C×Ð62ã4óôøÄx8±Ý
Å>Æ¨U¡\x0014¿µ; \x00082-3¥ÀÍí
ÛííÕ\x0015¾iÙ\x000c[îîäçÌJÁ~ø.Ý¹ºb\x0018znàóç\x001fY³aØéµ20×ë·Ý_\x0011câúæ"\x0016èú\x001e×6|°Võ0^d\x0016zm×ÆÚ\8èÔØfÏQª\x0006Ò¬­¹`ÍXzµâª¢ö3ãK;?
iÕo¯èL)daDbe¾\x0012Káåå\x001c\x000b×××âbckB<«J_I]%QÊ\x0008L²@NuàÉ¥¡\x0014'L³,s\x0017d¤3F¾ÌÙ,\x0003ø\x0004Lã\x001c­kd.ådÿ]ë\x001d§ñ3·?2ôR\x0016r\x000c\x000cûÝ
\x0005Xq<B.¢'­f\x0003xïiú\x001eëëP½¹äl\x001b[ý Í9AsÚ¯Aþ¢}®\x0017d
^¦J
(T÷Êz4zKA»3qår®-EBmFág£­F\x001d
¨ý\x0017ëkæu6KZº=ÄÀi<\x0012PÓóÅ|ÏXu¡0\x000e<<<ðòô\x0008ãD«Dª¾idþÚ%¶\x001d]£¶\Ö0Î\x0013¿þö\x001bÆ\x001a>ùLÓ8^ß^Y\x0016ñ«};\x001cx~z\x00116m"¿1¬Û+(Vv¸éû5Æ`Ô¡&N\x0013/#OO\x001c§\x00139\x0015¶cp\x001eï-Mã¸½»e·Û²ßïØl7tM#zÑ\x0018É1\x0010æe8\x001e\x000eoEáKÁsaIÊxUBV+¥dÑ\x0017[W[8ÌÀB,ç>§ºU]ÎÆ<ÏóL×ze[â=Dõ)e-
çÄ¶&@.ÿ-Kg¼ÎõdÑk	pë×­\x001fìÅ¬{\x001f×$gÀd1Q°\x000eS*ÑÈ³é{Þ#ã(¬qk·øÆ3\x000c\x001bRHÄ9««ç\¢D.ufÖw\\x0010OSëÁÌ¼D\×vª9CÉF¥"ÒæjJmõ¢ø\x0018X¯:½ú\x0010®ÉO[àõ¢rõ\x001b¼¸8ú&ëÖg¡gË}¯ÂÛR\x000c¾i\x00196[Dð	iæp:òë¯ãéñÏ?Ò6
¥ÈÞºi\x001ciÔìu	ÇgN§#WW;¶»-úã\x001f9\x001c,óÂËÓ3Cßã½$ÓÖyn¯®Ùv\x001bJ*y¡ë¤ËÛï®±Ö3Àoß¾q:\x001e¹¹¾¡ï{Úaàõpà8?s\x00153a\x0011õîîO\x001f?á¼gg6Ý\x0016ë\x000cûÝc·­\x0005¬\x0012oª@\x0014\x0019NW\x00065FµQV\x0013°SËú?	Y	]RËEÒÐ®B
\x0019¬w®\x0018\x0015
Ë¯jð+
¡\x0006Y+\x0007ÃP¡þB¹gI¬!F^Iqf¿\x0017\x0012Îñ8ò×¿þ\x0007¿~ûÊ\x001fÿð#··w¤Tøå·_i}OÛötC£\x000fù\x0019¼:s"K\x001cé@J\x000b1Íu&c)E\x0006Ô)è6.Ü\x000bE\x001dS\x0013\3cQí¢&Ë\x0002]'³\x0019\x0013²\x0010\x0000\x0010¦íÈ%óüúÆ8¾\x0012ç\x0014"øã§þÈçÏ_¸¿¹[w¡å¸0òÊ¾iØnd\x0016m]uØÑ\x000e¨B\x0017éM`ãü÷O&Ãwä«{ÔyE^É¬ÏÝåvñÔj·\x000fåL¿0\x0011Î¥&M³&OT]\x0014\x0016®î1©jr&¦ ë{tÜ\x0019\x0011\x00188\x001dÚ\x0001\x001b¡Í\x0017èû^,ùÚVL\x0019Þ\x0002)\x0004qÝ±àJád¤`ô¾eèE\x0012r<xy}å~äöæ\x0016ï=Bã\x0011a7l	1R\x000cóDL\x000býàØv\x0003MÛbéHÙ±}ßs<\x001dxz~âp<ñúôÈËó#)E6Û
»Ý\x0015>}\x0011Ãùë+º¶§\x001bºµk¥¼*¹0\x0010càt<ñòüÂi<Ðø÷wxûÂëñKBÕwÆhÇ¦	¥J\x0006eEXÂö\x0012´s©z¸1Rí´ó¡Xb(\x001c#»í°Bè¥@TÝRûTþÃZ\x001c\x0017Xg¼ÿ=$¯â¦ óe\x001dA÷1½¾ê%¢'×	¤Ë\x0002¯Ë¢./kéÚÈ4M:v2lv\x001b¬54m\x000b9õk×²6XÄÌ²,ÌÁ2¤N·Â'L\x0000ã
ó\x001ciûD\x001bJ2\x0018Û`!\x0013%\x000eªV©2G6²B\x000cë.Þ»\x001f3T¢ÿQÌï>«\x0006µò»¯Ô®`Mw\x0010w-Ã ~Õ§nY\x0016Ñ
\x001bêú~ÃfsEÛxÇ#oÏoäÅ¾Ê5
óqbÒNòæêZ·î:Ùj2Ùd>Þ"E\x0011:ÎaáðöÌô:fO×tì6{¼k¸¹»m\x000fXîç3C×­~mÛ\x000bÄÁÛýçÂ\x0019½Ð+.¥î,¦¨(Ù(\x0010V(Æ0
\x0011ÊµÍ D 
I\x0015¨ \x001bÅgcÞ¿Vµ)C!Å\x0015P"¤«T÷\x0012Ó<\x0011b\x0010ÖZ­êJæ4N\x001c^ßøöý+Cß³ÛnÉ¹ð\x001fù\x000bOO\x000füøå\x000b×··xïè;Ïù×æz¿g&iæ?þÈÍõ=m×É:r\x000eÇæâ\x0014­c#!\x001cy=<òz|$ç\x0017LkG\x0003-©4\x000cÃíæÍöÂ5FèÝ%s æD,T\x000e)ÌiaNSX X¼\x0013*}Li\x000e<½¼òúò)	¡mZ~øü/_¾àq\x0012ð-$\x0004¢ÎQM&²bÏã-#¢ay°ÎÇ &¬úW+Óè¹øÔó£Uä!]\x0013Þíx9wÏÚÖTF§tÎªµÒÏYMëµ×oë{»(hk`Cëlïd¯¥u\x0006ãeC)\]íY5X÷½Xyïe¦szÃ\x0019¦±\x0014\X#óÊHIº\x0012Ó<óÃ\x000f?°Ýí"]0ääì\x0016ñ,)ã/?üÄîÃ-ß~ý\x000bs)xgØìvl¯>Òu\x001bÚ¡ãÿú?ÿ\x000f~þþMfO9òéÃ=÷÷÷\]_Ño6ì®®éû
®iE;êÄ\x001bÉ3(Võ\x0000Í\x0018öû\x001b\x001aW8\x00109N\x0002áy+I/ªÝâ¥	8¥ã\x00191zßÒVsý<%8e5­\x0000Ë2¬Ád!\x0007\x0016S,!ÈÈQÑâ²"\x0007\x0015E¨÷Zcò¸t,\x00128¯\x0008­ÿü¬^Virv-Æ
°T;4\x0015ÕW\x0016rÝ\x0006R\x0012Uß\x0016aº9Ð¶\x0018\x000c Ò)@÷ïIrÏYØ§q¢h[Ï°i±®ÁZ)(R,,S¤é3Þ8Ù×4\x0014\x0012V¢iUXã[Xµ-¥X|½8gû\x0018¹Ù\x0015Z\x001fP£ÑX«R\x0011_ëõB²þÛÙ\x0006çb\x0005µ´ý@¿¹bØ^á}Ç\x001c\x00021eîï?r{{Ã2ÍN#óôÆfØ2ÜlÙm<Óqa\x0013­oÙ}\x0010ÒHÎÓi¤m[öÛ+qv±"ö\x0014a°
`LC%\x0002Z±Ã¹¾¾b·ß[R3ì÷Z\x0011r¶sªAB±RRÛèsø*¥\x0012\x0002jl8\x0003|E;`{y.µ:\x0013@POQ³\x0006Uìë\x0002eN
½\x0011\x0003Ä\x00140f|<\x001cùþý;ãxâþÃ-}×\x0013cä/ÿñgþöËÏ|ùò\x0003\x001fî?Ò÷\x0003!F\x000eoo´Þ±ÛôÜÝ\cNïó§;>ÝßÐ4Ót`6yY¸½¾¦oZJüù·?\x0013Ó/üË¿ü\x0017>~üiÌJT©\x0011^´
ó\x000c\x0016b:0NÏó\x000b¥\x001ciu8¿\x001bmãñM ó)ü\x001b&.Òx\x001f.sb2!À\x0012¥«ÉXÆiaÔ\x0019µÎö\x0018cÈÎà\x0001Û´5\x001e¬\x001c¸ô+I k[a°êÏ±Þáµ3³Ê`5ïáGS%\x0000ççªFêY\x0013\x0012\x0010"9^ \x0008'g¨û\x0000ë
s\x0000¶ºPZ=]a}?W,j!µv\x0002V~\x0016	@ê¦T!j\x0007Õp;«·d©AUßgãUá½Ã\x000c=w··qâh,Óë\x000b)E¬\x0015j¹Àñt¤\x001fz>~üHÎ2ÏNyY\x0019S\x0004Ý}ív i;þéýß¸úõ\x0007þúßþolãqÝÀ÷ç\x0017~þåÿ¥ñÇ§ï|}|b~}á~;ðñú\x000b·×{î>ÜÑïö4Ý ­¸\x0018»®¦\x0016¦Nra'\x0007él»¾Ço74Î@I²ú¬é\x0018ÚyI8D\x001a#ðVC\x0006d(ômÞëðBë=\x00051\x0015OU¦¢HÄ39ëN:2ç­³×\x000b÷\x001f%\x0015©~¡F#ù_9#.Eà\x00160ò½.Í¥A¥4\x0017óüu<u\x000ep\x0004¤\x001b]\x0005ïÈ\x0012áEWV\x0019#ò\x0012X¼ohVÐ«u&h)êaZÔ!å,ûD\x000f«ë
]ñÒ\x0000ä¢Ï|¤\x0012Î7Ò`øÑzßâ|oz1ËÀ9\x001b®\x0017$qúzq.»:M{ZñÈÍ3¹êô"ê/"Éük| ÒpY\x0017mRÀ»ýÕ\x001d]¿Çú\x000eãZ\x001c«\x001bÏ\x001e\x0019¦DÒîW"ÈÿÏÖ5I\x001cYzmwñÝcÍÌÊª\x0002Ð(t-Céyá\x0013Âg\x000c)M
g¦e\x001a¥PY¹ÇêëÝÌ\x000fjvÝ\x00133\x0001)df/÷ª\x001e=ç¨QÛ\x0017î+LPa²e7	ðÝÌ`Åâ&Ã\x0015_\x0015¤à¤@n\x0006\x0004E©´)ãÈhL[ ¢SE\x0016ÜØ*S¯L]UÎòÅã/æ¹qgTb%R¶54'P2»ãA`ÝI]cP\x001c#?ÿüW>|üÈåå\x0015¿ùõoÐýÈ»woÑJq<5wG>¼{Ëv·¥9n)ËétJU:®.ÖTNóüø\x0005?_\x0010¢¢kì7-«åÙ¤æx8ðþý/¼ùùg¾ÿî;®onX%www|xÿùtÉÅú¢(yqóß¾åþþù|EUMÓ&Ë=)¹\x0016#|®\x0000\x001dý!>bËUY Õ\x0014©t&Â\x0000j ²¡iÿB{ÿðT\x0011½Ã\x0007GÓ\x0018\x001e\x0002ûmdèKBtxmðQ3øÀ\x0010\x0005
-²`µaÿüÌa·¡¨1à}O\x0018àÓçÏüô×PJñêö%«Ò$\x0005é¡Dïq®\x0014¬6IöF@\x0011| OB\x0018'%Ä1ðe9X\Eò,ÈS\x000f&­·¯zs¢\x001b5F¦tç­!)hY}Nù:èS9 gF¦±\x000f7V¯ÍÒe\x0011\x000ej¹f~\x0014Q\x0010L@ãc2[ ®\x0007Ü0ðå°\x001fa»<´ïzî\x001fîÑÆp}}CUUødzÜµ-hEQ\x0016ÖÒ5->Fú týÇÇgþå?ý'êÕ\x0012UÍ0UÉOï¿ð_þËãÏ?þ\x0015­a6Ð\x001d\x000eLudzyÁb6e6m\x0008å,©k=yK~\x001cDnqhhö{b\x000cL§SAo\x0012Ìë{%7©&L\Å^·25\x0006E¯d\x001cFË´ø\x0014¸ôx^N&\x0004g(§ªÝû0\x0006ß\x001e\x0004ïÑÚ'²\x0007/\x0004ðh±\x0004Kç`Æz2\x0014\x001aÓZé~û`ë\x0018Eó9dGTUpJäÓ\x000fb\x0010¹¦N\x0005P\x001c\x0013ZÙ\x0003Î\x0015Ä`é\x0003càS0&TÙ»,'\x0004MZÇò\x001aò\x0004¯éü	Ö\x000f>°Û\x001fyzÚÈLCe6Ñ\x000c]O{8à%:'ÚËt!\x0007\x0013ièòñ 0*\x001ee"\x0001\x0018°9\x0000äLö«¸N\x001ev@ÐA0åqsÛé,Xf>\x0019é°yr¯ÒFª¼z¶%(+0q8cÊÞ¸ÎYtfµ%¡p\x001e\x001c\x0012G\x0015Bél*£Z¬¨HÁ.Ã8\x0019Ö9/ÿó3Äk0à\x000c¢<ïIÅ\x0004-Æ^õ<ð©ó\x000eºÄè3Zú\x0001Í±Á{ÑË\x001c\x000e\x00076gTÉtJ§Í3mßqyqÁt2a¿Ù³Ûl¸º¾fúê\x001bBô4gúî@ô\x001d}{à°{(ÄÇû/ÔuE×Î \x000eÐ³^Ïyñò\x001aE`·ß³Ù<ñüüÄb>c¹É´v­h»\x0001k-ûÝ¦k9´
ý \x000b´ë{H\x001b×%W7¼zõ\x001dW××¥k\x0007../)ª\x001a³©-§ë\x00173rM\x001d1nðþ	c\x001b´
©>Á®#*]ç\x0018[BØ\x0012\x0007næ¨¸»÷¼}säó§ÃÑÐ\x000f\x0005C ì))CÈ'eêõÒ÷4
¡o°V¤
F8ßVDÖFF³dÒ\x0010"mì	û=nðâ Aéßf¨\x00112\x0014æràë¬/µÚ FNs¦±\x0013ÍÛ\x0008³ BálL=î4¯sV
æàv\x0016@óE\x001c×'çÕ \x0010\x0018&.×zI´¹9jj¦`Ç¤¿ÍEMB\x001fD.R\x0010Ê0áê)¶¨Å%%$3á\x0008]?ph\x001bÖWèÒ\x0011µè½Jçè%XCçÄÃ«@\x001f\x0003]Í¾ÃÛ=ï\x001f7¨² \x001b\x0006.VK>¾ÿÈ_þÍv\x000f*²}Þ²T\¼¸äòâåjM5©T@§þN22NbkB¤÷\x0003ÇFæ÷9ç(g5\x0000¾oÓZ mÁZGé*jw¤ë\x0006¬"õõ""+Ìr\x0013	\x0001%mÐÄÞ\x000c\x0001\x00101KÀ\x0007écG\x0012\x0013X\x001b´±b©bs\x0018\x0007BµN&þJaµ¦O¶oÙr\x000e\x0012|¤\x0013îZî5
µ\x001fdëåÀ++ç4ª)\x0003ªäõãDú·xj*	¾Æ0hO¶»SJû¶\x0015\x0013ª²\x0014¥\x0014WkÌ AzË\x0003P\x0010cÏ0\x0004\x001e6Öá´¡p\x0006me=7Ç\x0016cö"/Lð-\x0014\x001al@¹\x0000®Cé\x0006G\x0019ÑÈ óôä½çù\x0019$\x0006I\x0014à:þ\x0007_©_)å&U:UZJ[ñÚ¬'²ðAå¸\x000e
\x0015\x0012µTeÚYõ\x0018O¯\x001eÓ
ÉÒçüwHï7Ã/#­^ËÌÌFôi1¤\x0000(Y8)³\x001dPJ%×$ÝH.è÷Ä\x0018X,xï¹¿¿c»Û²Z/O't0H3»ëþþÃáÀz}IbûÒ\x001a.Ö×X£h\x000f\x00025~ûí+%Î\x0006jnè{æÓÛKªÒ\x0012\x0016\x001d\x0007êÊ2Õ\x0010=ûý7?ÿÌÛ_ÞòÛ¿û;^½zµs>¼ÿÀÇ\x000f¿P¿ÂjÍt>åØt´±gµ\òâÅ\x000bf3	>îxùú;.¯oÑ(·(sàó§/EE\x0008ñþòçç
ß¼~ÍÕõ
UYÈZQù\x0002_KE\G\x0008\x0007b<jQ±'"#CÆÔ)UÒ2\x0004\x0019÷ÂhÕøØ÷^ôTÇ½b\x0018
\x0011ø&z²ÍÌ²>Ò5\x0010¬¸:T\x000eê«\x0005J-¥Bëë[êiM7t<<>`0X«Á3O?ôh\x001bd e×K¨IÜ\x0012£-Ê2\x0006¦\x000c§H 3©Ï\x001dÒc3 ë|F\x00005Wd¹T§Gä>dô§`4öN»cüWH§Rð§{\x001fãÏ/9\x000bL¤P câý¨/3^Ì\x0019r5\x0018¾JúNçA@Ñ\x0007-§NØöü(ê«J0òYR8c(Ë\x0002O \x000b\x0003®rÄFãbð'O_8vGêÅÅjÅöyËÅÄ"\x0000\x0000 \x0000IDATü\x0013\x001fÞ\x0004¥Nj¦eÁÅrÎ«\x001bnonX¬V¸²Â¸\x0002´Ty:¡Iâ&\x0014è®m\x0018º\x0001c\x001duQb¦\x001fz	\x0004Ôk\x0013\x001fHgl:å\x0000·Æ`£\x0018²+%1)Éç«Øð\x0007e2k/\x0007¼Ñ]'U)ê¡\x0011Wt\x0016ÖÈÔ{ïG3\x0006£$QFîD\x000c\x0007¬iûFjÅ\x001aé¿
Þ§\x0002 ¿Ç³ä-\x0004gÁ.ÃïjÜáhD	~Î\x0019!¶(Y:\x000eöx<R×\x0005\x0017ë\x0005®áÙU©è\x000cñ>¶¤T\x0001¦ï¥âÔ\x0013ªÊ1\x0018)\x0014aÈ#4µª0%\x0010\x0006¨¢C»\x0001\\x000bº\x0005%Á.\x001ai\x000f}Ed9¡À'ó\x0018\x0000ãé¡»_}é\x0008#u0ÿR*a]QRSÊ¢\x0012ÝMº¤>mlú=\x0019\x001c·lb\x0019æªIN\x0014É}\x0000%Ï!¥´\x001eKLlÄÄv\x0012Í¸èT\x0019\x0006ïÙl7ãôÅb\x0001!²Ûîøøá#JkêiÖÍv6×¯_³Z-	çùñ÷ïÞs8ì¨'õÇ\x0018ÏçÔU%Î0ÃÀ7··Ìf3bÜ\¬!(ê°Ñ>|ú@ß7,_Þâ¬áóñÀÛw¿ðêÕ7¬×+HA·ïZÞüü3Ú(f³)1x¾ãîî\x000b\x000f÷×ß¤i\x0012é´âæêét"VcÖquuI]W,\x0016KãB¬»ú¶çýÓ\x0007úÁóâå+¦Ó\x0018\x0015Éù|IßÇß0\x0004«\x0018H²¬¹¾1¬/¯¹¼¼d:\x0007®f@8ÆDås0¾aè÷Dßz\x0018br¤ cþhbPB±öiý\x001e@Ói=áêrÆbV\x0012(%\x0018%Óf
X¥0J6p\x0016*\x000bQ@\x000c»Á²TUÅz}ÁåÕ\x0015&\x000559ôâô_,\x0016K+¥Y®uÁe
\x000eó^J®L607£n\x0018G²Üig\x000e¬IÌJIeêæ\x0003\x00082£7Ut\x0007ÒÓ¾
±íJVùùò\x0001'í\x000c5¾là­8´\x000ca`\x0018zú^L§\x001fdtOÒöY'sæò8¨à;ºÝnð\x0014eî*Ú4ç­\x001f¼VMJ\é¤â-ì¨w+\x0001Åh5¦ª8ì÷¼ÿç§;\x001e\x0018Äû;¾ùî[.KV³	íjÁÐ{®W+n¯/øæöß¾~ÅÍÍ\x0015å¤\x0006£Ú¡´C\x001bÚ.r¯d_OD3&
±Jý­\x0018ER\x0013\x000cÄ\x0018d°³ÂYU"³xIh\x0016Óí<4zF\x0019ETÐÓ÷ä\x0001ÒÁgÛ¹(¦Ú©)=céJï6ÌYí\x0004M³öÄ&Äô\x001a2ý\\x0002¬¸äzÇ\x000fôi\x0004¬áxZV_ýåôýAs´µG¶N²\x001c¥\x0000£	Øq<\x001eéú\x0016k4ëå*\x0005>
¬çØö²OSÍñØ°Ýn©
Uîi+âÿ¡\x001b\x0018zIÓ @
­\x0003QH\x0012mälÒg:½SÏåo"»,á?e¢ÿ/ÙpY%\x001bP\x0008"\x0016g**WãL!pMÂ9|\x0018\x0015dº~\x0010A©X@\x0019aw\x001dx½õ}K×¶Lê	eU2Àv»'\x0002³é¢pìv2\x0010Öû\x0001£\x0015ÏÛ
mÛòâößüæ·\x0014®`Øñ×\x001fäÍO?3_ÌøÕwßRUe\x0012M7ÔÕè[ÚÎ³×,Vkf3\x0011¸ïw{v»-ëõ_}ÿ¢×¼{x¤k[^¾zÁt:áéñ_Þ}¤Ï©RÖX\x0018+ý\x0018
Ì²÷²ð&õ««[¶»\x0003»ÝÃaÏ|>c\x0018\x0006¢âßÿÿH\x0008Csäþþ\x001eb»ÝÑ÷Ã¡!\x0004¸ººäöÅK..oÐÊ°ÛíÑ³ùbÍd²D+MÛö\x0018SQ\x0014\x0006WÍpÏ;¶e22_Ì¤ál¥®S5¬Ñüý\x000f?Hv\x000evã2ôu¤d8à|¡(ú^J²®Ø0\x000c\x0007Úfæ\x001ej¨ñÉÁ'"Bg¥D\x001eã?QªôÞGÚÞÓµ\x00105!¾2÷FÑû±\x0003 \x001d\x0004b°,N\x001d1FdV_5¯_}Çr±`¹\Â\x0010	½ô­bïGoHk\x0005Bæ\x001d\x00104õÅKñh­GV¥\x001aû¾g\x0007â\x0014\x0008ÉÂzùAN\x000eÏ·Ý°¢%!HN5cð
áÿ±³ìO\x000c¾LÈ\x0004BÈå¨#CôézÉa/\x0008¨H\x0019ú¾£mZb\x0010\x0001¸FQV\x0015hKtoÄW\x0002)3í\x0019|ÄyùìûÝ&­¡¶\x0016ë\x001cÆyB\x000cR8k½A\x0002[Ì\x0017-Ï\x000fÜþB©aV|)hCûüD¹ZòOÿîæOÿú\x0007ö»-ß¾~É«Û\x001bn¯/¸Z¯¨ª\x0012m-AÛO\x0002ãE\x0002\x0004qP\x001a\x000e¥ä³XSÈ½ðYn\x00121hGi-\x001c¶°h+ùL\x0010\x0012û1äÂ$\x0004c#YD\x001e¼\x0004½àÅnñ«ä#\x0015
*E\x0014K®¶åg*\x0011¾ÀhÔãû6z¼¿&ÿÝg\x0003Ä2ÚçÔW\x0016v¨\x000fa$2P\x0003ùß)É:¡\x000fÁËx1y³at\x001a\x0002N=iíèÛÝf3R¡êä	\\x000e(#¬ð\x0010\x0002:ÊhµÝvÜ]*Ì 6yÚ\x0007º¶C;#~²¥éBAªh\x001dd(\x0002Ê@Ô-AõØüF,?7¨ÎÏ¯ñÿÎKÛ¿xq¬ðr©/VV2Aí\x0004
BhÄûÃ·ïßÒ\x001c¬\x0016+&õæØððpOYVL&5C?°Ýn¨Ji@ïö;ÞxÇl6e¹\Q5M×Q5ZÁÓcGÛµ\x0018%a!xÂP³ÏxqsÍ´ªèû\x000e?t\__r±Z`\x0014\x001cv;¾<?à¬e¾X°ZÏéúO?Óv
ëõ
­Ò¬»¾èéO»­Ø'Å@×\x001ch\x000e\x0007|×R,ç¬\x000b¶9ã§\x0007¨LaÈz¦¯^0Ï)"-ìÀÕå\x00151F¬-\x0000\x0019ëóöí\x0007B\x000c¬W\x0017h-y×«\x0015¿ýá÷\x000c¾§i[ÚcC]Ï©êJÛÉtf\x00112ÑJËôíÄn½¾Ur\x001b-ÓÎèDª¹ÆS§\x0013¼:é\x0000óÝ>ëßñ\x0010\x0008N\x0001q ëvl·I;5<ácO\x0018Ë|!\x0011i\x0015S_BÉtt¶_$n\x0008?o|øØð¼ôÞ¤ú,Ð½,\x0019g¬eø0ª\x0004\x001dù§çg>~ü6y5OpaÀ£h&3|s.þMì¯¶BhNÚ¸\ñæ\x0012,{è§Hv¸$vg"\x001c$$4ÙQïO\x0005\x0001¼ïÉ\x0004\x0013?êòR°\x000bÉÑ&\x001f¤çû5&&°\x0016
NP2Z¬°\Gk\x000cÚÈ¡Û÷=q&\x000e\x0018ysÂ\x001b{¤0\x001d\x00040Ê\x0012¬ÈL6ÏOø\x0010D¯;­1Î ­À§Ä¡NãFûA¬¨´a4¼|qKô/w÷l¶;BÐtY5åù_ÿ7÷÷<X¸ºXpy1gløTbî)%ý[	ðr]2¼§P2ÆÌ¤\x001141ÝDþÊ\x0012³\x0003Hb|Z£±ÎR\x0016\x0005eáh|'\x0012\x0018£\x0010K±ô9TFÎÒsæ
}
\x0019[<¿K/0jù0²¦k§Qh±füÝÈÉ#5k¤}²ÆS¨Ôb©z\x001f\x0012Ö\x0017¢Î®+ù\x0004HEÊWÅ_ÚK*õ1a ¤Y©Ûtz¨´Ã÷=C\x001fh­Ùãý@UU¥c6«1Z³
®÷9ìÐ6b ß´½´ÊlZ¯Cà¸;`ÅÖ\x0005:(T°bH­5\x00046\x0010\x0008äL² á.}¶\x0001eû³ÐsÑõÙ®Î¿\x0000Q\x0004òSµ\x0005UêçicEGÕ\x001eÙl8ì6\x001c{T\x001cØ<>0-¹¼XSU%ûÝ\x0010zno®Mg4MK\x0008\x0003¯^½@\x001bÍãã#Óºçêæù|)üÐ±ZÎùõ÷ßR8Ëv»a¿?`a¹\â¦ë<\x0004ÏtRQ\x0015sBßÓ\x001d÷D?pì:Ê²ÀjM52ô+>~þÌýý\x0017ÒIó¹oQxª² ×\x0003Ç¦A)¸X­øîõk\QÕÁj½¢O0ÖÑ\x001ek,®°\x0004\x0002÷÷w¼ÿðë\x001bVË\x0015Ï
÷÷wÜÜ¾àåWL&sª\puõ¨\x0002\x0017iúB d	^µ\x001a¥ÏÜçÓÚ\x000cjÜ\x0004¨MJp:oó\x0008Ü\x0017sÐÆu7\x001eø\x0019VÎw?Ä\x0014ôÒù¹®uî¯\x0000
}ØÐ
\x001bl\x0011¥ºVJæv%Ê¬Ò1ùp\x0006ÈÎüÑ§*<¢¼BwÓw}KÓ6\x001c@\x00080ñÔù:ÖñxVùäÍ\x000c"ô=\x001e\x000fâÂ9Ma³ÊGØ&O\x0000\x0019I\x0010íQà;R)eÜ\x0019^\x000cÙ=õqÆ0ú8V½ùñD5fîã\x001cS Ï0SJ\´6dãé|úè<©ý¬÷®\x0010&´Ò&\x0005½t\x0013µ	Yª\x0013\x001233\x001eÕ\x001cC/&Ê1òüøÈÇO\x001cÍ8¡ª&¬\x000b6\x0014Î¡§3sÄ¦áÐ¶ô}ÇÅõz:\x0019¡Yã
Êj:ÒíÃØÇ\x000c8+nK×\x000cmï<xh\x000eæË÷ü¿ÿÇÿ¡çöfÍËK®//Lj1\x0011Ð\x0016¥Å\x00160Ó­£\x001fð^Þ¯V`\x0012ãJbj$\x0006\x0001A \x0006dÖÑHÖ°Ëë²¢.JCñ2|x¼Î\x001arB\x000bù¼¸\x0014BL£J¶erw¢J½Ta)Ö\x000b§ÄÇ&ÂM¨CU\x0015'Ãðî8*eFèX¤÷Ö÷~¬ô\x0002&!*2p»(¬\x000cU©õcDZ¯çû?¯}ï\x0003\x0018©@½ÕYÉVóu®\x0002¼Oð«æpì9\x001c;\x00163Ïb>¡¨,Ué0Ë\x0019»=tmK\x000c2¶m¿o¨ª#ÖÌ(\x001cD\x0007Ú&DÓã\x000e[:T\x0010Áº\x0012âL"\x0019-\x0019»=Ó¹IwTfÝW¸c«ó«Ç¦\x001dx\x0016<ÉÖ\x0018Wã
[`¤Áy8îyz~¤ëZ./V\x0014®àùaÃÃý'Öë5ÓI1ûû'ö»
ÍR"\x001f?~Â\x0016ÕzÅj¹àééî]ÃÕeKUWTeÁd"#yÏçÑ\x0016c\x0014'ü¦ùQ½ÌþÁs±^3Í/\x0016\x0018kd¤u\ß\KÆ¨\x0014Î*\x000eû\x001doúÉdÊúâ\x0012­5mÛòç?ÿÅbÁju!UÈó\x0013³ù\x0017·L¦Ô\x001fìP+Í¯(ê)U5a1³\¬ùöõ·L¦Ó4öD\x0015/.×\\]È&R"\x0014Î\x0010ÏÑMe\x0013é\x0014rÎo
Q\x001aâãwR?ç\x000c7\x001b!³_Iç5ÉìÔ£KÕÇX±¤_RJò'wú©
«­°§bC?l0®e¦5Ú8BrJ1 i-\x0006Æ`GìS© S/6Y!ö8H¯nð\x0019êó¡6lSféTSò¾­Ö\x0018kL&Ôu-L24SdÀUu¶mKÌGÊ´r\x0006\x0003Æý[å`\x000fì!JNDÒûÈ\x000e=ÙL:3ÿ´²c\x0010\x0016\x000b¨du0;¥}2¡Î¦\x0004rO:Uà2Û.\x00054iº|µcÉF2Ã6§)âÖä\x0005\x001a¹ûtÇþô'&uÍ|±\x0012H~`¿;òpOUÕ¼zùù|r\x0005Õ²a²\q<<³\¯)Ëõ\x000f`,Ñ8¹Ò¶GGÁ'ØÑY¦I]RW\x0005éV;)T%;VK..×¼¸¹¡¬«´¶¥i´AE©$!Mfø£èºDQÊI
\x0004­åw\x0018}uE\x001c\x000e4÷ï\x0018º\x0003ÙæL%ÊZÊIÍÜhêûÑ²Ëh9uº¯0RÿuÚ§ilçéÌ*UÌ\x0003Ùýê4.
4\x0011£\x0012c±\x0006k¤º>Ää)\x000f9r	¸]ç\x0019znC$Y2¦\x001e¡s\x0018#{.Â(¡\x0018AiT¾!gI\x0015cÀ*¨nB+!ß(kÇ¡Ùaä¦->p8ôXÛ
8g)Ë\x0002¥¦lOF#¢Õ<î[êJZ3ÆÓÑJ¬â\x001a-5Ø\x0002m\x000bP\x0005FWX\x0013}!=Y\x0015±á<Ø\x0017þôï¬ÍÆ¿=\x0018¿Æh"ã¨\x0014iÏÛÕÁG6\x001d}ðì\x000e;\x001e\x001f\x001eøôù\x0013ÓÉ÷ÔUÅrµÀ÷²pÔUI]h\x0005>}ä·o©'\x0013³¬/®Ïgâââ2\x001dT&É\x0001¶2½8e8]×\x0013\x0015¸²q:!ò¼Ùòþý;¾ãæúÒY\YóôôÌû'nnnQZ±ÙnéÃÀ«o^³\\P\x0016\x0015Zi®®ohÛ\x000e\x0015\x0014«Õ\x0005uU\x0011ÛÛ\x0017hmN§\x0018\x0003%UC!þ¡ÊÈ\x0015dmW×\x0013.¯oÈü©p\x001b¯ûyU5^ò\x0008imM\x0004âÙÏ¾°ò=:\x001dããrº?Þ=içe\x0000 Ã!ßT"Ã@ö\x0008E)\x0000}a\x0011MÓt|øø\x000f\x001f>p±^óí7ß°[ ¥ïwp\x0000Z\x0008-!öÂ¬yíeÀ m¸\x000c	EÆT+#ÕGÂ0\x0010}þ_ë\x0012Òa¥­J\x001a)0Úa^>\x0005\x000bk,³Ù\x0018áx<\x0012{9%rhº\x000eß¥ùfÞãº^\x0004Â¹·¯û9D­V:ùq¦ÞOrÕÉ\x0002]2
¥Ò\x0016Ô(D#Ùøå[
gm13IaúüK®g\x001c¯¯\x001eá³ü§TçMÓÈáÜ\})éaßÝñâÅ\x000bnnn0Öq8\x001c9\x001e\x001c\x000e
Çã¾ëØn·Ì\x0017\x000bÊIY-)'5Æ)\x0016ë5Fyv;q;÷\x0003¶\x00080ò³UÚ\x0000@®³éõ\x000cHî\x001bOa\x000bªª ZºÀ\x0014\x0005¶}*#Ò´(÷Ô\x000f^ö²x£Á9-	®&\x0016\x0015ÖÕ²ÀÙ\x0002e
´uâÖâ\x001c¾ÛÐ¶;ºí\x0017\x0011¢\x001b-kêÕr½¤Þíy:\x001ei\x0007	V:¹´D­(ÒØ¥\x0018ÄìÂj=2xó\x0016Ï	Ê«^e=_L\x0013\x0012ì\x0008;wX)RlNkR8\x0012!\x00061\x0014®:KT%9Ëgzð!	çµôÌs\x0012«rÐÍã§DhÎøº9\x0000AµJ¥ñB \x0015ÎæV©²Õ`$\x0014Q\x0005úAf\x000eés·]Ïn\x001fÐº\x0016Ö«\x0011ùP]×tm+Ä¥\x0018iZ1/)+ó\x0018¥\x000bÞ3´\x001d}£QV¥ª~x¤óGB\x001a3\x0015	Ø¯5wç'e<;\x0010Ox¬øÎ6úU§Ü¨4Ú\x0016¸¢b2Q5CPt­ô\x001d«\x0015Óé²(h-eY2©jfY²Íj!F\x0016ó\x0005ÁÃjµæêúÅrIÛ¶¼ÿÇG^¾xÉ|>§ï\x0003?ÿü\x0018#¿ûÝ\x000fL§3BÂÕTÕ\x0014m
r¬\x0004ãB3/Ï$Î\x001b¦a¹\aåòú\x0005ZkêÙ\x0014k¬,N­Y®/X.W©ÂÑã¤Õz=V\x000f'Q|LD+YP!\x0010ÁÐÏ®'\x0002-¦ó\x0007ùS2!»âL\x0015sÎv2Ä\x0019¡Å|o2³ðì(SêT¥i%Á,Fé9ôMÜsäUö»=}ÓR\x0016N&\x0006\x0018MðcsàÍÏoxÿþ\x0003¿þÍo¸yy#©j0Ìf3Ê² i\x000exß3M¹¼X3©
\x0014\x0003ýpdèwÐ Ô 9\x0011\x000cÎ>\åÀ"gyÈåí\x0008áX«¨«	8¹ÄX¢\x0015óY%î Eé¤Z2\x001a£\x0012kïLÌ-Y«a:Ñ´-ww÷¶¤.K1	Ol7O\x0014½_->°înNùd,\x0002-¦kÍ[XüÍ¾¢N·g|Où^~eS5î;H&¤IÛ
*Ê¤0®¼\x00173¼,\x0007:mèqÍ@ü*ÁÉ×©\x0017\x0012ÙèA\T>ù\x000c
æ³\x0019\x0013\x0004§*ÁÙÉd i<?=Ó´
q\x0018ð1ðùÓG\x0006?pu}Íúòè\x001bÚ¡áÐì9\x001ew²5\x0016{b\x0006¨T¦h¥)]Åj¹ÆÚvßÐ·=«¨'\x0015ÚE\x001e¶÷<î6\[LÒ\x0002+e	(ÑÃùHT\x0005ª¬1Õj±ÀÔ5¶¬°õ\x0014m\x001d(C\x001fÅ0\x0002e\x0010â\x000c¬µEDÏ/\x0008w\x0015±ëÀ\x0004ôÜr{sIßµ<üáßDÇèõ´ÍÝ#Ñõ\x0005ïñ)xdÓq1\x0018O\x0015hêï	éE'¦&iÿþ\x001cV M²Sdü&Ý`1\x0005EQ&ÄK¸\x0004Êñ¹\x0006<7\x0006\x0015O}_[\x0013yä@,S\x000eÆ:
\x0017Î=Iy¨íF[3Âüí\x0003!Êë×uÖ¾÷ø¨8\x001c\x001baH\x001c\x0004u2bÊ(³ªªÇ#Á\x000f\x0003]×p<\x001a&m+,®ð\x0018+\x000b6\x000cÐ\x000c¨2\x0012lÏàÉil+Z0Tzò|É+R^ù¨\x001aù^Ú!õ.dúqúð\x0018À`0(³¤G%Ä¥ÔÌçKªj«*\x0012»<2Äi÷=Ï
Í/Ç{Ö«\x000bÒì÷bîºZ-¹¸º¡¨JÊJf¡9çX,\x0016ôCÀ\x0018µ\x0005W77Ì\x0017KBÔ	ÖÚ\x0013£J[|\x0010W/¿áå«oFýH!`±\Ä*WTÑ\x0006LbT:\x0011´\x001a\x001f#\x001diìÍé|\x001b\x0007ª¦ ¥ò© ñ\x0010ÒQèùéKX°qÌÀ¬cB\x0004½=ó¥Î`Î\ÁÅDÃnÄ¸·,K\áèº>UØâ³ys{³çÍ3\x001f>| ®\x0005jE)>}üH\x000cÕrNá¤°Û\x001d(J3«5ÎÀöéQz\x001bõ\x0014¥\x0005êº#m×°Ï¹\-ÖahhgÚö\x0011B+\x0014r
ò²Ë£@"
¼\x00174H\x0016\x001aCvï\x0003]\x001féZ0\x0014\\Ü¢\x000c\x001cZC\x0008\x000e¢¸U\x000cÑ3\x000cyb¶§ï=}w\x0018Ùgb%P©µ\x0005!ÀíÍ\x000b¦ó%ËÙùd3N\x0008W»
~èÑVS×5E¤\x00111ÃÓ8ÔÈ
VãAH\x0002YÕ©\x001eÉ	Ì\x0007×©H\x001fïôøó|´Éz\x0016ÒkÉ7s?2×Ê:-»h¥ê-5qcÒÜ©¨`\x0010ø8Ãµ*õSmÃn÷ÌÓæÝnK]U\x0004%\x0004\x0001\x001d
A\x0004Y\x0014Ã\x000e[Ö­¿üá_Ù?>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/2021-02/2021---affiche-snu-personnalisable-141.pdf](https://www.snu.gouv.fr/sites/default/files/2021-02/2021---affiche-snu-personnalisable-141.pdf)
  
  
  * Method: `GET`
  
  
  * Evidence: `<?==WÏO\x0018\x0011úo\x0001\x0016/|\x000eJß$\x0000pâw\x0000\x0008Ô%JdÞbGB±Ý\x0007í
ìàÆ¤S2í\x0014¬¾Lô\x001e\x0003\x0011Ú8\x0010\x00027:¬dwö/ÕæðG@¬Ô ¼ÉÚ\x0007nJá¨É+Î"Y	éõâ	\x0000'gWëì4ùD#n]\x0002lw+Zp·îLC¹Ð|èKIÜÔ\x000e\x0008äãäÓî\x001b|LÜþjZ\x0018f\x001bçÂq\x0007.\x0005Ò¥{.Ü4\x001e\x0000\x0001\x0004_!B\x0008\x0008
qx-¬´#¸	\x0012¹	»RNüÛ£37\x0001·¤å<µHPÕ }ë[ò¨I¿íhG\x001d"jÝ~9¬ã>ÉÆrýâõ\x0005/ÿzÜ -\x001c@ÀMÃhjtãÒàlªÈ#\x00188\x0017)0G\x001aïä1NãL¦\x0003u
NÁm\x001c©p\x0013~c¨FæÝ\x0010×YpY¬\x0013Þ.\x000e\x000bj\x0010 6NQàzÌ«Lßä°ð¿Å.ÚaåÛqÁEP(Ü7×\x000eQá±
ù	(¸÷îÕ#üá­\x001cí	i¡{\x0015ÁMqö\x0010\x0019ZÓ¥PØïð\x00083ôÓ=7õä¦VC\x000e¾,d\x0004PL³FP\x001bn\x001f#v&¸)Á¨J\x0017×©ñ\x0001k©tPðVYr¾x¼º±\x001eC@Â{²lÂ¹h4\x0007Uâ¦°4ÍÈ.ÜÔe¸\x0001
Ú!|Pê:dnê{\x0010ºpSWdO-­êÝ\x000e\x0012v<ÀV¼
$²ÓPaWTH\x0017ÐÜÔ¥y®;æ>¨\x0003C\x0015`åCþ8\x001f¤×Øl>\x001aõGïSÿìÌo?fèøãüóü³@2û\x00197Ù\x0004@ßÖÙÊ­\x0011}©g"y½»Ô\x0014\x0016Ý.Qg^D¸J{ìApSý3n:Oì\x0007ùçv!\x001f\x0017õcn*Ë}¿äy¡±ÒûìËÝQÊ\x0008(­DîmctÜ6FI\x0011h(0×!÷\x000f%s\x0013¿ÉM\x0011¥ì©Ó[þ&7q2Ë9ZrS¸	b²éäpWB=\x0004Í{ép ­è­\x0002J'äÁëi	¶PèÌM>ÐéÝpSýû×Óû"¿\x001fÌM¿	\x000bÇ \x00007áì¤_-\x0013 »\x000b\x0015ª|Òw((´\x0002BnôÈKÞä\x0010rêÂMÓ08pH¹©\x0011zYRÊçÐæ¹¹É(9!	¹iBúÑ½²Ê×õkq`ä¯Ü4|ÊM©{þ\x001a/©´ýðóo¹âó
üKæ&hèl¹º\x000fcÔ%-\x0018\x0002ÄÃÅ\x0004ÖÅÂÙ|\x0016·¬\§\x0018Þöf\x0008h¢ù÷×h¾ï6ßá,ÎÜÄ@³d'0P0?íÀ\x001b\x0010EÈílÅB½0¼Ì\x0015n:.t\x000cH\x0019³C\x0010MF±:µGÌ¾®@:y #¨à~í
Ñs\x001e/¯2t\x00154]O7òÄõÉ\x0018À§¤º¤RÎ\x0017ÑC.Oq\x001dL©p2©Þ<\x0007ìD`ÌÑáÀã \x000fÊ9s.?aH%\x001bbÑ$\x0018bJràÒ\x0018³û}É°ñpÜ/ç2ÏÇc6?ÈçFP©¼nøø\x001fï~à&7ánÇeLÃp&*>\x0004´\x000bà¦ÔÏ
\x000bDnò~ñ_W¯ßÆ¤þ\x0010>;\x000fóèýGÜ\x0004#9-\x001a¢5\x000e\x0002R\x000c¡ ¬*qS¯°\x0004*Ð­\x0000¡th\x0012¾MÜ\x0004êéLá&|?5ªéÚ®#7ñ\x0008\ÐÒÿ=D»½î²ÄM¤X\x0018q\x0013lLÜ4\x000eTÖù¦´Þ>Kñ\x0002nò<\x001cÏÜä½W\x001d\x000eÚMý+Üto>¨çÅf\x0014«ÚMR¡Ý(£4&Ë`ç±¸-\x0008aÔ^ÈM&s\x0013ÿ&7læ¦¶í[n\x0002vM7ºÌMmá&ü¼õ\x0017n*QP¢°\x001c#áÀîÃ>)yg&<Õ¥=28sèÃÈ}f½¬=µ\x0007ÛýØþ;o*x,c\x000e\x0011ßÙª©*s)mká­ß\x001b[¢0Ñ­q	\x000b~Åèª±¦1À\x0006Ó8[«\x0003#\x0019QáÌb´ìªÎòæ¸Äk¯àw\x0008ÓóIÆÅx\x00022ð´\x0006
N;]uÝþjdvq9\x001dÍI©ªB¤gÄ\x001en¯*õ'ÀyÁÀóªæR\\x0015UtP\x0014°\x0015þY×Õ,N\x0004CMuºá\x0017Çø?Þ«l¹q[êÅ±EAà
X\x0008dKq\SºU÷\x000fîsþÿ[îiÔ6gt\x001b$eØºûôiâª°Ê¢\x0010°ÜrüÍ¿c¾\x0005D!¡æºéq*IËÑJ\x0012£Ìß\x0011+'\x0012|x8öÎUµ,K×\x0008\x0003PH\x001cú>®Iè¨"¥ElYEÓTÉ¼NZ)­ÓªYFWx?!½°¡!Åo&$¶Ýb÷¹
}Ñöm\x0012mj·V·¶AQÚêÆoQßªD*¢\x0010	ò\x0001\x001c	*lÿÉVwÒàÅë1(e00ºÝWÀ\x0004JuÚi
£5\x0007­J°(iÊºÁçJäU\x000bGi[\x001bT\x0015¤PiE®0öªcæÓÛ=Î7\x0008½ÄWj*\x0018ÆP[N)³@®²T%¥G(\x0014\x0005\x0019,AY¦\x0018õå0wì\x0007v'%\x0008$Ê/uÓÕ\x001dKV:·wx¢ÚÒmÜ"
­®Ñ«Ì2×í+jµHÝ½Ä!¿/\x0002Ää>\x0011ÆÉ·Û\x0017~/Û\x001ag+æÛ§t¥F³®8\x0013e¯\x000e\x0011Aíxl\x001aj+*Gî©9·CTì\x0018SÑøâ 0*UWTÝ"zIiÁn¾,\x000fq\x001bÍg«þl?ì/Þì¦ÿ\x0005xÉãùmûcnÌÑð½ê\x0007¥Ø£eÕ`V¥Ð@²\t&\x0018VP{Ñh±´3TSYI®¡\x0011FYÄ`àX(Ñ¨ïËvÖå`\x0017£ýY»5ä£Qï%{ÕÜ÷&

K?6\x0002Ôó¹ïÉKÉ\x0003Ö¶zîm#ï¸mä%sÆ¡{\\x001e\x0012<Ï\x001fdv!ºcoÂC^\x0016C^çû\x000b23\x0005ÜºfZ-2`Âb\x001asÝvVÅ\x0002ï+¬\x0000ÃâAj0¨ºO`û\x0004À¯Î5@(!÷\x000cì­\x00130¢C,Ü}y;wâcêà\x0017\x0019þh8Pà2ÁÛF\x001dP«Û¬®B(OÓ\x0012\x0002+Áù6¢îfv!ðPJR¸\x0006Å\x000få9)¤¢l°}"».¦¼¶uK¥\x000b\x0014B T,vlp)0¢2\x0007é\x0016â0¼ûª
Huóg	/÷Û\x0006dô}LS÷ÂÑ#Y(WjPñO¯ÿJ\x001f\x0007ð?\x0016ÊßÒ\x0001C[MÆT¹«¼\x0010 Fj]K+ÊL\x0000À.\x001ao?`ÆFÞ{÷:ªÂÃe|íëßß}ýÑm>ÀAä<n´8\x0006A²+êÌ©\ \x0008Ú ÞvÖHS[i¥\x0011­\x0014aê1t¾Y3ïZÕ\x00181\x0006«\x000eÃ\x0008\x0006>
¾ÎüÜ\x000e1ò\x000c>â
CW@Sì\x0016Èggà\x0003OÚv¤ëû\x0015ô44úud0×±f½'ò\x0003z_\x0011Ã²\x0006Iy¥fÖ(E\x0014çFÈúÎûCd\x0011\x0002Qæ·m{<£\ÄOÇ±½ÈñHä\x0007ª  B<Îø8Ë÷_/Ý!3Ï#	¡ïéç¼""íøA\x000b IPöõ.ÏY\x001c¥oÖ3\x0006ÞÐÙ÷Áª×2º\x0006Z·E[.^$MÙÑ@$N\x0011s(Rä@\x0018Úõ@\x0017D¸T.BE¡Rà«\x000b\x0003ÐLÓ2{FÕ\x0004\x0012?\x0014Uâ\x0019ÁÓ^ BqõÂS\x0001ÌÝ§\x0005Ú¢¢\x0007ûÅùz{2J\x0011\x0004ÃÖ8íiÝX\x0008!køH)Ûþ"\x0012ÔM\x00168Ú\x000f%"&ÊòÓ\x0014\x000f|ÃÒeÀÉ[sf"¤[iÆJ5b»I*D7VÊ±6J.k.SáJuc©¸\x000c°?a)s±rà"Çl´Þ¢¨\x0013@-$îüùééy÷üËN,ãiÉ4	3ç±\x0000d±\x001a%\x0016ÊVßY=sõÂõ\x0019	\x0007Ü\x0017Ug2sgªHD\x001ac¤0õå §â\x000cÀB!t#ªl	êdsú#\x0000x\x0005«{x~¦©h»4k­Í[ÜèLç°Ìà;×yg½;:gPúi\x0010T\x0000âÆàS6Q]\x0000¯0
ç 2é¦ñÎwþ:ª"O¼\x0016\x0011*WÄ°MÛ8W§¹'\x0012ò\x0000\x0006\x0006)\x0014 @¦;½ª zI(÷õásxÿ¹qM¤m\x000cY\x000ceü"9dç
h°Ñ\x001aÿ\x0019\x0001P{(ÖMPC\x001b»\x001bf2SyãMg|æ3Gø\x0013>	ÝõFWM\x0019Î?NT¼yM.GZ}"Áç_!H\x0007ãNù¤NS6qq.jgHi\x0011Zá\x000c×I+¥uz3ë±s\x0004·'¤\x0017~ìHñ+m\x000fØ}Õj8\x000e¬!zæÝà-\x000cª­s}\x000f"_\x0019V9â\1\x0007îFÖu\x0018ñ¿ztö8eõÛ;¬\x0002³")¹\x0003vn\x001ax\x0005lÍèZ:OoÞq¶\x0006%§\x00178;Ûj£
2Ì¨LÝ÷íhÔ¼UDWx;\x0018\x000cT>Â]J)©nâu]b«9\x000bD\x0016×ÌDúTK\x0018L©½è\x0000k:Õºya8õÍ`îØÕBë\x0019rÒjåxú"r/Cà\x0001O\x0011²7a\x0011fínGÏ5\x0010±(Â*jVåá^âá~\x0003S§ðì÷ÁWÉn%2b½Ã\x0013ÍÇsºR£Y×FÎLÙëp0Úû{\x0008ÔVTÀé¦Ô0,¢bÏ\x0011SiY&Iz	u\x0014F­P]\x0001\x00020\x000fÈ`Lø´à0_¸Íæ³U¶ý_¼áO§?F?øÇóÃð	©XÝ×BWu\x000f\x001a\x0001ÀÜêèW¥Ð\x0018üªsÿFQÑè\x0016ÅÁS°{\x0002\x001dô\x00161hw8Ö]\x0014J;ú\x0012!-ç]ögíÖF½âAVsß|64,ýØ\x0008P¿|9\x001cÈKÉ\x0003Ö¶zîm#ï¸mä%3@Ó=.\x000f	>+\x001f(×nGwìMõíb¨ßæû6\x0003·À}]3­¶Jùn\x001fÓXØ&WÕÖu¥`\x001e²\x0002\x000f\x000fÚ\x0019ÓÙ#\x0003Ò1u\x0002ÎMmgS:åÞ\x0007: 	9WÔ	ÍÿóõãË¤¾&\x0015+\x001e?6§\x000co;sv@ªÅmVW!§i	A\x0015Æ[kD\x0013Qw3»\x0010`\x0014.ªCñSãAL
e;ÆS¦AâèÐ¡]*]­\x0013ÅÜT#	Ö¢¡e*Xk]\x0012²ªóë×^\x000e¨íd¦/p©L¦IE\x0003rú>¦©{IÉÒyxú%.©4ûôú¯ôøq\x0000ÿc¡ü]Sh\x0007GÆ4e½9M0vÎê¶\x0016C¢êªÊáí·nòoÈvÇ¾\x000fïoFô¡3½íí¿ööÛaó
ÌBÏãFc\x0010
ô`&ÿqDÃ£ÆÆ#Ë\x001d|£\x001bë5´\x001eÚH\x0011NS­à /72\x001f\x0003x\x001b½9\x001f_G\x0007Û\x000eÍÏí\x0010~\x0006\x001fu¡+ \x0019~\x000bOä³~f-lÖa"]ß¯ çhoÿç½JÜÆ¨\x000e\x001dÕå\x00127pÇF\x0010\x0002DR{Ê\x001e;ÂÑù>ÎÿÃ¼\x0004ÅÚ<ãvÏa2\x0005 )l¹½Íú:ÖÂ¤ÞÏ3ã0W\x00154\x0001l{\x0001gZû e¾ Ë³Íæ\x0010d\x0001%Y6WÓù©sÇãn·TØÍþ8ù\x00179\x0008ü\x0008Q\x0014DÖû3~åÇß^Ì8ÄûqìÐYÖTèÌ\x0002ÇP~èq'2ºÉo\x0010¥]·í§N«à\x001a\x00007ÊU®2æ}ø1¼1\x001a¤Ý
$- Q\x0000jÔÉ'Ú:çe+zJ\x0015e\x0005|ÃE/\x0018"Ï«ü\x001eÜ	 \x0002\x001ft%e
ç4ÍîÒ6e CÙ§ÑUÊÊìn\x0007ta¾î=¼F\x0019²(N\x0003ôjCënª2«¿\x0012(MÖ¿7Ñýo+Ó93NSG@¬©dø3ÁÔ6ÇE¶JØmÀ_©[se¢|¾À\x0005jö¦¨\x0010ÜX ÇÒ¨¸,µ\x000cp\x001eùxc%R±ýéØ>0\x000c£\x0002ÙÓz+\x0015DÔ8 ><déýÝÝ}|ÿ{Ô¶y1\x0010O,OIÊ,\x0010À^Ì\x0008&ï,^°xár\x0003ì«Á\x0005ìL¤Íç\x0018Ðòå ÷\x0015Å\x0019\x0012\x000b\x000c\x001e5M~Ã/Ñêü§\x0003Lj!ö\x0016Êe\x000c²øJi²\x000cüT\x000cØQ¾UÛÞ\x001boîÍÁt*SíS¤¦ .±&\x0005Éyª¸C}Éã\\x001acMïû×Q\x0005ÑDõ""§\x0004Pû\x0019áì-q5ÙØÇ¹Rä¡ñç8\x0003.Ç(]Ý½H1)Fk\x000eÎ\x0005!Ax"}\x0011\x0015\x001b®Øª\x001b%%î\x000c0\x001fR£á!ÇðÔ\x0008#høQÊUÝ«\x001e¹Óæ67\§:ôCnñ^©ÚT=Wùã¹!mNV*0\x000e«íß:`óÇ½sm'A\½°ëzW«,S		Ð\x0004¥Dî\x0015-"F"\x0006\x0018PQ¯lx4¯³W³\x001e\Ç##Î;¯Ò#íx\x000c\x0013aÛ\x0003v_q_\x000f16dÓ>²fÛw0¨Òñ[Ð¨ZÅ\x0012<Nñ\x0018ÎK¥Z)6\x0003îÉÁìÅ)ëÓ¤4Ì5I÷\x0015^aÕz0þ|NÖ^\x0008æ\x0014Zô
ÎNÛ`èO\x0002ÃQñQ
Up\x001eÅñi\x000f8$ëêüü\x001eCW«\x0018ñ
\x0018ÃUT(\x001dµ±:ÊÁðd\x0003\x0016×\x001bøIÜ\x000c\x0008\x0005>pðrZê\x0014·t\x000es÷"ÑHE#"\x0013Õ\x000bÆ[½ºc¶Îe.d{ÈÊÝD¡u]\x0014ÑµDâ-K71N­\x0013{/aÈ\x001fI8»Hº¾^G\x000fëªzXw2Â\x0015Í\x0015ôMf]\x001aåXª^;D\x0004µ§'ç¨-Y×Qs.AT$)çUÕzÍXAçQA&+BQãæ¤´`7Ý.Â6V«­úgûIÿËìîüçh\x0007ûñ|Úaøkl\x0011\x001bñkJ±1GË¢\x0004\x000bf¥Ð\x0018ì¢\x0001\x0011qúWý\x0006\x0015û\x0000$¬"×0¨{\x00083Ä`\x0007¬æ<\x001c<Þ}XÏZÍ\x0007{3Újo
ùÑ¨ï¥ü ¹ß|64,ý±Q}ù²ß\x0007,mñÜ·¼ãm#/áAè7,\x000f\x0005>¯>È\x000cáè\x0017{\x0013 
Û¡>_çß\x0007d:ÌeÍ´ÚeQ\x001ah§¢UÁëw
nÃa\x001e$4J*rÊhåõ!F¦Å\x0019yn·ñÊ C³T¥jk\x001d¡>E\x0008±\x001d\x0003\x0014þñíù\x001f;ñý¼ÍVsúóÁpÈÙm§^=^½qØß²<2¨lq¥5àqÈº«Ù®)wáKø¦é©ÎIº£PÄÒ,avÔCV»1]d!\x0004\x0002GéÑR\x0000\x00006f\x0006^	©\x0000M1ÖåðmËÉ÷\0ö	.ÅZ¶®i@ \x000e¤1~\x0014vÇ\x0018\x000bÃS¯áä?ýþ¿¼ñ×\x0001ü?\x000bÕoéÎn3\x001a2¦ª\»Uç]0\x0018ÐÇF6¥\x0001\x0000ðumz¡¾û©?m8l·îzÒÍÖyµ\x0005.þç·­þ¾[}÷VÜP\x00119\x001aÒ\x0008t§'ûyo%oF\x0014Ñ&¨¨iz­Ã&@óòÔCµ3BÀ¸\x000eÚË\x0013|ör8\x001d¿\x001c\x001f\x000f^ºþ×v1UÐåVöÐTú6=ÁOâ\x001b3fÝN¤Ëó%é\x0019(ùõ`\x0016\x0005	ú:\x001eÝ%|@3Îü*u\D\x000b43f
R\x0007!.t<.Ïá\x0012$¾	cs5]>>Nò&Ûóãq¸É8>=Íà§®)\x0010Nr\x0018>Îøq\x001fÿ}{\x001d2ã<iÚï{tæ\x0015EQ]£C\x000b IºnÚ»ªJÃ8á8nÓ\x0014Àog¿\x001d¬º6Á5\x0000~ÍØ\x000cÍfó>ü\x0010vo¦¤ßQ}\x0000\x0012\x0005 F¶¢]\x001fèKÊR*\x0007ðÛÔ*pÇ\x0001?"i\x0016ESÞgU\x000e\x0010ÑEU\x001aá,ó±,Ëï2Á
éü\x0015¸ÊYQ³»\x0008/ÐÅæ\x000f7të×(£\x0012QWue{§Á\x0006Z·hjÊ¬ãW\x0002¥it/âO¿­6v\x0000_=Z\x0002b¢!?Ò«\x0015\x0005.òUZÜ\x0006üº5W&Êt\x000bÌX Fho
Á\x0005r,ËRËJñç"m\x0014S\x0013ì/5î9\x0011ÓmQ\x0011\x0007¥õ6]TÛâl½Î\x0019ñ¦äÓ=È	Æ/\x001a\x0016?Ð<\x0005\x0002Ä>¡ÐtñÅ3\x0017/\®Qp}Ávã\x0003Å\x0012\x0005EnzýrÐg,$VÆÂ\x0013¤7ü\x0012­®ÿ\x001a@`ÓV©½¡
°$y¥4i­Í\x0003\x001b±fô±òfçB¼\x0005N¾`r0íS¤2Óá¯É±'\x0017urT\x0017I¡óÖþuTEìµ\x000b.ßATILKíö¢q\x001d=ù¹æ~'"\x001fÆ0
Ð\x000exun¼^Ôó$\Ú{¬Ï\x0018Æ?;ë¬¥s\x0019Ç\x0011MpYø0 \x0011ñÄ\x001bdF£á­l¿ß«ÑÄöc\x0018ð±¢
RÆJLaZßù\x000eºð\x0005Ò&ëCrL7¦k75jiùõÊIù×îà¿\x000b`úîú\x0004Áæ¿AÚNðaT.jmç]îæ´\x001c\x00129EÄÉ¬*Áid^'­ÖI=ÒËheâÔõ8\x001av\x0019IÑgªÃ¶÷Ø}ã\x000e§vwÞ'lêcow¾A»ÞÚq­i»\x0004§Òt\x0012~ÐÉ°\x001e\x000ftï``Xðô¯_`\x0015\x0001·'ã½qð
\x0018¹7\x0007»uÏÏ'ï?\x0013Ì©zå¸1üß¼WËÛ¸\x0011å"'m»%B$E/¼øHzuKnÛã3sE>#Ëùÿunb·¤ñ´YLU¤\x00084\x0008 ªnÝR\x0002¦\x001døY\x001d&ã\x0008­+ìz\x0011§2Z\x001c®9ôÂ\x0001VÁ\x0001©R¢¥\x00062\x0015<NxRäð\x00137n\x0010IqL%N\x0001_¥Á³á
¤àvÜ\x0014©M\x000cã/Gç¼¸c2KêÚ«-JC\x0011£%R®KÏ\x001c0¹XÔk?¥¦²°¾\x0016;åïìP¿"³Y],'ÓûÉry?QÜuqÅ÷¼®Ôè«c³\x0018\x0001é{!¨\x001dÆP\x001b«¿túÔêÍKf)Py¹Løâ 0ë\x0012Bt\x0000Ñ#¢\x0016\\x000fóÝã¼¶ê×ö3û\x001eïïÿveSÞOÒ¶ßc\x0016ãR~KõRl\x000cÑ2jWJ¡Ñ£\x0002\x000c EFãÇÀ)­da_P°\C#ï\x0015\x0002õT.ÕµQ\x0003VßO\x0006=\x001fìÙhßj¼5êµ,nd4÷µÉ\x0007CÃÒ·@õãÇ¾'/%\x000f\x0018Ûè¹¼ã²\x000c\x0019îvyÈ÷ÁòFr¹.Ý±7*\x001b1¦NÃý\x001e)\x000es\3­vé{îÌõzêit¥¨mRÙ\x0012
PÁ@b3jë\x0002éÜìPJ³®Ô:\x0013¾'=¹*
±>I,-æÒ\x0005)üõóÓÇuöå°_8\x0003ü\x0011Ù¦«L\ô\x001aù¨K1ºÍè*òdzBP _)\x0019\x0017\x0016uÁtJì(Zfbt!å\x0000ºð
àù®\x0000¤CoÛ*\x0018\x0004\x0017ìzv A&Ë\x00072idÆ\x0005¨)æzÜ~nÒ¦3E
\x0006ñ\x000ei+HüID\x0013zôÿ6M]\x0017øÃôô+\x001e©@\x001a¼zýKF|?ÿ´Pþææ`ªÖVNrY'+yX#Û
­¨x¼ÈA\x0000L\x0014iô~1]±_él³ZÕ§½WµjÔ¿>7êKï|\x0001\x00079³"r4I(Ðk¹.6%Ç\x0004Q\x0017¼Ë»|Ú\x0017\x0005\\x001c£àme)ÂaMÁCBÿ?øLI\x000b¾ïJù¸Ý¡þzØ=n\x000c¯\x001fÛ!\x0012½´:Þie/\x0015w	Oä³çÊÈ\x001d´Yý#è;\x000e~m\x0019Ì¨`2V_æ#\x0008´üúÓ¡º\x0012I3W¥(:+\x0015ªv;q¦y°âep\ÐE+Móø¸ß\x0019¶9<îºg9\x001e\x000f\x0010)£H2RluÝí\x0017o¿òûÿ>\x000fØ\x0000±£»n³)ñcXÑt\x001aEø1ÔWÀrÝmêåÒ³³lm·B_Y®ËÏÛRbþ`°ºÛ¸,¯Ão>÷.\x0006"iÖf\x000e&z³ÀìXË¶\x000e\x0006É\x001aä7b\x0019\x0002'j\x0015\x0015\x0000Í0\x0017oýe\x0000\x0012,Âåb¡`Îçs\x0014KþüÎËü0\x0008Ãù½?§'\x001e\x0005wSß·\x000fÕ/u£'/QF)`¸,@NjÝKgqDÈÚ}"RêMßdî»¿9UÙ¢^ÝDÄ²XÙ\x0006¼YÀÍÏ\x0013þHÞ\x001a2\x0013áùH3FªaÛER!º1R±Qr\x0019s\x0019è<ð2@\x0010K_¬a:6°/^gK\x0000º]o¬]@m\x0003
ýÉdî¿½»{ËÞ½\x0001)E\x0011\x001a¢°¸ã;eàÛc¡\x0001±Poô¥Ñ3/Ë\x000eº#áû¢Úu\x0007îL]Yhã-.ÔóA\x001fb3\x0000Gá)ã,]ùë~k\x001cÆ¼D¡BÅ|ÆÄ³xRJ\x001f+ªFtk0º7mÙ\x001a¢Ú\x000fe¡}æ+á\x000b
õµf3ÁPMi\x001dâ\x0017ï\x0004OC\x0016ªª2¥iÍË¬Aô³\x0005^\x0005B¯V'\x000c§a¤LÍZ0¨;­=ÊD	qªªöô Ni5¦¼x\x0012\x0003ÿÎXz¬Êª,iZ\x0014\x0007X,ó=(ýù\x0011@0£\x000bjOáM\x000fóµôÚ@±îJT6HHÂt¨\x0013\x0014ºÕ&4a)¯ìoÂ\x0018Õ6Z'UT	\x001d~:¥¤éÑ(£Îÿ/iôé\x0008ÁæßØ7
/T6­¨§É.ÑA Ê.n·VÒ"ØYÄ\x000cg¤Ù°NZ)­ÓèA\x001fº³JáþCGß¾PØvÝÇÕfôUdSÃLÙ\x000cª²éX¡\x0013Í¤\x0016±æð\x0003Í#ø\x0017\x0018Lw ¡;UãÅ§\x000f[\x001bL ër\x001b£kx\x0005¬ò¾4õû÷Û£©p¶z\x000bâìòÆ\x001a:æ[ð¡¾7\x001b-6Jè\x0005¹Âìq¯S'Ñé§æ*¥DÎ\x000cáª\x000b[]èeik¨¹R 2YU\x0002¤Yºf\x0019:D\x0005¡XÁ`/Ê=¼ÊCÛc2Uz ¾\x001f§qÇÌ\x0003û\x000b\x001aÒ\x0010§9F+
ÆèYF/Í6àÔ
±h®ÅNÙ\o>rj^\x0011ÏkêxêNïi!\x0019Ã\x0015ß\x000b\x0016t¥F_\x001d[p¦°û½ÖÔ>|h[j#* 8\x000c¨5Í\x000cQ1ó9\x000f(\x0002%\x000b\x0016\x000b\x001c\x0014fû@\x0007ð\x001d®\x0012*)9-¸\x0019.ç\x0007»
ÇymÕ¯íÇûàîôÛ\x0006^r{>YßY8\x000e£\x0008ý7j\x0001@_ê¦\x001eB£7£¢\x001aVÆgµe±¯)Ø&×(E-km\x0010\x0005Ã±\x000eáQ¾ÅêÉtÐh8Ø³Ñ¾Õ.
ykÔk¹­RFs_|04,}Û(Î~þy¿'/%\x000f\x0018Ûè¹¼ã²\x000cÜîvy0\x000c£\x001bÁNqntÇÞ¨lX1õùÓp %Sþ\x0019×L«ySfË\x0005O®TÃ<d\x0005\x0000\x001f\x001etë6?0f\x0004\x0013'àÜnÕê\x00128\x0017øÚ×iõ!å!KÍRåýûþ±\x0013_O;ø3À_k
×b\x0018Co«J£G·\x0019]P>K\x0008Â\x0008@ë´²¨ë\x000c.TpAØhÓ´>1v@>9\x001f0
*IÞoVá 
\x0019Ñ÷9RO.ELVÑ2\x0005fJÇ"Â\O\x000fÿ\ó~ÛV\Ìç÷Hçó,&4¡?#å*ÿVæoæó¹~¥|ðÕë_2âû\x0001ü§ò·lOíjS1uÔðNvµ®á\x000b^É4ª´µIR¢÷k»­])\x000eÝºùxÌÓuÓêu±.þóË:ÿºw¾Y¨a^kq]«\x001cÞä[óùzCèdSÕrSm*¶5µªs\x001aVË~e)ÂiGakò4ÏÆÌ[Öò¸1úéðúëýãÓ¡UMýc;D¢\x001fÀG¼ÀÐEeã_Â\x0013ù¬\x0019X\x000b\x001b´ßý#è;\x000e~m\x0019Ì¨`2V/¾ÃKNü`(\x000f	ô ~ÇÅ39«þÇ{µu7n\x001ba½äÔ±×2"\x0017"	\x0002¤@@EQek½\x0017Çi7gÏÉCÿK~Cw¿!\x0005ßn7}è@\x0001 \x0008\x000c¹|Sm\x0006\x0007¢\¨ïÝ»¦9\x000cä@É|>¢Õñ­µ··û½C°ÍÍ]ïòëëãñ\x0006\x0004(\x0015\x0011\x0015E¯×oW|»Ê\x001f¿>
\x0007
\x0006247®Sh8â\x0018Q(Ê±6[½XÌy:»»^\x0003n*Õªwªx\x000cª\x0001pSÚÄ&J½6?ÝK\x00034m\x0014\x0000H4É"\x001br\x0011;Ú:ç¼Ð\x0000¿I\x0000ß\x0014\x0016ñj±X\x0004A\x0012{\x000b\x001f \x0002¿E\x0018	3GªDÁÍ\x0003?\x0008üwójó M1*õ¯ºÏVF!\x0002IY¤VZH]6$wÄäY¯?\x0013(MÌ®.~ÔÊÖ]ß+\x0002bY"á^U\x001e âOfÁiÂï[cd"î`\x001aCy\x0011T\x0008n8Èá
\x0005\x0017\x0017Ëb\x0006é#CHy±Áýç\x0002}:»¢îl\x0001>ÈÈ+$\x0011HüÀ»¼ôççggç?]ü\x0008P\x001aó _½\x000bÂ9ÑÂ\x001f\x0012@8Î`>'\x0014:sºã´Ài¡«#à\x0000û\x0000#v¦$\x000fÈ
D²\x0012O\x0007}Á±É ÜditÂ/WãïÍ±Ùóâh\x0004ó\x0018ãO4\x000b!ä¦lDZÃ¸[\x0003Üa\x0008j\x001fÔJzÌ\x0013Üã\x0012ìIOY/A!Z¹åY\x001a²Phm±æyVÎ@òxH+q¹^\x001f=\x001f­¦!Eª[Î|ßb¾@äü¨µ=\x001eø1M±P­Î¹E1[z¯V¦Er\x0000a7s8D2ÅeÊ\eJ
\x001e\x0004:n©Û!·æÓ\x00069\x00062\x0019È¥FZiB\x0013¢Ç\x001bÛ\x0003Ð²×¥\ÖqÍeøù\x0012§wFH!¡¿	`\x001ay¼\x0003aóï?ì&_,m®¹.wKéûÒ×pj`+I\x0008v"Îpr¤$§#\x001fì*c\x001f{+½%F\x001bWm·Ø}¢·û¤½Ù2MwjQ[SÑÊÚlØª\J&dÈñBæ±6\x0001µ O´j'5Nú¸C	
­ºÒ\x0018©¡\x0015¸dYvÊèÛ»îÎè{ÃË2ª¸IË2­ÖÃEÇYÇKÑ¶¦+y'¸\x0006U¸Ý\x0003ËøøÐ¼
)ñ\x0004¾j.,*K-SY± äB\x0000ÊdZ&¥\x001beiÊéT¡«4Ø[\x001eÆVA)Ä0\x0015K!Gã'ïÜôÅ\x0013å^Þ4ófðÒ Is¢\x0012eµbêÀJÙbÑìüJÅ£æ5
S6¯7\x0000âÇæ\x001bäyN¦WÓ8¾V\x0005cSZo\x001eÑ
­êÊà#@=,ÊÇÖRqÙ_ä>¦ye9óòÜ÷ãx:%àç4kØWqZ'H(Á$p3>Na\x001bÉ·¤þÖ~¼ÿðfþ·ãï[Ý·çµí·q\x0005\x0011#\x000bý3Voxp\x0000ò%oµc2Ö8^eÄÓxóÄZD½&c7ÜâZhi`+c\x001dÍoÐ$\x001a{9\x001d9\x001e\x000eÖ]Ú\x0017ùöR_Óâ
¹ë~}åãEã¦ß\x0012ôø¸ß\x0006¸â4÷e!íxYHKÆ\x0008CÿxQ\x0010\x0004ñ\x001b
áÜè±\x0013Èq6õðiüLéd&i\x0013Î¼)Q³c
è\x0018¹MÐB·\x0000ÇT¥´Õ
§cü\x0008?·[[©àç|\x000f.yc,ºyÎy*$KÅì·/éù×c\x000f½îÏ\x000e\x0017g1á­÷ðPNmª§eÉ"1ºªdª\x0007¯;\x0019Uhqò]xp¦u#¨¼±ç3\\x000cvYÊv»>eº\x0002\x0011ÑórRpH¦HLÎmY\x0008ð\x0018sÝ\x001fþ±ÉÛÎÖ9\x0010Ä\x0005ÂyùÓ%M\x0008Ä\x00017&¼·ä\x0011°"¢Vê @\x001e|óù\x0019ñß
ø&ßÂ\x001eíz«è2eÜä\x001byjèB%×"]¨3»\*¯¶Ów×ß\oweºi¬Ü¬6«~ÙT_ûÉW`\x0013*2¥)\x0015&)aèM¹Ó\x000f{#0ýr[kÑ©N±Î`\x0014Cv=@cO¡3È6rútCó1'Ñâ®3òþæv»Êß\x001fîo¬hô÷í\x0010~t>üÙ
=;4é½tO¤³fD-lämOìÞ;§§À^\x000f\x0008æy®_¬«ð\x0001½]e\x0003ÂI±bÆYy"­»\x00035Í-ÈÁ¶¶}?\x0003%A0FS÷öþþöVhsüpÛh»ýøñ\x0008*Ëå\x0008æ\x0004HðvÅ·«üñëÓpÐóºn¿7h8\x0004
\x0012 \x0004\x0016X­º}aö°Ý\x0000n\x001aÓ/\x0007#?¥j\x0000Ü¨mÚ¦Æ¼6¿0ô^\\x001a¤íK$"e)×¥\x0004Ö)\x000fØ:\x0005® ·é2-#.Ë¦\x0002bã(J\x0017ç~\x0012\x0002Dd(Y,ª \x0008E\x0018\x0006\x0000ûáÙ¼ð£ ÂK?B-ô£epvåûCeý[³YM­B\x0004²ØÔMU5ª%¹yº$Ïºý;Rïê³w?LÖ¦]ï\x000f\x00078T¸®´\x001a>\x0006X3EJ0ñÂÓß\x0013·ÆÈDÎÁ\x000c\x00075ò"¨\x0010ÜpÃ\x0015
..Iéá\x0019"CH¥/w¸Q¢Ï\x000eCÈ\x00138ôAÞtÅ(À\x0001Eóé4ô/ÎÎ.f\x0017ç?\x0015E£J\x0003vIëÀ\x001f\\x0005\x0006ú\x0001¡PÏéÓ\x0002§®\x0003ì\x000bøÈFìL8²È
ÊTWO\x0007}LÉÎàXÈd\x0010nx¾8\x00195<þ«#4É«ê}\x000bÍ\x0007¿\=Q\x0018"?Õ\x000f\x0016fußzU«ïÚÞö­­[û`\x001b\x001dxªJ\x0003(ð¬òîIc´ª}\x0005%òbemkÛ¾}µ"M|N"ªVªôvû\x0018\x0004Õã8R\x0015í¡-¢\x001dæ\x000b\x0015:\x0010Ð\x001e­í\x001f?U\x0014VªB4\x0017Ð=|\x000eËølhZD1Ê\x000f\Á\x0000ÏVZx­nEn\x001eØ~ÕSw\x000bÜ¶B\x0015\x001bÄöt¬y«[Ýë6nc[ÕA=´\x0001DÝïµæ×ÙuU'¿>
bñs«jU×\x001b³ù+´­\x001f\x0006ÕuýË\x000f]W6µ\x0010Ý¾Ú0þ¾¨£¨FáìÀ½&&!\x0015W3öF9IR³Õ#?ì\x001bÍ=Þ÷:xØ\x0013£\x001dT5ù<ì>·wÿæ½\x001bE°RqÝíY\x000cB\x0012\x0002i\x0019`@H @²$Köú¼½½«½\%ÊC~K~ÂýÞ|
Â+ëö¼<¤»z\x0018`\x0019¦»¿î¾\x0019-ÖY; Fí(È#\x0014êúA"\x001fñ¶ÃÁ'm:ô!§\x00105ÍðÌÉ%Ôå\x001f\x001f\@©\x001d\x0005K\x0011E<UàÞ\x0015y0
÷ûb\x0017E÷8[Þ÷Xhâì¼Øå.&µ
Æ\x001dD³Üa¼O¦Ðº½AÅãÃýaö"¤\x000c\x001bp\x0008\x0018 ÁøU«±i¢íñë=\x0006°µ¸\x001aã\x0005`«Îñî@tñHô¸ëã®\x001cÓ)-\x001eþl¼i<ÃEMðß8¾Ñ+!»\x0011\x001f \x001c°Ð¢>¢ôx0-Õ	ÇúñK*§<^NíãWHQâÐh^]¢ô»lzN«uÙ¤õ®ûÔÐªµPJ6\x0000­à\x0011$\x000f\x000fó9I\x001da&ÆD%Í:ðN\x0017U«:\x001c6ªÚï£Â¬\x0006ª+Ñ:\x0013×\x0010Óãª9vÊßh4^Ûõkÿ£üÎë?îÿGÙôü|¬,ûrnÑ\x000eØ×q	\x0000üó¨frlZ³o\x0011Ó\x0017s\x001e=si\x0016ý=r	\x0002\x0016:!Â\x0007ý\x0016µU\x0012.½lV<,\x000f¶VÚçäTçJ}I3ªÕýRå¢¡és!@}zº¹!+%\x000b¨¥¶ÜS!ë8\x0015²*âÐµÜ^\x001f!xF0!ÖjÑµÕòX
úî¨¨ÃcuýNk4\\ë=Ón
õº¥al¶¼jôYe5Û¶9áY©\x0005\x0000\x001f:<\x0010|î­ÛíµÙ\x000e8·ç<\x0000Î©]Þåi4\x0007¨\x0003ÆÁ·Û¦£üòáÝWìã~\x00055*øjKðäã6ÞÎù}\x0010ñsS!§e	A1L\x0008nU¨Û¨LÈ·\x0018\x0005)4lnÒÆ\x0011;Ì­Òµ®ÚvW«2äey|¬+Ñ\x0003g'\x0008=Âasf[¶É0£í¸\x0006\x0010±ûÍ\x000fÉ¢Ë­io®®®´±Ú¤j«ÛÕ4±î9i\x0017È;ÊééÎªSIïÕöÿ2âË\x000eü?\x0013Åog¾Çy@ÊäÃxòÝ*ä!lÁs§5\x00088kÍQâíÇy\x0011Þ&\x0001[§iüýN)Lfá-¼|Xx\x001fWÈ,jÞRã<tÉ­XFuä`\x00023¡\x0007yÐ^¡\x001bz\x001b¹¡Åe°_\x0005lÊ¡0Åø9ò2Ô[àÐÙå\x0011¿ßlsr·½_ÏYøu@_\x000fû\x0004C\x0000wOál6ª²vÅù¸~_^\x0000.íºÌ`jF&SòËu(? «oñ»Å³ (J\x001a4mAõ»Åâ®¤:)Ñ´*Öoß¾½½u´Ø¿ÝfGÊó=\x0008©Ô\x0008îädÙùç«üöëãpPç\x0011\x0015ÅÍMzO£\x0011nh\x0003´ï\x001773Ãèó¬\x0017Û<Eºú.ú°ø£E\\x0005YÓéK÷Óõî©Ò`+Î\x001cÇ2Û\x0016\x001bÆ\x0006,¾¡_Gºâð\x0019_kd"¿qyì!@³ß·\x0006ßªF\x000fIÄxÐ7\x0006\x0003\x000fîìôz¦ª½k[Óµ~¿w©é¶Úï©úH»¸ÒÔ²\x0013ÿ2[øÍO^F!Â\x0018\x001aÃ(yÞ,XI3kDÈ¿§¤´{õ
k¿ùCc\x001aeñz»(\x0011cW~\x000cxì>:½FW?Nø5q«LtuQ§\x001a¥\x0004\x0015J7ê£\x0016
.u,ã¼¶
Áâ\x001a/ GàÙ¬¬\x001czÌ`ð¦ßF\x00111Æ\x0001é**/íÛo7ß´m»ß×tKk_êX\x0007dhj	\x0015\x0018Ê\x000cYh·¶Ú
j+¬ûædÜ\x0017éc»Ê©"±ûä\x0005Â\x000c½çÞ[äg\x0000\x0016r\x0019\x001b6\x0019DÕvãðkFÙ$ÊÐmÚÒ´¯h"IU}ß	bc,T\x0011©Ü¤E\à.\x001fâXjæ\x000bMH°&%>Uö\x00124À\x001d_	Û\x001e(\x0003?IÒ8-ÒO³
*\x0013å3!\x001eõ\,\x000eÆ\x000f\x0005\x0013.<¬¹Ò×\x000bÌ§ú\p)Ä!IÃ8Ø¶¢pfÇoE1ý.2mSàrØ¬¢©Ú¤\x0012\x000bi+©íXú>l6\x001bQÐã\x0014,¹DÐ\x000f
\x000cTä@NRÊB¦t'Zu/miÃ¥e0@¦á\x0007Ø~LýÀ\x000f$Lþ\x001bZ\x0004w øüÓ_î³Ì\x0006¶-EÒìX ëK.$1mB9PpR©öI;¥}¦²âUl+8ì\x000b©=¬q¯\x0000¿½ÁßíÝdýv£$¤ÓTIãM\x001aA¡ãb¥Är"\x0015_ò±ä
\x000eR:¾®ñÌ_Ç» Á)\x000fïw2\`\x0002/waÊ\x0004V\x0001%Ëp\x001d/?=Ý>¦É\x0013ÎV\x001aH\x0019Î.Z\x00042Â²w\x0002Ól\x0016[É·¾\x0006'Sx¼¶-uø)\x0011R¬\x0006°Jõ=Ë!ÃÃ\x0018ÚäÏlÏIg°\x0013Å¾é Oa¤À\x0014¶JU3Tñ(\x001cÈÀ/ÇuÓJQUõñe=ý'stT\x0000w/C¯ÔFÑ\x00122v:Ô÷ãFùNç$0²TNùÛ"@\x001c²WHU³dÜj7[ÕlE^§ÓlÑz=Z\x0012Zµ\x0016Ê(zíá\x0011$ïß\x0017\x0005I
|Ìu<¿V¥¼V9×uËjµtÝ0PGaÖ±eY ux0áÄ´á¬jò7\x001a×výÚÿ¨¿ó¦wqøu¬Óóó±7/ç\x0016
yèç8>ã\x0012\x0000ä)oÉ5ÖiÍ\x0000\x0003p"h|úÌ´gÜ%äìi@¦\x0011ÄOd
\x001fvp¬0JÓhl³U±U\x001el­´ÏÉ©"ÏúFgT«û¥Ê+ECÓçBúóÏwwd¥d\x0001µÔ{*d\x001d§BVRE\x001cºÛC\x001fXg\x0004\x0013\x0012\x000e];HÜGEýôCum"2\x0007\x0014y{¦Ýõ^G-ËÎ|×i\x0018|òp\x0016Ò\x0002\x000f \x000ee\x0011½Utx\x0007ÛgK \x0008t
¼J\x000b: É\x0011yRa¾ú¯¿ÿø×½øça\x000f»hTðW+0LÁÛB>\x0001¡j³©MP%\x0004\x0005VÈ$\x000c¥¨Û¨L(¶\x0005\x0005)4bâÇCÈñE )Ú)®\x0004û}\x0019ò6ìXéúæ"ô¾(gÏh\x00023z~$\x001bs==üíÆ]ß\x0016sWü÷*knÛHÂ|Ú­Z«$G'\x0012\x0000D\x0012\x0000\x0001\x0012\x0003\x0010\x0000\x0007$!\x0012"Eê4\x001dÅ9\ëT­Z?ì¾ìoÊïÜî\x0001!QrÖöæ!Ý\x001a\x0008À\x000cç@wý5¥{Î©YßoãÀ\x0000ÆzÇÏ¥þÖ©\x001e\x001aXO^ÿ\x0011\x000fà?,¿{é*\x001d9\x001a5\x0007\x001dÁÓï{NÜ5N9\x0010´Ýö¡÷}\x0017Â·\x000b%wKWÏe^æýóÌ{?«½\x0007\x000eÒ+ç\x0016I\\x0019{\x0016½)¢.L O°7á\x0013~t\x0016NèENä½Q,)Âjá,ru×¬2oh¹\x0006jØ»Dìê|1îw.\x0017WEÚKÂ/;!$ú\x0012|ìG\x0018z\x00044v¼
Oè³QÉZJ\x001dOQ«þ
ô|Pé×Á<ÎUêÖ:oI~ý\x0006+õX\x0018ö\x00039\x000bÃ\J[J,@ª¾,»R\x0012J»RÊÞÑèúúâ¢·lu³\x0018md2¹½]0Önc\x0010A8õF£ç+>_åã_o<\x000f%Ï"jO­\x0016<à\x0006p\x0011ßÏg	¼ó\x0014£ùD\x001c\x001f\x0003oF?Î#vg `\x0001\x0017¶ý±>6âøiø)ÊñÑH\x0002/µ»]C?2ìf\x000cÐ\x0000Ïñè½^³\x0007&°ÑÖ
8xí\x0000@SUÓÝz«aj§æ©
EGi£×h@±tÒxqbSªjã%UíºÚ¨«múâÖåÍàç$ëï?F\x0019¦V³ÕÄó\x0012?C¶6"ëä;$¥Ç\x0007;öÑÞ_jq4Å"B"f\x001bü1ÀkÔUá¦QûZÙLø%y«ÌLt\x0015Í¨¨l[I\x0005éFE9ªÉ¥Êe\x001dÃµ\x0001\x0015Á(ËÁþ=\x0017Þ¥²rhØ-ÛF¼µu½\x0004E	\x001fH=ÙßoÐÝ\x0017/vÉÞ\x000e\x0014'FU\x001e½T´:JÊ\x0002\x0010S­Sd¡ÇïT^Pyau\x000f	\x0007¸¯\x000fuHÉ±"éª\x0018\x0005®\x001ez\x000f\x001fze`\x0001°`È@º±­Ó
9ª­\x001bA\x0001{b2v!\x000e)Õ<B	y,i(úß%Bç0Áç"s\x0011\x0007"¾\x0007\x0012êÁñ9(å\x001c~J\x001cD'÷9¶F4/ID,rñ8+Ãê?\x0008;ÅJñ,[Ó:[çC\x001câYÃ\x0019#ª2ù`	\x0006PÀÖI¯¯ÙÚ¶a!Ë\x0019ìÂþàçØß$q\x0012Ç8-\x001clÐ\x0013H3øG9\x0019·à\x0003'æ\x001ex+-åøZÂ¾\x00130< k¼#¸à9\x0017Ðb\x0016Ð@>sÛ\x0010wÜ7\x0013]0ÿôïk\x001bÕ¾\x0013ïùþ0\x0018þ?ùë× ¾ïó-@B/êÛö(gÃÃÎå7\x001a~#¥æ\x001c\x00157A6Â\x0008|MNÊ}âNqzs6pHÂÖËÓ3Tx¦Ìc\x0017pz3¯ÌÙÕ9IÐ¦x.B0¨\x001f\x000câÙ\x000c¸ÉÇ];¹ÜÕ9ïzÞd\x0001ï¼E|á\x000fá+³\x001fÞ^ð@À\x0004î0^\x0006Bð\x0014¼\x0002\x001c\x00048K_¿YÜá=|[Þ
°àÛÏ}Î:Î9ãÞ¬ÈæÍ=Æ[Ò\x0015nWÜvxG_¿<I)z
°
\x001cÐ`üU\x0007¯º\x0005W;ý¾\x0005ì?\x001b@ÙIìÙ«.t0¤oà«8¸Þ\x000eêð*Ðx¿/Ç½ò¬¾_Bb¾¬¦w\x001f¤w\x0002ÀMGp'!µVa4\x0016Eà½ÇºÝv{|¡8Ø"Ö\x001c=\x00159åæß°õè\x0013rr2JÍÃ£ý\x0003]ß?<Bà
ëÑ&^±áªU\x0003ÛQÌ^«\x0015çØÞ¾L°u7âm<>®s~\w\x001cEÑõ\x0003Ei6áCÁ¬PLê\x0000\x0001°Óï8¨¸áQyÙÜÈcÔjÚõ§Îsò?zèßÖ¿Íxþ}ºEñ\x0019b\x0001B0BOãg*\x0001oë|X)F!*\x001d8¨	ÃñâA¥[´VC\x000cvá#\x000cÅ@ÞS. \x0006#\x0002µ\x000c?\x0018E)Ý?(U/?ìÆh¿×¶
ùÜ¨O¥ýL*s?5yih°ôóúþýj^\x001ePµÊs·\x001bzÇvC/q¤à¹½&d;ý å"\x0004ÿÃÙ N¿Ú\x0018êÝ÷åÿ}ÈÌ\x0018pÕq·¦BI]ãWµ¦Óy¢®ÛqÀ<h\x0005\x0000¾sÁý8àyxE\x0000é\x0008{
8·\x001cå<¯PNùTL\x0000Ô9GBdyXýÿúãOKöa½\x0004¿¨ðKÃå0@oÎïcÁ+·©\\x0005Q\x001eE\x0004õºdAÀíD¢n­t¡Ã0IÁå¸rúÌçí\x0008U¿\ÊW6®\x0007\x0019R\x0007ROà±¹ö\x0000·	¤»}¤§0×ýõ/³Þl1Iz®ª¾t®vC\x0013'\x0004ö0ö[(;ª¢ÊéñÉv*Ñ>yýSF|>ÿ°`þö&ëÉè|ÆäÆ¨7å¯)Oý8\x000eýÌ³Û\x0003 \x0000y§\x0013Cï|ÞÅìêl:þî.°¦ãÏ¢Yô_gáUí\x0003p\x0010¯WZ\x001c&	,ná»KáÁ\x0004Ö<I½ù`> Kúi(|á§^I°^"cXÀ
zUæ\x001d²ÀAM½»¹à÷×·ç±óææþ*ïOÒ/;!$ú\x0012|Ø#\x000c=\x0002\x001a§Ûð>+JÖBJ/Q«þ
ôbPé×ÁT
LFêÖ:nì"?ÀÞ \x0007JÏ\x001cö@ÎÊJi±0¥Ç· UßlöFJEJTµÌ¦eoQÜßßÝy\x001b­¿½]ld>ûv
Â¹ib\x0010q`eÅó\x0015¯òñ¯7ÃAdÈÇÅâòRÀCµ'Ó¤Âz¸È`°¸\x001cÃ\x001b9ÏUq3R
Äo)þq-ø÷v\x001fÍ\x0001ä&>·
;Ëßé)Ý2ZÌûÀKçÙ\x0016\x0001B\x00014Àâ×xtÏëx|\x0002ä×îXÀo|>\x000e;©a\x0018­ÝÞS\x000c
HD·Ý2ÚíPUµ¾¦A±ÔÐv\x001a.RÍ¦¶¯6]¥©)Íºs¤*ò&û×x\x0016\x001f>F\x0019¦\x0008S7uÃp\x001cÏÐ¥Ý9\x0000ÿ¤\x001eí2òÕ_k(²«\x001bDÙ%å\x0007x\x0015n\x000bn´Z½¹ðKòV\x0010Ï+QQ
Ù¶
ÒrT
KËÎ\x0003^jP!Ø\ñ\x0017`/w\x0013Y9hÌÄ\x001a\x0014ökY\x0011"¢\x0007×l\x001c\x001ejêÞÎÎÞÉËÝ¯]·ÕR¶Jö-\x0005ÅÔd\x0001\x0008ÀÙTTd¡´òÊ\x000b*/¬î!á\x0000÷jL$wÆÄmÉ\x0018±ÒðáC¯m3\x0000\x0016\x000c\x0019H7Ìù/ïU·Ý¶qyÙúøØÑ¡C\x0008\x0012\x0008"iþ$\x0000\x0006 V\x0010\x0016\x0002	"D%Ktä(Lº''î/Ú«¾U\x001e¡Õ\x0019Ð_R7éEg´\x0010°X.fwf¿ù¦:ÌÞ¼*¬~Mî´\x0019;\x0015EE©Z"I÷%¢`}
W¾\x0010C,$&`&b\x001e\x000bn\x000b~Á9(b1\x0001ª\x0002 ´\x0000*>\x0019\x0013Ì/U©jù¾à"\x0016÷³2ª^áNØ\x001eUZ\x000c\x000e\x000fWÊ.[e#Í8f¥Jeóá'\x0018~­|?^]°®£>öáÏ%I_ùÜç¦Å#ÆJÊ\x000e¦\x0019úS@â\x000ctI\x0000ïs°,ìÍf,¦nvûÌg´@\x0003%Ð -@@\x000c¢*ªÙ>\x000eº\x001d\x001f9Ðö_ã¯ª\x001fV:©~%,°\x0000\x00027ø#\x0012Âê\x001a\x0005\x0017ÿÍ·gQÔ÷ì®\x001eÅ,(¶O; ª ú©q<Õ\x0018HÉ\x0008i#¬{\x0004¸¦0{Ú) Ó	ïK>[-bP.&¤ø¬0\x001b=ÃÕ·üdÙ>>I>ùTHÏÄ\x001cjs~4¸Ó\x0006ÉA\x0013\x000c
Àx
NÏ2£\x0004û¬Ú\x0001î2ûþö\x0014\x0010'\x0018\x0008~ê
\x0001\x0001F\x0005:ÙvNx\x0018\¿_àF ¨Õ\\x0016è£»©£;ý9sÌãYxâ°\x0013AB¡ôv	zßé¼^}\x0018=J)¯\x000bUe6Sª9n©×ÑÁ-i`ØÞ5{á>Ûú´<EgDß0ViðnÃÝÅ±®\x0006¶+\x001d\x000bhÆ\x001dµõ2~p'½^\x0014#¼£Ú2*D\x001b\x0001lW*Ñ½IØ\x0018ª\x0006µ!«E%ò×E\x0000[E_(h\x0015_m\x0015Í­âÐ,¶ô½r®Ôè«y#ÎÔ@Y.\x0001¨ÝÞÇÔrT0ZJm4w\x0001ä]ÃPÕf³XTÕZÍ0hÖV³Ù\x001c2úaw\x000cR28Ê.t\x0019Â¬þÒzvþÃòW¿$Áqøtº³Ùy\x0005D'ô·?Ñ\x0014\x0000à¡&A®t4Ã\\x0011\x000cP}FãÅ¦aQ[\x0006tØ\x0005\x0010\x000cq$ï\x0001x\x0006½\x0012nk)\x0015\x001c¥(4v«i3ÝØÜi¿Õ\x001e:ò©S\x001fKãäî~ìòÌÑèé§ÎÙÇË%E)E@ÞòÈ}Ø(:\x001e6\x0012#\x0015ú	¾Ú|"\x0018B¬T¢ÿ¥Ò\x0010ë¹éô«£>¬³ÿ[mÊ<\x001bÉÚZ.í\x0014IF§¥BÍè<ÒÁ c`j!/ ðá
p\x0017âá\x001bI\x0012Lb×ÇÃ\x00188âª\x0002\x00131FP\x0007 B¤ éÖÎ?>`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p><?=óóß~¦í;~øá\x000b·¼¾¼p\x001aG¾× \x0008DF"çÈñøFÎÝnCÛzÅòôüÊëë3ðûû;ßqw{3"\x0006}~~âoÿñ\x0017®¯n¹Ù]ÛÂ\x001cfæyÆ{¡ó^_]±Ýí\x0018¶\x001búíF\Ûç\x0016Bt\x001cÞ<=~çåù¦muu\x0012VYNüùßÿ\x001dÈüá i\x001cË2ó×¿þÌÇO\x001føÃ\x001fþÈnw+:Àñj\x001ddÝ[ÎB]Ùµhpãjèµ8\x0010Ø°Ë!¬v6¿ãÖÂYÏJmÃ%\x0010À¼Ñô\x000b¾ëQ\x001b¤CC*
]¿e·ÝÒ´²]E\x000c\x000b\x0019[²xò\x0015íZ\x0014"¤Ç­\x0018x\x0015çi»ín/û\x0011\x0015E\x0002\x0008ÍO\x001f>²Ûî5@d%jU³ZéæªÖ®ÔæL!}q·Q4 (á`2(Ü¥\x0015oÕ¤¥\õYçdëYæ<\x0013©\x0018\x0014pJÎAl¥uGÖø\x000bw3ÜZçÒe]\x0011èQ)ègBKµ;+ºBLÐ\x000e\x0003Ò%\x0001&ÕÛ «ã\x0010s¼>÷\x0014\x0003ó<ÓBc²Àª\x00192yµ3Z`R(Y¼y}#îHu\R^c</p><p>8\x001f\x0019\x0007¶1ÚUÔbJÄÉ2S\x0002sÙ\x0002VuwH\}SéÈ\x0019Æ1ñl¶[®o\x001búM«\x0005Ua×çgÞ^^9½½±Ì5 ¶^fÜy.XªJÞÃ</p><p>a+/@È\x001eù|&\x000cZWý³vÞEF6ÖÊ\x000c=Ä¨få²U¤P\x0004]Ê	k")GI¨YÄñ¨\x0015WÖïm\x00149K%VÄC³ò`<dc	¹¬{9³æ\x0012s\°Eõ'¦à\x0014RPÉýp^¼=S®°²,\x0012®¢þy×\x0015a¹dñäÄ\x0002\x001erD\x001b
ÉÂb2Ó\x0014éÛD»dìq^fÁ'\x000bØdIÖb]\x0004(*g(\x0004r	R¤\x001a)¤Àÿ¶&½Hz4æw~ØêÃZÔOÛÀ\x000bXôÜyU#Þ\\x0005ìN\x001e4¼\x0004~\x0018¸»ýÀÐË¼H.Tdº1ce\x0017e¡\x001fzr)ã§§g6ýÝv±\x0018\x00131\x0004¦iÂZË4Í<>=Prf»ÝÑ4=o¯/\x0018cØï·l
¥dº®ÇÚLL3ó|"À0´@á·&È~¿åîN4wP`»Û¬\x001b¶O§#OÏOlëÝV½8º¯PÀ\x001b\x0019NW<Ý\x0019Çn³e«É¬ñÍpËõí9\x0004\x001eç¶|xàõùÆ{î?|`¿Ýa0tmÃ¿üé?ñ?üëÿHTF¬·\x000eï,\x001fî?\x0019nN\__Ñ\x000f\x0003>ÿÀ?ÿçÿ¬¦Æu¶Vï©>\x000fE\x000b[cViÄ\x0005Ú»Br\x0015r^ÚìêùáìÈBõõ¸LUP_Èy$,òÌ0ÌÂ\x0006,\x0016]¨ð´\x0014ÚV\x0003\x000bõA\x0016F(ºo/%IõÅ©ö±Å¸\x000e×ôtý¦í\x0010\x0015Ö\x001f0ÅÂ²\x0004æ É¦iÔñG3\x0002\x0018YbPXP;³º\x0005»È*ªÇ«ZM}Ê.Ç\x0008½YçÈÎáæ\x000cëÙó\x001e4ëÌ</p><p>±:dÃI¦Ûµ[¸,`¥ËD!
IÖ2.Ô\x0003P[\x001dZ\x0016-\x001atQùXTòFJýRel[¿tîVJâ8¾q<½Át\x0012\x0001;YÌ&\x001cx£[\x001a8ÃÜÎY¶\x0011Á{I,afZ&J)\x0002£YC"ëz\x0019
¶ÎÝ³\x00128ê57PM(©$bí/IYÙd\x000e§·Ó\x000cÆs{û\x0001ßn9\x001c'_Þx}}f:\x0008óLç=WW;>¸£õ\x001fH1òòòÄt:él*â³Ãe¤£]?\x000c1fÚº%¡\x0016JV¯©s\x0014s^\x000f&Ë`-Æ6êR",áyZtß^Ö"JºÅÆø5§XBÔBTgÂ\x001aÎ#sêÞ"aE+Ö\x0011\x0010+8@!§"2§fe3Ê\x001d\x0013©¬Iójáç½eÉÒÌË"\x0005ól7\x0003Ã0\x0010S\x0012\x0012^\x0007¿:ÍØ\x0015O\x0011¢&½S³D¨ó,³nw·j`-nhÁFL³`Ûb'¬[°.;LN¢éS1l\x0012_[ß%ÁI\x00198¹&:«±¬ÕaÅvÏ³3¤r­¸qÐWw;\x0015b\x0019=aOã[\x001c\x0002?¼<?ó·¿ýÌáõýõ\x0015í èB&\x0005©\x0014Î¢ q<\x001e)òúúÊn·ãj¿gØlXEtZÉãDßwl\x0014#Ãa\x0018Øívô}§´ÄfÓ³\x001d¾SâÛ×ß8\x001cF^RÀ{Ïn»a³ÙðýÛw¾}ûÊçÏ_0\x0016ú¡çÓçÏôm5¸\x0004é\x0014Ðå¸F¶\x001b§\x0018õ\x0001wl¶Wüá\x0002K¼½\x001d8\x001dO,ËÌ¼ÜÓ
\x0003¥\x0014æyfa³åöæÍ°aµ× \Øo\x001b
jF¬VH×à:ÏçÏW½ ¿\x001eÛ6P+÷ó3\x0001H²;¥÷Pc\x001c\x0017ó$¨É\x000co5\x0011JÇ£\x001dÂæ)×'õxuÈä4òRX³ ô÷Deoªq\x0016O\x0002óY\x0014YÈ¬\x001b\x0001¤Â¯×Hâ¬P½¯½k\x0018
íýîéøJ)bÜÝ8)V~ùõ7r»ë{ú¦]uó"6fs\x0008Ì1aüHe§¡N#¶°</p><p>Â«LÁ¸Ê\x0012>'1cí</p><p>ûÔÄrI±«è]G	FÑ:=XÐ\x0012,çû|\x001fx÷ßò¹çí% 3¬\x0015êRßúl¯yíâþI\x0016¥¾\x001fxKÑÝo\x001a`C\x000c¼<?óôð@9h\x0011ÍZë<¡Ã4B|ZG\x0012zMN§\x0013\x000f\x000f\x000f,AÄÉã\x001b)'eÄ¾1\x0005ãe»\x000bÓ¤]ª\x000eX¥D¢¶[1\x0006í</p><p>óC`\x001cG\x000e§¦\x001fØn®\x0018ÇQöV"Áv;p{ÃÍÕ\x0015W»\x001dsØXæ\x0013ãéÈ[)ä\x0018È1ÈyV÷\x0016Se!JTË%I"«\x0005c½«ÕíEf-8å¬\x0017^vóÆyÙô²\x0007Ñ"	kÏì^IXgX¼èkÊ³-\x0005§uVJô\x001fVÑbiXÏh»ÐþRóAE<Öù3ª\x000b\x0015¹\x0003Î3Í\x000bó\x001c0eÄ\x0019èºívËáx\x0010_f\x0010È²¾ÎdmÊDkIQ¼%\x0006²±ÄTX¡

Î'L\x000e\x001a+8é\x0005\x0002ãQV­¡UãjùYÖÞ</p><p>ÂzÑÊ</p><p>SJâÓäWñàË\x000eo½e-\x0004+DZ\x0003`Å­\x0015\x0017\x0016ï: B`'Jô}K\x000c\x0013/Ï#Wû\x001bú®\x0013Ø4elÝn5\x001031\x001a\x000e¦px{Á;9¬C×Ð62ã4óôøÄx8±Ý</p><p>Å>Æ¨U¡\x0014¿µ; \x00082-3¥ÀÍí
ÛííÕ\x0015¾iÙ\x000c[îîäçÌJÁ~ø.Ý¹ºb\x0018znàóç\x001fY³aØéµ20×ë·Ý_\x0011câúæ"\x0016èú\x001e×6|°Võ0^d\x0016zm×ÆÚ\8èÔØfÏQª\x0006Ò¬­¹`ÍXzµâª¢ö3ãK;?
iÕo¯èL)daDbe¾\x0012Káåå\x001c\x000b×××âbckB<«J_I]%QÊ\x0008L²@NuàÉ¥¡\x0014'L³,s\x0017d¤3F¾ÌÙ,\x0003ø\x0004Lã\x001c­kd.ådÿ]ë\x001d§ñ3·?2ôR\x0016r\x000c\x000cûÝ
\x0005Xq<B.¢'­f\x0003xïiú\x001eëëP½¹äl\x001b[ý Í9AsÚ¯Aþ¢}®\x0017d
^¦J</p><p>(T÷Êz4zKA»3qår®-EBmFág£­F\x001d
¨ý\x0017ëkæu6KZº=ÄÀi<\x0012PÓóÅ|ÏXu¡0\x000e<<<ðòô\x0008ãD«Dª¾idþÚ%¶\x001d]£¶\Ö0Î\x0013¿þö\x001bÆ\x001a>ùLÓ8^ß^Y\x0016ñ«};\x001cx~z\x00116m"¿1¬Û+(Vv¸éû5Æ`Ô¡&N\x0013/#OO\x001c§\x00139\x0015¶cp\x001eï-Mã¸½»e·Û²ßïØl7tM#zÑ\x0018É1\x0010æe8\x001e\x000eoEáKÁsaIÊxUBV+¥dÑ\x0017[W[8ÌÀB,ç>§ºU]ÎÆ<ÏóL×ze[â=Dõ)e-</p><p>çÄ¶&@.ÿ-Kg¼ÎõdÑk	pë×­\x001fìÅ¬{\x001f×$gÀd1Q°\x000eS*ÑÈ³é{Þ#ã(¬qk·øÆ3\x000c\x001bRHÄ9««ç\¢D.ufÖw\\x0010OSëÁÌ¼D\×vª9CÉF¥"ÒæjJmõ¢ø\x0018X¯:½ú\x0010®ÉO[àõ¢rõ\x001b¼¸8ú&ëÖg¡gË}¯ÂÛR\x000c¾i\x00196[Dð	iæp:òë¯ãéñÏ?Ò6
¥ÈÞºi\x001ciÔìu	ÇgN§#WW;¶»-úã\x001f9\x001c,óÂËÓ3Cßã½$ÓÖyn¯®Ùv\x001bJ*y¡ë¤ËÛï®±Ö3Àoß¾q:\x001e¹¹¾¡ï{Úaàõpà8?s\x00153a\x0011õîîO\x001f?á¼gg6Ý\x0016ë\x000cûÝc·­\x0005¬\x0012oª@\x0014\x0019NW\x00065FµQV\x0013°SËú?	Y	]RËEÒÐ®B
\x0019¬w®\x0018\x0015
Ë¯jð+
¡\x0006Y+\x0007ÃP¡þB¹gI¬!F^Iqf¿\x0017\x0012Îñ8ò×¿þ\x0007¿~ûÊ\x001fÿð#··w¤Tøå·_i}OÛötC£\x000fù\x0019¼:s"K\x001cé@J\x000b1Íu&c)E\x0006Ô)è6.Ü\x000bE\x001dS\x0013\3cQí¢&Ë\x0002]'³\x0019\x0013²\x0010\x0000\x0010¦íÈ%óüúÆ8¾\x0012ç\x0014"øã§þÈçÏ_¸¿¹[w¡å¸0òÊ¾iØnd\x0016m]uØÑ\x000e¨B\x0017éM`ãü÷O&Ãwä«{ÔyE^É¬ÏÝåvñÔj·\x000fåL¿0\x0011Î¥&M³&OT]\x0014\x0016®î1©jr&¦ ë{tÜ\x0019\x0011\x00188\x001dÚ\x0001\x001b¡Í\x0017èû^,ùÚVL\x0019Þ\x0002)\x0004qÝ±àJád¤`ô¾eèE\x0012r<xy}å~äöæ\x0016ï=Bã\x0011a7l	1R\x000cóDL\x000býàØv\x0003MÛbéHÙ±}ßs<\x001dxz~âp<ñúôÈËó#)E6Û
»Ý\x0015>}\x0011Ãùë+º¶§\x001bºµk¥¼*¹0\x0010càt<ñòüÂi<Ðø÷wxûÂëñKBÕwÆhÇ¦	¥J\x0006eEXÂö\x0012´s©z¸1Rí´ó¡Xb(\x001c#»í°Bè¥@TÝRûTþÃZ\x001c\x0017Xg¼ÿ=$¯â¦ óe\x001dA÷1½¾ê%¢'×	¤Ë\x0002¯Ë¢./kéÚÈ4M:v2lv\x001b¬54m\x000b9õk×²6XÄÌ²,ÌÁ2¤N·Â'L\x0000ã</p><p>ó\x001ciûD\x001bJ2\x0018Û`!\x0013%\x000eªV©2G6²B\x000cë.Þ»\x001f3T¢ÿQÌï>«\x0006µò»¯Ô®`Mw\x0010w-Ã ~Õ§nY\x0016Ñ
\x001bêú~ÃfsEÛxÇ#oÏoäÅ¾Ê5</p><p>óqbÒNòæêZ·î:Ùj2Ùd>Þ"E\x0011:ÎaáðöÌô:fO×tì6{¼k¸¹»m\x000fXîç3C×­~mÛ\x000bÄÁÛýçÂ\x0019½Ð+.¥î,¦¨(Ù(\x0010V(Æ0</p><p>\x0011ÊµÍ D </p><p>I\x0015¨ \x001bÅgcÞ¿Vµ)C!Å\x0015P"¤«T÷\x0012Ó<\x0011b\x0010ÖZ­êJæ4N\x001c^ßøöý+Cß³ÛnÉ¹ð\x001fù\x000bOO\x000füøå\x000b×··xïè;Ïù×æz¿g&iæ?þÈÍõ=m×É:r\x000eÇæâ\x0014­c#!\x001cy=<òz|$ç\x0017LkG\x0003-©4\x000cÃíæÍöÂ5FèÝ%s æD,T\x000e)ÌiaNSX X¼\x0013*}Li\x000e<½¼òúò)	¡mZ~øü/_¾àq\x0012ð-$\x0004¢ÎQM&²bÏã-#¢ay°ÎÇ &¬úW+Óè¹øÔó£Uä!]\x0013Þíx9wÏÚÖTF§tÎªµÒÏYMëµ×oë{»(hk`Cëlïd¯¥u\x0006ãeC)\]íY5X÷½Xyïe¦szÃ\x0019¦±\x0014\X#óÊHIº\x0012Ó<óÃ\x000f?°Ýí"]0ääì\x0016ñ,)ã/?üÄîÃ-ß~ý\x000bs)xgØìvl¯>Òu\x001bÚ¡ãÿú?ÿ\x000f~þþMfO9òéÃ=÷÷÷\]_Ño6ì®®éû
®iE;êÄ\x001bÉ3(Võ\x0000Í\x0018öû\x001b\x001aW8\x00109N\x0002áy+I/ªÝâ¥	8¥ã\x00191zßÒVsý<%8e5­\x0000Ë2¬Ád!\x0007\x0016S,!ÈÈQÑâ²"\x0007\x0015E¨÷Zcò¸t,\x00128¯\x0008­ÿü¬^Virv-Æ</p><p>°T;4\x0015ÕW\x0016rÝ\x0006R\x0012Uß\x0016aº9Ð¶\x0018\x000c Ò)@÷ïIrÏYØ§q¢h[Ï°i±®ÁZ)(R,,S¤é3Þ8Ù×4\x0014\x0012V¢iUXã[Xµ-¥X|½8gû\x0018¹Ù\x0015Z\x001fP£ÑX«R\x0011_ëõB²þÛÙ\x0006çb\x0005µ´ý@¿¹bØ^á}Ç\x001c\x00021eîï?r{{Ã2ÍN#óôÆfØ2ÜlÙm<Óqa\x0013­oÙ}\x0010ÒHÎÓi¤m[öÛ+qv±"ö\x0014a°</p><p>`LC%\x0002Z±Ã¹¾¾b·ß[R3ì÷Z\x0011r¶sªAB±RRÛèsø*¥\x0012\x0002jl8\x0003|E;`{y.µ:\x0013@POQ³\x0006Uìë\x0002eN</p><p>½\x0011\x0003Ä\x00140f|<\x001cùþý;ãxâþÃ-}×\x0013cä/ÿñgþöËÏ|ùò\x0003\x001fî?Ò÷\x0003!F\x000eoo´Þ±ÛôÜÝ\cNïó§;>ÝßÐ4Ót`6yY¸½¾¦oZJüù·?\x0013Ó/üË¿ü\x0017>~üiÌJT©\x0011^´</p><p>ó\x000c\x0016b:0NÏó\x000b¥\x001ciu8¿\x001bmãñM ó)ü\x001b&.Òx\x001f.sb2!À\x0012¥«ÉXÆiaÔ\x0019µÎö\x0018cÈÎà\x0001Û´5\x001e¬\x001c¸ô+I k[a°êÏ±Þáµ3³Ê`5ïáGS%\x0000ççªFêY\x0013\x0012\x0010"9^ \x0008'g¨û\x0000ë</p><p>s\x0000¶ºPZ=]a}?W,j!µv\x0002V~\x0016	@ê¦T!j\x0007Õp;«·d©AUßgãUá½Ã\x000c=w··qâh,Óë\x000b)E¬\x0015j¹Àñt¤\x001fz>~üHÎ2ÏNyY\x0019S\x0004Ý}ív i;þéýß¸úõ\x0007þúßþolãqÝÀ÷ç\x0017~þåÿ¥ñÇ§ï|}|b~}á~;ðñú\x000b·×{î>ÜÑïö4Ý ­¸\x0018»®¦\x0016¦Nra'\x0007él»¾Ço74Î@I²ú¬é\x0018ÚyI8D\x001a#ðVC\x0006d(ômÞëðBë=\x00051\x0015OU¦¢HÄ39ëN:2ç­³×\x000b÷\x001f%\x0015©~¡F#ù_9#.Eà\x00160ò½.Í¥A¥4\x0017óüu<u\x000ep\x0004¤\x001b]\x0005ïÈ\x0012áEWV\x0019#ò\x0012X¼ohVÐ«u&h)êaZÔ!å,ûD\x000f«ë
]ñÒ\x0000ä¢Ï|¤\x0012Î7Ò`øÑzßâ|oz1ËÀ9\x001b®\x0017$qúzq.»:M{ZñÈÍ3¹êô"ê/"Éük| ÒpY\x0017mRÀ»ýÕ\x001d]¿Çú\x000eãZ\x001c«\x001bÏ\x001e\x0019¦DÒîW"ÈÿÏÖ5I\x001cYzmwñÝcÍÌÊª\x0002Ð(t-Céyá\x0013Âg\x000c)M</p><p>g¦e\x001a¥PY¹ÇêëÝÌ\x000fjvÝ\x00133\x0001)df/÷ª\x001e=ç¨QÛ\x0017î+LPa²e7	ðÝÌ`Åâ&Ã\x0015_\x0015¤à¤@n\x0006\x0004E©´)ãÈhL[ ¢SE\x0016ÜØ*S¯L]UÎòÅã/æ¹qgTb%R¶54'P2»ãA`ÝI]cP\x001c#?ÿüW>|üÈåå\x0015¿ùõoÐýÈ»woÑJq<5wG>¼{Ëv·¥9n)ËétJU:®.ÖTNóüø\x0005?_\x0010¢¢kì7-«åÙ¤æx8ðþý/¼ùùg¾ÿî;®onX%www|xÿùtÉÅú¢(yqóß¾åþþù|EUMÓ&Ë=)¹\x0016#|®\x0000\x001dý!>bËUY Õ\x0014©t&Â\x0000j ²¡iÿB{ÿðT\x0011½Ã\x0007GÓ\x0018\x001e\x0002ûmdèKBtxmðQ3øÀ\x0010\x0005
-²`µaÿüÌa·¡¨1à}O\x0018àÓçÏüô×PJñêö%«Ò$\x0005é¡Dïq®\x0014¬6IöF@\x0011| OB\x0018'%Ä1ðe9X\Eò,ÈS\x000f&­·¯zs¢\x001b5F¦tç­!)hY}Nù:èS9 gF¦±\x000f7V¯ÍÒe\x0011\x000ej¹f~\x0014Q\x0010L@ãc2[ ®\x0007Ü0ðå°\x001fa»<´ïzî\x001fîÑÆp}}CUUødzÜµ-hEQ\x0016ÖÒ5->Fú týÇÇgþå?ý'êÕ\x0012UÍ0UÉOï¿ð_þËãÏ?þ\x0015­a6Ð\x001d\x000eLudzyÁb6e6m\x0008å,©k=yK~\x001cDnqhhö{b\x000cL§SAo\x0012Ìë{%7©&L\Å^·25\x0006E¯d\x001cFË´ø\x0014¸ôx^N&\x0004g(§ªÝû0\x0006ß\x001e\x0004ïÑÚ'²\x0007/\x0004ðh±\x0004Kç`Æz2\x0014\x001aÓZé~û`ë\x0018Eó9dGTUpJäÓ\x000fb\x0010¹¦N\x0005P\x001c\x0013ZÙ\x0003Î\x0015Ä`é\x0003càS0&TÙ»,'\x0004MZÇò\x001aò\x0004¯éü	Ö\x000f>°Û\x001fyzÚÈLCe6Ñ\x000c]O{8à%:'ÚËt!\x0007\x0013ièòñ 0*\x001ee"\x0001\x0018°9\x0000äLö«¸N\x001ev@ÐA0åqsÛé,Xf>\x0019é°yr¯ÒFª¼z¶%(+0q8cÊÞ¸ÎYtfµ%¡p\x001e\x001c\x0012G\x0015Bél*£Z¬¨HÁ.Ã8\x0019Ö9/ÿó3Äk0à\x000c¢<ïIÅ\x0004-Æ^õ<ð©ó\x000eºÄè3Zú\x0001Í±Á{ÑË\x001c\x000e\x00076gTÉtJ§Í3mßqyqÁt2a¿Ù³Ûl¸º¾fúê\x001bBô4gúî@ô\x001d}{à°{(ÄÇû/ÔuE×Î \x000eÐ³^Ïyñò\x001aE`·ß³Ù<ñüüÄb>c¹É´v­h»\x0001k-ûÝ¦k9´
ý \x000b´ë{H\x001b×%W7¼zõ\x001dW××¥k\x0007../)ª\x001a³©-§ë\x00173rM\x001d1nðþ	c\x001b´</p><p>©>Á®#*]ç\x0018[BØ\x0012\x0007næ¨¸»÷¼}säó§ÃÑÐ\x000f\x0005C ì))CÈ'eêõÒ÷4
¡o°V¤
F8ßVDÖFF³dÒ\x0010"mì	û=nðâ Aéßf¨\x00112\x0014æràë¬/µÚ FNs¦±\x0013ÍÛ\x0008³ BálL=î4¯sV</p><p>æàv\x0016@óE\x001c×'çÕ \x0010\x0018&.×zI´¹9jj¦`Ç¤¿ÍEMB\x001fD.R\x0010Ê0áê)¶¨Å%%$3á\x0008]?ph\x001bÖWèÒ\x0011µè½Jçè%XCçÄÃ«@\x001f\x0003]Í¾ÃÛ=ï\x001f7¨² \x001b\x0006.VK>¾ÿÈ_þÍv\x000f*²}Þ²T\¼¸äòâåjM5©T@§þN22NbkB¤÷\x0003ÇFæ÷9ç(g5\x0000¾oÓZ mÁZGé*jw¤ë\x0006¬"õõ""+Ìr\x0013	\x0001%mÐÄÞ\x000c\x0001\x00101KÀ\x0007écG\x0012\x0013X\x001b´±b©bs\x0018\x0007BµN&þJaµ¦O¶oÙr\x000e\x0012|¤\x0013îZî5</p><p>µ\x001fdëåÀ++ç4ª)\x0003ªäõãDú·xj*	¾Æ0hO¶»SJû¶\x0015\x0013ª²\x0014¥\x0014WkÌ AzË\x0003P\x0010cÏ0\x0004\x001e6Öá´¡p\x0006me=7Ç\x0016cö"/Lð-\x0014\x001al@¹\x0000®Cé\x0006G\x0019ÑÈ óôä½çù\x0019$\x0006I\x0014à:þ\x0007_©_)å&U:UZJ[ñÚ¬'²ðAå¸\x000e
\x0015\x0012µTeÚYõ\x0018O¯\x001eÓ
ÉÒçüwHï7Ã/#­^ËÌÌFôi1¤\x0000(Y8)³\x001dPJ%×$ÝH.è÷Ä\x0018X,xï¹¿¿c»Û²Z/O't0H3»ëþþÃáÀz}IbûÒ\x001a.Ö×X£h\x000f\x00025~ûí+%Î\x0006jnè{æÓÛKªÒ\x0012\x0016\x001d\x0007êÊ2Õ\x0010=ûý7?ÿÌÛ_ÞòÛ¿û;^½zµs>¼ÿÀÇ\x000f¿P¿ÂjÍt>åØt´±gµ\òâÅ\x000bf3	>îxùú;.¯oÑ(·(sàó§/EE\x0008ñþòçç
ß¼~ÍÕõ
UYÈZQù\x0002_KE\G\x0008\x0007b<jQ±'"#CÆÔ)UÒ2\x0004\x0019÷ÂhÕøØ÷^ôTÇ½b\x0018</p><p>\x0011ø&z²ÍÌ²>Ò5\x0010¬¸:T\x000eê«\x0005J-¥Bëë[êiM7t<<>`0X«Á3O?ôh\x001bd e×K¨IÜ\x0012£-Ê2\x0006¦\x000c§H 3©Ï\x001dÒc3 ë|F\x00005Wd¹T§Gä>dô§`4öN»cüWH§Rð§{\x001fãÏ/9\x000bL¤P câý¨/3^Ì\x0019r5\x0018¾JúNçA@Ñ\x0007-§NØöü(ê«J0òYR8c(Ë\x0002O \x000b\x0003®rÄFãbð'O_8vGêÅÅjÅöyËÅÄ"\x0000\x0000 \x0000IDATü\x0013\x001fÞ\x0004¥Nj¦eÁÅrÎ«\x001bnonX¬V¸²Â¸\x0002´Ty:¡Iâ&\x0014è®m\x0018º\x0001c\x001duQb¦\x001fz	\x0004Ôk\x0013\x001fHgl:å\x0000·Æ`£\x0018²+%1)Éç«Øð\x0007e2k/\x0007¼Ñ]'U)ê¡\x0011Wt\x0016ÖÈÔ{ïG3\x0006£$QFîD\x000c\x0007¬iûFjÅ\x001aé¿
Þ§\x0002 ¿Ç³ä-\x0004gÁ.ÃïjÜáhD	~Î\x0019!¶(Y:\x000eöx<R×\x0005\x0017ë\x0005®áÙU©è\x000cñ>¶¤T\x0001¦ï¥âÔ\x0013ªÊ1\x0018)\x0014aÈ#4µª0%\x0010\x0006¨¢C»\x0001\\x000bº\x0005%Á.\x001ai\x000f}Ed9¡À'ó\x0018\x0000ãé¡»_}é\x0008#u0ÿR*a]QRSÊ¢\x0012ÝMº¤>mlú=\x0019\x001c·lb\x0019æªIN\x0014É}\x0000%Ï!¥´\x001eKLlÄÄv\x0012Í¸èT\x0019\x0006ïÙl7ãôÅb\x0001!²Ûîøøá#JkêiÖÍv6×¯_³Z-	çùñ÷ïÞs8ì¨'õÇ\x0018ÏçÔU%Î0ÃÀ7··Ìf3bÜ\¬!(ê°Ñ>|ú@ß7,_Þâ¬áóñÀÛw¿ðêÕ7¬×+HA·ïZÞüü3Ú(f³)1x¾ãîî\x000b\x000f÷×ß¤i\x0012é´âæêét"VcÖquuI]W,\x0016KãB¬»ú¶çýÓ\x0007úÁóâå+¦Ó\x0018\x0015Éù|IßÇß0\x0004«\x0018H²¬¹¾1¬/¯¹¼¼d:\x0007®f@8ÆDås0¾aè÷Dßz\x0018br¤ cþhbPB±öiý\x001e@Ói=áêrÆbV\x0012(%\x0018%Óf
X¥0J6p\x0016*\x000bQ@\x000c»Á²TUÅz}ÁåÕ\x0015&\x000559ôâô_,\x0016K+¥Y®uÁe
\x000eó^J®L607£n\x0018G²Üig\x000e¬IÌJIeêæ\x0003\x00082£7Ut\x0007ÒÓ¾</p><p>±íJVùùò\x0001'í\x000c5¾là­8´\x000ca`\x0018zú^L§\x001fdtOÒöY'sæò8¨à;ºÝnð\x0014eî*Ú4ç­\x001f¼VMJ\é¤â-ì¨w+\x0001Åh5¦ª8ì÷¼ÿç§;\x001e\x0018Äû;¾ùî[.KV³	íjÁÐ{®W+n¯/øæöß¾~ÅÍÍ\x0015å¤\x0006£Ú¡´C\x001bÚ.r¯d_OD3&
±Jý­\x0018ER\x0013\x000cÄ\x0018d°³ÂYU"³xIh\x0016Óí<4zF\x0019ETÐÓ÷ä\x0001ÒÁgÛ¹(¦Ú©)=céJï6ÌYí\x0004M³öÄ&Äô\x001a2ý\\x0002¬¸äzÇ\x000fôi\x0004¬áxZV_ýåôýAs´µG¶N²\x001c¥\x0000£	Øq<\x001eéú\x0016k4ëå*\x0005></p><p>¬çØö²OSÍñØ°Ýn©</p><p>Uîi+âÿ¡\x001b\x0018zIÓ @</p><p>­\x0003QH\x0012mälÒg:½SÏåo"»,á?e¢ÿ/ÙpY%\x001bP\x0008"\x0016g**WãL!pMÂ9|\x0018\x0015dº~\x0010A©X@\x0019aw\x001dx½õ}K×¶Lê	eU2Àv»'\x0002³é¢pìv2\x0010Öû\x0001£\x0015ÏÛ
mÛòâößüæ·\x0014®`Øñ×\x001fäÍO?3_ÌøÕwßRUe\x0012M7ÔÕè[ÚÎ³×,Vkf3\x0011¸ïw{v»-ëõ_}ÿ¢×¼{x¤k[^¾zÁt:áéñ_Þ}¤Ï©RÖX\x0018+ý\x0018
Ì²÷²ð&õ««[¶»\x0003»ÝÃaÏ|>c\x0018\x0006¢âßÿÿH\x0008Csäþþ\x001eb»ÝÑ÷Ã¡!\x0004¸ººäöÅK..oÐÊ°ÛíÑ³ùbÍd²D+MÛö\x0018SQ\x0014\x0006WÍpÏ;¶e22_Ì¤ál¥®S5¬Ñüý\x000f?Hv\x000evã2ôu¤d8à|¡(ú^J²®Ø0\x000c\x0007Úfæ\x001ej¨ñÉÁ'"Bg¥D\x001eã?QªôÞGÚÞÓµ\x00105!¾2÷FÑû±\x0003 \x001d\x0004b°,N\x001d1FdV_5¯_}Çr±`¹\Â\x0010	½ô­bïGoHk\x0005Bæ\x001d\x00104õÅKñh­GV¥\x001aû¾g\x0007â\x0014\x0008ÉÂzùAN\x000eÏ·Ý°¢%!HN5cð
áÿ±³ìO\x000c¾LÈ\x0004BÈå¨#CôézÉa/\x0008¨H\x0019ú¾£mZb\x0010\x0001¸FQV\x0015hKtoÄW\x0002)3í\x0019|ÄyùìûÝ&­¡¶\x0016ë\x001cÆyB\x000cR8k½A\x0002[Ì\x0017-Ï\x000fÜþB©aV|)hCûüD¹ZòOÿîæOÿú\x0007ö»-ß¾~É«Û\x001bn¯/¸Z¯¨ª\x0012m-AÛO\x0002ãE\x0002\x0004qP\x001a\x000e¥ä³XSÈ½ðYn\x00121hGi-\x001c¶°h+ùL\x0010\x0012û1äÂ$\x0004c#YD\x001e¼\x0004½àÅnñ«ä#\x0015</p><p>*E\x0014K®¶åg*\x0011¾ÀhÔãû6z¼¿&ÿÝg\x0003Ä2ÚçÔW\x0016v¨\x000fa$2P\x0003ùß)É:¡\x000fÁËx1y³at\x001a\x0002N=iíèÛÝf3R¡êä	\\x000e(#¬ð\x0010\x0002:ÊhµÝvÜ]*Ì 6yÚ\x0007º¶C;#~²¥éBAªh\x001dd(\x0002Ê@Ô-AõØüF,?7¨ÎÏ¯ñÿÎKÛ¿xq¬ðr©/VV2Aí\x0004</p><p>BhÄûÃ·ïßÒ\x001c¬\x0016+&õæØððpOYVL&5C?°Ýn¨Ji@ïö;ÞxÇl6e¹\Q5M×Q5ZÁÓcGÛµ\x0018%a!xÂP³ÏxqsÍ´ªèû\x000e?t\__r±Z`\x0014\x001cv;¾<?à¬e¾X°ZÏéúO?Óv
ëõ</p><p>­Ò¬»¾èéO»­Ø'Å@×\x001ch\x000e\x0007|×R,ç¬\x000b¶9ã§\x0007¨LaÈz¦¯^0Ï)"-ìÀÕå\x00151F¬-\x0000\x0019ëóöí\x0007B\x000c¬W\x0017h-y×«\x0015¿ýá÷\x000c¾§i[ÚcC]Ï©êJÛÉtf\x00112ÑJËôíÄn½¾Ur\x001b-ÓÎèDª¹ÆS§\x0013¼:é\x0000óÝ>ëßñ\x0010\x0008N\x0001q ëvl·I;5<ácO\x0018Ë|!\x0011i\x0015S_BÉtt¶_$n\x0008?o|øØð¼ôÞ¤ú,Ð½,\x0019g¬eø0ª\x0004\x001dù§çg>~ü6y5OpaÀ£h&3|s.þMì¯¶BhNÚ¸\ñæ\x0012,{è§Hv¸$vg"\x001c$$4ÙQïO\x0005\x0001¼ïÉ\x0004\x0013?êòR°\x000bÉÑ&\x001f¤çû5&&°\x0016
NP2Z¬°\Gk\x000cÚÈ¡Û÷=q&\x000e\x0018ysÂ\x001b{¤0\x001d\x00040Ê\x0012¬ÈL6ÏOø\x0010D¯;­1Î ­À§Ä¡NãFûA¬¨´a4¼|qKô/w÷l¶;BÐtY5åù_ÿ7÷÷<X¸ºXpy1gløTbî)%ý[	ðr]2¼§P2ÆÌ¤\x001141ÝDþÊ\x0012³\x0003Hb|Z£±ÎR\x0016\x0005eáh|'\x0012\x0018£\x0010K±ô9TFÎÒsæ</p><p>}</p><p>\x0019[<¿K/0jù0²¦k§Qh±füÝÈÉ#5k¤}²ÆS¨Ôb©z\x001f\x0012Ö\x0017¢Î®+ù\x0004HEÊWÅ_ÚK*õ1a ¤Y©Ûtz¨´Ã÷=C\x001fh­Ùãý@UU¥c6«1Z³
®÷9ìÐ6b ß´½´ÊlZ¯Cà¸;`ÅÖ\x0005:(T°bH­5\x00046\x0010\x0008äL² á.}¶\x0001eû³ÐsÑõÙ®Î¿\x0000Q\x0004òSµ\x0005UêçicEGÕ\x001eÙl8ì6\x001c{T\x001cØ<>0-¹¼XSU%ûÝ\x0010zno®Mg4MK\x0008\x0003¯^½@\x001bÍãã#Óºçêæù|)üÐ±ZÎùõ÷ßR8Ëv»a¿?`a¹\â¦ë<\x0004ÏtRQ\x0015sBßÓ\x001d÷D?pì:Ê²ÀjM52ô+>~þÌýý\x0017ÒIó¹oQxª² ×\x0003Ç¦A)¸X­øîõk\QÕÁj½¢O0ÖÑ\x001ek,®°\x0004\x0002÷÷w¼ÿðë\x001bVË\x0015Ï
÷÷wÜÜ¾àåWL&sª\puõ¨\x0002\x0017iúB d	^µ\x001a¥ÏÜçÓÚ\x000cjÜ\x0004¨MJp:oó\x0008Ü\x0017sÐÆu7\x001eø\x0019VÎw?Ä\x0014ôÒù¹®uî¯\x0000
}ØÐ
\x001bl\x0011¥ºVJæv%Ê¬Ò1ùp\x0006ÈÎüÑ§*<¢¼BwÓw}KÓ6\x001c@\x00080ñÔù:ÖñxVùäÍ\x000c"ô=\x001e\x000fâÂ9Ma³ÊGØ&O\x0000\x0019I\x0010íQà;R)eÜ\x0019^\x000cÙ=õqÆ0ú8V½ùñD5fîã\x001cS Ï0SJ\´6dãé|úè<©ý¬÷®\x0010&´Ò&\x0005½t\x0013µ	Yª\x0013\x001233\x001eÕ\x001cC/&Ê1òüøÈÇO\x001cÍ8¡ª&¬\x000b6\x0014Î¡§3sÄ¦áÐ¶ô}ÇÅõz:\x0019¡Yã</p><p>Êj:ÒíÃØÇ\x000c8+nK×\x000cmï<xh\x000eæË÷ü¿ÿÇÿ¡çöfÍËK®//Lj1\x0011Ð\x0016¥Å\x00160Ó­£\x001fð^Þ¯V`\x0012ãJbj$\x0006\x0001A \x0006dÖÑHÖ°Ëë²¢.JCñ2|x¼Î\x001arB\x000bù¼¸\x0014BL£J¶erw¢J½Ta)Ö\x000b§ÄÇ&ÂM¨CU\x0015'Ãðî8*eFèX¤÷Ö÷~¬ô\x0002&!*2p»(¬\x000cU©õcDZ¯çû?¯}ï\x0003\x0018©@½ÕYÉVóu®\x0002¼Oð«æpì9\x001c;\x00163Ïb>¡¨,Ué0Ë\x0019»=tmK\x000c2¶m¿o¨ª#ÖÌ(\x001cD\x0007Ú&DÓã\x000e[:T\x0010Áº\x0012âL"\x0019-\x0019»=Ó¹IwTfÝW¸c«ó«Ç¦\x001dx\x0016<ÉÖ\x0018Wã</p><p>[`¤Áy8îyz~¤ëZ./V\x0014®àùaÃÃý'Öë5ÓI1ûû'ö»
ÍR"\x001f?~Â\x0016ÕzÅj¹àééî]ÃÕeKUWTeÁd"#yÏçÑ\x0016c\x0014'ü¦ùQ½ÌþÁs±^3Í/\x0016\x0018kd¤u\ß\KÆ¨\x0014Î*\x000eû\x001doúÉdÊúâ\x0012­5mÛòç?ÿÅbÁju!UÈó\x0013³ù\x0017·L¦Ô\x001fìP+Í¯(ê)U5a1³\¬ùöõ·L¦Ó4öD\x0015/.×\\]È&R"\x0014Î\x0010ÏÑMe\x0013é\x0014rÎo
Q\x001aâãwR?ç\x000c7\x001b!³_Iç5ÉìÔ£KÕÇX±¤_RJò'wú©</p><p>«­°§bC?l0®e¦5Ú8BrJ1 i-\x0006Æ`GìS© S/6Y!ö8H¯nð\x0019êó¡6lSféTSò¾­Ö\x0018kL&Ôu-L24SdÀUu¶mKÌGÊ´r\x0006\x0003Æý[å`\x000fì!JNDÒûÈ\x000e=ÙL:3ÿ´²c\x0010\x0016\x000b¨du0;¥}2¡Î¦\x0004rO:Uà2Û.\x00054iº|µcÉF2Ã6§)âÖä\x0005\x001a¹ûtÇþô'&uÍ|±\x0012H~`¿;òpOUÕ¼zùù|r\x0005Õ²a²\q<<³\¯)Ëõ\x000f`,Ñ8¹Ò¶GGÁ'ØÑY¦I]RW\x0005éV;)T%;VK..×¼¸¹¡¬«´¶¥i´AE©$!Mfø£èºDQÊI</p><p>\x0004­åw\x0018}uE\x001c\x000e4÷ï\x0018º\x0003ÙæL%ÊZÊIÍÜhêûÑ²Ëh9uº¯0RÿuÚ§ilçéÌ*UÌ\x0003Ùýê4.
4\x0011£\x0012c±\x0006k¤º>Ää)\x000f9r	¸]ç\x0019znC$Y2¦\x001e¡s\x0018#{.Â(¡\x0018AiT¾!gI\x0015cÀ*¨nB+!ß(kÇ¡Ùaä¦->p8ôXÛ</p><p>8g)Ë\x0002¥¦lOF#¢Õ<î[êJZ3ÆÓÑJ¬â\x001a-5Ø\x0002m\x000bP\x0005FWX\x0013}!=Y\x0015±á<Ø\x0017þôï¬ÍÆ¿=\x0018¿Æh"ã¨\x0014iÏÛÕÁG6\x001d}ðì\x000e;\x001e\x001f\x001eøôù\x0013ÓÉ÷ÔUÅrµÀ÷²pÔUI]h\x0005>}ä·o©'\x0013³¬/®Ïgâââ2\x001dT&É\x0001¶2½8e8]×\x0013\x0015¸²q:!ò¼Ùòþý;¾ãæúÒY\YóôôÌû'nnnQZ±ÙnéÃÀ«o^³\\P\x0016\x0015Zi®®ohÛ\x000e\x0015\x0014«Õ\x0005uU\x0011ÛÛ\x0017hmN§\x0018\x0003%UC!þ¡ÊÈ\x0015dmW×\x0013.¯oÈü©p\x001b¯ûyU5^ò\x0008imM\x0004âÙÏ¾°ò=:\x001dããrº?Þ=içe\x0000 Ã!ßT"Ã@ö\x0008E)\x0000}a\x0011MÓt|øø\x000f\x001f>p±^óí7ß°[ ¥ïwp\x0000Z\x0008-!öÂ¬yíeÀ m¸\x000c	EÆT+#ÕGÂ0\x0010}þ_ë\x0012Òa¥­J\x001a)0Úa^>\x0005\x000bk,³Ù\x0018áx<\x0012{9%rhº\x000eß¥ùfÞãº^\x0004Â¹·¯û9D­V:ùq¦ÞOrÕÉ\x0002]2</p><p>¥Ò\x0016Ô(D#Ùøå[</p><p>gm13IaúüK®g\x001c¯¯\x001eá³ü§TçMÓÈáÜ\})éaßÝñâÅ\x000bnnn0Öq8\x001c9\x001e\x001c\x000e
Çã¾ëØn·Ì\x0017\x000bÊIY-)'5Æ)\x0016ë5Fyv;q;÷\x0003¶\x00080ò³UÚ\x0000@®³éõ\x000cHî\x001bOa\x000bªª ZºÀ\x0014\x0005¶}*#Ò´(÷Ô\x000f^ö²x£Á9-	®&\x0016\x0015ÖÕ²ÀÙ\x0002e</p><p>´uâÖâ\x001c¾ÛÐ¶;ºí\x0017\x0011¢\x001b-kêÕr½¤Þíy:\x001ei\x0007	V:¹´D­(ÒØ¥\x0018ÄìÂj=2xó\x0016Ï	Ê«^e=_L\x0013\x0012ì\x0008;wX)RlNkR8\x0012!\x00061\x0014®:KT%9Ëgzð!	çµôÌs\x0012«rÐÍã§DhÎøº9\x0000AµJ¥ñB \x0015ÎæV©²Õ`$\x0014Q\x0005úAf\x000eés·]Ïn\x001fÐº\x0016Ö«\x0011ùP]×tm+Ä¥\x0018iZ1/)+ó\x0018¥\x000bÞ3´\x001d}£QV¥ª~x¤óGB\x001a3\x0015	Ø¯5wç'e<;\x0010Ox¬øÎ6úU§Ü¨4Ú\x0016¸¢b2Q5CPt­ô\x001d«\x0015Óé²(h-eY2©jfY²Íj!F\x0016ó\x0005ÁÃjµæêúÅrIÛ¶¼ÿÇG^¾xÉ|>§ï\x0003?ÿü\x0018#¿ûÝ\x000fL§3BÂÕTÕ\x0014m</p><p>r¬\x0004ãB3/Ï$Î\x001b¦a¹\aåòú\x0005ZkêÙ\x0014k¬,N­Y®/X.W©ÂÑã¤Õz=V\x000f'Q|LD+YP!\x0010ÁÐÏ®'\x0002-¦ó\x0007ùS2!»âL\x0015sÎv2Ä\x0019¡Å|o2³ðì(SêT¥i%Á,Fé9ôMÜsäUö»=}ÓR\x0016N&\x0006\x0018MðcsàÍÏoxÿþ\x0003¿þÍo¸yy#©j0Ìf3Ê² i\x000exß3M¹¼X3©</p><p>\x0014\x0003ýpdèwÐ Ô 9\x0011\x000cÎ>\åÀ"gyÈåí\x0008áX«¨«	8¹ÄX¢\x0015óY%î Eé¤Z2\x001a£\x0012kïLÌ-Y«a:Ñ´-ww÷¶¤.K1	Ol7O\x0014½_->°înNùd,\x0002-¦kÍ[XüÍ¾¢N·g|Où^~eS5î;H&¤IÛ</p><p>*Ê¤0®¼\x00173¼,\x0007:mèqÍ@ü*ÁÉ×©\x0017\x0012ÙèA\T>ù\x000c</p><p>æ³\x0019\x0013\x0004§*ÁÙÉd i<?=Ó´
q\x0018ð1ðùÓG\x0006?pu}Íúòè\x001bÚ¡áÐì9\x001ew²5\x0016{b\x0006¨T¦h¥)]Åj¹ÆÚvßÐ·=«¨'\x0015ÚE\x001e¶÷<î6\[LÒ\x0002+e	(ÑÃùHT\x0005ª¬1Õj±ÀÔ5¶¬°õ\x0014m\x001d(C\x001fÅ0\x0002e\x0010â\x000c¬µEDÏ/\x0008w\x0015±ëÀ\x0004ôÜr{sIßµ<üáßDÇèõ´ÍÝ#Ñõ\x0005ïñ)xdÓq1\x0018O\x0015hêï	éE'¦&iÿþ\x001cV M²Sdü&Ý`1\x0005EQ&ÄK¸\x0004Êñ¹\x0006<7\x0006\x0015O}_[\x0013yä@,S\x000eÆ:
\x0017Î=Iy¨íF[3Âüí\x0003!Êë×uÖ¾÷ø¨8\x001c\x001baH\x001c\x0004u2bÊ(³ªªÇ#Á\x000f\x0003]×p<\x001a&m+,®ð\x0018+\x000b6\x000cÐ\x000c¨2\x0012lÏàÉil+Z0Tzò|É+R^ù¨\x001aù^Ú!õ.dúqúð\x0018À`0(³¤G%Ä¥ÔÌçKªj«*\x0012»<2Äi÷=Ï
Í/Ç{Ö«\x000bÒì÷bîºZ-¹¸º¡¨JÊJf¡9çX,\x0016ôCÀ\x0018µ\x0005W77Ì\x0017KBÔ	ÖÚ\x0013£J[|\x0010W/¿áå«oFýH!`±\Ä*WTÑ\x0006LbT:\x0011´\x001a\x001f#\x001diìÍé|\x001b\x0007ª¦ ¥ò© ñ\x0010ÒQèùéKX°qÌÀ¬cB\x0004½=ó¥Î`Î\ÁÅDÃnÄ¸·,K\áèº>UØâ³ys{³çÍ3\x001f>| ®\x0005jE)>}üH\x000cÕrNá¤°Û\x001d(J3«5ÎÀöéQz\x001bõ\x0014¥\x0005êº#m×°Ï¹\-ÖahhgÚö\x0011B+\x0014r</p><p>ò²Ë£@"</p><p>¼\x00174H\x0016\x001aCvï\x0003]\x001féZ0\x0014\\Ü¢\x000c\x001cZC\x0008\x000e¢¸U\x000cÑ3\x000cyb¶§ï=}w\x0018Ùgb%P©µ\x0005!ÀíÍ\x000b¦ó%ËÙùd3N\x0008W»
~èÑVS×5E¤\x00111ÃÓ8ÔÈ
VãAH\x0002YÕ©\x001eÉ	Ì\x0007×©H\x001fïôøó|´Éz\x0016ÒkÉ7s?2×Ê:-»h¥ê-5qcÒÜ©¨`\x0010ø8Ãµ*õSmÃn÷ÌÓæÝnK]U\x0004%\x0004\x0001\x001d
A\x0004Y\x0014Ã\x000e[Ö­¿üá_Ù?></p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Sub Resource Integrity Attribute Missing
##### Medium (High)
  
  
  
  
#### Description
<p>The integrity attribute is missing on a script or link tag served by an external server. The integrity tag prevents an attacker who have gained access to this server from injecting a malicious content. </p>
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
Instances: 12
  
### Solution
<p>Provide a valid integrity attribute to the tag.</p>
  
### Reference
* https://developer.mozilla.org/en/docs/Web/Security/Subresource_Integrity

  
#### CWE Id : 345
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Vulnerable JS Library
##### Medium (Medium)
  
  
  
  
#### Description
<p>The identified library bootstrap, version 4.0.0 is vulnerable.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js](https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js](https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_Sk_5FPCbtvaCW1_SJUXh0cpAN8WN3gm73ttGk9CnYJE.js](https://www.snu.gouv.fr/sites/default/files/js/js_Sk_5FPCbtvaCW1_SJUXh0cpAN8WN3gm73ttGk9CnYJE.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js](https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js](https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `* Bootstrap v4.0.0`
  
  
  
  
Instances: 5
  
### Solution
<p>Please upgrade to the latest version of bootstrap.</p>
  
### Other information
<p>CVE-2019-8331</p><p>CVE-2018-14041</p><p>CVE-2018-14040</p><p>CVE-2018-14042</p><p></p>
  
### Reference
* https://github.com/twbs/bootstrap/issues/28236
* https://github.com/twbs/bootstrap/issues/20184
* 

  
#### CWE Id : 829
  
#### Source ID : 3

  
  
  
  
### Big Redirect Detected (Potential Sensitive Information Leak)
##### Low (Medium)
  
  
  
  
#### Description
<p>The server has responded with a redirect that seems to provide a large response. This may indicate that although the server sent a redirect it also responded with body content (which may include sensitive details, PII, etc.).</p>
  
  
  
* URL: [https://www.snu.gouv.fr/node/51](https://www.snu.gouv.fr/node/51)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/65](https://www.snu.gouv.fr/node/65)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/25](https://www.snu.gouv.fr/node/25)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/60](https://www.snu.gouv.fr/node/60)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/2](https://www.snu.gouv.fr/node/2)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/6](https://www.snu.gouv.fr/node/6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/13](https://www.snu.gouv.fr/node/13)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/5](https://www.snu.gouv.fr/node/5)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/52](https://www.snu.gouv.fr/node/52)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/accueil-5](https://www.snu.gouv.fr/accueil-5)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/16](https://www.snu.gouv.fr/node/16)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/node/3](https://www.snu.gouv.fr/node/3)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
### Solution
<p>Ensure that no sensitive information is leaked via redirect responses. Redirect responses should have almost no content.</p>
  
### Other information
<p>Location header URI length: 90 [https://www.snu.gouv.fr/generation-snu-episode-2-augustin-et-les-pompiers-du-patrimoine-51].</p><p>Predicted response size: 390.</p><p>Response Body Length: 606.</p>
  
### Reference
* 

  
#### CWE Id : 201
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Cross-Domain JavaScript Source File Inclusion
##### Low (Medium)
  
  
  
  
#### Description
<p>The page includes one or more script files from a third-party domain.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Parameter: `https://tag.aticdn.net/609231/smarttag.js`
  
  
  * Evidence: `<script src="https://tag.aticdn.net/609231/smarttag.js"></script>`
  
  
  
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_Sk_5FPCbtvaCW1_SJUXh0cpAN8WN3gm73ttGk9CnYJE.js](https://www.snu.gouv.fr/sites/default/files/js/js_Sk_5FPCbtvaCW1_SJUXh0cpAN8WN3gm73ttGk9CnYJE.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js](https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js](https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js](https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js](https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Eval`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sitemap.xml](https://www.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `must-revalidate, no-cache, private`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `max-age=900, public`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sitemap.xml](https://www.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_marianne_header.png](https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_marianne_header.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/inscription-blanc.svg](https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/inscription-blanc.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css](https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/inscription-bleu.svg](https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/inscription-bleu.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/styles/1200x800/public/2020-01/scx0609452-jpg-18.jpg?itok=HbzawNdR](https://www.snu.gouv.fr/sites/default/files/styles/1200x800/public/2020-01/scx0609452-jpg-18.jpg?itok=HbzawNdR)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/Horloge-rouge.svg](https://www.snu.gouv.fr/themes/custom/snu_theme/html/dist/assets/imgs/icons/Horloge-rouge.svg)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js](https://www.snu.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js](https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_Repubique_francaise_logo_SNU_header.png](https://www.snu.gouv.fr/sites/default/files/site_logo/2020-03/2020_Repubique_francaise_logo_SNU_header.png)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/2020-02/logo-snu_0.jpg](https://www.snu.gouv.fr/sites/default/files/2020-02/logo-snu_0.jpg)
  
  
  * Method: `GET`
  
  
  
  
Instances: 12
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_cz-ca4MQUWSkYxPzjdY05j9WTyweaPg6FoVUkfHsc9E`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_puUAMJLpARFyciPuk7zQumKmKNMg2e-60LrZdBepa4o`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  * Evidence: `/sites/default/files/css/css_8dgbZC8WC7xus7QrRyJJihdDKiKIxvwtDE7UBWTyTcQ`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�ȭz��y����ߊW���,��,���\x0000�K�\x0004E�ȏ�N�B銘�L�g��B�e�^��(</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
* URL: [https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98](https://www.snu.gouv.fr/retour-sur-cette-1ere-semaine-du-sejour-de-cohesion-98)
  
  
  * Method: `GET`
  
  
  * Evidence: `admin`
  
  
  
  
Instances: 12
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bADMIN\b and was detected in the element starting with: "<script type="application/json" data-drupal-selector="drupal-settings-json">{"path":{"baseUrl":"\/","scriptPath":null,"pathPrefi", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js](https://www.snu.gouv.fr/sites/default/files/js/js_hRvNfErhofwgw0Y9X0aiHE6pOcQGws-ofIcFF4PFJlc.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js](https://www.snu.gouv.fr/sites/default/files/js/js_LdWSnxjsBpZIqF5i2W7MV-ydwmQZvBFrpornUWuDzRY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js](https://www.snu.gouv.fr/sites/default/files/js/js_SVFncP9hcXmC-GALAw67dxwBmwg6KiY5Jcyg6FT9IF0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/2-000-jeunes-ont-experimente-le-snu-l-an-dernier-25](https://www.snu.gouv.fr/2-000-jeunes-ont-experimente-le-snu-l-an-dernier-25)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a><span>Le séjour de cohésion en 2021 se déroule dans un centre d'accueil de votre région, et a priori, en dehors de votre département, sauf exceptions et cas particulier. Vous pouvez prendre connaissance de votre lieu d’affectation sur </span></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-snu-est-sur-instagram-16](https://www.snu.gouv.fr/le-snu-est-sur-instagram-16)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23](https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a><span><span>Les affectations pour le séjour de cohésion sont prononcées en fonction des objectifs de représentativité des cohortes dans la limite des capacités d’accueil.</span></span></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a href="" data-video-raw-id="227" data-video-name="2e semaine" data-target="#video-modal" data-toggle="modal" title="Voir la vidéo" class="link-play-video js-trigger-modal">Retour sur la 2e semaine</a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js](https://www.snu.gouv.fr/sites/default/files/js/js_i2O6BvF65McVI3Ww32mEXzN9fcIa80kYqGi2OEEktcY.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a id='"+S+"'></a>`
  
  
  
  
* URL: [https://www.snu.gouv.fr/nous-contacter-35](https://www.snu.gouv.fr/nous-contacter-35)
  
  
  * Method: `GET`
  
  
  * Evidence: `<a>consulter la </a>`
  
  
  
  
Instances: 12
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sitemap.xml](https://www.snu.gouv.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `private`
  
  
  
  
Instances: 1
  
### Solution
<p>The content may be marked as storable by ensuring that the following conditions are satisfied:</p><p>The request method must be understood by the cache and defined as being cacheable ("GET", "HEAD", and "POST" are currently defined as cacheable)</p><p>The response status code must be understood by the cache (one of the 1XX, 2XX, 3XX, 4XX, or 5XX response classes are generally understood)</p><p>The "no-store" cache directive must not appear in the request or response header fields</p><p>For caching by "shared" caches such as "proxy" caches, the "private" response directive must not appear in the response</p><p>For caching by "shared" caches such as "proxy" caches, the "Authorization" header field must not appear in the request, unless the response explicitly allows it (using one of the "must-revalidate", "public", or "s-maxage" Cache-Control response directives)</p><p>In addition to the conditions above, at least one of the following conditions must also be satisfied by the response:</p><p>It must contain an "Expires" header field</p><p>It must contain a "max-age" response directive</p><p>For "shared" caches such as "proxy" caches, it must contain a "s-maxage" response directive</p><p>It must contain a "Cache Control Extension" that allows it to be cached</p><p>It must have a status code that is defined as cacheable by default (200, 203, 204, 206, 300, 301, 404, 405, 410, 414, 501).   </p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### CWE Id : 524
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Retrieved from Cache
##### Informational (Medium)
  
  
  
  
#### Description
<p>The content was retrieved from a shared cache. If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance. </p>
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/accueil-5](https://www.snu.gouv.fr/accueil-5)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js](https://www.snu.gouv.fr/sites/default/files/js/js_VtafjXmRvoUgAzqzYTA3Wrjkx9wcWhjP0G4ZnnqRamA.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css](https://www.snu.gouv.fr/sites/default/files/css/css_yahZU6stezUpiKbnjynBclwBPV_PMv5fLeaeYnE0xEY.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `HIT`
  
  
  
  
Instances: 12
  
### Solution
<p>Validate that the response does not contain sensitive, personal or user-specific information.  If it does, consider the use of the following HTTP response headers, to limit, or prevent the content being stored and retrieved from the cache by another user:</p><p>Cache-Control: no-cache, no-store, must-revalidate, private</p><p>Pragma: no-cache</p><p>Expires: 0</p><p>This configuration directs both HTTP 1.0 and HTTP 1.1 compliant caching servers to not store the response, and to not retrieve the response (without validation) from the cache, in response to a similar request.</p>
  
### Reference
* https://tools.ietf.org/html/rfc7234
* https://tools.ietf.org/html/rfc7231
* http://www.w3.org/Protocols/rfc2616/rfc2616-sec13.html (obsoleted by rfc7234)

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107](https://www.snu.gouv.fr/ils-l-ont-fait-le-defile-107)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/la-mission-d-interet-general-27](https://www.snu.gouv.fr/la-mission-d-interet-general-27)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-service-national-universel-29](https://www.snu.gouv.fr/le-service-national-universel-29)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/foire-aux-questions-11](https://www.snu.gouv.fr/foire-aux-questions-11)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/accueil-5](https://www.snu.gouv.fr/accueil-5)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/l-engagement-28](https://www.snu.gouv.fr/l-engagement-28)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-sejour-de-cohesion-26](https://www.snu.gouv.fr/le-sejour-de-cohesion-26)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=900`
  
  
  
  
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
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483644`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `70966589`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483645`
  
  
  
  
* URL: [https://www.snu.gouv.fr/](https://www.snu.gouv.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483647`
  
  
  
  
* URL: [https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101](https://www.snu.gouv.fr/les-volontaires-du-snu-au-defile-du-14-juillet-101)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr](https://www.snu.gouv.fr)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css](https://www.snu.gouv.fr/sites/default/files/css/css_mPodpH5f0tfuCWC-ylfGyU_u4ZLWUsAs__V1Jc2osm4.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `2147483646`
  
  
  
  
* URL: [https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54](https://www.snu.gouv.fr/proposez-des-missions-d-interet-general-54)
  
  
  * Method: `GET`
  
  
  * Evidence: `20200625`
  
  
  
  
* URL: [https://www.snu.gouv.fr/actualites-6](https://www.snu.gouv.fr/actualites-6)
  
  
  * Method: `GET`
  
  
  * Evidence: `20210712`
  
  
  
  
* URL: [https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23](https://www.snu.gouv.fr/donnees-personnelles-et-cookies-23)
  
  
  * Method: `GET`
  
  
  * Evidence: `334279774`
  
  
  
  
* URL: [https://www.snu.gouv.fr/le-kit-de-communication-snu-38](https://www.snu.gouv.fr/le-kit-de-communication-snu-38)
  
  
  * Method: `GET`
  
  
  * Evidence: `70966589`
  
  
  
  
Instances: 12
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>2147483644, which evaluates to: 2038-01-19 03:14:04</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
