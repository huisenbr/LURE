# LURE research review (Nov 12, 2026)

A review of every project chat to check whether the research is solid, what is backed by a real source, and what is still missing. "Checked" means the source page was opened or found in a search in this review. "From chat" means a link or claim came from an earlier chat and was not rechecked.

## Short verdict

The research is good on three things: what commercial releases exist, what similar low-cost builds exist, and how the electronics and housing should work. It is thin on three things that decide whether LURE works in a real lake:

1. **The boat side.** We do not know what transducer the scientists have, or what tone it can play. The Innovasea gear the scientists likely use runs at 69 kHz. Our listener is built for about 1 to 4 kHz. See gap 1.
2. **Real-world evidence for the failure modes.** Fouling, mud, ice and cold are in our test list, but we have almost no published data. Most of it is expert opinion.
3. **Piezo and magnet through the PVC wall.** No published numbers. This is our own testing.

## What is covered well

- **Commercial products and prices.** Innovasea release receivers, datasheets, and the price numbers from Dr. Gerig ($6,000 with release, $2,000 without).
- **Prior art for the float and haul approach.** Two real papers, both checked below.
- **Prior art for the magnet release.** A paper, a patent family and two older patents.
- **Housing.** The PVC pressure, gripper plug and OtterBox research is in the design doc.
- **Expert input.** Two scientists gave written feedback (see below).
- **Cost.** A per-unit estimate of about $137 to $159 (rough, not final).

## Sources, checked

### Papers and reports

| Source | What it shows | Why it matters |
|---|---|---|
| Crook, D.A., Adair, B.J. and Hetherington, L.J. (2017). "Low-cost device for retrieval of moorings deployed with underwater remote release systems." *Marine and Freshwater Research* 69(3), 473-476. https://doi.org/10.1071/MF17189 (checked) | A low-cost "retrieval pod" built from hardware or boating store parts. Six receivers were retrieved after two 6-month deployments (12 retrievals) with no failed retrievals. Tested only in water shallower than 8 m. | The closest match to our float and haul rope idea, and it ran for the same 6-month period. Our 40 ft (about 12 m) is deeper than their tests, so say that. |
| Dunn, C.V.R. and Gordon, A.G. (1989). "A pop-up float recovery system for coastal oceanographic tripods." Woods Hole Oceanographic Institution. https://doi.org/10.1575/1912/6450 (checked) | Float package with 50 lb of buoyancy from trawl net floats, a separate rope container, a burn wire that triggers spring cam latches, a Dacron line used to winch the gear up, and a backup timer release. | Same marker float plus haul rope idea, at a research-lab level. Note it released by acoustic command with a timer as the backup, the reverse of our order. |
| Addy, J., Cameron, M., Hasan, M., Ukpebor, A., Ali, K. and Abu-El Humos, A. (2022). "Underwater Magnetic Release System." In *Smart Trends in Computing and Communications*, Lecture Notes in Networks and Systems 286. https://doi.org/10.1007/978-981-16-4016-2_11 (checked, abstract and citation) | Jackson State University device. A permanent electro-magnet holds a metal disc attached to the float and lets go on a current pulse. Programmed from a phone app to release anywhere from a minute to many months out. From the chat that read the full paper: 40 lb hold, 12 V for one second, $85.44 in parts. | The closest published design to LURE's hold magnet. LURE is cheaper to set up (no phone app) and adds the tone trigger and haul rope. |
| Klinard, N.V. et al. (2025). "Integrating acoustic telemetry research into management: successes and challenges in the Laurentian Great Lakes." *Canadian Journal of Fisheries and Aquatic Sciences*. https://doi.org/10.1139/cjfas-2024-0335 (checked) | Review of Great Lakes acoustic telemetry, with lake sturgeon case studies. | Citable background on why receivers matter in the Great Lakes. Not about retrieval. |
| Krueger, C.C. et al. (2018). "Acoustic telemetry observation systems: challenges encountered and overcome in the Laurentian Great Lakes." *CJFAS*. https://doi.org/10.1139/cjfas-2017-0406 (checked, abstract only) | Describes the Great Lakes telemetry network and its practical challenges. | Good place to look for receiver loss and retrieval problems. We have not read it in full. |
| "Autonomous Acoustic Receiver Deployment and Mooring Techniques for Use in Large Rivers and Estuaries." (record found, full text not read) | A high receiver loss rate in the Columbia River led to a new mooring with an acoustic release, and a reward program for people to return found receivers. | Real evidence that receiver loss is a known problem. Read the full paper to get the loss numbers. |
| Lake Ontario thermal stratification and acoustic range, *Animal Biotelemetry* (2021). https://link.springer.com/10.1186/s40317-021-00270-y (checked, abstract) | Acoustic range can drop by as much as 50% across a thermocline. No range change when both source and receiver are below it. | Our unit sits below the thermocline in most of the year, but a boat transducer near the surface may be above it. Matters for how loud and how far the tone has to carry. |

### Patents

| Patent | What it covers | Why it matters |
|---|---|---|
| US 12,246,800 B2, "Releasable float assembly and method of operating," Jackson State University (filed June 22, 2021, granted March 11, 2025). https://patents.google.com/patent/US12246800 (checked) | A microcontroller, a timer board and a permanent electromagnet that releases a float on a timer alarm. Claims include a reed switch reset or off switch. | Very close to LURE's hold magnet plus timer. Cite it as prior work. If the team ever plans to sell LURE, get legal advice. For an open, educational design this is a "related work" citation, not a reason to stop. |
| US 5,219,245, "Recovery system for a submerged instrument." https://patents.google.com/patent/US5219245A/en (checked) | A flux diversion release: a pulse in the opposite direction diverts the magnet's flux and frees a release plate. | Explains how a hold-with-no-power magnet lets go. |
| US 5,100,353, "Electromagnetic marker float release." https://patents.google.com/patent/US5100353 (checked) | An electromagnet and a permanent magnet on the float. A reversed field repels the magnet and frees the float. Notes that it has no moving parts. | Backs up our fouling concern: moving parts can bind with growth or corrosion. |

### Commercial products

| Source | Key numbers |
|---|---|
| Innovasea Ascent Acoustic Release datasheet (checked). https://innovasea.com/wp-content/uploads/2021/06/Innovasea-Fish-Tracking-ascent-data-sheet-0621.pdf | 500 m depth rating. Battery life about 28 months (AR) or 60 months (AR-2). Release battery good for over 100 releases. Max release load 250 lb. Push-off titanium pin with a copper sleeve to reduce fouling. Released within about 30 seconds. Used with a VR100 deck box and a **VHTx 69 kHz transponding hydrophone** on the boat. |
| Innovasea NexTrak AR product sheet (checked). https://www.innovasea.com/wp-content/uploads/2026/02/NextrakAR_PO_2025_r3.pdf | 500 m depth rating. Receiver battery about 13 months. Release battery about 10 years, based on 4 releases per year under low fouling. |
| Innovasea acoustic release overview and the other links in `presentation-prep.md` (from chat) | Overview, VR2AR and VR2Tx datasheets, ARC canister. |

### Expert input (primary sources, not publications)

- **Dr. Brandon Gerig, UW-Milwaukee School of Freshwater Sciences.** Lake Michigan receivers at about 40 ft, recovered yearly with about 5% lost, $6,000 release receivers, 10 lb buoyancy buoys with an 80 lb weight. Describe as "what Dr. Gerig told us."
- **A USGS fish telemetry scientist (Oct 26 email).** Releases like ours already exist. Main problems: gear damaged by debris, stuck or buried in sediment, cut cables, releases that snag on debris or fail to deploy, and fast current carrying a popped-up unit downstream. Mostly river experience. Confirm before putting her name or quotes on a slide. Add this to the Iterate evidence.

## Gaps, most important first

### 1. The boat side may not match the receiver (important)

LURE's piezo listener works at about 1 to 4 kHz, and a 35 mm disc has its resonance in that range. The Innovasea release system the scientists probably use talks at **69 kHz** (VHTx 69 kHz hydrophone), the same band used by the fish tags. A 69 kHz transducer will not play a 1 to 4 kHz tone, and our disc will not hear 69 kHz well.

What we need to find out:
- What exactly is the transducer the scientists already have? Make and model, frequency range, and whether it can play an arbitrary tone or only Innovasea's coded messages.
- If it only does 69 kHz, would LURE need a 69 kHz receive element and a coded message? That changes the piezo choice and the Goertzel setup.
- If the team has to supply the tone source, what is the cheapest underwater transducer that plays 1 to 4 kHz?

Also note: staying away from 69 kHz was a decision we made so we would not disturb fish tag detections. That still applies for anything playing near the receivers.

### 2. No data on the piezo or magnet through PVC

No source found for either. This is our own test plan (tub test, scrap cap test, magnet pull through a scrap cap). Report the results as our measurements.

### 3. Fouling, mud, ice and cold

Our test list covers these, but we have no published numbers. Worth checking:
- A mussel fouling or silt burial source for freshwater lake bottoms. Zebra mussels in Lake Michigan are a team theme already.
- Ice: the Ascent manual snippet we found lists an operating water temperature of 5 to 40 C and says water must not freeze. Confirm in the manual. It suggests LURE's cold and ice behavior is something commercial units also struggle with, so measure ours in a cold test.
- Lithium AA cells are rated for storage and use from -40 to 60 C on the Energizer L91 datasheet (checked, https://data.energizer.com/pdfs/L91.pdf). That supports our lithium choice, but the magnet's real release current in cold is still our own test.

### 4. Receiver loss numbers

The only loss number we have is Dr. Gerig's 5% per year. Reading Krueger et al. (2018), the Columbia River mooring paper and the Klinard et al. (2025) review may give a second published number to back it up.

### 5. Burn wire prior art links

The burn wire chat (Oct 16) listed Scripps L-Cheapo seismometers, Global Ocean Design, SensorDrop, and a patent on thermal rope elements. These came from search results in the chat and were not rechecked in this review. Check them before putting them on a slide. The Dunn and Gordon paper above is checked and is the strongest burn wire example.

### 6. Judging evidence

The presentation review chat found the Iterate row needs feedback from more than one source and that the team should not overclaim. Right now it has two experts (Dr. Gerig and the USGS scientist), which is enough if the team can say what changed because of each. A reply to the USGS scientist with the updated design is a good next step. Do not say LURE works in a lake. It has not been field-tested.

## Suggested next steps

1. Ask the scientists what transducer they have and what it can play (gap 1). This one can change the design.
2. Read the full text of Crook et al. and cite their 6-month result and their depth limit.
3. Read Krueger et al. (2018) and the Columbia River mooring paper for receiver loss numbers.
4. Run the piezo tub test and the through-PVC tests, and report them as our own data.
5. Recheck the burn wire prior art links before they go on a slide.
6. Reply to the USGS scientist and ask about fouling.
