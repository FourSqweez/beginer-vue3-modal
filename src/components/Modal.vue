<template>
  <div class="backdrop" @click.self="closeModal">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <slot>default content</slot>
      <div class="actions">
        <slot name="links"></slot>
      </div>
      <slot name="test"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props: ['theme'],
  methods: {
    closeModal() {
      this.$emit('close')
    },
  },
}
</script>

<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.modal h1 {
  color: cadetblue;
  border: none;
  padding: 0;
}

.modal p {
  font-style: normal;
}

.modal.sale {
  background: crimson;
  color: white;
}

.modal.sale h1 {
  background: crimson;
  color: white;
}

.modal .actions a {
  color: #333;
  padding: 8px;
  border: 1px solid #eee;
  border-radius: 4px;
  text-decoration: none;
  margin: 10px;
}

.modal.sale .actions a {
  color: white;
}
</style>
