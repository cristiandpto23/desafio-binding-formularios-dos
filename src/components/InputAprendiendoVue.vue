<script>
export default {
    name: 'InputAprendiendoVue',
    data() {
        return {
            titulo: 'Estoy aprendiendo Vue 3',
            emoji: '👨‍💻',
            apreciacion: '',
            competencia: [],
            opinion: '',
        };
    },
};
</script>

<template>
    <main class="d-md-flex flex-column flex-lg-row gap-4">
        <section class="bg-dark text-white p-5 rounded-4 ingreso-inputs">
            <form>
                <div class="d-flex">
                    <label class="pe-2">Título: </label>
                    <input type="text" name="titulo" v-model="titulo" />
                </div>

                <hr />

                <div class="d-flex">
                    <label class="pe-2">Emoji: </label>
                    <select v-model="emoji">
                        <option value="👨‍💻">👨‍💻</option>
                        <option value="🙋‍♂️">🙋‍♂️</option>
                        <option value="🤩">🤩</option>
                        <option value="🥱">🥱</option>
                        <option value="🥴">🥴</option>
                    </select>
                </div>

                <hr />

                <div class="d-flex gap-4">
                    <label> Apreciación: </label>
                    <div class="d-flex gap-2">
                        <div class="d-flex gap-1">
                            <input type="radio" class="form-check-input" name="flexRadioDefault" id="m" value="Regular" v-model="apreciacion" />
                            <label class="form-check-label fw-normal" for="soltero"> Regular </label>
                        </div>
                        <div class="d-flex gap-1">
                            <input type="radio" class="form-check-input" name="flexRadioDefault" id="m" value="Bien" v-model="apreciacion" />
                            <label class="form-check-label fw-normal" for="soltero"> Bien </label>
                        </div>
                        <div class="d-flex gap-1">
                            <input type="radio" class="form-check-input" name="flexRadioDefault" id="m" value="Muy bien" v-model="apreciacion" />
                            <label class="form-check-label fw-normal" for="soltero"> Muy bien </label>
                        </div>
                        <div class="d-flex gap-2">
                            <input type="radio" class="form-check-input" name="flexRadioDefault" id="m" value="Increíble" v-model="apreciacion" />
                            <label class="form-check-label fw-normal" for="soltero"> Increíble </label>
                        </div>
                    </div>
                </div>

                <hr />

                <div class="d-flex gap-4">
                    <label class="text-start"> Competencias <br />aprendidas: </label>
                    <div>
                        <div class="d-flex gap-5 justify-content-between">
                            <div class="d-flex gap-2 form-check">
                                <input type="checkbox" class="form-check-input" v-model="competencia" value="Morfología de un componente" id="flexCheckAmerica" />
                                <label class="form-check-label fw-normal text-start" for="flexCheckAmerica">Morfología de un<br />componente</label>
                            </div>
                            <div class="d-flex gap-2 form-check">
                                <input type="checkbox" class="form-check-input" v-model="competencia" value="Directivas" id="flexCheckAmerica" />
                                <label class="form-check-label fw-normal text-start" for="flexCheckAmerica">Directivas</label>
                            </div>
                        </div>
                        <div class="d-flex gap-2 justify-content-between">
                            <div class="d-flex gap-2 form-check">
                                <input type="checkbox" class="form-check-input" v-model="competencia" value="One-Way y Two-Way data binding" id="flexCheckAmerica" />
                                <label class="form-check-label fw-normal text-start" for="flexCheckAmerica">One-Way y Two-Way<br />data binding</label>
                            </div>
                            <div class="d-flex gap-2 form-check">
                                <input type="checkbox" class="form-check-input" v-model="competencia" value="Estado" id="flexCheckAmerica" />
                                <label class="form-check-label fw-normal text-start" for="flexCheckAmerica">Estado</label>
                            </div>
                        </div>
                        <div class="d-flex gap-2 justify-content-between">
                            <div class="d-flex gap-2 form-check">
                                <input type="checkbox" class="form-check-input" v-model="competencia" value="El patrón de diseño MVVM" id="flexCheckAmerica" />
                                <label class="form-check-label fw-normal text-start" for="flexCheckAmerica">El patrón de diseño<br />MVVM</label>
                            </div>
                        </div>
                    </div>
                </div>

                <hr />

                <div class="d-flex gap-4">
                    <label class="text-start"> Opinión: </label>
                    <textarea name="" id="" v-model="opinion"></textarea>
                </div>
            </form>
        </section>

        <section class="w-100 texto-Reactivo p-5 border rounded-5">
            <div class="d-flex justify-content-center">
                <h1>{{ emoji }}</h1>
            </div>
            <br>
            <div class="d-flex justify-content-center">
                <h2>{{ titulo }}</h2>
            </div>
            <br>
            <div class="d-flex justify-content-center">
                <h5> Y me parece {{ apreciacion }}</h5>
            </div>
            <br>
            <div class="d-flex justify-content-center">
                <h4>He aprendido:</h4>
            </div>
            <div class="d-flex justify-content-center">
                    <p>{{ competencia }}</p>
            </div>
            <div class="d-flex flex-column justify-content-center">
                <h5>Mi opinión hasta ahora del framework es:</h5>
                <p>{{ opinion }}</p>
            </div>
            <div>
                <h5 class="fw-normal">Ahora podré desarrollar aplicaciones más cómodamente!</h5>
            </div>
        </section>
    </main>
</template>

<style scoped>
    textarea {
        width: 100%;
    }
    .ingreso-inputs {
        min-width: 45%;
        
    }

</style>
