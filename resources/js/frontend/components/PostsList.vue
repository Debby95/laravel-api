<template>
    <div class="row row-cols-3">
        <div class="col" v-for="post in posts" :key="posts.id">
            <div class="card" style="width: 18rem;">
                <img :src="post.cover_img" class="card-img-top" alt="...">
                <div class="card-body">
                    <h5 class="card-title">{{post.title}}</h5>
                    <p class="card-text" v-html="post.content"></p>
                    <a href="#" class="btn btn-primary">Go somewhere</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

    export default {
        data() {
            return {
                posts: []
            }
        },
        methods: {
            fetchPosts(){
                axios.get("api/posts")
                .then((resp) => {
                    this.posts = resp.data
                })
            }
        },
        mounted() {
            this.fetchPosts();
        }
    }
</script>