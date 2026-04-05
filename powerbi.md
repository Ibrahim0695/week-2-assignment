![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qfv361873dva1h53tiy6.png)
## Introduction to Power BI and Publishing

Power BI is a powerful business analytics tool by Microsoft that transforms raw data into interactive visualizations and reports. Once you've created a compelling report with charts, tables, and insights, the next step is sharing it with your audience. Power BI provides seamless publishing capabilities that allow you to publish your reports to the Power BI Service (the cloud platform), generate embed codes, and integrate those reports directly into websites for broader accessibility.

Publishing a Power BI report involves uploading your `.pbix` file from Power BI Desktop to the Power BI Service, organizing it within a workspace, and then using the embed functionality to display the report on any webpage. This guide walks you through the entire process with detailed steps and visual guidance.

## What you need:

Before you begin, ensure you have:

- Power BI Desktop installed
- A Power BI Pro or Power BI Premium license
- A Power BI account (sign up at app.powerbi.com)
- A report saved as a `.pbix` file
- A website where you can embed HTML/JavaScript code

---

## Step 1: Creating a Workspace in Power BI Service

A workspace in Power BI is a holder of your reports, datasets, dashboards, and workbooks. Think of it as a project folder where related content lives together.

**Screenshot: Power BI Service - Create Workspace**



**Step-by-step:**

1. **Sign in to Power BI Service**
   - Open your browser and navigate to [app.powerbi.com](https://app.powerbi.com)
   - Sign in with your Microsoft account


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/fj6bb4301s2dqhrk3wbv.png)
2. **Create a New Workspace**
   - In the left navigation pane, click on **"Workspaces"**
   - Click the **"Create a workspace"** button (a plus icon or "New" button)
   - You will see the workspace creation panel slide out

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7pan46tvxhlnpbm9xz3h.png)
3. **Configure Your Workspace**
   - **Name**: Enter a descriptive name such as "Sales Analytics" or "Marketing Reports"
   - **Description**: Add a brief description explaining the workspace's purpose
   - **Workspace settings**: Under "Advanced," you can configure:
     - **License mode**: Choose between Pro or Premium Per User (PPU)
     - **Storage**: Set a capacity if using Premium
     - **Contact list**: Add team members who will receive updates
     - **OneDrive**: Optionally connect to a SharePoint/OneDrive for seamless file management

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/loxjt0rnas4i4566fkcc.png)
4. **Save the Workspace**
   - Click **"Save"** to create the workspace
   - Your new workspace will appear in the workspaces list


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/9r00sz3avb4uq78zsooo.png)


---

## Step 2: Publishing Your Report to Power BI Service

With your workspace ready, the next step is to publish your `.pbix` file. This uploads both your data model and your report design to the cloud.

**Step-by-step in Power BI Desktop:**

1. **Open Your Report**
   - Launch Power BI Desktop
   - Open the `.pbix` file you want to publish


![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vnakcep86nxdklntfbg0.png)

2. **Initiate the Publish Process**
   - Click the **"Publish"** button on the Home ribbon tab
   - Alternatively, use the keyboard shortcut: **Alt + F → H → P**


3. **Select Your Destination**
   - The "Publish to Power BI" dialog box appears
   - Under "Destination," expand the dropdown
   - Select the **workspace you created** (e.g., "Sales Analytics")
   - Note: You can also publish to "My Workspace" for personal use

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2c3n0zfse2uxctdhu9ob.png)
4. **Confirm and Publish**
   - Click the **"Publish"** button
   - Power BI Desktop will validate your data, upload the dataset, and then publish the report
   - A success message appears with a link: **"Open 'Your Report' in Power BI"**


5. **Verify the Upload**
   - Click the success link or go to app.powerbi.com
   - Navigate to your workspace
   - Confirm that your report and dataset appear

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lx2y6q2xr9to8qkcqd5w.png)














## Step 3: Generating the Embed Code

Once your report is published, you can generate an embed code to display it on any website. Power BI offers two embedding methods: **Embed for your organization** (requires viewer authentication) and **Embed for your customers** (using embed tokens for public access).

**Step-by-step:**

1. **Navigate to Your Report**
   - In Power BI Service, go to your workspace
   - Click on the report you published

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xzgtli6ugfrb256vv63e.png)
2. **Access the Embed Options**
   - In the report view, look for the **"File"** menu or the **"Share"** button
   - Alternatively, click the **"..." (More options)** menu on the report tile
   - Select **"Embed"** → **"Website or portal"**

3. **Configure Embed Settings**
   - The embed dialog shows your report with configuration options:
     - **Security**: Choose "Organization" (requires sign-in) or "Public" (embed token)
     - **Size**: Select canvas size (e.g., 16:9, 4:3, or custom)
     - **Filters**: Enable/disable filter pane visibility
     - **Navigation**: Enable/disable page navigation
     - **Title and Banner**: Show or hide report title and action bar
     - **Background**: Set transparency level

4. **Generate the Embed Code**
   - After configuring settings, click **"Apply"**
   - Power BI generates an **iframe embed code** and optionally an **HTML/JavaScript snippet**

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/cm5i5ppsfsm4wwa94o2m.png)
5. **Copy the Embed Code**
   - Copy the iframe code or the embed link to your clipboard
   - You can also download the embed script for advanced integration

**Embed Code Example:**

```html
<iframe 
    title="Sales Report" 
    src="https://app.powerbi.com/reportEmbed?reportId=abc12345&groupId=xyz67890" 
    frameborder="0" 
    allowFullScreen="true">
</iframe>
```

**Screenshot Location:** Power BI Service → Report View → File → Embed → Website or portal



---

## Step 4: Embedding the Report on a Website

Now that you have the embed code, you can paste it into your website's HTML. The exact method depends on your website platform (WordPress, custom HTML, SharePoint, etc.).

### Method 1: Embedding in a Standard HTML Website

**Step-by-step:**

1. **Open Your Website Editor**
   - Access the HTML or source code of the page where you want the report
   - Use a code editor or the built-in HTML editor of your CMS

2. **Paste the Embed Code**
   - Locate the section of the page where you want the report to appear
   - Paste the iframe code you copied from Power BI

3. **Adjust Size and Styling**
   - Modify the `width` and `height` attributes to fit your layout:
   ```html
   <iframe 
       title="Sales Report" 
       width="100%" 
       height="600" 
       src="https://app.powerbi.com/reportEmbed?reportId=abc12345&groupId=xyz67890" 
       frameborder="0" 
       allowFullScreen="true">
   </iframe>
   ```

4. **Save and Preview**
   - Save your changes and preview the page
   - The Power BI report will load and be interactive within the iframe

### Method 2: Embedding in WordPress

1. **Switch to HTML/Code View**
   - In the WordPress editor, click the **"Code editor"** or **"</>"** button

2. **Paste the Embed Code**
   - Paste the iframe code in the desired location within the page/post

3. **Option: Use a Plugin**
   - Install a Power BI embed plugin for WordPress
   - Use a shortcode provided by the plugin instead of raw iframe code

### Method 3: Embedding in SharePoint Online

1. **Edit Your SharePoint Page**
   - Navigate to the SharePoint site and click **"Edit"**

2. **Add a Web Part**
   - Click the **"+" icon** to add a new web part
   - Search for and select **"Power BI"** (if available) or use the **"Embed"** web part

3. **Paste the Embed Link**
   - If using the Embed web part, paste the report URL (not the full iframe code):
   ```plaintext
   https://app.powerbi.com/reportEmbed?reportId=abc12345&groupId=xyz67890
   ```

4. **Save the Page**
   - Click **"Publish"** or **"Republish"** to make the report visible

### Method 4: Using Power BI Embedded (For Developers)

For advanced embedding with custom authentication and user-specific views, use the **Power BI Embedded** API:

1. **Register an Application in Azure**
   - Go to the Azure Portal → Azure Active Directory → App registrations
   - Create a new application registration
   - Note down the **Client ID** and **Client Secret**

2. **Obtain an Embed Token**
   - Use the Power BI REST API to generate an embed token for your report
   - Example using PowerShell or a backend script:
   ```powershell
   POST https://api.powerbi.com/v1.0/myorg/groups/{groupId}/reports/{reportId}/GenerateToken
   ```

3. **Embed Using the JavaScript SDK**
   - Add the Power BI Client SDK to your webpage:
   ```html
   <script src="https://npmcdn.com/powerbi-client@2.22.0/dist/powerbi.min.js"></script>
   ```
   - Initialize and embed the report:
   ```javascript
   const embedConfiguration = {
       type: 'report',
       id: 'YOUR_REPORT_ID',
       embedUrl: 'YOUR_EMBED_URL',
       accessToken: 'YOUR_EMBED_TOKEN',
       settings: {
           filterPaneEnabled: true,
           navContentPaneEnabled: true
       }
   };

   const report = powerbi.embed(reportContainer, embedConfiguration);
   ```





## Key Insights and Best Practices

### 1. Choose the Right Embedding Method
- **Publish to Web**: Quick and easy for public reports, but no row-level security. Use only for non-sensitive data.
- **Embed for Organization**: Leverages existing Power BI licenses. Users must sign in to view the report. Supports full security and row-level security.
- **Power BI Embedded (ISV)**: Best for embedding in applications you sell. Requires Azure registration and backend token generation.

### 2. Security Considerations
- Never expose your `.pbix` file credentials or embedded tokens publicly
- For sensitive data, always use row-level security (RLS) and embed with organizational authentication
- Regularly rotate your application secrets in Azure

### 3. Performance Optimization
- Use the **Power BI Service** to schedule dataset refreshes so your embedded report always shows current data
- Avoid embedding too many reports on a single page — each iframe consumes resources
- Consider using **Power BI paginated reports** for print-ready layouts instead of standard reports

### 4. Mobile Responsiveness
- Design your reports with **phone layouts** in Power BI Desktop
- Use responsive iframe sizing (`width="100%"`) in your website to ensure the report adapts to different screen sizes

### 5. Collaboration and Governance
- Use workspaces to organize reports by department or project
- Leverage **Power BI deployment pipelines** for moving reports between Development, Test, and Production environments
- Set up **workspaces with Premium capacity** if you need faster performance and larger dataset sizes

### 6. Tracking and Analytics
- For public embeds, you can track usage via Power BI's usage metrics
- For embedded applications, implement custom telemetry to monitor how users interact with your reports

---

## Conclusion

Publishing and embedding a Power BI report is a straightforward process that transforms how you share data insights. By creating a workspace in the Power BI Service, publishing your `.pbix` file, configuring embed settings, and pasting the embed code into your website, you can deliver interactive, real-time dashboards directly to your audience — whether they are internal stakeholders or external customers.

Remember to choose the embedding method that aligns with your security requirements, optimize your reports for performance, and leverage Power BI's governance features to maintain control over your analytics assets. With Power BI's publishing and embedding capabilities, your data stories can reach anyone, anywhere, on any device.

