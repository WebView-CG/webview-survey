# webview-survey


## What do you use WebView for?

- [x] Hybrid apps (Apache Cordova, Capacitor…)
- [ ] Browser apps
- [x] Mini apps
- [x] Internal/Information pages
- [x] Ads
- [x] Offline web content
- [ ] External links

## What WebView features do you use?

- [x] CSS injection
- [x] JavaScript injection
- [x] Cookies
- [x] WebStorage (localStorage, sessionStorage…)
- [x] Video Playback
- [x] WebSockets
- [x] Other: Native interfaces and message handlers

## What are your top pain points with using WebView?

- [ ] Missing web features
- [ ] WebView bugs
- [x] Inconsistency
- [ ] Performance
- [ ] Security
- [x] Other:
  - No granular control on requests (including POST request) for navigation, fetch(), etc.
  - No native hooks into [Permissions API](https://developer.mozilla.org/en-US/docs/Web/API/Permissions_API) to control access to features from native side.
  - No support for custom (native) permissions through Permissions API.
  - No way to run service workers without the webview & reattach them to it later.
  - No support for [BroadcastChannel](https://developer.mozilla.org/en-US/docs/Web/API/BroadcastChannel) across webviews using same origin.

## What specific platforms do you develop on?

- [x] Android
- [x] iOS
- [ ] macOS
- [ ] Linux
- [ ] Windows
- [ ] Other

## Which WebView implementation do you use?

- [x] Android WebView
- [ ] Custom Tabs
- [ ] SFSafariViewController
- [ ] UIWebView (deprecated)
- [x] WKWebView
- [ ] WebView2
- [ ] X5 WebView (Tencent Browser Services WebView)
- [ ] Other [ comment ]

## Do you know how to file bugs and search for documentation about WebView?

- [x] Yes
- [ ] No
- [ ] Unsure

## Do you feel WebView documentation is adequate?

- [x] Yes
- [ ] No
- [ ] Unsure [ comment ]

## How do you keep track of web platform features that are available in WebViews?

- [x] Blogs
- [x] Release notes
- [x] Experimentation

## What programming language is utilized in your embedding solution?

Kotlin, Swift, Typescript/Svelte.

## How are you achieving consistent behavior and rendering across different platforms and devices using WebView ?

Consistent behavior requires hooking into various DOM APIs using javascript injection when documents start loading, and polyfilling things with a lot of plumbing.

## What approaches do you take to test WebViews and ensure their behavior remains consistent across various devices and platforms?

Device farm.

## Are there features or functionality missing from Progressive Web Apps (PWAs) that if added would motivate you to maintaining a PWA instead of your WebView-based solution?

If the following things were both supported, we probably would only use PWA. If either is not supported, we still require native apps:

1. Ablity to distribute PWAs as-is (i.e. without a wrapper binary) on the various vendors' application stores (AppStore, Play Store…).
2. Ability to access any of a platform's public native APIs from WebAssembly, with permissions checked at install time rather than at runtime (through some "native binding manifest" maybe?).

## How do you decide when to use a WebView vs navigating to a browser app?

- WebView: anything were we need to inject authentication in for our users, anything that requires accessing native features provided by our vendors, anything that's self-contained and informational.
- Browser: external links, links to sites we want to persist the state of across apps and the browser, links to pages that have unrestricted outgoing links.

## How do you work around some of the shortcomings of WebView today?

With pain. See above.

## What are your thoughts about WebView from a privacy and security point of view?

It's irrelevant. A browser is an app with webviews. A browser can provide privacy and security. Our apps can as well.

## Are there features of functionality missing in the WebView you use? (e.g., prerender, WebviewPool,...)

> _features of functionality_

I could not understand this part.
