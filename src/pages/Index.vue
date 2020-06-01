<template>
  <Layout>
    <div class="content has-text-centered">
     <h1>
      Välkommna till RedMic
    </h1>
    </div>
    <div class="posts">
      <PostCard
        v-for="edge in $page.posts.edges"
        :key="edge.node.id"
        :post="edge.node"
      />
    </div>
  </Layout>
</template>

<page-query>
query {
  posts: allPost(filter: { published: { eq: true }}) {
    edges {
      node {
        id
        title
        date (format: "D/M -YYYY")
        timeToRead
        description
        cover_image (width: 770, height: 380, blur: 10)
        path
        tags {
          id
          title
          path
        }
      }
    }
  }
}
</page-query>

<script>

import PostCard from '~/components/PostCard.vue';

export default {
  components: {
     PostCard,
  },
  metaInfo: {
    title: 'Home',
  },
};
</script>
