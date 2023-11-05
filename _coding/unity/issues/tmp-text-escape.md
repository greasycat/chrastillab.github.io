---
layout: default
title: TextMeshPro Rendering Unicode on non-Unicode Text
nav_order: 1
grand_parent: Unity
parent: Troubleshooting
---

![](https://i.imgur.com/lyEjIfZ.png)

Explanation: The `\User\erro` is mistaken as a Unicode by TextMeshPro


Workaround 1: Replace `\` with `\\`
```csharp
someText.Replace(@"\", @"\\");
```

Possible Workaround 2: Disable Escape parsing in TextMeshPro Components
- not working on 
	- Unity Editor 2019.4.29f1
	- TMP Pro 2.1.6
