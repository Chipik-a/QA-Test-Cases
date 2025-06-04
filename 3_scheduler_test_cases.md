# Test Cases: Advanced Scheduler

## Test Case 1: Scheduler skips scanning on battery when *** setting is enabled

**Preconditions:**
- *** setting is set to `true`.
- Device is running on battery power.

**Steps:**
1. Ensure the device is not connected to power.
2. Run the command: `*** --sched`.
3. Check the exit status and logs.

**Expected Result:**
- Scanning does not start.
- Exit status is `"skipped"`.
- Logs contain a message explaining the skip due to battery power and cosmos setting.

---

## Test Case 2: Scheduler runs scanning on power supply with *** setting enabled

**Preconditions:**
- *** setting is set to `true`.
- Device is connected to power.

**Steps:**
1. Connect the device to a power source.
2. Run the command: `*** --sched`.
3. Verify scanning starts.

**Expected Result:**
- Scanning starts normally.
- Exit status is not `"skipped"`.

---

## Test Case 3: Scheduler runs scanning on battery with *** setting disabled

**Preconditions:**
- *** setting is set to `false`.
- Device is running on battery power.

**Steps:**
1. Ensure the device is running on battery.
2. Run the command: `*** --sched`.
3. Verify scanning starts.

**Expected Result:**
- Scanning starts normally.
- Exit status is not `"skipped"`.
