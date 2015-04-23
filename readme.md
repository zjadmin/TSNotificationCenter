###Type-safe event handling framework

----

###config TSNotificationCenter__config.h
```objective-c 
TSNC_1(hello,NSString*,name)
```

###reg
```objective-c
//self dealloc ---> will auto remove
[self ts_hello:^(NSString *name) {
    NSLog(@"---------- hello %@",name);
}];
```

###call
```objective-c
[TSNotificationCenter call_hello_with_name:@"fc01"];
```

----
    
###system notification
```objective-c
//self dealloc ---> will auto remove
[self ts_regSystemNotificationWithName:UIKeyboardWillShowNotification
                                  block:^(NSNotification *notification)
{
    NSLog(@"---------- UIKeyboardWillShowNotification");
}];
```