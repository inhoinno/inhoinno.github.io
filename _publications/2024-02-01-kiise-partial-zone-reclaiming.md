---
title: "Overcoming a Zone Reclaiming Overhead with Partial-Zone Reclaiming"
collection: publications
permalink: /publication/2024-02-01-kiise-partial-zone-reclaiming
excerpt: "A partial-zone reclaiming technique that interleaves in-flight host requests with the zone reclaiming process to mitigate reclaim-induced tail latency. Improves host request latency by up to 8% on average and reduces zone reclaiming time by up to 41%."
date: 2024-02-01
venue: "Journal of KIISE: Computer Systems and Theory, Vol. 51, No. 2, pp. 115–124"
paperurl: "https://dspace.kci.go.kr/handle/kci/2110970"
citation: "Inho Song, Wonjin Lee, Jae-Dong Lee, Seehwan Yoo, and Jongmoo Choi. &quot;Overcoming a Zone Reclaiming Overhead with Partial-Zone Reclaiming.&quot; <i>Journal of KIISE: Computer Systems and Theory</i>, vol. 51, no. 2, pp. 115–124, 2024. (Korean)"
---

**Inho Song**, Wonjin Lee, Jae-Dong Lee, Seehwan Yoo, and Jongmoo Choi. *Journal of KIISE: Computer Systems and Theory*, 51(2):115–124, 2024. (Korean journal article.)

- [KCI record](https://dspace.kci.go.kr/handle/kci/2110970)

### Abstract

Zone reclaiming on ZNS SSDs is a heavyweight operation that delays in-flight host requests while the zone is being reclaimed. We propose **Partial-Zone Reclaiming**, which interleaves the reclamation process with in-flight host I/O rather than blocking it end-to-end. In our experiments, partial-zone reclaiming improves host request latency by up to 8% on average and reduces zone reclaiming time by up to 41%.
