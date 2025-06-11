## 🧩 Installation Guide

### 1. Add the Script Tag

Paste this inside your HTML (or inside `useEffect` in React):

```html
<script
  id="onsense-product-suite"
  src="https://product-suite-hazel.vercel.app/product-suite.js"
  data-color="#041E50"
  data-text-color="#252928"
  data-border-radius="3px"
  data-model-id="your_model_id"
  data-model-number="your_model_number"
  data-part-id="part_id"
  data-user-id="your_user_id"
  data-project-id="your_project_id"
  data-origin="https://your-website.com"
  data-questions='[{"question": "Example?"}]'
  defer
></script>
```
| Attribute            | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| `data-color`         | Primary brand/theme color (e.g., `#041E50`)                          |
| `data-text-color`    | Text color inside the widget                                         |
| `data-border-radius` | Rounded corners for UI components (e.g., `3px`, `8px`)               |
| `data-model-id`      | Unique ID for the model being shown                                  |
| `data-model-number`  | Model number label displayed in the widget                           |
| `data-part-id`       | Default part to highlight in the exploded view                       |
| `data-user-id`       | Your **User ID**, provided upon request by the Product Suite team    |
| `data-project-id`    | Your **Project ID**, provided upon request by the Product Suite team |
| `data-origin`        | The domain where the widget is embedded (used for origin validation) |
| `data-questions`     | JSON string of any preloaded questions to be passed to the widget    |


### 📌 Note

The following fields will be provided on request:

- `data-user-id`
- `data-project-id`

Contact the Product Suite team to obtain these credentials.

---

### 2. Add the Widget Containers

```html
<!-- 🧩 Parts Display Widget -->
<div
        id="onsense-parts"
        class="h-[1500px] md:h-[800px] w-full my-10"
></div>

<!-- 🔍 Exploded Views Widget -->
<div
        id="onsense-exploded-views"
        class="h-[1700px] md:h-[1200px] w-full mb-10"
></div>

<!-- 🚨 Error Codes Mapping Widget -->
<div
        id="onsense-error-codes"
        class="h-[560px] md:h-[400px] w-full mb-10"
></div>

<!-- 📘 Model Documentation Widget -->
<div
        id="onsense-docs"
        class="h-[1200px] md:h-[700px] w-full"
></div>

```
