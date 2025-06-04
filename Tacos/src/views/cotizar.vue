<template>
  <h1>Cotizar</h1>
  <h2>Bienvenido a Chiquihuitl Tacos</h2>

<div class="linea-personas">
  <p>Cantidad de personas:</p>
  <p class="numero">{{ personas }}</p>
  <button @click="decrement" class="contador">-</button>
  <button @click="increment" class="contador">+</button>
</div>


<div class="linea-personas">
  <p>Cantidad de orden:&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
  <p class="numero">{{ orden }}</p>
  <button @click="decrement" class="contador">-</button>
  <button @click="increment" class="contador">+</button>
</div>

<div class="linea-personas">
  <p>Sabor de taco:</p>
  <p class="numero">{{ personas }}</p>
</div>

  <button class="button-cotizar">Cotizar</button>
  <h2>Total: {{ total }} </h2>
</template>

<script>
//contador
import { ref } from 'vue'

const personas = ref(50)

const increment = () => {
  personas.value++
}

const decrement = () => {
  if (personas.value > 50) {
    personas.value--
  }
}
//fin contador

</script>

<style>
.linea-personas {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 8px;
  font-size: 24px;
  margin-top: 25px;
  padding-right: 200px;
}

.numero {
  width: 40px;
  text-align: center;
  font-weight: bold;
  color: black;
}

.contador {
  font-size: 18px;
  padding: 5px 10px;
  background-color: #D2782A;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  display: block;
  margin: 0;

}

.button-cotizar {
  font-family: 'Roboto', sans-serif;
  display: block;
  margin: 20px auto;
  padding: 10px 20px;
  font-size: 18px;
  background-color: #D2782A;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

p{
  font-family: 'Roboto', sans-serif;
  padding-left: 200px;
  text-align: left;
  font-size: 30px;
  margin-top: 25px;
}

h2{
  font-family: 'Roboto', sans-serif;
  text-align: center;
  margin-top: 20px;
  font-size: 25px;
}

h1{
  font-family: 'Roboto', sans-serif;
  text-align: center;
  margin-top: 20px;
  font-size: 35px;
  font-weight: bold;
}
</style>
