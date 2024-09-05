# SDK

Here's a detailed list of CLI commands for SDK tools, focusing on various aspects of development and management.

### **1. Android SDK (SDK Manager and ADB)**

#### **SDK Manager**

- **List installed and available packages:**
  ```sh
  sdkmanager --list
  ```

- **Install packages:**
  ```sh
  sdkmanager "platform-tools" "platforms;android-30" "build-tools;30.0.3"
  ```

- **Update all installed packages:**
  ```sh
  sdkmanager --update
  ```

#### **ADB (Android Debug Bridge)**

- **List connected devices:**
  ```sh
  adb devices
  ```

- **Install an APK on a device:**
  ```sh
  adb install app_name.apk
  ```

- **Uninstall an app from a device:**
  ```sh
  adb uninstall package_name
  ```

- **View device logs (Logcat):**
  ```sh
  adb logcat
  ```

- **Push a file to the device:**
  ```sh
  adb push local_file_path /sdcard/remote_file_path
  ```

- **Pull a file from the device:**
  ```sh
  adb pull /sdcard/remote_file_path local_file_path
  ```

- **Reboot the device:**
  ```sh
  adb reboot
  ```

- **Enter the device shell:**
  ```sh
  adb shell
  ```

#### **AVD Manager**

- **List available AVDs:**
  ```sh
  avdmanager list avd
  ```

- **Create a new AVD:**
  ```sh
  avdmanager create avd -n my_avd -k "system-images;android-30;google_apis;x86"
  ```

- **Delete an AVD:**
  ```sh
  avdmanager delete avd -n my_avd
  ```

- **Start an AVD:**
  ```sh
  emulator -avd my_avd
  ```

### **2. iOS SDK (Xcode Command Line Tools)**

#### **xcodebuild**

- **Build a project:**
  ```sh
  xcodebuild -project ProjectName.xcodeproj -scheme SchemeName -configuration Release
  ```

- **Clean a project:**
  ```sh
  xcodebuild clean -project ProjectName.xcodeproj -scheme SchemeName
  ```

- **Archive a project:**
  ```sh
  xcodebuild archive -project ProjectName.xcodeproj -scheme SchemeName -archivePath ArchiveName.xcarchive
  ```

- **Export an IPA:**
  ```sh
  xcodebuild -exportArchive -archivePath ArchiveName.xcarchive -exportOptionsPlist ExportOptions.plist -exportPath ExportPath
  ```

#### **simctl (Simulator Control Tool)**

- **List available simulators:**
  ```sh
  xcrun simctl list
  ```

- **Boot a simulator:**
  ```sh
  xcrun simctl boot device_udid
  ```

- **Shutdown a simulator:**
  ```sh
  xcrun simctl shutdown device_udid
  ```

- **Install an app on a simulator:**
  ```sh
  xcrun simctl install device_udid app_name.app
  ```

- **Open a URL in a simulator:**
  ```sh
  xcrun simctl openurl device_udid http://example.com
  ```

### **3. .NET SDK (dotnet CLI)**

- **Install the .NET SDK:**
  ```sh
  sudo apt-get install dotnet-sdk-6.0
  ```

- **Check installed SDKs:**
  ```sh
  dotnet --list-sdks
  ```

- **Check installed runtimes:**
  ```sh
  dotnet --list-runtimes
  ```

- **Create a new console application:**
  ```sh
  dotnet new console -n MyConsoleApp
  ```

- **Build a project:**
  ```sh
  dotnet build
  ```

- **Run a project:**
  ```sh
  dotnet run
  ```

- **Add a package to a project:**
  ```sh
  dotnet add package PackageName
  ```

- **Publish a project:**
  ```sh
  dotnet publish -c Release -o ./publish
  ```

This list covers the primary CLI commands for managing and utilizing various SDK tools, including Android SDK, iOS SDK, .NET SDK.
