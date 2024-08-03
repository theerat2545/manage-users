<template>
  <div class="q-pa-md">
    <div class="q-py-md"><q-btn label="Add" color="primary" icon="add" @click="onCreate" /></div>
    <q-table
      title="Users"
      :rows="rows"
      :columns="columns"
      row-key="name"
    >
  <template v-slot:body-cell-avatar="props">
    <q-td :props="props">
      <q-img :src="props.row.avatar"/>
    </q-td>
  </template>
  <template v-slot:body-cell-actions="props">
    <q-td class="q-gutter-sm" :props="props">
      <q-btn  color="warning" icon="mode_edit" @click="onEdit(props.row.id)" />
      <q-btn  color="negative" icon="delete" @click="onDelete(props.row.id)" />
    </q-td>
  </template>
  </q-table>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import router from '../router'
const columns = ref([
  { name: 'id', align: 'center', label: '#ID', field: 'id', sortable: true },
  { name: 'avatar', align: 'center', label: 'Avatar', field: 'avatar'}, // ใช้ 'username' เป็น profile
  { name: 'fname', align: 'center', label: 'Firstname', field: 'fname', sortable: true }, // ใช้ 'name' สำหรับชื่อ
  { name: 'lname', align: 'center', label: 'Lastname', field: 'lname', sortable: true },
  { name: 'username', align: 'center', label: 'Username', field: 'username', sortable: true },
  { name: 'actions', align: 'center', label: 'Actions', field: 'actions'},
]);


const rows = ref([])

const fetchData = () => {
  fetch("https://www.melivecode.com/api/users")
  .then(res => res.json())
  .then((result) => {
    rows.value = result
  })
}
fetchData()

const onEdit = (id) =>{
alert(id + " edit")
}

const onDelete = (id) =>{
alert(id + " delete")
}

const onCreate = () =>{
  router.push('/create')
}
</script>
