# Testing and Verification

## Test Environment

- **IDE:** CODESYS V3.5 SP22 Patch 2
- **Controller:** CODESYS Control Win V3 x64 simulation
- **Language:** Ladder Diagram (LD)

## 1. Startup Sequence

| Test ID | Test | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| ST-01 | Press and release Start briefly. | Startup sequence remains active after the button is released. | Pending | Not tested |
| ST-02 | Observe the startup warning interval. | Siren remains active during the intended five-second interval. | Pending | Not tested |
| ST-03 | Observe timer completion. | Siren turns off and the motor command activates when all required conditions are satisfied. | Pending | Not tested |
| ST-04 | Activate the simulated emergency-stop input during startup. | Motor command is disabled without waiting for the startup timer. | Pending | Not tested |

## 2. Normal Stop Sequence

| Test ID | Test | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| NS-01 | Press and release Stop briefly. | Normal-stop sequence continues after the button is released. | Pending | Not tested |
| NS-02 | Observe the stop warning interval. | Siren follows the intended warning behaviour during the delay. | Pending | Not tested |
| NS-03 | Observe stop-timer completion. | Motor command turns off after the configured delay. | Pending | Not tested |
| NS-04 | Press Start while the stop sequence is active. | System follows the explicitly designed behaviour for this situation. | Pending | Not tested |
| NS-05 | Activate the simulated emergency-stop input during the stop delay. | Motor command is disabled without waiting for the normal-stop timer. | Pending | Not tested |

## 3. Issues and Troubleshooting

| Issue | Observed Behaviour | Investigation | Fix | Retest Result |
|---|---|---|---|---|
| Add an entry when an unexpected behaviour occurs. | Record what happened. | Record what you checked. | Record the change made, if any. | Record the observed retest result. |

## 4. Testing Notes

- Record actual observations, not assumed results.
- Mark a test as Passed only after verifying the expected behaviour.
- Record failures and retest after making changes.
- Include screenshots when they provide useful evidence of the program's state.