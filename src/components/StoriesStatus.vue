<template>
  <ul>
    <li>
      User Stories &nbsp;
      {{ status.total }}
    </li>
    <li>
      Defined &nbsp;
      {{ status.defined }}
    </li>
    <li>
      In Progress &nbsp;
      {{ status.inProgress }}
    </li>
    <li>
      Accepted &nbsp;
      {{ status.accepted }}
    </li>
    <li>
      Blocked &nbsp;
      {{ status.blocked }}
    </li>
    <li>
      Completed &nbsp;
      {{ status.completed }}
    </li>
  </ul>
</template>
<script>
export default {
  props: ['status']
}
</script>
<style>
</style>
