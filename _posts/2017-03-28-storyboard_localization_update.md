---
layout: post
title: How to update storyboard localization
tags:
- swift
- xcode
---

So, you localized your Xcode project and release the app. Now you have to add a new button a localize it. 
How to do it without recreating localization files for your storyboard?

1. Find Object ID for the new UI element you added to the storyboard
![Object ID on storyboard]({{ site.baseurl }}/images/Localization_03.png)
  ObjectID is 4OI-Q4-Xxk

2. Find localization file for the storyboard
![Object ID on storyboard]({{ site.baseurl }}/images/Localization_01.png)

3. Add localization for button's title 
![Object ID on storyboard]({{ site.baseurl }}/images/Localization_02.png)


Format for localization string is {ObjectID}.{property to update} = "Localized text";

```
"4OI-Q4-Xxk.normalTitle" = "COMBINER";
```
{: .language-swift}


* UIButton - normalTitle
* UILabel - text
* UISegmentedControl - segmentTitles[ N ]
* UITextField - placeholder
