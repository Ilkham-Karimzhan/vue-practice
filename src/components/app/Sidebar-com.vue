<template>
    <ul class="sidenav app-sidenav" :class="{open: value}">

        <li>
          <router-link
            v-for="link in links"
            :key="link.url"
            :to="link.url"
            active-class="active"
            hrefreoter-link="#"
            class="waves-effect waves-orange pointer"
            :exact="link.exact"
          >
           {{link.title}}
          </router-link>
        </li>
    </ul>
</template>

<script>
export default {
  props: ['value'],
  data: () => ({
    links: [
      { title: 'Счет', url: '/', exact: true },
      { title: 'История', url: '/history' },
      { title: 'Планирование', url: '/planning' },
      { title: 'Новая запись', url: '/record' },
      { title: 'Категории', url: '/categories' }
    ]
  })
}
</script>
