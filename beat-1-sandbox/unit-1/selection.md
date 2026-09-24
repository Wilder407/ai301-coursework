# Unit 1 — Issue Selection

Path: `beat-1-sandbox/unit-1/selection.md`

Record of the issue carried into Unit 2, and of the evaluation runs that produced
`eval-run.txt`. This file is graded at the path above; a copy kept anywhere else in
the repository is not read.

Complete every labelled field below. Each is graded on its own; content placed under the
wrong label is not graded.

---

## Selected issue

**Issue link**

[Keyword search raises ZeroDivisionError when the index is empty #68](https://github.com/codepath/pathreview-ai301-fa26-s3/issues/68)

**Verdict output**

Both required checks (current-issue, unclaimed) pass for all three — the repo pushed 7 days ago and isn't archived, and there are zero PRs in the whole repo, so no formal claims exist; the student "I'll take this" comments on #68 and #60 are exr the Path Review house rule. All three verdicts: accept.

Ranking (fit: Python-focused, wants root-cause tracing practice, prefers scope):

    #68 (ZeroDivisionError in KeywordSearcher.index) — single file + test, self-contained, and tracing why an empty corpus breaks the third-party BM25Okapi call is exactly the root-cause exercise the profile asks for. Now let me get the comments for issues 68 and 60, and check for linked PRs on all three.

Ran 6 shell commands

Both required checks (current-issue, unclaimed) pass for all three — the repo pushed 7 days ago and isn't archived, and there are zero PRs in the whole repo, so no formal claims exist; the student "I'll take this" comments on #68 and #60 are explicitly non-blocking under the Path Review house rule. All three verdicts: accept.

Ranking (fit: Python-focused, wants root-cause tracing practice, prefers scope):

    #68 (ZeroDivisionError in KeywordSearcher.index) — single file + test,ng why an empty corpus breaks the third-party BM25Okapi call is exactlythe root-cause exercise the profile asks for.
    #60 (FaithfulnessChecker text:None crash) — equally well-scoped with at the root cause is basically handed to you in the issue body, so lesstracing practice.
    #15 (session state not cleared between reviews) — touches three files across orchestrator/memory, longer estimated effort (3–4h), more of a design call about what to clear and when — still fine, but a bigger bite than the other two.

Maintainer responsiveness (preferred, doesn't gate verdict) graded weak for all three: a sample of 15 recent issues turned up only 2 maintainer comments total, both the maintainer closing their own issues rather than replying to students — bed.
```
[ { "item": "codepath/pathreview-ai301-fa26-s3#68", "checks": [ {"name": "current-issue", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:50:20Z (7 days before capture), archived: false"}, {"name": "unclaimed", "grade": "pass", "evidence": "0 PRs exist in m comment (acordero4852) is non-blocking per Path Review house rule"}, {"name": "issue-spec", "grade": "pass", "evidence": "one proposed change (guard index() against empty corpus), named files, named test to un-xfail, effort estimate 2-4h, no discussion thread"}, {"name": "maintainer-responsive", "grade": "fail", "evidence": "sample of 15 recently updated issues found only 2 maintainer comments total (both on the maintainer's own closed issues), below the 5-comment threshold"} ], "verdict": "accept" }, { "item": "codepath/pathreview-ai301-fa26-s3#60", "checks": [ {"name": "current-issue", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:50:20Z (7 days before capture), archived: false"}, {"name": "unclaimed", "grade": "pass", "evidence": "0 PRs exist in m comment (pkmaster21) is non-blocking per Path Review house rule"}, {"name": "issue-spec", "grade": "pass", "evidence": "one proposed change with literal repro snippet and named failing test (test_none_context_chunk_text), no discussion thread"}, {"name": "maintainer-responsive", "grade": "fail", "evidence": "same repo-wide sample: only 2 maintainer comments across 15 recent issues, below the 5-comment threshold"} ], "verdict": "accept" }, { "item": "codepath/pathreview-ai301-fa26-s3#15", "checks": [ {"name": "current-issue", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:50:20Z (7 days before capture), archived: false"}, {"name": "unclaimed", "grade": "pass", "evidence": "0 PRs exist in is issue"}, {"name": "issue-spec", "grade": "pass", "evidence": "one proposed change (clear ContextManager cache and delete session state on run start), 3 named files, effort estimate 3-4h, no discussion thread"}, {"name": "maintainer-responsive", "grade": "fail", "evidence": "same repo-wide sample: only 2 maintainer comments across 15 recent issues, below the 5-comment threshold"} ], "verdict": "accept" } ]
```


**The verdict must record `accept` for this issue.** Choose an issue your own skill
accepts. If your skill rejects every candidate you try, that is a signal about your
rubric rather than about the issues: revise it and re-run — retries are unlimited and a
partial re-run costs about $0.20 — or run the skill on different candidates. Output
recording `reject` for the issue you chose earns no credit for this field.

```
{ "item": "codepath/pathreview-ai301-fa26-s3#68", "checks": [ {"name": "current-issue", "grade": "pass", "evidence": "repo pushed_at 2026-09-16T21:50:20Z (7 days before capture), archived: false"}, {"name": "unclaimed", "grade": "pass", "evidence": "0 PRs exist in m comment (acordero4852) is non-blocking per Path Review house rule"}, {"name": "issue-spec", "grade": "pass", "evidence": "one proposed change (guard index() against empty corpus), named files, named test to un-xfail, effort estimate 2-4h, no discussion thread"}, {"name": "maintainer-responsive", "grade": "fail", "evidence": "sample of 15 recently updated issues found only 2 maintainer comments total (both on the maintainer's own closed issues), below the 5-comment threshold"} ], "verdict": "accept" }
```

---

## Eval iterations

**Run history**

My previous run history was not saved given that I closed the terminal. However, original run was 13/20, then 8/20, then 14/20, then back to 11/20. Some of the steps that I took to work increase the score was to adjust my scope check from preferred to required. I also did this with the maintainer check. Using the gold-standard labels JSON file as a refernce was a good place to identify what was causing the human rating. I then adjusted and added additional instances to the requirements. 

**Issue analysis**

Issue-09 was gold-standard "accept" but my skill rated it as "reject". The notes were: "failed: unclaimed, issue-spec (preferred), maintainer-responsive (preferred)". This likely was rejected because I didn't create a verification step that included maintainer asking for additional insight into an older, stagnant repo. So, on the surface, it appears to be older than 1 yr which my skill rejected.


**Check rationale**

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
|issue-spec| one proposed change with spec in repo-facts | one proposed change with clear, stated scope and criterion for acceptance; not a tracking issue; no abandoned PRs; less than 1 year design discussion in comments; not a new feature request | preferred |

This check is written to ensure that a good-first-issue would be selected. This includes a clear scope and crteria for acceptance. Also, this elimates issues that are feature requests which sometimes can be misplaced as issues. The note about less than 1 year of design discussion is important because even at that length, ths bug is likely closer to a feature than a bug. 

**Trade-offs**

When I updated the check to include spec/criterion for approval, the check didn't pass small repos that has legitimate issues. Because these repos only had a few issues (or one) and didn't have a template-like layout, these were not seen as having sufficient information. 

---

## Selection rationale

**Selection rationale**

1. I think that this issue is a good fit based on that it's a straightforward bug. There are two files that are impacted and the skill checker noted that the this would be a good start. 
2. The verdict correctly identified that this issue is reproducible and will meet my desire to work through codebase tracing. 
3. I believe that I will be able to meet the objective without any major unforseen challenges. I have worked through more complicated bugs which have prepared me for this. 

---

Related paths: `eval-run.txt` in this directory; your skill's files in
`tools/issue-select/`.
