<script lang="ts">
export default {
    created() {
        this.lastModDate = new Date(document.lastModified);
    },
    data(vm) {
        return {
            lastModDate: {} as Date
        }
    },
    computed: {
        lastmod() {
            const lastModDate = this.lastModDate
            const timezoneOffset = new Date().getTimezoneOffset()
            const lastmod = lastModDate.getFullYear() + "/" + (lastModDate.getMonth() + 1) + "/" + lastModDate.getDate() + " " + lastModDate.getHours() + ":" + ("0" + lastModDate.getMinutes()).slice(-2) + ":" + ("0" + lastModDate.getSeconds()).slice(-2)
            return lastmod
        },
        timezoneOffset() {
            return new Date().getTimezoneOffset()
        },
        timezone() {
            return (this.timezoneOffset === -540) ? "(JST)" : `GMT ${(this.timezoneOffset >= 0) ? "+" : ""}${Math.floor(this.timezoneOffset / -60)}:${this.timezoneOffset / 60}`
        }
    }

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
            <p>last modified at: {{ lastmod + " " + timezone }}</p>
            <p>© 2022 cheerppy</p>
        </div>
    </div>
</template>

<style scoped></style>
