```html
<div id="password" class="input_data">
	<input id="show_password" type="password" required />
	<div class="underline"></div>
	<label>비밀번호</label>
	<i class="fas fa-eye"></i>
</div>
```

```jsx
$(document).ready(function(){
    $('#password i').on('click',function(){
        console.log("클릭되었다")
        $('#password').toggleClass('active');
        if($('#password').hasClass('active')){
            $(this).attr('class',"fas fa-eye-slash");
            $('#show_password').attr('type',"text");
        }else{
            $(this).attr('class',"fa fa-solid fa-eye");
            $('#show_password').attr('type','password');
        }
    });
});
```