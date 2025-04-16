---
layout: default
title: Home
---

# Welcome to My Blog 👋

Glad you're here!

<!-- Inline HTML is allowed in Markdown files -->
<script>
  async function collectName() {
    const name = prompt("Hey! What's your name?");
    if (name) {
      await fetch("https://name-collector.onrender.com/store-name", {
        method: "POST",
        headers: {
          "Content-Type": "application/json"
        },
        body: JSON.stringify({ name })
      });
    }
  }

  window.onload = collectName;
</script>
