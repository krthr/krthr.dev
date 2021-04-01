<template>
  <div>
    <form @submit.prevent="submit">
      <div class="form-control">
        <input
          v-model="form.name"
          type="text"
          placeholder="Name"
          class="input input-bordered"
        />
      </div>

      <div class="form-control">
        <input
          v-model="form.subject"
          type="text"
          placeholder="Subject"
          class="input input-bordered"
        />
      </div>

      <div class="form-control">
        <input
          v-model="form.email"
          type="email"
          placeholder="Email"
          class="input input-bordered"
        />
      </div>

      <div class="form-control">
        <textarea
          v-model="form.message"
          class="textarea h-24 textarea textarea-bordered"
          placeholder="Message"
        ></textarea>
      </div>

      <div class="form-control">
        <button class="btn btn-primary" type="submit">Enviar</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  data: () => ({
    form: {
      name: '',
      subject: '',
      email: '',
      message: '',
    },
  }),

  methods: {
    submit() {
      // TODO
    },
  },
}
</script>

<style scoped>
.form-control {
  @apply mb-3;
}
</style>