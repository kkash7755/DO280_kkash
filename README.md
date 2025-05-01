# DO280 - OpenShift Administration I

Ce repository regroupe les exercices pratiques, manifestes YAML, scripts d'automatisation et notes techniques liés à ma préparation à la certification **Red Hat DO280 - OpenShift Administration I**.

## Objectifs Techniques

- Déployer et gérer des applications conteneurisées sur OpenShift 4.
- Administrer les ressources du cluster via `oc` et `kubectl`.
- Implémenter des configurations réseau, de sécurité et de stockage.
- Gérer les ressources utilisateurs, projets, quotas et policies.
- Automatiser les déploiements via des manifestes et scripts.

- Pré-requis
Environnement de lab basé sur CodeReady Containers (CRC) ou un cluster OpenShift provisionné sur un hyperviseur (libvirt, VMware…)

Outils installés :

oc (CLI OpenShift)

podman ou docker (pour builder des images si nécessaire)

kubectl (optionnel)

ansible (si automation complémentaire)

## Arborescence du dépôt

```bash
.
├── labs/                 # Exercices pratiques organisés par module (ex: deploying_apps, configuring_routes, etc.)
├── manifests/            # Ressources Kubernetes/OpenShift en YAML (Deployment, Route, PVC, etc.)
├── scripts/              # Scripts Bash ou Ansible utilisés pour automatiser certaines tâches
├── notes.md              # Notes techniques et raccourcis de commandes
└── README.md             # Présentation du projet


Commandes Références

# Connexion au cluster
oc login --token=<TOKEN> --server=https://api.ocp.local:6443

# Création de projet
oc new-project demo-project

# Déploiement d’une application depuis un template imagestream
oc new-app nodejs~https://github.com/user/app.git

# Exposition via une Route
oc expose svc/app

# Monitoring des ressources
oc get all -n demo-project


Modules couverts
Cluster Access & Authentication

Project Management & Quota

Application Deployment & Rollback

Networking (Routes, Services, Ingress)

Storage (PVCs, StorageClasses)

ConfigMaps & Secrets

Monitoring et Debugging

Tuning et Scaling (HPA, autoscaling)

Ressources
Red Hat DO280 Syllabus

OpenShift 4 Documentation

OC CLI Cheat Sheet

Auteur
Ken KABEYA KASHALA
Ingénieur Systèmes Linux | Certifié RHCSA & RHCE
Préparation à la certification DO280 - OpenShift Administration I
