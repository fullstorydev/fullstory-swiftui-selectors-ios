# fullstory-swiftui-selectors-ios

Swift package artifacts for FullStory SwiftUI selectors, an add-on to [the FullStory SDK for instrumenting iOS mobile apps](https://www.fullstory.com/mobile-apps/) that improves how SwiftUI views are captured.

This package is used alongside [fullstory-swift-package-ios](https://github.com/fullstorydev/fullstory-swift-package-ios), not instead of it. For setting up the FullStory SDK itself, see [Getting Started with iOS Capture](https://help.fullstory.com/hc/en-us/articles/360042772333-Getting-Started-with-iOS-Capture) in the FullStory Help Center.

Email mobile-support@fullstory.com for additional help.

For information about the content of each release, please see the [Release Notes](https://help.fullstory.com/hc/en-us/articles/4412766845591-Fullstory-for-Mobile-Apps-Release-Notes).

## Installation

In Xcode, add `https://github.com/fullstorydev/fullstory-swiftui-selectors-ios` as a package dependency, pin it to an exact version, and add the `FSSwiftUISelectors` library to your app target.

Each release is built against one specific FullStory build, so this package and the FullStory package must be pinned to the same version. The two share version numbers, so pick one from the [list of released versions](https://github.com/fullstorydev/fullstory-swiftui-selectors-ios/tags) and use it for both:

```swift
dependencies: [
    .package(url: "https://github.com/fullstorydev/fullstory-swiftui-selectors-ios", exact: "<version>"),
    .package(url: "https://github.com/fullstorydev/fullstory-swift-package-ios", exact: "<version>"),
]
```

Declaring the FullStory package is not strictly required, because depending on `FSSwiftUISelectors` pulls it in at the matching version automatically. Declare it anyway if your own code calls FullStory APIs such as `view.fsUnmask()`, which most projects do. Either way a version mismatch surfaces as a resolution error rather than a runtime failure, because this package pins FullStory with `exact:`.

This package declares no minimum platform, so it imposes no deployment target floor on your project.

---

Maintainers: see [`.github/workflows/README.md`](.github/workflows/README.md) for how releases are produced and why the manifest is shaped the way it is.
