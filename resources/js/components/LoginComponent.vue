<template>
    <div class="container-fluid"
        style="height: 80vh; background-image: url('build/assets/img/ace-login.jpg'); background-size: cover; background-repeat: no-repeat; background-position: center bottom; height: 100vh;">
        <div class="row justify-content-center align-items-center" style="height: 100%;">
            <div class="col-md-4">
                <div class="card">
                    <div class="card-header"><img src="build/assets/img/Logo preto.png" height="30px" class="pe-3"
                            alt="">Login</div>
                    <div class="card-body">
                        <form method="POST" action="">
                            <input type="hidden" name="_token" :value="token_csrf">
                            <div class="row mb-3">
                                <label for="email" class="col-md-4 col-form-label text-md-end">E-mail</label>
                                <div class="col-md-6">
                                    <input id="email" type="email" class="form-control" name="email" value="" required
                                        autocomplete="email" autofocus>
                                </div>
                            </div>
                            <div class="row mb-3">
                                <label for="password" class="col-md-4 col-form-label text-md-end">Senha</label>
                                <div class="col-md-6">
                                    <input id="password" type="password" class="form-control" name="password" required
                                        autocomplete="current-password">
                                </div>
                            </div>
                            <div class="row mb-3">
                                <div class="col-md-6 offset-md-4">
                                    <div class="form-check">
                                        <input class="form-check-input" type="checkbox" name="remember" id="remember">

                                        <label class="form-check-label" for="remember">
                                            Lembre-se de mim.
                                        </label>
                                    </div>
                                </div>
                            </div>
                            <div class="row mb-0">
                                <div class="col-md-8 offset-md-4">
                                    <button type="submit" class="btn btn-primary">
                                        Login
                                    </button>

                                    <a class="btn btn-link" href="#">
                                        Esqueci a senha.
                                    </a>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: [
        'token_csrf'
    ]
}
</script>
