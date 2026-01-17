# Grafana
## GRAFANA + PROMETHEUS INTEGRATION
```bash
sudo apt update
sudo apt install -y apt-transport-https software-properties-common
```
## Add Grafana GPG key:
```bash
sudo mkdir -p /etc/apt/keyrings
wget -q -O - https://apt.grafana.com/gpg.key | sudo tee /etc/apt/keyrings/grafana.asc > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/grafana.asc] https://apt.grafana.com stable main" | \
sudo tee /etc/apt/sources.list.d/grafana.list
```
# Install:
```bash
sudo apt update
sudo apt install -y grafana
```
# Start Grafana service
```bash
sudo systemctl daemon-reexec
sudo systemctl enable grafana-server
sudo systemctl start grafana-server
sudo systemctl status grafana-server
```

# Add Prometheus as Data Source
```bash
⚙️ Settings → Data sources → Add data source
```

