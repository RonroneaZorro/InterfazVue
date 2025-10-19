<script>
export default {
    name: 'UsuariosTabla',
    data() {
        return {
            usuarios: [{
                id: 1,
                nombre: 'Juan',
                apellido: 'Perez',
                fechaNacimiento: '1990-01-01',
                edad: 30
            }, {
                id: 2,
                nombre: 'Maria',
                apellido: 'Gomez',
                fechaNacimiento: '1995-02-02',
                edad: 25
            }, {
                id: 3,
                nombre: 'Pedro',
                apellido: 'Lopez',
                fechaNacimiento: '1998-03-03',
                edad: 22
            }, {
                id: 4,
                nombre: 'Ana',
                apellido: 'Garcia',
                fechaNacimiento: '1992-04-04',
                edad: 28
            }]
        }
    }
}
</script>
<template>
    <div class="container">
  <div class="row">
    <div class="col">Nombre</div>
    <div class="col">Apellido</div>
    <div class="col">Fecha de Nacimiento</div>
    <div class="col">Edad</div>
    <div class="row" v-for="usuario in usuarios" :key="usuario.id">
            <div class="col"> {{ usuario.nombre}} </div>    
            <div class="col"> {{ usuario.apellido}} </div>  
            <div class="col"> {{ usuario.fechaNacimiento}} </div>
            <div class="col"> {{ usuario.edad}} </div>
         </div>
    </div>
</div>
</template>
<style scoped>
.container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
    background-color: #f2f2f2;
}
.row {
    display: flex;
    justify-content: space-between;
    margin: auto 0;
     
}

.col {
    flex: 1;
    text-align: center;
    border: 1px solid #ccc;
    padding: 10px;
    background-color: #f2f2f2;
    border-radius: 5px;
    font-weight: bold;
    color: #2c3e50;
}
</style>