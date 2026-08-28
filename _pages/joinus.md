---
layout: page
title: join us
permalink: /joinus/
description:
nav: true
nav_order: 6

hero_image: /assets/img/joinus_hero_arch.jpg
hero_alt: The top of the Washington Square Arch lit up at night, Greenwich Village, New York City
---

The Rocha Lab is committed to build a supportive, inclusive, and collaborative training environment. We are a small, new group at NYU Biology looking for curious, motivated people with diverse perspectives and backgrounds, at every career stage.

Our campus at NYU Arts & Science lies at the heart of the coolest neighborhood of the vibrant, multicultural New York city (Greenwich Village). We also have connections and ongoing collaborations with the American Museum of Natural History.

### Graduate Students

NYU is always looking for students with passion for multi-disciplinary research to address fundamental questions in Biology. Interested students are encouraged to read the Graduate Student resources online and email [Joana](mailto:joana.rocha@nyu.edu) to discuss opportunities prior to applying to the [NYU Biology PhD program](https://as.nyu.edu/departments/biology/academics/phd/applying-to-the-phd-program.html). If you are already an NYU PhD student interested in rotating, reach out with a description of your research interests and CV.

### Postdoctoral Researchers

We welcome postdocs with strong background in evolutionary ecology and genomics. If you are interested in joining our team please email [Joana](mailto:joana.rocha@nyu.edu) to discuss opportunities, even if there are no advertised positions. Though we occasionally post internally-funded positions, we don't currently have funding to support additional postdoctoral researchers. All prospective postdocs are encouraged to apply for independent funding and we are always willing to work with motivated people to identify funding sources. If you are interested in being hosted in our lab with a fellowship, contact [Joana](mailto:joana.rocha@nyu.edu) at least half a year in advance of a fellowship deadline. Please include a 1) CV and a 2) brief description of your research/career interests and why the lab is a good fit and 3) contact information for 2–3 references.

### Undergraduate, Master's students and Visiting Scholars

We have limited spaces available for undergraduate students outside NYU CAS Biology for Fall and Spring semesters. Please email [Joana](mailto:joana.rocha@nyu.edu) with your CV and a short description of your research interests. Be respectful: don't use AI.

<h2 class="lab-gallery-heading">Lab life gallery</h2>

<style>
  .lab-gallery-heading {
    font-size: 1.6rem;
    font-weight: 600;
    color: var(--global-theme-color);
    border-bottom: 1px solid var(--global-divider-color);
    padding-bottom: 0.35rem;
    margin-top: 3rem;
    margin-bottom: 1.25rem;
  }
  .lab-gallery {
    display: flex;
    flex-wrap: wrap;
    gap: 1.25rem;
    align-items: flex-start;
    margin-top: 1rem;
  }
  .lab-gallery__card {
    flex: 0 1 320px;
    margin: 0;
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 12px;
  }
  .lab-gallery__title {
    font-weight: 700;
    color: var(--global-text-color);
    margin-bottom: 0.6rem;
  }
  .lab-gallery__media {
    display: block;
    width: 100%;
    border-radius: 8px;
    background: #000;
  }
</style>

<div class="lab-gallery">
  <figure class="lab-gallery__card">
    <figcaption class="lab-gallery__title">Board games night</figcaption>
    <video class="lab-gallery__media" loop muted autoplay playsinline preload="auto">
      <source src="{{ '/assets/video/lab_life.mp4' | relative_url }}" type="video/mp4">
    </video>
  </figure>
</div>

<script>
  // Keep the lab-life clip looping forever, restarting if a browser lets it end
  // and resuming when the tab becomes visible again.
  (function () {
    var v = document.querySelector(".lab-gallery__media");
    if (!v) return;
    v.muted = true;
    v.loop = true;
    function play() {
      var p = v.play();
      if (p && p.catch) p.catch(function () {});
    }
    v.addEventListener("ended", function () {
      try {
        v.currentTime = 0;
      } catch (e) {}
      play();
    });
    v.addEventListener("pause", function () {
      if (!document.hidden) play();
    });
    document.addEventListener("visibilitychange", function () {
      if (!document.hidden) play();
    });
    play();
  })();
</script>
