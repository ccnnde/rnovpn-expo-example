# Example of RNOvpn Module for Expo

This is an example (Android only) of the [RNOvpn Module](https://github.com/ccnnde/react-native-simple-openvpn) for an [Expo](https://expo.dev/) project created with [`create-expo-app`](https://www.npmjs.com/package/create-expo-app)

## Get started

1. Install dependencies

   ```bash
   npm install
   ```

2. Add the OpenVPN configuration file and import the `jniLibs` by following the instructions in the [RNOvpn Module](https://github.com/ccnnde/react-native-simple-openvpn) README

   ```tsx
   // app/(tabs)/ovpn.tsx
   async function startOvpn() {
     try {
       await RNSimpleOpenvpn.connect({
         remoteAddress: '',
         ovpnFileName: 'xxx', // your ovpn file name
         assetsPath: 'ovpn/',
         providerBundleIdentifier: 'com.example.RNSimpleOvpnExpoTest.NEOvpn',
         localizedDescription: 'RNSimpleOvpnExpo'
       });
     } catch (error) {
       updateLog(error);
     }
   }
   ```

3. Start the app

   ```bash
   npm run android
   ```
