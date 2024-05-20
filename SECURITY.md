# Security Policy

 */
apply plugin: 'com.android.library'

android {
    compileSdk rootProject.ext.compileSdk

    defaultConfig {
        minSdkVersion 22
        targetSdk rootProject.ext.targetSdk
    }
    buildTypes {
        debug {
            minifyEnabled true
//            shrinkResources true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
        beta {
            minifyEnabled true
//            shrinkResources true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
        release {
            minifyEnabled true
//            shrinkResources true
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
}

dependencies {
    implementation fileTree(include: ['*.jar'], dir: 'libs')
    implementation supportDependencies.appcompat
    
    testImplementation 'junit:junit:4.13.2'
}
