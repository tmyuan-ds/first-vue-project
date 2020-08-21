<template>
    <div id="footer">
        <h1>{{abc}}</h1>

        <nav>
            <ul id="SMIrow">
                <li id="socialMediaIcon">a</li> 
                <li id="socialMediaIcon">b</li> 
                <li id="socialMediaIcon">c</li> 
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
    name: "Header",
    props:{
        abc:String
        }
}
</script>

<style >
#footer{
        width:100%;
        height: 150px;
        background-color: lime;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-content: center;
        padding: 50px 20px;
    }

ul{
    list-style-type: none;
}

#SMIrow{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    width: 300px
}


#socialMediaIcon{
    width:50px;
    height:50px;
    border-radius: 50%;
    background-color: blue;
    text-align: center;
    padding:15px
}


</style>