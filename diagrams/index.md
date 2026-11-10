# Diagrams

This section contains mechanical, electrical, control, and data centre topology diagrams. These visuals support system understanding, workflow clarity, and engineering documentation.

Diagrams in this directory are used to illustrate equipment layouts, power paths, cooling configurations, and control system relationships.

## Included Content

- Mechanical Diagrams — HVAC layouts, chiller loops, airflow paths  
- Electrical Single-Line Diagrams — distribution paths, UPS, switchgear  
- Data Centre Topology — rack layouts, cooling zones, power redundancy  
- Control System Blocks — BMS components, sensor networks, control loops

                    REAL WORLD
                        │
                        ▼
                  OBSERVATION
                        │
                        ▼
               SITE NOTES COMPILER
                        │
                        ▼
             PATTERN / CASE EXTRACTION
                        │
                        ▼
          ENGINEERING KNOWLEDGE ARCHITECTURE
                        │
              ┌─────────┴─────────┐
              ▼                   ▼
         AI RETRIEVAL         HUMAN VERIFY
              │                   │
              └─────────┬─────────┘
                        ▼
                  CAPABILITY
                        │
                        ▼
              EVIDENCE / ARTIFACT
                        │
                        ▼
             READINESS / DECISION

                    PROFESSIONAL CAPABILITY
                            ▲
                            │
                   Evidence / Readiness
                            │
                            │
                 Operational Experience
                      ┌─────┴─────┐
                      │  Equinix  │
                      └─────┬─────┘
                            │
                     Site Observation
                            │
                 ┌──────────┴──────────┐
                 │                     │
          Knowledge Architecture   Communication OS
                 │                     │
                 └──────────┬──────────┘
                            │
                       AI + Systems
                         Thinking

![image](https://raw.githubusercontent.com/luckyaisystems/building-systems-data-centre-dev/refs/heads/main/image%20(1).jpg)

  # Data Centre Power Path — Step-by-Step Guide

*Based on hand-drawn single-line diagram (Side A / Side R dual-feed topology)*

---

## 1. The High Voltage Entry

- On the far left, **13.8 kV** (very high voltage) comes from the utility grid.
- It hits the **TX (Transformer)**, which steps it down to **600 V** so the building's equipment can safely use it.

## 2. The Main Switch Board (MSB) & ATS — Side A

- This 600 V power runs directly into the **MSB (Main Switch Board)**.
- Look closely at the sketch: the **ATS is built right into this board**.
- If utility power dies, a **G (Generator)** wired to this board fires up to take over Side A.

## 3. The Immediate Safety Net (UPS)

- Right below the ATS is the **UPS (Uninterruptible Power Supply)** with its **batt (battery)** pack.
- When the power clicks over from utility to generator, that **10-to-30 second gap** happens.
- The UPS batteries instantly hold up the power so the servers downstairs don't even blink.

## 4. The Backup Shield — Side R (Reserve)

- Now look at the right side of the drawing labeled **R**. This is your **+1 Redundancy** block.
- It has its own **MSB**, its own backup **Generator**, and its own completely separate **UPS** system.
- This entire right side exists just in case the left side (Side A) completely fails or needs to be turned off for maintenance.

## 5. The Instant Lifesaver: The ASTS

- At the bottom, both the Side A UPS and the Side R UPS plug into a box labeled **ASTS (Static Transfer Switch)**.
- An **ATS** uses mechanical parts and takes a moment to switch. An **ASTS** uses electronics and switches instantly — literally in **milliseconds**.
- If something goes wrong on the A-side UPS, the ASTS snaps the load over to the R-side UPS so fast that the downstream **Load** (your customer servers) never loses power, and the local batteries don't get drained out or damaged.

---

## Quick Reference Table

| Component | Full Name | Role |
|---|---|---|
| TX | Transformer | Steps 13.8 kV utility power down to 600 V |
| MSB | Main Switch Board | Distributes 600 V power; houses the ATS |
| ATS | Automatic Transfer Switch | Mechanically switches utility → generator (seconds) |
| G | Generator | Backup power source during utility outage |
| UPS | Uninterruptible Power Supply | Batteries bridge the 10–30 s generator start gap |
| ASTS | Static Transfer Switch | Electronic switching between UPS A and UPS R (milliseconds) |
| A | Side A (Primary) | Main power path |
| R | Side R (Reserve) | Fully independent +1 redundant path |
| Load | Customer servers | The equipment that must never lose power |

## Power Flow Summary

```
Utility Grid (13.8 kV)
        │
       TX ──► 600 V
        │
     MSB + ATS ◄── Generator (G)      [Side A]
        │
       UPS + Battery
        │────────────┐
                    ASTS ◄── Side R: MSB + G + UPS (full redundancy)
                     │
                   Load (customer servers)
```

# ATS vs. ASTS: Where Each Sits and Why

**System:** Electrical power distribution
**Source:** Whiteboard walkthrough with a lead engineer during my internship, plus my own follow-up reasoning
**Note type:** Personal learning note. Generic concepts only, no site-specific or confidential details.

## The two devices

| Device | How it switches | Where it sits (in the drawing) |
| --- | --- | --- |
| **ATS** (automatic transfer switch) | Mechanically | Upstream, inside the MSB, where the utility and generator sources come together |
| **ASTS** (automatic static transfer switch) | Electronically (solid-state), much faster | Downstream, after the UPS, just before the load |

## The power path I was shown

- Two independent paths (**A side** and **R side**), each with its own source, MSB and UPS.
- The **ATS** handles source transfer upstream, inside each path.
- The **ASTS** is where the two paths merge into one feed to the load.

## Why the ASTS sits downstream

- It is the **last point where there are still two independent sources**. After it there is only one path, so there is nothing left to switch between. That is more precise than "the last point before the customer."
- The farther downstream it sits, the more failures it covers. A failure on either path upstream can be handled by one fast electronic transfer, so the load never sees the interruption.

## Tradeoff to remember

The ASTS is itself a single point in the path. This is why devices like it are built simply and are typically paired with a **bypass**, so they can be serviced without dropping the load. *(My understanding from general reasoning, not something the engineer said. Worth verifying.)*

## Key shift for me

> Before: recognizing individual components. Now: seeing how components connect into one system, and asking *why* each one sits where it does.

## Related ideas

- Failure categories from my *System-Failure-Audit*: **input, decision, execution**. A transfer switch failing to transfer is an execution failure.
- Reliability is not only equipment and backups. It also depends on **maintenance, monitoring, procedures and people**.


