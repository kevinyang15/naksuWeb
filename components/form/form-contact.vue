<template>
    <form @submit.prevent="onSubmit" id="contact-form">
        <div class="tp-contact-input-form">
            <div class="row">
                <div class="col-xl-12 col-lg-12">
                    <div class="tp-contact-input p-relative">
                        <label style="color: white;">Nombre</label>
                        <field name="name" v-slot="{ field }">
                          <input type="text" v-bind="field" name="name">
                        </field>
                        <err-msg :msg="errors.name" />
                    </div>
                </div>
                <div class="col-xl-12 col-lg-12">
                    <div class="tp-contact-input p-relative">
                        <label style="color: white;">Teléfono</label>
                        <field name="phone" v-slot="{ field }">
                          <input type="text" v-bind="field" name="phone">
                        </field>
                        <err-msg :msg="errors.phone" />
                    </div>
                </div>
                <div class="col-xl-12 col-lg-12">
                    <div class="tp-contact-input p-relative">
                        <label style="color: white;">Email</label>
                        <field name="email" v-slot="{ field }">
                         <input type="email" v-bind="field" name="email">
                        </field>
                        <err-msg :msg="errors.email" />
                    </div>
                </div>
                <div class="col-xl-12 col-lg-12">
                    <div class="tp-contact-input p-relative">
                        <label style="color: white;">Asunto</label>
                        <field name="subject" v-slot="{ field }">
                          <input type="text" v-bind="field" name="subject">
                        </field>
                        <err-msg :msg="errors.subject" />
                    </div>
                </div>
                <div class="col-xl-12">
                    <div class="tp-contact-input p-relative">
                        <label style="color: white;">Mensaje</label>
                        <field name="message" v-slot="{ field }">
                          <textarea v-bind="field" name="message"></textarea>
                        </field>
                        <err-msg :msg="errors.message" />
                    </div>
                </div>
                <div class="col-xl-12">
                    <div class="tp-contact-input-remeber">
                        <input id="remeber" type="checkbox">
                        <label for="remeber" style="color: white;">Guardar mi nombre y contacto para recibir noticias.</label>
                    </div>
                </div>
                <div class="tp-contact-btn">
                    <button type="submit" class="tp-btn-inner" style="color:#FBF7BA ;">Enviar mensaje</button>
                </div>
            </div>
        </div>
    </form>
</template>

<script setup lang="ts">
import { useForm, Field } from "vee-validate";
import * as yup from "yup";

interface IFormValues {
  name?: string | null;
  email?: string | null;
  subject?: string | null;
  message?: string | null;
  phone?: string | null;
}

const { errors, handleSubmit, resetForm } = useForm<IFormValues>({
  validationSchema: yup.object({
    name: yup.string().required("El nombre es requerido"),
    email: yup.string().required("El Email es requerido").email("El Email es invalido"),
    subject: yup.string().required("El asunto es requerido"),
    message: yup.string().required("El mensaje es requerido"),
    phone: yup.string().required("El teléfono es requerido")
  }),
});

const onSubmit = handleSubmit((values) => {
  alert(JSON.stringify(values, null, 2));
  resetForm();
});

</script>