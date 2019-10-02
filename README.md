# Apple Swift Resources
Apple Swift Resources

<br />

1. [Apple Swift Resources](https://developer.apple.com/swift/resources/)
1. [Swift——Build apps using a powerful open language](https://developer.apple.com/documentation/swift)
1. [Swift Evolution](https://apple.github.io/swift-evolution/)

<br />

## Swift Used in 3rd Party Platforms

1. [Creating Objective-C and C++ packages using Swift Package Manager](http://ankit.im/swift/2016/05/21/creating-objc-cpp-packages-with-swift-package-manager/)
1. [Swift Package Manager](https://github.com/apple/swift-package-manager/tree/master/Documentation)
1. [在CentOS7.2中安装swift编译器](https://blog.csdn.net/solan8/article/details/80674953)

<br />

## My Own Useful Utilities

```swift
/// Execute the specified handler after the specified seconds
/// - parameters:
///     - seconds: the specified seconds
///     - handler: the closure to be executed
public func delayExecuteHandlerOnMainQueue(seconds: Double, handler: @escaping () -> Void) {
    
    let sec = seconds < 0.001953125 ? 0.001953125 : seconds
    DispatchQueue.main.asyncAfter(deadline:
        DispatchTime(uptimeNanoseconds: DispatchTime.now().uptimeNanoseconds +
            UInt64(sec * 1000_000_000.0)), execute: handler)
}
```

