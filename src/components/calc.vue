<template>
  <div class="calculator">
    <div class="app-title">
      <h1 class="fs-2">SPLI</h1>
      <h1 class="fs-2">TTER</h1>
    </div>
    <div class="main-calc bg-light">
      <p class="flex text-dark-accent-1 bold">Bill</p>
      <div class="flex bg-light-accent-2 input-bar">
        <p class="flex fs-2 text-dark-accent-2">$</p>
        <input
          class="flex bill-input fs-2 text-dark bold"
          v-model="bill"
          placeholder="142.55"
        />
      </div>
      <p class="flex fs-4 bold text-dark-accent-1">Select Tip %</p>
      <div class="grid tip-select">
        <button class="fs-2 bg-dark text-light bold">5%</button>
        <button class="fs-2 bg-dark text-light bold">10%</button>
        <button class="fs-2 bg-dark text-light bold active">15%</button>
        <button class="fs-2 bg-dark text-light bold">20%</button>
        <button class="fs-2 bg-dark text-light bold">25%</button>
        <button class="fs-2 bg-dark text-light bold">Custom</button>
      </div>
      
        <p class="flex fs-4 bold text-dark-accent-1">Number of People</p>
        <div class="flex num-people bg-light-accent-2">
          <p class="flex fs-2 text-dark-accent-2">!</p>
        <input
          class="flex people-input fs-2 text-dark bold"
          v-model="numPeople"
          placeholder="5"
        />
      </div>
      <div class="tip-total">
        <div>
          <div class="flex tip-amount">
            <p class="fs-4 text-light bold flex tip-amount-text">Tip Amount <br><span class="fs-5 text-dark-accent-2 bold">/ person</span>
            </p>
            <p class="fs-1 text-primary bold flex-inline">{{ 4.27 }}</p>
          </div>
          <div class="flex tip-amount">
            <p class="fs-4 text-light bold flex tip-amount-text">Total<br><span class="fs-5 text-dark-accent-2 bold">/ person</span></p>
            <p class="fs-1 text-primary bold flex-inline">{{ 32.79 }}</p>
          </div>
        </div>
        <button class="fs-3 bg-primary text-dark bold">RESET</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TipCalculator",
};
</script>

<style scoped>
.main-calc {
  border-radius: 1rem;
  padding: 1.5rem;
}

.tip-select {
  gap: 1.25rem;
  grid-template-columns: 1fr 1fr;
  margin-bottom: 2rem;
  margin-top: 1rem;
}

.tip-total {
  background-color: hsl(183, 100%, 15%);
  padding: 1rem;
  border-radius: 1rem;
}

.app-title {
  margin: 1.75rem auto;
  letter-spacing: 10px;
  color: #3d6666;
  text-align: center;
}

.input-bar {
  flex-direction: row;
  margin-bottom: 2rem;
  margin-top: 0.5rem;
}
.bill-input {
  background-color: transparent;
  border: none;
  margin-left: auto;
  width: 30%;
}

.num-people {
  flex-direction: row;
  margin-bottom: 2rem;
  margin-top: 0.5rem;
}

.people-input {
  background-color: transparent;
  border: none;
  margin-left: auto;
  width: 30%;
}

.tip-amount {
  flex-direction: row;
  justify-content: space-between;
  align-content: center;
  padding: 0.5rem;
}

.tip-amount-text {
  flex-direction: column;
}
</style>