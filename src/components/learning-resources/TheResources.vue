<template>
  <base-card>
    <base-button @click="setSelectedTab('stored-resources')"
      >Stored Resorces</base-button
    >
    <base-button @click="setSelectedTab('add-resources')"
      >Add Resorces</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import AddResources from './AddResources.vue';
import StoredResources from './StoredResources.vue';
export default {
  comments: [AddResources, StoredResources],
  data() {
    return {
      selectedTab: 'stored-rescources',
    };
  },
  mathods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
