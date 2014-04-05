# Objective-C Style

All `@interface` and `@implementation` should be separated from other content by __2 newlines__:

~~~objective-c
// copyright etc
// other comments

#import "Something.h"

@class OtherClass;


@interface MyThing : NSObject

@end
~~~

This should be true in both header files and implementation files:

~~~objective-c
// copyright stuff

#import "MyThing.h"


@implementation MyThing

@end
~~~

In the case of private interfaces this rule applies to the space between the blocks:

~~~objective-c
// copyright stuff

#import "MyThing.h"


@interface MyThing ()

@end


@implementation MyThing

@end
~~~
