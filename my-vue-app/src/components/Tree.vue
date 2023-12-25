<template>
    
    
    
    <q-tree :duration="0" :nodes="callTrace" node-key="uiId" label-key="name" children-key="childrenList"
    selected-color="primary" ref="myQtree"  color="secondary"></q-tree>
</template>
<script>
import {callTrace} from '../json_bigu'

export default {
    setup(){
        return{
            callTrace
        }
    }
}
</script>