# mix-react-native-mobile
React Native mobile NPM and demonstration mobile app

# Use google codespaces to develop for iOS and Android with the AwesomeProject
Just open the project with codespaces and edit the config.json file in your android/app/src/main/assets folder as well as ios/config.json to contain the client_id and client_secret you get when logging into mix.nuance.com

You'll also want to create a login at expo.dev and download the expo app to your handset. Don't worry the free account is all you need.

Once you've done that you need a terminal where you can login to expo and run `eas build` as shown below. It will provide a QR code that allows you to install the dev client on your device. The next step is to open another terminal window and run `./AwesomeProject/node_modules/.bin/ngrok http 3000` to provide a tunnel through which you will load you javascript bundle during development. You only need to run the `eas build` step if you change the underlying native code. 

setting up expo is easy 
https://youtu.be/id0Im72UN6w


## Check expo build queue and process here [ free tier 8-/ ]
https://docs.expo.dev/build-reference/troubleshooting/

```
@cleblanc-nuance ➜ /workspaces/mix-react-native-mobile (main) $ expo login
WARNING: The legacy expo-cli does not support Node +17. Migrate to the versioned Expo CLI (npx expo).
✔ Username/Email Address: … christopher.j.leblanc@gmail.com
✔ Password: … ***********

@cleblanc-nuance ➜ /workspaces/mix-react-native-mobile/AwesomeProject (main) $ eas build --profile development

Success. You are now logged in as cleblanc189.
✔ Select platform › All
Specified value for "android.package" in app.json is ignored because an android directory was detected in the project.
EAS Build will use the value found in the native code.

🤖 Android build
✔ Using remote Android credentials (Expo server)
✔ Using Keystore from configuration: Build Credentials 9e78kLJqNr (default)

Compressing project files and uploading to EAS Build. Learn more
✔ Compressed project files 4s (18.7 MB)
✔ Uploaded to EAS 
Specified value for "ios.bundleIdentifier" in app.json is ignored because an ios directory was detected in the project.
EAS Build will use the value found in the native code.

🍎 iOS build
✔ Using remote iOS credentials (Expo server)

If you provide your Apple account credentials we will be able to generate all necessary build credentials and fully validate them.
This is optional, but without Apple account access you will need to provide all the missing values manually and we can only run minimal validation on them.
✔ Do you want to log in to your Apple account? … yes

› Log in to your Apple Developer account to continue
✔ Apple ID: … christopher.j.leblanc@gmail.com
› Restoring session /home/node/.app-store/auth/christopher.j.leblanc@gmail.com/cookie
› Team Chris LeBlanc (C8UGF323HP)
› Provider Chris LeBlanc (126232895)
✔ Switched to provider: Chris LeBlanc (126232895)
✔ Logged in Local session
✔ Bundle identifier registered com.nuance.AwesomeProject
✔ Synced capabilities: No updates
✔ Synced capability identifiers: No updates
✔ Fetched Apple distribution certificates
✔ Fetched Apple provisioning profiles

Project Credentials Configuration

Project                   @cleblanc189/AwesomeProject
Bundle Identifier         com.nuance.AwesomeProject
                          
App Store Configuration   
                          
Distribution Certificate  
Serial Number             7E65E190EFF944F53800823408821491
Expiration Date           Sat, 06 Apr 2024 19:31:51 UTC
Apple Team                C8UGF323HP (Chris LeBlanc (Individual))
Updated                   11 days ago
                          
Provisioning Profile      
Developer Portal ID       2ZDK5A2RWX
Status                    active
Expiration                Sat, 06 Apr 2024 19:31:51 UTC
Apple Team                C8UGF323HP (Chris LeBlanc (Individual))
Updated                   11 days ago
                          
All credentials are ready to build @cleblanc189/AwesomeProject (com.nuance.AwesomeProject)


Compressing project files and uploading to EAS Build. Learn more
✔ Compressed project files 2s (18.7 MB)
✔ Uploaded to EAS 

🤖 Android build details: https://expo.dev/accounts/cleblanc189/projects/AwesomeProject/builds/8d15b6a9-a843-4aef-a9d3-4c72b810c603
🍎 iOS build details: https://expo.dev/accounts/cleblanc189/projects/AwesomeProject/builds/76de2e77-1ef9-40e7-8be4-bb66490de3b8

⠙ Waiting for builds to complete. You can press Ctrl+C to exit.
  🤖 Android build - status: finished

✔ 🤖 Android build - status: finished
  🍎 iOS build - status: finished
🤖 Android app:
https://expo.dev/artifacts/eas/iqsMrcah58gCsVkdcTswC4.aab

🍎 iOS app:
https://expo.dev/artifacts/eas/fFkRjGAM7mYxQJHZupokAY.ipa
Waiting for build to complete. You can press Ctrl+C to exit.

  ▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
  █ ▄▄▄▄▄ █▀▀▀ ▀  ▄█▄▀ ▀█▀  ▀▀▄▄█▄▀█▀▀  ▀▀▀ █ ▄▄▄▄▄ █
  █ █   █ █▀▄▀▄▀▀ █▄ ▀▀▀▄█▀▀▀▄▄▄▄▀▀▄█▄█▀▀█ ▄█ █   █ █
  █ █▄▄▄█ █▀ ▀▄▀█▀▄█ ▀ █▄ ▄▄▄  █▀▄█▄▀▀▀ ▄▀███ █▄▄▄█ █
  █▄▄▄▄▄▄▄█▄█ ▀▄█▄▀▄█ █ █ █▄█ ▀ ▀▄█ █▄▀▄▀▄▀ █▄▄▄▄▄▄▄█
  █▄  ▄▄█▄ ▄▄██▄▄▀ ▄ ▄▀▄▄▄  ▄▄▀█▄ ▄▀ █▀▄ ██▄▄▀ ▀ █ ██
  █  ▄▀ ▀▄█ ▄▀▄ ▀█▀▀▄  █ ▄▄██▄█▀ █▀▀█ ▄▄▀  ▄▄▀ ▀▀▄▀ █
  ██   ▀█▄ █ ▄▀▄▀█▄▀█ ▀▄▄ ▄  ███   ███   ▄▄▄▄▀ █▄▄ ▄█
  █▀  ▀▄█▄ ▀▀ ██▄█▄ ▀▄▀▀▄▄▄▄▀  ▀██▄▀▄▄▀▄█ ▄█▄▀ ▀▄▄  █
  █▄▄▄▀▀▀▄ ██ █▀▀▀▀▄█▄▀▄▄  ▄▀▄█▀▀  █ █▀  █▄▄ ▀█▀▄ ▄██
  █▄▀   █▄█▀▄ ▀ ▄  █▄██ █▄▄█▀▄▀▀██▀▀ ▄▄▄▀ █ ██▄▀██  █
  █▄▄▄▀▄ ▄ ▀▄▄▀▄▄▄▀█▄▀▀▄▀ ▄▄▄██▀▀  ▀██ ▄█▄█▄█▀ ▀█▄███
  █▀▀▄  ▄▄▄  █▀▄ ▀▀█ ███▄ ▄▄▄ █ ▄▀█ ▄  █  █ ▄▄▄  █▄ █
  █ ▀▀█ █▄█ ▀ ▄▄▀▀▀▄▄▄▀▄▄ █▄█ ▄█▄ ▄█▀██▄▀█  █▄█  ▄ ▄█
  █▄█▄▀▄ ▄▄ ▄▄▀▀▀█▀▀▀   ▀▄ ▄  ▀▀ ▀ ▀█ █▄▀ ▄▄▄▄▄▄█▄▀ █
  █  ▄▄██▄▀▀▀▄▀▄▀█▄▀▀  ▄▀▄█▀ █▄▀▀ ██▄▄▄  █  █▄▀▄▄  ██
  █▄▀█▀▄▀▄██▀▄▄▄▀▀▄ ▀ ▀ ▀▀   ▀█ ▄▀ ▀▄▄ █▀▄▄▀▀▄▀▄▀█  █
  █▄▄▄▀▄ ▄▀███  █▀▀▄▄▄▀▄▀▄█▀▄▀▄██▀▀█▀▄█▄▀█ ▄ █▀▄█▄███
  ██ █▀█▄▄█ ▀ █ ▄ ▀▀▄██▄▀▄ █▀▀   ▀  ▀ █▄ ▄▄▄█▄▄▀███▄█
  █▄▄ ▀▀▄▄▀  █▄ ▄▄▀█▄▀█▄▀█▀▀█▄ ▀▀  ▀██▄▄▀█  ▄▄▀▄▀▄▄▄█
  ██ ▀▀█▄▄▀█▀█▄  ▄▀█▀▄▀█▀██▄ ▀▄  ▀█▀▄▄ ██▄▄▀▄▄▀█▀█▄▄█
  █▄▄▄███▄▄▀▀▄▄▀▀▀▀▄▀▄ ▄▀ ▄▄▄ ▄▀█ █▀▀█▀ ▄▄▄ ▄▄▄ ▀▄ ██
  █ ▄▄▄▄▄ █▄█ █▀▀█▄▄▀ ██▀ █▄█ ▄▀█▀▀▀█▄██▀ █ █▄█ ▄▄▀ █
  █ █   █ █   ▀▄▀█▄▀▀  ▄█ ▄▄▄▄▄▀▀  █▄▄ ▄ ▄▀  ▄▄ ▀▄▄▄█
  █ █▄▄▄█ █  ▄▀█▄█▄ ▀▄▄▄█ ▄ ▄▄▄▀ █ ▀▄▄ ▄  ██▄▀▄▀▀██▀█
  █▄▄▄▄▄▄▄█▄█▄▄███▄▄▄▄▄▄███▄▄▄▄█▄▄███▄█▄▄▄▄█▄█▄██▄▄▄█


🍎 Open this link on your iOS devices (or scan the QR code) to install the app:
https://expo.dev/accounts/cleblanc189/projects/AwesomeProject/builds/922575d4-7572-4abd-8a24-3957df1e638e

@cleblanc-nuance ➜ /workspaces/mix-react-native-mobile (main) $ npx expo start --tunnel --dev-client
Starting project at /workspaces/mix-react-native-mobile/AwesomeProject
Starting Metro Bundler
Tunnel connected.
Tunnel ready.
▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
█ ▄▄▄▄▄ █▄▀ ▀ █ ██  ▄▄██ ▀█ █ █ ▄▄▄▄▄ █
█ █   █ █   █▀ ▄█ ▀▄▀▄█ ▀▄ ▀▄██ █   █ █
█ █▄▄▄█ █▄█▀ ▄▄ ▄▀ █ ▀█▄██  ▄ █ █▄▄▄█ █
█▄▄▄▄▄▄▄█▄█ █ █ █▄▀ ▀ █▄▀ █▄█ █▄▄▄▄▄▄▄█
█▄  ▄██▄▀▄▀ ▄ █▄██ ▀▀▀ ▀ ██▄▄  ██▄▄▄▀▄█
██ ▄█▄█▄▄█▄▀▄▄▀▀█▀█▄▀██  █▀▀█▄▄ █▄  ▀██
█▄█▀▄▀▀▄█▀▄▀▀  ▄▀▄ █ ██ █▀   ▀▀    ▄▀ █
████▄██▄ ▀▄█ █▄██ ▄█  ▀▄█▄█▄█  ▄█▄▄▄ ██
████▄▄ ▄▄█▄▀█▄ ▀ ▀▀▄█▀▄▀   ▀▀▄▄▀██▄ ▄ █
█▄▄▄▀▀█▄  █ ▀██▀▄▄▀██▀▄ █▀█ ▄ ▄▀ ▀▀▄▀▄█
█ ▀█ ▀▄▄█▄▄███▀█▄█▄ ▀     ▀██ ▄█ ▄█▀▀██
█ ██▀█ ▄▄ ▀▄▀▀ ██▀▄ █ ▄█  ▀▀██▀█▀▀  ███
█▄ ▄██ ▄▄▄▄▀ ▄▄ ▀▄ ███▄▄▄▄▄  ▀▄ ▀   █▀█
█▀▄▄▀ ▄▄ ▄▄▄██▄▄▀█▄▀ █▀ ███▀▀▀█ ▀ ▄▄ ▀█
████▄█▄▄▄ █   ▄█▀ ▀▄██▄▀  ▄█▄ ▄▄▄ ▀ █▀█
█ ▄▄▄▄▄ ██ ▀████ ▄▀██▄▄ █ █ █ █▄█ ▀█  █
█ █   █ █▀▄▀▀██ █ ▄  █   █▀▄█   ▄  ████
█ █▄▄▄█ █ ▄█▄  ▄▀█▄▀█ ▄▀▄ ▀ ▄▄█▄  ▀▀███
█▄▄▄▄▄▄▄█▄▄██▄▄▄██▄███▄▄█▄▄▄███▄███▄▄▄█

› Metro waiting on exp+awesomeproject://expo-development-client/?url=http%3A%2F%2Fxwikomc.cleblanc189.8081.exp.direct
› Scan the QR code above with Expo Go (Android) or the Camera app (iOS)

› Press a │ open Android
› Press w │ open web

› Press j │ open debugger
› Press r │ reload app
› Press m │ toggle menu

› Press ? │ show all commands

Logs for your project will appear below. Press Ctrl+C to exit.
› Reloading apps

```
## To Learn more about the native code see the README.md in ./AwesomeProject/react-native-nuance-mix
### The Android and iOS native code is in the react-native-nuance-mix folder is implemented in Java and Objective-C respectively
### The components provided by the native plugin react-native-nuance-mix are used in the App.js file in the root of the project. 