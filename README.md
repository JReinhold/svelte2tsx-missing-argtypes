Reproduction for `svelte2tsx@0.7.35` breaking arg types inference in Storybook.

To reproduce:

1. `npm install`
2. `npm run storybook`
3. Navigate to `http://localhost/?path=/story/stories-docs-ts--default`
4. You should see rows in the Controls panel at the bottom, but it is empty

(Storybook Dev with Svelte doesn't work for me right now, so you can also debug with the built Storybook instead):

1. `npm install`
2. `npm run build-storybook`
3. `npx http-serve storybook-static -c-1h`
4. ... same as above

Add the following to `package.json` and re-do the reproduction steps to see it now working correctly:

```json
  "overrides": {
    "svelte2tsx": "0.7.34"
  }
```
