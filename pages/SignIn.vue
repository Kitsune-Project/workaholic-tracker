<template>
    <div class="sign-in">
        <form action="">
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
            <fieldset>
                <input id="checkbox" type="checkbox" checked>
                <label for="checkbox">Aceito receber e-mails com as novidades.</label>
            </fieldset>
            <button type="submit">Cadastrar</button>
        </form>
    </div>
</template>
