# CLAUDE.md — 10mins.co Marketing

10mins.co (Ironbay Innovations Pvt Ltd): a small business gets its own branded app (web + native + admin) from its phone, using ready-made vertical apps (cab, gym, grocery, e-store, wedding...). This repo holds AI-generated ad material, one folder per vertical.
Language with the team: short Hinglish. Ad dialogues: Hindi.

## 1. Golden rules (har ad pe lagu)
1. **Only market the business.** Na usse zyada, na kam. Apni taraf se details assume mat karo (accent, backstory, extra props). Creativity sirf wahan jahan zarurat ho.
2. **Template ad.** Ek ad = har business ke liye reusable. Sirf `business insert` (screen recording) + end card text badalta hai.
3. **No names in dialogue.** Character labels (Riya, Ramesh) sirf prompts ke liye. Sambodhan: "मैम", "भैया", "सर".
4. **No promises/claims** jo har business pe sach na ho (e.g. "10 मिनट में हाज़िर" hata diya).
5. **No logos, no brand names, no text** in AI images (car badges bhi nahi). Number plates blurred.
6. **Green screen rule:** phone screen pure flat #00FF00 sirf first-person POV shot me. Jis shot me character ka chehra dikhe, phone screen uski taraf ho, camera ki taraf nahi.
7. **Physical logic check:** har shot me dekho koi cheez ulti/illogical to nahi (phone ulta, chhata kiske paas hai, etc.).
8. **Realistic demographics:** characters us business ke asli customer/owner jaise (e.g. cab driver = 45-50, patla, middle-aged).

## 2. Generic pipeline (naya vertical banane ka tareeka)
```
marketing/<vertical>_ad/
├── PLAN.md            # characters, scenes+dialogues, all prompts, steps, checklist
├── images/            # AI images, named by code (G1.png, D1.png, C1.png ...)
├── clips/             # Grok clips (s01.mp4 ...)
├── audio/             # recorded Hindi dialogues
├── <x>_inserts/       # per-business app screen recording (the swap part)
└── final/             # exported ads, one per business
```
Steps:
1. **PLAN.md likho:** characters (short, factual) -> scene table (time, action, image codes, dialogue) -> MASTER image prompt -> shot codes -> Grok prompts -> audio -> insert -> edit -> checklist.
2. **Images (ChatGPT/Gemini):** MASTER prompt paste -> pehle reference shots (har character/prop ka 1) -> baaki shots reference attach karke ("Match the attached reference exactly"). Agar model ek image me multiple panels de, crop karke alag save karo.
3. **QA har image:** same face/kapde/prop, green screen rule, no logo/text, 9:16, physical logic. Galat image kabhi aage mat bhejo.
4. **Video (Grok, image-to-video):** ek image + ek short motion prompt per clip; end me common line (photorealistic, 9:16, keep faces/props same, no text/logos, green stays green). Lip-sync pe depend mat karo.
5. **Audio:** dialogues alag record (real voices).
6. **Business insert:** business ke phone pe screen recording: home screen -> app icon tap -> app full screen khulta hai (6-8 sec, vertical).
7. **CapCut:** clips + audio -> POV phone pe chroma key insert -> tap pe zoom -> full 9:16 green frame (P2) pe insert full screen (no tracking) -> end card (business naam, city, 10mins.co) -> export `final/<vertical>_ad_<business>.mp4`.
8. **Naye business ke liye:** sirf insert + end card text badlo, export.

Image code convention: first letter = character/prop (G girl, D driver, C car, B bus stop, E environment, P plain/POV), number = shot. `1` = reference shot.

## 3. Verticals

### 3.1 Cab (`cab_ad/`) — status: 14 images done, clips pending
- **Goal:** cab driver ka apna app promote karna; passenger seedha driver ke app se book kare.
- **Setting:** North Indian Tier-2 town, monsoon, bus stop.
- **Characters**
  - Passenger (label Riya): 23-24, slim, sundar; blue-print kurta, blue dupatta, transparent chhata.
  - Driver (label Ramesh): 45-50, patla, middle-aged; light-blue shirt; **apna chhata nahi**.
  - Car: white sedan, no logo.
- **Story (~30 sec, 8 scenes)**
  1. Baarish, ladki bus stop pe wait.
  2. Ghadi dekhti hai: "उफ़्फ़… आधे घंटे से खड़ी हूँ…"
  3. Car aati hai; driver bina chhate utarta hai: "मैम, भीग जाएंगी… आइए…"
  4. Driver uska chhata leke use car me bithata hai: "थैंक यू भैया…"
  5. Driver: "इतना इंतज़ार करने की ज़रूरत ही नहीं थी मैम। मेरा अपना ऐप है…"
  6. Ladki bag se phone nikalti hai -> POV green screen tap: "अरे वाह, आपका अपना ऐप?"
  7. Full-screen takeover: driver ka app. "हाँ जी! अगली बार सीधे इसी से बुक कीजिए।"
  8. End card: driver naam + city + 10mins.co.
- **Lessons:** face + green screen same shot = phone ulta lagta hai (split into G6 bag + G7 POV); car pe Toyota logo aaya tha (hatana); chhata logic fix.
- **Next:** Grok clips (s01, s02, s03, s03b, s04–s07), P2 green frame, audio, pehla driver insert, CapCut edit.

### 3.x Next vertical (template)
Copy `cab_ad/PLAN.md` structure -> characters/setting/story badlo -> same rules + pipeline.

## 4. Other marketing refs
- Ad agencies research (paid option, Hindi-belt, rates + contacts): `../drafts/marketing_ad_agencies.md`.
