---
layout: default
title: Home
---

# Welcome to My Blog 👋

Glad you're here!

<!-- Inline HTML is allowed in Markdown files -->
<script>
  window.onload = async function collectName() {
    try {
      const name = prompt("Hey! What's your name?");
      if (!name) return;

      const response = await fetch("https://name-collector.onrender.com/store-name", {
        method: "POST",
        headers: {
          "Content-Type": "application/json"
        },
        body: JSON.stringify({ name })
      });

      if (response.ok) {
        console.log("Name submitted successfully!");
      } else {
        console.warn("Failed to submit name. Server responded with status:", response.status);
      }
    } catch (error) {
      console.error("Error submitting name:", error);
    }
  };
</script>
