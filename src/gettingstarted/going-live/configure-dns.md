# Going live

## Configure your DNS provider

The next step is to configure your DNS provider to point to the domain of your `master` environment on Platform.sh.

<asciinema-player src="/videos/asciinema/cname-target.cast" preload=1></asciinema-player>

You can access the CNAME target from your terminal by using the CLI and the command

```bash
platform environment:info edge_hostname
```

Add a CNAME record from your desired domain to the value of the `edge_hostname`. Depending on your registrar, this value may be called an "Alias" or something similar.

If your application is going to serve multiple domains, you will need to add a CNAME record for each of them.

You can find out more information about using an apex domain and CNAME records in the [Going Live documentation](/golive/steps/dns.md).

Depending on your registrar and the TTL you set for the domain, it may take up to 72 hours for the DNS change to fully propagate across the Internet.

<div class="buttons">
  <a class="button-link prev" onclick="gitbook.navigation.goPrev()">Back</a>
  <a class="button-link next" onclick="gitbook.navigation.goNext()">I have configured my DNS provider</a>
</div>
