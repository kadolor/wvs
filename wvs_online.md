# Get Started: WVS Online

This guide details how to use Wherobots Visual Studio (WVS) Online in Python to create a 3DE™️ powered image of your tabular data.
## Expectation


* WVS uses the provided coordinates to discern a place's location.
   * In `examples/001.csv`, the coordinates are the location of a hiking trail in Tokyo, Japan.
* WVS converts these coordinates to a contextually aware image.

## Prerequisites

Before beginning this Get Started tutorial, you must have the following:

* A Wherobots account. If you don't have an account yet, see [Creating Your Wherobots Account](https://docs.wherobots.com/latest/get-started/create-account/).
* A valid Wherobots API key. If you don't have an API key, see [API Keys](https://docs.wherobots.com/latest/get-started/api-keys/).

## Run a geospatial query

1. Login to [Wherobots Cloud](https://cloud.wherobots.com/).
2. On the left-hand side click **Wherobots Visual Studio**.
   
   ![nav](/images/navigation.png)

3. In the **Convert geospatial data** section, select `examples/001.csv` from the dropdown menu.
   
   ![convert](/images/convert.png)

4. Click **Start**. Wait between 2 to 3 minutes.

At this point, you should see the following contextually-aware image of a hiking trail in Japan:

![2d_3de](/images/dimension.png)

## What's next?

Only paid Wherobots users can convert additional data points. To convert data that isn't included in the default `examples` directory, you must upgade your account.

To learn more about upgrading your account, click the button below.
   
<div style="text-align: center;">
  <a href="https://wherobots.com/pricing/" class="button" style="display: inline-block; padding: 10px 20px; font-size: 16px; color: white; background-color: #007bff; border-radius: 5px; text-decoration: none; on-click: copyToClipboard;">See pricing plans</a>
</div>
<br>
<nav style="background-color: #333; padding: 10px;">
  <ul style="list-style-type: none; margin: 0; padding: 0; overflow: hidden;">
    <li style="float: left;"><a href="https://kadolor.github.io/wvs/" style="display: block; color: white; text-align: center; padding: 14px 16px; text-decoration: none; transition: background-color 0.3s;">Get Started</a></li>
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
