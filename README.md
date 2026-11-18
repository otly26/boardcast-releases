# BOARDCAST — Releases

Public downloads ng **BOARDCAST**. Dito lang ang installer at release notes —
**private ang source code** (`otly26/boardcast`, hindi pampubliko).

## ⬇️ Download

**[I-download ang pinakabagong installer →](https://github.com/otly26/boardcast-releases/releases/latest)**

Ang installer ay isang `.exe` na file sa ilalim ng **Assets** ng bawat release.

| Bersyon | File | Petsa |
|---|---|---|
| **2.4.6** | **`BOARDCAST_Setup_2.4.6.exe`** (247.6 MB) | **2026-11-16** |
| 2.4.5 | `BOARDCAST_Setup_2.4.5.exe` (247.6 MB) | 2026-11-12 |
| 2.4.4 | `BOARDCAST_Setup_2.4.4.exe` (247.5 MB) | 2026-11-10 |
| 2.4.3 | `BOARDCAST_Setup_2.4.3.exe` (247.5 MB) | 2026-11-10 |
| 2.4.2 | `BOARDCAST_Setup_2.4.2.exe` (247.5 MB) | 2026-11-08 |
| 2.4.1 | `BOARDCAST_Setup_2.4.1.exe` (247.5 MB) | 2026-11-07 |
| 2.4 | `BOARDCAST_Setup_2.4.exe` (~248 MB) | 2026-11-05 |

## 📱 About BOARDCAST

**BOARDCAST** is a Windows desktop application that combines a live soundboard,
a background music player, local and streamed music playback, internet radio,
and live broadcasting to Icecast and Shoutcast servers — all in one window. It
is designed for blind and screen reader users: every action is spoken aloud, and
every command can be reached from the keyboard. There is no menu bar; the whole
program lives in nine tabs across the top of the window.

### The nine tabs

| Tab | What it is for |
|---|---|
| **Boardcast** | The soundboard. A letter or digit plays a sound effect; Shift plus the same key plays background music. |
| **Playlist** | A gapless playlist of music files from the computer, with crossfade, shuffle, repeat and the Up Next queue. |
| **Broadcast** | Icecast and Shoutcast stations, stream settings, the microphone and line inputs, and recording of the show. |
| **Downloader** | Searches for and saves audio into the playlist, sound effects or background music folder. |
| **Settings** | General, Audio, Audio Devices, Equalizer, Broadcast Defaults, Accessibility and About. |
| **Events** | A timestamped log of everything the app has done during the current session. |
| **Radio** | Internet radio: play a stream address, save and rename stations, and search Philippine stations. |
| **Library** | YouTube playlists streamed without downloading, offline libraries built from a folder of songs, and the tracks of the open playlist. |
| **Help** | The complete user manual, opened with F1 from anywhere. |

### Soundboard and background music

- **Thirty-six sound effects** (L1 to L36) and **thirty-six background music
  tracks** (b1 to b36), each assigned to a key that follows the physical keyboard
  layout. A file becomes a key through its name: `l5_cheer.mp3` becomes L5,
  `b3.mp3` becomes b3.
- Sound effects never stack: pressing the same key again restarts the sound
  instead of playing a second copy, and holding a key down does not repeat it.
  **Control** stops every sound effect from any tab.
- **Space** pauses or resumes the background music, and **F9** turns looping on or
  off.
- The sound and background music folders are monitored while the app runs, so a
  file copied in becomes available immediately without a restart.
- The name of a sound is spoken when it plays, the last sound is shown on the tab,
  and every trigger is written to the Events log.

### Music playback

- **Playlist:** plays audio files from disk without gaps between tracks. Files can
  be added individually or by folder, and everything in the playlist folder is
  loaded automatically at startup.
- **Sixteen-second crossfade:** the outgoing track plays alone at full volume for
  the first eight seconds, and the incoming track then begins at its own 0:00
  during the remaining eight seconds — so the transition is smooth and no part of
  a song's intro is lost.
- **Shuffle**, **Repeat** (off, one, all), **Stop After This** and **Repeat This**
  are available for both the Playlist and the Library.
- **One Up Next queue for the whole application.** Entries can be queued from
  either the Playlist or the Library, reordered, played immediately, or removed.
- **Library:** YouTube playlists are streamed rather than downloaded, so they start
  playing without using disk space. Playlists made entirely of official art tracks
  are listed first, since those contain the album audio with no intros, outros or
  talking. Playlists can be searched, pasted as a link, saved for later, or
  reopened from a list that shows their track counts. A playlist is loaded up to
  five hundred tracks.
- **Offline libraries** turn any folder of songs on the computer into a playlist
  without copying or moving the files.
- **Copy Playlist URL** places the link of the open YouTube playlist on the
  clipboard.
- **Internet radio:** any stream address can be played, saved with a name, renamed
  or deleted. A station search covers Philippine stations by name, city or genre.

### Broadcasting

- Sends the program mix — playlist, Library, radio, background music and sound
  effects — to **one or more Icecast or Shoutcast servers at the same time**, with
  the microphone and up to three line inputs mixed in live.
- **Per-station settings** include host, port, mount point, user name, password,
  stream title, genre and protocol. Several stations can be ticked and fed
  simultaneously.
- **Stream settings:** sample rate of 22050, 44100 or 48000 Hz and a bitrate from
  64 to 320 kbps. **Auto Reconnect** restores a dropped connection by itself and
  continues the same recording.
- The status box shows **OFFLINE** or **LIVE**, and on Icecast servers that publish
  a status page it also shows the listener count, refreshed every fifteen seconds.
- **Microphone:** F8 mutes or unmutes it, and Shift+F8 records three seconds and
  plays them back so the level can be checked. While the microphone is live, the
  music automatically drops to twenty percent and returns when the microphone is
  muted.
- **A three-tone test signal** can be sent to the stream with Shift+F9.
- **Recording:** F7 records exactly what goes on air as a single MP3 file at
  128 kbps, named with the date, the time, the DJ name and the station title.
  Auto-record starts a recording whenever the broadcast goes live, and a reconnect
  continues the same file. Shift+F7 speaks the recording status and running time.

### Downloading

- A typed search returns official art tracks only — the clean album audio
  published by the labels — so a download never carries an intro, an outro or
  talking at the end.
- A video or playlist address can also be pasted directly.
- Files can be saved into the **playlist**, **sound effects** or **background
  music** folder, and the running app picks them up without a restart.
- **Formats:** MP3, OGG, FLAC, WAV, M4A and OPUS. Compressed formats are saved at
  128 kbps, 44100 Hz; FLAC and WAV keep their original quality. A running download
  can be cancelled.

### Audio control

- **Independent volume faders** for sound effects, background music, playlist and
  Library, radio, streaming output and monitor output. Changing one never moves
  another.
- **Streaming Output Volume** controls what listeners hear and never changes what
  the local speakers play. A separate **Monitor Output** device lets the operator
  listen at their own level while the main output keeps the full stream level.
- **Twelve-band equalizer** from 31 Hz to 20 kHz, adjustable from −10 dB to +10 dB
  per band, with fourteen presets and a Flat reset. It shapes the program mix on
  the speakers and on the stream at the same time; the microphone and line inputs
  are not equalized. With the equalizer switched off, or every band at zero, the
  audio passes through untouched.
- Devices are remembered by name, so saved choices survive a restart even when
  Windows renumbers them.

### Accessibility

- Every action, volume change, tab change and sound name is announced, and all
  announcements can be switched off individually in Settings.
- **F1** opens the Help tab from anywhere; the manual and the changelog are
  read-only texts that a screen reader can move through line by line.
- Focus is announced on every control, and lists keep the arrow keys for
  navigation so a shortcut never interferes with moving through them.
- The status bar shows the version and the sound effect and background music
  volumes; the Events log keeps the full history.

### Updates

The application checks for a newer version at startup and every fifteen minutes,
and can also be checked on demand with F12 or from Settings → About. When a newer
version exists, a message shows its version, size and changes, and asks before
anything is downloaded. The installer is then downloaded, verified and started.
The automatic check never installs anything by itself. A full changelog is
available in a read-only window designed for screen readers.

### Files and folders

Everything the application owns lives in its program folder: `sounds`, `bgm`,
`playlist`, `library`, `recordings`, and a `config` folder that holds all
settings, broadcast stations, saved radio stations and Library state.

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

### 2.4.6 — 2026-11-16

- **Crossfade na may hold:** sa 16-s na fade, ang **unang 8 segundo ay lumang
  kanta lang sa buong lakas**, at doon lang nagsisimula ang bago — sa 0:00 pa
  rin ito, kaya hindi nauubos ang intro bago ito marinig. Ang natitirang 8
  segundo ang tunay na crossfade. Parehong sa manual na pagpalit at sa
  natural na transition, sa Playlist at sa Library.
- **Hindi na nagla-lag ang tugtog habang may download:** dating bumabalik sa
  file ang audio callback kada block, at habang abala ang disk ay umaabot ng
  14-25 ms ang basa samantalang 23 ms lang ang isang buong block — kaya may
  butas sa tunog. Ngayon, isang malaking basahan (16,384 frames, ~0.37 s)
  kada 16 block, kaya bumaba sa 2.38 ms ang pinakamahabang basa at **0 na ang
  underflow** sa pagsukat.
- **Limitado sa 2 thread ang ffmpeg** kapag nagko-convert ng na-download na
  file, para may natitirang core sa audio.
- **1 ms GIL switch interval:** mas mabilis nakukuha ng audio callback ang
  GIL kapag abala ang download thread, sa halip na maghintay ng 5 ms.
- **Mas kaunting trabaho sa UI thread:** throttled ang progress updates,
  sinusuri kung pansamantalang file ang isang event, mas mababang priority
  ang download thread, isang fragment download kada pagkakataon, at may
  debounce ang BGM folder rescan.

`BOARDCAST_Setup_2.4.6.exe` — 247.6 MB (259,641,358 bytes), SHA-256
`e2e4aaa75df3907daa2151c39d2162572adb24556aca3ac9a42ffa7ac85a7d23`.

### 2.4.5 — 2026-11-12

- **Crossfade kapag manual na nagpalit ng kanta:** ang pagpili ng bagong
  kanta sa Playlist o Library ay may crossfade na — dati ay biglang putol ang
  lumang kanta. Eksaktong 16 segundo, kapareho ng natural na transition,
  kahit malapit nang matapos ang lumang kanta (hindi na ito pinuputol nang
  maaga para lang matapos ang fade).
- **Equal-power curve:** cos/sin na ang fade ngayon, kaya wala nang -3 dB na
  paghina sa gitna. Dati (linear) ay lumulubog ang kabuuang tunog bago
  lumakas muli; ngayon flat ang lakas mula simula hanggang dulo.
- **Walang click:** kapag paulit-ulit na pumili habang may fade pang
  tumatakbo, dinadaanan muna sa 0.35 s na collapse na panatilihin ang level,
  kaya walang biglang talon sa gain.
- **Hindi kinokonsumo ang Up Next:** kapag manual ang pagpalit, hindi ito
  itinuturing na queue entry — hindi maubos ang naka-queue at hindi
  nag-trigger ng stop-after.
- **Screen reader:** hindi na sinasabi ang "Crossfading to…" kapag manual
  kang nagpalit ng kanta — normal na "Playing: kanta" na lang, at isang
  announcement lang ang naririnig pagkatapos ng fade.

`BOARDCAST_Setup_2.4.5.exe` — 247.6 MB (259,645,396 bytes), SHA-256
`b388544918c843cd757f1fcce1ca56f9290848a5ed7a6b47936d6b0c9e5b927c`.

### 2.4.4 — 2026-11-10

- **Automatic update check:** bawat pagbukas ng app ay may check agad, at may
  panibagong check kada 15 minuto habang bukas ito — hindi na kailangang
  maghintay ng 24 oras o pindutin ang Check for updates. Kapag pinili mong
  **No** sa isang bersyon, hindi na ito mag-prompt muli para doon sa parehong
  session; maagang-aalok lang ulit kapag may mas bagong release o bagong
  bukas ng app.
- **Isang prompt lang:** habang nakabukas ang update window, hindi na
  nagbubukas ng panibagong prompt ang timer, kaya hindi nagkakapatong ang mga
  dialog. Sinusundan na rin ng **Automatic update check** checkbox sa
  Settings -> About ang bagong timer.
- **Help:** na-update ang nakasulat sa Help tungkol sa update check.

`BOARDCAST_Setup_2.4.4.exe` — 247.5 MB (259,554,518 bytes), SHA-256
`6d45e70d94b385d10e87803d3eee23498f2102554678744e333f71add0a5b2e4`.

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
