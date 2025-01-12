# Project

## build.gradle

```
plugins {
id("com.android.application")
}

android {
namespace = "com.example.project"
compileSdk = 34

    defaultConfig {
        applicationId = "com.example.project"
        minSdk = 26
        targetSdk = 34
        versionCode = 1
        versionName = "1.0"

        testInstrumentationRunner = "androidx.test.runner.AndroidJUnitRunner"
    }
    buildFeatures {
        viewBinding = true
    }
    buildTypes {
        release {
            isMinifyEnabled = false
            proguardFiles(
                getDefaultProguardFile("proguard-android-optimize.txt"),
                "proguard-rules.pro"
            )
        }
    }
    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_1_8
        targetCompatibility = JavaVersion.VERSION_1_8
    }
}

dependencies {
implementation ("androidx.core:core-ktx:1.12.0")
implementation ("androidx.appcompat:appcompat:1.6.1")
implementation ("com.google.android.material:material:1.10.0")
implementation ("androidx.constraintlayout:constraintlayout:2.1.4")
testImplementation ("junit:junit:4.13.2")
androidTestImplementation ("androidx.test.ext:junit:1.1.5")
androidTestImplementation ("androidx.test.espresso:espresso-core:3.5.1")
implementation ("com.github.bumptech.glide:glide:4.13.0")
annotationProcessor ("com.github.bumptech.glide:compiler:4.13.0")
implementation ("jp.wasabeef:glide-transformations:4.3.0")
implementation ("net.sourceforge.jexcelapi:jxl:2.6.12")
implementation ("androidx.recyclerview:recyclerview:1.3.2")
implementation("androidx.lifecycle:lifecycle-livedata-ktx:2.6.2")
implementation("androidx.lifecycle:lifecycle-runtime:2.6.2")
implementation("androidx.room:room-ktx:2.6.1")
annotationProcessor("androidx.room:room-compiler:2.6.1")
implementation ("com.prolificinteractive:material-calendarview:1.4.3")
}
```

## gradle.properties

```
org.gradle.jvmargs=-Xmx2048m -Dfile.encoding=UTF-8

android.useAndroidX=true
android.nonTransitiveRClass=true
android.enableJetifier=true

```
