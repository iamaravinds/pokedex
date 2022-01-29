<template>
    <v-row>
        <v-col align="end">
            <div>
                <v-btn
                @click="toggle">
                    {{action}}
                </v-btn>
            </div>
        </v-col>
    </v-row>
</template>
<script>
export default {
    name: 'AppBar',
    data() {
        return {
            action: 'Log In'
        };
    },
    methods: {
        toggle() {
            this.action = (this.action === 'Log In') ? 'Log Out' : 'Log In';
        }
    },
}
</script>

<style>

</style>