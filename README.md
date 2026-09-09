<div align="center">

<img src="img/icon.png" width="128" alt="PostureTomato">

# 🍅 PostureTomato

### A focus timer that sits up straight.

Wear AirPods. Settle in. Watch the fruit ripen while you hold the posture you started with.

**[→ posturetomato website](https://moecui22.github.io/posturetomato/)** · macOS 14+ · Free · No account, no tracking

</div>

---

<img src="img/crop-02-mirror.png" width="100%" alt="The tomato leaning, mirroring a tilted head">

## 🌱 What it does

A Pomodoro timer with a second job.

Start a session and a tomato grows on the vine while you work — **the vine is the clock.** Wear AirPods and something else happens: the tomato mirrors your head. Lean and it leans. Sink toward your shoulders and it sinks. Fifty times a second.

**Posture ripens the fruit.** Hold the position you settled into and the tomato ripens. Drift, and it stays pale. You read it out of the corner of your eye — no pop-up ever interrupts the focus the timer exists to protect.

Finish a session and it's harvested into your crate. 🥫 End early and it's squashed into a ketchup sachet, which sits in the drawer for seven days and then expires.

## ✨ Features

| | |
|---|---|
| ⏱️ | Pomodoro timer, focus and break lengths you choose |
| 🎧 | Live head-position mirroring through AirPods motion sensors |
| 🎯 | Five-second calibration — posture measured against *your* baseline |
| 🎨 | Ambient feedback through fruit colour, never a notification |
| 📊 | Posture summary at break time, not during focus |
| 📦 | Harvest crates for finished sessions, a ketchup drawer for abandoned ones |
| 🔔 | Hand-synthesised Japanese temple bell and water sounds — no audio files |
| 👒 | Tomatoes with hats, glasses and shoes, because why not |

## 🎧 Requirements

macOS 14 or later. Posture tracking needs **AirPods (3rd gen), AirPods Pro, AirPods Max, or Beats Fit Pro**.

Only one earbud in? That works — the app reports which ear it's reading and draws just that bud.

**No AirPods?** The timer, crates, drawer and sounds all work fine. You only lose the posture half.

## 🔒 Privacy

Motion data never leaves your Mac. No account, no analytics, **no networking code at all** — the binary links no networking frameworks and holds no network entitlement. Sessions live in local `UserDefaults`.

[Privacy policy](https://moecui22.github.io/posturetomato/privacy.html)

## 🔬 Notes on `CMHeadphoneMotionManager`

Things measured while building this, in case they save someone else the trouble:

- **Sample rate is 50 Hz**, not the 25 Hz widely repeated online.
- **Resting pitch sits around −39°**, not zero — the sensor is in your ear, not on the crown of your head. Calibration isn't a nicety, it's mandatory.
- **There's no magnetometer**, so yaw drifts and can't be trusted over a session. Pitch and roll are the usable channels.
- **Nothing tells you a bud came out.** There's no notification for it — you detect removal by watching for the stream to go silent.
- `sensorLocation` is annotated iOS-only in the macOS SDK but works anyway; read it via KVC.

## 🍅 A note on honesty

This app does **not** tell you whether your posture is good. It can't — head orientation alone cannot see your spine, and no app claiming otherwise from an earbud is being straight with you.

What it does is notice when you've drifted from the position *you* chose, and show you, gently.

---

<div align="center">

<img src="img/crop-05-done.png" width="420" alt="A ripe tomato inside a complete ring of vine">

© 2026 Eric Cui · [Website](https://moecui22.github.io/posturetomato/) · [Privacy](https://moecui22.github.io/posturetomato/privacy.html)

</div>
