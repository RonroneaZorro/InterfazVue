<script>
import data from '../data/personajes.js'
const pokemones = data.personajes

export default {
    data() {
        return {
            pokemones,
            searchQuery: '',
            isValid: true,
            filteredPokemons: []
        }
    },
    methods: {
        validateAndFilter() {
            this.isValid = this.searchQuery.trim() !== '';
                if (this.isValid) {
                    this.filteredPokemons = this.pokemones.filter(pokemones =>
                            pokemones.name.toLowerCase().includes(this.searchQuery.toLowerCase())
                            );
                } else {
                    this.filteredPokemons = [];
                };
            }
    },
    mounted(){
        this.filteredPokemons = [...this.personajes];
            },
        }
</script>

<template>
    <div class="conteiner">
        <h1>Buscar Pokémon</h1>
        <div class="mb-3">
            <input 
                type="text" 
                v-model="searchQuery" 
                @input="validateAndFilter" 
                class="form-control" 
                placeholder="Ingresa el nombre del Pokémon" 
                :class="{ 'is-invalid': !isValid }"
            >
            <div v-if="!isValid" class="invalid-feedback">
                Debes ingresar un nombre de Pokémon para buscar.
            </div>
        </div>
        <ul v-if="filteredPokemons.length > 0" class="list-group">
            <li v-for="pokemon in filteredPokemons" :key="pokemon.id" class="list-group-item">
                {{ pokemon.name }}
                <br>
                {{ pokemon.description }}
            </li>
        </ul>
        <p v-else-if="searchQuery && filteredPokemons.length === 0" class="text-danger mt-3">
            El pokemón que desea buscar no existe.
        </p>
    </div>
</template>

<style scoped>

</style>