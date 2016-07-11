# Appodeal AIR Documentation

[![](https://img.shields.io/badge/documentation-here-red.svg)](http://www.appodeal.com/sdk/documentation?framework=7)
![](https://img.shields.io/badge/version-1.14.15%2F0.10.7-green.svg)

### 1. Download SDK 
Here you can download latest appodeal air native extension:

[![](https://img.shields.io/badge/download-crossplatform-blue.svg)](https://s3-eu-west-1.amazonaws.com/appodeal-adobe-air/Appodeal_AIR_Android_1.14.15_iOS_0.10.7.zip)
[![](https://img.shields.io/badge/download-android-lightgrey.svg)](https://s3-eu-west-1.amazonaws.com/appodeal-adobe-air/Appodeal_AIR_Android_1.14.15.zip)

Minimum OS requirements:

OS | Android | iOS
--- | --- | ---
Version | 2.3 (API 9) | 7.1

### 2. AndroidManifest.xml

Add following permissions under manifest tag:

```
<uses-permission android:name="android.permission.ACCESS_WIFI_STATE"/>
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />
<!-- Optional -->
<uses-permission android:name="android.permission.GET_ACCOUNTS" />
```

Add following under application tag:

```
<meta-data android:name="com.appodeal.framework" android:value="android" />
<receiver android:name="com.appodeal.ads.AppodealPackageAddedReceiver" android:exported="true" android:enabled="true">
<intent-filter>
    <action android:name="android.intent.action.PACKAGE_ADDED" />
    <data android:scheme="package" />
</intent-filter>
</receiver>

<activity android:name="com.appodeal.ads.InterstitialActivity"
      android:configChanges="orientation|screenSize"
      android:theme="@android:style/Theme.Translucent.NoTitleBar" />
<activity android:name="com.appodeal.ads.VideoActivity"
      android:configChanges="orientation|screenSize"
      android:theme="@android:style/Theme.Translucent.NoTitleBar" />

<activity android:name="com.appodeal.ads.LoaderActivity"
      android:configChanges="orientation|screenSize"
      android:theme="@android:style/Theme.Translucent.NoTitleBar" />

<meta-data android:name="com.google.android.gms.version" android:value="@integer/google_play_services_version" />

<activity android:name="com.google.android.gms.ads.AdActivity"
      android:configChanges="keyboard|keyboardHidden|orientation|screenLayout|uiMode|screenSize|smallestScreenSize"
      android:theme="@android:style/Theme.Translucent" />

<activity android:name="com.chartboost.sdk.CBImpressionActivity" android:excludeFromRecents="true"
      android:hardwareAccelerated="true" android:theme="@android:style/Theme.Translucent.NoTitleBar.Fullscreen"
      android:configChanges="keyboardHidden|orientation|screenSize" />

<activity android:name="com.applovin.adview.AppLovinInterstitialActivity"
      android:theme="@android:style/Theme.Translucent" />

<activity android:name="com.mopub.mobileads.MoPubActivity"
      android:configChanges="keyboardHidden|orientation|screenSize"
      android:theme="@android:style/Theme.Translucent" />
<activity android:name="com.mopub.common.MoPubBrowser"
      android:configChanges="keyboardHidden|orientation|screenSize" />
<activity android:name="com.mopub.mobileads.MraidActivity"
      android:configChanges="keyboardHidden|orientation|screenSize" />
<activity android:name="com.mopub.mobileads.MraidVideoPlayerActivity"
      android:configChanges="keyboardHidden|orientation|screenSize" />

<activity android:name="org.nexage.sourcekit.mraid.MRAIDBrowser"
      android:configChanges="orientation|keyboard|keyboardHidden|screenSize"
      android:theme="@android:style/Theme.Translucent" />


<activity android:name="com.amazon.device.ads.AdActivity" android:configChanges="keyboardHidden|orientation|screenSize"/>

<activity android:name="com.my.target.ads.MyTargetActivity" android:configChanges="keyboard|keyboardHidden|orientation|screenLayout|uiMode|screenSize|smallestScreenSize"/>

<activity android:name="org.nexage.sourcekit.vast.activity.VASTActivity"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />

<activity android:name="org.nexage.sourcekit.vast.activity.VPAIDActivity"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />

<!--suppress AndroidDomInspection -->
<activity android:name="com.appodeal.ads.networks.vpaid.VPAIDActivity"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen" />

<activity android:name="com.appodeal.ads.networks.SpotXActivity"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen"/>
<!--suppress AndroidDomInspection -->
<activity android:name="com.facebook.ads.InterstitialAdActivity" android:configChanges="keyboardHidden|orientation|screenSize" />

<activity android:name="com.unity3d.ads.android.view.UnityAdsFullscreenActivity"
      android:configChanges="fontScale|keyboard|keyboardHidden|locale|mnc|mcc|navigation|orientation|screenLayout|screenSize|smallestScreenSize|uiMode|touchscreen"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen" android:hardwareAccelerated="true" />
<activity android:name="com.unity3d.ads.android2.view.UnityAdsFullscreenActivity"
      android:configChanges="fontScale|keyboard|keyboardHidden|locale|mnc|mcc|navigation|orientation|screenLayout|screenSize|smallestScreenSize|uiMode|touchscreen"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen" android:hardwareAccelerated="true" />


<!--suppress AndroidDomInspection -->
<activity android:name="com.jirbo.adcolony.AdColonyOverlay"
      android:configChanges="keyboardHidden|orientation|screenSize"
      android:theme="@android:style/Theme.Translucent.NoTitleBar.Fullscreen" />
<!--suppress AndroidDomInspection -->
<activity android:name="com.jirbo.adcolony.AdColonyFullscreen"
      android:configChanges="keyboardHidden|orientation|screenSize"
      android:theme="@android:style/Theme.Black.NoTitleBar.Fullscreen" />
<!--suppress AndroidDomInspection -->
<activity android:name="com.jirbo.adcolony.AdColonyBrowser"
      android:configChanges="keyboardHidden|orientation|screenSize"
      android:theme="@android:style/Theme.Black.NoTitleBar.Fullscreen" />
<!--suppress AndroidDomInspection -->
<activity android:name="com.vungle.publisher.FullScreenAdActivity"
      android:configChanges="keyboardHidden|orientation|screenSize"
      android:theme="@android:style/Theme.NoTitleBar.Fullscreen"/>
<!--suppress AndroidDomInspection -->
<activity android:name="com.startapp.android.publish.list3d.List3DActivity"
      android:theme="@android:style/Theme" />
<!--suppress AndroidDomInspection -->
<activity android:name="com.startapp.android.publish.OverlayActivity"
      android:theme="@android:style/Theme.Translucent"
      android:configChanges="orientation|keyboardHidden|screenSize" />
<!--suppress AndroidDomInspection -->
<activity android:name="com.startapp.android.publish.FullScreenActivity"
      android:theme="@android:style/Theme"
      android:configChanges="orientation|keyboardHidden|screenSize" />
<service android:name="com.yandex.metrica.MetricaService" android:enabled="true"
     android:exported="true" android:process=":Metrica">
	<intent-filter>
		<category android:name="android.intent.category.DEFAULT" />
		<action android:name="com.yandex.metrica.IMetricaService" />
		<data android:scheme="metrica" />
	</intent-filter>
	<meta-data android:name="metrica:api:level" android:value="44" />
</service>
<receiver android:name="com.yandex.metrica.MetricaEventHandler"
      android:enabled="true" android:exported="true">
	<intent-filter>
		<action android:name="com.android.vending.INSTALL_REFERRER" />
	</intent-filter>
</receiver>
<!--suppress AndroidDomInspection -->
<activity android:name="com.yandex.mobile.ads.AdActivity"
      android:configChanges="keyboard|keyboardHidden|orientation|screenLayout|uiMode|screenSize|smallestScreenSize" />
<activity android:name="com.inmobi.rendering.InMobiAdActivity"
      android:configChanges="keyboardHidden|orientation|keyboard|smallestScreenSize|screenSize"
      android:theme="@android:style/Theme.Translucent.NoTitleBar" android:hardwareAccelerated="true" />
<receiver android:name="com.inmobi.commons.core.utilities.uid.ImIdShareBroadCastReceiver"
      android:enabled="true" android:exported="true" >
	<intent-filter>
		<action android:name="com.inmobi.share.id" />
	</intent-filter>
</receiver>
<service android:enabled="true" android:name="com.inmobi.signals.activityrecognition.ActivityRecognitionManager" />

<!--suppress AndroidDomInspection -->
<activity android:name="com.flurry.android.FlurryFullscreenTakeoverActivity"
      android:configChanges="keyboard|keyboardHidden|orientation|screenLayout|uiMode|screenSize|smallestScreenSize" />
```

### 4. Adobe AIR Integration

#### 4.1 SDK Files

Include following libraries to your project:

* Appodeal.ane (or AppodealAndroid.ane in case you are using Android only)
* AndroidSupport.ane (Appodeal requires Android-support-v4 lib v23+, following ane includes stripped library v23.1.2)
* GooglePlayServices.ane (Appodeal requires Google Play Services, following ane includes stripped library v8.4.0)

Now add them to your descriptor under extensions tag:
```
<extensionID>com.appodeal.aneplugin</extensionID>
<extensionID>com.appodeal.playservicesane</extensionID>
<extensionID>com.appodeal.supportane</extensionID>
```
Also include files from assets folder to app build path, it should be included without "assets" folder as AIR already includes this files to assets folder in apk file.

Flash CC/Flash Pro: go to build settings -> general -> press "+" near "Included Files" window and add files.

IntelliJ Idea: go to app settings -> android and add files to "Files and folder to package" window.

Flash Builder: copy files to bin-debug for debug builds and to bin-release folder for release build. Check if this files are checked in Package Contents.

#### 4.2 Ad types

AdType.INTERSTITIAL

AdType.SKIPPABLE_VIDEO

AdType.BANNER

AdType.REWARDED_VIDEO

AdType.NON_SKIPPABLE_VIDEO

Ad types can be combined using "|" operator. For example AdType.INTERSTITIAL | AdType.SKIPPABLE_VIDEO

Note that it is better to use NON_SKIPPABLE_VIDEO or REWARDED_VIDEO, but if you are sure you want to use SKIPPABLE_VIDEO you must confirm usage by calling appodeal.confirm(AdType.SKIPPABLE_VIDEO) before SDK initialization

#### 4.3 SDK Initialization

Import the Appodeal classes

`import com.appodeal.aneplugin.*;`

We recommend making a variable in your class to store a reference to the global Appodeal instance:

`private var appodeal:Appodeal = new Appodeal();`

To initialize SDK, call the following code:

```var appKey:String = "fee50c333ff3825fd6ad6d38cff78154de3025546d47a84f";
appodeal.initialize(appKey, AdType.INTERSTITIAL | AdType.BANNER);```

Note: appKey is the key you received when you created an app.

To initialize only interstitials use appodeal.initialize(appKey, AdType.INTERSTITIAL)

To initialize only skippable videos use appodeal.initialize(appKey, AdType.SKIPPABLE_VIDEO)

To initialize only rewarded video use appodeal.initialize(appKey, AdType.REWARDED_VIDEO)

To initialize only non-skippable video use appodeal.initialize(appKey, AdType.NON_SKIPPABLE_VIDEO)

To initialize interstitials and videos use appodeal.initialize(appKey, AdType.INTERSTITIAL | AdType.SKIPPABLE_VIDEO)

To initialize only banners use appodeal.initialize(appKey, AdType.BANNER)

#### 4.4 Display ad

`appodeal.show(AdType);`

show() returns a boolean value indicating whether show call was passed to appropriate SDK

To display interstitial use appodeal.show(AdType.INTERSTITIAL)

To display skippable video use use appodeal.show(AdType.SKIPPABLE_VIDEO)

To display rewarded video use appodeal.show(AdType.REWARDED_VIDEO)

To display non-skippable video use appodeal.show(AdType.NON_SKIPPABLE_VIDEO)

To display interstitial or video use appodeal.show(AdType.INTERSTITIAL | AdType.SKIPPABLE_VIDEO)

To display banner at the bottom of the screen use appodeal.show(AdType.BANNER_BOTTOM)

To display banner at the top of the screen use appodeal.show(AdType.BANNER_TOP)

To display banner at the center of the screen use appodeal.show(AdType.BANNER_CENTER)

#### 4.5 Hiding banner

To hide banner you need to call the following code in activity:

`appodeal.hide(AdType.BANNER);`

#### 4.6 Samples

Display interstitial after it was loaded

```appodeal.setAutoCache(AdType.INTERSTITIAL, false);
appodeal.initialize(appKey, AdType.INTERSTITIAL);
appodeal.cache(AdType.INTERSTITIAL);
appodeal.addEventListener(AdEvent.INTERSTITIAL_LOADED, onInterstitialLoaded);
function onInterstitialLoaded(ae:AdEvent):void {
  appodeal.show(AdType.INTERSTITIAL);
}```

Display interstitial after app launch

```appodeal.initialize(appKey, AdType.INTERSTITIAL);
appodeal.show(AdType.INTERSTITIAL);```

How to know that the user clicked on the ad

```appodeal.addEventListener(AdEvent.INTERSTITIAL_CLICKED, onClickedInterstitial);
function onClickedInterstitial(event:AdEvent):void {
  trace('ad clicked');
}```

How to know this award for viewing REWARDED_VIDEO ad

```appodeal.addEventListener(AdEvent.REWARDED_VIDEO_FINISHED_CLICKED, onFinishedRewardedVideo);
function onFinishedRewardedVideo(event:AdEvent):void {
  trace('reward: amount='+event.amount+', name='+event.name);
}```

#### 4.7 Advanced features

Enabling test mode

`appodeal.setTesting(true);`

In test mode test ads will be shown and debug data will be written to logcat

Checking if ad is loaded

`appodeal.isLoaded(AdType);`

o check if interstitial is loaded use appodeal.isLoaded(AdType.INTERSTITIAL)

To check if skippable video is loaded use appodeal.isLoaded(AdType.SKIPPABLE_VIDEO)

To check if rewarded video is loaded use appodeal.isLoaded(AdType.REWARDED_VIDEO)

To check if non-skippable video is loaded use appodeal.isLoaded(AdType.NON_SKIPPABLE_VIDEO)

To check if banner is loaded use appodeal.isLoaded(AdType.BANNER)

Checking if loaded ad is precache

`appodeal.isPrecache(AdType);`

Currently supported only for interstitials, Use appodeal.isPrecache(AdType.INTERSTITIAL)

Setting Interstitial callbacks

```
appodeal.addEventListener(AdEvent.INTERSTITIAL_LOADED, onInterstitial);
appodeal.addEventListener(AdEvent.INTERSTITIAL_FAILED_TO_LOAD, onInterstitial);
appodeal.addEventListener(AdEvent.INTERSTITIAL_SHOWN, onInterstitial);
appodeal.addEventListener(AdEvent.INTERSTITIAL_CLICKED, onInterstitial);
appodeal.addEventListener(AdEvent.INTERSTITIAL_CLOSED, onInterstitial);
```

Callback function example:

```
function onInterstitial(event:AdEvent):void {
  switch (event.type) {
    case AdEvent.INTERSTITIAL_LOADED:
      trace('ad loaded');
      break;
    case AdEvent.INTERSTITIAL_FAILED_TO_LOAD:
      trace('failed to load ad');
      break;
    case AdEvent.INTERSTITIAL_SHOWN:
      trace('ad shown');
      break;
    case AdEvent.INTERSTITIAL_CLICKED:
      trace('ad has clicked');
      break;
    case AdEvent.INTERSTITIAL_CLOSED:
      trace('ad closed');
      break;
  }
}
```

Setting skippable video callbacks

```
appodeal.addEventListener(AdEvent.SKIPPABLE_VIDEO_LOADED, onVideo);
appodeal.addEventListener(AdEvent.SKIPPABLE_VIDEO_FAILED_TO_LOAD, onVideo);
appodeal.addEventListener(AdEvent.SKIPPABLE_VIDEO_SHOWN, onVideo);
appodeal.addEventListener(AdEvent.SKIPPABLE_VIDEO_FINISHED, onVideo);
appodeal.addEventListener(AdEvent.SKIPPABLE_VIDEO_CLOSED, onVideo);
```

Callback function example:

```
function onVideo(event:AdEvent):void {
  switch (event.type) {
    case AdEvent.SKIPPABLE_VIDEO_LOADED:
      trace('ad loaded');
      break;
    case AdEvent.SKIPPABLE_VIDEO_FAILED_TO_LOAD:
      trace('failed to load ad');
      break;
    case AdEvent.SKIPPABLE_VIDEO_SHOWN:
      trace('ad shown');
      break;
    case AdEvent.SKIPPABLE_VIDEO_FINISHED:
      trace('ad finished');
      break;
    case AdEvent.SKIPPABLE_VIDEO_CLOSED:
      trace('ad closed');
      break;
  }
}
```

Setting rewarded video callbacks

```
appodeal.addEventListener(AdEvent.REWARDED_VIDEO_LOADED, onRewardedVideo);
appodeal.addEventListener(AdEvent.REWARDED_VIDEO_FAILED_TO_LOAD, onRewardedVideo);
appodeal.addEventListener(AdEvent.REWARDED_VIDEO_SHOWN, onRewardedVideo);
appodeal.addEventListener(AdEvent.REWARDED_VIDEO_FINISHED, onRewardedVideo);
appodeal.addEventListener(AdEvent.REWARDED_VIDEO_CLOSED, onRewardedVideo);
```

Callback function example:

```
function onRewardedVideo(event:AdEvent):void {
  switch (event.type) {
    case AdEvent.REWARDED_VIDEO_LOADED:
      trace('ad loaded');
      break;
    case AdEvent.REWARDED_VIDEO_FAILED_TO_LOAD:
      trace('failed to load ad');
      break;
    case AdEvent.REWARDED_VIDEO_SHOWN:
      trace('ad shown');
      break;
    case AdEvent.REWARDED_VIDEO_FINISHED:
      trace('ad clicked, your reward:', event.amount, event.name);
      break;
    case AdEvent.REWARDED_VIDEO_CLOSED:
      trace('ad closed');
      break;
  }
}
```

Setting non-skippable video callbacks

```
appodeal.addEventListener(AdEvent.NON_SKIPPABLE_VIDEO_LOADED, onSkippableVideo);
appodeal.addEventListener(AdEvent.NON_SKIPPABLE_VIDEO_FAILED_TO_LOAD, onSkippableVideo);
appodeal.addEventListener(AdEvent.NON_SKIPPABLE_VIDEO_SHOWN, onSkippableVideo);
appodeal.addEventListener(AdEvent.NON_SKIPPABLE_VIDEO_FINISHED, onSkippableVideo);
appodeal.addEventListener(AdEvent.NON_SKIPPABLE_VIDEO_CLOSED, onSkippableVideo);
```

Callback function example:

```
function onSkippableVideo(event:AdEvent):void {
  switch (event.type) {
    case AdEvent.NON_SKIPPABLE_VIDEO_LOADED:
      trace('ad loaded');
      break;
    case AdEvent.NON_SKIPPABLE_VIDEO_FAILED_TO_LOAD:
      trace('failed to load ad');
      break;
    case AdEvent.NON_SKIPPABLE_VIDEO_SHOWN:
      trace('ad shown');
      break;
    case AdEvent.NON_SKIPPABLE_VIDEO_FINISHED:
      trace('ad clicked, your reward:', event.amount, event.name);
      break;
    case AdEvent.NON_SKIPPABLE_VIDEO_CLOSED:
      trace('ad closed');
      break;
  }
}
```

Setting banner callbacks

```
appodeal.addEventListener(AdEvent.BANNER_LOADED, onBanner);
appodeal.addEventListener(AdEvent.BANNER_FAILED_TO_LOAD, onBanner);
appodeal.addEventListener(AdEvent.BANNER_SHOWN, onBanner);
appodeal.addEventListener(AdEvent.BANNER_CLICKED, onBanner);
```

Callback function example:

```
function onBanner(event:AdEvent):void {
  switch (event.type) {
    case AdEvent.BANNER_LOADED:
      trace('ad loaded');
      break;
    case AdEvent.BANNER_FAILED_TO_LOAD:
      trace('failed to load ad');
      break;
    case AdEvent.BANNER_SHOWN:
      trace('ad shown');
      break;
    case AdEvent.BANNER_CLICKED:
      trace('ad clicked');
      break;
  }
}
```

Manual ad caching

`appodeal.cache(AdType);`

You should disable automatic caching before SDK initialization using setAutoCache(AdType, false).

To cache interstitial use appodeal.cache(AdType.INTERSTITIAL)

To cache skippable video use appodeal.cache(AdType.SKIPPABLE_VIDEO)

To cache rewarded video use appodeal.cache(AdType.REWARDED_VIDEO)

To cache non-skippable video use appodeal.cache(AdType.NON_SKIPPABLE_VIDEO)

To cache interstitial and video use appodeal.cache(AdType.INTERSTITIAL | AdType.SKIPPABLE_VIDEO)

To cache banner use appodeal.cache(AdType.BANNER)

Enabling or disabling automatic caching

`appodeal.setAutoCache(AdType, false);`

Should be used before SDK initialization

To disable automatic caching for interstitials use appodeal.setAutoCache(AdType.INTERSTITIAL, false)

To disable automatic caching for skippable videos use appodeal.setAutoCache(AdType.SKIPPABLE_VIDEO, false)

To disable automatic caching for rewarded videos use appodeal.setAutoCache(AdType.REWARDED_VIDEO, false)

To disable automatic caching for non-skippable videos use appodeal.setAutoCache(AdType.NON_SKIPPABLE_VIDEO, false)

To disable automatic caching for banners use appodeal.setAutoCache(AdType.BANNER, false)

Triggering onLoaded callback twice

`appodeal.setOnLoadedTriggerBoth(AdType, true);`

Currently supported only for interstitials

setOnLoadedTriggerBoth(AdType.INTERSTITIAL, false) - onInterstitialLoaded will trigger only when normal ad was loaded (default)..

setOnLoadedTriggerBoth(AdType.INTERSTITIAL, true) - onInterstitialLoaded will trigger twice, both when precache and normal ad were loaded..

Should be used before SDK initialization.

Disabling networks

`appodeal.disableNetwork(network);`

Available parameters: "amazon_ads", "applovin", "chartboost", "mopub", "unity_ads", "mailru", "facebook", "adcolony", "vungle", "liverail", "yandex", "startapp", "inmobi", "avocarrot", "flurry", "pubnative".

Should be used before SDK initialization

Disabling location permission check

To disable toast messages if ACCESS_COARSE_LOCATION permission is missing use the following method:

`appodeal.disableLocationPermissionCheck();`

Should be used before SDK initialization.

Tracking in-app purchase

`appodeal.trackInAppPurchase(amount, currencyCode);`

Tracks in-app purchase information and sends info to our servers for analytics. Example:

`appodeal.trackInAppPurchase(5, "USD");`

#### 4.8 Setting user data

Initialization

Our SDK provides the transfer of user data for better ad targeting and higher eCPM. All parameters are optional and can be defined partially.

Set the age of the user

Positive integer value.

`appodeal.settings.age = 30;`

Set birth date

`appodeal.settings.birthday = 478645200000; // unixtime(seconds)`

Parameter birthday takes unixtime econds. To determine unixtime by date, use the code:

```var date:Date = new Date(1985, 2, 3);
appodeal.settings.birthday = date.time```

Please note that the second parameter in the constructor Date (Month) class is set to 0, ie, in the example above, the date March 3, 1985.

To set the time to UTC, use the code:

```var date:Date = new Date(1985, 2, 3);
appodeal.settings.setBirthday(date.time, true);```

Set user email

`appodeal.settings.email = "mail@domain.com";`

Set Facebook ID

`appodeal.settings.facebookId = "1623169517896758";`

Set Vkontakte ID

`appodeal.settings.vkId = "91918219";`

Specify gender of the user

`appodeal.settings.gender = Gender.MALE;`

Possible values: Gender.FEMALE, Gender.MALE, Gender.OTHER.

Set interests of the user

`appodeal.settings.interests = "reading, games, movies, snowboarding";`

Specify occupation of the user

`appodeal.settings.occupation = Occupation.WORK;`

Possible values: Occupation.WORK, Occupation.SCHOOL, Occupation.UNIVERSITY, Occupation.OTHER

Specify marital status of the user

`appodeal.settings.relationship = Relation.MARRIED;`

Possible values: Relation.SINGLE, Relation.DATING, Relation.ENGAGED, Relation.MARRIED, Relation.SEARCHING, Relation.OTHER

Set drinking habits of the user

`appodeal.settings.alcohol = Alcohol.NEUTRAL;`

Possible values: Alcohol.NEGATIVE, Alcohol.NEUTRAL, Alcohol.POSITIVE.

User attitude to smoking

`appodeal.settings.smoking = Smoking.NEUTRAL;`

Possible values:: Smoking.NEGATIVE, Smoking.NEUTRAL, Smoking.POSITIVE.
