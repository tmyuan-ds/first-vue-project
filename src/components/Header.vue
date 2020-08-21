<template>

    <div id="header">
        <h1>{{logo}}</h1>

        <nav>
            <ul>
                <li>Home</li> 
                <li>About</li> 
                <li>Contact</li> 
            </ul>
        </nav>
    </div>
    
</template>

<script>
export default {
    name: "Header",
    props:{
        logo:String
        }
}
</script>

<style scoped>
#header{
        width:100%;
        height: 80px;
        background-color: darkgray;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-content: center;
        padding: 0 20px;
    }

ul{
    display:flex;
    flex-direction: row;
}
</style>