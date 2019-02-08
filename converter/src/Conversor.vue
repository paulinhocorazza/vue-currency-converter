<template>

    <div>
        <b-card bg-variant="light" text-variant="black" header="Conversor" class="text-center">
            <h5 class="card-title">{{ currency1 }} para {{ currency2 }}</h5>
            <input type="text" class="form-control text-center" v-model="currency1_value" v-bind:placeholder="currency1">
            <br>
            <b-button v-on:click="converter">Converter</b-button>
            <br>
            <h2 class="text-center"> {{ currency2_value }}</h2>
        </b-card>
    </div>
</template>

<script>
    export default {
        name: "Conversor",
        props: ["currency1", "currency2"],
        data() {
            return {
                currency1_value: '',
                currency2_value: 0
            }
        },
        methods: {
            converter() {

                let from = this.currency1 + "_" + this.currency2;
                let url = "https://free.currencyconverterapi.com/api/v5/convert?q=" + from + "&compact=y";


                fetch(url).then(res => {
                        return res.json()
                    })
                    .then(json => {
                        let cotacao = json[from].val;
                        this.currency2_value = (cotacao * parseFloat(this.currency1_value)).toFixed(2);
                    })
            }

        }
    }
</script>

<style scoped>

</style>