
# ZAP Scanning Report

Generated on Sat, 14 Aug 2021 10:39:58


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 3 |
| Low | 2 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| CSP: script-src unsafe-inline | Medium | 3 | 
| CSP: style-src unsafe-inline | Medium | 3 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Incomplete or No Cache-control Header Set | Low | 1 | 
| Permissions Policy Header Not Set | Low | 11 | 
| Base64 Disclosure | Informational | 4 | 
| Information Disclosure - Suspicious Comments | Informational | 11 | 
| Modern Web Application | Informational | 5 | 
| Storable and Cacheable Content | Informational | 6 | 
| Storable but Non-Cacheable Content | Informational | 5 | 
| Timestamp Disclosure - Unix | Informational | 6 | 

## Alert Detail


  
  
  
  
### CSP: script-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>script-src includes unsafe-inline.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### CSP: style-src unsafe-inline
##### Medium (Medium)
  
  
  
  
#### Description
<p>style-src includes unsafe-inline.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'self' https://api.stargate.igloo.fabnum.fr/api;script-src 'self' 'unsafe-inline' 'unsafe-eval';style-src 'self' 'unsafe-inline'`
  
  
  
  
Instances: 3
  
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

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  
  
Instances: 1
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/19679968cad2c9faaba654ba2c7361a8dbb981ff.b1b62fb7f28acabec8cf.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/19679968cad2c9faaba654ba2c7361a8dbb981ff.b1b62fb7f28acabec8cf.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.2c852fab7213d17b271d.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.2c852fab7213d17b271d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-1f6ba122e0a76d8bdb8e.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-1f6ba122e0a76d8bdb8e.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/ea91a2c606399ec57d3b9a186cee88b21ed6ba75.530bc8125188699e45bd.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/ea91a2c606399ec57d3b9a186cee88b21ed6ba75.530bc8125188699e45bd.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/29107295.e2f5a1d70484253c977c.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/29107295.e2f5a1d70484253c977c.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/d5ded92cff02a1f74e305d4e7c6466db475004fc.01f0dacc2f54b16663ed.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/d5ded92cff02a1f74e305d4e7c6466db475004fc.01f0dacc2f54b16663ed.js)
  
  
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

  
  
  
  
### Base64 Disclosure
##### Informational (Medium)
  
  
  
  
#### Description
<p>Base64 encoded data was disclosed by the application/web server. Note: in the interests of performance not all base64 strings in the response were analyzed individually, the entire response should be looked at by the analyst/security team/developer(s).</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `1323-lTBPUZY3qWP/aCn64oHG+p/xbco`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `f54-vY6swsAankv9Otihw7vA85Rwet4`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `1323-lTBPUZY3qWP/aCn64oHG+p/xbco`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/66d5c522d509ec0bd2ae14f9fa0a98ee41c080a9.8f40875f7f5a34f3d676.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/66d5c522d509ec0bd2ae14f9fa0a98ee41c080a9.8f40875f7f5a34f3d676.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z`
  
  
  
  
Instances: 4
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>�}��T�=FXޥ�����\x0007\x001b�ŷ(</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/pages/_app-57ee60eeddb26edc6d22.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/pages/_app-57ee60eeddb26edc6d22.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/19679968cad2c9faaba654ba2c7361a8dbb981ff.b1b62fb7f28acabec8cf.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/19679968cad2c9faaba654ba2c7361a8dbb981ff.b1b62fb7f28acabec8cf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/8fb74a092ad848b6f0246b3718b2199c09cae25a.171dbb6eec5c511adedf.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/8fb74a092ad848b6f0246b3718b2199c09cae25a.171dbb6eec5c511adedf.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.2c852fab7213d17b271d.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/commons.2c852fab7213d17b271d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/54eebfa4dac8607b9504a24a3e2a4dfdd62ccc24.232fd819fb450b21c57c.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/54eebfa4dac8607b9504a24a3e2a4dfdd62ccc24.232fd819fb450b21c57c.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `query`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/d5ded92cff02a1f74e305d4e7c6466db475004fc.01f0dacc2f54b16663ed.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/d5ded92cff02a1f74e305d4e7c6466db475004fc.01f0dacc2f54b16663ed.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `bug`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
Instances: 11
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bQUERY\b and was detected in the element starting with: "<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"IIMmR27PwGLOX1g", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"IIMmR27PwGLOX1gcg-S4G","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/","query":{},"buildId":"IIMmR27PwGLOX1gcg-S4G","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script id="__NEXT_DATA__" type="application/json">{"props":{"pageProps":{}},"page":"/404","query":{},"buildId":"IIMmR27PwGLOX1gcg-S4G","runtimeConfig":{"API_URL":"https://api.stargate.igloo.fabnum.fr/api"},"isFallback":false,"customServer":true,"appGip":true}</script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/polyfills-806d69b60a648b7a73e7.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/polyfills-806d69b60a648b7a73e7.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
Instances: 5
  
### Solution
<p>This is an informational alert and so no changes are required.</p>
  
### Other information
<p>No links have been found while there are scripts, which is an indication that this is a modern web application.</p>
  
### Reference
* 

  
#### Source ID : 3

  
  
  
  
### Storable and Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, and may be retrieved directly from the cache, rather than from the origin server by the caching servers, in response to similar requests from other users.  If the response data is sensitive, personal or user-specific, this may result in sensitive information being leaked. In some cases, this may even result in a user gaining complete control of the session of another user, depending on the configuration of the caching components in use in their environment. This is primarily an issue where "shared" caching servers such as "proxy" caches are configured on the local network. This configuration is typically found in corporate or educational environments, for instance.</p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/css/6ff37306c670ca78ffc0.css](https://stargate.igloo.fabnum.fr/_next/static/css/6ff37306c670ca78ffc0.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-1f6ba122e0a76d8bdb8e.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/webpack-1f6ba122e0a76d8bdb8e.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/main-fb3641aad4fb44695a9f.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=31536000`
  
  
  
  
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

  
  
  
  
### Storable but Non-Cacheable Content
##### Informational (Medium)
  
  
  
  
#### Description
<p>The response contents are storable by caching components such as proxy servers, but will not be retrieved directly from the cache, without validating the request upstream, in response to similar requests from other users. </p>
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/global.css](https://stargate.igloo.fabnum.fr/fonts/global.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff](https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff](https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff2](https://stargate.igloo.fabnum.fr/fonts/marianne-regular-webfont.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff2](https://stargate.igloo.fabnum.fr/fonts/marianne-bold-webfont.woff2)
  
  
  * Method: `GET`
  
  
  * Evidence: `max-age=0`
  
  
  
  
Instances: 5
  
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
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/robots.txt](https://stargate.igloo.fabnum.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/](https://stargate.igloo.fabnum.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741821`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js](https://stargate.igloo.fabnum.fr/_next/static/chunks/framework.e8d7d1fe01cd920b2e45.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741822`
  
  
  
  
* URL: [https://stargate.igloo.fabnum.fr/sitemap.xml](https://stargate.igloo.fabnum.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `29107295`
  
  
  
  
Instances: 6
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>29107295, which evaluates to: 1970-12-03 21:21:35</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
