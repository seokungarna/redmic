<template>
  <div class="content">
    Postad {{ post.date.toLocaleString('sv_SE') }}.
    <template v-if="post.timeToRead">
      <strong  v-if="post.timeToRead > 1">{{ post.timeToRead }} minuters läsning.</strong>
      <strong  v-if="post.timeToRead == 1">{{ post.timeToRead }} minuts läsning.</strong>
    </template>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      default() {
        return {};
      },
    },
  },
};
</script>
