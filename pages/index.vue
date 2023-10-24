<template>
  <div
    class="flex flex-col items-center justify-center min-h-screen min-w-screen overflow-hidden pb-32"
    style="background-color: #0b1227"
  >
    <div
      class="h-16 md:h-24 lg:h-32 my-4"
      data-aos="fade-down"
      data-aos-delay="300"
    >
      <img
        src="https://avatars.githubusercontent.com/u/122947008"
        class="h-16 md:h-24 lg:h-32"
      />
    </div>
    <Link
      v-for="(link, index) in links"
      :url="link.url"
      :name="link.name"
      :icon="link.icon"
      :delay="index * 100"
    />
    <div class="h-1 w-32 bg-gray-700 my-3"></div>
    <Link
      v-for="(link, index) in partners"
      :url="link.url"
      :name="link.name"
      :icon="link.icon"
      :delay="index * 100"
    />
  </div>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
}
</style>

<script setup lang="ts">
const links = [
  {
    url: "https://cubealgos.org",
    icon: "mdi:web",
    name: "Website",
  },
  {
    url: "https://discord.gg/znABzEacKf",
    icon: "mdi:discord",
    name: "Discord",
  },
  {
    url: "https://x.com/cubealgos",
    icon: "mdi:twitter",
    name: "Twitter",
  },
  {
    url: "https://github.com/cubealgos",
    icon: "mdi:github",
    name: "GitHub",
  },
];
const partners = [
  {
    url: "https://partner.bybit.com/b/cubealgos",
    icon: "mdi:bank-transfer",
    name: "ByBit",
  },
  {
    url: "https://promote.mexc.com/a/cubealgos",
    icon: "mdi:bank-transfer",
    name: "MEXC",
  },
];
</script>
