# Biscotti CMP — Client Source Code

This repository contains the unminified source code for `biscotti.min.js`, the consent management engine used by the [Biscotti CMP WordPress plugin](https://wordpress.org/plugins/biscotti-cmp/).

## What is this?

`biscotti.js` is the consent banner engine that runs on websites using Biscotti CMP. It handles:

- Cookie consent collection (GDPR, CCPA, ePrivacy)
- IAB TCF 2.3 compliance (Transparency & Consent Framework)
- Google Consent Mode v2 integration
- Script blocking until consent is granted
- Multi-language support (39 languages)

## Building

```bash
npm install
npm run build
```

This produces `biscotti.min.js` from `biscotti.js` using esbuild.

## License

GPL-2.0-or-later

## Links

- [Biscotti CMP Website](https://biscotti-cmp.com)
- [WordPress Plugin](https://wordpress.org/plugins/biscotti-cmp/)
- [Documentation](https://biscotti-cmp.com/en/documentation)
