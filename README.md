## Placeholder OAuth Redirect URL

I use [this repo](https://github.com/dtinth/oauth_gateway) as a [placeholder callback URL](https://oauth.spacet.me/) for OAuth apps.

<div id="result"></div>

<script>
  {
    const h3 = (t) => {
      const el = document.createElement("h3");
      el.textContent = t;
      return el;
    }
    const pre = (t) => {
      const el = document.createElement("pre");
      const code = document.createElement("code");
      code.textContent = t;
      el.appendChild(code);
      return el;
    }
    document.getElementById("result").appendChild(h3("Query:"));
    document.getElementById("result").appendChild(pre(
      JSON.stringify(
        Object.fromEntries(new URLSearchParams(window.location.search)),
        null,
        2
      )
    ));
    document.getElementById("result").appendChild(h3("Hash:"));
    document.getElementById("result").appendChild(pre(
      JSON.stringify(
        Object.fromEntries(new URLSearchParams(window.location.hash.replace(/^#/, ""))),
        null,
        2
      )
    ));
  }
</script>
