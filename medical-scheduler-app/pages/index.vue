<template>
    <v-container>
        <v-form>
            <v-text-field v-model="nome" label="Nome" required></v-text-field>
            <v-text-field
                v-model="dataNascimento"
                label="Data de Nascimento"
                type="date"
                required
            ></v-text-field>
            <v-text-field v-model="telefone" label="Telefone" required></v-text-field>
            <v-text-field v-model="email" label="Email" required></v-text-field>
            <v-btn @click="cadastrarPaciente">Cadastrar Paciente</v-btn>
        </v-form>
    </v-container>
</template>

<script>
export default {
    data() {
        return {
            nome: '',
            dataNascimento: '',
            telefone: '',
            email: '',
        };
    },
    methods: {
        async cadastrarPaciente() {
            await this.$axios.$post('/api/pacientes', {
                nome: this.nome,
                dataNascimento: this.dataNascimento,
                telefone: this.telefone,
                email: this.email,
            });
            // Resetar campos ou redirecionar
        },
    },
};
</script>
