<template>
  <div>
    <form
      class="flex flex-col justify-center"
    >
      <label class="text-2xl">input term</label>
      <input type="number" v-model="number" />
      <button type="submit">Ok</button>
    </form>
    <div>
      <p>{{ number }}</p>
    </div>
    <div v-if="teams.length > 0">
      <ShowTeams />
    </div>
  </div>
</template>

<script setup lang="tsx">
const number = ref(0)
const teams = ref([1, 2, 3, 4, 5, 6, 7, 8])

const sytler = ref<Styler>({
    border: "2px solid",
    backgournd: "gray"
})

interface Styler {
  border: string | null;
  backgournd: string | null;
}

const ShowTeams = () => (
  <div class=" text-2xl">
    <h1>555</h1>
    {teams.value.map((team) => {
      return (
        <h1>{team}</h1>
      )
    })}
  </div>
)
</script>

<style lang="scss" scoped></style>
