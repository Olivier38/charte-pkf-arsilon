<template>
    <div :class="color.name" class="color">
        <div class="content">
            <div>{{color.name}}</div>
            <div>{{color.cmjn}}</div>
            <div>{{color.rvb}}</div>
            <div>{{color.hexa}}</div>
            <div>{{color.pantone}}</div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default {
        name: 'color',
        props: ['color']
}
</script>
