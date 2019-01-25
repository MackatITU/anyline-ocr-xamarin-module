## Anyline Xamarin SDK ##

Anyline provides an easy-to-use SDK for applications to enable Optical Character Recognition (OCR) on mobile devices.


## Quick Start

* If you'd like to clone the repository you will have to use git-lfs. Use the following commands to install git-lfs.

Download git lfs from https://help.github.com/articles/installing-git-large-file-storage/

```
git lfs install
```


* If you prefer downloading a package, use the provided `zip` package on the [releases page](https://github.com/Anyline/anyline-ocr-xamarin-module/releases). Be aware that the github download zip button does not work for projects with git-lfs.

## File summary

* `BindingSource` - Xamarin [iOS](https://developer.xamarin.com/guides/ios/advanced_topics/binding_objective-c/) and [Android](https://developer.xamarin.com/guides/android/advanced_topics/binding-a-java-library/) Binding Libraries, including wrappers
* `Examples` - [Xamarin.iOS](Examples/AnylineXamarinApp.iOS), [Xamarin.Android](Examples/AnylineXamarinApp.Droid) and [Xamarin.Forms](Examples/AnylineXamarinForms) example apps
* `AnylineXamarinSDK.Droid.dll` - Precompiled library for Xamarin.Android
* `AnylineXamarinSDK.iOS.dll` - Precompiled library for Xamarin.iOS
* `AnylineResources.Bundle` - The iOS Resource files that have to be included to your app project as BundleResource (iOS only!)
* `AT.Anyline.Xamarin.App.Droid_<version>.apk` - Prebuilt Android APK ready to install on your Android device
* `README.md` - This readme.
* `LICENSE.md` - The license file.


### BindingSource

The `anylinesdk-xamarin.sln` Visual Studio solution located in the /BindingSource directory inhibits two projects: The project for Android bindings `AnylineXamarinSDK.Droid` and the iOS bindings project `AnylineXamarinSDK.iOS`.


#### Android: AnylineXamarinSDK.Droid

The Android Binding project creates a Bindings library from the provided Anyline Java library (.aar file), given Metadata.xml transforms and Additional C# code.

Located in the [Assets/tools](BindingSource/AnylineXamarinSDK.Droid/Assets/tools) directory lies the javadoc and python scripts to automatize parameter naming fixes, as the Xamarin build tool is not able to keep the correct parameter names after binding.


#### iOS: AnylineXamarinSDK.iOS

The iOS Binding project provides easy compilation from the provided Anyline framework, given linker & binding definitions via `Anyline.linkwith.cs`, `ApiDefinition.cs` and `StructsAndEnums.cs`.

The binding definitions are generated by the Xamarin tool [Objective Sharpie](https://developer.xamarin.com/guides/cross-platform/macios/binding/objective-sharpie/)


### Examples

The [Examples](Examples) directory provides source code for the Anyline Xamarin.iOS and Xamarin.Android Example apps. Simply build & run the example project for your desired platform and enjoy scanning :)


#### Quick start & setup

For a detailed setup guide on how to integrate Anyline for your scanning application, please visit the [Anyline Xamarin documentation](https://documentation.anyline.io/toc/platforms/xamarin/index.html).


### Available Modules
- [**Barcode:**](https://documentation.anyline.io/toc/modules/barcode/index.html)  Scan 23 types of international barcode & QR code formats.
- [**Energy:**](https://documentation.anyline.io/toc/modules/energy/index.html) Scan meter readings of various electric, gas, and water meters.
- [**Document:**](https://documentation.anyline.io/toc/modules/document/index.html) Detect and scan documents for further processing.
- [**MRZ:**](https://documentation.anyline.io/toc/modules/mrz/index.html) Reliable scanning of data from passports' and IDs' machine readable zones (MRZ).
- [**Anyline OCR:**](https://documentation.anyline.io/toc/modules/anyline_ocr/index.html) Create your own custom use case.
- [**License Plate:**](https://documentation.anyline.io/toc/modules/license_plate/index.html) Scan license plates.

### Requirements

- A Xamarin account (If you work with Visual Studio, you need at least a Xamarin business account. Check out the Xamarin Website for detailed information)
- Xamarin Studio or Visual Studio


#### Android

- Android device with SDK >= 18
- decent camera functionality (recommended: 720p and adequate auto focus)


#### iOS

- minimum iOS 8.2
- minimum iPhone4s
- A Mac computer for building / deploying to the iPhone


## License

See LICENSE file.