# widget-integration

# Product Suite – Exploded Views Integration Guide

Welcome to the *Product Suite* – a powerful, plug-and-play component system that allows you to seamlessly integrate modular product features like *Exploded Views, **Parts, **Model View, and **Error Codes* into your own web application.

This guide explains how to integrate the *Exploded Views* feature into your project using a simple <script> tag and a container <div>.

---

## Features

-  Exploded Views (interactive)
-  Parts display
-  Error Codes mapping
-  Model View visualization
-  Fully customizable (colors, radius, layout)

---

## Installation & Usage

### 1. Add the Script Tag

Paste the following <script> tag *anywhere in your HTML or in your Next.js/React component (e.g., in useEffect)*:

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




| Attribute            | Description                                                          |
| -------------------- | -------------------------------------------------------------------- |
| data-color         | Primary theme color (e.g., brand color)                              |
| data-text-color    | Text color inside the component                                      |
| data-border-radius | Border radius for rounded corners (e.g., 3px, 8px)               |
| data-model-id      | Unique identifier for the model being viewed                         |
| data-model-number  | Model number to display                                              |
| data-part-id       | Default part ID to highlight                                         |
| data-user-id       | Your User ID (provided by Product Suite team)                        |
| data-project-id    | Your Project ID (provided by Product Suite team)                     |
| data-origin        | The domain where the widget is embedded (for security)               |
| data-questions     | JSON string of any preloaded questions you want passed to the widget |


2. Add the Container
<div>Wherever you want to display the Exploded Views, simply add the following <div>:


<div
  id="onsense-exploded-views"
  class="h-[1700px] md:h-[1200px] w-full mb-10"
></div>
