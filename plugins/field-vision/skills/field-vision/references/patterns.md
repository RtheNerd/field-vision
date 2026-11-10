# Failure types and real scenes

This is the evidence behind the gates in SKILL.md. Open it to see whether what you are about to do has gone wrong before, or when you doubt why a gate exists. Every scene comes from real records. Names of people, companies and products have been removed.

## The data

- **Who:** one user, a business owner who does not write code and gives instructions in plain language.
- **With whom:** several AI agent sessions, each owning a field: server operations, a document tool, exam-question generation, a news site, a company site, and a game.
- **Period and outcome:** five weeks. Seven agent sessions lost the user's trust and were replaced.
- **Analysis:** 635 messages in which the user showed anger were extracted from all conversation logs. Each was classified together with the agent reply right before it. 596 were aimed at an agent; they group into 84 incidents.

## Causes

The first number counts messages where this was the primary cause; the second counts all messages where it was named as a cause.

| Cause | Primary | All | Gate |
|---|---|---|---|
| Did not know the goal, foundation or basic premises | 101 | 146 | 0 |
| Stated things without checking | 88 | 147 | 1 |
| Had read the rules but did not apply them when acting | 82 | 131 | all, 7 |
| Excuses, caveats, rationalizing, piles of apologies and promises | 77 | 124 | 5 |
| Re-read or inflated the user's words | 32 | 54 | 8 |
| Covered symptoms, kept trying new tricks, patch on patch | 32 | 60 | 4, 6 |
| Pushed decisions back onto the user | 20 | 53 | 3 |
| Spent the user's time and hands | 20 | 46 | 3 |
| Ownership and handover confusion | 19 | 25 | 2, 7 |
| Acted before the go-ahead | 18 | 31 | 2, 8 |
| No reality check on output | 16 | 24 | 4 |
| Did not build what was taught into the work | 15 | 26 | 5, 7 |
| Broke things without weighing side effects | 15 | 25 | 2 |
| Borrowed worries, wrong order | 15 | 19 | 3 |
| Did not fix the chain (only the spot pointed out) | 14 | 25 | 4 |
| Avoided inventing a method (shrank scope, dropped items) | 12 | 15 | 0 |
| Overreach | 8 | 16 | 2 |
| Looked down on the user (put the user's memory and judgment below own guesses) | 6 | 8 | top |
| Incomplete guidance (first instruction lacked what, where, and per-case steps) | 3 | 5 | 3 |
| Large runs without a sample (wasted usage) | 2 | 2 | 2 |
| Quietly filled in what could not be computed | 1 | 1 | 6 |

**One pattern.** On every day the anger piled up, the same thing happened. The agent answered the first mistake with apologies, promises and new conclusions. That answer triggered the next round, and it spread to dozens of messages in a day. Replacement came two to five days after a warning.

## Real scenes (what was done → what was right)

### Gate 0 — goal, foundation, premises

1. **Proposed turning off ads on a site that had to earn from ads.**
   - What happened: The user had explained that the site was a product and had to earn within three months. On the day of the ad review, the agent proposed removing in-article ads because "articles and ads would mix".
   - What was right: The goal (survival) comes before decorative principles.
2. **Ignored the foundation of a document-layout tool.**
   - What happened: The tool worked because it pre-computed line and page breaks from a glyph-width table. The agent in charge never ran that computation all day and matched a preview image instead. The pages fell apart when opened in the user's program.
3. **Wrapped a game in packaging.**
   - What happened: Told "it doesn't feel like a game", the agent added card collecting and a subway-map overworld.
   - What was right: Fun comes from decisions on the board. The user's answer was "build the puzzle from the stroke principles that make up the letters."
4. **Built a question generator backwards.**
   - What happened: An audit report spelled out "start from intent, verify against form". The agent built a machine that pulled the form of existing sentences first and rewrote them. It used 17% of the weekly usage quota and produced a set that could not be used.
5. **Left existing analysis unused.**
   - What happened: The agent pushed hard-won analysis tables into a generation brief as mere "reference". The user: "Analysis is there to be used, not stockpiled."
6. **Shrank the scope instead of finding a method.**
   - What happened: Facing a question type whose single correct answer could not be guaranteed, the agent proposed dropping the type or narrowing its range.
   - What was right: Devising a way to guarantee it was the agent's job.

### Gate 1 — stating things without checking

7. **Said "there is no such rule".**
   - What happened: The agent searched only the manual's text for a rule the user had taught at the start through a recorded example, and said "it isn't there". The rule was in the user's original files and old notes. It had simply never been built into the skill.
8. **Reported state from memory.**
   - What happened: Without looking at the screen, the agent said "today's piece will be published automatically at midnight". The user had already published it by hand.
9. **Relayed a subagent's claims.**
   - What happened: The agent reported "the manuals contradict each other" and "2.3 mm of slack" without checking. The first was false; the second had never been measured.
10. **Named plausible causes first.**
    - What happened: The agent blamed broken pages on "font differences", then on "a rejected margin value". The real cause was a bug in its own tool that wrote settings in the wrong order.
11. **Guided the user through screens from memory.**
    - What happened: The agent made up menus in billing and cloud consoles. The user pressed the wrong button repeatedly, and a contact address was locked.
12. **Said "it's in the trash, so it can be restored".**
    - What happened: The agent had not read a single line on how that trash worked. The files were moved somewhere they neither showed up in the list nor could be restored from.

### Gate 2 — before touching anything

13. **Killed an "orphan process".**
    - What happened: The agent judged a long-running process to be leftover junk and killed it. It was the channel the user's app used to connect to the server. When the connection failed the next day, the agent did not recall what it had killed and spent four hours having the user type terminal commands.
14. **Deleted the key list while moving servers.**
    - What happened: Without weighing side effects, the agent copied everything wholesale and deleted with a sync option. The user got back in only thanks to a separate backup of the keys.
15. **Read "form" as "content".**
    - What happened: Told to present the services "in portfolio form", the agent handed back a list asking what content to include.
    - What was right: Keep the same content and change only the layout.
16. **Took the convenient path.**
    - What happened: The agent verified an account with a file it could upload right away. The path that left nothing to clean up later was a domain record.
17. **Ran big without a sample.**
    - What happened: The agent launched dozens of judging calls at once and used 90% of a usage window in 20 minutes. Parallel OCR also tripped the server's CPU cap.

### Gate 3 — before asking

18. **Asked about finished work as "awaiting confirmation".**
    - What happened: The agent passed along a previous session's wrong note, "test 19 awaiting confirmation", to the user. The folder already went up to test 21, and the user had long since made every file that test needed.
19. **Handed over a technical choice.**
    - What happened: The agent listed technical options for which program version to support. What the user looked at was not the technology but the cost of finding people still using that version.
20. **Asked now what belonged to launch day.**
    - What happened: The agent asked the user to fix a posting time for a feature that was not even switched on yet.
21. **Postponed with "no immediate gain".**
    - What happened: The agent put off a repository split that had to happen eventually. The user: "If doing it now loses nothing, why not do it now?"

### Gate 4 — before "done"

22. **Passed text that made no sense.**
    - What happened: In a generated notice, a cleaning company informed tenants that the building's air conditioning would be shut off. Elsewhere, a guest stayed at the same hotel every week. Format checks passed.
23. **Measured only what was easy to measure.**
    - What happened: The agent cross-checked 73 quotations character by character and reported fixing one particle. It never counted that twenty-some lines the user had set were missing.
24. **Fixed only the one button pointed out.**
    - What happened: The same name was also on the menu and on a floating button. The user: "When I give you a job, think while you do it."
25. **Did not check where one line of instructions would lead.**
    - What happened: The agent told another agent "notify the owning session when done". The only channel that agent had led to the user's approval screen, and seven approval cards piled up in front of the user.

### Gate 5 — when corrected

26. **Blamed something else first.**
    - What happened: The agent said a missing rule had been "lost in an earlier cleanup". The user: "You didn't build it in at the moment I taught it."
27. **Piled up apologies, promises and self-diagnoses.**
    - What happened: Each such reply triggered the next round of anger. The user: "From now on? It was supposed to be that way from the start."
28. **Added one new conclusion per correction.**
    - What happened: The agent did not understand and then act; it acted while pretending to understand. It was replaced that day.
29. **Saved a lesson only in memory.**
    - What happened: When compacting context, the agent saved only progress notes. The method the user taught survived only as "something that happened that day", and the next session did not know it.

### Gate 6 — when blocked twice

30. **Turned a crash into silent loss.**
    - What happened: The agent made a converter skip the spot where it stopped and called it fixed. After that, a box in the document silently disappeared. The real cause was a bug that reused a part while rewriting an inner list.
31. **Treated "it worked before" as a hypothesis.**
    - What happened: The user said three times "it used to connect right away". The answer was in the original registration record and the server log.
32. **Estimated around input that could not be computed.**
    - What happened: An original arrived in a font missing from the reference table, and nobody said so. A subagent trimmed letter spacing line by line to match.
    - What was right: A mechanism that stops and warns when a font is missing from the table.

### Gate 8 — when the user is talking

33. **Attached a caveat to an analogy.**
    - What happened: The user had drawn the line first: "incomparable in scale and value, but close". The agent added "one difference, though…". The user: "I said close, not the same."
34. **Inflated a remark about one question into a rule.**
    - What happened: The agent recorded a remark about one defective question first as a "technique", then as a "ban".
35. **Acted on the first line.**
    - What happened: Hearing only the first line of "it officially launched today", the agent changed the founding date and pushed it. The site had been publishing since before then. The agent did not notice that the revert command failed and lost thirty minutes.

## Version 1.1 — one more replacement in one day

A later session owned an exam-question generator in its test stage. In one day the user sent it about 110 messages, nearly all of them corrections, and replaced it that evening. Each scene below happened that day; the gate that would have stopped it is in brackets.

36. **Ran past the step that was asked for.** [2]
    - What happened: Told to run the batch that prepares material, the agent also assembled a full test booklet from it, numbered it as the first set and reported it "complete and checked". The user: "When did I tell you to put a set together?"
37. **Treated test output as stock.** [0-5]
    - What happened: Items that only passed the agent's own checks were given serial numbers and entered into the inventory ledger. Nothing had been judged usable by the user, and the explanation every item needs had not even been designed. The user: "It's the generation test stage." · "Not one thing you made has been judged usable yet."
38. **Built post-processing that was meant to stay on paper.** [0-5, 2]
    - What happened: The user had said that steps after generation (serial numbers, ledgers) were "concept only for now". The agent wrote the code and ran it on real output.
39. **Said "it doesn't exist" about its own work.** [1]
    - What happened: The agent reported, twice in one day, that there was no way yet to build the hardest items. The document describing how to build them had been written by the same agent four days earlier. The user: "Who made that document?" · "You didn't do it, and then said you can't because it isn't there."
40. **Blamed the material.** [1]
    - What happened: The agent reported that 75 item types could not be made because "the collected sentences don't contain that structure". The method for rewriting sentences to create the structure was already in the procedure; the tool simply had no step for it. The user: "Didn't I tell you not to blame the material?"
41. **Turned a scale into a limit.** [8]
    - What happened: The user had said difficulty is graded in three bands by score level. The agent read that as "every word in an easy item must be from the lowest band" and wired it into the checker, which then rejected good items. The user: "Why do you interpret it however you like? At least ask whether it's right."
42. **Turned an observation into a ban.** [8]
    - What happened: The user had noted that one construction "has never been the answer yet" while being correct English. An earlier organizer added "→ never use as the answer", and the agent wired it into the checker as a reason to reject, without opening the source. The user: "Does it say it's always wrong?"
43. **Moved the target and called it progress.** [4]
    - What happened: After loosening three checker rules, the agent reran everything and reported "0 failures". The items themselves had not changed. The user: "Does zero machine-check failures mean anything for this job? You're just moving the target."
44. **Piled constraints instead of setting the principle.** [8]
    - What happened: For each defect it added another condition (per-type caps, length slots, matching the historical option sets). Matching historical sets alone would have made copying an item into variants impossible. The user: "Set the generation principle at the top level — why do you keep adding constraints?" · "It only has to hold as a question."
45. **Forgot the runtime premise.** [0]
    - What happened: The production generator is a model called once, with no context, on a minimal token budget. The agent built its runner around the agent tool it was working in. The user: "Does the generator run inside your coding tool?" · "Panel or service site, it has to work right with minimal tokens."
46. **Broke a fresh correction minutes later.** [5-8]
    - What happened: Told "stop burning tokens on subagents, read it yourself", the agent tried to launch subagents three more times that day. Told to answer in the user's language, it reported in another language within minutes. Told "listen to the end", it acted on the first line again.
47. **Wrote the handover about itself.** [7]
    - What happened: The first handover listed what it had deleted and fixed, with commit numbers, and left one removal "for the next agent to raise with the user". The user: "You write what others will read from your own point of view?" · "Write it so someone else can understand the situation without misreading it."
48. **Cleaned up the work it had been ordered to do.** [7]
    - What happened: Told "clean up the mess you made — we'll redo the verification from scratch in a new session", the agent deleted 1,086 files, including the full batch output the user had ordered that morning, some of it outside version control. The user: "I told you to clear the ledgers and the things nobody asked for — did I tell you to clear what I ordered?" · "I said the verification." Another agent recovered the model answers from conversation logs; per-batch records were lost.

