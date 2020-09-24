<template>
    <div>
        <q-card class="q-pa-md text-white bg-grey-8" style="max-width: 350px">
            <img src="images/mail.jpeg">

            <q-card-section>
                <div class="text-h6">Swift Childbirth Concise</div>
                <div class="text-subtitle2">by Dr. Joe Adejo</div>
            </q-card-section>

            <q-card-section class="q-pt-none">
                A Medical book backed by Scriptures. The book marks the 
                beginning of the end to maternal mortality.
            </q-card-section>

            <q-rating class="q-pl-xl" size="2em" v-model="model" :max="5" color="yellow" />

            <q-card-section align="right">
                <span class="text-white text-h6 text-weight-light">NGN 1,000</span> <br>
                <span class="text-white text-h6 text-weight-light">USD 3.00</span>                
            </q-card-section>

            <q-card-actions align="center">                
                <q-btn outline color="primary">Buy</q-btn>
                <q-btn color="primary">Donate</q-btn>
            </q-card-actions>
        </q-card>
    </div>
</template>

<script>
    export default {
        data(){
            return{
                model: 4,
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>