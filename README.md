# Expo Camera onBarCodeScanned Inconsistent Behavior

This repository demonstrates a bug where Expo's `Camera` component's `onBarCodeScanned` prop inconsistently fires its callback function.  The issue seems linked to concurrent UI updates or high system load.  This bug report includes code to reproduce the issue and a potential solution involving debouncing or using a more robust barcode scanning library.

## Reproducing the Bug

1. Clone the repository.
2. Run `npm install` or `yarn install`.
3. Run `expo start`.
4. Point the camera at a barcode.  Note that the callback might not always fire, even if the barcode is clearly scanned.

## Potential Solution

The solution file offers a possible fix using debouncing. This approach limits the frequency of callback execution to prevent potential race conditions stemming from UI updates and concurrent tasks.