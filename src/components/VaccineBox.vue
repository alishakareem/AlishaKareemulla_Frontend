<template>
    <div class="vaccinebox">
        <div class="vac" v-for="vaccine in vaccines" :key="vaccine.id" >
            <VaccineDetails :vaccines="vaccine"/>
        </div>
    </div>
</template>

<script>
    import VaccineDetails from './VaccineDetails.vue'

    export default{
        name: 'VaccineBox',
        components: {
            VaccineDetails
        },
        props:{   
            vaccines: JSON
        }
    };
    
</script>



<style scoped>

.vaccinebox{
/* background-color: bisque; */
padding: 1em;
color: gray;

}

</style>