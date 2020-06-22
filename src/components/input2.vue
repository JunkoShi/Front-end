<template>
    <div class="input2">
            同步：<input type='text' name='inputsyn2'  ref='test1' @input='changes' :value='$store.state.count'>
        </div>
</template>

<script>
import {mapState,mapMutations} from 'vuex'

export default {
    name:'input2',
    data() {
        return {}      
    },
    computed:{
        ...mapState(['count'])
    },
    methods:{
        ...mapMutations(['changeInput']),
        changes(){
            var inputvalue=this.$refs.test1.value
            this.changeInput(inputvalue)
        }
    }   
}
</script>