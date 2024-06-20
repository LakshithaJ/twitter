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

    <q-list>
      <q-item class="q-py-md">
        <q-item-section avatar top>
          <q-avatar size="xl">
            <img src="https://cdn.quasar.dev/img/avatar2.jpg">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-subtitle1"> <strong> Laksh J</strong> <span class="text-grey-7">@Laksh-j</span>
          </q-item-label>
          <q-item-label class="tweet-content text-body1">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Eligendi quisquam nam aspernatur sed exercitationem
            reprehenderit tempore error laboriosam dolores.

            Nihil facilis exercitationem minima aperiam praesentium
            quibusdam ipsum ipsam veniam sapiente?
          </q-item-label>
          <div class="row justify-between q-mt-sm tweet-icons">
            <q-btn round flat color="grey" icon="far fa-comment" size="sm" />
            <q-btn round flat color="grey" icon="fas fa-retweet" size="sm" />
            <q-btn round flat color="grey" icon="far fa-heart" size="sm" />
            <q-btn round flat color="grey" icon="fas fa-trash" size="sm" />
          </div>
        </q-item-section>

        <q-item-section side top>
          1 min ago
        </q-item-section>
      </q-item>
    </q-list>
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
.tweet-content
  white-space: pre-line
.tweet-icons
  margin-left: -5px
</style>