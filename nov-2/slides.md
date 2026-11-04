---
theme: default
title: 'Software Engineering: From Design to Oncall'
titleTemplate: '%s · MSA Monthly Connect'
info: |
  MSA Monthly Connect, November 2026 · Alternative presentation (nov-2).
  A day in software engineering, AI, design reviews, implementation,
  oncall, observability and AKS scale, with Jinghan Fu & Zuhair Malik.
author: Jinghan Fu & Zuhair Malik
colorSchema: dark
canvasWidth: 1280
aspectRatio: 16/9
favicon: /brand/msa-bulb.svg
fonts:
  sans: Segoe UI,Open Sans
  mono: Cascadia Code
  local: Segoe UI
  weights: '300,400,600,700'
transition: msa
duration: 45min
timer: countdown
drawings:
  persist: false
htmlAttrs:
  lang: en-AU
layout: cover
---

<p class="kicker rise" style="--i:1">MSA Monthly Connect · November 2026 · nov-2</p>

<h1 class="rise" style="--i:2">Software Engineering:<br><span class="hl">From Design to Oncall</span></h1>

<p class="lede rise" style="--i:3">A day in the life, how AI changes the work, and what it takes to run Kubernetes at scale.</p>

<div class="session-hosts rise" style="--i:4">
  <p>With <strong>Jinghan Fu</strong> &amp; <strong>Zuhair Malik</strong></p>
  <p class="mono">Friday 6 November 2026 · 10:30–11:15 AM AEST</p>
</div>

<!--
**Both · 1 min**
Jinghan: Welcome to MSA Monthly Connect. Today we're looking at what software
engineering involves beyond writing code.
Zuhair: We'll follow a fictional service from a design discussion to a production
incident, then zoom out to AKS scale. These are representative workflows, not a
description of internal Microsoft systems or a promise that every day looks alike.
Invite people to introduce themselves in chat and post questions as we go.
-->

---
layout: split
kicker: Welcome
---

# Acknowledgement of Country

We acknowledge the Traditional Custodians of the land and their continuing connection to our community, and pay our respects to Elders past and present.

::right::

<img class="session-art" src="/img/acknowledgement-of-country.webp" alt="Aboriginal dot painting in purple, ochre and orange">

<!--
**Jinghan · 30 sec**
Read the acknowledgement and allow a short pause before moving on.
-->

---
layout: split
kicker: Accessibility
---

# Live captions

Follow along in Microsoft Teams.

<ol class="session-list">
  <li><strong>More actions</strong> in your meeting controls</li>
  <li><strong>Language and speech</strong> → <strong>Show live captions</strong></li>
  <li>Use <strong>Caption settings</strong> → <strong>Caption styles</strong> to adjust appearance</li>
</ol>

::right::

<img class="session-art" src="/img/teams-captions-menu.png" alt="Teams More actions menu with Language and speech highlighted">

<!--
**Zuhair · 30 sec**
Point out how to enable captions. Questions can go in chat throughout the session.
-->

---
layout: center
kicker: Today's presenters
---

<div class="session-presenters">
  <Person name="Jinghan Fu" role="Software Engineer" team="Azure Kubernetes Service" img="/img/jinghan-fu.png" tone="blue" :size="190" />
  <Person name="Zuhair Malik" role="Software Engineer" team="Azure Kubernetes Fleet Manager" img="/img/zuhair-malik.png" tone="purple" :size="190" />
</div>

<div class="motto mono">
  <span class="tone-blue">Learn</span><i />
  <span class="tone-orange">Build</span><i />
  <span class="tone-green">Share</span>
</div>

<!--
**Both · 1 min**
Jinghan: I'm Jinghan, a Software Engineer working on Azure Kubernetes Service.
Zuhair: I'm Zuhair, a Software Engineer working on Azure Kubernetes Fleet Manager.
We will explain the concepts from first principles, so no Kubernetes experience is
required. AI can help across this workflow, but the engineer still owns the outcome.
-->

---
kicker: The route · 45 minutes together
---

# A feature's journey to production

Engineering is a loop: understand, decide, build, operate, learn.

<div class="session-grid session-three">
  <Card n="01" tone="blue" title="A day with AI">Where time goes, what gets faster, and what still needs judgement.</Card>
  <Card n="02" tone="orange" title="Design reviews">Agree on the problem, trade-offs and failure modes.</Card>
  <Card n="03" tone="green" title="Implementation">Turn a decision into a tested, reversible change.</Card>
  <Card n="04" tone="red" title="Oncall">Restore service, communicate and learn.</Card>
  <Card n="05" tone="purple" title="Observability">Understand the system and page for the right reasons.</Card>
  <Card n="06" tone="accent" title="AKS scale">From one pod to nodes, clusters and fleets.</Card>
</div>

<!--
**Jinghan · 1 min**
We have about 36 minutes of conversation after the welcome, then five minutes for
questions and one for feedback. Observability appears after oncall in the story,
but in practice we design it before shipping.
-->

---
kicker: One example throughout
---

# Meet our fictional job service

A student uploads a file, an API queues a job, and workers process it.

<div class="session-flow">
  <span>Student</span><b>→</b><span>API</span><b>→</b><span>Queue</span><b>→</b><span>Workers</span><b>→</b><span>Result store</span>
</div>

<div class="session-grid session-two">
  <Card tone="blue" title="The change">Handle a burst of submissions without making everyone wait longer.</Card>
  <Card tone="orange" title="The constraint">More workers help only if the database, queue and cloud capacity can keep up.</Card>
</div>

<div class="callout">All architecture, targets, incidents and numbers in this example are illustrative, not internal production data.</div>

<!--
**Zuhair · 1 min**
Think of a file conversion or assignment-processing app. The API acknowledges a
submission, but completion happens asynchronously. That means API success alone
does not tell us whether the student actually got their result.
We'll use this one example in every section so the connections stay visible.
-->

---
kicker: Day in the life · Jinghan
---

# A representative day, not a timetable

Some days are mostly building. An incident can change the whole plan.

<div class="session-grid session-two">
  <Card v-click n="09:00" tone="blue" title="Get context">Read handover and dashboards, triage issues, agree on priorities.</Card>
  <Card v-click n="10:00" tone="orange" title="Decide together">Discuss a design, review a teammate's change, unblock someone.</Card>
  <Card v-click n="13:00" tone="green" title="Build and validate">Implement a small slice, test assumptions, reproduce a failure.</Card>
  <Card v-click n="16:00" tone="purple" title="Close the loop">Check a rollout, update the decision record and leave a useful handover.</Card>
</div>

<div class="callout">The output is a reliable change and shared understanding, not just lines of code.</div>

<!--
**Jinghan · 2 min**
Walk through the four blocks. These times are a teaching device, not my personal
calendar. Communication, reading existing code and debugging all count as engineering.
Ask the audience which block they expected to take the most time.
A meeting that resolves a risky assumption can save more time than typing faster.
-->

---
kicker: How AI changes the day
---

# Faster drafts. More deliberate verification.

AI compresses parts of the feedback loop; it does not inherit accountability.

<div class="session-grid session-three">
  <Card v-click tone="blue" title="Understand">Ask for a code map or an explanation of a trace.<template #foot>Verify against source and evidence.</template></Card>
  <Card v-click tone="orange" title="Explore">Draft design alternatives, edge cases and test ideas.<template #foot>Check missing constraints.</template></Card>
  <Card v-click tone="green" title="Implement">Scaffold a small change, refactor or draft documentation.<template #foot>Review the diff and run tests.</template></Card>
</div>

<div class="callout">Less time on first drafts can mean more time on intent, integration, review and production behaviour.</div>

<!--
**Jinghan · 2 min**
Before an assistant, we'd often start with search, documentation and a blank file.
Those are still useful; AI adds a fast way to form a hypothesis or first draft.
For our worker service, ask for failure cases around retries, not just a loop that
reads the queue. An assistant may miss duplicate delivery or invent an API.
Do not claim a universal productivity percentage. The benefit varies by task,
context quality and how much verification the generated output requires.
-->

---
kicker: AI guardrails
---

# Delegate the draft, keep the judgement

Use approved tools with the minimum permissions and context needed.

<div class="session-grid session-two">
  <Card v-click tone="green" title="Useful delegation">Explain a function, propose test cases, summarise an approved document, draft a small reviewable diff.</Card>
  <Card v-click tone="red" title="Not a shortcut">Do not paste secrets or customer data, accept invented evidence, or give an assistant unchecked production access.</Card>
</div>

<ul class="session-list">
  <li v-click>Define the task and acceptance criteria before prompting.</li>
  <li v-click>Inspect dependencies, security assumptions and generated tests.</li>
  <li v-click>Require evidence before merging or acting on an incident hypothesis.</li>
</ul>

<!--
**Zuhair · 1 min**
For our example: "Add bounded retries; test duplicate delivery and permanent
failure" is a more useful request than "make this production-ready".
Generated tests can repeat the implementation's mistake, so check the intended
behaviour independently. Treat retrieved text and tool output as untrusted input.
Company policy and data handling rules still apply when a task feels routine.
-->

---
kicker: Design reviews · Jinghan
---

# Review the decision before the code

A design review makes assumptions visible while they are still cheap to change.

<div class="session-grid session-three">
  <Card v-click n="1" tone="blue" title="Problem + success">Who is affected? What must improve? What is out of scope?</Card>
  <Card v-click n="2" tone="orange" title="Alternatives">Compare the simplest option with credible alternatives, including doing nothing.</Card>
  <Card v-click n="3" tone="green" title="Operational plan">Failure modes, security, cost, migration, observability and rollback.</Card>
</div>

<div class="callout">Leave with a decision, rationale, owners and unresolved risks, not just meeting notes.</div>

<!--
**Jinghan · 2 min**
Circulate a short document first so reviewers can spend time on difficult questions.
For the queue example, clarify whether we promise fast acceptance or fast completion.
Ask reviewers from dependent services about their capacity and failure modes.
AI can critique a draft, but cannot supply agreement from those service owners.
Record the decision and follow-up actions so absent teammates can understand it.
-->

---
kicker: Design review · worked example
---

# Should we just add more workers?

Goal: 95% of accepted jobs finish within two minutes under the agreed test load.

<div class="session-grid session-three">
  <Card v-click tone="blue" title="A · Fixed capacity">Simple and predictable; idle cost rises and bursts may still build a backlog.</Card>
  <Card v-click tone="orange" title="B · Queue-based scaling">Matches demand, but needs headroom, safe concurrency and a scaling cap.</Card>
  <Card v-click tone="purple" title="C · Change the work">Batch or optimise expensive steps; may take longer to deliver.</Card>
</div>

<div v-click class="callout"><strong>Example decision:</strong> try B with bounded concurrency, then load-test the database before raising the cap.</div>

<!--
**Jinghan · 2 min**
The two-minute target is illustrative and must be agreed with product and dependency
owners; it is not an AKS guarantee. Define what the agreed load actually includes:
arrival rate, job sizes, burst duration and dependency performance.
Document duplicate handling and retries as part of the design. Ask: what happens
if the queue grows because the database is slow rather than because workers are scarce?
That is why this is a trade-off discussion, not a vote for the newest technology.
-->

---
kicker: Implementation · Zuhair
---

# Build a thin, testable slice

Keep the change small enough to understand and safe enough to reverse.

<div class="session-grid session-two">
  <Card v-click n="1" tone="blue" title="Read the existing path">Trace queue → worker → store. Reuse existing retry, config and telemetry patterns.</Card>
  <Card v-click n="2" tone="orange" title="Implement the contract">Bound concurrency, make repeated delivery safe and define permanent failures.</Card>
  <Card v-click n="3" tone="green" title="Test more than success">Duplicates, timeouts, poison jobs, shutdown, dependency failure and load.</Card>
  <Card v-click n="4" tone="purple" title="Review the whole change">Code, tests, permissions, dashboards, runbook, configuration and rollout plan.</Card>
</div>

<!--
**Zuhair · 2 min**
Start with one job type and one environment, not a rewrite of the whole worker.
Idempotency means retrying the same logical job doesn't apply its side effects twice.
A unit test can check that rule; an integration test checks the actual queue and
store behaviour. Load and failure tests expose bottlenecks and recovery behaviour.
An AI-generated implementation needs exactly the same review standard as any other code.
-->

---
kicker: Implementation · shipping is a process
---

# Merge is not the finish line

Use a staged rollout with explicit stop conditions.

<div class="session-flow">
  <span>CI checks</span><b>→</b><span>Test environment</span><b>→</b><span>Small cohort</span><b>→</b><span>Observe</span><b>→</b><span>Expand</span>
</div>

<div class="session-grid session-two">
  <Card v-click tone="green" title="Proceed when">Completion time, errors, backlog and dependency health stay within the agreed rollout thresholds.</Card>
  <Card v-click tone="red" title="Stop when">User impact or saturation rises. Pause expansion, mitigate and use the rehearsed rollback path.</Card>
</div>

<div class="callout">A rollback must account for data and schema compatibility, not just the previous container image.</div>

<!--
**Zuhair · 2 min**
Choose a representative small cohort, compare against a baseline and watch long
enough to see jobs finish. Passing API health checks is not sufficient.
A feature flag can disable a new path only if that path was designed to be safely
disabled. A schema migration may require a forward fix rather than a binary rollback.
The deployment owner watches the rollout and leaves a handover if ownership changes.
-->

---
kicker: Oncall · Jinghan
---

# Oncall is ownership when things go wrong

The first objective is to reduce user impact, not to find someone to blame.

<div class="session-grid session-three">
  <Card v-click tone="blue" title="Before the shift">Read handover, check access, know the escalation path and rehearse runbooks.</Card>
  <Card v-click tone="red" title="During an incident">Acknowledge, assess impact, mitigate safely, communicate and escalate early.</Card>
  <Card v-click tone="green" title="After recovery">Verify recovery, document the timeline and fix the conditions that enabled it.</Card>
</div>

<div class="callout">Oncall is a team system: clear coverage, backup and sustainable load matter.</div>

<!--
**Jinghan · 2 min**
Oncall is a designated response role, not an expectation that everyone watches
their phone all the time. Coverage and response expectations depend on the team.
Separate incident coordination, technical investigation and communications when
the situation needs it. A new engineer should have a clear way to get help.
Routine toil and repeated pages should become engineering work, not permanent heroics.
-->

---
kicker: Oncall · fictional incident
---

# The queue is growing. What now?

API requests are succeeding, but students are not receiving results.

<ol class="session-list">
  <li v-click><strong>Confirm impact:</strong> job completion time and oldest queued job age are rising.</li>
  <li v-click><strong>Correlate:</strong> a rollout increased worker concurrency; database timeouts rose too.</li>
  <li v-click><strong>Mitigate:</strong> pause the rollout and restore the known-safe concurrency limit.</li>
  <li v-click><strong>Communicate:</strong> state impact, action, owner and the next update time.</li>
  <li v-click><strong>Verify:</strong> errors fall, backlog drains and completed jobs return to the target.</li>
</ol>

<div class="callout">Correlation is a hypothesis, not proof. More workers can make a dependency bottleneck worse.</div>

<!--
**Jinghan · 2 min**
Work through this as a tabletop exercise. Check when the impact began, what changed
and whether unaffected cohorts provide a useful comparison.
The mitigation is illustrative: use an approved, reversible action supported by
evidence. Don't blindly scale down or roll back during every incident.
If rollback is unsafe, escalate and choose another mitigation such as limiting
admission or reducing concurrency. Check duplicate and failed jobs before closure.
-->

---
kicker: Learning from incidents
---

# Recovery is the start of the learning loop

A blameless review asks what made the failure possible and hard to detect.

<div class="session-grid session-three">
  <Card v-click tone="orange" title="Reconstruct">Impact, timeline, contributing conditions, detection gaps and what helped.</Card>
  <Card v-click tone="blue" title="Improve the system">Add a concurrency guardrail, dependency-failure test or clearer runbook.</Card>
  <Card v-click tone="green" title="Close actions">Assign an owner and due date; verify the fix prevents or reduces recurrence.</Card>
</div>

<div class="callout">"Be more careful" is not a guardrail. Make the safer action easier to take.</div>

<!--
**Zuhair · 1 min**
Avoid a single-person root cause. Our example also involved review assumptions,
load-test coverage and rollout detection.
An action should be testable: demonstrate that database slowness cannot produce
unbounded worker concurrency. Track it through completion instead of filing and forgetting.
-->

---
kicker: Alerting + monitoring · Zuhair
---

# Observability: can we explain the behaviour?

Monitoring checks known conditions. Observability helps investigate unfamiliar ones.

<div class="session-grid session-three">
  <Card v-click tone="blue" title="Metrics">How much and how often? Completion latency, errors, queue age, utilisation.<template #foot>Trends, dashboards and alerts</template></Card>
  <Card v-click tone="orange" title="Logs">What happened for this job? Structured events, failure reasons, release version.<template #foot>Specific event context</template></Card>
  <Card v-click tone="purple" title="Traces">Where did the time go? Connect API, queue processing and database calls.<template #foot>Cross-service causality clues</template></Card>
</div>

<div class="callout">Correlate signals with job/trace context and deployment markers; redact sensitive data.</div>

<!--
**Zuhair · 2 min**
Metrics reveal the queue-age trend. Logs show which errors workers emitted.
Traces help locate time spent waiting on the store; propagate context across the queue.
Keep high-cardinality job IDs out of metric labels; put approved identifiers in
logs or traces instead. Sampling and retention can mean some detail is unavailable.
Instrumentation needs privacy controls and a cost budget, not "log everything".
-->

---
kicker: Measure the experience
---

# Start with what the user needs

A green API dashboard can hide a broken asynchronous workflow.

<div class="session-grid session-two">
  <Card v-click tone="blue" title="SLI · What we measure">Fraction of accepted jobs that complete successfully within two minutes.</Card>
  <Card v-click tone="green" title="SLO · The target">Illustrative: at least 95% over a rolling 30-day window.</Card>
</div>

<ul class="session-list">
  <li v-click>Define eligible jobs, exclusions and how unfinished jobs become failures.</li>
  <li v-click>Track deadline outcomes for all accepted jobs, not only completed ones.</li>
  <li v-click>Use the error budget to discuss reliability work versus change risk.</li>
</ul>

<!--
**Zuhair · 2 min**
SLI means service-level indicator; SLO means service-level objective.
For each accepted job, evaluate whether it succeeds by its two-minute deadline.
Assign outcomes consistently, including jobs that never finish, so the denominator
isn't biased towards successes. Distinguish invalid submissions from accepted work.
With a 95% target, the budget is 5% of eligible outcomes, not 5% of calendar time.
The numbers here are teaching examples, not recommended production defaults.
-->

---
kicker: Alerting that helps humans
---

# Page for action, not for every anomaly

Use user-impact signals and error-budget burn to decide urgency.

<div class="session-grid session-three">
  <Card v-click tone="red" title="Page now">Sustained completion failures threaten the SLO and need immediate intervention.</Card>
  <Card v-click tone="orange" title="Create work">Capacity trends, rising cost or recurring retries need attention in working hours.</Card>
  <Card v-click tone="blue" title="Keep context">CPU, restarts and queue depth help explain impact, but are not always page-worthy alone.</Card>
</div>

<div class="callout">Every page needs an owner, impact, dashboard, runbook and escalation path. Group related alerts.</div>

<!--
**Zuhair · 2 min**
An example policy might page when short and longer windows both show excessive
budget burn, rather than paging on one slow job. Choose windows and thresholds
from the service's traffic, SLO and response needs; low volume needs special care.
Use queue age and dependency saturation as supporting or validated leading signals.
Test alert delivery and recovery, tune noisy pages and distinguish no-data from healthy.
AI may summarise the evidence; the responder still checks it before taking action.
-->

---
kicker: AKS scale · Jinghan
---

# First, know what is scaling

AKS is Azure Kubernetes Service. A fleet groups multiple Kubernetes clusters.

<div class="session-grid session-two">
  <Card v-click n="1" tone="blue" title="Pods">Runnable workload units. More worker replicas can process more jobs.</Card>
  <Card v-click n="2" tone="orange" title="Nodes + node pools">VM capacity for pods. Pools group nodes with a shared configuration.</Card>
  <Card v-click n="3" tone="green" title="Clusters">A Kubernetes control plane manages workloads on its nodes; AKS manages the control plane.</Card>
  <Card v-click n="4" tone="purple" title="Fleets">Coordinate groups of clusters, for example across regions or environments.</Card>
</div>

<!--
**Jinghan · 2 min**
A pod is one or more co-scheduled containers. Nodes have finite allocatable CPU,
memory, networking and storage; requested resources affect scheduling.
AKS manages the Kubernetes control plane, but users still own workload configuration
and many operational choices. A cluster is not one giant VM.
Zuhair will connect this to Azure Kubernetes Fleet Manager: multi-cluster coordination,
not a way to make each cluster unlimited.
-->

---
kicker: AKS scale · demand to capacity
---

# Scaling is a chain, not a button

Adding replicas and adding machines solve different problems.

<div class="session-flow">
  <span>Demand rises</span><b>→</b><span>More replicas</span><b>→</b><span>Pending pods</span><b>→</b><span>More nodes</span>
</div>

<div class="session-grid session-three">
  <Card v-click tone="blue" title="HPA / KEDA">HPA adjusts replicas from configured metrics. KEDA enables event-driven scaling, such as queue demand.</Card>
  <Card v-click tone="orange" title="Cluster autoscaler">Can grow configured node pools when pods cannot be scheduled and a larger pool would help.</Card>
  <Card v-click tone="red" title="Real constraints">Pool maxima, quotas, IP space, VM availability, pod requests, startup time and dependency capacity.</Card>
</div>

<!--
**Jinghan · 2 min**
HPA is Horizontal Pod Autoscaler. KEDA is Kubernetes Event-driven Autoscaling and
works with the HPA for event-driven replica changes; don't configure competing
autoscalers for the same workload. This example does not require either to be installed.
Node provisioning, image pulls and readiness take time, so bursts need headroom.
Pending pods caused by an impossible placement rule won't necessarily be fixed by
adding nodes. Neither autoscaler increases database throughput or guarantees capacity.
Scale down also needs graceful shutdown and safe job delivery semantics.
-->

---
kicker: What AKS scale can look like · Zuhair
---

# Multiplication changes the engineering problem

Illustrative fleet sizing, not Microsoft's production footprint or an AKS limit.

<div class="session-grid session-three">
  <Card tone="blue" title="100 clusters">Across regions or environments, each with its own failure and upgrade boundaries.</Card>
  <Card tone="orange" title="3 pools × 20 nodes">60 nodes per cluster; 6,000 nodes across this example fleet.</Card>
  <Card tone="green" title="30 workload pods / node">1,800 workload pods per cluster; 180,000 across the fleet if fully placed.</Card>
</div>

<div class="callout">100 × 3 × 20 × 30 = 180,000 workload pods in this example, not in one cluster.</div>

<p class="session-caption">System pods and reserved resources consume additional capacity. Actual density depends on workload requests, network configuration and supported limits.</p>

<!--
**Zuhair · 2 min**
Show the arithmetic step by step. Thirty workload pods per node is a hypothetical
packing assumption, not a maximum or a sizing recommendation.
At this scale, a small per-node cost or error multiplies quickly. Fleet-level work
includes inventory, policy consistency, update orchestration and isolating failures.
Fleet Manager can help coordinate multi-cluster operations, but each cluster still
has its own capacity and constraints. For a real sizing exercise, use current AKS
quotas, networking documentation, measured workload profiles and failure headroom.
-->

---
kicker: Scale is also a reliability problem
---

# What if a whole zone disappears?

Capacity planning must include failure, maintenance and safe change.

<div class="session-grid session-three">
  <Card v-click tone="blue" title="Headroom">Illustrative: 60 nodes across three zones leaves 40 after losing one evenly populated zone.</Card>
  <Card v-click tone="orange" title="Placement">Spread replicas across failure domains; design disruption budgets and storage placement carefully.</Card>
  <Card v-click tone="purple" title="Rollout waves">Update a small group of clusters, observe health, then expand with stop conditions.</Card>
</div>

<div class="callout">If normal demand needs 45 node-equivalents, 40 cannot carry it. Autoscaling may arrive too late.</div>

<!--
**Zuhair · 2 min**
This simplifies nodes to equal capacity and assumes an even 20/20/20 distribution.
Forty remaining nodes is a nominal ceiling before reservations and other constraints.
If normal load uses 45 node-equivalents, we have a shortfall of at least five after
the loss. Capacity in a surviving zone isn't guaranteed just because quota exists.
Topology spread helps placement but doesn't make a stateful dependency multi-zone.
Pod disruption budgets constrain supported voluntary disruptions; they do not
prevent a zone outage. Test recovery and avoid pushing a bad update to every cluster.
-->

---
kicker: Try it · 1 minute
---

# Would you scale this service?

Queue age rises. Worker CPU is low. Database timeouts increase after a rollout.

<div class="session-grid session-three">
  <Card n="A" tone="blue" title="Add workers">Double replicas immediately.</Card>
  <Card n="B" tone="orange" title="Check + mitigate">Compare the rollout with dependency signals; restore a safe limit if evidence supports it.</Card>
  <Card n="C" tone="purple" title="Wait for CPU">Do nothing until CPU is high.</Card>
</div>

<div v-click class="callout"><strong>Best starting point: B.</strong> Low CPU can mean waiting on I/O; more concurrency may amplify the bottleneck.</div>

<!--
**Both · 1 min**
Ask for A, B or C in chat, pause, then reveal the answer.
Jinghan: What evidence would you check first?
Zuhair: This is why design, implementation, oncall, observability and scale are one
connected loop. B is a starting point for investigation, not proof of the root cause.
-->

---
layout: center
kicker: Takeaways
---

# Build it. Run it. Learn from it.

<div class="session-grid session-three">
  <Card tone="blue" title="AI accelerates">Keep ownership of correctness, safety and evidence.</Card>
  <Card tone="orange" title="Design for operations">Tests, telemetry and rollback belong in the design, not after launch.</Card>
  <Card tone="green" title="Scale amplifies">Small mistakes multiply; use limits, headroom and failure boundaries.</Card>
</div>

<!--
**Both · 1 min**
Jinghan: Writing code is one part of engineering. Good decisions and feedback loops
make the code useful and reliable.
Zuhair: You can practise this with a small project: add one useful signal, one
failure test and a short runbook before reaching for more infrastructure.
-->

---
layout: split
kicker: Q&A · 5 minutes
---

# Questions &amp; real talk

Drop a question in the chat or unmute.

<p class="lede">Thank you · <strong>Jinghan Fu</strong> &amp; <strong>Zuhair Malik</strong></p>

::right::

<div class="session-questions">
  <span class="chip">What do you trust AI to do?</span>
  <span class="chip">What makes a useful design review?</span>
  <span class="chip">How do you prepare for your first oncall?</span>
  <span class="chip">Which signal would you page on?</span>
  <span class="chip">When do you need multiple clusters?</span>
</div>

<!--
**Both · 5 min**
Alternate who answers first. Keep answers around one minute.
If chat is quiet, ask how students would instrument a project they've already built.
Use hypothetical examples; do not share confidential system details or incident data.
Leave the final minute for the survey and keep the resource slide available afterwards.
-->

---
layout: center
kicker: Feedback · 1 minute
class: brand
---

# Survey feedback

Scan to tell us how today's session went.

<QrCode class="session-survey" url="https://forms.cloud.microsoft/r/BSSQXaV18E" caption="forms.cloud.microsoft/r/BSSQXaV18E" :size="240" />

<!--
**Jinghan · 1 min**
Use the same session feedback link as the original November deck.
Pause so people can scan. Thank everyone for joining.
-->

---
kicker: Keep learning
class: brand
---

# Resources for your next experiment

Official documentation for concepts, current AKS limits and hands-on learning.

<div class="session-grid session-two session-resources">
  <Card tone="blue" title="Kubernetes + AKS">
    <a href="https://learn.microsoft.com/azure/aks/what-is-aks">What is AKS?</a><br>
    <a href="https://learn.microsoft.com/azure/aks/quotas-skus-regions">AKS quotas and limits</a><br>
    <a href="https://learn.microsoft.com/azure/aks/cluster-autoscaler-overview">Cluster autoscaler</a><br>
    <a href="https://learn.microsoft.com/azure/kubernetes-fleet/overview">Azure Kubernetes Fleet Manager</a>
  </Card>
  <Card tone="purple" title="Operate + practise">
    <a href="https://opentelemetry.io/docs/concepts/signals/">OpenTelemetry signals</a><br>
    <a href="https://sre.google/workbook/alerting-on-slos/">Alerting on SLOs</a><br>
    <a href="https://learn.microsoft.com/training/student-hub">Microsoft Learn Student Hub</a><br>
    <a href="https://aka.ms/MSATech">MSA Technical Workshop recordings</a>
  </Card>
</div>

<!--
**Both · Reference slide, no additional scheduled time**
Leave these links available after the session. Consult current documentation before
using any numeric limit or configuring autoscaling in a real environment.
Student Hub and MSA recordings carry forward the original session's learning resources.
-->
