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

Currently in private access. [Contact me](https://github.com/8pz/ren-options-trader#access) for early access

</div>

# Table of Contents

- [Capabilites](https://github.com/8pz/ren-options-trader#capabilites)
- [Changelog](https://github.com/8pz/ren-options-trader#changelog)
- [Disclaimer](https://github.com/8pz/ren-options-trader#disclaimer)
- [Access](https://github.com/8pz/ren-options-trader#access)

# Capabilites

Ren Options Trader is an automated bot built in Python that can follow an analyst's alerts on Discord. It uses a selfbot system in order to fetch alerts, but does not interact with the Discord client in any way. It then interprets those alerts, executes them, and tracks them using the Webull API. 

<details>
<summary>Trade results (from 11/14)</summary>

<br>

| ID         | Analyst       | Ticker | Strike Price | Expiration | Quantity | Entry Filled Time        | DCA   | Exit Filled Time                                                                                                         | Exit Price               | PNL    |
| ---------- | ------------- | ------ | ------------ | ---------- | -------- | ------------------------ | ----- | ------------------------------------------------------------------------------------------------------------------------ | ------------------------ | ------ |
| 1037703227 | Paper Prophet | TSLA   | 240c         | 11/14      | 4        | 11/14/2023 13:40:44 EST  | 2.9   |                                                                                                                          | 2.22                     | -216   |
| 1042068551 | Paper Prophet | QQQ    | 384p         | 11/14      | 9        | 11/14/2023 14:06:49 EST  | 0.45  |                                                                                                                          | 0.36                     | -9.0   |
| 1042175627 | Bryce         | QQQ    | 385p         | 11/15      | 10       | 11/15/2023 09:31:47 EST  | 0.56  | 11/15/2023 09:33:58 EST                                                                                                  | 0.53                     | -30    |
| 1038453107 | Paper Prophet | NVDA   | 500c         | 11/15      | 1        | 11/15/2023 10:03:54 EST  | 3.2   | 11/15/2023 10:07:30 EST,                                                                                                 | 3.550,                   | 35.0   |
| 1042182659 | Paper Prophet | SPY    | 452c         | 11/15      | 13       | 11/15/2023 10:25:53 EST  | 0.48  | 11/15/2023 10:28:32 EST,                                                                                                 | 0.45,                    | -39.0  |
| 1042182659 | Paper Prophet | SPY    | 452c         | 11/15      | 21       | 11/15/2023 10:30:54 EST  | 0.41  | 11/15/2023 10:51:16 EST,                                                                                                 | 0.58                     | 357    |
| 1042212638 | Paper Prophet | QQQ    | 387c         | 11/15      | 7        | 11/15/2023 10:35:44 EST  | 0.79  | 11/15/2023 10:41:33 EST,11/15/2023 10:46:49 EST,11/15/2023 10:51:16 EST,                                                 | 0.97,0.94,1.22,          | 188.0  |
| 1042213118 | Bryce         | QQQ    | 383p         | 11/16      | 12       | 11/16/2023 09:31:54 EST  | 0.53  | 11/16/2023 09:33:29 EST,Unknown                                                                                          | 0.63,0.51                | 48     |
| 1042173777 | Paper Prophet | SPY    | 450c         | 11/16      | 7        | 11/16/2023 09:54:17 EST  | 0.95  | 11/16/2023 09:56:29 EST                                                                                                  | 1.05                     | 70     |
| 1042231584 | Bryce         | SPX    | 4485p        | 11/16      | 2        | 11/16/2023 10:23:06 EST  | 2.45  | 11/16/2023 10:36:19 EST                                                                                                  | 3.15                     | 140    |
| 1042182124 | Paper Prophet | SPY    | 449c         | 11/16      | 15       | 11/16/2023 13:58:50 EST  | 0.43  | 11/16/2023 14:02:36 EST,                                                                                                 | 0.41,                    | -30.0  |
| 1042286112 | Paper Prophet | SPX    | 4505c        | 11/16      | 3        | 11/16/2023 14:45:23 EST  | 2.2   | 11/16/2023 14:48:26 EST,11/16/2023 14:59:26 EST,                                                                         | 2.75,1.95                | 5.0    |
| 1041712413 | Paper Prophet | TSLA   | 250c         | 11/20      | 7        | 11/20/2023 09:42:18 EST  | 0.94  | 11/20/2023 9:49:23 EST,11/20/2023 9:53:51 EST,                                                                           | 0.98,0.89                | 1      |
| 1042294183 | Bryce         | SPX    | 4535c        | 11/20      | 2        | 11/20/2023 09:48:03 EST  | 2.25  | 11/20/2023 9:53:48 EST,                                                                                                  | 2.70,                    | 90     |
| 1042194345 | Paper Prophet | SPY    | 453c         | 11/20      | 13       | 11/20/2023 12:14:41 EST  | 0.51  | 11/20/2023 12:32:44 EST,                                                                                                 | 0.46,                    | -65.0  |
| 1042230461 | Bryce         | SPX    | 4520p        | 11/21      | 1        | 11/21/2023 09:31:23 EST  | 2.55  | 11/21/2023 09:47:09 EST,                                                                                                 | 2.33,                    | -22.0  |
| 1042198517 | Paper Prophet | SPY    | 453c         | 11/21      | 7        | 11/21/2023 09:39:36 EST  | 1.04  | 11/21/2023 09:46:09 EST,11/21/2023 10:45:01 EST,11/21/2023 10:48:17 EST,11/21/2023 11:01:52 EST,11/21/2023 11:12:21 EST, | 0.83,0.62,0.69,0.7,0.58, | -138.0 |
| 1042231987 | Paper Prophet | SPY    | 452p         | 11/21      | 11       | 11/21/2023 09:48:04 EST  | 0.59  | 11/21/2023 09:53:03 EST,                                                                                                 | 0.54                     | -55    |
| 1042230546 | Paper Prophet | IWM    | 180c         | 11/22      | 23       | 11/21/2023 10:09:33 EST  | 0.26  | 11/21/2023 10:55:55 EST,11/21/2023 11:15:47 EST,                                                                         | 0.29,0.25,               | -11.0  |
| 1042198517 | Paper Prophet | SPY    | 453c         | 11/21      | 9        | 11/21/2023 10:23:36 EST  | 0.78  | 11/21/2023 10:45:01 EST,11/21/2023 10:48:17 EST,11/21/2023 11:01:52 EST,11/21/2023 11:12:21 EST,                         | 0.62,0.69,0.7,0.58,      | -60.0  |
| 1042198517 | Paper Prophet | SPY    | 453c         | 11/21      | 12       | 11/21/2023 10:34:28 EST  | 0.55  | 11/21/2023 10:45:01 EST,11/21/2023 10:48:17 EST,11/21/2023 11:01:52 EST,11/21/2023 11:12:21 EST,                         | 0.62,0.69,0.7,0.58,      | 9.0    |
| 1041716749 | Paper Prophet | XOM    | 105c         | 11/21      | 15       | 11/21/2023 10:51:35 EST  | 0.44  | 11/21/2023 11:04:44 EST,                                                                                                 | 0.56,0.53                | 159.0  |
| 1042198517 | Paper Prophet | SPY    | 453c         | 11/21      | 8        | 11/21/2023 14:14:34 EST  | 0.86  | 11/21/2023 15:02:49 EST,                                                                                                 | 0.89,                    | 12     |
| 1042226466 | Bryce         | SPX    | 4575c        | 11/22      | 3        | 11/22/2023 09:31:42 EST  | 2.45  | 11/22/2023 09:33:21 EST                                                                                                  | 2.95                     | 150    |
| 1042307513 | Bryce         | SPX    | 4580c        | 11/22      | 1        | 11/22/2023 09:39:07 EST  | 2.45  | 11/22/2023 09:39:21 EST                                                                                                  | 3.1                      | 65     |
| 1042185411 | Paper Prophet | TSLA   | 242.50c      | 11/22      | 3        | 11/22/2023 09:49:22 EST  | 1.9   | 11/22/2023 09:53:21 EST                                                                                                  | 1.3                      | -180   |
| 1041694562 | Paper Prophet | TSLA   | 240c         | 11/22      | 6        | 11/22/2023 10:31:23 EST  | 1.14  | 11/22/2023 10:39:40 EST,                                                                                                 | 0.96,                    | -108.0 |
| 1041694562 | Paper Prophet | TSLA   | 240c         | 11/22      | 4        | 11/22/2023 10:50:14 EST  | 0.92  | 11/22/2023 10:53:43 EST,                                                                                                 | 0.68,                    | -96.0  |
| 1041792676 | Paper Prophet | META   | 330p         | 11/27      | 5        | 11/27/2023 14:25:55 EST  | 1.5   | 11/27/2023 14:49:01 EST,                                                                                                 | 1.96,                    | 92.0   |
| 1042300977 | Diesel        | SPX    | 4545p        | 11/28      | 3        | 11/28/2023 13:56:23 EST  | 1.1   | 11/28/2023 13:57:47 EST,11/28/2023 14:08:47 EST,                                                                         | 1.28,1.78                | 104    |
| 1042304792 | Bryce         | SPX    | 4570p        | 11/29      | 3        | 11/29/2023 10:04:03 EST  | 2.45  | 11/29/2023 10:06:30 EST,                                                                                                 | 3.6,                     | 345    |
| 1041793476 | Paper Prophet | BA     | 225c         | 11/29      | 4        | 11/29/2023 12:38:22 EST  | 1.24  | 11/29/2023 13:14:49 EST,11/29/2023 13:21:24 EST,11/29/2023 13:51:25 EST                                                  | 1.51,1.57,1.5            | 116    |
| 1042301429 | Paper Prophet | QQQ    | 391c         | 11/29      | 12       | 11/29/2023 14:10:49 EST  | 0.39  | 11/29/2023 14:12:16 EST,11/29/2023 14:27:28 EST,                                                                         | 0.45,                    | 72     |
| 1041788413 | Paper Prophet | TSLA   | 245c         | 11/30      | 2        | 11/30/2023 12:41:30 EST  | 2.13  | 11/30/2023 13:06:37 EST,                                                                                                 | 1.88,                    | -50.0  |
| 1041849515 | Paper Prophet | TGT    | 135c         | 12/15      | 2        | 11/30/2023 15:43:16 EST  | 1.58  | 12/01/2023 14:17:13 EST,                                                                                                 | 1.8,                     | 44.0   |
| 1042601678 | Bryce         | SPX    | 4585c        | 12/01      | 1        | 12/01/2023 09:34:25 EST  | 1.9   | 12/01/2023 09:37:11 EST,                                                                                                 | 2.15,                    | 25.0   |
| 1042285564 | Bryce         | QQQ    | 389c         | 12/01      | 10       | 12/01/2023 09:51:27 EST  | 0.63  | 12/01/2023 09:54:29 EST,                                                                                                 | 0.66,                    | 30.0   |
| 1041780855 | Paper Prophet | IWM    | 181c         | 12/01      | 12       | 12/01/2023 09:53:58 EST  | 0.33  | 12/01/2023 09:57:37 EST,12/01/2023 10:03:32 EST,12/01/2023 10:55:37 EST,12/01/2023 11:29:25 EST,                         | 0.48,0.64,1.14,2.09,     | 521.0  |
| 1041786985 | Paper Prophet | TSLA   | 240c         | 12/01      | 11       | 12/01/2023 10:11:13 EST  | 0.43  | 12/01/2023 14:17:30 EST,                                                                                                 | 0.30,                    | -143.0 |
| 1041790068 | Paper Prophet | META   | 325c         | 12/01      | 5        | 12/01/2023 10:12:31 EST  | 0.92  | 12/01/2023 10:17:05 EST,                                                                                                 | 0.57,                    | -175.0 |
| 1042223576 | Bryce         | SPX    | 4550p        | 12/04      | 2        | 12/04/2023 10:04:45 EST, | 2.45, | 12/04/2023 10:15:36 EST,                                                                                                 | 2.91                     | 92     |
| 1042463205 | Bryce         | QQQ    | 383p         | 12/04      | 4        | 12/04/2023 10:31:44 EST, | 0.75, | 12/04/2023 10:34:50 EST,12/04/2023 10:35:05 EST,12/04/2023 10:37:39 EST                                                  | 0.91,0.87,0.86           | 56     |
| 1042309118 | Bryce         | SPX    | 4585c        | 12/05      | 2        | 12/05/2023 10:02:00 EST, | 2.15  | 12/05/2023 10:02:45 EST,12/05/2023 10:03:06 EST,                                                                         | 3.15,2.6,                | 145.0  |
| 1042139465 | Bryce         | SPX    | 4600c        | 12/06      | 3        | 12/06/2023 09:39:49 EST, | 2.45  | 12/06/2023 09:41:46 EST,                                                                                                 | 2.65,                    | 60.0   |
| 1042300319 | Bryce         | SPX    | 4570p        | 12/06      | 1        | 12/06/2023 09:45:19 EST, | 3.3   | 12/06/2023 09:46:11 EST,                                                                                                 | 3.35,                    | 5.0    |
| 1042300319 | Bryce         | SPX    | 4570p        | 12/06      | 1        | 12/06/2023 10:22:35 EST, | 3.0   | 12/06/2023 10:24:57 EST,                                                                                                 | 6.05,                    | 305.0  |
| 1042421220 | Bryce         | SPX    | 4585c        | 12/07      | 1        | 12/07/2023 09:31:04 EST, | 3.1   | 12/07/2023 09:31:34 EST,                                                                                                 | 3.4,                     | 30.0   |
| 1042308534 | Bryce         | SPX    | 4590c        | 12/07      | 1        | 12/07/2023 10:18:54 EST, | 2.45  | 12/07/2023 10:20:58 EST,                                                                                                 | 2.93,                    | 48.0   |
| 1042111063 | Paper Prophet | NVDA   | 470c         | 12/07      | 1        | 12/07/2023 10:40:35 EST, | 1.7   | 12/07/2023 10:54:11 EST,                                                                                                 | 1.87,                    | 17.0   |
| 1042046867 | Paper Prophet | WMT    | 155c         | 12/07      | 20       | 12/07/2023 10:48:54 EST, | 0.21  | 12/07/2023 11:15:27 EST,                                                                                                 | 0.15,                    | -120.0 |
| 1042112529 | Paper Prophet | NVDA   | 475c         | 12/08      | 5        | 12/08/2023 09:40:27 EST, | 0.9   | 12/08/2023 09:44:42 EST,12/08/2023 09:45:35 EST,12/08/2023 09:46:29 EST,                                                 | 1.31,1.33,1.12,          | 190.0  |
| 1042050659 | Paper Prophet | NFLX   | 455c         | 12/08      | 4        | 12/08/2023 09:42:59 EST, | 1.2   | 12/08/2023 09:50:21 EST,12/08/2023 09:54:54 EST,                                                                         | 1.41,0.91,               | -16.0  |
| 1042308925 | Bryce         | SPX    | 4605c        | 12/08      | 2        | 12/08/2023 09:46:30 EST, | 2.5   | 12/08/2023 09:50:00 EST,                                                                                                 | 2.83,                    | 66.0   |
| 1042112529 | Paper Prophet | NVDA   | 475c         | 12/08      | 6        | 12/08/2023 09:52:11 EST, | 0.77  | 12/08/2023 09:58:23 EST,12/08/2023 09:59:23 EST                                                                          | 0.87,0.89                | 64     |
| 1042301940 | Bryce         | SPX    | 4565p        | 12/08      | 2        | 12/08/2023 09:54:02 EST, | 2.65  | 12/08/2023 09:57:42 EST,                                                                                                 | 2.78,                    | 26.0   |
| 1042112430 | Bryce         | QQQ    | 390c         | 12/08      | 4        | 12/08/2023 09:59:27 EST, | 0.95  | 12/08/2023 10:00:21 EST,                                                                                                 | 1.42,                    | 188.0  |
| 1042112529 | Paper Prophet | NVDA   | 475c         | 12/08      | 4        | 12/08/2023 12:23:26 EST, | 1.2   | 12/08/2023 12:55:02 EST,12/08/2023 13:31:49 EST,                                                                         | 1.35,1.24,               | 38.0   |
| 1041085430 | Paper Prophet | NFLX   | 465c         | 12/15      | 1        | 12/08/2023 15:55:01 EST, | 2.23  | 12/11/2023 09:30:14 EST,                                                                                                 | 4.08,                    | 185.0  |
| 1042517708 | Bryce         | QQQ    | 393c         | 12/11      | 11       | 12/11/2023 09:32:39 EST, | 0.63  | 12/11/2023 09:33:29 EST,12/11/2023 09:33:55 EST,                                                                         | 0.77,0.83,               | 184.0  |
| 1042517464 | Bryce         | QQQ    | 391p         | 12/11      | 10       | 12/11/2023 09:36:06 EST, | 0.62  | 12/11/2023 09:37:27 EST,                                                                                                 | 0.4,                     | -220.0 |
| 1042474660 | Bryce         | SPX    | 4615c        | 12/11      | 2        | 12/11/2023 09:38:31 EST, | 2.95  | 12/11/2023 09:40:02 EST,                                                                                                 | 3.25,                    | 60.0   |
| 1042478824 | Bryce         | SPX    | 4595p        | 12/12      | 1        | 12/12/2023 09:31:56 EST, | 2.75  | 12/12/2023 09:32:45 EST,                                                                                                 | 2.85,                    | 10.0   |
| 1038696791 | Paper Prophet | META   | 330c         | 12/12      | 1        | 12/12/2023 09:45:15 EST, | 2.55  | 12/12/2023 09:48:42 EST,                                                                                                 | 3.03,                    | 48.0   |
| 1039957282 | Paper Prophet | COIN   | 150c         | 12/12      | 4        | 12/12/2023 09:49:53 EST, | 1.05  | 12/12/2023 09:54:11 EST,12/12/2023 10:09:18 EST,                                                                         | 1.13,1.48,               | 102.0  |
| 1042521578 | Bryce         | QQQ    | 395p         | 12/12      | 7        | 12/12/2023 09:54:36 EST, | 0.95  | 12/12/2023 10:03:28 EST,                                                                                                 | 0.61,                    | -238.0 |
| 1042504050 | Bryce         | SPX    | 4635c        | 12/12      | 2        | 12/12/2023 10:34:51 EST, | 2.33  | 12/12/2023 10:36:56 EST,12/12/2023 10:38:01 EST,                                                                         | 2.68,2.98,               | 100.0  |
| 1042521822 | Bryce         | QQQ    | 397p         | 12/12      | 9        | 12/12/2023 11:08:49 EST, | 0.77  | 12/12/2023 11:12:37 EST,12/12/2023 11:12:56 EST,                                                                         | 0.87,0.86,               | 85.0   |
| 1042421898 | Bryce         | SPX    | 4620p        | 12/12      | 2        | 12/12/2023 11:17:08 EST, | 3.34  | 12/12/2023 11:23:54 EST,                                                                                                 | 2.53,                    | -162.0 |
| 1042504050 | Bryce         | SPX    | 4635c        | 12/12      | 1        | 12/12/2023 11:34:11 EST, | 2.85  | 12/12/2023 11:38:29 EST,                                                                                                 | 3.15,                    | 30.0   |
| 1041465351 | Paper Prophet | META   | 335c         | 12/12      | 2        | 12/12/2023 13:02:55 EST, | 2.15  | 12/12/2023 13:53:52 EST,12/12/2023 15:03:50 EST,                                                                         | 2.34,2.86,               | 90.0   |
| 1039358839 | Paper Prophet | AMZN   | 150c         | 12/15      | 8        | 12/12/2023 15:51:49 EST, | 0.56  | 12/13/2023 09:31:50 EST,                                                                                                 | 1.04,                    | 384.0  |
| 1042479600 | Bryce         | SPX    | 4615p        | 12/13      | 1        | 12/13/2023 09:32:32 EST, | 2.69  | 12/13/2023 09:34:47 EST,                                                                                                 | 2.05,                    | -64.0  |
| 1042475688 | Bryce         | SPX    | 4680c        | 12/13      | 2        | 12/13/2023 09:37:07 EST, | 2.4   | 12/13/2023 09:44:01 EST,                                                                                                 | 2.03,                    | -74.0  |
| 1042479600 | Bryce         | SPX    | 4615p        | 12/13      | 1        | 12/13/2023 09:44:56 EST, | 2.55  | 12/13/2023 09:51:43 EST,                                                                                                 | 2.55,                    | 0.0    |
| 1038650383 | Paper Prophet | NFLX   | 470c         | 12/13      | 1        | 12/13/2023 09:58:15 EST, | 2.94  | 12/13/2023 10:09:44 EST,                                                                                                 | 3.45,                    | 51.0   |
| 1038671298 | Paper Prophet | NVDA   | 500c         | 12/13      | 4        | 12/13/2023 09:59:46 EST, | 1.14  | 12/13/2023 10:00:50 EST,                                                                                                 | 1.22,                    | 32.0   |
| 1042475688 | Bryce         | SPX    | 4680c        | 12/13      | 2        | 12/13/2023 10:06:56 EST, | 2.35  | 12/13/2023 10:11:16 EST,12/13/2023 10:13:13 EST,                                                                         | 2.55,2.53,               | 38.0   |
| 1039957282 | Paper Prophet | COIN   | 150c         | 12/13      | 5        | 12/13/2023 10:12:42 EST, | 0.92  | 12/13/2023 11:22:32 EST,12/13/2023 14:20:18 EST,                                                                         | 1.12,1.31,               | 157.0  |
| 1038699651 | Paper Prophet | META   | 340c         | 12/13      | 2        | 12/13/2023 10:19:24 EST, | 2.01  | 12/13/2023 11:08:08 EST,                                                                                                 | 1.66,                    | -70.0  |
| 1038671298 | Paper Prophet | NVDA   | 500c         | 12/13      | 4        | 12/13/2023 11:08:57 EST, | 1.15  | 12/13/2023 11:23:34 EST,                                                                                                 | 0.96,                    | -76.0  |
| 1036719131 | Paper Prophet | TSLA   | 235c         | 12/13      | 2        | 12/13/2023 11:31:27 EST, | 1.91  | 12/13/2023 11:54:47 EST,                                                                                                 | 1.96,                    | 10.0   |
|            |
</details>

## Highly configurable

Designed to be flexible and reliable -- it provides users with a wide array of configuration options, allowing the program to trade like a real person. 

- An analyst with a non-specific entry structure?
   - Setup the config to enter and exit off any keyword.
- Analyst doesn't tell you what trade to exit? -- Auto fetch details 
   - Automatically fetch the details of last placed trade of the specific analyst to use to trim, exit, or average up/down.
- Auto cancel order
   - Any standing orders after a certain amount of time will be cancelled
- No more missing out on exits -- Auto cancel and resend sell order
   - If a LMT sell order was not filled, it will resend it at MKT price.
- Backtesting
   - The program provides access to both a live and a paper account, allowing the user to test their configs and analysts first before putting anything on the line. All trade data is exported to a csv.
- A risky trade? contracts too expensive? -- Keyword and auto position sizing
   - The program can automatically detect certain keywords in order to not enter a trade or enter half sized. It can automatically determine how many contracts to buy based off a limit as long as the contract size doesn't deceed/exceed a limit.
- Extensive logging
   - The program provides detailed logs, allowing you to understand exactly how the system works and improve on your configs.
 
## Showcase

![image](https://github.com/8pz/ren-options-trader/assets/70970973/6369fc0a-ed56-4752-9aac-43ae95772adf)

![image](https://github.com/8pz/ren-options-trader/assets/70970973/dd562cf0-4c1a-4982-b723-c4adf2ba5827)

![image](https://github.com/8pz/ren-options-trader/assets/70970973/799c3e59-2c04-4179-a45e-696f19255051)

![image](https://github.com/8pz/ren-options-trader/assets/70970973/99305cca-00dd-46ac-a0ba-4c48f1715c0a)

![image](https://github.com/8pz/ren-options-trader/assets/70970973/a2427681-26a4-405b-8572-5ba73ed35a26)
![image](https://github.com/8pz/ren-options-trader/assets/70970973/d0972d1b-2418-41f4-8baf-c7070f66c8ef)

https://github.com/8pz/ren-options-trader/assets/70970973/a3cd2d13-09d5-49fe-b268-eb72810c7e3b

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
- Improved overview command

### 11/10/23

- Auto cancel and resend sell orders as market orders if not filled
- Averaging up/down
- Improved tracking system for open positions
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

### 11/29/23

- Refactored `handler.py`, `utils.py` for readability and expandability
- Revamped tests
- Detailed logs which logs actions (trigger keywords, entry/sell, etc) for a specific trade
- Max trade size for each analyst

### 12/04/23

- Message logs
- Average down improvements
- Improved log handler system

### 12/09/23

- Expiration date formatting
- Better log formatting
- Bug fixes

## In development

- Preset message formats
- Further refactoring for readability and expandability

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
- tele @ [onasn](https://t.me/onasn)
- email @ 123781023@proton.me

