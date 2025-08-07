## Kong Servers

Connections

- This shows how I manage multiple Kong nodes in KONGA, with versioning and activation controls for each gateway—ensuring modular, testable, and scalable API infrastructure.



<img src="../../assets/Kong API Gateway/konga/konga1.png"  width="4000"/> <br>

Services

- This is the service configuration panel for infor, where I define protocol, host, and port—standardizing upstream service registration for secure, consistent routing.

<img src="../../assets/Kong API Gateway/konga/konga2.png"  width="4000"/> <br>

Routes

- This route setup defines how traffic is matched and forwarded using host/path rules and protocol filters—critical for precise API gateway routing and regex-based prioritization.


<img src="../../assets/Kong API Gateway/konga/konga3.png"  width="4000"/> <br>

Plugins

- Here I’ve attached Prometheus for metrics, File-log for persistent logging, and Basic-auth for access control—demonstrating layered observability and security across all consumers.

<img src="../../assets/Kong API Gateway/konga/konga4.png"  width="4000"/> <br>

Basic Auth | Credentials

- This shows how I assign Basic Auth credentials to the infor consumer in Kong, enabling secure, credential-based access to protected routes.

<img src="../../assets/Kong API Gateway/konga/konga5.png"  width="4000"/> <br>

Accessible Routes

- This interface displays the plugins and routes accessible to infor, where I’ve layered Prometheus for metrics, File Log for audit trails, and Basic Auth for authentication—ensuring observability and access control per consumer.

<img src="../../assets/Kong API Gateway/konga/konga6.png"  width="4000"/> <br>

---

## NGINX Load Balancer


NGINX Configuration

- This NGINX config defines SSL-secured reverse proxying to production and test upstreams, with health-check parameters and standardized headers—enabling seamless API routing across multiple domains and environments.


<img src="../../assets/Kong API Gateway/nginx/lb1.png"  width="4000"/> <br>

<img src="../../assets/Kong API Gateway/nginx/lb2.png"  width="4000"/> <br>

<img src="../../assets/Kong API Gateway/nginx/lb3.png"  width="4000"/> <br>

SSL Certificate Files

<img src="../../assets/Kong API Gateway/nginx/lb4.png"  width="4000"/> <br>

---


## Prometheus

- This shows Prometheus successfully scraping metrics from three Kong nodes—each labeled under the kong job and reporting healthy (UP) status—validating multi-node observability and real-time gateway monitoring.

<img src="../../assets/Kong API Gateway/prometheus/prometheus1.png"  width="4000"/> <br>
<img src=" "  width="4000"/> <br>

---

## Grafana

Grafana Dashboard

- This Grafana dashboard visualizes real-time API traffic, success/error rates, and request durations—helping us monitor endpoint health and troubleshoot issues quickly using logs filtered by client IP, method, and environment.

<img src="../../assets/Kong API Gateway/grafana/grafana1.png"  width="4000"/> <br>
<img src=" "  width="4000"/> <br>

Data Sources

- This shows my Grafana setup with Prometheus and Loki configured as data sources—enabling unified metrics and log observability across our infrastructure."

<img src="../../assets/Kong API Gateway/grafana/grafana2.png"  width="4000"/> <br>
<img src=" "  width="4000"/> <br>

Prometheus Config

- This is the Prometheus data source setup, pointing to http://prometheus:9090, which I use for real-time system metrics and alerting.

<img src="../../assets/Kong API Gateway/grafana/grafana3.png"  width="4000"/> <br>
<img src=" "  width="4000"/> <br>

Loki Config

- This is the Loki data source setup at http://loki:3100, which powers centralized log aggregation and filtering for all services.

<img src="../../assets/Kong API Gateway/grafana/grafana4.png"  width="4000"/> <br>
<img src=" "  width="4000"/> <br>
