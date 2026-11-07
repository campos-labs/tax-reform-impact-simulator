# Simulador de Impacto da Reforma Tributária

Estimativas de impacto tributário, resultado operacional e caixa a partir de dados fiscais, com premissas revisáveis e rastreabilidade por execução.

## Desenvolvimento

A arquitetura Fabric-first e os contratos da v1.0 estão no [DESIGN.md](DESIGN.md). O produto combina Python reutilizável, Lakehouse, Pipeline, Notebook e Power BI em Direct Lake.

A estrutura-alvo de código, testes e referências está no DESIGN. Os componentes serão criados conforme forem implementados; a estratégia para as definições nativas está em [fabric/](fabric/README.md).

## Exemplo de referência

[Notebook da POC](examples/poc_fabric_tax_simulation.ipynb) com massa sintética e catálogos da [pesquisa original](https://github.com/campos-labs/project-hub/tree/6c301455fce7a182a044ea5f44bba88e8f6731c2/docs/rfcs/002-tax-reform-impact-simulator/research). XMLs, TXT e CSVs preservam os bytes da origem; o manifesto corrige o checksum de um XML com LF final.

Requer Pandas, PyYAML e DuckDB. Execute a partir da raiz do repositório ou de `examples/`; a persistência no Fabric fica desativada por padrão.

## Origem e governança

[RFC #10](https://github.com/campos-labs/project-hub/issues/10) · [ADR #94](https://github.com/campos-labs/project-hub/issues/94) · [POC #78](https://github.com/campos-labs/project-hub/pull/78) · [Spike #80](https://github.com/campos-labs/project-hub/pull/80).

As pesquisas permanecem no `project-hub`. Aplicam-se a [governança](https://github.com/campos-labs/.github/blob/main/CONTRIBUTING.md) e a [política de segurança](https://github.com/campos-labs/.github/blob/main/SECURITY.md) da organização. Dados reais permanecem fora do Git.

[Licença MIT](LICENSE).
