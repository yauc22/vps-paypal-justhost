# VPS PayPal: Can You Buy Without a Credit Card, Does It Cost Extra, and What Does $1.99 Actually Get You? (JustHost Plans, Locations and Renewal Questions)

JustHost accepts PayPal at checkout, and its VPS lineup starts at **$1.99/month**, so you can order a server without typing a card number anywhere. You choose a location, choose a configuration, pay through PayPal, and the server shows up in your control panel with root access.

Below: what that entry price covers, where the machines physically sit, what PayPal does and doesn't protect you from, and the two questions worth settling with support before you pay.

> **Most readers should take the entry plan in the location nearest their users.** JustHost lists VPS from **$1.99/month** and takes PayPal, credit cards, Alipay, UnionPay and crypto at checkout. That's enough for a proxy, a small site, a bot or a test box. Move up only when RAM or disk is the actual limit. 👉 [Check the current JustHost entry price](https://justhost.asia/?ref=196392)

## Why JustHost doesn't have a tidy four-tier price table

Its catalog is organized by location first, configuration second. A third-party tracker that refreshes daily counted **99 JustHost VPS plans** listed as of 2026-10-24, with the cheapest at **$13.92/year**, spread across 20+ data centers. The same nominal plan therefore costs different amounts depending on whether the box sits in Moscow, Amsterdam, Hong Kong or São Paulo.

That's why the four-tier tables used by Cloudzy or LightNode don't map onto it cleanly. Here's what is verifiable:

| Where | What's confirmed | Price | Billing | Order |
| --- | --- | --- | --- | --- |
| Smallest config, location of your choice | KVM, NVMe/SSD storage, dedicated IPv4, built-in DDoS filtering | from **$1.99/mo** (site headline); **$13.92/yr** lowest annual listing (third-party, 2026-10-24) | Monthly or annual | [Open the JustHost order page](https://justhost.asia/?ref=196392) |
| Hong Kong | KVM, NVMe array, 300 Mbps–1 Gbps port, unlimited traffic, 1×IPv4 + 1×IPv6 | Set on the order page | Monthly | [Order a Hong Kong VPS](https://justhost.asia/?ref=196392) |
| São Paulo (SAO1), Brazil | KVM, NVMe array, 300 Mbps–1 Gbps, unlimited traffic, IPv4 only | Set on the order page | Monthly | [Order a Brazil VPS](https://justhost.asia/?ref=196392) |
| Other locations | 20+ data centers, free switching between them after purchase | Varies by location | Monthly or annual | [See all JustHost locations](https://justhost.asia/?ref=196392) |

Two specs to note before anything else. Hong Kong ships with both IPv4 and IPv6; the Brazil box is IPv4-only, according to an independent review of that location. And "unlimited traffic" refers to volume, not port speed. The port itself is 200 Mbps to 1 Gbps depending on the plan.

## The $1.99 question: what's the catch?

The entry price buys a small machine. That's not a flaw, it's the point. A 1 vCPU box with a gigabyte or so of RAM runs a WireGuard tunnel, a monitoring agent, a static site or a Telegram bot without complaint. It will not run a WooCommerce store with 40 plugins.

JustHost's own FAQ covers the rest of the basics: NVMe/SSD storage, 24/7 support, DDoS filtering included on every VPS, and a control panel for day-to-day management. You can also change the configuration later, adding CPU cores, RAM or disk without migrating your data to another server, with the changes applied at minimal downtime. That matters more than it sounds. It means the cheap plan isn't a trap you have to escape by rebuilding; it's a starting point you resize.

What JustHost does not publish is a renewal price. Neither does Cloudzy with its 50% discounts, nor Infrawire with its 40–50% cuts, nor HOSTKEY with its per-plan percentages. Every one of those figures is a current display price. Assume the first invoice and the third invoice may differ, and check what your renewal costs before you commit to an annual term.

## What paying with PayPal actually changes

Four things, and only one of them is about money.

**Your card number never reaches the host.** You authenticate on PayPal, PayPal settles with the merchant. If your funding source is a PayPal balance or a linked bank account, no card is involved at all. Infrawire states plainly that bank details "never pass through our checkout," and that's how PayPal works generally, not a special feature of one host.

**Refunds come back the way they went out.** Cloudzy spells this out for its own 14-day window: refunds return to the original payment method, so a PayPal payment lands back in your PayPal account. That's the standard route, and it's the reason to pay with PayPal if you think you might cancel inside the trial window. A refund to a card you've since closed is a much worse afternoon.

**You can change your mind about the method.** Both Cloudzy and Infrawire let you pay the first invoice with PayPal and switch to a card for renewals, or the reverse, from the client area, without touching the server. Whether JustHost's panel exposes the same toggle isn't documented on its pages, so confirm it in the client area after your first invoice if you plan to switch.

**PayPal's own costs are yours.** No host in this comparison adds a PayPal surcharge. Cloudzy says it doesn't, Infrawire says 0% payment fees, and LightNode says every payment method costs the same. The real cost sits with PayPal: currency conversion spread if your account currency differs from the invoice currency, plus whatever your funding source charges. On a $2 server that's noise. On a €52/month plan paid from a USD balance, it's worth thirty seconds of attention.

One more thing worth knowing before you plan around PayPal: eligibility is decided by PayPal's rules for your country, not by the host. Cloudzy's FAQ is unusually direct about this. The merchant accepts whatever PayPal approves on its end. If PayPal isn't available to you, JustHost's card, Alipay, UnionPay and crypto options are the fallback.

## Hong Kong or Brazil? What independent testing found

Both locations have been reviewed with actual benchmarks, and the results are specific enough to be useful.

The Hong Kong box runs on an E5-2690 v4 with KVM virtualization and BBR enabled. Disk I/O measured around 460 MB/s, with 4K read/write near 78 MB/s and roughly 19.6K IOPS. Geekbench 6 came in at 592 single-core and 1,736 multi-core. That's modest compute, fine for network-facing work, thin for compilation. The routing is the part to weigh: all three Chinese networks route outbound through the US, and return traffic for Telecom and Unicom does the same, so latency to mainland China is worse than the "Hong Kong" label suggests. The reviewer's own conclusion was that a relay improves it.

The São Paulo box uses an E5-2699 v4, I/O around 509 MB/s, 4K read/write near 82 MB/s at about 20.6K IOPS, and Geekbench 6 scores of 705 and 1,822. Latency is high on every route tested, which is geography, not configuration.

IP reputation is where the two diverge, and this is the kind of detail that decides purchases. The Hong Kong IP unlocked Singapore TikTok, Hong Kong Disney+ and Netflix, US Gemini and Steam currency, but not Claude or ChatGPT. The Brazil IP unlocked TikTok, ChatGPT, Claude, Disney+ and Netflix, but not Gemini. Both reviews date from early 2026, and IP-based unlock results change as addresses get recycled, so treat these as a snapshot rather than a guarantee.

Both locations support one-click data center switching and one-click IP switching from the panel, with up to 50 switches per VM on the Brazil series. If you're buying specifically to test which IP works for a service, that switching ability is worth more than a slightly faster CPU.

## How fast do you get root, and can you get your money back?

JustHost's documented flow is short: choose a plan, click Order, complete payment, then you get access to the control panel and the server with the configuration you picked. The site doesn't state a provisioning time, so treat "how many minutes" as an open question rather than a promise.

The rest of the market gives you a sense of what's reasonable. Cloudzy quotes 60 seconds to deploy and under 5 minutes from click to SSH. LightNode says 1–2 minutes, with the whole flow under 5. Infrawire lands around 5 minutes. HOSTKEY is the cautionary example: its page says servers deploy "in several minutes" near the top and "within a few hours" in the FAQ, which is exactly the kind of contradiction you only find by reading both.

On refunds, JustHost's pages don't state a money-back window. If a cancellation window is part of your decision, ask support in writing before you pay and keep the reply. Among the hosts that do publish one, Cloudzy offers 14 days and Infrawire 7. That gap between two providers making near-identical PayPal pitches is the single most overlooked line in this comparison.

| Provider | Entry price | Footprint | Billing | Refund window |
| --- | --- | --- | --- | --- |
| JustHost | $1.99/mo | 20+ locations | Monthly or annual | Not published |
| Cloudzy | $2.48/mo (list $4.95) | 13 regions | Hourly, monthly, yearly | 14 days |
| LightNode | $7.71/mo | 40+ countries | Hourly | Not stated |
| HOSTKEY | €1.27/mo, VAT excluded | Europe and US | Monthly or annual; annual is roughly 12× monthly | Not stated |
| Infrawire | €8.30/mo (list €16.60) | France plus other locations | Monthly | 7 days |

HOSTKEY's VAT note deserves a mention on its own. Its listed prices exclude VAT and the page says the final cost is whatever appears at checkout. Cloudzy, LightNode and Infrawire don't mention tax on their PayPal pages at all, which is not the same as saying there isn't any.

## Questions people ask before paying with PayPal

**Does JustHost charge extra for using PayPal?**
No PayPal surcharge is listed anywhere on JustHost's pages, and the three competitors that address it directly all say the same price applies regardless of method. Confirm the total on the final screen anyway, because that's the number that gets charged.

**Can I get a refund back to PayPal?**
Refunds return to the original payment method as standard practice. JustHost doesn't publish a refund window, so the window itself is the thing to confirm with support rather than the route.

**Do I need a credit card at all?**
No. PayPal can be funded from a balance or a linked bank account. LightNode markets its PayPal VPS specifically on the "no credit card" angle, and the mechanics are the same everywhere.

**Can I pay the first invoice with PayPal and renew by card?**
Cloudzy and Infrawire both allow this from the client area. JustHost's documentation doesn't cover it, so check the panel after your first payment.

**Is the price I see at checkout the final price?**
Not automatically. HOSTKEY publishes prices excluding VAT, and add-ons like extra IPs are billed separately at most hosts. The checkout total is the only figure that counts.

## Picking a plan, and two things to confirm first

Match the plan to the workload, not to the label. A proxy, a DNS resolver, a monitoring node or a test box needs the smallest configuration, and paying more for it buys nothing you'll notice. A production site with a database and real traffic needs the next tier up on RAM and disk, plus a location chosen for latency rather than price. If you're buying to test streaming or service unlocks, the one-click IP switching on the Hong Kong and Brazil series is a more useful feature than extra CPU.

Start small at $1.99, resize later without migrating, and you've kept the risk to one month's fee. 👉 [Start with the entry JustHost VPS](https://justhost.asia/?ref=196392)

Two things to nail down before you click pay. First, whether the checkout total includes tax and any add-ons, since that's the only number that reflects what leaves your account. Second, whether a refund window exists and how many days it runs, because a server you can't return is a server you have to live with.
