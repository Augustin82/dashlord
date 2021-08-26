
# ZAP Scanning Report

Generated on Thu, 26 Aug 2021 03:43:46


## Summary of Alerts

| Risk Level | Number of Alerts |
| --- | --- |
| High | 0 |
| Medium | 5 |
| Low | 5 |
| Informational | 6 |

## Alerts

| Name | Risk Level | Number of Instances |
| --- | --- | --- | 
| Content Security Policy (CSP) Header Not Set | Medium | 2 | 
| Cross-Domain Misconfiguration | Medium | 11 | 
| CSP: Wildcard Directive | Medium | 3 | 
| Source Code Disclosure - Java | Medium | 2 | 
| X-Frame-Options Header Not Set | Medium | 2 | 
| Incomplete or No Cache-control Header Set | Low | 2 | 
| Permissions Policy Header Not Set | Low | 9 | 
| Server Leaks Version Information via "Server" HTTP Response Header Field | Low | 11 | 
| Strict-Transport-Security Header Not Set | Low | 3 | 
| X-Content-Type-Options Header Missing | Low | 9 | 
| Base64 Disclosure | Informational | 2 | 
| Information Disclosure - Suspicious Comments | Informational | 5 | 
| Modern Web Application | Informational | 2 | 
| Storable and Cacheable Content | Informational | 2 | 
| Storable but Non-Cacheable Content | Informational | 9 | 
| Timestamp Disclosure - Unix | Informational | 13 | 

## Alert Detail


  
  
  
  
### Content Security Policy (CSP) Header Not Set
##### Medium (High)
  
  
  
  
#### Description
<p>Content Security Policy (CSP) is an added layer of security that helps to detect and mitigate certain types of attacks, including Cross Site Scripting (XSS) and data injection attacks. These attacks are used for everything from data theft to site defacement or distribution of malware. CSP provides a set of standard HTTP headers that allow website owners to declare approved sources of content that browsers should be allowed to load on that page — covered types are JavaScript, CSS, HTML frames, fonts, images and embeddable objects such as Java applets, ActiveX, audio and video files.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js](https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css](https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `Access-Control-Allow-Origin: *`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
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

  
  
  
  
### CSP: Wildcard Directive
##### Medium (Medium)
  
  
  
  
#### Description
<p>The following directives either allow wildcard sources (or ancestors), are not defined, or are overly broadly defined: </p><p>frame-ancestors, form-action</p><p></p><p>The directive(s): frame-ancestors, form-action are among the directives that do not fallback to default-src, missing/excluding them is the same as allowing anything.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `default-src 'none'`
  
  
  
  
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

  
  
  
  
### Source Code Disclosure - Java
##### Medium (Medium)
  
  
  
  
#### Description
<p>Application Source Code was disclosed by the web server - Java</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class j{async add(e){await l.post("/api/todos",e)}async retrieveAll(){return(await l.get("/api/todos")).data}}const S=c({name:"todo",initialState:{items:[],isFetching:!1,isAdding:!1},reducers:{startedToAddTodo:(e,t)=>n(d({},e),{isAdding:!0,items:[...e.items,t.payload]}),successfullyAddedTodo:e=>n(d({},e),{isAdding:!1}),startedToFetchTodos:e=>n(d({},e),{isFetching:!0}),successfullyFetchedTodos:(e,t)=>n(d({},e),{isFetching:!1,items:t.payload})}}),D=u({[S.name]:S.reducer}),k=e=>m({reducer:D,middleware:g({thunk:{extraArgument:e}})}),F=p,N=e=>e.todo.items,x=e=>e.todo.isFetching,G=e=>e.todo.isAdding,L=()=>{const e=F(x),t=F(N);return b.createElement("ul",null,e?"Loading...":t.map((e=>b.createElement("li",{key:e.uuid},e.description))))},H=e=>async(t,a,{todoGateway:r})=>{t(S.actions.startedToAddTodo(e)),await r.add(e),t(S.actions.successfullyAddedTodo())},I=()=>async(e,t,{todoGateway:a})=>(e(S.actions.startedToFetchTodos()),a.retrieveAll().then((t=>{e(S.actions.successfullyFetchedTodos(t))})));const z=()=>{(()=>{const e=y();f.exports.useEffect((()=>{e(I())}),[e])})();const e=y(),t=F(G),[a,r]=f.exports.useState(""),i=()=>{e(H({uuid:q(),description:a})),r("")};return b.createElement("div",{className:"App"},b.createElement("header",{className:"App-header"},b.createElement("img",{src:"/assets/logo.ecc203fb.svg",className:"App-logo",alt:"logo"}),b.createElement("p",null,"My todos"),b.createElement(L,null),b.createElement("input",{type:"text",value:a,onChange:e=>{t||r(e.target.value)},onKeyDown:e=>"Enter"===e.key&&i()}),b.createElement("button",{disabled:t,onClick:i},"Add Todo")))},C=/\+?[0-9]*/,M=w({email:O().required("Obligatoire").email("Veuillez saisir une adresse e-mail valide"),firstName:O().required("Obligatoire"),lastName:O().required("Obligatoire"),phone:O().matches(C,"Numero de téléphone incorrect").nullable(!0),dateStart:h().required("Obligatoire"),dateEnd:h().required("Obligatoire").min(v("dateStart"),"Date de fin doit être après la date de début").test("moins-28j","La durée maximale d'immersion est de 28 jours",((e,t)=>{const a=t.parent.dateStart;if(!(e&&a&&a instanceof Date))return!1;let r=new Date(a);return r.setDate(r.getDate()+28),e<=r})),siret:O().required("Obligatoire").length(14,"SIRET doit étre composé de 14 chiffres"),businessName:O().required("Obligatoire"),mentor:O().required("Obligatoire"),mentorPhone:O().required("Obligatoire").matches(C,"Numero de téléphone de tuteur incorrect"),mentorEmail:O().required("Obligatoire").email("Veuillez saisir un adresse mail correct"),workdays:E(O().required()).required("Obligatoire"),workHours:O().required("Obligatoire"),individualProtection:A().required("Obligatoire"),sanitaryPrevention:A().required("Obligatoire"),sanitaryPreventionDescription:O().nullable(!0),immersionAddress:O().nullable(!0),immersionObjective:O().nullable(!0),immersionProfession:O().required("Obligatoire"),immersionActivities:O().required("Obligatoire"),immersionSkills:O().nullable(!0),beneficiaryAccepted:A().equals([!0],"L'engagement est obligatoire"),enterpriseAccepted:A().equals([!0],"L'engagement est obligatoire")}).required(),R=w({id:O().required()}).required();w({id:O().required()}).required(),w({id:O().required(),formulaire:M.required()}).required();const V=w({id:O().required()}).required();console.log("GATEWAY : ","HTTP");const $=new j,B=new class{async add(e){await M.validate(e);const t=(await l.post("/api/formulaires",e)).data;return await R.validate(t),t.id}async get(e){const t=await l.get(`/api/formulaires/${e}`),a=n(d({},t.data),{dateStart:new Date(t.data.dateStart),dateEnd:new Date(t.data.dateEnd)});return console.log(a),await M.validate(a),a}async update(e,t){await M.validate(t);const a=(await l.post(`/api/formulaires/${e}`,t)).data;return await V.validate(a),a.id}},K=k({todoGateway:$});T.render(b.createElement(b.StrictMode,null,b.createElement(P,{store:K},b.createElement(z,null))),document.getElementById("root"));export{j as H,M as a,k as c,B as f}`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `class sy{constructor(e,t){if(this.refs=e,this.refs=e,"function"==typeof t)return void(this.fn=t);if(!ay(t,"is"))throw new TypeError("`is:` is required for `when()` conditions");if(!t.then&&!t.otherwise)throw new TypeError("either `then:` or `otherwise:` is required for `when()` conditions");let{is:n,then:r,otherwise:i}=t,o="function"==typeof n?n:(...e)=>e.every((e=>e===n));this.fn=function(...e){let t=e.pop(),n=e.pop(),a=o(...e)?r:i;if(a)return"function"==typeof a?a(n):n.concat(a.resolve(t))}}resolve(e,t){let n=this.refs.map((e=>e.getValue(null==t?void 0:t.value,null==t?void 0:t.parent,null==t?void 0:t.context))),r=this.fn.apply(e,n.concat(e,t));if(void 0===r||r===e)return e;if(!uy(r))throw new TypeError("conditions must return a schema object");return r.resolve(t)}}function ly(e){return null==e?[]:[].concat(e)}function cy(){return(cy=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}let fy=/\$\{\s*(\w+)\s*\}/g;class dy extends Error{static formatError(e,t){const n=t.label||t.path||"this";return n!==t.path&&(t=cy({},t,{path:n})),"string"==typeof e?e.replace(fy,((e,n)=>wp(t[n]))):"function"==typeof e?e(t):e}static isError(e){return e&&"ValidationError"===e.name}constructor(e,t,n,r){super(),this.name="ValidationError",this.value=t,this.path=n,this.type=r,this.errors=[],this.inner=[],ly(e).forEach((e=>{dy.isError(e)?(this.errors.push(...e.errors),this.inner=this.inner.concat(e.inner.length?e.inner:e)):this.errors.push(e)})),this.message=this.errors.length>1?`${this.errors.length} errors occurred`:this.errors[0],Error.captureStackTrace&&Error.captureStackTrace(this,dy)}}function hy(e,t){let{endEarly:n,tests:r,args:i,value:o,errors:a,sort:u,path:s}=e,l=(e=>{let t=!1;return(...n)=>{t||(t=!0,e(...n))}})(t),c=r.length;const f=[];if(a=a||[],!c)return a.length?l(new dy(a,o,s)):l(null,o);for(let d=0;d<r.length;d++){(0,r[d])(i,(function(e){if(e){if(!dy.isError(e))return l(e,o);if(n)return e.value=o,l(e,o);f.push(e)}if(--c<=0){if(f.length&&(u&&f.sort(u),a.length&&f.push(...a),a=f),a.length)return void l(new dy(a,o,s),o);l(null,o)}}))}}var py=xm,my=function(){try{var e=py(Object,"defineProperty");return e({},"",{}),e}catch(t){}}();var vy=function(e,t,n){"__proto__"==t&&my?my(e,t,{configurable:!0,enumerable:!0,value:n,writable:!0}):e[t]=n};var yy=function(e){return function(t,n,r){for(var i=-1,o=Object(t),a=r(t),u=a.length;u--;){var s=a[e?u:++i];if(!1===n(o[s],s,o))break}return t}}();var gy,by,wy,Ey,_y,xy,Sy,ky,Cy=function(e,t){for(var n=-1,r=Array(e);++n<e;)r[n]=t(n);return r},Oy={exports:{}};gy=Oy,wy=Dp,Ey=function(){return!1},_y=(by=Oy.exports)&&!by.nodeType&&by,xy=_y&&gy&&!gy.nodeType&&gy,Sy=xy&&xy.exports===_y?wy.Buffer:void 0,ky=(Sy?Sy.isBuffer:void 0)||Ey,gy.exports=ky;var Ty=Wp,jy=Qv,Py=Hp,Fy={};Fy["[object Float32Array]"]=Fy["[object Float64Array]"]=Fy["[object Int8Array]"]=Fy["[object Int16Array]"]=Fy["[object Int32Array]"]=Fy["[object Uint8Array]"]=Fy["[object Uint8ClampedArray]"]=Fy["[object Uint16Array]"]=Fy["[object Uint32Array]"]=!0,Fy["[object Arguments]"]=Fy["[object Array]"]=Fy["[object ArrayBuffer]"]=Fy["[object Boolean]"]=Fy["[object DataView]"]=Fy["[object Date]"]=Fy["[object Error]"]=Fy["[object Function]"]=Fy["[object Map]"]=Fy["[object Number]"]=Fy["[object Object]"]=Fy["[object RegExp]"]=Fy["[object Set]"]=Fy["[object String]"]=Fy["[object WeakMap]"]=!1;var Ay=function(e){return Py(e)&&jy(e.length)&&!!Fy[Ty(e)]};var Dy=function(e){return function(t){return e(t)}},Ny={exports:{}};!function(e,t){var n=Pp,r=t&&!t.nodeType&&t,i=r&&e&&!e.nodeType&&e,o=i&&i.exports===r&&n.process,a=function(){try{var e=i&&i.require&&i.require("util").types;return e||o&&o.binding&&o.binding("util")}catch(t){}}();e.exports=a}(Ny,Ny.exports);var My=Ay,Ly=Dy,zy=Ny.exports,Ry=zy&&zy.isTypedArray,Iy=Ry?Ly(Ry):My,Uy=Cy,$y=Wv,By=jp,Vy=Oy.exports,qy=Yv,Wy=Iy,Hy=Object.prototype.hasOwnProperty;var Yy=function(e,t){var n=By(e),r=!n&&$y(e),i=!n&&!r&&Vy(e),o=!n&&!r&&!i&&Wy(e),a=n||r||i||o,u=a?Uy(e.length,String):[],s=u.length;for(var l in e)!t&&!Hy.call(e,l)||a&&("length"==l||i&&("offset"==l||"parent"==l)||o&&("buffer"==l||"byteLength"==l||"byteOffset"==l)||qy(l,s))||u.push(l);return u},Qy=Object.prototype;var Gy=function(e){var t=e&&e.constructor;return e===("function"==typeof t&&t.prototype||Qy)};var Ky=function(e,t){return function(n){return e(t(n))}}(Object.keys,Object),Xy=Gy,Zy=Ky,Jy=Object.prototype.hasOwnProperty;var eg=om,tg=Qv;var ng=Yy,rg=function(e){if(!Xy(e))return Zy(e);var t=[];for(var n in Object(e))Jy.call(e,n)&&"constructor"!=n&&t.push(n);return t},ig=function(e){return null!=e&&tg(e.length)&&!eg(e)};var og=function(e){return ig(e)?ng(e):rg(e)},ag=yy,ug=og;var sg=function(e,t){return e&&ag(e,t,ug)},lg=nv;var cg=nv,fg=rv,dg=bv;var hg=nv,pg=function(){this.__data__=new lg,this.size=0},mg=function(e){var t=this.__data__,n=t.delete(e);return this.size=t.size,n},vg=function(e){return this.__data__.get(e)},yg=function(e){return this.__data__.has(e)},gg=function(e,t){var n=this.__data__;if(n instanceof cg){var r=n.__data__;if(!fg||r.length<199)return r.push([e,t]),this.size=++n.size,this;n=this.__data__=new dg(r)}return n.set(e,t),this.size=n.size,this};function bg(e){var t=this.__data__=new hg(e);this.size=t.size}bg.prototype.clear=pg,bg.prototype.delete=mg,bg.prototype.get=vg,bg.prototype.has=yg,bg.prototype.set=gg;var wg=bg;var Eg=bv,_g=function(e){return this.__data__.set(e,"__lodash_hash_undefined__"),this},xg=function(e){return this.__data__.has(e)};function Sg(e){var t=-1,n=null==e?0:e.length;for(this.__data__=new Eg;++t<n;)this.add(e[t])}Sg.prototype.add=Sg.prototype.push=_g,Sg.prototype.has=xg;var kg=Sg,Cg=function(e,t){for(var n=-1,r=null==e?0:e.length;++n<r;)if(t(e[n],n,e))return!0;return!1},Og=function(e,t){return e.has(t)};var Tg=function(e,t,n,r,i,o){var a=1&n,u=e.length,s=t.length;if(u!=s&&!(a&&s>u))return!1;var l=o.get(e),c=o.get(t);if(l&&c)return l==t&&c==e;var f=-1,d=!0,h=2&n?new kg:void 0;for(o.set(e,t),o.set(t,e);++f<u;){var p=e[f],m=t[f];if(r)var v=a?r(m,p,f,t,e,o):r(p,m,f,e,t,o);if(void 0!==v){if(v)continue;d=!1;break}if(h){if(!Cg(t,(function(e,t){if(!Og(h,t)&&(p===e||i(p,e,n,r,o)))return h.push(t)}))){d=!1;break}}else if(p!==m&&!i(p,m,n,r,o)){d=!1;break}}return o.delete(e),o.delete(t),d};var jg=Dp.Uint8Array,Pg=Bm,Fg=Tg,Ag=function(e){var t=-1,n=Array(e.size);return e.forEach((function(e,r){n[++t]=[r,e]})),n},Dg=function(e){var t=-1,n=Array(e.size);return e.forEach((function(e){n[++t]=e})),n},Ng=Np?Np.prototype:void 0,Mg=Ng?Ng.valueOf:void 0;var Lg=function(e,t,n,r,i,o,a){switch(n){case"[object DataView]":if(e.byteLength!=t.byteLength||e.byteOffset!=t.byteOffset)return!1;e=e.buffer,t=t.buffer;case"[object ArrayBuffer]":return!(e.byteLength!=t.byteLength||!o(new jg(e),new jg(t)));case"[object Boolean]":case"[object Date]":case"[object Number]":return Pg(+e,+t);case"[object Error]":return e.name==t.name&&e.message==t.message;case"[object RegExp]":case"[object String]":return e==t+"";case"[object Map]":var u=Ag;case"[object Set]":var s=1&r;if(u||(u=Dg),e.size!=t.size&&!s)return!1;var l=a.get(e);if(l)return l==t;r|=2,a.set(e,t);var c=Fg(u(e),u(t),r,i,o,a);return a.delete(e),c;case"[object Symbol]":if(Mg)return Mg.call(e)==Mg.call(t)}return!1};var zg=function(e,t){for(var n=-1,r=t.length,i=e.length;++n<r;)e[i+n]=t[n];return e},Rg=jp;var Ig=function(e,t,n){var r=t(e);return Rg(e)?r:zg(r,n(e))};var Ug=function(e,t){for(var n=-1,r=null==e?0:e.length,i=0,o=[];++n<r;){var a=e[n];t(a,n,e)&&(o[i++]=a)}return o},$g=function(){return[]},Bg=Object.prototype.propertyIsEnumerable,Vg=Object.getOwnPropertySymbols,qg=Ig,Wg=Vg?function(e){return null==e?[]:(e=Object(e),Ug(Vg(e),(function(t){return Bg.call(e,t)})))}:$g,Hg=og;var Yg=function(e){return qg(e,Hg,Wg)},Qg=Object.prototype.hasOwnProperty;var Gg=function(e,t,n,r,i,o){var a=1&n,u=Yg(e),s=u.length;if(s!=Yg(t).length&&!a)return!1;for(var l=s;l--;){var c=u[l];if(!(a?c in t:Qg.call(t,c)))return!1}var f=o.get(e),d=o.get(t);if(f&&d)return f==t&&d==e;var h=!0;o.set(e,t),o.set(t,e);for(var p=a;++l<s;){var m=e[c=u[l]],v=t[c];if(r)var y=a?r(v,m,c,t,e,o):r(m,v,c,e,t,o);if(!(void 0===y?m===v||i(m,v,n,r,o):y)){h=!1;break}p||(p="constructor"==c)}if(h&&!p){var g=e.constructor,b=t.constructor;g==b||!("constructor"in e)||!("constructor"in t)||"function"==typeof g&&g instanceof g&&"function"==typeof b&&b instanceof b||(h=!1)}return o.delete(e),o.delete(t),h},Kg=xm(Dp,"DataView"),Xg=rv,Zg=xm(Dp,"Promise"),Jg=xm(Dp,"Set"),eb=xm(Dp,"WeakMap"),tb=Wp,nb=cm,rb=nb(Kg),ib=nb(Xg),ob=nb(Zg),ab=nb(Jg),ub=nb(eb),sb=tb;(Kg&&"[object DataView]"!=sb(new Kg(new ArrayBuffer(1)))||Xg&&"[object Map]"!=sb(new Xg)||Zg&&"[object Promise]"!=sb(Zg.resolve())||Jg&&"[object Set]"!=sb(new Jg)||eb&&"[object WeakMap]"!=sb(new eb))&&(sb=function(e){var t=tb(e),n="[object Object]"==t?e.constructor:void 0,r=n?nb(n):"";if(r)switch(r){case rb:return"[object DataView]";case ib:return"[object Map]";case ob:return"[object Promise]";case ab:return"[object Set]";case ub:return"[object WeakMap]"}return t});var lb=wg,cb=Tg,fb=Lg,db=Gg,hb=sb,pb=jp,mb=Oy.exports,vb=Iy,yb=Object.prototype.hasOwnProperty;var gb=function(e,t,n,r,i,o){var a=pb(e),u=pb(t),s=a?"[object Array]":hb(e),l=u?"[object Array]":hb(t),c="[object Object]"==(s="[object Arguments]"==s?"[object Object]":s),f="[object Object]"==(l="[object Arguments]"==l?"[object Object]":l),d=s==l;if(d&&mb(e)){if(!mb(t))return!1;a=!0,c=!1}if(d&&!c)return o||(o=new lb),a||vb(e)?cb(e,t,n,r,i,o):fb(e,t,s,n,r,i,o);if(!(1&n)){var h=c&&yb.call(e,"__wrapped__"),p=f&&yb.call(t,"__wrapped__");if(h||p){var m=h?e.value():e,v=p?t.value():t;return o||(o=new lb),i(m,v,n,r,o)}}return!!d&&(o||(o=new lb),db(e,t,n,r,i,o))},bb=Hp;var wb=function e(t,n,r,i,o){return t===n||(null==t||null==n||!bb(t)&&!bb(n)?t!=t&&n!=n:gb(t,n,r,i,e,o))},Eb=wg,_b=wb;var xb=tm;var Sb=function(e){return e==e&&!xb(e)},kb=Sb,Cb=og;var Ob=function(e,t){return function(n){return null!=n&&(n[e]===t&&(void 0!==t||e in Object(n)))}},Tb=function(e,t,n,r){var i=n.length,o=i,a=!r;if(null==e)return!o;for(e=Object(e);i--;){var u=n[i];if(a&&u[2]?u[1]!==e[u[0]]:!(u[0]in e))return!1}for(;++i<o;){var s=(u=n[i])[0],l=e[s],c=u[1];if(a&&u[2]){if(void 0===l&&!(s in e))return!1}else{var f=new Eb;if(r)var d=r(l,c,s,e,t,f);if(!(void 0===d?_b(c,l,3,r,f):d))return!1}}return!0},jb=function(e){for(var t=Cb(e),n=t.length;n--;){var r=t[n],i=e[r];t[n]=[r,i,kb(i)]}return t},Pb=Ob;var Fb=zv,Ab=Kv;var Db=function(e,t){for(var n=0,r=(t=Fb(t,e)).length;null!=e&&n<r;)e=e[Ab(t[n++])];return n&&n==r?e:void 0},Nb=Db;var Mb=function(e,t){return null!=e&&t in Object(e)},Lb=ry;var zb=wb,Rb=function(e,t,n){var r=null==e?void 0:Nb(e,t);return void 0===r?n:r},Ib=function(e,t){return null!=e&&Lb(e,t,Mb)},Ub=em,$b=Sb,Bb=Ob,Vb=Kv;var qb=Db;var Wb=function(e){return function(t){return null==t?void 0:t[e]}},Hb=function(e){return function(t){return qb(t,e)}},Yb=em,Qb=Kv;var Gb=function(e){var t=jb(e);return 1==t.length&&t[0][2]?Pb(t[0][0],t[0][1]):function(n){return n===e||Tb(n,e,t)}},Kb=function(e,t){return Ub(e)&&$b(t)?Bb(Vb(e),t):function(n){var r=Rb(n,e);return void 0===r&&r===t?Ib(n,e):zb(t,r,3)}},Xb=function(e){return e},Zb=jp,Jb=function(e){return Yb(e)?Wb(Qb(e)):Hb(e)};var ew=function(e){return"function"==typeof e?e:null==e?Xb:"object"==typeof e?Zb(e)?Kb(e[0],e[1]):Gb(e):Jb(e)},tw=vy,nw=sg,rw=ew;var iw=function(e,t){var n={};return t=rw(t),nw(e,(function(e,r,i){tw(n,r,t(e,r,i))})),n};function ow(e){this._maxSize=e,this.clear()}ow.prototype.clear=function(){this._size=0,this._values=Object.create(null)},ow.prototype.get=function(e){return this._values[e]},ow.prototype.set=function(e,t){return this._size>=this._maxSize&&this.clear(),e in this._values||this._size++,this._values[e]=t};var aw=/[^.^\]^[]+|(?=\[\]|\.\.)/g,uw=/^\d+$/,sw=/^\d/,lw=/[~`!#$%\^&*+=\-\[\]\\';,/{}|\\":<>\?]/g,cw=/^\s*(['"]?)(.*?)(\1)\s*$/,fw=new ow(512),dw=new ow(512),hw=new ow(512),pw={Cache:ow,split:vw,normalizePath:mw,setter:function(e){var t=mw(e);return dw.get(e)||dw.set(e,(function(e,n){for(var r=0,i=t.length,o=e;r<i-1;){var a=t[r];if("__proto__"===a||"constructor"===a||"prototype"===a)return e;o=o[t[r++]]}o[t[r]]=n}))},getter:function(e,t){var n=mw(e);return hw.get(e)||hw.set(e,(function(e){for(var r=0,i=n.length;r<i;){if(null==e&&t)return;e=e[n[r++]]}return e}))},join:function(e){return e.reduce((function(e,t){return e+(yw(t)||uw.test(t)?"["+t+"]":(e?".":"")+t)}),"")},forEach:function(e,t,n){!function(e,t,n){var r,i,o,a,u=e.length;for(i=0;i<u;i++)(r=e[i])&&(gw(r)&&(r='"'+r+'"'),o=!(a=yw(r))&&/^\d+$/.test(r),t.call(n,r,a,o,i,e))}(Array.isArray(e)?e:vw(e),t,n)}};function mw(e){return fw.get(e)||fw.set(e,vw(e).map((function(e){return e.replace(cw,"$2")})))}function vw(e){return e.match(aw)}function yw(e){return"string"==typeof e&&e&&-1!==["'",'"'].indexOf(e.charAt(0))}function gw(e){return!yw(e)&&(function(e){return e.match(sw)&&!e.match(uw)}(e)||function(e){return lw.test(e)}(e))}const bw="$",ww=".";function Ew(e,t){return new _w(e,t)}class _w{constructor(e,t={}){if("string"!=typeof e)throw new TypeError("ref must be a string, got: "+e);if(this.key=e.trim(),""===e)throw new TypeError("ref must be a non-empty string");this.isContext=this.key[0]===bw,this.isValue=this.key[0]===ww,this.isSibling=!this.isContext&&!this.isValue;let n=this.isContext?bw:this.isValue?ww:"";this.path=this.key.slice(n.length),this.getter=this.path&&pw.getter(this.path,!0),this.map=t.map}getValue(e,t,n){let r=this.isContext?n:this.isValue?e:t;return this.getter&&(r=this.getter(r||{})),this.map&&(r=this.map(r)),r}cast(e,t){return this.getValue(e,null==t?void 0:t.parent,null==t?void 0:t.context)}resolve(){return this}describe(){return{type:"ref",key:this.key}}toString(){return`Ref(${this.key})`}static isRef(e){return e&&e.__isYupRef}}function xw(){return(xw=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}function Sw(e){function t(t,n){let{value:r,path:i="",label:o,options:a,originalValue:u,sync:s}=t,l=function(e,t){if(null==e)return{};var n,r,i={},o=Object.keys(e);for(r=0;r<o.length;r++)n=o[r],t.indexOf(n)>=0||(i[n]=e[n]);return i}(t,["value","path","label","options","originalValue","sync"]);const{name:c,test:f,params:d,message:h}=e;let{parent:p,context:m}=a;function v(e){return _w.isRef(e)?e.getValue(r,p,m):e}function y(e={}){const t=iw(xw({value:r,originalValue:u,label:o,path:e.path||i},d,e.params),v),n=new dy(dy.formatError(e.message||h,t),r,t.path,e.type||c);return n.params=t,n}let g,b=xw({path:i,parent:p,type:c,createError:y,resolve:v,options:a,originalValue:u},l);if(s){try{var w;if(g=f.call(b,r,b),"function"==typeof(null==(w=g)?void 0:w.then))throw new Error(`Validation test of type: "${b.type}" returned a Promise during a synchronous validate. This test will finish after the validate call has returned`)}catch(E){return void n(E)}dy.isError(g)?n(g):g?n(null,g):n(y())}else try{Promise.resolve(f.call(b,r,b)).then((e=>{dy.isError(e)?n(e):e?n(null,e):n(y())}))}catch(E){n(E)}}return t.OPTIONS=e,t}_w.prototype.__isYupRef=!0;function kw(e,t,n,r=n){let i,o,a;return t?(pw.forEach(t,((u,s,l)=>{let c=s?(e=>e.substr(0,e.length-1).substr(1))(u):u;if((e=e.resolve({context:r,parent:i,value:n})).innerType){let r=l?parseInt(c,10):0;if(n&&r>=n.length)throw new Error(`Yup.reach cannot resolve an array item at index: ${u}, in the path: ${t}. because there is no value at that index. `);i=n,n=n&&n[r],e=e.innerType}if(!l){if(!e.fields||!e.fields[c])throw new Error(`The schema does not contain the path: ${t}. (failed at: ${a} which is a type: "${e._type}")`);i=n,n=n&&n[c],e=e.fields[c]}o=c,a=s?"["+u+"]":"."+u})),{schema:e,parent:i,parentPath:o}):{parent:i,parentPath:t,schema:e}}class Cw{constructor(){this.list=new Set,this.refs=new Map}get size(){return this.list.size+this.refs.size}describe(){const e=[];for(const t of this.list)e.push(t);for(const[,t]of this.refs)e.push(t.describe());return e}toArray(){return Array.from(this.list).concat(Array.from(this.refs.values()))}add(e){_w.isRef(e)?this.refs.set(e.key,e):this.list.add(e)}delete(e){_w.isRef(e)?this.refs.delete(e.key):this.list.delete(e)}has(e,t){if(this.list.has(e))return!0;let n,r=this.refs.values();for(;n=r.next(),!n.done;)if(t(n.value)===e)return!0;return!1}clone(){const e=new Cw;return e.list=new Set(this.list),e.refs=new Map(this.refs),e}merge(e,t){const n=this.clone();return e.list.forEach((e=>n.add(e))),e.refs.forEach((e=>n.add(e))),t.list.forEach((e=>n.delete(e))),t.refs.forEach((e=>n.delete(e))),n}}function Ow(){return(Ow=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}class Tw{constructor(e){this.deps=[],this.conditions=[],this._whitelist=new Cw,this._blacklist=new Cw,this.exclusiveTests=Object.create(null),this.tests=[],this.transforms=[],this.withMutation((()=>{this.typeError(Ep.notType)})),this.type=(null==e?void 0:e.type)||"mixed",this.spec=Ow({strip:!1,strict:!1,abortEarly:!0,recursive:!0,nullable:!1,presence:"optional"},null==e?void 0:e.spec)}get _type(){return this.type}_typeCheck(e){return!0}clone(e){if(this._mutate)return e&&Object.assign(this.spec,e),this;const t=Object.create(Object.getPrototypeOf(this));return t.type=this.type,t._typeError=this._typeError,t._whitelistError=this._whitelistError,t._blacklistError=this._blacklistError,t._whitelist=this._whitelist.clone(),t._blacklist=this._blacklist.clone(),t.exclusiveTests=Ow({},this.exclusiveTests),t.deps=[...this.deps],t.conditions=[...this.conditions],t.tests=[...this.tests],t.transforms=[...this.transforms],t.spec=hp(Ow({},this.spec,e)),t}label(e){var t=this.clone();return t.spec.label=e,t}meta(...e){if(0===e.length)return this.spec.meta;let t=this.clone();return t.spec.meta=Object.assign(t.spec.meta||{},e[0]),t}withMutation(e){let t=this._mutate;this._mutate=!0;let n=e(this);return this._mutate=t,n}concat(e){if(!e||e===this)return this;if(e.type!==this.type&&"mixed"!==this.type)throw new TypeError(`You cannot \`concat()\` schema's of different types: ${this.type} and ${e.type}`);let t=this,n=e.clone();const r=Ow({},t.spec,n.spec);return n.spec=r,n._typeError||(n._typeError=t._typeError),n._whitelistError||(n._whitelistError=t._whitelistError),n._blacklistError||(n._blacklistError=t._blacklistError),n._whitelist=t._whitelist.merge(e._whitelist,e._blacklist),n._blacklist=t._blacklist.merge(e._blacklist,e._whitelist),n.tests=t.tests,n.exclusiveTests=t.exclusiveTests,n.withMutation((t=>{e.tests.forEach((e=>{t.test(e.OPTIONS)}))})),n}isType(e){return!(!this.spec.nullable||null!==e)||this._typeCheck(e)}resolve(e){let t=this;if(t.conditions.length){let n=t.conditions;t=t.clone(),t.conditions=[],t=n.reduce(((t,n)=>n.resolve(t,e)),t),t=t.resolve(e)}return t}cast(e,t={}){let n=this.resolve(Ow({value:e},t)),r=n._cast(e,t);if(void 0!==e&&!1!==t.assert&&!0!==n.isType(r)){let i=wp(e),o=wp(r);throw new TypeError(`The value of ${t.path||"field"} could not be cast to a value that satisfies the schema type: "${n._type}". \n\nattempted value: ${i} \n`+(o!==i?`result of cast: ${o}`:""))}return r}_cast(e,t){let n=void 0===e?e:this.transforms.reduce(((t,n)=>n.call(this,t,e,this)),e);return void 0===n&&(n=this.getDefault()),n}_validate(e,t={},n){let{sync:r,path:i,from:o=[],originalValue:a=e,strict:u=this.spec.strict,abortEarly:s=this.spec.abortEarly}=t,l=e;u||(l=this._cast(l,Ow({assert:!1},t)));let c={value:l,path:i,options:t,originalValue:a,schema:this,label:this.spec.label,sync:r,from:o},f=[];this._typeError&&f.push(this._typeError),this._whitelistError&&f.push(this._whitelistError),this._blacklistError&&f.push(this._blacklistError),hy({args:c,value:l,path:i,sync:r,tests:f,endEarly:s},(e=>{e?n(e,l):hy({tests:this.tests,args:c,path:i,sync:r,value:l,endEarly:s},n)}))}validate(e,t,n){let r=this.resolve(Ow({},t,{value:e}));return"function"==typeof n?r._validate(e,t,n):new Promise(((n,i)=>r._validate(e,t,((e,t)=>{e?i(e):n(t)}))))}validateSync(e,t){let n;return this.resolve(Ow({},t,{value:e}))._validate(e,Ow({},t,{sync:!0}),((e,t)=>{if(e)throw e;n=t})),n}isValid(e,t){return this.validate(e,t).then((()=>!0),(e=>{if(dy.isError(e))return!1;throw e}))}isValidSync(e,t){try{return this.validateSync(e,t),!0}catch(n){if(dy.isError(n))return!1;throw n}}_getDefault(){let e=this.spec.default;return null==e?e:"function"==typeof e?e.call(this):hp(e)}getDefault(e){return this.resolve(e||{})._getDefault()}default(e){if(0===arguments.length)return this._getDefault();return this.clone({default:e})}strict(e=!0){var t=this.clone();return t.spec.strict=e,t}_isPresent(e){return null!=e}defined(e=Ep.defined){return this.test({message:e,name:"defined",exclusive:!0,test:e=>void 0!==e})}required(e=Ep.required){return this.clone({presence:"required"}).withMutation((t=>t.test({message:e,name:"required",exclusive:!0,test(e){return this.schema._isPresent(e)}})))}notRequired(){var e=this.clone({presence:"optional"});return e.tests=e.tests.filter((e=>"required"!==e.OPTIONS.name)),e}nullable(e=!0){return this.clone({nullable:!1!==e})}transform(e){var t=this.clone();return t.transforms.push(e),t}test(...e){let t;if(t=1===e.length?"function"==typeof e[0]?{test:e[0]}:e[0]:2===e.length?{name:e[0],test:e[1]}:{name:e[0],message:e[1],test:e[2]},void 0===t.message&&(t.message=Ep.default),"function"!=typeof t.test)throw new TypeError("`test` is a required parameters");let n=this.clone(),r=Sw(t),i=t.exclusive||t.name&&!0===n.exclusiveTests[t.name];if(t.exclusive&&!t.name)throw new TypeError("Exclusive tests must provide a unique `name` identifying the test");return t.name&&(n.exclusiveTests[t.name]=!!t.exclusive),n.tests=n.tests.filter((e=>{if(e.OPTIONS.name===t.name){if(i)return!1;if(e.OPTIONS.test===r.OPTIONS.test)return!1}return!0})),n.tests.push(r),n}when(e,t){Array.isArray(e)||"string"==typeof e||(t=e,e=".");let n=this.clone(),r=ly(e).map((e=>new _w(e)));return r.forEach((e=>{e.isSibling&&n.deps.push(e.key)})),n.conditions.push(new sy(r,t)),n}typeError(e){var t=this.clone();return t._typeError=Sw({message:e,name:"typeError",test(e){return!(void 0!==e&&!this.schema.isType(e))||this.createError({params:{type:this.schema._type}})}}),t}oneOf(e,t=Ep.oneOf){var n=this.clone();return e.forEach((e=>{n._whitelist.add(e),n._blacklist.delete(e)})),n._whitelistError=Sw({message:t,name:"oneOf",test(e){if(void 0===e)return!0;let t=this.schema._whitelist;return!!t.has(e,this.resolve)||this.createError({params:{values:t.toArray().join(", ")}})}}),n}notOneOf(e,t=Ep.notOneOf){var n=this.clone();return e.forEach((e=>{n._blacklist.add(e),n._whitelist.delete(e)})),n._blacklistError=Sw({message:t,name:"notOneOf",test(e){let t=this.schema._blacklist;return!t.has(e,this.resolve)||this.createError({params:{values:t.toArray().join(", ")}})}}),n}strip(e=!0){let t=this.clone();return t.spec.strip=e,t}describe(){const e=this.clone(),{label:t,meta:n}=e.spec;return{meta:n,label:t,type:e.type,oneOf:e._whitelist.describe(),notOneOf:e._blacklist.describe(),tests:e.tests.map((e=>({name:e.OPTIONS.name,params:e.OPTIONS.params}))).filter(((e,t,n)=>n.findIndex((t=>t.name===e.name))===t))}}}Tw.prototype.__isYupSchema__=!0;for(const PT of["validate","validateSync"])Tw.prototype[`${PT}At`]=function(e,t,n={}){const{parent:r,parentPath:i,schema:o}=kw(this,e,t,n.context);return o[PT](r&&r[i],Ow({},n,{parent:r,path:e}))};for(const PT of["equals","is"])Tw.prototype[PT]=Tw.prototype.oneOf;for(const PT of["not","nope"])Tw.prototype[PT]=Tw.prototype.notOneOf;Tw.prototype.optional=Tw.prototype.notRequired;var jw=e=>null==e;function Pw(){return new Fw}class Fw extends Tw{constructor(){super({type:"boolean"}),this.withMutation((()=>{this.transform((function(e){if(!this.isType(e)){if(/^(true|1)$/i.test(String(e)))return!0;if(/^(false|0)$/i.test(String(e)))return!1}return e}))}))}_typeCheck(e){return e instanceof Boolean&&(e=e.valueOf()),"boolean"==typeof e}isTrue(e=Sp.isValue){return this.test({message:e,name:"is-value",exclusive:!0,params:{value:"true"},test:e=>jw(e)||!0===e})}isFalse(e=Sp.isValue){return this.test({message:e,name:"is-value",exclusive:!0,params:{value:"false"},test:e=>jw(e)||!1===e})}}Pw.prototype=Fw.prototype;let Aw=/^((([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_`{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+(\.([a-z]|\d|[!#\$%&'\*\+\-\/=\?\^_`{\|}~]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])+)*)|((\x22)((((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(([\x01-\x08\x0b\x0c\x0e-\x1f\x7f]|\x21|[\x23-\x5b]|[\x5d-\x7e]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(\\([\x01-\x09\x0b\x0c\x0d-\x7f]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF]))))*(((\x20|\x09)*(\x0d\x0a))?(\x20|\x09)+)?(\x22)))@((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))$/i,Dw=/^((https?|ftp):)?\/\/(((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:)*@)?(((\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5])\.(\d|[1-9]\d|1\d\d|2[0-4]\d|25[0-5]))|((([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|\d|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.)+(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])*([a-z]|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])))\.?)(:\d*)?)(\/((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)+(\/(([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)*)*)?)?(\?((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|[\uE000-\uF8FF]|\/|\?)*)?(\#((([a-z]|\d|-|\.|_|~|[\u00A0-\uD7FF\uF900-\uFDCF\uFDF0-\uFFEF])|(%[\da-f]{2})|[!\$&'\(\)\*\+,;=]|:|@)|\/|\?)*)?$/i,Nw=/^(?:[0-9a-f]{8}-[0-9a-f]{4}-[1-5][0-9a-f]{3}-[89ab][0-9a-f]{3}-[0-9a-f]{12}|00000000-0000-0000-0000-000000000000)$/i,Mw=e=>jw(e)||e===e.trim(),Lw={}.toString();function zw(){return new Rw}class Rw extends Tw{constructor(){super({type:"string"}),this.withMutation((()=>{this.transform((function(e){if(this.isType(e))return e;if(Array.isArray(e))return e;const t=null!=e&&e.toString?e.toString():e;return t===Lw?e:t}))}))}_typeCheck(e){return e instanceof String&&(e=e.valueOf()),"string"==typeof e}_isPresent(e){return super._isPresent(e)&&!!e.length}length(e,t=_p.length){return this.test({message:t,name:"length",exclusive:!0,params:{length:e},test(t){return jw(t)||t.length===this.resolve(e)}})}min(e,t=_p.min){return this.test({message:t,name:"min",exclusive:!0,params:{min:e},test(t){return jw(t)||t.length>=this.resolve(e)}})}max(e,t=_p.max){return this.test({name:"max",exclusive:!0,message:t,params:{max:e},test(t){return jw(t)||t.length<=this.resolve(e)}})}matches(e,t){let n,r,i=!1;return t&&("object"==typeof t?({excludeEmptyString:i=!1,message:n,name:r}=t):n=t),this.test({name:r||"matches",message:n||_p.matches,params:{regex:e},test:t=>jw(t)||""===t&&i||-1!==t.search(e)})}email(e=_p.email){return this.matches(Aw,{name:"email",message:e,excludeEmptyString:!0})}url(e=_p.url){return this.matches(Dw,{name:"url",message:e,excludeEmptyString:!0})}uuid(e=_p.uuid){return this.matches(Nw,{name:"uuid",message:e,excludeEmptyString:!1})}ensure(){return this.default("").transform((e=>null===e?"":e))}trim(e=_p.trim){return this.transform((e=>null!=e?e.trim():e)).test({message:e,name:"trim",test:Mw})}lowercase(e=_p.lowercase){return this.transform((e=>jw(e)?e:e.toLowerCase())).test({message:e,name:"string_case",exclusive:!0,test:e=>jw(e)||e===e.toLowerCase()})}uppercase(e=_p.uppercase){return this.transform((e=>jw(e)?e:e.toUpperCase())).test({message:e,name:"string_case",exclusive:!0,test:e=>jw(e)||e===e.toUpperCase()})}}zw.prototype=Rw.prototype;var Iw=/^(\d{4}|[+\-]\d{6})(?:-?(\d{2})(?:-?(\d{2}))?)?(?:[ T]?(\d{2}):?(\d{2})(?::?(\d{2})(?:[,\.](\d{1,}))?)?(?:(Z)|([+\-])(\d{2})(?::?(\d{2}))?)?)?$/;let Uw=new Date("");function $w(){return new Bw}class Bw extends Tw{constructor(){super({type:"date"}),this.withMutation((()=>{this.transform((function(e){return this.isType(e)?e:(e=function(e){var t,n,r=[1,4,5,6,7,10,11],i=0;if(n=Iw.exec(e)){for(var o,a=0;o=r[a];++a)n[o]=+n[o]||0;n[2]=(+n[2]||1)-1,n[3]=+n[3]||1,n[7]=n[7]?String(n[7]).substr(0,3):0,void 0!==n[8]&&""!==n[8]||void 0!==n[9]&&""!==n[9]?("Z"!==n[8]&&void 0!==n[9]&&(i=60*n[10]+n[11],"+"===n[9]&&(i=0-i)),t=Date.UTC(n[1],n[2],n[3],n[4],n[5]+i,n[6],n[7])):t=+new Date(n[1],n[2],n[3],n[4],n[5],n[6],n[7])}else t=Date.parse?Date.parse(e):NaN;return t}(e),isNaN(e)?Uw:new Date(e))}))}))}_typeCheck(e){return t=e,"[object Date]"===Object.prototype.toString.call(t)&&!isNaN(e.getTime());var t}prepareParam(e,t){let n;if(_w.isRef(e))n=e;else{let r=this.cast(e);if(!this._typeCheck(r))throw new TypeError(`\`${t}\` must be a Date or a value that can be \`cast()\` to a Date`);n=r}return n}min(e,t=xp.min){let n=this.prepareParam(e,"min");return this.test({message:t,name:"min",exclusive:!0,params:{min:e},test(e){return jw(e)||e>=this.resolve(n)}})}max(e,t=xp.max){var n=this.prepareParam(e,"max");return this.test({message:t,name:"max",exclusive:!0,params:{max:e},test(e){return jw(e)||e<=this.resolve(n)}})}}Bw.INVALID_DATE=Uw,$w.prototype=Bw.prototype,$w.INVALID_DATE=Uw;var Vw=function(e,t,n,r){var i=-1,o=null==e?0:e.length;for(r&&o&&(n=e[++i]);++i<o;)n=t(n,e[i],i,e);return n};var qw=function(e){return function(t){return null==e?void 0:e[t]}}({"À":"A","Á":"A","Â":"A","Ã":"A","Ä":"A","Å":"A","à":"a","á":"a","â":"a","ã":"a","ä":"a","å":"a","Ç":"C","ç":"c","Ð":"D","ð":"d","È":"E","É":"E","Ê":"E","Ë":"E","è":"e","é":"e","ê":"e","ë":"e","Ì":"I","Í":"I","Î":"I","Ï":"I","ì":"i","í":"i","î":"i","ï":"i","Ñ":"N","ñ":"n","Ò":"O","Ó":"O","Ô":"O","Õ":"O","Ö":"O","Ø":"O","ò":"o","ó":"o","ô":"o","õ":"o","ö":"o","ø":"o","Ù":"U","Ú":"U","Û":"U","Ü":"U","ù":"u","ú":"u","û":"u","ü":"u","Ý":"Y","ý":"y","ÿ":"y","Æ":"Ae","æ":"ae","Þ":"Th","þ":"th","ß":"ss","Ā":"A","Ă":"A","Ą":"A","ā":"a","ă":"a","ą":"a","Ć":"C","Ĉ":"C","Ċ":"C","Č":"C","ć":"c","ĉ":"c","ċ":"c","č":"c","Ď":"D","Đ":"D","ď":"d","đ":"d","Ē":"E","Ĕ":"E","Ė":"E","Ę":"E","Ě":"E","ē":"e","ĕ":"e","ė":"e","ę":"e","ě":"e","Ĝ":"G","Ğ":"G","Ġ":"G","Ģ":"G","ĝ":"g","ğ":"g","ġ":"g","ģ":"g","Ĥ":"H","Ħ":"H","ĥ":"h","ħ":"h","Ĩ":"I","Ī":"I","Ĭ":"I","Į":"I","İ":"I","ĩ":"i","ī":"i","ĭ":"i","į":"i","ı":"i","Ĵ":"J","ĵ":"j","Ķ":"K","ķ":"k","ĸ":"k","Ĺ":"L","Ļ":"L","Ľ":"L","Ŀ":"L","Ł":"L","ĺ":"l","ļ":"l","ľ":"l","ŀ":"l","ł":"l","Ń":"N","Ņ":"N","Ň":"N","Ŋ":"N","ń":"n","ņ":"n","ň":"n","ŋ":"n","Ō":"O","Ŏ":"O","Ő":"O","ō":"o","ŏ":"o","ő":"o","Ŕ":"R","Ŗ":"R","Ř":"R","ŕ":"r","ŗ":"r","ř":"r","Ś":"S","Ŝ":"S","Ş":"S","Š":"S","ś":"s","ŝ":"s","ş":"s","š":"s","Ţ":"T","Ť":"T","Ŧ":"T","ţ":"t","ť":"t","ŧ":"t","Ũ":"U","Ū":"U","Ŭ":"U","Ů":"U","Ű":"U","Ų":"U","ũ":"u","ū":"u","ŭ":"u","ů":"u","ű":"u","ų":"u","Ŵ":"W","ŵ":"w","Ŷ":"Y","ŷ":"y","Ÿ":"Y","Ź":"Z","Ż":"Z","Ž":"Z","ź":"z","ż":"z","ž":"z","Ĳ":"IJ","ĳ":"ij","Œ":"Oe","œ":"oe","ŉ":"'n","ſ":"s"}),Ww=Av,Hw=/[\xc0-\xd6\xd8-\xf6\xf8-\xff\u0100-\u017f]/g,Yw=RegExp("[\\u0300-\\u036f\\ufe20-\\ufe2f\\u20d0-\\u20ff]","g");var Qw=function(e){return(e=Ww(e))&&e.replace(Hw,qw).replace(Yw,"")},Gw=/[^\x00-\x2f\x3a-\x40\x5b-\x60\x7b-\x7f]+/g;var Kw=function(e){return e.match(Gw)||[]},Xw=/[a-z][A-Z]|[A-Z]{2}[a-z]|[0-9][a-zA-Z]|[a-zA-Z][0-9]|[^a-zA-Z0-9 ]/;var Zw=function(e){return Xw.test(e)},Jw="\\xac\\xb1\\xd7\\xf7\\x00-\\x2f\\x3a-\\x40\\x5b-\\x60\\x7b-\\xbf\\u2000-\\u206f \\t\\x0b\\f\\xa0\\ufeff\\n\\r\\u2028\\u2029\\u1680\\u180e\\u2000\\u2001\\u2002\\u2003\\u2004\\u2005\\u2006\\u2007\\u2008\\u2009\\u200a\\u202f\\u205f\\u3000",eE="["+Jw+"]",tE="\\d+",nE="[\\u2700-\\u27bf]",rE="[a-z\\xdf-\\xf6\\xf8-\\xff]",iE="[^\\ud800-\\udfff"+Jw+tE+"\\u2700-\\u27bfa-z\\xdf-\\xf6\\xf8-\\xffA-Z\\xc0-\\xd6\\xd8-\\xde]",oE="(?:\\ud83c[\\udde6-\\uddff]){2}",aE="[\\ud800-\\udbff][\\udc00-\\udfff]",uE="[A-Z\\xc0-\\xd6\\xd8-\\xde]",sE="(?:"+rE+"|"+iE+")",lE="(?:"+uE+"|"+iE+")",cE="(?:[\\u0300-\\u036f\\ufe20-\\ufe2f\\u20d0-\\u20ff]|\\ud83c[\\udffb-\\udfff])?",fE="[\\ufe0e\\ufe0f]?"+cE+("(?:\\u200d(?:"+["[^\\ud800-\\udfff]",oE,aE].join("|")+")[\\ufe0e\\ufe0f]?"+cE+")*"),dE="(?:"+[nE,oE,aE].join("|")+")"+fE,hE=RegExp([uE+"?"+rE+"+(?:['’](?:d|ll|m|re|s|t|ve))?(?="+[eE,uE,"$"].join("|")+")",lE+"+(?:['’](?:D|LL|M|RE|S|T|VE))?(?="+[eE,uE+sE,"$"].join("|")+")",uE+"?"+sE+"+(?:['’](?:d|ll|m|re|s|t|ve))?",uE+"+(?:['’](?:D|LL|M|RE|S|T|VE))?","\\d*(?:1ST|2ND|3RD|(?![123])\\dTH)(?=\\b|[a-z_])","\\d*(?:1st|2nd|3rd|(?![123])\\dth)(?=\\b|[A-Z_])",tE,dE].join("|"),"g");var pE=Kw,mE=Zw,vE=Av,yE=function(e){return e.match(hE)||[]};var gE=Vw,bE=Qw,wE=function(e,t,n){return e=vE(e),void 0===(t=n?void 0:t)?mE(e)?yE(e):pE(e):e.match(t)||[]},EE=RegExp("['’]","g");var _E=function(e){return function(t){return gE(wE(bE(t).replace(EE,"")),e,"")}},xE=_E((function(e,t,n){return e+(n?"_":"")+t.toLowerCase()}));var SE=function(e,t,n){var r=-1,i=e.length;t<0&&(t=-t>i?0:i+t),(n=n>i?i:n)<0&&(n+=i),i=t>n?0:n-t>>>0,t>>>=0;for(var o=Array(i);++r<i;)o[r]=e[r+t];return o};var kE=function(e,t,n){var r=e.length;return n=void 0===n?r:n,!t&&n>=r?e:SE(e,t,n)},CE=RegExp("[\\u200d\\ud800-\\udfff\\u0300-\\u036f\\ufe20-\\ufe2f\\u20d0-\\u20ff\\ufe0e\\ufe0f]");var OE=function(e){return CE.test(e)};var TE=function(e){return e.split("")},jE="[\\ud800-\\udfff]",PE="[\\u0300-\\u036f\\ufe20-\\ufe2f\\u20d0-\\u20ff]",FE="\\ud83c[\\udffb-\\udfff]",AE="[^\\ud800-\\udfff]",DE="(?:\\ud83c[\\udde6-\\uddff]){2}",NE="[\\ud800-\\udbff][\\udc00-\\udfff]",ME="(?:"+PE+"|"+FE+")"+"?",LE="[\\ufe0e\\ufe0f]?"+ME+("(?:\\u200d(?:"+[AE,DE,NE].join("|")+")[\\ufe0e\\ufe0f]?"+ME+")*"),zE="(?:"+[AE+PE+"?",PE,DE,NE,jE].join("|")+")",RE=RegExp(FE+"(?="+FE+")|"+zE+LE,"g");var IE=TE,UE=OE,$E=function(e){return e.match(RE)||[]};var BE=kE,VE=OE,qE=function(e){return UE(e)?$E(e):IE(e)},WE=Av;var HE=function(e){return function(t){t=WE(t);var n=VE(t)?qE(t):void 0,r=n?n[0]:t.charAt(0),i=n?BE(n,1).join(""):t.slice(1);return r[e]()+i}}("toUpperCase"),YE=Av,QE=HE;var GE=function(e){return QE(YE(e).toLowerCase())},KE=_E((function(e,t,n){return t=t.toLowerCase(),e+(n?GE(t):t)})),XE=vy,ZE=sg,JE=ew;var e_=function(e,t){var n={};return t=JE(t),ZE(e,(function(e,r,i){XE(n,t(e,r,i),e)})),n},t_={exports:{}};function n_(e,t){var n=e.length,r=new Array(n),i={},o=n,a=function(e){for(var t=new Map,n=0,r=e.length;n<r;n++){var i=e[n];t.has(i[0])||t.set(i[0],new Set),t.has(i[1])||t.set(i[1],new Set),t.get(i[0]).add(i[1])}return t}(t),u=function(e){for(var t=new Map,n=0,r=e.length;n<r;n++)t.set(e[n],n);return t}(e);for(t.forEach((function(e){if(!u.has(e[0])||!u.has(e[1]))throw new Error("Unknown node. There is an unknown node in the supplied edges.")}));o--;)i[o]||s(e[o],o,new Set);return r;function s(e,t,o){if(o.has(e)){var l;try{l=", node was:"+JSON.stringify(e)}catch(d){l=""}throw new Error("Cyclic dependency"+l)}if(!u.has(e))throw new Error("Found unknown node. Make sure to provided all involved nodes. Unknown node: "+JSON.stringify(e));if(!i[t]){i[t]=!0;var c=a.get(e)||new Set;if(t=(c=Array.from(c)).length){o.add(e);do{var f=c[--t];s(f,u.get(f),o)}while(t);o.delete(e)}r[--n]=e}}}t_.exports=function(e){return n_(function(e){for(var t=new Set,n=0,r=e.length;n<r;n++){var i=e[n];t.add(i[0]),t.add(i[1])}return Array.from(t)}(e),e)},t_.exports.array=n_;var r_=t_.exports;function i_(e,t){let n=1/0;return e.some(((e,r)=>{var i;if(-1!==(null==(i=t.path)?void 0:i.indexOf(e)))return n=r,!0})),n}function o_(e){return(t,n)=>i_(e,t)-i_(e,n)}function a_(){return(a_=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}let u_=e=>"[object Object]"===Object.prototype.toString.call(e);const s_=o_([]);class l_ extends Tw{constructor(e){super({type:"object"}),this.fields=Object.create(null),this._sortErrors=s_,this._nodes=[],this._excludedEdges=[],this.withMutation((()=>{this.transform((function(e){if("string"==typeof e)try{e=JSON.parse(e)}catch(t){e=null}return this.isType(e)?e:null})),e&&this.shape(e)}))}_typeCheck(e){return u_(e)||"function"==typeof e}_cast(e,t={}){var n;let r=super._cast(e,t);if(void 0===r)return this.getDefault();if(!this._typeCheck(r))return r;let i=this.fields,o=null!=(n=t.stripUnknown)?n:this.spec.noUnknown,a=this._nodes.concat(Object.keys(r).filter((e=>-1===this._nodes.indexOf(e)))),u={},s=a_({},t,{parent:u,__validating:t.__validating||!1}),l=!1;for(const c of a){let e=i[c],n=ay(r,c);if(e){let n,i=r[c];s.path=(t.path?`${t.path}.`:"")+c,e=e.resolve({value:i,context:t.context,parent:u});let o="spec"in e?e.spec:void 0,a=null==o?void 0:o.strict;if(null==o?void 0:o.strip){l=l||c in r;continue}n=t.__validating&&a?r[c]:e.cast(r[c],s),void 0!==n&&(u[c]=n)}else n&&!o&&(u[c]=r[c]);u[c]!==r[c]&&(l=!0)}return l?u:r}_validate(e,t={},n){let r=[],{sync:i,from:o=[],originalValue:a=e,abortEarly:u=this.spec.abortEarly,recursive:s=this.spec.recursive}=t;o=[{schema:this,value:a},...o],t.__validating=!0,t.originalValue=a,t.from=o,super._validate(e,t,((e,l)=>{if(e){if(!dy.isError(e)||u)return void n(e,l);r.push(e)}if(!s||!u_(l))return void n(r[0]||null,l);a=a||l;let c=this._nodes.map((e=>(n,r)=>{let i=-1===e.indexOf(".")?(t.path?`${t.path}.`:"")+e:`${t.path||""}["${e}"]`,u=this.fields[e];u&&"validate"in u?u.validate(l[e],a_({},t,{path:i,from:o,strict:!0,parent:l,originalValue:a[e]}),r):r(null)}));hy({sync:i,tests:c,value:l,errors:r,endEarly:u,sort:this._sortErrors,path:t.path},n)}))}clone(e){const t=super.clone(e);return t.fields=a_({},this.fields),t._nodes=this._nodes,t._excludedEdges=this._excludedEdges,t._sortErrors=this._sortErrors,t}concat(e){let t=super.concat(e),n=t.fields;for(let[r,i]of Object.entries(this.fields)){const e=n[r];void 0===e?n[r]=i:e instanceof Tw&&i instanceof Tw&&(n[r]=i.concat(e))}return t.withMutation((()=>t.shape(n)))}getDefaultFromShape(){let e={};return this._nodes.forEach((t=>{const n=this.fields[t];e[t]="default"in n?n.getDefault():void 0})),e}_getDefault(){return"default"in this.spec?super._getDefault():this._nodes.length?this.getDefaultFromShape():void 0}shape(e,t=[]){let n=this.clone(),r=Object.assign(n.fields,e);if(n.fields=r,n._sortErrors=o_(Object.keys(r)),t.length){Array.isArray(t[0])||(t=[t]);let e=t.map((([e,t])=>`${e}-${t}`));n._excludedEdges=n._excludedEdges.concat(e)}return n._nodes=function(e,t=[]){let n=[],r=[];function i(e,i){var o=pw.split(e)[0];~r.indexOf(o)||r.push(o),~t.indexOf(`${i}-${o}`)||n.push([i,o])}for(const o in e)if(ay(e,o)){let t=e[o];~r.indexOf(o)||r.push(o),_w.isRef(t)&&t.isSibling?i(t.path,o):uy(t)&&"deps"in t&&t.deps.forEach((e=>i(e,o)))}return r_.array(r,n).reverse()}(r,n._excludedEdges),n}pick(e){const t={};for(const n of e)this.fields[n]&&(t[n]=this.fields[n]);return this.clone().withMutation((e=>(e.fields={},e.shape(t))))}omit(e){const t=this.clone(),n=t.fields;t.fields={};for(const r of e)delete n[r];return t.withMutation((()=>t.shape(n)))}from(e,t,n){let r=pw.getter(e,!0);return this.transform((i=>{if(null==i)return i;let o=i;return ay(i,e)&&(o=a_({},i),n||delete o[e],o[t]=r(i)),o}))}noUnknown(e=!0,t=kp.noUnknown){"string"==typeof e&&(t=e,e=!0);let n=this.test({name:"noUnknown",exclusive:!0,message:t,test(t){if(null==t)return!0;const n=function(e,t){let n=Object.keys(e.fields);return Object.keys(t).filter((e=>-1===n.indexOf(e)))}(this.schema,t);return!e||0===n.length||this.createError({params:{unknown:n.join(", ")}})}});return n.spec.noUnknown=e,n}unknown(e=!0,t=kp.noUnknown){return this.noUnknown(!e,t)}transformKeys(e){return this.transform((t=>t&&e_(t,((t,n)=>e(n)))))}camelCase(){return this.transformKeys(KE)}snakeCase(){return this.transformKeys(xE)}constantCase(){return this.transformKeys((e=>xE(e).toUpperCase()))}describe(){let e=super.describe();return e.fields=iw(this.fields,(e=>e.describe())),e}}function c_(e){return new l_(e)}function f_(){return(f_=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}function d_(e){return new h_(e)}c_.prototype=l_.prototype;class h_ extends Tw{constructor(e){super({type:"array"}),this.innerType=e,this.withMutation((()=>{this.transform((function(e){if("string"==typeof e)try{e=JSON.parse(e)}catch(t){e=null}return this.isType(e)?e:null}))}))}_typeCheck(e){return Array.isArray(e)}get _subType(){return this.innerType}_cast(e,t){const n=super._cast(e,t);if(!this._typeCheck(n)||!this.innerType)return n;let r=!1;const i=n.map(((e,n)=>{const i=this.innerType.cast(e,f_({},t,{path:`${t.path||""}[${n}]`}));return i!==e&&(r=!0),i}));return r?i:n}_validate(e,t={},n){var r,i;let o=[],a=t.sync,u=t.path,s=this.innerType,l=null!=(r=t.abortEarly)?r:this.spec.abortEarly,c=null!=(i=t.recursive)?i:this.spec.recursive,f=null!=t.originalValue?t.originalValue:e;super._validate(e,t,((e,r)=>{if(e){if(!dy.isError(e)||l)return void n(e,r);o.push(e)}if(!c||!s||!this._typeCheck(r))return void n(o[0]||null,r);f=f||r;let i=new Array(r.length);for(let n=0;n<r.length;n++){let e=r[n],o=`${t.path||""}[${n}]`,a=f_({},t,{path:o,strict:!0,parent:r,index:n,originalValue:f[n]});i[n]=(t,n)=>s.validate(e,a,n)}hy({sync:a,path:u,value:r,errors:o,endEarly:l,tests:i},n)}))}clone(e){const t=super.clone(e);return t.innerType=this.innerType,t}concat(e){let t=super.concat(e);return t.innerType=this.innerType,e.innerType&&(t.innerType=t.innerType?t.innerType.concat(e.innerType):e.innerType),t}of(e){let t=this.clone();if(!uy(e))throw new TypeError("`array.of()` sub-schema must be a valid yup schema not: "+wp(e));return t.innerType=e,t}length(e,t=Cp.length){return this.test({message:t,name:"length",exclusive:!0,params:{length:e},test(t){return jw(t)||t.length===this.resolve(e)}})}min(e,t){return t=t||Cp.min,this.test({message:t,name:"min",exclusive:!0,params:{min:e},test(t){return jw(t)||t.length>=this.resolve(e)}})}max(e,t){return t=t||Cp.max,this.test({message:t,name:"max",exclusive:!0,params:{max:e},test(t){return jw(t)||t.length<=this.resolve(e)}})}ensure(){return this.default((()=>[])).transform(((e,t)=>this._typeCheck(e)?e:null==t?[]:[].concat(t)))}compact(e){let t=e?(t,n,r)=>!e(t,n,r):e=>!!e;return this.transform((e=>null!=e?e.filter(t):e))}describe(){let e=super.describe();return this.innerType&&(e.innerType=this.innerType.describe()),e}nullable(e=!0){return super.nullable(e)}defined(){return super.defined()}required(e){return super.required(e)}}d_.prototype=h_.prototype;
/*! DSFR v1.1.0 | SPDX-License-Identifier: MIT | License-Filename: LICENCE.md | restricted use (see terms and conditions) */
const p_=window.dsfr||{core:{}};window.dsfr=p_;const m_=e=>`fr-${e}`;m_.selector=(e,t)=>(void 0===t&&(t="."),`${t}${m_(e)}`),(m_.attr=(e,t,n)=>`data-${m_(e)}`).selector=(e,t)=>{let n=m_.attr(e);return void 0!==t&&(n+=`="${t}"`),`[${n}]`},m_.event=e=>`dsfr.${e}`;const v_=(e,t,n)=>{"."===t.charAt(0)&&(t=t.substr(1));const r=e.className.split(" "),i=r.indexOf(t);!0===n?i>-1&&r.splice(i,1):-1===i&&r.push(t),e.className=r.join(" ")},y_=(e,t)=>v_(e,t),g_=(e,t)=>v_(e,t,!0);class b_{constructor(){this.closures=[],this.nexts=[],this.rendering=this.render.bind(this),this.render()}add(e){return this.closures.push(e),()=>{const t=this.closures.indexOf(e);-1!==t&&this.closures.splice(t,1)}}next(e,t){t=void 0===t?0:t-1,void 0===this.nexts[t]&&(this.nexts[t]=[]),this.nexts[t].push(e)}render(){window.requestAnimationFrame(this.rendering);for(const t of this.closures)t.call();const e=this.nexts.shift();if(e)for(const t of e)t.call()}}const w_=new class{constructor(){this.renderer=new b_}register(e,t){}start(){}stop(){}};class E_{constructor(e,t){this.selector=e,this.builders=t,this.instances=[],"loading"!==document.readyState?window.requestAnimationFrame(this.start.bind(this)):document.addEventListener("DOMContentLoaded",this.start.bind(this))}start(){if(!(this.instances.length>0)&&document.querySelectorAll(this.selector).length>0)for(let e=0;e<this.builders.length;e++)this.instances.push(this.builders[e]())}}const __={},x_={};let S_=0;const k_=e=>{for(const n in x_)if(x_[n]===e)return n;S_++;const t=S_;return x_[t]=e,t};class C_{constructor(e,t,n){const r=k_(e);__[r]||(__[r]=[]),__[r].push(this),this.element=e,this.id=e.id,this._isRendering=!1,this._isResizing=!1,this.listeners={},this.isResizing=t,this.isRendering=n}dispatch(e,t){const n=new CustomEvent(e,t);this.element.dispatchEvent(n)}listen(e,t){this.listeners[e]||(this.listeners[e]=[]),this.listeners[e].indexOf(t)>-1||(this.listeners[e].push(t),this.element.addEventListener(e,t))}unlisten(e,t){if(e)if(t){if(!this.listeners[e])return;const n=this.listeners[e].indexOf(t);n>-1&&this.listeners[e].splice(n,1),this.element.removeEventListener(t)}else{if(!this.listeners[e])return;for(const t of this.listeners[e])this.element.removeEventListener(t);this.listeners[e].length=0}else for(const n in this.listeners)this.unlisten(n)}get isRendering(){return this._isRendering}set isRendering(e){this._isRendering!==e&&(this._isRendering=e)}render(){}get isResizing(){return this._isResizing}set isResizing(e){this._isResizing!==e&&(this._isResizing=e)}resize(){}destroy(){}static getInstances(e,t){const n=k_(e);return __[n]?t?__[n].filter((e=>e instanceof t)):__[n]:null}}const O_=m_.attr("group"),T_=[];class j_{constructor(e,t){this.id=e,this.element=t,this.members=[],this._index=-1,this._current=null,T_.push(this)}static getGroupById(e){for(const t of T_)if(t.constructor===this&&t.id===e)return t;return new this(e)}static getGroupByElement(e){for(const t of T_)if(t.element===e)return t;return new this(!1,e)}static groupById(e,t){const n=e.element.getAttribute(O_);null!==n&&t.getGroupById(n).add(e)}static groupByParent(e,t,n){if(void 0===n&&(n=t.selector),""===n)return;let r=e.element.parentElement;for(;r;){if(r.classList.contains(e.constructor.selector))return;if(r.classList.contains(n))return void t.getGroupByElement(r).add(e);r=r.parentElement}}static get selector(){return""}add(e){if(-1===this.members.indexOf(e))switch(this.members.push(e),e.setGroup(this),!0){case null!==this.current:case!(e.disclosed||e.primary&&e.primary.disclosed):e.disclosed=!1;break;default:this._current=e,this._index=this.members.indexOf(e),e.disclosed=!0}}get length(){return this.members.length}get index(){return this._index}set index(e){e<-1||e>=this.length||this._index===e||(null!==this.current&&this.current.conceal(!0,!0),this._index=e,this._current=this._index>-1?this.members[this._index]:null,null!==this.current&&this.current.disclose(!0),this.apply())}get current(){return this._current}set current(e){this.index=this.members.indexOf(e)}get hasFocus(){return void 0===this.current?null:this.current.hasFocus}apply(){}}class P_{constructor(e,t){this.element=e,this.disclosure=t,this.hasAttribute=this.element.hasAttribute(this.disclosure.attributeName),this.element.addEventListener("click",this.click.bind(this)),this.observer=new MutationObserver(this.mutate.bind(this)),this.observe()}observe(){this.observer.observe(this.element,{attributes:!0})}click(e){this.disclosure.change(this.hasAttribute)}mutate(e){e.forEach((e=>{"attributes"===e.type&&e.attributeName===this.disclosure.attributeName&&this.disclosure.change(this.disclosed)}))}apply(e){this.hasAttribute&&(this.observer&&this.observer.disconnect(),this.element.setAttribute(this.disclosure.attributeName,e),this.observer&&this.observe())}get disclosed(){return"true"===this.element.getAttribute(this.disclosure.attributeName)}get hasFocus(){return this.element===document.activeElement}}const F_=m_.event("DISCLOSE"),A_=m_.event("CONCEAL"),D_=[];class N_ extends C_{constructor(e){super(e),this.buttons=[],this._selector=this.constructor.selector,this.modifier=this._selector+"--"+this.type.id,this.attributeName=this.type.ariaState?"aria-"+this.type.id:m_.attr(this.type.id),this.pristine=!0;const t=document.querySelectorAll(this.type.ariaControls?`[aria-controls="${this.id}"]`:m_.attr.selector("controls",this.id));if(t.length>0)for(let n=0;n<t.length;n++)this.addButton(t[n]);this.disclosed=this.primary&&this.primary.disclosed,this.gather()}gather(){this.group||(j_.groupById(this,this.GroupConstructor),j_.groupByParent(this,this.GroupConstructor))}static build(e){const t=Array.prototype.slice.call(e.querySelectorAll(`.${this.selector}`));for(const n of t)D_.push(new this(n))}get type(){return this.constructor.type}static get type(){return null}static get selector(){return""}addButton(e){const t=this.buttonFactory(e);t.hasAttribute&&(void 0===this.primary?this.primary=t:t.apply(this.primary.disclosed)),this.buttons.push(t)}get GroupConstructor(){return j_}buttonFactory(e){return new P_(e,this)}disclose(e){return!this.disclosed&&(this.pristine=!1,this.disclosed=!0,e||void 0===this.group||(this.group.current=this),!0)}conceal(e,t){if(!this.disclosed)return!1;this.pristine=!1,this.disclosed=!1,t||this.focus(),e||void 0===this.group||(this.group.current=null);for(const n of D_)n!==this&&this.element.contains(n.element)&&n.reset();return!0}get disclosed(){return this._disclosed}set disclosed(e){if(this._disclosed!==e){this.dispatch(e?F_:A_,this.type),this._disclosed=e,e?y_(this.element,this.modifier):g_(this.element,this.modifier);for(let t=0;t<this.buttons.length;t++)this.buttons[t].apply(e)}}reset(){}change(e){if(this.constructor.type.canConceal)switch(!0){case!e:case this.disclosed:this.conceal();break;default:this.disclose()}else this.disclose()}setGroup(e){this.group=e}get buttonHasFocus(){return!!this.buttons.some((e=>e.hasFocus))}get hasFocus(){return this.element===document.activeElement||this.element.querySelectorAll(":focus").length>0||this.buttonHasFocus}focus(){for(let e=0;e<this.buttons.length;e++){const t=this.buttons[e];if(t.hasAttribute)return void t.element.focus()}}}N_.DISCLOSE_EVENT=F_,N_.CONCEAL_EVENT=A_;const M_={expand:{id:"expanded",ariaState:!0,ariaControls:!0,canConceal:!0},select:{id:"selected",ariaState:!0,ariaControls:!0,canConceal:!1},opened:{id:"opened",ariaState:!1,ariaControls:!0,canConceal:!0}};class L_{constructor(e){this.element=e,this.collections={}}_add(e,t){void 0===this.collections[e]&&(this.collections[e]=new z_(e,this.element)),this.collections[e].add(t)}down(e,t,n,r){this._add("down",new R_(e,t,n,r))}up(e,t,n,r){this._add("up",new R_(e,t,n,r))}dispose(){for(const e of this.collections)e.dispose();this.types=null}}class z_{constructor(e,t){this.type=e,this.element=t,this.actions=[],this.binding=this.handle.bind(this),this.element.addEventListener("key"+e,this.binding)}add(e){this.actions.push(e)}handle(e){for(const t of this.actions)t.handle(e)}dispose(){this.element.removeEventListener("key"+this.type,this.binding),this.actions=null}}class R_{constructor(e,t,n,r){this.key=e,this.closure=t,this.preventDefault=!0===n,this.stopPropagation=!0===r}handle(e){e.keyCode===this.key&&(this.closure(e),this.preventDefault&&e.preventDefault(),this.stopPropagation&&e.stopPropagation())}}L_.TAB=9,L_.ESCAPE=27,L_.END=35,L_.HOME=36,L_.LEFT=37,L_.UP=38,L_.RIGHT=39,L_.DOWN=40;const I_=m_("collapse"),U_=[],$_={};class B_ extends N_{constructor(e){super(e),U_.push(this),this.requesting=this.request.bind(this),e.addEventListener("transitionend",this.transitionend.bind(this)),this.disclosed&&this.unbound()}gatherByAscendants(){if(!this.group)for(const e in $_){let t=this.element.parentElement;for(;t;){if(t.classList.contains(e))return void("string"==typeof $_[e]?j_.groupByParent(this,j_,$_[e]):j_.groupByParent(this,$_[e]));t=t.parentElement}}}gather(){this.gatherByAscendants(),super.gather()}static get type(){return M_.expand}static get selector(){return I_}static register(e,t){$_[e]=t;for(const n of U_)n.gatherByAscendants()}transitionend(e){this.disclosed||(this.element.style.maxHeight="")}unbound(){this.element.style.maxHeight="none"}disclose(e){this.disclosed||(this.unbound(),this.adjust(),this.requested=()=>{super.disclose(e)},window.requestAnimationFrame(this.requesting))}conceal(e,t){this.disclosed&&(this.adjust(),this.requested=()=>{super.conceal(e,t)},window.requestAnimationFrame(this.requesting))}request(){this.requested&&this.requested(),this.requested=null}adjust(){this.element.style.setProperty("--collapser","none");const e=this.element.offsetHeight;this.element.style.setProperty("--collapse",-e+"px"),this.element.style.setProperty("--collapser","")}reset(){this.pristine||(this.disclosed=!1)}}p_.core.ns=m_,p_.core.addClass=y_,p_.core.removeClass=g_,p_.core.engine=w_,p_.core.Instance=C_,p_.core.Initializer=E_,p_.core.Disclosure=N_,p_.core.DisclosureButton=P_,p_.core.DisclosuresGroup=j_,p_.core.DISCLOSURE_TYPES=M_,p_.KeyListener=L_,p_.Collapse=B_,p_.Equisized=class{constructor(e,t){this.selector=e,this.group=t,this.elements=this.group.querySelectorAll(this.selector),this.maxWidth=0,this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),window.addEventListener("load",this.changing)}change(){this.reset();for(let e=0;e<this.elements.length;e++){const t=this._getWidth(this.elements[e]);t>this.maxWidth&&(this.maxWidth=t)}this.apply()}apply(){for(let e=0;e<this.elements.length;e++)this.elements[e].style.width=this.maxWidth+1+"px"}reset(){for(let e=0;e<this.elements.length;e++)this.elements[e].style.width="auto";this.maxWidth=0}_getWidth(e){let t=e.offsetWidth;const n=getComputedStyle(e);return t+=parseInt(n.marginLeft)+parseInt(n.marginRight),t}},new E_(`.${I_}`,[()=>{B_.build(document)}]);const V_=p_.core.ns("accordions-group"),q_=p_.core.ns("accordion");class W_ extends p_.core.DisclosuresGroup{static get selector(){return V_}}p_.AccordionsGroup=W_,p_.Collapse.register(q_,W_);const H_=`${p_.core.ns.selector("breadcrumb")} ${p_.core.ns.selector("collapse")}`;class Y_ extends p_.core.Instance{constructor(e){super(e),this.collapse=p_.core.Instance.getInstances(e,p_.Collapse)[0],this.links=[...this.element.querySelectorAll("a[href]")],this.count=0,this.links.length&&(this.listen(p_.core.Disclosure.DISCLOSE_EVENT,this.focus.bind(this)),this.resizing=this.resize.bind(this),window.addEventListener("resize",this.resizing))}focus(){this.links[0].focus(),p_.core.engine.renderer.next((()=>{this.verify()}))}verify(){this.count++,this.count>100||document.activeElement!==this.links[0]&&this.focus()}resize(){window.matchMedia("(min-width: 48em)").matches?this.collapse.buttons[0]===document.activeElement&&this.links.focus():this.links.indexOf(document.activeElement)>-1&&this.collapse.focus()}}new p_.core.Initializer(H_,[()=>{const e=[],t=document.querySelectorAll(H_);for(let n=0;n<t.length;n++)e.push(new Y_(t[n]))}]);const Q_=p_.core.ns.selector("btn"),G_=p_.core.ns.selector("btns-group"),K_=p_.core.ns.selector("btns-group--equisized");new p_.core.Initializer(G_,[()=>{const e=document.querySelectorAll(K_),t=[];for(let n=0;n<e.length;n++)t.push(new p_.Equisized(Q_,e[n]))}]);const X_=p_.core.ns.selector("modal"),Z_=p_.core.ns("modal"),J_=p_.core.ns("no-scroll"),ex=p_.core.ns("scroll-shadow"),tx=p_.core.ns.selector("modal__body"),nx=['[tabindex="0"]',"a[href]","button:not([disabled])","input:not([disabled])","select:not([disabled])","textarea:not([disabled])","audio[controls]","video[controls]",'[contenteditable]:not([contenteditable="false" i])',"details>summary:first-of-type","details"].join(),rx=['[tabindex]:not([tabindex="-1"]):not([tabindex="0"])'].join(),ix=(e,t)=>{if("hidden"===window.getComputedStyle(e).visibility)return!1;for(void 0===t&&(t=e);t.contains(e);){if("none"===window.getComputedStyle(e).display)return!1;e=e.parentElement}return!0};class ox{constructor(e,t){this.element=null,this.activeElement=null,this.onTrap=e,this.onUntrap=t,this.waiting=this.wait.bind(this),this.handling=this.handle.bind(this),this.current=null}get trapped(){return null!==this.element}trap(e){this.trapped&&this.untrap(),this.element=e,this.isTrapping=!0,this.wait(),this.onTrap&&this.onTrap()}wait(){ix(this.element)?this.trapping():p_.core.engine.renderer.next(this.waiting)}trapping(){if(!this.isTrapping)return;this.isTrapping=!1;const e=this.focusables;e.length&&e[0].focus(),this.element.setAttribute("aria-modal",!0),window.addEventListener("keydown",this.handling),this.stunneds=[]}stun(e){for(const t of e.children)t!==this.element&&(t.contains(this.element)?this.stun(t):this.stunneds.push(new ax(t)))}handle(e){if(9!==e.keyCode)return;const t=this.focusables;if(0===t.length)return;const n=t[0],r=t[t.length-1],i=t.indexOf(document.activeElement);e.shiftKey?!this.element.contains(document.activeElement)||i<1?(e.preventDefault(),r.focus()):(document.activeElement.tabIndex>0||t[i-1].tabIndex>0)&&(e.preventDefault(),t[i-1].focus()):this.element.contains(document.activeElement)&&i!==t.length-1&&-1!==i?document.activeElement.tabIndex>0&&(e.preventDefault(),t[i+1].focus()):(e.preventDefault(),n.focus())}get focusables(){let e=[...this.element.querySelectorAll(nx)];const t=[...document.documentElement.querySelectorAll('input[type="radio"]')];if(t.length){const n={};for(const e of t){const t=e.getAttribute("name");void 0===n[t]&&(n[t]=new ux(t)),n[t].push(e)}e=e.filter((e=>{if("input"!==e.tagName.toLowerCase()||"radio"!==e.getAttribute("type").toLowerCase())return!0;const t=e.getAttribute("name");return n[t].keep(e)}))}const n=[...this.element.querySelectorAll(rx)];n.sort(((e,t)=>e.tabIndex-t.tabIndex));const r=e.filter((e=>-1===n.indexOf(e)));return n.concat(r).filter((e=>"-1"!==e.tabIndex&&ix(e,this.element)))}untrap(){this.trapped&&(this.isTrapping=!1,this.element.removeAttribute("aria-modal"),window.removeEventListener("keydown",this.handling),this.element=null,this.onUntrap&&this.onUntrap())}}class ax{constructor(e){this.element=e,this.hidden=e.getAttribute("aria-hidden"),this.inert=e.getAttribute("inert"),this.element.setAttribute("aria-hidden",!0),this.element.setAttribute("inert","")}unstun(){null===this.hidden?this.element.removeAttribute("aria-hidden"):this.element.setAttribute("aria-hidden",this.hidden),null===this.inert?this.element.removeAttribute("inert"):this.element.setAttribute("inert",this.inert)}}class ux{constructor(e){this.name=e,this.buttons=[]}push(e){this.buttons.push(e),(e===document.activeElement||e.checked||void 0===this.selected)&&(this.selected=e)}keep(e){return this.selected===e}}class sx extends p_.core.DisclosuresGroup{constructor(){super(),this.trap=new ox}apply(e,t){super.apply(e,t),null===this.current?this.trap.untrap():this.trap.trap(this.current.element)}}const lx=new sx;class cx extends p_.core.Disclosure{constructor(e){super(e),this.body=this.element.querySelector(tx),this.scrollDistance=0,this.scrolling=this.resize.bind(this,!1),this.resizing=this.resize.bind(this,!0),this.init(),this.resize(!0)}init(){this.element.addEventListener("click",this.click.bind(this)),this.keyListener=new p_.KeyListener(this.element),this.keyListener.down(p_.KeyListener.ESCAPE,this.conceal.bind(this),!0,!0),this.body&&(this.body.addEventListener("scroll",this.scrolling),window.addEventListener("resize",this.resizing))}click(e){this.body&&this.body!==e.target&&!this.body.contains(e.target)&&this.conceal()}gather(){lx.add(this)}disclose(e){return!!super.disclose(e)&&(this.resize(!0),this.handleScroll(!1),!0)}conceal(e,t){return!!super.conceal(e,t)&&(this.handleScroll(!0),!0)}handleScroll(e){e?(p_.core.removeClass(document.documentElement,J_),document.body.style.top="",window.scroll(0,this.scrollDistance)):(document.documentElement.classList.contains(J_)||(this.scrollDistance=window.scrollY),document.body.style.top=-1*this.scrollDistance+"px",p_.core.addClass(document.documentElement,J_))}resize(e,t){this.body&&(this.body.scrollHeight>this.body.clientHeight?this.body.offsetHeight+this.body.scrollTop>=this.body.scrollHeight?p_.core.removeClass(this.body,ex):p_.core.addClass(this.body,ex):p_.core.removeClass(this.body,ex),this.isMedium=window.matchMedia("(min-width: 48em)").matches,e&&(this.isMedium?this.body.style.removeProperty("max-height"):(this.body.style.maxHeight=window.innerHeight-32+"px",p_.core.engine.renderer.next((()=>{this.body.style.maxHeight=window.innerHeight-32+"px"})))))}static get type(){return p_.core.DISCLOSURE_TYPES.opened}static get selector(){return Z_}get GroupConstructor(){return sx}}p_.Modal=cx,p_.ModalsGroup=sx,p_.FocusTrap=ox,new p_.core.Initializer(X_,[()=>{cx.build(document)}]);const fx=p_.core.ns("nav"),dx=p_.core.ns("nav__list"),hx=p_.core.ns("nav__item"),px=p_.core.ns("nav__item--align-right"),mx=p_.core.ns("menu");class vx extends p_.core.DisclosuresGroup{constructor(e,t){super(e,t),this.menus=[],this.navList=t.querySelector(`.${dx}`),document.addEventListener("focusout",this.focusOut.bind(this)),window.addEventListener("resize",this.resize.bind(this)),window.addEventListener("orientationchange",this.resize.bind(this)),this.resize()}static get selector(){return fx}add(e){super.add(e),e.element.classList.contains(mx)&&this.menus.push(new yx(e,this.navList.getBoundingClientRect().right))}focusOut(e){requestAnimationFrame((()=>{null===this.current||this.current.hasFocus||(this.index=-1)}))}get index(){return super.index}set index(e){-1===e&&null!==this.current&&this.current.hasFocus&&this.current.focus(),super.index=e}resize(){const e=this.navList.getBoundingClientRect().right;for(const t of this.menus)t.place(e)}}class yx{constructor(e,t){this.initialize(e),this.place(t)}initialize(e){this.element=e.element;for(const n of e.buttons)if(n.hasAttribute){this.button=n.element;break}let t=this.element.parentElement;for(;t;){if(t.classList.contains(hx)){this.item=t;break}t=t.parentElement}}place(e){const t=getComputedStyle(this.element),n=parseFloat(t.width);this.button.getBoundingClientRect().left+n>e?p_.core.addClass(this.item,px):p_.core.removeClass(this.item,px)}}p_.Navigation=vx,p_.Collapse.register(fx,vx);const gx=p_.core.ns.attr("theme"),bx=p_.core.ns.attr("transition");class wx{constructor(){this.init()}init(){if(this.root=document.documentElement,this.scheme=localStorage.getItem("scheme")?localStorage.getItem("scheme"):null,null===this.scheme){const e=this.root.getAttribute(gx);"dark"===e||"light"===e?this.scheme=e:window.matchMedia("(prefers-color-scheme: dark)").matches?(this.scheme="dark",localStorage.setItem("scheme","dark")):this.scheme="light"}"dark"===this.scheme?this.root.hasAttribute(bx)?(this.root.removeAttribute(bx),this.root.setAttribute(gx,"dark"),setTimeout((()=>{this.root.setAttribute(bx,"")}),300)):this.root.setAttribute(gx,"dark"):this.root.setAttribute(gx,"light"),this.observer=new MutationObserver(this.mutate.bind(this)),this.observer.observe(this.root,{attributes:!0})}mutate(e){e.forEach((e=>{if("attributes"===e.type&&e.attributeName===gx){const e=this.root.getAttribute(gx);"dark"===e?localStorage.setItem("scheme","dark"):"light"===e&&localStorage.setItem("scheme","light")}}))}}p_.Scheme=wx;const Ex=`input[name="${p_.core.ns.selector("radios-theme","")}"]`,_x=p_.core.ns.selector("switch-theme","#"),xx=p_.core.ns.attr("theme");class Sx{constructor(){this.attributeName=xx,this.theme=null,this.radios=document.querySelectorAll(Ex);for(var e=0;e<this.radios.length;e++)this.radios[e].addEventListener("change",this.change.bind(this));this.observer=new MutationObserver(this.mutate.bind(this)),this.observe(),this.apply()}observe(){this.observer.observe(document.documentElement,{attributes:!0})}mutate(e){e.forEach((e=>{"attributes"===e.type&&e.attributeName===this.attributeName&&this.apply()}))}apply(){const e=document.documentElement.getAttribute(this.attributeName);this.isApplying=!0;for(var t=0;t<this.radios.length;t++)this.radios[t].checked=this.radios[t].value===e;this.isApplying=!1}change(){this.isApplying||(this.observer&&this.observer.disconnect(),this.theme=document.querySelector(Ex+":checked"),this.theme?document.documentElement.setAttribute(this.attributeName,this.theme.value):document.documentElement.removeAttribute(this.attributeName),this.observer&&this.observe())}}new p_.core.Initializer(`:root[${gx}]`,[()=>{new wx}]),new p_.core.Initializer(`${_x}`,[()=>{new Sx}]);const kx=p_.core.ns("sidemenu"),Cx=p_.core.ns("sidemenu__list");p_.Collapse.register(kx,Cx);const Ox=p_.core.ns.selector("table"),Tx=p_.core.ns("table--no-scroll"),jx=p_.core.ns("table--shadow"),Px=p_.core.ns("table--shadow-left"),Fx=p_.core.ns("table--shadow-right");class Ax{constructor(e){this.init(e)}init(e){this.table=e,this.table.setAttribute(p_.core.ns.attr("js-table"),"true"),this.tableElem=this.table.querySelector("table"),this.tableContent=this.tableElem.querySelector("tbody"),this.isScrollable=this.tableContent.offsetWidth>this.tableElem.offsetWidth,this.caption=this.tableElem.querySelector("caption"),this.captionHeight=0;const t=this.change.bind(this);this.tableElem.addEventListener("scroll",t)}change(){const e=this.tableContent.offsetWidth>this.tableElem.offsetWidth;let t=this.tableElem.offsetWidth>this.table.offsetWidth;e||t?this.table.classList.contains(Tx)||this.scroll():e!==this.isScrollable&&this.delete(),this.isScrollable=e,t=!1;const n=this.caption.getBoundingClientRect();this.table.style.setProperty("--table-offset",n.height+"px")}delete(){p_.core.removeClass(this.table,Fx),p_.core.removeClass(this.table,Px),p_.core.removeClass(this.table,jx),this.caption&&(this.tableElem.style.marginTop="",this.caption.style.top="",this.tableElem.style.marginBottom="",this.caption.style.bottom="")}scroll(){p_.core.addClass(this.table,jx),this.setShadowPosition()}setShadowPosition(){const e=this.getScrollPosition("left"),t=this.getScrollPosition("right");"rtl"===document.documentElement.getAttribute("dir")?(this.setShadowVisibility("right",e),this.setShadowVisibility("left",t)):(this.setShadowVisibility("left",e),this.setShadowVisibility("right",t))}getScrollPosition(e){let t=1;switch("rtl"===document.documentElement.getAttribute("dir")&&(t=-1),e){case"left":return this.tableElem.scrollLeft*t;case"right":return this.tableContent.offsetWidth-this.tableElem.offsetWidth-this.tableElem.scrollLeft*t;default:return!1}}setShadowVisibility(e,t){t<=1?"left"===e?p_.core.removeClass(this.table,Px):"right"===e&&p_.core.removeClass(this.table,Fx):"left"===e?p_.core.addClass(this.table,Px):"right"===e&&p_.core.addClass(this.table,Fx)}}p_.Table=Ax;const Dx=[],Nx=()=>{for(let e=0;e<Dx.length;e++)Dx[e].change()};new p_.core.Initializer(Ox,[()=>{const e=document.querySelectorAll(Ox);for(let t=0;t<e.length;t++)Dx.push(new Ax(e[t]));window.addEventListener("resize",Nx),window.addEventListener("orientationchange",Nx),Nx()}]);class Mx extends p_.core.DisclosureButton{apply(e){super.apply(e),this.hasAttribute&&this.element.setAttribute("tabindex",e?"0":"-1")}}const Lx=p_.core.ns.selector("tabs"),zx=p_.core.ns("tabs"),Rx=p_.core.ns("tabs__tab"),Ix=p_.core.ns("tabs__panel"),Ux=p_.core.ns("tabs__list");class $x extends p_.core.DisclosuresGroup{constructor(e,t){super(e,t),this.list=t.querySelector(`.${Ux}`),t.addEventListener("transitionend",this.transitionend.bind(this)),this.init(),p_.core.engine.renderer.add(this.render.bind(this))}static get selector(){return zx}transitionend(e){this.element.style.transition="none"}init(){this.keyListener=new p_.KeyListener(this.element),this.keyListener.down(p_.KeyListener.RIGHT,this.arrowRightPress.bind(this),!0,!0),this.keyListener.down(p_.KeyListener.LEFT,this.arrowLeftPress.bind(this),!0,!0),this.keyListener.down(p_.KeyListener.HOME,this.homePress.bind(this),!0,!0),this.keyListener.down(p_.KeyListener.END,this.endPress.bind(this),!0,!0)}arrowRightPress(){document.activeElement.classList.contains(Rx)&&(this.index<this.length-1?this.index++:this.index=0,this.focus())}arrowLeftPress(){document.activeElement.classList.contains(Rx)&&(this.index>0?this.index--:this.index=this.length-1,this.focus())}homePress(){document.activeElement.classList.contains(Rx)&&(this.index=0,this.focus())}endPress(){document.activeElement.classList.contains(Rx)&&(this.index=this.length-1,this.focus())}focus(){this.current&&this.current.focus()}apply(){for(let e=0;e<this._index;e++)this.members[e].translate(-1);this.current.element.style.transition="",this.current.element.style.transform="";for(let e=this._index+1;e<this.length;e++)this.members[e].translate(1);this.element.style.transition=""}add(e){if(super.add(e),1===this.length||e.disclosed)this.current=e;else{const t=this.members.indexOf(e);this._index>-1&&this._index!==t&&e.translate(t<this._index?-1:1,!0)}}render(){if(null===this.current)return;const e=Math.round(this.current.element.offsetHeight);this.panelHeight!==e&&(this.panelHeight=e,this.element.style.height=this.panelHeight+this.list.offsetHeight+"px")}}class Bx extends p_.core.Disclosure{static get type(){return p_.core.DISCLOSURE_TYPES.select}static get selector(){return Ix}get GroupConstructor(){return $x}buttonFactory(e){return new Mx(e,this)}translate(e,t){this.element.style.transition=t?"none":"",this.element.style.transform=`translate(${100*e}%)`}reset(){this.group.index=0}}p_.Tab=Bx,p_.TabButton=Mx,p_.TabsGroup=$x,new p_.core.Initializer(Lx,[()=>{Bx.build(document)}]);const Vx=p_.core.ns.selector("header"),qx=p_.core.ns.selector("header__search"),Wx=p_.core.ns.selector("header__menu"),Hx=p_.core.ns.selector("header__tools-links"),Yx=p_.core.ns.selector("header__menu-links"),Qx=`${Hx} ${p_.core.ns.selector("links-group")}`;class Gx{constructor(e){this.header=e||document.querySelector(Vx),this.modals=[],this.init()}getModal(e){const t=this.header.querySelector(e);if(!t)return;const n=p_.core.Instance.getInstances(t,p_.Modal);n&&n.length&&this.modals.push(new Kx(n[0]))}init(){this.getModal(qx),this.getModal(Wx),this.linksGroup=this.header.querySelector(Qx),this.toolsLinks=this.header.querySelector(Hx),this.menuLinks=this.header.querySelector(Yx),this.changing=this.change.bind(this),window.addEventListener("resize",this.changing),this.change()}change(){this.isLarge=window.matchMedia("(min-width: 62em)").matches,this.isLarge?this.modals.forEach((e=>e.disable())):this.modals.forEach((e=>e.enable())),null!==this.linksGroup&&(this.isLarge?this.toolsLinks.appendChild(this.linksGroup):this.menuLinks.appendChild(this.linksGroup))}}class Kx{constructor(e){this.modal=e}enable(){this.modal.element.setAttribute("role","dialog"),this.modal.element.setAttribute("aria-labelledby",this.modal.primary.element.id)}disable(){this.modal.conceal(),this.modal.element.removeAttribute("role"),this.modal.element.removeAttribute("aria-labelledby")}}p_.Header=Gx,new p_.core.Initializer(Vx,[()=>{const e=Array.prototype.slice.call(document.querySelectorAll(Vx)),t=[];for(const n of e)t.push(new Gx(n))}]);var Xx=Array.isArray,Zx=Object.keys,Jx=Object.prototype.hasOwnProperty,eS="undefined"!=typeof Element;function tS(e,t){if(e===t)return!0;if(e&&t&&"object"==typeof e&&"object"==typeof t){var n,r,i,o=Xx(e),a=Xx(t);if(o&&a){if((r=e.length)!=t.length)return!1;for(n=r;0!=n--;)if(!tS(e[n],t[n]))return!1;return!0}if(o!=a)return!1;var u=e instanceof Date,s=t instanceof Date;if(u!=s)return!1;if(u&&s)return e.getTime()==t.getTime();var l=e instanceof RegExp,c=t instanceof RegExp;if(l!=c)return!1;if(l&&c)return e.toString()==t.toString();var f=Zx(e);if((r=f.length)!==Zx(t).length)return!1;for(n=r;0!=n--;)if(!Jx.call(t,f[n]))return!1;if(eS&&e instanceof Element&&t instanceof Element)return e===t;for(n=r;0!=n--;)if(!("_owner"===(i=f[n])&&e.$$typeof||tS(e[i],t[i])))return!1;return!0}return e!=e&&t!=t}var nS=function(e,t){try{return tS(e,t)}catch(n){if(n.message&&n.message.match(/stack|recursion/i)||-2146828260===n.number)return console.warn("Warning: react-fast-compare does not handle circular references.",n.name,n.message),!1;throw n}},rS=function(e){return function(e){return!!e&&"object"==typeof e}(e)&&!function(e){var t=Object.prototype.toString.call(e);return"[object RegExp]"===t||"[object Date]"===t||function(e){return e.$$typeof===iS}(e)}(e)};var iS="function"==typeof Symbol&&Symbol.for?Symbol.for("react.element"):60103;function oS(e,t){return!1!==t.clone&&t.isMergeableObject(e)?uS((n=e,Array.isArray(n)?[]:{}),e,t):e;var n}function aS(e,t,n){return e.concat(t).map((function(e){return oS(e,n)}))}function uS(e,t,n){(n=n||{}).arrayMerge=n.arrayMerge||aS,n.isMergeableObject=n.isMergeableObject||rS;var r=Array.isArray(t);return r===Array.isArray(e)?r?n.arrayMerge(e,t,n):function(e,t,n){var r={};return n.isMergeableObject(e)&&Object.keys(e).forEach((function(t){r[t]=oS(e[t],n)})),Object.keys(t).forEach((function(i){n.isMergeableObject(t[i])&&e[i]?r[i]=uS(e[i],t[i],n):r[i]=oS(t[i],n)})),r}(e,t,n):oS(t,n)}uS.all=function(e,t){if(!Array.isArray(e))throw new Error("first argument should be an array");return e.reduce((function(e,n){return uS(e,n,t)}),{})};var sS=uS,lS="object"==typeof global&&global&&global.Object===Object&&global,cS="object"==typeof self&&self&&self.Object===Object&&self,fS=lS||cS||Function("return this")(),dS=fS.Symbol,hS=Object.prototype,pS=hS.hasOwnProperty,mS=hS.toString,vS=dS?dS.toStringTag:void 0;var yS=Object.prototype.toString;var gS=dS?dS.toStringTag:void 0;function bS(e){return null==e?void 0===e?"[object Undefined]":"[object Null]":gS&&gS in Object(e)?function(e){var t=pS.call(e,vS),n=e[vS];try{e[vS]=void 0;var r=!0}catch(o){}var i=mS.call(e);return r&&(t?e[vS]=n:delete e[vS]),i}(e):function(e){return yS.call(e)}(e)}function wS(e,t){return function(n){return e(t(n))}}var ES=wS(Object.getPrototypeOf,Object);function _S(e){return null!=e&&"object"==typeof e}var xS=Function.prototype,SS=Object.prototype,kS=xS.toString,CS=SS.hasOwnProperty,OS=kS.call(Object);function TS(e){if(!_S(e)||"[object Object]"!=bS(e))return!1;var t=ES(e);if(null===t)return!0;var n=CS.call(t,"constructor")&&t.constructor;return"function"==typeof n&&n instanceof n&&kS.call(n)==OS}function jS(e,t){return e===t||e!=e&&t!=t}function PS(e,t){for(var n=e.length;n--;)if(jS(e[n][0],t))return n;return-1}var FS=Array.prototype.splice;function AS(e){var t=-1,n=null==e?0:e.length;for(this.clear();++t<n;){var r=e[t];this.set(r[0],r[1])}}function DS(e){var t=typeof e;return null!=e&&("object"==t||"function"==t)}AS.prototype.clear=function(){this.__data__=[],this.size=0},AS.prototype.delete=function(e){var t=this.__data__,n=PS(t,e);return!(n<0)&&(n==t.length-1?t.pop():FS.call(t,n,1),--this.size,!0)},AS.prototype.get=function(e){var t=this.__data__,n=PS(t,e);return n<0?void 0:t[n][1]},AS.prototype.has=function(e){return PS(this.__data__,e)>-1},AS.prototype.set=function(e,t){var n=this.__data__,r=PS(n,e);return r<0?(++this.size,n.push([e,t])):n[r][1]=t,this};function NS(e){if(!DS(e))return!1;var t=bS(e);return"[object Function]"==t||"[object GeneratorFunction]"==t||"[object AsyncFunction]"==t||"[object Proxy]"==t}var MS=fS["__core-js_shared__"],LS=function(){var e=/[^.]+$/.exec(MS&&MS.keys&&MS.keys.IE_PROTO||"");return e?"Symbol(src)_1."+e:""}();var zS=Function.prototype.toString;function RS(e){if(null!=e){try{return zS.call(e)}catch(t){}try{return e+""}catch(t){}}return""}var IS=/^\[object .+?Constructor\]$/,US=Function.prototype,$S=Object.prototype,BS=US.toString,VS=$S.hasOwnProperty,qS=RegExp("^"+BS.call(VS).replace(/[\\^$.*+?()[\]{}|]/g,"\\$&").replace(/hasOwnProperty|(function).*?(?=\\\()| for .+?(?=\\\])/g,"$1.*?")+"$");function WS(e){return!(!DS(e)||(t=e,LS&&LS in t))&&(NS(e)?qS:IS).test(RS(e));var t}function HS(e,t){var n=function(e,t){return null==e?void 0:e[t]}(e,t);return WS(n)?n:void 0}var YS=HS(fS,"Map"),QS=HS(Object,"create");var GS=Object.prototype.hasOwnProperty;var KS=Object.prototype.hasOwnProperty;function XS(e){var t=-1,n=null==e?0:e.length;for(this.clear();++t<n;){var r=e[t];this.set(r[0],r[1])}}function ZS(e,t){var n,r,i=e.__data__;return("string"==(r=typeof(n=t))||"number"==r||"symbol"==r||"boolean"==r?"__proto__"!==n:null===n)?i["string"==typeof t?"string":"hash"]:i.map}function JS(e){var t=-1,n=null==e?0:e.length;for(this.clear();++t<n;){var r=e[t];this.set(r[0],r[1])}}XS.prototype.clear=function(){this.__data__=QS?QS(null):{},this.size=0},XS.prototype.delete=function(e){var t=this.has(e)&&delete this.__data__[e];return this.size-=t?1:0,t},XS.prototype.get=function(e){var t=this.__data__;if(QS){var n=t[e];return"__lodash_hash_undefined__"===n?void 0:n}return GS.call(t,e)?t[e]:void 0},XS.prototype.has=function(e){var t=this.__data__;return QS?void 0!==t[e]:KS.call(t,e)},XS.prototype.set=function(e,t){var n=this.__data__;return this.size+=this.has(e)?0:1,n[e]=QS&&void 0===t?"__lodash_hash_undefined__":t,this},JS.prototype.clear=function(){this.size=0,this.__data__={hash:new XS,map:new(YS||AS),string:new XS}},JS.prototype.delete=function(e){var t=ZS(this,e).delete(e);return this.size-=t?1:0,t},JS.prototype.get=function(e){return ZS(this,e).get(e)},JS.prototype.has=function(e){return ZS(this,e).has(e)},JS.prototype.set=function(e,t){var n=ZS(this,e),r=n.size;return n.set(e,t),this.size+=n.size==r?0:1,this};function ek(e){var t=this.__data__=new AS(e);this.size=t.size}ek.prototype.clear=function(){this.__data__=new AS,this.size=0},ek.prototype.delete=function(e){var t=this.__data__,n=t.delete(e);return this.size=t.size,n},ek.prototype.get=function(e){return this.__data__.get(e)},ek.prototype.has=function(e){return this.__data__.has(e)},ek.prototype.set=function(e,t){var n=this.__data__;if(n instanceof AS){var r=n.__data__;if(!YS||r.length<199)return r.push([e,t]),this.size=++n.size,this;n=this.__data__=new JS(r)}return n.set(e,t),this.size=n.size,this};var tk=function(){try{var e=HS(Object,"defineProperty");return e({},"",{}),e}catch(t){}}();function nk(e,t,n){"__proto__"==t&&tk?tk(e,t,{configurable:!0,enumerable:!0,value:n,writable:!0}):e[t]=n}var rk=Object.prototype.hasOwnProperty;function ik(e,t,n){var r=e[t];rk.call(e,t)&&jS(r,n)&&(void 0!==n||t in e)||nk(e,t,n)}function ok(e,t,n,r){var i=!n;n||(n={});for(var o=-1,a=t.length;++o<a;){var u=t[o],s=r?r(n[u],e[u],u,n,e):void 0;void 0===s&&(s=e[u]),i?nk(n,u,s):ik(n,u,s)}return n}function ak(e){return _S(e)&&"[object Arguments]"==bS(e)}var uk=Object.prototype,sk=uk.hasOwnProperty,lk=uk.propertyIsEnumerable,ck=ak(function(){return arguments}())?ak:function(e){return _S(e)&&sk.call(e,"callee")&&!lk.call(e,"callee")},fk=Array.isArray;var dk="object"==typeof exports&&exports&&!exports.nodeType&&exports,hk=dk&&"object"==typeof module&&module&&!module.nodeType&&module,pk=hk&&hk.exports===dk?fS.Buffer:void 0,mk=(pk?pk.isBuffer:void 0)||function(){return!1},vk=/^(?:0|[1-9]\d*)$/;function yk(e,t){var n=typeof e;return!!(t=null==t?9007199254740991:t)&&("number"==n||"symbol"!=n&&vk.test(e))&&e>-1&&e%1==0&&e<t}function gk(e){return"number"==typeof e&&e>-1&&e%1==0&&e<=9007199254740991}var bk={};function wk(e){return function(t){return e(t)}}bk["[object Float32Array]"]=bk["[object Float64Array]"]=bk["[object Int8Array]"]=bk["[object Int16Array]"]=bk["[object Int32Array]"]=bk["[object Uint8Array]"]=bk["[object Uint8ClampedArray]"]=bk["[object Uint16Array]"]=bk["[object Uint32Array]"]=!0,bk["[object Arguments]"]=bk["[object Array]"]=bk["[object ArrayBuffer]"]=bk["[object Boolean]"]=bk["[object DataView]"]=bk["[object Date]"]=bk["[object Error]"]=bk["[object Function]"]=bk["[object Map]"]=bk["[object Number]"]=bk["[object Object]"]=bk["[object RegExp]"]=bk["[object Set]"]=bk["[object String]"]=bk["[object WeakMap]"]=!1;var Ek="object"==typeof exports&&exports&&!exports.nodeType&&exports,_k=Ek&&"object"==typeof module&&module&&!module.nodeType&&module,xk=_k&&_k.exports===Ek&&lS.process,Sk=function(){try{var e=_k&&_k.require&&_k.require("util").types;return e||xk&&xk.binding&&xk.binding("util")}catch(t){}}(),kk=Sk&&Sk.isTypedArray,Ck=kk?wk(kk):function(e){return _S(e)&&gk(e.length)&&!!bk[bS(e)]},Ok=Object.prototype.hasOwnProperty;function Tk(e,t){var n=fk(e),r=!n&&ck(e),i=!n&&!r&&mk(e),o=!n&&!r&&!i&&Ck(e),a=n||r||i||o,u=a?function(e,t){for(var n=-1,r=Array(e);++n<e;)r[n]=t(n);return r}(e.length,String):[],s=u.length;for(var l in e)!t&&!Ok.call(e,l)||a&&("length"==l||i&&("offset"==l||"parent"==l)||o&&("buffer"==l||"byteLength"==l||"byteOffset"==l)||yk(l,s))||u.push(l);return u}var jk=Object.prototype;function Pk(e){var t=e&&e.constructor;return e===("function"==typeof t&&t.prototype||jk)}var Fk=wS(Object.keys,Object),Ak=Object.prototype.hasOwnProperty;function Dk(e){return null!=e&&gk(e.length)&&!NS(e)}function Nk(e){return Dk(e)?Tk(e):function(e){if(!Pk(e))return Fk(e);var t=[];for(var n in Object(e))Ak.call(e,n)&&"constructor"!=n&&t.push(n);return t}(e)}var Mk=Object.prototype.hasOwnProperty;function Lk(e){if(!DS(e))return function(e){var t=[];if(null!=e)for(var n in Object(e))t.push(n);return t}(e);var t=Pk(e),n=[];for(var r in e)("constructor"!=r||!t&&Mk.call(e,r))&&n.push(r);return n}function zk(e){return Dk(e)?Tk(e,!0):Lk(e)}var Rk="object"==typeof exports&&exports&&!exports.nodeType&&exports,Ik=Rk&&"object"==typeof module&&module&&!module.nodeType&&module,Uk=Ik&&Ik.exports===Rk?fS.Buffer:void 0,$k=Uk?Uk.allocUnsafe:void 0;function Bk(e,t){var n=-1,r=e.length;for(t||(t=Array(r));++n<r;)t[n]=e[n];return t}function Vk(){return[]}var qk=Object.prototype.propertyIsEnumerable,Wk=Object.getOwnPropertySymbols,Hk=Wk?function(e){return null==e?[]:(e=Object(e),function(e,t){for(var n=-1,r=null==e?0:e.length,i=0,o=[];++n<r;){var a=e[n];t(a,n,e)&&(o[i++]=a)}return o}(Wk(e),(function(t){return qk.call(e,t)})))}:Vk;function Yk(e,t){for(var n=-1,r=t.length,i=e.length;++n<r;)e[i+n]=t[n];return e}var Qk=Object.getOwnPropertySymbols?function(e){for(var t=[];e;)Yk(t,Hk(e)),e=ES(e);return t}:Vk;function Gk(e,t,n){var r=t(e);return fk(e)?r:Yk(r,n(e))}function Kk(e){return Gk(e,Nk,Hk)}function Xk(e){return Gk(e,zk,Qk)}var Zk=HS(fS,"DataView"),Jk=HS(fS,"Promise"),eC=HS(fS,"Set"),tC=HS(fS,"WeakMap"),nC=RS(Zk),rC=RS(YS),iC=RS(Jk),oC=RS(eC),aC=RS(tC),uC=bS;(Zk&&"[object DataView]"!=uC(new Zk(new ArrayBuffer(1)))||YS&&"[object Map]"!=uC(new YS)||Jk&&"[object Promise]"!=uC(Jk.resolve())||eC&&"[object Set]"!=uC(new eC)||tC&&"[object WeakMap]"!=uC(new tC))&&(uC=function(e){var t=bS(e),n="[object Object]"==t?e.constructor:void 0,r=n?RS(n):"";if(r)switch(r){case nC:return"[object DataView]";case rC:return"[object Map]";case iC:return"[object Promise]";case oC:return"[object Set]";case aC:return"[object WeakMap]"}return t});var sC=uC,lC=Object.prototype.hasOwnProperty;var cC=fS.Uint8Array;function fC(e){var t=new e.constructor(e.byteLength);return new cC(t).set(new cC(e)),t}var dC=/\w*$/;var hC=dS?dS.prototype:void 0,pC=hC?hC.valueOf:void 0;function mC(e,t,n){var r,i,o,a=e.constructor;switch(t){case"[object ArrayBuffer]":return fC(e);case"[object Boolean]":case"[object Date]":return new a(+e);case"[object DataView]":return function(e,t){var n=t?fC(e.buffer):e.buffer;return new e.constructor(n,e.byteOffset,e.byteLength)}(e,n);case"[object Float32Array]":case"[object Float64Array]":case"[object Int8Array]":case"[object Int16Array]":case"[object Int32Array]":case"[object Uint8Array]":case"[object Uint8ClampedArray]":case"[object Uint16Array]":case"[object Uint32Array]":return function(e,t){var n=t?fC(e.buffer):e.buffer;return new e.constructor(n,e.byteOffset,e.length)}(e,n);case"[object Map]":return new a;case"[object Number]":case"[object String]":return new a(e);case"[object RegExp]":return(o=new(i=e).constructor(i.source,dC.exec(i))).lastIndex=i.lastIndex,o;case"[object Set]":return new a;case"[object Symbol]":return r=e,pC?Object(pC.call(r)):{}}}var vC=Object.create,yC=function(){function e(){}return function(t){if(!DS(t))return{};if(vC)return vC(t);e.prototype=t;var n=new e;return e.prototype=void 0,n}}();var gC=Sk&&Sk.isMap,bC=gC?wk(gC):function(e){return _S(e)&&"[object Map]"==sC(e)};var wC=Sk&&Sk.isSet,EC=wC?wk(wC):function(e){return _S(e)&&"[object Set]"==sC(e)},_C={};function xC(e,t,n,r,i,o){var a,u=1&t,s=2&t,l=4&t;if(n&&(a=i?n(e,r,i,o):n(e)),void 0!==a)return a;if(!DS(e))return e;var c=fk(e);if(c){if(a=function(e){var t=e.length,n=new e.constructor(t);return t&&"string"==typeof e[0]&&lC.call(e,"index")&&(n.index=e.index,n.input=e.input),n}(e),!u)return Bk(e,a)}else{var f=sC(e),d="[object Function]"==f||"[object GeneratorFunction]"==f;if(mk(e))return function(e,t){if(t)return e.slice();var n=e.length,r=$k?$k(n):new e.constructor(n);return e.copy(r),r}(e,u);if("[object Object]"==f||"[object Arguments]"==f||d&&!i){if(a=s||d?{}:function(e){return"function"!=typeof e.constructor||Pk(e)?{}:yC(ES(e))}(e),!u)return s?function(e,t){return ok(e,Qk(e),t)}(e,function(e,t){return e&&ok(t,zk(t),e)}(a,e)):function(e,t){return ok(e,Hk(e),t)}(e,function(e,t){return e&&ok(t,Nk(t),e)}(a,e))}else{if(!_C[f])return i?e:{};a=mC(e,f,u)}}o||(o=new ek);var h=o.get(e);if(h)return h;o.set(e,a),EC(e)?e.forEach((function(r){a.add(xC(r,t,n,r,e,o))})):bC(e)&&e.forEach((function(r,i){a.set(i,xC(r,t,n,i,e,o))}));var p=c?void 0:(l?s?Xk:Kk:s?zk:Nk)(e);return function(e,t){for(var n=-1,r=null==e?0:e.length;++n<r&&!1!==t(e[n],n,e););}(p||e,(function(r,i){p&&(r=e[i=r]),ik(a,i,xC(r,t,n,i,e,o))})),a}_C["[object Arguments]"]=_C["[object Array]"]=_C["[object ArrayBuffer]"]=_C["[object DataView]"]=_C["[object Boolean]"]=_C["[object Date]"]=_C["[object Float32Array]"]=_C["[object Float64Array]"]=_C["[object Int8Array]"]=_C["[object Int16Array]"]=_C["[object Int32Array]"]=_C["[object Map]"]=_C["[object Number]"]=_C["[object Object]"]=_C["[object RegExp]"]=_C["[object Set]"]=_C["[object String]"]=_C["[object Symbol]"]=_C["[object Uint8Array]"]=_C["[object Uint8ClampedArray]"]=_C["[object Uint16Array]"]=_C["[object Uint32Array]"]=!0,_C["[object Error]"]=_C["[object Function]"]=_C["[object WeakMap]"]=!1;function SC(e){return xC(e,4)}function kC(e,t){for(var n=-1,r=null==e?0:e.length,i=Array(r);++n<r;)i[n]=t(e[n],n,e);return i}function CC(e){return"symbol"==typeof e||_S(e)&&"[object Symbol]"==bS(e)}function OC(e,t){if("function"!=typeof e||null!=t&&"function"!=typeof t)throw new TypeError("Expected a function");var n=function(){var r=arguments,i=t?t.apply(this,r):r[0],o=n.cache;if(o.has(i))return o.get(i);var a=e.apply(this,r);return n.cache=o.set(i,a)||o,a};return n.cache=new(OC.Cache||JS),n}OC.Cache=JS;var TC,jC,PC,FC=/[^.[\]]+|\[(?:(-?\d+(?:\.\d+)?)|(["'])((?:(?!\2)[^\\]|\\.)*?)\2)\]|(?=(?:\.|\[\])(?:\.|\[\]|$))/g,AC=/\\(\\)?/g,DC=(TC=function(e){var t=[];return 46===e.charCodeAt(0)&&t.push(""),e.replace(FC,(function(e,n,r,i){t.push(r?i.replace(AC,"$1"):n||e)})),t},jC=OC(TC,(function(e){return 500===PC.size&&PC.clear(),e})),PC=jC.cache,jC);function NC(e){if("string"==typeof e||CC(e))return e;var t=e+"";return"0"==t&&1/e==-Infinity?"-0":t}var MC=dS?dS.prototype:void 0,LC=MC?MC.toString:void 0;function zC(e){if("string"==typeof e)return e;if(fk(e))return kC(e,zC)+"";if(CC(e))return LC?LC.call(e):"";var t=e+"";return"0"==t&&1/e==-Infinity?"-0":t}function RC(e){return fk(e)?kC(e,NC):CC(e)?[e]:Bk(DC(function(e){return null==e?"":zC(e)}(e)))}var IC={exports:{}},UC={};function $C(){return($C=Object.assign||function(e){for(var t=1;t<arguments.length;t++){var n=arguments[t];for(var r in n)Object.prototype.hasOwnProperty.call(n,r)&&(e[r]=n[r])}return e}).apply(this,arguments)}function BC(e,t){if(null==e)return{};var n,r,i={},o=Object.keys(e);for(r=0;r<o.length;r++)n=o[r],t.indexOf(n)>=0||(i[n]=e[n]);return i}
/** @license React v0.18.0
 * scheduler.production.min.js
 *
 * Copyright (c) Facebook, Inc. and its affiliates.
 *
 * This source code is licensed under the MIT license found in the
 * LICENSE file in the root directory of this source tree.
 */
!function(e){var t,n,r,i,o;if(Object.defineProperty(e,"__esModule",{value:!0}),"undefined"==typeof window||"function"!=typeof MessageChannel){var a=null,u=null,s=function(){if(null!==a)try{var t=e.unstable_now();a(!0,t),a=null}catch(n){throw setTimeout(s,0),n}},l=Date.now();e.unstable_now=function(){return Date.now()-l},t=function(e){null!==a?setTimeout(t,0,e):(a=e,setTimeout(s,0))},n=function(e,t){u=setTimeout(e,t)},r=function(){clearTimeout(u)},i=function(){return!1},o=e.unstable_forceFrameRate=function(){}}else{var c=window.performance,f=window.Date,d=window.setTimeout,h=window.clearTimeout;if("undefined"!=typeof console){var p=window.cancelAnimationFrame;"function"!=typeof window.requestAnimationFrame&&console.error("This browser doesn't support requestAnimationFrame. Make sure that you load a polyfill in older browsers. https://fb.me/react-polyfills"),"function"!=typeof p&&console.error("This browser doesn't support cancelAnimationFrame. Make sure that you load a polyfill in older browsers. https://fb.me/react-polyfills")}if("object"==typeof c&&"function"==typeof c.now)e.unstable_now=function(){return c.now()};else{var m=f.now();e.unstable_now=function(){return f.now()-m}}var v=!1,y=null,g=-1,b=5,w=0;i=function(){return e.unstable_now()>=w},o=function(){},e.unstable_forceFrameRate=function(e){0>e||125<e?console.error("forceFrameRate takes a positive int between 0 and 125, forcing framerates higher than 125 fps is not unsupported"):b=0<e?Math.floor(1e3/e):5};var E=new MessageChannel,_=E.port2;E.port1.onmessage=function(){if(null!==y){var t=e.unstable_now();w=t+b;try{y(!0,t)?_.postMessage(null):(v=!1,y=null)}catch(n){throw _.postMessage(null),n}}else v=!1},t=function(e){y=e,v||(v=!0,_.postMessage(null))},n=function(t,n){g=d((function(){t(e.unstable_now())}),n)},r=function(){h(g),g=-1}}function x(e,t){var n=e.length;e.push(t);e:for(;;){var r=Math.floor((n-1)/2),i=e[r];if(!(void 0!==i&&0<C(i,t)))break e;e[r]=t,e[n]=i,n=r}}function S(e){return void 0===(e=e[0])?null:e}function k(e){var t=e[0];if(void 0!==t){var n=e.pop();if(n!==t){e[0]=n;e:for(var r=0,i=e.length;r<i;){var o=2*(r+1)-1,a=e[o],u=o+1,s=e[u];if(void 0!==a&&0>C(a,n))void 0!==s&&0>C(s,a)?(e[r]=s,e[u]=n,r=u):(e[r]=a,e[o]=n,r=o);else{if(!(void 0!==s&&0>C(s,n)))break e;e[r]=s,e[u]=n,r=u}}}return t}return null}function C(e,t){var n=e.sortIndex-t.sortIndex;return 0!==n?n:e.id-t.id}var O=[],T=[],j=1,P=null,F=3,A=!1,D=!1,N=!1;function M(e){for(var t=S(T);null!==t;){if(null===t.callback)k(T);else{if(!(t.startTime<=e))break;k(T),t.sortIndex=t.expirationTime,x(O,t)}t=S(T)}}function L(e){if(N=!1,M(e),!D)if(null!==S(O))D=!0,t(z);else{var r=S(T);null!==r&&n(L,r.startTime-e)}}function z(t,o){D=!1,N&&(N=!1,r()),A=!0;var a=F;try{for(M(o),P=S(O);null!==P&&(!(P.expirationTime>o)||t&&!i());){var u=P.callback;if(null!==u){P.callback=null,F=P.priorityLevel;var s=u(P.expirationTime<=o);o=e.unstable_now(),"function"==typeof s?P.callback=s:P===S(O)&&k(O),M(o)}else k(O);P=S(O)}if(null!==P)var l=!0;else{var c=S(T);null!==c&&n(L,c.startTime-o),l=!1}return l}finally{P=null,F=a,A=!1}}function R(e){switch(e){case 1:return-1;case 2:return 250;case 5:return 1073741823;case 4:return 1e4;default:return 5e3}}var I=o;e.unstable_ImmediatePriority=1,e.unstable_UserBlockingPriority=2,e.unstable_NormalPriority=3,e.unstable_IdlePriority=5,e.unstable_LowPriority=4,e.unstable_runWithPriority=function(e,t){switch(e){case 1:case 2:case 3:case 4:case 5:break;default:e=3}var n=F;F=e;try{return t()}finally{F=n}},e.unstable_next=function(e){switch(F){case 1:case 2:case 3:var t=3;break;default:t=F}var n=F;F=t;try{return e()}finally{F=n}},e.unstable_scheduleCallback=function(i,o,a){var u=e.unstable_now();if("object"==typeof a&&null!==a){var s=a.delay;s="number"==typeof s&&0<s?u+s:u,a="number"==typeof a.timeout?a.timeout:R(i)}else a=R(i),s=u;return i={id:j++,callback:o,priorityLevel:i,startTime:s,expirationTime:a=s+a,sortIndex:-1},s>u?(i.sortIndex=s,x(T,i),null===S(O)&&i===S(T)&&(N?r():N=!0,n(L,s-u))):(i.sortIndex=a,x(O,i),D||A||(D=!0,t(z))),i},e.unstable_cancelCallback=function(e){e.callback=null},e.unstable_wrapCallback=function(e){var t=F;return function(){var n=F;F=t;try{return e.apply(this,arguments)}finally{F=n}}},e.unstable_getCurrentPriorityLevel=function(){return F},e.unstable_shouldYield=function(){var t=e.unstable_now();M(t);var n=S(O);return n!==P&&null!==P&&null!==n&&null!==n.callback&&n.startTime<=t&&n.expirationTime<P.expirationTime||i()},e.unstable_requestPaint=I,e.unstable_continueExecution=function(){D||A||(D=!0,t(z))},e.unstable_pauseExecution=function(){},e.unstable_getFirstCallbackNode=function(){return S(O)},e.unstable_Profiling=null}(UC),IC.exports=UC;var VC=function(e){return"function"==typeof e},qC=function(e){return null!==e&&"object"==typeof e},WC=function(e){return String(Math.floor(Number(e)))===e},HC=function(e){return"[object String]"===Object.prototype.toString.call(e)},YC=function(e){return qC(e)&&VC(e.then)};function QC(e,t,n,r){void 0===r&&(r=0);for(var i=RC(t);e&&r<i.length;)e=e[i[r++]];return void 0===e?n:e}function GC(e,t,n){for(var r=SC(e),i=r,o=0,a=RC(t);o<a.length-1;o++){var u=a[o],s=QC(e,a.slice(0,o+1));if(s&&(qC(s)||Array.isArray(s)))i=i[u]=SC(s);else{var l=a[o+1];i=i[u]=WC(l)&&Number(l)>=0?[]:{}}}return(0===o?e:i)[a[o]]===n?e:(void 0===n?delete i[a[o]]:i[a[o]]=n,0===o&&void 0===n&&delete r[a[o]],r)}function KC(e,t,n,r){void 0===n&&(n=new WeakMap),void 0===r&&(r={});for(var i=0,o=Object.keys(e);i<o.length;i++){var a=o[i],u=e[a];qC(u)?n.get(u)||(n.set(u,!0),r[a]=Array.isArray(u)?[]:{},KC(u,t,n,r[a])):r[a]=t}return r}var XC=t.exports.createContext(void 0),ZC=XC.Provider;function JC(){var e=t.exports.useContext(XC);return e}function eO(e,t){switch(t.type){case"SET_VALUES":return $C({},e,{values:t.payload});case"SET_TOUCHED":return $C({},e,{touched:t.payload});case"SET_ERRORS":return nS(e.errors,t.payload)?e:$C({},e,{errors:t.payload});case"SET_STATUS":return $C({},e,{status:t.payload});case"SET_ISSUBMITTING":return $C({},e,{isSubmitting:t.payload});case"SET_ISVALIDATING":return $C({},e,{isValidating:t.payload});case"SET_FIELD_VALUE":return $C({},e,{values:GC(e.values,t.payload.field,t.payload.value)});case"SET_FIELD_TOUCHED":return $C({},e,{touched:GC(e.touched,t.payload.field,t.payload.value)});case"SET_FIELD_ERROR":return $C({},e,{errors:GC(e.errors,t.payload.field,t.payload.value)});case"RESET_FORM":return $C({},e,{},t.payload);case"SET_FORMIK_STATE":return t.payload(e);case"SUBMIT_ATTEMPT":return $C({},e,{touched:KC(e.values,!0),isSubmitting:!0,submitCount:e.submitCount+1});case"SUBMIT_FAILURE":case"SUBMIT_SUCCESS":return $C({},e,{isSubmitting:!1});default:return e}}XC.Consumer;var tO={},nO={};function rO(e){var n=e.validateOnChange,r=void 0===n||n,i=e.validateOnBlur,o=void 0===i||i,a=e.validateOnMount,u=void 0!==a&&a,s=e.isInitialValid,l=e.enableReinitialize,c=void 0!==l&&l,f=e.onSubmit,d=BC(e,["validateOnChange","validateOnBlur","validateOnMount","isInitialValid","enableReinitialize","onSubmit"]),h=$C({validateOnChange:r,validateOnBlur:o,validateOnMount:u,onSubmit:f},d),p=t.exports.useRef(h.initialValues),m=t.exports.useRef(h.initialErrors||tO),v=t.exports.useRef(h.initialTouched||nO),y=t.exports.useRef(h.initialStatus),g=t.exports.useRef(!1),b=t.exports.useRef({});t.exports.useEffect((function(){}),[]),t.exports.useEffect((function(){return g.current=!0,function(){g.current=!1}}),[]);var w=t.exports.useReducer(eO,{values:h.initialValues,errors:h.initialErrors||tO,touched:h.initialTouched||nO,status:h.initialStatus,isSubmitting:!1,isValidating:!1,submitCount:0}),E=w[0],_=w[1],x=t.exports.useCallback((function(e,t){return new Promise((function(n,r){var i=h.validate(e,t);null==i?n(tO):YC(i)?i.then((function(e){n(e||tO)}),(function(e){r(e)})):n(i)}))}),[h.validate]),S=t.exports.useCallback((function(e,t){var n=h.validationSchema,r=VC(n)?n(t):n,i=t&&r.validateAt?r.validateAt(t,e):function(e,t,n,r){void 0===n&&(n=!1);void 0===r&&(r={});var i=oO(e);return t[n?"validateSync":"validate"](i,{abortEarly:!1,context:r})}(e,r);return new Promise((function(e,t){i.then((function(){e(tO)}),(function(n){"ValidationError"===n.name?e(function(e){var t={};if(e.inner){if(0===e.inner.length)return GC(t,e.path,e.message);var n=e.inner,r=Array.isArray(n),i=0;for(n=r?n:n[Symbol.iterator]();;){var o;if(r){if(i>=n.length)break;o=n[i++]}else{if((i=n.next()).done)break;o=i.value}var a=o;QC(t,a.path)||(t=GC(t,a.path,a.message))}}return t}(n)):t(n)}))}))}),[h.validationSchema]),k=t.exports.useCallback((function(e,t){return new Promise((function(n){return n(b.current[e].validate(t))}))}),[]),C=t.exports.useCallback((function(e){var t=Object.keys(b.current).filter((function(e){return VC(b.current[e].validate)})),n=t.length>0?t.map((function(t){return k(t,QC(e,t))})):[Promise.resolve("DO_NOT_DELETE_YOU_WILL_BE_FIRED")];return Promise.all(n).then((function(e){return e.reduce((function(e,n,r){return"DO_NOT_DELETE_YOU_WILL_BE_FIRED"===n||n&&(e=GC(e,t[r],n)),e}),{})}))}),[k]),O=t.exports.useCallback((function(e){return Promise.all([C(e),h.validationSchema?S(e):{},h.validate?x(e):{}]).then((function(e){var t=e[0],n=e[1],r=e[2];return sS.all([t,n,r],{arrayMerge:aO})}))}),[h.validate,h.validationSchema,C,x,S]),T=sO((function(e){return void 0===e&&(e=E.values),IC.exports.unstable_runWithPriority(IC.exports.LowPriority,(function(){return O(e).then((function(e){return g.current&&_({type:"SET_ERRORS",payload:e}),e})).catch((function(e){}))}))})),j=sO((function(e){return void 0===e&&(e=E.values),_({type:"SET_ISVALIDATING",payload:!0}),O(e).then((function(e){return g.current&&(_({type:"SET_ISVALIDATING",payload:!1}),nS(E.errors,e)||_({type:"SET_ERRORS",payload:e})),e}))}));t.exports.useEffect((function(){u&&!0===g.current&&T(p.current)}),[u,T]);var P=t.exports.useCallback((function(e){var t=e&&e.values?e.values:p.current,n=e&&e.errors?e.errors:m.current?m.current:h.initialErrors||{},r=e&&e.touched?e.touched:v.current?v.current:h.initialTouched||{},i=e&&e.status?e.status:y.current?y.current:h.initialStatus;p.current=t,m.current=n,v.current=r,y.current=i;var o=function(){_({type:"RESET_FORM",payload:{isSubmitting:!!e&&!!e.isSubmitting,errors:n,touched:r,status:i,values:t,isValidating:!!e&&!!e.isValidating,submitCount:e&&e.submitCount&&"number"==typeof e.submitCount?e.submitCount:0}})};if(h.onReset){var a=h.onReset(E.values,G);YC(a)?a.then(o):o()}else o()}),[h.initialErrors,h.initialStatus,h.initialTouched]);t.exports.useEffect((function(){c||(p.current=h.initialValues)}),[c,h.initialValues]),t.exports.useEffect((function(){c&&!0===g.current&&!nS(p.current,h.initialValues)&&(p.current=h.initialValues,P())}),[c,h.initialValues,P]),t.exports.useEffect((function(){c&&!0===g.current&&!nS(m.current,h.initialErrors)&&(m.current=h.initialErrors||tO,_({type:"SET_ERRORS",payload:h.initialErrors||tO}))}),[c,h.initialErrors]),t.exports.useEffect((function(){c&&!0===g.current&&!nS(v.current,h.initialTouched)&&(v.current=h.initialTouched||nO,_({type:"SET_TOUCHED",payload:h.initialTouched||nO}))}),[c,h.initialTouched]),t.exports.useEffect((function(){c&&!0===g.current&&!nS(y.current,h.initialStatus)&&(y.current=h.initialStatus,_({type:"SET_STATUS",payload:h.initialStatus}))}),[c,h.initialStatus,h.initialTouched]);var F=sO((function(e){if(VC(b.current[e].validate)){var t=QC(E.values,e),n=b.current[e].validate(t);return YC(n)?(_({type:"SET_ISVALIDATING",payload:!0}),n.then((function(e){return e})).then((function(t){_({type:"SET_FIELD_ERROR",payload:{field:e,value:t}}),_({type:"SET_ISVALIDATING",payload:!1})}))):(_({type:"SET_FIELD_ERROR",payload:{field:e,value:n}}),Promise.resolve(n))}return h.validationSchema?(_({type:"SET_ISVALIDATING",payload:!0}),S(E.values,e).then((function(e){return e})).then((function(t){_({type:"SET_FIELD_ERROR",payload:{field:e,value:t[e]}}),_({type:"SET_ISVALIDATING",payload:!1})}))):Promise.resolve()})),A=t.exports.useCallback((function(e,t){var n=t.validate;b.current[e]={validate:n}}),[]),D=t.exports.useCallback((function(e){delete b.current[e]}),[]),N=sO((function(e,t){return _({type:"SET_TOUCHED",payload:e}),(void 0===t?o:t)?T(E.values):Promise.resolve()})),M=t.exports.useCallback((function(e){_({type:"SET_ERRORS",payload:e})}),[]),L=sO((function(e,t){return _({type:"SET_VALUES",payload:e}),(void 0===t?r:t)?T(e):Promise.resolve()})),z=t.exports.useCallback((function(e,t){_({type:"SET_FIELD_ERROR",payload:{field:e,value:t}})}),[]),R=sO((function(e,t,n){return _({type:"SET_FIELD_VALUE",payload:{field:e,value:t}}),(void 0===n?r:n)?T(GC(E.values,e,t)):Promise.resolve()})),I=t.exports.useCallback((function(e,t){var n,r=t,i=e;if(!HC(e)){e.persist&&e.persist();var o=e.target?e.target:e.currentTarget,a=o.type,u=o.name,s=o.id,l=o.value,c=o.checked,f=(o.outerHTML,o.options),d=o.multiple;r=t||(u||s),i=/number|range/.test(a)?(n=parseFloat(l),isNaN(n)?"":n):/checkbox/.test(a)?function(e,t,n){if("boolean"==typeof e)return Boolean(t);var r=[],i=!1,o=-1;if(Array.isArray(e))r=e,i=(o=e.indexOf(n))>=0;else if(!n||"true"==n||"false"==n)return Boolean(t);if(t&&n&&!i)return r.concat(n);if(!i)return r;return r.slice(0,o).concat(r.slice(o+1))}(QC(E.values,r),c,l):d?function(e){return Array.from(e).filter((function(e){return e.selected})).map((function(e){return e.value}))}(f):l}r&&R(r,i)}),[R,E.values]),U=sO((function(e){if(HC(e))return function(t){return I(t,e)};I(e)})),$=sO((function(e,t,n){return void 0===t&&(t=!0),_({type:"SET_FIELD_TOUCHED",payload:{field:e,value:t}}),(void 0===n?o:n)?T(E.values):Promise.resolve()})),B=t.exports.useCallback((function(e,t){e.persist&&e.persist();var n=e.target,r=n.name,i=n.id,o=(n.outerHTML,t||(r||i));$(o,!0)}),[$]),V=sO((function(e){if(HC(e))return function(t){return B(t,e)};B(e)})),q=t.exports.useCallback((function(e){VC(e)?_({type:"SET_FORMIK_STATE",payload:e}):_({type:"SET_FORMIK_STATE",payload:function(){return e}})}),[]),W=t.exports.useCallback((function(e){_({type:"SET_STATUS",payload:e})}),[]),H=t.exports.useCallback((function(e){_({type:"SET_ISSUBMITTING",payload:e})}),[]),Y=sO((function(){return _({type:"SUBMIT_ATTEMPT"}),j().then((function(e){var t=e instanceof Error;if(!t&&0===Object.keys(e).length){var n;try{if(void 0===(n=K()))return}catch(r){throw r}return Promise.resolve(n).then((function(){g.current&&_({type:"SUBMIT_SUCCESS"})})).catch((function(e){if(g.current)throw _({type:"SUBMIT_FAILURE"}),e}))}if(g.current&&(_({type:"SUBMIT_FAILURE"}),t))throw e}))})),Q=sO((function(e){e&&e.preventDefault&&VC(e.preventDefault)&&e.preventDefault(),e&&e.stopPropagation&&VC(e.stopPropagation)&&e.stopPropagation(),Y().catch((function(e){console.warn("Warning: An unhandled error was caught from submitForm()",e)}))})),G={resetForm:P,validateForm:j,validateField:F,setErrors:M,setFieldError:z,setFieldTouched:$,setFieldValue:R,setStatus:W,setSubmitting:H,setTouched:N,setValues:L,setFormikState:q,submitForm:Y},K=sO((function(){return f(E.values,G)})),X=sO((function(e){e&&e.preventDefault&&VC(e.preventDefault)&&e.preventDefault(),e&&e.stopPropagation&&VC(e.stopPropagation)&&e.stopPropagation(),P()})),Z=t.exports.useCallback((function(e){return{value:QC(E.values,e),error:QC(E.errors,e),touched:!!QC(E.touched,e),initialValue:QC(p.current,e),initialTouched:!!QC(v.current,e),initialError:QC(m.current,e)}}),[E.errors,E.touched,E.values]),J=t.exports.useCallback((function(e){return{setValue:function(t){return R(e,t)},setTouched:function(t){return $(e,t)},setError:function(t){return z(e,t)}}}),[R,$,z]),ee=t.exports.useCallback((function(e){var t=qC(e),n=t?e.name:e,r=QC(E.values,n),i={name:n,value:r,onChange:U,onBlur:V};if(t){var o=e.type,a=e.value,u=e.as,s=e.multiple;"checkbox"===o?void 0===a?i.checked=!!r:(i.checked=!(!Array.isArray(r)||!~r.indexOf(a)),i.value=a):"radio"===o?(i.checked=r===a,i.value=a):"select"===u&&s&&(i.value=i.value||[],i.multiple=!0)}return i}),[V,U,E.values]),te=t.exports.useMemo((function(){return!nS(p.current,E.values)}),[p.current,E.values]),ne=t.exports.useMemo((function(){return void 0!==s?te?E.errors&&0===Object.keys(E.errors).length:!1!==s&&VC(s)?s(h):s:E.errors&&0===Object.keys(E.errors).length}),[s,te,E.errors,h]);return $C({},E,{initialValues:p.current,initialErrors:m.current,initialTouched:v.current,initialStatus:y.current,handleBlur:V,handleChange:U,handleReset:X,handleSubmit:Q,resetForm:P,setErrors:M,setFormikState:q,setFieldTouched:$,setFieldValue:R,setFieldError:z,setStatus:W,setSubmitting:H,setTouched:N,setValues:L,submitForm:Y,validateForm:j,validateField:F,isValid:ne,dirty:te,unregisterField:D,registerField:A,getFieldProps:ee,getFieldMeta:Z,getFieldHelpers:J,validateOnBlur:o,validateOnChange:r,validateOnMount:u})}function iO(e){var n=rO(e),r=e.component,i=e.children,o=e.render,a=e.innerRef;return t.exports.useImperativeHandle(a,(function(){return n})),t.exports.useEffect((function(){}),[]),t.exports.createElement(ZC,{value:n},r?t.exports.createElement(r,n):o?o(n):i?VC(i)?i(n):function(e){return 0===t.exports.Children.count(e)}(i)?null:t.exports.Children.only(i):null)}function oO(e){var t={};for(var n in e)if(Object.prototype.hasOwnProperty.call(e,n)){var r=String(n);!0===Array.isArray(e[r])?t[r]=e[r].map((function(e){return!0===Array.isArray(e)||TS(e)?oO(e):""!==e?e:void 0})):TS(e[r])?t[r]=oO(e[r]):t[r]=""!==e[r]?e[r]:void 0}return t}function aO(e,t,n){var r=e.slice();return t.forEach((function(t,i){if(void 0===r[i]){var o=!1!==n.clone&&n.isMergeableObject(t);r[i]=o?sS(Array.isArray(t)?[]:{},t,n):t}else n.isMergeableObject(t)?r[i]=sS(e[i],t,n):-1===e.indexOf(t)&&r.push(t)})),r}var uO="undefined"!=typeof window&&void 0!==window.document&&void 0!==window.document.createElement?t.exports.useLayoutEffect:t.exports.useEffect;function sO(e){var n=t.exports.useRef(e);return uO((function(){n.current=e})),t.exports.useCallback((function(){for(var e=arguments.length,t=new Array(e),r=0;r<e;r++)t[r]=arguments[r];return n.current.apply(void 0,t)}),[])}function lO(e){var n=JC(),r=n.getFieldProps,i=n.getFieldMeta,o=n.getFieldHelpers,a=n.registerField,u=n.unregisterField,s=qC(e)?e:{name:e},l=s.name,c=s.validate;return t.exports.useEffect((function(){return l&&a(l,{validate:c}),function(){l&&u(l)}}),[a,u,l,c]),[r(s),i(l),o(l)]}function cO(e){var n=e.validate,r=e.name,i=e.render,o=e.children,a=e.as,u=e.component,s=BC(e,["validate","name","render","children","as","component"]),l=BC(JC(),["validate","validationSchema"]);t.exports.useEffect((function(){}),[]);var c=l.registerField,f=l.unregisterField;t.exports.useEffect((function(){return c(r,{validate:n}),function(){f(r)}}),[c,f,r,n]);var d=l.getFieldProps($C({name:r},s)),h=l.getFieldMeta(r),p={field:d,form:l};if(i)return i($C({},p,{meta:h}));if(VC(o))return o($C({},p,{meta:h}));if(u){if("string"==typeof u){var m=s.innerRef,v=BC(s,["innerRef"]);return t.exports.createElement(u,$C({ref:m},d,{},v),o)}return t.exports.createElement(u,$C({field:d,form:l},s),o)}var y=a||"input";if("string"==typeof y){var g=s.innerRef,b=BC(s,["innerRef"]);return t.exports.createElement(y,$C({ref:g},d,{},b),o)}return t.exports.createElement(y,$C({},d,{},s),o)}function fO(e){if(null===e||!0===e||!1===e)return NaN;var t=Number(e);return isNaN(t)?t:t<0?Math.ceil(t):Math.floor(t)}function dO(e,t){if(t.length<e)throw new TypeError(e+" argument"+(e>1?"s":"")+" required, but only "+t.length+" present")}function hO(e){dO(1,arguments);var t=Object.prototype.toString.call(e);return e instanceof Date||"object"==typeof e&&"[object Date]"===t?new Date(e.getTime()):"number"==typeof e||"[object Number]"===t?new Date(e):("string"!=typeof e&&"[object String]"!==t||"undefined"==typeof console||(console.warn("Starting with v2.0.0-beta.1 date-fns doesn't accept strings as date arguments. Please use `parseISO` to parse strings. See: https://git.io/fjule"),console.warn((new Error).stack)),new Date(NaN))}function pO(e,t){dO(2,arguments);var n=hO(e),r=fO(t);return isNaN(r)?new Date(NaN):r?(n.setDate(n.getDate()+r),n):n}function mO(e,t){dO(2,arguments);var n=hO(e).getTime(),r=fO(t);return new Date(n+r)}function vO(e){var t=new Date(Date.UTC(e.getFullYear(),e.getMonth(),e.getDate(),e.getHours(),e.getMinutes(),e.getSeconds(),e.getMilliseconds()));return t.setUTCFullYear(e.getFullYear()),e.getTime()-t.getTime()}function yO(e){dO(1,arguments);var t=hO(e);return!isNaN(t)}t.exports.forwardRef((function(e,n){var r=e.action,i=BC(e,["action"]),o=r||"#",a=JC(),u=a.handleReset,s=a.handleSubmit;return t.exports.createElement("form",Object.assign({onSubmit:s,ref:n,onReset:u,action:o},i))})).displayName="Form";var gO={lessThanXSeconds:{one:"less than a second",other:"less than {{count}} seconds"},xSeconds:{one:"1 second",other:"{{count}} seconds"},halfAMinute:"half a minute",lessThanXMinutes:{one:"less than a minute",other:"less than {{count}} minutes"},xMinutes:{one:"1 minute",other:"{{count}} minutes"},aboutXHours:{one:"about 1 hour",other:"about {{count}} hours"},xHours:{one:"1 hour",other:"{{count}} hours"},xDays:{one:"1 day",other:"{{count}} days"},aboutXWeeks:{one:"about 1 week",other:"about {{count}} weeks"},xWeeks:{one:"1 week",other:"{{count}} weeks"},aboutXMonths:{one:"about 1 month",other:"about {{count}} months"},xMonths:{one:"1 month",other:"{{count}} months"},aboutXYears:{one:"about 1 year",other:"about {{count}} years"},xYears:{one:"1 year",other:"{{count}} years"},overXYears:{one:"over 1 year",other:"over {{count}} years"},almostXYears:{one:"almost 1 year",other:"almost {{count}} years"}};function bO(e){return function(){var t=arguments.length>0&&void 0!==arguments[0]?arguments[0]:{},n=t.width?String(t.width):e.defaultWidth,r=e.formats[n]||e.formats[e.defaultWidth];return r}}var wO={date:bO({formats:{full:"EEEE, MMMM do, y",long:"MMMM do, y",medium:"MMM d, y",short:"MM/dd/yyyy"},defaultWidth:"full"}),time:bO({formats:{full:"h:mm:ss a zzzz",long:"h:mm:ss a z",medium:"h:mm:ss a",short:"h:mm a"},defaultWidth:"full"}),dateTime:bO({formats:{full:"{{date}} 'at' {{time}}",long:"{{date}} 'at' {{time}}",medium:"{{date}}, {{time}}",short:"{{date}}, {{time}}"},defaultWidth:"full"})},EO={lastWeek:"'last' eeee 'at' p",yesterday:"'yesterday at' p",today:"'today at' p",tomorrow:"'tomorrow at' p",nextWeek:"eeee 'at' p",other:"P"};function _O(e){return function(t,n){var r,i=n||{};if("formatting"===(i.context?String(i.context):"standalone")&&e.formattingValues){var o=e.defaultFormattingWidth||e.defaultWidth,a=i.width?String(i.width):o;r=e.formattingValues[a]||e.formattingValues[o]}else{var u=e.defaultWidth,s=i.width?String(i.width):e.defaultWidth;r=e.values[s]||e.values[u]}return r[e.argumentCallback?e.argumentCallback(t):t]}}function xO(e){return function(t){var n=arguments.length>1&&void 0!==arguments[1]?arguments[1]:{},r=n.width,i=r&&e.matchPatterns[r]||e.matchPatterns[e.defaultMatchWidth],o=t.match(i);if(!o)return null;var a,u=o[0],s=r&&e.parsePatterns[r]||e.parsePatterns[e.defaultParseWidth],l=Array.isArray(s)?kO(s,(function(e){return e.test(u)})):SO(s,(function(e){return e.test(u)}));a=e.valueCallback?e.valueCallback(l):l,a=n.valueCallback?n.valueCallback(a):a;var c=t.slice(u.length);return{value:a,rest:c}}}function SO(e,t){for(var n in e)if(e.hasOwnProperty(n)&&t(e[n]))return n}function kO(e,t){for(var n=0;n<e.length;n++)if(t(e[n]))return n}var CO,OO={code:"en-US",formatDistance:function(e,t,n){var r;return n=n||{},r="string"==typeof gO[e]?gO[e]:1===t?gO[e].one:gO[e].other.replace("{{count}}",t),n.addSuffix?n.comparison>0?"in "+r:r+" ago":r},formatLong:wO,formatRelative:function(e,t,n,r){return EO[e]},localize:{ordinalNumber:function(e,t){var n=Number(e),r=n%100;if(r>20||r<10)switch(r%10){case 1:return n+"st";case 2:return n+"nd";case 3:return n+"rd"}return n+"th"},era:_O({values:{narrow:["B","A"],abbreviated:["BC","AD"],wide:["Before Christ","Anno Domini"]},defaultWidth:"wide"}),quarter:_O({values:{narrow:["1","2","3","4"],abbreviated:["Q1","Q2","Q3","Q4"],wide:["1st quarter","2nd quarter","3rd quarter","4th quarter"]},defaultWidth:"wide",argumentCallback:function(e){return Number(e)-1}}),month:_O({values:{narrow:["J","F","M","A","M","J","J","A","S","O","N","D"],abbreviated:["Jan","Feb","Mar","Apr","May","Jun","Jul","Aug","Sep","Oct","Nov","Dec"],wide:["January","February","March","April","May","June","July","August","September","October","November","December"]},defaultWidth:"wide"}),day:_O({values:{narrow:["S","M","T","W","T","F","S"],short:["Su","Mo","Tu","We","Th","Fr","Sa"],abbreviated:["Sun","Mon","Tue","Wed","Thu","Fri","Sat"],wide:["Sunday","Monday","Tuesday","Wednesday","Thursday","Friday","Saturday"]},defaultWidth:"wide"}),dayPeriod:_O({values:{narrow:{am:"a",pm:"p",midnight:"mi",noon:"n",morning:"morning",afternoon:"afternoon",evening:"evening",night:"night"},abbreviated:{am:"AM",pm:"PM",midnight:"midnight",noon:"noon",morning:"morning",afternoon:"afternoon",evening:"evening",night:"night"},wide:{am:"a.m.",pm:"p.m.",midnight:"midnight",noon:"noon",morning:"morning",afternoon:"afternoon",evening:"evening",night:"night"}},defaultWidth:"wide",formattingValues:{narrow:{am:"a",pm:"p",midnight:"mi",noon:"n",morning:"in the morning",afternoon:"in the afternoon",evening:"in the evening",night:"at night"},abbreviated:{am:"AM",pm:"PM",midnight:"midnight",noon:"noon",morning:"in the morning",afternoon:"in the afternoon",evening:"in the evening",night:"at night"},wide:{am:"a.m.",pm:"p.m.",midnight:"midnight",noon:"noon",morning:"in the morning",afternoon:"in the afternoon",evening:"in the evening",night:"at night"}},defaultFormattingWidth:"wide"})},match:{ordinalNumber:(CO={matchPattern:/^(\d+)(th|st|nd|rd)?/i,parsePattern:/\d+/i,valueCallback:function(e){return parseInt(e,10)}},function(e){var t=arguments.length>1&&void 0!==arguments[1]?arguments[1]:{},n=e.match(CO.matchPattern);if(!n)return null;var r=n[0],i=e.match(CO.parsePattern);if(!i)return null;var o=CO.valueCallback?CO.valueCallback(i[0]):i[0];o=t.valueCallback?t.valueCallback(o):o;var a=e.slice(r.length);return{value:o,rest:a}}),era:xO({matchPatterns:{narrow:/^(b|a)/i,abbreviated:/^(b\.?\s?c\.?|b\.?\s?c\.?\s?e\.?|a\.?\s?d\.?|c\.?\s?e\.?)/i,wide:/^(before christ|before common era|anno domini|common era)/i},defaultMatchWidth:"wide",parsePatterns:{any:[/^b/i,/^(a|c)/i]},defaultParseWidth:"any"}),quarter:xO({matchPatterns:{narrow:/^[1234]/i,abbreviated:/^q[1234]/i,wide:/^[1234](th|st|nd|rd)? quarter/i},defaultMatchWidth:"wide",parsePatterns:{any:[/1/i,/2/i,/3/i,/4/i]},defaultParseWidth:"any",valueCallback:function(e){return e+1}}),month:xO({matchPatterns:{narrow:/^[jfmasond]/i,abbreviated:/^(jan|feb|mar|apr|may|jun|jul|aug|sep|oct|nov|dec)/i,wide:/^(january|february|march|april|may|june|july|august|september|october|november|december)/i},defaultMatchWidth:"wide",parsePatterns:{narrow:[/^j/i,/^f/i,/^m/i,/^a/i,/^m/i,/^j/i,/^j/i,/^a/i,/^s/i,/^o/i,/^n/i,/^d/i],any:[/^ja/i,/^f/i,/^mar/i,/^ap/i,/^may/i,/^jun/i,/^jul/i,/^au/i,/^s/i,/^o/i,/^n/i,/^d/i]},defaultParseWidth:"any"}),day:xO({matchPatterns:{narrow:/^[smtwf]/i,short:/^(su|mo|tu|we|th|fr|sa)/i,abbreviated:/^(sun|mon|tue|wed|thu|fri|sat)/i,wide:/^(sunday|monday|tuesday|wednesday|thursday|friday|saturday)/i},defaultMatchWidth:"wide",parsePatterns:{narrow:[/^s/i,/^m/i,/^t/i,/^w/i,/^t/i,/^f/i,/^s/i],any:[/^su/i,/^m/i,/^tu/i,/^w/i,/^th/i,/^f/i,/^sa/i]},defaultParseWidth:"any"}),dayPeriod:xO({matchPatterns:{narrow:/^(a|p|mi|n|(in the|at) (morning|afternoon|evening|night))/i,any:/^([ap]\.?\s?m\.?|midnight|noon|(in the|at) (morning|afternoon|evening|night))/i},defaultMatchWidth:"any",parsePatterns:{any:{am:/^a/i,pm:/^p/i,midnight:/^mi/i,noon:/^no/i,morning:/morning/i,afternoon:/afternoon/i,evening:/evening/i,night:/night/i}},defaultParseWidth:"any"})},options:{weekStartsOn:0,firstWeekContainsDate:1}};function TO(e,t){dO(2,arguments);var n=fO(t);return mO(e,-n)}function jO(e,t){for(var n=e<0?"-":"",r=Math.abs(e).toString();r.length<t;)r="0"+r;return n+r}var PO=function(e,t){var n=e.getUTCFullYear(),r=n>0?n:1-n;return jO("yy"===t?r%100:r,t.length)},FO=function(e,t){var n=e.getUTCMonth();return"M"===t?String(n+1):jO(n+1,2)},AO=function(e,t){return jO(e.getUTCDate(),t.length)},DO=function(e,t){return jO(e.getUTCHours()%12||12,t.length)},NO=function(e,t){return jO(e.getUTCHours(),t.length)},MO=function(e,t){return jO(e.getUTCMinutes(),t.length)},LO=function(e,t){return jO(e.getUTCSeconds(),t.length)},zO=function(e,t){var n=t.length,r=e.getUTCMilliseconds();return jO(Math.floor(r*Math.pow(10,n-3)),t.length)};function RO(e){dO(1,arguments);var t=1,n=hO(e),r=n.getUTCDay(),i=(r<t?7:0)+r-t;return n.setUTCDate(n.getUTCDate()-i),n.setUTCHours(0,0,0,0),n}function IO(e){dO(1,arguments);var t=hO(e),n=t.getUTCFullYear(),r=new Date(0);r.setUTCFullYear(n+1,0,4),r.setUTCHours(0,0,0,0);var i=RO(r),o=new Date(0);o.setUTCFullYear(n,0,4),o.setUTCHours(0,0,0,0);var a=RO(o);return t.getTime()>=i.getTime()?n+1:t.getTime()>=a.getTime()?n:n-1}function UO(e){dO(1,arguments);var t=IO(e),n=new Date(0);n.setUTCFullYear(t,0,4),n.setUTCHours(0,0,0,0);var r=RO(n);return r}function $O(e,t){dO(1,arguments);var n=t||{},r=n.locale,i=r&&r.options&&r.options.weekStartsOn,o=null==i?0:fO(i),a=null==n.weekStartsOn?o:fO(n.weekStartsOn);if(!(a>=0&&a<=6))throw new RangeError("weekStartsOn must be between 0 and 6 inclusively");var u=hO(e),s=u.getUTCDay(),l=(s<a?7:0)+s-a;return u.setUTCDate(u.getUTCDate()-l),u.setUTCHours(0,0,0,0),u}function BO(e,t){dO(1,arguments);var n=hO(e,t),r=n.getUTCFullYear(),i=t||{},o=i.locale,a=o&&o.options&&o.options.firstWeekContainsDate,u=null==a?1:fO(a),s=null==i.firstWeekContainsDate?u:fO(i.firstWeekContainsDate);if(!(s>=1&&s<=7))throw new RangeError("firstWeekContainsDate must be between 1 and 7 inclusively");var l=new Date(0);l.setUTCFullYear(r+1,0,s),l.setUTCHours(0,0,0,0);var c=$O(l,t),f=new Date(0);f.setUTCFullYear(r,0,s),f.setUTCHours(0,0,0,0);var d=$O(f,t);return n.getTime()>=c.getTime()?r+1:n.getTime()>=d.getTime()?r:r-1}function VO(e,t){dO(1,arguments);var n=t||{},r=n.locale,i=r&&r.options&&r.options.firstWeekContainsDate,o=null==i?1:fO(i),a=null==n.firstWeekContainsDate?o:fO(n.firstWeekContainsDate),u=BO(e,t),s=new Date(0);s.setUTCFullYear(u,0,a),s.setUTCHours(0,0,0,0);var l=$O(s,t);return l}var qO="midnight",WO="noon",HO="morning",YO="afternoon",QO="evening",GO="night",KO={G:function(e,t,n){var r=e.getUTCFullYear()>0?1:0;switch(t){case"G":case"GG":case"GGG":return n.era(r,{width:"abbreviated"});case"GGGGG":return n.era(r,{width:"narrow"});case"GGGG":default:return n.era(r,{width:"wide"})}},y:function(e,t,n){if("yo"===t){var r=e.getUTCFullYear(),i=r>0?r:1-r;return n.ordinalNumber(i,{unit:"year"})}return PO(e,t)},Y:function(e,t,n,r){var i=BO(e,r),o=i>0?i:1-i;return"YY"===t?jO(o%100,2):"Yo"===t?n.ordinalNumber(o,{unit:"year"}):jO(o,t.length)},R:function(e,t){return jO(IO(e),t.length)},u:function(e,t){return jO(e.getUTCFullYear(),t.length)},Q:function(e,t,n){var r=Math.ceil((e.getUTCMonth()+1)/3);switch(t){case"Q":return String(r);case"QQ":return jO(r,2);case"Qo":return n.ordinalNumber(r,{unit:"quarter"});case"QQQ":return n.quarter(r,{width:"abbreviated",context:"formatting"});case"QQQQQ":return n.quarter(r,{width:"narrow",context:"formatting"});case"QQQQ":default:return n.quarter(r,{width:"wide",context:"formatting"})}},q:function(e,t,n){var r=Math.ceil((e.getUTCMonth()+1)/3);switch(t){case"q":return String(r);case"qq":return jO(r,2);case"qo":return n.ordinalNumber(r,{unit:"quarter"});case"qqq":return n.quarter(r,{width:"abbreviated",context:"standalone"});case"qqqqq":return n.quarter(r,{width:"narrow",context:"standalone"});case"qqqq":default:return n.quarter(r,{width:"wide",context:"standalone"})}},M:function(e,t,n){var r=e.getUTCMonth();switch(t){case"M":case"MM":return FO(e,t);case"Mo":return n.ordinalNumber(r+1,{unit:"month"});case"MMM":return n.month(r,{width:"abbreviated",context:"formatting"});case"MMMMM":return n.month(r,{width:"narrow",context:"formatting"});case"MMMM":default:return n.month(r,{width:"wide",context:"formatting"})}},L:function(e,t,n){var r=e.getUTCMonth();switch(t){case"L":return String(r+1);case"LL":return jO(r+1,2);case"Lo":return n.ordinalNumber(r+1,{unit:"month"});case"LLL":return n.month(r,{width:"abbreviated",context:"standalone"});case"LLLLL":return n.month(r,{width:"narrow",context:"standalone"});case"LLLL":default:return n.month(r,{width:"wide",context:"standalone"})}},w:function(e,t,n,r){var i=function(e,t){dO(1,arguments);var n=hO(e),r=$O(n,t).getTime()-VO(n,t).getTime();return Math.round(r/6048e5)+1}(e,r);return"wo"===t?n.ordinalNumber(i,{unit:"week"}):jO(i,t.length)},I:function(e,t,n){var r=function(e){dO(1,arguments);var t=hO(e),n=RO(t).getTime()-UO(t).getTime();return Math.round(n/6048e5)+1}(e);return"Io"===t?n.ordinalNumber(r,{unit:"week"}):jO(r,t.length)},d:function(e,t,n){return"do"===t?n.ordinalNumber(e.getUTCDate(),{unit:"date"}):AO(e,t)},D:function(e,t,n){var r=function(e){dO(1,arguments);var t=hO(e),n=t.getTime();t.setUTCMonth(0,1),t.setUTCHours(0,0,0,0);var r=t.getTime(),i=n-r;return Math.floor(i/864e5)+1}(e);return"Do"===t?n.ordinalNumber(r,{unit:"dayOfYear"}):jO(r,t.length)},E:function(e,t,n){var r=e.getUTCDay();switch(t){case"E":case"EE":case"EEE":return n.day(r,{width:"abbreviated",context:"formatting"});case"EEEEE":return n.day(r,{width:"narrow",context:"formatting"});case"EEEEEE":return n.day(r,{width:"short",context:"formatting"});case"EEEE":default:return n.day(r,{width:"wide",context:"formatting"})}},e:function(e,t,n,r){var i=e.getUTCDay(),o=(i-r.weekStartsOn+8)%7||7;switch(t){case"e":return String(o);case"ee":return jO(o,2);case"eo":return n.ordinalNumber(o,{unit:"day"});case"eee":return n.day(i,{width:"abbreviated",context:"formatting"});case"eeeee":return n.day(i,{width:"narrow",context:"formatting"});case"eeeeee":return n.day(i,{width:"short",context:"formatting"});case"eeee":default:return n.day(i,{width:"wide",context:"formatting"})}},c:function(e,t,n,r){var i=e.getUTCDay(),o=(i-r.weekStartsOn+8)%7||7;switch(t){case"c":return String(o);case"cc":return jO(o,t.length);case"co":return n.ordinalNumber(o,{unit:"day"});case"ccc":return n.day(i,{width:"abbreviated",context:"standalone"});case"ccccc":return n.day(i,{width:"narrow",context:"standalone"});case"cccccc":return n.day(i,{width:"short",context:"standalone"});case"cccc":default:return n.day(i,{width:"wide",context:"standalone"})}},i:function(e,t,n){var r=e.getUTCDay(),i=0===r?7:r;switch(t){case"i":return String(i);case"ii":return jO(i,t.length);case"io":return n.ordinalNumber(i,{unit:"day"});case"iii":return n.day(r,{width:"abbreviated",context:"formatting"});case"iiiii":return n.day(r,{width:"narrow",context:"formatting"});case"iiiiii":return n.day(r,{width:"short",context:"formatting"});case"iiii":default:return n.day(r,{width:"wide",context:"formatting"})}},a:function(e,t,n){var r=e.getUTCHours()/12>=1?"pm":"am";switch(t){case"a":case"aa":return n.dayPeriod(r,{width:"abbreviated",context:"formatting"});case"aaa":return n.dayPeriod(r,{width:"abbreviated",context:"formatting"}).toLowerCase();case"aaaaa":return n.dayPeriod(r,{width:"narrow",context:"formatting"});case"aaaa":default:return n.dayPeriod(r,{width:"wide",context:"formatting"})}},b:function(e,t,n){var r,i=e.getUTCHours();switch(r=12===i?WO:0===i?qO:i/12>=1?"pm":"am",t){case"b":case"bb":return n.dayPeriod(r,{width:"abbreviated",context:"formatting"});case"bbb":return n.dayPeriod(r,{width:"abbreviated",context:"formatting"}).toLowerCase();case"bbbbb":return n.dayPeriod(r,{width:"narrow",context:"formatting"});case"bbbb":default:return n.dayPeriod(r,{width:"wide",context:"formatting"})}},B:function(e,t,n){var r,i=e.getUTCHours();switch(r=i>=17?QO:i>=12?YO:i>=4?HO:GO,t){case"B":case"BB":case"BBB":return n.dayPeriod(r,{width:"abbreviated",context:"formatting"});case"BBBBB":return n.dayPeriod(r,{width:"narrow",context:"formatting"});case"BBBB":default:return n.dayPeriod(r,{width:"wide",context:"formatting"})}},h:function(e,t,n){if("ho"===t){var r=e.getUTCHours()%12;return 0===r&&(r=12),n.ordinalNumber(r,{unit:"hour"})}return DO(e,t)},H:function(e,t,n){return"Ho"===t?n.ordinalNumber(e.getUTCHours(),{unit:"hour"}):NO(e,t)},K:function(e,t,n){var r=e.getUTCHours()%12;return"Ko"===t?n.ordinalNumber(r,{unit:"hour"}):jO(r,t.length)},k:function(e,t,n){var r=e.getUTCHours();return 0===r&&(r=24),"ko"===t?n.ordinalNumber(r,{unit:"hour"}):jO(r,t.length)},m:function(e,t,n){return"mo"===t?n.ordinalNumber(e.getUTCMinutes(),{unit:"minute"}):MO(e,t)},s:function(e,t,n){return"so"===t?n.ordinalNumber(e.getUTCSeconds(),{unit:"second"}):LO(e,t)},S:function(e,t){return zO(e,t)},X:function(e,t,n,r){var i=(r._originalDate||e).getTimezoneOffset();if(0===i)return"Z";switch(t){case"X":return ZO(i);case"XXXX":case"XX":return JO(i);case"XXXXX":case"XXX":default:return JO(i,":")}},x:function(e,t,n,r){var i=(r._originalDate||e).getTimezoneOffset();switch(t){case"x":return ZO(i);case"xxxx":case"xx":return JO(i);case"xxxxx":case"xxx":default:return JO(i,":")}},O:function(e,t,n,r){var i=(r._originalDate||e).getTimezoneOffset();switch(t){case"O":case"OO":case"OOO":return"GMT"+XO(i,":");case"OOOO":default:return"GMT"+JO(i,":")}},z:function(e,t,n,r){var i=(r._originalDate||e).getTimezoneOffset();switch(t){case"z":case"zz":case"zzz":return"GMT"+XO(i,":");case"zzzz":default:return"GMT"+JO(i,":")}},t:function(e,t,n,r){var i=r._originalDate||e;return jO(Math.floor(i.getTime()/1e3),t.length)},T:function(e,t,n,r){return jO((r._originalDate||e).getTime(),t.length)}};function XO(e,t){var n=e>0?"-":"+",r=Math.abs(e),i=Math.floor(r/60),o=r%60;if(0===o)return n+String(i);var a=t||"";return n+String(i)+a+jO(o,2)}function ZO(e,t){return e%60==0?(e>0?"-":"+")+jO(Math.abs(e)/60,2):JO(e,t)}function JO(e,t){var n=t||"",r=e>0?"-":"+",i=Math.abs(e);return r+jO(Math.floor(i/60),2)+n+jO(i%60,2)}function eT(e,t){switch(e){case"P":return t.date({width:"short"});case"PP":return t.date({width:"medium"});case"PPP":return t.date({width:"long"});case"PPPP":default:return t.date({width:"full"})}}function tT(e,t){switch(e){case"p":return t.time({width:"short"});case"pp":return t.time({width:"medium"});case"ppp":return t.time({width:"long"});case"pppp":default:return t.time({width:"full"})}}var nT={p:tT,P:function(e,t){var n,r=e.match(/(P+)(p+)?/),i=r[1],o=r[2];if(!o)return eT(e,t);switch(i){case"P":n=t.dateTime({width:"short"});break;case"PP":n=t.dateTime({width:"medium"});break;case"PPP":n=t.dateTime({width:"long"});break;case"PPPP":default:n=t.dateTime({width:"full"})}return n.replace("{{date}}",eT(i,t)).replace("{{time}}",tT(o,t))}},rT=["D","DD"],iT=["YY","YYYY"];function oT(e){return-1!==rT.indexOf(e)}function aT(e){return-1!==iT.indexOf(e)}function uT(e,t,n){if("YYYY"===e)throw new RangeError("Use `yyyy` instead of `YYYY` (in `".concat(t,"`) for formatting years to the input `").concat(n,"`; see: https://git.io/fxCyr"));if("YY"===e)throw new RangeError("Use `yy` instead of `YY` (in `".concat(t,"`) for formatting years to the input `").concat(n,"`; see: https://git.io/fxCyr"));if("D"===e)throw new RangeError("Use `d` instead of `D` (in `".concat(t,"`) for formatting days of the month to the input `").concat(n,"`; see: https://git.io/fxCyr"));if("DD"===e)throw new RangeError("Use `dd` instead of `DD` (in `".concat(t,"`) for formatting days of the month to the input `").concat(n,"`; see: https://git.io/fxCyr"))}var sT=/[yYQqMLwIdDecihHKkms]o|(\w)\1*|''|'(''|[^'])+('|$)|./g,lT=/P+p+|P+|p+|''|'(''|[^'])+('|$)|./g,cT=/^'([^]*?)'?$/,fT=/''/g,dT=/[a-zA-Z]/;function hT(e,t,n){dO(2,arguments);var r=String(t),i=n||{},o=i.locale||OO,a=o.options&&o.options.firstWeekContainsDate,u=null==a?1:fO(a),s=null==i.firstWeekContainsDate?u:fO(i.firstWeekContainsDate);if(!(s>=1&&s<=7))throw new RangeError("firstWeekContainsDate must be between 1 and 7 inclusively");var l=o.options&&o.options.weekStartsOn,c=null==l?0:fO(l),f=null==i.weekStartsOn?c:fO(i.weekStartsOn);if(!(f>=0&&f<=6))throw new RangeError("weekStartsOn must be between 0 and 6 inclusively");if(!o.localize)throw new RangeError("locale must contain localize property");if(!o.formatLong)throw new RangeError("locale must contain formatLong property");var d=hO(e);if(!yO(d))throw new RangeError("Invalid time value");var h=vO(d),p=TO(d,h),m={firstWeekContainsDate:s,weekStartsOn:f,locale:o,_originalDate:d},v=r.match(lT).map((function(e){var t=e[0];return"p"===t||"P"===t?(0,nT[t])(e,o.formatLong,m):e})).join("").match(sT).map((function(n){if("''"===n)return"'";var r=n[0];if("'"===r)return pT(n);var a=KO[r];if(a)return!i.useAdditionalWeekYearTokens&&aT(n)&&uT(n,t,e),!i.useAdditionalDayOfYearTokens&&oT(n)&&uT(n,t,e),a(p,n,o.localize,m);if(r.match(dT))throw new RangeError("Format string contains an unescaped latin alphabet character `"+r+"`");return n})).join("");return v}function pT(e){return e.match(cT)[1].replace(fT,"'")}var mT={dateTimeDelimiter:/[T ]/,timeZoneDelimiter:/[Z ]/i,timezone:/([Z+-].*)$/},vT=/^-?(?:(\d{3})|(\d{2})(?:-?(\d{2}))?|W(\d{2})(?:-?(\d{1}))?|)$/,yT=/^(\d{2}(?:[.,]\d*)?)(?::?(\d{2}(?:[.,]\d*)?))?(?::?(\d{2}(?:[.,]\d*)?))?$/,gT=/^([+-])(\d{2})(?::?(\d{2}))?$/;function bT(e,t){dO(1,arguments);var n=t||{},r=null==n.additionalDigits?2:fO(n.additionalDigits);if(2!==r&&1!==r&&0!==r)throw new RangeError("additionalDigits must be 0, 1 or 2");if("string"!=typeof e&&"[object String]"!==Object.prototype.toString.call(e))return new Date(NaN);var i,o=wT(e);if(o.date){var a=ET(o.date,r);i=_T(a.restDateString,a.year)}if(isNaN(i)||!i)return new Date(NaN);var u,s=i.getTime(),l=0;if(o.time&&(l=ST(o.time),isNaN(l)||null===l))return new Date(NaN);if(!o.timezone){var c=new Date(s+l),f=new Date(0);return f.setFullYear(c.getUTCFullYear(),c.getUTCMonth(),c.getUTCDate()),f.setHours(c.getUTCHours(),c.getUTCMinutes(),c.getUTCSeconds(),c.getUTCMilliseconds()),f}return u=CT(o.timezone),isNaN(u)?new Date(NaN):new Date(s+l+u)}function wT(e){var t,n={},r=e.split(mT.dateTimeDelimiter);if(r.length>2)return n;if(/:/.test(r[0])?(n.date=null,t=r[0]):(n.date=r[0],t=r[1],mT.timeZoneDelimiter.test(n.date)&&(n.date=e.split(mT.timeZoneDelimiter)[0],t=e.substr(n.date.length,e.length))),t){var i=mT.timezone.exec(t);i?(n.time=t.replace(i[1],""),n.timezone=i[1]):n.time=t}return n}function ET(e,t){var n=new RegExp("^(?:(\\d{4}|[+-]\\d{"+(4+t)+"})|(\\d{2}|[+-]\\d{"+(2+t)+"})$)"),r=e.match(n);if(!r)return{year:null};var i=r[1]&&parseInt(r[1]),o=r[2]&&parseInt(r[2]);return{year:null==o?i:100*o,restDateString:e.slice((r[1]||r[2]).length)}}function _T(e,t){if(null===t)return null;var n=e.match(vT);if(!n)return null;var r=!!n[4],i=xT(n[1]),o=xT(n[2])-1,a=xT(n[3]),u=xT(n[4]),s=xT(n[5])-1;if(r)return function(e,t,n){return t>=1&&t<=53&&n>=0&&n<=6}(0,u,s)?function(e,t,n){var r=new Date(0);r.setUTCFullYear(e,0,4);var i=r.getUTCDay()||7,o=7*(t-1)+n+1-i;return r.setUTCDate(r.getUTCDate()+o),r}(t,u,s):new Date(NaN);var l=new Date(0);return function(e,t,n){return t>=0&&t<=11&&n>=1&&n<=(OT[t]||(TT(e)?29:28))}(t,o,a)&&function(e,t){return t>=1&&t<=(TT(e)?366:365)}(t,i)?(l.setUTCFullYear(t,o,Math.max(i,a)),l):new Date(NaN)}function xT(e){return e?parseInt(e):1}function ST(e){var t=e.match(yT);if(!t)return null;var n=kT(t[1]),r=kT(t[2]),i=kT(t[3]);return function(e,t,n){if(24===e)return 0===t&&0===n;return n>=0&&n<60&&t>=0&&t<60&&e>=0&&e<25}(n,r,i)?36e5*n+6e4*r+1e3*i:NaN}function kT(e){return e&&parseFloat(e.replace(",","."))||0}function CT(e){if("Z"===e)return 0;var t=e.match(gT);if(!t)return 0;var n="+"===t[1]?-1:1,r=parseInt(t[2]),i=t[3]&&parseInt(t[3])||0;return function(e,t){return t>=0&&t<=59}(0,i)?n*(36e5*r+6e4*i):NaN}var OT=[31,null,31,30,31,30,31,31,30,31,30,31];function TT(e){return e%400==0||e%4==0&&e%100}export{iO as F,ic as P,R,Cd as a,Ld as b,np as c,Jh as d,nf as e,c_ as f,Xh as g,zw as h,$w as i,Ew as j,d_ as k,Pw as l,Gl as m,pO as n,lO as o,hT as p,cO as q,t as r,bT as s,uf as u,fp as v}`
  
  
  
  
Instances: 2
  
### Solution
<p>Ensure that application Source Code is not available with alternative extensions, and ensure that source code is not present within other files or data deployed to the web server, or served by the web server. </p>
  
### Other information
<p>class j{async add(e){await l.post("/api/todos",e)}async retrieveAll(){return(await l.get("/api/todos")).data}}const S=c({name:"todo",initialState:{items:[],isFetching:!1,isAdding:!1},reducers:{startedToAddTodo:(e,t)=>n(d({},e),{isAdding:!0,items:[...e.items,t.payload]}),successfullyAddedTodo:e=>n(d({},e),{isAdding:!1}),startedToFetchTodos:e=>n(d({},e),{isFetching:!0}),successfullyFetchedTodos:(e,t)=>n(d({},e),{isFetching:!1,items:t.payload})}}),D=u({[S.name]:S.reducer}),k=e=>m({reducer:D,middleware:g({thunk:{extraArgument:e}})}),F=p,N=e=>e.todo.items,x=e=>e.todo.isFetching,G=e=>e.todo.isAdding,L=()=>{const e=F(x),t=F(N);return b.createElement("ul",null,e?"Loading...":t.map((e=>b.createElement("li",{key:e.uuid},e.description))))},H=e=>async(t,a,{todoGateway:r})=>{t(S.actions.startedToAddTodo(e)),await r.add(e),t(S.actions.successfullyAddedTodo())},I=()=>async(e,t,{todoGateway:a})=>(e(S.actions.startedToFetchTodos()),a.retrieveAll().then((t=>{e(S.actions.successfullyFetchedTodos(t))})));const z=()=>{(()=>{const e=y();f.exports.useEffect((()=>{e(I())}),[e])})();const e=y(),t=F(G),[a,r]=f.exports.useState(""),i=()=>{e(H({uuid:q(),description:a})),r("")};return b.createElement("div",{className:"App"},b.createElement("header",{className:"App-header"},b.createElement("img",{src:"/assets/logo.ecc203fb.svg",className:"App-logo",alt:"logo"}),b.createElement("p",null,"My todos"),b.createElement(L,null),b.createElement("input",{type:"text",value:a,onChange:e=>{t||r(e.target.value)},onKeyDown:e=>"Enter"===e.key&&i()}),b.createElement("button",{disabled:t,onClick:i},"Add Todo")))},C=/\+?[0-9]*/,M=w({email:O().required("Obligatoire").email("Veuillez saisir une adresse e-mail valide"),firstName:O().required("Obligatoire"),lastName:O().required("Obligatoire"),phone:O().matches(C,"Numero de téléphone incorrect").nullable(!0),dateStart:h().required("Obligatoire"),dateEnd:h().required("Obligatoire").min(v("dateStart"),"Date de fin doit être après la date de début").test("moins-28j","La durée maximale d'immersion est de 28 jours",((e,t)=>{const a=t.parent.dateStart;if(!(e&&a&&a instanceof Date))return!1;let r=new Date(a);return r.setDate(r.getDate()+28),e<=r})),siret:O().required("Obligatoire").length(14,"SIRET doit étre composé de 14 chiffres"),businessName:O().required("Obligatoire"),mentor:O().required("Obligatoire"),mentorPhone:O().required("Obligatoire").matches(C,"Numero de téléphone de tuteur incorrect"),mentorEmail:O().required("Obligatoire").email("Veuillez saisir un adresse mail correct"),workdays:E(O().required()).required("Obligatoire"),workHours:O().required("Obligatoire"),individualProtection:A().required("Obligatoire"),sanitaryPrevention:A().required("Obligatoire"),sanitaryPreventionDescription:O().nullable(!0),immersionAddress:O().nullable(!0),immersionObjective:O().nullable(!0),immersionProfession:O().required("Obligatoire"),immersionActivities:O().required("Obligatoire"),immersionSkills:O().nullable(!0),beneficiaryAccepted:A().equals([!0],"L'engagement est obligatoire"),enterpriseAccepted:A().equals([!0],"L'engagement est obligatoire")}).required(),R=w({id:O().required()}).required();w({id:O().required()}).required(),w({id:O().required(),formulaire:M.required()}).required();const V=w({id:O().required()}).required();console.log("GATEWAY : ","HTTP");const $=new j,B=new class{async add(e){await M.validate(e);const t=(await l.post("/api/formulaires",e)).data;return await R.validate(t),t.id}async get(e){const t=await l.get(`/api/formulaires/${e}`),a=n(d({},t.data),{dateStart:new Date(t.data.dateStart),dateEnd:new Date(t.data.dateEnd)});return console.log(a),await M.validate(a),a}async update(e,t){await M.validate(t);const a=(await l.post(`/api/formulaires/${e}`,t)).data;return await V.validate(a),a.id}},K=k({todoGateway:$});T.render(b.createElement(b.StrictMode,null,b.createElement(P,{store:K},b.createElement(z,null))),document.getElementById("root"));export{j as H,M as a,k as c,B as f}</p>
  
### Reference
* http://blogs.wsj.com/cio/2013/10/08/adobe-source-code-leak-is-bad-news-for-u-s-government/

  
#### CWE Id : 540
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### X-Frame-Options Header Not Set
##### Medium (Medium)
  
  
  
  
#### Description
<p>X-Frame-Options header is not included in the HTTP response to protect against 'ClickJacking' attacks.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Frame-Options`
  
  
  
  
Instances: 2
  
### Solution
<p>Most modern Web browsers support the X-Frame-Options HTTP header. Ensure it's set on all web pages returned by your site (if you expect the page to be framed only by pages on your server (e.g. it's part of a FRAMESET) then you'll want to use SAMEORIGIN, otherwise if you never expect the page to be framed, you should use DENY. Alternatively consider implementing Content Security Policy's "frame-ancestors" directive. </p>
  
### Reference
* https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options

  
#### CWE Id : 1021
  
#### WASC Id : 15
  
#### Source ID : 3

  
  
  
  
### Incomplete or No Cache-control Header Set
##### Low (Medium)
  
  
  
  
#### Description
<p>The cache-control header has not been set properly or is missing, allowing the browser and proxies to cache content.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `Cache-Control`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js](https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js](https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css](https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `nginx/1.14.0 (Ubuntu)`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js](https://immersion.beta.pole-emploi.fr/node_modules/@gouvfr/dsfr/dist/js/dsfr.nomodule.min.js)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
Instances: 3
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js](https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css](https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Parameter: `X-Content-Type-Options`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `com/document/d/1siwGSE4fQB5hGWoppXLMoUYX42r9N-mGZbM_Gz_iS7c/edit`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `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`
  
  
  
  
Instances: 2
  
### Solution
<p>Manually confirm that the Base64 data does not leak sensitive information, and that the data cannot be aggregated/used to exploit other vulnerabilities.</p>
  
### Other information
<p>r��v�.�������,\x0006HN\x001f@\x001ea\x0019j)�r̡F\x0017�j�7�e�?\x001b?�K�?yح</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Information Disclosure - Suspicious Comments
##### Informational (Low)
  
  
  
  
#### Description
<p>The response appears to contain suspicious comments which may help an attacker. Note: Matches made within script blocks or files are against the entire content not only comments.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `db`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `XXX`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `select`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `todo`
  
  
  
  
Instances: 5
  
### Solution
<p>Remove all comments that return information that may help an attacker and fix any underlying problems they refer to.</p>
  
### Other information
<p>The following pattern was used: \bDB\b and was detected in the element starting with: " */function Kc(e){if("object"==typeof e&&null!==e){var t=e.$$typeof;switch(t){case Ac:switch(e=e.type){case Ic:case Uc:case Nc:c", see evidence field for the suspicious comment/snippet.</p>
  
### Reference
* 

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3

  
  
  
  
### Modern Web Application
##### Informational (Medium)
  
  
  
  
#### Description
<p>The application appears to be a modern web application. If you need to explore it automatically then the Ajax Spider may well be more effective than the standard one.</p>
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script>`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `<script type="module" crossorigin src="/assets/formulaire.7b58570d.js"></script>`
  
  
  
  
Instances: 2
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/sitemap.xml](https://immersion.beta.pole-emploi.fr/sitemap.xml)
  
  
  * Method: `GET`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/robots.txt](https://immersion.beta.pole-emploi.fr/robots.txt)
  
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/formulaire.html](https://immersion.beta.pole-emploi.fr/formulaire.html)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg](https://immersion.beta.pole-emploi.fr/assets/favicon.17e50649.svg)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js](https://immersion.beta.pole-emploi.fr/assets/main.59a6c114.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/](https://immersion.beta.pole-emploi.fr/)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css](https://immersion.beta.pole-emploi.fr/assets/formulaire.1e365751.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js](https://immersion.beta.pole-emploi.fr/assets/main.3a7debd0.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css](https://immersion.beta.pole-emploi.fr/assets/main.caf5225f.css)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js](https://immersion.beta.pole-emploi.fr/assets/formulaire.7b58570d.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `no-cache`
  
  
  
  
Instances: 9
  
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
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `00000000`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741825`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `0123456789`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741824`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `1073741823`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `33554432`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `268435456`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217727`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `805306368`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `67108864`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `62914560`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `134217728`
  
  
  
  
* URL: [https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js](https://immersion.beta.pole-emploi.fr/assets/vendor.8553ee58.js)
  
  
  * Method: `GET`
  
  
  * Evidence: `2146828260`
  
  
  
  
Instances: 13
  
### Solution
<p>Manually confirm that the timestamp data is not sensitive, and that the data cannot be aggregated to disclose exploitable patterns.</p>
  
### Other information
<p>00000000, which evaluates to: 1970-01-01 00:00:00</p>
  
### Reference
* http://projects.webappsec.org/w/page/13246936/Information%20Leakage

  
#### CWE Id : 200
  
#### WASC Id : 13
  
#### Source ID : 3
