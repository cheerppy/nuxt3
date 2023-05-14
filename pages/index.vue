<script lang="ts" setup>
const jst = new Date(document.lastModified);
const timezoneOffset = new Date().getTimezoneOffset()
const lastmod = jst.getFullYear() + "/" + (jst.getMonth() + 1) + "/" + jst.getDate() + " " + jst.getHours() + ":" + ("0" + jst.getMinutes()).slice(-2) + ":" + ("0" + jst.getSeconds()).slice(-2)
const timezone = (timezoneOffset === -540) ? "(JST)" : `GMT ${(timezoneOffset >= 0) ? "+" : ""}${Math.floor(timezoneOffset / -60)}:${timezoneOffset / 60}`
</script>

<template>
    <div>
        <p>Hello Nuxt!!!</p>
        <p>
            <NuxtLink to="coc">coc</NuxtLink>
        </p>
        <p>
            <NuxtLink to="/coc">/coc</NuxtLink>
        </p>
        <p>
            <NuxtLink to="trpg">trpg</NuxtLink>
        </p>
        <p>
            <NuxtLink to="/trpg">/trpg</NuxtLink>
        </p>
        <div class="footer__inner">
            <p>last modified at: {{ lastmod + " " + timezone }}</p>
            <p>© 2022 cheerppy</p>
        </div>
    </div>
</template>

<style scoped></style>
