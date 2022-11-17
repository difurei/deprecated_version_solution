## Solution of Deprecated Android version on Flutter

### Changing in AndroidManifest

```xml
"your_project_name"/android/app/src/main/AndroidManifest.xml : 

 <application
        android:name="${applicationName}"

 <meta-data
                android:name="flutterEmbedding"
                android:value="2" />
```

### Changing in MainActivity.java
```java
"your_project_name"/android/app/src/main/java/co/appbrewery/"project"/MainActivity.java :

import io.flutter.embedding.android.FlutterActivity;

public class MainActivity extends FlutterActivity {

}
```

## Geolocator Settings

### Android

```xml
"your_project_name"/android/app/src/main/AndroidManifest.xml :

add this lines after <mainfest> tag:

<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```

### IOS
```xml
"your_project_name"\ios\Runner\Info.plist :

add this lines in <dict> tag:

<key>NSLocationWhenInUseUsageDescription</key>
<string>This app needs access to location when open.</string>
<key>NSLocationAlwaysUsageDescription</key>
<string>This app needs access to location when in the background.</string>
```
