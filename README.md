<div align="center">

# ⚡ FitX — Indian Fitness PWA

### Your all-in-one health & fitness companion, built for India.

#### *Calories • Diet • Workouts • Learn • Reminders — all in one app-like website*

<br/>

![FitX Banner](https://img.shields.io/badge/FitX-Indian%20Fitness%20App-00e5ff?style=for-the-badge&labelColor=000000&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHRleHQgeT0iMTgiIGZvbnQtc2l6ZT0iMTgiPuKaoeefj/wvaW5mbz48L3N2Zz4=)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-69ff47?style=for-the-badge&labelColor=000000)
![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-ffd740?style=for-the-badge&labelColor=000000)
![Single File](https://img.shields.io/badge/Single-HTML%20File-e040fb?style=for-the-badge&labelColor=000000)
![India Focused](https://img.shields.io/badge/🇮🇳-India%20Focused-ff9933?style=for-the-badge&labelColor=000000)

<br/>


> **Zero installs. Zero dependencies. One HTML file. Works like a native app.**

</div>

-----

## 📱 Live Demo

> Open `FitX.html` in any browser — or host it anywhere and add it to your home screen.

```
📂 FitX.html   ← The entire app. That's it.
```

-----

## ✨ Features

### 🔢 Calorie Calculator

- Uses the **Mifflin-St Jeor BMR formula** (industry standard)
- Inputs: Name, Age, Gender, Height, Current Weight, Target Weight, Activity Level, Goal
- Outputs: BMR, TDEE (maintenance), Target Calories, BMI with animated scale
- Recommended **macros** (Protein / Carbs / Fats) with animated bars
- Personalised tip with water intake recommendation

### 🍱 Indian Diet Plans

- Separate **Vegetarian** and **Non-Vegetarian** daily meal plans
- 5 meals per day: Breakfast, Mid-Morning Snack, Lunch, Evening Snack, Dinner
- All Indian foods — Roti, Dal, Paneer, Rajma, Chicken, Eggs, Soya, Curd, Rice & more
- Per-meal calorie and macro breakdown (tap to expand)
- High-protein focus with a reference table of protein-dense Indian foods
- Daily totals: Calories / Protein / Carbs / Fats

### 🏋️ Workout Plans

- **12 complete weekly plans** — every combination of:
  - 3 levels: Beginner • Intermediate • Advanced
  - 2 locations: Home • Gym
  - 2 goals: Fat Loss • Muscle Gain
- Full 7-day structure with rest days, exercise names, sets/reps, and muscle focus
- Tap any day to expand exercises

### 📚 Learn Calories

- Plain-language explanation of calories, BMR, TDEE, deficits & surpluses
- Calorie reference table for **popular Indian dishes** (Dal Tadka to Biryani)
- Hand-based **portion control guide**
- Macro gram-to-calorie cheat sheet
- Recommended fitness tracking apps for India (HealthifyMe, MyFitnessPal, etc.)
- Key fitness glossary (TDEE, NEAT, Progressive Overload, etc.)

### ⏰ Reminders & Tools

- **⏱️ Workout Countdown Timer**
  - 8 quick presets: 1, 5, 10, 15, 20, 30, 45, 60 minutes
  - Custom timer: set any minutes + seconds
  - Animated circular progress ring (glows cyan → green on completion)
  - Start / Pause / Resume / Reset
  - Vibration feedback on completion (Android)
  - Push notification when timer ends
  - Session log — last 5 completed timers saved locally
- **🔔 Daily Reminders** with browser push notifications
  - Morning Workout, Meal Prep, Water Reminder, Evening Workout, Sleep
  - Each with a toggle switch; saves state across sessions
- **🔥 Daily Check-in Streak** tracker (localStorage-persisted)
- **💧 Water Intake Tracker** — tap 8 glasses, resets daily
- **Add to Home Screen** instructions (Android & iOS)
- **Motivational Quotes** with Indian-relevant content

-----

## 🚀 Getting Started

### Option 1 — Open Directly

```bash
# Just open in browser — no server needed for basic use
open FitX.html
```

### Option 2 — Serve Locally (recommended for PWA features)

```bash
# Python
python3 -m http.server 8080

# Node.js
npx serve .

# Then open: http://localhost:8080/FitX.html
```

### Option 3 — Deploy to GitHub Pages

```bash
git init
git add FitX.html README.md
git commit -m "🚀 Initial FitX release"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/fitx.git
git push -u origin main
```

Then enable **GitHub Pages** → `Settings → Pages → Branch: main → / (root)`.

Your app will be live at: `https://YOUR_USERNAME.github.io/fitx/FitX.html`

-----

## 📲 Add to Home Screen (PWA)

FitX is a full **Progressive Web App (PWA)** — install it like a native app:

|Platform                 |Steps                                                  |
|-------------------------|-------------------------------------------------------|
|**Android (Chrome)**     |Open site → Tap `⋮` menu → **“Add to Home screen”**    |
|**iOS (Safari)**         |Open site → Tap `Share (□↑)` → **“Add to Home Screen”**|
|**Desktop (Chrome/Edge)**|Address bar → Click install icon → **“Install”**       |

Once installed, FitX:

- Opens in fullscreen with no browser UI
- Works **offline** after first load (Service Worker caches assets)
- Appears on home screen with its own icon

-----

## 🏗️ Tech Stack

|Layer           |Technology                                          |
|----------------|----------------------------------------------------|
|Structure       |Pure HTML5                                          |
|Styling         |Pure CSS3 (CSS Variables, Grid, Flexbox, Animations)|
|Logic           |Vanilla JavaScript (ES6+)                           |
|Fonts           |Google Fonts — Bebas Neue + Plus Jakarta Sans       |
|Offline         |Service Worker API (Cache-first strategy)           |
|Install         |Web App Manifest (injected via JS Blob URL)         |
|Notifications   |Notification API                                    |
|Storage         |localStorage                                        |
|Vibration       |Vibration API                                       |
|**Dependencies**|**None**                                            |


> 🏆 **Zero npm. Zero frameworks. Zero build steps.** Just one `.html` file.

-----

## 🗂️ Project Structure

```
fitx/
├── FitX.html          # The entire app — HTML + CSS + JS in one file
└── README.md          # This file
```

Everything is self-contained in `FitX.html`:

```
FitX.html
├── <head>              → Meta tags, PWA manifest, Google Fonts link
├── <style>             → ~600 lines of CSS (variables, layout, animations)
├── <body>
│   ├── .app-header     → Logo + streak counter
│   ├── .main-content   → 5 tab panels
│   │   ├── #panel-calc     → Calorie Calculator
│   │   ├── #panel-diet     → Diet Plans
│   │   ├── #panel-workout  → Workout Plans
│   │   ├── #panel-learn    → Learn Calories
│   │   └── #panel-remind   → Reminders + Timer
│   └── .bottom-nav     → 5-tab navigation bar
└── <script>            → ~900 lines of JS (logic, data, PWA setup)
```

-----

## 🎨 Design System

FitX uses a **Shiny Black** design language — inspired by premium dark-mode interfaces:

```css
/* Core Palette */
--bg:       #000000   /* Pure black background      */
--card:     #111111   /* Elevated card surfaces      */
--orange:   #00e5ff   /* Electric cyan — primary     */
--green:    #69ff47   /* Neon green — success/veg    */
--gold:     #ffd740   /* Gold — calories & timer     */
--purple:   #e040fb   /* Electric purple — accent    */
```

**Typography:** Bebas Neue (display/numbers) + Plus Jakarta Sans (body text)

-----

## 🧮 Calorie Formula

FitX uses the **Mifflin-St Jeor equation** for BMR calculation:

```
Male:   BMR = (10 × weight_kg) + (6.25 × height_cm) − (5 × age) + 5
Female: BMR = (10 × weight_kg) + (6.25 × height_cm) − (5 × age) − 161

TDEE = BMR × Activity Multiplier
  Sedentary      → × 1.2
  Lightly Active → × 1.375
  Moderately     → × 1.55
  Very Active    → × 1.725
  Extra Active   → × 1.9

Fat Loss   = TDEE − 400 kcal
Muscle Gain = TDEE + 300 kcal

Protein = body_weight_kg × 1.8–2.2g
Fats    = 25% of target calories ÷ 9
Carbs   = remaining calories ÷ 4
```

-----

## 📊 Data Coverage

|Section            |Data Points                                          |
|-------------------|-----------------------------------------------------|
|Workout Plans      |12 complete weekly plans (7 days each = 84 day-plans)|
|Diet Meals         |10 meal entries (5 veg + 5 non-veg) with full macros |
|Indian Food Table  |10 common dishes with calories + protein             |
|Protein Reference  |8 high-protein Indian foods                          |
|Motivational Quotes|10 quotes (including desi content)                   |
|Reminder Types     |5 preset daily reminders                             |
|Timer Presets      |8 quick-select durations                             |

-----

## 🔒 Privacy

FitX is **100% client-side**:

- ✅ No data sent to any server
- ✅ No analytics, no tracking, no cookies
- ✅ No account or sign-up required
- ✅ All data stored locally on your device (localStorage)
- ✅ Works fully offline after first load

-----

## 🤝 Contributing

Contributions are welcome! Here are some ideas:

- [ ] Add more Indian meal plan variations (South Indian, Gujarati, Bengali)
- [ ] BMI chart history with date tracking
- [ ] Progressive overload tracker (log weights per exercise)
- [ ] Meal calorie search/lookup
- [ ] Dark/light theme toggle
- [ ] Multi-language support (Hindi, Tamil, Telugu, etc.)
- [ ] Export calorie results as PDF/image
- [ ] Ramadan/fasting meal plans
- [ ] Rest timer between sets

```bash
# Fork → Clone → Edit FitX.html → Test in browser → Pull Request
git clone https://github.com/YOUR_USERNAME/fitx.git
cd fitx
# Make your changes to FitX.html
# Open in browser to test
# Submit PR
```

-----

-----

## 🙏 Acknowledgements

- **Mifflin-St Jeor (1990)** — BMR formula used by most dietitians worldwide
- **Google Fonts** — Bebas Neue & Plus Jakarta Sans
- **Indian fitness community** — HealthifyMe, Fittr, and the desi gym culture 💪
- Built with ❤️ for India 🇮🇳

-----

<div align="center">

**Made for India. No BS. Just Results. 💪**

⚡ *FitX — Train Hard. Eat Smart. Stay Consistent.*

</div>
