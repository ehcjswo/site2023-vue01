<template>
  <div class="youtube__cont container">
    <ul>
      <li v-for="(youtube, index) in youtubes" :key="index">
        <a
          :href="`https://youtube.com/watch?v=${youtube.id.videoId}`"
          target="_blank"
        >
          <img
            :src="youtube.snippet.thumbnails.medium.url"
            :alt="youtube.snippet.title"
          />
          <em>
            <span class="title">{{ youtube.snippet.channelTitle }}</span>
          </em>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    youtubes: {
      youtubes: {
        type: Array,
        required: true,
      },
    },
  },
};
</script>

<style lang="scss">
.youtube__cont {
  ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    margin-bottom: 100px;

    li {
      width: 24.333%;
      margin-bottom: 4%;

      img {
        border-radius: 4px;
      }

      span {
        display: block;
        margin: 4px 0;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
      }
    }
  }
}
</style>
