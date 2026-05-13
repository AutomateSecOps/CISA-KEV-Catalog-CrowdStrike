## Patching What Matters: A Tines Story for CISA KEV Hosts in CrowdStrike

*Posted on AutomateSecOps by Tom Power*

---

## The Problem with Prioritization

Security teams drown in vulnerability data. 

Tens of thousands of CVE IDs are published every year, and your CrowdStrike Spotlight dashboard is probably no different — a long tail of findings ranked by CVSS score, severity label, or whatever your scanner vendor decided mattered most this quarter.

But CVSS scores don't tell you what's being weaponized right now. 
The CISA Known Exploited Vulnerabilities (KEV) catalog does.

The KEV is a curated list maintained by the Cybersecurity and Infrastructure Security Agency of CVE IDs that have confirmed, active exploitation in the wild. 

It's not theoretical risk. 

It's real-world attack surface. 

And if a host in your environment has an open vulnerability that's on that list, that's where your patching energy should go first.

The problem? Cross-referencing the CISA KEV against your CrowdStrike Spotlight data every week is a manual chore. This Tines story eliminates that chore.

---

## What This Story Does

The **CISA-KEV-CrowdStrike-Hosts** story runs on a schedule and produces a weekly CSV report of every CrowdStrike-managed host in your environment that has an open vulnerability matching a CVE ID on the CISA KEV catalog. It enriches each finding with ransomware campaign association data, internet exposure status, asset criticality, CISA remediation due dates, and more — then writes each result to a Tines Record and emails the full report as a CSV attachment.

The output gives your team a clear, actionable list: these specific hosts, these specific CVEs, patch by this date.

I hope you find this useful.

Happy Building!

Tom

This post was drafted with AI assistance based on the author's story design and technical notes.

## Tines Documenation
- [Tines AI Automatic Mode Event Transformation](https://www.tines.com/docs/actions/types/event-transformation/automatic//)
- [Tines WHERE Function](https://www.tines.com/docs/formulas/functions/where/)
- [Tines OBJECT Function](https://www.tines.com/docs/formulas/functions/object/)
- [Tines OBJECTS TO CSV Function](https://www.tines.com/docs/formulas/functions/objects-to-csv/)
- [Tines Append Element to Resource](https://www.tines.com/api/resources/append-element/)
- [Tines Resources](https://www.tines.com/docs/resources/)
- [Tines Records](https://www.tines.com/docs/records/)
- [Tines Community Edition](https://www.tines.com/pricing/)
