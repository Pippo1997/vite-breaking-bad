<script>
import { store } from '../store.js';

export default {
    data(){
        return{
            store,
            archetypes: [
                'Alien',
                'Dark Magician',
                'Cipher',
                'Laval',
            ],
        }
    }
}
</script>

<template lang="">
    <div class="container">
        <div class="row">
            <div class="col-12">
                <div class="mt-5">
                    <select v-model="store.selectedGenere" @change="$emit ('filter')">
                        <option v-for="(item, index) in archetypes" :key="index" :value="item">{{ item }}</option>
                    </select>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
    select{
        background-color: white;
        border: none;
        border-radius: 5px;
        width: 200px;
        padding: 10px 5px;
    }
</style>