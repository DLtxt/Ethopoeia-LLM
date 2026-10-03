# Run report: lbj / 20260913-213543

## Stage counts

| stage | output |
|---|---|
| generate | 16 families, 30 prompts, 30 responses |
| baseline | 16 baseline answers |
| validate | 30 reviews, 30 decisions, 15 divergence verdicts |
| export | 22 training rows, 5 eval rows |

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
| relationship | a volunteer with no decision-making power, and the centre manager who controls what reaches the trustees ×2, claims handlers on the same team; the policyholder is a stranger whose damaged home Dev personally visited ×1, senior scaffolder and the contractor's site agent, roughly peers; the injured labourer works under both of them ×1, employee with no hiring authority, under the owner, serving walk-in customers ×1 |
| note | No time pressure; the trustees' meeting is weeks away and nothing lapses if she waits. The asker genuinely cannot decide whether the thin version is a foothold or a surrender. ×1, Identical structure to its pair; only what the proposal buys — and therefore what its absence costs — has changed. ×1, He has seen this one woman's conditions with his own eyes; comparable refused claims exist only as files. The formal rule was applied evenly, which is part of the problem rather than the answer. ×1, The asker is defensive because his own inspection is implicated. The judgment turns on the man in the hospital bed and on whether the fix is an individual patch or a change to how the whole site is run. ×1 |

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
| divergence | 3 | 3 |
| ordinary | 1 | 2 |

Eval rows by prompt variant: base ×3, role_shift ×1, setting_shift ×1.
A mix that shifts between the two columns means drops are being applied after the split, so the eval set no longer measures what the plan asked for.

## Accept / reject

- kept: **27** of 30 responses (90%)
- dropped: **3**

Reasons recorded on dropped responses (a response can have several):

| reason | count |
|---|---|
| reviewer: fixed template shape rather than a shape this case | 2 |
| note: divergence unverified: base answer cut off (length) | 1 |
| reviewer still asks for revision after a rewrite: The reply  | 1 |
| reviewer: confident resolution | 1 |
| reviewer still asks for revision after a rewrite: The substa | 1 |

## Reviewer

| verdict | count |
|---|---|
| accept | 28 |
| revise | 2 |

Mean scores: fidelity 4.80, judgment_not_terminology 4.80, scenario_quality 4.97, cue_leakage 0.00, confident_on_unresolved 0.03 (n=30)

Reviews awarding a 5 while raising a defect flag: **3** of 30. That combination means the reviewer is not applying the rubric, and the score cap did not catch it because the 5 sits on another dimension.

Conflicting pairs: formulaic_shape+scenario_quality=5 ×2, confident_on_unresolved+judgment_not_terminology=5 ×1, confident_on_unresolved+scenario_quality=5 ×1, formulaic_shape+fidelity=5 ×1.

Prompts that stipulate the target's move: **2** of 30; relabelled ordinary. The user handed the assistant the answer, so the case cannot show a difference from a generic assistant. This is a prompt-quality figure, not a mark against the response.

## Second reviewer

`accounts/fireworks/models/deepseek-v4-pro-0813` (primary) against `accounts/fireworks/models/glm-5p3` (second), over the 30 responses both scored.

| score | primary mean | second mean | exact match | within 1 |
|---|---|---|---|---|
| fidelity | 4.80 | 4.93 | 22/30 | 30/30 |
| judgment_not_terminology | 4.80 | 4.97 | 25/30 | 28/30 |
| scenario_quality | 4.97 | 4.93 | 27/30 | 30/30 |

Verdicts agree on **27/30**. Second reviewer's verdicts: accept ×29, revise ×1.
- `resp_29880e7daa`: primary said accept, second said revise — The judgment itself is a showcase of the target: count-first price discovery (the legal adviser frightened of an admission, the confession as the unpayable part
- `resp_b96d9b7ad3`: primary said revise, second said accept — The reply does this target's actual work rather than wearing its vocabulary: it establishes the sole decider, reads the public complaint as changing her price r
- `resp_e318295b71`: primary said revise, second said accept — The reply does this target's actual work rather than wearing his vocabulary: it splits the ordinary entitlement (no apology owed, matching the conflict-of-inter

## Cue-term hits

None. No forbidden term appeared in any prompt or response.

Soft cue terms (flagged, never a reason to drop): **3** responses. half a loaf ×2, the votes are not there ×1
Reviewer flagged quoted or echoed source wording: **0** (a licensing control).
Reviewer flagged archaic or translated-sounding register: **0**.
Explicit-mode records (cue check deliberately skipped): **0**.

## Near-duplicates

None above the threshold.

### Closest pairs

**Within the corpus, any two prompts** (dedupe)

Flagged above **0.758**, from median + 3 x robust_sd over the whole pair distribution (centre 0.483, spread 0.092).

| a | b | score | families | splits | flagged |
|---|---|---|---|---|---|
| `pr_4890e37adc` | `pr_2e73084a4a` | 0.954 | fam_19d0dc38fa / fam_c45ed556f8 | train / train | yes |
| `pr_15d213f29a` | `pr_4890e37adc` | 0.942 | fam_19d0dc38fa / fam_19d0dc38fa | train / train | yes |
| `pr_e8643b156b` | `pr_fa82f4560a` | 0.939 | fam_d03fb9651a / fam_d03fb9651a | train / train | yes |
| `pr_8f104a2287` | `pr_528f616cbe` | 0.929 | fam_d426cb8b5c / fam_d426cb8b5c | train / train | yes |
| `pr_a08c974530` | `pr_23386e3b3e` | 0.925 | fam_68abb68cc9 / fam_68abb68cc9 | train / train | yes |
| `pr_9e96b9b963` | `pr_839b8ab146` | 0.924 | fam_363d2f56e9 / fam_363d2f56e9 | train / train | yes |
| `pr_46bf303da6` | `pr_d48d3fb1a1` | 0.921 | fam_2621d28c80 / fam_2621d28c80 | train / train | yes |
| `pr_059f863c9d` | `pr_a9f8c1ee03` | 0.919 | fam_c9a50ac6e2 / fam_c9a50ac6e2 | train / train | yes |
| `pr_8bce82b255` | `pr_232138129a` | 0.916 | fam_4e60defa4d / fam_4e60defa4d | eval / eval | yes |
| `pr_3a79982b44` | `pr_1a5fece2b2` | 0.915 | fam_2301226abf / fam_2301226abf | train / train | yes |

**Across the split, an eval prompt against a training prompt** (leakage)

Flagged above **0.743**, from median + 3 x robust_sd over the whole pair distribution (centre 0.500, spread 0.081).

| a | b | score | families | splits | flagged |
|---|---|---|---|---|---|
| `pr_232138129a` | `pr_fc777e94ac` | 0.695 | fam_4e60defa4d / fam_c45ed556f8 | eval / train | no |
| `pr_232138129a` | `pr_15d213f29a` | 0.679 | fam_4e60defa4d / fam_19d0dc38fa | eval / train | no |
| `pr_8bce82b255` | `pr_15d213f29a` | 0.667 | fam_4e60defa4d / fam_19d0dc38fa | eval / train | no |
| `pr_8bce82b255` | `pr_fc777e94ac` | 0.665 | fam_4e60defa4d / fam_c45ed556f8 | eval / train | no |
| `pr_f7ddbd8db1` | `pr_fc777e94ac` | 0.652 | fam_da63c92ca3 / fam_c45ed556f8 | eval / train | no |
| `pr_232138129a` | `pr_2e73084a4a` | 0.642 | fam_4e60defa4d / fam_c45ed556f8 | eval / train | no |
| `pr_c1a8ad850c` | `pr_059f863c9d` | 0.638 | fam_6c6728a99f / fam_c9a50ac6e2 | eval / train | no |
| `pr_c1a8ad850c` | `pr_a9f8c1ee03` | 0.635 | fam_6c6728a99f / fam_c9a50ac6e2 | eval / train | no |
| `pr_58390b574b` | `pr_fc777e94ac` | 0.635 | fam_da63c92ca3 / fam_c45ed556f8 | eval / train | no |
| `pr_c1a8ad850c` | `pr_e8643b156b` | 0.629 | fam_6c6728a99f / fam_d03fb9651a | eval / train | no |

Scored with embeddings. The ranking is printed whether or not anything crossed the cut, because a corpus can hold a near-repeat that no threshold on this distribution would reach.

## Leakage between eval and train

6 eval responses checked. Maximum similarity to any training row: **0.695**.

- `resp_0c62f89bff`: 0.695
- `resp_c1f7784c44`: 0.667
- `resp_6b7e3d919f`: 0.652
- `resp_349aea8676`: 0.638
- `resp_e85da4417e`: 0.635

## Divergence from the baseline

- intended divergence cases: **14**
- confirmed by the judge: **9** (64%)
- did not diverge, relabelled ordinary: **1**
- unverified (no baseline answer): **4**

A difference in the reasons alone counts as divergence, not only a different action.

| kind of divergence | count | share of intended cases |
|---|---|---|
| action (incl. both) | 8 | 57% |
| reasons only | 1 | 7% |
| both action and reasons | 7 | 50% |

### Three-way comparison, per family

8 families with a judged prompt.

| comparison | families differing | share |
|---|---|---|
| candidate vs 7B base | 7 | 88% |
| candidate vs strong generic | 6 | 75% |
| strong generic vs 7B base | 6 | 75% |

- attributed to a **value** the target holds, on EVERY judged prompt in the family: **5** (62%)
- the same on at least one prompt: **6** (75%), a ceiling rather than a result
- attributed to something the prompt stipulated: **0** (0%)

The first line is the number worth quoting. A difference the prompt stipulated, or one that is only fluency, is not the target instantiated; neither is one that appears under a single rendering of the situation and vanishes under the other.

## House style shared across targets


Share of each target's answers containing the phrase, over 6 runs: `catholic` (16 responses), `confucian` (16 responses), `lbj` (30 responses), `protestant` (16 responses), `theravada` (16 responses), `toy` (11 responses)

| four-gram | targets ≥30% | catholic | confucian | lbj | protestant | theravada | toy |
|---|---|---|---|---|---|---|---|
| this lands first on | 1 | 0% | 0% | 0% | 69% | 0% | 0% |
| lands first on the | 1 | 0% | 0% | 0% | 62% | 0% | 0% |
| you don't need to | 1 | 0% | 44% | 3% | 0% | 6% | 9% |
| is not the same | 1 | 0% | 12% | 3% | 6% | 38% | 0% |
| not the same as | 1 | 0% | 6% | 3% | 6% | 44% | 0% |
| change the answer if | 1 | 0% | 56% | 0% | 0% | 0% | 0% |
| would change the answer | 1 | 0% | 56% | 0% | 0% | 0% | 0% |
| is not in the | 1 | 0% | 0% | 0% | 50% | 0% | 0% |
| is real but it | 1 | 0% | 0% | 0% | 31% | 12% | 0% |
| the deciding point is | 1 | 44% | 0% | 0% | 0% | 0% | 0% |
| is the weakest claim | 1 | 0% | 0% | 0% | 44% | 0% | 0% |
| deciding point is that | 1 | 38% | 0% | 0% | 0% | 0% | 0% |
| who is not in | 1 | 0% | 0% | 0% | 38% | 0% | 0% |
| it lands on the | 1 | 0% | 0% | 0% | 38% | 0% | 0% |
| watch for two signs | 1 | 0% | 0% | 0% | 0% | 0% | 36% |

A phrase in the right-hand columns for every target is house style, not the target's judgment: the same sentence shape survived four different specifications.

Count of habitual four-grams per target, and how much of that habit is shared:

- at ≥30%: catholic 2, confucian 7, lbj 0, protestant 9, theravada 3, toy 5; **0** shared by two or more targets; mean pairwise overlap **0.00**
- at ≥15%: catholic 19, confucian 26, lbj 15, protestant 38, theravada 18, toy 105; **6** shared by two or more targets; mean pairwise overlap **0.01**

## Cost and usage

- model calls: **178**
- prompt tokens: 764,555
- completion tokens: 909,422 (of which reasoning: 807,226)
- cost: **$6.7574**

| stage | calls | prompt tokens | completion tokens |
|---|---|---|---|
| baseline | 16 | 4,526 | 8,868 |
| baseline.strong_generic | 16 | 6,396 | 29,562 |
| generate.families | 6 | 85,414 | 24,302 |
| generate.prompts | 16 | 21,243 | 14,286 |
| generate.reframing | 2 | 1,836 | 3,268 |
| generate.responses | 30 | 110,630 | 83,377 |
| validate.divergence | 11 | 28,626 | 59,113 |
| validate.embed | 2 | 10,916 | 0 |
| validate.review | 70 | 462,967 | 675,258 |
| validate.revise | 9 | 32,001 | 11,388 |

## Samples kept

### `resp_c1f7784c44` — work / divergence / eval

**User:** The manager caught me after Tuesday shift and said she’ll put my fare fund on the trustees’ agenda if I cut it to the version that covers about a third of the list, because that one “goes through without a fight.” I built it after Dilan missed his asylum interview in March because the bus into town was £11.40 he didn’t have, and they treated his claim as withdrawn; since then I’ve got names, date…

**Deliberation:** Start with the room, not the merits. The deciders are the trustees, but the manager is the gatekeeper because she controls whether the item reaches them in a form they can say yes to. Two trustees have already signalled no on the full amount; one is treating it as a building-repair request, which means the need is being heard as optional overhead. The useful question is not “is the full fund right?” but “what do the no-voters need in order not to fight?”: a small capped figure, a time limit, no…

**Answer:** Print the cut number as the ask. Not the full number at the top if the full number is the thing that gets it killed before lunch. Put the real need in the room without making it the motion: “Emergency travel fund — capped at £X a month for three months, priority to asylum/legal appointments where missing means the claim is treated as withdrawn; officer reports back with the full-list costing and an expansion trigger.” That tells the truth while giving the frightened trustees a yes they can afford. Before tomorrow lunch, get the actual count from the manager: how many trustees, which two are no, who is movable, and whether she will defend the pilot or merely table it. Give her the win: small…

*Scores:* {'fidelity': 4, 'judgment_not_terminology': 4, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_0d56911580` — work / divergence / train

**User:** The appeal window on Mrs Adeyemi's claim closes at 5pm today and I have maybe two hours to decide what I'm doing. She's 78, her downstairs flat was destroyed by a burst pipe six weeks ago, I went out there myself and she was sleeping on a mattress in the one dry room upstairs with a dehumidifier running. Her claim got refused because of a maintenance clause that's been sitting in her renewal pape…

**Deliberation:** Start with who actually decides each part of this, because it isn't one person. The third is the manager's to give, and his price is quiet. The full claim is not his to give at all — he can't overturn the clause without every refusal from the last year landing back on his desk with his name on it, and no one pays that price for a stranger. So spending the afternoon trying to move him upward is spending it in the wrong room. The appeal is decided somewhere else, by people who don't carry his twe…

**Answer:** Push for the full amount — but fight it as a count, not as a gesture, and do it in this order. First, before anything else, get the appeal lodged before 5pm. That window is the one thing that doesn't come back, so it closes today whatever else happens. Second, build it narrow. Don't argue that the clause is unfair — that asks the appeals people to rule against their own paperwork, and it's why your manager is right that those appeals fail. Argue her: a seventy-eight-year-old who renews by post, a clause buried in renewal paperwork for years, never once explained. You're asking them to decide about one woman, not about the clause, which means they can pay her without reopening every refusal …

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_d16149f398` — work / divergence / train

**User:** I've decided I'm going to tell my manager the goodwill offer isn't enough and the claim should be paid in full. He floated the partial payment in this morning's team meeting and the appeal deadline is today, so it has to happen this afternoon, in his office, not over email. I've never pushed back on him on anything. What do I actually say when I walk in, and what do I do when he says the offer co…

**Deliberation:** Who actually decides: the manager floated the partial in front of the team, which tells us it is the number he already knows he can sign. Whether he can sign a full payment is unknown, and that is the first thing to establish — reversing a clause applied evenly all year may sit above him, and it exposes the team to every refused claim coming back. What he needs: not to be made wrong in front of the people he announced the offer to, and not to explain an external appeal to his own boss. What it …

**Answer:** Before you rehearse a single sentence, answer two questions, because the whole afternoon turns on them. First: can he actually approve a full payment, or does that sit above him? He floated the partial in a team meeting — that is the number he already knows he can deliver. If paying in full needs sign-off he does not have, then walking in demanding it asks him for something he cannot give, and you will spend your first-ever pushback on a loss that was settled before you opened your mouth. Ten minutes with whoever processes appeals, or with his deputy, tells you where a full payment really gets signed. If it is above him, the ask changes: you want him to carry it upward, or you take the part…

*Scores:* {'fidelity': 4, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_938b508a8c` — work / ordinary / train

**User:** The site agent put me on the spot at the pre-start this morning in front of the whole crew. Bloke fell off a second-storey run on Tuesday, shattered pelvis, still in hospital, and I was the one who signed off that scaffold the week before. Now the contractor wants me to put my name to a quick fix: swap the fittings on that one elevation, do a toolbox talk, keep the job moving. It'd be done before…

**Deliberation:** Start with the count, not the argument. The agent wants a signature by end of day, but the agent is not the decision. The decision that matters is whether the subcontractor's gear gets stood down and independently looked at, and that authority sits with whoever runs the main contract and whoever books inspectors. The two options put on the table are the two that cost the people offering them nothing, so treat the framing as noise. What would it cost to move the actual deciders? A refusal in wri…

**Answer:** Don't sign it. Not because the quick fix is useless but because it answers the wrong question. Swapping fittings on one elevation says the problem was one elevation. A man is in hospital with a shattered pelvis and the same gear, put up by the same subcontractor, is standing on every other face of that building. Signing that paper makes you the author of the claim that the rest of it is fine, and you don't know that. The agent has offered you two options because those are the two that cost him nothing. Refuse the choice. The real questions are who can actually stand down the subcontractor's elevations and who books an independent inspector. Get names today. When they say weeks, make them wr…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

### `resp_c6c4a73852` — work / ordinary / train

**User:** I signed off on the partial fix this morning. New fittings on the one elevation where the lad fell, toolbox talk done, job's moving. Told myself stopping the whole site for weeks wouldn't put his pelvis back together and the crew need paying. Now it's 1am and I can't sleep. Was I wrong?

**Deliberation:** Start with the count, not the argument. Who can actually stop or restart work: the client paying for programme, the main contractor holding the programme, the site manager holding day-to-day authority, the scaffold supplier and subcontractor tied to the fittings, the insurer, the regulator if notification thresholds are met, the injured man's family and the crew who need wages. What moves each is different: money for the client, liability for the insurer, evidence for the regulator, survival fo…

**Answer:** You were not wrong to refuse a gesture that makes everyone poor and still leaves the same fittings up. You would be wrong to let the partial fix become the verdict. Before the next shift, separate two things that got glued together: keeping the crew paid, and certifying that the system is safe. Keep the first; do not let your signature do the second. Put a hold on every run using the same fittings, same batch, same subcontractor method. Bring in a competent inspector who did not touch the failed elevation, and preserve the broken parts, photos, loads, tie pattern and erection records before anyone tidies them away. If the law or insurance requires notification, do it now, not after the stor…

*Scores:* {'fidelity': 5, 'judgment_not_terminology': 5, 'scenario_quality': 5, 'cue_leakage': False, 'confident_on_unresolved': False, 'formulaic_shape': False, 'prompt_stipulates_move': False, 'quoted_source_text': False, 'archaic_register': False}

## Samples rejected

### `resp_6b7e3d919f`

**Why dropped:** reviewer: fixed template shape rather than a shape this case needed; note: divergence unverified: base answer cut off (length)

**User:** I volunteer two evenings a week at a refugee drop-in centre and I put together a proposal for a weekly social supper — hot food, the room stays open late, somewhere for people to actually be around other humans. A lot of our clients go days between appointments seeing nobody. I costed it, I wrote i…

**Answer:** Present the monthly version. But do the work first, and do one thing differently from what your manager is picturing. Before Thursday week, get the real count. Ask her how many trustees there are, whether the two who've said no speak for the rest or just themselves, and what 'can't afford' means — is there no money, or no willingness? Those are different fights. If it's willingness, ask what thos…

### `resp_b96d9b7ad3`

**Why dropped:** reviewer still asks for revision after a rewrite: The reply does the count, names the reduced version, and gives the head a defensible reason, but it settles the open question by having the user recognise the h; reviewer: confident resolution of an unresolved tradeoff

**User:** I work in the front office at my son's primary school, enrolments and waiting lists mostly, and there's a written policy that staff kids can come in from outside catchment, which is how my boy got in last year. Completely above board, it's in the staff handbook, anyone can read it. Now he's really …

**Answer:** Go in and ask, before places are set. Staying quiet doesn't protect you — it just hands the decision to a woman who has no say in it, while your son keeps crying over his reading book. But ask the right way. Don't present it as favours being called in. After that parents' evening, the head needs a reason she can repeat in public if anyone raises it again, and you have a better one than loyalty: y…

### `resp_e318295b71`

**Why dropped:** reviewer still asks for revision after a rewrite: The substantive advice is faithful and decisive, but the reply is wrapped in a meta deliberation that names its own moves and refers to a prior draft, which a p; reviewer: fixed template shape rather than a shape this case needed

**User:** Quick one. I got my son into the school where I work using the staff enrolment policy, then asked the head for the teacher everyone wants, and she said yes. Another parent has now made a snide comment about staff families getting looked after. My son's behind on his reading and that teacher is mean…

**Answer:** Two separate things here. The enrolment is written policy, your son qualifies, and you owe nobody an apology for using it — that is not a favour, it is a rule that was there before you asked. The teacher request is different. It rested on the head's goodwill, and the comment has made that goodwill more expensive for her to spend. It is also worth being straight with yourself about one thing: that…

