# @afc/vue-tailwind

![version](https://img.shields.io/badge/version-0.1.0-blue.svg) ![license](https://img.shields.io/badge/license-MIT-blue.svg) <a href="https://github.com/afc-org/vue-tailwind/issues?q=is%3Aopen+is%3Aissue" target="_blank">![GitHub issues open](https://img.shields.io/github/issues/@afc/vue-tailwind.svg)</a> <a href="https://github.com/afc-org/vue-tailwind?q=is%3Aissue+is%3Aclosed" target="_blank">![GitHub issues closed](https://img.shields.io/github/issues-closed-raw/@afc/vue-tailwind.svg)</a>

<div align="center"><img src="./assets/logos/vuejs-tailwind-logo.png" alt="@afc/vue-tailwind" width="300"/></div>

### A dynamic plugin extension for TailwindCSS.

**@afc/vue-tailwind** is Free and Open Source. It does not change or add any CSS to the already one from TailwindCSS, It comes with code written with VueJS as an extension to TailwindCSS for you to have dynamic components inside your app as well.

### Components

It comes with 8 dynamic components, that any website needs.
We plan on implementing more, in the weeks to come.


## Table of Contents

* [Versions](#versions)
* [Components](#components)
* [Quick Start](#quick-start)
* [Documentation](#documentation)
* [Dependencies](#dependencies)
* [Browser Support](#browser-support)
* [Reporting Issues](#reporting-issues)
* [Licensing](#licensing)
* [Resources](#resources)

## Versions

|Angular|JavaScript|React|Svelte|VueJS|
| --- | --- | --- | --- | --- |
| <a href="https://github.com/afc-org/angular-tailwind" target="_blank">![Check Angular](./assets/logos/angular-tailwind-logo.png)</a>  | <a href="https://github.com/afc-org/js-tailwind" target="_blank">![Check JavaScript](./assets/logos/javascript-tailwind-logo.png)</a>  | <a href="https://github.com/afc-org/react-tailwind" target="_blank">![Check React](./assets/logos/reactjs-tailwind-logo.png)</a>  | <a href="https://github.com/afc-org/svelte-tailwind" target="_blank">![Check Svelte](./assets/logos/svelte-tailwind-logo.png)</a>    | <a href="https://github.com/afc-org/vue-tailwind" target="_blank">![Check VueJS](./assets/logos/vuejs-tailwind-logo.png)</a>|

## Components

- Alert
- Dropdown (PopperJS)
- Responsive Menu
- Modal
- Responsive Navbar
- Popover (PopperJS)
- Tooltip (PopperJS)
- Tab Pills

## Quick start

```
npm i -E @afc/vue-tailwind
```

## Documentation - VueJS

After you have installed `@afc/vue-tailwind` into your project, you can import and use our components like so:

```
<template>
  <div>
      <tw-alert>Default</tw-alert>
  </div>
</template>
<script>
  import { TwAlert } from "@afc/vue-tailwind";
  // or direct import
  // import TwAlert from "@afc/vue-tailwind/TwAlert";
  export default {
    name: "YourComponentName"
  }
</script>
```

### Styles

Do not forget that you will need to either get a compiled version of TailwindCSS, or to compile your own version, but one that will have the following classes from TailwindCSS:
```
px-5 py-3 border border-solid rounded relative mb-4 absolute bg-transparent text-2xl font-semibold leading-none right-0 top-0 outline-none focus:outline-none opacity-50 hover:opacity-75 hover:text-black text-xl inline-block mr-5 align-middle mr-8 bg-indigo-200 text-indigo-800 border-indigo-300 bg-gray-300 text-gray-800 border-gray-400 bg-green-200 text-green-800 border-green-300 bg-red-200 text-red-800 border-red-300 bg-orange-200 text-orange-800 border-orange-300 bg-blue-200 text-blue-800 border-blue-300 bg-white text-gray-600 border-gray-100 bg-gray-400 border-gray-500 left-0 z-50 hidden py-2 text-base text-left list-none mt-1 mb-1 mr-1 ml-1 block w-full py-1 px-6 clear-both font-normal whitespace-no-wrap border-0 hover:text-gray-900 hover:bg-gray-100 active:text-white active:bg-blue-500 text-white bg-blue-500 text-gray-400 pointer-events-none mb-2 flex flex-wrap items-center bg-gray-600 justify-between px-4 bg-blue-600 container mx-auto lg:px-4 px-0 capitalize mr-4 leading-relaxed ml-auto cursor-pointer px-3 text-gray-300 lg:hidden lg:flex lg:w-auto flex-grow lg:items-center lg:ml-auto pl-0 mb-0 flex-col lg:flex-row px-2 no-underline mb-3 leading-normal text-sm break-words text-center bg-black mr-2 ml-2 bg-green-600 bg-red-600 bg-yellow-500 bg-teal-500 bg-gray-100 text-gray-900 text-black bg-gray-800 -mb-px flex-auto text-blue-600 hover:text-blue-700 cursor-default rounded-t border-transparent border-b-0 border-b border-gray-200 sm:flex-row md:flex-row xl:flex-row navbar-expand sm:hidden md:hidden xl:hidden p-4 pointer-events-auto border-gray-600 transition-transform duration-300 ease-out w-auto m-2 sm:my-8 sm:mx-auto transform -translate-y-1 sm:max-w-xs md:max-w-screen-md lg:max-w-screen-lg sm:max-w-screen-sm justify-end p-3 border-t border-gray-300 rounded-b items-start opacity-0 fixed h-full overflow-hidden transition-opacity duration-75 ease-linear font-medium leading-tight mb-3mr-3 ml-3 mt-3
```
If you use `purge`, `postcss-purgecss`, `postcss` or any other tool to delete unused `css`, you can add the following array into your ignore (i.e. keep classes / whitelist etc.):
```
["px-5","py-3","border","border-solid","rounded","relative","mb-4","absolute","bg-transparent","text-2xl","font-semibold","leading-none","right-0","top-0","outline-none","focus:outline-none","opacity-50","hover:opacity-75","hover:text-black","text-xl","inline-block","mr-5","align-middle","mr-8","bg-indigo-200","text-indigo-800","border-indigo-300","bg-gray-300","text-gray-800","border-gray-400","bg-green-200","text-green-800","border-green-300","bg-red-200","text-red-800","border-red-300","bg-orange-200","text-orange-800","border-orange-300","bg-blue-200","text-blue-800","border-blue-300","bg-white","text-gray-600","border-gray-100","bg-gray-400","border-gray-500","left-0","z-50","hidden","py-2","text-base","text-left","list-none","mt-1","mb-1","mr-1","ml-1","block","w-full","py-1","px-6","clear-both","font-normal","whitespace-no-wrap","border-0","hover:text-gray-900","hover:bg-gray-100","active:text-white","active:bg-blue-500","text-white","bg-blue-500","text-gray-400","pointer-events-none","mb-2","flex","flex-wrap","items-center","bg-gray-600","justify-between","px-4","bg-blue-600","container","mx-auto","lg:px-4","px-0","capitalize","mr-4","leading-relaxed","ml-auto","cursor-pointer","px-3","text-gray-300","lg:hidden","lg:flex","lg:w-auto","flex-grow","lg:items-center","lg:ml-auto","pl-0","mb-0","flex-col","lg:flex-row","px-2","no-underline","mb-3","leading-normal","text-sm","break-words","text-center","bg-black","mr-2","ml-2","bg-green-600","bg-red-600","bg-yellow-500","bg-teal-500","bg-gray-100","text-gray-900","text-black","bg-gray-800","-mb-px","flex-auto","text-blue-600","hover:text-blue-700","cursor-default","rounded-t","border-transparent","border-b-0","border-b","border-gray-200","sm:flex-row","md:flex-row","xl:flex-row","navbar-expand","sm:hidden","md:hidden","xl:hidden","p-4","pointer-events-auto","border-gray-600","transition-transform","duration-300","ease-out","w-auto","m-2","sm:my-8","sm:mx-auto","transform","-translate-y-1","sm:max-w-xs","md:max-w-screen-md","lg:max-w-screen-lg","sm:max-w-screen-sm","justify-end","p-3","border-t","border-gray-300","rounded-b","items-start","opacity-0","fixed","h-full","overflow-hidden","transition-opacity","duration-75","ease-linear","font-medium","leading-tight","mb-3mr-3","ml-3","mt-3"]
```
Then, you can import your styles inside your `index.js` file (mounting js file for your app) like so:
```
import "path/to/your/tailwindcss/compiled/styles.css";
```
**NOTE**: alternatively, you can leave the components without any TailwindCSS styling code and render only HTML.

## Dependencies - VueJS

**@afc/vue-tailwind** to properly work needs the following dependencies:
- **@popperjs/core**@2.2.1
- **vue**@2.6.11
```
npm i -E @popperjs/core@2.2.1 vue@2.6.11
```

## Browser Support

At present, we officially aim to support the last two versions of the following browsers:

| Chrome | Firefox | Edge | Safari | Opera |
|:---:|:---:|:---:|:---:|:---:|
| <img src="./assets/logos/chrome-logo.png" width="64" height="64"> | <img src="./assets/logos/firefox-logo.png" width="64" height="64"> | <img src="./assets/logos/edge-logo.png" width="64" height="64"> | <img src="./assets/logos/safari-logo.png" width="64" height="64"> | <img src="./assets/logos/opera-logo.png" width="64" height="64"> |

## Reporting Issues

We use GitHub Issues as the official bug tracker for the Angular Landing Page. Here are some advices for our users that want to report an issue:

1. Make sure that you are using the latest version of the @afc/vue-tailwind.
2. Providing us reproducible steps for the issue will shorten the time it takes for it to be fixed.
3. Some issues may be browser specific, so specifying in what browser you encountered the issue might help.

## Contributors
This project exists thanks to all the people who contribute. [[Contribute](CONTRIBUTING.md)].

## Licensing

- Copyright 2020 @afc/vue-tailwind

- Licensed under <a href="https://github.com/afc-org/vue-tailwind/blob/master/LICENSE.md" target="_blank">MIT</a>

## Resources
- AFC-ORG projects: <a href="https://github.com/afc-org/" target="_blank">https://github.com/afc-org/</a>
- JavaScript & TailwindCSS: <a href="https://github.com/afc-org/js-tailwind" target="_blank">https://github.com/afc-org/js-tailwind</a>
- Angular & TailwindCSS: <a href="https://github.com/afc-org/angular-tailwind" target="_blank">https://github.com/afc-org/angular-tailwind</a>
- React & TailwindCSS: <a href="https://github.com/afc-org/angular-tailwind" target="_blank">https://github.com/afc-org/react-tailwind</a>
- Svelte & TailwindCSS: <a href="https://github.com/afc-org/angular-tailwind" target="_blank">https://github.com/afc-org/svelte-tailwind</a>
- VueJS & TailwindCSS:  <a href="https://github.com/afc-org/angular-tailwind" target="_blank">https://github.com/afc-org/vue-tailwind</a>
- Issues: <a href="https://github.com/afc-org/vue-tailwind/issues" target="_blank">Github Issues Page</a>
