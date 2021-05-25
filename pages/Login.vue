<template>
    <div class="login">
        <div v-if="activePage == 'login'">
            <form>
                <fieldset>
                    <label for="email">Email</label>
                    <input id="email" type="email" required>
                </fieldset>
                <fieldset>
                    <label for="senha">Senha</label>
                    <input id="senha" type="password" pattern="" required>
                </fieldset>
                <fieldset>
                    <input id="checkbox" type="checkbox" checked>
                    <label for="checkbox">Continuar conectado?</label>
                </fieldset>
                <a href="#">Esqueceu sua senha?</a>
                <a href="#" @click="toSignInPage()">Criar uma conta</a>
                <button type="submit">Entrar</button>
            </form>
            <div>
                <p>Entre com</p>
                <div>
                    <div v-for="(social, index) in socials" :key="index">
                        <img src="../assets/images/placeholder-icon.svg" width="50" height="50" alt="icon-placeholder">
                        <p>{{ social }}</p>
                    </div>
                </div>
            </div>
        </div>
        <div v-if="activePage == 'cadastro'">
            <form>
                <fieldset>
                    <label for="nome">Nome</label>
                    <input id="nome" type="text" required>
                </fieldset>
                <fieldset>
                    <label for="email">Email</label>
                    <input id="email" type="email" required>
                </fieldset>
                <fieldset>
                    <label for="senha">Senha</label>
                    <input id="senha" type="password" pattern="^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9]).{6,12}$" required>
                </fieldset>
                <fieldset>
                    <label for="confirmar-senha">Confirmar senha</label>
                    <input id="confirmar-senha" type="password" pattern="^(?=.*[a-z])(?=.*[A-Z])(?=.*[0-9]).{6,12}$" required>
                </fieldset>
                <a href="#" @click="toLoginPage()">Já tem uma conta? Entre!</a>
                <fieldset>
                    <input id="checkbox-email" type="checkbox" checked>
                    <label for="checkbox-email">Aceito receber e-mails com as novidades.</label>
                </fieldset>
                <a href="#">Leia os termos de privacidade</a>
                <fieldset>
                    <input id="checkbox-privacidade" type="checkbox" checked required>
                    <label for="checkbox-privacidade">Concordo com os termos de privacidade.</label>
                </fieldset>
                <button type="submit">Cadastrar</button>
            </form>
            <div>
                <p>Cadastre-se com</p>
                <div>
                    <div v-for="(social, index) in socials" :key="index">
                        <img src="../assets/images/placeholder-icon.svg" width="50" height="50" alt="icon-placeholder">
                        <p>{{ social }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            activePage: 'login',
            socials: ['Google','GitHub','Facebook','Discord','Microsoft']
        };
    },
    methods: {
        toSignInPage() {
            this.activePage = 'cadastro';
        },
        toLoginPage() {
            this.activePage = 'login';
        },
    },
}
</script>
