# Awesome Web Components [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> This is a curated list of Web Components design systems, libraries and resources.

- Web Components are the **native component model** on the web platform.
- Web Components **exposes capabilities** previously reserved for native code
- Web Components are **low level** DOM APIs

```js
import sheet from './styles.css';

class MyElement extends HTMLElement {
  constructor() {
    super();
    this.attachShadow({ mode: 'open' });
    this.shadowRoot.adoptedStyleSheets = [sheet];
  }
  connectedCallback() {}
  disconnectedCallback() {}
  attributeChangedCallback() {}
  adoptedCallback() {}
  static get observedAttributes() {
    return ['foo'];
  }
}
```

## Contents

- [Latest Articles](#articles)
- [Libraries](#libraries)
- [Component Libraries](#component-libraries)
- [Sites build entirely with Web Components](sites-build-entirely-with-web-components)
- [Specification Drafts, Reviews & Explainers](specification-drafts-reviews--explainers)


## Latest Articles

- [2023-04-17 — 2023 State of Web Components](https://eisenbergeffect.medium.com/2023-state-of-web-components-c8feb21d4f16)
- [2023-03-27 — Debunking Web Component Myths and Misconceptions](https://eisenbergeffect.medium.com/debunking-web-component-myths-and-misconceptions-ea9bb13daf61) — by Rob Eisenberg from the FAST team
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

## Specifications (W3C Web Components Community Group)

Web components are a collection of [web standards](https://github.com/WICG/webcomponents) that enable an HTML native component model.
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

- [Declarative Shadow DOM (DSD)](https://github.com/dwhatwg/html/pull/5465)
  - [Chrome 90 (`shadowroot` — non-standard)](https://developer.chrome.com/blog/new-in-chrome-90/#declarative)
  - [Chrome 111 (`shadowrootmode` — standardized)](https://developer.chrome.com/en/articles/declarative-shadow-dom/)
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
- [Lion by ING](https://github.com/ing-bank/lion)
- [Lithium UI](https://github.com/coryrylan/lithium)
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
- [Reddit](https://twitter.com/43081j/status/1634860644372561921) (`<shreddit-mod-comment>`)
- [TikTok](https://twitter.com/justinfagnani/status/1633831934643273730) (`<cookie-settings-modal>`)
- [Figma](https://twitter.com/ChrisDHolt/status/1584982495887781890?s=20)
- [SpaceX](https://www.reddit.com/r/spacex/comments/gxb7j1/comment/ft6bydt/)
- [Adobe Firefly](https://twitter.com/justinfagnani/status/1661082772419772416?s=20)
- [Firefox](https://github.com/mozilla/gecko-dev/blob/master/toolkit/content/widgets/lit-utils.mjs)

## Frameworks & Routers

- [CrossBow](https://crossbow-wc-2ayn6.ondigitalocean.app/)
> The goal of Crossbow is to be the _Next.js_ for web-components.

- [Rocket](https://rocket.modern-web.dev/)
> A modern web [setup](https://twitter.com/techytacos/status/1408507828063535109) for static sites with a sprinkle of JavaScript.

- [Enhance](https://enhance.dev/)
- [Appolo Elements](https://apolloelements.dev/)
- [FAST Router](https://github.com/microsoft/fast/tree/master/packages/web-components/fast-router)

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

## Widgets

- [Google Map Widget](https://cloud.google.com/blog/products/maps-platform/build-maps-faster-web-components)

## Resources

- [📈 Custom Element Popularity (`CustomElementRegistryDefine` stats)](https://chromestatus.com/metrics/feature/timeline/popularity/1689)
- [Are Web Components A Thing Yet](https://arewebcomponentsathingyet.com/)
- [Web Components Community](https://community.webcomponents.dev/)
- [Web Components and lists](https://twitter.com/techytacos/status/1407068338644144155)
- [Awesome Lit](https://github.com/web-padawan/awesome-lit)
- [Awesome Standalones](https://github.com/davatron5000/awesome-standalones)
- [Starter Templates](https://webcomponents.today/starter-templates/)
