
# react-native-haptic-feedback

## Getting started

`$ npm install react-native-haptic-feedback --save`

## Migrate from V1 to V2
- No Default import. Please use corresponding imports from the docs
- trigger() now only accepts an object of arguments according to docs.

Previously:
```javascript
import RNHapticFeedback from "react-native-haptic-feedback"
RNHapticFeedback.trigger('impactLight');
```

Now:
```javascript
import {HapticFeedback} from "react-native-haptic-feedback"
HapticFeedback.trigger({type: 'impactLight'})
```

### Linking

`$ react-native link react-native-haptic-feedback`

### Manual Linking


#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-haptic-feedback` and add `RNReactNativeHapticFeedback.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNReactNativeHapticFeedback.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainApplication.java`
  - Add `import com.reactlibrary.RNReactNativeHapticFeedbackPackage;` to the imports at the top of the file
  - Add `new RNReactNativeHapticFeedbackPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-haptic-feedback'
  	project(':react-native-haptic-feedback').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-haptic-feedback/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-haptic-feedback')
  	```

## Usage
```javascript
import ReactNativeHapticFeedback from 'react-native-haptic-feedback';

ReactNativeHapticFeedback.trigger('impactLight', true);
```

### Available methods HapticFeedback

#### trigger({type, enableVibrateFallback})
#### isHapticFeedbackAvailable({type, enableVibrateFallback})

### TouchableWithHapticFeedback Props

