# 🌅 Human Awaking — Spiritual Wellness App

> **AI-powered breathwork, meditation & personal growth platform built with Flutter & Firebase**

---

## 🎯 Business Strategy: What Makes Wellness Apps $227M/Year

### The Revenue Formula (Calm = $227M, Headspace = $64.5M annually)

| Strategy | What Works | How We Implement |
|---|---|---|
| **Freemium Hook** | Free core draws users in, premium converts | Free: 3 breathwork sessions, basic streak. Premium: unlimited AI guidance, advanced programs |
| **Streak Psychology** | Daily habit = daily open = retention | Meditation & breathwork streaks with visual calendar heatmap |
| **Barnum Personalisation** | Users feel the app "gets" them | Onboarding quiz generates personalised Soul Profile — reads true for 95% of people |
| **Subscription Tiers** | Monthly $9.99 / Annual $69.99 / Lifetime $199 | Anchoring: lifetime looks cheap next to annual |
| **Daily Nudge** | Push notification at user's chosen "sacred time" | "Good morning [Name], your energy is calling" |
| **Progress Visibility** | Users stay to protect their streak | Streak counter, XP points, level system (Seeker → Sage → Awakened) |
| **Content Library** | New content = reason to return | Weekly new AI-generated guidance sessions |
| **B2B Corporate Wellness** | Headspace earns 30% from enterprise | Offer team packages for wellness studios, yoga centres |

---

## 🧠 The Barnum Effect — Built Into Every Screen

The Barnum/Forer Effect: people accept vague-but-positive descriptions as uniquely personal to them.

### How We Use It Ethically:

**Onboarding Soul Profile Quiz (5 questions):**
```
1. "What time of day do you feel most alive?" → Morning / Midday / Evening / Night
2. "Which element resonates with you?" → Fire / Water / Earth / Air
3. "What's your biggest challenge right now?" → Stress / Focus / Sleep / Purpose / Connection
4. "How do you recharge?" → Solo practice / Guided sessions / Community / Nature
5. "What does 'awakening' mean to you?" → Inner peace / Clarity / Energy / Connection
```

**Generated Soul Profile (Barnum-style, feels personal):**
> "You are a deeply intuitive person who sometimes carries more than others realise. You have an inner knowing that often goes unspoken — a natural sensitivity to energy, emotion, and the needs of those around you. You are on the edge of a significant personal shift."

This description fits ~87% of wellness app users — but every user feels it was written *for them*.

**Result:** Higher trust → Higher conversion → Higher retention

---

## 🎨 UI Design System — Fresh, Light & Crisp

### Design Philosophy
- **Default: Pure Light Mode** — white, airy, clean. Feels like morning sunlight.
- **Dark Mode Toggle** — available in settings & quick-access widget in top bar
- **No heavy dark backgrounds** — wellness = clarity = light
- **Inspired by:** Notion's cleanliness + Calm's warmth + Linear's precision

### Colour Palette

```dart
// LIGHT MODE (default)
primary:        #4A90D9  // Soft sky blue — trust, calm, clarity
secondary:      #7BC67E  // Sage green — growth, nature, healing  
accent:         #F4A261  // Warm amber — energy, warmth, sunrise
background:     #FAFAFA  // Near-white — clean, airy
surface:        #FFFFFF  // Pure white cards
textPrimary:    #1A1A2E  // Deep navy — readable, grounded
textSecondary:  #6B7280  // Mid grey — secondary info
border:         #E5E7EB  // Feather grey — subtle separation

// DARK MODE (toggle)
darkBackground: #0F172A  // Deep midnight
darkSurface:    #1E293B  // Slate card surface
darkPrimary:    #60A5FA  // Lighter blue
darkText:       #F1F5F9  // Soft white text
```

### Typography
```dart
headingFont:  'Playfair Display'  // Elegant serif — spiritual, premium feel
bodyFont:     'Inter'             // Clean sans-serif — readable, modern
monoFont:     'JetBrains Mono'   // For timers, counters
```

### Card Design
- Rounded corners: `borderRadius: 16px`
- Soft shadow: `boxShadow: 0 2px 12px rgba(0,0,0,0.06)`
- White background with `1px #E5E7EB border`
- Hover/tap: scale 0.98 + shadow increase

---

## 📱 Screen Architecture

### 1. Onboarding Flow (5 screens)
```
Splash → Soul Quiz → Profile Generated → Choose Goal → Paywall (soft) → Home
```
- Animated lotus/sun particle effect on splash
- Progress bar during quiz
- Profile reveal with typewriter animation
- Free trial CTA: "Begin Your 7-Day Awakening — Free"

### 2. Home Dashboard
```
┌─────────────────────────────────┐
│  ☀️  Good morning, Giustino      │  ← Personalised greeting
│  "You are ready for today"       │  ← Daily Barnum affirmation
├─────────────────────────────────┤
│  🔥 Streak: 7 days  🌿 Level: Seeker │
├─────────────────────────────────┤
│  [ TODAY'S PRACTICE ]           │
│  Wim Hof Morning Round          │
│  ⏱ 8 min  •  🌬️ Breathwork      │
│  [  BEGIN SESSION  ]            │
├─────────────────────────────────┤
│  [ AI SOUL READING ]            │
│  "Your energy today suggests..."│
│  [ VIEW FULL READING ]          │
├─────────────────────────────────┤
│  [ PROGRESS ]  [ COMMUNITY ]    │
└─────────────────────────────────┘
```

### 3. Breathwork Timer
```
- Full screen, clean white background
- Large animated circle (SVG path animation)
- Phase text: INHALE / HOLD / EXHALE in Playfair Display
- Round counter: 1 of 30
- Soft ambient sound (binaural tone)
- Completion screen: confetti + streak update
```

### 4. AI Soul Guide (Gemini-powered)
```
- Daily personalised reading based on:
  • Mood check-in slider (1-10)
  • Time of day
  • Current streak level
  • Soul Profile archetype
- Output: Affirmation + Breathwork rec + Grounding practice
- "This reading is for you alone" — reinforces Barnum effect
- Save reading to journal
```

### 5. Progress & Levels
```
LEVEL SYSTEM:
🌱 Seeker     (0-7 days)
🌿 Awakening  (8-30 days)
🌸 Blooming   (31-90 days)
☀️  Radiant    (91-180 days)
🌟 Sage       (181-365 days)
🔮 Awakened   (365+ days)

XP earned from:
- Completing sessions (+50 XP)
- Daily login (+10 XP)
- Sharing insight (+20 XP)
- Journaling (+30 XP)
```

### 6. Settings
```
- Light/Dark mode TOGGLE (top right, always visible)
- Sacred Time — choose daily reminder time
- Soul Profile — view & retake quiz
- Subscription management
- Privacy & data
```

---

## 💰 Monetisation Structure

### Free Tier
- 3 breathwork sessions per day
- Basic streak tracking
- 1 AI Soul Reading per week
- Community feed (read-only)

### Premium — $9.99/month or $69.99/year
- Unlimited breathwork + meditation sessions
- Daily AI Soul Reading
- Full content library (50+ programs)
- Advanced analytics & insights
- Offline mode
- Community posting

### Lifetime — $199 one-time
- Everything in Premium, forever
- Exclusive "Awakened" badge
- Early access to new features

### B2B Wellness Studio Package — $49/month per studio
- Branded version for yoga studios, retreat centres
- Team dashboard
- Custom content uploads

---

## 🔔 Retention Mechanics

| Mechanic | Psychology | Implementation |
|---|---|---|
| Daily streak | Loss aversion | Streak breaks hurt more than gains feel good |
| Sacred Time notification | Habit formation | Push at user's chosen ritual time |
| Weekly Soul Report | Curiosity + validation | Email/push: "Your weekly awakening report is ready" |
| Level progression | Achievement bias | Visual level up animation + badge |
| Community feed | Social proof | See others' streaks and insights |
| Content drops | Variable reward | New content Tuesday & Friday = reason to open app |
| Streak freeze | Sunk cost | "Use a Streak Shield to protect your 30-day streak" |

---

## 🛠 Tech Stack

```
Frontend:    Flutter (Dart) — iOS + Android + Web
State:       Riverpod + StateNotifier
Navigation:  go_router
Backend:     Firebase (Auth, Firestore, Storage, Functions)
AI:          Gemini 1.5 Flash API
Notifs:      Firebase Cloud Messaging
Analytics:   Firebase Analytics + Mixpanel
Payments:    RevenueCat (handles iOS/Android subscriptions)
Fonts:       Google Fonts (Playfair Display + Inter)
Audio:       audioplayers package
```

---

## 📁 Project Structure

```
lib/
├── main.dart
├── app.dart                    # App root, theme switching
├── firebase_options.dart
│
├── core/
│   ├── theme/
│   │   ├── app_theme.dart      # Light + Dark ThemeData
│   │   ├── app_colors.dart     # Colour constants
│   │   └── app_typography.dart # Text styles
│   ├── router/
│   │   └── app_router.dart     # go_router config
│   └── providers/
│       └── theme_provider.dart # Light/Dark toggle state
│
├── features/
│   ├── onboarding/
│   │   ├── screens/
│   │   │   ├── splash_screen.dart
│   │   │   ├── soul_quiz_screen.dart
│   │   │   ├── profile_reveal_screen.dart
│   │   │   └── paywall_screen.dart
│   │   └── providers/
│   │       └── onboarding_provider.dart
│   │
│   ├── auth/
│   │   ├── screens/
│   │   │   └── auth_screen.dart
│   │   └── providers/
│   │       └── auth_provider.dart
│   │
│   ├── home/
│   │   ├── screens/
│   │   │   └── home_screen.dart
│   │   └── widgets/
│   │       ├── greeting_card.dart
│   │       ├── streak_banner.dart
│   │       ├── daily_practice_card.dart
│   │       └── ai_preview_card.dart
│   │
│   ├── breathwork/
│   │   ├── screens/
│   │   │   └── breathwork_screen.dart
│   │   ├── widgets/
│   │   │   ├── breath_circle.dart
│   │   │   └── phase_label.dart
│   │   └── providers/
│   │       └── breathwork_provider.dart
│   │
│   ├── ai_guide/
│   │   ├── screens/
│   │   │   └── soul_guide_screen.dart
│   │   ├── services/
│   │   │   └── gemini_service.dart
│   │   └── providers/
│   │       └── ai_guide_provider.dart
│   │
│   ├── progress/
│   │   ├── screens/
│   │   │   └── progress_screen.dart
│   │   └── widgets/
│   │       ├── level_card.dart
│   │       ├── streak_calendar.dart
│   │       └── xp_bar.dart
│   │
│   └── settings/
│       ├── screens/
│       │   └── settings_screen.dart
│       └── widgets/
│           └── theme_toggle.dart
│
└── shared/
    ├── widgets/
    │   ├── ha_button.dart        # Primary button component
    │   ├── ha_card.dart          # Standard card component
    │   └── theme_toggle_fab.dart # Floating dark/light toggle
    └── models/
        ├── user_model.dart
        ├── session_model.dart
        └── soul_profile_model.dart
```

---

## 🚀 Launch Strategy

1. **Soft launch** — share with 50 wellness practitioners in Brisbane
2. **Instagram/TikTok** — breathwork demo videos (hook: "30 breaths, 30 seconds")
3. **Partnership** — offer free B2B accounts to 5 local yoga studios
4. **SEO/ASO** — keywords: breathwork app, Wim Hof app, spiritual wellness, morning ritual
5. **Email funnel** — Soul Profile quiz on web → email → app download

---

*Built by Giustino — Brisbane, Australia 🌅*
