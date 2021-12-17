# Awesome Web Components [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> This is a curated list of Web Components design systems, libraries and resources.

- Web Components are the **native component model** on the web platform.
- Web Components **exposes capabilities** previously reserved for native code
- Web Components are **low level** DOM APIs

## Contents

- [Libraries](#libraries)
- [Component Libraries](#component-libraries)
- [Sites build entirely with Web Components](sites-build-entirely-with-web-components)
- [Specification Drafts, Reviews & Explainers](specification-drafts-reviews--explainers)
- [Articles](#articles)

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

- [Fast](https://www.fast.design/)
- [Ideanote](https://start.ideanote.io/)
- [DeckDeckGo](https://app.deckdeckgo.com/)
- [Simplr](https://simplr.company/)
- [ViteMaDose](https://vitemadose.covidtracker.fr/)

## [Specifications](https://github.com/WICG/webcomponents)

Web components are a collection of web standards that enable an HTML native component model.
They are a meta-specification made possible by the above [specifications](https://techxplore.com/news/2019-06-w3c-whatwg-agreement-version-html.html):

- Shadow DOM
  - [DOM Standard › Shadow DOM](https://dom.spec.whatwg.org/#shadow-trees)

- Custom Elements
  - [HTML Standard › Custom Elements](https://html.spec.whatwg.org/multipage/scripting.html#custom-elements)

- HTML Templates
  - [HTML Standard › HTML Templates](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element)

- CSS changes
  - [CSS Scoping](https://drafts.csswg.org/css-scoping/)
  - [CSS Shadow Parts](https://drafts.csswg.org/css-shadow-parts/)

- [JSON](https://www.chromestatus.com/feature/5749863620804608), [CSS](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/css-modules-v1-explainer.md), [HTML](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/html-modules-explainer.md) Modules


## Specification Drafts, Reviews & Explainers

- [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494)
  - [Chrome 90](https://developer.chrome.com/blog/new-in-chrome-90/#declarative)

> A declarative API to allow the creation of #shadowroots using only HTML and no Javascript. This API allows Web Components that use Shadow DOM to also make use of Server-Side Rendering (SSR), to get rendered content onscreen quickly without requiring Javascript for shadow root attachment and population.

- [Form-associated custom elements (attachInternals)](https://github.com/whatwg/html/pull/4383)
  - [HTML Living Standard](https://html.spec.whatwg.org/multipage/custom-elements.html#custom-elements-face-example)
  - [Chrome 77](https://www.chromestatus.com/features/4708990554472448)
  - [Bugzilla](https://bugzilla.mozilla.org/show_bug.cgi?id=1552327)
  - [Creating Custom Form Controls with ElementInternals ](https://css-tricks.com/creating-custom-form-controls-with-elementinternals/)


- [Shadow DOM Delegate Focus](https://blog.whatwg.org/focusing-on-focus)
> When the shadow root of an element has delegates focus flag set, focusing on the shadow host would automatically “delegates” focus to the first focusable element in the shadow tree instead.

- [CSSOM Constructable Stylesheet Objects](https://wicg.github.io/construct-stylesheets/)

- [my-element:--my-state custom state pseudo class](https://wicg.github.io/custom-state-pseudo-class/)
  - [Chrome 90](https://www.chromestatus.com/feature/6537562418053120)
  - [This feature is not (yet) a standard](https://css-tricks.com/custom-state-pseudo-classes-in-chrome/#this-feature-is-not-yet-a-standard)

## Articles

- [A history of the HTML slot element](https://component.kitchen/blog/posts/a-history-of-the-html-slot-element)
- [Brief, incomplete, and mostly incorrect history of Web Components](https://dmitriid.com/blog/2017/03/the-broken-promise-of-web-components/#brief-incomplete-and-mostly-incorrect-history-of-web-components)
- [The Firefox UI is now built with Web Components](https://briangrinstead.com/blog/firefox-webcomponents/)
- [GitHub is using custom elements for their modal dialogs, autocomplete and display time.](https://githubengineering.com/removing-jquery-from-github-frontend/#custom-elements)
- [Container Queries in Web Components](https://mxb.dev/blog/container-queries-web-components/)
- [Links on Web Components](https://css-tricks.com/links-on-web-components/)
- [Awesome Standalones](https://github.com/davatron5000/awesome-standalones)
- [Web Components and lists](https://twitter.com/techytacos/status/1407068338644144155)

## Frameworks & Routers

- [CrossBow](https://crossbow-wc-2ayn6.ondigitalocean.app/)
> The goal of Crossbow is to be the _Next.js_ for web-components.

- [Rocket](https://rocket.modern-web.dev/)
> A modern web [setup](https://twitter.com/techytacos/status/1408507828063535109) for static sites with a sprinkle of JavaScript.

- [Appolo Elements](https://apolloelements.dev/)

- [FAST Router](https://github.com/microsoft/fast/tree/master/packages/web-components/fast-router)

## Stats

- [Percentage of page loads that use custom element](https://www.chromestatus.com/metrics/feature/timeline/popularity/1689)

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

## Resources

- [Awesome Lit](https://nicedoc.io/web-padawan/awesome-lit)
- [Awesome Standalones](https://github.com/davatron5000/awesome-standalones)
- [Are Web Components A Thing Yet](https://arewebcomponentsathingyet.com/)
- [All the Ways to Make a Web Component](https://webcomponents.dev/blog/all-the-ways-to-make-a-web-component/)
