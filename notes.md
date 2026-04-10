# Pod C - Build Notes

## Problem We're Solving

Motivation is the hardest part of starting a fitness routine. You tell yourself you'll go for a run tomorrow morning — but when the alarm goes off, you snooze it and go back to sleep. There's nothing stopping you.

## Our Approach

Build a fitness alarm that you literally cannot ignore. When the alarm fires, it plays a looping sound that won't stop until you either start your activity or complete your goal. You set it the night before — activity type, distance goal, alarm time — and the app holds you accountable in the morning.

## What We Built

**FitAlarm** — a mobile-first web app (single HTML file, no install needed) with:

- **4 activity types**: Run, Walk, Cycling, Gym
- **Goal setting**: distance in km (run/walk/cycling) or duration in minutes (gym)
- **Alarm scheduler**: set a time, app counts down and fires the alarm at that exact moment
- **Persistent alarm**: looping audio that can't be dismissed — only paused temporarily
- **Inactivity detection**: if you pause the sound and stop moving (via DeviceMotion API), the alarm auto-resumes after 25 seconds
- **GPS distance tracking**: real-time haversine distance calculation, auto-completes when you hit your goal
- **Progress ring**: live visual showing how far along you are
- **Workout summary screen**: distance, time, pace/speed, and a motivational message
- **Light/Dark mode**: toggle in the top corner, persists across sessions
- **Works on any phone browser** — no app store, no install

## How to Demo It

1. Open the app on your phone browser (or share the link)
2. Pick **Run**, set goal to **1 km**, set alarm time to **1 minute from now**
3. Tap **Set Alarm** — you'll see the countdown screen
4. Or tap **🔔 Test Now** to fire the alarm immediately (great for live demos)
5. When alarm fires — show the pulsing red screen and looping sound
6. Tap **Start Activity** — show the GPS tracking screen with live distance
7. Tap **Mark Complete** — show the workout summary with stats and motivational message

**Key demo moment**: tap "Test Now" on the standby screen to trigger the alarm instantly without waiting.

## What We'd Do Next

- Push notifications so the alarm works even when the browser is closed
- React Native / Expo version for a real app store release
- Streak tracking — consecutive days you hit your goal
- Social sharing — post your run stats to Instagram/X
- Integration with Apple Health / Google Fit

## Prompts That Worked Well

- *"Build a mobile-first fitness alarm web app as a single HTML file. Features: set activity type (run/walk/cycling/gym), set distance or time goal, set alarm time. When alarm fires, play a looping audio alarm that cannot be dismissed — only paused. If phone detects inactivity via DeviceMotion API, resume alarm. Use GPS for distance tracking. Include progress ring and completion screen."*

- *"Walk through the full user flow of this app as if you're a first-time user. Write down every issue you find, fix the top 3 demo-breaking bugs, and improve the completion screen."*

- *"Add light and dark mode with a toggle button. Persist the choice in localStorage."*
