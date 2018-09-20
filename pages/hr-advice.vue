<template>
  <div class="">
    <!-- <GlobalHeader/> -->
    <div class="">
      <div class="">
        <div class="">
            <div class="">
                <PostPreview v-for="(post, i) in posts" :post="post" :key="i" />
            </div>
            <div class="">
                email signup
                dates
            </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script>
import GlobalHeader from '~/components/partials/GlobalHeader';

export default {
  layout: 'blog',
  components: {
    GlobalHeader,
  },
  asyncData: async ({ app }) => ({
    posts: await app.$content('/posts').getAll(),
  }),
};
</script>


