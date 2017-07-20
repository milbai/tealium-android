# Tealium Mobile Library for Android

[![License](https://img.shields.io/badge/license-Proprietary-blue.svg?style=flat
            )](https://github.com/Tealium/tealium-java/blob/master/LICENSE.txt)
[![Platform](https://img.shields.io/badge/Platform-Android-lightgrey.svg?style=flat
             )](https://developer.android.com/guide/index.html)
[![Language](https://img.shields.io/badge/Language-Java-orange.svg?style=flat
             )](https://developer.android.com/reference/packages.html)        

This mobile library leverages the power of Tealium's [TiQ™ Tag Management](http://tealium.com/products/tealium-iq-tag-management-system/), [AudienceStream™](http://tealium.com/products/audiencestream/) and [Data Access™](http://tealium.com/products/tealium-dataaccess/) products, or any combination of, making them natively available to Android applications. Please contact your Account Manager first to verify your agreement(s) for licensed products.

**Minimum Android API: 9 (Gingerbread)**

## What does Tealium do?

Tealium provides the platform for crafting a modern, scalable and flexible marketing technology stack so you can easily connect and integrate all of your best-in-class solutions.

### What is Tag Management ?

Tags are snippets of code that nearly every digital marketing vendor requires their customers to embed in the source code of their web sites and mobile applications.

A tag management system is a new type of application that makes it easy for digital marketers and IT professionals to deploy and manage these tags via an intuitive user interface with no coding required.

A key part of enterprise-class tag management systems is the [data layer](http://tealium.com/what-is-a-data-layer/), the behind-the-scenes data and structure that drive customer interactions in web, mobile, and other digital channels.

The Tealium iQ™ tag management system is a powerful and highly extensible solution that helps marketers easily manage their mission-critical technologies across web and mobile channels. Tealium iQ drives the complexity out of vendor tag deployments and is the cornerstone for achieving unified marketing, i.e., the ability to harmonize applications and data to drive superior cross-channel customer interactions.

### What is Audience Stream ?

The Tealium AudienceStream™ Influence DMP (data management platform) enables you to build a universal 360-degree customer profile to better influence and engage visitors in your web or mobile channels in real time. AudienceStream leverages the richest source of real-time, first-party data to help you deliver more relevant and timely interactions, thereby improving loyalty and conversions and creating new opportunities for growth.

### What is Data Access ?

The Tealium DataAccess™ solution is a rich set of customer data services and feeds delivered at the speed needed to fuel strong personalization and other timely customer interactions. DataAccess offers a clean, fully correlated dataset for your business intelligence (BI) or enterprise customer data initiatives.

## How To Get Started

* Check out the [Getting Started](https://community.tealiumiq.com/t5/Tealium-for-Android/Adding-Tealium-to-Your-Android-App/ta-p/16846) guide for a step by step walkthough of adding Tealium to an extisting project.  
* The public API can viewed online [here](https://tealium.github.io/tealium-android), it is also provided in the [documentation directory](/../../tree/master/Documentation) of this repo generated by JavaDoc.
* There are many other useful articles on our [community site](https://community.tealiumiq.com).

## Contact Us

* If you have **code questions** or have experienced **errors** please post an issue in the [issues page](../../issues)
* If you have **general questions** or want to network with other users please visit the [Tealium Learning Community](https://community.tealiumiq.com)
* If you have **account specific questions** please contact your Tealium account manager

## Change Log
- 5.3.1
    - Added method to allow overriding log level at init time (setForceOverrideLogLevel)
    - Changed calls to webview to protect against an edge case where the first event is not sent after a period of inactivity, if the publish settings timeout had expired (webview was being reloaded before the javascript call could finish)
    - Cookies from the webview are now flushed to disk immediately after any track call. This protects against an edge case where cookies may not be saved to disk when the app is closed quickly
    - Added protection to stop Android webview from requesting Favicon.ico when the webview loads
    - Added optional Optimizely Listener module to pass Optimizely tracking events to Tealium
    - Minor internal updates
- 5.3.0
    - Tealium data variable added:
        - tealium_datasource 
- 5.2.0
    - New optional module: Ad Identifier. Module adds ```google_adid``` to data variables
    - New optional module Install Referrer. Module adds ```install_referrer``` to data variables
- 5.1.0
    - New track call trackEventType()
    - Tag Management: CookieManager enabled by default
    - Maven Support
        - library (core)
        - lifecycle
    - Tealium data variables added:
        - tealium_event (previously event_name / link_id)
        - app_uuid (previously uuid)
        - tealium_event_type
- 5.0.4
    - Standardized Tealium data variables
    - Added lifecycle_totalcrashcount to lifecycle module
    - Fixed late initialization null pointer issue
- 5.0.3
	- Renamed OnMetricUpdateListener to MetricUpdateListener
	- Fixed data clobbering bug
	- Fixed JavaScript evaluation in Marshmallow
- 5.0.2
    - Fixed setOverrideCollectDispatchUrl bug
- 5.0.1 
    - Fixed cause of "Ignoring InnerClasses attribute for an anonymous inner class" warning
    - Clarified "Retrieved bad visitor profile:" error message
    - Override S2S legacy now allows for querystring variables
- 5.0.0 Initial Release
    - Multiton support
    - Collect Dispatch support
    - S2S Dispatch support
    - Tag Managment Dispatch support
    - TIQ Mobile Publish Settings v5 support

## License

Use of this software is subject to the terms and conditions of the license agreement contained in the file titled "LICENSE.txt".  Please read the license before downloading or using any of the files contained in this repository. By downloading or using any of these files, you are agreeing to be bound by and comply with the license agreement.


---
Copyright (C) 2012-2017, Tealium Inc.
