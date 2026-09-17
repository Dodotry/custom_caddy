# custom_caddy
自定义插件编译caddy
```powershell
$env:GOOS="windows"
$env:GOARCH="amd64"
xcaddy.exe build v2.11.4 `
--with github.com/greenpau/caddy-security `
--with github.com/caddyserver/replace-response `
--with github.com/sjtug/caddy2-filter `
--with github.com/mholt/caddy-webdav `
--with github.com/mholt/caddy-l4 `
--with github.com/mholt/caddy-ratelimit `
--with github.com/git001/caddyv2-upload `
--with github.com/caddyserver/forwardproxy

```
```powershell
$env:GOOS="linux"
$env:GOARCH="amd64"
xcaddy.exe build v2.11.4 `
--with github.com/greenpau/caddy-security `
--with github.com/caddyserver/replace-response `
--with github.com/sjtug/caddy2-filter `
--with github.com/mholt/caddy-webdav `
--with github.com/mholt/caddy-l4 `
--with github.com/mholt/caddy-ratelimit `
--with github.com/git001/caddyv2-upload `
--with github.com/caddyserver/forwardproxy

```
****

### 插件清单
```text
admin.api.load
admin.api.metrics
admin.api.pki
admin.api.reverse_proxy
caddy.adapters.caddyfile
caddy.config_loaders.http
caddy.filesystems
caddy.listeners.http_redirect
caddy.listeners.proxy_protocol
caddy.listeners.tls
caddy.logging.cores.mock
caddy.logging.encoders.append
caddy.logging.encoders.console
caddy.logging.encoders.filter
caddy.logging.encoders.filter.cookie
caddy.logging.encoders.filter.delete
caddy.logging.encoders.filter.hash
caddy.logging.encoders.filter.ip_mask
caddy.logging.encoders.filter.multi_regexp
caddy.logging.encoders.filter.query
caddy.logging.encoders.filter.regexp
caddy.logging.encoders.filter.rename
caddy.logging.encoders.filter.replace
caddy.logging.encoders.journald
caddy.logging.encoders.json
caddy.logging.writers.discard
caddy.logging.writers.file
caddy.logging.writers.net
caddy.logging.writers.stderr
caddy.logging.writers.stdout
caddy.network_proxy.none
caddy.network_proxy.url
caddy.storage.file_system
events
http
http.authentication.hashes.argon2id
http.authentication.hashes.bcrypt
http.authentication.providers.http_basic
http.encoders.gzip
http.encoders.zstd
http.handlers.acme_server
http.handlers.authentication
http.handlers.copy_response
http.handlers.copy_response_headers
http.handlers.encode
http.handlers.error
http.handlers.file_server
http.handlers.headers
http.handlers.intercept
http.handlers.invoke
http.handlers.log_append
http.handlers.map
http.handlers.metrics
http.handlers.push
http.handlers.request_body
http.handlers.reverse_proxy
http.handlers.rewrite
http.handlers.static_response
http.handlers.subroute
http.handlers.templates
http.handlers.tracing
http.handlers.vars
http.ip_sources.static
http.matchers.client_ip
http.matchers.expression
http.matchers.file
http.matchers.header
http.matchers.header_regexp
http.matchers.host
http.matchers.method
http.matchers.not
http.matchers.path
http.matchers.path_regexp
http.matchers.protocol
http.matchers.query
http.matchers.remote_ip
http.matchers.tls
http.matchers.vars
http.matchers.vars_regexp
http.precompressed.br
http.precompressed.gzip
http.precompressed.zstd
http.reverse_proxy.selection_policies.client_ip_hash
http.reverse_proxy.selection_policies.cookie
http.reverse_proxy.selection_policies.first
http.reverse_proxy.selection_policies.header
http.reverse_proxy.selection_policies.ip_hash
http.reverse_proxy.selection_policies.least_conn
http.reverse_proxy.selection_policies.query
http.reverse_proxy.selection_policies.random
http.reverse_proxy.selection_policies.random_choose
http.reverse_proxy.selection_policies.round_robin
http.reverse_proxy.selection_policies.uri_hash
http.reverse_proxy.selection_policies.weighted_round_robin
http.reverse_proxy.transport.fastcgi
http.reverse_proxy.transport.http
http.reverse_proxy.upstreams.a
http.reverse_proxy.upstreams.multi
http.reverse_proxy.upstreams.srv
pki
tls
tls.ca_pool.source.combined
tls.ca_pool.source.file
tls.ca_pool.source.http
tls.ca_pool.source.inline
tls.ca_pool.source.pki_intermediate
tls.ca_pool.source.pki_root
tls.ca_pool.source.storage
tls.ca_pool.source.system
tls.certificates.automate
tls.certificates.load_files
tls.certificates.load_folders
tls.certificates.load_pem
tls.certificates.load_storage
tls.client_auth.verifier.leaf
tls.ech.publishers.dns
tls.get_certificate.http
tls.get_certificate.tailscale
tls.handshake_match.local_ip
tls.handshake_match.remote_ip
tls.handshake_match.sni
tls.handshake_match.sni_regexp
tls.issuance.acme
tls.issuance.internal
tls.issuance.zerossl
tls.leaf_cert_loader.file
tls.leaf_cert_loader.folder
tls.leaf_cert_loader.pem
tls.leaf_cert_loader.storage
tls.permission.http
tls.stek.distributed
tls.stek.standard

  Standard modules: 132

caddy.listeners.layer4
http.authentication.providers.authorizer
http.handlers.authenticator
http.handlers.filter
http.handlers.forward_proxy
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
