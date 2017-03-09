# iPhone Web Browser

Project settings: Uncheck size classes to make your app fit properly on the screen. Adjust project's settings under the 'info' tab and disable the default launch view.

## The interface file

```
//
//  ViewController.h
//  Browser
//
//  Created by Gary on 7/27/15.
//  Copyright (c) 2015 personal. All rights reserved.
//

#import &lt;UIKit/UIKit.h&gt;

@interface ViewController : UIViewController

@property (strong, nonatomic) IBOutlet UIWebView *webView;

@end
```

## Control drag to link up the view and the code

![](https://raw.githubusercontent.com/atabegruslan/iBrowser/master/Illustrations/iBrowser1.PNG)

```
//
//  ViewController.m
//  Browser
//
//  Created by Gary on 7/27/15.
//  Copyright (c) 2015 personal. All rights reserved.
//

#import "ViewController.h"

@interface ViewController ()

@end

@implementation ViewController

- (void)viewDidLoad {
    [super viewDidLoad];
    // Do any additional setup after loading the view, typically from a nib.
    NSURL *url = [NSURL URLWithString:@"http://www.google.com"];
    NSURLRequest *request = [NSURLRequest requestWithURL:url];
    [_webView loadRequest:request];
}

- (void)didReceiveMemoryWarning {
    [super didReceiveMemoryWarning];
    // Dispose of any resources that can be recreated.
}

- (BOOL)shouldAutorotate{
    return NO;
}

- (NSUInteger)supportedInterfaceOrientations{
    return UIInterfaceOrientationMaskPortrait;
}

@end
```
												
## In the view, add button items. Then control-drag link up each button and their functionality respectively

![](https://raw.githubusercontent.com/atabegruslan/iBrowser/master/Illustrations/iBrowser1.PNG)

## Setting AutoRotate to no locks the screen orientation. Only allowing "UIInterfaceOrientationMaskPortrait" (i.e.: right-way-up) under "supportedInterfaceOrientations" also locks the screen.				
