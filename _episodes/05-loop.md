





<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  <link rel="dns-prefetch" href="https://github.githubassets.com">
  <link rel="dns-prefetch" href="https://avatars0.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars1.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars2.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars3.githubusercontent.com">
  <link rel="dns-prefetch" href="https://github-cloud.s3.amazonaws.com">
  <link rel="dns-prefetch" href="https://user-images.githubusercontent.com/">



  <link crossorigin="anonymous" media="all" integrity="sha512-7mtunHqp/Bw0ND9akjJME8XCh0WPm3HAXOSeX7skL0qGAhpdfzkQvYcujYcwNPTpWKeKMFUGZGtvnEkcczFgwQ==" rel="stylesheet" href="https://github.githubassets.com/assets/frameworks-9b5314213e37056ed87b0418056c4f2c.css" />
  
    <link crossorigin="anonymous" media="all" integrity="sha512-buKrCr/U0ONf5rzeRzWnv1EyeTW4RjXcppt74M0ghnwsD4Tsu0LsD6XIIGhvpB4eJKk3n8wyJOzWqV7jwNEhAA==" rel="stylesheet" href="https://github.githubassets.com/assets/github-f07e60f7e20ba26efee2908fc2297f76.css" />
    
    
    
    


  <meta name="viewport" content="width=device-width">
  
  <title>shell-novice/05-loop.md at gh-pages · swcarpentry/shell-novice</title>
    <meta name="description" content="Software Carpentry introduction to the shell for novices. - swcarpentry/shell-novice">
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <meta property="fb:app_id" content="1401488693436528">

    <meta name="twitter:image:src" content="https://avatars1.githubusercontent.com/u/2238358?s=400&amp;v=4" /><meta name="twitter:site" content="@github" /><meta name="twitter:card" content="summary" /><meta name="twitter:title" content="swcarpentry/shell-novice" /><meta name="twitter:description" content="Software Carpentry introduction to the shell for novices. - swcarpentry/shell-novice" />
    <meta property="og:image" content="https://avatars1.githubusercontent.com/u/2238358?s=400&amp;v=4" /><meta property="og:site_name" content="GitHub" /><meta property="og:type" content="object" /><meta property="og:title" content="swcarpentry/shell-novice" /><meta property="og:url" content="https://github.com/swcarpentry/shell-novice" /><meta property="og:description" content="Software Carpentry introduction to the shell for novices. - swcarpentry/shell-novice" />

  <link rel="assets" href="https://github.githubassets.com/">
  <link rel="web-socket" href="wss://live.github.com/_sockets/VjI6NDU1MDAxMjY0OjZmYTI0MzIyYjEzODgwZDVjOGFiY2MyYWQyNGE3OTU0NDBkMmZhNGRjNzQ2MDc2YTYyOGUwYjQ1YjVkMjIzYTE=--f116c8ec6e63f11db7461cf9a8f1f2fb2d9c7feb">
  <link rel="sudo-modal" href="/sessions/sudo_modal">

    <meta name="request-id" content="C5EF:3C2D:A3CDE63:A84A61A:5DF02866" data-pjax-transient>



  

  <meta name="selected-link" value="repo_source" data-pjax-transient>

      <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
    <meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-site-verification" content="GXs5KoUUkNCoaAZn7wPN-t01Pywp9M3sEjnt_3_ZWPc">

    <meta name="octolytics-host" content="collector.githubapp.com" /><meta name="octolytics-app-id" content="github" /><meta name="octolytics-event-url" content="https://collector.githubapp.com/github-external/browser_event" /><meta name="octolytics-dimension-request_id" content="C5EF:3C2D:A3CDE63:A84A61A:5DF02866" /><meta name="octolytics-dimension-region_edge" content="sea" /><meta name="octolytics-dimension-region_render" content="iad" /><meta name="octolytics-dimension-ga_id" content="" class="js-octo-ga-id" /><meta name="octolytics-dimension-visitor_id" content="2560940999897393916" /><meta name="octolytics-actor-id" content="12768545" /><meta name="octolytics-actor-login" content="jonjab" /><meta name="octolytics-actor-hash" content="31559e89d522998f303fca85f330ef6cf14818bb3089e40d2b563d4720e64976" />

<meta name="analytics-location" content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" />



    <meta name="google-analytics" content="UA-3769691-2">

  <meta class="js-ga-set" name="userId" content="a8a77ffad91beabc78993a7b22489ae8">

<meta class="js-ga-set" name="dimension1" content="Logged In">



  

      <meta name="hostname" content="github.com">
    <meta name="user-login" content="jonjab">

      <meta name="expected-hostname" content="github.com">

      <meta name="js-proxy-site-detection-payload" content="MjQ1YTY1ZmFhNmM2ZTJiZjM3NmJkOTViYzgzYTJjMDdlYzYxZGNhMzUzYjBhODQ5MTZkZmQwOTY5OGMyNjFmYXx7InJlbW90ZV9hZGRyZXNzIjoiMTY5LjIzMS45OS4yMyIsInJlcXVlc3RfaWQiOiJDNUVGOjNDMkQ6QTNDREU2MzpBODRBNjFBOjVERjAyODY2IiwidGltZXN0YW1wIjoxNTc2MDIwMDc3LCJob3N0IjoiZ2l0aHViLmNvbSJ9">

    <meta name="enabled-features" content="LAUNCH_PROJECT,MARKETPLACE_FEATURED_BLOG_POSTS,MARKETPLACE_INVOICED_BILLING,MARKETPLACE_SOCIAL_PROOF_CUSTOMERS,MARKETPLACE_TRENDING_SOCIAL_PROOF,MARKETPLACE_RECOMMENDATIONS,MARKETPLACE_PENDING_INSTALLATIONS,NOTIFY_ON_BLOCK,RELATED_ISSUES,GHE_CLOUD_TRIAL">

    <meta name="html-safe-nonce" content="6f077df35955184e026c33581f861103eed593d1">

  <meta http-equiv="x-pjax-version" content="c75b47f31a9b8aa232a84779d7d6d113">
  

      <link href="https://github.com/swcarpentry/shell-novice/commits/gh-pages.atom" rel="alternate" title="Recent Commits to shell-novice:gh-pages" type="application/atom+xml">

  <meta name="go-import" content="github.com/swcarpentry/shell-novice git https://github.com/swcarpentry/shell-novice.git">

  <meta name="octolytics-dimension-user_id" content="2238358" /><meta name="octolytics-dimension-user_login" content="swcarpentry" /><meta name="octolytics-dimension-repository_id" content="25592861" /><meta name="octolytics-dimension-repository_nwo" content="swcarpentry/shell-novice" /><meta name="octolytics-dimension-repository_public" content="true" /><meta name="octolytics-dimension-repository_is_fork" content="false" /><meta name="octolytics-dimension-repository_network_root_id" content="25592861" /><meta name="octolytics-dimension-repository_network_root_nwo" content="swcarpentry/shell-novice" /><meta name="octolytics-dimension-repository_explore_github_marketplace_ci_cta_shown" content="false" />


    <link rel="canonical" href="https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md" data-pjax-transient>


  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">

  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">

  <link rel="mask-icon" href="https://github.githubassets.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" class="js-site-favicon" href="https://github.githubassets.com/favicon.ico">

<meta name="theme-color" content="#1e2327">



  <meta name="webauthn-auth-enabled" content="true">

  <meta name="webauthn-registration-enabled" content="true">

  <link rel="manifest" href="/manifest.json" crossOrigin="use-credentials">

  </head>

  <body class="logged-in env-production emoji-size-boost page-responsive page-blob">
    

  <div class="position-relative js-header-wrapper ">
    <a href="#start-of-content" tabindex="1" class="p-3 bg-blue text-white show-on-focus js-skip-to-content">Skip to content</a>
    <span class="Progress progress-pjax-loader position-fixed width-full js-pjax-loader-bar">
      <span class="progress-pjax-loader-bar top-0 left-0" style="width: 0%;"></span>
    </span>

    
    
    


          <header class="Header js-details-container Details flex-wrap flex-lg-nowrap p-responsive" role="banner">

    <div class="Header-item d-none d-lg-flex">
      <a class="Header-link" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg class="octicon octicon-mark-github v-align-middle" height="32" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
</a>

    </div>

    <div class="Header-item d-lg-none">
      <button class="Header-link btn-link js-details-target" type="button" aria-label="Toggle navigation" aria-expanded="false">
        <svg height="24" class="octicon octicon-three-bars" viewBox="0 0 12 16" version="1.1" width="18" aria-hidden="true"><path fill-rule="evenodd" d="M11.41 9H.59C0 9 0 8.59 0 8c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zm0-4H.59C0 5 0 4.59 0 4c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zM.59 11H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1H.59C0 13 0 12.59 0 12c0-.59 0-1 .59-1z"/></svg>
      </button>
    </div>

    <div class="Header-item Header-item--full flex-column flex-lg-row width-full flex-order-2 flex-lg-order-none mr-0 mr-lg-3 mt-3 mt-lg-0 Details-content--hidden">
        <div class="header-search flex-self-stretch flex-lg-self-auto mr-0 mr-lg-3 mb-3 mb-lg-0 scoped-search site-scoped-search js-site-search position-relative js-jump-to"
  role="combobox"
  aria-owns="jump-to-results"
  aria-label="Search or jump to"
  aria-haspopup="listbox"
  aria-expanded="false"
>
  <div class="position-relative">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-site-search-form" role="search" aria-label="Site" data-scope-type="Repository" data-scope-id="25592861" data-scoped-search-url="/swcarpentry/shell-novice/search" data-unscoped-search-url="/search" action="/swcarpentry/shell-novice/search" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
      <label class="form-control input-sm header-search-wrapper p-0 header-search-wrapper-jump-to position-relative d-flex flex-justify-between flex-items-center js-chromeless-input-container">
        <input type="text"
          class="form-control input-sm header-search-input jump-to-field js-jump-to-field js-site-search-focus js-site-search-field is-clearable"
          data-hotkey="s,/"
          name="q"
          value=""
          placeholder="Search or jump to…"
          data-unscoped-placeholder="Search or jump to…"
          data-scoped-placeholder="Search or jump to…"
          autocapitalize="off"
          aria-autocomplete="list"
          aria-controls="jump-to-results"
          aria-label="Search or jump to…"
          data-jump-to-suggestions-path="/_graphql/GetSuggestedNavigationDestinations#csrf-token=yHL3+lT32FxBasBa7WizbxLcKwu7W8YXzqTlgUTuWYPXm1Z2Q+fLDTFY90mrKk4SowYN7JKxo2J30MMXAvYSKQ=="
          spellcheck="false"
          autocomplete="off"
          >
          <input type="hidden" class="js-site-search-type-field" name="type" >
            <img src="https://github.githubassets.com/images/search-key-slash.svg" alt="" class="mr-2 header-search-key-slash">

            <div class="Box position-absolute overflow-hidden d-none jump-to-suggestions js-jump-to-suggestions-container">
              
<ul class="d-none js-jump-to-suggestions-template-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-suggestion" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

</ul>

<ul class="d-none js-jump-to-no-results-template-container">
  <li class="d-flex flex-justify-center flex-items-center f5 d-none js-jump-to-suggestion p-2">
    <span class="text-gray">No suggested jump to results</span>
  </li>
</ul>

<ul id="jump-to-results" role="listbox" class="p-0 m-0 js-navigation-container jump-to-suggestions-results-container js-jump-to-suggestions-results-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-scoped-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-global-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>


    <li class="d-flex flex-justify-center flex-items-center p-0 f5 js-jump-to-suggestion">
      <img src="https://github.githubassets.com/images/spinners/octocat-spinner-128.gif" alt="Octocat Spinner Icon" class="m-2" width="28">
    </li>
</ul>

            </div>
      </label>
</form>  </div>
</div>


      <nav class="d-flex flex-column flex-lg-row flex-self-stretch flex-lg-self-auto" aria-label="Global">
    <a class="Header-link d-block d-lg-none py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:dashboard:user" aria-label="Dashboard" href="/dashboard">
      Dashboard
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g p" data-ga-click="Header, click, Nav menu - item:pulls context:user" aria-label="Pull requests you created" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls" href="/pulls">
    Pull requests
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g i" data-ga-click="Header, click, Nav menu - item:issues context:user" aria-label="Issues you created" data-selected-links="/issues /issues/assigned /issues/mentioned /issues" href="/issues">
    Issues
</a>
    <div class="mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15">
      <a class="js-selected-navigation-item Header-link" data-ga-click="Header, click, Nav menu - item:marketplace context:user" data-octo-click="marketplace_click" data-octo-dimensions="location:nav_bar" data-selected-links=" /marketplace" href="/marketplace">
        Marketplace
</a>      

    </div>

  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:explore" data-selected-links="/explore /trending /trending/developers /integrations /integrations/feature/code /integrations/feature/collaborate /integrations/feature/ship showcases showcases_search showcases_landing /explore" href="/explore">
    Explore
</a>


    <a class="Header-link d-block d-lg-none mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" href="https://github.com/jonjab">
      <img class="avatar" height="20" width="20" alt="@jonjab" src="https://avatars1.githubusercontent.com/u/12768545?s=60&amp;v=4" />
      jonjab
</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="Olog6oH/TIrFgkdxbjqptLrqfeISdtqlMdk+x7q0Np9cinVB+UEbvTaZ9AFfSTnU9D31cUTel15Wc+YoXHc6Zg==" />
      <button type="submit" class="Header-link mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15 d-lg-none btn-link d-block width-full text-left" data-ga-click="Header, sign out, icon:logout" style="padding-left: 2px;">
        <svg class="octicon octicon-sign-out v-align-middle" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9V7H8V5h4V3l4 3-4 3zm-2 3H6V3L2 1h8v3h1V1c0-.55-.45-1-1-1H1C.45 0 0 .45 0 1v11.38c0 .39.22.73.55.91L6 16.01V13h4c.55 0 1-.45 1-1V8h-1v4z"/></svg>
        Sign out
      </button>
</form></nav>

    </div>

    <div class="Header-item Header-item--full flex-justify-center d-lg-none position-relative">
      <div class="css-truncate css-truncate-target width-fit position-absolute left-0 right-0 text-center">
              <svg class="octicon octicon-repo" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
    <a class="Header-link" href="/swcarpentry">swcarpentry</a>
    /
    <a class="Header-link" href="/swcarpentry/shell-novice">shell-novice</a>

</div>
    </div>


    <div class="Header-item mr-0 mr-lg-3 flex-order-1 flex-lg-order-none">
      

    <a aria-label="You have unread notifications" class="Header-link notification-indicator position-relative tooltipped tooltipped-sw js-socket-channel js-notification-indicator" data-hotkey="g n" data-ga-click="Header, go to notifications, icon:unread" data-channel="notification-changed:12768545" href="/notifications">
        <span class="mail-status unread"></span>
        <svg class="octicon octicon-bell" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 12v1H0v-1l.73-.58c.77-.77.81-2.55 1.19-4.42C2.69 3.23 6 2 6 2c0-.55.45-1 1-1s1 .45 1 1c0 0 3.39 1.23 4.16 5 .38 1.88.42 3.66 1.19 4.42l.66.58H14zm-7 4c1.11 0 2-.89 2-2H5c0 1.11.89 2 2 2z"/></svg>
</a>
    </div>


    <div class="Header-item position-relative d-none d-lg-flex">
      <details class="details-overlay details-reset">
  <summary class="Header-link"
      aria-label="Create new…"
      data-ga-click="Header, create new, icon:add">
    <svg class="octicon octicon-plus" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9H7v5H5V9H0V7h5V2h2v5h5v2z"/></svg> <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw">
    
<a role="menuitem" class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a role="menuitem" class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>

<a role="menuitem" class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, create new gist">
  New gist
</a>

  <a role="menuitem" class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>


  <div role="none" class="dropdown-divider"></div>
  <div class="dropdown-header">
    <span title="swcarpentry/shell-novice">This repository</span>
  </div>
    <a role="menuitem" class="dropdown-item" href="/swcarpentry/shell-novice/issues/new" data-ga-click="Header, create new issue" data-skip-pjax>
      New issue
    </a>


  </details-menu>
</details>

    </div>

    <div class="Header-item position-relative mr-0 d-none d-lg-flex">
      
  <details class="details-overlay details-reset js-feature-preview-indicator-container" data-feature-preview-indicator-src="/users/jonjab/feature_preview/indicator_check.json">

  <summary class="Header-link"
    aria-label="View profile and more"
    data-ga-click="Header, show menu, icon:avatar">
    <img alt="@jonjab" class="avatar" src="https://avatars2.githubusercontent.com/u/12768545?s=40&amp;v=4" height="20" width="20">
      <span class="feature-preview-indicator js-feature-preview-indicator" hidden></span>
    <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw mt-2" style="width: 180px">
    <div class="header-nav-current-user css-truncate"><a role="menuitem" class="no-underline user-profile-link px-3 pt-2 pb-2 mb-n2 mt-n1 d-block" href="/jonjab" data-ga-click="Header, go to profile, text:Signed in as">Signed in as <strong class="css-truncate-target">jonjab</strong></a></div>
    <div role="none" class="dropdown-divider"></div>

      <div class="pl-3 pr-3 f6 user-status-container js-user-status-context pb-1" data-url="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1">
        
<div class="js-user-status-container
    user-status-compact rounded-1 px-2 py-1 mt-2
    border
  " data-team-hovercards-enabled>
  <details class="js-user-status-details details-reset details-overlay details-overlay-dark">
    <summary class="btn-link btn-block link-gray no-underline js-toggle-user-status-edit toggle-user-status-edit "
      role="menuitem" data-hydro-click="{&quot;event_type&quot;:&quot;user_profile.click&quot;,&quot;payload&quot;:{&quot;profile_user_id&quot;:2238358,&quot;target&quot;:&quot;EDIT_USER_STATUS&quot;,&quot;user_id&quot;:12768545,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;}}" data-hydro-click-hmac="aba0ea5924fca3123ccf3fd3dac49cd03f660392c14e002a154a69b069275414">
      <div class="d-flex">
        <div class="f6 lh-condensed user-status-header
          d-inline-block v-align-middle
            user-status-emoji-only-header circle
            pr-2
"
            style="max-width: 29px"
          >
          <div class="user-status-emoji-container flex-shrink-0 mr-1 mt-1 lh-condensed-ultra v-align-bottom" style="">
            <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 01-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 01-1.45-2.17A6.59 6.59 0 011.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 018 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
          </div>
        </div>
        <div class="
          d-inline-block v-align-middle
          
          
           css-truncate css-truncate-target 
           user-status-message-wrapper f6"
           style="line-height: 20px;" >
          <div class="d-inline-block text-gray-dark v-align-text-top text-left">
              <span class="text-gray ml-2">Set status</span>
          </div>
        </div>
      </div>
    </summary>
    <details-dialog class="details-dialog rounded-1 anim-fade-in fast Box Box--overlay" role="dialog" tabindex="-1">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="position-relative flex-auto js-user-status-form" action="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="_method" value="put" /><input type="hidden" name="authenticity_token" value="f8jHqMZ0YyBbkZtthDuopFyiJCEMg6V8uuocd/edkkqvud5+jqXbczg4Thjb610l2RNAN2xyuzsIl1SUuQc/2g==" />
        <div class="Box-header bg-gray border-bottom p-3">
          <button class="Box-btn-octicon js-toggle-user-status-edit btn-octicon float-right" type="reset" aria-label="Close dialog" data-close-dialog>
            <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
          </button>
          <h3 class="Box-title f5 text-bold text-gray-dark">Edit status</h3>
        </div>
        <input type="hidden" name="emoji" class="js-user-status-emoji-field" value="">
        <input type="hidden" name="organization_id" class="js-user-status-org-id-field" value="">
        <div class="px-3 py-2 text-gray-dark">
          <div class="js-characters-remaining-container position-relative mt-2">
            <div class="input-group d-table form-group my-0 js-user-status-form-group">
              <span class="input-group-button d-table-cell v-align-middle" style="width: 1%">
                <button type="button" aria-label="Choose an emoji" class="btn-outline btn js-toggle-user-status-emoji-picker btn-open-emoji-picker p-0">
                  <span class="js-user-status-original-emoji" hidden></span>
                  <span class="js-user-status-custom-emoji"></span>
                  <span class="js-user-status-no-emoji-icon" >
                    <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 01-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 01-1.45-2.17A6.59 6.59 0 011.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 018 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
                  </span>
                </button>
              </span>
              <text-expander keys=": @" data-mention-url="/autocomplete/user-suggestions" data-emoji-url="/autocomplete/emoji">
                <input
                  type="text"
                  autocomplete="off"
                  data-no-org-url="/autocomplete/user-suggestions"
                  data-org-url="/suggestions?mention_suggester=1"
                  data-maxlength="80"
                  class="d-table-cell width-full form-control js-user-status-message-field js-characters-remaining-field"
                  placeholder="What's happening?"
                  name="message"
                  value=""
                  aria-label="What is your current status?">
              </text-expander>
              <div class="error">Could not update your status, please try again.</div>
            </div>
            <div style="margin-left: 53px" class="my-1 text-small label-characters-remaining js-characters-remaining" data-suffix="remaining" hidden>
              80 remaining
            </div>
          </div>
          <include-fragment class="js-user-status-emoji-picker" data-url="/users/status/emoji"></include-fragment>
          <div class="overflow-auto ml-n3 mr-n3 px-3 border-bottom" style="max-height: 33vh">
            <div class="user-status-suggestions js-user-status-suggestions collapsed overflow-hidden">
              <h4 class="f6 text-normal my-3">Suggestions:</h4>
              <div class="mx-3 mt-2 clearfix">
                  <div class="float-left col-6">
                      <button type="button" value=":palm_tree:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="palm_tree" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f334.png">🌴</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          On vacation
                        </div>
                      </button>
                      <button type="button" value=":face_with_thermometer:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="face_with_thermometer" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f912.png">🤒</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Out sick
                        </div>
                      </button>
                  </div>
                  <div class="float-left col-6">
                      <button type="button" value=":house:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="house" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3e0.png">🏠</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Working from home
                        </div>
                      </button>
                      <button type="button" value=":dart:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="dart" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3af.png">🎯</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Focusing
                        </div>
                      </button>
                  </div>
              </div>
            </div>
            <div class="user-status-limited-availability-container">
              <div class="form-checkbox my-0">
                <input type="checkbox" name="limited_availability" value="1" class="js-user-status-limited-availability-checkbox" data-default-message="I may be slow to respond." aria-describedby="limited-availability-help-text-truncate-true-compact-true" id="limited-availability-truncate-true-compact-true">
                <label class="d-block f5 text-gray-dark mb-1" for="limited-availability-truncate-true-compact-true">
                  Busy
                </label>
                <p class="note" id="limited-availability-help-text-truncate-true-compact-true">
                  When others mention you, assign you, or request your review,
                  GitHub will let them know that you have limited availability.
                </p>
              </div>
            </div>
          </div>
            

<div class="d-inline-block f5 mr-2 pt-3 pb-2" >
  <div class="d-inline-block mr-1">
    Clear status
  </div>

  <details class="js-user-status-expire-drop-down f6 dropdown details-reset details-overlay d-inline-block mr-2">
    <summary class="f5 btn-link link-gray-dark border px-2 py-1 rounded-1" aria-haspopup="true">
      <div class="js-user-status-expiration-interval-selected d-inline-block v-align-baseline">
        Never
      </div>
      <div class="dropdown-caret"></div>
    </summary>

    <ul class="dropdown-menu dropdown-menu-se pl-0 overflow-auto" style="width: 220px; max-height: 15.5em">
      <li>
        <button type="button" class="btn-link dropdown-item js-user-status-expire-button ws-normal" title="Never">
          <span class="d-inline-block text-bold mb-1">Never</span>
          <div class="f6 lh-condensed">Keep this status until you clear your status or edit your status.</div>
        </button>
      </li>
      <li class="dropdown-divider" role="none"></li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 30 minutes" value="2019-12-10T15:51:17-08:00">
            in 30 minutes
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 1 hour" value="2019-12-10T16:21:17-08:00">
            in 1 hour
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 4 hours" value="2019-12-10T19:21:17-08:00">
            in 4 hours
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="today" value="2019-12-10T23:59:59-08:00">
            today
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="this week" value="2019-12-15T23:59:59-08:00">
            this week
          </button>
        </li>
    </ul>
  </details>
  <input class="js-user-status-expiration-date-input" type="hidden" name="expires_at" value="">
</div>

          <include-fragment class="js-user-status-org-picker" data-url="/users/status/organizations"></include-fragment>
        </div>
        <div class="d-flex flex-items-center flex-justify-between p-3 border-top">
          <button type="submit" disabled class="width-full btn btn-primary mr-2 js-user-status-submit">
            Set status
          </button>
          <button type="button" disabled class="width-full js-clear-user-status-button btn ml-2 ">
            Clear status
          </button>
        </div>
</form>    </details-dialog>
  </details>
</div>

      </div>
      <div role="none" class="dropdown-divider"></div>


    <a role="menuitem" class="dropdown-item" href="/jonjab" data-ga-click="Header, go to profile, text:your profile">Your profile</a>

    <a role="menuitem" class="dropdown-item" href="/jonjab?tab=repositories" data-ga-click="Header, go to repositories, text:your repositories">Your repositories</a>

    <a role="menuitem" class="dropdown-item" href="/jonjab?tab=projects" data-ga-click="Header, go to projects, text:your projects">Your projects</a>

    <a role="menuitem" class="dropdown-item" href="/jonjab?tab=stars" data-ga-click="Header, go to starred repos, text:your stars">Your stars</a>
      <a role="menuitem" class="dropdown-item" href="https://gist.github.com/mine" data-ga-click="Header, your gists, text:your gists">Your gists</a>





    <div role="none" class="dropdown-divider"></div>
      
<div id="feature-enrollment-toggle" class="hide-sm hide-md feature-preview-details position-relative">
  <button
    type="button"
    class="dropdown-item btn-link"
    role="menuitem"
    data-feature-preview-trigger-url="/users/jonjab/feature_previews"
    data-feature-preview-close-details="{&quot;event_type&quot;:&quot;feature_preview.clicks.close_modal&quot;,&quot;payload&quot;:{&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}"
    data-feature-preview-close-hmac="e060235cd0e03ffe7dd2c982c8a31ee2c9d75fb15da4677323fea2ebd580f4cb"
    data-hydro-click="{&quot;event_type&quot;:&quot;feature_preview.clicks.open_modal&quot;,&quot;payload&quot;:{&quot;link_location&quot;:&quot;user_dropdown&quot;,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}"
    data-hydro-click-hmac="263796d468f18efaa6375b3879f2c135085c5784f966b0a896e7df8c6bf999b8"
  >
    Feature preview
  </button>
    <span class="feature-preview-indicator js-feature-preview-indicator" hidden></span>
</div>

    <a role="menuitem" class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">Help</a>
    <a role="menuitem" class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">Settings</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="logout-form" action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="q9Xz51E2V1cDZIwhlj0KFx4GELfIzT1HSV4n7imJXODNBaZMKYgAYPB/P1GnTpp3UNGYJJ5lcLwu9P8Bz0pQGQ==" />
      
      <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout" role="menuitem">
        Sign out
      </button>
</form>  </details-menu>
</details>

    </div>

  </header>

      

  </div>

  <div id="start-of-content" class="show-on-focus"></div>


    <div id="js-flash-container">

</div>



  <div class="application-main " data-commit-hovercards-enabled>
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode" class="">
    <main  >
      


  



  








  <div class=" pagehead repohead readability-menu experiment-repo-nav pt-0 pt-lg-4 ">
    <div class="repohead-details-container clearfix container-lg p-responsive d-none d-lg-block">

      <ul class="pagehead-actions">




  <li>
    
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form data-remote="true" class="clearfix js-social-form js-social-container" action="/notifications/subscribe" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="4ElvRkTCq1rrOrLts6ZWg+KabQdt7EbLJfPvFJqCJ/RiKqOy//wA/W7pe+fsmnOO0TdI7vMQ2MSCgZbWLqWlsQ==" />      <input type="hidden" name="repository_id" value="25592861">

      <details class="details-reset details-overlay select-menu float-left">
        <summary class="select-menu-button float-left btn btn-sm btn-with-count" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;WATCH_BUTTON&quot;,&quot;repository_id&quot;:25592861,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}" data-hydro-click-hmac="8ca9ab71fa55d8be9a55a03cf1f3726cfc3f393675c688cd1f9b399f8b64babd" data-ga-click="Repository, click Watch settings, action:blob#show">          <span data-menu-button>
              <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
              Watch
          </span>
</summary>        <details-menu
          class="select-menu-modal position-absolute mt-5"
          style="z-index: 99;">
          <div class="select-menu-header">
            <span class="select-menu-title">Notifications</span>
          </div>
          <div class="select-menu-list">
            <button type="submit" name="do" value="included" class="select-menu-item width-full" aria-checked="true" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Not watching</span>
                <span class="description">Be notified only when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Watch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="release_only" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Releases only</span>
                <span class="description">Be notified of new releases, and when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch releases
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="subscribed" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Watching</span>
                <span class="description">Be notified of all conversations.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="ignore" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Ignoring</span>
                <span class="description">Never be notified.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-mute v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 2.81v10.38c0 .67-.81 1-1.28.53L3 10H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h2l3.72-3.72C7.19 1.81 8 2.14 8 2.81zm7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06L11.44 8 9.47 9.97l1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06L13.56 8l1.97-1.97z"/></svg>
                  Stop ignoring
                </span>
              </div>
            </button>
          </div>
        </details-menu>
      </details>
        <a class="social-count js-social-count"
          href="/swcarpentry/shell-novice/watchers"
          aria-label="89 users are watching this repository">
          89
        </a>
</form>
  </li>

  <li>
      <div class="js-toggler-container js-social-container starring-container ">
    <form class="starred js-social-form" action="/swcarpentry/shell-novice/unstar" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="cxrYRbu5XDnVa44LoLT2jVV11HF4RrBLcFEP6P4T4sxLf/A/QIGGwbwrgbIHmnSKmVEfUCA3gtim4KUx/B0ELw==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Unstar swcarpentry/shell-novice" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;UNSTAR_BUTTON&quot;,&quot;repository_id&quot;:25592861,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}" data-hydro-click-hmac="77199123a14429d6b0bd58a4914d8f80fd8691dfedc09f96466b83be94d29559" data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">        <svg aria-label="star" height="16" class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" role="img"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>

        Unstar
</button>        <a class="social-count js-social-count" href="/swcarpentry/shell-novice/stargazers"
           aria-label="173 users starred this repository">
           173
        </a>
</form>
    <form class="unstarred js-social-form" action="/swcarpentry/shell-novice/star" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="jRtGJOzDzFNk7pTQD/nHwnEW82fZZB6YJVck5qyCv7q+2dySEFH1X6wr05af45wbSrApQ4TXdL5Y7LckxMT5dQ==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Star swcarpentry/shell-novice" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;STAR_BUTTON&quot;,&quot;repository_id&quot;:25592861,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}" data-hydro-click-hmac="261214dd7ae44d84daebbc3c403f7bb48e2ef2b2b01891b62a5dc0160db2504f" data-ga-click="Repository, click star button, action:blob#show; text:Star">        <svg aria-label="star" height="16" class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" role="img"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>

        Star
</button>        <a class="social-count js-social-count" href="/swcarpentry/shell-novice/stargazers"
           aria-label="173 users starred this repository">
          173
        </a>
</form>  </div>

  </li>

  <li>
          <details class="details-reset details-overlay details-overlay-dark d-inline-block float-left">
            <summary class="btn btn-sm btn-with-count" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;FORK_BUTTON&quot;,&quot;repository_id&quot;:25592861,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}" data-hydro-click-hmac="67b3b5aaced5a50778d612066291c1fe5aaa3eb9ef6fd5d74eaee76c36981395" data-ga-click="Repository, show fork modal, action:blob#show; text:Fork" title="Fork your own copy of swcarpentry/shell-novice to your account">              <svg class="octicon octicon-repo-forked v-align-text-bottom" viewBox="0 0 10 16" version="1.1" width="10" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 00-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 002 1a1.993 1.993 0 00-1 3.72V6.5l3 3v1.78A1.993 1.993 0 005 15a1.993 1.993 0 001-3.72V9.5l3-3V4.72A1.993 1.993 0 008 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
              Fork
</summary>            <details-dialog
              class="anim-fade-in fast Box Box--overlay d-flex flex-column"
              src="/swcarpentry/shell-novice/fork?fragment=1"
              preload>
              <div class="Box-header">
                <button class="Box-btn-octicon btn-octicon float-right" type="button" aria-label="Close dialog" data-close-dialog>
                  <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
                </button>
                <h3 class="Box-title">Fork shell-novice</h3>
              </div>
              <div class="overflow-auto text-center">
                <include-fragment>
                  <div class="octocat-spinner my-3" aria-label="Loading..."></div>
                  <p class="f5 text-gray">If this dialog fails to load, you can visit <a href="/swcarpentry/shell-novice/fork">the fork page</a> directly.</p>
                </include-fragment>
              </div>
            </details-dialog>
          </details>

    <a href="/swcarpentry/shell-novice/network/members" class="social-count"
       aria-label="638 users forked this repository">
      638
    </a>
  </li>
</ul>

      <h1 class="public ">
    <svg class="octicon octicon-repo" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
  <span class="author" itemprop="author"><a class="url fn" rel="author" data-hovercard-type="organization" data-hovercard-url="/orgs/swcarpentry/hovercard" href="/swcarpentry">swcarpentry</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a data-pjax="#js-repo-pjax-container" href="/swcarpentry/shell-novice">shell-novice</a></strong>
  

</h1>

    </div>
    
<nav class="hx_reponav reponav js-repo-nav js-sidenav-container-pjax container-lg p-responsive d-none d-lg-block"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
    aria-label="Repository"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a class="js-selected-navigation-item selected reponav-item" itemprop="url" data-hotkey="g c" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /swcarpentry/shell-novice" href="/swcarpentry/shell-novice">
      <div class="d-inline"><svg class="octicon octicon-code" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg></div>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" data-hotkey="g i" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /swcarpentry/shell-novice/issues" href="/swcarpentry/shell-novice/issues">
        <div class="d-inline"><svg class="octicon octicon-issue-opened" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 011.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"/></svg></div>
        <span itemprop="name">Issues</span>
        <span class="Counter">94</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a data-hotkey="g p" data-skip-pjax="true" itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /swcarpentry/shell-novice/pulls" href="/swcarpentry/shell-novice/pulls">
      <div class="d-inline"><svg class="octicon octicon-git-pull-request" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0010 15a1.993 1.993 0 001-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 00-1 3.72v6.56A1.993 1.993 0 002 15a1.993 1.993 0 001-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg></div>
      <span itemprop="name">Pull requests</span>
      <span class="Counter">6</span>
      <meta itemprop="position" content="3">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement" class="position-relative float-left">
      <a data-hotkey="g w" data-skip-pjax="true" class="js-selected-navigation-item reponav-item" data-selected-links="repo_actions /swcarpentry/shell-novice/actions" href="/swcarpentry/shell-novice/actions">
        <div class="d-inline"><svg class="octicon octicon-play" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 8A7 7 0 110 8a7 7 0 0114 0zm-8.223 3.482l4.599-3.066a.5.5 0 000-.832L5.777 4.518A.5.5 0 005 4.934v6.132a.5.5 0 00.777.416z"/></svg></div>
        Actions
</a>
    </span>

    <a data-hotkey="g b" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /swcarpentry/shell-novice/projects" href="/swcarpentry/shell-novice/projects">
      <div class="d-inline"><svg class="octicon octicon-project" viewBox="0 0 15 16" version="1.1" width="15" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg></div>
      Projects
      <span class="Counter" >0</span>
</a>


    <a data-skip-pjax="true" class="js-selected-navigation-item reponav-item" data-selected-links="security alerts policy code_scanning /swcarpentry/shell-novice/security/advisories" href="/swcarpentry/shell-novice/security/advisories">
      <div class="d-inline"><svg class="octicon octicon-shield" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 2l7-2 7 2v6.02C14 12.69 8.69 16 7 16c-1.69 0-7-3.31-7-7.98V2zm1 .75L7 1l6 1.75v5.268C13 12.104 8.449 15 7 15c-1.449 0-6-2.896-6-6.982V2.75zm1 .75L7 2v12c-1.207 0-5-2.482-5-5.985V3.5z"/></svg></div>
      Security
</a>
    <a class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors dependency_graph pulse people /swcarpentry/shell-novice/pulse" href="/swcarpentry/shell-novice/pulse">
      <div class="d-inline"><svg class="octicon octicon-graph" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg></div>
      Insights
</a>

</nav>

  <div class="reponav-wrapper reponav-small d-lg-none">
  <nav class="reponav js-reponav text-center no-wrap"
       itemscope
       itemtype="http://schema.org/BreadcrumbList">

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a class="js-selected-navigation-item selected reponav-item" itemprop="url" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /swcarpentry/shell-novice" href="/swcarpentry/shell-novice">
        <span itemprop="name">Code</span>
        <meta itemprop="position" content="1">
</a>    </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /swcarpentry/shell-novice/issues" href="/swcarpentry/shell-novice/issues">
          <span itemprop="name">Issues</span>
          <span class="Counter">94</span>
          <meta itemprop="position" content="2">
</a>      </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /swcarpentry/shell-novice/pulls" href="/swcarpentry/shell-novice/pulls">
        <span itemprop="name">Pull requests</span>
        <span class="Counter">6</span>
        <meta itemprop="position" content="3">
</a>    </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /swcarpentry/shell-novice/projects" href="/swcarpentry/shell-novice/projects">
          <span itemprop="name">Projects</span>
          <span class="Counter">0</span>
          <meta itemprop="position" content="4">
</a>      </span>


      <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="security alerts policy code_scanning /swcarpentry/shell-novice/security/advisories" href="/swcarpentry/shell-novice/security/advisories">
        <span itemprop="name">Security</span>
        <meta itemprop="position" content="6">
</a>
      <a class="js-selected-navigation-item reponav-item" data-selected-links="pulse /swcarpentry/shell-novice/pulse" href="/swcarpentry/shell-novice/pulse">
        Pulse
</a>
      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="community /swcarpentry/shell-novice/community" href="/swcarpentry/shell-novice/community">
          Community
</a>      </span>

  </nav>
</div>


  </div>
<div class="container-lg clearfix new-discussion-timeline experiment-repo-nav  p-responsive">
  <div class="repository-content ">

    
    


  


    <a class="d-none js-permalink-shortcut" data-hotkey="y" href="/swcarpentry/shell-novice/blob/31b511c79e784c5f2cc792646e27b4a250186c8b/_episodes/05-loop.md">Permalink</a>

    <!-- blob contrib key: blob_contributors:v21:457a7109afbfb99cb3e989655ab9910f -->
      

    <div class="d-flex flex-items-start flex-shrink-0 pb-3 flex-column flex-md-row">
      <span class="d-flex flex-justify-between width-full width-md-auto">
        
<details class="details-reset details-overlay select-menu branch-select-menu  hx_rsm" id="branch-select-menu">
  <summary class="btn btn-sm select-menu-button css-truncate"
           data-hotkey="w"
           title="Switch branches or tags">
    <i>Branch:</i>
    <span class="css-truncate-target" data-menu-button>gh-pages</span>
  </summary>

  <details-menu class="select-menu-modal hx_rsm-modal position-absolute" style="z-index: 99;" src="/swcarpentry/shell-novice/refs/gh-pages/_episodes/05-loop.md?source_action=show&amp;source_controller=blob" preload>
    <include-fragment class="select-menu-loading-overlay anim-pulse">
      <svg height="32" class="octicon octicon-octoface" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M14.7 5.34c.13-.32.55-1.59-.13-3.31 0 0-1.05-.33-3.44 1.3-1-.28-2.07-.32-3.13-.32s-2.13.04-3.13.32c-2.39-1.64-3.44-1.3-3.44-1.3-.68 1.72-.26 2.99-.13 3.31C.49 6.21 0 7.33 0 8.69 0 13.84 3.33 15 7.98 15S16 13.84 16 8.69c0-1.36-.49-2.48-1.3-3.35zM8 14.02c-3.3 0-5.98-.15-5.98-3.35 0-.76.38-1.48 1.02-2.07 1.07-.98 2.9-.46 4.96-.46 2.07 0 3.88-.52 4.96.46.65.59 1.02 1.3 1.02 2.07 0 3.19-2.68 3.35-5.98 3.35zM5.49 9.01c-.66 0-1.2.8-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.54-1.78-1.2-1.78zm5.02 0c-.66 0-1.2.79-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.53-1.78-1.2-1.78z"/></svg>
    </include-fragment>
  </details-menu>
</details>

        <div class="BtnGroup flex-shrink-0 d-md-none">
          <a href="/swcarpentry/shell-novice/find/gh-pages"
                class="js-pjax-capture-input btn btn-sm BtnGroup-item"
                data-pjax
                data-hotkey="t">
            Find file
          </a>
          <clipboard-copy value="_episodes/05-loop.md" class="btn btn-sm BtnGroup-item">
            Copy path
          </clipboard-copy>
        </div>
      </span>
      <h2 id="blob-path" class="breadcrumb flex-auto min-width-0 text-normal flex-md-self-center ml-md-2 mr-md-3 my-2 my-md-0">
        <span class="js-repo-root text-bold"><span class="js-path-segment"><a data-pjax="true" href="/swcarpentry/shell-novice"><span>shell-novice</span></a></span></span><span class="separator">/</span><span class="js-path-segment"><a data-pjax="true" href="/swcarpentry/shell-novice/tree/gh-pages/_episodes"><span>_episodes</span></a></span><span class="separator">/</span><strong class="final-path">05-loop.md</strong>
      </h2>

      <div class="BtnGroup flex-shrink-0 d-none d-md-inline-block">
        <a href="/swcarpentry/shell-novice/find/gh-pages"
              class="js-pjax-capture-input btn btn-sm BtnGroup-item"
              data-pjax
              data-hotkey="t">
          Find file
        </a>
        <clipboard-copy value="_episodes/05-loop.md" class="btn btn-sm BtnGroup-item">
          Copy path
        </clipboard-copy>
      </div>
    </div>

    



    
  <div class="Box Box--condensed d-flex flex-column flex-shrink-0">
      <div class="Box-body d-flex flex-justify-between bg-blue-light flex-column flex-md-row flex-items-start flex-md-items-center">
        <span class="pr-md-4 f6">
          <a rel="contributor" data-skip-pjax="true" data-hovercard-type="user" data-hovercard-url="/users/gcapes/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/gcapes"><img class="avatar" src="https://avatars0.githubusercontent.com/u/12446270?s=40&amp;v=4" width="20" height="20" alt="@gcapes" /></a>
          <a class="text-bold link-gray-dark lh-default v-align-middle" rel="contributor" data-hovercard-type="user" data-hovercard-url="/users/gcapes/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/gcapes">gcapes</a>
            <span class="lh-default v-align-middle">
              <a data-pjax="true" title="Remove demotivating use of just

And a few that weren&#39;t demotivating, but unnecessary.

Fix #1023." class="link-gray" href="/swcarpentry/shell-novice/commit/a22c1907a751e4c0029da0fd658b3c6eb0470374">Remove demotivating use of just</a>
            </span>
        </span>
        <span class="d-inline-block flex-shrink-0 v-align-bottom f6 mt-2 mt-md-0">
          <a class="pr-2 text-mono link-gray" href="/swcarpentry/shell-novice/commit/a22c1907a751e4c0029da0fd658b3c6eb0470374" data-pjax>a22c190</a>
          <relative-time datetime="2019-09-03T13:08:12Z" class="no-wrap">Sep 3, 2019</relative-time>
        </span>
      </div>

    <div class="Box-body d-flex flex-items-center flex-auto f6 border-bottom-0 flex-wrap" >
      <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark float-left mr-2" id="blob_contributors_box">
        <summary class="btn-link">
          <span><strong>22</strong> contributors</span>
        </summary>
        <details-dialog
          class="Box Box--overlay d-flex flex-column anim-fade-in fast"
          aria-label="Users who have contributed to this file"
          src="/swcarpentry/shell-novice/contributors-list/gh-pages/_episodes/05-loop.md" preload>
          <div class="Box-header">
            <button class="Box-btn-octicon btn-octicon float-right" type="button" aria-label="Close dialog" data-close-dialog>
              <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
            </button>
            <h3 class="Box-title">
              Users who have contributed to this file
            </h3>
          </div>
          <include-fragment class="octocat-spinner my-3" aria-label="Loading..."></include-fragment>
        </details-dialog>
      </details>
        <span class="">
    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/gcapes/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=gcapes">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/12446270?s=40&amp;v=4" width="20" height="20" alt="@gcapes" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/csqrs/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=csqrs">
      <img class="avatar mr-1" src="https://avatars1.githubusercontent.com/u/19807761?s=40&amp;v=4" width="20" height="20" alt="@csqrs" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/colinmorris/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=colinmorris">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/695907?s=40&amp;v=4" width="20" height="20" alt="@colinmorris" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/gvwilson/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=gvwilson">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/911566?s=40&amp;v=4" width="20" height="20" alt="@gvwilson" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/gdevenyi/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=gdevenyi">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/3001850?s=40&amp;v=4" width="20" height="20" alt="@gdevenyi" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/marisalim/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=marisalim">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/5659802?s=40&amp;v=4" width="20" height="20" alt="@marisalim" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/rgaiacs/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=rgaiacs">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/1506457?s=40&amp;v=4" width="20" height="20" alt="@rgaiacs" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/jarekbryk/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=jarekbryk">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/7264784?s=40&amp;v=4" width="20" height="20" alt="@jarekbryk" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/ErinBecker/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=ErinBecker">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/19176319?s=40&amp;v=4" width="20" height="20" alt="@ErinBecker" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/mozeran/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=mozeran">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/31317895?s=40&amp;v=4" width="20" height="20" alt="@mozeran" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/willfurnass/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=willfurnass">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/1249695?s=40&amp;v=4" width="20" height="20" alt="@willfurnass" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/slel/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=slel">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/2786973?s=40&amp;v=4" width="20" height="20" alt="@slel" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/tomhohenstein/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=tomhohenstein">
      <img class="avatar mr-1" src="https://avatars1.githubusercontent.com/u/6785464?s=40&amp;v=4" width="20" height="20" alt="@tomhohenstein" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/pgmccann/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=pgmccann">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/1590010?s=40&amp;v=4" width="20" height="20" alt="@pgmccann" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/jpellman/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=jpellman">
      <img class="avatar mr-1" src="https://avatars1.githubusercontent.com/u/5000591?s=40&amp;v=4" width="20" height="20" alt="@jpellman" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/meiselj/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=meiselj">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/7231023?s=40&amp;v=4" width="20" height="20" alt="@meiselj" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/lxvii/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=lxvii">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/11477383?s=40&amp;v=4" width="20" height="20" alt="@lxvii" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/HoWol76/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=HoWol76">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/5634717?s=40&amp;v=4" width="20" height="20" alt="@HoWol76" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/jarrah42/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=jarrah42">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/6130694?s=40&amp;v=4" width="20" height="20" alt="@jarrah42" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/BrianBill/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=BrianBill">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/12534127?s=40&amp;v=4" width="20" height="20" alt="@BrianBill" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/alex-konovalov/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=alex-konovalov">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/5751387?s=40&amp;v=4" width="20" height="20" alt="@alex-konovalov" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/users/kathrynnapier/hovercard" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md?author=kathrynnapier">
      <img class="avatar mr-1" src="https://avatars0.githubusercontent.com/u/42160715?s=40&amp;v=4" width="20" height="20" alt="@kathrynnapier" /> 
</a>
</span>

    </div>
  </div>





    <div class="Box mt-3 position-relative">
      
<div class="Box-header py-2 d-flex flex-column flex-shrink-0 flex-md-row flex-md-items-center">
  <div class="text-mono f6 flex-auto pr-3 flex-order-2 flex-md-order-1 mt-2 mt-md-0">

      742 lines (667 sloc)
      <span class="file-info-divider"></span>
    22.7 KB
  </div>

  <div class="d-flex py-1 py-md-0 flex-auto flex-order-1 flex-md-order-2 flex-sm-grow-0 flex-justify-between">

    <div class="BtnGroup">
      <a id="raw-url" class="btn btn-sm BtnGroup-item" href="/swcarpentry/shell-novice/raw/gh-pages/_episodes/05-loop.md">Raw</a>
        <a class="btn btn-sm js-update-url-with-hash BtnGroup-item" data-hotkey="b" href="/swcarpentry/shell-novice/blame/gh-pages/_episodes/05-loop.md">Blame</a>
      <a rel="nofollow" class="btn btn-sm BtnGroup-item" href="/swcarpentry/shell-novice/commits/gh-pages/_episodes/05-loop.md">History</a>
    </div>


    <div>
            <a class="btn-octicon tooltipped tooltipped-nw"
               href="github-mac://openRepo/https://github.com/swcarpentry/shell-novice?branch=gh-pages&amp;filepath=_episodes%2F05-loop.md"
               aria-label="Open this file in GitHub Desktop"
               data-ga-click="Repository, open with desktop, type:mac">
                <svg class="octicon octicon-device-desktop" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M15 2H1c-.55 0-1 .45-1 1v9c0 .55.45 1 1 1h5.34c-.25.61-.86 1.39-2.34 2h8c-1.48-.61-2.09-1.39-2.34-2H15c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm0 9H1V3h14v8z"/></svg>
            </a>

            <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form js-update-url-with-hash" action="/swcarpentry/shell-novice/edit/gh-pages/_episodes/05-loop.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="MopDE7TiyT4vpYPVD0nFRoWWgXN2m6AfczOzB/UIB/7tmbtggfrc7sdGOdnBL5r8/mLawV8hLcNYdUiOQIsslw==" />
              <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
                aria-label="Fork this project and edit the file" data-hotkey="e" data-disable-with>
                <svg class="octicon octicon-pencil" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 011.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
              </button>
</form>
          <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form" action="/swcarpentry/shell-novice/delete/gh-pages/_episodes/05-loop.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="rf1P48oOPxWd8ho7jE6MWol+Om+sm91KymWYEZzPnz/ZU7kbeb/iETEn1ea2Uapqcv38STjwUrj0NQhMP4lUog==" />
            <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
              aria-label="Fork this project and delete the file" data-disable-with>
              <svg class="octicon octicon-trashcan" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
            </button>
</form>    </div>
  </div>
</div>




      
  <div id="readme" class="Box-body readme blob js-code-block-container">
    <article class="markdown-body entry-content p-3 p-md-6" itemprop="text"><table data-table-type="yaml-metadata">
  <thead>
  <tr>
  <th>title</th>
  <th>teaching</th>
  <th>exercises</th>
  <th>questions</th>
  <th>objectives</th>
  <th>keypoints</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>Loops</div></td>
  <td><div>40</div></td>
  <td><div>10</div></td>
  <td><div><table>
  <tbody>
  <tr>
  <td><div>How can I perform the same actions on many different files?</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  <td><div><table>
  <tbody>
  <tr>
  <td><div>Write a loop that applies one or more commands separately to each file in a set of files.</div></td>
  <td><div>Trace the values taken on by a loop variable during execution of the loop.</div></td>
  <td><div>Explain the difference between a variable's name and its value.</div></td>
  <td><div>Explain why spaces and some punctuation characters shouldn't be used in file names.</div></td>
  <td><div>Demonstrate how to see what commands have recently been executed.</div></td>
  <td><div>Re-run recently executed commands without retyping them.</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  <td><div><table>
  <tbody>
  <tr>
  <td><div>A `for` loop repeats commands once for every thing in a list.</div></td>
  <td><div>Every `for` loop needs a variable to refer to the thing it is currently operating on.</div></td>
  <td><div>Use `$name` to expand a variable (i.e., get its value). `${name}` can also be used.</div></td>
  <td><div>Do not use spaces, quotes, or wildcard characters such as '*' or '?' in filenames, as it complicates variable expansion.</div></td>
  <td><div>Give files consistent names that are easy to match with wildcard patterns to make it easy to select them for looping.</div></td>
  <td><div>Use the up-arrow key to scroll up through previous commands to edit and repeat them.</div></td>
  <td><div>Use `Ctrl-R` to search through the previously entered commands.</div></td>
  <td><div>Use `history` to display recent commands, and `!number` to repeat a command by number.</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table>

<p><strong>Loops</strong> are a programming construct which allow us to repeat a command or set of commands
for each item in a list.
As such they are key to productivity improvements through automation.
Similar to wildcards and tab completion, using loops also reduces the
amount of typing required (and hence reduces the number of typing mistakes).</p>
<p>Suppose we have several hundred genome data files named <code>basilisk.dat</code>, <code>minotaur.dat</code>, and
<code>unicorn.dat</code>.
For this example, we'll use the <code>creatures</code> directory which only has three example files,
but the principles can be applied to many many more files at once.</p>
<p>The structure of these files is the same: the common name, classification, and updated date are
presented on the first three lines, with DNA sequences on the following lines.
Let's look at the files:</p>
<pre><code>head -n 5 basilisk.dat minotaur.dat unicorn.dat
</code></pre>
<p>{: .language-bash}</p>
<p>We would like to print out the classification for each species, which is given on the second
line of each file.
For each file, we would need to execute the command <code>head -n 2</code> and pipe this to <code>tail -n 1</code>.
We’ll use a loop to solve this problem, but first let’s look at the general form of a loop:</p>
<pre><code>for thing in list_of_things
do
    operation_using $thing    # Indentation within the loop is not required, but aids legibility
done
</code></pre>
<p>{: .language-bash}</p>
<p>and we can apply this to our example like this:</p>
<pre><code>$ for filename in basilisk.dat minotaur.dat unicorn.dat
&gt; do
&gt;    head -n 2 $filename | tail -n 1
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<pre><code>CLASSIFICATION: basiliscus vulgaris
CLASSIFICATION: bos hominus
CLASSIFICATION: equus monoceros
</code></pre>
<p>{: .output}</p>
<blockquote>
<h2><a id="user-content-follow-the-prompt" class="anchor" aria-hidden="true" href="#follow-the-prompt"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Follow the Prompt</h2>
<p>The shell prompt changes from <code>$</code> to <code>&gt;</code> and back again as we were
typing in our loop. The second prompt, <code>&gt;</code>, is different to remind
us that we haven't finished typing a complete command yet. A semicolon, <code>;</code>,
can be used to separate two commands written on a single line.
{: .callout}</p>
</blockquote>
<p>When the shell sees the keyword <code>for</code>,
it knows to repeat a command (or group of commands) once for each item in a list.
Each time the loop runs (called an iteration), an item in the list is assigned in sequence to
the <strong>variable</strong>, and the commands inside the loop are executed, before moving on to
the next item in the list.
Inside the loop,
we call for the variable's value by putting <code>$</code> in front of it.
The <code>$</code> tells the shell interpreter to treat
the variable as a variable name and substitute its value in its place,
rather than treat it as text or an external command.</p>
<p>In this example, the list is three filenames: <code>basilisk.dat</code>, <code>minotaur.dat</code>, and <code>unicorn.dat</code>.
Each time the loop iterates, it will assign a file name to the variable <code>filename</code>
and run the <code>head</code> command.
The first time through the loop,
<code>$filename</code> is <code>basilisk.dat</code>.
The interpreter runs the command <code>head</code> on <code>basilisk.dat</code>
and pipes the first two lines to the <code>tail</code> command,
which then prints the second line of <code>basilisk.dat</code>.
For the second iteration, <code>$filename</code> becomes
<code>minotaur.dat</code>. This time, the shell runs <code>head</code> on <code>monotaur.dat</code>
and pipes the first two lines to the <code>tail</code> command,
which then prints the second line of <code>monotaur.dat</code>.
For the third iteration, <code>$filename</code> becomes
<code>unicorn.dat</code>, so the shell runs the <code>head</code> command on that file,
and <code>tail</code> on the output of that.
Since the list was only three items, the shell exits the <code>for</code> loop.</p>
<blockquote>
<h2><a id="user-content-same-symbols-different-meanings" class="anchor" aria-hidden="true" href="#same-symbols-different-meanings"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Same Symbols, Different Meanings</h2>
<p>Here we see <code>&gt;</code> being used a shell prompt, whereas <code>&gt;</code> is also
used to redirect output.
Similarly, <code>$</code> is used as a shell prompt, but, as we saw earlier,
it is also used to ask the shell to get the value of a variable.</p>
<p>If the <em>shell</em> prints <code>&gt;</code> or <code>$</code> then it expects you to type something,
and the symbol is a prompt.</p>
<p>If <em>you</em> type <code>&gt;</code> or <code>$</code> yourself, it is an instruction from you that
the shell should redirect output or get the value of a variable.
{: .callout}</p>
</blockquote>
<p>When using variables it is also
possible to put the names into curly braces to clearly delimit the variable
name: <code>$filename</code> is equivalent to <code>${filename}</code>, but is different from
<code>${file}name</code>. You may find this notation in other people's programs.</p>
<p>We have called the variable in this loop <code>filename</code>
in order to make its purpose clearer to human readers.
The shell itself doesn't care what the variable is called;
if we wrote this loop as:</p>
<pre><code>$ for x in basilisk.dat minotaur.dat unicorn.dat
&gt; do
&gt;    head -n 2 $x | tail -n 1
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>or:</p>
<pre><code>$ for temperature in basilisk.dat minotaur.dat unicorn.dat
&gt; do
&gt;    head -n 2 $temperature | tail -n 1
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>it would work exactly the same way.
<em>Don't do this.</em>
Programs are only useful if people can understand them,
so meaningless names (like <code>x</code>) or misleading names (like <code>temperature</code>)
increase the odds that the program won't do what its readers think it does.</p>
<blockquote>
<h2><a id="user-content-variables-in-loops" class="anchor" aria-hidden="true" href="#variables-in-loops"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Variables in Loops</h2>
<p>This exercise refers to the <code>data-shell/molecules</code> directory.
<code>ls</code> gives the following output:</p>
<pre><code>cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
</code></pre>
<p>{: .output}</p>
<p>What is the output of the following code?</p>
<pre><code>$ for datafile in *.pdb
&gt; do
&gt;    ls *.pdb
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>Now, what is the output of the following code?</p>
<pre><code>$ for datafile in *.pdb
&gt; do
&gt;	ls $datafile
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>Why do these two loops give different outputs?</p>
<blockquote>
<h2><a id="user-content-solution" class="anchor" aria-hidden="true" href="#solution"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>The first code block gives the same output on each iteration through
the loop.
Bash expands the wildcard <code>*.pdb</code> within the loop body (as well as
before the loop starts) to match all files ending in <code>.pdb</code>
and then lists them using <code>ls</code>.
The expanded loop would look like this:</p>
<pre><code>$ for datafile in cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
&gt; do
&gt;	ls cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<pre><code>cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb
</code></pre>
<p>{: .output}</p>
<p>The second code block lists a different file on each loop iteration.
The value of the <code>datafile</code> variable is evaluated using <code>$datafile</code>,
and then listed using <code>ls</code>.</p>
<pre><code>cubane.pdb
ethane.pdb
methane.pdb
octane.pdb
pentane.pdb
propane.pdb
</code></pre>
<p>{: .output}
{: .solution}
{: .challenge}</p>
</blockquote>
</blockquote>
<blockquote>
<h2><a id="user-content-limiting-sets-of-files" class="anchor" aria-hidden="true" href="#limiting-sets-of-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Limiting Sets of Files</h2>
<p>What would be the output of running the following loop in the <code>data-shell/molecules</code> directory?</p>
<pre><code>$ for filename in c*
&gt; do
&gt;    ls $filename
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<ol>
<li>No files are listed.</li>
<li>All files are listed.</li>
<li>Only <code>cubane.pdb</code>, <code>octane.pdb</code> and <code>pentane.pdb</code> are listed.</li>
<li>Only <code>cubane.pdb</code> is listed.</li>
</ol>
<blockquote>
<h2><a id="user-content-solution-1" class="anchor" aria-hidden="true" href="#solution-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>4 is the correct answer. <code>*</code> matches zero or more characters, so any file name starting with
the letter c, followed by zero or more other characters will be matched.
{: .solution}</p>
</blockquote>
<p>How would the output differ from using this command instead?</p>
<pre><code>$ for filename in *c*
&gt; do
&gt;    ls $filename
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<ol>
<li>The same files would be listed.</li>
<li>All the files are listed this time.</li>
<li>No files are listed this time.</li>
<li>The files <code>cubane.pdb</code> and <code>octane.pdb</code> will be listed.</li>
<li>Only the file <code>octane.pdb</code> will be listed.</li>
</ol>
<blockquote>
<h2><a id="user-content-solution-2" class="anchor" aria-hidden="true" href="#solution-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>4 is the correct answer. <code>*</code> matches zero or more characters, so a file name with zero or more
characters before a letter c and zero or more characters after the letter c will be matched.
{: .solution}
{: .challenge}</p>
</blockquote>
</blockquote>
<blockquote>
<h2><a id="user-content-saving-to-a-file-in-a-loop---part-one" class="anchor" aria-hidden="true" href="#saving-to-a-file-in-a-loop---part-one"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Saving to a File in a Loop - Part One</h2>
<p>In the <code>data-shell/molecules</code> directory, what is the effect of this loop?</p>
<pre><code>for alkanes in *.pdb
do
    echo $alkanes
    cat $alkanes &gt; alkanes.pdb
done
</code></pre>
<p>{: .language-bash}</p>
<ol>
<li>Prints <code>cubane.pdb</code>, <code>ethane.pdb</code>, <code>methane.pdb</code>, <code>octane.pdb</code>, <code>pentane.pdb</code> and <code>propane.pdb</code>,
and the text from <code>propane.pdb</code> will be saved to a file called <code>alkanes.pdb</code>.</li>
<li>Prints <code>cubane.pdb</code>, <code>ethane.pdb</code>, and <code>methane.pdb</code>, and the text from all three files would be
concatenated and saved to a file called <code>alkanes.pdb</code>.</li>
<li>Prints <code>cubane.pdb</code>, <code>ethane.pdb</code>, <code>methane.pdb</code>, <code>octane.pdb</code>, and <code>pentane.pdb</code>, and the text
from <code>propane.pdb</code> will be saved to a file called <code>alkanes.pdb</code>.</li>
<li>None of the above.</li>
</ol>
<blockquote>
<h2><a id="user-content-solution-3" class="anchor" aria-hidden="true" href="#solution-3"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<ol>
<li>The text from each file in turn gets written to the <code>alkanes.pdb</code> file.
However, the file gets overwritten on each loop interation, so the final content of <code>alkanes.pdb</code>
is the text from the <code>propane.pdb</code> file.
{: .solution}
{: .challenge}</li>
</ol>
</blockquote>
</blockquote>
<blockquote>
<h2><a id="user-content-saving-to-a-file-in-a-loop---part-two" class="anchor" aria-hidden="true" href="#saving-to-a-file-in-a-loop---part-two"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Saving to a File in a Loop - Part Two</h2>
<p>Also in the <code>data-shell/molecules</code> directory, what would be the output of the following loop?</p>
<pre><code>for datafile in *.pdb
do
    cat $datafile &gt;&gt; all.pdb
done
</code></pre>
<p>{: .language-bash}</p>
<ol>
<li>All of the text from <code>cubane.pdb</code>, <code>ethane.pdb</code>, <code>methane.pdb</code>, <code>octane.pdb</code>, and
<code>pentane.pdb</code> would be concatenated and saved to a file called <code>all.pdb</code>.</li>
<li>The text from <code>ethane.pdb</code> will be saved to a file called <code>all.pdb</code>.</li>
<li>All of the text from <code>cubane.pdb</code>, <code>ethane.pdb</code>, <code>methane.pdb</code>, <code>octane.pdb</code>, <code>pentane.pdb</code>
and <code>propane.pdb</code> would be concatenated and saved to a file called <code>all.pdb</code>.</li>
<li>All of the text from <code>cubane.pdb</code>, <code>ethane.pdb</code>, <code>methane.pdb</code>, <code>octane.pdb</code>, <code>pentane.pdb</code>
and <code>propane.pdb</code> would be printed to the screen and saved to a file called <code>all.pdb</code>.</li>
</ol>
<blockquote>
<h2><a id="user-content-solution-4" class="anchor" aria-hidden="true" href="#solution-4"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>3 is the correct answer. <code>&gt;&gt;</code> appends to a file, rather than overwriting it with the redirected
output from a command.
Given the output from the <code>cat</code> command has been redirected, nothing is printed to the screen.
{: .solution}
{: .challenge}</p>
</blockquote>
</blockquote>
<p>Let's continue with our example in the <code>data-shell/creatures</code> directory.
Here's a slightly more complicated loop:</p>
<pre><code>$ for filename in *.dat
&gt; do
&gt;     echo $filename
&gt;     head -n 100 $filename | tail -n 20
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>The shell starts by expanding <code>*.dat</code> to create the list of files it will process.
The <strong>loop body</strong>
then executes two commands for each of those files.
The first command, <code>echo</code>, prints its command-line arguments to standard output.
For example:</p>
<pre><code>$ echo hello there
</code></pre>
<p>{: .language-bash}</p>
<p>prints:</p>
<pre><code>hello there
</code></pre>
<p>{: .output}</p>
<p>In this case,
since the shell expands <code>$filename</code> to be the name of a file,
<code>echo $filename</code> prints the name of the file.
Note that we can't write this as:</p>
<pre><code>$ for filename in *.dat
&gt; do
&gt;     $filename
&gt;     head -n 100 $filename | tail -n 20
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>because then the first time through the loop,
when <code>$filename</code> expanded to <code>basilisk.dat</code>, the shell would try to run <code>basilisk.dat</code> as a program.
Finally,
the <code>head</code> and <code>tail</code> combination selects lines 81-100
from whatever file is being processed
(assuming the file has at least 100 lines).</p>
<blockquote>
<h2><a id="user-content-spaces-in-names" class="anchor" aria-hidden="true" href="#spaces-in-names"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Spaces in Names</h2>
<p>Spaces are used to separate the elements of the list
that we are going to loop over. If one of those elements
contains a space character, we need to surround it with
quotes, and do the same thing to our loop variable.
Suppose our data files are named:</p>
<pre><code>red dragon.dat
purple unicorn.dat
</code></pre>
<p>{: .source}</p>
<p>To loop over these files, we would need to add double quotes like so:</p>
<pre><code>$ for filename in "red dragon.dat" "purple unicorn.dat"
&gt; do
&gt;     head -n 100 "$filename" | tail -n 20
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>It is simpler to avoid using spaces (or other special characters) in filenames.</p>
<p>The files above don't exist, so if we run the above code, the <code>head</code> command will be unable
to find them, however the error message returned will show the name of the files it is
expecting:</p>
<pre><code>head: cannot open ‘red dragon.dat’ for reading: No such file or directory
head: cannot open ‘purple unicorn.dat’ for reading: No such file or directory
</code></pre>
<p>{: .output}
Try removing the quotes around <code>$filename</code> in the loop above to see the effect of the quote
marks on spaces. Note that we get a result from the loop command for unicorn.dat when we run this code in the <code>creatures</code> directory:</p>
<pre><code>head: cannot open ‘red’ for reading: No such file or directory
head: cannot open ‘dragon.dat’ for reading: No such file or directory
head: cannot open ‘purple’ for reading: No such file or directory
CGGTACCGAA
AAGGGTCGCG
CAAGTGTTCC
</code></pre>
<p>{: . output}
{: .callout}</p>
</blockquote>
<p>We would like to modify each of the files in <code>data-shell/creatures</code>, but also save a version
of the original files, naming the copies <code>original-basilisk.dat</code> and <code>original-unicorn.dat</code>.
We can't use:</p>
<pre><code>$ cp *.dat original-*.dat
</code></pre>
<p>{: .language-bash}</p>
<p>because that would expand to:</p>
<pre><code>$ cp basilisk.dat minotaur.dat unicorn.dat original-*.dat
</code></pre>
<p>{: .language-bash}</p>
<p>This wouldn't back up our files, instead we get an error:</p>
<pre><code>cp: target `original-*.dat' is not a directory
</code></pre>
<p>{: .error}</p>
<p>This problem arises when <code>cp</code> receives more than two inputs. When this happens, it
expects the last input to be a directory where it can copy all the files it was passed.
Since there is no directory named <code>original-*.dat</code> in the <code>creatures</code> directory we get an
error.</p>
<p>Instead, we can use a loop:</p>
<pre><code>$ for filename in *.dat
&gt; do
&gt;     cp $filename original-$filename
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>This loop runs the <code>cp</code> command once for each filename.
The first time,
when <code>$filename</code> expands to <code>basilisk.dat</code>,
the shell executes:</p>
<pre><code>cp basilisk.dat original-basilisk.dat
</code></pre>
<p>{: .language-bash}</p>
<p>The second time, the command is:</p>
<pre><code>cp minotaur.dat original-minotaur.dat
</code></pre>
<p>{: .language-bash}</p>
<p>The third and last time, the command is:</p>
<pre><code>cp unicorn.dat original-unicorn.dat
</code></pre>
<p>{: .language-bash}</p>
<p>Since the <code>cp</code> command does not normally produce any output, it's hard to check
that the loop is doing the correct thing.
However, we learned earlier how to print strings using <code>echo</code>, and we can modify the loop
to use <code>echo</code> to print our commands without actually executing them.
As such we can check what commands <em>would be</em> run in the unmodified loop.</p>
<p>The following diagram
shows what happens when the modified loop is executed, and demonstrates how the
judicious use of <code>echo</code> is a good debugging technique.</p>
<p><a target="_blank" rel="noopener noreferrer" href="/swcarpentry/shell-novice/blob/gh-pages/fig/shell_script_for_loop_flow_chart.svg"><img src="/swcarpentry/shell-novice/raw/gh-pages/fig/shell_script_for_loop_flow_chart.svg?sanitize=true" alt="For Loop in Action" style="max-width:100%;"></a></p>
<h2><a id="user-content-nelles-pipeline-processing-files" class="anchor" aria-hidden="true" href="#nelles-pipeline-processing-files"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Nelle's Pipeline: Processing Files</h2>
<p>Nelle is now ready to process her data files using <code>goostats</code> --- a shell script written by her supervisor.
This calculates some statistics from a protein sample file, and takes two arguments:</p>
<ol>
<li>an input file (containing the raw data)</li>
<li>an output file (to store the calculated statistics)</li>
</ol>
<p>Since she's still learning how to use the shell,
she decides to build up the required commands in stages.
Her first step is to make sure that she can select the right input files --- remember,
these are ones whose names end in 'A' or 'B', rather than 'Z'. Starting from her home directory, Nelle types:</p>
<pre><code>$ cd north-pacific-gyre/2012-07-03
$ for datafile in NENE*[AB].txt
&gt; do
&gt;     echo $datafile
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<pre><code>NENE01729A.txt
NENE01729B.txt
NENE01736A.txt
...
NENE02043A.txt
NENE02043B.txt
</code></pre>
<p>{: .output}</p>
<p>Her next step is to decide
what to call the files that the <code>goostats</code> analysis program will create.
Prefixing each input file's name with 'stats' seems simple,
so she modifies her loop to do that:</p>
<pre><code>$ for datafile in NENE*[AB].txt
&gt; do
&gt;     echo $datafile stats-$datafile
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<pre><code>NENE01729A.txt stats-NENE01729A.txt
NENE01729B.txt stats-NENE01729B.txt
NENE01736A.txt stats-NENE01736A.txt
...
NENE02043A.txt stats-NENE02043A.txt
NENE02043B.txt stats-NENE02043B.txt
</code></pre>
<p>{: .output}</p>
<p>She hasn't actually run <code>goostats</code> yet,
but now she's sure she can select the right files and generate the right output filenames.</p>
<p>Typing in commands over and over again is becoming tedious,
though,
and Nelle is worried about making mistakes,
so instead of re-entering her loop,
she presses the up arrow.
In response,
the shell redisplays the whole loop on one line
(using semi-colons to separate the pieces):</p>
<pre><code>$ for datafile in NENE*[AB].txt; do echo $datafile stats-$datafile; done
</code></pre>
<p>{: .language-bash}</p>
<p>Using the left arrow key,
Nelle backs up and changes the command <code>echo</code> to <code>bash goostats</code>:</p>
<pre><code>$ for datafile in NENE*[AB].txt; do bash goostats $datafile stats-$datafile; done
</code></pre>
<p>{: .language-bash}</p>
<p>When she presses <kbd>Enter</kbd>,
the shell runs the modified command.
However, nothing appears to happen --- there is no output.
After a moment, Nelle realizes that since her script doesn't print anything to the screen any longer,
she has no idea whether it is running, much less how quickly.
She kills the running command by typing <code>Ctrl-C</code>,
uses up-arrow to repeat the command,
and edits it to read:</p>
<pre><code>$ for datafile in NENE*[AB].txt; do echo $datafile; bash goostats $datafile stats-$datafile; done
</code></pre>
<p>{: .language-bash}</p>
<blockquote>
<h2><a id="user-content-beginning-and-end" class="anchor" aria-hidden="true" href="#beginning-and-end"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Beginning and End</h2>
<p>We can move to the beginning of a line in the shell by typing <code>Ctrl-a</code>
and to the end using <code>Ctrl-e</code>.
{: .callout}</p>
</blockquote>
<p>When she runs her program now,
it produces one line of output every five seconds or so:</p>
<pre><code>NENE01729A.txt
NENE01729B.txt
NENE01736A.txt
...
</code></pre>
<p>{: .output}</p>
<p>1518 times 5 seconds,
divided by 60,
tells her that her script will take about two hours to run.
As a final check,
she opens another terminal window,
goes into <code>north-pacific-gyre/2012-07-03</code>,
and uses <code>cat stats-NENE01729B.txt</code>
to examine one of the output files.
It looks good,
so she decides to get some coffee and catch up on her reading.</p>
<blockquote>
<h2><a id="user-content-those-who-know-history-can-choose-to-repeat-it" class="anchor" aria-hidden="true" href="#those-who-know-history-can-choose-to-repeat-it"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Those Who Know History Can Choose to Repeat It</h2>
<p>Another way to repeat previous work is to use the <code>history</code> command to
get a list of the last few hundred commands that have been executed, and
then to use <code>!123</code> (where '123' is replaced by the command number) to
repeat one of those commands. For example, if Nelle types this:</p>
<pre><code>$ history | tail -n 5
</code></pre>
<p>{: .language-bash}</p>
<pre><code>  456  ls -l NENE0*.txt
  457  rm stats-NENE01729B.txt.txt
  458  bash goostats NENE01729B.txt stats-NENE01729B.txt
  459  ls -l NENE0*.txt
  460  history
</code></pre>
<p>{: .output}</p>
<p>then she can re-run <code>goostats</code> on <code>NENE01729B.txt</code> simply by typing
<code>!458</code>.
{: .callout}</p>
</blockquote>
<blockquote>
<h2><a id="user-content-other-history-commands" class="anchor" aria-hidden="true" href="#other-history-commands"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Other History Commands</h2>
<p>There are a number of other shortcut commands for getting at the history.</p>
<ul>
<li><code>Ctrl-R</code> enters a history search mode 'reverse-i-search' and finds the
most recent command in your history that matches the text you enter next.
Press <code>Ctrl-R</code> one or more additional times to search for earlier matches.</li>
<li><code>!!</code> retrieves the immediately preceding command
(you may or may not find this more convenient than using the up-arrow)</li>
<li><code>!$</code> retrieves the last word of the last command.
That's useful more often than you might expect: after
<code>bash goostats NENE01729B.txt stats-NENE01729B.txt</code>, you can type
<code>less !$</code> to look at the file <code>stats-NENE01729B.txt</code>, which is
quicker than doing up-arrow and editing the command-line.
{: .callout}</li>
</ul>
</blockquote>
<blockquote>
<h2><a id="user-content-doing-a-dry-run" class="anchor" aria-hidden="true" href="#doing-a-dry-run"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Doing a Dry Run</h2>
<p>A loop is a way to do many things at once --- or to make many mistakes at
once if it does the wrong thing. One way to check what a loop <em>would</em> do
is to <code>echo</code> the commands it would run instead of actually running them.</p>
<p>Suppose we want to preview the commands the following loop will execute
without actually running those commands:</p>
<pre><code>$ for file in *.pdb
&gt; do
&gt;   analyze $file &gt; analyzed-$file
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<p>What is the difference between the two loops below, and which one would we
want to run?</p>
<pre><code># Version 1
$ for file in *.pdb
&gt; do
&gt;   echo analyze $file &gt; analyzed-$file
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<pre><code># Version 2
$ for file in *.pdb
&gt; do
&gt;   echo "analyze $file &gt; analyzed-$file"
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<blockquote>
<h2><a id="user-content-solution-5" class="anchor" aria-hidden="true" href="#solution-5"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>The second version is the one we want to run.
This prints to screen everything enclosed in the quote marks, expanding the
loop variable name because we have prefixed it with a dollar sign.</p>
<p>The first version redirects the output from the command <code>echo analyze $file</code> to
a file, <code>analyzed-$file</code>. A series of files is generated: <code>analyzed-cubane.pdb</code>,
<code>analyzed-ethane.pdb</code> etc.</p>
<p>Try both versions for yourself to see the output! Be sure to open the
<code>analyzed-*.pdb</code> files to view their contents.
{: .solution}
{: .challenge}</p>
</blockquote>
</blockquote>
<blockquote>
<h2><a id="user-content-nested-loops" class="anchor" aria-hidden="true" href="#nested-loops"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Nested Loops</h2>
<p>Suppose we want to set up up a directory structure to organize
some experiments measuring reaction rate constants with different compounds
<em>and</em> different temperatures.  What would be the
result of the following code:</p>
<pre><code>$ for species in cubane ethane methane
&gt; do
&gt;     for temperature in 25 30 37 40
&gt;     do
&gt;         mkdir $species-$temperature
&gt;     done
&gt; done
</code></pre>
<p>{: .language-bash}</p>
<blockquote>
<h2><a id="user-content-solution-6" class="anchor" aria-hidden="true" href="#solution-6"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Solution</h2>
<p>We have a nested loop, i.e. contained within another loop, so for each species
in the outer loop, the inner loop (the nested loop) iterates over the list of
temperatures, and creates a new directory for each combination.</p>
<p>Try running the code for yourself to see which directories are created!
{: .solution}
{: .challenge}</p>
</blockquote>
</blockquote>
</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>

    <div class="Popover anim-scale-in js-tagsearch-popover"
     hidden
     data-tagsearch-url="/swcarpentry/shell-novice/find-symbols"
     data-tagsearch-ref="gh-pages"
     data-tagsearch-path="_episodes/05-loop.md"
     data-tagsearch-lang="Markdown"
     data-hydro-click="{&quot;event_type&quot;:&quot;code_navigation.click_on_symbol&quot;,&quot;payload&quot;:{&quot;action&quot;:&quot;click_on_symbol&quot;,&quot;repository_id&quot;:25592861,&quot;ref&quot;:&quot;gh-pages&quot;,&quot;language&quot;:&quot;Markdown&quot;,&quot;client_id&quot;:&quot;596265541.1570646780&quot;,&quot;originating_request_id&quot;:&quot;C5EF:3C2D:A3CDE63:A84A61A:5DF02866&quot;,&quot;originating_url&quot;:&quot;https://github.com/swcarpentry/shell-novice/blob/gh-pages/_episodes/05-loop.md&quot;,&quot;referrer&quot;:&quot;https://github.com/swcarpentry/shell-novice/tree/gh-pages/_episodes&quot;,&quot;user_id&quot;:12768545}}"
     data-hydro-click-hmac="4680bb8a86712c7fb2da0563c6ad2c5dab720c217fcbad2bf9ee343554ecb209">
  <div class="Popover-message Popover-message--large Popover-message--top-left TagsearchPopover mt-1 mb-4 mx-auto Box box-shadow-large">
    <div class="TagsearchPopover-content js-tagsearch-popover-content overflow-auto" style="will-change:transform;">
    </div>
  </div>
</div>



  </div>
</div>

    </main>
  </div>
  

  </div>

        
<div class="footer container-lg width-full p-responsive" role="contentinfo">
  <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light ">
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
      <li class="mr-3 mr-lg-0">&copy; 2019 GitHub, Inc.</li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:help" href="https://help.github.com">Help</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon d-none d-lg-block mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
   <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>

    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 000 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 00.01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
    </button>
    You can’t perform that action at this time.
  </div>


    
    <script crossorigin="anonymous" integrity="sha512-70iNd/Gg+yLXPhfcelP5Zr8W3AA2fp2GsH2O/ZLbKoNOS51UGEKF/twbq+aS7x15R9F80cENGrgErdVG5frxqQ==" type="application/javascript" src="https://github.githubassets.com/assets/frameworks-ef488d77.js"></script>
    
    <script crossorigin="anonymous" async="async" integrity="sha512-zfhpmK5/eY3WaaOaHic6RIaeUtntjJbHUILU6uv3gFglx3Tfeyu3Y880GgCNhblT3TT3+jbXVNBiVLoli3eq7Q==" type="application/javascript" src="https://github.githubassets.com/assets/github-bootstrap-cdf86998.js"></script>
    
    
    
  <div class="js-stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 000 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 00.01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <span class="js-stale-session-flash-signed-in" hidden>You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="js-stale-session-flash-signed-out" hidden>You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark hx_rsm" open>
    <summary role="button" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast hx_rsm-dialog hx_rsm-modal">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

  <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>

  <div aria-live="polite" class="js-global-screen-reader-notice sr-only"></div>

  </body>
</html>

