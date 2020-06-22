<template>
    <div class="input1">
        <form>
        输入：<input type='text' name='inputsyn1' ref='test' @input='changes' :value='$store.state.count'/>
        </form>
    </div>
</template>

<script>
import {mapState,mapMutations} from 'vuex'

export default {
    name:'input1',
    data() {
        return {
        }
    },
    computed:{
        ...mapState(['count'])
    },
    methods:{
        ...mapMutations(['changeInput']),
        changes(){
            var inputvalue=this.$refs.test.value
            this.changeInput(inputvalue)
        }
    }
}

</script>