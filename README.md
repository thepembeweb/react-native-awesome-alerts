<p align="center">
  <img alt="react-native-awesome-alerts" src="http://res.cloudinary.com/rishabhbhatia/image/upload/c_scale,w_200/v1504947704/awesome-alerts/react-native-awesome-alerts.png">
</p>

# React Native Awesome Alerts

### Demo [(Watch it on YouTube)](https://youtu.be/VIJYKUFpFCU)

![alt text](http://res.cloudinary.com/rishabhbhatia/image/upload/c_scale,w_200/v1505042954/awesome-alerts/v1.0.3/react-native-awesome-alerts.gif)


## Getting Started

- [Installation](#installation)
- [Basic Usage](#basic-usage)
- [Properties](#properties)

### Installation
```bash
$ npm i react-native-awesome-alerts --save
```

### Basic Usage
```jsx
import React from 'react';
import { StyleSheet, View, Text, TouchableOpacity } from 'react-native';

import AwesomeAlert from 'react-native-awesome-alerts';

export default class App extends React.Component {

  constructor(props) {
    super(props);
    this.state = { showAlert: false };
  };

  showAlert = () => {
    this.setState({
      showAlert: true
    });
  };

  hideAlert = () => {
    this.setState({
      showAlert: false
    });
  };

  render() {
    const {showAlert} = this.state;

    return (
      <View style={styles.container}>

        <Text>I'm AwesomeAlert</Text>
        <TouchableOpacity onPress={() => {
          this.showAlert();
        }}>
          <View style={styles.button}>
            <Text style={styles.text}>Try me!</Text>
          </View>
        </TouchableOpacity>

        <AwesomeAlert
          show={showAlert}
          showProgress={false}
          title="AwesomeAlert"
          message="I have a message for you!"
          closeOnTouchOutside={true}
          closeOnHardwareBackPress={false}
          showCancelButton={true}
          showConfirmButton={true}
          cancelText="No, cancel"
          confirmText="Yes, delete it"
          confirmButtonColor="#DD6B55"
          onCancelPressed={() => {
            this.hideAlert();
          }}
          onConfirmPressed={() => {
            this.hideAlert();
          }}
        />
      </View>
    );
  };
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
    backgroundColor: '#fff',
  },
  button: {
    margin: 10,
    paddingHorizontal: 10,
    paddingVertical: 7,
    borderRadius: 5,
    backgroundColor: "#AEDEF4",
  },
  text: {
    color: '#fff',
    fontSize: 15
  }
});

```
![alt text](http://res.cloudinary.com/rishabhbhatia/image/upload/c_scale,w_200/v1504950440/awesome-alerts/react-native-awesome-alerts-basic.gif)

### Properties

#### Basic

| Prop  | Type | Description | Default|
| :------------ |:---------------:| :---------------:| :-----|
| show | `boolean` | Show / Hide awesome alert | false |
| showProgress | `boolean` | Show / Hide progress bar | false |
| title | `string` | Title text to display | hidden |
| message | `string` | Message text to display | hidden |
| closeOnTouchOutside | `bool` | Dismiss alert on clicking outside | true |
| closeOnHardwareBackPress | `bool` | Dismiss alert on hardware back press (android) | true |
| showCancelButton | `bool` | Show a cancel button | false |
| showConfirmButton | `bool` | Show a confirmation button | false |
| cancelText | `string` | Cancel button text | Cancel |
| confirmText | `string` | Confirm button text | Confirm |
| cancelButtonColor | `string` | Background color for Cancel button | #D0D0D0 |
| confirmButtonColor | `string` | Background color for Confirm button | #AEDEF4 |
| onCancelPressed | `func` | Action to perform when Cancel is pressed | - |
| onConfirmPressed | `func` | Action to perform when Confirm is pressed | - |

## Contribution

- [@rishabhbhatia](mailto:rishabh.bhatia08@gmail.com) Author.

## Inspiration

Pedant: sweet-alert-dialog [(Github)](https://github.com/pedant/sweet-alert-dialog)

## Questions

Feel free to [Contact me](mailto:rishabh.bhatia08@gmail.com) or [Create an issue](https://github.com/rishabhbhatia/react-native-awesome-alerts/issues/new)

## License

Released under the [Mit License](https://opensource.org/licenses/MIT)
