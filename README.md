# BOARDCAST — Releases

Public downloads ng **BOARDCAST**. Dito lang ang installer at release notes —
**private ang source code** (`otly26/boardcast`, hindi pampubliko).

## ⬇️ Download

**[I-download ang pinakabagong installer →](https://github.com/otly26/boardcast-releases/releases/latest)**

Ang installer ay isang `.exe` na file sa ilalim ng **Assets** ng bawat release.

| Bersyon | File | Petsa |
|---|---|---|
| **2.4.3** | **`BOARDCAST_Setup_2.4.3.exe`** | **2026-11-10** |
| 2.4.2 | `BOARDCAST_Setup_2.4.2.exe` (247.5 MB) | 2026-11-08 |
| 2.4.1 | `BOARDCAST_Setup_2.4.1.exe` (247.5 MB) | 2026-11-07 |
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
`playlist/`, `library/`, `recordings/`, at ang buong `config/` folder (settings,
stations, radio at Library state). Gayunman, mag-backup pa rin bago mag-upgrade.

## 📝 Mga bersyon

### 2.4.4 — 2026-11-10

- **Automatic update check:** bawat pagbukas ng app ay may check agad, at may
  panibagong check kada 15 minuto habang bukas ito — hindi na kailangang
  maghintay ng 24 oras o pindutin ang Check for updates. Kapag pinili mong
  **No** sa isang bersyon, hindi na ito mag-prompt muli para doon sa parehong
  session; maagang-aalok lang ulit kapag may mas bagong release o bagong
  bukas ng app.

> Hindi pa nailalabas ang `BOARDCAST_Setup_2.4.4.exe` — isasama ito sa
> releases page kapag na-build na ang installer.

### 2.4.3 — 2026-11-10

- **YouTube Music na ang source:** ang Downloader search ay nagtatanong na sa
  YouTube Music at **art tracks lang** (Topic) ang inililista — ang mga kanta
  na sariling upload ng label, nasa "<Artist> - Topic" channel. Iyon ang
  malinis na album audio, kaya walang intro, outro, o boses na nag-uusap sa
  dulo ng na-download na kanta. Wala na sa listahan ang music video at
  ordinaryong upload.
- **Library tab:** ang **Search YouTube Playlist** ay sa YouTube pa rin
  naghahanap at **marami ang resulta** — hanggang ~40 playlist sa isang
  search. Naka-priority lang ngayon ang mga **playlist na puro Topic** (art
  track) na nasa unahan, kaya walang intro, outro o boses na nag-uusap sa
  dulo kapag iyon ang pinili. May nakasulat na track count sa mga iyon,
  pareho ng ilalabas ng Library kapag binuksan. Sumusunod pa rin sa
  listahan ang ibang resulta, kaya may laman ang listahan kahit puro music
  video ang playlist ng isang genre gaya ng OPM. Ganoon pa rin ang Open,
  Add to Library, Back to Search Results at ang pasted na playlist link
  (bukas agad, walang check).
- **Crossfade:** **fixed na 16 segundo** na sa lahat ng pagpalit ng kanta —
  Playlist tab, Library tab at Settings > Audio. Tinanggal na ang chooser
  (Off / 2 / 3 / 4 / 6 / … hanggang 20 segundo) sa tatlong lugar, kaya iisa
  lang ang tunog sa lahat ng transition at walang setting na makakalimutang
  ibalik.
- **Playlist, mabilis nang mag-play:** pagpindot ng Enter, tumutugtog agad
  ang kanta. In-app na ang MP3 decoding (libsndfile) sa halip na bagong
  FFmpeg process bawat kanta, at ang samplerate at haba ng bawat file ay
  sinusukat na sa background pagbukas ng app. Mula ~1.1 s bumaba sa ~10 ms
  ang simula; ang m4a, mp4 at webm ay sa FFmpeg pa rin, pero may naka-cache
  nang file info kaya mabilis din ang ikalawang play.
- **Eksakto ang tunog kapag patay ang equalizer:** ang Playlist at BGM ay
  tumutugtog na nang **eksakto** tulad ng file mismo. Dati, ang mga kantang
  hindi 44.1 kHz (hal. 48 kHz na MP3) ay hinahati-hati sa bawat block bago
  i-resample, kaya nagkakaroon ng phase jitter at parang malabo ang tunog.
  Ngayon tuloy-tuloy ang resampling sa buong kanta — sinusukat na
  kapareho (max difference 0.0000001) ng isang buong resample ng file — at
  mas magaan pa sa CPU (mga 0.7 ms kada block, dati 1.3 ms). Ang equalizer
  lang ang nagbabago ng tunog, at kapag naka-off ito o flat ang lahat ng
  band, dumadaan ang audio nang walang pinagbabago.
- **Malinis ang app folder — `config\`:** nasa isang `config\` folder na
  ang lahat ng `.json` ng app — ang settings (`.boardcast_config.json`),
  broadcast stations (`bc_stations.json`), saved radio
  (`boardcast_radio_stations.json`) at Library state
  (`boardcast_online_playlists.json`) — kaya wala nang nakakalat na file sa
  tabi ng exe. Awtomatikong inililipat doon ang lumang file sa unang
  pagbukas, kaya walang nawawalang station, radio o setting kapag
  nag-update; hindi rin ito binubura ng installer.
- **Help at changelog:** na-update ang mga nakasulat tungkol sa search sa
  Downloader at Library, sa fixed na crossfade, at sa mas mabilis na simula
  ng Playlist.

### 2.4.2 — 2026-11-07

- **Help tab:** may bagong **Help** tab sa dulo ng tab bar — kumpletong user
  manual ng app, naka-topic (11 na seksyon, 38 na paksa): Getting Started,
  Keyboard, Soundboard and BGM, Playlist, Library, Radio, Broadcast, Audio,
  Downloader, Settings, at Other. Sinasaklaw nito ang lahat ng feature, key,
  setting, folder at karaniwang problema, at nakasulat sa English.
- **F1:** binubuksan ang Help mula sa kahit anong tab. Ang kaliwa ay listahan
  ng seksyon at paksa (arrow keys, Right/Left para mag-expand), ang kanan ay
  read-only na teksto na binabasa ng screen reader line by line. Enter sa isang
  paksa ay inililipat ang focus sa teksto; ang pagpili ng seksyon ay
  nagpapakita ng listahan ng mga paksa nito, kaya hindi kailanman blangko ang
  pane.
- **Changelog:** may bagong entry tungkol sa Help tab at F1, at inayos ang
  lumang linyang nagsasabing may sariling queue ang Library (wala na iyon).
- **Bersyon:** 2.4.2 — kung **2.4.1** ang naka-install, awtomatikong io-offer
  ito ng app sa susunod na check (o Settings → About → Check for updates).

### 2.4.1 — 2026-11-07

- **Equalizer:** 12 bands (31 Hz hanggang 20 kHz), 2.5-octave ang lapad,
  **-10 dB hanggang +10 dB** kada band, may 13 preset.
- **Screen reader fix sa equalizer:** ang bawat band slider ay nagbabasa na ng
  totoong dB (-10 … 0 … 10). Dati, porsyento ang iniuulat ng Windows trackbar,
  kaya “50” ang naririnig kapag flat at “100” kapag +10.
- **Line In 1 / 2 / 3:** may hiwalay nang level kada input (0–100 %), tama ang
  pagpili ng device kahit “Default” ang naka-set, at hindi na nawawala ang
  cable loopback kapag may ibang input.
- **Mic:** hindi na pinapatay ang mic kapag naka-auto ang mix papunta sa
  broadcast.
- Kung **2.4** ang naka-install, awtomatikong io-offer ito ng app sa susunod
  na check (o Settings → About → Check for updates).

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
