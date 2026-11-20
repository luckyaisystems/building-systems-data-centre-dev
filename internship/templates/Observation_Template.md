# Microsoft CET Intern: Interview Quick Reference

**Mon Nov 23, 4:00 PM** | Manager + Senior Critical Environment Tech
*General study notes only. No proprietary or site-specific info.*

**Pace rule:** one sentence first, then stop. Add detail only if asked.

---

## 1. 30-second intro

> I'm a Building Systems Engineering Technician student at Seneca and an intern at Equinix, where I've spent the past few months learning critical facilities operations across electrical, mechanical, and life safety systems. I like the procedure-driven, safety-first nature of the work, and I'm looking to build more hands-on skills in an environment like Microsoft's.

## 2. Why this role / why Microsoft

- Safety and procedure-driven work (EOPs, MOPs, SOPs) is how I like to work.
- Scale: 100+ datacenters, a mature operations culture to learn from.
- Structured growth: training, certifications, and rotations (from the posting).
- It's the direct next step toward critical facilities operations.

---

## 3. Posting keyword -> my one-liner

| They said | My answer |
|---|---|
| Monitoring and inspection | I observe equipment and spot abnormal conditions, then verify before concluding anything |
| EOP / MOP / SOP | I follow the written procedure, and I don't improvise |
| Documentation and escalation | I separate facts, interpretation, and what needs verification |
| CMMS and work orders | Tracks assets and maintenance. I log accurately and clearly |
| Incident timelines / RCA | Gather facts in order, then look for the cause, then actions |
| Communicate with stakeholders | I adapt to the reader: short, clear, direct |
| Learn and grow | I study on my own (Seneca, self-study) and ask questions |

---

## 4. Quick technical answers (one sentence each)

| Topic | Answer |
|---|---|
| Power path (illustrative) | Utility, transformer (step-down), switchgear, MSB/ATS (utility or generator), UPS, PDU, rack. Placement of each element varies by design |
| UPS | Keeps conditioned, uninterrupted power flowing to critical loads; its stored energy bridges upstream interruptions until another source is available |
| ATS vs STS | ATS: mechanical switch between utility and generator. STS: electronic (SCR) switch between two sources, much faster. Not every design has an external STS |
| Generator | Longer-duration backup source; typically starts and accepts load in about 10 s, depending on design |
| N / N+1 / 2N | N = needed to carry load. +1 = one spare. 2N = two complete independent systems |
| Concurrently maintainable | Planned maintenance on capacity and distribution components can happen without interrupting the critical load, within the design's defined scope |
| Cooling chain (chilled-water example) | Server air, CRAH coil, chilled water, chiller, condenser water, cooling tower, outdoors. Air-cooled and DX designs reject heat differently |
| CRAC vs CRAH | CRAC: direct-expansion refrigerant cycle. CRAH: chilled-water coil |
| Containment | Stops hot and cold air mixing. Less recirculation, better efficiency |
| PUE | Total facility energy / IT energy over a defined period (power ratios for instant readings). 1.0 is ideal, lower is better |
| BMS vs EPMS | BMS: mechanical/environmental monitoring. EPMS: electrical monitoring |
| Alarms | An alarm is a prompt, not a conclusion. Verify before acting |
| LOTO | Lock and tag isolation points so equipment can't be re-energized during work |
| Arc flash | Fault through air: intense heat and blast. PPE, labels, boundaries, de-energize when possible |
| MOP / SOP / EOP | MOP: planned task plan with rollback. SOP: routine work. EOP: emergencies |
| Change management | Plan, risk-assess, approve, schedule, and document every change to a live environment |
| CMMS | Computerized maintenance management system |

---

## 5. Scenario answers

**Framework: Stop, Assess, Verify, Escalate, Document**

**"Unexpected UPS alarm on the BMS. What do you do?"**
> I'd check what the alarm says and whether other alarms are active, without changing anything. I'd notify my supervisor right away, verify the status in person if it's safe and authorized, and follow the alarm response procedure. I wouldn't reset or operate equipment outside my authorization. I'd document the timeline and help with follow-up.

**"Why does a data centre need a UPS if it has generators?"**
> The UPS maintains uninterrupted power during an upstream disturbance, including the time generators need to start and stabilize. Generators provide longer-duration backup, while the UPS bridges the transition and helps maintain power quality.

(Then stop. Expand only if asked about runtime, topology, or bypass.)

**"You notice something unsafe."**
> Stop, keep myself and others clear, report it to my supervisor immediately, and document what I saw.

**"You're unsure how to do a task."**
> I stop and ask, because guessing is the unsafe option. Then I follow the written procedure.

**"Tell me about a mistake."**
> [Fill in a real example: what happened, what I did, what I changed.]

---

## 6. My stories (60-90 seconds each)

**Format:** Situation, what I did, what I learned.

1. **Supervised fire suppression test**
   - Observed a supervised functional test.
   - Didn't understand the release sequence at first.
   - Studied how solenoids work electromagnetically and discussed it with the technician.
   - Learned: electrical actuation vs. stored-pressure discharge, and to verify my understanding.

2. **Fact vs. interpretation vs. verify**
   - In documentation I separate what technicians did, what I understood, and what still needed checking.
   - Result: [fill in: what became easier or clearer].

3. **Adapting to the reader**
   - [Fill in: a real example of changing how I communicated for a supervisor or engineer.]

---

## 7. Honest-limits phrases (use freely)

- "My experience is observation and supervised learning, not hands-on operation."
- "I'd verify with my supervisor before touching anything."
- "I can't share site specifics, but the principle is..."
- Understanding a system is not the same as being authorized to operate it. Use the first phrase when asked about my level of responsibility, not before every answer.
- "I'm not sure, but here's how I'd find out."

---

## 8. Availability / school (fill in before the call)

- Start: January 2027, 6 months, fully on-site: **[confirmed? yes/no]**
- School plan during the term: **[fill in]**
- Shifts / weekends / holidays: **[fill in]**
- Equinix internship ends Nov 27.

---

## 9. Questions to ask them

1. What does the first month look like for an intern, and how do interns progress from observing to assisting with MOPs?
2. What separates interns who do well in this role from those who struggle?

## 10. Close

> Thank you, I'm genuinely interested in this role. What are the next steps?
