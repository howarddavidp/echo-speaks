
## Why this fork (howarddavidp)

This fork exists to fix a Hubitat re-authentication redirect bug in upstream tonesto7 Echo Speaks: starting Amazon login / server setup from the app could send the browser to an **HTTP** `cloud.hubitat.com` URL instead of **HTTPS**.

**Fix:** `getAppEndpointUrl()` in `apps/echo-speaks.groovy` forces the Hubitat API base URL to HTTPS when `getApiServerUrl()` returns `http://…`. Local cookie-server URLs (for example `http://192.168.50.35:8091`) are unchanged on purpose.

Use this package in place of the upstream tonesto7 Hubitat Echo Speaks apps/drivers when you need that redirect fix. Pair it with a local cookie server (see [howarddavidp/echo-speaks-server](https://github.com/howarddavidp/echo-speaks-server) for the session-drop fixes).

<p align="center"><img src="https://raw.githubusercontent.com/tonesto7/echo-speaks/master/resources/icons/EchoSpeaks.png"></p>
<h2 align="center">
  Welcome to Echo Speaks
</h2>

<p align="center">
  <b>Links:</b><br>
  <a href="https://tonesto7.github.io/echo-speaks-docs">Documentation</a> |
  <a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HWBN4LB9NMHZ4">Donations</a>
</p>

<h4>Description:</h4>
<p>Integrate your Amazon Echo devices into your Hubitat environment to create virtual Echo Devices. These virtual devices will allow you to speak text, make announcements, control media playback including volume, and many other Alexa features.</p>

