# Svelte x ETS x Chota x Feather Starter 

This Starters recipe:

  + Svelte
  + Easy Toggle State
  + Chota
  + Svelte-Chota (ui component kit for svelte)
  + Svelte Feather Icons 

  writing and scripting style switching feel like natural HTML. Easy Toggle JS s a great, minimal library which gives elements toggle-able attributes, without having to write any JS orselves! Check out the starter on Glitch to see exactly how it works. I think it extends svelte very well as it makes our styles and markup feel more integrated while leaving alllll of  th data logic to svelte/js.
  
## Shout-out 

  All of the credit goes to the maintainers of these awesome libraries! Make sure to star their projects. Its only because of them that this awesome DX is possible.
  
  Note: This is not a minimal or bullet proof starter per say, just an experiment in how DX can be improved on the front-end with readily available, fairly minimal tools. At the moment the ETS package seems to be incompatible with HMR livereload (like snowpack), and actual page refresh is required to reload the page and init ETS.
  
## Get Started

git clone this repo and npm install just like the official starter. 

npm run dev, and then be sure to RTFM's of each package to see exactly how it works !

## On Glitch

Remix this app on Glitch and you should be ready to go!

When the Glitch runs `npm run build`, this app uses rollup to package everything.

When `npm run start` is run, this app uses [sirv](https://github.com/lukeed/sirv) to serve the static site.


## Single-page app mode

By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
`
