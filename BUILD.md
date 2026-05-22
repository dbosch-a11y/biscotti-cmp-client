# Biscotti CMP — JavaScript Build Instructions

## Source Files

The minified JavaScript files in this directory are built from the source code
located in the `src/client/` directory of the Biscotti CMP monorepo.

### biscotti.min.js

- **Source:** `src/client/biscotti.js` (ES module source)
- **Dependencies:** `@iabtcf/cmpapi`, `@iabtcf/core` (IAB TCF libraries)
- **Build tool:** esbuild
- **Build command:** `npm run build:engine`
- **Equivalent:** `esbuild src/client/biscotti.js --bundle --minify --outfile=src/client/biscotti.min.js --format=iife`

### biscotti.js

The unminified source file is included alongside the minified version.
It contains ES module `import` statements that are resolved by esbuild
during the build process. The file is NOT directly loadable in a browser
without bundling.

### Other JS files

- `admin.js` — WordPress admin shell (unminified, human-readable)
- `connection.js` — Setup wizard connection logic (unminified)
- `consent.js` — Consent management utilities (unminified)
- `blocks.js` — Gutenberg block registrations (unminified)

## Rebuilding

```bash
# From the monorepo root:
npm install
npm run build:engine

# Then sync to the WordPress plugin:
cp src/client/biscotti.min.js src/wordpress/biscotti-cmp/assets/js/biscotti.min.js
cp src/client/biscotti.js src/wordpress/biscotti-cmp/assets/js/biscotti.js
```
