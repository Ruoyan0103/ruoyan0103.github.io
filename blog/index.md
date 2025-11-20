---
layout: default
title: Blog
---
# Blog Index

<div class="blog-index">

<div class="tree">
  <ul>

    <!-- Level 1 -->
    <li>
      <span class="toggle">ML Applications</span>
      <ul class="collapsed">

        <!-- Level 2 -->
        <li>
          <span class="toggle">Building Machine Learning Powered Applications</span>
          <ul class="collapsed">
            <li>
              <a href="contents/test.md">
                Nice to Know · 2025-11-17
              </a>
            </li>
          </ul>
        </li>

        <li>
          <span class="toggle">Deep Learning for Coders with Fastai and PyTorch</span>
          <ul class="collapsed">
            <li>
              <a href="contents/ML2P.html">
                From Model to Production—A simple demo · 2025-11-16
              </a>
            </li>
          </ul>
        </li>

      </ul>
    </li>

    <!-- Other root sections -->
    <li>Kaggle</li>
    <li>Insights</li>
    <li>Others</li>

  </ul>
</div>

<script>
  document.querySelectorAll(".toggle").forEach(t => {
    t.addEventListener("click", () => {
      t.classList.toggle("open");
      const nextUl = t.nextElementSibling;
      if (nextUl) nextUl.classList.toggle("collapsed");
    });
  });
</script>

</div>
