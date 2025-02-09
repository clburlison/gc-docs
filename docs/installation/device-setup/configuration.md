---
title: Configuration File
layout: default
parent: Device Setup
grand_parent: Installation
nav_exclude: true
---

Once you're done installing and setting up all the [pre-required] software, you can finally move onto configuring Exeggcute itself.

The expected configuration is in JSON format and looks like this:

```
{
    "api_key": "<exeggcute_api_key>",
    "device_name": "<device_name>",
    "rotom_url": "ws://<rotom_url>",
    "workers_count": <workers_count>
}
```

Depending on the platform and deployment model you're following for your devices, this configuration might need to be placed in one or another directory; usually you wouldn't need to bother with this yourself as the process is often automated by specific tools or scripts.

### API Key

The field `api_key` is supposed to hold your Exeggcute API key, that you can get by following instructions in the Discord server.

### Device name
The field `device_name` is an optional string field that you can use to override the device name that Exeggcute posts to both Rotom and Dragonite.

{: .note }
> Starting with iOS16, third-party apps won't be able to access the real device name anymore.[^1]
>
> You will have to fill this property if you want your devices to have a human-readable name in your Rotom and Dragonite dashboards.

### Rotom URL
The field `rotom_url` should point to your [Rotom] installation.

### Workers count
The field `workers_count` is an optional integer field that you can use to override the number of mapping workers that Exeggcute will run on a single device.

The default value is `1` and the upper limit is `5`.

[pre-required]: {% link docs/installation/installation.md %}
[^1]: [com.apple.developer.device-information.user-assigned-device-name](https://developer.apple.com/documentation/bundleresources/entitlements/com_apple_developer_device-information_user-assigned-device-name)
[Rotom]: https://github.com/UnownHash/Rotom
