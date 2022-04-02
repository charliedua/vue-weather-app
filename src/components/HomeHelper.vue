<script>
export default {
    name: "HomeHelper",
    msg: {
        type: String,
        required: true,
    }
}
</script>

<template>
    <p>
        {{ msg }}
    </p>
</template>