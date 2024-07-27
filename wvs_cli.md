---
title: WVS CLI Get Started
---

# Get Started: Wherobots Visual Studio Command line interface

This guide details how to get started using the Wherobots visual studio CLI to create a visual representation.

To showcase what's possible with WVS, this guide demonstrates how transform tabular geospatial data into a three dimensional data.

## Prerequisites

Before beginning this Get Started tutorial, you must have the following:

* A Wherobots account. If you don't have an account yet, see [Creating Your Wherobots Account](https://docs.wherobots.com/latest/get-started/create-account/).
* A valid Wherobots API key. If you don't have an API key, see [API Keys](https://docs.wherobots.com/latest/get-started/api-keys/).
* An active version of Python. For more information on active versions of Python, see [Active Releases](https://www.python.org/downloads/#Active-Python-Releasex) in the Python Documentation.
* A code editor or IDE.
* A packagage manager like `pip`.

## Establish your developement environment

To establish your developement environment you must:

* Install WVS
* Store your API Key

### Install WVS

To install WVS, do the following:

1. Within your command line, run the following command:

<div style="position: relative;">
  <pre><code id="code-sample">
    pip install wherobotsvs
  </code></pre>
  <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 5px 5px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
      <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
      <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
    </svg>
  </button>
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

1. Confirm that you have installed WVS successfully by running the followwing command:

<div style="position: relative;">
  <pre><code id="code-sample">
    python wherobotsvs -v
  </code></pre>
  <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 5px 10px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
      <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
      <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
    </svg>
  </button>
</div>

If installed WVS is installed successfully successfully, this command returns WVS' latest stable version.

### Store your API key

1. In your browser, go to [Wherobots Cloud](https://cloud.wherobots.com/).
   1. Click **Settings**
   2. Click **API keys**
   3. Copy your API Key. For more information, see [API Keys](https://docs.wherobots.com/latest/get-started/api-keys/).

1. Add the API key to your bash profile.
   1. From your command line,

       ```python
       python wherobotsvs -v
       ```
       
## Run a geospatial query

### View the tabular data

WVS contains an example directory with several CSV files that can be transformed with WVS.

1. Convert the example CSV into a dataframe
2. Enter the geometry
3. 

## What's next?
Unless you're a paid Wherobots user, you can't transform any additional data points.

To learn more about upgrading your account, click the button button below

<div style="text-align: center;">
  <a href="https://wherobots.com/pricing/" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; border-radius: 5px; text-decoration: none; on-click: copyToClipboard;">See pricing plans</a>
</div>

