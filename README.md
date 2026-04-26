# Instalator AI Pirate

Skrypt instalacyjny dla aplikacji AI Pirate (Ubuntu).

## Uruchomienie

```bash
curl -fsSL https://raw.githubusercontent.com/NoSkillSense/instal_ai_pirat/main/install.sh | bash
```

Lub:

```bash
git clone https://github.com/NoSkillSense/instal_ai_pirat.git
cd instal_ai_pirat
./install.sh
```

## Wymagania

- Ubuntu (lub inny Debian-based)
- Dostęp do repo [ai_pirat](https://github.com/NoSkillSense/ai_pirat) (Deploy key dodany podczas instalacji)

## Przeglądarka (Chromium + WebRTC / mikrofon)

Instalator dobiera **Chromium** (`apt`), żeby kiosk i nagrywanie głosu działały przewidywalnie.

1. **Jednorazowo w Chromium:** w pasku adresu otwórz  
   `chrome://flags/#enable-webrtc-allow-input-volume-adjustment`  
   Ustaw **Allow WebRTC to adjust the input volume.** na **Enabled**, potem **Relaunch**.
2. Launcher `start-app-fullscreen.sh` dodatkowo przekazuje  
   `--enable-features=WebRtcAllowInputVolumeAdjustment` przy starcie Chromium / Chrome (żeby ta opcja była aktywna bez ręcznej konfiguracji, gdy silnik to honoruje).

Jeśli mikrofon nadal zachowuje się dziwnie, sprawdź tę samą flagę (np. wyłączenie auto-regulacji głośności wejścia).
