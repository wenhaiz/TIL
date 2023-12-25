# Add color value for both light mode and dark mode
In SwiftUI,I found a way to declare color values used for both light mode and dark mode by adding extension variables for `ColorScheme`.

E.g.
```swift
extension ColorScheme{

    var isDarkMode:Bool{
        self == .dark
    }
    
    var cardBgColor:Color{
        isDarkMode ? .brown.opacity(0.2) : .white
    }

    //other colors
}

//In your Views
```swift
import SwiftUI

// inject the colorScheme object
@Environment(\.colorScheme) var colorScheme

struct MyView:View{
    var body:View{
        VStack{
            Text("My view")
        }
        //use the color
        .background(colorScheme.cardBgColor)
    }
}
```

```
