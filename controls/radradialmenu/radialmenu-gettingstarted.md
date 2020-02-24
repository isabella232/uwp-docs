---
title: Getting Started
page_title: Getting Started
description: Check our &quot;Getting Started&quot; documentation article for RadRadialMenu for UWP control.
slug: radialmenu-gettingstarted
tags: getting,started
published: True
position: 1
---

# Getting Started

In order to use Telerik RadRadialMenu control in your application you have to add reference to the **Telerik UI for {{ site.framework_name }} SDK**:

Right-click on your project > `Add Reference` > {% if site.site_name == 'WIN8' %}`Windows 8.1`{% endif %}{% if site.site_name == 'UWP' %}`Universal Windows`{% endif %} > `Extensions` > `Telerik UI for {{ site.framework_name }}` > `OK`.

You can alternatively use binaries. You will need to add reference to the the following assemblies:

* **Telerik.Core.dll**
* **Telerik.UI.Xaml.Primitives.dll**

To add them:  
Right click on your project > `Add Reference` > `Browse` > C:\Program Files (x86)\Telerik\UI for {{ site.framework_name }} Rx 20xx\Binaries > select the relevant assemblies > `OK`

To use RadRadialMenu in XAML you have to add the following namespace declaration:

	xmlns:telerikPrimitives="using:Telerik.UI.Xaml.Controls.Primitives"

## RadRadialMenu as a Normal Menu

Here is an example demonstrating how to declare a new RadRadialMenu instance.

	<telerikPrimitives:RadRadialMenu/>

## RadRadialMenu as a Context Menu

Here is an example demonstrating how to declare a RadRadialMenu instance as a context menu for a **TextBlock**. This can be done by attaching the **Menu** and **Behavior** properties of the **[RadRadialContextMenu]({%slug radialmenu-behavior%})** class to the **TextBlock** target element.

> If the **Behavior** attached property is not added, the menu will not be visualized.

	<TextBlock Text="Some Text">
	    <telerikPrimitives:RadRadialContextMenu.Behavior>
	        <telerikPrimitives:RadialMenuTriggerBehavior AttachTriggers="Focused" />
	    </telerikPrimitives:RadRadialContextMenu.Behavior>
	    <telerikPrimitives:RadRadialContextMenu.Menu>
	        <telerikPrimitives:RadRadialMenu/>
	    </telerikPrimitives:RadRadialContextMenu.Menu>
	</TextBlock>


# See Also

 * [Visual Structure]({%slug radialmenu-visualstructure%})
 * [Properties and Configuration]({%slug radialmenu-propertiesandconfiguration%})
