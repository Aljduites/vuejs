/* eslint-disable */
<template>
  <div class="home flex flex-col">
    <div v-for="post in posts">
      <blog-post
        :key="post.id"
        :title="post.title"
        @enlarge-text="enlargeText"
        :style="{ fontSize: postFontSize + 'em' }">
        {{ post.content }}</blog-post>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import ButtonCounter from '@/components/ButtonCounter';
import BlogPost from '@/components/BlogPost';

export default {
  name: "home",
  data () {
    return {
      posts: [
        { id: 1, title: 'Compoenent Design', content: 'lorem ipsum' },
        { id: 2, title: 'API Call', icon: '😁', content: 'lorem ipsum' },
        { id: 3, title: 'Introduction to Vuex', content: 'lorem ipsum' },
      ],
      postFontSize: 0.9,
    }
  },
  components: {
    HelloWorld,
    ButtonCounter,
    BlogPost,
  },
  methods: {
    enlargeText (fontSize) {
      this.postFontSize = fontSize
      console.log(this.postFontSize)
    }
  }
};
</script>
