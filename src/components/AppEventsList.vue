<script>
import { store } from "../store";

export default {
  name: "AppEventList",
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <section>
    <h1>Eventi:</h1>
    <div class="container">
      <div class="row">
        <div class="col-md-4 gy-4" v-for="event in store.eventList">
          <div class="card h-100">
            <div class="card-body">
              <h5 class="card-title">{{ event.name }}</h5>
              <h6 class="card-subtitle mb-2 text-muted">
                {{ event.user ? event.user.name : "Utente sconosciuto" }}
              </h6>
              <p class="card-text">
                Biglietti disponibili: {{ event.available_tickets }}
              </p>
              <a href="#" class="btn btn-primary">Dettagli:</a>
              <a href="#" class="btn btn-warning ms-2">Compra biglietti</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
