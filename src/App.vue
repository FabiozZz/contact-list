<template>
  <div class="app">
      <post-form @create="createPost"/>
    <post-list 
    :posts="posts"/>
  </div>
</template>
<script>
import PostForm from '@/components/PostForm'
import PostList from '@/components/PostList'
export default {
    components:{
        PostList,PostForm
    },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "Пост о JavaScript",
          description: "JavaScript - универсальный язык программирования",
        },
        {
          id: 2,
          title: "Пост о HTML",
          description: "HTML - единственно доступный язык разметки",
        },
        {
          id: 3,
          title: "Пост о CSS",
          description:
            "CSS - язык форматирования, оформления внешнего вида сайта",
        },
        {
          id: 4,
          title: "Пост о PHP",
          description: "PHP - серверный язык программирования",
        },
      ],
    };
  },
  methods: {
    createPost(post) {
        this.posts.push(post)
    },
  },
};
</script>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.app {
  padding: 20px;
}

</style>
