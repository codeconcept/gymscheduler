<script>
  const nbOfDays = [
    { id: 1, text: "One day", value: 1 },
    { id: 2, text: "Two days", value: 2 },
    { id: 3, text: "Three days", value: 3 },
    { id: 4, text: "Four day", value: 4 },
    { id: 5, text: "Five days", value: 5 },
    { id: 6, text: "Six days", value: 6 },
    { id: 7, text: "one day", value: 7 }
  ];

  let nbDaysTrainingPerWeek;

  function handleSubmit(event) {
    console.log('handleSubmit');
  }

  function handleNumberDays(event) {
    nbDaysTrainingPerWeek = event.target.value;
    console.log(nbDaysTrainingPerWeek.value);
  }
</script>

<style>

</style>

<div>
  <form on:submit|preventDefault={handleSubmit}>
    <select bind:value={nbDaysTrainingPerWeek}>
      {#each nbOfDays as day (day.id)}
        <option value={day}> {day.text} </option>
      {/each}
    </select>
  </form>
  {JSON.stringify(nbDaysTrainingPerWeek)}
</div>
