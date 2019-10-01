# Apple Swift Resources
Apple Swift Resources

<br />

1. [Apple Swift Resources](https://developer.apple.com/swift/resources/)
1. [Swift——Build apps using a powerful open language](https://developer.apple.com/documentation/swift)
1. [Swift Evolution](https://apple.github.io/swift-evolution/)

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

