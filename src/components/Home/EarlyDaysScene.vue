<template>
  <div class="earlyDays">
    <TitleSection scene="earlyTitle">
      <TitleFunction
        params="2011,2018"
        subtitle="&lt;table&gt;&lt;tr&gt;&lt;td&gt;..."
        >earlyDays</TitleFunction
      >

      <div class="clouds cloud-1"></div>
      <Pepe v-bind="{ isPlaying }" />
      <div class="clouds cloud-2"></div>
      <div class="clouds cloud-3"></div>
      <Ocean v-bind="{ isPlaying }" />
    </TitleSection>

    <SceneSection id="early-days">
      <TextBlock>
        <p>Rokas Rudzianskas | Design & illustration.</p>
        <p class="-big">
          Few years ago, I got into tech.<br />
          <span class="-purple">Today, it have changed my life forever.</span>
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days2">
      <TextBlock>
        <p class="-big">
          <span class="-purple">Programming</span> &<br />
          <span class="-purple">Creating Tech Content:</span><br />
          <span class="-purple">@TikTok</span> &
          <span class="-purple">@YouTube.</span>
        </p>
        <p>
          Few years ago, I jumped into tech, it was love from first sight.
          Through these years I worked on art and all sorts of creative interactions with Machine Learning,
          creating ThreeJS based web applications and mobile apps, and the guts of playing with OpenAI.
          <br />
        </p>
      </TextBlock>
    </SceneSection>
    <SceneSection id="early-days3">
      <TextBlock>
        <p>
          This journey, have opened many proud partnerships with the starring
          of some big Tech names such as:<br />
          <span class="-big -purple"
            ><em>Expo</em>, <em>Vercel</em>, Get-Stream,
            <em>Vox Implant</em></span
          >
          among many others...
        </p>
      </TextBlock>
    </SceneSection>
  </div>
</template>

<script>
import Pepe from '../Characters/Pepe/Pepe.vue'
import Ocean from '../Characters/Ocean/Ocean.vue'
import TitleSection from '../TitleSection.vue'
import TitleFunction from '../TitleFunction.vue'
import TextBlock from '../TextBlock.vue'
import SceneSection from '../SceneSection.vue'

export default {
  name: 'EarlyDaysScene',
  components: {
    TitleSection,
    Pepe,
    Ocean,
    TitleFunction,
    TextBlock,
    SceneSection,
  },
  props: {
    isPlaying: Boolean,
  },
}
</script>

<style lang="scss">
.earlyDays {
  .pepe {
    position: absolute;
    z-index: 2;
    top: 50%;
    left: 100%;
    transform: scale(0.4) translate3d(0, -50%, 0);
    transform-origin: 0 0;

    @media screen and (max-width: 568px) {
      transform: scale(0.2) translate3d(0, -50%, 0);
    }
  }

  .clouds {
    position: absolute;
    width: 150vw;
    height: 150vh;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transform-origin: 50% 50%;
    background: url('../Characters/Pepe/assets/clouds-1.png') no-repeat center;
    background-size: contain;
    opacity: 0.5;

    &.cloud-2 {
      background-image: url('../Characters/Pepe/assets/clouds-2.png');
    }

    &.cloud-3 {
      background-image: url('../Characters/Pepe/assets/clouds-3.png');
      width: 100vw;
      height: 100vh;
      z-index: -1;
      opacity: 0.25;
    }
  }
}
</style>
