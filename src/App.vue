<script setup>
import './index.scss';
import './assets/Fonts/awesome/css/all.css';

import Header from './components/header.vue';
import Main from './components/main.vue';
import Services from './components/services.vue';
import About from './components/about.vue';
import Clients from './components/clients.vue';
import Recalls from './components/recalls.vue';
import Contacts from './components/contacts.vue';
import Copyright from './components/copyright.vue';

function Scroll(className){
    let ElementToScroll = document.getElementsByClassName(className);
    ElementToScroll[0].scrollIntoView();
}
</script>

<template lang="pug">
Header(@scroll='Scroll')
Main.main-block
Services.services-block
About.about-block
Clients.clients-block
Recalls.recalls-block
Contacts.contacts-block
Copyright
</template>

<style>

</style>
