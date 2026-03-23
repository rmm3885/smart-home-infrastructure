# Aqara P2 Presence Sensor Incident

## Problem
Aqara P2 presence sensor stopped updating state despite appearing connected.

## Impact
Kitchen lighting automation failed to trigger, reducing system reliability.

## Symptoms
- Sensor showed as connected in Home Assistant
- No state changes detected on movement
- Automation logic remained unchanged but did not execute

## Investigation
- Confirmed device power was stable  
- Verified Aqara hub was online and responsive  
- Reviewed automation configuration (no changes)  
- Checked logs for state updates and device activity  

## Root Cause
Sensor had a stale / incomplete reset, resulting in a “ghost entity” that appeared connected but did not report state changes.

## Resolution
- Performed full reset of sensor and Aqara hub  
- Removed existing entity completely  
- Re-paired device as a fresh integration  

## Verification
- Sensor state updated correctly upon movement  
- Kitchen lighting automation triggered as expected  

## Follow-up
Ensure devices are fully removed before re-pairing to avoid ghost entities and inconsistent state behaviour.
