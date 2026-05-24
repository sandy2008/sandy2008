### Hi, I'm Sandy 👋

Based in Tokyo. I work on the unglamorous parts of distributed systems — the parts that page someone at 3 AM.

Most of my open-source time goes into **observability infrastructure** (Prometheus-compatible storage, log shipping, OpenTelemetry SDKs) and **transport security** (mTLS for OTLP across SDKs). I like fixing the bug that's been "flaky for ages," the one nobody wants to bisect.

---

#### 🌍 OSS contributions

**Observability — storage, query, shipping**

- **[cortexproject/cortex](https://github.com/cortexproject/cortex/pulls?q=author%3Asandy2008)** — 3 merged, 8 open. Ingester correctness (counter leaks, send-on-closed-channel panics, TSDB appender lifecycle on error paths), ring/backoff timer reuse to cut per-poll allocations, memberlist cluster-label safety against accidental cross-cluster joins, plus the in-flight `integration_query_fuzz` stabilisation series.
- **[grafana/loki](https://github.com/grafana/loki/pulls?q=author%3Asandy2008)** — 2 merged. Azure Managed Identity for the blob backend; better fluent-bit output plugin startup error messages.
- **[grafana/grafana](https://github.com/grafana/grafana/pulls?q=author%3Asandy2008)** — Alerting (instance-wide UI disable setting, disable Grafana-managed alert creation) and Dashboards (N+1 query in `GetDashboardsByPluginID`).
- **[fluent/fluent-bit](https://github.com/fluent/fluent-bit/pulls?q=author%3Asandy2008)** — 2 merged. `in_tail` file-watching: inotify reconciliation after missed events, append-cleanup on failure.
- **[fluent/fluent-operator](https://github.com/fluent/fluent-operator/pulls?q=author%3Asandy2008)** — 1 merged. CRD validation preventing a fluent-bit crash on null `logfmt` parser values.

**OpenTelemetry — mTLS for OTLP across languages**

- **[open-telemetry/opentelemetry-dotnet](https://github.com/open-telemetry/opentelemetry-dotnet/pulls?q=author%3Asandy2008)** — 5 merged. End-to-end mTLS for OTLP exporters: TLS HTTP client factory, custom-CA-only trust scope, helper renames, integration-test cert generation via MSBuild.
- **[open-telemetry/opentelemetry-dotnet-instrumentation](https://github.com/open-telemetry/opentelemetry-dotnet-instrumentation/pulls?q=author%3Asandy2008)** — 1 merged. mTLS env-var documentation.
- **[open-telemetry/opentelemetry-go](https://github.com/open-telemetry/opentelemetry-go/pulls?q=author%3Asandy2008)** — 1 merged + 1 open. Fail-closed when an HTTP endpoint is paired with TLS client config; async-callback unregister deadlock fix in the SDK metric path.
- **[open-telemetry/opentelemetry-go-contrib](https://github.com/open-telemetry/opentelemetry-go-contrib/pulls?q=author%3Asandy2008)** — 1 merged. `otelconf` client-key/cert symmetry validation for mTLS.
- **[open-telemetry/opentelemetry-python](https://github.com/open-telemetry/opentelemetry-python/pulls?q=author%3Asandy2008)** — 1 merged. Client key/cert file support for all OTLP exporters.
- **[open-telemetry/opentelemetry-specification](https://github.com/open-telemetry/opentelemetry-specification/pulls?q=author%3Asandy2008)** — proposal for mTLS client-key password & certificate-revocation config.

**Auth, proxies, migration tooling**

- **[oauth2-proxy/oauth2-proxy](https://github.com/oauth2-proxy/oauth2-proxy/pulls?q=author%3Asandy2008)** — 1 merged. `cookie-secret-file` support.
- **[openrewrite/rewrite-spring](https://github.com/openrewrite/rewrite-spring/pulls?q=author%3Asandy2008)** — 1 merged. OpenTelemetry migration recipes for Spring Boot.
- **[traefik/traefik](https://github.com/traefik/traefik/pulls?q=author%3Asandy2008)** — open: HRW hashring perf path + benchmark; dynamic log-level via API.

I also keep [**react-otel-observability**](https://github.com/sandy2008/react-otel-observability) as a working example of an OTel-instrumented frontend wired to Loki / Tempo / Cortex.

#### 🧰 Languages I actually write

- **Go** — observability work, ring/gossip internals, gRPC services.
- **TypeScript** — day-to-day product work (React, Node, Tauri, WeChat mini-program).
- **Python** — research, data crunching, older trading / ML projects.
- **C / C++** — fluent-bit patches and a few low-level toolkits.
- **C#** — OTel .NET SDK contributions.
- **Java** — OpenRewrite recipes, JSP-era projects.
- **Rust** — occasional; servers and CLI tools.
- **Past lives:** MATLAB / Verilog (a CNN on FPGA), GDScript, Vue, a goyacc calculator.

#### 🧪 Things I've built for fun

- [**kanbun**](https://github.com/sandy2008/kanbun) — a Classical-Chinese-inspired programming language.
- [**PyCCompiler**](https://github.com/sandy2008/PyCCompiler) — a small C compiler written in Python.
- [**CNN-FPGA**](https://github.com/sandy2008/CNN-FPGA) — a convolutional neural net synthesised onto an FPGA (Verilog).
- [**Neural-Networks-to-solve-PDE**](https://github.com/sandy2008/Neural-Networks-to-solve-PDE) — using NNs as solvers for partial differential equations.

---

![Sandy's GitHub Stats](https://github-readme-stats.vercel.app/api?username=sandy2008&show_icons=true&theme=tokyonight&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=sandy2008&layout=compact&theme=tokyonight&hide_border=true&langs_count=10)
