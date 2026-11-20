# Power Automate documentation and training

An interactive, hand-drawn, 14-step walkthrough of a Power Automate flow that imports mentions from a fictional media service, Pulsewire, into a SharePoint list.

Click + and the next step draws in. Each step opens a card anchored to it with a dotted leader. The card explains what the step does, why it is there (tied to the previous and next steps and the overall goal), and how to configure it. Three of the steps include a quick knowledge check. You answer the check before the next step unlocks. The finish screen recaps three guardrails and shows a doughnut chart of the seven checks from testing.

## Demo

[Open Power Automate documentation and training](https://anandragav.github.io/copilot-html-dashboards/build-the-flow/)

## Use it in SharePoint

1. Download [`build-the-flow.html`](build-the-flow.html). This is the SharePoint-ready file.
2. In your SharePoint site, open Site Pages and upload the HTML page.
3. The page uses the SharePoint-provided D3 and Chart.js libraries through the library manifest in the file. You do not need to add those libraries yourself.

## Make one from your own flow

[Download the Copilot in SharePoint skill](power-automate-documentation-and-training.zip) (`power-automate-documentation-and-training.zip`).

1. Unzip it and add the `power-automate-documentation-and-training` folder to your site's Agent Assets > Skills library.
2. Export your cloud flow (My flows > Export > Package (.zip)), upload the zip to a document library, and give Copilot in SharePoint the link.
3. Copilot plays back the flow, asks you to approve the masking and a few questions, then builds a page like this one from the bundled template.

## Files in this folder

The GitHub Pages demo and the SharePoint upload are two files, because hosts outside SharePoint do not honor the library manifest.

- `index.html` is the GitHub Pages demo. It keeps the same library manifest, so it still works if you upload it to SharePoint. Outside SharePoint, a small loader fetches D3 7.9.0 and Chart.js 4.6.1 from jsDelivr only when `window.d3` or `window.Chart` is missing.
- `build-the-flow.html` is the SharePoint-ready copy for upload to Site Pages. It expects SharePoint to supply D3 and Chart.js.
- `power-automate-documentation-and-training.zip` is the Copilot in SharePoint skill that builds pages like this one.
