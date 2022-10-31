# oauth_gateway
I use this repo as callback URLs for OAuth apps

<div id="result"></div>

<script>
  {
    const pre = document.createElement("pre");
    const code = document.createElement("code");
    code.textContent = JSON.stringify(
      Object.fromEntries(new URLSearchParams(window.location.search)),
      null,
      2
    );
    pre.appendChild(code);
    document.getElementById("result").appendChild(pre);
  }
</script>
