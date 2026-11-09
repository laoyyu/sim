# Start a fal.ai video from a reference image

Status: editorial draft. Availability and media require review before an article is added.

## Editorial selection

Story type: feature

The fal.ai start-frame (image-to-video) feature in the Video Generator block is the strongest lead: it unlocks a genuinely new creative capability—using a reference image to anchor video generation—for most fal.ai video models. It is a complete, user-visible workflow capability extending an existing block. Alternatives: Higgsfield integration (v0.9.47, different release tag), security hardening (internal, no user-visible capability change), CSV leading-zero fix (narrower scope), Chat Human-in-the-Loop fix (bug restoration), Atlassian/Notion multi-account fix (secondary). No candidates share the v0.9.48 tag, so no 'Also in' section.

## Proposed article

Sim's Video Generator block accepts a start frame image for fal.ai models with image-to-video support, so agents can generate video that begins from a chosen image.

The Video Generator block accepts an optional start frame for fal.ai models that support image-to-video. When available, a start frame input appears in the block panel. Attach an image and the block switches to the model's image-to-video mode—duration, aspect ratio, resolution, audio, and prompt optimizer settings update to match, and options the image mode does not accept are hidden. Models such as Kling and Veo support start frames; selecting a model without image-to-video support returns a clear error.

Connect your fal.ai account and open the Video Generator block. [Video Generator block docs](https://docs.sim.ai/workflows/blocks/agent). Check each model's fal.ai documentation for specific supported settings.

## Editorial review

- Removed 'now' from summary, body, social, and email per editorial policy against rollout language in automatic drafts.
- Simplified 'endpoint' language to 'mode' in public copy for readability; kept 'endpoint' only in claims where precision matters.
- Named Kling and Veo as representative model families based on PR test cases (Kling v3 Pro and Veo 3.1); asked question to confirm these are the best examples.
- The docs link points to the generic agent block page—question asks whether a dedicated Video Generator page exists. This is the only verified link that appears relevant.
- Added note in proof_limit about verifying model-switching behavior after a frame is attached, matching the PR's reviewer guidance.
- The PR states 94 of 112 catalog models have image-to-video support; this count is kept in claims for evidence but excluded from public copy per operation-count guideline.

## Source evidence

- The Video Generator block routes to a fal.ai model's image-to-video endpoint when a start frame is attached and hides settings the image endpoint does not accept. — simstudioai/sim#9761
- Models without an image-to-video endpoint reject a start frame with a clear error instead of a generic 'Unknown model' failure. — simstudioai/sim#9761
- Duration, aspect ratio, resolution, audio, and prompt optimizer dropdowns update to reflect the endpoint that will run when a start frame is present. — simstudioai/sim#9761
- The start frame input is shown in the block UI only for fal.ai models that have an image-to-video sibling endpoint (94 of 112 catalog models per PR). — simstudioai/sim#9761

- https://github.com/simstudioai/sim/pull/9761

## Availability and open questions

- [ ] Can the start frame be provided as a workflow variable or only via direct upload/URL input in the block UI?
- [ ] Is the 5 MB start frame size limit enforced at the block UI level, the tool level, or both?
- [ ] Which fal.ai model families are most commonly used with image-to-video—Kling and Veo are named in test cases; are there others worth highlighting?
- [ ] Has conditional field visibility been verified in a running build, as the PR requests?
- [ ] Is there a dedicated docs page for the Video Generator block, or should the generic agent block docs link be used?

## Links checked during drafting

- [Video Generator block docs](https://docs.sim.ai/workflows/blocks/agent)

## Media production

Format: video · 25 seconds
Subject: Video Generator block with fal.ai model and start frame image attached
Starting state: Video Generator block open in a workflow, fal.ai model selected, no start frame attached
Action: User attaches a start frame image; block UI updates to show image-to-video-compatible settings
Visible result: Block panel shows start frame thumbnail and updated settings (duration, aspect ratio, etc.) ready to run
Poster: Block panel with start frame thumbnail visible and settings dropdowns updated for image-to-video
Framing: Block panel at 390px width, settings clearly readable, start frame thumbnail visible
Demonstration limits: Capture requires a real fal.ai credential configured in settings and a fal.ai model with image-to-video support selected (e.g. Kling v3 Pro or Veo 3.1). Do not use placeholder keys or fabricate UI state. Verify conditional field visibility: start frame input should appear only for supported models, and switching models after a frame is attached should update or hide settings correctly.

Record a short screen capture of the Video Generator block with a fal.ai model selected, showing a start frame image attached and block settings updating to reflect image-to-video mode. End on the configured block ready to run, with the start frame thumbnail and applicable settings visible.

1. Open a workflow with a Video Generator block and a fal.ai model selected (e.g. Kling v3 Pro or Veo 3.1)
2. Attach a sample start frame image—show the block panel updating to display image-to-video settings (duration, aspect ratio, resolution dropdowns appropriate to the image endpoint)
3. Hold on the configured block showing the start frame thumbnail and active settings, ready to run

Suggested alt text: Sim Video Generator block with a fal.ai model selected and a start frame image attached, showing image-to-video settings in the block panel

- [ ] Independently verify the feature and rollout; record evidence and limitations.
- [ ] Review a product capture, verified diagram, or original editorial illustration; retain capture or generation provenance.
- [ ] Choose the final image or video poster; verify it reads clearly at 390px. Candidate assets are not approved media.
- [ ] Add optimized versioned media, captions if spoken, and index.mdx with draft: true.
- [ ] Verify the final media on desktop and mobile and run the content audit.
- [ ] Feature owner confirms availability; editor approves copy and links.
- [ ] After the approved site deployment, verify article, media, RSS and sitemap before marking published.

## Announcement drafts

**Social**

Sim's Video Generator block supports start frame images for fal.ai models with image-to-video. Attach a reference image and the block switches to image-to-video mode, updating available settings to match. Connect your fal.ai account to try it.

**Email**

The Video Generator block in Sim accepts a start frame image for fal.ai models that support image-to-video. Attach an image and the block switches to the correct mode, showing only applicable settings. Open the Video Generator block in your workflow to use it.

Final canonical URL is assigned when the reviewed article slug is chosen. Do not distribute these drafts before publication.

Editorial contract: apps/sim/content/changelog/README.md and editorial-standard.md. This brief is public repository content; keep private operational evidence in Sim.
