# Critical Facilities — Daily Log

**Rule for every entry:** separate what I observed from what I understood and what needs verification.

## Template

```markdown
## YYYY-MM-DD

**Studied / observed (facts):**
-

**What I understood (my interpretation):**
-

**Needs verification:**
-

**Questions for a senior engineer:**
-

**One-sentence summary (practice conciseness):**

**Restudy tomorrow:**
-
```

---

## 2026-11-20

### Studied / observed (facts)
- Reviewed the power path from utility to rack, redundancy terms, cooling heat chain, controls and safety, and procedures.
- Watched cooling and solenoid/actuator videos on The Engineering Mindset.

### What I understood (my interpretation)
- UPS sits in series, and the STS is the fast electronic switch near the load.
- PUE is total facility power divided by IT power, and cooling efficiency moves it most.

### Needs verification
- How my site's redundant block is configured (+1 vs 2N).

### Questions for a senior engineer
- Which resources would you recommend for UPS topologies?

### One-sentence summary (practice conciseness)
Power flows utility → transformer → switchgear → MSB/ATS → UPS → PDU → rack, with an STS near the load for source redundancy.

### Restudy tomorrow
- UPS topologies
- Cooling heat chain
- PUE drivers

---

## 2026-11-18

### Systems Observed
Clean Agent Suppression System Test (Novec agent), including:
- Releasing control panel
- Solenoid actuators on agent tanks
- VESDA (Very Early Smoke Detection Apparatus) pipes
- Cross-zone countdown timers
- Manual release/abort switches
- Discharge warning strobes
- Releasing circuits

### Activities Observed
Technicians performed a live functional test of the suppression system:
- Isolated the panel in bypass mode and physically unthreaded the solenoids from the Novec tanks so the test could run safely without agent discharge
- Tested VESDA pipes with smoke spray for transport time
- Blocked VESDA airflow to confirm trouble signals
- Verified cross-zone countdown timers
- Checked manual release/abort switches and discharge warning strobes
- Confirmed the releasing circuit fired the solenoid plungers on time
- Reset and re-armed the system after the test

### My Role
Shadowing/escorting — observed the functional test and discussed the operation of the solenoid release chain with the technician.

### Technical Understanding
A solenoid is an electromagnetic actuator. When its coil is energized, the resulting magnetic field moves a ferromagnetic plunger.

In a clean-agent suppression system, that mechanical movement operates a release mechanism or pilot valve, depending on the equipment design. The distinction is:

- The solenoid actuator converts an electrical command into mechanical movement.
- The release mechanism or valve assembly controls the discharge path.
- The stored pressure of the suppression agent provides the energy that drives the agent through the distribution system.

Therefore, the solenoid does not generate the pressure that expels the agent — it initiates the mechanism that allows the pressurized agent to discharge. That's why observing the disconnected solenoid actuate during the functional test was meaningful: it demonstrated the electrical-to-mechanical portion of the release chain without requiring an actual agent discharge. The exact arrangement varies by manufacturer and system design.

### Verification Source
- Interpretation reviewed verbally with the technician performing the test.
- General operating principles cross-referenced with an educational explanation of electromagnetic solenoids.

### Ladder Mapping
Fire alarm and life-safety systems; suppression system testing and inspection procedures; understanding actuator and release mechanisms.

### Lessons Learned
- The division of roles in a suppression release chain: solenoid = electrical-to-mechanical conversion; valve assembly = discharge path control; stored agent pressure = the force behind discharge.
- A functional test can validate portions of the release chain (solenoid actuation, timers, strobes, abort switches) without discharging agent.

### Open Questions
- How does the bypass mode interact with the building fire alarm system during the test window?
- What differences exist between manufacturers in solenoid/release mechanism arrangement?
