---
layout: page
permalink: /publications/
title: publications
description:
nav: true
nav_order: 4
---

<!-- _pages/publications.md -->

<p class="pub-legend">
  <strong>Bold</strong> denotes first or co-first author
  <span class="pub-legend-sep">|</span>
  <span class="pub-legend-underline">Underlined</span> denotes co-author
</p>

<div class="publications">

{% bibliography %}

</div>

<script>
  // Group the year-by-year bibliography under career-stage subtitles. The
  // bibliography is rendered server-side as a flat sequence of year headers
  // (descending), so we insert each subtitle before the year that starts a
  // stage: 2026 (NYU), 2025 (postdoc, covers 2024–2025), 2023 (PhD, 2021–2023).
  document.addEventListener("DOMContentLoaded", function () {
    var stages = {
      "2026": "Joana’s work since joining NYU Biology",
      "2025": "Joana’s PostDoc work at the University of California, Berkeley",
      "2023": "Joana’s PhD work at the University of Porto and UC Berkeley",
    };
    document.querySelectorAll(".publications h2.bibliography").forEach(function (yearHeader) {
      var label = stages[yearHeader.textContent.trim()];
      if (!label) return;
      var subtitle = document.createElement("h2");
      subtitle.className = "career-stage";
      subtitle.textContent = label;
      yearHeader.parentNode.insertBefore(subtitle, yearHeader);
    });
  });
</script>
