# SvelteKit CSP bug repro

Steps to reproduce in isolation

1) `npm create svelte@latest my-app`
2) `cd my-app`
3) `npm install`
4) `npm add @svelte/adapter-node`
5) Edit `svelte.config.js`
6) Replace auto adapter with `adapter-node`
6) Add `kit.csp.directives` for `style-src` with `'unsafe-inline'`
7) Add `kit.inlineStyleThreshold` with a value of e.g. `5 * 1024`
8) `npm run build`
9) `node build`
10) Open the webpage (`http://localhost:3000`) in your browser
11) Check console for errors

Steps to reproduce in this repo

1) `git clone https://github.com/lietu/sveltekit-csp-demo`
2) `cd sveltekit-csp-demo`
3) `npm install`
4) `npm run build`
5) `node build`
6) Open the webpage (`http://localhost:3000`) in your browser
7) Check console for errors
