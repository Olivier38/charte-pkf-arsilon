<template>
    <div @click="copyText()" :class="PrimColor.name" title="Copier Hexa" class="color">
        <div class="content">
            <div class="colorName">{{PrimColor.name}}</div>
            <div class="details">{{PrimColor.cmjn}}</div>
            <div class="details">{{PrimColor.rvb}}</div>
            <div class="details">{{PrimColor.hexa}}</div>
            <div class="details">{{PrimColor.pantone}}</div>
            <div class="show" v-if="show"><i class="gg-chevron-down-o"></i><span class="text-show">Copié !</span></div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from '@vue/composition-api';

export default {
        name: 'PrimColor',
        props: ['PrimColor'],
        data() {
            return {
                show: false,
            }
        },

        methods: {
            copyText() {
                navigator.clipboard.writeText(this.PrimColor.hexa);
                console.log(this.PrimColor.hexa);
                this.show = true,
                 setTimeout(() => {
                    this.show = false;
                }, 2000);
                console.log(this.show)
            },
               
        }
}

</script>