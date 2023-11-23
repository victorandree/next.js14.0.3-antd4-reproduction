# Demonstration of antd@4 and Next.js 14.0.3 issue

When trying to use `antd@4.x` with Next.js 14.0.3, the project fails to build. This app demonstrates the bug.

```shell
$ npm run build

> build
> next build

 ✓ Linting and checking validity of types
   ▲ Next.js 14.0.4-canary.11

 ✓ Creating an optimized production build
 ✓ Compiled successfully
   Collecting page data  ./next.js14.0.3-antd4-reproduction/node_modules/antd/es/spin/index.js:1
import _extends from "@babel/runtime/helpers/esm/extends";
^^^^^^

SyntaxError: Cannot use import statement outside a module
    at internalCompileFunction (node:internal/vm:73:18)
    at wrapSafe (node:internal/modules/cjs/loader:1153:20)
    at Module._compile (node:internal/modules/cjs/loader:1197:27)
    at Module._extensions..js (node:internal/modules/cjs/loader:1287:10)
    at Module.load (node:internal/modules/cjs/loader:1091:32)
    at Module._load (node:internal/modules/cjs/loader:938:12)
    at Module.require (node:internal/modules/cjs/loader:1115:19)
    at mod.require (/next.js14.0.3-antd4-reproduction/node_modules/next/dist/server/require-hook.js:65:28)
    at require (node:internal/modules/helpers:130:18)
    at 9 (/next.js14.0.3-antd4-reproduction/.next/server/pages/index.js:1:742)

> Build error occurred
Error: Failed to collect page data for /
    at /next.js14.0.3-antd4-reproduction/node_modules/next/dist/build/utils.js:1217:15
    at process.processTicksAndRejections (node:internal/process/task_queues:95:5) {
  type: 'Error'
}
```

## Getting Started

These are the steps you should follow when creating a bug report:

- Bug reports must be verified against the `next@canary` release. The canary version of Next.js ships daily and includes all features and fixes that have not been released to the stable version yet. Think of canary as a public beta. Some issues may already be fixed in the canary version, so please verify that your issue reproduces before opening a new issue. Issues not verified against `next@canary` will be closed after 30 days.
- Make sure your issue is not a duplicate. Use the [GitHub issue search](https://github.com/vercel/next.js/issues) to see if there is already an open issue that matches yours. If that is the case, upvoting the other issue's first comment is desireable as we often prioritize issues based on the number of votes they receive. Note: Adding a "+1" or "same issue" comment without adding more context about the issue should be avoided. If you only find closed related issues, you can link to them using the issue number and `#`, eg.: `I found this related issue: #3000`.
- If you think the issue is not in Next.js, the best place to ask for help is our [Discord community](https://nextjs.org/discord) or [GitHub discussions](https://github.com/vercel/next.js/discussions). Our community is welcoming and can often answer a project-related question faster than the Next.js core team.
- Make the reproduction as minimal as possible. Try to exclude any code that does not help reproducing the issue. E.g. if you experience problems with Routing, including ESLint configurations or API routes aren't necessary. The less lines of code is to read through, the easier it is for the Next.js team to investigate. It may also help catching bugs in your codebase before publishing an issue.

## How to use this template

Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init), [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/), or [pnpm](https://pnpm.io) to bootstrap the example:

```bash
npx create-next-app --example reproduction-template-pages reproduction-app
```

```bash
yarn create next-app --example reproduction-template-pages reproduction-app
```

```bash
pnpm create next-app --example reproduction-template-pages reproduction-app
```

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
- [How to Contribute to Open Source (Next.js)](https://www.youtube.com/watch?v=cuoNzXFLitc) - a video tutorial by Lee Robinson
- [Triaging in the Next.js repository](https://github.com/vercel/next.js/blob/canary/contributing.md#triaging) - how we work on issues
- [CodeSandbox](https://codesandbox.io/s/github/vercel/next.js/tree/canary/examples/reproduction-template-pages) - Edit this repository on CodeSandbox

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deployment

If your reproduction needs to be deployed, the easiest way is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
