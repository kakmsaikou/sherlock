<template>
  <nav>
    <router-link to="/labels" class="item" active-class="selected">
      <Icon name="labels"/>
      标签
    </router-link>
    <router-link to="/money" class="item" active-class="selected">
      <Icon name="money"/>
      记账
    </router-link>
    <router-link to="/statistic" class="item" active-class="selected">
      <Icon name="statistic"/>
      统计
    </router-link>
  </nav>
</template>

<script lang="ts">
  export default {
    name: 'Nav',
  };
</script>

<style lang="scss" scoped>
  @import "~@/assets/styles/helper.scss";

  nav {
    display: flex;
    box-shadow: 0 0 3px rgba(0, 0, 0, 0.05);
    font-size: 12px;
    background-color: white;

    > .item {
      padding: 2px 0;
      flex-grow: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      color: $color-dark-grey;

      .icon {
        width: 32px;
        height: 32px;
      }
    }

    > :last-child .icon{
        width: 28px;
        height: 28px;
    }

    > .item.selected {
      color: $color-blue;
    }
  }
</style>