# Important Integration Notes


<h4><code>data-model-id</code> Must Point to a Valid Model</h4>
<p>
  The widget also needs a valid <code>data-model-id</code> to render a product view. This value can be:
  <ul>
    <li><strong>Hardcoded</strong> (for quick testing)</li>
    <li><strong>Dynamically retrieved</strong> using the Model Search API</li>
  </ul>
</p>

<h3>🔍 How to Get a <code>model-id</code> from a Model Number</h3>
<p>You can query our <strong>Model Search API</strong> using your <code>model_number</code>. But first, you'll need to generate an authentication token.</p>

<h4>🔐 Step 1: Generate Token</h4>
<p>Send a <code>POST</code> request to:</p>
<pre><code>https://manage.macaan.ai/api/extern/verify</code></pre>

<p>With this JSON payload:</p>
<pre><code>{
  "user_id": "your_user_id",
  "project_id": "your_project_id"
}</code></pre>

<p>Response:</p>
<pre><code>{
  "token": "your_generated_token"
}</code></pre>

<h4>🔎 Step 2: Use Token to Query Model</h4>
<p>Send a <code>GET</code> request to:</p>
<pre><code>https://manage.macaan.ai/api/extern/models/search?query=MODEL_NUMBER</code></pre>

<p>Include the token in the Authorization header:</p>
<pre><code>Authorization: Bearer your_generated_token</code></pre>

<p>This will return a list of models with their <code>model_id</code>. Use the correct <code>model_id</code> in your script tag.</p>

<hr />

<h4>✅ Summary Flow</h4>
<ol>
  <li>Contact Product Suite team for <code>user_id</code> and <code>project_id</code>.</li>
  <li>Generate token via <code>/api/extern/verify</code>.</li>
  <li>Use token to search for model ID via <code>/api/extern/models/search?query=...</code>.</li>
  <li>Add the <code>model_id</code>, <code>user_id</code>, and <code>project_id</code> to your widget script.</li>
  <li>Done ✅ — your widget is ready to use.</li>
</ol>
