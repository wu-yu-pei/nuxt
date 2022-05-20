<template>
  <div>
    登录
    <input type="text" ref="names" />
    <input type="text" ref="password" />
    <button ref="button">登录</button>
    <nuxt-child />
  </div>
</template>

<script setup>
let names = ref(null);
let password = ref(null);
let button = ref(null);
let router = useRouter();
onMounted(() => {
  button.value.addEventListener('click', () => {
    if (names.value.value === '123456' && password.value.value === '123456') {
      alert('登录成功');
      console.log(router);
      router.push('/main');
    } else {
      alert('登录失败');
    }
  });
});
</script>

<style></style>
