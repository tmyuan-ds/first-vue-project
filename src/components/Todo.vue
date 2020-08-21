<template>
    <div>
        <div class="taskItem" v-bind:key="item.id" v-for="item in lists">
            <input type="checkbox" 
            v-on:change="updateTaskStatus(item)" 
            v-bind:checked="item.completed"
            />
            <p class="itemText" 
            v-bind:class="{completedItem:item.completed}"
            >
                {{item.title}}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name:'Todo',
    props: {
            lists:[]
        },
    // data(){
    //     return{
    //         apple:1
    //         }
    //     },
    // Declare state in Vue
    methods:{
            updateTaskStatus(item){
                    // update the state
                    // this.apple ++;
                    // console.log(this.apple)
                    console.log("check box is clicked");
                    item.completed = !item.completed
            },
        },

    // created(){
    //     console.log("This page is rendered")

}

</script>

<style scoped>
    .taskItem{
        padding: 15px 10px;
        border-bottom: 1px solid rgba(0,0,0,0.5);
        display: flex;
        flex-direction: row;
        align-items: center;
        }

    .itemText{
        color:grey
    }

    input{
        margin-right: 20px;
        }

    .completedItem{
        text-decoration: line-through;
    }

</style>