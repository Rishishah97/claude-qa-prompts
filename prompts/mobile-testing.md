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
