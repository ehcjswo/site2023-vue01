<template>
  <main>
    <SliderSection attr="slider__wrap section nanum5" />
    <IntroSection attr="intro__wrap Nanum5 section bg-blue" />
    <PortSection attr="port__wrap Nanum5 section center bg-blue" />
    <YoutubeSection attr="youtube__wrap Nanum5 section" />
    <UnsplashSection attr="unsplash__wrap Nanum5 section bg-blue" />
    <MovieSection attr="movies__wrap Nanum5 container section" />
  </main>
</template>

<script>
import SliderSection from "@/components/section/SliderSection.vue";
import IntroSection from "@/components/section/IntroSection.vue";
import PortSection from "@/components/section/PortSection.vue";
import MovieSection from "@/components/section/MovieSection.vue";
import YoutubeSection from "@/components/section/YoutubeSection.vue";
import UnsplashSection from "@/components/section/UnsplashSection.vue";

export default {
  components: {
    IntroSection,
    SliderSection,
    PortSection,
    MovieSection,
    YoutubeSection,
    UnsplashSection,
  },
};
</script>
