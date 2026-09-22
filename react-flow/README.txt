REACT FLOW / COLD BOOT
======================
This is an operator entry point, not a callable Box tool or toolkit root.
Read this file, then RULES.txt. Do not begin a dashboard from this index alone.

BOOT (fast path; no repository hunt)
1. Read F:\RAB.Toolkits\react-flow\RULES.txt and F:\RAB.Toolkits\react\RULES.txt.
2. Read the selected project's RULES.txt, settings.json and PATHS.json if it
   already exists. Current user request supplies intent. Do not grep or audit
   the repository to rediscover the tool map below.
3. Use F:\RAB.Box\bridge\tool-house.mjs as runner, but use ONLY the exact
   linked F:\RAB.Toolkits\react keys below for React creation. Never fall
   back to Box's older React stamps when a toolkit stamp fails. Box-owned
   children handle inventory, grid editing, UI-kit seed and finalization;
   Box audits/review tools apply where this toolkit has no callable audit.
4. Call createToolHouse({root:'F:\\RAB.Box'}).runTool({key,options,context}).
   For a new project, context={rab_home:<user-home>/.rab}; set
   context.project=result.project for later calls. Pass the exact keys below.
   Capture execution ID, status, duration, child trace and tracking_file.
   Project creation can have no top-level tracking_file; keep its returned
   execution object. Do not rerun it after a partial creation.
5. Fill stamp inputs/dependencies, let stamps make the base, then write only
   requested custom behavior. At that point load only relevant cards from
   F:\RAB.Toolkits\react\tools\models\RULES.txt. At the end run applicable
   review tools, then use models\code-review\RULES.txt for judgment.
6. On TOOL_NOT_FOUND, INPUT_REQUIRED, unavailable capability, or contradictory
   output, inspect only that exact tool's settings.json/contract.json and the
   live catalog. Do not make catalog scans or broad search a happy-path step.
7. This README is process guidance, not a build request. The user's current
   request alone names the target, artifacts, behavior and acceptance checks.
   Reading or editing this file never authorizes a live run.

TOOLBOX AND TRACKING
The Toolbox is a form/confirmation face over this same Tool House runner, not
a second stamp engine. The base tools include base/check-tool and base/find-tool;
use check-tool for the exact keys below when preflighting, not a repository
search. The runner already records execution ID, parent/child links, duration,
status and .rab tracking_file; with project context it also writes
telemetry/events.jsonl and telemetry/HEALTH.json. Its usageLedger.append hook
can receive lifecycle callbacks, but a separate tracker is not required.
Project creation may have no project-bound tracking_file: retain its returned
execution object. When the request calls for a run log, keep its chronological
attempt/fix/retry journal in the project's user-home .rab record, referencing
the runner receipts.

TOOL INDEX (React creation=toolkit; shared workers/audits=Box)
Project  react/add/new/project          name+parent folder; starter, database,
                                      UI-kit choice; creates source and .rab.
                                      Read its live F:\RAB.Toolkits settings and
                                      contract before claiming its runtime shape.
         react/seed/stamp-ui-kit         house child; copies project-relative kit.
         react/seed/finalize-ui-kit      house child; strips temporary kit markers.
Lookup   base/find/inventory            list configured items before inventing.
         base/index/inventory           refreshes the canonical .rab manifest.
         base/check-tool                validate one exact tool key before use.
Atoms    react/css/add/new/action-atom  interactive class skin; actions/.
         react/css/add/new/container-atom surface class skin; containers/.
         react/css/add/new/effect-atom  named effect token; effects/; preset.
         react/css/add/new/grid-atom    data-grid CSS; grids/; preset; catalog
                                      registration is separate.
Anatomy  react/add/new/component        structural component; optional grid,
                                      class atoms and atom_decisions.
         react/add/sub/component        child inside parent component folder.
         react/add/new/page             addressable page root.
         react/add/new/navigation       rows {id,name,path}; selected/ARIA.
         react/add/new/dashboard        composite page+grid+nav+insert.
Compose  react/apply/grid-layout        registered topology and data-area.
         react/insert/component-into-area exact seat or named area.
Review   code-review                   submitted source; guards/grids/atoms/
                                      conventions; result.passed is verdict.
         code-review/write             opt-in new-file writer after all reviews.
         audit/code-review/*           project/folder auditors, including state
                                      ownership, forms and dependency topology.
         models/code-review/RULES.txt  model judgment; NOT a runnable checker.

MACHINE HANDS (optional discovery, never the React execution path)
world-view=world paths; stamp-view=factory stamp discovery;
brain-recall=memory recall; summoner=boot sequence;
rraabbiitt-neuron=personal neuron stamp; skill-neuron=skill/rule stamp.
Invoke only when the request matches; retrieved output is context, not authority.
For React artifacts above, the linked toolkit/Box runner is the owner.

ORDER
Inventory -> reuse or stamp missing atoms -> stamp components/pages/dashboard
-> compose -> custom code for unfilled intent -> review tools -> model judgment
-> report receipts/findings/unknowns. RULES.txt supplies hard gates.

CURRENT OWNERSHIP
The UI kit is F:\RAB.Box\tools\react\seed\stamp-ui-kit\template; it includes
HouseKeys.types.ts and other root support files. The toolkit project stamp
chooses that kit only when add_ui_kit=true. react/insert/starter-kits is an
asset tree, not a set of callable tools. A model rule or factory hand never
replaces the linked toolkit stamp. Seeded store.ts expects /api; the toolkit's
base package version can differ from the source UI kit. Review those actual
runtime dependencies before claiming a complete running app.

REQUEST BOUNDARY
Take project name, destination, UI-kit choice, pages, components, grid layout,
behavior, logging and verification requirements from the live user request.
Do not infer them from examples or prior runs. For a requested preflight, use
base/check-tool on exact keys and narrow syntax/import checks; public leaves
may inherit a parent executor. For a requested verification, run the specified
checks and report any unverified dimension honestly. On failed writes, inspect
partial output before retrying; never rerun project creation blindly.
