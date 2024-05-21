<script setup>
import { inject, reactive, onMounted, ref } from 'vue';
import '@melloware/coloris/dist/coloris.css';
import Coloris from '@melloware/coloris';

const toast = inject('moshaToast');
const swal = inject('$swal');

const state = reactive({
  loading: false,
  action: 'none',
  only: 'all',
  stock: 'ever',
  tag: [],
  action_phone: null,
  opts: {},
});

const refs = ref(null);

const getDescription = (action, type) => {
  return type?.find(({ value }) => value === action)?.['description'] || '';
};

const findEl = (name) => refs.value?.[name] || null;

const saveTemplate = (el) => {
  el.addEventListener('click', async () => {
    const payload = { opts: state.opts };
    const action = state.action;

    if (action === 'whatsapp') {
      const phone = state.action_phone;
      if (!phone) {
        toast('Insira um número de telefone na aba \'Ação\'', { type: 'danger' });
        return;
      }
    }

    state.loading = true;
  });
};

const reset = () => {
  const findSettingTab = document.querySelector('button[data-bs-toggle="pill"][data-bs-target="#setting"]');
};

onMounted(() => {
  Coloris.init();
  Coloris({
    el: '.coloris',
    theme: 'pill',
    themeMode: 'dark',
    formatToggle: true,
    closeButton: true,
    closeLabel: 'Fechar',
  });
});
</script>

<template>
  <div class="container" ref="refs">
    <section>
      <button @click="saveTemplate">Salvar Template</button>
    </section>
  </div>
</template>
