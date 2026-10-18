# 10mins.co — Cab driver ad (template) — PLAN
Length ~30 sec · 9:16 vertical · Hindi · Tools: ChatGPT/Gemini (images) -> Grok (video) -> CapCut (edit)

## 0. Sabse important idea: TEMPLATE ad
Ad ek baar banega, har driver ke liye reuse hoga.
- Ladki ke phone ki screen hamesha PURE GREEN (#00FF00) rahegi.
- Har naye driver ke liye sirf ek cheez badlegi: `driver_inserts/<driver_name>.mp4`
  = driver ke apne phone ki 6-8 sec screen recording:
  home screen -> uske app icon pe tap -> app full screen khulta hai -> "Book ride" dikhta hai.
- Edit me ye recording 2 jagah lagti hai:
  1. Scene 6 (phone haath me): green screen pe chroma key se.
  2. Scene 7 (FULL SCREEN TAKEOVER): phone zoom hota hai, poora 9:16 frame green ho jaata hai -> wahi recording full screen. Koi tracking/keying ki zarurat nahi — automatically fit.
- Dialogue me driver ka naam/app ka naam nahi bola jaata -> har driver pe chalega. Naam sirf end card text me (edit me badlo).
- RULE: koi bhi character kisi ka naam nahi bolega. "Riya"/"Ramesh" sirf hamare liye label hain (prompt me pehchaan ke liye), screen pe ya dialogue me kabhi nahi. Sambodhan sirf "मैम" / "भैया".

## 1. Folder structure
```
cab_ad/
├── PLAN.md            <- ye file (characters, scenes, dialogues, saare prompts, steps)
├── images/            <- 14 AI images (G1.png, D1.png ... naming neeche)
├── clips/             <- Grok clips (s01.mp4 ... s07.mp4)
├── audio/             <- recorded Hindi dialogues (s02_riya.m4a ...)
├── driver_inserts/    <- har driver ki app screen recording (ramesh_gorakhpur.mp4 ...)
└── final/             <- final ads (cab_ad_<driver>.mp4)
```

## 2. Characters
**RIYA (passenger)** — Indian woman, 23-24, slim, fair-wheatish, beautiful, expressive big eyes, long black hair in a loose side braid, light kajal, small bindi, small gold jhumkas. Pastel-pink cotton kurta, white churidar, white dupatta, tan sling bag, transparent umbrella, phone in hand. 

**RAMESH BHAIYA (cab driver)** — Indian man, 45-50, thin/lean build, salt-and-pepper short hair, neat moustache, kind eyes. Light-blue half-sleeve shirt (slightly faded), dark grey trousers, sandals, steel watch. Polite. Uske paas apna chhata NAHI hai.

**CAR** — White compact sedan (common Indian taxi), no logos/badges, number plate blurred, raindrops on body, headlights on.

**PLACE** — North Indian Tier-2 town (Gorakhpur/Lucknow type), monsoon, grey clouds, drizzle, wet road, puddles, e-rickshaws blurred. Old bus shelter: tin roof, faded green paint, steel bench, blank poster board.

## 3. Scenes + dialogues (~30 sec)
| # | Time | Kya hota hai | Images | Dialogue |
|---|---|---|---|---|
| S1 | 0–3s | Baarish wali sadak, bus stop pe Riya akeli | E1, B1 | (rain + traffic sound) |
| S2 | 3–7s | Riya ghadi dekhti hai, sadak ki taraf dekhti hai, pareshaan | G2, G3 | **Riya** (dheere se): "उफ़्फ़… आधे घंटे से खड़ी हूँ, कोई गाड़ी ही नहीं मिल रही।" |
| S3 | 7–11s | Safed car puddle splash ke saath aake rukti hai, Ramesh bhaiya bina chhate ke utarte hain (halka bheegte hue), Riya ki taraf aate hain | C2, D2 | **Ramesh**: "मैम, भीग जाएंगी… आइए, जहाँ जाना है छोड़ देता हूँ।" |
| S4 | 11–15s | Ramesh, Riya se uska transparent chhata le lete hain, uske upar pakadte hain, peeche ka darwaza kholke use bithate hain | D3, G4 | **Riya**: "थैंक यू भैया… मैं तो कब से इंतज़ार कर रही थी।" |
| S5 | 15–20s | Car ke andar; Ramesh peeche mudke muskurate hain | D4, G5 | **Ramesh**: "इतना इंतज़ार करने की ज़रूरत ही नहीं थी मैम। मेरा अपना ऐप है — अभी आपके फ़ोन पे भेजता हूँ।" (phone "ting") |
| S6 | 20–23s | Riya muskurate hue purse se phone nikalti hai (screen nahi dikhti) -> phir uski aankh se POV: haath me phone, GREEN screen, ungli se tap | G6, G7 | (tap sound) **Riya**: "अरे वाह, आपका अपना ऐप?" |
| S7 | 23–27s | **FULL SCREEN TAKEOVER**: phone zoom -> poora frame = driver insert recording (app khulta hai) | P2 (pure green frame) | **Ramesh** (VO): "हाँ जी! अगली बार सीधे इसी से बुक कीजिए।" |
| S8 | 27–30s | End card: driver ka naam + city + "Book on my app" + 10mins.co logo | CapCut | **VO**: "अपना बिज़नेस, अपना ऐप — 10mins.co" |

Bolne ka tone: Ramesh = polite. Riya = pareshaan -> raahat -> khush.

## 4. STEP 1 — Images (ChatGPT / Gemini)
Pehle MASTER prompt paste karo. Phir ek-ek code: "Generate G1". G1, D1, C1 pehle banao; baaki banate waqt inhe reference image attach karo (chehra same rahega). Har image `images/<CODE>.png` naam se save.

### MASTER PROMPT
```
You are my image generator for a 30-second vertical (9:16) Indian ad. I will ask for images one at a time by code. Keep EVERY image consistent with this bible. Photorealistic, cinematic, natural skin texture, 35mm lens, soft overcast monsoon light, teal-grey grade with warm skin tones. Aspect ratio 9:16. No text, no logos, no watermarks, no brand names anywhere.

PLACE: North Indian Tier-2 town street, late afternoon monsoon, heavy grey clouds, light drizzle, wet road with reflections, puddles, blurred e-rickshaws and scooters, shop shutters, overhead electric wires. Bus shelter: old concrete, tin roof, faded green paint, steel bench, blank weathered poster board, rain dripping from the roof edge.

RIYA (passenger): Indian woman, 23-24, slim, fair-wheatish, beautiful, big expressive eyes, long black hair in a loose side braid, light kajal, small bindi, small gold jhumkas. Pastel-pink cotton kurta, white churidar, white dupatta, tan sling bag, transparent umbrella.

RAMESH (cab driver): Indian man, 45-50, thin lean build, salt-and-pepper short hair, neat moustache, kind eyes. Light-blue faded half-sleeve shirt, dark grey trousers, sandals, steel watch. Polite. He has NO umbrella of his own — never show him with his own umbrella. Uske paas apna chhata NAHI hai.

CAR: white compact 4-door sedan, common Indian taxi, no logos or badges, number plate blurred, raindrops, headlights on.

PHONE RULE (very important): whenever Riya's phone screen is visible, the ENTIRE screen must be flat, evenly lit, pure chroma green #00FF00, no reflections, no glare, no icons, no text, edges clearly visible, screen facing the camera as straight as possible. A green screen may ONLY appear in first-person POV shots (G7). In shots where we see Riya's face, her phone screen must face HER, not the camera.

Confirm, then wait for my first code.
```

### Shot codes (14 images)
| Code | Prompt (paste: "Generate <code> — ...") |
|---|---|
| G1 | Riya face reference: front medium close-up at the bus shelter, soft smile, looking at camera. |
| G2 | Riya full body under the bus shelter, checking her wristwatch, impatient, rain behind her. |
| G3 | Riya side profile looking down the road for a vehicle, umbrella open, drizzle, worried. |
| G4 | Riya getting into the back seat of the white sedan while Ramesh holds HER transparent umbrella over her (he took it from her), grateful smile. Rain falls on Ramesh's shoulders. |
| G5 | Riya sitting in the back seat, relieved, wiping raindrops off her arm, rain on the window. |
| G6 | Riya in the back seat, smiling, taking her phone out of her brown sling bag after hearing a notification. Phone screen faces her / not visible to camera. Rain on the window. |
| G7 | First-person POV from Riya's eyes in the back seat of the car: both her hands hold a black smartphone upright, screen pure flat green #00FF00 facing the viewer, her right index finger about to tap the screen, rain-streaked car window and beige seat softly blurred behind. Only her hands and blue-print kurta sleeves visible, no face. Phone held steady and straight. (Style reference: images/G7_style_ref.png) |
| D1 | Ramesh face reference: front medium close-up beside his white sedan, gentle smile. |
| D2 | Ramesh stepping out of the driver door with NO umbrella, raindrops on his shirt, looking toward the bus stop. |
| D3 | At the bus stop, Ramesh politely takes Riya's transparent umbrella from her hand with one hand and opens the rear door with the other; his shirt is slightly wet from the rain. Respectful. |
| D4 | Ramesh in the driver seat turned back toward the rear seat, smiling, holding up his own phone (screen turned away from camera). His shirt is slightly wet; Riya's folded transparent umbrella lies on the floor near the back seat. No other umbrella. |
| C1 | The white sedan, 3/4 front view parked on the wet road, headlights on, no people. |
| C2 | The white sedan arriving at the bus stop, low angle, water splashing from a puddle, slight motion blur. |
| E1 | Establishing wide shot: rainy small-town street with the bus shelter, Riya small in frame waiting alone. |

P2 = khud banao: 1080x1920 pure #00FF00 image (CapCut me solid color). AI ki zarurat nahi.

## 5. STEP 2 — Video clips (Grok, image-to-video)
Har shot: image upload + prompt. Har prompt ke end me ye line jodo:
`Photorealistic, 9:16, monsoon rain, natural subtle motion, keep faces, clothes and car exactly as in the image, no text, no logos. If a phone screen is visible keep it pure flat green #00FF00.`

| Clip | Image | Prompt |
|---|---|---|
| s01 | E1 | Slow cinematic push-in toward the bus shelter in the rain, light traffic passing blurred. |
| s02 | G2 | The woman checks her wristwatch, sighs, looks down the road impatiently, rain dripping from the roof. |
| s03 | C2 | The white sedan drives in and stops at the bus shelter, water splashing, wipers moving. |
| s03b | D2 | The car has stopped at the bus shelter; the thin middle-aged driver steps out without any umbrella, rain falling on him, and walks toward the woman. |
| s04 | D3 | The driver politely takes the woman's transparent umbrella from her, holds it over her head and helps her into the back seat of the car. |
| s05 | D4 | Inside the car, the driver turns back, smiles and talks warmly, then taps his own phone. |
| s06 | G6 | The woman hears a notification, smiles and takes her phone out of her bag, looking at it happily. |
| s07 | G7 | First-person view: her finger taps the centre of the green phone screen; the phone stays steady, rain on the window behind. |
(Ek clip 2-3 baar generate karo, best rakho. Lip-sync pe depend mat karo.)

## 6. STEP 3 — Audio
Har dialogue phone pe record karo (shant kamre me), `audio/s02_riya.m4a`, `audio/s03_ramesh.m4a` ... Male aur female voice alag log. Background: rain sound (CapCut library).

## 7. STEP 4 — Driver insert (har driver ke liye)
Driver ke phone pe (ya demo phone pe):
1. Home screen pe driver ka app icon dikhe (10mins app "Add to home screen").
2. Screen recording start -> icon pe tap -> app khule -> booking screen 3 sec.
3. Save: `driver_inserts/<naam>_<city>.mp4` (vertical, 6-8 sec).

## 8. STEP 5 — CapCut edit
1. s01–s07 clips order me rakho, audio sync karo.
2. s07 pe driver insert overlay -> Chroma Key (green) -> phone screen me fit (scale/position).
3. Tap ke frame pe "zoom in" transition -> P2 green frame -> uske upar driver insert FULL 9:16 (S7). Yahi "pop-up full screen" moment.
4. End card: driver photo/naam, city, "Mere app se book karein", 10mins.co logo.
5. Export `final/cab_ad_<driver>.mp4`. Agle driver ke liye: sirf insert + end card naam badlo -> export.

## Checklist
- [ ] 14 images (images/)
- [ ] P2 green frame
- [ ] 8 clips (clips/: s01, s02, s03, s03b, s04–s07)
- [ ] Dialogues recorded (audio/)
- [ ] First driver insert (driver_inserts/)
- [ ] Edit + export (final/)
