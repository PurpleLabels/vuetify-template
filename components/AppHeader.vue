<template>
  <div>
    <v-navigation-drawer v-model="drawer" temporary>
      <v-list :items="items"></v-list>
    </v-navigation-drawer>
    <v-app-bar>
      <v-app-bar-nav-icon @click.stop="drawer = true"></v-app-bar-nav-icon>
      <v-icon :icon="mdiGoogle"></v-icon>
      <v-app-bar-title> Title</v-app-bar-title>
    </v-app-bar>
  </div>
</template>

<script setup lang="ts">
  import { mdiGoogle } from "@mdi/js";
  let drawer: Ref<boolean> = ref(false);
  const items = [
    {
      title: "Foo",
      value: "foo",
    },
    {
      title: "Bar",
      value: "bar",
    },
    {
      title: "Fizz",
      value: "fizz",
    },
    {
      title: "Buzz",
      value: "buzz",
    },
  ];
</script>
