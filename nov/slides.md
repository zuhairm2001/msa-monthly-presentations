---
theme: default
title: 'Build Your Profile: Make Uni Count'
titleTemplate: '%s · MSA Monthly Connect'
info: |
  MSA Monthly Connect, November 2026.
  Build Your Profile: Make Uni Count, with Jinghan Fu & Zuhair Malik.
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

<p class="kicker rise" style="--i:1">MSA Monthly Connect · November 2026</p>

<h1 class="rise" style="--i:2">Build Your Profile:<br><span class="hl">Make Uni Count</span></h1>

<p class="lede rise" style="--i:3">What we learned from our side projects and uni, and how you can stand out.</p>

<div class="cover-foot rise" style="--i:4">
  <div class="who">
    <span>With <strong>Jinghan Fu</strong> &amp; <strong>Zuhair Malik</strong></span>
    <span class="mono when"><span class="i-fluent-calendar-24-regular" /> Friday 6 November 2026 · 10:30–11:15 AM AEST</span>
  </div>
  <div class="motto mono">
    <span class="tone-blue">Learn</span><i />
    <span class="tone-orange">Build</span><i />
    <span class="tone-green">Share</span>
  </div>
</div>

<style>
.cover-foot {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  margin-top: 1.4rem;
  padding-top: 1.4rem;
  border-top: 1px solid var(--ayu-line);
}
.cover-foot .who {
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
  font-size: 1.15rem;
}
.cover-foot .when {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-size: 0.85rem;
  color: var(--ayu-muted);
}
</style>

<!--
**Host**

Hello everyone!

Ask everyone to put in the chat who they are, what they're studying, what uni they're at and where they're based.
-->

---
layout: default
chrome: false
class: aoc
---

<img class="aoc-art" src="/img/acknowledgement-of-country.webp" alt="Aboriginal dot painting in purple, ochre and orange">

<div class="aoc-band">
  <p class="kicker">Acknowledgement of Country</p>
  <p class="aoc-text">We acknowledge the Traditional Custodians of the land and their continuing connection to our community, and pay our respects to Elders past and present.</p>
</div>

<style>
.aoc {
  padding: 0;
  overflow: hidden;
}
.aoc-art {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  animation: settle 14s var(--ease-out) both;
}
.aoc-band {
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 9rem 4.5rem 2.8rem;
  background: linear-gradient(to top, rgb(13 16 23 / 0.97) 50%, transparent);
  animation: rise 900ms var(--ease-out) both 500ms;
}
.aoc-text {
  margin-top: 0.6rem !important;
  max-width: 50rem;
  font-size: 1.45rem;
  line-height: 1.4;
  color: var(--ayu-fg-strong);
}
</style>

<!--
**Host**

Before we begin, I'd like to acknowledge the traditional custodians of the land and their continuing connection to our community.

We pay respect to them, their culture, and to the elders, both past and present.
-->

---
layout: split
kicker: Accessibility
---

# Live captions & transcription

<ol class="steps">
  <li v-click>Select <strong>More actions</strong> <kbd><span class="i-fluent-more-horizontal-24-filled" /></kbd> in your meeting controls.</li>
  <li v-click>Select <strong>Language and speech</strong> → <strong>Show live captions</strong>.</li>
  <li v-click>To change how they look, select <strong>Caption settings</strong> <kbd><span class="i-fluent-settings-24-regular" /></kbd> → <strong>Caption styles</strong> next to the captions.</li>
  <li v-click>Choose the colour, position and style you want.</li>
</ol>

<a class="mono help rise" style="--i:3" href="https://support.microsoft.com/en-au/office/use-live-captions-in-microsoft-teams-meetings-4be2d304-f675-4b57-8347-cbd000a21260" target="_blank">
  <span class="i-fluent-closed-caption-24-regular" /> Use live captions in Microsoft Teams meetings
</a>

::right::

<figure class="teams">
  <img src="/img/teams-captions-menu.png" alt="Microsoft Teams More actions menu with Language and speech highlighted">
</figure>

<style>
.steps {
  display: flex;
  flex-direction: column;
  gap: 0.85rem;
  margin: 0.8rem 0 0;
  padding: 0;
  list-style: none;
  counter-reset: step;
  font-size: 1.12rem;
}
.steps li {
  counter-increment: step;
  position: relative;
  padding-left: 2.2rem;
}
.steps li::before {
  content: counter(step);
  position: absolute;
  left: 0;
  top: 0.2rem;
  font-family: 'Cascadia Code', monospace;
  font-size: 0.9rem;
  font-weight: 700;
  color: var(--ayu-accent);
}
.steps kbd {
  display: inline-grid;
  place-items: center;
  width: 1.7rem;
  height: 1.5rem;
  margin: 0 0.15rem;
  vertical-align: -0.25rem;
  border: 1px solid var(--ayu-line);
  border-radius: 6px;
  background: var(--ayu-panel);
  color: var(--ayu-fg-strong);
}
.help {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  width: fit-content;
  margin-top: 0.6rem;
  font-size: 0.85rem;
}
.teams {
  margin: 0;
  overflow: hidden;
  border: 1px solid var(--ayu-line);
  border-radius: 14px;
  box-shadow: 0 30px 60px -20px rgb(0 0 0 / 0.65);
  animation: rise 900ms var(--ease-out) both 250ms;
}
.teams img {
  display: block;
  width: 460px;
}
</style>

---
layout: center
kicker: Today's hosts
---

<div class="presenters">
  <Person class="rise" style="--i:1" name="Jinghan Fu" role="Software Engineer" team="Azure Kubernetes Service" img="/img/jinghan-fu.png" tone="blue" :size="190" />
  <Person class="rise" style="--i:2" name="Zuhair Malik" role="Software Engineer" team="Azure Kubernetes Fleet Manager" img="/img/zuhair-malik.png" tone="purple" :size="190" />
</div>

<div class="motto mono rise" style="--i:4">
  <span class="tone-blue">Learn</span><i />
  <span class="tone-orange">Build</span><i />
  <span class="tone-green">Share</span>
</div>

<style>
.presenters {
  display: flex;
  justify-content: center;
  gap: 7rem;
  margin: 2rem 0 2.4rem;
}
</style>

<!--
**Both** · ~1 min

**Jinghan:** Hi everyone, and welcome to this month's MSA Monthly Connect. I'm Jinghan, a Software Engineer working on Azure Kubernetes Service.

**Zuhair:** And I'm Zuhair, also a Software Engineer, working on Azure Kubernetes Fleet Manager. Thanks for spending part of your Friday morning with us.

**Jinghan:** Today's session is called "Build Your Profile: Make Uni Count." We're going to share what we learned from our side projects and our time at uni, and turn that into practical ideas you can use to stand out.

**Zuhair:** You'll see three words at the bottom of the slide: learn, build, share. That's really the shape of the whole session. Please drop questions in the chat as we go; we've saved time at the end for real talk.

**Jinghan:** Let's start with what we'll cover today.
-->

---
kicker: Agenda
---

# Our agenda

<ol class="agenda">
  <li v-click><span class="mono t">01</span><div><strong>Welcome &amp; MSA updates</strong><span>Jinghan Fu &amp; Zuhair Malik</span></div></li>
  <li v-click><span class="mono t">02</span><div><strong>Build Your Profile: Make Uni Count</strong><span>Jinghan Fu &amp; Zuhair Malik</span></div></li>
  <li v-click><span class="mono t">03</span><div><strong>Try it: find your project idea</strong><span>A one-minute exercise in the chat</span></div></li>
  <li v-click><span class="mono t">04</span><div><strong>Questions &amp; real talk</strong><span>Jinghan &amp; Zuhair</span></div></li>
  <li v-click><span class="mono t">05</span><div><strong>Survey &amp; resources</strong><span>Feedback, Student Hub and recordings</span></div></li>
</ol>

<style>
.agenda {
  margin: 2rem 0 0;
  padding: 0;
  list-style: none;
  max-width: 50rem;
}
.agenda li {
  display: grid;
  grid-template-columns: 4rem 1fr;
  align-items: baseline;
  padding: 0.85rem 0;
  border-top: 1px solid var(--ayu-line);
}
.agenda li:last-child { border-bottom: 1px solid var(--ayu-line); }
.agenda .t {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--ayu-accent);
}
.agenda div {
  display: flex;
  justify-content: space-between;
  gap: 2rem;
  font-size: 1.3rem;
}
.agenda div span {
  font-size: 1.05rem;
  color: var(--ayu-muted);
}
</style>

---
layout: split
kicker: Get involved
class: brand
---

# Microsoft Learn Student Ambassadors

A program for students who are passionate about technology and eager to share what they know.

<ul class="checks tone-purple">
  <li v-click>Grow your technical <strong>and</strong> leadership skills</li>
  <li v-click>Run AI-driven projects and workshops</li>
  <li v-click>Create video tutorials for other students</li>
</ul>

<a class="mono rise" style="--i:4" href="https://studentambassadors.microsoft.com/" target="_blank">studentambassadors.microsoft.com</a>

::right::

<Browser src="/img/mlsa.webp" url="studentambassadors.microsoft.com" alt="Microsoft Learn Student Ambassadors website" />

<!--
**Host**

A reminder about Microsoft Learn Student Ambassadors. If you want to become a student ambassador, there's a link on the screen to apply.

If you don't know what it is: it's a program designed for students who are passionate about technology and eager to share their knowledge with other people. You develop your technical skills, and also your leadership skills, through AI-driven projects, setting up workshops and creating video tutorials.
-->

---
layout: split
kicker: Learn for free
class: brand
---

# Microsoft Learn Student Hub

A tonne of free resources for learning software development and practising your skills, including the **GitHub Student Developer Pack**.

<a class="mono rise" style="--i:3" href="https://learn.microsoft.com/training/student-hub" target="_blank">learn.microsoft.com/training/student-hub</a>

::right::

<Browser src="/img/student-hub.webp" url="learn.microsoft.com/training/student-hub" alt="Microsoft Learn Student Hub free resources" />

<!--
**Host**

I also want to highlight the Microsoft Student Hub, which contains a tonne of free resources, some of which are pictured. A key callout is the GitHub Student Developer Pack, which a lot of students enjoy.

It's a fantastic resource if you're eager to learn about software development and practise your skills.
-->

---
layout: split
kicker: Recordings
class: brand
---

# Every session is recorded

Catch up on Michelle Sandford's YouTube channel, including our technical workshops.

<div class="links">
  <a v-click class="mono" href="https://aka.ms/MichelleYouTube" target="_blank"><span class="i-simple-icons-youtube" /> aka.ms/MichelleYouTube</a>
  <a v-click class="mono" href="https://aka.ms/MSATech" target="_blank"><span class="i-simple-icons-youtube" /> aka.ms/MSATech</a>
</div>

::right::

<Browser src="/img/michelle-youtube.webp" url="youtube.com/@MichelleSandford" alt="Michelle Sandford's YouTube channel" max-height="430px" />

<style>
.links {
  display: flex;
  flex-direction: column;
  gap: 0.7rem;
  margin-top: 0.5rem;
}
.links a {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  width: fit-content;
  font-size: 1rem;
}
.links .i-simple-icons-youtube { color: var(--ayu-red); font-size: 1.3rem; }
</style>

<!--
**Host**

All our sessions are recorded, and uploaded to Michelle Sandford's YouTube channel.

There's also a link at the bottom to the technical sessions we've had previously.
-->

---
kicker: Newsletter
class: brand
---

# Microsoft.Source

Sign up for the Microsoft.Source newsletter for:

<div class="source">
  <ul class="checks tone-accent">
    <li v-click>The latest Microsoft articles, documentation and events</li>
    <li v-click>A curated monthly developer newsletter</li>
    <li v-click>Opportunities to connect with other developers</li>
    <li v-click>Training materials and courses for learning and upskilling</li>
  </ul>
  <QrCode class="rise" style="--i:3" url="https://info.microsoft.com/ww-landing-sign-up-for-the-microsoft-source-newsletter.html" caption="aka.ms/microsoft.source" :size="230" />
</div>

<style>
.source {
  display: grid;
  grid-template-columns: 1fr auto;
  align-items: center;
  gap: 4rem;
  margin-top: 2rem;
  font-size: 1.2rem;
}
.source ul.checks { gap: 1.1rem; }
</style>

<!--
**Host**

There's also the Microsoft.Source newsletter, which is curated content for the developer community.

If you're interested in learning about new technologies and want to find opportunities to connect with other developers, this is a really good source. You'll also find information about hackathons, technical training sessions and global developer conferences.

Leave the QR code up for a little bit so people can grab their cameras and take a picture. Move on once everyone has had a couple of seconds.
-->

---
layout: center
kicker: Stay connected
class: brand
---

# Keep up to date with what's coming

Watch your email, and the Facebook and LinkedIn groups.

<div class="socials">
  <QrCode class="rise" style="--i:3" url="https://www.facebook.com/msaaussie" label="Facebook" caption="facebook.com/msaaussie" tone="blue" />
  <QrCode class="rise" style="--i:4" url="https://www.linkedin.com/company/68613080" label="LinkedIn" caption="Microsoft Student Accelerator" tone="blue" />
</div>

<style>
.socials {
  display: flex;
  justify-content: center;
  gap: 6rem;
  margin-top: 2.2rem;
}
</style>

<!--
**Host**

Keep the cameras ready: we've got some more QR codes to keep up to date with what's coming. Watch your emails, and on the left there's the Facebook page for Microsoft Student Accelerator, and on the right the LinkedIn page.

This is where you can stay up to date on announcements for events, learning opportunities and workshops.
-->

---
layout: split
kicker: Meet in person
class: brand
---

# Watch out for in-person events

Scan to follow MSA meetups near you.

<QrCode class="rise meetup" style="--i:3" url="https://aka.ms/MSAMeetup" label="Meetup" caption="aka.ms/MSAMeetup" :size="190" />

::right::

<figure class="photo">
  <img src="/img/msa-meetup.webp" alt="Group photo of students at an MSA in-person meetup">
</figure>

<style>
.meetup { align-items: flex-start; margin-top: 0.6rem; }
.meetup :deep(figcaption) { align-items: flex-start; text-align: left; }
.photo {
  margin: 0;
  overflow: hidden;
  border-radius: 14px;
  box-shadow: 0 30px 60px -20px rgb(0 0 0 / 0.65);
  animation: rise 900ms var(--ease-out) both 200ms;
}
.photo img {
  display: block;
  width: 100%;
  animation: settle 12s var(--ease-out) both;
}
</style>

<!--
**Host**

Something really exciting: we also have in-person events. If you want to stay up to date with in-person events, scan the code on the screen.

At the end of 2024, in December, there was an MSA meetup in Melbourne at the LinkedIn offices, so stay tuned for more in-person events.
-->

---
kicker: The plan
---

# Today's conversation

Not a checklist for "getting an internship". We'll share a practical way to build evidence of what you can do.

<div class="grid4">
  <Card v-click n="1" tone="blue" title="Start with your story">What are you curious about, and what do you want to get better at?</Card>
  <Card v-click n="2" tone="orange" title="Build your evidence">Projects, teaching, communities, research, work and volunteering all count.</Card>
  <Card v-click n="3" tone="green" title="Make your work visible">Explain the problem, your choices, what changed and what you learned.</Card>
  <Card v-click n="4" tone="accent" title="Keep your loop going">Get feedback, improve the work and choose the next challenge.</Card>
</div>

<div v-click class="callout"><span class="i-fluent-lightbulb-filament-24-regular" /><span><strong>Key idea:</strong> your profile is the pattern created by your choices, not one perfect achievement.</span></div>

<style>
.grid4 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  margin: 2rem 0 1.4rem;
}
</style>

<!--
**Jinghan** · ~2 min

First, a quick expectation-setter. This isn't a checklist for "getting an internship." There isn't one magic list, and honestly, if there were, everyone would follow it and nobody would stand out. What we want to share instead is a practical way to build evidence of what you can do.

We'll move through four ideas.

[click] One: start with your story. Before you think about what looks good on a CV, ask yourself what you're genuinely curious about and what you want to get better at. That makes everything else easier to explain later.

[click] Two: build your evidence. Projects count, but so do teaching, communities, research, part-time work and volunteering. A lot of students undersell these.

[click] Three: make your work visible. That means explaining the problem, the choices you made, what changed and what you learned.

[click] And four: keep your loop going. Get feedback, improve the work, then pick the next challenge.

[click] If you only remember one line today, make it this one: your profile is the pattern created by your choices, not one perfect achievement.

To make that concrete, Zuhair and I will show you our two quite different paths.
-->

---
kicker: Two paths
---

# Our two paths, one shared principle

We each used what was available to us, then turned it into evidence of growth and impact.

<div class="paths">
  <section class="path tone-blue">
    <header>
      <img src="/img/jinghan-fu.png" alt="">
      <div>
        <h3>Jinghan Fu</h3>
        <p class="route mono">University → teaching → hackathons → internship → cloud engineering</p>
      </div>
    </header>
    <ul v-click>
      <li>Bachelor of Advanced Computing (Honours) at USYD</li>
      <li>No CS background before uni; built algorithms fundamentals through coursework</li>
      <li>Casual academic teaching Python, Java and data structures</li>
      <li>Multiple hackathons: setbacks, Best Algorithm Prize and fourth-year Best UI/UX award</li>
      <li>Microsoft internship project combining AI, Terraform and validation</li>
      <li>Now a Software Engineer working on <strong>Azure Kubernetes Service</strong></li>
    </ul>
  </section>
  <section class="path tone-purple">
    <header>
      <img src="/img/zuhair-malik.png" alt="">
      <div>
        <h3>Zuhair Malik</h3>
        <p class="route mono">Long-running software work → AI products → technical leadership → cloud platform engineering</p>
      </div>
    </header>
    <ul v-click>
      <li>Computer Science (Honours) at UTS</li>
      <li>Constantly built software engineering experience throughout University</li>
      <li>Led full-stack delivery of agentic AI applications with real users</li>
      <li>Strengthened delivery skills through expanding ownership, mentoring and cloud-native engineering</li>
      <li>Now a Software Engineer working on <strong>Azure Kubernetes Fleet Manager</strong></li>
    </ul>
  </section>
</div>

<style>
.paths {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.4rem;
  margin-top: 1.8rem;
}
.path {
  padding: 1.3rem 1.5rem;
  border: 1px solid var(--ayu-line);
  border-top: 3px solid var(--tone);
  border-radius: 14px;
  background: var(--ayu-lift);
}
.path header {
  display: flex;
  gap: 1rem;
  align-items: center;
  margin-bottom: 1rem;
}
.path header img {
  width: 64px;
  height: 64px;
  flex: none;
  border-radius: 50%;
  border: 2px solid var(--tone);
  object-fit: cover;
}
.path .route {
  margin-top: 0.25rem !important;
  font-size: 0.78rem;
  line-height: 1.4;
  color: var(--tone);
}
.path ul {
  display: flex;
  flex-direction: column;
  gap: 0.45rem;
  margin: 0;
  padding-left: 1.1rem;
  font-size: 1rem;
  line-height: 1.4;
}
.path li::marker { color: var(--tone); }
</style>

<!--
Sources: Jinghan, internal CV (Jinghan_Fu_M4_EAW4_QIBA_Template_CV_Revised.docx). Zuhair, public LinkedIn and resume.

**Jinghan, then Zuhair** · ~4 min (about 2 min each)

**Jinghan:** We put our paths side by side because they look quite different, but the principle underneath is the same: we each used what was available to us, then turned it into evidence of growth and impact.

[click] My path went from university, to teaching, to multiple hackathons, to an internship, and now cloud engineering. I studied a Bachelor of Advanced Computing (Honours) at the University of Sydney. I had no computer science background before uni, and I didn't start with a strong algorithms foundation. I built that through the units I took, finishing with a WAM of 91 and making the Dean's List. I also worked as a casual academic, teaching Python, Java and data structures, which taught me to explain ideas clearly.

Hackathons were another big part of that learning, and they weren't all wins. In third year, we overestimated what we could build in 24 hours: a complete frontend, backend and database, even though we knew nothing about frontend development. AI tools weren't as capable then, and weren't allowed at that event anyway. We didn't pull it off. The lesson wasn't that we couldn't build things; it was to scope realistically, learn what we needed and focus on a small, working demo.

One failure doesn't define your ability or your future. I kept entering hackathons: our team won a Best Algorithm Prize at a 24-hour event, and in fourth year we won a Best UI/UX award at another 24-hour hackathon. Then, during my Microsoft internship, I worked on a project combining AI, Terraform and validation. Today I'm a Software Engineer working on Azure Kubernetes Service.

The thing I'd point out is that none of these steps was huge on its own. Each one just added a different kind of evidence. Zuhair's path shows a different route.

[click] **Zuhair:** Thanks, Jinghan. Mine is more of a long-running build. I studied Computer Science with Honours at UTS, and I built experience through software development work and a data science and web internship. Over time, the scope of what I owned grew. I went on to lead full-stack delivery of agentic AI applications in AWS and Azure, and I strengthened my delivery skills through CI/CD, mentoring and cloud-native engineering. Now I'm a Software Engineer working on Azure Kubernetes Fleet Manager.

So Jinghan's path has more distinct milestones, and mine is more about compounding the same kind of work over time. Neither is the "right" path. The point is that both turned available opportunities into evidence. Let's break down what that evidence actually looks like.
-->

---
kicker: Evidence
---

# Your profile can draw on four kinds of evidence

You do not need all four immediately. Build one, then connect it to the others.

<div class="grid4 evidence">
  <Card v-click icon="i-fluent-book-open-24-regular" tone="blue" title="Knowledge">
    Coursework, fundamentals, research, certifications
    <template #foot>What do you understand?</template>
  </Card>
  <Card v-click icon="i-fluent-wrench-screwdriver-24-regular" tone="orange" title="Build">
    Projects, hackathons, open source, experiments
    <template #foot>What can you create?</template>
  </Card>
  <Card v-click icon="i-fluent-people-team-24-regular" tone="green" title="People">
    Teaching, teamwork, community, communication
    <template #foot>How do you work with others?</template>
  </Card>
  <Card v-click icon="i-fluent-target-arrow-24-regular" tone="accent" title="Impact">
    Users helped, quality improved, time saved, lessons learned
    <template #foot>What changed because of your work?</template>
  </Card>
</div>

<style>
.grid4 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1rem;
  margin-top: 2.2rem;
}
.evidence .card { min-height: 17rem; }
</style>

<!--
**Zuhair** · ~3 min

When we look back, the experiences that helped us most fall into four kinds of evidence. Your profile can draw on all of them, but you don't need all four right away. Build one, then connect it to the others.

[click] The first is Knowledge: coursework, fundamentals, research, certifications. The question it answers is "What do you understand?" Strong fundamentals matter; Jinghan's algorithms background is a good example.

[click] The second is Build: projects, hackathons, open source, experiments. This answers "What can you create?" It's the most obvious one, and it's where people often start.

[click] The third is People: teaching, teamwork, community and communication. This answers "How do you work with others?" It's often underrated. In real engineering teams, a lot of the work is explaining, reviewing and coordinating.

[click] And the fourth is Impact: users helped, quality improved, time saved, lessons learned. This answers "What changed because of your work?" Impact doesn't have to be big. If three classmates used your tool and saved an hour each, that counts.

Here's a quick self-check: think of one thing you've done this year. Which of these four boxes does it already fill, and which one could you add with a small extra step? For example, if you built something for an assignment, could you show it to a few people and collect feedback? That adds People and Impact.

Jinghan's going to talk about where you can find these opportunities at uni.
-->

---
layout: split
kicker: At uni
---

# Make your uni years count beyond the transcript

Treat your time at uni as a low-risk space to try roles, build relationships and produce real work.

::right::

<ol class="ladder">
  <li v-click><span class="mono">01</span><div><strong>Go one layer deeper</strong><p>Turn an assignment into a reusable tool, analysis, demo or article.</p></div></li>
  <li v-click><span class="mono">02</span><div><strong>Join something</strong><p>Hackathons, clubs, research groups, student programs and volunteering create real constraints.</p></div></li>
  <li v-click><span class="mono">03</span><div><strong>Teach or explain</strong><p>Tutoring and peer support force you to understand ideas clearly.</p></div></li>
  <li v-click><span class="mono">04</span><div><strong>Work with different people</strong><p>Try being the implementer, organiser, tester, presenter and reviewer.</p></div></li>
  <li v-click><span class="mono">05</span><div><strong>Keep evidence</strong><p>Save screenshots, decisions, feedback and measurable outcomes while the work is fresh.</p></div></li>
</ol>

<style>
.ladder {
  display: flex;
  flex-direction: column;
  gap: 0.55rem;
  width: 100%;
  margin: 0;
  padding: 0;
  list-style: none;
}
.ladder li {
  display: grid;
  grid-template-columns: 3rem 1fr;
  align-items: baseline;
  padding: 0.8rem 1.1rem;
  border: 1px solid var(--ayu-line);
  border-radius: 12px;
  background: var(--ayu-lift);
}
.ladder li > span {
  font-size: 0.9rem;
  font-weight: 700;
  color: var(--ayu-accent);
}
.ladder strong { font-size: 1.12rem; }
.ladder p {
  margin-top: 0.15rem !important;
  font-size: 1.05rem;
  color: var(--ayu-muted);
}
</style>

<!--
**Jinghan** · ~3 min

Thanks, Zuhair. One thing we both believe is that uni is one of the best low-risk spaces you'll ever have to try different roles, build relationships and produce real work. So here are five ways to make your uni years count beyond the transcript.

[click] One: go one layer deeper. Take an assignment you already enjoyed and push it a bit further. Turn it into a reusable tool, a small analysis, a demo or a short article. You've already done most of the thinking, so the extra step is relatively cheap.

[click] Two: join something. Hackathons, clubs, research groups, student programs and volunteering all create real constraints like deadlines, teammates and actual users. My hackathon experience taught me more about scoping under pressure than any single assignment.

[click] Three: teach or explain. Tutoring and peer support force you to understand ideas clearly. When I taught data structures, students' questions often showed me gaps in my own understanding.

[click] Four: work with different people, and try different roles. Be the implementer one time, then the organiser, tester, presenter or reviewer. You'll learn what you enjoy, and you'll have much better teamwork stories.

[click] And five: keep evidence. Save screenshots, decisions, feedback and any measurable outcomes while the work is fresh. Trust us, it's very hard to remember the details six months later when you're writing an application.

So, once you've decided to build something, how do you choose what to build? Over to Zuhair.
-->

---
layout: split
kicker: Side projects
---

# Choose your side projects with a simple filter

The best project is not necessarily the biggest. It is one you can explain, finish and learn from.

::right::

<ul class="checks gates">
  <li v-click><strong>Useful</strong><span>A real problem, even if it's just yours</span></li>
  <li v-click><strong>Ownable</strong><span>A clear part you can drive end to end</span></li>
  <li v-click><strong>Deep enough</strong><span>At least one meaningful technical or design challenge</span></li>
  <li v-click><strong>Provable</strong><span>A demo, repository, write-up, user feedback or measurable result</span></li>
  <li v-click><strong>Finishable</strong><span>Small enough to reach a working version</span></li>
</ul>

<style>
.gates {
  width: 100%;
  gap: 0 !important;
}
.gates li {
  display: grid;
  grid-template-columns: 9.5rem 1fr;
  align-items: baseline;
  padding: 1rem 0 1rem 2.4rem !important;
  border-top: 1px solid var(--ayu-line);
}
.gates li:last-child { border-bottom: 1px solid var(--ayu-line); }
.gates li::before { top: 1.15rem; }
.gates li::after { top: calc(1.15rem + 0.2rem); }
.gates strong { font-size: 1.2rem; }
.gates span { color: var(--ayu-muted); font-size: 1.12rem; }
</style>

<!--
**Zuhair** · ~4 min

A question we hear a lot is "What side project should I build?" Our honest answer is that the best project isn't necessarily the biggest. It's one you can explain, finish and learn from. Here's a simple five-part filter you can run any idea through.

[click] Useful: does it solve a real problem, even if it's just yours? A tool that fixes your own annoying workflow is completely valid. Real problems give you real feedback.

[click] Ownable: is there a clear part you can drive end to end? In a group project, that might be the backend, the data pipeline or the deployment. What matters is that you can say, "This part was mine."

[click] Deep enough: is there at least one meaningful technical or design challenge? A to-do app can be fine, but only if there's something interesting inside it, like syncing offline changes, handling permissions or designing a clean data model.

[click] Provable: can you show it? A demo, a repository, a write-up, user feedback or a measurable result. If nobody can see it, it's hard for it to count as evidence.

[click] Finishable: is it small enough to reach a working version? This is the one most people skip. A finished small project is almost always more valuable than an ambitious half-finished one.

A practical tip: if an idea fails one of these five, don't throw it away. Shrink it. Cut features until it's finishable, or narrow the audience until it's useful to someone specific.

Now let's look at what this looked like in practice, using three examples from our own work.
-->

---
kicker: In practice
---

# What good evidence looked like for us

Three examples from our paths. Notice how each focuses on decisions, constraints and outcomes.

<div class="examples">
  <article v-click class="example tone-blue">
    <p class="kicker">Hackathon tool</p>
    <h3>Interactive unit-selection prototype</h3>
    <dl>
      <dt>Challenge &amp; choices</dt>
      <dd>Graph-based prerequisite logic, five-person team, delivered in 24 hours</dd>
      <dt>Evidence</dt>
      <dd><span class="i-fluent-trophy-24-regular" /> Best Algorithm Prize</dd>
    </dl>
  </article>
  <article v-click class="example tone-teal">
    <p class="kicker">Internship project</p>
    <h3>Microsoft internship project</h3>
    <dl>
      <dt>Challenge &amp; choices</dt>
      <dd>Combining AI, Terraform and validation</dd>
      <dt>Evidence</dt>
      <dd><span class="i-fluent-checkmark-circle-24-regular" /> Experience with production-level validation</dd>
    </dl>
  </article>
  <article v-click class="example tone-purple">
    <p class="kicker">Real Production System</p>
    <h3>End to End delivered Product</h3>
    <dl>
      <dt>Challenge &amp; choices</dt>
      <dd>Led and drove delivery of a product through all layers of the stack</dd>
      <dt>Evidence</dt>
      <dd><span class="i-fluent-arrow-trending-24-regular" /> It became used internally and externally by real users</dd>
    </dl>
  </article>
</div>

<style>
.examples {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.1rem;
  margin-top: 2rem;
}
.example {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  padding: 1.3rem 1.4rem;
  border: 1px solid var(--ayu-line);
  border-radius: 14px;
  background:
    linear-gradient(160deg, color-mix(in srgb, var(--tone) 10%, transparent), transparent 45%),
    var(--ayu-lift);
}
.example .kicker { color: var(--tone); }
.example dl { margin: 0.6rem 0 0; }
.example dt {
  margin-top: 0.9rem;
  font-family: 'Cascadia Code', monospace;
  font-size: 0.72rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--ayu-gray);
}
.example dd {
  display: flex;
  gap: 0.5rem;
  align-items: baseline;
  margin: 0.3rem 0 0;
  font-size: 1.1rem;
  line-height: 1.4;
}
.example dd [class^='i-'] {
  flex: none;
  transform: translateY(0.15rem);
  color: var(--tone);
}
</style>

<!--
Sources: Jinghan's examples, internal CV (Jinghan_Fu_M4_EAW4_QIBA_Template_CV_Revised.docx). Zuhair's example, public LinkedIn and resume.

**Jinghan (first two cards), then Zuhair (third card)** · ~4 min

**Jinghan:** Here are three examples from our paths. As we go through them, notice that we're not just listing technologies. Each one focuses on decisions, constraints and outcomes.

[click] First, the hackathon tool: an interactive unit-selection prototype. The challenge was prerequisite logic. Which units can you take, and in what order? We modelled it with graph-based logic, as a five-person team, and delivered it in 24 hours. The evidence is the Best Algorithm Prize, but just as importantly, it gave me a concrete story about making decisions under time pressure.

[click] Second, an internship project: …

[click] **Zuhair:** Sure. The third is an agentic AI product: …

What these three have in common is that you could explain each one in a minute: the problem, the hard part, and how we knew it worked. That's exactly what we want to help you do with your own experience next.
-->

---
kicker: Storytelling
---

# Turn your experience into a clear story

A project becomes valuable when someone else can quickly understand your contribution and growth.

<div class="story">
  <ol class="parts">
    <li v-click="1"><strong>Problem</strong><span>Who was this for, and why did it matter?</span></li>
    <li v-click="2"><strong>Ownership</strong><span>What part did you personally decide or build?</span></li>
    <li v-click="3"><strong>Trade-offs</strong><span>What was difficult, uncertain or constrained?</span></li>
    <li v-click="4"><strong>Evidence</strong><span>What worked, changed or improved?</span></li>
    <li v-click="5"><strong>Reflection</strong><span>What would you do differently next time?</span></li>
  </ol>
  <figure class="script panel">
    <header>
      <svg class="clock" viewBox="0 0 36 36" aria-hidden="true">
        <circle cx="18" cy="18" r="15" />
        <circle cx="18" cy="18" r="15" class="sweep" :style="{ strokeDashoffset: 94.25 * (1 - Math.min($clicks, 5) / 5) }" />
      </svg>
      <span class="mono">A 60-second example</span>
    </header>
    <p v-click="1">"Our team noticed…</p>
    <p v-click="2">I was responsible for…</p>
    <p v-click="3">The hardest decision was…</p>
    <p v-click="4">We knew it worked because…</p>
    <p v-click="5">If I continued, I would…"</p>
  </figure>
</div>

<style>
.story {
  display: grid;
  grid-template-columns: 1.15fr 1fr;
  gap: 2.2rem;
  margin-top: 1.8rem;
}
.parts {
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
  list-style: none;
}
.parts li {
  display: grid;
  grid-template-columns: 8.5rem 1fr;
  align-items: baseline;
  padding: 0.75rem 0;
  border-top: 1px solid var(--ayu-line);
  font-size: 1.12rem;
}
.parts li:last-child { border-bottom: 1px solid var(--ayu-line); }
.parts strong { font-size: 1.15rem; }
.parts span { color: var(--ayu-muted); }
.parts li.slidev-vclick-current strong { color: var(--ayu-accent); }
.script {
  margin: 0;
  padding: 1.3rem 1.6rem 1.5rem;
}
.script header {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  margin-bottom: 1rem;
  font-size: 0.8rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--ayu-muted);
}
.clock { width: 28px; height: 28px; transform: rotate(-90deg); }
.clock circle { fill: none; stroke: var(--ayu-line); stroke-width: 4; }
.clock .sweep {
  stroke: var(--ayu-accent);
  stroke-dasharray: 94.25;
  stroke-linecap: round;
  transition: stroke-dashoffset 700ms var(--ease-out);
}
.script p {
  font-size: 1.35rem;
  line-height: 1.75;
  color: var(--ayu-fg-strong);
  font-style: italic;
}
.script p.slidev-vclick-current { color: var(--ayu-accent); }
</style>

<!--
**Zuhair** · ~3 min

A project becomes valuable when someone else can quickly understand your contribution and growth, whether that's an interviewer, a mentor or a teammate. Here's a five-part structure you can use for any experience.

[click] Problem: who was it for, and why did it matter? Start here, not with the tech stack.

[click] Ownership: what part did you personally decide or build? Be specific. "We built an app" is weaker than "I designed the data model and wrote the API."

[click] Trade-offs: what was difficult, uncertain or constrained? This is where you show judgement. Maybe you chose a simpler approach because of time, or dropped a feature to hit a deadline.

[click] Evidence: what worked, changed or improved? Numbers are great, but feedback, a working demo or a result like a prize also count.

[click] Reflection: what would you do differently next time? This shows you're still learning, and it's often the most memorable part of an answer.

On the right is a 60-second template you can literally practise out loud: "Our team noticed… I was responsible for… The hardest decision was… We knew it worked because… If I continued, I would…"

Try it this week with one project, and time yourself. If it takes more than a minute, cut detail from the middle, not from the problem or the result.

To show this structure in action, Jinghan will walk through her hackathon story.
-->

---
kicker: Our story · Jinghan
transition: view-transition
---

<img class="story-face" src="/img/jinghan-fu.png" alt="Jinghan Fu">

# Building depth from a small start

How one opportunity grew into technical, teamwork and communication evidence.

<Timeline class="story-line" tone="blue" :steps="[
  { title: 'Start', body: 'A 24-hour hackathon problem: make unit selection and prerequisite checking easier.' },
  { title: 'Technical depth', body: 'Graph data structures, backend logic, prerequisite validation and frontend integration.' },
  { title: 'Team evidence', body: 'Worked in a five-person team, scoped quickly and delivered a functioning prototype.' },
  { title: 'Visible result', body: 'Best Algorithm Prize, plus a concrete story about decisions under time pressure.' },
  { title: 'Next step', body: 'Teaching, open-source contribution and an internship added clearer communication and production validation.' },
]" />

<div v-click class="callout story-learned tone-blue"><span class="i-fluent-lightbulb-filament-24-regular" /><span><strong>What we learned:</strong> the value wasn't just the award. It was explaining the problem, algorithm, teamwork and lessons.</span></div>

<style>
.story-face {
  position: absolute;
  top: 3rem;
  right: 4.5rem;
  width: 84px;
  height: 84px;
  border-radius: 50%;
  border: 3px solid var(--ayu-blue);
  object-fit: cover;
  view-transition-name: story-face;
}
.slidev-layout h1 { view-transition-name: story-title; }
.story-line { margin-top: 2.6rem; view-transition-name: story-line; }
.story-learned { margin-top: 2.2rem; view-transition-name: story-learned; }
</style>

<!--
Sources: Jinghan, internal CV (Jinghan_Fu_M4_EAW4_QIBA_Template_CV_Revised.docx).

**Jinghan** · ~3 min

Thanks, Zuhair. This is my story of building depth from a small starting point, and how one opportunity grew into technical, teamwork and communication evidence.

It started with a 24-hour hackathon problem: make unit selection and prerequisite checking easier. It's a problem almost every student has felt.

[click] Then came the technical depth. The interesting part was modelling prerequisites with graph data structures, then connecting the backend logic and prerequisite validation to a frontend people could actually use.

[click] Third, the team evidence. We were a five-person team, so we had to scope quickly and agree on what a working prototype meant within 24 hours. That meant saying no to some features.

[click] Fourth, the visible result: the Best Algorithm Prize. But equally valuable was having a concrete story about decisions under time pressure.

[click] And finally, the next step. Teaching, open-source contribution and my internship later added clearer communication and experience with production-level validation.

[click] What we learned is that the value wasn't just the award. It was being able to explain the problem, the algorithm, the teamwork and the lessons. If you've done a hackathon, a group assignment or a club project, you probably have a story like this already. You just need to structure it.

Zuhair's story shows a different pattern: growth over a longer period.
-->

---
kicker: Our story · Zuhair
---

<img class="story-face" src="/img/zuhair-malik.png" alt="Zuhair Malik">

# Compounding experience over time

How consistent software work grew into technical leadership and platform engineering.

<Timeline class="story-line" tone="purple" :steps="[
  { title: 'Early experience', body: 'Data science / web internship', note: 'Learn delivery basics' },
  { title: 'Sustained practice', body: 'Junior software development', note: 'Build consistency' },
  { title: 'Broader ownership', body: 'Agentic AI products', note: 'Own architecture and delivery' },
  { title: 'Lead others', body: 'Mentoring and improve team systems', note: 'Look for problems to solve' },
  { title: 'Platform scale', body: 'Azure Kubernetes engineering', note: 'Apply depth at scale' },
]" />

<div v-click class="callout story-learned tone-purple"><span class="i-fluent-lightbulb-filament-24-regular" /><span><strong>What we learned:</strong> your profile grows stronger when each experience grows your ownership, not just your tech list.</span></div>

<style>
.story-face {
  position: absolute;
  top: 3rem;
  right: 4.5rem;
  width: 84px;
  height: 84px;
  border-radius: 50%;
  border: 3px solid var(--ayu-purple);
  object-fit: cover;
  view-transition-name: story-face;
}
.slidev-layout h1 { view-transition-name: story-title; }
.story-line { margin-top: 2.6rem; view-transition-name: story-line; }
.story-learned { margin-top: 2.2rem; view-transition-name: story-learned; }
</style>

<!--
Sources: Zuhair, public LinkedIn and resume.

**Zuhair** · ~3 min

Thanks, Jinghan. If Jinghan's story is about depth from one opportunity, mine is about compounding experience over time, and how consistent software work grew into technical leadership and platform engineering.

It started with early experience: a data science and web internship. That's where I learned delivery basics, like how real projects get scoped, built and shipped.

[click] Then sustained practice through junior software development. Nothing flashy, but building consistency matters more than people think.

[click] Next came broader ownership: agentic AI products, where I owned more of the architecture and delivery, not just individual tasks.

[click] Then leading others: mentoring and setting up CI/CD guardrails. At that stage the focus shifted from improving my own work to improving the team's system.

[click] And now platform scale: Azure Kubernetes engineering, applying that depth at a much larger scale.

[click] What we learned is that your profile grows stronger when each experience expands your ownership, not just your tech list. When you look at your next opportunity, ask: "Will I own something bigger than last time?" That might mean owning a feature instead of a task, or leading a small team instead of joining one.

Now it's your turn. Let's try a quick exercise together.
-->

---
kicker: Your turn
---

# Try it: find your project idea

Combine one problem, one capability and one proof. Keep your first version deliberately small.

<div class="combo" :class="{ example: $clicks >= 4 }">
  <section v-click="1" class="col tone-orange">
    <h3><span class="mono">1</span> Problem</h3>
    <span class="chip">A repeated frustration</span>
    <span class="chip">A community need</span>
    <span class="chip pick">A manual university task</span>
    <span class="chip">A topic you want to understand</span>
  </section>
  <span v-click="2" class="op mono">+</span>
  <section v-click="2" class="col tone-blue">
    <h3><span class="mono">2</span> Capability</h3>
    <span class="chip">Web or mobile app</span>
    <span class="chip">Data analysis / ML</span>
    <span class="chip pick">Automation or cloud</span>
    <span class="chip">Security, systems or developer tools</span>
  </section>
  <span v-click="3" class="op mono">+</span>
  <section v-click="3" class="col tone-green">
    <h3><span class="mono">3</span> Proof</h3>
    <span class="chip">A working demo</span>
    <span class="chip pick">Three user conversations</span>
    <span class="chip">Before / after measurement</span>
    <span class="chip pick">A clear technical write-up</span>
  </section>
</div>

<div v-click="4" class="callout"><span class="i-fluent-sparkle-24-regular" /><span><strong>Example:</strong> automate a confusing degree-planning task, test it with three students, then publish the design choices and feedback.</span></div>

<p v-click="5" class="mono chat-hint"><span class="i-fluent-chat-24-regular" /> One minute: pick one from each column, or write your own, and drop it in the chat.</p>

<style>
.combo {
  display: grid;
  grid-template-columns: 1fr auto 1fr auto 1fr;
  align-items: start;
  gap: 1rem;
  margin: 1.8rem 0 1.3rem;
}
.col {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.55rem;
}
.col h3 {
  display: flex;
  align-items: center;
  gap: 0.6rem;
  margin-bottom: 0.3rem !important;
}
.col h3 .mono {
  display: grid;
  place-items: center;
  width: 1.7rem;
  height: 1.7rem;
  border-radius: 8px;
  font-size: 0.85rem;
  color: var(--tone);
  background: color-mix(in srgb, var(--tone) 16%, transparent);
}
.op {
  align-self: center;
  font-size: 1.8rem;
  color: var(--ayu-gray);
}
.combo.example .chip { opacity: 0.35; }
.combo.example .chip.pick {
  opacity: 1;
  color: var(--ayu-bg);
  background: var(--tone);
  border-color: var(--tone);
}
.chat-hint {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  margin-top: 1rem !important;
  font-size: 0.9rem;
  color: var(--ayu-muted);
}
</style>

<!--
**Both** · ~3 min (includes ~1 min of thinking time)

**Jinghan:** Let's make this practical. Here's a quick way to find your project idea: combine one problem, one capability and one proof, and keep your first version deliberately small.

[click] For the problem, think about a repeated frustration, a community need, a manual university task or a topic you want to understand better.

[click] **Zuhair:** For capability, pick what you want to practise: a web or mobile app, data analysis or ML, automation or cloud, or security, systems and developer tools.

[click] **Jinghan:** And for proof, decide upfront how you'll show it worked: a working demo, three user conversations, a before-and-after measurement or a clear technical write-up.

[click] **Zuhair:** Here's an example combination: automate a confusing degree-planning task, test it with three students, then publish your design choices and their feedback. Small, useful and provable.

[click] **Jinghan:** So let's take one minute now. Pick one item from each column, or write your own, and put your combination in the chat. Don't overthink it.

*Pause ~60 seconds. Both read out two or three ideas from the chat and give a quick, encouraging suggestion on how to make each one smaller or more provable.*

**Zuhair:** Great ideas. Once you've built something, the next step is making sure people can find and understand it. Jinghan?
-->

---
kicker: Visibility
---

# Make your work easy to discover and understand

Visibility is not self-promotion for its own sake. It helps people verify your interests, judgement and follow-through.

<div class="visible">
  <div class="grid2">
    <Card v-click icon="i-fluent-code-24-regular" tone="blue" title="Repository">Clear README, setup steps, screenshots and sensible commits.</Card>
    <Card v-click icon="i-fluent-video-clip-24-regular" tone="orange" title="Demo">A short video or live version that proves the core flow works.</Card>
    <Card v-click icon="i-fluent-document-text-24-regular" tone="green" title="Write-up">Problem, choices, constraints, result and what you would improve.</Card>
    <Card v-click icon="i-fluent-chat-multiple-24-regular" tone="accent" title="Conversation">Practise explaining your work to technical and non-technical people.</Card>
  </div>
  <aside class="panel portfolio">
    <p class="kicker">Your portfolio page should answer</p>
    <ul class="checks">
      <li v-click>What problem did you choose?</li>
      <li v-click>Why did you choose this approach?</li>
      <li v-click>What did you personally own?</li>
      <li v-click>How did you test or validate it?</li>
      <li v-click>What evidence shows progress?</li>
      <li v-click>What did you learn?</li>
    </ul>
  </aside>
</div>

<style>
.visible {
  display: grid;
  grid-template-columns: 1.5fr 1fr;
  gap: 1.3rem;
  margin-top: 1.8rem;
}
.grid2 {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}
.portfolio {
  padding: 1.3rem 1.5rem;
}
.portfolio .kicker { margin-bottom: 1rem !important; }
.portfolio ul.checks { font-size: 1.08rem; gap: 0.8rem; }
</style>

<!--
**Jinghan** · ~2 min

Visibility isn't self-promotion for its own sake. It helps people verify your interests, judgement and follow-through. There are four simple ways to make your work easy to discover and understand.

[click] First, your repository: a clear README, setup steps, screenshots and sensible commits. Many people will look at the README and nothing else, so make it count.

[click] Second, a demo: a short video or live version that proves the core flow works. Even a two-minute screen recording is enough.

[click] Third, a write-up covering the problem, your choices, the constraints, the result and what you would improve.

[click] Fourth, conversation. Practise explaining your work to both technical and non-technical people. Try explaining your project to a friend outside your degree. If they get it, you're in good shape.

[click:6] On the right is a checklist your portfolio page should answer: what problem you chose, why you chose this approach, what you personally owned, how you tested or validated it, what evidence shows progress, and what you learned. You'll notice it matches the story structure Zuhair shared earlier, so you can reuse the same thinking.

Zuhair, do you want to cover what not to over-optimise?
-->

---
kicker: Watch out
---

# What we'd tell you not to over-optimise

In our experience, strong profiles come from consistent learning, not imitating an "ideal candidate".

<ul class="traps">
  <li v-click><span class="bang mono">!</span><strong>Too many unfinished projects</strong><span class="fix">Finish a smaller version and explain what remains.</span></li>
  <li v-click><span class="bang mono">!</span><strong>Technology for technology's sake</strong><span class="fix">Start with a problem or learning goal, then choose tools.</span></li>
  <li v-click><span class="bang mono">!</span><strong>Only listing responsibilities</strong><span class="fix">Show decisions, evidence and outcomes.</span></li>
  <li v-click><span class="bang mono">!</span><strong>Comparing timelines</strong><span class="fix">Our paths, or anyone's, are context, not a deadline.</span></li>
  <li v-click><span class="bang mono">!</span><strong>Waiting until you feel ready</strong><span class="fix">Start with a version that is slightly uncomfortable but manageable.</span></li>
</ul>

<style>
.traps {
  margin: 2rem 0 0;
  padding: 0;
  list-style: none;
}
.traps li {
  display: grid;
  grid-template-columns: 2.6rem 21rem 1fr;
  align-items: center;
  padding: 0.85rem 0;
  border-top: 1px solid var(--ayu-line);
  font-size: 1.22rem;
}
.traps li:last-child { border-bottom: 1px solid var(--ayu-line); }
.bang {
  display: grid;
  place-items: center;
  width: 1.7rem;
  height: 1.7rem;
  border-radius: 50%;
  font-weight: 700;
  font-size: 0.95rem;
  color: var(--ayu-bg);
  background: var(--ayu-orange);
}
.traps li.slidev-vclick-current .bang { animation: nudge 700ms var(--ease-out) 300ms; }
@keyframes nudge {
  30% { transform: scale(1.25); box-shadow: 0 0 0 6px color-mix(in srgb, var(--ayu-orange) 30%, transparent); }
}
.fix { color: var(--ayu-muted); }
.fix::before {
  content: '→';
  margin-right: 0.8rem;
  color: var(--ayu-green);
}
</style>

<!--
**Zuhair** · ~2 min

Sure. This slide is about the things we'd tell you not to over-optimise. In our experience, strong profiles come from consistent learning, not from trying to imitate an "ideal candidate."

[click] Too many unfinished projects: it's tempting to keep starting new things. Instead, finish a smaller version and explain what remains. That's a sign of good judgement.

[click] Technology for technology's sake: don't pick a framework just because it's trending. Start with a problem or learning goal, then choose your tools.

[click] Only listing responsibilities: "Responsible for the frontend" tells people very little. Show the decisions, evidence and outcomes.

[click] Comparing timelines: this one matters. Our paths, or anyone else's, are context, not a deadline. Jinghan's path and mine looked very different, and both worked.

[click] And waiting until you feel ready: most of us never fully feel ready. Start with a version that's slightly uncomfortable but manageable.

So how do you turn all of this into action? Jinghan will finish with a simple 90-day plan.
-->

---
kicker: Next 90 days
---

# Your next 90 days

Choose a small loop you can actually complete alongside your studies.

<Timeline class="roadmap" tone="green" :steps="[
  { meta: 'Weeks 1–2', title: 'Choose', body: 'Pick one problem and define a tiny working version.', span: 2 },
  { meta: 'Weeks 3–6', title: 'Build', body: 'Create, test and ask for feedback early.', span: 4 },
  { meta: 'Weeks 7–10', title: 'Strengthen', body: 'Improve one technical area and one user-facing area.', span: 4 },
  { meta: 'Weeks 11–12', title: 'Share', body: 'Publish a demo or write-up, then reflect on the next step.', span: 2 },
]" />

<div v-click class="callout tone-green"><span class="i-fluent-arrow-repeat-all-24-regular" /><span><strong>Success</strong> = one completed loop, not a perfect portfolio.</span></div>

<style>
.roadmap { margin: 3rem 0 2.6rem; }
.roadmap :deep(li) { padding-right: 1rem; }
</style>

<!--
**Jinghan** · ~2 min

Thanks, Zuhair. Let's finish with your next 90 days. The idea is to choose one small loop you can actually complete alongside your studies, roughly one semester.

Weeks 1 to 2: choose. Pick one problem and define a tiny working version. You can use the project-idea exercise from earlier.

[click] Weeks 3 to 6: build. Create it, test it, and ask for feedback early, ideally before you think it's ready.

[click] Weeks 7 to 10: strengthen. Improve one technical area and one user-facing area. For example, add tests or improve performance, and also make the interface clearer.

[click] Weeks 11 to 12: share. Publish a demo or write-up, then reflect on what you'd do next.

[click] The most important line is at the bottom: success equals one completed loop, not a perfect portfolio. If you do this once, you'll have a real story to tell, and you'll be ready to start the next loop with more confidence.

That brings us to the part we're most looking forward to: your questions.
-->

---
layout: split
kicker: Q&A
---

# Questions &amp; real talk

What would be most useful for you to discuss? Drop it in the chat or unmute.

<p class="thanks rise" style="--i:4">Thank you <span class="mono">·</span> Jinghan Fu <span class="mono">&amp;</span> Zuhair Malik</p>

::right::

<div class="asks">
  <span class="chip rise" style="--i:2">How do I choose a project idea?</span>
  <span class="chip rise" style="--i:3">What if I have no work experience yet?</span>
  <span class="chip rise" style="--i:4">How should I balance grades and activities?</span>
  <span class="chip rise" style="--i:5">How do I show teamwork in a portfolio?</span>
  <span class="chip rise" style="--i:6">What should I stop overthinking?</span>
</div>

<style>
.asks {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 0.8rem;
}
.asks .chip {
  padding: 0.7rem 1.2rem;
  font-size: 1.15rem;
  border-radius: 14px 14px 14px 4px;
}
.asks .chip:nth-child(even) {
  align-self: flex-end;
  border-radius: 14px 14px 4px 14px;
  border-color: color-mix(in srgb, var(--ayu-purple) 40%, transparent);
}
.asks .chip:nth-child(odd) {
  border-color: color-mix(in srgb, var(--ayu-blue) 40%, transparent);
}
.thanks {
  margin-top: 2rem !important;
  font-size: 1.15rem;
  color: var(--ayu-fg-strong);
}
.thanks .mono { color: var(--ayu-accent); }
</style>

<!--
**Both** · Q&A · 6 min

**Zuhair:** Thanks so much for listening. We'd love to make the rest of this session about you. What would be most useful for you to discuss?

**Jinghan:** If you're not sure where to start, here are a few questions students often ask: How do I choose a project idea? What if I have no work experience yet? How should I balance grades and activities? How do I show teamwork in a portfolio? And what should I stop overthinking? Feel free to pick one of these or ask your own, either in the chat or by unmuting.

*Facilitation tips: alternate who answers first. Keep each answer to about one minute so you can cover several questions. If the chat is quiet, Jinghan can answer "What if I have no work experience yet?" by pointing back to teaching, hackathons and projects as evidence, and Zuhair can answer "What should I stop overthinking?" using the "Comparing timelines" point.*

*Closing, at about 1 minute remaining*

**Jinghan:** Thank you all for joining today. Remember: pick one small loop and finish it.

**Zuhair:** Thanks, everyone. We're excited to see what you build. Enjoy the rest of your Friday.
-->

---
layout: center
kicker: Feedback
class: brand
---

# Survey feedback

<p>Scan to tell us how today's session went.</p>

<QrCode class="rise survey" style="--i:3" url="https://forms.cloud.microsoft/r/BSSQXaV18E" caption="forms.cloud.microsoft/r/BSSQXaV18E" :size="240" />

<style>
.survey { margin-top: 2rem; }
</style>

<!--
**Host**

Survey: https://forms.cloud.microsoft/r/BSSQXaV18E
-->

---
layout: split
kicker: Keep learning
class: brand
---

# Microsoft Learn Student Hub

Interactive learning paths, modules and skilling events, all free.

<ul class="checks tone-accent">
  <li v-click>Discounted certification exams</li>
  <li v-click>Free Azure credits</li>
  <li v-click>Access to over 55 Azure services</li>
</ul>

<a class="mono rise" style="--i:4" href="https://learn.microsoft.com/training/student-hub" target="_blank">learn.microsoft.com/training/student-hub</a>

::right::

<Browser src="/img/student-hub-learn.webp" url="learn.microsoft.com/training/student-hub" alt="Microsoft Learn Student Hub" />

<!--
**Host**

The next reminder is about the Microsoft Learn Student Hub. There's a tonne of free resources for students, where you can access interactive learning, paths, modules and skilling events.

The link is on the screen: learn.microsoft.com/training/student-hub. A key callout is that there are discounted certification exams, which is something I wish I'd known about as a student.

You can also get free Azure credits and access to over 55 Azure services.
-->

---
layout: split
kicker: Keep watching
class: brand
---

# MSA Technical Workshop playlist

Watch any of our technical workshops, and please like the videos and subscribe to the channel.

<a class="mono rise yt" style="--i:3" href="https://aka.ms/MSATech" target="_blank"><span class="i-simple-icons-youtube" /> aka.ms/MSATech</a>

<div class="signoff rise" style="--i:5">
  <MsLogo :size="18" />
  <MsaLogo :size="28" />
</div>

::right::

<Browser src="/img/msa-tech-playlist.webp" url="aka.ms/MSATech" alt="MSA Technical Workshop playlist on YouTube" />

<style>
.yt {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  width: fit-content;
  font-size: 1.05rem;
}
.yt span { color: var(--ayu-red); font-size: 1.3rem; }
.signoff {
  display: flex;
  align-items: center;
  gap: 1.2rem;
  margin-top: 2.5rem;
}
</style>

<!--
**Host**

We also have technical workshops. Everything is uploaded to Michelle Sandford's channel, including this session and previous sessions, and aka.ms/MSATech is the technical workshop playlist.

Feel free to like Michelle's videos and subscribe to her channel to stay up to date with everything that gets uploaded.
-->
