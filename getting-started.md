# Product Suite – Installation Guide

<p>
  Welcome to the <strong>Product Suite</strong> – a powerful, plug-and-play component system that enables you to seamlessly integrate advanced product visualization tools into your own web application.
</p>
<p>
  With just a few lines of code, you can add interactive views like:
</p>
<ul>
  <li>🧩 <strong>Parts Display</strong></li>
  <li>🔍 <strong>Exploded Views</strong></li>
  <li>📘 <strong>Model Documentation</strong></li>
  <li>🚨 <strong>Error Code Mapping</strong></li>
</ul>

<hr />

<h2>🎯 Key Features</h2>
<ul>
  <li><strong>Exploded Views</strong> — Interactive model breakdown with part relationships</li>
  <li><strong>Parts Display</strong> — Modular part-by-part rendering</li>
  <li><strong>Error Code Mapping</strong> — Smart error references with linked documentation</li>
  <li><strong>Model Documentation</strong> — Organized technical info, diagrams, and specs</li>
  <li><strong>Customizable UI</strong> — Colors, layout, text, and borders tailored to your brand</li>
</ul>

<hr />

## Add the Script Tag

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
  data-user-id="your_user_id"
  data-project-id="your_project_id"
  data-origin="https://your-website.com"
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
| `data-user-id`       | Your **User ID**, provided upon request by the Product Suite team    |
| `data-project-id`    | Your **Project ID**, provided upon request by the Product Suite team |
| `data-origin`        | The domain where the widget is embedded (used for origin validation) |


## Note

These credentials are unique to each client and must be requested from the Product Suite team. Without them, the script will not load the widget.

- `data-user-id`
- `data-project-id`

> Also for information on how to get `data-model-id` [click here](project_id_token.md).

---

## Add the Widget Containers

```html
<!-- 🧩 Parts Display Widget -->
<div
        id="onsense-parts"
        class="h-[1500px] md:h-[800px] w-full my-10"
></div>

```

```html

<!-- 🔍 Exploded Views Widget -->
<div
        id="onsense-exploded-views"
        class="h-[1700px] md:h-[1200px] w-full mb-10">
</div>

```

```html
<!-- 🚨 Error Codes Mapping Widget -->
<div
        id="onsense-error-codes"
        class="h-[560px] md:h-[400px] w-full mb-10"
></div>

```

```html
<!-- 📘 Model Documentation Widget -->
<div
        id="onsense-docs"
        class="h-[1200px] md:h-[700px] w-full"
></div>

```
