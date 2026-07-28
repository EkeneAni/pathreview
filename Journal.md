## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/156

**Issue title:** README scorer test fixture is too short for its own word-count assertion

**Tier:** [X] Tier 1  [ ] Tier 2  [ ] Tier 3

**Problem summary:**
From what I understand, the README is expected to be long enough for the test to work but the one used in the sample is too short, hence the test will fail, even though the scoring logic is correct

**Branch name:** test/156-readme_scorer_test_fixture_too_short

**Setup confirmation:** [X] App runs locally at localhost:5173

**Cohort ledger:** [X] Issue added to cohort ledger

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** Put in as a screenshot in the root of the project.

**Reproduction summary:**
At first, I couldn't get the test to run, but then I used Chat to give help me. I then ran `pip install structlog` and then I was able to reproduce the error by running `pytest tests/unit/test_readme_scorer.py::TestReadmeScorer::test_readme_with_all_quality_signals -q`. 

The test failed because the sample README used in the fixture has a `word_count` of 51, while the test asserts `word_count > 100`, causing a single failing assertion even though the scorer returns a valid overall score.

I observed that there were 22 tests that passed and then 1 test that failed which was the test on the word count of the 

**Reproduction summary:**
[1–2 sentences: How did you reproduce the issue? What did you observe?]

**PLAN.md link:** [link to PLAN.md in your fork]

**Walkthrough video (recommended):** [link to your Loom video, ≤2 min — recommended, not graded]

**Blockers or open questions:**
[Anything you're still uncertain about going into Week 9, or leave blank]

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** readme_bug_reproduction.png (root of repository) or 
https://github.com/EkeneAni/pathreview/blob/test/156-readme_scorer_test_fixture_too_short/readme_bug_reproduction.png


**PLAN.md link:** It's in the root of the directory

**Walkthrough video (recommended):**
None

**Blockers or open questions:**
- Nothing at the moment