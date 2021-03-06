ValueBar
========

A beautiful Android custom View that works similar to a range or seekbar. Selection by gesture. With animations. **Supporting API level 11+.**

![alt tag](https://raw.github.com/PhilJay/ValueBar/master/screenshots/adgraphic.jpg)


Demo
=======
For a short demonstration, please download the [**demo application**](https://play.google.com/store/apps/details?id=com.philjay.valuebarexample) from the Google PlayStore. The corresponding code for the demo application can be found in the `ValueBarExample` folder.

Usage
========

For using `ValueBar`, there are various possibilities: 

**1. Gradle dependency**

 - Add the following to your `build.gradle`:
 ```gradle
repositories {
	    maven { url "https://jitpack.io" }
}

dependencies {
	    compile 'com.github.PhilJay:ValueBar:v1.0.2'
}
```

**2. Maven**
- Add the following to your `pom.xml`:
 ```xml
<repository>
       	<id>jitpack.io</id>
	    <url>https://jitpack.io</url>
</repository>

<dependency>
	    <groupId>com.github.PhilJay</groupId>
	    <artifactId>ValueBar</artifactId>
	    <version>v1.0.2</version>
</dependency>
```

**3. jar file**
- download the **latest .jar file** from the [**release-section**](https://github.com/PhilJay/ValueBar/releases) and copy it into the `libs` folder of your Android application project.

**4. clone repo**
- clone this repository and add the library folder to your Android application project

Create a `ValueBar` in .xml:

```xml
<com.philjay.valuebar.ValueBar
        android:id="@+id/valueBar"
        android:layout_width="match_parent"
        android:layout_height="60dp"
        android:layout_margin="5dp" />

```

or in code, and then add it to a layout:

```java
 ValueBar bar = new ValueBar(Context);
```

Apply styling, and display values:

```java
 bar.setMinMax(0, 1000);
 bar.setInterval(1f); // interval in which can be selected
 bar.setDrawBorder(false);
 bar.setValueTextSize(14f);
 bar.setMinMaxTextSize(14f);
 bar.setValueTextTypeface(...);
 bar.setMinMaxTextTypeface(...);
 bar.setOverlayColor(...);
 
 // create your custom color formatter by using the BarColorFormatter interface
 bar.setColorFormatter(new RedToGreenFormatter());
 
 // add your custom text formatter by using the ValueTextFormatter interface
 bar.setValueTextFormatter(...);
            
 bar.setValue(800f); // display a value
 
 // or animate from a specific value to a specific value
 bar.animate(from, to, animationDuration);
            
 bar.setValueBarSelectionListener(...); // add a listener for callbacks when touching

```

Donations
======

If you would like to support this project's further development, the creator of this project or the continuous maintenance of this project, **feel free to donate**. Your donation is highly appreciated.

PayPal

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=EGBENAC5XBCKS)
