# Tailwind CSS PurgeCSS Issue

This repository demonstrates a problem with PurgeCSS not removing unused styles from a Tailwind CSS production build.  Even with what seems to be correct configuration, unnecessary styles remain, increasing the bundle size.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run build`.
4. Analyze the resulting CSS file to see unused styles.  They should be purged but are not.

## Expected Behavior

PurgeCSS should remove all unused Tailwind CSS styles, resulting in a smaller CSS file.

## Actual Behavior

PurgeCSS fails to remove unused styles, resulting in a larger than necessary CSS file.

## Possible Solutions (Investigate)

* Incorrect PurgeCSS configuration. Review the `purge` options in `tailwind.config.js` for correctness and completeness.
* Conflicting plugins or integrations with PurgeCSS. Temporarily disable other plugins to isolate the issue. 
* Issues with the way content is handled or generated dynamically. Check for content loaded after initial build.
* Bug in PurgeCSS itself or incompatibility with current Tailwind version. Refer to PurgeCSS and Tailwind documentation for compatibility updates and potential workarounds.