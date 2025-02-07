# Storybook

## About storybook

Storybook is used to create reusable component libraries that you can deploy to the web to re use the components in later projects. An example of a completed storybook is this one by
[Grafana Labs](https://developers.grafana.com/ui/latest/index.html?path=/story/docs-overview-intro--page).

We understand not everyone will want to learn the extra overhead of storybook. We included it in this template because we believe the principles of [atomic design](https://bradfrost.com/blog/post/atomic-web-design/) are important. Creating component libraries with storybook allows you to create components once that you can re use anywhere which we believe will be essential to the Terra Developer ecosystem as professional teams continue to scale.

## Get started with storybook

If you are interested in learning more about storybook you can start with the introductory guide [here](https://storybook.js.org/docs/react/get-started/whats-a-story)

## Storybook Testing

Storybook allows us to write less Unit and Integration tests as we can replace them with interaction tests directly within storybook.
[Here](https://storybook.js.org/blog/test-component-interactions-with-storybook/) and [here](https://storybook.js.org/blog/testing-component-interactions/) are 2 different blog posts from the storybook team about how to run interaction testing

## Remove storybook

Feel free to remove storybook if you decide it isn't for you.
[This answer](https://stackoverflow.com/questions/68062232/how-to-remove-storybook-from-the-react-project) on stack overflow explains the process.

1. Remove `.storybook` directory
2. Remove `src/stories/`
3. Within `"scripts"` in `package.json`, remove 2 scripts related to storybook

```
"storybook": "start-storybook -p 6006 -s public",
"build-storybook": "build-storybook -s public"
```

4. under `"devDependencies"` in `package.json` remove these devDependencies related to storybook.

```
    "@storybook/addon-actions": "^6.4.19",
    "@storybook/addon-essentials": "^6.4.19",
    "@storybook/addon-interactions": "^6.4.19",
    "@storybook/addon-links": "^6.4.19",
    "@storybook/builder-webpack5": "^6.4.19",
    "@storybook/manager-webpack5": "^6.4.19",
    "@storybook/node-logger": "^6.4.19",
    "@storybook/preset-create-react-app": "^4.0.1",
    "@storybook/react": "^6.4.19",
    "@storybook/testing-library": "^0.0.9",
    ...
    "eslint-plugin-storybook": "^0.5.7",

```

5. In the `.eslintrc.json` file remove `"plugin:storybook/recommended"` from the `extends` list
6. Run yarn install to update your yarn.lock file

## Extra Storybook resources

This is a list of links I consistently use to help me with storybook development.

- [Repo for interaction testing addon](https://github.com/storybookjs/storybook/blob/next/addons/interactions/README.md)

- [Documenting with mdx article](https://levelup.gitconnected.com/documenting-design-systems-with-storybook-docs-e54b2fa5203)
- [Official docs about writing docs](https://storybook.js.org/docs/react/writing-docs/docs-page)
- [Doc Blocks in GitHub](https://github.com/storybookjs/storybook/tree/main/addons/docs/src/blocks)
- [Official docs for themes](https://storybook.js.org/docs/react/configure/theming)
- [Setting up dark mode](https://www.npmjs.com/package/storybook-dark-mode)
- [Naming and sorting components in storybook](https://storybook.js.org/docs/react/writing-stories/naming-components-and-hierarchy)
- [Custom Gist from storybook Maintainer for creating mobile view in docs](https://gist.github.com/kylegach/c529189196258a3c98cc8f2bfbd3c50b)
