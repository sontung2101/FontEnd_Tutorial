<template>
    <div class="demo-slot">
        <comp-tabs v-bind:title="title" >
            <ul class="tabs-hedear">
                <li 
                v-for="(item,index) in tabsHeader" 
                v-bind:key="index" 
                v-on:click="setActiveTab(index)"
                v-bind:class="{active:tabActive === index}" 
                >{{item.text}}</li>
            </ul>
            <div class="tab-content tab1" v-if="tabActive === 0">
                <p>Tab1 Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?</p>

            </div>
            <div class="tab-content tab2" v-else-if="tabActive === 1">
                <p>Tab2 Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?</p>
                     <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Voluptatibus,
                          delectus eius aut asperiores saepe eveniet laudantium minima doloremque cum voluptates, quibusdam esse doloribus accusamus dolore soluta, odit sint maiores maxime.</p>
            </div>
            <div class="tab-content tab3" v-else>
                <p>Tab3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?</p>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minus explicabo recusandae sapiente voluptas, 
                    error alias sequi temporibus sit dolor laudantium, voluptate tempora hic aliquid ipsum consequuntur quibusdam? Recusandae, sit ut.</p>
                <p>Tab3 Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores culpa accusantium obcaecati perspiciatis
                     eveniet sequi doloribus itaque ipsa repellat numquam corrupti, quo ab delectus impedit aliquid. Minus numquam incidunt explicabo?</p>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Minus explicabo recusandae sapiente voluptas, 
                    error alias sequi temporibus sit dolor laudantium, voluptate tempora hic aliquid ipsum consequuntur quibusdam? Recusandae, sit ut.</p>
            </div>

        </comp-tabs>
    </div>
</template>

<script>
import CompTabs from './compTabs.vue'
export default {
    name:'demo-slot',
    data(){
        return{
            title:" tiêu đề của tabs",
            tabsHeader:[
                {text:'Tab1'},
                {text:'Tab2'},
                {text:'Tab3'},
            ],
            tabActive:1

        }
    },
    methods:{
        setActiveTab(index){
            this.tabActive = index
        }
        
    },
    components:{
        CompTabs,
    }

}
</script>

<style>
    .demo-slot{
        margin-top: 100px;
        padding: 100px 30px;
        border: 1px solid #000;
        margin-bottom: 100px;
    }
</style>