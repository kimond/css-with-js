<template>
    <div>
        <input type="checkbox" v-model="isActive"/>
        <ul>
            <li :class="{active: isActive}" v-for="n in 1000">
                {{n}} <span v-show="isActive" class="li-span">(active)</span>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "JsImplementation",
        data() {
            return {
                isActive: true
            }
        },
    }
</script>

<style>
    li.active {
        color: #780000;
    }

    li .li-span {
        display: inline-block;
    }
</style>