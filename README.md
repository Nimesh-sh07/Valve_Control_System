# Valve Controller App (React Native + Expo Dev Client)

An Android app used to operate irrigation valves by sending commands over USB serial and showing the device's replies. Built as a team project during an internship at Ukshati Technologies.

## Features
- Connect to a USB serial device from the phone
- Pick a zone and switch individual valves on/off
- Flow-meter readings table (valve, status, reading in L/min)
- Live command log showing what was sent and received

## Tech
React Native 0.79, Expo SDK 53 (Dev Client), Expo Router, TypeScript, and a Kotlin native module (`UsbSerialModule`) built on `usb-serial-for-android`.

## Why Expo Dev Client
USB serial needs a native Android module, which Expo Go cannot load, so the project was migrated to a custom Dev Client.

## Run
```bash
npm install
npx expo run:android          # builds and installs the dev client on a connected Android phone
npx expo start --dev-client   # later runs
```
Enable USB debugging and accept the USB permission prompt on the phone.

## Project structure
```
app/                 screens and routes (Expo Router)
app/(tabs)/          valve controller and profile tabs
components/          shared UI components
android/             native Android project, including UsbSerialModule.kt
```

## Team
Shravan K, Rakshith R Poojary, Dinesh Raj Upadhya, Shetty Nimesh, Nishant U, for Ukshati Technologies. For internship and academic purposes.
