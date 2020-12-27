<template>
  <div class="post" v-if="post">
    <article>
        <b-container>

      <div class="image">
        <img :alt="post.fields.title" :src="`${post.fields.image[0].fields.file.url}?w=1680&h=750&fit=crop`">
      </div>
      <div class="content-wrapper">
        <h2>{{ post.fields.title }}</h2>
        <div class="content" v-html="post.fields.content.html"></div>
      </div>
        </b-container>

    </article>
  </div>
</template>

<script>
  import Comfortable from 'comfortable-javascript';
  import { comfortable } from '@/comfortable.js'

  export default {
    name: 'blogPost',
    data() {
      return {
        post: null,
        author: null,
      }
    },
    methods: {
      getPost() {
        const options = {
          embedAssets: true,
          includes: 1,
          filters: new Comfortable.Filter()
            .addAnd('slug', 'equal', this.$route.params.slug)
        };

        comfortable.getDocuments(options)
        .then(result => {
          this.post = result.data[0];
        })
        .catch(err => {
          throw err;
        })
      }
    },
    created() {
      this.getPost();
    }
  }
</script>

<style>
  .post .image{
    width: 100%;
  }

  .post .image img{
    width: 100%;
  }

  .post .author img {
    margin-top: 10px;
  }

  .post .author img {
    display: inline-block;
    margin-bottom: -8px;
    margin-right: 10px;
    border-radius: 50%;
  }
</style>
