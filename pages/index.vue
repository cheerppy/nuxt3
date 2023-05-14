<script lang="ts">
export default {
    // created() {
    //     const lastmodDate = new Date(document.lastModified);
    //     const timezoneOffset = new Date().getTimezoneOffset()
    //     const lastmodStr = lastmodDate.getFullYear() + "/" + (lastmodDate.getMonth() + 1) + "/" + lastmodDate.getDate() + " " + lastmodDate.getHours() + ":" + ("0" + lastmodDate.getMinutes()).slice(-2) + ":" + ("0" + lastmodDate.getSeconds()).slice(-2)
    //     const timezone = (timezoneOffset === -540) ? "(JST)" : `GMT ${(timezoneOffset >= 0) ? "+" : ""}${Math.floor(timezoneOffset / -60)}:${timezoneOffset / 60}`
    //     this.lastmodStr = lastmodStr;
    //     this.timezone = timezone;
    // },
    data(vm) {
        return {
            lastmodStr: "",
            timezone: ""
        }
    },


}
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
            <p>last modified at: {{ lastmodStr + " " + timezone }}</p>
            <p>© 2022 cheerppy</p>
        </div>

    </div>
</template>

<style scoped></style>
