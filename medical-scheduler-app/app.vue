<template>
    <v-app class="app-content">
        <v-app-bar app color="green darken-3" dark>
            <v-toolbar-title class="white--text">Medical Scheduler</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text @click="$router.push('/')">Início</v-btn>
            <v-btn text @click="$router.push('/medicos')">Médicos</v-btn>
            <v-btn text @click="$router.push('/pacientes')">Pacientes</v-btn>
            <v-btn text @click="$router.push('/consultas')">Agendamentos</v-btn>
        </v-app-bar>
        <v-main class="main-content">
            <NuxtPage />
        </v-main>
        <v-footer color="green darken-3" app>
            <v-col class="white--text" text-align="center">
                &copy; {{ new Date().getFullYear() }} Your Corporation Name
            </v-col>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    // Você pode adicionar lógica aqui se necessário
};
</script>

<style>
.app-content {
    height: 100vh;
    overflow: hidden;
}
.main-content {
    background-color: black; /* Define o fundo como preto */
    color: white; /* Define a cor do texto como branco para contraste */
    height: 80%;
    padding: 16px; /* Adiciona um pouco de espaçamento */
}
</style>
