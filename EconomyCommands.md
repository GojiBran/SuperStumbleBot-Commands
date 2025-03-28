# 💰 GojiBux Economy Command Reference

This document outlines all available economy commands for your bot, organized into categories for clarity and ease of reference.

---

## 💵 Gojibux

| Command      | Target   | Amount / Cost       | Description                       | Cooldown | Alias               | Emoji |
|--------------|----------|----------------------|-----------------------------------|----------|----------------------|--------|
| .mybux       |          |                      | Your Gojibux balance              |          |                      | 💵     |
| .getbux      |          |                      | Get Gojibux from ?                | 30s      | .gojibux, .gbx       | 🤑     |
| .snarfbux    |          |                      | Lose Gojibux                      |          |                      | 💵📉   |
| .$NARF       |          |                      | Your negative Gojibux balance     |          |                      | 💵     |
| .givebux     | username | amount \| max \| all | Give Gojibux to target            |          |                      | 🧧     |
| .donatebank  |          | amount \| max \| all | Donate Gojibux to LGH             |          |                      | 🏦🎁   |
| .stashbux    |          | amount \| max \| all | Stash your Gojibux                | 10s      |                      | 💰➕   |
| .unstashbux  |          | amount \| max \| all | Unstash your Gojibux              |          |                      | 💰➖   |
| .mystashbux  |          |                      | Your Gojibux stash                |          |                      | 💰     |
| .wallet      | username |                      | Your (or target’s) balance        |          | .balance, .bal       | 💼     |

---

## 🥦 Weed

| Command        | Target   | Amount / Cost       | Description                        | Cooldown | Alias       | Emoji |
|----------------|----------|----------------------|------------------------------------|----------|-------------|--------|
| .buyweed       |          | amount \| max \| all | Buy weed from WGH/LGH              |          | .priceweed  | 🥦➕   |
| .sellweed      |          | amount \| max \| all | Sell weed to WGH/LGH               |          |             | 🥦➖   |
| .donateweed    |          | amount \| max \| all | Donate weed to WGH                 |          |             | 🏬🎁   |
| .getweed       |          |                      | Get free weed                      | 30s      | .grow       | 🥦🌱   |
| .harvest       |          |                      | Harvest weed for WGH               | 30s      |             | 🏬🌱   |
| .myweed        |          |                      | Your weed balance                  |          |             | 🥦🎒   |
| .giveweed      | username | amount \| max \| all | Give weed to user                  |          |             | 🥦🎁   |
| .stealweed     | username |                      | Steal weed from user               |          |             | 🥦🤏   |
| .stashweed     |          |                      | Stash your weed                    | 1m       |             | 🥦🔒   |
| .unstashweed   |          |                      | Unstash your weed                  | 1m       |             | 🥦🔓   |
| .mystashweed   |          |                      | Your weed stash balance            |          |             | 🔒🎒   |
| .sesh          |          | 1–28g?               | Group smoke weed                   |          |             | 🍃     |
| .jointroll     |          | amount \| max \| all | Roll joints                        |          |             | 🥖     |
| .myjoints      |          |                      | Your joints balance                |          |             | 🥖🎒   |
| .jointsmoke    |          | amount \| max \| all | Smoke joints                       |          |             | 🥖💨   |
| .extract       |          |                      | Convert weed to extracts [WIP]     |          |             | 🥦⚡   |
| .selljoint     | offshore |                      | Sell joints offshore               |          |             | 🥖💸   |

---

## 🍝🍕 Food (Spaget & Pixxa)

| Command        | Target   | Amount / Cost       | Description                  | Cooldown | Alias                    | Emoji |
|----------------|----------|----------------------|------------------------------|----------|---------------------------|--------|
| .buyspaget     |          | amount \| max \| all | Buy spaget (20gbx)           |          | .spaget, .spg             | 🍝➕   |
| .myspaget      |          |                      | Your spaget balance          |          |                           | 🍝🎒   |
| .givespaget    | username | amount \| max \| all | Give spaget to user          |          |                           | 🍝🎁   |
| .stealspaget   | username |                      | Steal spaget                 |          |                           | 🍝🤏   |
| .eatspaget     |          | amount \| max \| all | Eat spaget                   |          |                           | 🍝🍽️  |
| .buypizza      |          | amount \| max \| all | Buy pixxa (10gbx)            |          | .pizza, .pixxa, .pza      | 🍕➕   |
| .mypizza       |          |                      | Your pixxa balance           |          |                           | 🍕🎒   |
| .givepizza     | username | amount \| max \| all | Give pixxa to user           |          |                           | 🍕🎁   |
| .eatpizza      |          | amount \| max \| all | Eat pixxa                    |          |                           | 🍕🍽️  |
| .getcookie     |          |                      | Get a cookie!                | 7s       | .cookie                   | 🍪➕   |
| .cook          |          |                      | Cook 1–20 spaget + 1–20 pixxa| 30m      |                           | 👨‍🍳   |

---

## 🐸🥔💎 Other Items

| Command     | Target   | Amount / Cost       | Description                  | Cooldown | Alias           | Emoji |
|-------------|----------|----------------------|------------------------------|----------|------------------|--------|
| .buyfrog    |          | amount \| max \| all | Buy frog coin (1M gbx)       |          | .frog            | 🐸➕   |
| .myfrog     |          |                      | Your frog coins              |          |                  | 🐸🎒   |
| .buypotato  |          | amount \| max \| all | Buy potato (1gbx)            |          | .potato, .tato   | 🥔➕   |
| .mypotato   |          |                      | Your potato balance          |          |                  | 🥔🎒   |
| .buycoin    |          |                      | Buy Goji coin (1B gbx)       |          | .coin            | 💎➕   |
| .mycoin     |          |                      | Your Goji coin balance       |          |                  | 💎🎒   |

---

## 🧨 Heists & Robbery

| Command       | Target   | Amount / Cost       | Description                    | Cooldown | Alias    | Emoji  |
|---------------|----------|----------------------|--------------------------------|----------|----------|--------|
| .bankrob      |          | 250gbx + 3–10%       | Rob the bank                   | 2m       | .brob    | 🏦🤏   |
| .weedrob      |          | 100g + 5–12%         | Rob the weed bank              | 2m       | .wrob    | 🏬🤏   |
| .bankheist    |          | 1000gbx + 10%        | Big bank robbery               | 10m      | .bheist  | 🏦🚛   |
| .weedheist    |          | 1000g + ?            | Big weed bank robbery          | 10m      | .wheist  | 🏬🚛   |
| .stealbux     | username |                      | Steal Gojibux from user        |          |          | 💵🤏   |

---

## 🎲 Gambling & Fun

| Command     | Target | Amount / Cost       | Description                        | Cooldown | Alias | Emoji |
|-------------|--------|----------------------|------------------------------------|----------|--------|--------|
| .gamble     |        | amount \| max \| all | Win or lose Gojibux                |          | .bet   | 🎰     |
| .adventure  |        |                      | Daily adventure for Gojibux        | 1m       | .ad    | 🧳     |
| .lottery    |        |                      | See current lottery pot            |          | .pot   | 🎫     |
| .givelottery|        | amount \| max \| all | Donate to lottery                  |          | .givepot | 🎫🎁 |
| .getlottery |        |                      | Pick a lottery winner              | 20m      | .getpot | 🎫🎊 |

---

## 🧹 Dumping / Resetting

| Command      | Target | Amount / Cost | Description                            | Cooldown | Alias | Emoji |
|--------------|--------|----------------|----------------------------------------|----------|--------|--------|
| .dumpall     |        |                | Dump all items (needs update)          |          |        | 🗑     |
| .dumpbux     |        |                | Dump all Gojibux into LGH              |          |        | 🗑💵   |
| .dumpweed    |        |                | Dump all weed into WGH                 |          |        | 🗑🥦   |
| .dumpspaget  |        |                | Delete all spaget                      |          |        | 🗑🍝   |

---

## 🧾 Info / Stats

| Command     | Target | Amount / Cost | Description                  | Cooldown | Alias        | Emoji |
|-------------|--------|----------------|------------------------------|----------|--------------|--------|
| .lgh        |        |                | LGH Gojibux balance          |          | .bank        | 🏦     |
| .wgh        |        |                | WGH weed balance             |          | .dispo       | 🏬     |
| .economy    |        |                | Circulation info             |          | .circulation | 📊     |
| .menu       |        |                | Items and prices menu        |          |              | 🛒     |
| .priceweed  |        |                | Weed buy/sell prices         |          |              | 🥦💵   |
| .stats      |        |                | Users with stashes count     |          |              | 📊     |

---

## 🏆 Leaderboards

| Command        | Target | Amount / Cost | Description               | Cooldown | Alias | Emoji |
|----------------|--------|----------------|---------------------------|----------|--------|--------|
| .top           |        |                | Top user stashes          |          |        | 🏆     |
| .topbux        |        |                | Top Gojibux stashes       |          |        | 🏆💵   |
| .topstashbux   |        |                | Top offshore Gojibux      |          |        | 🏆💰   |
| .topweed       |        |                | Top weed stashes          |          |        | 🏆🥦   |
| .topjoint      |        |                | Top joint stashes         |          |        | 🏆🥖   |
| .topspaget     |        |                | Top spaget stashes        |          |        | 🏆🍝   |
| .toppizza      |        |                | Top pixxa stashes         |          |        | 🏆🍕   |
| .topcookie     |        |                | Top cookie stashes        |          |        | 🏆🍪   |
| .topfrog       |        |                | Top frog coin stashes     |          |        | 🏆🐸   |
| .toppotato     |        |                | Top potato stashes        |          |        | 🏆🥔   |
| .topcoin       |        |                | Top Goji coin stashes     |          |        | 🏆💎   |
| .leastbux      |        |                | Bottom Gojibux stashes    |          |        | 🏆💵   |
| .leastweed     |        |                | Bottom weed stashes       |          |        | 🏆🥦   |
