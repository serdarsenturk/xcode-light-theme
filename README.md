# Xcode Light Theme

[![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/yugosdex.xcode-light-theme?style=flat-square&logo=visual-studio-code&logoColor=white&label=VS%20Code%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=yugosdex.xcode-light-theme)
[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/yugosdex.xcode-light-theme?style=flat-square&logo=visual-studio-code&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=yugosdex.xcode-light-theme)
[![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/yugosdex.xcode-light-theme?style=flat-square&logo=visual-studio-code&logoColor=white)](https://marketplace.visualstudio.com/items?itemName=yugosdex.xcode-light-theme)
[![GitHub](https://img.shields.io/github/license/yugosdex/xcode-light-theme?style=flat-square)](https://github.com/yugosdex/xcode-light-theme/blob/main/LICENSE)

A faithful recreation of Xcode's default light theme with Xcode-style project navigator layout and enhanced syntax highlighting.

## Features

- 🎨 **Authentic Colors**: Uses Xcode's original light theme color palette
- 🗂️ **Xcode-style Navigator**: Project explorer styled to match Xcode's project navigator
- 🔍 **Enhanced Syntax Highlighting**: Optimized for multiple programming languages
- 📝 **Language-specific Rules**: Special highlighting for Swift, Objective-C, JavaScript/TypeScript, and Python
- 🖥️ **Complete UI Theme**: Carefully crafted colors for sidebar, activity bar, tabs, and more

## Screenshots

### Editor View
![Xcode Light Theme - Editor](https://raw.githubusercontent.com/yugosdex/xcode-light-theme/main/images/editor-preview.png)

### Project Navigator
![Xcode Light Theme - Navigator](https://raw.githubusercontent.com/yugosdex/xcode-light-theme/main/images/navigator-preview.png)

### Syntax Highlighting Examples
![Xcode Light Theme - Syntax](https://raw.githubusercontent.com/yugosdex/xcode-light-theme/main/images/syntax-preview.png)

## Installation

### From Trae IDE (Open-VSX Registry)

1. Open Trae IDE
2. Go to Extensions panel
3. Search for "Xcode Light Theme"
4. Click Install
5. Activate the theme by pressing `Ctrl+K Ctrl+T` (or `Cmd+K Cmd+T`) and select "Xcode Light"

### From VS Code Marketplace

1. Open Visual Studio Code
2. Go to Extensions panel (`Ctrl+Shift+X` or `Cmd+Shift+X`)
3. Search for "Xcode Light Theme" by yugosdex
4. Click Install
5. Activate the theme by pressing `Ctrl+K Ctrl+T` (or `Cmd+K Cmd+T`) and select "Xcode Light"

### Manual Installation

1. Download the `.vsix` file from releases
2. In your editor, press `Ctrl+Shift+P` (or `Cmd+Shift+P`)
3. Type "Extensions: Install from VSIX"
4. Select the downloaded `.vsix` file
5. Restart your editor and activate the theme

## Color Palette

This theme uses the following color palette inspired by Xcode's original light theme:

- **Keywords**: `#ad3da4` (Purple) - for language keywords and control flow
- **Strings**: `#d12f1b` (Red) - for string literals and text
- **Functions**: `#272ad8` (Blue) - for function names and method calls
- **Comments**: `#536579` (Gray, italic) - for code comments
- **Numbers**: `#272ad8` (Blue) - for numeric literals
- **Classes**: `#3f6e75` (Teal) - for class names and types
- **Variables**: `#000000` (Black) - for variable names

## UI Colors

- **Sidebar Background**: `#f6f6f6` - matches Xcode's project navigator
- **Activity Bar**: `#f0f0f0` - clean, minimal appearance
- **Editor Background**: `#ffffff` - pure white for optimal readability
- **Selection**: `#0066cc` - Xcode-style blue selection

## Supported Languages

Optimized syntax highlighting for:

- **Swift** - Attributes, types, and Swift-specific keywords
- **Objective-C** - Preprocessor directives and class names
- **JavaScript/TypeScript** - Modern JS/TS syntax and types
- **Python** - Decorators and Python-specific constructs
- **C/C++** - System types and preprocessor
- **Java** - Annotations and Java keywords
- **HTML/CSS** - Web development syntax
- **JSON/XML** - Data format highlighting
- **Markdown** - Documentation formatting
- And many more...

## Recommended Settings

For the best Xcode-like experience, add these settings to your `settings.json`:

```json
{
  "editor.fontFamily": "'SF Mono', Menlo, Monaco, 'Courier New', monospace",
  "editor.fontSize": 12,
  "editor.fontWeight": "400",
  "editor.lineHeight": 1.4,
  "editor.tabSize": 4,
  "editor.insertSpaces": true,
  "editor.renderWhitespace": "selection",
  "editor.minimap.enabled": true,
  "workbench.colorTheme": "Xcode Light",
  "workbench.iconTheme": "vs-seti"
}
```

## Configuration

### Customizing Colors

You can customize specific colors by adding overrides to your `settings.json`:

```json
{
  "workbench.colorCustomizations": {
    "[Xcode Light]": {
      "editor.background": "#ffffff",
      "sideBar.background": "#f6f6f6",
      "activityBar.background": "#f0f0f0",
      "editor.selectionBackground": "#0066cc33"
    }
  }
}
```

### Token Color Customizations

To modify syntax highlighting colors:

```json
{
  "editor.tokenColorCustomizations": {
    "[Xcode Light]": {
      "keywords": "#ad3da4",
      "strings": "#d12f1b",
      "functions": "#272ad8",
      "comments": "#536579"
    }
  }
}
```

## Screenshots

### Swift Development
```swift
import UIKit

// MARK: - View Controller
class ViewController: UIViewController {
    @IBOutlet weak var titleLabel: UILabel!
    
    override func viewDidLoad() {
        super.viewDidLoad()
        setupUI()
    }
    
    private func setupUI() {
        titleLabel.text = "Hello, Xcode!"
        titleLabel.textColor = .systemBlue
    }
}
```

### JavaScript/TypeScript
```typescript
// Modern JavaScript with TypeScript
interface User {
    id: number;
    name: string;
    email?: string;
}

class UserManager {
    private users: User[] = [];
    
    async fetchUser(id: number): Promise<User | null> {
        const response = await fetch(`/api/users/${id}`);
        return response.ok ? response.json() : null;
    }
    
    addUser(user: User): void {
        this.users.push(user);
    }
}
```

### Python
```python
# Python with decorators and type hints
from typing import List, Optional
from dataclasses import dataclass

@dataclass
class Person:
    name: str
    age: int
    email: Optional[str] = None
    
    def __post_init__(self):
        if self.age < 0:
            raise ValueError("Age cannot be negative")

def process_people(people: List[Person]) -> List[str]:
    """Process a list of people and return their names."""
    return [person.name for person in people if person.age >= 18]
```

## Changelog

### Version 1.0.0 (Latest)
- 🎉 Initial release of Xcode Light Theme
- 🎨 Faithful recreation of Xcode's default light theme color palette
- 🗂️ Xcode-style project navigator layout with enhanced sidebar colors
- 🔍 Enhanced syntax highlighting for multiple programming languages
- 📝 Language-specific rules for Swift, Objective-C, JavaScript/TypeScript, and Python
- 🖥️ Complete UI theme with carefully crafted colors for sidebar, activity bar, tabs
- ✨ Optimized for readability and developer productivity
- 🎯 Perfect color matching with Xcode's original light theme

## Support

### Issues and Bug Reports

If you encounter any issues or have suggestions for improvements:

1. Check the [existing issues](https://github.com/yugosdex/xcode-light-theme/issues) first
2. If your issue is new, [create a new issue](https://github.com/yugosdex/xcode-light-theme/issues/new)
3. Provide detailed information including:
   - VS Code/Trae version
   - Operating system
   - Steps to reproduce the issue
   - Screenshots if applicable

### Feature Requests

Have an idea for a new feature? We'd love to hear it!

- [Submit a feature request](https://github.com/yugosdex/xcode-light-theme/issues/new?labels=enhancement)
- Describe your use case and how it would benefit other users

### Community

- ⭐ Star this repository if you find it useful
- 🐛 Report bugs and issues
- 💡 Suggest new features
- 📖 Improve documentation

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Apple for the beautiful Xcode design inspiration
- The VS Code community for theming guidelines
- Trae IDE for providing an excellent development platform

---

**Note**: This theme is not an official Apple product and is not endorsed by Apple Inc.