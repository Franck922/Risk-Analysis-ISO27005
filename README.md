# 🛡️ Analyse de Risques SSI — Norme ISO/IEC 27005:2022
> **Expertise GRC | Étude de cas : Éditeur de Logiciel SaaS B2B en environnement Cloud**

Ce projet simule une mission de conseil en gestion des risques pour un éditeur SaaS traitant des données sensibles. L'objectif était de structurer une démarche d'analyse rigoureuse pour identifier les scénarios redoutés et proposer un plan de traitement (PTR) aligné sur les enjeux business.

---

## 📋 Contexte & Périmètre
L'organisation étudiée héberge des données critiques pour plusieurs entreprises clientes via une infrastructure Cloud. Une compromission unique peut impacter l'ensemble du portefeuille client.

**Périmètre de l'analyse :**
*   **Chaîne CI/CD** : Pipeline de développement et déploiement continu.
*   **Environnements de Production** : Infrastructure Cloud hébergeant le service.
*   **Données Clients** : Actifs hautement sensibles soumis au RGPD.
*   **Comptes à Privilèges** : Accès administrateur et secrets techniques.

## 🔍 Méthodologie (Cycle itératif ISO 27005)
L'étude a suivi les étapes normatives pour transformer des menaces théoriques en décisions stratégiques :

1.  **Identification des Actifs Critiques** : Définition des actifs primordiaux et supports.
2.  **Modélisation des Menaces & Vulnérabilités** : Analyse des vecteurs d'attaque (compromission dev, secrets exposés, dépendances vulnérables).
3.  **Évaluation de la Criticité** : Estimation de l'Impact (Confidentialité, Intégrité, Disponibilité) et de la Vraisemblance.

### Exemples de Scénarios de Risque identifiés :
| Risque | Menace | Vulnérabilité | Niveau |
| :--- | :--- | :--- | :--- |
| **Injection de code via CI/CD** | Compromission d'un compte dev | Absence de MFA / Droits excessifs | **Très Élevé** |
| **Exfiltration de BDD Cloud** | Accès non autorisé externe | Mauvaise configuration / Secrets exposés | **Élevé** |
| **Exploitation de dépendances** | Bibliothèque tierce vulnérable | Absence de scan de sécurité (SCA) | **Élevé** |

## 🛠️ Plan de Traitement des Risques (PTR)
Mise en place de mesures de réduction ciblées pour ramener le risque à un niveau acceptable :
*   **Réduction (Technique)** : Intégration d'outils d'analyse de code (SAST) dans le pipeline et isolation des environnements.
*   **Hardening** : Déploiement de coffres-forts de mots de passe (Vault) et mise en place de la rotation automatique des clés.
*   **Résilience** : Établissement d'un Plan de Reprise d'Activité (PRA) et architecture redondante.

## ✅ Résultats & Apports
*   **Gouvernance** : Établissement de critères d'acceptabilité clairs pour la direction.
*   **Suivi** : Définition des fréquences de révision des risques et calcul du risque résiduel.

---
[📄 Consulter la présentation de l'analyse (PDF)](./docs/Presentation_Analyse_Risques_SaaS.pdf)
