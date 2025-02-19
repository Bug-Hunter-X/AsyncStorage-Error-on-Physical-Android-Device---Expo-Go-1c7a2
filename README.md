# Expo AsyncStorage Error on Physical Android Device

This repository demonstrates a bug where AsyncStorage fails to access storage on a physical Android device when building an Expo app, but works correctly within the Expo Go Android emulator. The issue stems from inconsistencies between the emulator and physical device environments in terms of permissions and AsyncStorage implementation.

## Problem

The provided `bug.js` file contains a simple example of using AsyncStorage to store data. This code functions correctly in the Expo Go Android emulator. However, when building and installing the app on a physical Android device, `AsyncStorage.setItem` throws an error, indicating a failure to access storage.  The exact error message will vary but often points to a permission or path issue. 

## Solution

The solution, detailed in `bugSolution.js`, focuses on ensuring correct permissions and addressing possible implementation differences between emulators and physical devices. It may involve checking for specific Android permissions at runtime or employing alternative storage solutions where appropriate.