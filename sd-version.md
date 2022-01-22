<p align="center">
 <img src="https://dl.dropboxusercontent.com/s/bmfjwfe2ngnivwn/sdversion.png?dl=0" alt="SDVersion"/>
</p>

<p align="center">
    <a href="https://gitter.im/sebyddd/SDiPhoneVersion?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge">
        <img src="https://img.shields.io/badge/gitter-join%20chat-1dce73.svg"
             alt="Gitter">
    </a>
    <a href="http://sebastiandobrincu.com">
        <img src="https://img.shields.io/badge/platform-iOS%20%7C%20watchOS%20%7C%20tvOS%20%7C%20macOS-D0547F.svg"
             alt="Platform">
    </a>
    <a href="http://sebastiandobrincu.com">
        <img src="http://img.shields.io/cocoapods/v/SDVersion.svg"
             alt="Cocoapods Version">
    </a>
</p>

Lightweight Cocoa library for detecting the running device's model and screen size.

With the newer  devices, developers have more work to do. This library simplifies their job by allowing them to get information about the running device and easily target the ones they want.

SDVersion supports iOS, watchOS, tvOS, and macOS. Browse through the implementation of each platform using the links below.

<p align="center">
	<a href="#ios">
        	<img src="https://dl.dropboxusercontent.com/s/ck42lqeda643v02/sdversion-ios.png?dl=0" alt="iOS">
	</a>
	<a href="#mac-os">
		<img src="https://dl.dropboxusercontent.com/s/2yhgx57v4alnzld/sdversion-mac.png?dl=0" alt="Mac">
	</a>
</p>

## How it works
  

```swift
      // Check for device model
      if SDiOSVersion.deviceVersion() == .iPhone7 {
            print("You got the iPhone 7. Sweet 🍭!")
      }

      // Check for device screen size
      if SDiOSVersion.deviceSize() == .Screen3Dot5inch {
            print("Still on 3.5 inches!? 😮")
      }

      // Get device name
      print(SDiOSVersion.deviceNameString())
      /* e.g: Outputs 'iPhone 7 Plus' */

      // Check for iOS Version
      if SDiOSVersion.versionGreaterThan("10") {
            print("You are running iOS 10 or above!")
      }
```

## Add to your project

There are 2 ways you can add SDVersion to your project:


### Installation with CocoaPods

CocoaPods is a dependency manager for Objective-C, which automates and simplifies the process of using 3rd-party libraries like SDVersion in your projects. See the "[Getting Started](http://guides.cocoapods.org/syntax/podfile.html)" guide for more information.


### Available iOS Version Finder methods
  ```objective-c
      + (BOOL)versionEqualTo:(NSString *)version;
      + (BOOL)versionGreaterThan:(NSString *)version;
      + (BOOL)versionGreaterThanOrEqualTo:(NSString *)version;
      + (BOOL)versionLessThan:(NSString *)version;
      + (BOOL)versionLessThanOrEqualTo:(NSString *)version;
  ```       

### Helpers
```objective-c
	  NSLog(@"%@", [SDVersion deviceVersionName:[SDVersion deviceVersion]]);
      /* e.g: Outputs 'iPad Air 2' */

      NSLog(@"%@", [SDVersion deviceSizeName:[SDVersion deviceSize]]);
      /* e.g: Outputs '4.7 inch' */
```
Or in Swift: 
```swift
      let deviceVersionName = SDiOSVersion.deviceVersionName(SDiOSVersion.deviceVersion())
      let deviceSizeName = SDiOSVersion.deviceSizeName(SDiOSVersion.deviceSize())    
```


### Available watchOS Version Finder methods
```objective-c
    + (BOOL)versionEqualTo:(NSString *)version;
    + (BOOL)versionGreaterThan:(NSString *)version;
    + (BOOL)versionGreaterThanOrEqualTo:(NSString *)version;
    + (BOOL)versionLessThan:(NSString *)version;
    + (BOOL)versionLessThanOrEqualTo:(NSString *)version;
```      


### Helpers
```objective-c
      NSLog(@"%@", [SDVersion deviceSizeName:[SDVersion deviceSize]]);
      /* e.g: Outputs '15 inch' */

      NSLog(@"%@",[SDVersion deviceScreenResolutionName:[SDVersion deviceScreenResolution]])
      /* e.g: Outputs '{2880, 1800}' */
```

## Used by

<p align="center">
       <img src="https://dl.dropboxusercontent.com/s/yp3kwu2lobe9pvg/who-uses-sdversion.png?dl=0" alt="Who uses SDVersion">
</p>

## License
Usage is provided under the [MIT License](http://opensource.org/licenses/mit-license.php). See LICENSE for the full details.