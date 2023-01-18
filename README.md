
<!DOCTYPE html>
<html lang="en-US">
<head ><meta charset="UTF-8" /><script>if(navigator.userAgent.match(/MSIE|Internet Explorer/i)||navigator.userAgent.match(/Trident\/7\..*?rv:11/i)){var href=document.location.href;if(!href.match(/[?&]nowprocket/)){if(href.indexOf("?")==-1){if(href.indexOf("#")==-1){document.location.href=href+"?nowprocket=1"}else{document.location.href=href.replace("#","?nowprocket=1#")}}else{if(href.indexOf("#")==-1){document.location.href=href+"&nowprocket=1"}else{document.location.href=href.replace("#","&nowprocket=1#")}}}}</script><script>class RocketLazyLoadScripts{constructor(){this.triggerEvents=["keydown","mousedown","mousemove","touchmove","touchstart","touchend","wheel"],this.userEventHandler=this._triggerListener.bind(this),this.touchStartHandler=this._onTouchStart.bind(this),this.touchMoveHandler=this._onTouchMove.bind(this),this.touchEndHandler=this._onTouchEnd.bind(this),this.clickHandler=this._onClick.bind(this),this.interceptedClicks=[],window.addEventListener("pageshow",(e=>{this.persisted=e.persisted})),window.addEventListener("DOMContentLoaded",(()=>{this._preconnect3rdParties()})),this.delayedScripts={normal:[],async:[],defer:[]},this.allJQueries=[]}_addUserInteractionListener(e){document.hidden?e._triggerListener():(this.triggerEvents.forEach((t=>window.addEventListener(t,e.userEventHandler,{passive:!0}))),window.addEventListener("touchstart",e.touchStartHandler,{passive:!0}),window.addEventListener("mousedown",e.touchStartHandler),document.addEventListener("visibilitychange",e.userEventHandler))}_removeUserInteractionListener(){this.triggerEvents.forEach((e=>window.removeEventListener(e,this.userEventHandler,{passive:!0}))),document.removeEventListener("visibilitychange",this.userEventHandler)}_onTouchStart(e){"HTML"!==e.target.tagName&&(window.addEventListener("touchend",this.touchEndHandler),window.addEventListener("mouseup",this.touchEndHandler),window.addEventListener("touchmove",this.touchMoveHandler,{passive:!0}),window.addEventListener("mousemove",this.touchMoveHandler),e.target.addEventListener("click",this.clickHandler),this._renameDOMAttribute(e.target,"onclick","rocket-onclick"))}_onTouchMove(e){window.removeEventListener("touchend",this.touchEndHandler),window.removeEventListener("mouseup",this.touchEndHandler),window.removeEventListener("touchmove",this.touchMoveHandler,{passive:!0}),window.removeEventListener("mousemove",this.touchMoveHandler),e.target.removeEventListener("click",this.clickHandler),this._renameDOMAttribute(e.target,"rocket-onclick","onclick")}_onTouchEnd(e){window.removeEventListener("touchend",this.touchEndHandler),window.removeEventListener("mouseup",this.touchEndHandler),window.removeEventListener("touchmove",this.touchMoveHandler,{passive:!0}),window.removeEventListener("mousemove",this.touchMoveHandler)}_onClick(e){e.target.removeEventListener("click",this.clickHandler),this._renameDOMAttribute(e.target,"rocket-onclick","onclick"),this.interceptedClicks.push(e),e.preventDefault(),e.stopPropagation(),e.stopImmediatePropagation()}_replayClicks(){window.removeEventListener("touchstart",this.touchStartHandler,{passive:!0}),window.removeEventListener("mousedown",this.touchStartHandler),this.interceptedClicks.forEach((e=>{e.target.dispatchEvent(new MouseEvent("click",{view:e.view,bubbles:!0,cancelable:!0}))}))}_renameDOMAttribute(e,t,n){e.hasAttribute&&e.hasAttribute(t)&&(event.target.setAttribute(n,event.target.getAttribute(t)),event.target.removeAttribute(t))}_triggerListener(){this._removeUserInteractionListener(this),"loading"===document.readyState?document.addEventListener("DOMContentLoaded",this._loadEverythingNow.bind(this)):this._loadEverythingNow()}_preconnect3rdParties(){let e=[];document.querySelectorAll("script[type=rocketlazyloadscript]").forEach((t=>{if(t.hasAttribute("src")){const n=new URL(t.src).origin;n!==location.origin&&e.push({src:n,crossOrigin:t.crossOrigin||"module"===t.getAttribute("data-rocket-type")})}})),e=[...new Map(e.map((e=>[JSON.stringify(e),e]))).values()],this._batchInjectResourceHints(e,"preconnect")}async _loadEverythingNow(){this.lastBreath=Date.now(),this._delayEventListeners(),this._delayJQueryReady(this),this._handleDocumentWrite(),this._registerAllDelayedScripts(),this._preloadAllScripts(),await this._loadScriptsFromList(this.delayedScripts.normal),await this._loadScriptsFromList(this.delayedScripts.defer),await this._loadScriptsFromList(this.delayedScripts.async);try{await this._triggerDOMContentLoaded(),await this._triggerWindowLoad()}catch(e){}window.dispatchEvent(new Event("rocket-allScriptsLoaded")),this._replayClicks()}_registerAllDelayedScripts(){document.querySelectorAll("script[type=rocketlazyloadscript]").forEach((e=>{e.hasAttribute("src")?e.hasAttribute("async")&&!1!==e.async?this.delayedScripts.async.push(e):e.hasAttribute("defer")&&!1!==e.defer||"module"===e.getAttribute("data-rocket-type")?this.delayedScripts.defer.push(e):this.delayedScripts.normal.push(e):this.delayedScripts.normal.push(e)}))}async _transformScript(e){return await this._littleBreath(),new Promise((t=>{const n=document.createElement("script");[...e.attributes].forEach((e=>{let t=e.nodeName;"type"!==t&&("data-rocket-type"===t&&(t="type"),n.setAttribute(t,e.nodeValue))})),e.hasAttribute("src")?(n.addEventListener("load",t),n.addEventListener("error",t)):(n.text=e.text,t());try{e.parentNode.replaceChild(n,e)}catch(e){t()}}))}async _loadScriptsFromList(e){const t=e.shift();return t?(await this._transformScript(t),this._loadScriptsFromList(e)):Promise.resolve()}_preloadAllScripts(){this._batchInjectResourceHints([...this.delayedScripts.normal,...this.delayedScripts.defer,...this.delayedScripts.async],"preload")}_batchInjectResourceHints(e,t){var n=document.createDocumentFragment();e.forEach((e=>{if(e.src){const i=document.createElement("link");i.href=e.src,i.rel=t,"preconnect"!==t&&(i.as="script"),e.getAttribute&&"module"===e.getAttribute("data-rocket-type")&&(i.crossOrigin=!0),e.crossOrigin&&(i.crossOrigin=e.crossOrigin),n.appendChild(i)}})),document.head.appendChild(n)}_delayEventListeners(){let e={};function t(t,n){!function(t){function n(n){return e[t].eventsToRewrite.indexOf(n)>=0?"rocket-"+n:n}e[t]||(e[t]={originalFunctions:{add:t.addEventListener,remove:t.removeEventListener},eventsToRewrite:[]},t.addEventListener=function(){arguments[0]=n(arguments[0]),e[t].originalFunctions.add.apply(t,arguments)},t.removeEventListener=function(){arguments[0]=n(arguments[0]),e[t].originalFunctions.remove.apply(t,arguments)})}(t),e[t].eventsToRewrite.push(n)}function n(e,t){let n=e[t];Object.defineProperty(e,t,{get:()=>n||function(){},set(i){e["rocket"+t]=n=i}})}t(document,"DOMContentLoaded"),t(window,"DOMContentLoaded"),t(window,"load"),t(window,"pageshow"),t(document,"readystatechange"),n(document,"onreadystatechange"),n(window,"onload"),n(window,"onpageshow")}_delayJQueryReady(e){let t=window.jQuery;Object.defineProperty(window,"jQuery",{get:()=>t,set(n){if(n&&n.fn&&!e.allJQueries.includes(n)){n.fn.ready=n.fn.init.prototype.ready=function(t){e.domReadyFired?t.bind(document)(n):document.addEventListener("rocket-DOMContentLoaded",(()=>t.bind(document)(n)))};const t=n.fn.on;n.fn.on=n.fn.init.prototype.on=function(){if(this[0]===window){function e(e){return e.split(" ").map((e=>"load"===e||0===e.indexOf("load.")?"rocket-jquery-load":e)).join(" ")}"string"==typeof arguments[0]||arguments[0]instanceof String?arguments[0]=e(arguments[0]):"object"==typeof arguments[0]&&Object.keys(arguments[0]).forEach((t=>{delete Object.assign(arguments[0],{[e(t)]:arguments[0][t]})[t]}))}return t.apply(this,arguments),this},e.allJQueries.push(n)}t=n}})}async _triggerDOMContentLoaded(){this.domReadyFired=!0,await this._littleBreath(),document.dispatchEvent(new Event("rocket-DOMContentLoaded")),await this._littleBreath(),window.dispatchEvent(new Event("rocket-DOMContentLoaded")),await this._littleBreath(),document.dispatchEvent(new Event("rocket-readystatechange")),await this._littleBreath(),document.rocketonreadystatechange&&document.rocketonreadystatechange()}async _triggerWindowLoad(){await this._littleBreath(),window.dispatchEvent(new Event("rocket-load")),await this._littleBreath(),window.rocketonload&&window.rocketonload(),await this._littleBreath(),this.allJQueries.forEach((e=>e(window).trigger("rocket-jquery-load"))),await this._littleBreath();const e=new Event("rocket-pageshow");e.persisted=this.persisted,window.dispatchEvent(e),await this._littleBreath(),window.rocketonpageshow&&window.rocketonpageshow({persisted:this.persisted})}_handleDocumentWrite(){const e=new Map;document.write=document.writeln=function(t){const n=document.currentScript,i=document.createRange(),r=n.parentElement;let o=e.get(n);void 0===o&&(o=n.nextSibling,e.set(n,o));const s=document.createDocumentFragment();i.setStart(s,0),s.appendChild(i.createContextualFragment(t)),r.insertBefore(s,o)}}async _littleBreath(){Date.now()-this.lastBreath>45&&(await this._requestAnimFrame(),this.lastBreath=Date.now())}async _requestAnimFrame(){return document.hidden?new Promise((e=>setTimeout(e))):new Promise((e=>requestAnimationFrame(e)))}static run(){const e=new RocketLazyLoadScripts;e._addUserInteractionListener(e)}}RocketLazyLoadScripts.run();</script>

<meta name="viewport" content="width=device-width, initial-scale=1" />
<meta name='robots' content='index, follow, max-image-preview:large, max-snippet:-1, max-video-preview:-1' />

	<!-- This site is optimized with the Yoast SEO Premium plugin v19.2 (Yoast SEO v19.14) - https://yoast.com/wordpress/plugins/seo/ -->
	<title>Rich Coconut Buns - Metemgee</title><style id="rocket-critical-css">html{font-family:sans-serif;-webkit-text-size-adjust:100%;-ms-text-size-adjust:100%}body{margin:0}article,aside,figure,header,main,nav,section{display:block}a{background-color:transparent}strong{font-weight:bold}h1{font-size:2em;margin:0.67em 0}img{border:0}svg:not(:root){overflow:hidden}figure{margin:20px 0}input,textarea{color:inherit;font:inherit;margin:0}input[type="submit"]{-webkit-appearance:button}input::-moz-focus-inner{border:0;padding:0}input{line-height:normal}input[type="search"]{-moz-box-sizing:content-box;-webkit-box-sizing:content-box;box-sizing:content-box;-webkit-appearance:textfield}input[type="search"]::-webkit-search-cancel-button,input[type="search"]::-webkit-search-decoration{-webkit-appearance:none}textarea{overflow:auto}*,input[type="search"]{-moz-box-sizing:border-box;-webkit-box-sizing:border-box;box-sizing:border-box}.entry:after,.entry-content:after,.nav-primary:after,.site-container:after,.site-header:after,.site-inner:after,.widget:after,.widget-area:after,.wrap:after{clear:both;content:" ";display:table}body{background-color:#fff;color:#515555;font-family:"Rubik",sans-serif;font-size:100%;letter-spacing:0.3px;line-height:1.875;margin:0}a{color:#ba4d2f}p{margin:0 0 30px;padding:0}ul{margin:0;padding:0}li{list-style-type:none}strong{font-weight:600}em{font-style:italic}h1,h2,h3{font-family:"Karma",Helvetica,Arial,sans-serif;font-weight:300;line-height:1.3;margin:0 0 10px}h1{font-size:2em}h2{font-size:1.625em}h3{font-size:1.375em}iframe,img{max-width:100%}img{height:auto}figure{margin:0}input,input[type="search"],textarea{background-color:#fff;border:1px solid #eee;-webkit-border-radius:0;border-radius:0;color:#515555;font-weight:300;line-height:1.625;padding:13px;width:100%}input[type="search"]{-webkit-appearance:none}::-moz-placeholder{color:#515555;opacity:1}::-webkit-input-placeholder{color:#515555}input[type="submit"]{background-color:transparent;border:1px solid #ba4d2f;color:#ba4d2f;font-family:"Rubik",sans-serif;font-weight:400;letter-spacing:2px;line-height:1;padding:17px 21px;text-decoration:none;text-transform:uppercase;white-space:normal;width:auto}input[type="search"]::-webkit-search-cancel-button,input[type="search"]::-webkit-search-results-button{display:none}.screen-reader-shortcut,.screen-reader-text{border:0;clip:rect(0,0,0,0);height:1px;overflow:hidden;position:absolute!important;width:1px;word-wrap:normal!important}.site-container{margin:0 auto}.content-sidebar-wrap,.site-inner,.wrap{margin:0 auto;max-width:1140px}.site-inner{background:#fff;margin:10px auto;padding:15px}.content{float:right;position:relative;width:720px}.content-sidebar .content{float:left}.sidebar{float:right;width:300px}.alignleft{float:left;text-align:left}.aligncenter,.aligncenter img{display:block;margin:0 auto 24px;text-align:center}.search-form{overflow:hidden;position:relative}.search-form input{background:#fdf8f5 url(https://secureservercdn.net/45.40.148.147/rnn.53d.myftpupload.com/wp-content/themes/seasonedpro-v443/images/search.svg) center right 10px no-repeat;-webkit-background-size:contain;background-size:19px 19px;border:0;border-bottom:1px solid #fff;padding:11px}.search-form input[type="submit"]{border:0;clip:rect(0,0,0,0);height:1px;margin:-1px;padding:0;position:absolute;width:1px}.entry-title{font-weight:300}.entry-title{color:#515555;text-decoration:none}.widget{margin-bottom:37px;word-wrap:break-word}.widget ul>li:last-of-type,.widget-area .widget:last-of-type{margin-bottom:0}.widget ul>li:last-of-type{padding-bottom:0}img[data-lazy-src]{opacity:0}img.lazyloaded{opacity:1}.genesis-skip-link{margin:0}.genesis-skip-link li{height:0;list-style:none;width:0}:focus{color:#000;outline:#ccc solid 1px}@media only screen and (min-width:1023px){.site-inner{margin:20px auto 0;padding:27px 37.5px}}.site-header{background:#fff;border-bottom:1px solid #eee;min-height:55px;padding:11px 37px;top:0;text-align:center;width:100%;z-index:9999}.site-header .wrap{margin:0 auto;max-width:1065px}.title-area{float:left;padding-bottom:7px;padding-top:7px}.site-title{font-size:2em;font-weight:300;line-height:1;margin:10px 0 0}.site-title a{color:#515555;text-decoration:none}.genesis-nav-menu{clear:both;line-height:1;width:100%}.genesis-nav-menu li{float:none;list-style-type:none}.genesis-nav-menu li li{margin-left:0}.genesis-nav-menu .menu-item{display:inline-block;text-align:left;min-height:52px}.genesis-nav-menu a{color:#333333;display:block;font-family:"Rubik",sans-serif;font-weight:400;letter-spacing:1px;padding:25px 15px}.nav-primary{float:right;margin:0 auto;text-align:right;width:810px}.nav-primary .genesis-nav-menu .menu-item{vertical-align:middle}#seasoned-social .simple-social-icons ul{padding:9px 0}.genesis-nav-menu .simple-social-icons{margin:0 3px;vertical-align:baseline}.genesis-nav-menu .simple-social-icons li{margin:0 2px!important}.genesis-nav-menu .search-form{display:inline-block;margin-left:17px;vertical-align:middle;width:auto}.entry{margin-bottom:77px}p.entry-meta{color:#333333;margin-bottom:31px}.entry-meta a{color:#333333}.comment-respond label{display:block;margin-right:12px}.sidebar{line-height:1.75}@media only screen and (max-width:1200px){.title-area{float:left}.nav-primary{float:none}nav{display:none;position:relative}.genesis-nav-menu{border:none}.genesis-nav-menu .menu-item{border-bottom:1px solid #eee;display:block;position:relative;text-align:left}.genesis-nav-menu .search-form{margin-left:0;width:100%}.genesis-nav-menu .search-form input{background:#fff url(https://secureservercdn.net/45.40.148.147/rnn.53d.myftpupload.com/wp-content/themes/seasonedpro-v443/images/search.svg) center left 20px no-repeat;-webkit-background-size:contain;background-size:19px 19px;padding:17px 17px 17px 47px}.seasoned-social{padding:17px 17px 17px 7px}.genesis-nav-menu .simple-social-icons ul.aligncenter{text-align:left}.site-header>.wrap{position:relative}.nav-primary{clear:left}#seasoned-social .simple-social-icons ul{padding:0!important}.genesis-nav-menu .menu-item.seasoned-search,.nav-primary .search-form input{border-bottom:none}}@media only screen and (max-width:1023px){.site-inner{max-width:720px}.content,.sidebar{width:100%}.site-header{padding-left:5%;padding-right:5%}.content-sidebar .content{margin-bottom:77px}}@media only screen and (max-width:782px){.site-inner{max-width:100%;padding-left:5%;padding-right:5%}}@media only screen and (min-width:1023px){.site-inner{margin:20px auto 0;padding:27px 37.5px}.genesis-nav-menu .menu-item{min-height:inherit}.genesis-nav-menu a{font-size:0.8em}.genesis-nav-menu .search-form input{font-size:0.8em}p.entry-meta{font-size:0.8em}.sidebar{font-size:0.8em}}.shared-counts-wrap.style-buttons .facebook.shared-counts-button{background-color:#3B5998}.shared-counts-wrap.style-buttons .pinterest.shared-counts-button{background-color:#CB2027}.shared-counts-wrap{margin:0 0 20px 0;overflow:hidden;width:100%}.shared-counts-wrap .shared-counts-label{letter-spacing:normal}.shared-counts-wrap.style-buttons .shared-counts-button{display:block;float:left;margin:0;width:32px;height:32px;line-height:0;text-align:center}.shared-counts-wrap.style-buttons .shared-counts-button svg{fill:#fff;width:16px;height:16px;margin-top:8px}.shared-counts-wrap.style-buttons .shared-counts-button .shared-counts-label,.shared-counts-wrap.style-buttons .shared-counts-button .shared-counts-count{display:none}.shared-counts-wrap.style-buttons .shared-counts-button{margin-right:12px}.shared-counts-wrap.style-buttons .shared-counts-button:last-child{margin-right:0}.shared-counts-wrap.style-buttons a.shared-counts-button{border-radius:16px;width:64px}.wp-block-group{box-sizing:border-box}h1,h2,h3{overflow-wrap:break-word}.wp-block-image{margin:0 0 1em}.wp-block-image img{height:auto;max-width:100%;vertical-align:bottom}.wp-block-image .aligncenter{display:table}.wp-block-image .aligncenter{margin-left:auto;margin-right:auto}.wp-block-image.is-style-rounded img{border-radius:9999px}.wp-block-image figure{margin:0}ul{overflow-wrap:break-word}p{overflow-wrap:break-word}.wp-block-post-featured-image{margin-left:0;margin-right:0}.wp-block-post-featured-image img{max-width:100%;width:100%;height:auto;vertical-align:bottom}:root{--wp--preset--font-size--normal:16px;--wp--preset--font-size--huge:42px}.has-text-align-center{text-align:center}.aligncenter{clear:both}.screen-reader-text{border:0;clip:rect(1px,1px,1px,1px);-webkit-clip-path:inset(50%);clip-path:inset(50%);height:1px;margin:-1px;overflow:hidden;padding:0;position:absolute;width:1px;word-wrap:normal!important}.screen-reader-text{border:0;clip:rect(1px,1px,1px,1px);-webkit-clip-path:inset(50%);clip-path:inset(50%);height:1px;margin:-1px;overflow:hidden;overflow-wrap:normal!important;word-wrap:normal!important;padding:0;position:absolute!important;width:1px}:root{--woocommerce:#a46497;--wc-green:#7ad03a;--wc-red:#a00;--wc-orange:#ffba00;--wc-blue:#2ea2cc;--wc-primary:#a46497;--wc-primary-text:white;--wc-secondary:#ebe9eb;--wc-secondary-text:#515151;--wc-highlight:#77a464;--wc-highligh-text:white;--wc-content-bg:#fff;--wc-subtext:#767676}:root{--woocommerce:#a46497;--wc-green:#7ad03a;--wc-red:#a00;--wc-orange:#ffba00;--wc-blue:#2ea2cc;--wc-primary:#a46497;--wc-primary-text:white;--wc-secondary:#ebe9eb;--wc-secondary-text:#515151;--wc-highlight:#77a464;--wc-highligh-text:white;--wc-content-bg:#fff;--wc-subtext:#767676}.screen-reader-text{clip:rect(1px,1px,1px,1px);height:1px;overflow:hidden;position:absolute!important;width:1px;word-wrap:normal!important}.simple-social-icons svg[class^="social-"]{display:inline-block;width:1em;height:1em;stroke-width:0;stroke:currentColor;fill:currentColor}.simple-social-icons{overflow:hidden}.simple-social-icons ul{margin:0;padding:0}.simple-social-icons ul li{background:none!important;border:none!important;float:left;list-style-type:none!important;margin:0 6px 12px!important;padding:0!important}.simple-social-icons ul li a{border:none!important;-moz-box-sizing:content-box;-webkit-box-sizing:content-box;box-sizing:content-box;display:inline-block;font-style:normal!important;font-variant:normal!important;font-weight:normal!important;height:1em;line-height:1em;text-align:center;text-decoration:none!important;text-transform:none!important;width:1em}.simple-social-icons ul.aligncenter{text-align:center}.simple-social-icons ul.aligncenter li{display:inline-block;float:none}fieldset.wprm-comment-ratings-container br{display:none}.wprm-recipe{overflow:hidden;zoom:1;text-align:left;clear:both}.wprm-recipe *{box-sizing:border-box}.wprm-recipe a.wprm-recipe-link{-webkit-box-shadow:none;-moz-box-shadow:none;box-shadow:none}.wprm-block-text-normal{font-weight:400;font-style:normal;text-transform:none}.wprm-recipe-icon svg{display:inline;vertical-align:middle;margin-top:-0.15em;width:1.3em;height:1.3em;overflow:visible}.wprm-recipe-link{text-decoration:none}.wprm-recipe-link.wprm-recipe-link-inline-button{display:inline-block;margin:0 5px 5px 0}.wprm-recipe-link.wprm-recipe-link-inline-button{border-width:1px;border-style:solid;padding:5px}</style>
	<meta name="description" content="Rich Coconut buns bring together the rich flavor of grated coconut in a easy and simple recipe. These are the perfect afterschool snack." />
	<link rel="canonical" href="https://metemgee.com/2013/01/30/rich-coconut-buns/" />
	<meta property="og:locale" content="en_US" />
	<meta property="og:type" content="article" />
	<meta property="og:title" content="Rich Coconut Buns" />
	<meta property="og:description" content="Rich Coconut buns bring together the rich flavor of grated coconut in a easy and simple recipe. These are the perfect afterschool snack." />
	<meta property="og:url" content="https://metemgee.com/2013/01/30/rich-coconut-buns/" />
	<meta property="og:site_name" content="Metemgee" />
	<meta property="article:published_time" content="2013-01-30T16:04:36+00:00" />
	<meta property="article:modified_time" content="2022-05-03T20:42:20+00:00" />
	<meta property="og:image" content="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg" />
	<meta property="og:image:width" content="2048" />
	<meta property="og:image:height" content="1648" />
	<meta property="og:image:type" content="image/jpeg" />
	<meta name="author" content="Althea Brown" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:label1" content="Written by" />
	<meta name="twitter:data1" content="Althea Brown" />
	<meta name="twitter:label2" content="Est. reading time" />
	<meta name="twitter:data2" content="7 minutes" />
	<script type="application/ld+json" class="yoast-schema-graph">{"@context":"https://schema.org","@graph":[{"@type":"Article","@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#article","isPartOf":{"@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/"},"author":{"name":"Althea Brown","@id":"https://metemgee.com/#/schema/person/22273b3e32710d039a82480840019639"},"headline":"Rich Coconut Buns","datePublished":"2013-01-30T16:04:36+00:00","dateModified":"2022-05-03T20:42:20+00:00","mainEntityOfPage":{"@id":"https://rnn53d.p3cdn1.secureserver.net/2013/01/30/rich-coconut-buns/"},"wordCount":1185,"commentCount":16,"publisher":{"@id":"https://metemgee.com/#/schema/person/817c2f0fc7fbed081f41270b0eb65405"},"image":{"@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#primaryimage"},"thumbnailUrl":"https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg?time=1673945671","keywords":["coconut buns","How to make coconut buns","How to make coconut drops","How to make coconut rock buns","How to make dairy free coconut buns","How to make egg free coconut buns","How to make Vegan Coconut Buns","How to make Vegan Coconut Drops","How to make vegan rock buns","metemgee","metemgee blog"],"articleSection":["Baking","Desserts","Quick and Easy Recipes","Vegan"],"inLanguage":"en-US","potentialAction":[{"@type":"CommentAction","name":"Comment","target":["https://metemgee.com/2013/01/30/rich-coconut-buns/#respond"]}]},{"@type":"WebPage","@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/","url":"https://metemgee.com/2013/01/30/rich-coconut-buns/","name":"Rich Coconut Buns - Metemgee","isPartOf":{"@id":"https://rnn53d.p3cdn1.secureserver.net/#website"},"primaryImageOfPage":{"@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#primaryimage"},"image":{"@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#primaryimage"},"thumbnailUrl":"https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg?time=1673945671","datePublished":"2013-01-30T16:04:36+00:00","dateModified":"2022-05-03T20:42:20+00:00","description":"Rich Coconut buns bring together the rich flavor of grated coconut in a easy and simple recipe. These are the perfect afterschool snack.","breadcrumb":{"@id":"https://rnn53d.p3cdn1.secureserver.net/2013/01/30/rich-coconut-buns/#breadcrumb"},"inLanguage":"en-US","potentialAction":[{"@type":"ReadAction","target":["https://metemgee.com/2013/01/30/rich-coconut-buns/"]}]},{"@type":"ImageObject","inLanguage":"en-US","@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#primaryimage","url":"https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg?time=1673945671","contentUrl":"https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg?time=1673945671","width":2048,"height":1648},{"@type":"BreadcrumbList","@id":"https://metemgee.com/2013/01/30/rich-coconut-buns/#breadcrumb","itemListElement":[{"@type":"ListItem","position":1,"name":"\"Home\"","item":"https://metemgee.com/"},{"@type":"ListItem","position":2,"name":"Baking","item":"https://metemgee.com/category/baking/"},{"@type":"ListItem","position":3,"name":"Rich Coconut Buns"}]},{"@type":"WebSite","@id":"https://metemgee.com/#website","url":"https://metemgee.com/","name":"Metemgee","description":"","publisher":{"@id":"https://metemgee.com/#/schema/person/817c2f0fc7fbed081f41270b0eb65405"},"potentialAction":[{"@type":"SearchAction","target":{"@type":"EntryPoint","urlTemplate":"https://metemgee.com/?s={search_term_string}"},"query-input":"required name=search_term_string"}],"inLanguage":"en-US"},{"@type":["Person","Organization"],"@id":"https://metemgee.com/#/schema/person/817c2f0fc7fbed081f41270b0eb65405","name":"Althea Brown","image":{"@type":"ImageObject","inLanguage":"en-US","@id":"https://metemgee.com/#/schema/person/image/","url":"https://secure.gravatar.com/avatar/a3a3e11e22e6164bd56749736ee72b4d?s=96&d=mm&r=g","contentUrl":"https://secure.gravatar.com/avatar/a3a3e11e22e6164bd56749736ee72b4d?s=96&d=mm&r=g","caption":"Althea Brown"},"logo":{"@id":"https://metemgee.com/#/schema/person/image/"}},{"@type":"Person","@id":"https://metemgee.com/#/schema/person/22273b3e32710d039a82480840019639","name":"Althea Brown","image":{"@type":"ImageObject","inLanguage":"en-US","@id":"https://metemgee.com/#/schema/person/image/","url":"https://secure.gravatar.com/avatar/aa1ed4ca8d2d9940e250166842563de8?s=96&d=mm&r=g","contentUrl":"https://secure.gravatar.com/avatar/aa1ed4ca8d2d9940e250166842563de8?s=96&d=mm&r=g","caption":"Althea Brown"}}]}</script>
	<!-- / Yoast SEO Premium plugin. -->


<link rel='dns-prefetch' href='//scripts.mediavine.com' />

<link rel="alternate" type="application/rss+xml" title="Metemgee &raquo; Feed" href="https://metemgee.com/feed/" />
<link rel="alternate" type="application/rss+xml" title="Metemgee &raquo; Comments Feed" href="https://metemgee.com/comments/feed/" />
<link rel='preconnect' href='https://rnn53d.p3cdn1.secureserver.net' crossorigin />
<link rel="alternate" type="application/rss+xml" title="Metemgee &raquo; Rich Coconut Buns Comments Feed" href="https://metemgee.com/2013/01/30/rich-coconut-buns/feed/" />
<link rel='preload'  href='https://rnn53d.p3cdn1.secureserver.net/wp-content/themes/seasonedpro-v443/style.css?ver=4.4.3&#038;time=1673945671' data-rocket-async="style" as="style" onload="this.onload=null;this.rel='stylesheet'" onerror="this.removeAttribute('data-rocket-async')"  type='text/css' media='all' />
<style id='seasoned-pro-theme-inline-css' type='text/css'>
.before-header, .footer-widgets, .form-allowed-tags, .more-from-category, .enews-widget, blockquote::before{background:#769aa3;}.site-title a, .site-title a:hover, h1, h2, h3, h4, h5, h6{color:#000000;}.genesis-nav-menu a{color:#127c84;}.genesis-nav-menu a:hover, .genesis-nav-menu a:focus, .genesis-nav-menu .current-menu-item > a, .nav-primary .genesis-nav-menu .sub-menu a:focus, .nav-primary .genesis-nav-menu .sub-menu a:hover{color:#c78d92;}.button, button, .content .enews-widget input[type="submit"], .sidebar .enews-widget input[type="submit"], a.more-link, .sidebar .button, input[type="submit"], input[type="button"]{background:#c78d92;}.button, button, .enews-widget input[type="submit"], a.more-link, input[type="submit"], input[type="button"]{border-color:#c78d92;color:#ffffff;}.button:hover, button:hover, .button:focus, .button:active, button:focus, button:active, .enews-widget input[type="submit"]:hover, .enews-widget input[type="submit"]:focus, a.more-link:hover, a.more-link:focus, .before-header .enews-widget input[type="submit"], .content .enews-widget input[type="submit"]:hover, .content .enews-widget input[type="submit"]:focus, .sidebar .enews-widget input[type="submit"]:hover, .sidebar .enews-widget input[type="submit"]:focus, .more-from-category, .home-top article:not(.simple-grid) .entry-title:before, input[type="submit"]:hover, input[type="submit"]:focus, input[type="submit"]:active, input[type="button"]:hover, input[type="button"]:focus, input[type="button"]:active{background:#127c84;}
</style>
<link rel='preload'  href='https://rnn53d.p3cdn1.secureserver.net/wp-includes/css/dist/block-library/style.min.css?ver=6.1.1&#038;time=1673945671' data-rocket-async="style" as="style" onload="this.onload=null;this.rel='stylesheet'" onerror="this.removeAttribute('data-rocket-async')"  type='text/css' media='all' />
<link rel='preload'  href='https://rnn53d.p3cdn1.secureserver.net/wp-includes/css/classic-themes.min.css?ver=1&#038;time=1673945671' data-rocket-async="style" as="style" onload="this.onload=null;this.rel='stylesheet'" onerror="this.removeAttribute('data-rocket-async')"  type='text/css' media='all' />
<style id='global-styles-inline-css' type='text/css'>
body{--wp--preset--color--black: #000000;--wp--preset--color--cyan-bluish-gray: #abb8c3;--wp--preset--color--white: #ffffff;--wp--preset--color--pale-pink: #f78da7;--wp--preset--color--vivid-red: #cf2e2e;--wp--preset--color--luminous-vivid-orange: #ff6900;--wp--preset--color--luminous-vivid-amber: #fcb900;--wp--preset--color--light-green-cyan: #7bdcb5;--wp--preset--color--vivid-green-cyan: #00d084;--wp--preset--color--pale-cyan-blue: #8ed1fc;--wp--preset--color--vivid-cyan-blue: #0693e3;--wp--preset--color--vivid-purple: #9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg,rgba(6,147,227,1) 0%,rgb(155,81,224) 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg,rgb(122,220,180) 0%,rgb(0,208,130) 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg,rgba(252,185,0,1) 0%,rgba(255,105,0,1) 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg,rgba(255,105,0,1) 0%,rgb(207,46,46) 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg,rgb(238,238,238) 0%,rgb(169,184,195) 100%);--wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg,rgb(74,234,220) 0%,rgb(151,120,209) 20%,rgb(207,42,186) 40%,rgb(238,44,130) 60%,rgb(251,105,98) 80%,rgb(254,248,76) 100%);--wp--preset--gradient--blush-light-purple: linear-gradient(135deg,rgb(255,206,236) 0%,rgb(152,150,240) 100%);--wp--preset--gradient--blush-bordeaux: linear-gradient(135deg,rgb(254,205,165) 0%,rgb(254,45,45) 50%,rgb(107,0,62) 100%);--wp--preset--gradient--luminous-dusk: linear-gradient(135deg,rgb(255,203,112) 0%,rgb(199,81,192) 50%,rgb(65,88,208) 100%);--wp--preset--gradient--pale-ocean: linear-gradient(135deg,rgb(255,245,203) 0%,rgb(182,227,212) 50%,rgb(51,167,181) 100%);--wp--preset--gradient--electric-grass: linear-gradient(135deg,rgb(202,248,128) 0%,rgb(113,206,126) 100%);--wp--preset--gradient--midnight: linear-gradient(135deg,rgb(2,3,129) 0%,rgb(40,116,252) 100%);--wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');--wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');--wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');--wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');--wp--preset--duotone--midnight: url('#wp-duotone-midnight');--wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');--wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');--wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');--wp--preset--font-size--small: 13px;--wp--preset--font-size--medium: 20px;--wp--preset--font-size--large: 36px;--wp--preset--font-size--x-large: 42px;--wp--preset--spacing--20: 0.44rem;--wp--preset--spacing--30: 0.67rem;--wp--preset--spacing--40: 1rem;--wp--preset--spacing--50: 1.5rem;--wp--preset--spacing--60: 2.25rem;--wp--preset--spacing--70: 3.38rem;--wp--preset--spacing--80: 5.06rem;}:where(.is-layout-flex){gap: 0.5em;}body .is-layout-flow > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-flow > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-flow > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-constrained > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-constrained > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > :where(:not(.alignleft):not(.alignright):not(.alignfull)){max-width: var(--wp--style--global--content-size);margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignwide{max-width: var(--wp--style--global--wide-size);}body .is-layout-flex{display: flex;}body .is-layout-flex{flex-wrap: wrap;align-items: center;}body .is-layout-flex > *{margin: 0;}:where(.wp-block-columns.is-layout-flex){gap: 2em;}.has-black-color{color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-color{color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-color{color: var(--wp--preset--color--white) !important;}.has-pale-pink-color{color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-color{color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-color{color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-color{color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-color{color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-color{color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-color{color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-color{color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-color{color: var(--wp--preset--color--vivid-purple) !important;}.has-black-background-color{background-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-background-color{background-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-background-color{background-color: var(--wp--preset--color--white) !important;}.has-pale-pink-background-color{background-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-background-color{background-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-background-color{background-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-background-color{background-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-background-color{background-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-background-color{background-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-background-color{background-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-background-color{background-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-background-color{background-color: var(--wp--preset--color--vivid-purple) !important;}.has-black-border-color{border-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-border-color{border-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-border-color{border-color: var(--wp--preset--color--white) !important;}.has-pale-pink-border-color{border-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-border-color{border-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-border-color{border-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-border-color{border-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-border-color{border-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-border-color{border-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-border-color{border-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-border-color{border-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-border-color{border-color: var(--wp--preset--color--vivid-purple) !important;}.has-vivid-cyan-blue-to-vivid-purple-gradient-background{background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;}.has-light-green-cyan-to-vivid-green-cyan-gradient-background{background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;}.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;}.has-luminous-vivid-orange-to-vivid-red-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;}.has-very-light-gray-to-cyan-bluish-gray-gradient-background{background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;}.has-cool-to-warm-spectrum-gradient-background{background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;}.has-blush-light-purple-gradient-background{background: var(--wp--preset--gradient--blush-light-purple) !important;}.has-blush-bordeaux-gradient-background{background: var(--wp--preset--gradient--blush-bordeaux) !important;}.has-luminous-dusk-gradient-background{background: var(--wp--preset--gradient--luminous-dusk) !important;}.has-pale-ocean-gradient-background{background: var(--wp--preset--gradient--pale-ocean) !important;}.has-electric-grass-gradient-background{background: var(--wp--preset--gradient--electric-grass) !important;}.has-midnight-gradient-background{background: var(--wp--preset--gradient--midnight) !important;}.has-small-font-size{font-size: var(--wp--preset--font-size--small) !important;}.has-medium-font-size{font-size: var(--wp--preset--font-size--medium) !important;}.has-large-font-size{font-size: var(--wp--preset--font-size--large) !important;}.has-x-large-font-size{font-size: var(--wp--preset--font-size--x-large) !important;}
.wp-block-navigation a:where(:not(.wp-element-button)){color: inherit;}
:where(.wp-block-columns.is-layout-flex){gap: 2em;}
.wp-block-pullquote{font-size: 1.5em;line-height: 1.6;}
</style>
<link rel='preload'  href='https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/css/style.css?ver=3.0.2&#038;time=1673945671' data-rocket-async="style" as="style" onload="this.onload=null;this.rel='stylesheet'" onerror="this.removeAttribute('data-rocket-async')"  type='text/css' media='all' />
<script type='text/javascript' async="async" data-noptimize="1" data-cfasync="false" src='https://scripts.mediavine.com/tags/metemgee.js?ver=6.1.1' id='mv-script-wrapper-js'></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-includes/js/jquery/jquery.min.js?ver=3.6.1&#038;time=1673945671' id='jquery-core-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-includes/js/jquery/jquery-migrate.min.js?ver=3.3.2&#038;time=1673945671' id='jquery-migrate-js' defer></script>
<link rel="https://api.w.org/" href="https://metemgee.com/wp-json/" /><link rel="alternate" type="application/json" href="https://metemgee.com/wp-json/wp/v2/posts/233" /><link rel="EditURI" type="application/rsd+xml" title="RSD" href="https://metemgee.com/xmlrpc.php?rsd" />
<link rel="wlwmanifest" type="application/wlwmanifest+xml" href="https://rnn53d.p3cdn1.secureserver.net/wp-includes/wlwmanifest.xml?time=1673945671" />
<meta name="generator" content="WordPress 6.1.1" />
<link rel='shortlink' href='https://metemgee.com/?p=233' />
<link rel="alternate" type="application/json+oembed" href="https://metemgee.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fmetemgee.com%2F2013%2F01%2F30%2Frich-coconut-buns%2F" />
<link rel="alternate" type="text/xml+oembed" href="https://metemgee.com/wp-json/oembed/1.0/embed?url=https%3A%2F%2Fmetemgee.com%2F2013%2F01%2F30%2Frich-coconut-buns%2F&#038;format=xml" />
<style id='feast-blockandfront-styles'>.feast-about-author { background-color: #f2f2f2; color: #32373c; padding: 17px; margin-top: 57px; display: grid; grid-template-columns: 1fr 3fr !important; } .feast-about-author h2 { margin-top: 7px !important;} .feast-about-author img{ border-radius: 50% !important; }aside .feast-about-author { grid-template-columns: 1fr !important; }.wp-block-search .wp-block-search__input { max-width: 100%; }.screen-reader-text { width: 1px; height: 1px; }footer ul li, .site-footer ul li { list-style-type: none; }footer ul li, .site-footer ul li { list-style-type: none; }aside .wp-block-search { display: grid; grid-template-columns: 1fr; margin: 37px 0;  } aside .wp-block-search__inside-wrapper { display: grid !important; grid-template-columns: 1fr; } aside input { min-height: 50px; }  ​aside .wp-block-search__label, aside .wp-block-search__button { display: none; } aside p, aside div, aside ul { margin: 17px 0; }@media only screen and (max-width: 600px) { aside .wp-block-search { grid-template-columns: 1fr; } aside input { min-height: 50px; margin-bottom: 17px;} }.feast-button a { border: 2px solid var(--feast-branding-primary-background); padding: 7px 14px; border-radius: 20px; background: var(--feast-branding-primary); color: var(--feast-branding-primary-background); text-decoration: none !important; font-weight: bold; } .feast-button { padding: 27px 7px; }.feast-box-primary { color: var( --feast-branding-primary ) !important; background: var(--feast-branding-primary-background) !important; padding: 17px !important; margin: 17px 0 !important;  }.feast-box-secondary { color: var( --feast-branding-secondary ) !important; background: var(--feast-branding-secondary-background) !important; padding: 17px !important; margin: 17px 0 !important;  }.feast-box-primary li, .feast-box-secondary li {margin-left: 17px !important; }.feast-checklist li::marker { color: transparent; } .feast-checklist li:before { content: '✓'; margin-right: 17px; }.schema-faq-question { font-size: 1.2em; display: block; margin-bottom: 7px;} .schema-faq-section { margin: 37px 0; }</style>
<style type="text/css">
	.feast-category-index-list {
		display: grid;
		grid-template-columns: repeat(2, minmax(0, 1fr) );
		grid-gap: 57px 17px;
		list-style: none;
		list-style-type: none;
		margin: 17px 0 !important;
	}
	.feast-category-index-list li {
		min-height: 150px;
		text-align: center;
		position: relative;
		list-style: none !important;
		margin-left: 0 !important;
		list-style-type: none !important;
		overflow: hidden;
	}
	.feast-category-index-list li a.title {
		text-decoration: none;
	}
	.feast-category-index-list-overlay .fsci-title {
		position: absolute;
		top: 88%;
		left: 50%;
		transform: translate(-50%, -50%);
		background: #FFF;
		padding: 5px;
		color: #333;
		font-weight: bold;
		border: 2px solid #888;
		text-transform: uppercase;
		width: 80%;
	}
	.listing-item:focus-within, .wp-block-search__input:focus {outline: 2px solid #555; }
	.listing-item a:focus, .listing-item a:focus .fsri-title, .listing-item a:focus img { opacity: 0.8; outline: none; }
	li.listing-item:before { content: none !important; } /* needs to override theme */
	.listing-item { display: grid; } .fsri-rating, .fsri-time { place-self: end center; } /* align time + rating bottom */
	.feast-image-frame, .feast-image-border { border: 3px solid #DDD; }
	.feast-image-round, .feast-image-round img { border-radius: 50%; }
	.feast-image-shadow { box-shadow: 3px 3px 5px #AAA; }
	.feast-line-through { text-decoration: line-through; }
	.feast-grid-full, .feast-grid-half, .feast-grid-third, .feast-grid-fourth, .feast-grid-fifth { display: grid; grid-gap: 57px 17px; }
	.feast-grid-full { grid-template-columns: 1fr !important; }
	.feast-grid-half { grid-template-columns: repeat(2, minmax(0, 1fr)) !important; }
	.feast-grid-third { grid-template-columns: repeat(3, minmax(0, 1fr)) !important; }
	.feast-grid-fourth { grid-template-columns: repeat(4, minmax(0, 1fr)) !important; }
	.feast-grid-fifth { grid-template-columns: repeat(5, minmax(0, 1fr)) !important; }
	@media only screen and (min-width: 600px)  {
		.feast-category-index-list { grid-template-columns: repeat(4, minmax(0, 1fr) ); }
		.feast-desktop-grid-full { grid-template-columns: 1fr !important; }
		.feast-desktop-grid-half { grid-template-columns: repeat(2, 1fr) !important; }
		.feast-desktop-grid-third { grid-template-columns: repeat(3, 1fr) !important; }
		.feast-desktop-grid-fourth { grid-template-columns: repeat(4, 1fr) !important; }
		.feast-desktop-grid-fifth { grid-template-columns: repeat(5, 1fr) !important; }
		.feast-desktop-grid-sixth { grid-template-columns: repeat(6, 1fr) !important; }
	}
	@media only screen and (min-width: 1100px) { .full-width-content main.content { width: 1080px; max-width: 1080px; } }
	@media only screen and (max-width: 600px) { .entry-content .wp-block-image { width: 100% !important; }}
	@media only screen and (min-width: 1024px) {
		.feast-full-width-wrapper { width: 100vw; position: relative; left: 50%; right: 50%; margin: 37px -50vw; background: #F5F5F5; padding: 17px 0; }
		.feast-full-width-wrapper .feast-recipe-index { width: 1140px; margin: 0 auto; }
		.feast-full-width-wrapper .listing-item { background: #FFF; padding: 17px; }
	}
	.home main .wp-block-search { margin: 57px 0; padding: 13px; background: #FFF; }
	.home main .wp-block-search button { display: none; visibility: hidden; }
	.home main .wp-block-search__label { position:absolute; left:-10000px; top:auto; }
	.feast-prev-next { display: grid; grid-template-columns: 1fr;  border-bottom: 1px solid #CCC; margin: 57px 0;  }
	.feast-prev-post, .feast-next-post { padding: 37px 17px; border-top: 1px solid #CCC; }
	.feast-next-post { text-align: right; }
	@media only screen and (min-width: 600px) {
		.feast-prev-next { grid-template-columns: 1fr 1fr; border-bottom: none; }
		.feast-next-post { border-left: 1px solid #CCC;}
		.feast-prev-post, .feast-next-post { padding: 37px; }
	}
	.has-background { padding: 1.25em 2.375em; margin: 1em 0; }
	@media only screen and (max-width: 1023px) {
		.content-sidebar .content, .sidebar-primary { float: none; clear: both; }
		.has-background { padding: 1em; margin: 1em 0; }
	}
	hr.has-background { padding: inherit; margin: inherit; }
	body { -webkit-animation: none !important; animation: none !important; }
	summary { display: list-item; }
	.comment-form-cookies-consent > label {
    		display: inline-block;
		margin-left: 30px;
	}
	@media only screen and (max-width: 600px) { .comment-form-cookies-consent { display: grid; grid-template-columns: 1fr 12fr; } }
	.bypostauthor .comment-author-name { color: unset; }
	.comment-list article header { overflow: auto; }
     .fsri-rating .wprm-recipe-rating { pointer-events: none; }</style><script type="rocketlazyloadscript" data-rocket-type="text/javascript">
	window._wp_rp_static_base_url = 'https://wprp.zemanta.com/static/';
	window._wp_rp_wp_ajax_url = "https://metemgee.com/wp-admin/admin-ajax.php";
	window._wp_rp_plugin_version = '3.6.4';
	window._wp_rp_post_id = '233';
	window._wp_rp_num_rel_posts = '4';
	window._wp_rp_thumbnails = true;
	window._wp_rp_post_title = 'Rich+Coconut+Buns';
	window._wp_rp_post_tags = ['how+to+make+dairy+free+coconut', 'metemgee', 'how+to+make+coconut+rock+buns', 'metemgee+blog', 'how+to+make+coconut+drops', 'how+to+make+vegan+rock+buns', 'how+to+make+coconut+buns', 'how+to+make+vegan+coconut+drop', 'coconut+buns', 'how+to+make+vegan+coconut+buns', 'how+to+make+egg+free+coconut+b', 'vegan', 'quick+and+easy+recipes', 'desserts', 'baking', 'coconut', 'alt', 'ec', 'recip', 'h2', 'sugar', 'bun', 'cream', 'school', 'fat', 'home', 'blog', 'flour', 'scone', 'rub'];
	window._wp_rp_promoted_content = true;
</script>
<link rel="preload" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/wordpress-23-related-posts-plugin/static/themes/vertical.css?version=3.6.4" data-rocket-async="style" as="style" onload="this.onload=null;this.rel='stylesheet'" onerror="this.removeAttribute('data-rocket-async')"  />
<style type="text/css"> .wprm-comment-rating svg { width: 18px !important; height: 18px !important; } img.wprm-comment-rating { width: 90px !important; height: 18px !important; } .wprm-comment-rating svg path { fill: #343434; } .wprm-comment-rating svg polygon { stroke: #343434; } .wprm-comment-ratings-container svg .wprm-star-full { fill: #343434; } .wprm-comment-ratings-container svg .wprm-star-empty { stroke: #343434; }</style><link rel="apple-touch-icon" sizes="180x180" href="/wp-content/uploads/fbrfg/apple-touch-icon.png">
<link rel="icon" type="image/png" sizes="32x32" href="/wp-content/uploads/fbrfg/favicon-32x32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/wp-content/uploads/fbrfg/favicon-16x16.png">
<link rel="manifest" href="/wp-content/uploads/fbrfg/site.webmanifest">
<link rel="mask-icon" href="/wp-content/uploads/fbrfg/safari-pinned-tab.svg" color="#5bbad5">
<link rel="shortcut icon" href="/wp-content/uploads/fbrfg/favicon.ico">
<meta name="msapplication-TileColor" content="#00aba9">
<meta name="msapplication-config" content="/wp-content/uploads/fbrfg/browserconfig.xml">
<meta name="theme-color" content="#ffffff"><link rel="pingback" href="https://metemgee.com/xmlrpc.php" />
	<style>
		/* Add animation (Chrome, Safari, Opera) */
		@-webkit-keyframes openmenu {
		  from {left:-100px;opacity: 0;}
		  to {left:0px;opacity:1;}
		}
		@-webkit-keyframes closebutton {
		    0% {opacity: 0;}
		    100% {opacity: 1;}
		}

		/* Add animation (Standard syntax) */
		@keyframes openmenu {
		  from {left:-100px;opacity: 0;}
		  to {left:0px;opacity:1;}
		}
		@keyframes closebutton {
		    0% {opacity: 0;}
		    100% {opacity: 1;}
		}

          /* Ensure the jump link is below the fixed nav */
          html {
               scroll-padding-top: 90px;
          }

		/* The mmm's background */
		.feastmobilemenu-background {
			display: none;
			position: fixed;
			z-index: 9999;
			left: 0;
			top: 0;
			width: 100%;
			height: 100%;
			overflow: auto;
			background-color: rgb(0, 0, 0);
			background-color: rgba(0, 0, 0, 0.4);
		}

		/* Display the mmm when targeted */
		.feastmobilemenu-background:target {
			display: table;
			position: fixed;
		}

		/* The mmm box */
		.mmm-dialog {
			display: table-cell;
			vertical-align: top;
			font-size: 20px;
		}

		/* The mmm's content */
		.mmm-dialog .mmm-content {
			margin: 0;
			padding: 10px 10px 10px 20px;
			position: fixed;
			left: 0;
			background-color: #FEFEFE;
			contain: strict;
			overflow-x: hidden;
			overflow-y: auto;
			outline: 0;
			border-right: 1px #777 solid;
			border-bottom: 1px #777 solid;
			text-align: justify;
			width: 320px;
			height: 90%;
			box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

			/* Add animation */
			-webkit-animation-name: openmenu; /* Chrome, Safari, Opera */
			-webkit-animation-duration: 0.6s; /* Chrome, Safari, Opera */
			animation-name: openmenu;
			animation-duration: 0.6s;
		}
		.mmm-content li {
		    list-style: none;
		}
		#menu-feast-modern-mobile-menu li {
			min-height: 50px;
			margin-left: 5px;
		    	list-style: none;
		}
		#menu-feast-modern-mobile-menu li a {
			color: inherit;
			text-decoration: inherit;
		}

		/* The button used to close the mmm */
		.closebtn {
			text-decoration: none;
			float: right;
			margin-right: 10px;
			font-size: 50px;
			font-weight: bold;
			color: #333;
			z-index:1001;
  			top: 0;
			position: fixed;
			left: 270px;
			-webkit-animation-name: closebutton; /* Chrome, Safari, Opera */
			-webkit-animation-duration: 1.5s; /* Chrome, Safari, Opera */
			animation-name: closebutton;
			animation-duration: 1.5s;
		}

		.closebtn:hover,
		.closebtn:focus {
			color: #555;
			cursor: pointer;
		}
		@media (prefers-reduced-motion) { /* accessibility animation fix */
		  .mmm-dialog .mmm-content, .closebtn {
			animation: none !important;
		  }
		}
		.mmmheader {
			font-size: 25px;
			color: #FFF;
			height: 80px;
			display: flex;
			justify-content: space-between;
		}
		#mmmlogo {
			max-width: 200px;
			max-height: 70px;
		}
		#feast-mobile-search {
			margin-bottom: 17px;
			min-height: 50px;
			overflow: auto;
		}
		#feast-mobile-search input[type=submit] {
			display: none;
		}
		#feast-mobile-search input[type=search] {
			width: 100%;
		}

		#feast-mobile-menu-social-icons {
			margin-top: 17px;
		}

		#feast-social .simple-social-icons {
			list-style: none;
			margin: 0 !important;
		}

		.feastmobilenavbar {
			position: fixed;
			top: 0;
			left: 0;
			z-index: 998;
			width: 100%;
			height: 80px;
			padding: 0;
			margin: 0 auto;
			box-sizing: border-box;
			border-top: 1px solid #CCC;
			border-bottom: 1px solid #CCC;
			background: #FFF;
			display: grid;
			grid-template-columns: repeat(7, minmax(50px, 1fr));
			text-align: center;
			contain: strict;
			overflow: hidden;
		}
		.feastmobilenavbar > div { height: 80px; }
		.admin-bar .feastmobilenavbar {
			top: 32px;
		}
		@media screen and (max-width:782px) {
			.admin-bar .feastmobilenavbar {
				top: 0;
				position: sticky;
			}
			.admin-bar .site-container, .admin-bar .body-template-content {
				margin-top: 0;
			}
		}
		.feastmobilenavbar a img {
			margin-bottom: inherit !important;
		}
		.feastmenutoggle, .feastsearchtoggle, .feastsubscribebutton {
			display: flex;
			align-items: center;
			justify-items: center;
			justify-content: center;
		}

		
		.feastsearchtoggle svg, .feastmenutoggle svg {
			width: 30px;
			height: 30px;
			padding: 10px;
			box-sizing: content-box;
			color: black;
		}
		.feastsubscribebutton {
   		 	overflow: hidden;
		}
		.feastsubscribebutton img {
			max-width: 90px;
			padding: 15px;
			margin: 1px;
		}
		.feastsubscribebutton svg {
			color: #000;
		}
						.feastmenulogo {
			overflow: hidden;
			display: flex;
			align-items: center;
			justify-content: center;
			grid-column-end: span 4;
		}


					.desktop-inline-modern-menu .sub-menu { display: none; }
			.desktop-inline-modern-menu, .modern-menu-desktop-social { display: none; }
			@media only screen and (min-width: 1200px) {
				.desktop-inline-modern-menu, .modern-menu-desktop-social { display: block; }
				.feastmobilenavbar .feastmenutoggle { display: none; } /* hide menu toggle */
				.feastmobilenavbar { grid-template-columns: 1fr 3fr 1fr 50px !important; } /* rearrange grid for desktop */
				.feastmenulogo { grid-column-end: span 1 !important; }
				.desktop-inline-modern-menu ul {
					display: grid;
					grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
					height: 70px;
					overflow: hidden;
					margin: 0 17px;
				}
				.desktop-inline-modern-menu ul li {
					display: flex;
					justify-content: center;
					align-items: center;
					min-height: 70px;
				}
				.desktop-inline-modern-menu ul li:nth-child(n+6) { display: none; }
				.modern-menu-desktop-social .simple-social-icons li:nth-child(n+4), .modern-menu-desktop-social .widgettitle { display: none; }
				.modern-menu-desktop-social { display: flex !important; justify-content: center; align-items: center; }
				.feastmobilenavbar a { color: #000; text-decoration: none; }

			} /* end desktop query */
			 /* end testing */
		

		@media only screen and ( max-width: 1199px ) {
			.feastmenulogo {grid-column-end: span 3; }
			.feastsubscribebutton { grid-column-end: span 2; }
		}
		@media only screen and (max-width: 359px) { /* 320px fix */
			.feastmobilenavbar {
				grid-template-columns: repeat(6, minmax(50px, 1fr));
			}
			.feastmenulogo {grid-column-end: span 2; }		}
		header.site-header, .nav-primary  {
			display: none !important;
			visibility: hidden;
		}
		.site-container, .body-template-content {
			margin-top: 80px; /* prevents menu overlapping content */
		}
		@media only screen and ( min-width: 1200px ) {
			.feastmobilenavbar {
				width: 100%;
				left: 0;
				padding-left: calc(50% - 550px);
				padding-right: calc(50% - 550px);
			}
							.feastsubscribebutton { display: none; }
					}
		@media print {
			.feastmobilenavbar { position: static; }
		}
		</style>

		<style id='feast-increase-content-width'>@media only screen and (min-width: 1200px) { #genesis-content { min-width: 728px; } #content-container { min-width: 728px; }  }</style>
		<style id='feast-system-fonts'>body {font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !important;}
h1,h2,h3,h4,h5,h6 {font-family:-apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !important;}
</style>
	<style id='feast-edit-font-sizes'>body { font-size: 18px; }</style><link rel="icon" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/12/cropped-metemgee-favicon-512-1-32x32.png" sizes="32x32" />
<link rel="icon" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/12/cropped-metemgee-favicon-512-1-192x192.png" sizes="192x192" />
<link rel="apple-touch-icon" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/12/cropped-metemgee-favicon-512-1-180x180.png" />
<meta name="msapplication-TileImage" content="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/12/cropped-metemgee-favicon-512-1-270x270.png" />
		<style type="text/css" id="wp-custom-css">
			/* Modern Footer (sr)
------------------------------------------ */

.feast-button a {
    border: 2px solid #c78d92;
    padding: 7px 14px;
    border-radius: 20px;
    background: #c78d92;
    color: #ffffff !important;
    text-decoration: none !important;
    font-weight: bold;
}

/* 60 minute customization 11/16/21 (sr)
------------------------------------------ */
.search-form input {
    background: #ffffff url(images/search.svg) center right 10px no-repeat !important;
		border: 1px solid #127c84;
	border-bottom: 1px solid #127c84;
}

.listing-item img, .about-the-author {
    border-top: 2px solid #127c84 !important;
}

a {
	color: #127c84;
}

a:hover,
a:focus {
	color: #c78d92;
}

.entry-title,
.entry-title a,
	color: #127c84;
	text-decoration: none;
}

.entry-title a:hover,
.entry-title a:focus {
	color: #c78d92;
}

@media only screen and (min-width: 1024px) {
.feast-full-width-wrapper {
    background: #127c84 !important;
}
}
@media only screen and (max-width: 425px) {

.wp-block-post-featured-image + .remove_padding > .mv-ad-box {

margin-top: 10px;

}

}

@media only screen and (max-width: 399px) {

.wprm-recipe-container li .mv-ad-box {

margin-left: -32px;

}

}

@media only screen and (max-width: 359px) {

.site-inner {

padding-left: 10px;

padding-right: 10px;

}

li .mv-ad-box {

min-width: 300px;

margin-left: -37px;

}

.wprm-recipe-template-compact {

padding-left: 0px !important;

padding-right: 0px !important;

border-left-width: 0px !important;

border-right-width: 0px !important;

}

}		</style>
		
     <style id="feast-homepage-styling-233">

          
     </style>
<noscript><style id="rocket-lazyload-nojs-css">.rll-youtube-player, [data-lazy-src]{display:none !important;}</style></noscript><script type="rocketlazyloadscript">
/*! loadCSS rel=preload polyfill. [c]2017 Filament Group, Inc. MIT License */
(function(w){"use strict";if(!w.loadCSS){w.loadCSS=function(){}}
var rp=loadCSS.relpreload={};rp.support=(function(){var ret;try{ret=w.document.createElement("link").relList.supports("preload")}catch(e){ret=!1}
return function(){return ret}})();rp.bindMediaToggle=function(link){var finalMedia=link.media||"all";function enableStylesheet(){link.media=finalMedia}
if(link.addEventListener){link.addEventListener("load",enableStylesheet)}else if(link.attachEvent){link.attachEvent("onload",enableStylesheet)}
setTimeout(function(){link.rel="stylesheet";link.media="only x"});setTimeout(enableStylesheet,3000)};rp.poly=function(){if(rp.support()){return}
var links=w.document.getElementsByTagName("link");for(var i=0;i<links.length;i++){var link=links[i];if(link.rel==="preload"&&link.getAttribute("as")==="style"&&!link.getAttribute("data-loadcss")){link.setAttribute("data-loadcss",!0);rp.bindMediaToggle(link)}}};if(!rp.support()){rp.poly();var run=w.setInterval(rp.poly,500);if(w.addEventListener){w.addEventListener("load",function(){rp.poly();w.clearInterval(run)})}else if(w.attachEvent){w.attachEvent("onload",function(){rp.poly();w.clearInterval(run)})}}
if(typeof exports!=="undefined"){exports.loadCSS=loadCSS}
else{w.loadCSS=loadCSS}}(typeof global!=="undefined"?global:this))
</script></head>
<body class="post-template-default single single-post postid-233 single-format-standard feast-plugin header-full-width content-sidebar genesis-breadcrumbs-hidden genesis-footer-widgets-hidden seasoned-pro"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-dark-grayscale"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0 0.49803921568627" /><feFuncG type="table" tableValues="0 0.49803921568627" /><feFuncB type="table" tableValues="0 0.49803921568627" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-grayscale"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0 1" /><feFuncG type="table" tableValues="0 1" /><feFuncB type="table" tableValues="0 1" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-purple-yellow"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0.54901960784314 0.98823529411765" /><feFuncG type="table" tableValues="0 1" /><feFuncB type="table" tableValues="0.71764705882353 0.25490196078431" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-blue-red"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0 1" /><feFuncG type="table" tableValues="0 0.27843137254902" /><feFuncB type="table" tableValues="0.5921568627451 0.27843137254902" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-midnight"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0 0" /><feFuncG type="table" tableValues="0 0.64705882352941" /><feFuncB type="table" tableValues="0 1" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-magenta-yellow"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0.78039215686275 1" /><feFuncG type="table" tableValues="0 0.94901960784314" /><feFuncB type="table" tableValues="0.35294117647059 0.47058823529412" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-purple-green"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0.65098039215686 0.40392156862745" /><feFuncG type="table" tableValues="0 1" /><feFuncB type="table" tableValues="0.44705882352941 0.4" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 0 0" width="0" height="0" focusable="false" role="none" style="visibility: hidden; position: absolute; left: -9999px; overflow: hidden;" ><defs><filter id="wp-duotone-blue-orange"><feColorMatrix color-interpolation-filters="sRGB" type="matrix" values=" .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 .299 .587 .114 0 0 " /><feComponentTransfer color-interpolation-filters="sRGB" ><feFuncR type="table" tableValues="0.098039215686275 1" /><feFuncG type="table" tableValues="0 0.66274509803922" /><feFuncB type="table" tableValues="0.84705882352941 0.41960784313725" /><feFuncA type="table" tableValues="1 1" /></feComponentTransfer><feComposite in2="SourceGraphic" operator="in" /></filter></defs></svg><div class="site-container"><ul class="genesis-skip-link"><li><a href="#genesis-nav-primary" class="screen-reader-shortcut"> Skip to primary navigation</a></li><li><a href="#genesis-content" class="screen-reader-shortcut"> Skip to main content</a></li><li><a href="#genesis-sidebar-primary" class="screen-reader-shortcut"> Skip to primary sidebar</a></li></ul><header class="site-header"><div class="wrap"><div class="title-area"><div class="site-title"><a href="https://metemgee.com/">Metemgee</a></div></div><nav class="nav-primary" aria-label="Main" id="genesis-nav-primary"><div class="wrap"><ul id="menu-feast-modern-mobile-menu" class="menu genesis-nav-menu menu-primary js-superfish"><li id="menu-item-10033" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10033"><a href="https://metemgee.com/about-me/"><span >Meet Althea Brown</span></a></li>
<li id="menu-item-10030" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10030"><a href="https://metemgee.com/recipes/"><span >Recipes</span></a></li>
<li id="menu-item-10031" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-10031"><a href="https://www.amazon.com/shop/metemgee"><span >Shop</span></a></li>
<li id="menu-item-12432" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-12432"><a href="https://metemgee.com/work-with-me/"><span >Contact Me</span></a></li>
<li id="seasoned-social" class="seasoned-social menu-item"><aside class="widget-area"><h2 class="genesis-sidebar-title screen-reader-text">Nav Social Menu</h2><section id="simple-social-icons-9" class="widget simple-social-icons"><div class="widget-wrap"><ul class="aligncenter"><li class="ssi-facebook"><a href="https://www.facebook.com/metemgee" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-facebook" aria-labelledby="social-facebook-9"><title id="social-facebook-9">Facebook</title><use xlink:href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-facebook"></use></svg></a></li><li class="ssi-instagram"><a href="https://www.instagram.com/metemgee/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-instagram" aria-labelledby="social-instagram-9"><title id="social-instagram-9">Instagram</title><use xlink:href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-instagram"></use></svg></a></li><li class="ssi-pinterest"><a href="https://www.pinterest.com/metemgee/_created/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-pinterest" aria-labelledby="social-pinterest-9"><title id="social-pinterest-9">Pinterest</title><use xlink:href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-pinterest"></use></svg></a></li><li class="ssi-youtube"><a href="https://www.youtube.com/user/MetemgeeBlog" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-youtube" aria-labelledby="social-youtube-9"><title id="social-youtube-9">YouTube</title><use xlink:href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-youtube"></use></svg></a></li></ul></div></section>
</aside></li><li id="seasoned-search" class="seasoned-search menu-item"><form class="search-form" method="get" action="https://metemgee.com/" role="search"><label class="search-form-label screen-reader-text" for="searchform-1">search...</label><input class="search-form-input" type="search" name="s" id="searchform-1" placeholder="search..."><input class="search-form-submit" type="submit" value="Search"><meta content="https://metemgee.com/?s={s}"></form></li></ul></div></nav></div></header><div class="feastmobilenavbar"><div class="feastmenutoggle"><a href="#feastmobilemenu"><?xml version="1.0" encoding="iso-8859-1"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "//www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg version="1.1" id="Capa_1" xmlns="//www.w3.org/2000/svg" xmlns:xlink="//www.w3.org/1999/xlink" x="0px" y="0px" width="30px" height="30px" viewBox="0 0 459 459" style="enable-background:new 0 0 459 459;" xml:space="preserve" aria-labelledby="menuicon" role="img">
	<title id="menuicon">menu icon</title>
	<g id="menu">
		<path fill="currentColor" d="M0,382.5h459v-51H0V382.5z M0,255h459v-51H0V255z M0,76.5v51h459v-51H0z"/>
	</g>
</svg>
</a></div><div class="feastmenulogo"><a href="https://metemgee.com"><img src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-200x70-1.png" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-400x140-1.png 2x" alt="go to homepage" data-skip-lazy data-pin-nopin="true" height="70" width="200" /></a></div><nav class='desktop-inline-modern-menu'><ul id="menu-feast-modern-mobile-menu-1" class="menu"><li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10033"><a href="https://metemgee.com/about-me/">Meet Althea Brown</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10030"><a href="https://metemgee.com/recipes/">Recipes</a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-10031"><a href="https://www.amazon.com/shop/metemgee">Shop</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-12432"><a href="https://metemgee.com/work-with-me/">Contact Me</a></li>
</ul></nav><div class='modern-menu-desktop-social'><div id="feast-social"><li id="simple-social-icons-8" class="widget simple-social-icons"><ul class="alignleft"><li class="ssi-facebook"><a data-wpel-link="ignore" href="https://www.facebook.com/metemgee" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-facebook" aria-labelledby="social-facebook-8"><title id="social-facebook-8">Facebook</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-facebook"></use></svg></a></li><li class="ssi-instagram"><a data-wpel-link="ignore" href="https://www.instagram.com/metemgee/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-instagram" aria-labelledby="social-instagram-8"><title id="social-instagram-8">Instagram</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-instagram"></use></svg></a></li><li class="ssi-pinterest"><a data-wpel-link="ignore" href="https://www.pinterest.com/metemgee/_created/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-pinterest" aria-labelledby="social-pinterest-8"><title id="social-pinterest-8">Pinterest</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-pinterest"></use></svg></a></li><li class="ssi-youtube"><a data-wpel-link="ignore" href="https://www.youtube.com/user/MetemgeeBlog" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-youtube" aria-labelledby="social-youtube-8"><title id="social-youtube-8">YouTube</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-youtube"></use></svg></a></li></ul></li>
</div></div><div class="feastsubscribebutton"><a href="/subscribe/"><svg id="svg" version="1.1" xmlns="//www.w3.org/2000/svg" xmlns:xlink="//www.w3.org/1999/xlink" height="30px" width="90px" viewBox="0, 0, 400,62.365591397849464">
  <title>subscribe</title>
  <g id="svgg">
    <path fill="currentColor" id="path0" d="M26.050 5.330 C 19.725 7.308,15.771 12.123,15.771 17.846 C 15.771 25.406,19.962 29.225,32.891 33.446 C 48.466 38.530,48.556 50.896,33.017 50.896 C 25.829 50.896,22.500 48.560,20.505 42.115 C 19.726 39.597,14.337 40.411,14.337 43.046 C 14.337 56.105,41.674 61.606,48.769 49.975 C 54.448 40.665,48.765 31.572,34.767 27.571 C 23.980 24.488,20.269 20.193,23.310 14.313 C 27.257 6.680,43.728 9.562,43.728 17.886 C 43.728 19.171,44.177 19.355,47.312 19.355 C 49.283 19.355,50.896 19.252,50.896 19.127 C 50.896 9.148,37.546 1.734,26.050 5.330 M160.932 4.926 C 143.613 9.505,145.768 26.536,164.445 32.693 C 175.194 36.236,177.778 38.236,177.778 43.011 C 177.778 53.848,156.854 53.818,154.473 42.977 C 153.842 40.106,147.658 39.647,147.686 42.473 C 147.827 56.888,176.357 61.890,183.180 48.696 C 187.688 39.978,182.226 32.186,168.371 27.569 C 156.805 23.715,152.605 17.927,157.885 13.118 C 164.593 7.008,177.778 10.406,177.778 18.244 C 177.778 19.087,178.577 19.355,181.097 19.355 L 184.417 19.355 183.994 16.747 C 182.636 8.383,170.802 2.317,160.932 4.926 M205.522 5.288 C 193.113 9.929,187.498 27.839,193.471 43.728 C 200.113 61.398,225.168 60.783,229.987 42.832 L 230.709 40.143 227.272 40.143 C 224.006 40.143,223.813 40.253,223.393 42.354 C 221.152 53.560,205.804 54.266,200.382 43.412 C 197.373 37.389,197.248 24.155,200.140 17.838 C 205.236 6.706,220.504 7.247,223.462 18.664 C 224.326 21.998,230.667 22.645,230.225 19.355 C 228.759 8.450,216.195 1.295,205.522 5.288 M58.781 24.396 C 58.781 45.482,59.019 47.008,62.941 51.141 C 70.903 59.530,87.303 57.865,93.053 48.085 L 94.982 44.803 95.203 24.910 L 95.424 5.018 92.199 5.018 L 88.974 5.018 88.752 24.194 C 88.469 48.664,87.490 50.887,76.988 50.893 C 66.447 50.900,65.236 48.111,65.234 23.835 L 65.233 5.018 62.007 5.018 L 58.781 5.018 58.781 24.396 M106.093 30.538 L 106.093 56.059 118.100 55.784 C 131.707 55.472,134.341 54.673,138.131 49.704 C 142.597 43.849,140.283 32.689,134.070 30.116 L 131.852 29.197 134.377 27.481 C 140.228 23.505,140.846 14.573,135.646 9.123 C 132.673 6.006,128.030 5.018,116.357 5.018 L 106.093 5.018 106.093 30.538 M240.143 30.466 L 240.143 55.914 243.369 55.914 L 246.595 55.914 246.595 45.520 L 246.595 35.125 252.509 35.126 L 258.423 35.127 264.025 45.521 L 269.628 55.914 273.190 55.914 C 276.653 55.914,276.730 55.869,275.923 54.301 C 275.467 53.414,272.875 48.634,270.163 43.679 C 264.354 33.065,264.551 34.140,268.014 31.954 C 278.032 25.630,275.856 9.891,264.455 6.209 C 261.718 5.325,258.109 5.018,250.455 5.018 L 240.143 5.018 240.143 30.466 M284.588 30.466 L 284.588 55.914 287.814 55.914 L 291.039 55.914 291.039 30.466 L 291.039 5.018 287.814 5.018 L 284.588 5.018 284.588 30.466 M303.226 30.466 L 303.226 55.914 313.953 55.914 C 325.859 55.914,330.021 55.026,333.601 51.722 C 339.739 46.056,339.150 35.284,332.463 30.920 L 329.863 29.224 332.594 26.619 C 336.044 23.329,337.133 19.713,336.111 14.946 C 334.474 7.313,329.244 5.018,313.490 5.018 L 303.226 5.018 303.226 30.466 M348.387 30.466 L 348.387 55.914 364.559 55.914 L 380.732 55.914 380.509 53.226 L 380.287 50.538 367.563 50.342 L 354.839 50.146 354.839 41.202 L 354.839 32.258 365.950 32.258 L 377.061 32.258 377.061 29.749 L 377.061 27.240 365.950 27.240 L 354.839 27.240 354.839 18.996 L 354.839 10.753 367.384 10.753 L 379.928 10.753 379.928 7.885 L 379.928 5.018 364.158 5.018 L 348.387 5.018 348.387 30.466 M129.099 11.862 C 132.543 13.644,133.822 19.465,131.498 22.784 C 129.472 25.675,126.727 26.523,119.390 26.523 L 112.545 26.523 112.545 18.638 L 112.545 10.753 119.749 10.753 C 124.849 10.753,127.579 11.077,129.099 11.862 M263.574 12.151 C 266.573 13.979,267.549 15.950,267.549 20.179 C 267.549 27.041,264.112 29.448,253.584 29.960 L 246.595 30.299 246.595 20.526 L 246.595 10.753 253.943 10.755 C 259.953 10.758,261.706 11.011,263.574 12.151 M328.021 13.122 C 333.818 19.868,328.285 26.523,316.881 26.523 L 310.394 26.523 310.394 18.575 L 310.394 10.626 318.343 10.868 C 326.030 11.103,326.349 11.177,328.021 13.122 M129.773 33.345 C 133.706 35.379,135.094 40.558,133.031 45.495 C 131.463 49.248,128.894 50.179,120.107 50.179 L 112.545 50.179 112.545 41.219 L 112.545 32.258 120.107 32.258 C 125.465 32.258,128.283 32.575,129.773 33.345 M329.093 34.958 C 332.751 39.055,331.571 46.679,326.905 49.092 C 325.435 49.852,322.636 50.179,317.598 50.179 L 310.394 50.179 310.394 41.157 L 310.394 32.135 318.698 32.376 L 327.003 32.616 329.093 34.958 " stroke="none" fill-rule="evenodd"></path>
  </g>
</svg>
</a></div><div class="feastsearchtoggle"><a href="#feastmobilemenu"><svg xmlns="//www.w3.org/2000/svg" xmlns:xlink="//www.w3.org/1999/xlink" xml:space="preserve" xmlns:svg="//www.w3.org/2000/svg" version="1.1" x="0px" y="0px" width="30px" height="30px" viewBox="0 0 100 100" aria-labelledby="searchicon" role="img">
  <title id="searchicon">search icon</title>
  <g transform="translate(0,-952.36218)">
    <path fill="currentColor" d="M 40 11 C 24.007431 11 11 24.00743 11 40 C 11 55.9926 24.007431 69 40 69 C 47.281794 69 53.935267 66.28907 59.03125 61.84375 L 85.59375 88.40625 C 86.332786 89.16705 87.691654 89.1915 88.4375 88.4375 C 89.183345 87.6834 89.175154 86.2931 88.40625 85.5625 L 61.875 59.03125 C 66.312418 53.937244 69 47.274551 69 40 C 69 24.00743 55.992569 11 40 11 z M 40 15 C 53.830808 15 65 26.16919 65 40 C 65 53.8308 53.830808 65 40 65 C 26.169192 65 15 53.8308 15 40 C 15 26.16919 26.169192 15 40 15 z " transform="translate(0,952.36218)">
    </path>
  </g>
</svg>
</a></div></div><div id="feastmobilemenu" class="feastmobilemenu-background" aria-label="main"><div class="mmm-dialog"><div class="mmm-content"><a href="https://metemgee.com"><img id="mmmlogo" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%200%200'%3E%3C/svg%3E" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-400x140-1.png 2x" alt="Homepage link" data-pin-nopin="true" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-200x70-1.png" /><noscript><img id="mmmlogo" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-200x70-1.png" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/10/metemgee-logo-lockup-script-2color-web-400x140-1.png 2x" alt="Homepage link" data-pin-nopin="true" /></noscript></a><div id="feast-mobile-search"><form class="search-form" method="get" action="https://metemgee.com/" role="search"><label class="search-form-label screen-reader-text" for="searchform-2">search...</label><input class="search-form-input" type="search" name="s" id="searchform-2" placeholder="search..."><input class="search-form-submit" type="submit" value="Search"><meta content="https://metemgee.com/?s={s}"></form></div><ul id="menu-feast-modern-mobile-menu-2" class="menu"><li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10033"><a href="https://metemgee.com/about-me/">Meet Althea Brown</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-10030"><a href="https://metemgee.com/recipes/">Recipes</a></li>
<li class="menu-item menu-item-type-custom menu-item-object-custom menu-item-10031"><a href="https://www.amazon.com/shop/metemgee">Shop</a></li>
<li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-12432"><a href="https://metemgee.com/work-with-me/">Contact Me</a></li>
</ul><div id="feast-mobile-menu-social-icons"><div id="feast-social"><li id="simple-social-icons-8" class="widget simple-social-icons"><ul class="alignleft"><li class="ssi-facebook"><a data-wpel-link="ignore" href="https://www.facebook.com/metemgee" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-facebook" aria-labelledby="social-facebook-8"><title id="social-facebook-8">Facebook</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-facebook"></use></svg></a></li><li class="ssi-instagram"><a data-wpel-link="ignore" href="https://www.instagram.com/metemgee/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-instagram" aria-labelledby="social-instagram-8"><title id="social-instagram-8">Instagram</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-instagram"></use></svg></a></li><li class="ssi-pinterest"><a data-wpel-link="ignore" href="https://www.pinterest.com/metemgee/_created/" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-pinterest" aria-labelledby="social-pinterest-8"><title id="social-pinterest-8">Pinterest</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-pinterest"></use></svg></a></li><li class="ssi-youtube"><a data-wpel-link="ignore" href="https://www.youtube.com/user/MetemgeeBlog" target="_blank" rel="noopener noreferrer"><svg role="img" class="social-youtube" aria-labelledby="social-youtube-8"><title id="social-youtube-8">YouTube</title><use xlink:data-wpel-link="ignore" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/symbol-defs.svg#social-youtube"></use></svg></a></li></ul></li>
</div></div><a href="#" class="closebtn">×</a></div></div></div><div class="site-inner"><div class="content-sidebar-wrap"><main class="content" id="genesis-content"><p id="breadcrumbs"><span><span><a href="https://metemgee.com/">"Home"</a></span> » <span><a href="https://metemgee.com/category/baking/">Baking</a></span></span></p><article class="post-233 post type-post status-publish format-standard has-post-thumbnail category-baking category-desserts category-quick-and-easy category-vegan tag-coconut-buns tag-how-to-make-coconut-buns tag-how-to-make-coconut-drops tag-how-to-make-coconut-rock-buns tag-how-to-make-dairy-free-coconut-buns tag-how-to-make-egg-free-coconut-buns tag-how-to-make-vegan-coconut-buns tag-how-to-make-vegan-coconut-drops tag-how-to-make-vegan-rock-buns tag-metemgee tag-metemgee-blog mv-content-wrapper entry" aria-label="Rich Coconut Buns"><header class="entry-header"><h1 class="entry-title">Rich Coconut Buns</h1>
<p class="entry-meta">Published: <time class="entry-time">Jan 30, 2013</time> · Modified: <time class="entry-modified-time">May 3, 2022</time> by <span class="entry-author"><span class="entry-author-name">Althea Brown</span></span> · This post may contain affiliate links · <span class="entry-comments-link"><a href="https://metemgee.com/2013/01/30/rich-coconut-buns/#comments">16 Comments</a></span></p></header><div class="entry-content">
<h2 id="updated-582020"   >UPDATED 5/8/2020</h2>



<p><em>Rich Coconut Buns are one of my favorite afternoon snacks from my childhood. These buns are very similar to scones in how they are made, but no one ever calls them scones. They are simply buns or coconut buns regardless of if there is one or more than one. I learned to make buns in my Home Ec. class in high school. We used the rub in method for combining the fat and the dry ingredients. For years, I was using a creaming method, to make my buns but recently I went right back into the rub in method for the fat and the dry ingredients. I love that my buns making has come full circle. And before we get to the recipe, don't forget to subscribe to my blog so you don't miss upcoming recipes and please follow me on <a href="https://www.instagram.com/metemgee/">Instagram.</a></em></p>



<figure class="wp-block-image"><img decoding="async" width="1024" height="824" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20824'%3E%3C/svg%3E" alt="" class="wp-image-3621" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1024x824.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-600x483.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-300x241.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-768x618.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1536x1236.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-720x579.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-360x290.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-180x145.jpg 180w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1060x853.jpg 1060w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-550x442.jpg 550w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-621x500.jpg 621w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1920x1545.jpg 1920w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1342x1080.jpg 1342w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-2000x1609.jpg 2000w" data-lazy-sizes="(max-width: 1024px) 100vw, 1024px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1024x824.jpg" /><noscript><img decoding="async" width="1024" height="824" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1024x824.jpg" alt="" class="wp-image-3621" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1024x824.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-600x483.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-300x241.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-768x618.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1536x1236.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-scaled-scaled.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-720x579.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-360x290.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-180x145.jpg 180w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1060x853.jpg 1060w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-550x442.jpg 550w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-621x500.jpg 621w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1920x1545.jpg 1920w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-1342x1080.jpg 1342w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5312-2000x1609.jpg 2000w" sizes="(max-width: 1024px) 100vw, 1024px" /></noscript></figure>


<style>#feast-advanced-jump-to { z-index: 999; border: none; opacity: 0.97; background: #FCFCFC; border-left:4px solid #CCC; padding:5px 0 10px 20px; margin-bottom: 57px;} #feast-advanced-jump-to summary, #feast-advanced-jump-to ul{ margin-left:0;min-height:50px;} #feast-advanced-jump-to li { list-style-type:none; }  #feast-advanced-jump-to li a { text-decoration: none; }</style>
<details id="feast-advanced-jump-to" open><summary>Jump to:</summary><ul id="feast-jump-to-list"><li><a href="#updated-582020" >UPDATED 5/8/2020</a></li>
<li><a href="#simple-ingredients-for-rich-coconut-buns" >Simple Ingredients for Rich Coconut Buns</a></li>
<li><a href="#using-coconut-flakes" >Using Coconut Flakes</a></li>
<li><a href="#fun-for-the-family" >Fun for the Family</a></li>
<li><a href="#making-the-buns-vegan" >Making the Buns Vegan</a></li>
<li><a href="#the-rich-coconut-buns-video-tutorial" >The Rich Coconut Buns Video Tutorial:</a></li>
<li><a href="#save-it-for-later" >Save it for later</a></li>
<li><a href="#the-printable-rich-coconut-buns-recipe" >The Printable Rich Coconut Buns Recipe:</a></li>
<li><a href="#the-vegan-coconut-buns-recipe" >The Vegan Coconut Buns Recipe:</a></li>
<li><a href="#check-out-these-other-great-recipes" >Check out these other great recipes:</a></li>
</ul>
</details>



<h2 id="simple-ingredients-for-rich-coconut-buns"   >Simple Ingredients for Rich Coconut Buns</h2>



<figure class="wp-block-image"><img decoding="async" width="856" height="1024" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20856%201024'%3E%3C/svg%3E" alt="" class="wp-image-3624" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-856x1024.jpg 856w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-scaled-600x718.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-251x300.jpg 251w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-768x919.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-1284x1536.jpg 1284w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-1712x2048.jpg 1712w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-scaled.jpg 1605w" data-lazy-sizes="(max-width: 856px) 100vw, 856px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-856x1024.jpg" /><noscript><img decoding="async" width="856" height="1024" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-856x1024.jpg" alt="" class="wp-image-3624" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-856x1024.jpg 856w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-scaled-600x718.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-251x300.jpg 251w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-768x919.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-1284x1536.jpg 1284w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-1712x2048.jpg 1712w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-64-scaled.jpg 1605w" sizes="(max-width: 856px) 100vw, 856px" /></noscript></figure>



<p>Traditionally we make buns using all purpose flour, sugar, fresh grated coconuts and lots of butter, with some baking powder and spices. In my home no one likes raisins or any other kind of dried fruits in their buns. Many people love to add a maraschino cherry to their buns before baking. No one in my family likes this, so we just skip it. When you're making your buns, you can feel free to add raisins or currents and top it with a maraschino cherry. You can also switch up the spices by adding some grated nutmeg and a bit of orange zest for freshness. But we keep our buns pretty basic.</p>



<h2 id="using-coconut-flakes"   >Using Coconut Flakes</h2>



<p>Before discovering frozen grated coconuts in my local Asian market I made my coconut buns with sweetened coconut flakes. It makes a pretty tasty coconut buns. If you are using coconut flakes, I recommend using 3 ½ cups of coconut flakes and pulsing it in the food processor to make it closer to the texture of grated coconut.</p>



<h2 id="fun-for-the-family"   >Fun for the Family</h2>



<figure class="wp-block-image"><img decoding="async" width="1024" height="839" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20839'%3E%3C/svg%3E" alt="" class="wp-image-3623" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1024x839.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-scaled-600x492.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-300x246.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-768x629.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1536x1258.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-2048x1678.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-scaled.jpg 1920w" data-lazy-sizes="(max-width: 1024px) 100vw, 1024px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1024x839.jpg" /><noscript><img decoding="async" width="1024" height="839" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1024x839.jpg" alt="" class="wp-image-3623" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1024x839.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-scaled-600x492.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-300x246.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-768x629.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-1536x1258.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-2048x1678.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/FullSizeRender-65-scaled.jpg 1920w" sizes="(max-width: 1024px) 100vw, 1024px" /></noscript></figure>



<p>This recipe is very family friendly. Let the little ones help with rubbing the fat into the dry ingredients or even scooping the buns onto the baking sheet. My daughter loved pulling up a chair to the counter and helping to scoop these out and of course she loves eating buns.</p>



<div class="wp-block-image"><figure class="aligncenter"><img decoding="async" width="934" height="1024" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20934%201024'%3E%3C/svg%3E" alt="" class="wp-image-3622" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5310-934x1024.jpg"/><noscript><img decoding="async" width="934" height="1024" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/IMG_5310-934x1024.jpg" alt="" class="wp-image-3622"/></noscript></figure></div>



<h2 id="making-the-buns-vegan"   >Making the Buns Vegan</h2>



<p>My children have dairy allergies, so I've been converting my recipes to dairy free or vegan wherever I can. I converted this recipe to vegan, after my aunt (who has been vegan for decades) visited lasted year and made coconut buns with my children Her vegan buns tasted exactly the same as the regular butter filled buns and inspired me to switch to making vegan coconut buns.</p>



<h2 id="the-rich-coconut-buns-video-tutorial"   >The Rich Coconut Buns Video Tutorial:</h2>



<figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
<iframe title="Easy Rich Coconut Buns || With additional vegan option" width="720" height="405" src="https://www.youtube.com/embed/0kuj98OXbfE?feature=oembed" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div></figure>



<h2 id="save-it-for-later"   >Save it for later</h2>



<div class="wp-block-image"><figure class="aligncenter"><img decoding="async" width="683" height="1024" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20683%201024'%3E%3C/svg%3E" alt="" class="wp-image-3626" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-683x1024.png 683w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-600x900.png 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-200x300.png 200w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns.png 735w" data-lazy-sizes="(max-width: 683px) 100vw, 683px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-683x1024.png" /><noscript><img decoding="async" width="683" height="1024" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-683x1024.png" alt="" class="wp-image-3626" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-683x1024.png 683w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-600x900.png 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns-200x300.png 200w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/01/Coconut-Buns.png 735w" sizes="(max-width: 683px) 100vw, 683px" /></noscript></figure></div>



<h2 id="the-printable-rich-coconut-buns-recipe"   >The Printable Rich Coconut Buns Recipe:</h2>



<div class="easyrecipe" data-rating="0">
<div class="item ERName">[b]Rich Coconut Buns[/b]</div>
<div class="ERClear">&nbsp;</div>
<div class="ERHead">Cuisine: <span class="cuisine">Caribbean</span></div>
<div class="ERHead">Author: <span class="author">Althea Brown</span></div>
<div class="ERHead">Prep time: <time datetime="PT15M">15 mins</time></div>
<div class="ERHead">Cook time: <time datetime="PT25M">25 mins</time></div>
<div class="ERHead">Total time: <time datetime="PT40M">40 mins</time></div>
<div class="ERHead">Serves: <span class="yield">12 to 16 buns</span></div>
<div class="ERSummary summary">Grated coconut, butter and sugar combined with all purpose flour to form a sweet scone like bun/biscuit.</div>
<div class="ERIngredients">
<div class="ERIngredientsHeader">Ingredients</div>
<ul class="ingredients">
<li class="ingredient">2 cups All Purpose flour</li>
<li class="ingredient">1 cup of finely grated coconut (about 1 whole coconut) or 7 ounces of coconut flakes</li>
<li class="ingredient">1 teaspoon baking powder</li>
<li class="ingredient">¼ teaspoon salt</li>
<li class="ingredient">½ cup of brown sugar</li>
<li class="ingredient">½ cup of butter</li>
<li class="ingredient">2 eggs, beaten</li>
<li class="ingredient">½ teaspoon of vanilla extract</li>
<li class="ingredient">½ teaspoon of almond extract</li>
</ul>
</div>
<div class="ERInstructions">
<div class="ERInstructionsHeader">Instructions</div>
<div class="instructions">
<ol>
<li class="instruction">Preheat your oven to 350°F</li>
<li class="instruction">To a large mixing bowl add the all purpose flour, baking powder, salt and brown sugar and mix together well</li>
<li class="instruction">Then using a fork or a pastry blender cut/rub butter into flour mixture. You can grate your butter on the shred side of a cheese grater to make it easier to mix with the flour and dry ingredients</li>
<li class="instruction">When the dry ingredients and the butter are combined and form a crumbly texture add the grated coconuts and mix together well</li>
<li class="instruction">Next, beat together the eggs, vanilla extract and almond extract and set aside</li>
<li class="instruction">Then form a well in the center of the dry ingredients and add the eggs mixture</li>
<li class="instruction">Using a wooden spoon or spatula mix the eggs and dry ingredients until a soft dough forms</li>
<li class="instruction">Next on a greased baking sheet separate the dough into 12 to 16 pieces depending on the size of buns that you like. You can use a [url href="https://amzn.to/3fzVKn1"]cookie scoop[/url] for this step or two spoons</li>
<li class="instruction">Then bake for 25 minutes at 350°F</li>
<li class="instruction">Remove from the oven and place on a cooling rack to cool</li>
<li class="instruction">When cooled enjoy!</li>
</ol>
</div>
</div>
<div class="ERNutrition">&nbsp;</div>
<div>
<div class="ERNotesHeader">Notes</div>
<div class="ERNotes">You can substitute the fresh/frozen grated coconuts for 3 ½ cups of coconut flakes. I like to pulse the coconut flakes in the food processor to make the texture similar to grated coconut.[br][br]Check out the video tutorial [url href="https://youtu.be/0kuj98OXbfE"]HERE[/url]</div>
</div>
<div class="endeasyrecipe" style="display: none;">3.5.3251</div>
</div>



<h2 id="the-vegan-coconut-buns-recipe"   >The Vegan Coconut Buns Recipe:</h2>



<div class="easyrecipe" data-rating="0">
<div class="item ERName">[b]Vegan Coconut Buns[/b]</div>
<div class="ERClear">&nbsp;</div>
<div class="ERHead"><span class="xlate">Recipe Type</span>: <span class="type">Vegan</span></div>
<div class="ERHead">Cuisine: <span class="cuisine">Caribbean</span></div>
<div class="ERHead">Author: <span class="author">Althea Brown</span></div>
<div class="ERHead">Prep time: <time datetime="PT10M">10 mins</time></div>
<div class="ERHead">Cook time: <time datetime="PT30M">30 mins</time></div>
<div class="ERHead">Total time: <time datetime="PT40M">40 mins</time></div>
<div class="ERHead">Serves: <span class="yield">12-16 buns</span></div>
<div class="ERSummary summary">Grated coconut, coconut oil and coconut milk combined with all purpose flour to form a sweet scone like bun/biscuit.</div>
<div class="ERIngredients">
<div class="ERIngredientsHeader">Ingredients</div>
<ul class="ingredients">
<li class="ingredient">2 cups All Purpose flour</li>
<li class="ingredient">1 cup of finely grated coconut (about 1 whole coconut) or 7 ounces of coconut flakes</li>
<li class="ingredient">½ cup of brown sugar</li>
<li class="ingredient">½ cup of coconut oil</li>
<li class="ingredient">¼ teaspoon salt</li>
<li class="ingredient">½ cup of coconut milk</li>
<li class="ingredient">1 teaspoon baking powder</li>
<li class="ingredient">½ teaspoon of vanilla extract</li>
<li class="ingredient">½ teaspoon of almond extract</li>
</ul>
</div>
<div class="ERInstructions">
<div class="ERInstructionsHeader">Instructions</div>
<div class="instructions">
<ol>
<li class="instruction">Preheat your oven to 350°F</li>
<li class="instruction">To a large mixing bowl add the all purpose flour, baking powder, salt and brown sugar and mix together well</li>
<li class="instruction">Then using a fork or cut/rub coconut oil into the flour mixture.</li>
<li class="instruction">When the dry ingredients and the coconut oil are combined and form a crumbly texture add the grated coconuts and mix together well</li>
<li class="instruction">Next add the vanilla extract and almond extract to the coconut milk and set aside</li>
<li class="instruction">Then form a well in the center of the dry ingredients and add the coconut milk mixture</li>
<li class="instruction">Using a wooden spoon or spatula mix the wet ingredients and dry ingredients until a soft dough forms</li>
<li class="instruction">Next on a greased baking sheet separate the dough into 12 to 16 scoops depending on the size of buns that you like. You can use a [url href="https://amzn.to/3fzVKn1"]cookie scoop[/url] for this step or two spoons</li>
<li class="instruction">Then bake for 30 minutes at 350°F</li>
<li class="instruction">Remove from the oven and place on a cooling rack to cool</li>
<li class="instruction">When cooled enjoy!</li>
</ol>
</div>
</div>
<div class="ERNutrition">&nbsp;</div>
<div>
<div class="ERNotesHeader">Notes</div>
<div class="ERNotes">You can substitute the fresh/frozen grated coconuts for 3 ½ cups of coconut flakes. I like to pulse the coconut flakes in the food processor to make the texture similar to grated coconut.[br][br]Click [url href="https://youtu.be/0kuj98OXbfE"]HERE[/url] for the video tutorial</div>
</div>
<div class="endeasyrecipe" style="display: none;">3.5.3251</div>
</div>



<h2 id="check-out-these-other-great-recipes"   >Check out these other great recipes:</h2>



<h4 id="h-banana-muffins"><a href="https://metemgee.com/2013/03/13/bananas-over-banana-bread-banana-walnut-bread/">Banana Muffins</a></h4>



<div class="wp-block-image"><figure class="aligncenter"><a href="https://metemgee.com/2013/03/13/bananas-over-banana-bread-banana-walnut-bread/"><img decoding="async" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%200%200'%3E%3C/svg%3E" alt="" class="wp-image-3493" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/FullSizeRender-53-790x1024.jpg"/><noscript><img decoding="async" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/FullSizeRender-53-790x1024.jpg" alt="" class="wp-image-3493"/></noscript></a></figure></div>



<h4 id="h-butter-flaps"><a href="https://metemgee.com/2020/05/01/butter-flaps-or-coco-bread/">Butter Flaps</a></h4>



<div class="wp-block-image"><figure class="aligncenter"><a href="https://metemgee.com/2020/05/01/butter-flaps-or-coco-bread/"><img decoding="async" width="1024" height="680" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%201024%20680'%3E%3C/svg%3E" alt="" class="wp-image-3516" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1024x680.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-scaled-600x398.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-300x199.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-768x510.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1536x1020.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-scaled-scaled.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-720x478.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-360x239.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-180x120.jpg 180w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1060x704.jpg 1060w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-550x365.jpg 550w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-753x500.jpg 753w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1920x1275.jpg 1920w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1626x1080.jpg 1626w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-2000x1328.jpg 2000w" data-lazy-sizes="(max-width: 1024px) 100vw, 1024px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1024x680.jpg" /><noscript><img decoding="async" width="1024" height="680" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1024x680.jpg" alt="" class="wp-image-3516" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1024x680.jpg 1024w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-scaled-600x398.jpg 600w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-300x199.jpg 300w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-768x510.jpg 768w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1536x1020.jpg 1536w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-scaled-scaled.jpg 2048w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-720x478.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-360x239.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-180x120.jpg 180w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1060x704.jpg 1060w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-550x365.jpg 550w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-753x500.jpg 753w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1920x1275.jpg 1920w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-1626x1080.jpg 1626w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/04/IMG_5236-2000x1328.jpg 2000w" sizes="(max-width: 1024px) 100vw, 1024px" /></noscript></a></figure></div>



<p><em><strong>Affiliate Disclosure: This post contains Affiliate Links. This means that if you click on a link and complete a purchase I earn a commission at no extra cost to you. This does not affect my opinion about the products shared in anyway. These are truly my favorite products to use, with or without the commission. Thank you for checking out my post.&nbsp;</strong></em></p>
<!--<rdf:RDF xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#"
			xmlns:dc="http://purl.org/dc/elements/1.1/"
			xmlns:trackback="http://madskills.com/public/xml/rss/module/trackback/">
		<rdf:Description rdf:about="https://metemgee.com/2013/01/30/rich-coconut-buns/"
    dc:identifier="https://metemgee.com/2013/01/30/rich-coconut-buns/"
    dc:title="Rich Coconut Buns"
    trackback:ping="https://metemgee.com/2013/01/30/rich-coconut-buns/trackback/" />
</rdf:RDF>-->
</div><div class="feast-prev-next"><div class="feast-prev-post">&laquo; <a aria-label="Previous post: " href="https://metemgee.com/2013/01/23/30-minutes-meal-chicken-chowmein/" rel="prev">Guyanese Style Chicken Chowmein</a></div><div class="feast-next-post"><a aria-label="Next post: " href="https://metemgee.com/2013/02/06/altee-had-a-little-lamb-stew/" rel="next">Lamb Stew {With Instant Pot Instructions}</a> &raquo;</div></div><footer class="entry-footer"></footer></article><h2 class="screen-reader-text">Reader Interactions</h2><div class="entry-comments" id="comments"><h3>Comments</h3><ol class="comment-list">
	<li class="comment even thread-even depth-1" id="comment-210">
	<article id="article-comment-210">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Anisia</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">February 05, 2013 at 5:20 am</time></p>		</header>

		<div class="comment-content">
			
			<p>Althee, meh proud ah yuh gyal. Never knew you had a food blog. It's about time a fellow Guyanese, or should i say young generation Guyanese start something like this. There are some dishes that we learn from we muma that have no exact recipe. It's a pinch of this and a butter cup of that.  Love it!! Keep this blog going. Xoxox - Anisia</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-210' data-commentid="210" data-postid="233" data-belowelement="article-comment-210" data-respondelement="respond" data-replyto="Reply to Anisia" aria-label='Reply to Anisia'>Reply</a></div>
		
	</article>
	<ul class="children">

	<li class="comment byuser comment-author-alteebee bypostauthor odd alt depth-2" id="comment-211">
	<article id="article-comment-211">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Metemgee</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">February 05, 2013 at 8:09 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Thanks Anisia. It's a lot of work, but lots of fun!</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-211' data-commentid="211" data-postid="233" data-belowelement="article-comment-211" data-respondelement="respond" data-replyto="Reply to Metemgee" aria-label='Reply to Metemgee'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

	<li class="comment even thread-odd thread-alt depth-1" id="comment-212">
	<article id="article-comment-212">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Fan</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">July 30, 2013 at 7:49 am</time></p>		</header>

		<div class="comment-content">
			
			<p>Love the recipe, keep posting more.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-212' data-commentid="212" data-postid="233" data-belowelement="article-comment-212" data-respondelement="respond" data-replyto="Reply to Fan" aria-label='Reply to Fan'>Reply</a></div>
		
	</article>
	<ul class="children">

	<li class="comment byuser comment-author-alteebee bypostauthor odd alt depth-2" id="comment-213">
	<article id="article-comment-213">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Metemgee</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">August 01, 2013 at 11:47 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Thank you.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-213' data-commentid="213" data-postid="233" data-belowelement="article-comment-213" data-respondelement="respond" data-replyto="Reply to Metemgee" aria-label='Reply to Metemgee'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

	<li class="comment even thread-even depth-1" id="comment-214">
	<article id="article-comment-214">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Dr.Marquita Caroll</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">August 14, 2013 at 7:15 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Love my coconut bun, here the request, for the sugar buns what  are the bit of flour please what else?</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-214' data-commentid="214" data-postid="233" data-belowelement="article-comment-214" data-respondelement="respond" data-replyto="Reply to Dr.Marquita Caroll" aria-label='Reply to Dr.Marquita Caroll'>Reply</a></div>
		
	</article>
	<ul class="children">

	<li class="comment byuser comment-author-alteebee bypostauthor odd alt depth-2" id="comment-215">
	<article id="article-comment-215">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Metemgee</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">September 06, 2013 at 5:17 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Sugar buns? Not sure what those are...</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-215' data-commentid="215" data-postid="233" data-belowelement="article-comment-215" data-respondelement="respond" data-replyto="Reply to Metemgee" aria-label='Reply to Metemgee'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

	<li class="comment even thread-odd thread-alt depth-1" id="comment-216">
	<article id="article-comment-216">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Queen Bee</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">December 09, 2013 at 4:07 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>I was about to make the buns when I realized that the measurement does not added up.  1 cup is equal to 8 ozs.  So does the recipe need 8 ozs  or 4 ozs. of butter?  The same for the sugar, flour and coconut flakes.  6 ozs cannot equal to 1 cup and 7 ozs cannot equal 2 1/2 cups.  Please review.  Thank you.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-216' data-commentid="216" data-postid="233" data-belowelement="article-comment-216" data-respondelement="respond" data-replyto="Reply to Queen Bee" aria-label='Reply to Queen Bee'>Reply</a></div>
		
	</article>
	<ul class="children">

	<li class="comment byuser comment-author-alteebee bypostauthor odd alt depth-2" id="comment-217">
	<article id="article-comment-217">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Metemgee</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">December 09, 2013 at 9:39 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Hi there. Sorry for the confusion. I actually weighed my ingredients but got a bit sloppy with the conversion. You are right, for the butter, sugar is 1/2 cup. The flour is 3/4 cups (about) and the coconut flakes were actually 2 1/2 cups cause there are light in weight but a lot volume wise. I've also made this recipe measuring the ingredients with a measuring cup and I've used 1 cup of flour for a slightly denser bun. Hope this helps. I'm out of town on vacation and will adjust the site when I get home. Thanks for letting me know.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-217' data-commentid="217" data-postid="233" data-belowelement="article-comment-217" data-respondelement="respond" data-replyto="Reply to Metemgee" aria-label='Reply to Metemgee'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

	<li class="comment even thread-even depth-1" id="comment-218">
	<article id="article-comment-218">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Kim</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">February 23, 2014 at 9:28 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>This the third item I've made by following your receipe and I must say yummy. ( salara and the pumpkin receipe were the others, although I used butternut squash). Oh wait I forgot I also made roti but I don't have the technique to perfect it as yet. Next up is bake n cross bun for Easter. Keep the receipes coming. Thanks</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-218' data-commentid="218" data-postid="233" data-belowelement="article-comment-218" data-respondelement="respond" data-replyto="Reply to Kim" aria-label='Reply to Kim'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->

	<li class="comment odd alt thread-odd thread-alt depth-1" id="comment-18088">
	<article id="article-comment-18088">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Aria</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">November 06, 2020 at 5:53 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>I just found this website - the vegan coconut drops - oh mercy! I don't have the self-discipline to stop eating! They are SO good! I am not vegan but I can't eat eggs and miss out on so much. I used butter instead of coconut oil and almond milk instead of coconut but it was still sooooo good. I know I'm 7 years late but this was too good not to say thanks all the same.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-18088' data-commentid="18088" data-postid="233" data-belowelement="article-comment-18088" data-respondelement="respond" data-replyto="Reply to Aria" aria-label='Reply to Aria'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->

	<li class="comment even thread-even depth-1" id="comment-53549">
	<article id="article-comment-53549">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Elsa</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">June 20, 2021 at 10:51 am</time></p>		</header>

		<div class="comment-content">
			
			<p>Hi:  I love coconut buns. Is it possible for you to give me the original recipe? I’m just lost without it.  I’m sure this version is great, but I’m old school🙂</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-53549' data-commentid="53549" data-postid="233" data-belowelement="article-comment-53549" data-respondelement="respond" data-replyto="Reply to Elsa" aria-label='Reply to Elsa'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->

	<li class="comment odd alt thread-odd thread-alt depth-1" id="comment-59194">
	<article id="article-comment-59194">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Lisa Walker</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">October 17, 2021 at 9:59 am</time></p>		</header>

		<div class="comment-content">
			
			<p>Hi,<br />
Is the coconut milk the chilled milk from a carton or the canned variety please?<br />
Many thanks,<br />
Lisa</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-59194' data-commentid="59194" data-postid="233" data-belowelement="article-comment-59194" data-respondelement="respond" data-replyto="Reply to Lisa Walker" aria-label='Reply to Lisa Walker'>Reply</a></div>
		
	</article>
	<ul class="children">

	<li class="comment byuser comment-author-alteebrowngmail-com even depth-2" id="comment-61537">
	<article id="article-comment-61537">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Althea Brown</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">December 13, 2021 at 9:47 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>You can use the milk from the can or the one in the carton just make sure it says coconut milk and not coconut beverage</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-61537' data-commentid="61537" data-postid="233" data-belowelement="article-comment-61537" data-respondelement="respond" data-replyto="Reply to Althea Brown" aria-label='Reply to Althea Brown'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ul><!-- .children -->
</li><!-- #comment-## -->

	<li class="comment odd alt thread-even depth-1" id="comment-66098">
	<article id="article-comment-66098">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Shaquille</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">March 10, 2022 at 2:38 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>Tried it, loved it. Well done.</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-66098' data-commentid="66098" data-postid="233" data-belowelement="article-comment-66098" data-respondelement="respond" data-replyto="Reply to Shaquille" aria-label='Reply to Shaquille'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->

	<li class="comment even thread-odd thread-alt depth-1" id="comment-69490">
	<article id="article-comment-69490">

		
		<header class="comment-header">
			<p class="comment-author">
				<span class="comment-author-name">Sherisha</span> <span class="says">says</span>			</p>

			<p class="comment-meta"><time class="comment-time">November 21, 2022 at 5:03 pm</time></p>		</header>

		<div class="comment-content">
			
			<p>I just made these for the first time and WOW! They are so perfect! My dad was always the one to make buns in our family, but hasn't in a while. I'm so glad I gave these a shot; they taste just like his and were so quick and easy to make (especially because I didn't have to crack open, separate, and grate a fresh coconut :). Thank you and I can't wait to make them again!</p>
		</div>

		<div class="comment-reply"><a rel='nofollow' class='comment-reply-link' href='#comment-69490' data-commentid="69490" data-postid="233" data-belowelement="article-comment-69490" data-respondelement="respond" data-replyto="Reply to Sherisha" aria-label='Reply to Sherisha'>Reply</a></div>
		
	</article>
	</li><!-- #comment-## -->
</ol></div><div class="entry-pings"><h3>Trackbacks</h3><ol class="ping-list">		<li id="comment-63016" class="trackback even thread-even depth-1">
			<article id="div-comment-63016" class="comment-body">
				<footer class="comment-meta">
					<div class="comment-author vcard">
												<b class="fn">3mutation</b> <span class="says">says:</span>					</div><!-- .comment-author -->

					<div class="comment-metadata">
						<a href="https://metemgee.com/2013/01/30/rich-coconut-buns/#comment-63016"><time datetime="2022-01-12T16:38:16-07:00">January 12, 2022 at 4:38 pm</time></a>					</div><!-- .comment-metadata -->

									</footer><!-- .comment-meta -->

				<div class="comment-content">
					<p><strong>1feeding</strong></p>
				</div><!-- .comment-content -->

				<div class="reply"><a rel='nofollow' class='comment-reply-link' href='#comment-63016' data-commentid="63016" data-postid="233" data-belowelement="div-comment-63016" data-respondelement="respond" data-replyto="Reply to 3mutation" aria-label='Reply to 3mutation'>Reply</a></div>			</article><!-- .comment-body -->
		</li><!-- #comment-## -->
</ol></div>	<div id="respond" class="comment-respond">
		<h3 id="reply-title" class="comment-reply-title">Leave a Reply <small><a rel="nofollow" id="cancel-comment-reply-link" href="/2013/01/30/rich-coconut-buns/#respond" style="display:none;">Cancel reply</a></small></h3><form action="https://metemgee.com/wp-comments-post.php" method="post" id="commentform" class="comment-form" novalidate><p class="comment-notes"><span id="email-notes">Your email address will not be published.</span> <span class="required-field-message">Required fields are marked <span class="required">*</span></span></p><div class="comment-form-wprm-rating" style="display: none">
	<label for="wprm-comment-rating-1997597586">Recipe Rating</label>	<span class="wprm-rating-stars">
		<fieldset class="wprm-comment-ratings-container" data-original-rating="0" data-current-rating="0">
			<legend>Recipe Rating</legend>
			<input aria-label="Don&#039;t rate this recipe" name="wprm-comment-rating" value="0" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" style="margin-left: -18px !important; width: 18px !important; height: 18px !important;" checked="checked"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
    <polygon class="wprm-star-empty" id="wprm-star-empty-0" fill="none" stroke="#343434" stroke-width="2" stroke-linecap="square" stroke-miterlimit="10" points="12,2.6 15,9 21.4,9 16.7,13.9 18.6,21.4 12,17.6 5.4,21.4 7.3,13.9 2.6,9 9,9" stroke-linejoin="miter"/>
  </defs>
	<use xlink:href="#wprm-star-empty-0" x="0" y="0" />
	<use xlink:href="#wprm-star-empty-0" x="24" y="0" />
	<use xlink:href="#wprm-star-empty-0" x="48" y="0" />
	<use xlink:href="#wprm-star-empty-0" x="72" y="0" />
	<use xlink:href="#wprm-star-empty-0" x="96" y="0" />
</svg></span><br><input aria-label="Rate this recipe 1 out of 5 stars" name="wprm-comment-rating" value="1" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" style="width: 18px !important; height: 18px !important;"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
	<polygon class="wprm-star-empty" id="wprm-star-empty-1" fill="none" stroke="#343434" stroke-width="2" stroke-linecap="square" stroke-miterlimit="10" points="12,2.6 15,9 21.4,9 16.7,13.9 18.6,21.4 12,17.6 5.4,21.4 7.3,13.9 2.6,9 9,9" stroke-linejoin="miter"/>
	<path class="wprm-star-full" id="wprm-star-full-1" fill="#343434" d="M12.712,1.942l2.969,6.015l6.638,0.965c0.651,0.095,0.911,0.895,0.44,1.354l-4.804,4.682l1.134,6.612c0.111,0.649-0.57,1.143-1.152,0.837L12,19.286l-5.938,3.122C5.48,22.714,4.799,22.219,4.91,21.57l1.134-6.612l-4.804-4.682c-0.471-0.459-0.211-1.26,0.44-1.354l6.638-0.965l2.969-6.015C11.579,1.352,12.421,1.352,12.712,1.942z"/>
  </defs>
	<use xlink:href="#wprm-star-full-1" x="0" y="0" />
	<use xlink:href="#wprm-star-empty-1" x="24" y="0" />
	<use xlink:href="#wprm-star-empty-1" x="48" y="0" />
	<use xlink:href="#wprm-star-empty-1" x="72" y="0" />
	<use xlink:href="#wprm-star-empty-1" x="96" y="0" />
</svg></span><br><input aria-label="Rate this recipe 2 out of 5 stars" name="wprm-comment-rating" value="2" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" style="width: 18px !important; height: 18px !important;"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
	<polygon class="wprm-star-empty" id="wprm-star-empty-2" fill="none" stroke="#343434" stroke-width="2" stroke-linecap="square" stroke-miterlimit="10" points="12,2.6 15,9 21.4,9 16.7,13.9 18.6,21.4 12,17.6 5.4,21.4 7.3,13.9 2.6,9 9,9" stroke-linejoin="miter"/>
	<path class="wprm-star-full" id="wprm-star-full-2" fill="#343434" d="M12.712,1.942l2.969,6.015l6.638,0.965c0.651,0.095,0.911,0.895,0.44,1.354l-4.804,4.682l1.134,6.612c0.111,0.649-0.57,1.143-1.152,0.837L12,19.286l-5.938,3.122C5.48,22.714,4.799,22.219,4.91,21.57l1.134-6.612l-4.804-4.682c-0.471-0.459-0.211-1.26,0.44-1.354l6.638-0.965l2.969-6.015C11.579,1.352,12.421,1.352,12.712,1.942z"/>
  </defs>
	<use xlink:href="#wprm-star-full-2" x="0" y="0" />
	<use xlink:href="#wprm-star-full-2" x="24" y="0" />
	<use xlink:href="#wprm-star-empty-2" x="48" y="0" />
	<use xlink:href="#wprm-star-empty-2" x="72" y="0" />
	<use xlink:href="#wprm-star-empty-2" x="96" y="0" />
</svg></span><br><input aria-label="Rate this recipe 3 out of 5 stars" name="wprm-comment-rating" value="3" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" style="width: 18px !important; height: 18px !important;"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
	<polygon class="wprm-star-empty" id="wprm-star-empty-3" fill="none" stroke="#343434" stroke-width="2" stroke-linecap="square" stroke-miterlimit="10" points="12,2.6 15,9 21.4,9 16.7,13.9 18.6,21.4 12,17.6 5.4,21.4 7.3,13.9 2.6,9 9,9" stroke-linejoin="miter"/>
	<path class="wprm-star-full" id="wprm-star-full-3" fill="#343434" d="M12.712,1.942l2.969,6.015l6.638,0.965c0.651,0.095,0.911,0.895,0.44,1.354l-4.804,4.682l1.134,6.612c0.111,0.649-0.57,1.143-1.152,0.837L12,19.286l-5.938,3.122C5.48,22.714,4.799,22.219,4.91,21.57l1.134-6.612l-4.804-4.682c-0.471-0.459-0.211-1.26,0.44-1.354l6.638-0.965l2.969-6.015C11.579,1.352,12.421,1.352,12.712,1.942z"/>
  </defs>
	<use xlink:href="#wprm-star-full-3" x="0" y="0" />
	<use xlink:href="#wprm-star-full-3" x="24" y="0" />
	<use xlink:href="#wprm-star-full-3" x="48" y="0" />
	<use xlink:href="#wprm-star-empty-3" x="72" y="0" />
	<use xlink:href="#wprm-star-empty-3" x="96" y="0" />
</svg></span><br><input aria-label="Rate this recipe 4 out of 5 stars" name="wprm-comment-rating" value="4" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" style="width: 18px !important; height: 18px !important;"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
	<polygon class="wprm-star-empty" id="wprm-star-empty-4" fill="none" stroke="#343434" stroke-width="2" stroke-linecap="square" stroke-miterlimit="10" points="12,2.6 15,9 21.4,9 16.7,13.9 18.6,21.4 12,17.6 5.4,21.4 7.3,13.9 2.6,9 9,9" stroke-linejoin="miter"/>
	<path class="wprm-star-full" id="wprm-star-full-4" fill="#343434" d="M12.712,1.942l2.969,6.015l6.638,0.965c0.651,0.095,0.911,0.895,0.44,1.354l-4.804,4.682l1.134,6.612c0.111,0.649-0.57,1.143-1.152,0.837L12,19.286l-5.938,3.122C5.48,22.714,4.799,22.219,4.91,21.57l1.134-6.612l-4.804-4.682c-0.471-0.459-0.211-1.26,0.44-1.354l6.638-0.965l2.969-6.015C11.579,1.352,12.421,1.352,12.712,1.942z"/>
  </defs>
	<use xlink:href="#wprm-star-full-4" x="0" y="0" />
	<use xlink:href="#wprm-star-full-4" x="24" y="0" />
	<use xlink:href="#wprm-star-full-4" x="48" y="0" />
	<use xlink:href="#wprm-star-full-4" x="72" y="0" />
	<use xlink:href="#wprm-star-empty-4" x="96" y="0" />
</svg></span><br><input aria-label="Rate this recipe 5 out of 5 stars" name="wprm-comment-rating" value="5" type="radio" onclick="WPRecipeMaker.rating.onClick(this)" id="wprm-comment-rating-1997597586" style="width: 18px !important; height: 18px !important;"><span aria-hidden="true" style="width: 90px !important; height: 18px !important;"><svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" width="80px" height="16px" viewBox="0 0 120 24">
  <defs>
	<path class="wprm-star-full" id="wprm-star-full-5" fill="#343434" d="M12.712,1.942l2.969,6.015l6.638,0.965c0.651,0.095,0.911,0.895,0.44,1.354l-4.804,4.682l1.134,6.612c0.111,0.649-0.57,1.143-1.152,0.837L12,19.286l-5.938,3.122C5.48,22.714,4.799,22.219,4.91,21.57l1.134-6.612l-4.804-4.682c-0.471-0.459-0.211-1.26,0.44-1.354l6.638-0.965l2.969-6.015C11.579,1.352,12.421,1.352,12.712,1.942z"/>
  </defs>
	<use xlink:href="#wprm-star-full-5" x="0" y="0" />
	<use xlink:href="#wprm-star-full-5" x="24" y="0" />
	<use xlink:href="#wprm-star-full-5" x="48" y="0" />
	<use xlink:href="#wprm-star-full-5" x="72" y="0" />
	<use xlink:href="#wprm-star-full-5" x="96" y="0" />
</svg></span>		</fieldset>
	</span>
</div>
<p class="comment-form-comment"><label for="comment">Comment <span class="required">*</span></label> <textarea id="comment" name="comment" cols="45" rows="8" maxlength="65525" required></textarea></p><p class="comment-form-author"><label for="author">Name <span class="required">*</span></label> <input id="author" name="author" type="text" value="" size="30" maxlength="245" autocomplete="name" required /></p>
<p class="comment-form-email"><label for="email">Email <span class="required">*</span></label> <input id="email" name="email" type="email" value="" size="30" maxlength="100" aria-describedby="email-notes" autocomplete="email" required /></p>
		<div hidden class="wpsec_captcha_wrapper">
			<div class="wpsec_captcha_image"></div>
			<label for="wpsec_captcha_answer">
			Type in the text displayed above			</label>
			<input type="text" class="wpsec_captcha_answer" name="wpsec_captcha_answer" value=""/>
		</div>
		<p class="form-submit"><input name="submit" type="submit" id="submit" class="submit" value="Post Comment" /> <input type='hidden' name='comment_post_ID' value='233' id='comment_post_ID' />
<input type='hidden' name='comment_parent' id='comment_parent' value='0' />
</p><p style="display: none;"><input type="hidden" id="akismet_comment_nonce" name="akismet_comment_nonce" value="f344f7ffc5" /></p><p style="display: none !important;"><label>&#916;<textarea name="ak_hp_textarea" cols="45" rows="8" maxlength="100"></textarea></label><input type="hidden" id="ak_js_1" name="ak_js" value="86"/><script type="rocketlazyloadscript">document.getElementById( "ak_js_1" ).setAttribute( "value", ( new Date() ).getTime() );</script></p></form>	</div><!-- #respond -->
	</main><aside class="sidebar sidebar-primary widget-area" role="complementary" aria-label="Primary Sidebar" id="genesis-sidebar-primary"><h2 class="genesis-sidebar-title screen-reader-text">Primary Sidebar</h2><div class='feast-modern-sidebar'>
<div class="is-layout-flow wp-block-group feast-about-author"><div class="wp-block-group__inner-container">
<div class="wp-block-image is-style-rounded"><figure class="aligncenter size-large"><img src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%200%200'%3E%3C/svg%3E" alt="" class="wp-image-10017" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/08/althea-1024x1024.jpg"/><noscript><img src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2021/08/althea-1024x1024.jpg" alt="" class="wp-image-10017"/></noscript></figure></div>



<p><strong>Hi, I'm Althea!</strong> I have a real passion for cooking, especially traditional Caribbean recipes with deep roots! I was born and raised in Georgetown, Guyana and now live in Denver, Colorado with my husband and 3 kids. I am a Whole30 Certified Coach and love sharing wholesome remixes to traditional Guyanese and Caribbean dishes.</p>



<p class="has-text-align-center"><a href="/about">More about me →</a></p>
</div></div>



<h3 id="h-new-recipes">New Recipes</h3>


<div class='feast-category-index  feast-recipe-index'><ul class="feast-category-index-list fsri-list feast-grid-half feast-desktop-grid-half"><li class="listing-item"><a href="https://metemgee.com/2022/12/16/non-alcoholic-guyanese-black-cake/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/12/non-alcoholic-black-cake-e1671234164584-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Non-alcoholic Guyanese Black Cake</div></a></li><li class="listing-item"><a href="https://metemgee.com/2022/11/18/pumpkin-flan/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/11/Flan-Cover-Image-scaled-e1668809449955-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Pumpkin Flan</div></a></li><li class="listing-item"><a href="https://metemgee.com/2022/05/18/guyanese-cheese-straws/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/05/cheese-straw-main-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Guyanese Cheese Straws</div></a></li><li class="listing-item"><a href="https://metemgee.com/2022/03/22/creamy-farine-cassava-grits/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2022/03/Shrimp-and-Farine-Grits-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Creamy Farine (Cassava) Grits</div></a></li></ul></div>


<h3 id="h-wholesome-faves">Wholesome Faves</h3>


<div class='feast-category-index  feast-recipe-index'><ul class="feast-category-index-list fsri-list feast-grid-half feast-desktop-grid-half"><li class="listing-item"><a href="https://metemgee.com/2020/07/12/boneless-brown-stew-chicken/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/07/IMG_9245-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Boneless Brown Stew Chicken</div></a></li><li class="listing-item"><a href="https://metemgee.com/2020/01/31/instant-pot-dhal/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/01/IP-Dhal-featured-image-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Instant Pot Dhal {Whole30}</div></a></li><li class="listing-item"><a href="https://metemgee.com/2020/05/13/gluten-free-grain-free-roti/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2020/05/IMG_6071-scaled-scaled-e1650592754540-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Gluten Free / Grain Free Roti</div></a></li><li class="listing-item"><a href="https://metemgee.com/2013/03/27/happy-holi-with-parsad/" style="text-decoration: none;"><img width="360" height="480" src="data:image/svg+xml,%3Csvg%20xmlns='http://www.w3.org/2000/svg'%20viewBox='0%200%20360%20480'%3E%3C/svg%3E" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" data-lazy-srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-180x240.jpg 180w" data-lazy-sizes="(max-width: 360px) 100vw, 360px" data-lazy-src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-360x480.jpg" /><noscript><img width="360" height="480" src="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-360x480.jpg" class=" wp-post-image" alt="" decoding="async" data-pin-nopin="true" aria-hidden="true" loading="lazy" srcset="https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-360x480.jpg 360w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-720x960.jpg 720w, https://rnn53d.p3cdn1.secureserver.net/wp-content/uploads/2013/03/Parsad_traditional_featured-image-1-180x240.jpg 180w" sizes="(max-width: 360px) 100vw, 360px" /></noscript><div class='fsri-title'>Guyanese Parsad</div></a></li></ul></div>









</div></aside></div></div><footer class="site-footer"><div class="wrap"><h2 class='screen-reader-text'>Footer</h2>
<div class='feast-modern-footer'>
<p class="has-text-align-center feast-button has-black-color has-text-color"><a href="#">↑ back to top</a></p>



<div class="is-layout-flex wp-container-7 wp-block-columns has-white-color has-text-color has-background" style="background-color:#127c84">
<div class="is-layout-flow wp-block-column has-white-color has-text-color has-background" style="background-color:#127c84">
<h3 class="has-white-color has-text-color" id="h-about">About</h3>



<ul class="has-white-color has-text-color"><li><a href="/about">Meet Althea</a></li><li><a href="/privacy-policy">Privacy Policy</a></li><li><a href="/recipes">Recipes</a></li></ul>
</div>



<div class="is-layout-flow wp-block-column has-white-color has-text-color has-background" style="background-color:#127c84">
<h3 class="has-white-color has-text-color" id="h-newsletter">Newsletter</h3>



<ul class="has-text-color" style="color:#252c32"><li><a href="https://metemgee.com/subscribe/">Sign up to stay connected!</a></li></ul>



<p></p>
</div>



<div class="is-layout-flow wp-block-column has-white-color has-text-color has-background" style="background-color:#127c84">
<h3 class="has-white-color has-text-color" id="h-contact">Contact</h3>



<ul class="has-white-color has-text-color"><li><a href="https://metemgee.com/work-with-me/">Get In Touch</a></li></ul>



<p></p>
</div>
</div>



<p class="has-text-align-center">Copyright © 2022 Metemgee, LLC</p>
</div></div></footer></div><style type="text/css" media="screen">#simple-social-icons-9 ul li a, #simple-social-icons-9 ul li a:hover, #simple-social-icons-9 ul li a:focus { background-color: #ffffff !important; border-radius: 30px; color: #000000 !important; border: 0px #ffffff solid !important; font-size: 15px; padding: 8px; }  #simple-social-icons-9 ul li a:hover, #simple-social-icons-9 ul li a:focus { background-color: #12adbb !important; border-color: #ffffff !important; color: #ffffff !important; }  #simple-social-icons-9 ul li a:focus { outline: 1px dotted #12adbb !important; } #simple-social-icons-8 ul li a, #simple-social-icons-8 ul li a:hover, #simple-social-icons-8 ul li a:focus { background-color: #ffffff !important; border-radius: 30px; color: #000000 !important; border: 0px #ffffff solid !important; font-size: 15px; padding: 8px; }  #simple-social-icons-8 ul li a:hover, #simple-social-icons-8 ul li a:focus { background-color: #12adbb !important; border-color: #ffffff !important; color: #000000 !important; }  #simple-social-icons-8 ul li a:focus { outline: 1px dotted #12adbb !important; } #simple-social-icons-8 ul li a, #simple-social-icons-8 ul li a:hover, #simple-social-icons-8 ul li a:focus { background-color: #ffffff !important; border-radius: 30px; color: #000000 !important; border: 0px #ffffff solid !important; font-size: 15px; padding: 8px; }  #simple-social-icons-8 ul li a:hover, #simple-social-icons-8 ul li a:focus { background-color: #12adbb !important; border-color: #ffffff !important; color: #000000 !important; }  #simple-social-icons-8 ul li a:focus { outline: 1px dotted #12adbb !important; }</style><style id='core-block-supports-inline-css' type='text/css'>
.wp-block-columns.wp-container-7{flex-wrap:nowrap;}
</style>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-includes/js/comment-reply.min.js?ver=6.1.1&#038;time=1673945671' id='comment-reply-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-includes/js/hoverIntent.min.js?ver=1.10.2&#038;time=1673945671' id='hoverIntent-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-content/themes/genesis/lib/js/menu/superfish.min.js?ver=1.7.10&#038;time=1673945671' id='superfish-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-content/themes/genesis/lib/js/menu/superfish.args.min.js?ver=3.4.0&#038;time=1673945671' id='superfish-args-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-content/themes/genesis/lib/js/skip-links.min.js?ver=3.4.0&#038;time=1673945671' id='skip-links-js' defer></script>
<script type="rocketlazyloadscript" data-rocket-type='text/javascript' src='https://captcha.wpsecurity.godaddy.com/api/v1/captcha/script?trigger=comment' id='wpsec_show_captcha-js' defer></script>
<script type="rocketlazyloadscript" defer data-rocket-type='text/javascript' src='https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/akismet/_inc/akismet-frontend.js?ver=1669924056&#038;time=1673945671' id='akismet-frontend-js'></script>
		<script type="rocketlazyloadscript">'undefined'=== typeof _trfq || (window._trfq = []);'undefined'=== typeof _trfd && (window._trfd=[]),_trfd.push({'tccl.baseHost':'secureserver.net'}),_trfd.push({'ap':'wpaas'},{'server':'7dac603b-1992-06ad-053c-bcaa61a7d8de.secureserver.net'},{'pod':'P3NLWPPOD10'},{'storage':'p3cephmah004pod10_data17'},{'xid':'43466594'},{'wp':'6.1.1'},{'php':'7.4.33'},{'loggedin':'0'},{'cdn':'1'},{'builder':'wp-block-editor'},{'theme':'genesis'},{'wds':'0'},{'wp_alloptions_count':'1811'},{'wp_alloptions_bytes':'445867'})</script>
		<script type="rocketlazyloadscript">window.addEventListener('click', function (elem) { var _elem$target, _elem$target$dataset, _window, _window$_trfq; return (elem === null || elem === void 0 ? void 0 : (_elem$target = elem.target) === null || _elem$target === void 0 ? void 0 : (_elem$target$dataset = _elem$target.dataset) === null || _elem$target$dataset === void 0 ? void 0 : _elem$target$dataset.eid) && ((_window = window) === null || _window === void 0 ? void 0 : (_window$_trfq = _window._trfq) === null || _window$_trfq === void 0 ? void 0 : _window$_trfq.push(["cmdLogEvent", "click", elem.target.dataset.eid]));});</script>
		<script type="rocketlazyloadscript" src='https://img1.wsimg.com/tcc/tcc_l.combined.1.0.6.min.js' defer></script>
		<script type="rocketlazyloadscript" src='https://img1.wsimg.com/traffic-assets/js/tccl-tti.min.js' onload="window.tti.calculateTTI()" defer></script>
		<script>window.lazyLoadOptions=[{elements_selector:"img[data-lazy-src],.rocket-lazyload",data_src:"lazy-src",data_srcset:"lazy-srcset",data_sizes:"lazy-sizes",class_loading:"lazyloading",class_loaded:"lazyloaded",threshold:300,callback_loaded:function(element){if(element.tagName==="IFRAME"&&element.dataset.rocketLazyload=="fitvidscompatible"){if(element.classList.contains("lazyloaded")){if(typeof window.jQuery!="undefined"){if(jQuery.fn.fitVids){jQuery(element).parent().fitVids()}}}}}},{elements_selector:".rocket-lazyload",data_src:"lazy-src",data_srcset:"lazy-srcset",data_sizes:"lazy-sizes",class_loading:"lazyloading",class_loaded:"lazyloaded",threshold:300,}];window.addEventListener('LazyLoad::Initialized',function(e){var lazyLoadInstance=e.detail.instance;if(window.MutationObserver){var observer=new MutationObserver(function(mutations){var image_count=0;var iframe_count=0;var rocketlazy_count=0;mutations.forEach(function(mutation){for(var i=0;i<mutation.addedNodes.length;i++){if(typeof mutation.addedNodes[i].getElementsByTagName!=='function'){continue}
if(typeof mutation.addedNodes[i].getElementsByClassName!=='function'){continue}
images=mutation.addedNodes[i].getElementsByTagName('img');is_image=mutation.addedNodes[i].tagName=="IMG";iframes=mutation.addedNodes[i].getElementsByTagName('iframe');is_iframe=mutation.addedNodes[i].tagName=="IFRAME";rocket_lazy=mutation.addedNodes[i].getElementsByClassName('rocket-lazyload');image_count+=images.length;iframe_count+=iframes.length;rocketlazy_count+=rocket_lazy.length;if(is_image){image_count+=1}
if(is_iframe){iframe_count+=1}}});if(image_count>0||iframe_count>0||rocketlazy_count>0){lazyLoadInstance.update()}});var b=document.getElementsByTagName("body")[0];var config={childList:!0,subtree:!0};observer.observe(b,config)}},!1)</script><script data-no-minify="1" async src="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/wp-rocket/assets/js/lazyload/17.5/lazyload.min.js"></script><script>"use strict";function wprRemoveCPCSS(){var preload_stylesheets=document.querySelectorAll('link[data-rocket-async="style"][rel="preload"]');if(preload_stylesheets&&0<preload_stylesheets.length)for(var stylesheet_index=0;stylesheet_index<preload_stylesheets.length;stylesheet_index++){var media=preload_stylesheets[stylesheet_index].getAttribute("media")||"all";if(window.matchMedia(media).matches)return void setTimeout(wprRemoveCPCSS,200)}var elem=document.getElementById("rocket-critical-css");elem&&"remove"in elem&&elem.remove()}window.addEventListener?window.addEventListener("load",wprRemoveCPCSS):window.attachEvent&&window.attachEvent("onload",wprRemoveCPCSS);</script><noscript><link rel='stylesheet' id='seasoned-pro-theme-css' href='https://rnn53d.p3cdn1.secureserver.net/wp-content/themes/seasonedpro-v443/style.css?ver=4.4.3&#038;time=1673945671' type='text/css' media='all' /><link rel='stylesheet' id='wp-block-library-css' href='https://rnn53d.p3cdn1.secureserver.net/wp-includes/css/dist/block-library/style.min.css?ver=6.1.1&#038;time=1673945671' type='text/css' media='all' /><link rel='stylesheet' id='classic-theme-styles-css' href='https://rnn53d.p3cdn1.secureserver.net/wp-includes/css/classic-themes.min.css?ver=1&#038;time=1673945671' type='text/css' media='all' /><link rel='stylesheet' id='simple-social-icons-font-css' href='https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/simple-social-icons/css/style.css?ver=3.0.2&#038;time=1673945671' type='text/css' media='all' /><link rel="stylesheet" href="https://rnn53d.p3cdn1.secureserver.net/wp-content/plugins/wordpress-23-related-posts-plugin/static/themes/vertical.css?version=3.6.4" /></noscript></body></html>

<!-- This website is like a Rocket, isn't it? Performance optimized by WP Rocket. Learn more: https://wp-rocket.me -->
