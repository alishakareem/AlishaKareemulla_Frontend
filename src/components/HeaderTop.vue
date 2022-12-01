<template>
    <div>
        <h1> {{projectName}} </h1>
        <h4> {{subTitle}} </h4>
        <img id="i1" src="img1.jpg">
        <img id="i2" src="img2.png">
    </div>
</template>
    
<script>

    export default{
        name: 'HeaderTop',
        props:{
            projectName: String,
            subTitle:String
        }
    }
    
</script>
    
<style scoped>
    
    div{
        text-align: center;
        font-size: 28px;
        
    }

    h1{
        color: red;
    }

    #i1{
        margin-top: 25px;
        border-radius: 20px;
        width:500px;
    }
    
</style>