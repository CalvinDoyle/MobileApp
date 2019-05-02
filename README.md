# MobileApp

#Introduction
CA Project for Mobile App Development
Lichess is an app for recording games that occurred on the website lichess.com. 
The app is used to record the unique website link, the winner of the game, the white player and the black player.
It can also be used to upload a picture of what the board looked like at the end of the game and also the location in which it occurred 

#Getting started
Install Android Studio using the following https://developer.android.com/studio/
Follow the setup wizards to install any SDK packages that it reccomends

#Kotlin setup
Add Kotlin to Android Studio by going to 
Preferences->Plugins->Browse Repository->Search for Kotlin then->Install

#If you wish to write your own Kotlin app do the following
#Otherwise Android Studio is ready to run Lichess
Add Kotlin classpath to the *project* build.gradle
buildscript {
    ext.kotlin_version = "1.1.1"
    ext.supportLibVersion = "25.3.0"
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:2.3.0'
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
        classpath "org.jetbrains.kotlin:kotlin-android-extensions:$kotlin_version"

        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

Add Kotlin library and apply the Kotlin plugins in the *module* build.gradle
apply plugin: 'com.android.application'
apply plugin: 'kotlin-android'
apply plugin: 'kotlin-android-extensions'

android {
    // ... various gradle setup
}

dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    testCompile 'junit:junit:4.12'
    compile "com.android.support:appcompat-v7:$supportLibVersion"
    compile "com.android.support:recyclerview-v7:$supportLibVersion"
    compile "org.jetbrains.kotlin:kotlin-stdlib:$kotlin_version"
}

#Author
Calvin Doyle
