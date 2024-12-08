# Expo Linking API Android Deep Link Event Listener Inconsistency

This repository demonstrates a bug in Expo's `Linking` API on Android.  The `Linking.addEventListener` for deep links doesn't always fire reliably when the app is already open, especially when it's in the background. This inconsistency causes deep link handling to fail intermittently.

The `bug.js` file showcases the problematic behavior, while `bugSolution.js` provides a workaround to mitigate the issue.  This workaround involves using a combination of `Linking.getInitialURL` and a persistent event listener to capture all potential deep link events.