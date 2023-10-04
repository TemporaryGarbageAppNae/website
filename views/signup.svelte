<script>
	import Button from './../components/button.svelte';
    import PasswordField from '../components/password_field.svelte';
    import TextField from '../components/text_field.svelte';
    import { 
            signup_title_str, 
            password_str, 
            company_name_str, 
            email_str, 
            CNPJ_str, 
            confirm_password_str, 
            confirm_button_str}
    from '../resources/strings.json';

    function validade_signup(){

    }
</script>

<div class="view">
    <h1 class="title">{signup_title_str}</h1>
        <form class="column">
            <TextField id="company_name" hint={company_name_str}/>
            <TextField id="email" hint={email_str}/>
            <TextField id="CNPJ" hint={CNPJ_str}/>
        </form>
        <form class="column">
            <PasswordField id="password" hint={password_str}/>
            <PasswordField id="confirm_password" hint={confirm_password_str}/>
            <Button message={confirm_button_str} method={validade_signup}/>
        </form>
</div>

<style>
    *{
        box-sizing: border-box;
        margin-top: 220px;
    }
    .view{
        align-items: center;
        margin: 0px 80px 0px 80px
    }
    h1{
        font-weight: bold; 
        font-size: 65px;
        color: black; 
        margin-bottom: 0px;
        display: flex;
        margin-left: 40px;
    }
    .column{
        float: left;
        width: 50%;
        padding: 10px;
    }
    form{
        margin-top: 20px;
    }
    form:after{
        content: "";
        display: table;
        clear: both;
    }
</style>

