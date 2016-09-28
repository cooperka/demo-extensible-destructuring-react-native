# ExtensibleDestructuringReactNative

Demo project showing how the
[`extensible-destructuring` Babel plugin](https://github.com/vacuumlabs/babel-plugin-extensible-destructuring)
breaks React Native v0.34.

## Usage

Terminal 1:

1. `npm install`
2. `npm start`

Terminal 2:

3. `react-native run-ios`

## Results

When using mode `optin`, everything works as expected.

When using mode `optout` (see [commit](https://github.com/cooperka/extensible-destructuring-react-native/commit/d7d960a8550345af07b61ba813e966aad9246880)),
the app fails to start in the iOS simulator with the error
`Unhandled JS Exception: ReferenceError: Can't find variable: require`.

On my full app, I don't even see this error and instead it simply shows an empty white screen
and the app never connects to the HMR server (normally the console message shows
`[Hot Module Replacement] Client connected` when Hot Reloading is enabled).

## Issue

I've opened an issue [here](https://github.com/vacuumlabs/babel-plugin-extensible-destructuring/issues/14)
for discussion.
