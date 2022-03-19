<template>
    <div>
        <div class="p-6 sm:px-20 bg-white border-b border-gray-200">

            <div class="mt-8 text-2xl">
                Welcome to your Jetstream application!
                Total: {{total_noticias}}
                Total Alta: {{total_noticias}}
                Total Media: {{total_noticias}}
                Total Baja: {{total_noticias}}
                <table class="min-w-full divide-y divide-gray-200 w-full">
                        <thead>
                            <tr>
                                <th scope="col" class="px-6 py-3 bg-gray-50 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                                    categoria</th>
                                <th scope="col" colspan="2" class="px-6 py-3 bg-gray-50 text-left text-xs font-medium text-gray-500 uppercase tracking-wider">
                                    total</th>
                            </tr>
                        </thead>
                        <tbody class="bg-white divide-y divide-gray-200">
                            <tr v-for="nota in total_noticias">
                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-900">
                                    {{nota.categoria}}
                                </td>
                                <td class="px-6 py-4 whitespace-nowrap text-sm text-gray-900">
                                    {{nota.total}}
                                </td>
                            </tr>
                        </tbody>
                    </table>
            </div>

        </div>
    </div>
</template>

<script>
    import { defineComponent } from 'vue'
    import JetApplicationLogo from '@/Jetstream/ApplicationLogo.vue'
    import AppLayout from '@/Layouts/AppLayout.vue'

    export default defineComponent({
        components: {
            JetApplicationLogo,
            AppLayout,
        },
        props: {
            total_noticias: Array
        }
    })
</script>
