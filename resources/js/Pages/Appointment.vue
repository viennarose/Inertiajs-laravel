<template>
 <h1>My Appointments</h1>
 <hr>

<div class="d-flex align-contents-between">
    <div class="card mb-3" v-for="appointment in appointments" :key="appointment.id">
        <div class="card-header">
            <h5>Appointment Number: {{appointment.id}}</h5>
        </div>
        <div class="card-body" >
            <h6>Patient Information</h6>
            <table class="table">
                <tr>
                    <th>Name:</th>
                    <td>{{appointment.name}}</td>
                </tr>
                <tr>
                    <th>Contact:</th>
                    <td>{{appointment.contact}}</td>
                </tr>
            </table>
        </div>
    </div>
</div>
</template>

<script setup>
import Layout from '../Shared/Layout.vue'

</script>
<script>
export default {
    layout: Layout,
    props: {
        appointments: Array
    }
}
</script>

<style scoped>
.card{
    width: 375px;

}
</style>
