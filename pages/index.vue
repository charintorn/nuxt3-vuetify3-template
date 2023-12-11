<template>
    <div>

        <h2>Hompate</h2>
        <v-btn color="red">button</v-btn>
        <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim, quia accusantium a ab qui blanditiis provident
            quo
            hic consequuntur perspiciatis voluptates accusamus quisquam odit officiis explicabo eos. Reprehenderit, labore
            sit?
        </p>
        <v-container>
            <v-row align="center" justify="center">
                <v-col cols="auto">
                    <v-radio-group v-model="color" inline>
                        <v-radio label="indigo" color="indigo" value="indigo"></v-radio>
                        <v-radio label="indigo-darken-3" color="indigo-darken-3" value="indigo-darken-3"></v-radio>
                        <v-radio label="primary" color="primary" value="primary"></v-radio>
                        <v-radio label="secondary" color="secondary" value="secondary"></v-radio>
                    </v-radio-group>
                </v-col>
            </v-row>
            <v-row align="center" justify="center">
                <v-col v-for="(variant, i) in variants" :key="i" cols="auto">
                    <v-card class="mx-auto" max-width="344" :color="color" :variant="variant">
                        <v-card-item>
                            <div>
                                <div class="text-overline mb-1">
                                    {{ variant }}
                                </div>
                                <div class="text-h6 mb-1">
                                    Headline
                                </div>
                                <div class="text-caption">Greyhound divisely hello coldly fonwderfully</div>
                            </div>
                        </v-card-item>

                        <v-card-actions>
                            <v-btn>
                                Button
                            </v-btn>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const variants = ['elevated', 'flat', 'tonal', 'outlined']
const color = ref('indigo')
</script>
<style lang="scss" scoped></style>