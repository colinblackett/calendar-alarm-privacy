# Calendar Alarm — Privacy Policy

_Last updated: 2026-05-12_

Calendar Alarm ("the app", package `com.melncoly.calendaralarm`) is published
by Colin Blackett ("the developer"). This document describes what data the
app accesses, what it does with that data, and what it deliberately does
**not** do.

## Summary

The app reads your device's calendar to schedule alarms. **Nothing leaves
your phone.** There is no server, no analytics, no third-party SDKs, and no
internet permission.

## What the app reads

The app reads from Android's local **Calendar Provider**
(`android.permission.READ_CALENDAR`) to find your upcoming calendar events
and schedule a phone alarm for the next one. The fields it reads:

- Event titles, start times, and end times.
- Display names of calendars you've added to your device.
- Your RSVP status on each event, so the app can skip events you've declined
  (and, depending on your in-app settings, ones you haven't responded to).

The Calendar Provider is the same data source the Android system Calendar
app reads from. The app does not directly access your Google account, any
online calendar service, or any other cloud system.

## What the app does NOT do

- **Does not transmit data.** The app does not declare the `INTERNET`
  permission, so it is technically incapable of sending data over the
  network. Everything happens locally on your device.
- **Does not collect, store, or share personal information** with the
  developer or any third party.
- **Does not include analytics, crash reporting, or advertising SDKs.**
- **Cannot modify your calendar.** The app declares only `READ_CALENDAR`,
  not `WRITE_CALENDAR`.
- **Cannot see your Google account credentials.** No `GET_ACCOUNTS`,
  `MANAGE_ACCOUNTS`, or OAuth flows are used.

## Other permissions

| Permission | Purpose |
| --- | --- |
| `USE_EXACT_ALARM`, `SCHEDULE_EXACT_ALARM` | Schedule a wake-up alarm at the next calendar event's start time minus your chosen lead time. |
| `POST_NOTIFICATIONS` | Show a status notification ("Next alarm: …") and the alarm-ringing notification. |
| `USE_FULL_SCREEN_INTENT` | Show the alarm UI over the lock screen, like the system alarm clock. |
| `RECEIVE_BOOT_COMPLETED` | Re-arm any scheduled alarm after the phone reboots. |
| `WAKE_LOCK`, `TURN_SCREEN_ON` | Wake the device and turn the screen on when the alarm rings. |
| `VIBRATE` | Vibrate during the alarm. |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_SHORT_SERVICE` | Run the alarm-ringing service while the alarm sounds. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Let you (optionally) grant a battery-optimization exemption so alarms remain reliable. |

## Data retention

The only state the app keeps is your in-app settings — which calendars to
watch, lead time, sound choice, vibration pattern, and similar preferences —
stored in Android's private DataStore inside the app's sandbox. Uninstalling
the app removes everything.

## Children

The app is not directed at children. It does not collect any data that
could be used to identify a user, regardless of age.

## Changes to this policy

If the policy changes, the **Last updated** date above will be updated.
Material changes will also be highlighted in the app's release notes on
Google Play.

## Contact

Questions or concerns: [colin@cenithinnovations.com](mailto:colin@cenithinnovations.com).
