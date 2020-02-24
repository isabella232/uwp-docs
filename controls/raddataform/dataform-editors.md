---
title: Editors
page_title: Editors
description: Check our &quot;Editors&quot; documentation article for RadDataForm for UWP control.
slug: dataform-editors
tags: dataform,raddataform,editors
published: True
position: 6
---

#Generating Editors#

For each property the RadDataForm an **EntityProperty** object which is vizualized through the **EntityPropertyControl** which contains of **Label** and **Editor**.
RadDataForm has predefined **Editors** for the following types by default:

- string : StringEditor
- double : NumericEditor
- enum   : EnumEditor
- DateTime : DateEditor, TimeEditor

The developer can register **Custom Editors** or **Views**(for read-only properties) for a **Type** of specific **Property** through the following API:

- public void RegisterTypeEditor(Type propertyType, Type editorType)

- public void RegisterPropertyEditor(string propertyName, Type editorType)

- public void RegisterTypeView(Type propertyType, Type viewType)

- public void RegisterPropertyView(string propertyName, Type viewType)

- public void UnRegisterTypeEditor(Type propertyType = null)

- public void UnRegisterPropertyEditor(string propertyName = null)

- public void UnRegisterTypeView(Type propertyType = null)

- public void UnRegisterPropertyView(string propertyName = null)


#Example#

     this.form.RegisterTypeEditor(typeof(List<string>), typeof(ListEditor));

Where the ListEditor implements the **ITypeEditor** interface.