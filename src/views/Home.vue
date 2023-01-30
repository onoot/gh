<template>
  <div class="nes-container with-title mb-10">
    <div class="pt-10 px-10 flex justify-center align-middle">
      <p class="text-4xl pt-3 px-1 mt-1 text-black underline">SOLANA</p>
      <img :width="50" :height="50" src="../assets/400x600.gif" />
      <p class="text-4xl pt-3 px-2 mt-1 text-black underline">STEKING</p>
    </div>
    <p>Welcome to the #1 NFT Staking solution on Solana!</p>
    <p class="mt-5">
      This interface is primarily intended for testing and farm management. You probably want to create a nicer interface for your speakers.
    </p>
    <p class="mt-5">
      That said, if you're a staker, in theory nothing is stopping you from
      using this front-end to access ALL the farms you're staking with. Simply
      go to the
      <router-link to="/farmer" class="text-blue-700">farmer</router-link> tab
      and enter the farm address (ask your NFT project for it).
    </p>
    <p class="mt-5">
      dApp is deployed.
    </p>
  </div>
  <div class="flex flex-row">
    <div class="nes-container with-title flex-1 mr-5">
      <p class="title">Start/manage a farm</p>
      <p class="mb-5">
        Choose this if you have your own NFT collection you'd like to offer
        staking for.
      </p>
      <router-link to="manager">
        <button class="nes-btn is-primary">Start a farm</button>
      </router-link>
    </div>
    <div class="nes-container with-title flex-1 ml-5">
      <p class="title">Stake your NFTs</p>
      <p class="mb-5">
        Choose this if you'd like to stake your NFTs at one of the existing
        farms.
      </p>
      <router-link to="farmer">
        <button class="nes-btn is-primary">Stake NFTs</button>
      </router-link>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { GEM_FARM_PROG_ID } from '@gemworks/gem-farm-ts';
export default defineComponent({
  setup() {
    return {
      GEM_FARM_PROG_ID,
    };
  },
});
</script>
<style scoped></style>
