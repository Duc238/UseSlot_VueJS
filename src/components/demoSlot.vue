<template>
    <div>
        <comp-tabs title="Tiêu đề của tab">
            <ul class="tabs-header">
                <li v-for="(item, index) in tabsHeader" v-bind:key="index"
                    v-on:click="setActiveTab(index)"
                >{{item.text}}</li>
            </ul>
            <div class="tabContentTab1" v-if="tabActive===0">
                <p>Maragret Wang</p>
            </div>
            <div class="tabContentTab2" v-else-if="tabActive===1">
                <p>Trần Hoài Ngọc</p>
            </div>
            <div class="tabContentTab3" v-else>
                <p>Trần Mỹ Sương</p>
            </div>
        </comp-tabs>
    </div>
</template>
<script>
import CompTabs from "./CompTabs.vue"
export default {
    components:{
        CompTabs
    },
    data(){
        return{
            tabsHeader:[
                {text:"Tab1"},
                {text:"Tab2"},
                {text:"Tab3"}
            ],
            tabActive:0
        }
    },
    methods:{
        setActiveTab(index){
            this.tabActive=index;
        }
    }
}
</script>
<style>
    
</style>