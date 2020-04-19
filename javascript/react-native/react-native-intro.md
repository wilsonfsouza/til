<h1 align="center">
    <img height=50 alt="idea" src="https://reactnative.dev/img/header_logo.svg" />
    <br>
    Intro to React Native
</h1>

<h3 align="center">Overview</h3>
<p align="center">
  <a href="#what-is-it">What is it?</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#how-it-works">How it works?</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#syntax">Syntax</a>
</p>

# What is it?
- It is a version of React for mobile development.

- It offers a multiplatform approach since the application that is written in JavaScript will work in both iOS and Android.

- It can achieve that by injecting a tool that allows our phone to understand the code written in JavaScript.

- It allows us to take a different approach for each platform if needed.

# How it works?

> In summary, it transforms JavaScript code into a native interface/view for our phones.

<center>

|Steps | Activity Summary |
| --- | ---|
| Reading | JS --> Metro Bundler |
| Transforming | Metro Bundler --> bundle.js |
| Converting | bundle.js --> Bridge APIs |
| Interpreting | Bridge APIs --> iOS or Android |

</center>

`Metro bundler (packager)` = It is responsible for monitoring all changes in the JavaScript code and transforming it into a **bundle.js** file. It does a similar job as the `webpack` package used in ReactJs for web development.

`Bridge API` = It connects our bundle.js to the native code, "converting" the code into iOS or Android native format.

# Syntax

### Example: Creating a Button Component

:heavy_check_mark: Import React<br>
:heavy_check_mark: Import View, TouchableOpacity, and Text components from react-native<br>
:heavy_check_mark: Declare Styles Object<br>
:heavy_check_mark: Add parameters for styling<br>
:heavy_check_mark: Create a function to return the Component<br>
:heavy_check_mark: Use react-native components to create your button component<br>

```javascript
import React from 'react';
import {
    StyleSheet,
    View,
    Text,
    TouchableOpacity
} from 'react-native';

const styles = StyleSheet.create({
    container: {
        alignItems: 'center',
    },

    button: {
        backgroundColor: '#7159c1',
    },

    text: {
        fontWeight: 'bold',
    },
});

export default function Button() {
    return (
        <View style={styles.container}>
            <TouchableOpacity style={styles.button}>
                <Text style={styles.text}>Send</Text>
            </TouchableOpacity>
        </View>
    );
}

```

See the [React Native
Documentation](https://reactnative.dev/docs/getting-started) for more details.

---
Made with :heart: by Wilson Franca :wave: [Get in touch!](https://www.linkedin.com/in/wilsonfranca-env-engineer/)










