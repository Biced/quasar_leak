<template>
    <div class="q-pa-md">
      <div class="q-gutter-y-md" style="max-width: 600px">
        <q-card>
          <q-tabs
            v-model="tab"
            dense
            class="text-grey"
            active-color="primary"
            indicator-color="primary"
            align="justify"
            narrow-indicator
          >
            <q-tab name="mails" label="Mails" />
            <q-tab name="alarms" label="Alarms" />
          </q-tabs>
  
          <q-separator />
  
          <q-tab-panels v-model="tab" animated>
            <q-tab-panel name="mails">
              <div class="text-h6">Mails</div>
              <Tree/>
            </q-tab-panel>
  
            <q-tab-panel name="alarms">
              <div class="text-h6">Alarms</div>
              <Tree/>
            </q-tab-panel>
          </q-tab-panels>
        </q-card>

      </div>
    </div>
  </template>
  <script>
  import { ref } from 'vue'
  import Tree from './Tree.vue';

  export default {
    components:{Tree}
,
    setup () {
      return {
        tab: ref('mails')
      }
    }
  }
  </script>