<template>
    <div class="mdc-layout-grid__inner" :id="id">
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: ['id']
}
</script>