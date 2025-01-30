# Countdown Flipper SwiftUI 📆

## 👨🏻‍🏫 Introduction
`countdown-flipper-swiftui` is a versatile and visually engaging flip counter swiftui component designed to display the current time in a flipping animation style. It leverages SwiftUI to create a dynamic and interactive experience, simulating the look and feel of traditional flip clocks like use cases.


## 🧑🏻‍💻 Requirements
- Swift 6.0 or later
- iOS 17 or later


## ✨ Features

- **Two-Way Flipping**: Configure the `flipperType` parameter for `.flipFromTop`, or `.flipFromBottom`.
- **Automatic Counter Placement**: When you assign a new value to the `counter` parameter, the top and bottom counters are automatically managed behind the scenes.
- **Customizations**: Additional customizations, such as color, corner radius, and text, will be added upon request.

  
## 🤳🏻 Previews
|UI Component - Counter Flipper|Use Case - Flip Clock|
|-|-|
| <img src="https://github.com/KDTechniques/ReadMe_Media_Files/blob/main/countdown-flipper-swiftui/Counter%20Flipper.gif?raw=true" alt="Counter Flipper">|<img src="https://github.com/KDTechniques/ReadMe_Media_Files/blob/main/countdown-flipper-swiftui/Demo.gif?raw=true" alt="Demo">|


## 🛠️ Installation

### Swift Package Manager

To integrate `countdown-flipper-swiftui` into your Swift project, add the following dependency to your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/KDTechniques/countdown-flipper-swiftui.git", from: "1.0.0")
]
```
### 🫛 CocoaPods
For CocoaPods, add the following to your Podfile:

```ruby
pod 'countdown-flipper-swiftui', :git => '[https://github.com/KDTechniques/countdown-flipper-swiftui.git](https://github.com/KDTechniques/countdown-flipper-swiftui.git)'
```


## 📖 Usage
```swift
import SwiftUI
import CountdownFlipperSwiftUI

struct ContentView: View {
    @State private var counter: Int = 0
    
    var body: some View {
        VStack(spacing: 50) {
            CountdownFlipperView(flipperType: .flipFromTop, counter: $counter, fontSize: 200) // <--- here
            
            Button("Generate Random Number: \(counter)") {
                counter = .random(in: 0...9)
            }
            .buttonStyle(.bordered)
            .controlSize(.large)
        }
    }
}
```

## Behind the Scenes
This is how I break down a larger problem into smaller, understandable pieces and build upon each step by step to achieve the final goal.

<img src="https://github.com/KDTechniques/ReadMe_Media_Files/blob/main/countdown-flipper-swiftui/Behind%20the%20Scenes.jpg?raw=true" alt="Behind the Scenes">


## 🤝 Contribution
Contributions are welcome! If you have suggestions or improvements, please submit a pull request or open an issue on GitHub.


## 📜 License
`countdown-flipper-swiftui` is released under the MIT License. See the [LICENSE](https://github.com/KDTechniques/countdown-flipper-swiftui/blob/main/LICENSE) file for details.
