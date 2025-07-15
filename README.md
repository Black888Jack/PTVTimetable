# 🚉 PTV Smart Widget for iOS

A smarter, more personal way to track your Melbourne train, tram, or bus — right from your iPhone home screen.

This Scriptable widget fetches **live PTV departure info** and routes based on:
- 📍 Your **location** (postcode-based)
- ⏰ The **time of day**
- 🛠 A fallback **default route**

Perfect for commuters who use the same route frequently and want to skip manually opening the PTV app.

> ⚠️ Not affiliated with PTV or Myki. This widget is for personal use only.

---

### 🔥 Key Features
- **Smart routing**: Automatically picks the right route based on your location, time, or a fallback
- **Live ETD** (Estimated Departure Times)
- **Scheduled time vs real time** (AM/PM format)
- **Express train flag** and **platform info**
- **Cached postcode fallback** when offline
- **Disruption alerts** with tap-through link

---

### 📲 How to Install on iPhone

> Requires the [Scriptable app](https://apps.apple.com/us/app/scriptable/id1405459188)

#### 1. Install Scriptable
Download it from the App Store if you haven’t already.

#### 2. Add a New Script
- Open Scriptable
- Tap **+** to create a new script
- Copy and paste the full code from [`ptv-smart-widget.js`](./ptv-smart-widget.js)
- Tap the name to rename it to something like `PTV Widget`

#### 3. Customise Your Routes
Near the top of the script, edit the `routingRules` to suit your needs:

```js
const routingRules = [
  ["Southern Cross Station", "Syndal Station", "3000", "train", "Glen Waverley"],
  ["Southern Cross Station", "Syndal Station", [12, 14], "train", "Glen Waverley"],
  ["Syndal Station", "Flinders Street Station", "default", "train", "Glen Waverley"]
];
