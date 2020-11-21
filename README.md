# react-native-drawer-item-selector

The Package can be found at [react-native-drawer-item-selector](https://www.npmjs.com/package/react-native-drawer-item-selector).

Item Selector from given drawer component for React Native.

* Maximum Customization
* Max Lightweight Component
* No Dependency, Configuration
* Add Your own Component To Bottom Sheet
* Support Gesture
* Available for iOS and Android
* Smooth Animation
* Selector Shape Changeable(Dot, Square)
* Dynamically adjust Title and Items

<table>
        <tr>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704073-e2f7ac80-2abd-11eb-83fa-892078f2aeb1.PNG" height = "440" width="250"></td>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704092-e854f700-2abd-11eb-9600-afc0376163d1.PNG" height = "440" width="250"></td>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704183-09b5e300-2abe-11eb-852a-17a546ba72a1.PNG" height = "440" width="250"></td>
       </tr>
</table> 

<table>
        <tr>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704335-441f8000-2abe-11eb-9192-b1e45ec36ec4.PNG" height = "440" width="250"></td>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704375-513c6f00-2abe-11eb-9ed6-16c8c21f64f3.PNG" height = "440" width="250"></td>
<td><img src = "https://user-images.githubusercontent.com/35291991/99704303-323ddd00-2abe-11eb-9d71-d497ed51f083.PNG" height = "440" width="250"></td>
       </tr>
</table> 

## Installation

```
npm i react-native-drawer-item-selector --save
```

### or

```
yarn add react-native-drawer-item-selector
```
## Usage

#### Class component

```jsx
import React, { Component } from "react";
import { StyleSheet, View, Text, Button } from 'react-native';

import DrawerSelector from 'react-native-drawer-item-selector';

export default class App extends Component {
  render() {
    var setmodalVisible;
    const setDrawerSelector = (func) => {
      setmodalVisible = func;
    }
    return (
      <View style={styles.view}>
        <Text style={styles.text}>Hello World React Native!</Text>
        <Button
          onPress={() => { setmodalVisible(); }}
          title='Open Drawer'
        />
        <DrawerSelector data={[['1', 'Item 1', () => { console.log('Item 1 Selected') }], ['2', 'Item 2', () => { console.log('Item 2 Selected') }]]} setDrawerSelector={setDrawerSelector} />
      </View>
    );
  }
};

const styles = StyleSheet.create({
  view: {
    backgroundColor: '#d3d3d3',
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center'
  },
  text: {
    color: 'white'
  }
});
```

#### Functional component

```jsx
import React from 'react';
import { StyleSheet, View, Text, Button } from 'react-native';

import DrawerSelector from 'react-native-drawer-item-selector';

const App = () => {
  var setmodalVisible;
  const setDrawerSelector = (func) => {
    setmodalVisible = func;
  }
  return (
      <View style={styles.view}>
        <Text style={styles.text}>Hello World React Native!</Text>
        <Button
          onPress={() => { setmodalVisible(); }}
          title='Open Drawer'
        />
        <DrawerSelector data={[['1', 'Item 1', () => { console.log('Item 1 Selected') }], ['2', 'Item 2', () => { console.log('Item 2 Selected') }]]} setDrawerSelector={setDrawerSelector} />
      </View>
  );
};

const styles = StyleSheet.create({
  view: {
    backgroundColor: '#d3d3d3',
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center'
  },
  text: {
    color: 'white'
  }
});

export default App;
```

## Props

| Props            | Type     | Description                                             |
| ---------------- | -------- | ------------------------------------------------------- |
| setDrawerSelector| function   | Takes function setmodalVisible and set setmodalVisible = True whenever setmodalVisible() is called |
| backgroundColor    | string  | Sets Drawer Background color, Default = '#2c2c2e'   |
| selector | string   | Sets Selector type, takes only values = 'dot', 'square', Default = 'dot' |
| selectorColor     | string   | Sets Selector Color, Default = 'red'             |
| itemTextStyle    | object   | Sets text style for each item            |
| itemHeight  | number  | Sets Height of Each Row in drawer (Height of each item), Default = 60             |
| itemContainerStyle    | object   | Sets style for each item container            |
| seperatingLineColor  | string  | Sets seperating line color, Default = '#000000' |
| title | string  | Title of the Drawer, Default = 'Title'           |
| titleTextStyle | object  | Sets text style for title |
| titleContainerStyle | object  | Sets style for title container           |
| data          | array | Sets data for Drawer, at each index ['ID', 'Item Name', ()=>{  //Function to perform  }], Default = [['1', 'Item 1', () => { }], ['2', 'Item 2', () => { }]]          |


## License

This project is licensed under the MIT License - see [LICENSE.md](https://github.com/ansh-099/react-native-drawer-item-selector/blob/master/LICENSE.md) for details


## Author

Made by [Anshul Singh](https://github.com/ansh-099)
