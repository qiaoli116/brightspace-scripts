
## d2lExpandCollapseSidePanel.html: Expand/Collapse Brightspace Side Panel
This script adds a button to Brightspace content pages that allows the user to expand or collapse the left-side navigation panel.

**Features:**
-   Shows a button labeled "Expand Side Panel" or "Collapse Side Panel" depending on the current state.
-   Hides the button if the side panel is not found on the page.
-   Changes the button text and toggles the visibility of the side panel when clicked.

**How to Use:**
1.  Save the script as `d2lExpandCollapseSidePanel.html`.
2.  Upload the `d2lExpandCollapseSidePanel.html` file to the **Managed Files** in a Brightspace shell. Uploading to Managed Files ensures Brightspace hosts it as a static resource.
3.  Embed the script in a Brightspace content page using an iframe:

```html
<p style="margin: 0;">
    <iframe src="/content/enforced/<your-course-id>/d2lExpandCollapsSidePanel.html" style="
        border: none;
        height: 40px;
        width: 100%;
        overflow: hidden;"
    ></iframe>
</p>
```

**Important Note:**
-   Since the script modifies the parent document (`parent.document`) to access the side panel element, it's crucial that the script is hosted on the same domain (origin) as the Brightspace content page. Uploading the script to Brightspace's Managed Files fulfills this requirement.
-   **Identifying the Side Panel:** This script relies on a combination of the following class names (`d2l-box`,  `d2l-box-h`,  `d2l-twopanelselector-side`, and `d2l-twopanelselector-side-sep`) to identify the side panel element. These class names are based on an examination of the current Brightspace webpage structure. It's important to understand that these class names may change in future Brightspace updates. If the script stops working after a Brightspace update, you may need to adjust the `sidePanelQuery` variable in the script to target the updated side panel element's class names.

**Screenshots**
-   File uploaded to Managed Files in a Brightspace shell.
![image](https://github.com/qiaoli116/brightspace-scripts/assets/26584180/63250ccd-9f14-462c-96f3-4e3d671030c4)
-   Embeded code in a page
![image](https://github.com/qiaoli116/brightspace-scripts/assets/26584180/68cfdb28-92c9-4298-b778-e07c4f330239)
-   The button labeled "Collapse Side Panel" with the side panel expanded.
![Image](https://github.com/qiaoli116/brightspace-scripts/assets/26584180/d3b9f349-0f50-4834-9216-4956ee2653a4)
-   The button labeled "Expand Side Panel" with the side panel collapsed.
![image](https://github.com/qiaoli116/brightspace-scripts/assets/26584180/2a0647c3-6386-4728-a01c-8fb385822da7)

**Additional Notes:**
-   You can modify the `sidePanelQuery` variable to target a different element if needed.
