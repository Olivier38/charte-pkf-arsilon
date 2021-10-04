<template>
    <div @click="copyText()" :class="SecondColor.name" title="Copier Hexa" class="color">
        <div class="content">
            <div class="colorName">{{SecondColor.name}}</div>
            <div class="details">{{SecondColor.cmjn}}</div>
            <div class="details">{{SecondColor.rvb}}</div>
            <div class="details">{{SecondColor.hexa}}</div>
            <div class="details">{{SecondColor.pantone}}</div>
            <div class="show" v-if="show"><i class="gg-chevron-down-o"></i><span class="text-show">Copié !</span></div>
            <div class="show" v-if="!show"><i class="gg-copy"></i></div>
        </div>
    </div>

</template>

<script>
import { defineComponent } from '@vue/composition-api'

export default {
        name: 'SecondColor',
        props: ['SecondColor'],
        data() {
            return {
                show: false,
            }
        },

       methods: {
            copyText() {
                navigator.clipboard.writeText(this.SecondColor.hexa);
                console.log(this.SecondColor.hexa);
                this.show = true,
                 setTimeout(() => {
                    this.show = false;
                }, 2000);
                console.log(this.show)
            },
               
        }
}

</script>
