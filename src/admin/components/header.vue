<template lang="pug">
    #header
      h1.header__title Панель администрирования
      a(@click="logout").header__link Вернуться на сайт
</template>

<script>
import { mapActions } from "vuex";

export default {
    methods: {
        ...mapActions({
            logout: 'user/logout'
        })
    }
}
</script>


<style lang="scss" scoped>

#header {
  display: flex;
  justify-content: space-between;
  padding: 20px 30px;
  background-color: #16c2aa;
  align-items: center;
}

.header__title {
    color: #fff;
}

.header__link {
    color: rgba(#fff, 0.8);
    cursor: pointer;

    &:hover {
        color: rgba(#fff, 1);
    }
}
</style>


