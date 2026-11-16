# HamStation

Download HamStation-Setup-0.63.2.exe below and run it. It installs over your current HamStation and keeps your logbook and settings.
----------------------------------------------------------------------

HamStation 0.63.5

New:

The SDR scope shows the CW or digital part of the band
- While the CW tab is open, the panadapter shows just the CW part of the band you're on (20 m: 14.000-14.070). While the Digi tab is open, it shows the digital part (20 m: 14.070-14.112, where FT8 and RTTY are).
- It only does this while the radio is tuned inside that part. Tune outside it, or go to another tab, and the scope goes back to your usual span.
- A Segment checkbox on the panadapter bar, next to AGC, turns it off.
- Not used with the FT-710's own scope.

Everything else is the same as 0.63.2.
-----------------------------------------------------------------------------------------

HamStation 0.63.2

New:

Click a received number to log it
- While a contest with a serial number or zone is open, numbers in the decoded RTTY and CW text are clickable (cyan, dotted underline), the same way callsigns are.
- Click one and it goes into the received Nr (or Zone) box of the QSO entry. 599 and 5NN are left alone, and CW cut numbers like 1T go in as 10.

Worked All Europe contests
- WAE CW, SSB and RTTY are now built in, with RST and a serial number. The serial counts up by itself (001, 002, 003...) and the received serial is logged.
- A WAE contest you already set up from the N1MM contest list picks this up by itself.
- QTC traffic is not handled.

Fixes:

RTTY QSOs logged as FT8
- HamStation sends RTTY with the radio in DATA-U, and DATA-U was logged as FT8 with a -10 report. While HamStation's RTTY is in use (the panel is up, or was in the last 30 minutes, or the open contest is an RTTY one) it now logs RTTY with 599.

Everything else is the same as 0.63.1.
------------------------------------------------------

HamStation 0.63.1

New:

RTTY contest macros
- When a contest is open (one that isn't CW-only or phone-only), the RTTY panel now brings up a macro set for that contest by itself. A picker next to Run / S&P switches back to General.
- The set is built from the contest's own exchange, so it sends the right thing for ARRL RTTY Roundup, CQ WW RTTY, CQ WPX RTTY, NAQP RTTY and the rest.
- Each contest has its own Run and S&P sides. Run: F1 CQ, F2 exchange, F3 TU and log. S&P: F1 your call, F2 TU plus your exchange and log.
- Edit them with Edit macros; your changes are kept for that contest only.
- New macro field {EX}: your exchange without the RST, so a macro can send "599 CO CO" the usual RTTY way.

Everything else is the same as 0.63.
-----------------------------------------------------------------------

HamStation 0.63

New:

RTTY, in a new Digi Modes tab
- A new Digi Modes tab holds the newer digital modes under one tab, so the tab bar doesn't keep growing. RTTY is there now; PSK31 and SSTV are coming soon.
- Click a signal on the waterfall to copy it: HamStation snaps onto its two tones. Shift+click puts the centre exactly where you click.
- Standard 45 baud, 170 Hz shift RTTY. Reverse for a station sending upside down, and a Gate setting that keeps noise from printing junk.
- Send from F1-F12 macros or type ahead. It sends as audio in DATA-U, and what you send shows in red in the text. Click a callsign in the text to put it in the QSO entry.
- Tune sends a steady tone for 10 seconds to set power and ALC. Esc stops sending.

Hotkeys and foot pedal PTT (Settings, Hotkeys)
- Pick a key to use as PTT, hold to talk or press to toggle. Space works anywhere in the app, even after clicking a spot or the cluster.
- USB foot pedals work, either set to send a key (F13-F24 are best) or as a game controller button.
- Shortcut keys for band up and down, next mode, new QSO and QRZ lookup, and Alt+1-9 for the tabs. All of them can be changed.
- For safety PTT lets go when the HamStation window loses focus, and the radio unkeys if the key stops reporting in.

Run and S&P macros
- The CW keyer and RTTY macros now come in two sets: Run (calling CQ) and S&P (answering stations). On the POTA set they are Activator and Hunter.
- Switch with the buttons next to the macro set, or Alt+R. Each side has its own F1-F12 you can edit.
- Your existing macros became the Run (Activator) side, so nothing you set up was lost.

Fixes:

CW decoder
- After you retune onto a new signal, the decoder now picks it up right away instead of taking up to half a minute.

CW keyer on the FTDX101
- HamStation lengthens the radio's break-in delay while it sends, so the relay closes once for the over instead of clicking between letters. The FTDX101 only accepts that delay in 10 ms steps and was turning it down; it now gets a value it accepts.
- If a radio still keeps its own delay, a yellow note under the macros says so and what to set it to.


---------------------------------------------------------------------------
HamStation 0.62.5

Fix:

CW keyer relay chatter
- When sending CW in CW mode, the radio's T/R relay chattered on the first letter of every over before settling down.
- With the radio's break-in switched on, the key now brings the transmitter up by itself, the same way a paddle does, and HamStation holds a longer break-in delay for the over so the relay closes once and stays closed. Your break-in delay is restored afterward.
- With break-in off, HamStation switches the radio to transmit over CAT as before, and now waits until the radio says it is transmitting before the first dit.

Everything else is the same as 0.62.
-----------------------------------------------------

HamStation 0.62

New in this version:

CW decoder
- HamStation's own CW decoder copies up to six signals at once from the radio's receive audio, in CW or DATA-U. Turn it on in Settings > CW.
- Each signal gets its own line with its tone and speed. Text shows about a second after it's sent and firms up two seconds behind real time.
- Click a callsign in the text to put it in the QSO entry.

CW waterfall
- The CW tab has its own waterfall, 200 to 2800 Hz, with each decoded signal marked on the scale and your sending tone as a red bracket.
- Click a signal to send on it. In CW mode the click retunes the radio so you land right on the other station.
- Very strong signals no longer leave ghost copies far down the waterfall when the radio's narrow CW filter is on.

CW keyer
- Send CW from F1-F12 macros or by typing. WPM (PageUp / PageDown), Practice on the PC speakers, Tune, and Esc stops sending anywhere.
- Sends in real CW mode by keying the radio's second USB port (DTR or RTS), or as an audio tone in DATA-U. Pick the keying port in Edit macros > Sending in CW mode.
- In CW mode HamStation lengthens the radio's break-in delay for each over and puts it back afterwards, so the relay doesn't chatter.
- The radio's CW pitch is read from the radio (Yaesu).
- Macro help: a button in Edit macros explains every macro field in plain words, shows what each holds right now, and gives ready-made examples. Each macro shows a "Sends now" line.
- POTA macro set: quick park exchanges with your report and state, plus thanks-and-log, hunter report and park to park. Set My state and My park in Edit macros.

Gold stars for confirmed QSOs
- QSOs confirmed on LoTW or QRZ get a gold star next to their green check in the Log tab.
- Enter your LoTW website login in Settings > LoTW (Test login checks it). HamStation checks LoTW every 6 hours by itself; the star-arrow button above the log checks now.
- The first LoTW check reads every confirmation you've ever had and can take 20-30 minutes. After that each check takes seconds.

Radio
- Optional: switch the radio on when HamStation starts and off when it closes (Settings > Radio > Connection).

Fixes
- HamStation could freeze (no waterfall, no decoding) if the logbook got locked while a QRZ lookup was saving. The logbook now uses a safer mode and this can't happen any more.

User manual
- The manual is updated for everything new since 0.58, with new screenshots: CW decoder and keyer, FT8 decoder and audio waterfall, Alerts tab, fldigi link, gold stars and more.
---------------------------------------------------------------------------------------------------------------------------------

HamStation 0.61

New in this version:

Built-in FT8 decoder
- HamStation can decode FT8 itself from the radio's receive audio, with no WSJT-X running. Turn it on in Settings > Digital > FT8 decoder.
- Its decodes feed the FT8 Call Roster, PSK Map and waterfall labels just like WSJT-X's. Answering a station still needs WSJT-X for now.
- The FT8 Call Roster and PSK Map tabs only show while you're on an FT8 frequency (or WSJT-X is connected).

Alerts
- New Alerts tab: add callsigns to watch, see the latest spot of each one, and a history of the alerts you've had. Click a spot to tune to it.
- Star any call in the cluster or POTA spot lists to watch it. Alerts now come from cluster and POTA spots, not just DXpeditions.
- Type a park reference (like US-9626) in the comment and the QSO is logged as a POTA contact.

Panadapter
- The FT8 audio waterfall keeps its own gain, so switching between it and the SDR waterfall no longer means resetting the gain each time.
- Clicking the scope tunes to the nearest 500 Hz.

Logging
- Fix: WSJT-X QSOs were sometimes logged twice.
- WSJT-X QSOs now get the station's name and QTH from QRZ (or from your last QSO with them).
- The log table has separate City and State columns. Long names and places are shortened, with the full text on hover.
- Portable calls with a slash (JA2MAX/P, AG4V/R) now get their QRZ look-up, country and worked-before info.
- The entry form shows a bearing line under the call info.

POTA
- Spot POTA activators on pota.app from HamStation.

Other
- The tuning step starts at 500 Hz.
- HamStation's window opens about a second faster.
- ---------------------------------------------------------------------------------------------

HamStation 0.60

New in this version:

FT8 audio waterfall
- On FT8 or FT4 the panadapter turns into an audio waterfall from the radio's USB codec, drawn like WSJT-X's Wide Graph: 0-3500 Hz scale, sharp lines, green 15 s period lines with time and band, WSJT-X's RX (green) and TX (red) markers.
- WSJT-X's decodes are written into the waterfall where they were heard. Click a call to answer it in WSJT-X; click anywhere else to move WSJT-X's RX frequency there.
- Audio WF in the panadapter bar: Auto (switches on FT8 / FT4), Always or Off. Four colour schemes: WSJT-X, Linrad blue, Fire, Greyscale.
- WSJT-X needs Settings > Reporting > "Accept UDP requests" ticked for click-to-call and click-to-set-RX.

fldigi link
- HamStation can be fldigi's logbook server. In fldigi: Configure > Config Dialog > Misc > TCP-IP sessions, fllog row: Addr 127.0.0.1, Port 8421, then Reconnect. QSOs logged in fldigi land in HamStation, and fldigi's dupe check and name / QTH look-up use HamStation's log.
- Settings: the WSJT-X tab is now called Digital, with Rig control, WSJT-X and Fldigi sub-tabs.

Radio panel
- PO, ALC and SWR meters with scales while transmitting, on Yaesu, Icom and Hamlib radios.

Panadapter
- POTA activators shown in cyan with the cluster spots (POTA box in the bar to turn them off).
- The world map behind the scope has been removed.

DX cluster
- Mode filter on the Clusters tab: All, Radio's mode, CW, Phone, Digital, FT8, FT4.
- Time filter: last 5 / 15 / 30 minutes, hour or 3 hours.
- DX cluster node dropdown in Settings.
- Fix: VE7CC (and other nodes ending spot lines with beeps) showed no spots. Please update if you use VE7CC.
- While a contest is open, greyed-out "worked" spots mean worked in this contest.

DXpeds tab
- Cluster spots of each DXpedition from the last hour: a Spotted filter, and click a call to see its spots (click one to tune).

Maps
- QSO map and 3D globe: show the current QSO, last 10, your last run, last 24 hours or last week. Maps are centred on your grid.
- Flat maps zoom right down to ground detail like the globe.

Contests
- ARRL School Club Roundup with its full exchange.

Layout
- The main window fits the screen without scrolling: clock above the radio panel on the left, QSO entry and map to the right, panadapter across the bottom.
- FT8 Call Roster: click a column heading to sort A-Z, again for Z-A.
===================================================================================================================================

Download HamStation-Setup-0.59.exe below and run it. It installs over your current HamStation and keeps your logbook and settings.

What's new in 0.59:
- Grey line on the maps: the daytime map where the sun is up, the city-lights night map where it's down, and a soft twilight band between. Switch it off with the gear button in the tab row.
- Cluster list sorting: click a column heading to sort, and click again to reverse. The band filter has a new "Radio's band" choice that follows your radio.
- Contest auto-fill: as you type a call, the exchange fills in from earlier QSOs, earlier contests, QRZ and cty.dat (zones, sections). Filled values are dimmed until you type over them.
- Mic EQ for the FTDX101D / FTDX101MP: the EQ button now works on these radios, not just the FT-891.
- Waterfall colour and gain: new WF (colour scheme) and WF gain controls on the panadapter toolbar.
- User manual: a full manual with screenshots of every feature.
=========================================================================================


New in 0.58

Contests
- In a contest, the entry clears when you tune more than 1 kHz away from
  where you started typing a call (like N1MM). Clicking a spot doesn't clear it.

DX alerts
- Spot alerts fade away after 15 seconds.
- Alerts pause while a contest log is open (no burst afterward).

Display
- Classic skin: analog S-meter in the Yaesu style (dark face, white scale,
  red needle).
- The green home-station dot is gone from the map behind the panadapter.

Install: download HamStation-Setup-0.58.exe below, run it, and click Next.
Your logbook and settings are kept.

**HamStation** is a ham radio station program for Windows by **K0BF**, shared with the
**DX Sharks** and friends: rig control, logging, DX cluster and POTA spots, maps, a
panadapter, contest logging, DXpedition alerts, and QRZ.com / LoTW uploads, all in one window.

You don't need a GitHub account to download it.

====================================================================================================

## Download and install (about 2 minutes)

1. Click **[Releases](../../releases/latest)** (or the **Releases** link on the right of this page).
2. Under **Assets**, click **`HamStation-Setup-…exe`**. Your browser downloads it.
3. Open the downloaded file (double-click it, or click it in your browser's downloads list).
4. Windows may show a blue box saying **"Windows protected your PC"**. That only means
   HamStation isn't from a big software company. Click **More info**, then **Run anyway**.
5. Click **Next** a few times, then **Finish**.
6. Start **HamStation** from the icon on your Desktop or in the Start menu.

## The first time you start it

1. Click **⚙ Main Settings** and fill in your **callsign** and **grid square**.
2. Under **Radio**, choose your radio type and click **Find radio**. HamStation finds the
   COM port for you. Close any other program that uses the radio first (HRD, N1MM, WSJT-X CAT…).
3. Optional: add your **QRZ.com** login and Logbook API key under **QRZ** to look up calls
   and upload QSOs.

That's it. Your settings and logbook stay on your computer.

## Updating

HamStation tells you when there's a new version (**Main Settings → Updates**, or a note
when it starts). Click the button, run the new setup the same way as above, and your
logbook and settings are kept.

## Questions or problems

Ask **K0BF**, or in the DX Sharks group. Please say which radio you have and what you clicked.

---

HamStation © 2026 K0BF. All rights reserved. Free to download and use for your own amateur
radio station; please don't sell it, re-upload it or put it in other software without asking
K0BF. It comes as-is, without any warranty. HamStation can key your transmitter and upload to
online logbooks; you're responsible for how it runs your station.
