<template lang="html">
    <div class="">
        <v-editor
        :input-content="inputContent"
        :upload-url="uploadUrl"
        v-model="outputContent"></v-editor>
        <input type="button" name="name" value="submit" @click="submit">
    </div>
</template>

<script>
  import 'jquery'
import Editor from './components/wangeditor/Editor'
export default {
    data() {
        return {
            // input content to editor
            inputContent: 'base on wangeditor',
            // output content from editor
            outputContent: '',
            // set image upload api url
            uploadUrl: '/api/v1/help/upload/wangEditorH5File'
        }
    },
    computed: {},
    ready() {},
    attached() {},
    methods: {
        submit() {
            console.log(this.outputContent)
        }
    },
    components: {
        'v-editor': Editor
    }
}
</script>

<style lang="css">
</style>
