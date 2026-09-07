# custom_caddy
自定义插件编译caddy
```powershell
$env:GOOS="linux"
$env:GOARCH="amd64"
xcaddy build v2.11.4 --output ./caddy_linux_amd64 `
--with github.com/greenpau/caddy-security `
--with github.com/caddyserver/replace-response `
--with github.com/caddyserver/replace-response `
--with github.com/sjtug/caddy2-filter `
--with github.com/mholt/caddy-webdav `
--with github.com/mholt/caddy-l4 `
--with github.com/mholt/caddy-ratelimit `
--with github.com/git001/caddyv2-upload

```

### 插件清单
```text
caddy.listeners.layer4
http.authentication.providers.authorizer
http.handlers.authenticator
http.handlers.filter
http.handlers.rate_limit
http.handlers.replace_response
http.handlers.upload
http.handlers.webdav
layer4
layer4.handlers.close
layer4.handlers.echo
layer4.handlers.postgres_tls
layer4.handlers.proxy
layer4.handlers.proxy_protocol
layer4.handlers.socks5
layer4.handlers.subroute
layer4.handlers.tee
layer4.handlers.throttle
layer4.handlers.tls
layer4.handlers.vars
layer4.matchers.clock
layer4.matchers.dns
layer4.matchers.http
layer4.matchers.local_ip
layer4.matchers.not
layer4.matchers.openvpn
layer4.matchers.postgres
layer4.matchers.proxy_protocol
layer4.matchers.quic
layer4.matchers.rdp
layer4.matchers.regexp
layer4.matchers.remote_ip
layer4.matchers.remote_ip_list
layer4.matchers.socks4
layer4.matchers.socks5
layer4.matchers.ssh
layer4.matchers.tls
layer4.matchers.vars
layer4.matchers.vars_regexp
layer4.matchers.winbox
layer4.matchers.wireguard
layer4.matchers.xmpp
layer4.proxy.selection_policies.first
layer4.proxy.selection_policies.ip_hash
layer4.proxy.selection_policies.least_conn
layer4.proxy.selection_policies.random
layer4.proxy.selection_policies.random_choose
layer4.proxy.selection_policies.round_robin
layer4.proxy.selection_policies.weighted_round_robin
security
tls.handshake_match.alpn
```
