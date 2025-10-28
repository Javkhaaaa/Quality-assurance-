# MeetingPlanner - Unit Testing Lab

Run with Ant:

1. Compile
   - `ant compile`
2. Run unit tests (JUnit 4)
   - `ant test`
   - Reports under `build/reports`
3. Generate Javadoc
   - `ant javadoc`
   - Output under `build/javadoc`

Notes:
- Tests cover success and failure cases for `Calendar`, `Person`, `Room`, and `Organization`.
- Known bug documented by test: adding a meeting that fully encloses an existing meeting is not detected as conflict by `Calendar.addMeeting`.
