# Tealium Mobile Library for TVOS 

This mobile library leverages the power of [AudienceStream™](http://tealium.com/products/audiencestream/) and [Data Access™](http://tealium.com/products/tealium-dataaccess/) products, or any combination of, making them natively available to tvOS applications. Please contact your Account Manager first to verify your agreement(s) for licensed products.

## What does Tealium do?

Tealium provides the platform for crafting a modern, scalable and flexible marketing technology stack so you can easily connect and integrate all of your best-in-class solutions.

### What is Tag Managment ?

Tags are snippets of code that nearly every digital marketing vendor requires their customers to embed in the source code of their web sites and mobile applications.

A tag management system is a new type of application that makes it easy for digital marketers and IT professionals to deploy and manage these tags via an intuitive user interface with no coding required.

A key part of enterprise-class tag management systems is the [data layer](http://tealium.com/what-is-a-data-layer/), the behind-the-scenes data and structure that drive customer interactions in web, mobile, and other digital channels.

The Tealium iQ™ tag management system is a powerful and highly extensible solution that helps marketers easily manage their mission-critical technologies across web and mobile channels. Tealium iQ drives the complexity out of vendor tag deployments and is the cornerstone for achieving unified marketing, i.e., the ability to harmonize applications and data to drive superior cross-channel customer interactions.

### What is Audience Stream ?

The Tealium AudienceStream™ Influence DMP (data management platform) enables you to build a universal 360-degree customer profile to better influence and engage visitors in your web or mobile channels in real time. AudienceStream leverages the richest source of real-time, first-party data to help you deliver more relevant and timely interactions, thereby improving loyalty and conversions and creating new opportunities for growth.

### What is Data Access ?

The Tealium DataAccess™ solution is a rich set of customer data services and feeds delivered at the speed needed to fuel strong personalization and other timely customer interactions. DataAccess offers a clean, fully correlated dataset for your business intelligence (BI) or enterprise customer data initiatives.

## How To Get Started

* Check out the [Getting Started](https://community.tealiumiq.com/t5/6-Mobile-Documentation/Mobile-122-Getting-Started-with-tvOS-5-x/ta-p/10375) guide for a step by step walkthough of adding Tealium to an extisting project.  
* The public API can viewed online [here](http://tealium.github.io/tealium-tvos/), it is also provided in the Documentation directory of this repo as html and docset for Xcode and Dash integration.
* There are many other useful articles on our [community site](https://community.tealiumiq.com).

## Contact Us

* If you have **code questions** or have experienced **errors** please post an issue in the [issues page](../../issues)
* If you have **general questions** or want to network with other users please visit the [Tealium Learning Community](https://community.tealiumiq.com)
* If you have **account specific questions** please contact your Tealium account manager

## Change Log

- 5.3.0
    - Configuration updated with new initializer that takes a 'datasource' arg - 6 digit alphanumeric UDH Datasource Id
    - Removed variable:
        - page_type

- 5.2.1
    - Lifecycle module fix: Missing wake detection
    - Lifecycle module fix: Errant didDetectCrash=true when no actual crash occurred

- 5.2.0
    - @synchronization protection added to the captureTimeDatasources function
    - Log warning if a call is made to uninitilized Tealium instance (previously silent fail).

- 5.1.3 Bug Fix
    - Nullable attributes added to dispatch manager
    - Improved Tealium Logger handling to support more development side control 

- 5.1.2 Bug Fix
    - Dispatch manager logic fix related to purged dispatches
    - Protections added for saving dispatches to persistence

- 5.1.1 Bug Fix
    - Corrected issue related to call_type datasource

- 5.1
    - New track with type API added and optional completion
    - Swift sample apps updated to support Swift 3
    - Removed underscores from binaries
    - Tealium universal data sources added for all dispatches:
        - tealium_event (previously event_name / link_id)
        - app_uuid (previously uuid)
        - tealium_event_type

- 5.0.4 Universal Data Sources & Bug Fixes
    - First track event now waits for webview ready when Tag Management option enabled
    - Lifecycle module first launch auto detection fixed
    - Devices only builds added to repo (no simulator support frameworks)
    - DSYMs provided with each framework
    - Tealium universal data sources added for all dispatches:
        - event_name (previously link_id)
        - tealium_account
        - tealium_environment
        - tealium_library_name
        - tealium_library_version
        - tealium_profile
        - tealium_random (different 16 digit long number for each track event)
        - tealium_session_id
        - tealium_timestamp_epoch (previously timestamp_unix)
        - tealium_visitor_id (previously tealium_vid)

- 5.0.3 Bug Fixes
    - Protections added to the collectDispatchURL that may have caused crashes at launch time
    - Lifecycle module update fixing errant isFirstLaunch data source with subsequent events
    - Simulator stripping run script added to Sample Apps

- 5.0.2 Lifecycle Module & Sample App Added
    - TealiumIOSLifecycle.framework and sample app added to Support folder
    - Initial queue size init after first launch for default -1 setting fixed
    - CaptureTimeDataSources now safely adds additional data for certain launch edge cases
    - DestroyInstanceForKey: method now properly clears persistent data
    - Additional Data Source Keys to support lifecycle module added
    - Offline TagBridge feature enabled

- 5.0.1 Bug fixes
    - Remote disable fix
    - Reachability check fix
    - @import TealiumIOS module name fix
    - Minutes between refresh now displays correct time remaining
    - Dispatch logs updated with a QA verbosity option
    - Minor documentation update
    - Nullability specifiers for inits corrected for cleaner swift implementation
    - OverrideS2SLegacyDispatchURL can now accept base addresses without trailing '?'
    - TEALDispatch stringForDispatchStatusType class method made public
    - Track calls forced to stay on main thread until data capture complete, then to background queue
    - Blank sample app updated with proper method signatures

- 5.0.0 Initial Release*
    - Multiton support
    - Collect Dispatch support
    - S2S Dispatch support
    - TIQ Mobile Publish Settings v5 support
    - * This is the first tvOS release - version number matches publish setting options found in TIQ for simplicity

## License

Use of this software is subject to the terms and conditions of the license agreement contained in the file titled "LICENSE.txt".  Please read the license before downloading or using any of the files contained in this repository. By downloading or using any of these files, you are agreeing to be bound by and comply with the license agreement.


---
Copyright (C) 2012-2017, Tealium Inc.
