<template>
    <div>
        <div class="taskItem" v-bind:key="item.id" v-for="item in lists">
            <p >{{item.title}}</p>
        </div>
    </div>
</template>

<script>
export default {
    name:'Todo',
    props: {
            lists:[]
        }
}

</script>

<style scoped>
    .taskItem{
        padding: 15px 10px;
        border-bottom: 1px solid rgba(0,0,0,0.5);
        }

</style>