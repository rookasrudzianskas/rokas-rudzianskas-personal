<template>
  <section class="scene-intro" id="intro">
    <div class="static-container">
      <h1 class="title">
        <span class="iuri">hi</span>
        <span class="func">.rokas()</span>
      </h1>

      <TextBlock>
        <p class="-purple">Rokas Rudzianskas</p>
        <p class="-gray">
          Hi! 👋 I craft awesome things for awesome people!<br />
          I'm a full-stack developer. Known for my whimsical creations, ability to context switch, and deliver innovative solutions.
        </p>
      </TextBlock>
    </div>
  </section>
</template>

<script>
import TextBlock from '../TextBlock.vue'

export default {
  name: 'IntroScene',
  components: { TextBlock },
}
</script>
