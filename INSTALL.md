# Install Zorofin on LG webOS

Download `org.zorofin.tv_1.4.0_all.ipk` from the release and verify it with `SHA256SUMS`. You need your own Jellyfin server and lawful media. No server, account, channels or subscriptions are included.

## Developer Mode / DevMode Manager

Enable LG's Developer Mode app, pair your computer, and use webOS DevMode Manager's local IPK install action. The same file can be installed through LG CLI or webOS Studio. Root is not required by Zorofin. Keep Developer Mode active; LG removes its apps when Developer Mode is disabled.

```sh
ares-install --device YOUR_TV_ALIAS org.zorofin.tv_1.4.0_all.ipk
ares-launch --device YOUR_TV_ALIAS org.zorofin.tv
```

Use your own paired alias. Do not uninstall an existing account-bearing app to force an update. Compare is a separate test app and is not included here.

## Homebrew Channel

The webOSbrew central-catalog submission is a separate review. Until its maintainers accept the entry, this release does not imply catalog availability. The owner tested the installed 1.4 baseline on LG B5/webOS 25; this release adds an automatically validated Catch Up focus fix without a new physical-TV retest; Homebrew/rooted installation and cross-store updates are not independently accepted by those tests.

LG instructions: https://webostv.developer.lge.com/develop/getting-started/developer-mode-app
DevMode Manager: https://github.com/webosbrew/dev-manager-desktop

Detailed guide: https://zorofin.app/lg-tv
