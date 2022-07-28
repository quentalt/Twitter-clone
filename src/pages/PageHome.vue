<template>
  <q-page>
    <div class="q-py-lg q-px-md row items-end q-col-gutter-md">
      <div class="col">
        <q-input
          bottom-slots
          class="new-qweet"
          v-model="newQweetContent"
          placeholder="Qu'est-ce qui arrive?"
          counter
          maxlength="280"
        >
          <template v-slot:before>
            <q-avatar>
              <img src="https://cdn.quasar.dev/img/avatar5.jpg">
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn
        :disable="!newQweetContent"
        class="q-mb-lg"
        color="primary"
        label="Qweet"
        rounded
        unelevated
        no-caps
        />
      </div>
    </div>
    <q-separator
    class="divider"
    color="grey-2"
    size="10px"
    />
  </q-page>
</template>

<script>
export default {
  name: 'PageHome',
  data() {
    return {
      newQweetContent:''
    }
  },
}
</script>

<style lang="sass">
.new-qweet
  font-size: 19px
  line-height: 1.4 !important
</style>
