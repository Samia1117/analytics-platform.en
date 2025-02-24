---
description: Segmenting on individual metrics allows you to make metric comparisons within the same report. 
title: Segmented metrics
feature: Calculated Metrics
exl-id: 1e7e048b-9d90-49aa-adcc-15876c864e04
---
# Filtered metrics

In the Calculated metric builder, you can apply filters within your metric definition. This is helpful if you want to derive new metrics to use in your analysis. Keep in mind, filter definitions can be updated through the Filter builder. If changes are made, the filter will automatically update anywhere it is applied, including if it is part of a calculated metric definition.

![](assets/german-visitors.png)

## Create a filtered metric {#create}

Let's say you want to compare different aspects of a "German Visitors" filter to those of an "International Visitors" filter. You can create metrics that will give you insights such as:

* How does content browsing behavior compare between the two groups? (Another example would be: How does the conversion rate compare between the two filters?) 
* As a percentage of total visitors, how many German visitors browse certain pages, versus International visitors? 
* Where are the biggest differences in terms of which content is accessed by these different filters?

1. If you don't have a comparable filter, create an adhoc segment right in the Calculated Metric Builder called "German Visitors", where "Countries" equals "Germany". Just drag the Countries dimension into the Definition canvas and select Germany as the value:

   ![](assets/segment-from-dimension.png)

   >[!NOTE]
   >
   >You can also do this in the [Filter Builder](/help/components/filters/create-filters.md), but we have simplified the workflow by making dimensions available in the Calculated Metric Builder. "Adhoc" means that the segment is not visible in the **[!UICONTROL Filters]** list in the left rail. You can however, make it public by hovering over the "i" icon next to it and clicking **[!UICONTROL Make public]**.

1. If you don't have a comparable filter, create a filter called "International Visitors" where "Countries" does not equal "Germany." 
1. Build and save a metric called "German Visitors" by dragging the Germany filter into the Definition canvas and dragging the Unique Visitors metric within it:

   ![](assets/german-visitors.png)

1. Repeat Step 3 with the International Visitors segment and the Unique Visitors metric to create an International Visitors metric.
1. In Analysis Workspace, drag the **[!UICONTROL Page]** Dimension into a Freeform Table and drag the 2 new calculated metrics next to each other to the top:

   ![](assets/workspace-pages.png)

Here is a video overview:

>[!VIDEO](https://video.tv.adobe.com/v/25407/?quality=12)

## Percent of total metrics {#percent-total}

You can take the example above a step further by comparing your filter to a total population. To do so, create two new metrics, "% of Total German Visitors" and "% of Total International Visitors":

1. Drop the German (or International) Visitors filter into the canvas.
1. Drop another German (or International) Visitors filter below. However, this time, click its configuration (gear) icon to select the Metric Type "Total". The Format should be "Percent". The operator should be "divided by". You end up with this metric definition:

   ![](assets/cm_metric_total.png)

1. Apply this metric to your project:

   ![](assets/cm_percent_total.png)
