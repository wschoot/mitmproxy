# mitmproxy

run mitmproxy, browse to mitm.it on your device (setup proxy in WiFi settings in Android); and download the certifcate.
Trust it as a user-cert (which is all you can do when not rooted)
you need a signed apk which you can fortunately do yourself
From Android API version 26 and above, you also need to modify the apk to also trust user certs (instead of the new default, only system certs) 

https://github.com/levyitay/AddSecurityExceptionAndroid decscribes the proces but the signing doesn't work.

use SignApk.zip for this to work

# Sign APK 
java -jar signapk.jar certificate.pem key.pk8 <APK> <SIGNED APK>

If you don't do this, or you use the signing from jarsigner with a selfsigned keytool, the app threw a "App not installed" for me (Android pie)
