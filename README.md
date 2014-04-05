# Objective-C Style

## `@interface` and `@implementation` Spacing

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


## `@interface` Elements

- Properties should be listed first, and should be explicit about all their attributes.
- Constructors should follow
- Then other class methods
- Then instance methods

~~~objective-c
@interface MyClass : NSObject

@property (strong, nonatomic, readwrite) NSString *text;
@property (assign, nonatomic, readonly) BOOL isHelpful;

+ (instancetype)newWithText:(NSString *)text helpful:(BOOL)isHelpful;
- (instancetype)initWithText:(NSString *)test helpful:(BOOL)isHelpful;

+ (NSString *)defaultText;

- (void)takeAction;
- (NSArray *)getSomeCollection;

@end
~~~
