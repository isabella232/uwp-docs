---
title: Getting Started
page_title: Getting Started
description: Check our &quot;Getting Started&quot; documentation article for RadSideDrawer for UWP control.
slug: sidedrawer-getting-started
tags: sidedrawer,radsidedrawer
published: True
position: 0
---

# Overview

The **SideDrawer** is a control enabling quick and easy navigation across all levels of your app. It can be accessed from anywhere within your app as it has 4 built-in opening directions and an array of predefined open/close animations.

## Getting Started

This article shows how to create a RadSideDrawer. First, add references to the following assemblies:

* **Telerik.Core**
* **Telerik.UI.Xaml.Primitives**

Alternatively, you can add a reference to **Telerik UI for {{ site.framework_name }} SDK**.

Then add the **Telerik.UI.Xaml.Primitives** namespace in your xaml page:

	xmlns:telerikPrimitives="using:Telerik.UI.Xaml.Controls.Primitives"

Now, declare the RadSideDrawer:

	<telerikPrimitives:RadSideDrawer />

The next step would be to create Main Content and Drawer Content:

        <telerikPrimitives:RadSideDrawer>
            <telerikPrimitives:RadSideDrawer.MainContent>
                <Grid Background="Green">
                    <TextBlock Text="Main Content" />
                </Grid>
            </telerikPrimitives:RadSideDrawer.MainContent>
            <telerikPrimitives:RadSideDrawer.DrawerContent>
                <Grid Width="300" Background="Yellow">
                    <TextBlock Text="Drawer Content" />
                </Grid>
            </telerikPrimitives:RadSideDrawer.DrawerContent>
        </telerikPrimitives:RadSideDrawer>

For further settings and customizations, you can check  the Features article.

