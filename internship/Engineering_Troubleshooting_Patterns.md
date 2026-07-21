# Engineering Troubleshooting Patterns

A reusable framework for documenting troubleshooting events across systems, workflows, and operational environments.  
Each entry follows a consistent structure to support long‑term pattern recognition and engineering growth.

---

## Template

### Problem
Describe the issue observed.

### Symptoms
List measurable indicators or alarms.

### Evidence Gathered
Record logs, observations, conversations, or system behavior.

### Incorrect Hypotheses Eliminated
Document causes that were tested and ruled out.

### Root Cause
State the confirmed cause clearly.

### Solution
Actions taken to resolve the issue.

### Verification
How the fix was validated.

### Lessons Learned
Key insights for future troubleshooting.

---

## Example Entry — GitHub Pages Deployment Failure

### Problem
GitHub Pages site failed to deploy and remained stuck in queued state.

### Symptoms
- Repeated deployment failures  
- Long queue times  
- 404 on published site  

### Evidence Gathered
- `_config.yml` parsed correctly  
- `index.md` existed  
- Pages source set to `main`  
- Build logs showed early termination  

### Incorrect Hypotheses Eliminated
- Markdown errors  
- Folder structure issues  
- Missing homepage  

### Root Cause
Missing GitHub Pages workflow (`pages.yml`).

### Solution
Added explicit workflow to `.github/workflows/pages.yml`.

### Verification
Deployment succeeded immediately; site published correctly.

### Lessons Learned
Explicit workflows can bypass silent deployment failures.
