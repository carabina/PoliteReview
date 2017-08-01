# PoliteReview
A Polite Way to Request Reviews for iOS

# Features
Polite Review is an elegant way to request ratings and reviews from your users.

* For 10.3 and above, uses `StoreKit` to request reviews, in compliance with store guidelines.
* For below 10.3, falls back to a simple alert which will open the App Store to the review page.

## Coming Soon

* Carthage Support
* Notifications for analytics within your app
* Swift 4

# Getting Started

The best way to get started with PoliteReview is with Carthage(coming soon) and CocoaPods.

## Installation with CocoaPods
```ruby
pod 'Gloss'
```

## Installation with Carthage
```
coming soon
```

## Usage

Add PoliteReview to `AppDelegate`

```
import PoliteReview

...

func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {

    PoliteReview().setup(itunesID: <your itunes id>, contactURL: <a link to a website contact page>, contactEmail: <your contact email>, triggerCount: <a launch count>)
    return true
}
```
* Your iTunes App ID is a string of numbers, found in iTunes connect.
* Trigger count is the minimum number of times your app has been launched before any alerts are shown.

In any ViewController, you can request a review by calling `RequestPoliteReview().request()`. PoliteReview will determine if an alert will be shown.

Example:

```
class ViewController: UIViewController {
...

    func methodCalledByUser() {
    ...
    RequestPoliteReview().request()
    }
        
```


