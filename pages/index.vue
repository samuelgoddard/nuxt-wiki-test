<template>
  <div class="page-index">
    <GlobalHeader/>
    <div class="wrapper">
      <h2>Home</h2>
    </div>
  </div>
</template>

<script>
import GlobalHeader from '~/components/partials/GlobalHeader';

export default {
  layout: 'page',
  components: {
    GlobalHeader,
  },
  asyncData: async ({ app }) => ({
    text: await app.$content('/pages').get('/home'),
  }),
};
</script>
