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

<!-- Typewriter effect for the header: types the name first, then the subtitle, then
     removes the caret from both. Runs early (before the publications list paints) to
     avoid a flash of the fully-rendered text. -->
<script>
  (function () {
    var title = document.querySelector(".post-header .post-title");
    var desc = document.querySelector(".post-header .desc");
    if (!title) return;
    // Respect users who prefer reduced motion: leave the text as-is, no animation.
    if (window.matchMedia && window.matchMedia("(prefers-reduced-motion: reduce)").matches) return;

    var titleText = title.textContent.replace(/\s+/g, " ").trim();
    var descText = desc ? desc.textContent.replace(/\s+/g, " ").trim() : "";
    // Blank both lines up front so neither flashes its final text before typing.
    title.textContent = "";
    if (desc) {
      desc.style.minHeight = desc.offsetHeight + "px"; // reserve space, avoid layout jump
      desc.textContent = "";
    }

    function type(el, text, speed, keepCursor, done) {
      var cursor = document.createElement("span");
      cursor.className = "tw-cursor";
      cursor.setAttribute("aria-hidden", "true");
      cursor.textContent = "|";
      el.appendChild(cursor);
      var i = 0;
      (function step() {
        if (i < text.length) {
          cursor.insertAdjacentText("beforebegin", text.charAt(i++));
          setTimeout(step, speed);
        } else {
          if (!keepCursor) cursor.remove(); // drop the caret unless this is the final line
          if (done) done();
        }
      })();
    }

    // Name at 110ms/char (caret moves on when done); subtitle 2x faster (55ms) and
    // keeps a blinking blue caret at the end.
    type(title, titleText, 110, false, function () {
      if (desc && descText) type(desc, descText, 55, true, null);
    });
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

<h2><a href="/news/" style="color: inherit">news</a></h2>
{% include news.liquid %}

## Selected Publications

{% include bib_search.liquid %}

<div class="publications">
{% bibliography %}
</div>

<!-- Visitor world map (MapMyVisitors). Only records visits on the live site. -->
<div class="mapmyvisitors-widget" style="text-align: center; margin-top: 2rem;">
  <script type="text/javascript" id="mapmyvisitors" src="https://mapmyvisitors.com/map.js?cl=ffffff&w=400&t=n&d=3rN61ber80qeVaChuc-YM5G0mQqSQPErALEyw17o7ag&co=a4aeb5&cmo=3acc3a&cmn=ff5353&ct=ffffff"></script>
</div>
