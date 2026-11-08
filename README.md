# Colo Data Center: What You're Renting, Which Model Fits, and the Questions That Decide the Quote (Plus the 30–50 kW Density Test)

A colo data center rents you floor space, power, cooling and network access inside a building someone else owns and operates. The servers in your rack stay yours, and so does everything running on them. Four things decide whether a given facility fits: how many kilowatts it will contractually deliver to your rack, how the hall is cooled, whether you can choose your own carriers, and what the SLA actually commits to. Since AI workloads started landing in ordinary enterprise racks, there is a fifth question worth asking early: can this building cool a rack drawing 30–50 kW, or only the density it was originally designed for?

Below: how colo differs from cloud and from your own machine room, how to pick between retail, wholesale and hybrid, the specifics to verify in writing, what a quote should itemize, and when colo is the wrong purchase entirely. SpinServers comes in where it is relevant, since its colocation business runs on quotes rather than a public price list.

> **If you already know you want colo:** send the provider your rack count, kW per rack, target metro and term length, and ask for a written quote that separates space, power, cross-connects and remote hands. SpinServers handles colocation, GPU and custom deployments this way — 👉 [submit your rack and power requirements to SpinServers](https://bit.ly/Spinservers) and get the numbers before you compare anyone else's.

## Colo, cloud, and your own machine room: where the responsibility line sits

In a colo, you own and operate the physical assets and you are wholly responsible for managing and securing the entire infrastructure stack. In a cloud, the underlying physical assets belong to the provider, and responsibility is split between provider and customer according to the service model (IaaS, PaaS, SaaS). That single difference explains most of the practical trade-offs: colo gives you hardware control and predictable capacity, cloud gives you elastic capacity and someone else's hardware problem.

Building your own facility is the third option, and the expensive one. Operating an in-house data center means paying for power, cooling, staff and property taxes on an ongoing basis, and expanding means major capital spending; a new build runs into millions. Colocation spreads cooling, power, security and connectivity costs across many tenants, and removes the need to plan utility feeds, backup generators and HVAC yourself.

## Retail, wholesale, or hybrid: pick by what you're leasing, not by company size

| Model | What you lease | How it's usually billed | Typical fit |
| --- | --- | --- | --- |
| Retail | A rack, part of a rack, or a caged-off area | Per square foot plus power used; some providers sell lockable cabinets with power in fixed increments | Teams starting with one to a handful of racks, or whose density varies |
| Wholesale | A large share of a facility or an entire data hall | Lower unit rate in exchange for a bigger commitment | Organizations isolating equipment in locking cages, private suites, or the whole building |
| Hybrid | Colo space plus cloud integration | Mixed: colo line items plus connectivity and cloud services | Workloads split between on-premises hardware and cloud, where traffic between them matters |

The decision rule is short. If your requirement is a lockable cabinet or a partial rack and you expect to grow a rack at a time, retail is the structure built for that. If you need a private suite or the whole hall, wholesale pricing exists precisely because you are buying space at that scale. If half your stack is staying in cloud and latency between your hardware and your cloud region is a design constraint, ask specifically about direct connections to internet exchanges and cloud providers; that is what turns a colo into a hybrid deployment rather than just a cage in a building.

## The verification list: seven systems to inspect before you sign

Power. Look for multiple utility feeds, uninterruptible power supplies and backup generators, typically diesel or natural gas, with power distribution units delivering conditioned power to each rack. Ask how many independent paths reach your cabinet, not how many the building has in total.

Cooling. Computer room air conditioners and air handlers are the baseline; hot aisle/cold aisle containment is what keeps them efficient. Ask what happens on a design-day failure and whether liquid cooling exists as an option or only as a future plan.

Network. A colo should give you access to a range of telecom carriers and network providers, with redundant high-bandwidth options and direct connections to internet exchanges and cloud providers. The industry term carrier hotel is increasingly used for facilities that are carrier-neutral, meaning no single ISP owns your path out.

Physical security. Biometric access controls, surveillance cameras and on-site personnel on the building side; firewalls, intrusion detection and prevention systems on the network side.

Fire suppression. FM-200 or inert gas systems, which protect equipment rather than drenching it.

Monitoring. Environmental monitoring keeps hardware out of overheating and over-humid conditions, and DCIM gives you a single view of the estate. Ask whether the DCIM interface is reachable through a web browser and whether it exports data in standard formats so it can feed your own systems.

SLA. Availability targets, response times and the planned maintenance process, plus the provider's actual uptime history. "Five nines" (99.999%) works out to roughly five minutes of downtime a year; whether you get anywhere near that depends on how the credit terms and maintenance windows are written, not on the headline number. On compliance, the common baselines are PCI DSS, HIPAA and SOC 2, with ISO 27001 and Tier III or Tier IV certifications as signals of redundancy and availability discipline.

## Why density is now the first question, not the last

The bar has moved. Colocation is no longer a conversation about renting rack space and power; it is a conversation about whether the facility can handle the heat and density that modern compute and AI workloads produce. A facility can hold a perfect SLA and still cap you at a rack density that strands the GPUs you just bought.

Concrete example of what "built for it" looks like: a Denver facility listed at 11100 West 8th Ave publishes roughly 2 MW of current power capacity and plans for centralized chilled water plus direct-to-chip liquid cooling to support rack densities of 30–50 kW and above. That profile also notes UPS-backed power, generator redundancy, and existing 10-inch water infrastructure sized for large-scale cooling expansion, with Lumen and Zayo as upstream carriers. It is a third-party facility description, not a commitment to any customer, but it shows the shape of the answer you should be looking for.

Three questions to put to any provider:

1. **What kW will you contractually deliver to a single rack today?** Not the peak the building can hit somewhere, the number written into your order.
2. **Is liquid cooling in service, or planned?** Direct-to-chip and chilled-water loops are being designed into facilities now; whether yours has them running changes what hardware you can deploy this quarter.
3. **What are the power and water ceilings for expansion?** A facility at 2 MW with utility commitments and large-bore water lines can grow with you; one at its limit cannot.

If your next deployment is a GPU rack rather than a web tier, these three answers matter more than the price per square foot. 👉 [Ask SpinServers about colocation and GPU deployments](https://bit.ly/Spinservers) with your density target included in the request.

## Why you won't find a colo price list, and what a quote should itemize

Colocation is usually billed on space plus power, and providers route pricing through a quote or consultation rather than publishing rates. Public facility pages list service forms (suites, cages, private and partial cabinets, individual servers, remote hands, bare metal, cloud servers) and then send you to a quote form, because the price depends on your power draw, term and cross-connect count.

That makes the quote itself the thing to scrutinize. Require these lines in writing:

| Line item | What to require |
| --- | --- |
| Space | Unit type (full cabinet, half cabinet, cage, suite), minimum term, and what the footprint includes |
| Power | Contracted kW versus burst kW, price per additional kW, and whether billing follows the contracted figure or metered draw at the PDU |
| Cooling ceiling | kW per rack included before a surcharge applies, and the surcharge above it |
| Cross-connects | Price per cross-connect, per carrier, and whether you can add carriers later without penalty |
| Remote hands | Hourly rate, minimum increments, after-hours rate, what tasks are in scope |
| SLA | Availability percentage, credit formula, response times, notice period for planned maintenance |
| Exit | Notice period, decommissioning fees, and who owns the cross-connects and cabling you paid for |

The exit line is the one most buyers skip. Moving out of a colo is slow and awkward, which is exactly why the terms are worth negotiating before you sign rather than after.

## Cost, risk, and who shouldn't colo at all

The financial case rests on sharing: cooling, power, security and connectivity are operated for many tenants at once, which removes utility and HVAC planning from your budget and lets your IT team work on systems instead of facilities. Downtime is the other side of that ledger. Across Global 2000 companies, downtime costs an estimated $400 billion a year, roughly $9,000 per minute, which is the number that justifies paying for redundancy rather than hoping.

The honest downsides:

- **TCO still needs calculating.** Colo removes capital spending, not all operating cost. Add power, cross-connects, remote hands and your own staff time before comparing against cloud.
- **Switching is painful.** Vendor lock-in in colo comes from logistics, not contracts; moving racks between buildings takes planning and downtime.
- **Security stays yours.** The provider secures the building. Your audits, vulnerability assessments and application-layer controls remain your responsibility.
- **Remote management is a real constraint.** Without staff near the facility, every failed disk becomes a remote-hands ticket.
- **Distance costs latency.** Close to users is faster; check how long your team needs to reach the site during a disruption.
- **Energy and environmental footprint** are increasingly part of procurement review, and the facility's power source is part of your number.

And the case against colo entirely: if you need one or two servers, colo is the wrong product. Renting space, power and cooling to run two boxes costs more than renting the boxes. SpinServers publishes monthly pricing for dedicated servers starting at $79, deployable in Dallas or Silicon Valley, which is the cheaper route below roughly a rack of demand. The same company takes colocation, GPU and custom deployment requirements through its team, and its Dallas facility is described as meeting HIPAA, PCI and SOC 2 standards. 👉 [Compare SpinServers' dedicated server options and ask about colo](https://bit.ly/Spinservers).

## Choosing, in one pass

One to five racks with variable growth, and you want your own carrier mix: retail colo, quoted per cabinet with power increments spelled out. Private suite or a large block of power: wholesale, where the unit rate drops because the commitment rises. Hardware that has to sit close to a cloud region: hybrid, and the direct-connect question becomes the deciding one. A handful of servers, no cage: dedicated hosting, not colo.

Before signing, confirm three things: whether power is billed on contracted kW or metered draw, whether the liquid cooling you were shown is already serving customers or still on a roadmap, and what the exit terms actually say. Those three answers separate a quote you can budget from one you'll be renegotiating in eighteen months.

👉 [Send SpinServers your colo requirement and get a written quote](https://bit.ly/Spinservers).
