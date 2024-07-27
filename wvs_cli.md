---
title: Get Started: WVS CLI
---

# Get Started: WVS Command line interface (Python)

This guide details how to use the Wherobots Visual Studio CLI in Python to create a 3DE™️ powered image of your tabular data.

## Expectation

* WVS uses the provided coordinates to discern a place's location.  In this example, the coordinates are the location of a hiking trail in Tokyo, Japan.
* WVS converts these coordinates to a contextually aware image.

## Prerequisites

Before beginning this Get Started tutorial, you must have the following:

* A Wherobots account. If you don't have an account yet, see [Creating Your Wherobots Account](https://docs.wherobots.com/latest/get-started/create-account/).
* A valid Wherobots API key. If you don't have an API key, see [API Keys](https://docs.wherobots.com/latest/get-started/api-keys/).
* An active version of Python. For more information on active versions of Python, see [Active Releases](https://www.python.org/downloads/#Active-Python-Releasex) in the Python Documentation.
* A code editor or IDE.
* A packagage manager like `pip`.

## Establish your developement environment

To establish your developement environment you must:

* Install the WVS Python package
* Store your API Key

### Install WVS

To install WVS, complete the following steps:

1. Within your command line, run the following command:

    <div style="position: relative;">
      <pre><code id="code-sample">
        pip install wherobotsvs
      </code></pre>
      <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 1px 1px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
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

2. Confirm that you have installed WVS successfully by running the followwing command:

    <div style="position: relative;">
      <pre><code id="code-sample">
        python wherobotsvs -v
      </code></pre>
      <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 1px 1px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
          <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
          <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
        </svg>
      </button>
    </div>

If installed WVS is installed successfully, this command returns WVS' latest stable version.

### Store your API key

1. In your browser, go to [Wherobots Cloud](https://cloud.wherobots.com/).
   1. Login with your Wherobots username and password.
   2. Click **Settings**.
   3. Click **API keys**.
   4. Copy your API Key. For more information, see [API Keys](https://docs.wherobots.com/latest/get-started/api-keys/).

1. Add the API key to your bash profile.
   1. From your command line, open your bash profile.

    <div style="position: relative;">
      <pre><code id="code-sample">
        nano ~./bash_profile
      </code></pre>
      <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 1px 1px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
          <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
          <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
        </svg>
      </button>
    </div>
    
   2. Add your API key as a variable. 

    <div style="position: relative;">
      <pre><code id="code-sample">
        API_KEY = YOUR_API_KEY
      </code></pre>
      <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 1px 1px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
          <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
          <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
        </svg>
      </button>
    </div>

    Replace `YOUR_API_KEY` with the Wherobots API Key you previously copied.
    
## Run a geospatial query

WVS contains an example directory with several CSV files that can be transformed with WVS.

1. To generate a contextually aware 3DE image, run the following command:

<div style="position: relative;">
  <pre><code id="code-sample">
    python wherobotsvs --convert file="examples/001.csv"
  </code></pre>
  <button onclick="copyToClipboard()" style="position: absolute; top: 0; right: 0; padding: 1px 1px; background-color: #007bff; color: white; border: none; border-radius: 1px; cursor: pointer;">
    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-clipboard" viewBox="0 0 16 16">
      <path d="M10 1.5H6a.5.5 0 0 0-.5.5v1H4a2 2 0 0 0-2 2v8a2 2 0 0 0 2 2h8a2 2 0 0 0 2-2V5a2 2 0 0 0-2-2h-1.5v-1a.5.5 0 0 0-.5-.5zM6 2h4v1H6V2z"/>
      <path d="M4.5 3h7a1 1 0 0 1 1 1v8a1 1 0 0 1-1 1h-7a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1z"/>
    </svg>
  </button>
</div>

2. Wait 2 to 3 minutes.

At this point, you should see the following contextually-aware image of a hiking trail in Japan:

![2d_3de](/images/dimension.png)


## What's next?

Only paid Wherobots users can transform additional data points. To transform data that isn't included in the default `examples` directory, you must upgade your account.

To learn more about upgrading your account, click the button below.

<div style="text-align: center;">
  <a href="https://wherobots.com/pricing/" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; border-radius: 5px; text-decoration: none; on-click: copyToClipboard;">See pricing plans</a>
</div>
<br>
<nav style="background-color: #333; padding: 10px;">
  <ul style="list-style-type: none; margin: 0; padding: 0; overflow: hidden;">
    <li style="float: left;"><a href="/" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">Get Started</a></li>
    <li style="float: left;"><a href="https://kadolor.github.io/wvs/wvs_cli" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">WVS CLI</a></li>
    <li style="float: left;"><a href="https://kadolor.github.io/wvs/wvs_online" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">WVS Online</a></li>
    <li style="float: left;"><a href="https://kadolor.github.io/wvs/roadmap" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">Known Issues & Roadmap</a></li>
    <li style="float: left;"><a href="https://kadolor.github.io/wvs/methodology" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">Methodology</a></li>
  </ul>
</nav>
<div style="padding: 20px;">
</div>
<style>
  nav ul li a:hover {
    background-color: #575757;
  }
</style>
<div style="padding: 20px;">
</div>
