<template>
  <q-page class="">
    <div class="q-py-lg q-px-md row  items-end q-col-gutter-md">
      <div class="col">
        <q-input bottom-slots v-model="newTweetContent" placeholder="What's happening?" counter maxlength="280" autogrow
          class="new-tweet">
          <template v-slot:before>
            <q-avatar size="lg">
              <img src="https://cdn.quasar.dev/img/avatar5.jpg" />
            </q-avatar>
          </template>
        </q-input>
      </div>
      <div class="col col-shrink">
        <q-btn rounded elevated color="primary" label="Tweet" no-caps :disable="!newTweetContent" class="q-mb-lg" />
      </div>

    </div>

    <q-separator size="10px" color="grey-2" class="divider" />
  </q-page>
</template>

<script setup lang="ts">
defineOptions({
  name: 'HomePage',
  data() {
    return {
      newTweetContent: '',
    };
  },
});
</script>
<style lang="sass">
.new-tweet
  textarea
    font-size: 19px
    line-height: 1.4 !important
.divider
  border-top: 1px solid
  border-bottom: 1px solid
  border-color: $grey-3
</style>