# Agency Content Planner with Duplicate Prevention

Run the daily content planner for a digital agency handling several client brands at once. The planner has four sources of truth that must always agree: the Drive folder stage, the client sheet row, the posting calendar event and the live social profile. When they disagree, the live profile wins and the other three get corrected.

## Keep the planner current

- Work from two supply sources per brand, mixed: the brand's Scheduled folder and its approved-not-posted backlog. Never let approved creatives sit idle while a slot stays empty.

- Treat the posting calendar as a file-location tracker. Every event's description carries brand, SKU, title, format, time, status and the file's current Drive folder, and gets updated at every real stage move, never speculatively.

- Run the daily rhythm: inventory and plan the next two days in the evening, schedule tomorrow's posts after that, and keep at least a two-day buffer of scheduled posts at all times.

- Give festival posts priority at the early-morning festival slot so none is missed. Never place two posts of the same brand at the same time.

- Mark a calendar event as scheduled in the scheduler tool only after the scheduling actually succeeded, with a visible marker on the title and the scheduled date and time in the description.

## Prevent duplicate posts

This is the core of the skill. Every duplicate so far came from a creative that was treated as fresh when it had already been posted, or from a file that stayed in a scheduling folder after going live.

- Before scheduling any creative, check three records: the brand's live profile grid for the same creative, the sheet row's posting status and live URL column, and the file's current folder. If any one shows it already posted, do not schedule it.

- Treat backlog items as unproven, not as approved-not-posted. A backlog file is only safe to schedule after its creative has been checked against the brand's live profile and found absent. File names that look like live-post exports are a warning sign, not a guarantee.

- Compare creatives by what is on screen, not by file name alone: headline text, scene, product and caption. Two files with different names can be the same creative, and one scene can carry two different headlines, so open the creative or its frames before judging.

- Verify the SKU prefix matches the brand page it will post to, and check the creative's end card carries only that brand's logo, website and phone. A mismatch means skip and flag, never post.

- Never schedule anything still in client review, no matter how old it is. Approval is read from the approval portal, not assumed from age or from the sheet.

- After a post goes live, move its file out of every scheduling source the same day (see the lifecycle below). A file left in Scheduled or backlog will be picked up again and posted twice.

## Move files through the lifecycle

- Move files, never copy them. A media file and its caption file travel together and live in exactly one stage folder at a time: intake, ready, in review, scheduled, posted, plus rejection and change-request folders for items that leave the flow.

- Use each brand's own folders. Never park one brand's files in another brand's folder, even temporarily.

- Verify after every move that the file is gone from the previous folder. A move that cannot be verified is reported as not done.

- When a client requests changes, the new version continues the circle from review onward, and the superseded version moves to the change-request folder so it can never be scheduled by mistake.

## Close the circle after posting

- Accept a post as posted only with a verified live URL from the brand's own profile. No live URL means no posted status anywhere.

- Complete all four updates for every live post: file and caption moved to the Posted folder, sheet row set to Posted with the post date and the live URL in the URL column, calendar event status set to Posted with the same URL, and the scheduler checked so nothing remains queued for that creative.

- Close the circle proactively as posts go live. Do not wait to be asked, and do not batch it into a later day.

- If a duplicate is discovered live, never delete a live post yourself. Report it with both permalinks and let the user decide; correct the records to match whichever copy survives.

## Audit on a schedule

- Compare the scheduler's queued posts against the calendar and the live profiles regularly. Flag any queued item whose creative is already live, any calendar event whose file is not in the folder it claims, and any sheet row marked Posted without a live URL.

- Treat a sheet row marked Posted with an empty live URL column as unverified. Do not reschedule that creative until its live status is proven either way.

- Report audit results as exceptions only: the duplicates, mismatches and unverified rows, each with its permalink or file link as proof.

## Available connectors

- [Google Drive](/opt/hatch/connectors/google_drive/CONNECTOR.md) for the stage folders that hold every creative and caption file.

- [Google Calendar](/opt/hatch/connectors/google_calendar/CONNECTOR.md) for the posting calendar that tracks each file's stage and slot.

- [Instagram](/opt/hatch/connectors/instagram/CONNECTOR.md) for reading brand profiles when verifying what is already live.

- [Facebook](/opt/hatch/connectors/facebook_cli/CONNECTOR.md) for the brand pages the scheduler posts to.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Websites

- [Meta Business Suite](https://business.facebook.com/) for scheduling and checking queued posts across the brand pages. Carry the exact SKU, title, slot time and the separate Facebook and Instagram captions into the task, and verify each queued post against the calendar before leaving.

- Your client approval portal for approval status. Use admin URLs only, and read the status from the deliverable itself before treating anything as approved.

## Alternatives for better results

- When the live profile cannot be read far enough back to prove a creative is new, hold the item out of the schedule and flag it instead of guessing. An empty slot is cheaper than a duplicate post.

- When several items need the same verification, batch them into one profile scan per brand rather than one visit per item.
