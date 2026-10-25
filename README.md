# Formation loom_v2

**Construire un agent IA qui travaille pour de vrai**, en 15 modules.

👉 **Lire la formation : https://denislamard.github.io/docs_loom_v2/**

Vous suivez un seul agent, `assistant`, l'assistant de la Plomberie Dupont, et vous lui ajoutez une capacité par module. Il commence par répondre, puis il calcule, se souvient, rédige, demande la permission, survit à une panne, sert plusieurs entreprises et se fait évaluer. Chaque module part de l'état laissé par le précédent.

La formation s'appuie sur [loom_v2](https://github.com/denislamard/loom_v2), un orchestrateur d'agents IA en Python, distribué sous le nom `loom-ia`.

## Programme

### Niveau 1 : découverte
*Un agent, des outils, des modèles*

1. **Les bases de l'agent** : installer loom-ia, écrire et lancer un premier agent, garder une trace de ses runs
2. **Outils Python** : `@tool`, arguments refusés, délais, appels parallèles, boucle bornée
3. **Modèles et configuration** : plusieurs fournisseurs, cache de prompt, secrets, profils

### Niveau 2 : maîtrise
*Un agent qui se comporte comme prévu*

4. **Conversations, mémoire et state** : sessions, compaction, journal, RGPD
5. **Outils MCP et mémoire long terme** : serveurs MCP, mémoire RAG avec loom-notes
6. **Rôles, sous-agents et vision** : déléguer la rédaction, décrire une photo, sous-agents
7. **Fiabilité des sorties** : sortie structurée, contrats, juges, politiques

### Niveau 3 : production
*Un agent qui tient dans la vraie vie*

8. **Actions sensibles et exécution durable** : approbation humaine, idempotence, reprise après plantage
9. **Résilience et coûts** : retry, modèle de secours, disjoncteur, plafonds de dépense
10. **Ouvrir l'agent : Python, REST, MCP** : librairie, API REST, serveur MCP, streaming
11. **Automatiser : webhooks, workers, bus** : déclenchement par un CRM, files de tâches
12. **Plusieurs clients et données sensibles** : espaces isolés, quotas, chiffrement, rétention

### Niveau 4 : expert
*Un agent qu'on comprend, qu'on teste, qu'on étend*

13. **Observabilité et rejeu** : traces, OpenTelemetry, masquage, rejeu de runs
14. **Qualité : évals et non-régression** : suites d'évals, doublures, corpus tiré du journal
15. **Sources d'outils et sandbox forge** : outils fournis par un paquet, microVM Firecracker

Pages annexes : installation et premier run, référence CLI et configuration, pièges et dépannage, glossaire, matrice des 100 fonctions couvertes.

## Ce qu'il faut

- Un terminal sous **Linux**
- [**uv**](https://docs.astral.sh/uv/) (le module 1 l'installe si besoin)
- Rien d'autre pour commencer : pas de clé d'API, Python est installé par uv, et les exercices tournent par défaut sur un modèle simulé, ce qui rend les sorties reproductibles

Quelques exercices demandent une ressource en plus, et chaque module le signale : Postgres, Redis ou RabbitMQ (un conteneur Docker suffit), le serveur MCP loom-notes, un collecteur OpenTelemetry, ou KVM pour la sandbox du module 15.

La formation est écrite pour `loom-ia` 2.0.11 et suivantes, avec Python 3.14.

## Lire en local

Les pages sont du HTML statique, sans étape de build :

```bash
git clone https://github.com/denislamard/docs_loom_v2.git
cd docs_loom_v2
python3 -m http.server 8000
# puis ouvrir http://localhost:8000
```

## Licence

Contenu sous licence [Apache-2.0](LICENSE), comme loom-ia.

---

Formation loom_v2 · App-Novative