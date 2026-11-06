# BOARDCAST — Releases

Public downloads ng **BOARDCAST**. Dito lang ang installer at release notes —
**private ang source code** (`otly26/boardcast`, hindi pampubliko).

## ⬇️ Download

**[I-download ang pinakabagong installer →](https://github.com/otly26/boardcast-releases/releases/latest)**

Ang installer ay isang `.exe` na file sa ilalim ng **Assets** ng bawat release.

| Bersyon | File | Petsa |
|---|---|---|
| 2.4 | `BOARDCAST_Setup_2.4.exe` (~248 MB) | 2026-11-05 |

## 💻 Kailangan

- Windows 10 o Windows 11, 64-bit
- ~1 GB na espasyo sa disk (kasama ang bundled na ffmpeg/deno at Python runtime)
- Wala nang hiwalay na installation ng Python — sarili nang runtime ng installer

## 🔧 Pag-install

1. I-download ang `BOARDCAST_Setup_x.y.exe`.
2. I-double-click at sundan ang setup wizard.
3. Kung magpakita ang **Windows SmartScreen** ng "Windows protected your PC",
   pindutin ang **More info → Run anyway**. Hindi pa naka-code-sign ang installer,
   kaya normal lang ito. I-verify pa rin ang SHA-256 (nasa bawat release notes)
   kung galing sa ibang pinagmulan ang file.
4. Buksan ang **BOARDCAST** mula sa Start Menu o desktop shortcut.

## ✅ Bago mag-install

Ihihiwalay ng installer ang mga user file mo — hindi nito binubura ang `bgm/`,
`playlist/`, `library/`, `recordings/`, at ang mga config (`bc_stations.json`,
`.boardcast_config.json`). Gayunman, mag-backup pa rin bago mag-upgrade.

## 📝 Mga bersyon

### 2.4 — 2026-11-05 (muling na-build 2026-11-06)

- **Auto-updater:** kusang nagche-check ng bagong release pagbukas ng app
  (minsan kada 24 oras). May **Check for updates** din sa Settings → About at
  **F12** shortcut. Kapag may bagong bersyon, ang app na ang magda-download at
  magpapatakbo ng installer.
- Ayos sa **crossfade**: tamang haba na ang fade kahit mas mahaba ito kaysa sa
  kanta, at hindi na napuputol ang susunod na track.
- Hindi na lumilihis ang timing kapag binago ang haba ng crossfade habang
  tumutugtog; wala nang drift sa resampling.
- Ayos sa frame counting ng stream voice at sa buffering ng Library.

## 🐞 Problema at mungkahi

Magbukas ng **issue** dito para sa bug o request. Para sa mga usaping may
kaugnayan sa source code, sa private repo ilagay (kung may access ka).

---

*Hindi ito ang source repository. Walang source code, build script, o credential
na makikita dito — installer at release notes lang.*
