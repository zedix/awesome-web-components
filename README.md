# Awesome Web Components [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> This is a curated list of Web Components articles, design systems, libraries and resources.

## Latest Articles

- [2023-07-20 — Hacker News Lit: Simple, fast web components ](https://news.ycombinator.com/item?id=36806747)
- [2023-07-19 — Dynamic Slots](https://www.abeautifulsite.net/posts/dynamic-slots/)
- [2023-06-28 — If Web Components are so great, why am I not using them?](https://daverupert.com/2023/07/why-not-webcomponents/)
- [2023-04-17 — 2023 State of Web Components](https://eisenbergeffect.medium.com/2023-state-of-web-components-c8feb21d4f16)
- [2023-03-27 — Debunking Web Component Myths and Misconceptions](https://eisenbergeffect.medium.com/debunking-web-component-myths-and-misconceptions-ea9bb13daf61) ⭐ — by Rob Eisenberg from the FAST team
- [2023-03-09 — Faster dashboards with web components](https://blog.datawrapper.de/dashboard-performance-web-components/)
- [2023-02-13 — Hello Web Components](https://eisenbergeffect.medium.com/hello-web-components-795ed1bd108e)
- [2022-02-17 — All the Ways to Make a Web Component](https://webcomponents.dev/blog/all-the-ways-to-make-a-web-component/)
- [2021-05-26 — Links on Web Components](https://css-tricks.com/links-on-web-components/)
- [2021-05-15 — Container Queries in Web Components](https://mxb.dev/blog/container-queries-web-components/)
- [2020-03-27 — The bright future of Web Components](https://maxart2501.github.io/web-components-talk/codemotion-rm20/#63)
- [2019-11-07 — The Firefox UI is now built with Web Components](https://briangrinstead.com/blog/firefox-webcomponents/)
- [2019-04-08 — A history of the HTML slot element](https://component.kitchen/blog/posts/a-history-of-the-html-slot-element)
- [2018-09-06 — GitHub is using custom elements for their modal dialogs, autocomplete and display time.](https://githubengineering.com/removing-jquery-from-github-frontend/#custom-elements)
- [2017-03-14 — Brief, incomplete, and mostly incorrect history of Web Components](https://dmitriid.com/blog/2017/03/the-broken-promise-of-web-components/#brief-incomplete-and-mostly-incorrect-history-of-web-components)

## Example

```js
import sheet from './base.css' assert { type: 'css' };

class MyButton extends HTMLElement
{
  static observedAttributes = ['my-attr'];// tell the platform about reactive attributes
  #internals;
  #shadowRoot;

  constructor() {
    super();
    // custom construction logic such as creating your shadow DOM
    this.attachShadow({ mode: 'open'});
    this.#shadowRoot.adoptedStyleSheets = [sheet];
    // specify the default ARIA role
    this.#internals = this.attachInternals();
    this.#internals.ariaRole = 'button';
  }

  connectedCallback() {
    // this lifecycle hook is called by the platform when your
    // element is connected to the DOM
  }

  disconnectedCallback() {
    // this lifecycle hook is called by the platform when your
    // element is disconnected from the DOM
  }

  attributeChangedCallback(name, oldValue, newValue) {
    // this lifecycle hook is called whenever one of your
    // observed attributes changes in value
  }
}

customElements.define('my-element', MyButton);
```

- Web Components are the **native component model** on the web platform.
- Web Components **exposes capabilities** previously reserved for native code
- Web Components are **low level** DOM APIs

## Performance

From [About Web Components](https://eisenbergeffect.medium.com/about-web-components-7b2a3ed67a78) by Rob Eisenberg

Web Components have clear performance benefits. There are several reasons for this:

- The core capabilities of Web Components are implemented in C++/Rust as part of each browser’s native HTML parser and runtime. JavaScript frameworks simply can’t match the speed and memory efficiency of C++.

- Because the component model is implemented by the browser, less JavaScript needs to be downloaded, parsed, and executed before a component is able to render.

- With JavaScript frameworks, the browser doesn’t “see” the components and thus can’t optimize for them. It just looks like one gigantic DOM tree to the runtime. With Web Components, the browser knows about every component and its boundaries, and can perform various internal optimizations to improve performance. This is particularly important in applications with large amounts of CSS where the absence of Web Component Shadow DOM makes it impossible to fix certain rendering performance problems. Non-web component libraries literally block the browser from optimizations it could otherwise perform.

- The Web Component model favors modern reactivity patterns and surgical DOM updates that massively outperform the Virtual DOM approaches of libraries like React. You can see this in the way that observedAttributes and the attributeChangedCallback work.

## Specifications

Web components are a [collection](https://w3c.github.io/webcomponents-cg/2022.html) of [web standards](https://github.com/WICG/webcomponents) (W3C Web Components Community Group) that enable an HTML native component model.
They are a meta-specification made possible by the above [specifications](https://techxplore.com/news/2019-06-w3c-whatwg-agreement-version-html.html):

- Shadow DOM
  - [DOM Standard › Shadow DOM](https://dom.spec.whatwg.org/#shadow-trees)

- Custom Elements
  - [HTML Standard › Custom Elements](https://html.spec.whatwg.org/multipage/scripting.html#custom-elements)
  - [Form Associated Custom Elements (Fully Supported)](https://developer.mozilla.org/en-US/docs/Web/API/ElementInternals/form)

- HTML Templates
  - [HTML Standard › HTML Templates](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element)

- CSS changes
  - [CSS Scoping](https://drafts.csswg.org/css-scoping/)
  - [CSS Shadow Parts](https://drafts.csswg.org/css-shadow-parts/)

- [JSON](https://www.chromestatus.com/feature/5749863620804608), [CSS](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/css-modules-v1-explainer.md), [HTML](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/html-modules-explainer.md) Modules


## Drafts, Reviews & Explainers

- [Declarative Shadow DOM (DSD)](https://github.com/whatwg/html/pull/5465)
  - [Server-Side Rendering (SSR) API](https://github.com/webcomponents-cg/community-protocols/issues/7)
  - [Can I use `shadowrootmode`?](https://caniuse.com/mdn-html_elements_template_shadowrootmode)
  - [Chrome 90 (`shadowroot` — non-standard)](https://developer.chrome.com/blog/new-in-chrome-90/#declarative)
  - [Chrome 111 (`shadowrootmode` — standardized)](https://developer.chrome.com/en/articles/declarative-shadow-dom/)
  - [Bugzilla #1712140](https://bugzilla.mozilla.org/show_bug.cgi?id=1712140)
  - [Safari Technology Preview 162](https://webkit.org/blog/13851/declarative-shadow-dom/)
    - [Streaming DSD: Chromium Intent to Ship](https://groups.google.com/a/chromium.org/g/blink-dev/c/xzT-vN-bx0s/m/qWrGNWwQAAAJ?pli=1)
    - [Streaming DSD: Playground](https://lit.dev/playground/#gist=d2540b636f7d9d420c2dd8ddd8436c81)

> A declarative API to allow the creation of #shadowroots using only HTML and no Javascript. This API allows Web Components that use Shadow DOM to also make use of Server-Side Rendering (SSR), to get rendered content onscreen quickly without requiring Javascript for shadow root attachment and population.

- [Form-associated custom elements (attachInternals)](https://github.com/whatwg/html/pull/4383)
  - [HTML Living Standard](https://html.spec.whatwg.org/multipage/custom-elements.html#custom-elements-face-example)
  - [Chrome 77](https://www.chromestatus.com/features/4708990554472448)
  - [FF 98](https://bugzilla.mozilla.org/show_bug.cgi?id=1745378)
  - [Safari Technology Preview 162](https://webkit.org/blog/13851/declarative-shadow-dom/)
  - [Creating Custom Form Controls with ElementInternals ](https://css-tricks.com/creating-custom-form-controls-with-elementinternals/)


- [Shadow DOM Delegate Focus](https://blog.whatwg.org/focusing-on-focus)
> When the shadow root of an element has delegates focus flag set, focusing on the shadow host would automatically “delegates” focus to the first focusable element in the shadow tree instead.

- [CSSOM Constructable Stylesheet Objects](https://wicg.github.io/construct-stylesheets/)
- [CSS Custom States (Chromium)](https://developer.mozilla.org/en-US/docs/Web/API/CustomStateSet)
- [CSS Theming (Proposal)](https://w3c.github.io/webcomponents-cg/2022.html#theming)

- [my-element:--my-state custom state pseudo class](https://wicg.github.io/custom-state-pseudo-class/)
  - [Chrome 90](https://www.chromestatus.com/feature/6537562418053120)
  - [This feature is not (yet) a standard](https://css-tricks.com/custom-state-pseudo-classes-in-chrome/#this-feature-is-not-yet-a-standard)

- [Children Changed Callback (Proposal)](https://w3c.github.io/webcomponents-cg/2022.html#children-changed-callback)
- [Custom Attributes (Identified)](https://eisenbergeffect.medium.com/2023-state-of-web-components-c8feb21d4f16)
- [Composed Selection (Consensus/No Spec)](https://w3c.github.io/webcomponents-cg/2022.html#initial-api-summary-quick-api-proposal-0)
- [Declarative Custom Element (Proposal)](https://w3c.github.io/webcomponents-cg/2022.html#declarative-custom-elements)

- Rendering & Performance
  - [Declarative Shadow DOM (Mostly Supported)](https://developer.chrome.com/articles/declarative-shadow-dom/)

- Template Instantiation
  - [DOM Parts (Proposal)](https://w3c.github.io/webcomponents-cg/2022.html#initial-api-summary-quick-api-proposal-10)

- Package & Distribution
  - [Lazy Custom Element Definitions (Proposal)](https://w3c.github.io/webcomponents-cg/2022.html#lazy-custom-element-definitions)

```js
customElements.defineLazy('my-element',  async () => (await import('my-element.js')).default);
```

## Libraries

Some [tools/libraries](https://webcomponents.dev/blog/all-the-ways-to-make-a-web-component/board/) that simplify <code>Custom Elements</code> definition and content:

- [Lit](https://lit.dev/)
  - [Community protocols](https://github.com/webcomponents/community-protocols)
- [Fast](https://github.com/microsoft/fast)
- [SkateJS](https://github.com/skatejs/skatejs)
- [Stencil](https://stenciljs.com/) (23/08/2017) A web component compiler (powering Ionic 4)
- [Atomico](https://github.com/atomicojs/atomico)
- [Hybrids](https://hybrids.js.org/)
- [µce+µhtml](https://github.com/WebReflection/uce)
  ⇢ [µce vs lit-element](https://gist.github.com/WebReflection/ae3451c17c5e882bbc7f0714c14eefcd)
  ⇢ [µce does @vue/lit things](https://codepen.io/WebReflection/pen/LYNJwoV?editors=0010)

- [µce-template+µce-loader]
> uce-template is a 100% Custom Elements based library, which goal is to help defining portable components once, but usable everywhere, directly in the HTML. Combined with µce-loader, it is possible to stream definitions, as these are found in the page, making uce-template an ideal static/server page companion for graceful, client-side, enhancement.

## Component Libraries

- [GitHub Elements](https://github.com/github/github-elements)
- [Google Material](https://github.com/material-components/material-components-web-components)
- [Helix UI](https://helixdesignsystem.github.io/helix-ui/)
- [Microsoft Fast](https://fast.design/)
- [Microsoft Graph](https://github.com/microsoftgraph/microsoft-graph-toolkit)
  ⇢ [StoryBook](https://mgt.dev/)
- [PatternFly Design System](https://github.com/patternfly/patternfly-elements)
- [Porsche Design System](https://designsystem.porsche.com/latest/#/start-coding/vanilla-js)
- [SAP UI5](https://github.com/SAP/ui5-webcomponents)

### Built with [Lit-element](https://github.com/Polymer/lit-element)

![lit-element](https://img.shields.io/badge/lib-lit--element-blue.svg?maxAge=60)

- [Astro Space UX Design System](https://www.astrouxds.com/)
- [Auro Design System by Alaska Airlines](https://auro.alaskaair.com/)
- [AXA Pattern Library](https://github.com/axa-ch/patterns-library)
  ⇢ [StoryBook](https://patterns.axa.ch/?path=/story/welcome--to-pattern-library)
- [Blackstone UI](https://github.com/kjantzer/bui)
- [Chameleon Design System](https://github.com/MaritzSTL/chameleon)
  ⇢ [StoryBook](https://chameleon-design-system.netlify.app/?path=/story/*)
- [Clever UI](https://github.com/CleverCloud/clever-components)
  ⇢ [StoryBook](https://www.clever-cloud.com/doc/clever-components/)
- [Carbon by IBM](https://github.com/carbon-design-system/carbon-custom-elements)
  ⇢ [StoryBook](https://web-components.carbondesignsystem.com/)
- [Kor UI Design System](https://kor-ui.com/)
- [LrnWebComponents](https://github.com/elmsln/lrnwebcomponents)
- [Lion by ING](https://github.com/ing-bank/lion) + [Lion Components](https://lion-web.netlify.app/)
- [Nordhealth Design System](https://nordhealth.design/)
- [Shoelace](https://github.com/shoelace-style/shoelace) ❤︎
- [Vaadin](https://github.com/vaadin/web-components) ❤︎
  ⇢ [Documentation](https://vaadin.com/docs/latest/ds/overview)
- [Spectrum by Adobe](https://github.com/adobe/spectrum-web-components)
- [ClarityCore by VMware](https://clarity.design/storybook/core/)
- [Weightless](https://weightless.dev/)
- [Zedix UI](https://github.com/zedix/zedix-ui)

### Built with [Stencil](https://github.com/ionic-team/stencil)

![lit-stencil](https://img.shields.io/badge/lib-lit--stencil-blue.svg?maxAge=60)

- [Duet Design System by LocalTapiola](https://www.duetds.com/)
- [Scale Design System By Telekom](https://github.com/telekom/scale)
- [Elix](https://component.kitchen/elix)

## Design Systems build entirely with Web Components

- [ING Lion](https://lion-web.netlify.app/)
- [Adobe Spectrum](https://spectrum.adobe.com/)
- [Red Hat Design System](https://ux.redhat.com/)

## Sites build entirely with Web Components

- [MSN](https://www.msn.com/fr-fr)
> A couple of years back, Microsoft re-built the MSN experience with the [Fluent UI Web Components based on FAST](https://learn.microsoft.com/en-us/fluent-ui/web-components/). This improved performance by 30%–50% over the previous React version Approximately 1,500 teams and/or projects within Microsoft have adopted FAST Web Components in the last three years (from 2022).

- [Bing](https://www.bing.com/)
- [YouTube](https://www.youtube.com/) (`<ytd-video-preview>`)
- [Photoshop for Web](https://web.dev/ps-on-the-web/)
- [Fast](https://www.fast.design/)
- [Ideanote](https://start.ideanote.io/)
- [Simplr](https://simplr.company/)
- [ViteMaDose](https://vitemadose.covidtracker.fr/)

## Sites using Lit elements

- [ChromeDevTools](https://twitter.com/steren/status/1633359619874754561?s=20) (`<devtools-button>`)
- [VSCode](https://github.com/microsoft/vscode-webview-ui-toolkit)
- [Reddit](https://twitter.com/addyosmani/status/1677776509837402112?s=20) ([shreddit-mod-comment](https://sh.reddit.com/)) Lit
- [TikTok](https://twitter.com/justinfagnani/status/1633831934643273730) (`<cookie-settings-modal>`)
- [Figma](https://twitter.com/ChrisDHolt/status/1584982495887781890?s=20)
- [SpaceX](https://www.reddit.com/r/spacex/comments/gxb7j1/comment/ft6bydt/)
- [Shopify](https://shopify.engineering/shopifys-platform-is-the-web-platform) (`<ui-nav-menu>`)
- [Adobe Firefly](https://twitter.com/justinfagnani/status/1661082772419772416?s=20)
- [Firefox](https://github.com/mozilla/gecko-dev/blob/master/toolkit/content/widgets/lit-utils.mjs)
- [Google Maps API](https://developers.google.com/maps/documentation/javascript/web-components/overview?hl=fr) (`<gmp-map>`)

## Frameworks & Routers

- [Enhance](https://enhance.dev/) by [Brian Leroux](https://begin.com/blog/posts/2023-02-23-enhancing-fwas-with-web-components) + [Enhance Movies Showcase (3.9 kb JS compressed)](https://begin.com/blog/posts/2023-07-26-introducing-enhance-movie)
> Enhance provides file-based routing, reusable Custom Elements, a customizable utility CSS system, and mapped API data routes that get deployed to isolated, single-purpose cloud functions, no build steps to configure.

- [Rocket](https://rocket.modern-web.dev/)
> A modern web [setup](https://twitter.com/techytacos/status/1408507828063535109) for static sites with a sprinkle of JavaScript.

- [Eleventy with WebC](https://www.11ty.dev/docs/languages/webc/)

- [Appolo Elements](https://apolloelements.dev/)
- [FAST Router](https://github.com/microsoft/fast/tree/master/packages/web-components/fast-router)
- [CrossBow](https://crossbow-wc-2ayn6.ondigitalocean.app/)
> The goal of Crossbow is to be the _Next.js_ for web-components.

## Stats

- [Percentage of page loads that use custom element: over 18%](https://www.chromestatus.com/metrics/feature/timeline/popularity/1689)

## Companies using Web Components

Major technology organizations investing in the future of web components:

- Adobe
- Amazon
- Apple
- Blizzard
- BYU
- Caniuse
- Comcast
- CSS Tricks
- EA
- ESRI
- Ford
- GE
- Github
- GM
- Google
- IBM
- Infragistics
- ING
- Internet Archive
- Ionic
- MSFT
- NASA
- Netlify
- Nintendo
- Penn State
- RedHat
- Salesforce
- SAP
- SpaceX
- Ubisoft
- VMware
- …

## Accessibility

- [How Shadow DOM and accessibility are in conflict](https://alice.pages.igalia.com/blog/how-shadow-dom-and-accessibility-are-in-conflict/)

## Widgets / Standalone elements

- [Rhino Editor](https://github.com/konnorrogers/rhino-editor)
- [Swiper Element](https://swiperjs.com/element)
- [Mux Uploader](https://docs.mux.com/guides/video/mux-uploader)
- [Google Map Widget](https://cloud.google.com/blog/products/maps-platform/build-maps-faster-web-components)

## Resources

- [📈 Custom Element Popularity (`CustomElementRegistryDefine` stats)](https://chromestatus.com/metrics/feature/timeline/popularity/1689)
- [Are Web Components A Thing Yet](https://arewebcomponentsathingyet.com/)
- [Web Components Community](https://community.webcomponents.dev/)
- [Web Components and lists](https://twitter.com/techytacos/status/1407068338644144155)
- [Awesome Lit](https://github.com/web-padawan/awesome-lit)
- [Awesome Standalones](https://github.com/davatron5000/awesome-standalones)
- [Starter Templates](https://webcomponents.today/starter-templates/)
- [Stubbornella on WC/Wasm](https://news.ycombinator.com/item?id=34632657)
