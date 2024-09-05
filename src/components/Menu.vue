<template>
    <v-list>
        <v-list-item prepend-avatar="https://cdn.vuetifyjs.com/images/john.png" title="Ivan Pires"
            subtitle="ivanpires@unemat.br" />
    </v-list>
    <v-divider />
    <v-list :items="menu"></v-list>
</template>
<script setup>
const menu = [
    {
        title: 'Início',
        props: {
            prependIcon: 'mdi-home',
            link: true
        }
    },
    {
        title: 'Contato',
        props: {
            prependIcon: 'mdi-whatsapp'
        },
    },
    {
        title: 'Relatório',
        props: {
            prependIcon: 'mdi-file-document'
        }
    }
]
</script>