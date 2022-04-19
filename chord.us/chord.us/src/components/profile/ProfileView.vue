<template>
  <q-dialog>
    <q-card style="width: 40%">
      <q-card-section class="row items-center q-pb-none">
        <div class="text-h6">Visitor Profile</div>
        <q-space />
        <q-btn v-close-popup icon="close" flat round dense />
      </q-card-section>

      <q-card-section>
        <div>
          <q-input class="q-pa-xs" outlined label="First Name" />
          <q-input class="q-pa-xs" outlined label="Last Name" />
          <q-input class="q-pa-xs" outlined label="E-mail" />
        </div>
      </q-card-section>
    </q-card>
  </q-dialog>
</template>
