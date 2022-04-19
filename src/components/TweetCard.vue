<template>
    <div>
        <p>{{username}}</p>
        <h5>{{content}}</h5>
        <h6>{{dateCreated}}</h6>
    </div>
</template>

<script>
    export default {
        name : "TweetCard",
        props: {
            username: String,
            content: String,
            dateCreated: String
        }
    }
</script>

<style scoped>

div {
    box-sizing: border-box;
    border: none;
    box-shadow: 1px 2px 2px #383838;
    height: 150px;
    width: 300px;
    scroll-behavior: smooth;
    list-style: none;
}
img {
    height: 50px;
    width: 50px;
    border-radius: 50%;
    border: 2px red solid;
    }
    
</style>