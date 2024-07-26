# Wherobots Visual Studio

Welcome to Wherobots Visual Studio (WVS), the fictitious geospatial visualization studio for building spatial workflows
and visualizing spatial data on WherobotsDB.

## What can you do with WVS?

Using the proprietary Dimensional Data Depiction Engine (3DE) ™️, Wherobots showcases the value in your flat data sources by creating engaging geospatial images that capture your insights.

## Get Started

You can use WVS from the command line or from the browser.

# Code Sample with Copy Button

Below is an example of a code block with a copy button.

<div style="position: relative;">
  <pre><code id="code-sample">
    // Your code here
    console.log('Hello, World!');
  </code></pre>
  <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 5px 10px; background-color: #007bff; color: white; border: none; border-radius: 5px; cursor: pointer;">Copy</button>
</div>

<script>
  function copyToClipboard() {
    const code = document.getElementById('code-sample').innerText;
    navigator.clipboard.writeText(code).then(() => {
      alert('Code copied to clipboard!');
    }, (err) => {
      console.error('Failed to copy: ', err);
    });
  }
</script>

<pre>Hello</pre>

<div style="text-align: center;">
  <a href="https://example.com" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; border-radius: 5px; text-decoration: none; on-click: copyToClipboard;">WVS CLI</a>
</div>
<br>
<div style="text-align: center;">
  <a href="https://example.com" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; border-radius: 5px; text-decoration: none;">WVS Online</a>
</div>
