<template>
  <ul class="sidenav app-sidenav open">
    <router-link v-slot="{isActive}" v-for="link in links" :key="link.url" active-class="active" :exact="link.exact" :to="link.url">
      <li :active="isActive">
        <a href="#" class="waves-effect waves-orange pointer">{{link.title}}</a>
      </li>
    </router-link>
  </ul>
</template>

<script>
export default {
  name: "Sidebar",
  data: () => ({
    links: [
      {title:'Счёт', url:'/', exact: true},
      {title:'История', url:'/history'},
      {title:'Планирование', url:'/planning'},
      {title:'Новая запись', url:'/record'},
      {title:'Категории', url:'/categories'},
    ]
  })
};
</script>

<style scoped>

</style>