# Best Asia VPS: Is Evoxt's $5.99 Plan Enough, Where Does It Deploy in Asia, and What Happens When You Hit the Transfer Cap? (All 11 Plans, Priced)

Evoxt's VM-1 costs **$5.99/month** and gives you 1 core advertised at up to 6.0 GHz, 2 GB RAM, 20 GB of storage, 1 TB of monthly transfer and a weekly backup, deployable in Tokyo or Malaysia. For one website, one bot, a small API or a WireGuard endpoint, that is the plan to buy, and it is cheaper than the 2 GB tiers at Cloudzy and LightNode that most "best Asia VPS" lists push first.

The $2.99 VM-0.5 exists for people who genuinely need 512 MB. It stops being pleasant the moment Docker enters the picture. If your last box had 2 GB and kept running out, VM-2 at **$11.99** doubles the RAM and adds 10 GB of disk for roughly the price of two coffees a month.

What follows: all eleven plans, what "Asia" actually means in Evoxt's region list compared with Cloudzy, Contabo and LightNode, what the transfer cap does when you cross it, and the cases where buying a VPS at all is the wrong move.

> **Quick pick:** VM-1 at $5.99/mo for a single site, app or tunnel. VM-2 at $11.99/mo once Docker, a compiler and a database share the machine. 👉 [Open Evoxt's plan list and choose a region](https://bit.ly/EvoXt)

## All Evoxt plans and prices

Every core in the table is advertised at up to 6.0 GHz, and every plan includes a weekly backup. Prices are in USD, billed monthly unless you prepay.

| Plan | vCPU / RAM | Storage | Transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512 MB | 5 GB | 500 GB | $2.99/mo | [Deploy VM-0.5](https://bit.ly/EvoXt) |
| VM-0.75 | 1 core / 1 GB | 10 GB | 750 GB | $4.99/mo | [Deploy VM-0.75](https://bit.ly/EvoXt) |
| VM-1 | 1 core / 2 GB | 20 GB | 1 TB | $5.99/mo | [Deploy VM-1](https://bit.ly/EvoXt) |
| VM-1.5 | 2 cores / 2 GB | 20 GB | 1.5 TB | $6.95/mo | [Deploy VM-1.5](https://bit.ly/EvoXt) |
| VM-2 | 2 cores / 4 GB | 30 GB | 2 TB | $11.99/mo | [Deploy VM-2](https://bit.ly/EvoXt) |
| VM-3 | 4 cores / 4 GB | 30 GB | 3 TB | $14.99/mo | [Deploy VM-3](https://bit.ly/EvoXt) |
| VM-4 | 4 cores / 8 GB | 60 GB | 4 TB | $23.99/mo | [Deploy VM-4](https://bit.ly/EvoXt) |
| VM-6 | 8 cores / 8 GB | 60 GB | 5 TB | $29.99/mo | [Deploy VM-6](https://bit.ly/EvoXt) |
| VM-8 | 8 cores / 16 GB | 80 GB | 6 TB | $47.99/mo | [Deploy VM-8](https://bit.ly/EvoXt) |
| VM-12 | 16 cores / 16 GB | 80 GB | 8 TB | $60.95/mo | [Deploy VM-12](https://bit.ly/EvoXt) |
| VM-16 | 16 cores / 32 GB | 100 GB | 10 TB | $95.99/mo | [Deploy VM-16](https://bit.ly/EvoXt) |

The pricing has a logic worth knowing before you pick. From VM-1 up, the models with the round numbers (VM-1, VM-2, VM-4, VM-8, VM-16) land at almost exactly $3 per GB of RAM. Their core-heavy twins cost more per gigabyte because the second half of the name is what you're buying: VM-3 works out to $3.75 per GB, VM-6 the same, VM-12 to $3.81. VM-8 is the cheapest way to reach 16 GB at $47.99, and VM-12 is the cheapest way to reach 16 cores.

Disk grows far more slowly than RAM. VM-1 ships 20 GB and VM-16 ships 100 GB, so a container-heavy workload hits the storage ceiling long before the RAM ceiling. Evoxt does let you add individual resources to an existing VM without changing plans, which softens that, though the pricing page only publishes one add-on price: an extra IPv4 at $3/month.

VM-1.5 deserves a mention because it's an odd shape. For $0.96 more than VM-1 you get a second core at the same 2 GB of RAM. Compiling, ffmpeg, a game server tick loop: worth the dollar. Running three Docker containers: the RAM is still the wall.

## What every plan includes, and what it doesn't

Included across the range, per Evoxt's pricing page and VPSBenchmarks' feature record:

- Weekly backup of every VM, restorable by you when needed
- IPv6 alongside the IPv4 address
- A firewall where you pick open and closed ports per VM
- A REST API at api.evoxt.com
- Monitoring charts for CPU, bandwidth, RAM and storage
- Root access, a custom control panel, one-click upgrades
- Card, PayPal and Bitcoin
- Windows images, which a longer third-party review reports come without a licence surcharge at any tier

Not included:

- **DDoS protection.** VPSBenchmarks lists it as absent. If you run something that attracts attacks, budget for a proxy in front of it.
- **Hourly billing.** Evoxt bills monthly up to three years, and lets you top up account credit and have invoices drawn from it. If you want a box for three days, this is the wrong product.
- **Reverse DNS.** Relevant if you plan to send mail directly from the box.
- **A stated money-back window.** The pricing page doesn't publish one, and a LowEndTalk thread describing a difficult refund is cited in third-party coverage. Treat the first purchase as the trial and start at $2.99 if that worries you.

## Where Evoxt's Asia regions actually sit

This is the part most listicles skip. Evoxt's region strip lists the United States, United Kingdom, Canada, Germany, Poland, Amsterdam, Japan (Tokyo), Malaysia and Australia. In APAC that means Tokyo, Malaysia and Australia, and **no Singapore**.

Third-party trackers put the footprint larger than the strip suggests. VPSBenchmarks counts 18 data centres across four continents, StackRates counts 11 regions, and a separate published review mentions Hong Kong, Osaka and a "Malaysia Premium" location. That review also reports that the premium regions keep the same plan price but cut the monthly transfer allowance roughly in half. Confirm which region you're getting in the cart before you pay; the transfer number changes with it.

Now compare how the competition defines "Asia":

- **Cloudzy** runs ap-sgp-1 in Singapore and ap-syd-1 in Sydney. Its own FAQ says a Tokyo region is on the way but is not open for deployment, even though the page's overview box lists "SGP + TYO". Prices are identical across regions.
- **Contabo** has exactly one Asian location, in Singapore's Tai Seng data centre district, with Telia and Hurricane Electric as upstreams and a public test IP of 103.164.55.91 for checking latency before you buy.
- **Kamatera** includes Hong Kong among its locations and states that Asian VPS pricing matches its other regions.
- **LightNode** advertises 23 Asian regions with KVM virtualisation and hourly billing.

If your users are in Indonesia, Thailand, Vietnam or the Philippines, Evoxt's Malaysia location is the closest thing it has to Singapore, and Malaysia-to-Jakarta latency is in the same ballpark as Singapore-to-Jakarta. If you need a Singapore IP specifically, Evoxt's published list doesn't offer one and you should look elsewhere.

👉 [Check which Evoxt regions are available on the order page](https://bit.ly/EvoXt)

## What the public benchmark runs show

VPSBenchmarks collects YABS runs on Evoxt instances. Four plans have published results, each a single run on a different date and host.

| Plan | Geekbench 6 single | Geekbench 6 multi | Disk read | Network down |
| --- | --- | --- | --- | --- |
| VM-1 (Feb 2026) | 2,390 | 2,385 | 1,930 MB/s | 7,905 Mbit/s |
| VM-2 (Aug 2026) | 1,964 | 3,662 | 1,420 MB/s | 8,970 Mbit/s |
| VM-4 (Nov 2025) | 2,572 | 6,994 | 1,382 MB/s | 9,605 Mbit/s |
| VM-8 (May 2026) | 2,722 | 11,459 | 2,137 MB/s | 935 Mbit/s |

Single-core scores in the 2,400–2,700 range are the reason to look at Evoxt at all; that is high for the price bracket and it's what the company markets. Don't read the VM-1 versus VM-2 gap as VM-2 having a slower CPU. These are single runs on different hosts months apart, and the spread is normal noise. The VM-8 network figure is far below the other three in the same collection, which could be a busy host or a capped port on that particular machine.

## Same budget, different specs

Two RAM classes, three providers, all figures read from each provider's own page.

| RAM | Provider & plan | vCPU | Storage | Transfer | Price/mo |
| --- | --- | --- | --- | --- | --- |
| 2 GB | Evoxt VM-1 | 1 | 20 GB | 1 TB | $5.99 |
| 2 GB | Cloudzy 2 GB | 1 | 60 GB | 3 TB | $7.48 promo ($14.95 list) |
| 2 GB | LightNode 2 GB | 1 | 50 GB | 1 TB | $7.71 |
| 4 GB | Evoxt VM-2 | 2 | 30 GB | 2 TB | $11.99 |
| 4 GB | Cloudzy 4 GB | 2 | 120 GB | 5 TB | $14.48 promo ($28.95 list) |
| 4 GB | LightNode 4 GB | 2 | — | 2 TB | $14.70 |

The dash is where LightNode's page lists core count and transfer for that tier but not storage. Cloudzy's promotional rate is described in its own FAQ as a 50% discount on the annual plan, so that $7.48 or $14.48 assumes you prepay twelve months; the list prices are what you pay monthly.

Evoxt wins the monthly comparison and loses badly on disk. If your workload wants 60 GB or more of local storage, paying Cloudzy $1.49 to $2.49 more per month for triple the disk is straightforwardly better value, provided you're happy prepaying a year. If you'd rather stay monthly, the honest comparison is $5.99 against $14.95.

## What happens when you cross the transfer allowance

Evoxt throttles. It doesn't bill overages, and there are no bandwidth penalty fees. VPSBenchmarks records the pricing model as "allowance then throttled", with a free allowance of 2 TB/month for a 2-core/4 GB instance, which matches VM-2's published 2 TB. Evoxt does not publish the speed you drop to after throttling, so the practical impact depends on which plan you're on and how hard you were pushing it.

Other providers handle the same moment differently:

- **OVHcloud** publishes APAC quotas of 500 GB on VPS-1, 1 TB on VPS-2 and VPS-3, and 3 TB on VPS-4, after which the port drops to **10 Mbps**.
- **Cloudzy** tiers 1 TB, 3 TB and 5 TB by plan and claims no egress fees.
- **LightNode** tiers 1 TB to 4 TB by plan.

A reality check on what 1 TB means, since it sounds like a lot: 1 TB is roughly 33 GB a day, which is about 33,000 page views daily at 1 MB per page. Ship 3 MB pages with images and it's closer to 11,000. A brochure site will never notice. A media-heavy WordPress site with a video on the homepage can burn through it in a fortnight.

👉 [Start with VM-2 if you want the 2 TB allowance and 4 GB of RAM](https://bit.ly/EvoXt)

## Billing, renewals and the hourly question

Evoxt publishes one price per plan on its pricing page, with no separate first-term promotional rate that expires later. StackRates, which tracks the page, recorded the prices as unchanged since 14 October 2026. Prepayment runs from monthly to three years, and account credit can be topped up and applied to future invoices automatically.

There's no hourly option, which separates Evoxt from Cloudzy, Kamatera and LightNode. Kamatera also has no minimum contract and a 30-day free trial; Cloudzy offers a 14-day money-back guarantee. A month of Evoxt's smallest box costs $2.99, so a short experiment isn't expensive here, it's just not metered by the hour.

## Who should not buy this

**You're a DDoS target.** No protection is included. Put Cloudflare in front or pick a provider that bundles mitigation.

**You need a Singapore IP.** Evoxt's published regions are Tokyo, Malaysia and Australia in APAC. Close enough for Southeast Asian users, not the same thing if a vendor or a payment processor geo-checks you.

**You want a guarantee before you commit.** No money-back window is published. Spend $2.99 on VM-0.5, break it, rebuild it, and decide from there.

**You need enterprise support.** Evoxt was founded in 2020. Third-party coverage reports ticket responses stretching to 48 hours at peak, with Telegram and Discord channels answering faster. Fine for a side project, thin for a production incident at 3 a.m.

**You're hosting one small site and own a spare PC.** A used Dell OptiPlex micro form factor with 8–12 GB of RAM and a 256 GB drive runs about $100, idles near 10 watts, and paired with Tailscale gives you a machine you can reach from anywhere. Against a $10/month VPS that pays for itself in around ten months. The catch is a residential connection, no public IP, and you become the on-call engineer.

## Which plan to order

- One static site, a bot, a WireGuard or OpenVPN endpoint → **VM-0.5 or VM-0.75**, $2.99 or $4.99. 512 MB runs nginx and a tunnel comfortably.
- One Node, Django or Laravel app with a small database → **VM-1**, $5.99. 2 GB is the point where a language server and a build stop fighting each other for memory.
- Docker Compose with several containers, or anything that compiles → **VM-2**, $11.99. The extra 10 GB of disk matters as much as the extra 2 GB of RAM.
- CPU-bound and RAM-light (transcoding, build agents, a game server) → **VM-1.5** at $6.95 or **VM-3** at $14.99.
- 16 GB or more → **VM-8** at $47.99 for RAM value, **VM-12** at $60.95 if you need the cores instead.

Two things to confirm in the cart before you pay. First, the region: Tokyo, Malaysia and any premium locations carry different transfer allowances for the same money. Second, whether the plan's disk is enough, because 20 GB on VM-1 fills faster than you expect once images and dependencies land.

👉 [Deploy Evoxt's VM-1 from $5.99/month](https://bit.ly/EvoXt)
