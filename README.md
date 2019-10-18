[![](https://jitpack.io/v/zainfikrih/jsonloader-library.svg)](https://jitpack.io/#zainfikrih/jsonloader-library)

# JSONLoader Library
A simple library to open JSON from assets

## Download
Grab the latest dependencies through Gradle, add it to your build.gradle with:
```gradle
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
and:

```gradle
dependencies {
    implementation 'com.github.zainfikrih:jsonloader-library:{latest version}'
}
```

## Usage
Put the json file in the assets package on the android project (src / main / assets / filename.json).
For more information, see [Where do I place the 'assets' folder in Android Studio?](https://stackoverflow.com/questions/18302603/where-do-i-place-the-assets-folder-in-android-studio)

Get JSON as a string:
```java
  String jsonString = JSONLoader.with(getApplicationContext()).fileName("filename.json").get();
```

Get JSON as JSON Object:
```java
  JSONObject jsonObject = JSONLoader.with(getApplicationContext()).fileName("filename.json").getAsJSONObject();
```

Get JSON as JSON Array:
```java
  JSONArray jsonArray = JSONLoader.with(getApplicationContext()).fileName("filename.json").getAsJSONArray();
```

For some examples, see the sample App.
