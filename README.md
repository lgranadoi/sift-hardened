# sift-hardened

Drop-in replacement for [`sift`](https://www.npmjs.com/package/sift) `17.1.3` that remediates [CVE-2026-85625](https://nvd.nist.gov/vuln/detail/CVE-2026-85625).

Not affiliated with crcn/sift.js.

## Changes from 17.1.3

- Query keys are enumerated with `Object.keys` (own properties only), so a polluted `Object.prototype.$where` is not treated as an operator.
- String `$where` values are rejected. Function `$where` still works.

## Install (npm alias)

```json
"overrides": {
  "sift": "github:lgranadoi/sift-hardened#17.1.4"
}
```
