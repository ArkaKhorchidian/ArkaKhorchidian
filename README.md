### Hi, I'm Arka 👋

I build fast systems for markets and networks: **C++ trading infrastructure**, **quant research tooling**, **telecom / broadband data pipelines**, and **open-source developer tools** you can run in one command.
MS Electrical Engineering @ Columbia (ML + internet systems) · building broadband planning infrastructure at Wireless 20|20 · co-founder of [Crowded](https://crowded.nyc).

---

### 📊 Featured: [booktop](https://github.com/ArkaKhorchidian/booktop)

**A live order book in your terminal, like `htop` for markets.** `uvx booktop` streams the real BTC-USD book from Coinbase: depth ladder, trade tape, imbalance and flow. No key, no setup. It also replays any stock from a NASDAQ ITCH day.

<a href="https://github.com/ArkaKhorchidian/booktop"><img src="https://raw.githubusercontent.com/ArkaKhorchidian/booktop/main/docs/hero.gif" alt="booktop streaming the live BTC-USD order book" width="720"></a>

### ⚡ Featured: [fastitch](https://github.com/ArkaKhorchidian/fastitch)

**NASDAQ TotalView-ITCH 5.0 → Polars / pandas / Parquet, at native speed.** One `pip install`, all 23 message types, streaming in constant memory, plus order-book reconstruction. 51x faster than existing Python parsers on real NASDAQ data.

```python
import fastitch
frames = fastitch.read("12302019.NASDAQ_ITCH50.gz", types="orders", symbols=["AAPL"])
book   = fastitch.book("12302019.NASDAQ_ITCH50.gz", "AAPL", depth=5, every="1s")
```

---

### 🧰 Developer tools

| Tool | Try it | What it does |
|---|---|---|
| [subwaytop](https://github.com/ArkaKhorchidian/subwaytop) | `uvx subwaytop` | Every NYC subway train, live, on a map in your terminal, plus departure boards and service alerts |
| [zombieports](https://github.com/ArkaKhorchidian/zombieports) | `uvx zombieports` | What's running on port 3000? Every listening port, which project started it, how long it's been up, and one key to kill the forgotten ones |
| [whoholdsup](https://github.com/ArkaKhorchidian/whoholdsup) | `uvx whoholdsup` | Who holds up your app? Reads your lockfile and shows how many dependencies are kept alive by one person, untouched for years, or recently changed hands |
| [sketchydeps](https://github.com/ArkaKhorchidian/sketchydeps) | `uvx sketchydeps` | Is anything sketchy installed? Checks `node_modules` and your Python env for known malware, typosquats, brand-new packages and install-time code |
| [isitthewifi](https://github.com/ArkaKhorchidian/isitthewifi) | `uvx isitthewifi` | Is it the Wi-Fi? Grades your connection A–F (lag under load, jitter, loss, DNS) and tells you in plain English whether it's your Wi-Fi, your router, your ISP or DNS |
| [whotalks](https://github.com/ArkaKhorchidian/whotalks) | `uvx whotalks` | Who does your computer talk to? Watches every connection for a minute and groups them by company and app, with a privacy grade |
| [slowrc](https://github.com/ArkaKhorchidian/slowrc) | `uvx slowrc` | Why does your terminal take so long to open? Profiles your `.zshrc` line by line and fixes the slow parts safely |
| [loosekeys](https://github.com/ArkaKhorchidian/loosekeys) | `uvx loosekeys` | Finds API keys sitting in plain text on your laptop: shell history, forgotten `.env` files, AI tool & MCP configs. Masked output, nothing leaves your machine |
| [shellwrapped](https://github.com/ArkaKhorchidian/shellwrapped) | `uvx shellwrapped` | Spotify Wrapped for your terminal: top commands, typos, 2am sessions, your shell personality |
| [codewrapped](https://github.com/ArkaKhorchidian/codewrapped) | `uvx codewrapped ~/code` | Spotify Wrapped for your code, across every git repo on your machine, private ones included |

<a href="https://github.com/ArkaKhorchidian/subwaytop"><img src="https://raw.githubusercontent.com/ArkaKhorchidian/subwaytop/main/docs/hero.gif" alt="subwaytop: live NYC subway map in the terminal" width="720"></a>

<p>
  <a href="https://github.com/ArkaKhorchidian/shellwrapped"><img src="https://raw.githubusercontent.com/ArkaKhorchidian/shellwrapped/main/docs/card.png" alt="shellwrapped share card" width="400"></a>
  <a href="https://github.com/ArkaKhorchidian/codewrapped"><img src="https://raw.githubusercontent.com/ArkaKhorchidian/codewrapped/main/docs/card.png" alt="codewrapped share card" width="400"></a>
</p>

---

### 🏗️ Trading infrastructure (C++20)

| Project | What it does |
|---|---|
| [Limit Order Book Simulator](https://github.com/ArkaKhorchidian/Limit-Order-Book-Simulator) | Price-time priority matching engine, fixed-point prices, cache-aware layout |
| [Lock-Free Queues](https://github.com/ArkaKhorchidian/Lock-Free-Queue-SPSC-Ring-Buffer) | SPSC ring buffer + bounded MPMC queue, every `memory_order` justified |
| [Latency Benchmarking Harness](https://github.com/ArkaKhorchidian/Latency-Benchmarking-Harness) | RDTSC cycle counting: caches, syscalls, atomics, branch misprediction |
| [ITCH 5.0 Parser & Replay](https://github.com/ArkaKhorchidian/ITCH-5.0-Full-Parser-NASDAQ-Historical-Replay) | Book reconstruction + microstructure analytics on real NASDAQ data |
| [FIX 4.2 Parser & Order Router](https://github.com/ArkaKhorchidian/FIX-Protocol-Parser-Order-Router) | Stream parser, session state machine, smart order routing |
| [Pre-Trade Risk Gateway](https://github.com/ArkaKhorchidian/Pre-Trade-Risk-Gateway) | Sub-µs risk checks in front of the router: price collars, fat-finger, worst-case position, throttling, self-trade prevention, kill switch |
| [OUCH 5.0 Client & Exchange Simulator](https://github.com/ArkaKhorchidian/OUCH-Order-Entry-Client-Simulator) | NASDAQ binary order entry over SoupBinTCP, gap-free reconnect, price-time matching simulator |
| [Multicast Market Data Analyzer](https://github.com/ArkaKhorchidian/Market-Data-Multicast-Analyzer) | UDP feed timing, gap detection, pcap replay |

### 📈 Quant research (Python)

| Project | What it does |
|---|---|
| [Optimal Execution](https://github.com/ArkaKhorchidian/Market-Impact-Optimal-Execution-Model) | Almgren–Chriss with Monte Carlo and TWAP/VWAP benchmarks |
| [Factor Model & PCA Alpha](https://github.com/ArkaKhorchidian/Factor-Model-PCA-Alpha-Research) | Factor construction → alpha → backtest → attribution |
| [Regime & Volatility](https://github.com/ArkaKhorchidian/Regime-Detection-Volatility-Forecasting) | HMM regimes; EWMA vs GARCH vs GJR vs HAR-RV out of sample |

### 📡 Networks, telecom & hardware

| Project | What it does |
|---|---|
| [gtp-meter](https://github.com/ArkaKhorchidian/GTP-U-Diameter-packet-parser-metering-pipeline) | GTP-U / Diameter parsing with line-rate per-subscriber metering |
| [Policy / Authorization Service](https://github.com/ArkaKhorchidian/Real-Time-Policy-Authorization-Service) | 5G PCF / 4G PCRF-style real-time policy decisions |
| [6G Channel Estimation](https://github.com/ArkaKhorchidian/6G-Neural-Network-Channel-Estimation-Project) | Neural OFDM estimators: +11.7 dB NMSE over mismatched MMSE |
| [Polyglot ASIC](https://github.com/ArkaKhorchidian/tt-protocol-emulator) | Programmable protocol-emulator chip for Jane Street's Tiny Tapeout contest |
| [SignSpeak](https://github.com/ArkaKhorchidian/SignSpeak) | On-device ASL fingerspelling on an ESP32-S3 with a BLE Flutter app |

---

**Stack:** C++20 · Python · Polars/Arrow · PyTorch · Linux networking · Verilog
**Find me:** [arkakhorchidian.com](https://arkakhorchidian.com)
