
# react-native-ruler-picker

**RulerPicker** is a customizable horizontal ruler-style picker for React Native applications. It allows users to select values within a defined range using an intuitive scrolling interface. Perfect for weight, height, or any range-based selection.

![RulerPicker Demo](https://example.com/demo.gif) <!-- Replace with a demo image or GIF -->

## Features

- 📏 **Customizable scale**: Define min/max values and step sizes.
- 🎨 **Style options**: Fully customizable styles for lines, text, and ruler elements.
- 🚀 **Performance optimized**: Smooth scrolling and precise value selection.
- 📦 **Lightweight**: Easy to integrate into any React Native project.

## Installation

```bash
npm install react-native-ruler-picker
```

or

```bash
yarn add react-native-ruler-picker
```

## Usage

Here's how to use the **RulerPicker** in your React Native project:

```tsx
import React from 'react';
import { View } from 'react-native';
import RulerPicker from 'react-native-ruler-picker';

const App = () => {
  const handleValueChange = (value: number) => {
    console.log('Selected Value:', value);
  };

  return (
    <View style={{ flex: 1, justifyContent: 'center', alignItems: 'center' }}>
      <RulerPicker
        initialValue={70}
        minValue={10}
        maxValue={200}
        step={1}
        unit="Kg"
        onValueChange={handleValueChange}
      />
    </View>
  );
};

export default App;
```

## Props

| Prop                 | Type        | Default  | Description                                                                 |
|----------------------|-------------|----------|-----------------------------------------------------------------------------|
| `initialValue`       | `number`    | `68`     | Initial value displayed on the ruler.                                      |
| `minValue`           | `number`    | `8`      | Minimum value selectable on the ruler.                                     |
| `maxValue`           | `number`    | `230`    | Maximum value selectable on the ruler.                                     |
| `step`               | `number`    | `0.1`    | Step between consecutive scale values.                                     |
| `unit`               | `string`    | `"Kg"`   | Unit displayed next to the selected value.                                 |
| `onValueChange`      | `function`  | `null`   | Callback triggered when the selected value changes.                        |
| `rulerStyle`         | `ViewStyle` | `null`   | Style for the ruler container.                                             |
| `scaleItemStyle`     | `ViewStyle` | `null`   | Style for individual scale items.                                          |
| `lineStyle`          | `ViewStyle` | `null`   | Style for the line elements on the ruler.                                  |
| `textStyle`          | `TextStyle` | `null`   | Style for the text elements of scale values.                               |
| `unitStyle`          | `TextStyle` | `null`   | Style for the unit text (e.g., `"Kg"`).                                    |
| `centerLineStyle`    | `ViewStyle` | `null`   | Style for the center marker line of the ruler.                             |
| `scaleWrapperStyle`  | `ViewStyle` | `null`   | Style for the wrapper containing scale elements.                           |
| `weightTextStyle`    | `TextStyle` | `null`   | Style for the selected value text.                                         |
| `weightContainerStyle` | `ViewStyle` | `null`   | Style for the container displaying the selected value and unit.           |

## Customization

The **RulerPicker** is highly customizable. Use the provided style props to modify the appearance to suit your app's design.

For example:

```tsx
<RulerPicker
  initialValue={50}
  minValue={20}
  maxValue={100}
  unit="Kg"
  weightTextStyle={{ fontSize: 40, color: 'blue' }}
  centerLineStyle={{ backgroundColor: 'red', height: 80 }}
  lineStyle={{ backgroundColor: 'gray' }}
  textStyle={{ color: 'black', fontSize: 12 }}
  onValueChange={(value) => console.log(value)}
/>
```

## Example Output

```
Selected Value: 68
```

## License

This package is licensed under the [MIT License](./LICENSE).

---

### Contributing

We welcome contributions! Feel free to submit a pull request or open an issue for any bug fixes or feature suggestions.