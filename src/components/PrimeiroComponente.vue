<template>
    <!-- Conceitos abordados: Dados dinâmicos (interpolação)
    e Data binding -->
    <div>
        <h1>Olá {{frame}}!</h1>

         <div class="form-control">
                <div class="txt-group">
                    <input id="txtForMail" name="password" v-model="input_name"
                    placeholder="maratonas" type="text">
                    <label for="txtForMail">Email</label>
                    <br>
                    <span class= "hidden">Mensagem de erro</span>
                </div>

                <button class="btn-larger">
                    Vamos lá
                    <img src="../assets/btn-arrow.svg" alt="">
                </button>
            </div>
            <p style="font-size: 20px">Data binding here: <b>{{input_name}}</b></p>

        

    </div>
</template>

<script>
export default{
    name: 'PrimeiroComponente',
    data() {
        return{
            frame: 'Angular',
            input_name:""
        }
    }
}
</script>

<style scoped>
    .txt-group{
    position: relative;
    display:inline-block
    }
    .txt-group input{
        width: 452px;
        height: 60px;
        background: #FFFFFF;
        border: 1px solid rgba(0, 0, 0, 0.08);
        box-sizing: border-box;

        /* font styles */
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 22px;

        padding-left: 16px;
        padding-top: 26px;
        color: rgba(0, 0, 0, 0.9);
    }
    .txt-group input::placeholder{
        color: transparent;
    }
    .txt-group label{
        position: absolute;
        left: 16px;
        top: 19px;

        /* font styles */
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 22px;
        color: rgba(0, 0, 0, 0.4);
        transition: all 0.1s;
    }
    .txt-group input:focus + label,
    .txt-group input:not(:placeholder-shown) + label{
        top: 7px;
        font-size: 13px;
    }
    .txt-group span{
        font-style: normal;
        font-weight: 400;
        font-size: 15px;
        line-height: 18px;
        color: #FFA00A;
        padding-left: 2px;
    }
    .btn-larger{
        width: 182px;
        height: 60px;
        background: #D81F26;
        border: none;
        color: #fff;

        /* Tipografia */
        font-style: normal;
        font-weight: normal;
        font-size: 24px;
        line-height: 33px;
    }
    .btn-larger img{
        width: 8.75px;
        height: 16.25px;
        margin-left: 7px;
    }
    .form-control{
        display: flex;
    }
</style>
