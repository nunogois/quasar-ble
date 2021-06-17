# Quasar BLE (quasar-ble)

Quasar Framework BLE (Bluetooth Low Energy) App Example.

Built using <a href="https://quasar.dev/">Quasar Framework</a> - A <a href="https://vuejs.org/">VueJS</a> framework.

Also <a href="https://capacitorjs.com/">Capacitor v3</a> and the Capacitor Community plugin <a href="https://github.com/capacitor-community/bluetooth-le">bluetooth-le</a>.

<p align="center">
  <a href="https://github.com/nunogois/quasar-ble/blob/master/demo_screenshots/quasar-ble.png?raw=true"><img src="https://github.com/nunogois/quasar-ble/blob/master/demo_screenshots/quasar-ble.png?raw=true" height="600" /></a>
</p>

# ✨ Features

- 100% cross-platform with a single open-source codebase
  - Note: In this specific case it only makes sense to build for mobile since we're using BLE and browser support is still behind
- BLE - Bluetooth Low Energy
- Composition API
- Capacitor v3

<br />

# 👨‍💻 &nbsp;Using

![Quasar Framework](https://img.shields.io/badge/-Quasar%20Framework-141321?style=flat&logo=quasar&logoColor=1976D2)&nbsp;
![Capacitor (Mobile)](<https://img.shields.io/badge/-Capacitor%20(Mobile)-141321?style=flat&logo=Capacitor&logoColor=119EFF>)&nbsp;
![TypeScript](https://img.shields.io/badge/-TypeScript-141321?style=flat&logo=TypeScript&logoColor=3178C6)&nbsp;
![Sass (indented syntax)](<https://img.shields.io/badge/-Sass%20(indented%20syntax)-141321?style=flat&logo=Sass&logoColor=CC6699>)&nbsp;
![ESLint](https://img.shields.io/badge/-ESLint-141321?style=flat&logo=ESLint&logoColor=4B32C3)&nbsp;
![Prettier](https://img.shields.io/badge/-Prettier-141321?style=flat&logo=Prettier&logoColor=F7B93E)&nbsp;

### And also...

- Lottie

[Bestdit icon](https://www.flaticon.com/free-icon/trophy_3112946) made by <a href="https://www.freepik.com" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a>

Free animated illustrations from [LottieFiles](https://lottiefiles.com/)

<br />

# 🔨 &nbsp;Builds

## [Capacitor - Mobile (Android, iOS)](https://quasar.dev/quasar-cli/developing-capacitor-apps/introduction)

With a simple command we can issue a mobile build from this code base.

Since I don't have a Mac with me at the moment, I've only built the Android version (APK).

The APK is currently being built targeting Android SDK 29. However, since it has a minSdkVersion parameter of 21, any Android 5.0+ should be able to run the app.

If you wish to build for iOS, simply follow the steps in the Quasar documentation.

# 📌 To Do

- [x] Upgrade Capacitor to v3
- [x] Implement capacitor-community/bluetooth-le
- [x] Scan and list the results
- [x] Result component
- [x] Welcome component
- [x] Add Lottie
- [x] GitHub repo
- [x] Add meta tags
- [ ] App icon
- [ ] Setup builds (PWA, Windows, Android, etc)
