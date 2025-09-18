# David Vizena - Hello World Portfolio Project

A modern, containerized React application showcasing David Vizena, built with Docker and deployed on Kubernetes.

## 🚀 Features

- **React Frontend**: Modern, responsive UI with Tailwind CSS
- **Docker Containerization**: Multi-stage build for optimized production image
- **Kubernetes Deployment**: Scalable deployment with network policies
- **Load Balancer**: High availability with external access
- **Portfolio Ready**: Professional presentation for potential employers

## 🛠️ Tech Stack

- **Frontend**: React 18, Tailwind CSS
- **Containerization**: Docker, Nginx
- **Orchestration**: Kubernetes
- **Networking**: Network Policies, LoadBalancer Service

## 📦 Quick Start

### Prerequisites

- Node.js 18+
- Docker
- Kubernetes cluster (local or cloud)
- kubectl configured

### Local Development

1. **Install dependencies**:
   ```bash
   npm install
   ```

2. **Start development server**:
   ```bash
   npm start
   ```

3. **Build for production**:
   ```bash
   npm run build
   ```

### Docker Deployment

1. **Build Docker image**:
   ```bash
   docker build -t davidvizena/hello-world:latest .
   ```

2. **Run locally**:
   ```bash
   docker run -p 8080:8080 davidvizena/hello-world:latest
   ```

### Kubernetes Deployment

1. **Start minikube cluster**:
   ```bash
   minikube start
   ```

2. **Deploy to Kubernetes**:
   ```bash
   ./deploy.sh
   ```

3. **Or deploy manually**:
   ```bash
   kubectl apply -f k8s/
   ```

4. **Get service URL**:
   ```bash
   minikube service david-vizena-service -n david-vizena
   ```

## 🌐 Free Hosting Options

### Option 1: Railway
- Connect your GitHub repo to Railway
- Automatic deployments on push
- Free tier available
- Custom domain support

### Option 2: Render
- Connect GitHub repo
- Free tier with custom domains
- Automatic SSL certificates

### Option 3: Vercel
- Perfect for React apps
- Free tier available
- Automatic deployments

## 📁 Project Structure

```
├── src/
│   ├── App.js          # Main React component
│   ├── index.js        # React entry point
│   └── index.css       # Tailwind CSS imports
├── public/
│   └── index.html      # HTML template
├── k8s/
│   ├── namespace.yaml  # Kubernetes namespace
│   ├── deployment.yaml # App deployment
│   ├── service.yaml    # LoadBalancer service
│   └── network-policy.yaml # Network policies
├── Dockerfile          # Multi-stage Docker build
├── nginx.conf          # Nginx configuration
└── deploy.sh           # Deployment script
```

## 🔧 Configuration

### Environment Variables
- `PORT`: Application port (default: 8080)

### Kubernetes Resources
- **CPU**: 50m request, 100m limit
- **Memory**: 64Mi request, 128Mi limit
- **Replicas**: 2 (for high availability)


## 📝 License

MIT License - feel free to use this as a template for your own portfolio projects!

---

**Built with ❤️ by David Vizena**
