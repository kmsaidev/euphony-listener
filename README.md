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
## Quick Start


### 1. Repository clone (저장소 클론)

```bash
$ git clone https://github.com/euphony-io/euphony-listener.git
```

![clone](https://user-images.githubusercontent.com/47289893/128968369-e30bfc36-3c57-418d-b3b2-b8976436493b.png)


### 2. Open in Android Studio (안드로이드 스튜디오에서 열기)

Find the path of the cloned project and open it.  
clone한 프로젝트의 경로를 찾아서 열어준다.

![open](https://user-images.githubusercontent.com/47289893/128968509-21778091-1c48-432d-8c68-856d89c59a07.png)

Press the 'Trust Project' button.  
Trust Project 버튼을 누른다.

![trust](https://user-images.githubusercontent.com/47289893/128968544-78756386-1740-43e7-9f27-78f9322307f8.png)


### 3. JDK settings (JDK 설정)

JDK location error may occur when opening the file for the first time.  
처음 열 때 JDK location error가 발생할 수 있다.

![set jdk-1](https://user-images.githubusercontent.com/47289893/128968605-e73af820-0ae7-4e8c-997a-1c1cdbef7129.png)

Click 'Change JDK location' to specify Gradle JDK.  
Change JDK location을 클릭하여 Gradle JDK를 지정한다.

![set jdk-2](https://user-images.githubusercontent.com/47289893/128968614-0988ac95-1672-411d-8e9e-336503be69cd.png)

When you reopen the project, the build starts.  
프로젝트를 다시 열면 build가 시작된다.

![build](https://user-images.githubusercontent.com/47289893/128968741-00b1cd80-a9f7-4481-bd1a-ff388141080f.png)



### 4. Connect the device (디바이스 연결)

By default, there is no device.  
기본적으로 디바이스가 없다.

![no device](https://user-images.githubusercontent.com/47289893/128968845-d0868890-cb57-4721-a956-857b871e7393.png)

It is automatically recognized when devices with developer mode are connected.  
개발자 모드가 활성화된 디바이스를 연결하면 자동으로 인식된다.

![yes device](https://user-images.githubusercontent.com/47289893/128968864-35b7ae72-6fb8-4bb2-8706-1ec2257faf73.png)



### 5. Test (테스트)

Operate 'euphony-listener' app on the connected device.  
연결된 디바이스에서 euphony-listener를 동작시킨다.

![run](https://user-images.githubusercontent.com/47289893/128968893-cca8c520-4dcc-41e7-9e04-9d4849143176.png)

![run-build](https://user-images.githubusercontent.com/47289893/128969518-043e50ae-aa45-4d0a-b145-9e7d1176353c.png)

#### Speaker

Speaker demo is available at (https://dev.jbear.co/euphony/). Enter short text and press the 'broadcast' button.  
[여기](https://dev.jbear.co/euphony/)에서 Speaker demo를 사용할 수 있다. 짧은 텍스트를 입력하고 broadcast 버튼을 누른다.

![speaker](https://user-images.githubusercontent.com/47289893/128968935-b4cd781a-5de0-42cf-a01a-ec87a47f77b6.png)


#### Listener

When the 'LISTEN' button is pressed, recognition begins.  
LISTEN 버튼을 누르면 인식이 시작된다.

![device](https://user-images.githubusercontent.com/47289893/128969127-1b7847ec-43c7-42cb-8b6b-a6602f51db7f.png)

#### Log

![logcat](https://user-images.githubusercontent.com/47289893/128969052-3b70b562-f4ce-4ba6-98e5-d9be4096ab76.png)


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
