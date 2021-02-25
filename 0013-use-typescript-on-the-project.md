# 13. Use TypeScript on the project

Date: 2021-02-25

## Status

In discussion

## Context

While the whole JavaScript community welcome TypeScript easily, our project JS is not typed at all. In order to improve the maintainability of the project and use latest TC39 features, a good idea would be to use TypeScript.

What would benefit the project of using it :
- Detect bugs before sending PRs, TypeScript users says that globally, it permit to detect around 15% of bugs that you would detect by testing.
- Use latest features such as Optional Chaining, Tuples and Records... really early.
- Types are increasing the quality of the project, because we would be able to detect dangerous changes, related bugs... If we use it on PHP side, why don't we use types while using JS ?
- Vue 3 offered a new API : Composition API, this one is pretty easy to use with TypeScript as it's mainly functional programming instead of opiniated APIs of Vue, that would be a good moove to preshot the Vue update in the BO.

## Decision

Add the possibility to transpile ts files inside every js folders of the project with webpack.

[Here is a POC](https://github.com/PrestaShop/PrestaShop/pull/23221) of basically using TypeScript on a small part of the PrestaShop Grid system.

## Consequences

It's a bit more difficult if you're not used to develop with types, it will probably require a bit of time for contributors which are not used to work with TS, but almost every known projects are refactoring their JS with TS, it's beginning to be a must have on maintained projects. 

The worst scenario would be that JS contributors almost stop to contribute because of a lack of knowledge, but we've not much JS contributions for the moment and I doubt this is a big risk.