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
## Euphony Listener is very easy to use (Euphony Listener는 사용하기 매우 쉽습니다.)
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
## Architecture (아키텍처)
euphony architecture
## Contributing (기여)
Changes and improvements are more than welcome! Feel Free to fork and open a pull request. Please make your changes in a specific branch and request to pull into master.
변화와 개선은 환영입니다! 자유롭게 fork와 PR하세요. 당신의 변경사항을 특정한 branch에 commit해주시고 master branch로 PR해주세요.
## License
Euphony is licensed under the Apache 2.0 license. (https://github.com/designe/Euphony/blob/master/LICENSE)
Euphony는 Apache 2.0 license에 따라 라이센스가 부여됩니다.
