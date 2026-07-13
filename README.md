# 🧠 Graph Machine Learning Analytics Platform

### *"Transforming Connected Data into Actionable Intelligence"*

[![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.104+-green.svg)](https://fastapi.tiangolo.com)
[![React](https://img.shields.io/badge/React-18.2+-blue.svg)](https://reactjs.org)
[![Neo4j](https://img.shields.io/badge/Neo4j-5.14+-yellow.svg)](https://neo4j.com)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-red.svg)](https://pytorch.org)
[![License](https://img.shields.io/badge/License-MIT-red.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

---

## 📋 Table of Contents
- [Overview](#overview)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [ML Models](#ml-models)
- [API Documentation](#api-documentation)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)

---

## 🎯 Overview

The **Graph Machine Learning Analytics Platform** is a comprehensive, full-stack solution designed to bridge the gap between graph databases and machine learning. This platform empowers data scientists, analysts, and developers to explore complex relationships, classify nodes, detect anomalies, and extract meaningful insights from graph-structured data using state-of-the-art Graph Neural Networks (GNNs).

### 🎓 Purpose
This project is specifically designed for **learning and practice purposes**, making it accessible to students, researchers, and professionals looking to understand and implement graph machine learning without the complexity of enterprise-level infrastructure.

### 🚀 Key Capabilities
- 🔍 **Relationship Discovery**: Identify hidden patterns and connections in graph data
- 🏷️ **Node Classification**: Categorize nodes based on graph structure and features
- ⚠️ **Anomaly Detection**: Detect outliers and unusual patterns in graph data
- 📊 **Graph Visualization**: Interactive graph rendering with modern UI
- 🤖 **GNN Models**: Implementations of GCN, GAT, and GraphSAGE

---

## ✨ Key Features

### 📊 Graph Data Management
- ✅ Neo4j integration for graph database operations
- ✅ Complete CRUD operations for nodes and edges
- ✅ CSV/JSON file upload with automatic graph conversion
- ✅ Graph schema validation and data migration tools
- ✅ Batch import/export capabilities

### 🧮 Graph Neural Networks
- ✅ **GCN (Graph Convolutional Networks)**: Node classification and feature extraction
- ✅ **GAT (Graph Attention Networks)**: Attention-based relationship learning
- ✅ **GraphSAGE**: Inductive representation learning on large graphs
- ✅ Model training pipeline with progress monitoring
- ✅ Model persistence and version management

### 🔍 Analytics Engine
- ✅ Community detection using Louvain algorithm
- ✅ Centrality measures (PageRank, Degree, Betweenness)
- ✅ Similarity metrics (Jaccard, Adamic-Adar)
- ✅ Path analysis and pattern finding
- ✅ Statistical analysis and reporting

### 🎨 User Interface
- ✅ Interactive graph visualization with Cytoscape.js
- ✅ Real-time dashboard with metrics and statistics
- ✅ Responsive design (Mobile-first approach)
- ✅ Dark/Light theme support
- ✅ Drag-and-drop file upload
- ✅ Charts and data visualization with Recharts

---

## 🛠️ Tech Stack

### Backend
| Technology | Version | Purpose |
|------------|---------|---------|
| Python | 3.9+ | Core programming language |
| FastAPI | 0.104+ | REST API framework |
| Neo4j | 5.14+ | Graph database |
| PostgreSQL | 15+ | Relational database |
| PyTorch | 2.0+ | Deep learning framework |
| PyTorch Geometric | 2.5+ | GNN library |
| DGL | 1.1+ | Deep Graph Library |
| SQLAlchemy | 2.0+ | ORM for PostgreSQL |
| Alembic | 1.12+ | Database migrations |
| Celery | 5.3+ | Task queue |
| Redis | 7.0+ | Caching and message broker |

### Frontend
| Technology | Version | Purpose |
|------------|---------|---------|
| React | 18.2+ | UI framework |
| React Router | 6.18+ | Routing |
| Tailwind CSS | 3.3+ | Styling |
| Material-UI | 5.14+ | UI components |
| Cytoscape.js | 3.25+ | Graph visualization |
| D3.js | 7.8+ | Data visualization |
| Recharts | 2.8+ | Charts |
| Axios | 1.5+ | HTTP client |
| React Query | 3.39+ | Data fetching |

### DevOps
| Technology | Purpose |
|------------|---------|
| Docker | Containerization |
| Docker Compose | Multi-container orchestration |
| Git | Version control |
| GitHub Actions | CI/CD |

---

## 🏗️ Architecture

---

## 🚀 Quick Start

### Prerequisites
- Python 3.9 or higher
- Node.js 16 or higher
- Docker and Docker Compose (optional)
- Git

### Method 1: Using Docker (Recommended)

```bash
# Clone the repository
git clone https://github.com/vishakha2121/graph-ml-analytics-platform.git
cd graph-ml-analytics-platform

# Start all services
docker-compose up -d

# Wait for services to start (approx 30 seconds)

# Access the application
# Frontend: http://localhost:3000
# Backend API: http://localhost:8000
# API Documentation: http://localhost:8000/docs
# Neo4j Browser: http://localhost:7474

# Navigate to backend
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your database credentials

# Initialize database
python scripts/init_db.py

# Seed sample data
python scripts/seed_data.py

# Run backend server
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000

# Navigate to frontend (in a new terminal)
cd frontend

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env

# Run development server
npm start