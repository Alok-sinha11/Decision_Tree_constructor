# Decision_Tree_constructor
A complete Decision Tree constructor built using C++ for backend processing and a frontend interface for user interaction. This project automatically generates an ID3 Decision Tree based on any dataset and attributes provided by the user.
# 🌳 Decision Tree Generator

A modern, interactive web application for generating decision trees using the **ID3 algorithm**. Built with vanilla HTML, CSS, and JavaScript, featuring a beautiful dark-themed UI with real-time visualization.

![Decision Tree Generator](https://img.shields.io/badge/Algorithm-ID3-blue) ![License](https://img.shields.io/badge/License-MIT-green) ![Status](https://img.shields.io/badge/Status-Active-success)

## ✨ Features

- **🎯 ID3 Algorithm Implementation** - Classic decision tree algorithm using Information Gain and Entropy
- **📊 Visual Tree Rendering** - Interactive SVG-based tree visualization with node labels and connections
- **📝 ASCII Tree Output** - Text-based tree representation for easy reading and copying
- **📈 Real-time Statistics** - View tree metrics including node count, depth, and root entropy
- **📋 Copy to Clipboard** - One-click copy of the generated tree
- **📱 Share via WhatsApp** - Share your results directly to WhatsApp
- **🎨 Modern UI** - Beautiful dark theme with gradient accents and glassmorphism effects
- **📱 Responsive Design** - Fully responsive layout that adapts to all screen sizes
- **🎲 Preset Datasets** - Quick-start with example datasets (Play Tennis, Weather prediction)
- **⚡ Real-time Generation** - Instant tree generation as you type

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- No server or installation required!

### Installation

1. Clone or download this repository:
```bash
git clone <repository-url>
cd "DECISION TREE"
```

2. Open `dtree.html` in your web browser:
   - Simply double-click the file, or
   - Right-click → Open with → Your preferred browser

That's it! The application runs entirely in your browser with no dependencies.

## 📖 Usage Guide

### Basic Usage

1. **Enter Attributes**: Input your feature names separated by commas
   - Example: `Outlook,Temperature,Humidity,Play`
   - ⚠️ **Note**: The last attribute is treated as the target/class label

2. **Enter Dataset**: Provide your data rows, one per line
   - Each row should have values matching the attributes
   - Example:
     ```
     Sunny,Hot,High,No
     Sunny,Mild,High,No
     Overcast,Hot,High,Yes
     ```

3. **Generate Tree**: Click the "Generate Tree" button

4. **View Results**: 
   - See the ASCII tree representation
   - View the visual SVG tree diagram
   - Check statistics (nodes, depth, entropy)

### Using Presets

Select a preset dataset from the dropdown menu:
- **Play Tennis (classic)** - Classic decision tree example
- **Weather (rain?)** - Weather prediction dataset
- **Custom input** - Use your own data

### Sharing Results

- **Copy Output**: Click "Copy Output" to copy the ASCII tree to clipboard
- **Share WhatsApp**: Click "Share WhatsApp" to share the tree and website link via WhatsApp

## 🧮 How ID3 Algorithm Works

The ID3 (Iterative Dichotomiser 3) algorithm builds decision trees using:

1. **Entropy Calculation**: Measures the impurity of a dataset
   ```
   H(S) = -Σ p(x) × log₂(p(x))
   ```

2. **Information Gain**: Determines the best attribute to split on
   ```
   Gain(S, A) = H(S) - Σ (|Sv|/|S|) × H(Sv)
   ```

3. **Recursive Splitting**: 
   - Selects the attribute with highest information gain
   - Splits the dataset based on attribute values
   - Recursively builds subtrees for each split
   - Stops when all samples belong to the same class (pure node)

## 📊 Output Format

### ASCII Tree
```
└── Outlook
    [Sunny]
    └── Humidity
        [High]
        └── (class) No
        [Normal]
        └── (class) Yes
    [Overcast]
    └── (class) Yes
    [Rain]
    └── (class) Yes
```

### Visual Tree
- **Purple gradient circles**: Decision nodes (attributes)
- **Green circles**: Leaf nodes (class labels)
- **Gray lines**: Tree branches with attribute values

### Statistics
- **Nodes**: Total number of nodes in the tree
- **Depth**: Maximum depth of the tree
- **Entropy (root)**: Entropy of the root node

## 🎨 Features in Detail

### Visual Feedback
- Buttons flash with success colors when clicked
- Smooth transitions and hover effects
- Responsive grid layout adapts to screen size

### Data Validation
- Automatic trimming of whitespace
- Handles empty rows gracefully
- Clear error messages for invalid input

## 📁 Project Structure

```
DECISION TREE/
│
├── dtree.html          # Main application file (all-in-one)
└── README.md           # This file
```

## 🛠️ Technical Details

### Technologies Used
- **HTML5** - Structure and semantic markup
- **CSS3** - Modern styling with CSS Grid, Flexbox, and custom properties
- **Vanilla JavaScript** - No frameworks or dependencies
- **SVG** - Scalable vector graphics for tree visualization

### Browser Compatibility
- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Opera (latest)

### Performance
- Lightweight: Single HTML file (~20KB)
- Fast: Client-side processing, no server calls
- Efficient: Optimized tree rendering algorithm

## 🔧 Customization

### Changing Colors
Edit the CSS variables in the `:root` section:
```css
:root {
    --bg: #0f172a;           /* Background color */
    --accent: #7c3aed;       /* Primary accent */
    --accent-2: #10b981;     /* Secondary accent */
    --text: #e2e8f0;         /* Text color */
}
```

### Adding Presets
Add new presets in the JavaScript `presets` object:
```javascript
const presets = {
    yourPreset: {
        attrs: "Attr1,Attr2,Class",
        data: `value1,value2,class1\nvalue3,value4,class2`
    }
};
```

## 📝 Example Datasets

### Play Tennis Dataset
```
Attributes: Outlook,Temperature,Humidity,Windy,Play
14 samples with weather conditions and play decision
```

### Weather Dataset
```
Attributes: Outlook,Temp,Humidity,Wind,RainTomorrow
14 samples predicting rain based on weather conditions
```

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- ID3 Algorithm by Ross Quinlan
- Inspired by classic machine learning examples
- Built with modern web technologies

## 📞 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check the code comments for implementation details

---

**Made with ❤️ using vanilla JavaScript**

*Last updated: 2024*

