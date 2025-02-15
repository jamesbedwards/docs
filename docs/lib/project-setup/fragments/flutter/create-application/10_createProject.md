**Open Android Studio.**  Select **+ Start a new Flutter project**

![](~/images/lib/getting-started/flutter/set-up-android-studio-welcome.png)

 In **Select a Project Template**, select **Flutter Application**. Press **Next**.

Next, configure your project:

1. Enter *MyAmplifyApp* in the **Name** field
2. Make sure your Flutter SDK path is set correctly to where it is installed on your machine 
3. Press **Next**. On the next screen, press **Finish**. 

  ![](~/images/lib/getting-started/flutter/set-up-android-studio-configure-your-project.png)

Android Studio will open your project with a tab opened to *main.dart*

<amplify-callout warning>

If you are using Flutter (2.2.0), you need to disable sound null safety by following the instructions [here](https://dart.dev/null-safety/unsound-null-safety#testing-or-running-mixed-version-programs). Null safety support for Amplify Flutter is being worked on actively.

</amplify-callout>

If you use CocoaPods, modify your Podfile to target iOS platform 11.0 or higher.  Within your project open `ios/Podfile` and change the second line to be `platform :ios, '11.0'.

```bash
sudo gem install cocoapods

# make sure you are in the ios folder
pod init
```

In XCode, select your project in the Project Navigator and select the "Info" tab.  Set the Deployment Target to at least 11.0.

  ![](~/images/lib/getting-started/flutter/set-up-xcode-deployment-target.png)

You now have an empty Flutter project into which you'll add Amplify in the next steps.
