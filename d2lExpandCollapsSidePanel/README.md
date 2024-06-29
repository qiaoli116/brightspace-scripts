
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

-   ![Screenshot 1: Script embedded in a Brightspace content page](https://github.com/qiaoli116/brightspace-scripts/assets/26584180/d3b9f349-0f50-4834-9216-4956ee2653a4)
-   This screenshot should show the button displayed next to the content area.
-   [Screenshot 2: Side panel expanded](screenshot2.png) - This screenshot should show the button labeled "Collapse Side Panel" with the side panel expanded.
-   [Screenshot 3: Side panel collapsed](screenshot3.png) - This screenshot should show the button labeled "Expand Side Panel" with the side panel collapsed.

**Additional Notes:**

-   You can modify the `sidePanelQuery` variable to target a different element if needed.
