Item	Notes
Issue	Aqara P2 presence sensor stopped updating state
Effect	Kitchen lights did not turn on automatically
Description of issue	Sensor showed as connected but state never changed
Checks performed	Power confirmed, hub online, automation logic unchanged, logs reviewed
Cause	Sensor had a stale / incomplete reset and remained as a ghost entity
Resolution	Full reset of sensor and Aqara hub, device re-paired cleanly
Verification	Walked into room, sensor state updated, automation triggered correctly
Follow-up	Fully remove device before re-pairing in future
