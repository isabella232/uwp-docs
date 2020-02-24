---
title: Data Virtualization
page_title: Data Virtualization
description: Check our &quot;Data Virtualization&quot; documentation article for RadDataGrid for UWP control.
slug: raddatagrid-datavirtualization
tags: data,virtualization
published: True
position: 5
---

# Data Virtualization

This topic describes how to enable incremental loading in **RadDataGrid**.

To enable incremental loading in **RadDataGrid**, you have to use as its **ItemsSource**
a collection that implements the **ISupportIncrementalLoading** interface.
You can also take advantage of the **IncrementalLoadingCollection** which is our default implementation.

## Example

![Data Grid-Data Virtualization-Incremental Loading](images/DataGrid-DataVirtualization-IncrementalLoading.png)

XAML:

	<telerikGrid:RadDataGrid x:Name="grid" ItemsSource="{Binding}"  IncrementalLoadingMode="Explicit"/>

Code behind:

	IncrementalLoadingCollection<Data> collection = new IncrementalLoadingCollection<Data>(
	    async count =>
	    {
	        return (from c in Enumerable.Range(0, 10)
	                select new Data { Category = "Name " + c }).ToList();
	    }) { BatchSize = 100 };
	
	this.DataContext = collection;

Data class:
	
	public class Data
	{
	    public string Category { get; set; }
	
	    public double Value { get; set; }
	}