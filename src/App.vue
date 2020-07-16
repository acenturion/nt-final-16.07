<template>
    <div id="app">
        <div class="container">
          <label>Ingresar texto:</label>
            <hr>
            <input v-model="message" type="text"/>
            <TextDisplay :message="message"/>
        </div>


   <div>
       <h3>Respuestas</h3>
       <p>1: b</p>
       <p>2: b y d</p>
       <p>3: c</p>
       <p>4: b</p>
       <p>5: b</p>
   </div>
    </div>
</template>

<script>
    import TextDisplay from './components/TextDisplay.vue'

    export default {
        name: 'App',
        data() {
            return {
                message: '',
            }
        },
        components: {
            TextDisplay
        }
    }
</script>

<style>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
