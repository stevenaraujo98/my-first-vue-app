<template>
    <div>
        <h1>Contacto</h1>

        <Pokemon/>
        <button @click="changeContador">Aumentar {{contador}}</button>

        <br/>
        <br/>

        {{"Tu mensaje es "+mensaje}}
        <form>
            <input type="email" v-model="mensaje"/>
        </form>
    </div>
</template>

<script>
import Pokemon from '@/components/Pokemon.vue';
export default {
    components:{
        Pokemon
    },
    data(){
        return {
            contador: 0,
            mensaje: ''
        }
    },
    methods:{
        changeContador(){
            this.contador++;
        }
    },
    mounted() {
        console.log("Aqui se haria uso de axios para fetch o ajax");
    }
}

</script>