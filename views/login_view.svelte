<script lang='ts'>
    import Button from "../components/button.svelte";
    import PasswordField from "../components/password_field.svelte";
    import TextField from "../components/text_field.svelte";
    import {login_title_str, user_str, password_str, login_button_str, no_account_str} from '../resources/strings.json';
    import links from "../resources/links.json";
    let error:string = "";

    function validate_login(){
        
    }

</script>

<div class="view">
    <div class="form_div">
        <h1>{login_title_str}</h1>
        <form class="form">
            <TextField id="user" hint={user_str}/>
            <PasswordField id="password" hint={password_str} />
            <Button message={login_button_str} method={validate_login} />
            <a href={links[2].url}><u>{no_account_str}</u></a>
        </form>
    </div>

    <div class="side_img">
        <div class="img_container">
            <img src='../resources/download2.avif' alt='monkeypic'/>
        </div>
    </div>

</div>

<style>
    h1{
        font-weight: bold; 
        font-size: 80px;
        color: black; 
        margin-bottom: 26px
    }
    form{
        text-align: right;
    }
    a{
        color: black;
        font-size: 25px;
        margin-right: 10px;
    }
    .view{
        display: flex;
        align-items: center;
        margin: 0px 80px 0px 80px;
    }
    .form_div{
        flex: 1;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        text-align: center;
        padding: 20px;
        margin-bottom: 150px;
    }
    .side_img{
        flex: 1;
    }
    .img_container{
        border-radius: 10px;
        overflow: hidden;
        margin-bottom: 20px;
    }

    .img_container img{
        width: 100%;
        height: auto;
    }

</style>