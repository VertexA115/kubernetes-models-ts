# @kubernetes-models/flagger

## 0.2.0

### Minor Changes

- [`d46053b`](https://github.com/tommy351/kubernetes-models-ts/commit/d46053b15d0315e91fdfdb1f7fe0b60b681a499a) Thanks [@tommy351](https://github.com/tommy351)! - Decrease the size of export map in `package.json` by using wildcard pattern (`*`).

  ```js
  // Before
  {
    "exports": {
      "./v1/Pod": {
        "import": "./v1/Pod.mjs",
        "require": "./v1/Pod.js"
      },
      "./v1/Service": {
        "import": "./v1/Service.mjs",
        "require": "./v1/Service.js"
      }
    }
  }

  // After
  {
    "exports": {
      "./v1/*": {
        "import": "./v1/*.mjs",
        "require": "./v1/*.js"
      }
    }
  }
  ```

- [`f82b1cc`](https://github.com/tommy351/kubernetes-models-ts/commit/f82b1cc64b27884a862166977617f00911a03e49) Thanks [@tommy351](https://github.com/tommy351)! - Support TypeScript `nodenext` module resolution by adding `types` to export map.

  ```js
  // Before
  {
    "exports": {
      "./v1/Pod": {
        "import": "./v1/Pod.mjs",
        "require": "./v1/Pod.js"
      }
    }
  }

  // After
  {
    "exports": {
      "./v1/Pod": {
        "import": {
          "types": "./v1/Pod.d.ts",
          "default": "./v1/Pod.mjs"
        }
        "require": {
          "types": "./v1/Pod.d.ts",
          "default": "./v1/Pod.js"
        }
      }
    }
  }
  ```

### Patch Changes

- Updated dependencies []:
  - @kubernetes-models/apimachinery@1.1.0

## 0.1.0

### Minor Changes

- [#109](https://github.com/tommy351/kubernetes-models-ts/pull/109) [`b71d10c`](https://github.com/tommy351/kubernetes-models-ts/commit/b71d10cd68180c5619e41b8d70bb4c363f83dbae) Thanks [@tommy351](https://github.com/tommy351)! - First release.

### Patch Changes

- Updated dependencies []:
  - @kubernetes-models/apimachinery@1.1.0