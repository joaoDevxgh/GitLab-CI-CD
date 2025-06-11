
Este repositório tem como objetivo documentar e exemplificar o uso do **GitLab CI/CD**, uma poderosa ferramenta de integração e entrega contínua (CI/CD) para automação de processos de build, teste e deploy de aplicações.

## 🛠️ O que é CI/CD?

- **CI (Integração Contínua)**: prática de integrar alterações de código com frequência, permitindo a detecção precoce de erros.
- **CD (Entrega Contínua/Deploy Contínuo)**: automatização da entrega do código para ambientes de staging ou produção, com testes automatizados garantindo qualidade.

---

## 📄 Estrutura do Repositório

- `.gitlab-ci.yml` — Arquivo principal de configuração da pipeline.
- `scripts/` — Scripts auxiliares usados nos jobs.
- `src/` — Exemplo de aplicação simples (opcional).
- `docs/` — Documentação adicional.

---

## 🚀 Funcionamento do GitLab CI/CD

### 1. `.gitlab-ci.yml`

Arquivo de configuração localizado na raiz do repositório. Define:

- **Stages**: etapas do pipeline (ex: build, test, deploy).
- **Jobs**: tarefas executadas em cada stage.
- **Runners**: máquinas que executam os jobs.
- **Regras e Condições**: quando e como cada job deve rodar.

### Exemplo de YAML:
```yaml
stages:
  - build
  - test
  - deploy

build_job:
  stage: build
  script:
    - echo "Compilando aplicação..."

test_job:
  stage: test
  script:
    - echo "Executando testes automatizados..."

deploy_job:
  stage: deploy
  script:
    - echo "Fazendo deploy para ambiente de staging..."
  only:
    - main# GitLab-CI-CD
