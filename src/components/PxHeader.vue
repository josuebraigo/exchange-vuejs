<template>
  <header class="shadow w-screen">
    <nav>
      <nav class="flex items-center justify-between flex-wrap bg-green-400 p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
          <px-icon class="mr-2" />
          <router-link
            :to="{ name: 'home' }"
            class="font-semibold text-xl tracking-tight"
            >Platzi Exchange</router-link
          >
        </div>
        <div
          class="
            hidden
            sm:block
            block
            flex-grow
            lg:flex
            lg:items-center
            lg:w-auto">
          <div class="flex text-sm lg:flex-grow">
            <router-link
              v-for="link in links"
              :key="link.title"
              :to="link.to"
              class="
                block
                mt-2
                lg:inline-block
                lg:mt-0
                text-teal-200
                hover:text-white
                mr-4
              "
            >
              {{ link.title }}
            </router-link>
          </div>
        </div>
      </nav>
    </nav>
  </header>
</template>

<script>
import PxIcon from "./PxIcon";

export default {
  name: "PxHeader",
  components: {
    PxIcon,
  },
  props: {
    links: {
      type: Array,
      default: () => [],
    }
  }
};
</script>
