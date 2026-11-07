# Simulador de Impacto da Reforma Tributária

Estimativas de impacto tributário, resultado operacional e caixa a partir de dados fiscais, com premissas revisáveis e rastreabilidade por execução.

## Desenvolvimento

A arquitetura Fabric-first e os contratos da v1.0 estão no [DESIGN.md](DESIGN.md). O produto combina Python reutilizável, Lakehouse, Pipeline, Notebook e Power BI em Direct Lake.

A estrutura-alvo de código, testes e referências está no DESIGN. Os componentes serão criados conforme forem implementados; a estratégia para as definições nativas está em [fabric/](fabric/README.md).

## Origem e governança

[RFC #10](https://github.com/campos-labs/project-hub/issues/10) · [ADR #94](https://github.com/campos-labs/project-hub/issues/94) · [POC #78](https://github.com/campos-labs/project-hub/pull/78) · [Spike #80](https://github.com/campos-labs/project-hub/pull/80).

As pesquisas permanecem no `project-hub`. Aplicam-se a [governança](https://github.com/campos-labs/.github/blob/main/CONTRIBUTING.md) e a [política de segurança](https://github.com/campos-labs/.github/blob/main/SECURITY.md) da organização. Dados reais permanecem fora do Git.

[Licença MIT](LICENSE).

