# 📱 Mobile Testing Prompts

Use these prompts to generate mobile-specific test cases covering devices, OS versions, gestures, and network conditions.

---

## 1. Generate Mobile Test Cases for a Feature

```
You are a mobile QA engineer. Generate test cases for the following mobile feature.

Feature:
[Describe the feature]

Platform: [iOS / Android / Both]
App type: [Native / React Native / Flutter / Hybrid]

Cover:
- Core functionality on both platforms (if applicable)
- Device-specific behaviour (different screen sizes, notches, foldables)
- OS version compatibility (latest and N-1)
- Portrait and landscape orientation
- Gesture interactions (tap, swipe, pinch, long press)
- Keyboard and input behaviour
- Background / foreground app switching
- Push notifications (if relevant)
- Offline and low connectivity scenarios
```

---

## 2. Generate Device and OS Compatibility Test Matrix

```
Create a device and OS compatibility test matrix for the following mobile app.

App details:
- Platform: [iOS / Android / Both]
- Minimum supported OS: [e.g. iOS 15 / Android 10]
- Target audience: [e.g. global / UK / enterprise users]

Generate a test matrix that includes:
- Priority device categories (flagship, mid-range, budget, tablet)
- OS versions to test (with rationale based on market share)
- Screen size categories to cover
- Manufacturer-specific considerations (Samsung, Huawei, etc.)
- Browser considerations (for hybrid/PWA apps)

Format as a table with Device, OS Version, Screen Size, Priority, and Notes.
```

---

## 3. Network Condition Test Scenarios

```
Generate test scenarios for the following mobile app under varying network conditions.

App:
[Describe the app and its key data-heavy features]

Create scenarios for:
- No connectivity (airplane mode)
- Intermittent connectivity (flaky network)
- Switching between WiFi and mobile data
- 2G / 3G / 4G / 5G speed simulation
- High latency connections
- App behaviour when connection drops mid-action (e.g. during a payment or file upload)
- Reconnection handling and data sync

For each scenario include: condition, steps, expected behaviour, and pass/fail criteria.
```

---

## 4. Mobile Performance Test Cases

```
Generate performance test cases for the following mobile app.

App:
[Describe the app]

Platform: [iOS / Android / Both]

Cover:
- App launch time (cold start and warm start)
- Screen transition speed
- Scroll and animation smoothness (frame rate)
- Memory usage during extended sessions
- Battery consumption during typical usage
- Network request response times
- Behaviour under low battery / low memory conditions
- App size and install time

For each test: metric to measure, how to measure it, and acceptable threshold.
```

---

## 5. Mobile Accessibility Test Cases

```
Generate accessibility test cases for a mobile app.

Platform: [iOS / Android / Both]
Key screens to test: [list screens]

Cover:
- VoiceOver (iOS) / TalkBack (Android) screen reader support
- Font size scaling (small to largest accessibility size)
- Colour contrast ratios
- Touch target sizes (minimum 44x44pt)
- Focus order and navigation logic
- Alternative text for images and icons
- Error messages accessible to screen readers
- Timeout warnings and sufficient time limits

Reference: WCAG 2.1 AA and platform-specific guidelines (Apple HIG / Material Design).
```

---

## 6. Generate Interrupt and Notification Test Cases

```
Generate test cases for how the app handles interruptions and system notifications.

App:
[Describe the app and any active states — e.g. playing audio, recording, mid-form fill]

Cover:
- Incoming phone call during active session
- SMS / push notification received
- Low battery warning
- App moved to background then restored
- Device locked and unlocked mid-session
- Other apps stealing audio focus
- Permission dialogs interrupting flow (camera, location, mic)
- App killed by OS due to low memory, then relaunched
- Behaviour after device restart with the app in a specific state
```

---

## 7. Generate App Store Submission Test Checklist

```
Create a pre-submission test checklist for the following mobile app before release to the App Store or Google Play.

App:
[Describe the app]

Platform: [iOS / Android / Both]

Cover:
- App launches without crash on all target devices
- All deep links work correctly
- Push notifications function end-to-end
- In-app purchases complete successfully (if applicable)
- Privacy permissions requested correctly (no over-asking)
- App works correctly after update from previous version
- Offline behaviour is graceful
- App icon, splash screen, and screenshots match store listing
- No debug logs, test credentials, or placeholder content visible
- Compliance with platform guidelines (Apple App Review / Google Play Policy)
```

---

## 8. Generate Battery and Resource Usage Test Cases

```
Generate test cases to evaluate battery and resource usage for the following mobile app.

App:
[Describe the app and its background behaviours]

Platform: [iOS / Android / Both]

Cover:
- Battery drain during typical 30-minute active session
- Background battery usage (location tracking, sync, push)
- CPU usage during heavy operations (video, large data loads)
- Memory usage over an extended session (1+ hour)
- Memory release when app goes to background
- Network data consumption per session
- Storage growth over time (cache, downloaded files)
- Behaviour under thermal throttling (device gets hot)

For each: how to measure, tool to use, and acceptable threshold.
```

---

## 9. Write Test Cases for Mobile Deep Links and Universal Links

```
Generate test cases for deep links and universal links in the following mobile app.

App:
[Describe the app]

Deep link scheme: [e.g. myapp://]
Universal link domain: [e.g. https://myapp.com]

Deep links to test:
[List the key deep links — e.g. myapp://product/123, myapp://profile]

Cover:
- Link opens correct screen when app is installed and open
- Link opens correct screen when app is installed but in background
- Link opens correct screen when app is installed but closed (cold start)
- Link falls back to web correctly when app is not installed
- Invalid or malformed deep links handled gracefully
- Deep links from: browser, email, QR code, AirDrop/Share sheet
- Authentication state respected (redirect to login if not authenticated)
```

---

## 10. Generate Localisation and Internationalisation Test Cases

```
Generate test cases to validate localisation (l10n) and internationalisation (i18n) for the following mobile app.

App:
[Describe the app]

Supported locales: [e.g. en-GB, fr-FR, de-DE, ar-SA, ja-JP]

Cover:
- All UI strings translated (no English fallbacks visible)
- Text expansion handled (German text is ~30% longer than English)
- RTL layout for Arabic/Hebrew locales
- Date, time, and number formats match locale conventions
- Currency symbols and formatting correct per locale
- Pluralisation rules applied correctly
- Images and icons culturally appropriate per region
- App Store / Play Store listing localised
- Device locale change reflected without app restart
```
