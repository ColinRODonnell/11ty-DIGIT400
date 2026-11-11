---
title: Gallery
tags: section
order: 0
---
<is-land on:visible>

<div id="gallery" v-scope="{ active: 'all' }">
  <div class="filters">
    <button @click="active = 'all'" :class="{ on: active === 'all' }" :aria-pressed="String(active === 'all')">All</button>
    <button @click="active = 'general'" :class="{ on: active === 'general' }" :aria-pressed="String(active === 'general')">General AI Copyright Info</button>
    <button @click="active = 'should'" :class="{ on: active === 'should' }" :aria-pressed="String(active === 'should')">AI Should Copyright</button>
    <button @click="active = 'shouldnot'" :class="{ on: active === 'shouldnot' }" :aria-pressed="String(active === 'shouldnot')">AI Shouldn't Copyright</button>
  </div>
  <section class="topic" v-show="active === 'all' || active === 'general'">
    <h3>General AI Copyright Info</h3>
    <img src="img/general/ai-face.jpg" alt="ai face">
    <img src="img/general/brain.png" alt="brain">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'should'">
    <h3>AI Should be able to Copyright</h3>
    <img src="img/approve-ai/city.jpg" alt="city">
    <img src="img/approve-ai/learn.png" alt="learn">
  </section>
  <section class="topic" v-show="active === 'all' || active === 'shouldnot'">
    <h3>AI Should not be able to Copyright</h3>
    <img src="img/deny-ai/bad.png" alt="bad">
    <img src="img/deny-ai/bubble.jpg" alt="bubble">
  </section>
</div>

  <template data-island>
    <script type="module">
      import { createApp } from './js/petite-vue.js'
      createApp().mount('#gallery')
    </script>
  </template>

</is-land>