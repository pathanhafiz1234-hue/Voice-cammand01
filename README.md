# Voice Commander (Android)

Background mein chalne wala voice-command app. Wake word bolo, phir "open" ya "call" command do.

## Kaise use karo

1. **Android Studio** mein is folder ko "Open" karke import karo (File → Open → is folder ko select karo).
   Android Studio khud Gradle wrapper download kar lega — internet chahiye pehli baar sync ke liye.
2. Ek real Android phone connect karo (USB debugging ON), ya emulator use karo.
3. Run karo (▶ button). App khulega.
4. **"Start Listening"** button dabao — ye permissions maangega (Microphone, Call, Contacts, Notifications). Sab **Allow** karo.
5. Ab app background mein permanently sunta rahega (ek notification dikhegi — Android ka rule hai).

## Voice Commands

| Bolo | Kya hoga |
|---|---|
| "command on" | Software activate ho jaayega — ab ye open/call commands sunega |
| "command off" | Software suspend ho jaayega — open/call commands ignore karega, but chalta rahega |
| "open camera" / "open whatsapp" | Us naam ka app dhoondh kar open karega |
| "call ramesh" | Contacts mein "ramesh" dhoondh kar call lagayega |

Koi bhi aur command (jaise "kya haal hai") ignore ho jaayega — sirf "open" aur "call" commands ka jawab milta hai, jaisa aapne bola tha.

**Important:** "command on/off" hamesha kaam karega chahe active ho ya na ho. Baaki (open/call) sirf tabhi kaam karenge jab "command on" bola ho.

## Band/Delete kaise karo

- **Sirf sunna band karna ho:** app kholo, "Stop Listening" button dabao. Ya bologe: koi voice-off command nahi hai for full stop — button use karo.
- **Poora hata na ho:** Settings → Apps → Voice Commander → **Uninstall**. Ye service ko turant band kar dega, kuch bhi background mein nahi rahega.

## Limitations (jaanana zaroori)

- `SpeechRecognizer` internet/Google service pe depend karta hai — offline recognition sab phones pe kaam nahi karega.
- Continuous listening battery zyada use karti hai.
- Android 11+ pe background se app launch karne par kabhi-kabhi extra restrictions aa sakti hain (manufacturer-specific).
- Ye ek starting point/skeleton hai — production-ready polish (jaise better fuzzy-matching, multi-language support) aapko add karna padega.
