<template>
    <q-page class="flex flex-center bg-grey-3">
        <q-card class="q-pa-md col-4 " style="height: 400px; width:300px; border-radius: 10px;">
            <div class="flex flex-center">
                <q-avatar square color="red" text-color="white" icon="directions" />
            </div>
            <div class="flex flex-center q-my-md" style="font-size: 30px; ">
                LogIn
            </div>
            <div class="flex flex-center row">
                <div class="flex flex-center">
                    <q-avatar>
                        <img src="https://cdn.quasar.dev/img/avatar.png">
                    </q-avatar>
                    <div class="text-weight-bold">
                        Hello XYZ, enter your password to Login<br>to your account
                    </div>
                </div>
            </div>
            <div class="flex flex-center">

            </div>
            <div class="q-my-md">
                <q-input type="password" label="password" v-model="formData.password"></q-input>
            </div>
            <div class="row q-my-sm">
                <q-btn class="col" color="green" rounded unelevated label="Login" @click="login"></q-btn>


            </div>
            <div class="flex flex-center">
                <q-btn flat color="red" label="forget password?" no-caps />
            </div>

        </q-card>
    </q-page>
</template>
<script>
export default {
    data() {
        return {
            formData: {},
            response: {}
        }
    },

}
</script>
  
  