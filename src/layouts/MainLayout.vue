<template>
<q-layout view="lHh Lpr lFf">
    <q-header elevated>
        <q-toolbar>

            <q-toolbar-title class="text-bold">
                Madrid 2022 | OTOÑO
            </q-toolbar-title>

            <div>
              <img src="~assets/spain.png" alt="img spain flag" style="width:2.5rem;">
            </div>
        </q-toolbar>
    </q-header>

    <q-page-container>
        <router-view />
    </q-page-container>
</q-layout>
</template>

<script>
import {
    defineComponent,
    ref
} from 'vue'

export default defineComponent({
    name: 'MainLayout',

    components: {
    },

    setup() {
        const leftDrawerOpen = ref(false)

        return {
        }
    }
})
</script>
