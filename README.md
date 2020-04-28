# TrackerControl

**If you're missing features or find bugs, discuss these on [Matrix or Telegram](#installation), use the [issue tracker](https://github.com/OxfordHCC/tracker-control-android/issues) or contact Konrad directly (tc@kollnig.net).**

TrackerControl allows users to monitor and control the widespread,
ongoing, hidden data collection in mobile apps about user behaviour ('tracking').

<p align="center">
  <img alt="TrackerControl Logo" src="images/logo.png" style="display: block; margin: 0 auto;" height="100%" width="200" >
</p>

To detect tracking, TrackerControl checks all network traffic against the Disconnect blocklist.
This is the same list, that is used by the Firefox browser.
This **reveals the companies behind tracking** to users
and allows users to **block tracking selectively**.
This blocklist also allows to expose the **purpose of tracking**, such as analytics or advertising.

The app further aims to educate users about their **legal rights** under
current EU Data Protection Law (i.e. GDPR and the ePrivacy Directive)

Under the hood, TrackerControl uses Android's VPN functionality,
to analyse apps' network communications *locally on the Android device*.
This is accomplished through a local VPN server, through which all network communications
are passed, to enable the analysis by TrackerControl.
In other words,
no external VPN server is used, and hence
no network data leaves the user's device for the purposes of tracker analysis.

## Installation
*Disclaimer: The usage of this app is at your own risk. No app can offer 100% protection against tracking.*

The app can be [downloaded here](https://github.com/OxfordHCC/tracker-control-android/releases).

## Communities

1. Telegram: https://t.me/TrackerControl
2. Matrix: https://matrix.to/#/!htazLJNOSogSGbSPQL:matrix.org?via=matrix.org

## Highlights
TrackerControl provides
- *real-time monitoring* of app tracking,
- *granular blocking* of app tracking,
- *one-click data requests* as granted under EU Data Protection Legislation, and
- [ad-blocking](ADBLOCKING.md) using widely available host files.

<p align="center">
    <img alt="Screenshot of main screen" src="images/main.png" style="display: block; margin: 0 auto;" height="100%" width="25%" >
    <img alt="Screenshot of trackers screen" src="images/trackers.png" style="display: block; margin: 0 auto;" height="100%" width="25%" >
    <img alt="Screenshot of actions screen" src="images/actions.png" style="display: block; margin: 0 auto;" height="100%" width="25%" >
</p>

Contrary to similar solutions, this application does not intercept SSL
connections, minimising privacy risks and allowing for usage on
unrooted Android devices.
Only the meta data about network communications is logged, and displayed
to the users.

## Privacy notice

TrackerControl allows users to monitor the network communications on their
Android device.
This network data qualifies as personal data, but is only processed
locally on the user's device.

If the user consents, TrackerControl contacts the Google Play Store
to retrieve further information about the users' apps.
The app automatically contacts GitHub to check for updates,
which can be disabled from the app settings.
No personal data is ever shared, other than what is strictly
necessary for network communications (e.g. IP address).

TrackerControl saves two pieces of information on the user's device:

1. a database of network communications, and
2. user settings.

This data is necessary for the functioning of TrackerControl.

This information is kept on the user's device until app data is
removed manually by the user (e.g. by uninstalling).

## Credits

The majority of the development was carried out by Konrad Kollnig (University of Oxford).

Yet, the development of this app would not have been possible without the help of many outstandings minds, including Max van Kleek, Katherine Fletcher, George Chalhoub, Sir Nigel Shadbolt and numerous app testers and friends.

Further, the app itself builds upon a range of publicly available tools, the foundation of this work.

- *VPN Functionality:* The underlying network analysis functionality is provided by the [NetGuard
Firewall](https://github.com/M66B/NetGuard), developed by Marcel Bokhorst.

- *Disconnect Tracker List:* TrackerControl integrates the [Disconnect list](https://github.com/mozilla-services/shavar-prod-lists) of known tracker domains,
that is distributed with the Firefox browser.

- *X-Ray Tracker List:* TrackerControl also uses the tracker database by Reuben Binns, Ulrik Lyngs,
Max Van Kleek, Jun Zhao, Timothy Libert, and Nigel Shadbolt from the [X-Ray project](https://www.sociam.org/mobile-app-x-ray).
This database was released as part of their 2018 paper on
[Third Party Tracking in the Mobile Ecosystem](https://doi.org/10.1145/3201064.3201089).
The original data can be retrieved [here](https://osf.io/4nu9e/).

- *Icons:* The app uses icons made by [bqlqn](https://www.flaticon.com/authors/bqlqn) from [www.flaticon.com](https://www.flaticon.com/), and a [rocket icon](https://www.iconfinder.com/icons/1608817/rocket_icon) by Dave Gandy under the SIL Open Font License

- *GDPR Requests:* For the GDPR requests, the templates from the website [My Data Done Right](https://www.mydatadoneright.eu/) by the NGO "Bits of Freedom" were adopted.

## License
This project is licensed under
[GPLv3](https://www.gnu.org/licenses/gpl-3.0.html).
