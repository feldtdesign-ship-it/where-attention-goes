# Where Attention Goes

A scroll-driven page about how much of our time goes to social and video apps, and what is shifting.
It is a proof of a motion stack: smooth scroll, a 3D particle field, counters, and CSS scroll animation.

**Live page:** https://feldtdesign-ship-it.github.io/where-attention-goes/

## What it shows

- The weekly time people spend on social and video platforms, and who spends the most.
- Daily time in the biggest apps, and the scale of the audience, with one dot standing for 100 million people.
- Playing games while watching TV, and watching video at 2x speed.
- Where time is leaving the open web.

## How it is built

- One static page, no build step, no tracking, no cookies.
- Lenis for smooth scroll, GSAP ScrollTrigger for counters and scroll triggers, three.js for the particle field.
- CSS scroll-driven animation for the reveals and bars. Browsers without support, such as Firefox today, fall back to GSAP automatically.
- The "Hold to watch this page at 2x" button runs the whole page on a doubled clock while it is held, the same gesture as Instagram and TikTok.
- Fonts are self-hosted so line breaks match on every device.
- Reduced motion is respected. The page is still and fully readable.

Test switches: add `?fx=gsap` to force the JavaScript motion layer, add `?reduce=1` to simulate reduced motion, and press `P` for a frame meter.

## Run it locally

Serve the folder, because the fonts load by URL:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000/.

## Sources and caveats

Every number on the page comes from one of these. Figures were checked against the source text on October 31, 2026, except the Instagram launch date, which comes from news coverage and was not checked against a page I opened.

- [DataReportal, Digital 2027 Global Overview](https://datareportal.com/reports/digital-2027-global-overview-report): weekly time (GWI), per-app daily time (Similarweb, August 2026, mobile apps only, excluding China), 5.81 billion social media user identities (may count some people more than once), 36+ hours a week in the Philippines, 24+ hours for ages 16 to 24, 12 countries above 24 hours, 3.24 billion generative AI users, ChatGPT 1.1 billion+.
- [DataReportal, The Steady Decline of the World Wide Web](https://datareportal.com/reports/digital-2027-the-steady-decline-of-the-web): the 11.2% fall is for the world's top 10,000 websites over 24 months (Similarweb), not all web time.
- [Pew Research Center, Teens, Social Media and AI Chatbots 2025](https://www.pewresearch.org/internet/2025/12/09/teens-social-media-and-ai-chatbots-2025/): 21% of US teens on TikTok almost constantly, up from 16% in 2022.
- [Meta, third quarter 2026 results](https://investor.atmeta.com/investor-news/press-release-details/2026/Meta-Reports-Third-Quarter-2026-Results/default.aspx): 3.64 billion daily active people, September 2026.
- [YouTube CEO on 200 billion daily Shorts views, via Tubefilter](https://www.tubefilter.com/2025/06/18/youtube-shorts-200-billion-daily-views-google-veo-3-ai-neal-mohan/amp/), June 2025. This is YouTube's own claim, one creator disputes it, and YouTube has not shared how it counts. The "2.3 million views a second" is simple division of that claim.
- [LG Ad Solutions, The Connected Gamer, via Advanced Television](https://www.advanced-television.com/2023/04/19/study-gamers-watch-more-fast-svod-than-ctv-owners/): 53% of US console gamers with connected TVs play games while streaming, fielded March 2023.
- [GWI via WARC](https://www.warc.com/content/article/warc-datapoints-gwi/44-of-sea-consumers-play-video-games-while-watching-tv/138701): 44% of Southeast Asian consumers play games while watching TV, August 2021.
- [YouTube, playback speed trends](https://blog.youtube/inside-youtube/youtube-watch-video-playback-speeds-trends): over 900 years of video time saved a day, and speed changes are speed-ups more than 85% of the time, June 2022 data.
- [Social Media Today](https://www.socialmediatoday.com/news/instagram-adds-2x-playback-reels/743749/): Instagram added 2x Reels playback in March 2025.

The statistics belong to their sources. Check the source before quoting a number.

## Third-party code

Loaded from public CDNs, not bundled in this repository:

- [GSAP](https://gsap.com/) and ScrollTrigger, under the [GSAP Standard License](https://gsap.com/standard-license/).
- [Lenis](https://github.com/darkroomengineering/lenis), MIT license.
- [three.js](https://github.com/mrdoob/three.js), MIT license.

Bundled in `fonts/`, under the SIL Open Font License 1.1 (license texts included):

- Newsreader
- Inter

## Reuse

All rights reserved for now. Open an issue if you would like to reuse the page or its code.
