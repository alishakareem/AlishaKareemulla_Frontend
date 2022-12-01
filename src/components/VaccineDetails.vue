<template>
    
    <div>
        <h2> {{vaccines.name}}</h2>
        <h4> Manufacturer : {{vaccines.manufacturer}}</h4>
        <h4> Doses : {{vaccines.doses}}</h4>
        <h4> Frequency of Doses : {{vaccines.frequency}}</h4>
        <h4> Effectiveness : {{vaccines.effectiveness}}</h4>
        <h4> Possible Side Effects : {{vaccines.possibleSideEffects}}</h4>
    </div>
    
</template>

<script>

export default{
    name: 'VaccineDetails',
    props:{
        vaccines: JSON
    }
}

</script>


<style scoped>

h4{
    margin: 2px;
    padding-left: 30px;
    padding-top: 8px;
    font-size: 17px;
}

div{
    /* background-color: #f5b39a; */
    background-color: rgb(183, 230, 225);
    color: black;
    padding: 1em;
    border-radius: 20px;
    margin-bottom: 12px;
}

h2{
    color: blue;
    
}
</style>