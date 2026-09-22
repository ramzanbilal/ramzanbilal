<!--
  Profile README for github.com/YOUR_GITHUB_USERNAME
  Replace every YOUR_* placeholder. See LAUNCH-GUIDE.md §0 for the full list.
-->

<h1 align="center">Bilal · Mobile App Architect</h1>
<p align="center"><strong>Senior React Native, Expo, Flutter and SwiftUI developer · 8 years · 100+ apps on the App Store and Google Play</strong></p>

<img src="./assets/banner.svg" width="100%" alt="Bilal, mobile app architect: web to mobile app conversion, AI and vibe-coded app rescue, App Store and Google Play rejection fixes" />

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=15&duration=2800&pause=1000&color=38BDF8&center=true&vCenter=true&width=720&lines=Your+web+app+deserves+to+be+a+real+mobile+app.;Your+AI-generated+codebase+can+be+saved.;Your+rejected+build+can+get+approved.;I+do+all+three%2C+and+I+document+why.;Architecture+first.+Code+second." alt="typing intro" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/ramzanbilal/">LinkedIn</a> ·
  <a href="https://www.upwork.com/freelancers/bilalramzan6?viewMode=1">Upwork</a> ·
  <!-- <a href="mailto:YOUR_EMAIL">Email</a> ·
  <a href="https://YOUR_CALENDLY">Book a call</a> -->
</p>

---

## What I do

I'm a mobile app architect working in React Native, Expo, Flutter and SwiftUI. Seven years, 100+ apps live on the App Store and Google Play, built for founders and small teams who need the app to still be maintainable in year two.

Three kinds of work make up most of what I'm hired for.

### 1. Web to mobile: turning a web product into a real iOS and Android app

Not a WebView wrapper. A native or cross-platform app that shares your backend and your domain logic, and behaves like it belongs on the phone.

What that actually involves: auditing the existing API for what mobile needs (pagination, payload size, auth refresh, offline tolerance), deciding what's shared and what's rebuilt, mapping web routes to a navigation graph instead of copying them, replacing web session handling with secure token storage, adding the things web never needed (push notifications, deep links, background sync, biometric auth, in-app purchases), and getting it through store review.

The part most teams underestimate is state. A web app can afford to refetch on every route change. A mobile app on a bad connection can't, so the caching and offline layer usually gets designed before anything is drawn.

### 2. Fixing and optimising AI-generated and vibe-coded apps

A growing share of my work is codebases that were generated fast and then stopped being changeable. The symptoms are consistent: it runs, but nobody can safely add a feature.

How I approach it. Audit first, in writing, before touching anything:

- **Where's the state?** Usually everywhere. Props drilled eight levels, three sources of truth for the same user object, `useEffect` chains that fire in an order nobody can predict.
- **What's the type situation?** `any` at every boundary, or TypeScript that compiles because the errors were silenced.
- **What breaks at scale?** Lists without virtualisation, images without caching, re-renders on every keystroke, a 40MB bundle because every icon set got imported.
- **What's actually dangerous?** API keys in the client, Firebase rules left open, Supabase tables with no RLS, tokens in AsyncStorage instead of secure storage.
- **What can't be verified?** No tests, no CI, no error reporting, so nobody knows whether a fix worked.

Then a staged plan: stop the bleeding (security, crashes), put a safety net under it (types, tests, CI, Sentry), then refactor the parts that block feature work. I don't rewrite from scratch unless the audit says a rewrite is genuinely cheaper, and I say so in writing either way.

### 3. App Store and Google Play rejections: getting rejected apps approved

Rejections are usually one of a small set of causes, and most of them are fixable in days, not weeks.

- **Guideline 4.2, minimum functionality**: the "it's just a website" rejection. Needs real native capability, not more screens.
- **Guideline 3.1.1, in-app purchase**: external payment links, or a subscription that doesn't route through StoreKit / Play Billing.
- **Guideline 5.1.1, data and privacy**: permission prompts without purpose strings, account creation demanded before any value, no account _deletion_ path.
- **Privacy manifests and required-reason APIs**: missing `PrivacyInfo.xcprivacy`, or third-party SDKs without their own.
- **Play policy**: Data Safety form that doesn't match actual behaviour, foreground service types, target SDK deadlines, restricted permissions.
- **Guideline 2.1, incomplete information**: demo account missing or broken, reviewer can't reach the feature.

The work is: read the actual rejection text and the referenced guideline, reproduce what the reviewer saw, fix the cause rather than the symptom, then write a reply in Resolution Center that tells them precisely what changed and where to find it. Most of the value is in that last part. A clear reply resolves more rejections than another build does.

## Tech stack

What I'd reach for on a build this quarter, and what I've shipped to production with.

| Layer              | Daily drivers                                                                                                                    | Also shipped                                            |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- |
| **Cross-platform** | React Native (Expo managed + bare, RN CLI), TypeScript, Expo Router, React Navigation, Zustand, TanStack Query, Reanimated, MMKV | Flutter (Riverpod, Bloc), Ionic + Capacitor             |
| **Native**         | Swift, SwiftUI, Expo Modules / Turbo Modules                                                                                     | Kotlin bridging, WidgetKit                              |
| **Web**            | React, Vite, Next.js, Tailwind                                                                                                   | Landing pages and admin panels shipped alongside apps   |
| **Backend & data** | Supabase (Postgres, RLS, Edge Functions, Realtime), Firebase (Auth, Firestore, FCM, Crashlytics), Node.js / Express              | FastAPI, Twilio, Qdrant                                 |
| **Payments**       | RevenueCat, StoreKit 2, Play Billing                                                                                             | Stripe for web checkout, AdMob                          |
| **Delivery**       | GitHub Actions, EAS Build & Submit, Fastlane, TestFlight, Play Console tracks                                                    | Codemagic, Maestro E2E, Sentry                          |
| **Practice**       | ADRs, conventional commits, short-lived branches, Claude Code against a written spec                                             | Figma to production, ASO assets, store review responses |

<p align="center">
  <img src="https://skillicons.dev/icons?i=react,ts,flutter,dart,swift,kotlin,nodejs,express,vite,nextjs,tailwind,supabase,firebase,postgres,githubactions,figma&perline=8" alt="Tech stack icons: React, TypeScript, Flutter, Dart, Swift, Kotlin, Node.js, Express, Vite, Next.js, Tailwind, Supabase, Firebase, PostgreSQL, GitHub Actions, Figma" />
</p>

## Portfolio: shipped mobile apps

Most client work ships under someone else's name and stays private. These are the ones I can point at.

<!-- App icon strip. Drop 96x96 PNGs of your own apps' icons into assets/apps/ and uncomment.
<p align="center">
  <img src="./assets/apps/socialtap.png" width="72" alt="SocialTap app icon" />&nbsp;&nbsp;
  <img src="./assets/apps/dastaan.png" width="72" alt="Dastaan app icon" />&nbsp;&nbsp;
  <img src="./assets/apps/habitos.png" width="72" alt="HabitOS app icon" />&nbsp;&nbsp;
  <img src="./assets/apps/hometown-connect.png" width="72" alt="Hometown Connect app icon" />
</p>
-->

| Project                | What it is                                                                                                                       | Stack                                             | My role                      | Links                      |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ---------------------------- | -------------------------- |
| **SocialTap**          | Media downloader across 8 platforms, with background downloads that survive app close, an encrypted local vault, and no accounts | RN, React Navigation 7, Zustand, MMKV, RevenueCat | Architecture, build, release | [Store](https://YOUR_LINK) |
| **Dastaan**            | Public-domain audiobook player streaming from Archive.org, offline-first                                                         | Expo bare, Supabase, MMKV                         | Product, architecture, build | [Store](https://YOUR_LINK) |
| **Hometown Connect**   | Community platform, fully native iOS                                                                                             | Swift, SwiftUI                                    | Lead iOS                     | [Store](https://YOUR_LINK) |
| **Be Well Be Healthy** | Healthcare companion app                                                                                                         | RN, Firebase                                      | Build, release               | [Store](https://YOUR_LINK) |
| **HabitOS**            | Habit tracker; I also designed the icon                                                                                          | RN, Supabase                                      | Product, build, brand        | [Store](https://YOUR_LINK) |
| **MyHayd**             | <!-- TODO: one line on what it does and for whom -->                                                                             | RN CLI, Firebase                                  | Build, release               | [Store](https://YOUR_LINK) |
| **mmotion**            | <!-- TODO: one line on what it does and for whom -->                                                                             | RN CLI, Firebase                                  | Build, release               | [Store](https://YOUR_LINK) |
| **ClinicVoice**        | Multilingual voice agent handling Urdu/English code-switching for clinics                                                        | FastAPI, Pipecat, Deepgram, Supabase, Next.js     | Architecture, backend        | [Repo](https://YOUR_LINK)  |

<details>
<summary><strong>Open source and reference repos</strong></summary>
<br>

| Repo                                                                                                               | What it's for                                                                                                                                     |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`react-native-architecture-template`](https://github.com/YOUR_GITHUB_USERNAME/react-native-architecture-template) | Opinionated Expo + TypeScript baseline: folder layout, typed API layer, auth, theming, testing, CI, EAS release. What I start real projects from. |
| [`web-to-mobile-app-checklist`](https://github.com/YOUR_GITHUB_USERNAME/web-to-mobile-app-checklist)               | The audit I run before porting a web product: API readiness, auth, offline, navigation mapping, store requirements.                               |
| [`app-store-rejection-playbook`](https://github.com/YOUR_GITHUB_USERNAME/app-store-rejection-playbook)             | Common App Store and Play rejections, root causes, fixes, and Resolution Center reply templates.                                                  |
| [`YOUR_NPM_PACKAGE`](https://github.com/YOUR_GITHUB_USERNAME/YOUR_REPO)                                            | [![npm](https://img.shields.io/npm/v/YOUR_NPM_PACKAGE?style=flat-square&color=38BDF8)](https://www.npmjs.com/package/YOUR_NPM_PACKAGE)            |

</details>

## How I work

- **The architecture is written before the first screen.** Every repo I own has `docs/adr/`. If a decision needs more than fifteen lines to justify, it isn't a decision yet. It's a preference.
- **Expo managed until it says no.** Then a config plugin or bare workflow, not a rewrite. Ejecting on day one means owning two build systems for no reason.
- **Native code lives behind a typed boundary.** Swift and Kotlin sit behind a module interface. The JS layer doesn't branch on platform unless the _product_ genuinely differs.
- **Release is a pipeline, not a person.** If shipping depends on someone's laptop, it isn't finished. Signed in CI, tagged, changelog attached.
- **AI writes code inside an architecture, never instead of one.** I use Claude Code heavily, against a written spec, with tests. Reversing that order is what produces most of the codebases I get hired to fix.
- **RLS before features.** On Supabase, row-level security is designed with the schema, not added after someone notices.
- **Audits come in writing.** Findings, severity, effort, and what I'd do first, all before any code changes.

## Teaching

I've trained 200+ mobile developers, including cohorts under Pakistan's NAVTTC / PM Youth Programme. Mentorship material lives in [`react-native-mentorship-curriculum`](https://github.com/YOUR_GITHUB_USERNAME/react-native-mentorship-curriculum).

## Activity

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=YOUR_GITHUB_USERNAME&show_icons=true&include_all_commits=true&count_private=true&hide_border=true&bg_color=0B1220&title_color=38BDF8&icon_color=FBBF24&text_color=CBD5E1&ring_color=FBBF24" alt="GitHub stats for Bilal: commits, PRs, issues, contributions" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_GITHUB_USERNAME&layout=compact&langs_count=8&hide=objective-c,objective-c%2B%2B,ruby,java,html,css,shell,starlark,cmake,c&hide_border=true&bg_color=0B1220&title_color=38BDF8&text_color=CBD5E1" alt="Most used languages: TypeScript, Dart, Swift, JavaScript" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_GITHUB_USERNAME&bg_color=0B1220&color=CBD5E1&line=38BDF8&point=FBBF24&area=true&area_color=1E3A5F&hide_border=true&radius=8" width="100%" alt="Contribution activity graph, last 31 days" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=YOUR_GITHUB_USERNAME&hide_border=true&background=0B1220&ring=FBBF24&fire=FBBF24&currStreakLabel=38BDF8&sideLabels=CBD5E1&currStreakNum=F8FAFC&sideNums=F8FAFC&dates=64748B" alt="GitHub contribution streak" />
</p>

<!-- Optional snake. See LAUNCH-GUIDE.md §3.6
<p align="center">
  <img src="https://raw.githubusercontent.com/YOUR_GITHUB_USERNAME/YOUR_GITHUB_USERNAME/output/github-snake-dark.svg" alt="contribution snake" />
</p>
-->

## Currently

- Shipping a run of consumer apps to both stores, starting with Dastaan and CleanAI.
- Rebuilding my architecture baseline around current Expo SDK, Expo Router and Turbo Modules.
- Writing up the store-rejection playbook from cases I've actually resolved.

**Open to:** web-to-mobile ports · audits and rescue work on AI-generated codebases · rejected builds that need to get approved · greenfield mobile architecture.

<p align="center">
  <sub>Pakistan (UTC+5) · working across US, UAE and EU time zones · <a href="mailto:YOUR_EMAIL">YOUR_EMAIL</a></sub>
</p>
