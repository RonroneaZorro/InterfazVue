<script>
export default {
    name: 'ListadoPokemones',
    data() {
        return {
            personajes: [
                 { 
                "id": "1", 
                "nombre": "Pikachu", 
                "descripcion": "Se almacena la electricidad en los sacos eléctricos en sus mejillas. Cuando se libera la energía acumulada en una ráfaga, la energía eléctrica es igual a un rayo." 
            }, 
            { 
                "id": "2", 
                "nombre": "Kakuna", 
                "descripcion": "A la espera de la evolución, se esconde debajo de las hojas de los depredadores y en los rincones de las ramas." 
            }, 
            { 
                "id": "3", 
                "nombre": "Beedrill", 
                "descripcion": "Su mejor ataque consiste en volar alrededor a gran velocidad, golpeando con las agujas de veneno, y luego volando." 
            }, 
            { 
                "id": "4", 
                "nombre": "Metapod", 
                "descripcion": "Una concha de acero duro protege a su tierno cuerpo. Se queda en silencio soportando las dificultades a la espera de la evolución." 
            }, 
            { 
                "id": "5", 
                "nombre": "Rattata", 
                "descripcion": "Cauteloso en extremo, su vitalidad robusta le permite vivir en cualquier tipo de ambiente." 
            }
            ]
        } 
    } 
}
</script>
<template>
    <h1>Personajes de Pokemón</h1>

<div class="container">
    <div class="row">
        <div class="col-1">Nombre</div>
        <div class="col-1">Descripción</div>
    </div>
    <div class="row" v-for="pokemon in personajes" :key="pokemon.id">
        <div class="col"> {{ pokemon.nombre }} </div>    
        <div class="col"> {{ pokemon.descripcion }} </div>  
    </div>
</div>
</template>
<style>

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: auto;
  width: 100%;
  background-color: silver;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
}
.row {
    display: flex;
    justify-content: space-between;
    margin: auto 0;
    width: 80%;
}
.col {
    flex: 1;
    padding: 15px;
    border: 1px solid #0c0404;
    border-radius: 5px;
    background-color: #fff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    width: 100%;
    height: auto;
    text-align: center;
    vertical-align: middle;
}
.col-1 {
    flex: 1;
    text-align: center;
    padding: 10px;
    border: 1px solid #0c0404;
    border-radius: 5px;
    background-color: #fff;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
    width: 100%;
    font-weight: bold;
    font-size: 18px;
    color: #000;
}

</style>