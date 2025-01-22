# Expo CLI Hangs on Development Server Start

This repository demonstrates a bug where the Expo CLI hangs indefinitely when attempting to start the development server. The issue is particularly perplexing due to the lack of error messages in the console, making debugging difficult.  This bug appears to manifest after updating the Expo CLI version and/or installing new packages.

## Steps to Reproduce

1.  Follow the instructions in `expoBug.js` to set up a simple Expo project.
2.  Run `expo start`.
3.  Observe that the Expo CLI hangs without any error messages.

## Solution

The solution, found in `expoBugSolution.js`, involves identifying potential conflicting dependencies or misconfigurations in the project's `package.json`. In my case the conflict was related to `metro-resolver` and `metro-minify-terser`. 