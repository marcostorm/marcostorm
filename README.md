# Marcos Henrique Melo de Araújo
10+ anos construindo e sustentando sistemas backend em produção nos setores governo, corporativo e produto próprio. Mestre em Ciência da Computação (UFAC) com pesquisa em dívida técnica e qualidade de código publicada em periódico internacional.<br><br>Rio Branco - AC, Brasil (GMT-3) · Disponível para remoto / Internacional


## 🌐 Socials:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/marcostorm) [![email](https://img.shields.io/badge/Email-D14836?logo=gmail&logoColor=white)](mailto:mhstorms@gmail.com)

## 📄 Currículo
[**Currículo completo (PDF)**](./Marcos_Araujo_Java_Senior_Backend.pdf)

## 🚧 No que estou trabalhando agora

### Storm Lab: lab de IA engineering interno
Infraestrutura própria de RAG, servidores MCP e (em breve) pipelines e agentes pra amplificar produtividade nos meus produtos. Não é oferta comercial; é ferramental pessoal de senior dev. Cada peça só avança quando a anterior provou valor em uso real.

Peças construídas:
- **storm-lab-rag**: RAG local sobre meus códigos, docs e memórias curadas. Postgres + pgvector + `intfloat/multilingual-e5-small` em CPU, chunking por seção em markdown e size-based em código, ingestão incremental por hash. ~765 chunks em 9 projetos, watcher incremental via `storm-rag watch`. Exposto ao Claude Code via MCP (`search_my_code`, `list_projects`, `get_file_context`).
- **storm-vps**: dashboard Streamlit (humano) + servidor MCP (agente) que leem o VPS Hostinger via SSH on-demand com Paramiko. Mesmo `collector.py` nas duas interfaces. 8 tools no MCP: 4 de leitura (health, containers, logs, tags de imagem) e 4 destrutivas com `confirm=False` retornando dry-run por padrão (restart, prune, deploy, rollback).
- **storm-projects**: servidor MCP com estado git dos repos locais em `~/workspace/` e release amarrado ao fluxo real (tag `vYYYYMMDD-HHMM`, sem semver). Zero SSH, tudo via `git -C`. `release_commerce` desacopla git tag e deploy no VPS, retornando o próximo passo em vez de disparar sozinho.
- **storm-lab-docs**: servidor MCP que lê docs institucionais em `.docx` (via python-docx), `.md`, `.html` e `.txt`. Validação de path via `relative_to(DOCS_ROOT)` bloqueia traversal. Fecha o gap de `.docx` no RAG.

Próximas peças previstas: mais MCPs conforme fricção real aparecer, depois pipelines e workers (digest semanal, watchdog do VPS, orquestrador de backups) rodando num `storm-agents-runner` no VPS, e harness tuned com skills por projeto.

### Produtos sob o Storm Lab
- 🚀 **[Storm Commerce](https://github.com/marcostorm/storm-commerce)**: SaaS multi-tenant de e-commerce em produção, com deploy automatizado, backups em Cloudflare R2 e integração Mercado Pago. Laboratório de arquitetura full-stack e DevOps.
- ⚖️ **GED - Editor Jurídico (visual law)**: editor jurídico com recursos de Visual Law em Spring Boot 3.5 + Angular 21 com Postgres.
- 🌳 **Calor & Verde Rio Branco**: pipeline geoespacial que cruza LST (Landsat), NDVI (Sentinel-2) e perda de vegetação por setor censitário IBGE pra gerar ranking de prioridade de plantio.

### Estudos
- 🎓 **AWS Cloud Practitioner Essentials** pra aprofundar os conhecimentos sobre cloud pública.

# 💻 Tech Stack:
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white) ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white) ![Hibernate](https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=Hibernate&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![Angular](https://img.shields.io/badge/angular-%23DD0031.svg?style=for-the-badge&logo=angular&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white) ![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white) ![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white) ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white) ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white) ![Nginx](https://img.shields.io/badge/nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black) ![GitLab CI](https://img.shields.io/badge/gitlab%20CI-%23FC6D26.svg?style=for-the-badge&logo=gitlab&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white) ![SonarQube](https://img.shields.io/badge/SonarQube-4E9BCD?style=for-the-badge&logo=sonarqube&logoColor=white) ![Swagger](https://img.shields.io/badge/Swagger-85EA2D.svg?style=for-the-badge&logo=swagger&logoColor=black) ![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)

Também em uso no Storm Lab: Streamlit, Paramiko, sentence-transformers, pgvector, MCP (Model Context Protocol), Claude Code.

## 📚 Pesquisa Acadêmica
- *[Technical Debt of Software Projects Based on Merge Code Comments](https://journals-sol.sbc.org.br/index.php/jserd/article/view/4801/3278).* **JSERD**, 2025.
- *[Analysis of the Technical Debt of Software Projects Based on Merge Code Comments](https://dl.acm.org/doi/abs/10.1145/3622748.3622751).* **SBC**, 2023.
- *Zenoss × Zabbix: Um Estudo de Caso sobre Sistemas de Gerenciamento de Redes.* **SBPC**, 2014.


# 📊 GitHub Stats:
![](https://github-readme-stats.shion.dev/api/top-langs/?username=marcostorm&theme=dark&hide_border=false&include_all_commits=false&count_private=false&layout=compact)

---
[![](https://komarev.com/ghpvc/?username=marcostorm&icon=0&color=0)](https://visitcount.itsvg.in)

<!-- Proudly created with GPRM ( https://gprm.itsvg.in ) -->
