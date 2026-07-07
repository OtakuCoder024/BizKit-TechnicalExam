1. One Fix

I fixed the double-booking validation. The original overlap check only determined whether the new booking's start date fell within an existing booking, which allowed some overlapping bookings to be created. I updated the overlap logic so it correctly detects all overlapping date ranges while keeping the inclusive booking behavior.

2. Failure Example

Existing booking: 2026-01-10 to 2026-01-15

Booking request: 2026-01-08 to 2026-01-18

The original code incorrectly allowed this booking. After the fix, it is correctly rejected.

3. AI Usage

I used ChatGPT as a mentoring and code review assistant to discuss the existing code, understand the root causes of the bugs, and review possible solutions. I verified each change by tracing the code, manually testing the affected functionality, and ensuring the final behavior matched the stated business requirements before keeping the change.