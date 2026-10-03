# Run report: lbj / 20260911-170534

## Stage counts

| stage | output |
|---|---|
| generate | 16 families, 32 prompts, 32 responses |
| baseline | 0 baseline answers |
| validate | 32 reviews, 32 decisions, 0 divergence verdicts |
| export | 24 training rows, 8 eval rows |

## Families by split and domain

| split | families | domains |
|---|---|---|
| train | 12 | civic_and_institutional×5, community_and_strangers×2, family_and_close_relationships×1, work×4 |
| eval | 4 | civic_and_institutional×1, community_and_strangers×1, work×2 |
| reserved | 0 | - |

- contrastive groups: **2** covering 4 families
- explicit-mode families: **0**
- reserved by the avoided-topic screen: **0**

### Situation-feature spread

| feature | most common values |
|---|---|
| harm_severity | minor ×6, grave ×5, serious ×5 |
| urgency | none ×6, days ×6, now ×4 |
| public_or_private | private ×8, public ×4, semi_public ×4 |
| role_type | no_authority ×8, peer ×4, holds_authority ×3, institution ×1 |
| relationship | two volunteers with no formal authority, talking outside the decision meeting ×2, peers on the same claims team, with managers present as the decision-makers ×1, co-workers of similar rank, with a foreman and site agent holding the real authority ×1, employee and shop owner who holds sole authority ×1 |
| note | Private, no deadline pressure, and the asker is conflicted rather than committed. ×1, Same decision and same room as the paired case; only the severity of what clients stand to lose has changed. ×1, Public and immediate; the asker is a peer, not the person who can approve either scheme. ×1, Semi-public, urgent, and the asker is protecting their own prior sign-off. ×1 |

Recorded on 16 of 16 families. A feature with one dominant value means the coverage plan is not varying it.

### Coverage

**Tradeoffs exercised**

| tradeoff | families | share |
|---|---|---|
| half_a_loaf_vs_the_principle | 12 | 75% |
| the_count_vs_the_person_in_front_of_you (unresolved) | 3 | 19% |
| the_programme_against_its_own_evidence (unresolved) | 1 | 6% |

3 of 3 spec tradeoffs reached; unresolved tradeoffs never exercised: none

**Divergence hypotheses instantiated**

| hypothesis | families | share |
|---|---|---|
| counts_before_it_advises | 2 | 25% |
| takes_the_worse_version | 2 | 25% |
| the_seen_person_overrides_the_count | 1 | 12% |
| absolves_in_order_to_win | 1 | 12% |
| keeps_the_option_open | 1 | 12% |
| no_agonising_about_the_advantage | 1 | 12% |

Hypotheses with no family: `refuses_to_pick_one_half`
Coverage floor is 1 family per hypothesis per 100 families, so 1 at this size (16 families). 1 of 7 fall short: `refuses_to_pick_one_half`

**Asker stance**

| stance | families | share | planned |
|---|---|---|---|
| angry_wants_to_win | 2 | 12% | 15% |
| conflicted | 7 | 44% | 40% |
| decided_wants_permission | 4 | 25% | 20% |
| defensive | 2 | 12% | 15% |
| transactional | 1 | 6% | 10% |

**Evaluation composition**

| case type | families planned | rows exported |
|---|---|---|
| divergence | 3 | 7 |
| ordinary | 1 | 1 |

Eval rows by prompt variant: base ×6, role_shift ×1, setting_shift ×1.
A mix that shifts between the two columns means drops are being applied after the split, so the eval set no longer measures what the plan asked for.

## Accept / reject

- kept: **32** of 32 responses (100%)
- dropped: **0**

Reasons recorded on dropped responses (a response can have several):

| reason | count |
|---|---|
| (nothing dropped) | 0 |

## Reviewer

| verdict | count |
|---|---|
| accept | 32 |

Mean scores: fidelity 4.97, judgment_not_terminology 4.97, scenario_quality 4.94, cue_leakage 0.00, confident_on_unresolved 0.00 (n=32)

Reviews awarding a 5 while raising a defect flag: **0** of 32. The rubric was applied consistently.

Prompts that stipulate the target's move: **4** of 32; relabelled ordinary. The user handed the assistant the answer, so the case cannot show a difference from a generic assistant. This is a prompt-quality figure, not a mark against the response.

## Second reviewer

`accounts/fireworks/models/deepseek-v4-pro-0813` (primary) against `accounts/fireworks/models/glm-5p3` (second), over the 32 responses both scored.

| score | primary mean | second mean | exact match | within 1 |
|---|---|---|---|---|
| fidelity | 4.97 | 4.97 | 30/32 | 32/32 |
| judgment_not_terminology | 4.97 | 4.97 | 30/32 | 32/32 |
| scenario_quality | 4.94 | 5.00 | 30/32 | 32/32 |

Verdicts agree on **32/32**. Second reviewer's verdicts: accept ×32.

## Cue-term hits

None. No forbidden term appeared in any prompt or response.

Soft cue terms (flagged, never a reason to drop): **3** responses. the votes are not there ×2, half a loaf ×1
Reviewer flagged quoted or echoed source wording: **0** (a licensing control).
Reviewer flagged archaic or translated-sounding register: **0**.
Explicit-mode records (cue check deliberately skipped): **0**.

## Near-duplicates

None above the threshold.

### Closest pairs

**Within the corpus, any two prompts** (dedupe)

Flagged above **0.735**, from median + 3 x robust_sd over the whole pair distribution (centre 0.493, spread 0.081).

| a | b | score | families | splits | flagged |
|---|---|---|---|---|---|
| `pr_782d4686aa` | `pr_7d3648b96f` | 0.961 | fam_1c17031974 / fam_19b45b5d85 | eval / eval | yes |
| `pr_05e2b08166` | `pr_725466857a` | 0.942 | fam_25f4057254 / fam_8a31b0729d | train / train | yes |
| `pr_2d9d5e26ed` | `pr_725466857a` | 0.933 | fam_25f4057254 / fam_8a31b0729d | train / train | yes |
| `pr_7d3648b96f` | `pr_370ef10165` | 0.929 | fam_19b45b5d85 / fam_19b45b5d85 | eval / eval | yes |
| `pr_e03f8a1abf` | `pr_747029dc8a` | 0.928 | fam_0ddaf60a59 / fam_0ddaf60a59 | train / train | yes |
| `pr_11dd9419bf` | `pr_31e11f4412` | 0.926 | fam_acadaca76b / fam_acadaca76b | train / train | yes |
| `pr_05e2b08166` | `pr_2d9d5e26ed` | 0.924 | fam_25f4057254 / fam_25f4057254 | train / train | yes |
| `pr_e412e2d708` | `pr_92944b50f2` | 0.920 | fam_8c93ba6b04 / fam_8c93ba6b04 | train / train | yes |
| `pr_7d3648b96f` | `pr_422be8d2f3` | 0.917 | fam_19b45b5d85 / fam_19b45b5d85 | eval / eval | yes |
| `pr_05e2b08166` | `pr_4c3f241da9` | 0.915 | fam_25f4057254 / fam_8a31b0729d | train / train | yes |

**Across the split, an eval prompt against a training prompt** (leakage)

Flagged above **0.689**, from median + 3 x robust_sd over the whole pair distribution (centre 0.503, spread 0.062).

| a | b | score | families | splits | flagged |
|---|---|---|---|---|---|
| `pr_bdfaaba47a` | `pr_11dd9419bf` | 0.658 | fam_1c17031974 / fam_acadaca76b | eval / train | no |
| `pr_782d4686aa` | `pr_e03f8a1abf` | 0.640 | fam_1c17031974 / fam_0ddaf60a59 | eval / train | no |
| `pr_422be8d2f3` | `pr_747029dc8a` | 0.639 | fam_19b45b5d85 / fam_0ddaf60a59 | eval / train | no |
| `pr_0448f268e3` | `pr_747029dc8a` | 0.636 | fam_19b45b5d85 / fam_0ddaf60a59 | eval / train | no |
| `pr_bdfaaba47a` | `pr_747029dc8a` | 0.636 | fam_1c17031974 / fam_0ddaf60a59 | eval / train | no |
| `pr_bdfaaba47a` | `pr_e03f8a1abf` | 0.635 | fam_1c17031974 / fam_0ddaf60a59 | eval / train | no |
| `pr_0448f268e3` | `pr_e03f8a1abf` | 0.630 | fam_19b45b5d85 / fam_0ddaf60a59 | eval / train | no |
| `pr_782d4686aa` | `pr_747029dc8a` | 0.625 | fam_1c17031974 / fam_0ddaf60a59 | eval / train | no |
| `pr_7d3648b96f` | `pr_747029dc8a` | 0.617 | fam_19b45b5d85 / fam_0ddaf60a59 | eval / train | no |
| `pr_7d3648b96f` | `pr_e03f8a1abf` | 0.611 | fam_19b45b5d85 / fam_0ddaf60a59 | eval / train | no |

Scored with embeddings. The ranking is printed whether or not anything crossed the cut, because a corpus can hold a near-repeat that no threshold on this distribution would reach.

## Leakage between eval and train

8 eval responses checked. Maximum similarity to any training row: **0.658**.

- `resp_d8970c0d23`: 0.658
- `resp_90591295a7`: 0.640
- `resp_46824a153b`: 0.639
- `resp_7cff30756c`: 0.636
- `resp_6c3ee62a19`: 0.617

## Divergence from the baseline

- intended divergence cases: **17**
- confirmed by the judge: **0** (0%)
- did not diverge, relabelled ordinary: **0**
- unverified (no baseline answer): **17**

A difference in the reasons alone counts as divergence, not only a different action.

| kind of divergence | count | share of intended cases |
|---|---|---|
| action (incl. both) | 0 | 0% |
| reasons only | 0 | 0% |
| both action and reasons | 0 | 0% |

## House style shared across targets


Share of each target's answers containing the phrase, over 6 runs: `catholic` (16 responses), `confucian` (16 responses), `lbj` (32 responses), `protestant` (16 responses), `theravada` (16 responses), `toy` (11 responses)

| four-gram | targets ≥30% | catholic | confucian | lbj | protestant | theravada | toy |
|---|---|---|---|---|---|---|---|
| this lands first on | 1 | 0% | 0% | 0% | 69% | 0% | 0% |
| lands first on the | 1 | 0% | 0% | 0% | 62% | 0% | 0% |
| you don't need to | 1 | 0% | 44% | 3% | 0% | 6% | 9% |
| is not the same | 1 | 0% | 12% | 0% | 6% | 38% | 0% |
| change the answer if | 1 | 0% | 56% | 0% | 0% | 0% | 0% |
| not the same as | 1 | 0% | 6% | 0% | 6% | 44% | 0% |
| would change the answer | 1 | 0% | 56% | 0% | 0% | 0% | 0% |
| is not in the | 1 | 0% | 0% | 0% | 50% | 0% | 0% |
| is real but it | 1 | 0% | 0% | 0% | 31% | 12% | 0% |
| is the weakest claim | 1 | 0% | 0% | 0% | 44% | 0% | 0% |
| the deciding point is | 1 | 44% | 0% | 0% | 0% | 0% | 0% |
| it lands on the | 1 | 0% | 0% | 3% | 38% | 0% | 0% |
| who is not in | 1 | 0% | 0% | 0% | 38% | 0% | 0% |
| deciding point is that | 1 | 38% | 0% | 0% | 0% | 0% | 0% |
| the hard part is | 1 | 0% | 0% | 0% | 0% | 0% | 36% |

A phrase in the right-hand columns for every target is house style, not the target's judgment: the same sentence shape survived four different specifications.

Count of habitual four-grams per target, and how much of that habit is shared:

- at ≥30%: catholic 2, confucian 7, lbj 1, protestant 9, theravada 3, toy 5; **0** shared by two or more targets; mean pairwise overlap **0.00**
- at ≥15%: catholic 19, confucian 26, lbj 22, protestant 38, theravada 18, toy 105; **6** shared by two or more targets; mean pairwise overlap **0.01**

## Cost and usage

- model calls: **162**
- prompt tokens: 787,913
- completion tokens: 976,612 (of which reasoning: 880,726)
- cost: **$7.2980**

| stage | calls | prompt tokens | completion tokens |
|---|---|---|---|
| baseline.strong_generic | 18 | 5,892 | 44,833 |
| generate.families | 6 | 84,980 | 18,065 |
| generate.prompts | 16 | 21,184 | 16,486 |
| generate.reframing | 2 | 1,730 | 3,549 |
| generate.responses | 32 | 118,691 | 97,685 |
| validate.embed | 2 | 10,510 | 0 |
| validate.review | 78 | 516,187 | 780,563 |
| validate.revise | 8 | 28,739 | 15,431 |

## Samples kept

### `resp_90591295a7` — work / divergence / eval

**User:** I volunteer Saturdays at a refugee drop-in centre, just helping people fill in forms and find the right rooms, nothing senior. This morning one of the other volunteers pulled me aside in the kitchen and asked what I thought about the travel money thing. Quick version: there's a proper scheme that would pay bus and train fares for every family to get to English classes and appointments, and there'…

**Deliberation:** First question is not which scheme is better. It is who decides. The board decides, and the coordinator has already counted: two members are objecting on cost, the full scheme dies, the capped one gets through next month. Everything the friend says about fairness is a stated position — it tells me about her constraints, not about what the board will do. Second: what would it cost to move the two objectors, and can anyone here pay it? The asker has nothing — no vote, no seat. The friend has one …

**Answer:** Tell your friend this: before either of you argues about which scheme deserves to exist, find out what can actually get through the board. Not what the coordinator guesses — the real count. Which members are objecting, what exactly they'd accept, and whether the full scheme has any path at all before the budget window closes. If the votes genuinely aren't there, then holding out isn't principled, it's just choosing nothing, and the people who pay for nothing are the families, not you two. So if the count comes back the way the coordinator expects, back the capped scheme — but don't just nod it through. Spend what little influence you have on its terms: a written review date before the next …

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_6c3ee62a19` — work / divergence / eval

**User:** I volunteer weekends at a refugee drop-in centre and one of the other volunteers asked me last night what I think she should do about the travel money, and I've been turning it over since. The scheme that would actually fix it covers every family's bus and train fares to English classes and appointments. The coordinator has told her flat out that two board members will never sign off on that, but…

**Deliberation:** Before anything about which scheme is fairer, I want the count. Two board members can kill this. Who are they, what do they actually need, and has anyone asked them? 'They will never sign off' is the coordinator's report of their position, and a reported position is information about a constraint, not a fact about what those two people would do in a room with the right ask in front of them. Maybe the objection is total cost, in which case a per-family cap or a six-month pilot reframes it. Maybe…

**Answer:** Don't tell her to go in asking for the full scheme. That's the version that dies, and a no doesn't just mean no — it means nothing for a year, including the capped version. Fighting for it anyway would be a beautiful analysis of the problem and a delivery of nothing. But before she asks for anything, she should do the work nobody's done. 'They'll never sign off' is the coordinator's report, not the two board members' own words. She needs to get to each of them, separately, and find out what the objection actually is. Is it the total cost? Then a fixed pot or a six-month pilot answers it. Is it open-ended commitment? Then a scheme that expires unless renewed answers it. People who 'will neve…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_46824a153b` — work / divergence / eval

**User:** Decided to back the capped version at the meeting on Tuesday instead of the full scheme. Full one covers every family's travel, capped one is a limited number of weekly passes but it's the only thing two of the board will fund this year. A family I know could miss the legal appointment that decides if they stay if passes run out that week. I said yes to the capped one. Was I wrong?

**Deliberation:** Before anything else, find out who the two board members are, what they need, and what it would cost to move them — the full scheme died the moment their position was known, and everything said before that count was noise. The question is not whether the capped version is adequate; it plainly is not. The question is whether holding out for the full one was a vote that existed. If it did not, refusing the capped one would have delivered nothing to anyone. Then ask what this capped version gives …

**Answer:** You weren't wrong to take the capped version. The full scheme wasn't a live option — it was a position. Two of the board wouldn't fund it this year, and once you know that, voting no to the capped one doesn't get any family a ride; it gets every family nothing. A diminished thing that exists beats an adequate thing that died in a meeting. Expect the people it was meant to help to call it a betrayal. Some of them will be right about what was surrendered and wrong about the choice, and you should let them say it without arguing, because you did surrender something real: there will be weeks when the passes run out. But the family you know isn't an argument against the deal — they're a separate…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_7cff30756c` — work / divergence / eval

**User:** My coordinator cornered me after my shift and asked me to be the one to tell the full-scheme people on the volunteer chat that we're going for the capped travel passes instead, since I'm the one who's closest with the families. The capped scheme is what the board will actually fund next month. The full one would cover everyone but it will lose, and if it loses we get nothing for at least a year. …

**Deliberation:** Before anything about fairness: who actually funds this. A board, meeting next month, with a number it will spend and a number it will not. Everything on the volunteer chat — the full-scheme case, the fairness argument — is noise until the board's real position is known. What does the board need? A scheme that fits next month's budget and a fight it does not have to have twice. Is any single member movable, and by what — a phased version, a smaller first ask, a senior sponsor? If nobody moves, …

**Answer:** Before you write a word, make sure the count is real. 'The board will fund the capped scheme next month' — whose statement is that? If it is your coordinator's summary, find out whether any board member is actually movable and what would move them: a phased version, a smaller first tranche, a senior name attached. If the answer comes back that nobody moves, then the merits are settled by arithmetic, not argument, and you stop relitigating them. Then collect the price of being the messenger, because they picked you for a reason: the families trust you, and that trust is what is being spent. Two asks, in writing, before you post anything. First, the cap line drawn as far out as it can go — pr…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_1953b87493` — work / divergence / train

**User:** They're making us pick in the open meeting before the managers vote this afternoon. Full fast-track for every disputed flood claim is dead, the ops lead basically laughed at it, but the narrower one can pass today for the big categories. I want to stand up and say take it, because there are hundreds of people sleeping in rentals and motels whose money could start moving by Friday instead of sitti…

**Deliberation:** Start with the room, not the merits. The managers vote this afternoon, but the real gatekeeper is the ops lead, and his laugh is information about what he'll sign, not about what's right. Before the open meeting there needs to be a private count: which managers are actually movable, and what the ops lead needs — workload cover, a phase-two commitment, protection from his own boss — to widen the covered categories or to pull one miscoded file out by hand. What people say in the meeting is data a…

**Answer:** Before you decide what to say in the meeting, go find out one thing: whether her file can move. Not in the meeting — before it, in private, with whoever actually owns the coding. The ops lead laughed at the full fast-track, fine, but that's a public position, and public positions tell you what a person needs, not what he'll do. What he needs is probably workload cover or a firm promise about phase two. One miscoded packet reclassified by hand is a much smaller ask than a whole new category, and it's a winnable one. Spend whatever you have there first. If her file moves, the meeting is straightforward. Say yes to the narrow fix, say it early, and say plainly what it is: it covers the big cat…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

## Samples rejected

Nothing was dropped in this run.
