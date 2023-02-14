# Registation-Form
<!DOCTYPE html>
<html>
    <head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"></html>
</head>
  <body onload="startup();">
    <div class="login">
      <form name='form-login'>

          <h1>Registration Form</h1>
          <label for="Fname">Name</label>
          <input type="text" id="fname" placeholder="Your Name" required><br>
          <label for="email">Email</label>
          <input type="email" id="email" placeholder="Username" required><br>

          <label for="pw">Password</label>
          <input type="password"
                 id= "pw"
                 placeholder="Password" required><br>
                 <label for="name">Date of Birth</label>
                 <input type="date" id="dob" name="dob" placeholder="Date of Birth" maxlength="8" required>
                 <script language="javascript">
                  var today = new Date();
                 var dd = String(today.getDate()).padStart(2, '0');
                 var mm = String(today.getMonth()+1).padStart(2, '0');		
                 var yyyy = today.getFullYear();
                 today = yyyy + '-' + mm + '-' + dd;
                 var mindate = '1967' + '-' + mm + '-' + dd;
                 document.getElementById("dob").min=mindate;
                 document.getElementById("dob").max=today;
                // $('#dob').attr('max',today);
             </script>
          <div id="remember">
            <br/>
            <input type="checkbox" value="lsRememberMe" id="rememberMe" required
                   style="display: inline-block;">
            <label>Accept Terms & condition</label>
        </div>
        <br/>
          <input id="rgstr_btn" type="submit" value="Register" onclick="store()">

      </form>
    </div>

    <div class="login" style="width:650px;">
      <form name='form-login'>
          <h1>Display Entries</h1>
          <table style="border:1px solid white;" width="100%">
            <tr>
              <th>Name</th>
              <th>Email</th>
              <th>Password</th>
              <th>Date of Birth</th>
              <th>Accept Terms&Codition</th>
            </tr>
            <tr>
              <td align="center">  
<p id="fnametd"></p>
              </td>
              <td align="center">  
                <p id="emailtd"></p>     
              </td>
              <td align="center"> 
                <p id="passtd"></p>      
              </td>
              <td align="center">
                <p id="dobtd"></p>
              </td>
              <td align="center">
                <p id="rememberMetd"></p>
              </td>
            </tr>
          </table>
          </form>
</div>    
  </body>
</html>
