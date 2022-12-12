<template>
  <div class="ghibliScene">
    <SceneSection id="Ghibli">
      <TextBlock>
        <p>
          It took me a while to get to this point, but I'm finally here. Through this process, I learned:
          <span class="-big -purple">
            Craft Web-Based apps, Web/Mobile animating techniques and building my own brand.
          </span>
          There are many things I want to learn, I am super excited to see what the future holds for me!
        </p>
      </TextBlock>

      <template #container>
        <div class="sky">
          <div class="cloud c1"></div>
          <div class="cloud c2"></div>
        </div>

        <HolwsCastle :isPlaying="isPlaying" />

        <div class="grass1"></div>
        <div class="grass2"></div>
      </template>
    </SceneSection>
    <SceneSection id="Ghibli2" />
    <SceneSection id="Ghibli3">
      <TextBlock>
        <p>
          Through these years, I built a few innovative projects, I am happy to share.
        </p>
        <p class="-big">
          My First & Failed Startup (at age 17):
          <span class="-purple"
            >BrainlyEmails.</span
          > <br />
          Feedback toolbox: <span class="-purple">QuickFeedback.</span>
          <br />
          My Tech Brand at age 18: <span class="-purple">@RokasRudzianskas.</span>
        </p>
        <p>
          All of these projects have a major impact on how I start and develop
          my creative processes, leading the way on how I view web and app development
          today.
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="Ghibli4" />
  </div>
</template>

<script>
import HolwsCastle from '../Characters/HolwsCastle/HolwsCastle.vue'
import SceneSection from '../SceneSection.vue'
import TextBlock from '../TextBlock.vue'

export default {
  name: 'GhibliScene',
  props: {
    isPlaying: Boolean,
  },
  components: { TextBlock, SceneSection, HolwsCastle },
}
</script>

<style lang="scss">
.ghibliScene {
  .castle-container {
    position: absolute;
    top: 70%;
    left: 100%;
    transform: scale(0.5);

    @media screen and (max-width: 568px) {
      transform: scale(0.3);
    }
  }

  .sky {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;

    .c1 {
      position: absolute;
      transform-origin: left bottom;
      bottom: 0;
      left: 0;
      width: 45vw;
      height: 50vh;
      background: url('../../components/Characters/HolwsCastle/assets/cloud1.png')
        no-repeat 0 bottom;
      background-size: contain;
    }

    .c2 {
      position: absolute;
      transform-origin: right bottom;
      bottom: 0;
      right: 0;
      width: 60vw;
      height: 60vh;
      background: url('../../components/Characters/HolwsCastle/assets/cloud2.png')
        no-repeat right bottom;
      background-size: contain;
    }

    @media screen and (max-width: 768px) {
      .c1,
      .c2 {
        width: 100vw;
        height: 90vh;
        background-size: 100% auto;
      }
    }
  }

  .grass1 {
    transform-origin: left bottom;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 50vw;
    height: 25vh;
    transform: scale(1.2);
    background: url('../../components/Characters/HolwsCastle/assets/grass1.png')
      no-repeat 0 bottom;
    background-size: contain;
    filter: blur(2px);
  }

  .grass2 {
    transform-origin: right bottom;
    position: absolute;
    bottom: 0;
    right: 0;
    width: 40vw;
    height: 20vh;
    transform: scale(1.2);
    background: url('../../components/Characters/HolwsCastle/assets/grass2.png')
      no-repeat right bottom;
    background-size: contain;
    filter: blur(2px);
  }
}
</style>
