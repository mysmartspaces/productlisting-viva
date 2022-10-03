---
ROBOTS: NOINDEX,NOFOLLOW
title: Power BI tips, troubleshooting, and FAQ
description: Learn some tips, troubleshooting, and answers to the FAQ about setting up and using the Viva Insights Templates
author: lilyolason
ms.author: v-lilyolason
ms.topic: article
ms.localizationpriority: medium 
ms.collection: viva-insights-advanced
ms.service: viva 
ms.subservice: viva-insights 
search.appverid: 
- MET150 
manager: helayne
audience: Admin
---

# Power BI tips, FAQ, and troubleshooting

The following provides a few guidelines to consider when setting up the Power BI templates, answers to some of the most frequently asked questions, and troubleshooting for the most common issues about setting up and using the templates in the the advanced insights app with Viva Insights.

## Setting up the Power BI template

These templates are designed to help Viva Insights users with the most common setups and business scenarios. For best results, use the following guidelines for selecting the parameters while setting up the templates for Power BI:

* Limit the number of employees included in your query results to 50,000 or less.
* Select the last six months or less for the time period.
* Include up to seven organizational attributes in your query, including the required ones.

You must use Power BI Desktop to initialize the Viva Insights Power BI templates. When you open the Power BI template for the first time, and after you provide the query URLs, Power BI will load the output of the queries. Depending on the parameters you selected when setting up the Viva Insights queries, loading data into Power BI may take up to several hours. This applies to weekly data refresh as well.

If you follow the above guidelines, interacting with elements (like slicers) in the reports or navigating between pages should only take a few seconds.

After initializing the template, you might consider publishing it to the Power BI service to consume and share with others. For best results, publish the reports to a workspace in a Premium capacity. You can also [configure scheduled refresh](/power-bi/connect-data/refresh-scheduled-refresh) in the Power BI service to define when you want to refresh the dataset.  

## Sharing a report

Like other products that work with sensitive data, such as HR systems, advanced insights in Viva Insights are only available for certain users who should be trained to handle sensitive information. See [Data-protection considerations](/viva/insights/privacy/data-protection-considerations?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) when using data generated by Viva Insights.

Anyone you share the Power BI *desktop file* with can access the underlying dataset at the same level of granularity as the analyst role. For this reason, consider the following alternatives that do not provide access to the underlying data:

* **Publish the report to Power BI Service and share insights in an app** - This option allows other users to navigate the dashboard without access to the underlying data. See [Distribute insights in an app](/power-bi/service-how-to-collaborate-distribute-dashboards-reports#distribute-insights-in-an-app) for details.

* **Share as a PDF or other static file** - This option generates a report that's not interactive. See [Export reports from Power BI to PDF](/power-bi/consumer/end-user-pdf).

## Customizing a template

Power BI templates are a great way to begin your journey with Viva Insights. After you get familiar with these templates, you can customize them to fit your organization’s needs. While you’re welcome to make changes, keep in mind that template customizations could affect report performance. Power BI reports that have been customized or modified are not supported by the Viva Insights team.

## Power BI tips

A few tips to help you use these dashboards in Power BI:

* **Cross-filter and cross-highlight** - All visuals on a report page are interconnected. If you select a data point on one of the visuals, all the others on the page that contain that data will change, based on that selection.
* **Drill down into a visual that has a hierarchy** - When a visual has a hierarchy, you can drill down to reveal additional details. Some of the charts in the dashboards support this capability, such as the "By Organization and Level Designation" chart in the Business Continuity dashboard.
* **Export data as a table** - From the upper right corner of any visualization, select **More options** (**…**) and select **Export data**.

For more details about using Power BI, see [Interact with visuals in reports, dashboards, and apps](/power-bi/consumer/end-user-visualizations).

## FAQ

##### Q1 Who can create the dashboard in Power BI?

You must be assigned the role of [Analyst](/viva/insights/use/user-roles?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) in the advanced insights app to create the dashboard. You must also have a Power BI license and have the desktop version installed. See [Install and run Power BI Desktop](/power-bi/desktop-getting-started#install-and-run-power-bi-desktop) for details.

##### Q2 How frequently is data refreshed in the dashboard?

The dashboard gets repopulated once a week after the advanced insights app finishes its weekend processing. **Note**: You must manually adjust the **Selected time frame** setting in the dashboard's **Settings and scope** report to view the most recently processed data.

##### Q3 How do I share the dashboard with others in my organization?

You can share the dashboard with others in your organization *without sharing the underlying data* by publishing the insights in an app or as PDF or static file. See [Sharing a report](#sharing-a-report) for details.

##### Q4 Can I share the underlying dashboard dataset with others in my organization?

To maintain data privacy, only employees assigned the role of [Analyst](/viva/insights/use/user-roles?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) in the advanced insights app should have access to the underlying dataset in the Power BI dashboard.

##### Q5 How do I know if I have the latest version of the template?

Starting with version 2 and later versions of a template, you can find the version number at the end of the title in the lower left of the dashboard’s Settings page.

##### Q6 How can I extend the dates of the data used in the dashboard?

If you have been using a dashboard for a few months now, you are probably using data for the last six months. You need to run new queries that include the last one year. For the Business continuity dashboard, see [Template update](/viva/insights/tutorials/power-bi-bc?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#template-update) for details.  

##### Q7 How do I set up the Viva Insights data?

See [Create a Person Query](/viva/insights/tutorials/person-queries?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) for details.

##### Q8 How do I change the axis of a chart to use a different Organizational data attribute?

Only the required Organizational attributes are used when setting up the Power BI file. If you selected more Organizational attributes when setting up the queries, you can use those in the visuals. To use a different Organizational attribute:

1. Select the visualization you want to change.  
2. In the **Fields** pane, select and drag the Organizational attribute to the **Axis** section of the visualization.

##### Q9 How do I integrate additional metrics or data sources with this dashboard?

See [Connect to data in Power BI](/power-bi/connect-data/) to learn more about how to connect data in Power BI. See [Prepare organizational data](/viva/insights/setup/prepare-organizational-data?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to learn about what organizational data you can analyze in the advanced insights app and see [Data sources](/viva/insights/use/data-sourcesv2?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) to see what data sources you can connect to and analyze from within the advanced insights app.

##### Q10 How do I use Power BI?

See [Power BI documentation](/power-bi/) for details on how to use Power BI.

##### Q11 What languages are the dashboards available in?

The dashboards are currently only available in English and will only work with data generated from the English version of the advanced insights app. Before running the required queries, confirm the browser language in the app's URL includes **en-us**, or change it to include **en-us**: ...office.com/en-us/...

## Troubleshooting

##### Unable to open document

If you get the following error, you do not have the latest version of Power BI.

  ![Unable to open error.](../Images/WpA/Tutorials/bcd-open-error.png)

However, the template might work with the earlier version of Power BI that you're using. To test it:  

1. Close any warnings.
2. If you can view the **Settings** page, the dashboard will work with this version. If you cannot view **Settings**, you need to download the latest version of Power BI.

##### Report layout differences might exist

If you get the following error, you do not have the latest version of Power BI. However, the template might work with this earlier version. To test it, repeat the steps in the previous section.

  ![Report layout error.](../Images/WpA/Tutorials/bcd-report-error.png)

##### OData request failed

The following error (or similar 500+ error) can occur for one of the following reasons.

  ![OData error.](../Images/WpA/Tutorials/bcd-odata-error.png)

* **If you were not prompted to sign in with your organizational account** while setting up the dashboard and Power BI fails to load the data, follow these steps to clear existing permissions:

  1. In Power BI, open the **Transform data** menu, and select **Data source settings**.
  2. Select **Global permissions**, select `https://workplaceanalytics.office.com` (or `https://workplaceanalytics-eu.office.com`), and then select **Clear permissions**.
  3. Select **Delete**.
  4. Close Power BI and follow the set up instructions for the applicable dashboard.

* **If you are signed in with the wrong organizational account**, you'll get an error when loading the data with the template. To fix it, follow these steps:

  1. In Power BI, open the **Transform data** menu, and select **Data source settings**.
  2. Select **Global permissions**, select `https://workplaceanalytics.office.com` (or `https://workplaceanalytics-eu.office.com`), and then select **Edit permissions**.
  3. For **Credentials**, select **Edit**.
  4. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in** or **Sign in as a different user**.
  5. Select the account that you use to sign in to the advanced insights app, enter the password, and then when prompted in **OData feed**, select **Save**.
  6. In **Edit Permissions**, select **OK**, and then close the **Data source settings** window.
  7. Close Power BI and follow the set up instructions in **Set up the dashboard** for the applicable dashboard.

##### The Power BI visuals fail to load or show errors in the tables

Power BI cannot complete a data join if data values are missing in the Organization or Level Designation tables. To validate this error:

1. In the **Fields** pane in Power BI, look for an **error** (!) icon in either the **Organization** or **LevelDesignation** tables. If you see an error about blank values similar to the following, select the field with the error to view it.

   **Blank-value error** - Column in table contains blank values and this is not allowed for columns on the one side of a many-to-one relationship or for columns that are used as the primary key of a table.

2. To remediate this error, select **Transform Data** > **Transform Data** to open the Power Query Editor.
3. Select the applicable results.
4. In the data preview table, locate the column for Organization and LevelDesignation, expand the column header, select **Remove Empty**, and then select **OK**.
5. Select **Hourly collaboration** and repeat **Steps 3-4** to filter out empty values.
6. Select **Close & Apply** to apply the changes and return to the dashboard.

##### Failed to save modifications error in Power BI

The following error occurs because of a preview features setting in Power BI. To change the setting for the dashboard, go to **File** > **Options and Settings** > **Options** > **Preview features**. Clear the checkbox for preview features, and then save and restart the template.

  ![Preview features error.](../Images/WpA/Tutorials/pbi-preview-error.png)

##### OData error that the given URL neither points to an OData service or a feed in Power BI

When you publish this dashboard to workspaces, they get split into two parts, reports and datasets (data sources). This error occurs when your permission authentication token expires in Power BI. Do the following to reset permissions for the Power BI service.

1. Open your [Power BI service](/power-bi/consumer/end-user-experience#open-the-power-bi-service) (app.powerbi.com).
2. From **Home**, select the **ellipsis** (**...**) on the ribbon to view the menu, and then select **Settings** > **Settings**.

   ![Power BI Service Settings.](../Images/WpA/Tutorials/pbi-service-settings.png)

3. Select **Datasets**, and then for the dashboard you're getting the error for, select the **ellipsis** (**...**) > **Settings**.
4. In **Data source credentials**, select **Edit credentials** for the advanced insights app.
5. Select the account that you use to sign in to the advanced insights app, enter the password, and then when prompted, select **Save**.

Do the following to reset your global permissions for the OData feed.

1. In Power BI, open the **Transform data** menu, and select **Data source settings**.
2. Select **Global permissions**, select `https://workplaceanalytics.office.com` (or `https://workplaceanalytics-eu.office.com`), and then select **Edit permissions**.
3. For **Credentials**, select **Edit**.
4. In the **OData feed** dialog box, select **Organizational account**, and then select **Sign in** or **Sign in as a different user**.
5. Select the account that you use to sign in to the advanced insights app, enter the password, and then when prompted in **OData feed**, select **Save**.
6. In **Edit Permissions**, select **OK**, and then close the **Data source settings** window.

##### Apply query error for blank values in columns

When setting up a report or refreshing an existing report for either the [Business continuity](/viva/insights/tutorials/power-bi-bc?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) or the [Ways of working assessment](/viva/insights/tutorials/power-bi-collab-assess?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json) dashboards in Power BI, you might get the following Power BI error about the PersonIdDateKey column in a table containing "blank values," which is "not allowed for columns on the one side of a many-to-one relationship or for columns that are used as the primary key of a table."

![Blank values error.](../Images/WpA/Tutorials/pbi-blank-error.png)

To resolve this error, you must download the template for the applicable data in **Query designer** > **Results**, and then set up the template again in Power BI.

##### Collaborators record not found

If you get the following error, you have not selected the Organizational attribute that represents the employees' worksite location, such as the office or building for the Return to worksites dashboard.

![Collaborators record not found error.](../Images/WpA/Tutorials/pbi-collaborators-error.png)

Close Power BI, redo the set up steps in [Set up the dashboard for Return to worksites](/viva/insights/tutorials/power-bi-return-tw?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json#set-up-the-dashboard), and then select the applicable Organizational attribute in **Steps 7 and 9** for the worksite location for the employees included in the analysis.

## Support

* **Dashboard support** - Contact the Viva Insights team member that referred you to this page for support about onboarding, usage, and interpretation of the data contained within the dashboard.
* **Viva Insights support** - Refer to [Viva Insights documentation](../index.yml) or [Viva Insights Support](../overview/getting-support.md) for additional help.
* **Support with other Microsoft products and tools** - Support for Power BI and other tools used in the context of this dashboard can be found through each product's associated support channels.

## Related topics

* [Templates introduction](/viva/insights/tutorials/power-bi-intro?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)
* [View, download, and export query results](/viva/insights/use/view-download-and-export-query-results?toc=/viva/insights/use/toc.json&bc=/viva/insights/breadcrumb/toc.json)