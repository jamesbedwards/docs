* A Flutter application targeting Flutter SDK >= 1.20 (stable version) with Amplify libraries integrated
    * An iOS configuration targeting at least iOS 11.0
    * An Android configuration targeting at least Android API level 21 (Android 5.0) or above
    * [Amplify Init](https://docs.amplify.aws/lib/project-setup/create-application/q/platform/flutter) and [Amplify Auth already set up](https://docs.amplify.aws/lib/auth/getting-started/q/platform/flutter)
    * For instructions on how to set up Amplify, please follow the [project setup walkthrough](~/lib/project-setup/create-application.md)

<amplify-callout warning>

If you are using Flutter (2.2.0), you need to disable sound null safety by following the instructions [here](https://dart.dev/null-safety/unsound-null-safety#testing-or-running-mixed-version-programs). Null safety support for Amplify Flutter is being worked on actively.

</amplify-callout>
    

You can see [an example Amplify Auth + Flutter application here](https://github.com/aws-amplify/amplify-flutter/tree/master/packages/amplify_storage_s3/example).
