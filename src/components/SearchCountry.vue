<!-- eslint-disable vue/require-v-for-key -->
<template>
    <div>
    <select @change="onChange" v-model="selected" class="form-select mt-1 block w-full border p-3 rounded">
    // eslint-disable-next-line vue/require-v-for-key
    <option v-for="country in countries" :value="country.ID" >
        {{ country.Country }}</option></select>
    </div>
</template>

<script>
export default{
    name:'SearchCountry',
    props: ['countries'],
    data(){
        return{
            selected:0
        }
        
    },
    methods:{
        onChange(){
            const country = this.countries.find((item)=>item.ID ===this.selected)
            this.$emit('get-country', country)

        }
    }
}
</script>
