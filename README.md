# extend_fab_sample

# ExtendFabを追加する時の注意
https://www.geeksforgeeks.org/extended-floating-action-button-in-android-with-example/

AppThemeにマテリアルのテーマを追加しないと、クラッシュする。
<details>
  <summary>スタックトレース</summary>

  ```
2021-06-28 20:28:20.610 9165-9165/com.example.expandingfab E/AndroidRuntime: FATAL EXCEPTION: main
    Process: com.example.expandingfab, PID: 9165
    java.lang.RuntimeException: Unable to start activity ComponentInfo{com.example.expandingfab/com.example.expandingfab.MainActivity}: android.view.InflateException: Binary XML file line #41: Binary XML file line #41: Error inflating class com.google.android.material.floatingactionbutton.ExtendedFloatingActionButton
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2827)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:2902)
        at android.app.ActivityThread.-wrap11(Unknown Source:0)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1603)
        at android.os.Handler.dispatchMessage(Handler.java:105)
        at android.os.Looper.loop(Looper.java:169)
        at android.app.ActivityThread.main(ActivityThread.java:6578)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.Zygote$MethodAndArgsCaller.run(Zygote.java:240)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:767)
     Caused by: android.view.InflateException: Binary XML file line #41: Binary XML file line #41: Error inflating class com.google.android.material.floatingactionbutton.ExtendedFloatingActionButton
     Caused by: android.view.InflateException: Binary XML file line #41: Error inflating class com.google.android.material.floatingactionbutton.ExtendedFloatingActionButton
     Caused by: java.lang.reflect.InvocationTargetException
        at java.lang.reflect.Constructor.newInstance0(Native Method)
        at java.lang.reflect.Constructor.newInstance(Constructor.java:334)
        at android.view.LayoutInflater.createView(LayoutInflater.java:647)
        at android.view.LayoutInflater.createViewFromTag(LayoutInflater.java:790)
        at android.view.LayoutInflater.createViewFromTag(LayoutInflater.java:730)
        at android.view.LayoutInflater.rInflate(LayoutInflater.java:863)
        at android.view.LayoutInflater.rInflateChildren(LayoutInflater.java:824)
        at android.view.LayoutInflater.rInflate(LayoutInflater.java:866)
        at android.view.LayoutInflater.rInflateChildren(LayoutInflater.java:824)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:515)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:423)
        at android.view.LayoutInflater.inflate(LayoutInflater.java:374)
        at androidx.appcompat.app.AppCompatDelegateImpl.setContentView(AppCompatDelegateImpl.java:699)
        at androidx.appcompat.app.AppCompatActivity.setContentView(AppCompatActivity.java:195)
        at com.example.expandingfab.MainActivity.onCreate(MainActivity.kt:14)
        at android.app.Activity.performCreate(Activity.java:7016)
        at android.app.Instrumentation.callActivityOnCreate(Instrumentation.java:1214)
        at android.app.ActivityThread.performLaunchActivity(ActivityThread.java:2780)
        at android.app.ActivityThread.handleLaunchActivity(ActivityThread.java:2902)
        at android.app.ActivityThread.-wrap11(Unknown Source:0)
        at android.app.ActivityThread$H.handleMessage(ActivityThread.java:1603)
        at android.os.Handler.dispatchMessage(Handler.java:105)
        at android.os.Looper.loop(Looper.java:169)
        at android.app.ActivityThread.main(ActivityThread.java:6578)
        at java.lang.reflect.Method.invoke(Native Method)
        at com.android.internal.os.Zygote$MethodAndArgsCaller.run(Zygote.java:240)
        at com.android.internal.os.ZygoteInit.main(ZygoteInit.java:767)
     Caused by: java.lang.IllegalArgumentException: The style on this component requires your app theme to be Theme.MaterialComponents (or a descendant).
        at com.google.android.material.internal.ThemeEnforcement.checkTheme(ThemeEnforcement.java:243)
        at com.google.android.material.internal.ThemeEnforcement.checkMaterialTheme(ThemeEnforcement.java:217)
        at com.google.android.material.internal.ThemeEnforcement.checkCompatibleTheme(ThemeEnforcement.java:145)
        at com.google.android.material.internal.ThemeEnforcement.obtainStyledAttributes(ThemeEnforcement.java:76)
        at com.google.android.material.button.MaterialButton.<init>(MaterialButton.java:229)
  ```
</details>
