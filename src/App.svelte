<script>
  let email = "";
  let password = "";
</script>

<style>
  body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f4f4f4;
    margin: 0;
  }

  .login-container {
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    width: 300px;
    text-align: center;
  }

  input {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 4px;
  }

  button {
    width: 100%;
    padding: 10px;
    background: #007BFF;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
  }

  button:hover {
    background: #0056b3;
  }
</style>

<div class="login-container">
  <h2>Iniciar Sesión</h2>
  <form on:submit|preventDefault={() => console.log(email, password)}>
    <input
      type="email"
      placeholder="Correo electrónico"
      bind:value={email}
      required
    />
    <input
      type="password"
      placeholder="Contraseña"
      bind:value={password}
      required
    />
    <button type="submit">Iniciar Sesión</button>
  </form>
</div>
