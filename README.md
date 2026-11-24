# Hong Kong VPS Hosting: What Does It Cost, Which Plan Do You Need, and Will It Actually Be Fast From China? (Full Evoxt Plan Table)

Evoxt's cheapest Hong Kong plan is $2.99 a month for 512 MB of RAM, which is too small for anything running a database. The plan most people should start on is VM-1: one core rated up to 6.0 GHz, 2 GB RAM, 20 GB storage, 1 TB of transfer, $5.99 a month. What follows is every plan Evoxt lists, what the Hong Kong location changes about them, and the add-on charges that decide your real monthly bill.

> **Short answer for most readers:** VM-1 at $5.99/month covers a small WordPress site, a VPN endpoint, a Docker host, or a monitoring box. Buy VM-0.5 or VM-0.75 only for a static page, a DNS relay, or a jump host where 512 MB and 5 GB of disk are genuinely enough.
> 👉 [See Evoxt's current Hong Kong plans and deploy one](https://bit.ly/EvoXt)

## Every Evoxt plan, side by side

Prices are USD per month on monthly billing. Evoxt also sells prepaid terms from one month out to three years, so a longer commitment is available if you already know you're staying.

| Plan | vCPU | RAM | Storage | Transfer/mo | Price |
| --- | --- | --- | --- | --- | --- |
| [VM-0.5](https://bit.ly/EvoXt) | 1 core | 512 MB | 5 GB | 500 GB | $2.99 |
| [VM-0.75](https://bit.ly/EvoXt) | 1 core | 1 GB | 10 GB | 750 GB | $4.99 |
| [VM-1](https://bit.ly/EvoXt) | 1 core | 2 GB | 20 GB | 1 TB | $5.99 |
| [VM-1.5](https://bit.ly/EvoXt) | 2 cores | 2 GB | 20 GB | 1.5 TB | $6.95 |
| [VM-2](https://bit.ly/EvoXt) | 2 cores | 4 GB | 30 GB | 2 TB | $11.99 |
| [VM-3](https://bit.ly/EvoXt) | 4 cores | 4 GB | 30 GB | 3 TB | $14.99 |
| [VM-4](https://bit.ly/EvoXt) | 4 cores | 8 GB | 60 GB | 4 TB | $23.99 |
| [VM-6](https://bit.ly/EvoXt) | 8 cores | 8 GB | 60 GB | 5 TB | $29.99 |
| [VM-8](https://bit.ly/EvoXt) | 8 cores | 16 GB | 80 GB | 6 TB | $47.99 |
| [VM-12](https://bit.ly/EvoXt) | 16 cores | 16 GB | 80 GB | 8 TB | $60.95 |
| [VM-16](https://bit.ly/EvoXt) | 16 cores | 32 GB | 100 GB | 10 TB | $95.99 |

Two things about that table matter more than the headline prices. Evoxt lists one price per plan with no separate renewal rate, so the $5.99 is what recurs each month rather than a first-term teaser. And the transfer column reflects Evoxt's standard allocation: Hong Kong sits in its premium network group alongside Osaka and Malaysia Premium, which carry a smaller monthly allowance at the same plan price. Third-party Evoxt write-ups put the reduction at roughly half. Check the allowance shown for Hong Kong on the deploy screen before you settle on a plan size.

## What comes with every plan

Evoxt includes a weekly offsite backup on all plans at no extra cost, which is unusual at this price. The control panel also handles firewall rules without an SSH session, IP reassignment between servers, VM cloning, a browser VNC console for when SSH is broken, monitoring graphs, and sub-accounts for team members. Extra IPv4 addresses cost $3 per month each.

Payment is by credit or debit card, PayPal, Bitcoin, or USDt on Tron. You can also top up account credit and let Evoxt apply it to future invoices, which is the practical route if you want to pay in crypto once and let several months run.

## The Hong Kong location: same price, less transfer

Evoxt doesn't charge more for Hong Kong than for its standard regions. What you give up is monthly transfer, and that's the one line item to check against your actual usage. A 1 TB allowance on VM-1 is generous for a website and tight for a media proxy or a backup target.

The other gap is documentation. Evoxt doesn't name the Hong Kong facility or list its upstream carriers on the plan pages, so you can't verify the building or the peering mix before you buy. Two competitors in the same market do publish both: OliveVPS names Equinix HK1 in Tsuen Wan and lists HKIX, PCCW, China Telecom, NTT and Cogent as carriers; EDIS Global names Equinix HK2 on Shing Yiu Street in Kwai Chung and lists NTT, Cogent, PCCW and Level3. If a named Tier III facility is a hard requirement, that information exists elsewhere.

👉 [Check what the Hong Kong region costs on Evoxt today](https://bit.ly/EvoXt)

## What the published latency numbers actually measure

OliveVPS prints a latency table for its own Hong Kong facility: 1–3 ms locally, 55 ms to Tokyo, 120 ms to Sydney, 200 ms to London. EDIS Global ran a Speedtest CLI test from its Hong Kong platform on 21 September 2026 and recorded 934.06 Mbps down, 930.23 Mbps up and 0.34 ms idle latency against a Hutchison HK test server, with a note on the same page that the result is not a guarantee of throughput or latency to any other destination.

Both sets of figures come from the providers' own hosts and their own test targets. The 0.34 ms in particular measures a hop inside Hong Kong, not the experience of a visitor in Shenzhen at 9 pm. For mainland traffic, one third-party Evoxt buying guide describes the general range as 20–60 ms to southern provinces on a well-optimised CN2 path, degrading to 150–260 ms at peak on congested routes. Evoxt does not advertise a China-optimised route for Hong Kong in the material reviewed here.

If mainland latency is the whole reason you're buying, treat it as an unknown and test it. Deploy the smallest plan that fits, run MTR from your own network during evening peak against your real user locations, and decide inside the refund window. Several providers in this market publish test IPs, looking glass pages or downloadable test files you can ping before ordering anything.

## The bill after the headline price

**Extra IPs.** Evoxt charges $3 per month per additional IPv4. If you're terminating TLS for several sites on separate addresses, that adds up across a year.

**Overage.** Evoxt's pricing page doesn't publish a bandwidth overage rate. Competitors publish theirs, which gives you the range to negotiate against: OliveVPS bills $0.005/GB past the plan allowance, and Host Hong Kong charges HK$50 per additional TB per month, or HK$1,200/month for 100 Mbit of dedicated international bandwidth. On a bandwidth-heavy workload, ask support for the overage rate in writing before you prepay three years.

**Windows.** Evoxt advertises Windows RDP images alongside Linux. Which tier includes a licence, and whether the licence is bundled or bring-your-own, is worth confirming at checkout. This is where cheap Hong Kong plans usually bite: OliveVPS makes its $3.99 Starter Linux-only and moves Windows to the $7.99 Pro tier, and EDIS marks its KVM Smart and Starter plans as unsuitable for Windows Server, pushing buyers to the €21.99 Basic Plus.

**Prepay discount.** Evoxt sells terms from monthly to three years but doesn't publish a prepay discount rate, so the saving comes from not thinking about invoices rather than from a percentage. For scale, EDIS gives one month free on annual billing, about 8.3%.

**Your own time.** Evoxt is self-managed. Host Hong Kong states outright that its KVM plans are unmanaged and bills management hourly, with remote hands at HK$500/hr in working hours and HK$1,000/hr outside them. EDIS limits support to infrastructure, connectivity, account and billing questions. None of the sub-$10 tiers in this market include someone to fix your broken PHP upgrade.

## Which plan fits which job

The price steps between adjacent plans are uneven, and two of them are clearly better value than the rest.

- A static page, a DNS relay, a WireGuard endpoint for two people: VM-0.5 at $2.99 or VM-0.75 at $4.99. The 5 GB disk on VM-0.5 fills quickly once logs and a database appear.
- One WordPress site with a cache plugin, a small team VPN, or a Docker host running a handful of containers: VM-1 at $5.99.
- Work that's bound by cores rather than memory: VM-1.5 at $6.95, which is 96 cents more than VM-1 for double the cores.
- Several sites or a busier Postgres instance: VM-2 at $11.99 for 4 GB, or VM-3 at $14.99 for the same 4 GB and double the cores, a $3 difference.
- 8 GB and up: VM-4 at $23.99 has 4 cores, VM-6 at $29.99 has 8. Six dollars for four more cores is the best step on the list unless something else in your stack is the bottleneck.
- VM-8 through VM-16 at $47.99–$95.99 are for fleets, resale, or workloads with a specific 16-core requirement.

Evoxt also states that you can add individual resources to a VM without changing plans, so starting at VM-1 and growing sideways is a supported path rather than a migration.

## When Evoxt is the wrong choice

A few cases where another provider fits better, based on what each one publishes:

**You need hourly billing.** LightNode bills from $0.012/hour and lists four Hong Kong plans from $10.41/month to $74.31/month, with deployment quoted at 1–2 minutes. Evoxt starts at monthly and goes up from there.

**You want the cheapest 1 GB box with a short refund window.** OliveVPS sells 1 GB, 25 GB NVMe, 1 TB on 1 Gbps for $3.99/month, Linux only, with a 7-day money-back guarantee and no free trial.

**You want the data centre named before you pay.** OliveVPS and EDIS both publish the building, the address and the carrier list. Evoxt doesn't.

**You want to pay in HKD and scale RAM hard.** Host Hong Kong runs from HK$80/month for 2 GB to HK$1,600/month for 128 GB, all unmanaged, with subnet blocks priced from HK$160/month for a /29.

**You want traffic that doesn't expire.** EDIS handles overage through a traffic pool that carries over rather than billing per GB.

## FAQ

**Is the Evoxt Hong Kong VPS managed?** No. You get full root access and you're responsible for the software stack, security patches and backups inside the VM. The weekly offsite backup is Evoxt's, not a substitute for your own copy.

**Can I run Windows?** Evoxt lists Windows RDP images among its OS options. Confirm on the deploy screen which plans include a licence and whether it's bundled or BYOL, since providers in this price bracket often restrict Windows to higher tiers.

**What happens if I go over the transfer allowance?** Evoxt doesn't publish an overage rate on its pricing page. Ask support before you commit to a long prepaid term.

**Can I pay monthly, and can I pay in crypto?** Yes to both. Billing runs from monthly to three-year terms, and Evoxt accepts cards, PayPal, Bitcoin and USDt on Tron.

**What's the refund policy?** Third-party Evoxt setup guides describe a 14-day money-back guarantee with a full refund available inside the first 24 hours. Confirm the current terms on the order page, since refund language is the thing providers change most often.

**Can I upgrade later?** Yes. Evoxt supports adding individual resources to an existing VM without moving plans, and additional IPv4 addresses are $3/month each.

**Will it be fast from mainland China?** That depends on the route your visitors' carriers take into Hong Kong, not on the plan you buy. Evoxt doesn't publish a China-optimised routing claim for Hong Kong. Test with MTR from the networks that matter to you during peak hours and use the refund window as your safety net.

## Before you order

Match the plan to the job and stop there: static page or jump host, VM-0.5; one site or a VPN, VM-1; core-bound work, VM-1.5 or VM-3; 8 GB and multi-site, VM-6.

Then confirm two things on the order screen. First, that the region reads Hong Kong and not a standard region, because the plan you selected will show a different transfer allowance once the premium group is applied. Second, the monthly figure and the transfer limit shown for that specific region, since the table above reflects standard allocations and Evoxt bills one recurring price with no separate renewal rate.

👉 [Open the Evoxt Hong Kong deploy screen and confirm the plan price for your region](https://bit.ly/EvoXt)
