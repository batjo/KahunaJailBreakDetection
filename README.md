# KahunaJailBreakDetection

[![CI Status](http://img.shields.io/travis/siddharthchopra/KahunaJailBreakDetection.svg?style=flat)](https://travis-ci.org/siddharthchopra/KahunaJailBreakDetection)
[![Version](https://img.shields.io/cocoapods/v/KahunaJailBreakDetection.svg?style=flat)](http://cocoapods.org/pods/KahunaJailBreakDetection)
[![License](https://img.shields.io/cocoapods/l/KahunaJailBreakDetection.svg?style=flat)](http://cocoapods.org/pods/KahunaJailBreakDetection)
[![Platform](https://img.shields.io/cocoapods/p/KahunaJailBreakDetection.svg?style=flat)](http://cocoapods.org/pods/KahunaJailBreakDetection)

![LogCamp](http://www.kahuna-mobihub.com/templates/ja_puresite/images/logo-trans.png)

KahunaJailBreakDetection is written in Objective C

## Example

To run the example project, clone the repo, and run `pod install` from the Example directory first.

## Installation

KahunaJailBreakDetection is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'KahunaJailBreakDetection', '~> 0.1.8'
```
> New development will happen exclusively on the master/Swift 3 branch.

## Detect an iOS device is jailbroken or not
```swift
KahunaJailBreakDetection.isJailbroken()
```

## Required methods to be written in appdelegate class.
> _Note:_
Call checkDeviceRooted in applicationWillEnterForeground method
```swift
func checkDeviceRooted() {
    let jailbreak = KahunaJailBreakDetection.sharedInstance() as! KahunaJailBreakDetection
    if let rootViewController = self.window?.rootViewController {
        jailbreak.setYourViewController(rootViewController)
        jailbreak .checkJailDeviceinDevice()
    }
}
  ```  

## For Swift 2.3
> _Note:_ KahunaJailBreakDetection requires Swift 3 (and Xcode 8) or greater. If you absolutely
> need compatibility with Swift 2.3 you can use the swift2.3 branch by adding following line to your Podfile:
```ruby
pod 'KahunaJailBreakDetection', '~> 0.1.1’
```

## Author

siddharthchopra, siddharth.chopra@kahunasystems.com

## License

KahunaJailBreakDetection is available under the MIT license. See the LICENSE file for more info.
