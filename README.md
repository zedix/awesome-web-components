# Awesome Web Components [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> This is a curated list of Web Components design systems, librairies and resources.

- Web Components are the **native component model** on the web platform.
- Web Components **exposes capabilities** previously reserved for native code
- Web Components are **low level** DOM APIs

## Contents

- [Component Libraries](#component-libraries)

## Component Libraries

- [Google Material](https://github.com/material-components/material-components-web-components)
- [Helix UI](https://helixdesignsystem.github.io/helix-ui/)
- [Microsoft Fast](https://fast.design/)
- [Microsoft Graph](https://github.com/microsoftgraph/microsoft-graph-toolkit)
  ⇢ [StoryBook](https://mgt.dev/)
- [PatternFly Design System](https://github.com/patternfly/patternfly-elements)
- [SAP UI5](https://github.com/SAP/ui5-webcomponents)
- [Vaddin](https://vaadin.com/components)

### Built with [Lit-element](https://github.com/Polymer/lit-element)

![lit-element](https://img.shields.io/badge/lib-lit--element-blue.svg?maxAge=60)

- [Alaska Airlines Auro Design System](https://auro.alaskaair.com/)
- [AXA Pattern Library ](https://github.com/axa-ch/patterns-library)
  ⇢ [StoryBook](https://patterns.axa.ch/?path=/story/welcome--to-pattern-library)
- [Blackstone UI](https://github.com/kjantzer/bui)
- [Chameleon Design System](https://github.com/MaritzSTL/chameleon)
  ⇢ [StoryBook](https://chameleon-design-system.netlify.app/?path=/story/*)
- [Clever UI](https://github.com/CleverCloud/clever-components)
  ⇢ [StoryBook](https://www.clever-cloud.com/doc/clever-components/)
- [IBM Carbon Design System](https://github.com/carbon-design-system/carbon-custom-elements)
  ⇢ [StoryBook](https://web-components.carbondesignsystem.com/)
- [Kor UI Design System](https://kor-ui.com/)
- [ING Lion](https://github.com/ing-bank/lion)
- [Lithium UI](https://github.com/coryrylan/lithium)
- [Shoelace](https://github.com/shoelace-style/shoelace) ❤︎
- [Weightless](https://weightless.dev/)
- [Zedix UI](https://github.com/zedix/zedix-ui)

### Built with [Stencil](https://github.com/ionic-team/stencil)

![lit-stencil](https://img.shields.io/badge/lib-lit--stencil-blue.svg?maxAge=60)

- [Duet Design System](https://www.duetds.com/)
- [Elix](https://component.kitchen/elix)

## Sites build entirely with Web Components

- [Fast](https://www.fast.design/)
- [Ideanote](https://ideanote.io/)


## [Specifications](https://github.com/WICG/webcomponents)

Web components is a meta-specification made possible by the above specifications:

- Shadow DOM
  - [DOM Standard › Shadow DOM](https://dom.spec.whatwg.org/#shadow-trees)

- Custom Elements
  - [HTML Standard › Custom Elements](https://html.spec.whatwg.org/multipage/scripting.html#custom-elements)

- HTML Templates
  - [HTML Standard › HTML Templates](https://html.spec.whatwg.org/multipage/scripting.html#the-template-element)

- CSS changes
  - [CSS Scoping](https://drafts.csswg.org/css-scoping/)
  - [CSS Shadow Parts](https://drafts.csswg.org/css-shadow-parts/)

- JSON, [CSS](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/css-modules-v1-explainer.md), [HTML](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/html-modules-explainer.md) Modules


## Specification Drafts, Reviews & Explainers

- [Declarative Shadow DOM](https://github.com/w3ctag/design-reviews/issues/494)
> A declarative API to allow the creation of #shadowroots using only HTML and no Javascript. This API allows Web Components that use Shadow DOM to also make use of Server-Side Rendering (SSR), to get rendered content onscreen quickly without requiring Javascript for shadow root attachment and population.

- [Form-associated custom elements (attachInternals)](https://www.chromestatus.com/feature/4708990554472448)

- [Shadow DOM Delegate Focus](https://blog.whatwg.org/focusing-on-focus)
> When the shadow root of an element has delegates focus flag set, focusing on the shadow host would automatically “delegates” focus to the first focusable element in the shadow tree instead.

- [CSSOM Constructable Stylesheet Objects](https://wicg.github.io/construct-stylesheets/)

- [:state() custom state pseudo class](https://github.com/WICG/webcomponents/blob/gh-pages/proposals/custom-states-and-state-pseudo-class.md)

## Articles

- [A history of the HTML slot element](https://component.kitchen/blog/posts/a-history-of-the-html-slot-element)
- [Brief, incomplete, and mostly incorrect history of Web Components](https://dmitriid.com/blog/2017/03/the-broken-promise-of-web-components/#brief-incomplete-and-mostly-incorrect-history-of-web-components)
- [The Firefox UI is now built with Web Components](https://briangrinstead.com/blog/firefox-webcomponents/)
- [GitHub is using custom elements for their modal dialogs, autocomplete and display time.](https://githubengineering.com/removing-jquery-from-github-frontend/#custom-elements)
