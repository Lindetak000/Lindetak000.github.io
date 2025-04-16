---
layout: default
title: Home
---

# Welcome to My Blog 👋

Glad you're here!

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
        alert("Thanks, " + name + "! Your name has been saved.");
      } else {
        alert("Oops! Something went wrong. Please try again later.");
      }
    } catch (error) {
      alert("Network error — couldn't send your name. Please check your connection.");
    }
  };
</script>
