 **To Monitor most of the Backend services, we use the ecosystem of:**
 - Telegraf
 - Prometheus
 - Grafana

**What is Prometheus?**

- It is an open-source system monitoring and alerting toolkit.
- It has three major parts:
	- **Prometheus Server**: Scrapes and stores time series data.
	- **Retrieval**: Responsible for scraping the data
	- **TSDB**: Responsible for storing and retrieval of data.
	- **HTTP Server:** Powers the Prometheus web UI and serves the query request.
	- **Alert Manager**: For all kinds of alerts and notifications.
	- **Prometheus Web UI:** Operations like querying, setting the alert, and managing (Gateway to server)

![[telegraf.jpeg]]