## 5.0.1 (May 19, 2015)

- Fixes stringify to only take ancestors into account when checking
  circularity.
  It previously assumed every visited object was circular which led to [false
  positives][issue9].
  Uses the tiny serializer I wrote for [Must.js][must] a year and a half ago.
- Fixes calling the `replacer` function in the proper context (`thisArg`).
- Fixes calling the `cycleReplacer` function in the proper context (`thisArg`).
- Speeds serializing by a factor of
  Big-O(h-my-god-it-linearly-searched-every-object) it had ever seen. Searching
  only the ancestors for a circular references speeds up things considerably.

[must]: https://github.com/moll/js-must
[issue9]: https://github.com/isaacs/json-stringify-safe/issues/9

## 5.0.2 (Nov 15, 2024)

- Rewrite package in typescript
- Update test suite from mocha to jest
- Integrate `tsup` bundler

# 5.0.4 (Nov 15, 2024)

- Implement array replacers [Issue #14](https://github.com/moll/json-stringify-safe/issues/14)
- BigInt support [PR #35](https://github.com/moll/json-stringify-safe/pull/35)
