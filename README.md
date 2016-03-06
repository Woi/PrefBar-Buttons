# PrefBar buttons

This are additional buttons created for use with [PrefBar](http://prefbar.tuxfamily.org/) in Mozilla based browsers.
Check AMO for [installing PrefBar](https://addons.mozilla.org/de/seamonkey/addon/prefbar/).
It's possible to reset settings to a desired default at browser start via [user.js](http://kb.mozillazine.org/User.js_file).
This is very useful to make sure changes are only temporary, even in cases you forgot to set them back.

## MinTLS

Use the MinTLS button to easily select the minimum supported SSL/TLS protocol version.
This allows to use a more secure setting in every days usage and only temporarly fall back should a server not support the modern TLS variants.
For SeaMonkey this setting also affect the connections made my MailNews, so your mail servers need to support the higher settings as well.

Please note that SSL 3.0 support was disabled by default in [December 2014](https://www.mozilla.org/en-US/firefox/34.0.5/releasenotes/) due to serious security issues.
So stick to TLS 1.0 and above.

Hardened TLS settings can be protected by adding `user_pref("security.tls.version.min", 3);` to `user.js`.

## Fx compat

This button allows to switch advertisement of Firefox compatibility in the user agent string of SeaMonkey and maybe other Mozilla-based browsers.
Some websites fail to correctly identify Mozilla browsers others then Firefox, due to parsing the user agent string for "Firefox" instead of testing for supported features or check type and version of the rendering engine.
Among these websites are Microsoft Outlook Web Access (OWA), Google Websearch and Google Maps.
There is an article on MDA [for details and better approches](https://developer.mozilla.org/en-US/docs/Browser_detection_using_the_user_agent).

Most Mozilla browsers come with Firefox compatibility enabled by default, but there are various reasons to disable it:
Be it out of curiosity which websites fail on a prober detection, be it to advocate a diverse web and support your favourite browser or be it because broken websites should not be fixed permanently by a dirty workaround.

This setting can be protected by adding `user_pref("general.useragent.compatMode.firefox", false);` to `user.js`.
