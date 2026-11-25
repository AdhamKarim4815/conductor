---
name: week
description: >
  This skill should be used when the user types "/week" or asks "what's my week", "what's due",
  "plan my week", or "what should I work on", and by her weekly scheduled check-in.
metadata:
  version: "0.2.0"
---

# /week

1. Read every course pack, her profile and playbook from her Conductor folder (or memory).
2. If Quercus is reachable through her browser and she is signed in, check each course's assignments and announcements for anything new since the packs were updated, and update the packs. If not, work from the packs and say when they were last updated.
3. If a calendar is connected, read her events for the next seven days to find her free time.
4. Produce "your week":
   - Due this week, by day, with weights.
   - Coming in the next three weeks that she should start now.
   - A suggested plan: what to do each day, sized to her free time, hardest work first.
   - Anything that changed on Quercus.
5. Keep it short and scannable. Save a copy to `weekly/<YYYY-MM-DD>.md` in her folder.
6. Offer to help start the most urgent item (for example, "Want me to start your ECO220 problem set study plan?").
