<template>
    <div>
        <button @click="toggleView">{{ toggleButtonText }}</button>
    </div>
</template>

<script>
    export default {
        name: "ToggleButton",
        data() {
            return {
                toggleButtonText: "Switch to Grid View",
                isListView: true
            }
        },
        methods: {
            toggleView() {
                this.$emit('toggleClicked');
                this.isListView = !this.isListView;
                if(!this.isListView){
                    this.isListView;
                    this.toggleButtonText = "Switch to List View";
                    console.log('this is list view');
                }else {
                    this.toggleButtonText = "Switch to Grid View";
                    console.log('this is grid view');
                }
            },
            }
}
</script>

<style scoped>

</style>