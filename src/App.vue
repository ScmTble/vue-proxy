<script setup>
import axios from 'axios';


const handleSetCookie = () => {
  axios.get("https://nginx-proxy-st.zeabur.app/api/setcookie")
}

const handleGetCookie = () => {
  axios.get("https://nginx-proxy-st.zeabur.app/api/getcookie", {
    withCredentials: true
  }).then(res => {
    console.log(res)
  })
}

</script>


<template>
  <div>
    <button @click="handleSetCookie">设置Cookie</button>
    <button @click="handleGetCookie">获取Cookie</button>
  </div>
</template>

