# Strings-lhp


#import <Foundation/Foundation.h>

int main(int argc, const char * argv[]) {
    @autoreleasepool {
    
        NSString *name = @"Mar ";
        NSLog(@"My name is %@", name);
        
        NSUInteger nameLength = [name length];
        NSLog(@"My name is %lu characters long.", (unsigned long)nameLength);
        
        NSString *nameCaps = [name uppercaseString];
        NSLog(@"%@", nameCaps);
        
        NSString *nameLowcase = [name lowercaseString];
        NSLog(@"%@", nameLowcase);
        
        NSString *nameLast = @"Koss";
        NSString *nameFull = [name stringByAppendingString:nameLast];
        NSLog(@"My full name is %@", nameFull);
        
        NSString *nameOther = @"Pooter";
        NSString *nameNot = [nameFull stringByReplacingOccurrencesOfString:nameLast withString:nameOther];
        NSLog(@"My name is not %@", nameNot);
        
        //
        
        NSString *madLib = @"Yesterday, _PERSON_ and I when to the park. On our way to the _ADJECTIVE_1 park, we saw a _ADJECTIVE_2 _NOUN_ on a bike. We also saw big _ADJECTIVE_2 balloons tied to the _NOUN_. Once we got to the _ADJECTIVE_1 park, the sky turned _ADJECTIVE_2. It started to _VERB_. _PERSON_ and I _VERB_ all the way home.";
        
        madLib = [madLib stringByReplacingOccurrencesOfString:@"_PERSON_" withString:@"Shaq"];
        madLib = [madLib stringByReplacingOccurrencesOfString:@"_ADJECTIVE_1" withString:@"lactating"];
        madLib = [madLib stringByReplacingOccurrencesOfString:@"_ADJECTIVE_2" withString:@"slobbering"];
        madLib = [madLib stringByReplacingOccurrencesOfString:@"_NOUN_" withString:@"swamp dweller"];
        madLib = [madLib stringByReplacingOccurrencesOfString:@"_VERB_" withString:@"gaped"];
        
        NSLog(@"%@", madLib);
        
        NSString *madderLib = @"When I was a(n) ADJECTIVE1 NOUN1, I knew a(n) ADJECTIVE2 NOUN2. I most often found them in the ADJECTIVE3 PLACE1 continually VERB2 a(n) NOUN4. It scarred me for life.";
        
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"ADJECTIVE1" withString:@"filthy"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"NOUN1" withString:@"grill master"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"ADJECTIVE2" withString:@"blithering"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"NOUN2" withString:@"monkey trainer"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"ADJECTIVE3" withString:@"worst"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"PLACE1" withString:@"library"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"VERB2" withString:@"pooping"];
        madderLib = [madderLib stringByReplacingOccurrencesOfString:@"NOUN4" withString:@"murder of crows"];
        
        NSLog(@"%@", madderLib);
        
    }
    return 0;
}
