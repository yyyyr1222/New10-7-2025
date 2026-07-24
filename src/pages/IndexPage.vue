<template>
  <div class="q-pa-md" style="max-width: 400px">
    <q-form @submit="onSubmit" @reset="onReset" class="q-gutter-md">
      <q-input filled v-model="name" label="Your name(ชื่อ) *" hint="Name and surname" lazy-rules
        :rules="[val => (val && val.length > 0) || 'Please type something']" />

      <q-input filled type="number" v-model.number="age" label="Your age(อายุ) *" lazy-rules :rules="[
        val => (val !== null && val !== '') || 'Please type your age',
        val => (val > 0 && val < 100) || 'Please type a real age'
      ]" />

      <q-toggle v-model="accept" label="I accept the license and terms(ฉันยอมรับเงื่อนไข)" />

      <div>
        <q-btn label="Submit" type="submit" color="primary" />
        <q-btn label="Reset" type="reset" color="primary" flat class="q-ml-sm" />
      </div>
    </q-form>
  </div>
</template>

<script setup>
<template>
  <div class="q-pa-md">
    <div class="q-gutter-y-md column" style="max-width: 300px">
      <q-input color="purple-12" v-model="text" label="Label(ชื่อสีม่วง)">
        <template v-slot:prepend>
          <q-icon name="event" />
        </template>
      </q-input>

      <q-input color="teal" filled v-model="text" label="Label(นามสกุลสีเขียว)">
        <template v-slot:prepend>
          <q-icon name="event" />
        </template>
      </q-input>

      <q-input
        color="grey-3"
        label-color="orange"
        outlined
        v-model="text"
        label="Label"
      >
        <template v-slot:append>
          <q-icon name="event" color="orange" />
        </template>
      </q-input>

      <q-input
        color="lime-11"
        bg-color="green"
        filled
        v-model="text"
        label="Label"
      >
        <template v-slot:prepend>
          <q-icon name="event" />
        </template>
      </q-input>

      <q-input color="teal" outlined v-model="text" label="Label">
        <template v-slot:append>
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo.svg" />
          </q-avatar>
        </template>
      </q-input>

      <q-input
        color="orange"
        standout
        bottom-slots
        v-model="text"
        label="Label"
        counter
        clearable
      >
        <template v-slot:prepend>
          <q-icon name="place" />
        </template>
        <template v-slot:append>
          <q-icon name="favorite" />
        </template>

        <template v-slot:hint> Field hint </template>
      </q-input>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const text = ref('')
</script>
<script>
import { ref } from 'vue'

const text = ref('')
</script>
