![header](./header.png)
![animation](./preview.gif)

# Garland View for Android
[![Twitter](https://img.shields.io/badge/Twitter-@Ramotion-blue.svg?style=flat)](http://twitter.com/Ramotion)


**Looking for developers for your project?**<br>
This project is maintained by Ramotion, Inc. We specialize in the designing and coding of custom UI for Mobile Apps and Websites.


<a href="https://ramotion.com/?utm_source=gthb&utm_medium=special&utm_campaign=garland-view-android-contact-us/#Get_in_Touch"> 
<img src="https://github.com/ramotion/gliding-collection/raw/master/contact_our_team@2x.png" width="187" height="34"></a> <br>


The [Android mockup](https://store.ramotion.com?utm_source=gthb&utm_medium=special&utm_campaign=garland-view-android) available [here](hhttps://store.ramotion.com/product/samsung-galaxy-s7-edge-mockups?utm_source=gthb&utm_medium=special&utm_campaign=garland-view-android).

## Requirements
​
- Android 4.4 KitKat (API lvl 19) or greater
- Your favorite IDE

## Installation
​
Just download the package from [here](http://central.maven.org/maven2/com/ramotion/garlandview/garland-view/0.1.0/garland-view-0.1.0.aar) and add it to your project classpath, or just use the maven repo:

Gradle:
```groovy
compile 'com.ramotion.garlandview:garland-view:0.2.1'
```
SBT:
```scala
libraryDependencies += "com.ramotion.garlandview" % "garland-view" % "0.2.1"
```
Maven:
```xml
<dependency>
    <groupId>com.ramotion.garlandview</groupId>
    <artifactId>garland-view</artifactId>
    <version>0.2.1</version>
</dependency>
```


## Basic usage

`GarlandView` consists of classes for inner items that are scrolled vertically
and outer items that are scrolled horizontally, and each of which contains
one inner item.

First of all, you need to implement the classes necessary to create internal items: InnerItem and InnerAdapter.

`InnerAdapter` is an abstract class inherited from RecyclerView.Adapter.
It works only with InnerItem - ViewHolder.

In `InnerItem`, you need to override the `getInnerLayout` method, which must return
the main layout of the inner item.

Next, you need to override the classes required for external items: `HeaderItem` and` HeaderAdapter`.

`HeaderAdapter` is an abstract class inherited from RecyclerView.Adapter,
It works only with HeaderItem - ViewHolder.

In `HeaderItem`, you need to redefine 4 methods:` getHeader`, `getHeaderAlphaView`,` isScrolling`, `getViewGroup`.
The method `getViewGroup` should return InnerRecyclerView.
The `isScrolling` method must return the InnerRecyclerView's scrolling state.
The `getHeaderAlpha` method should return an alpha-layout, which will be used for dimming (hiding header's views).
The `getHeader` method must return the main layout of the header, an outer item.

Finally, place `TailRecyclerView` in the Activity's layout. Next, create a TailLayoutManager and
specify it as a LayoutManager for `TailRecyclerView`.

Here are the attributes of `TailRecyclerView` you can specify in the XML layout:
*`itemStart` - Outer item left and right offset size.
*`itemGap` -  Distance between outer items.

## License
​
CardSlider for Android is released under the MIT license.
See [LICENSE](./LICENSE.md) for details.

# Get the Showroom App for iOS to give it a try
Try our UI components in our iOS app. Contact us if interested.

<a href="https://itunes.apple.com/app/apple-store/id1182360240?pt=550053&ct=garland-view-android&mt=8" > 
<img src="https://github.com/ramotion/gliding-collection/raw/master/app_store@2x.png" width="117" height="34"></a>
<a href="https://ramotion.com/?utm_source=gthb&utm_medium=special&utm_campaign=garland-view-android-contact-us/#Get_in_Touch"> 
<img src="https://github.com/ramotion/gliding-collection/raw/master/contact_our_team@2x.png" width="187" height="34"></a>
<br>
<br>

Follow us for the latest updates 
<br>
[![Twitter URL](https://img.shields.io/twitter/url/http/shields.io.svg?style=social)](https://twitter.com/intent/tweet?text=https://github.com/ramotion/garland-vew-android)
[![Twitter Follow](https://img.shields.io/twitter/follow/ramotion.svg?style=social)](https://twitter.com/ramotion)
