<img src="docs/images/icon.png" alt="" width="96" align="left">

# SDR Workbench

**One front panel for many radios. Use your ANAN, Hermes Lite 2, FlexRadio,
Kenwood TS-890S or TS-990S, or a USB receiver from your Windows PC or Mac,
with the same keys, meters and bandscope for each.**

[![Download](https://img.shields.io/github/v/release/lmacc/SDR-Workbench-Releases?label=Download)](https://github.com/lmacc/SDR-Workbench-Releases/releases/latest)
![Windows 10 and 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows)
![macOS 13 and later](https://img.shields.io/badge/macOS-13%2B%20%C2%B7%20Apple%20silicon%20%26%20Intel-555555?logo=apple)
[![Licence key](https://img.shields.io/badge/Licence%20key-PayPal-00457C?logo=paypal)](https://www.paypal.com/donate/?business=9XVP453VRC5GC&amount=20&no_recurring=1&item_name=SDR+Workbench.+For+a+licence+key+%28EUR+20+or+more%29%2C+put+your+PC+code+in+the+note.+73%2C+Leslie+EI5GJB&currency_code=EUR)

<br clear="left">

![SDR Workbench on an ANAN G2 with three receivers](docs/images/anan-g2-three-receivers.jpg)

*An ANAN G2 listening on three bands at once: 40 m, 20 m and 17 m, each with
its own bandscope and waterfall. Along the top are the menus and the tools.
On the left are the meter and the transmit, receive and noise keys. On the
right you choose the band, the mode and the filter width, and the sliders
for volume, filter, power and CW run along the bottom. The controls follow
the receiver you click, and its outline shows which one that is.*

You learn one panel and use it with every radio you own. SDR Workbench shows
only what the radio in front of it can do, so a receiver shows no transmit
keys and a Kenwood shows the Kenwood's own filters. The panel lays itself
out to fit your screen, from a laptop to a wide monitor, and you can move
any group of controls with Ctrl+E.

Everything runs on your own computer. There is no account to make and
nothing to sign in to.

## The radios it works with

- **Apache Labs:** the ANAN G2, Orion MkII and Angelia, and the ANAN 10,
  100, 100D and 200D, with PureSignal.
- **Hermes Lite 2** and the openHPSDR Metis boards.
- **FlexRadio:** the FLEX-5000A and 5000C on FireWire (Windows only), and
  the FLEX-6000 and 8000 series over your network.
- **Kenwood:** the TS-890S and TS-990S, over USB or over your network.
- **USB receivers:** RTL-SDR dongles, the Airspy R2, Mini, HF+ and HF+
  Discovery, the SDRplay RSP family, and the RX888 MkII (Windows only).
- **The simulator,** so you can learn the panel before you connect anything.

The FLEX-6000 and 8000 series and the EU1SW Brick 2 follow their makers'
published information but have not yet been tried on a real radio.

## The same panel on every radio

![A FLEX-5000A with two receivers](docs/images/flex-5000a-two-receivers.jpg)

*A FLEX-5000A with its second receiver on 20 m. The panel is the same, and
the radio's own keys, for image rejection and swapping the IQ, are in the
DEVICE group on the right.*

![A Kenwood TS-990S with both receivers](docs/images/ts-990s-two-receivers.jpg)

*A Kenwood TS-990S. RX2 is the radio's sub band, with its own antenna, mode
and filter, and the bandscope comes from the radio itself.*

![A Kenwood TS-890S](docs/images/ts-890s.jpg)

*A Kenwood TS-890S. The radio does its own processing, so the panel works
the radio's own filters, its scope and its keys.*

## A closer look

![The RACK](docs/images/rack.png)

*The RACK: SDR Workbench's own transmit audio units, from a phase rotator
and EQ through compressors to a limiter, in the order you choose. Your own
VST 3 plugins can go anywhere in the chain. Each unit shows what it is doing
to your voice as you speak, and here the RACK takes a microphone in through
an audio interface and sends it out again to the radio.*

![Trying a style before you use it](docs/images/rack-styles.png)

*Point at a style and the picture shows what it would do before you click
it. Drag the picture's handles to change a unit, and press TRY to hear the
whole rack on your own voice without transmitting.*

![The VST HOST](docs/images/vst-host.png)

*The VST HOST runs your audio interface through your VST 3 plugins and out
to your radios, in a row or side by side, with every delay lined up. Here a
microphone goes through five plugins, one after another, at 96 kHz.*

![The Audio Analyser](docs/images/audio-analyser.png)

*The Audio Analyser shows what you receive, or your own transmit audio, with
four holds to compare before and after, and levels, loudness and distortion.*

![Settings](docs/images/settings.png)

*All the settings are in one window. Type a word in Find a setting and it
takes you straight there.*

![A picture behind the bandscope](docs/images/picture-behind-bandscope.png)

*Put any picture you like behind the bandscope.*

There is much more: power calibration for your own radio, a logbook, a DX cluster with alerts, CW, RTTY and PSK
decoding, FreeDV, recording and playback, KiwiSDR and UberSDR receivers
tuned along with your radio, CAT and TCI for your other programs, and
operating from away from home through a Raspberry Pi.

## Download

From the [latest release](https://github.com/lmacc/SDR-Workbench-Releases/releases/latest):

- **SDR-Workbench-&lt;version&gt;-setup.exe**: the installer for Windows 10
  and 11 (64-bit).
- **SDR-Workbench-&lt;version&gt;-macos.dmg**: for macOS 13 and later, on
  Apple silicon and Intel Macs.
- **libspecbleach** and **codec2 source zips**: the source of two libraries
  SDR Workbench uses, offered as their licence asks. You don't need them to
  run it.
- **SHA256SUMS.txt**: a checksum for each file.

> **"Windows protected your PC"?** The installer isn't signed. Click
> **More info**, then **Run anyway**. On a Mac, the README in the disk image
> says how to open it the first time.

## Before you start

- **A network radio** (an ANAN, Hermes Lite 2 or FLEX-6000): connect it to
  the same network as your computer. Add Radio finds it for you.
- **A Kenwood:** for USB, install Kenwood's virtual COM port driver so the
  radio's ports appear. For the network, set up the radio's LAN screen with
  its address and login.
- **A USB receiver on Windows:** if Windows has it on the wrong driver,
  SDR Workbench offers to fix it for you the first time.
- **A USB receiver on a Mac:** install its library with
  [Homebrew](https://brew.sh): `brew install librtlsdr airspy airspyhf`. An
  SDRplay RSP needs SDRplay's own API from sdrplay.com.
- **A FLEX-5000A:** SDR Workbench brings FlexRadio's own driver and offers
  to install it.

The user guide is inside the application, under **HELP**, then
**User guide**. It covers every control and how to set everything up, with
pictures.

## Calibrating your radio

Some radios need no calibrating at all, and the others start from sensible
figures. The guide's chapter 26 explains each one step by step.

- **Kenwood TS-890S and TS-990S, FLEX-6000 and 8000:** the radio calibrates
  itself. There is nothing to do.
- **FLEX-5000A:** SDR Workbench reads the radio's own calibration from its
  memory every time it starts. There is nothing to do.
- **ANAN G2:** starts from power and frequency figures measured on a real
  G2, so it is close straight away. Measure your own to make it exact.
- **Other ANANs:** start with a cautious power curve, so the PWR slider gives
  less than it says until you measure yours.
- **Hermes Lite 2:** its power works in its own fixed steps, so there is no
  power curve to measure.

**Measuring your power** takes about a minute a band. You need a dummy load
and a wattmeter; never do it into an antenna.

1. With the radio running, open **Settings**, then **Transmitting**, then
   **PA gain**, and press **CALIBRATE**.
2. Pick the band, set **Most** to the highest power you are happy with, and
   light **DUMMY LOAD**. Nothing transmits until you do.
3. Press **KEY**. A steady carrier goes out for four seconds. Read your
   wattmeter, type the reading in and press **ADD**.
4. Repeat for the next step. After about four carriers the band is done.
   Press **SAVE**, and the PWR and TUNE sliders use the new figures at once.

The first carrier is always low, and no step that would go over your Most
is keyed. The S meter, the frequency and the watt meter are set on the
**Calibration** and **Watt meter** pages in Settings.

## Licence keys

SDR Workbench works fully for 14 days from the first time you start it.
After that it needs a licence key for your computer. A key costs EUR 20 or
more and is yours for good, with free updates.

1. Open **HELP**, then **Licence key**, and press **COPY** to copy your
   computer's code.
2. Press **GET A KEY**. PayPal opens in your browser. Paste your code in the
   note with your payment.
3. Your key comes back by email. Enter that email address, paste the key
   and press **ACTIVATE**.

A key works on one computer. For another computer, get a key with that
computer's code. Keys for the TS-890S Desktop and TS-990S Desktop apps don't
work in SDR Workbench.

## Use at your own risk

SDR Workbench is provided "as is", without warranty of any kind. It controls
a radio transmitter, and you use it entirely at your own risk. To the
fullest extent the law allows, I accept no responsibility or liability for
any damage, loss or harm arising from its use or from being unable to use
it. That includes damage to your radio, amplifier, antenna or other
equipment, loss of data, and interference caused to others. You are
responsible for your station: for how it is set up, and for operating it
within your licence and the regulations that apply to you.

SDR Workbench is not made by or endorsed by Apache Labs, FlexRadio or
JVCKENWOOD. ANAN is a trademark of Apache Labs. TS-890S, TS-990S and
KENWOOD are trademarks of JVCKENWOOD.

## Problems and suggestions

Please use [Issues](https://github.com/lmacc/SDR-Workbench-Releases/issues).
Say which version you have (**HELP**, then **About SDR Workbench**, shows
it) and which radio, and what you did just before the problem.

73, Leslie EI5GJB
