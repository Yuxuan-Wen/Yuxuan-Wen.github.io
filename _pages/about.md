---
layout: about
title: about
permalink: /
subtitle: Ph.D. Student @ Duke University

profile:
  align: right
  image: yw_prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <div class="profile-social">
    <a href="mailto:yuxuan.wen@duke.edu" title="Email"><i class="fa-solid fa-envelope"></i></a>
    <a href="https://github.com/Yuxuan-Wen" title="GitHub" target="_blank" rel="external nofollow noopener"><i class="fa-brands fa-github"></i></a>
    <a href="https://www.linkedin.com/in/yuxuan-wen-b87977261" title="LinkedIn" target="_blank" rel="external nofollow noopener"><i class="fa-brands fa-linkedin"></i></a>
    <a href="https://scholar.google.com/citations?user=M9q_L8oAAAAJ" title="Google Scholar" target="_blank" rel="external nofollow noopener"><i class="ai ai-google-scholar"></i></a>
    </div>

selected_papers: false # full publication list is embedded below instead
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # rendered manually below (before Publications) instead of in the layout's default spot

latest_posts:
  enabled: false
---

<!-- LinkedIn-style header: build a banner + overlapping circular avatar at the top of
     the post by relocating al-folio's profile image. Runs early to avoid a layout flash. -->
<script>
  (function () {
    var post = document.querySelector(".post");
    var profile = document.querySelector(".profile");
    var header = document.querySelector(".post-header");
    if (!post || !profile || document.querySelector(".li-header")) return;
    var img = profile.querySelector("img");
    if (!img) return;
    var social = profile.querySelector(".profile-social");

    var li = document.createElement("div");
    li.className = "li-header";
    var banner = document.createElement("div");
    banner.className = "li-banner";
    var avatar = document.createElement("div");
    avatar.className = "li-avatar";
    avatar.appendChild(img); // move the existing profile photo into the avatar
    li.appendChild(banner);
    li.appendChild(avatar);
    post.insertBefore(li, post.firstChild); // banner + avatar at the very top

    if (social && header) {
      social.classList.add("li-social"); // left-align the icons under the name
      header.appendChild(social);
    }
    profile.style.display = "none"; // hide the now-empty right-aligned block
  })();
</script>

<!-- Typewriter effect for the header: the NAME stays static; only the subtitle types
     out (55ms/char) and keeps a blinking blue caret at the end. Runs early to avoid a
     flash of the fully-rendered subtitle. -->
<script>
  (function () {
    var desc = document.querySelector(".post-header .desc");
    if (!desc) return;
    // Respect users who prefer reduced motion: leave the subtitle as-is, no animation.
    if (window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches) return;

    var descText = desc.textContent.replace(/\s+/g, " ").trim();
    if (!descText) return;
    desc.style.minHeight = desc.offsetHeight + "px"; // reserve space, avoid layout jump
    desc.textContent = "";

    var cursor = document.createElement("span");
    cursor.className = "tw-cursor";
    cursor.setAttribute("aria-hidden", "true");
    cursor.textContent = "|";
    desc.appendChild(cursor);

    var i = 0;
    (function step() {
      if (i < descText.length) {
        cursor.insertAdjacentText("beforebegin", descText.charAt(i++));
        setTimeout(step, 55);
      }
      // leave the blinking caret at the end
    })();
  })();
</script>

I am a first-year Ph.D. student in [Biomedical Engineering](https://bme.duke.edu/) at Duke University, advised by [Prof. Timothy W. Dunn](https://www.tdunnlab.org/). My research focuses on AI/ML methods and foundation models.

Before Duke, I completed a concurrent B.S./B.Eng. in Electrical Engineering at the University of Cincinnati and Chongqing University.

During my undergraduate study, I was fortunate to conduct research at:

- [REHAssist](https://www.epfl.ch/labs/rehassist/) ([BioRob](https://www.epfl.ch/labs/biorob/)), EPFL — advised by [Dr. Mohamed Bouri](https://people.epfl.ch/mohamed.bouri)
- [Center for Robotics Research](https://www.ceas.uc.edu/research/centers-labs/center-for-robotics-research.html), UC — advised by [Prof. Janet Dong](https://researchdirectory.uc.edu/p/dongjg)
- [Meller Lab](https://folding.cchmc.org/), Cincinnati Children's — advised by [Prof. Jarek Meller](https://www.cincinnatichildrens.org/bio/m/jarek-meller)
- Dept. of Computer Science, CQU — advised by [Prof. Yunfei Yin](https://faculty.cqu.edu.cn/YunfeiYin/en/index.htm)

<!-- During my undergraduate study, I was fortunate to work with and be advised by [Dr. Mohamed Bouri](https://people.epfl.ch/mohamed.bouri) ([REHAssist](https://www.epfl.ch/labs/rehassist/), [BioRob](https://www.epfl.ch/labs/biorob/), [EPFL](https://www.epfl.ch/)), [Prof. Janet Dong](https://researchdirectory.uc.edu/p/dongjg) ([Center for Robotics Research](https://www.ceas.uc.edu/research/centers-labs/center-for-robotics-research.html), UC), [Prof. Jarek Meller](https://www.cincinnatichildrens.org/bio/m/jarek-meller) ([Meller Lab](https://folding.cchmc.org/), [Cincinnati Children's](https://www.cincinnatichildrens.org/)), and [Prof. Yunfei Yin](https://www.cqu.edu.cn/) (CQU). -->


Feel free to reach me by [email](mailto:yuxuan.wen@duke.edu) or [LinkedIn](https://www.linkedin.com/in/yuxuan-wen-b87977261/), and visit my [GitHub](https://github.com/Yuxuan-Wen).

<h2>Research Highlights</h2>
<div class="research-highlights">
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/autonomous_driving.gif' | relative_url }}" alt="Autonomous Driving" loading="lazy" /></div>
    <div class="rh-caption">Autonomous Driving</div>
  </div>
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/rep_learning.png' | relative_url }}" alt="Representation Learning" loading="lazy" /></div>
    <div class="rh-caption">Representation Learning</div>
  </div>
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/surgical_robotic.png' | relative_url }}" alt="Surgical Robotics and Medical Image Analysis" loading="lazy" /></div>
    <div class="rh-caption">Surgical Robotics &amp; Medical Image Analysis</div>
  </div>
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/docking.png' | relative_url }}" alt="ML for Drug Screening and Docking" loading="lazy" /></div>
    <div class="rh-caption">ML for Drug Screening &amp; Docking</div>
  </div>
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/underwater_robotic.gif' | relative_url }}" alt="Underwater Robotics" loading="lazy" /></div>
    <div class="rh-caption">Underwater Robotics</div>
  </div>
  <div class="rh-card">
    <div class="rh-media"><img src="{{ '/assets/img/research/neural.png' | relative_url }}" alt="Neural Behavior Foundation Model" loading="lazy" /></div>
    <div class="rh-caption">Neural Behavior Foundation Model</div>
  </div>
</div>

<h2><a href="/news/" style="color: inherit">news</a></h2>
{% include news.liquid %}

## Selected Publications

{% include bib_search.liquid %}

<div class="publications">
{% bibliography %}
</div>

<!-- Visitor world map (MapMyVisitors). Only records visits on the live site. -->
<div class="mapmyvisitors-widget" style="text-align: center; margin-top: 2rem;">
  <script type="text/javascript" id="mapmyvisitors" src="https://mapmyvisitors.com/map.js?cl=000000&w=300&t=tt&d=3rN61ber80qeVaChuc-YM5G0mQqSQPErALEyw17o7ag&co=ffffff&cmo=3acc3a&cmn=ff5353&ct=808080"></script>
</div>
