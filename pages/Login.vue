<template>
    <div class="login">
        <form action="">
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
            <a href="#">Criar uma conta</a>
            <button type="submit">Entrar</button>
        </form>
    </div>
</template>
