<template>
  <aside class="menu">
    <p class="menu-label">Menu Principal</p>
    <ul class="menu-list">
      <li @click="handleClick(0)" class="hand-option">
        <a :class="{'is-active' : menu == 0 }">Dashboard</a>
      </li>
      <li @click="handleClick(1)" class="hand-option">
        <a :class="{'is-active' : menu == 1 }">Departamentos</a>
      </li>
      <li @click="handleClick(2)" class="hand-option">
        <a :class="{'is-active' : menu == 2 }">Cargos</a>
      </li>
      <li @click="handleClick(3)" class="hand-option">
        <a :class="{'is-active' : menu == 3 }">Empleados</a>
      </li>
    </ul>
  </aside>
</template>

<script>
  export defaults {
    props: {
      menu: {
        type: Number,
        required: false,
        default: 0
      }
    },
    methods: {
      handleClick (value) {
        this.$emit('update:menu', value)
      }
    }
  }
</script>
