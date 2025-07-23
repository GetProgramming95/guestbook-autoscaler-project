# Gästebuch-App mit Kubernetes, Docker und Autoscaling

Dieses Projekt wurde im Rahmen eines IBM Cloud Kurses auf Coursera umgesetzt. Es handelt sich um eine einfache Gästebuch-Webanwendung, die in Go geschrieben ist und als Container-App auf Kubernetes bereitgestellt wurde.

## Features

- Multi-Stage Docker Build (Go → Ubuntu)
- Deployment via Kubernetes (Deployment + Port Forwarding)
- Horizontal Pod Autoscaler (HPA)
- Rollierende Updates und Rollbacks
- Ressourcenlimits definiert (CPU Requests/Limits)
- Screenshots und Beweise der Umsetzung inklusive

## Struktur

- `main.go` – Go Backend
- `Dockerfile` – Multi-Stage Build
- `deployment.yml` – Kubernetes Deployment
- `public/` – Frontend Dateien (HTML/CSS/JS)
- `screenshots/` – Nachweise aus dem Lab

## Deployment & Nutzung

1. Docker-Image erstellen und pushen  
2. `kubectl apply -f deployment.yml`  
3. `kubectl port-forward deployment.apps/guestbook 3000:3000`  
4. Anwendung im Browser öffnen: [http://localhost:3000](http://localhost:3000)  
