# Firebase Initialization Error: Unexpected or Missing Options

This repository demonstrates a common but easily missed error when initializing the Firebase JavaScript SDK.  The `initializeApp` function requires specific properties within the options object.  Providing incorrect or missing properties can lead to initialization failure with vague error messages.

The `firebaseBug.js` file demonstrates the problem, where the `apiKey` is missing and there is a typo in `credential`. The `firebaseBugSolution.js` file shows the corrected initialization.

## How to reproduce
1. Clone this repository.
2. Run `firebaseBug.js` and observe the failure.
3. Compare to `firebaseBugSolution.js` and observe the correct initialization.

## Solution
Carefully verify the `options` object passed to `initializeApp` against the official Firebase documentation to ensure all required properties are provided correctly with proper spelling and values.  Use a linter or code formatter to aid in detecting typos.