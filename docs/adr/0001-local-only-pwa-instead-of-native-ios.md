# Local-only PWA instead of a native iOS app

The app is for one person's iPhone, but we're building it as a Progressive Web App installed to the home screen rather than a native SwiftUI app. The dev Mac runs macOS 13.7 without Xcode (it can only take Xcode 15.x, which likely can't deploy to a current iOS), and native sideloading means either a $99/year developer account or re-signing every 7 days. All data stays on the device in browser storage: no account, no backend, no sync.

## Consequences

- Data lives only in the installed web app's storage on the phone. Home-screen web apps are exempt from Safari's 7-day storage eviction, but deleting the app deletes the data — so a manual backup path matters.
- No home-screen widget; push notifications are possible (iOS 16.4+) but deferred.
- Moving to native later means a rewrite of the UI and a data migration, not a port.
