<template>
  <div>
    <div class="container">
      <div v-if="video" class="video-wrapper">
        <div class="vimeo-container">
          <iframe
            :src="
              'https://player.vimeo.com/video/' +
              video +
              '?api=1&autoplay=1&controls=0&sidedock=0&loop=1&title=0&byline=0&portrait=0&muted=1&background=1&quality=1080p'
            "
            frameborder="0"
            allow="autoplay; fullscreen; picture-in-picture"
            allowfullscreen
          ></iframe>
        </div>
        <!-- <script src="https://player.vimeo.com/api/player.js"></script> -->
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["src", "video"],
};
</script>
