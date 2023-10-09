---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
address: |
  <inhoinno@vt.edu>\
  [linkedin.com/in/inhoinno](https://www.linkedin.com/in/inhoinno)\
  [github.com/inhoinno](https://github.com/inhoinno)
---

::: rSection
OBJECTIVE

I'm a Computer Science Ph.D. student at Virginia Tech. I am broadly
interested in computer systems, especially \"How to design a scalable,
high performance storage systems\".\
My research interests include but are not limited to, SSD(solid-state
device), file system, CXL(compute express link), operating system, and
flash-centric systems for AI applications(NDP).
:::

::: rSection
Education **Ph.D. in Computer Science** *Virginia Tech* *Aug. 2023 -*

::: itemize
**Research Topic: Storage System** Co-advised by Huaicheng Li and Sam H.
Noh
:::

**Master's Degree in Computer Science** *Dankook University* *Graduated
in Aug. 2023*

::: itemize
**Research Topic: ZNS SSD Internals and Filesystem** GPA 4.4/4.5
Advisor: Jongmoo Choi
:::

**Visiting Scholar** *Syracuse University* *July -- Dec. 2022*

::: itemize
Electrical Engineering and Computer Science Co-advised by Bryan S. Kim
and Jongmoo Choi
:::

**Bachelor of Computer Science** *Dankook University* *Graduated in Feb.
2022*

::: itemize
Department of Software GPA 4.06/4.5
:::
:::

::: rSection
Patent

Jongmoo Choi, Samuel Woo, and **Inho Song** *Korea: filed*\
**Method for analyzing vehicle forensic and computing device for
execution the same** *10-2022-0139234*
:::

::: rSection
research project

**Building a Big Data System with Next-generation SSD***funded by IITP
(2022 -- 2030)*

-   This is the **StarLab project in IITP**. There are numerous studies
    about next-generation SSD focusing on the bottleneck of the existing
    storage system. I am **expecting to provide higher isolation
    support** and **stable tail latency with HW-SW co-design.**

-   **Expected impact**:

    1.  **Achieve optimal throughput** with **lower garbage collection
        overhead** and **lower write amplification factor.** (Motivated
        by F2FS\[1\] and ZNS\[2\])

    2.  **Supports high isolation among tenants with scalable design.**
        (Inspired by MAX\[3\] and Tectonic\[4\])

**Design Tradeoff in ZNS SSD** *funded by SK Hynix(2020-2022)*

-   This is research for ZNS SSD internals. The main goal of this work
    is to **show the design tradeoff in ZNS SSD** with **a reliable ZNS
    emulator.**

-   **Impact**:

    1.  **This ZNS emulator** shows **under 6-17% error rate** on
        average which is accurate performance compared to the real
        device.Based on this software, 3 main lessons are uncovered
        which **motivates the existing ZNS ecosystem.**

    2.  This work shows the **tradeoff between different designs in
        ZNS.** However, it also uncovers that **existing ZNS ecosystems
        are unaware of this tradeoff in ZNS.**

**Semantic-aware Vehicle Forensic** *funded by SPO(2020-2021) and
IITP(2022)*

-   According to
    [Google](https://www.kurzweilai.net/googles-self-driving-car-gathers-nearly-1-gbsec),
    modern vehicles are now generating about 1GB of data every second.
    This emerging field is not only in the spotlight of the forensic
    investigation field but also for the storage systems. After
    recognizing significant results, the project grows more important.
    This work motivated development of a forensic big data system that
    is useful to SPO and national police organizations.

-   **Impact**:

    1.  Based on a holistic approach to retrieving the artifacts from
        the vehicle, we found **critical artifacts that strongly imply
        the driver's or accompanies behaviors.**

    2.  This work shows that even if the driver deletes data in the
        vehicle, **data could still be retrieved** by physical dump with
        metadata analysis.

::: tiny
  -- ---------------------------------------------------------------------------------------------
     Changman Lee, et al., F2FS: A New File System for Flash Storage, FAST'15
     Matias Björling, et al., ZNS: Avoiding the Block Interface Tax for Flash-based SSDs, ATC'21
     Xiaojian Liao, et al., MAX: A Multicore-Accelerated File System for Flash Storage, ATC'21
     Satadru Pan, et al., Facebook's Tectonic Filesystem: Efficiency from Exascale, ATC'21
  -- ---------------------------------------------------------------------------------------------
:::
:::

::: rSection
SKILLS

  ------------------------------ -----------------------------------------------------------------------------------------------------------------------------------
  **Programming**                C/C++, Python, and Java
  **Systems**                    Linux Kernel, RocksDB, and F2FS
  **Open Source Contribution**   [FEMU ](https://www.usenix.org/conference/fast18/presentation/li)[(https://github.com/vtess/FEMU)](https://github.com/vtess/FEMU)
  ------------------------------ -----------------------------------------------------------------------------------------------------------------------------------

\
:::

::: rSection
Academic Awards and Achievements

-   Academic Excellence Scholarship *Fall Semester 2022*

-   Academic Excellence Scholarship *Spring Semester 2022*

-   Graduation Excellence Award *Dankook Univ. 2022*

-   Dean's List *Spring Semester 2020*

-   Academic Excellence Scholarship *Spring Semester 2020*

-   Dean's List *Fall Semester 2019*

-   Academic Excellence Scholarship *Fall Semester 2016*

-   Admission Scholarship *Spring Semester 2015*
:::

::: rSection
Certification

-   **Teacher's Certificate** *Ministry of Education,*\
    The Secondary School Teacher(Grade II) of Information & Computer
    *Republic of Korea, 2022*
:::

::: rSection
Miscellaneous Activities

-   International Joint Workshop for High-Potential Individuals Global
    Training Program *IITP 2022*

-   CPU cache simulator [\[Git\]](https://github.com/inhoinno/CacheSim)
    *2021*

-   Dankook university data analysis AI contest (Rank: 13/400) *DACON
    2021*

-   Camino de Santiago *Santiago Compostella, Spain, 2018*

-   Military service in Republic of Korea Army *Republic of Korea, Jan.
    2017 -- Oct. 2018*

    -   Special Warrior Certification

-   **Editor**, Consulate General of the Republic of Korea in Jeddah
    *Jeddah, Saudi Arabia, Sep. -- Dec. 2016*
:::

<!-- 
---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* B.S. in GitHub, GitHub University, 2012
* M.S. in Jekyll, GitHub University, 2014
* Ph.D in Version Control Theory, GitHub University, 2018 (expected)

Work experience
======
* Summer 2015: Research Assistant
  * Github University
  * Duties included: Tagging issues
  * Supervisor: Professor Git

* Fall 2015: Research Assistant
  * Github University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
--> 
