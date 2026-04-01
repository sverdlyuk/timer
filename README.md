# ⏱️ Timer for Lilka

A simple and convenient timer for the **Lilka (ESP32-S3)** handheld console, featuring button controls and sound notifications.

## ✨ Features

- Set time (hours, minutes, seconds)
- Start / pause timer
- Real-time countdown
- Sound notification when finished
- Intuitive button controls
- Minimalistic interface

## 🎮 Controls

| Button | Action |
|--------|--------|
| ⬅️ / ➡️ | Switch between fields (HH / MM / SS) |
| ⬆️ / ⬇️ | Change value |
| 🅰️ | Start / Pause / Reset |
| 🅱️ | Exit program |

## 🖥️ Interface

- Time format: `HH:MM:SS`
- Active field is highlighted
- Dynamic hints for **A** button:
  - `Start` — begin countdown
  - `Stop` — pause timer
  - `Reset` — after completion

## 🔊 Sound

A melody is played through the buzzer when the timer finishes.

## ⚙️ How it works

- Time is set using three fields: hours, minutes, seconds
- On start, total time is converted into seconds
- The timer subtracts `delta` (time between frames)
- When it reaches zero:
  - the timer stops
  - a melody starts playing
  - state changes to `finished`

## 📦 Requirements

- Lilka with firmware supporting:
  - `display`
  - `controller`
  - `buzzer`
  - `notes`
  - `util`
