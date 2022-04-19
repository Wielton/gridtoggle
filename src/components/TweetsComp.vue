<template>
    <div>
        <div>
            <button @click="toggleView">{{ toggleButtonText }}</button>
        </div>
        <div :class="[ isListView ? 'listContainer' : 'gridContainer']">
            <TweetCard
                v-for="post in tweets" 
                :key="post.username"
                v-bind="post"
            />
        </div>
    </div>
</template>

<script>
import TweetCard from '@/components/TweetCard.vue';
export default {
        name : "TweetsComp",
        components: { TweetCard },
        data() {
            return {
                toggleButtonText: "Switch to Grid View",
                isListView: true,
                
                tweets : [
                    {
                        username : 'Nelson Mandela',
                        content : 'The greatest glory in living lies not in never falling, but in rising every time we fall.',
                        dateCreated : "10-14-2022",
                    },
                    {
                        username : 'Walt Disney',
                        content : 'The way to get started is to quit talking and begin doing.',
                        dateCreated : "10-15-2021"
                    },
                    {
                        username : 'Eleanor Roosevelt',
                        content : 'If life were predictable it would cease to be life, and be without flavor.',
                        dateCreated : "02-11-2022"
                    },
                    {
                        username : 'John Lennon',
                        content : "Life is what happens when you're busy making other plans.",
                        dateCreated : "06-24-2021"
                    },
                    {
                        username : 'James Cameron',
                        content : "If you set your goals ridiculously high and it's a failure, you will fail above everyone else's success.",
                        dateCreated : "11-09-2021"
                    },
                    {
                        username: 'Winston S. Churchill',
                        content : 'Success is not final; failure is not fatal: It is the courage to continue that counts.',
                        dateCreated : "7-10-2021"
                    },
                    {
                        username : 'Henry David Thoreau',
                        content : 'Success usually comes to those who are too busy to be looking for it',
                        dateCreated : "09-17-2021" 
                    },
                    {
                        username : 'John D. Rockefeller Jr.',
                        content : 'The secret of success is to do the common thing uncommonly well.',
                        dateCreated : "11-30-2021"
                    },
                    {
                        username : 'Thomas Jefferson',
                        content : 'I find that the harder I work, the more luck I seem to have',
                        dateCreated : "01-03-2022"
                    },
                    {
                        username : 'Franklin D. Roosevelt',
                        content : 'The only limit to our realization of tomorrow will be our doubts of today',
                        dateCreated : "04-12-2021"
                    },
                    {
                        username : 'Steve Jobs',
                        content : 'If you really look closely, most overnight successes took a long time',
                        dateCreated : "10-11-2021"
                    },
                    ]
                }
            },
            methods: {
            toggleView() {
                this.isListView = !this.isListView;
                if(!this.isListView){
                    this.isListView;
                    this.toggleButtonText = "Switch to List View";
                    console.log('this is grid view');
                }else {
                    !this.isListView;
                    this.toggleButtonText = "Switch to Grid View";
                    console.log('this is list view');
                }
            },
            }
            
            
    }
</script>

<style scoped>
*{
    box-sizing: border-box;
}
    .listContainer {
        display: block;
        }
    .gridContainer {
        
        display: grid;
        grid-template-columns: repeat(5, 1fr);
        grid-template-rows: auto;
        }
</style>