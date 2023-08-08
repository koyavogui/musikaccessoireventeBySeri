<template>
  <q-page padding class="">
    <div class="row q-pa-md q-mt-md">
      <q-skeleton size="2.8rem" style="border-radius: 0.5rem" />
      <q-space />
      <q-skeleton size="2.8rem" style="border-radius: 0.5rem" />
    </div>
    <section class="q-pa-md">
      <!-- CArte d'article en vedette -->
      <q-skeleton
        height="10rem"
        square
        class="q-pa-md row items-end bg-grey-7"
        style="border-radius: 0.8rem"
      >
        <q-skeleton
          square
          height="1.8rem"
          width="8rem"
          style="border-radius: 0.5rem"
          class="bg-white"
        />
      </q-skeleton>
    </section>
    <div class="q-px-md">
      <q-skeleton type="text" width="40vw" style="border-radius: 0.5rem" />
    </div>
    <section class="q-py-md">
      <q-tabs
        v-model="tab"
        dense
        inline-label
        indicator-color="transparent"
        class="bg-transparent"
      >
        <q-tab name="mails" :ripple="false" class="">
          <q-skeleton
            square
            height="2.3rem"
            width="8rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
        <q-tab name="alarms" class="q-px-sm" :ripple="false">
          <q-skeleton
            square
            height="2.3rem"
            width="6rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
        <q-tab name="movies" :ripple="false">
          <q-skeleton
            square
            height="2.3rem"
            width="8rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
        <q-tab name="photos" class="q-px-sm" :ripple="false">
          <q-skeleton
            square
            height="2.3rem"
            width="5rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
        <q-tab name="videos" :ripple="false">
          <q-skeleton
            square
            height="2.3rem"
            width="7rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
        <q-tab name="addressbook" class="q-px-sm" :ripple="false">
          <q-skeleton
            square
            height="2.3rem"
            width="8rem"
            class="bg-grey-4"
            style="border-radius: 0.5rem"
          />
        </q-tab>
      </q-tabs>
      <q-tab-panels v-model="tab" animated dense class="q-px-md">
        <q-tab-panel name="mails" class="q-px-none q-gutter-y-sm">
          <q-skeleton
            v-for="n in 2"
            :key="n"
            height="9rem"
            square
            class="q-pa-sm row items-center bg-grey-4"
            style="border-radius: 0.8rem"
          >
            <q-skeleton
              square
              height="7rem"
              width="7rem"
              style="border-radius: 0.5rem"
              class="bg-grey-7"
            />
          </q-skeleton>
        </q-tab-panel>

        <q-tab-panel name="alarms">
          <q-skeleton
            height="9rem"
            square
            class="q-pa-sm row items-center bg-grey-4"
            style="border-radius: 0.8rem"
          >
            <q-skeleton
              square
              height="7rem"
              width="7rem"
              style="border-radius: 0.5rem"
              class="bg-grey-7"
            />
          </q-skeleton>
        </q-tab-panel>

        <q-tab-panel name="movies">
          <div class="text-h6">Movies</div>
          Lorem ipsum dolor sit amet consectetur adipisicing elit.
        </q-tab-panel>
      </q-tab-panels>
    </section>
  </q-page>
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
  setup() {
    return {
      tab: ref("mails"),
    };
  },
});
</script>
