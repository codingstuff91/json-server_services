<template>
    <div>
        <h1>Liste des jeux</h1>
        <div v-for="game in games[0]" :key="game.id">
            <Game :title="game.title" :plateforme="game.plateforme" />
        </div>
    </div>
</template>

<script>
import GameService from "../services/GameService";
import Game from "@/components/Game.vue";

export default {
    data() {
        return {
            games: [],
        };
    },
    components: {
      Game,
    },
    mounted() {
        GameService.getGames().then((response) =>
            this.games.push(response.data)
        );
    },
};
</script>
