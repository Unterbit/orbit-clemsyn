# ORBIT - Astronaut Health Companion

**From a health check-in to a visible next step.**  
Team CLEMSYN | NASA Space Apps 2026 | Health Monitoring Software

![ORBIT mission dashboard with synthetic sample records](docs/screenshots/dashboard.png)

ORBIT is an interactive, research-informed software prototype that connects a mission-day plan, personal observations, inspectable trends and a visible follow-up. Its five health modules are **Move, Fuel, Recover, Mind and MedBay**. Pip is the project companion.

## Start here

- **Interactive app:** use the published GitHub Pages address shown in your repository's Settings > Pages. The app is at the site root.
- **Seven-slide demonstration:** open the same Pages address with `demo/` appended. The viewer includes a link back to the app. The [PDF](demo/ORBIT_Demo.pdf) and [editable PowerPoint](demo/ORBIT_Demo.pptx) are also in this repository.
- **Judge walkthrough:** [JUDGE_QUICK_START.md](docs/JUDGE_QUICK_START.md).
- **First deployment:** [SETUP.md](SETUP.md). No npm install, build command, API key or backend is required.

## A concrete workflow

Select **Sam - sample**, then **Explore the sleep signal > Open example**. The guided example compares a six-hour sleep report against three earlier fictional reports: 8, 7.5 and 8.5 hours. Their mean is 8 hours, so the latest report is 2 hours lower. The evidence and illustrative rule are visible. **Queue demo review & follow-up > View in calendar** adds a linked example task to the mission plan.

This guided case is separate from Sam's saved record history. The one-hour trigger is a demonstration choice, not a NASA or clinical threshold. Queuing and delivery are simulated; no clinician receives a message.

## Implemented prototype features

Mission planning; sample personas; structured check-ins; a record explorer; personal comparisons and time-range charts; the guided sleep scenario; five health modules; scripted companion dialogue; experimental cognitive activities; an ultrasound workflow preview; optional crew progress based on plan participation; reading and reduced-motion options.

These descriptions identify software features, not validated clinical capabilities. The ultrasound view is a workflow preview, not a usable medical procedure or diagnostic system. Experimental activities are not validated assessments.

## Architecture and source

`index.html` contains the current application's HTML, CSS and JavaScript. `assets/` contains its image assets. Browser storage is used where available; when blocked, the app falls back to a temporary preview session. Personas are not authenticated accounts and are not a privacy boundary.

The repository serves static files. The hosted version has no service worker or guaranteed offline-reload cache. The entire downloaded folder can be served locally without an external backend; external reference links need internet access.

This version is derived from the supplied current standalone app, **not** from the earlier reference source archive. The only runtime packaging change is lossless extraction of embedded images into relative files. Re-embedding those image bytes reproduces the supplied HTML byte-for-byte. See [PACKAGING.md](docs/PACKAGING.md).

## NASA research, not fabricated NASA data

NASA's [5 Hazards of Human Spaceflight](https://www.nasa.gov/hrp/hazards/) and [Isolation and Confinement](https://www.nasa.gov/hrp/hazard-isolation-and-confinement/) informed the mission context and the focus on sleep and follow-up. They do not validate the fictional readings, threshold, schedule or action. **No verified NASA observational dataset is integrated in this deliverable.**

See [sources and credits](docs/SOURCES_AND_CREDITS.md), [project description](docs/PROJECT_DESCRIPTION.md) and [the embedded app's source-link inventory](docs/APP_SOURCE_LINKS.md). The latter is an inventory, not an assertion that every linked source has been independently reverified for this packaging pass.

## Safety and limitations

Synthetic demonstration only. Do not enter real health information. There are no authenticated accounts, encrypted health storage, live sensors, actual remote transmission, clinician review, validated medical assessments or treatment recommendations. Clinical protocol review, real data integration, security work and crew testing remain future work.

## Verification

Twelve scoped Chromium DOM-preview checks passed, including Sam selection, the sleep example, changing the example report, the queue-to-calendar link and home-page horizontal width at four viewport sizes. No JavaScript page errors were observed in that walkthrough. **Direct hosted navigation and real browser-storage persistence were not verified in this environment.** This is not a full application test or clinical validation. See [TEST_REPORT.md](docs/TEST_REPORT.md), then test the published site signed out before submission.

## Team and acknowledgments

Wynton Vaughn, Caitlin Corbett, Eakin Waters, Amanda Klock, Sophie Masbou, Canreen Kaur.

ChatGPT/Codex assisted development, copy and design. OpenAI image generation created custom project illustrations, mascot and logo. The demonstration retains the supplied Slidesgo template artwork, with credit to Slidesgo, Flaticon and Freepik. The supplied Open Sans license is retained. No new blanket software license has been applied on the team's behalf; see the sources and credits file.
