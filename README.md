# Birthday

Someone's bday celebration website with interactive journey!

## 🎉 User Journey Flow

The website guides users through an interactive birthday celebration experience:

1. **Countdown** (`countdown.html`)
   - Countdown to birthday date (2026-01-02)
   - Glass break effect transition → Dino game

2. **Dino Game** (`dino.html`)
   - Challenge: Score exactly 18 points
   - Rules: Space to jump, avoid cactuses
   - Score == 18 → Plays `bomb.mp4` animation → Special Day page

3. **Special Day** (`specialday.html`)
   - Animated message: "DO YOU KNOW IT'S A SPECIAL DAY TODAY?"
   - Auto-transitions to Birthday page (5 sec)

4. **It's Your Birthday!** (`bday.html`)
   - Full-screen celebration with penguin & decorations
   - Animated pulsing text
   - Auto-transitions to Rain page (6 sec)

5. **Raining Words** (`rain.html`)
   - Realistic water with wave animation
   - Falling animated words
   - Floating words on water
   - Zoom transition → Choice page

6. **Wish Type Selection** (`wishtype.html`)
   - Choose between: Simple or Advance wish

7. **Simple Wish** (`simple.html`)
   - Birthday message card
   - Next button → Enjoy page

8. **Advance Wish** (`advance.html`)
   - "ARE YOU SURE?!" interactive page
   - Yes/No buttons (No button moves away)
   - Yes → Enjoy page

9. **Did You Enjoy?** (`enjoy.html`)
   - Two YEA buttons for feedback
   - Either choice → Thanks page

10. **Thanks** (`thanks.html`)
    - Moon text animation
    - "THANKS" text reveal animation
    - Final celebration message

## 📁 Project Structure

```
birthday-site/
├── *.html (11 interactive pages)
├── assets/ (for video files)
│   └── bomb.mp4 (REQUIRED - plays on dino score 18)
└── README.md
```

## 🎬 Required Video Files

Place these MP4 files in `assets/` folder:

1. **bomb.mp4** - Plays after dino game score reaches 18
   - Duration: ~3-5 seconds recommended
   
2. **scary.mp4** (Optional) - Mentioned in advance path
   - Could be a jumpscare effect
   
3. **final vid.mp4** (Optional) - Final video for advance path
   - Celebratory video

## 🚀 How to Use

1. Open `countdown.html` in a browser to start the journey
2. Follow the interactive flow
3. Add MP4 files to `assets/` folder for complete experience

## 💡 Features

- ✨ Auto-transitioning pages with smooth flows
- 🎮 Interactive Dino game (score = 18 to win)
- 🎨 Beautiful animations and transitions
- 📱 Responsive design
- 🎯 Complete user journey tracking
birthday-site/
│
├── index.html              # Countdown Page
│   └── On countdown 0 → glass break → game.html
│
├── game.html               # Dino Game
│   ├── If score = 18 → bomb video → special-day.html
│   └── If score ≠ 18 → fail message → restart game.html
│
├── special-day.html        # Special Day UI
│   └── Auto → birthday.html
│
├── birthday.html           # It's Your Birthday UI
│   └── Auto → rain.html
│
├── rain.html               # Raining Words
│   └── After animation → wish-type.html
│
├── wish-type.html          # Wishing Options
│   ├── Option 1 → simple-wish.html
│   └── Option 2 → sure.html
│
├── simple-wish.html        # Simple Wishing Page
│   └── Auto → enjoy.html
│
├── sure.html               # Confirmation Page
│   └── Auto → enjoy.html
│
├── jumpscare.html          # Optional jumpscare (triggered by wrong action)
│   └── Auto → enjoy.html
│
├── enjoy.html              # Main Enjoy Page
│   └── Auto → thanks.html
│
└── thanks.html             # Ending Thank You Page
