<div align="center">
<pre>
██████╗ ███████╗███╗   ██╗    ████████╗██████╗  █████╗ ██████╗ ███████╗██████╗ 
██╔══██╗██╔════╝████╗  ██║    ╚══██╔══╝██╔══██╗██╔══██╗██╔══██╗██╔════╝██╔══██╗
██████╔╝█████╗  ██╔██╗ ██║       ██║   ██████╔╝███████║██║  ██║█████╗  ██████╔╝
██╔══██╗██╔══╝  ██║╚██╗██║       ██║   ██╔══██╗██╔══██║██║  ██║██╔══╝  ██╔══██╗
██║  ██║███████╗██║ ╚████║       ██║   ██║  ██║██║  ██║██████╔╝███████╗██║  ██║
╚═╝  ╚═╝╚══════╝╚═╝  ╚═══╝       ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝╚═════╝ ╚══════╝╚═╝  ╚═╝
---------------------------------------------------
program to execute options trades from Discord analyst alerts
</pre>
</div>

Currently in private access. [Contact me](https://github.com/8pz/ren-options-trader#access) early access

# Table of Contents

- [Capabilites](https://github.com/8pz/ren-options-trader#capabilites)
- [Changelog](https://github.com/8pz/ren-options-trader#changelog)
- [Disclaimer](https://github.com/8pz/ren-options-trader#disclaimer)
- [Access](https://github.com/8pz/ren-options-trader#access)

# Capabilites

Ren Options Trader is an automated bot built in Python that can follow an analyst's alerts on Discord. It uses a selfbot system in order to fetch alerts without interacting with the client in any way. It then interprets those alerts and execute options alerts using the Webull API.
![image](https://github.com/8pz/ren-options-trader/assets/70970973/ae7f4dba-1888-4cf8-ac11-fe0897a75dfa)

## Highly configurable

Designed to be flexible and reliable -- it provides users with a wide array of configuration options, allowing the program to trade like how the user would. 

- An analyst with a non-specific entry structure?
   - Setup the config to enter and exit off any keyword.
- Analyst doesn't tell you what trade to exit? -- Auto fetch details 
   - Automatically fetch the details of last placed trade of the specific analyst to use to trim, exit, or average up/down.
- Auto cancel order
   - any standing orders after a certain amount of time will be cancelled
- No more missing out on exits -- auto cancel and resend sell order
   - If a LMT sell order was not filled, it will resend it at MKT price.
- Backtesting
   - The program provides both a live and a paper account, allowing the user to test their configs and analysts first before putting anything on the line. All trade data is exported to a csv.
- A risky trade? contracts too expensive? -- Keyword and auto position sizing
   - The program can automatically detect certain keywords in order to not enter a trade or enter half sized. It can automatically determine how many contracts to buy based off a limit as long as the contract size doesn't deceed/exceed a limit.

## Video demonstration

...

# Changelog

### 11/05/23

- Initial release

### 11/07/23

- Tracking system for open positions
- STC types (MKT, LMT)
- Auto fetch last option details
- Improved code readability

### 11/09/23

- Auto cancel order if not filled
- Custom Webull API
- Added tests (somewhat functional)
- Improved overview command

### 11/10/23

- Auto cancel and resend sell orders as market orders if not filled
- Averaging up/down
- Improved tracking system for open positions
- Bug and QoL changes
- Improved code structure

### 11/14/23

- Export trading data to CSV
- Max size per trade option
- Take profit orders

### 11/15/23

- Preset ticker system
- Auto quantity calculator
- Revamped structure for asynchronicity
- GUI to show console, history, current positions, and edit orders

### 11/18/23

- Max/min contract size
- Exit and trim from GUI
- GUI clock
- Persistent monitored positions

### 11/26/23

- Settings page for analysts and config
- Refactored config and api system
- Updated error handling
- ```"alert_type"``` deprecated
- Bug fixes

# Disclaimer

This project is in development. Bugs **will** occur, please test and monitor the system yourself.

This project and all dependencies have not been tested extensively. Please backtest your own config with a paper account and use with caution.

This bot is used specifically for options trading on Webull. No other platforms are currently supported.

The automation of User Discord accounts also known as self-bots is a violation of Discord Terms of Service & Community guidelines and can result in your account(s) being terminated. I am not responsible for your actions.

**By using this project, you expressly acknowledge and agree to be bound by all the terms and conditions outlined below.**

<details>
<summary>Terms and Conditions</summary>

<br>

1. Not Investment Advice:
   This project and the alerts it tracks do not provide financial or investment advice. Users are solely responsible for their trading decisions, and should not rely on this program for investment guidance.

2. No Guarantees:
   Trading involves risks, and there are no guarantees of success. Past performance is not indicative of future results. Users should be aware of the inherent risks associated with trading.

3. Not Responsible for Losses:
   The creators and contributors of this project are not liable for any financial losses incurred by users due to their trading activities. Users use the program at their own risk.

4. Use at Your Own Risk:
   Users are encouraged to use this project at their own risk and with caution. It is recommended to seek professional financial advice before making any investment decisions.

5. No Endorsement of Alerts:
   This project does not endorse or validate the alerts it tracks. It is a tool for tracking and automation purposes only.

6. Disclaimer of Accuracy:
   The information provided by this project may not always be accurate or up-to-date. Users should verify and cross-check the information independently.

7. No Legal or Regulatory Compliance:
   This project does not offer legal or regulatory compliance services. Users are responsible for complying with all applicable laws and regulations.

</details>

# Access

Contact me for private access

- discord @ 123781023
- tele @ onasn
- email @ 123781023@proton.me
