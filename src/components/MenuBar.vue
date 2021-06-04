<template>
    <div class="nav-item" @mouseenter="showChild=true" @mouseleave="showChild=false">
        <span v-if="typeof val === 'string' || val instanceof String">
            <a :href="val" target="_blank" rel="noopener noreferrer">{{name}}</a>
        </span>
        <div v-else>
            {{name}}
                    
                <transition-group enter-active-class="animate__bounceIn" leave-active-class="animate__bounceOut" tag="ul" class="popup">
                    <li v-for="(link, name) in val" v-show="showChild" :key="name">
                        <a :href="link" target="_blank" rel="noopener noreferrer">{{name}}</a>
                    </li>
                </transition-group>
            
        </div>
    </div>
</template>

<script>
export default {
    name: 'MenuBar',
    props: ['name', 'val'],
    data() {
        return {
            showChild: false
        }
    }
}
</script>
