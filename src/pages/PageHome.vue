<template>
  <q-page class="constrain q-pa-md">
    <q-card v-for="post in posts" :key="post.id" class="card-post q-mb-md" flat bordered>
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://cdn.quasar.dev/img/boy-avatar.png">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">Evgenii_Morgunov</q-item-label>
          <q-item-label caption>
            {{post.location}}
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />
      <q-img
        :src="post.imageUrl"
      />
      <q-card-section>
        <div>{{post.caption}}</div>
        <div class="text-caption text-grey">{{post.date}}</div>
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
export default {
  name: 'PageHome',
  data(){
    return {
      posts:[
        {
          id:1,
          caption:'New image',
          date:1621308155312,
          location: 'Tyumen, Russia',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg',
        },
        {
          id:2,
          caption:'New image',
          date:1621308155312,
          location: 'Tyumen, Russia',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg',
        },
        {
          id:3,
          caption:'New image',
          date:1621308155312,
          location: 'Tyumen, Russia',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg',
        },
        {
          id:4,
          caption:'New image',
          date:1621308155312,
          location: 'Tyumen, Russia',
          imageUrl:'https://cdn.quasar.dev/img/parallax2.jpg',
        },
      ]
    }
  }
}
</script>
<style lang="sass">
  .card-post
    .q-img
      min-height: 200px
</style>