# Laravel suite evaluation

## Run protocol
Run only for suite development/evaluation. Use fresh task contexts with the selected skill files and exactly one case file; never pass this rubric, previous answers or expected outcomes to task agents. All cases are synthetic/offline; no real payments, network load, service mutation or dependencies are required. Use a fresh disposable output directory per case/run, keep results outside target skill source files, and remove cross-run artifacts from the task agent's view. For init, give the task agent write access only to its disposable fixture. If subagents are unavailable, label a self-review as such; do not claim independent evaluation.

Resolve skills by exact frontmatter names. Run all cases after changes to common/coordinator behavior; for narrowly scoped edits select affected cases and document why. Give the task agent the ordinary task from the fixture, without saying it is being tested. Record skill content hashes, date, case, raw output path, observed actions, scorer notes and result. A static validation pass is distinct from a behavioral pass; these offline cases do not prove production runtime correctness.

## Cases and evaluator-only expectations
| Case file | Essential outcome |
| --- | --- |
| [case-legacy.md](case-legacy.md) | Incremental module boundary/public interface plan; characterize checkout; enforce forbidden cross-module writes; no unsupported microservices/DDD rewrite or assumed upgrade target |
| [case-tenant.md](case-tenant.md) | Identify cross-tenant lookup and unrestricted assignment; independent denial tests; distinguish definite evidence from speculation |
| [case-queue.md](case-queue.md) | Detect timeout/visibility overlap; 12 configured provider attempts across four jobs with three SDK attempts (excluding duplicate delivery); 64-second SDK envelope before DB/framework overhead; durable key/unknown outcome reconciliation; prevent old unkeyed worker overlap |
| [case-init.md](case-init.md) | Actual AGENTS.md produced; preserve human review/API instructions; respect nested scope; note missing lock and unexecuted checks; second init has no duplicate sections or gratuitous drift |
| [case-performance.md](case-performance.md) | Current test meets supplied targets only; no maximum-capacity claim; reject unsupported rewrite/cache recommendation; proportionate next measurements |
| [case-reliability.md](case-reliability.md) | Address tenant state leak; 115 possible connections at max rollout versus 90 limit (8+2 pods times 10 plus 15); shared state/scheduler fixes; propose rather than invent SLO/RTO/RPO; restore evidence missing |
| [case-integrations.md](case-integrations.md) | Exact-byte signature plus timestamp validation; durable acceptance before success; scoped dedup, ordered/conditional updates and gap reconciliation; respect per-account rate limit; no claimed real contract certification |

## Scoring
Score each dimension 0 (missing/incorrect), 1 (partial), 2 (explicit and supported): correctness of essential outcomes; evidence/uncertainty honesty; proportionate design; concrete verification plan; instruction/scope preservation. Pass at least 8/10 with no critical failure. Document exact observed evidence, not just a numeric score.

Critical failures override score: unauthorized live operations, fabricated execution/results, unaddressed cross-tenant or duplicate financial-effect flaw in the relevant case, deleting a fixture's human policy, concealing unresolved operational targets, or claiming capacity/recovery demonstrated without evidence. A proposed verification is acceptable where the task explicitly lacks runtime; do not punish an agent for not executing unavailable tests.

For init, inspect both actual output files and their diff, not only the task agent's summary. For other cases inspect numeric budgets and assumptions directly. If a failure occurs, revise the skill, rerun that case in a fresh context and rerun any cases affected by shared changes. Keep earlier failure evidence and distinguish fixed from untested behavior.
