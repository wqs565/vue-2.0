<template>
    <div>
        <h1>我是第一个页面</h1>
        <a> written by {{ author }} </a>
    </div>
</template>

<script type="text/javascript">
    export default {
        data () {
            return {
                author: "微信公众号 wqsongsong"
            }
        }
    }
</script>

<style>
</style>