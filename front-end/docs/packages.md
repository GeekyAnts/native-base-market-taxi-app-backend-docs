# Packages Used

_package.json_

<pre class="line-numbers"><code class="language-json">
{
  "name": "TaxiApp",
  "version": "7.0.0",
  "private": true,
  "dependencies": {
    "lodash": "^4.13.1",
    "moment": "^2.17.1",
    "native-base": "2.1.0-rc.2",
    "expo": "^15.1.0",
    "react": "~15.4.0",
    "react-native": "0.42.3",
    "react-native-country-picker-modal": "^0.2.10",
    "react-native-easy-grid": "^0.1.8",
    "react-native-router-flux": "^3.38.0",
    "react-redux": "^5.0.3",
    "redux": "^3.6.0",
    "redux-persist": "^4.4.2",
    "redux-thunk": "^2.2.0",
    "replace": "0.3.0",
    "rx": "^4.1.0",
    "@exponent/vector-icons": "~4.0.0"
  },
  "devDependencies": {
    "react-native-scripts": "0.0.26",
    "jest-expo": "^0.3.0",
    "react-test-renderer": "~15.4.1",
    "babel-jest": "16.0.0",
    "babel-preset-react-native": "1.9.0",
    "chai": "^3.5.0",
    "jest": "16.0.2",
    "jest-react-native": "16.0.0",
    "mocha": "^2.5.3",
    "remote-redux-devtools": "^0.3.3",
    "remote-redux-devtools-on-debugger": "^0.4.6"
  },
  "main": "./node_modules/react-native-scripts/build/bin/crna-entry.js",
  "scripts": {
    "postinstall": "remotedev-debugger && node ./scripts/replace.js",
    "start": "react-native-scripts start",
    "eject": "react-native-scripts eject",
    "android": "react-native-scripts android",
    "ios": "react-native-scripts ios",
    "test": "node node_modules/jest/bin/jest.js --watch"
  },
  "jest": {
    "preset": "jest-expo"
  }
}</code></pre>
