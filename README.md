# euphony-listener
Euphony Listener / Euphony Library Demo Solution
Acoustic Data Telecommunication Library. This is for Android version.
Euphony provides a handiness library designed to communicate with other devices(android and web) using mic and recorder.
Official Facebook Page : https://www.facebook.com/euphonyproject
Official Library Site : https://dev.jbear.co/euphony
## Prerequisite
build.gradle in app module
```java
dependencies {
    implementation 'euphony.lib:euphony:0.7.1.6'
}
```
AndroidManifest.xml
```xml
<uses-permission android:name="android.permission.RECORD_AUDIO" />
```
## Euphony Listener is very easy to use
## Euphony Listener는 사용하기 매우 쉽습니다.
```java
EuRxManager mRxManager = new EuRxManager();
mRxManager.setAcousticSensor(new AcousticSensor() {
@Override
    public void notify(String letters) {
        //when data is received
    }
});
mRxManager.listen();  //Listening Start
// if you want to finish listening, call the finish();
// mRxManager.finish();
```
## Architecture
euphony architecture
## Contributing
Changes are improvements are more than welcome! Feel Free to fork and open a pull request. Please make your changes in a specific branch and request to pull into master.
## License
Euphony is licensed under the Apache 2.0 license. (https://github.com/designe/Euphony/blob/master/LICENSE)
