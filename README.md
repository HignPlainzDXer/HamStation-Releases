# HamStation

Download HamStation-Setup-0.60.exe below and run it. It installs over your current HamStation and keeps your logbook and settings.
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
