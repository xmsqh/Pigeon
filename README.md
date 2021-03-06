Pigeon
======
Library for checking new version from App Store, and notify user with local notifications.

#### Features
- Just add 2 lines of code, and it works. VERY EASY TO USE.
- Checking new version from App Store automatically. No server-side required.
- Notify user after finish using the app. No Bother.

#### Demo 

![image](https://github.com/lightory/Pigeon/raw/master/Screenshot.png)

#### Quick Example

``` objective-c
@implementation AppDelegate

- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    [[Pigeon sharedInstance] startWithAppleId:@"584296227"];
    
    return YES;
}

- (void)application:(UIApplication *)application didReceiveLocalNotification:(UILocalNotification *)notification
{
    [[Pigeon sharedInstance] openInAppStore];
}

@end
```

#### Customize

You can also customize Pigeon as you wish. REMEMBER to set the customizable properties before you call `startWithAppleId:`;

Manage the `latestVersion` yourself, so `Pigeon` won't fetch it from App Store.

``` objective-c
@property (strong, nonatomic) NSString *latestVersion;
```
The message of local notification.

``` objective-c
@property (strong, nonatomic) NSString *updateMessage;
```

The notify interval. Default values is one day.

``` objective-c
@property (assign, nonatomic) NSTimeInterval notifyInterval;
```

#### Who use Pigeon?

If you're building your applications using `Pigeon`, please let me know! (add your application name & App Store link here and pullreuqest this README~


#### License

The MIT License (MIT)

Copyright (c) 2013 LIGHT lightory@gmail.com

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
