<template>
        <div>
          <img :src="profile" :alt="name" class="profile-pic" />
          <h3 class="name">{{name}}</h3>
          <p class="user-data">{{info}}</p>
        </div>
</template>

<script>
export default {
  name: 'userinfo',
  props: {
    profile: String,
    name: String,
    info: String,
  }
}
</script>

