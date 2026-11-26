# Simulador de Impacto da Reforma Tributária

Estimativas de impacto tributário, resultado operacional e caixa a partir de dados fiscais, com premissas revisáveis e rastreabilidade por execução.

## Desenvolvimento

O pacote `tax_reform_impact_simulator` é importável sem dependências de execução. O desenvolvimento e a validação local usam Python 3.13.16, fixado em `.python-version`. A wheel aceita a série 3.13, usada pelo Spark Runtime 2.0 do Microsoft Fabric.

Na raiz do repositório, use o `uv` para sincronizar o ambiente, verificar a importação e gerar as distribuições.

```sh
uv sync --locked
uv run --locked python -c "import tax_reform_impact_simulator"
uv build
```

O build gera em `dist/` a distribuição fonte e a wheel `tax_reform_impact_simulator-0.1.0-py3-none-any.whl`.

O [DESIGN.md](DESIGN.md) descreve os contratos da v1.0 e as integrações planejadas com Lakehouse, Pipeline e Notebook no Microsoft Fabric e com Power BI em Direct Lake. A estratégia para as definições nativas está no [guia do Fabric](fabric/README.md).

## Exemplo de referência

[Notebook da POC](examples/poc_fabric_tax_simulation.ipynb) com massa sintética e catálogos da [pesquisa original](https://github.com/campos-labs/project-hub/tree/6c301455fce7a182a044ea5f44bba88e8f6731c2/docs/rfcs/002-tax-reform-impact-simulator/research). XMLs, TXT e CSVs preservam os bytes da origem; o manifesto corrige o checksum de um XML com LF final.

Use um ambiente do notebook com Pandas, PyYAML e DuckDB. Execute a partir da raiz do repositório ou de `examples/`. A persistência no Fabric fica desativada por padrão.

## Origem e governança

[RFC #10](https://github.com/campos-labs/project-hub/issues/10) · [ADR #94](https://github.com/campos-labs/project-hub/issues/94) · [POC #78](https://github.com/campos-labs/project-hub/pull/78) · [Spike #80](https://github.com/campos-labs/project-hub/pull/80).

As pesquisas permanecem no `project-hub`. Aplicam-se a [governança](https://github.com/campos-labs/.github/blob/main/CONTRIBUTING.md) e a [política de segurança](https://github.com/campos-labs/.github/blob/main/SECURITY.md) da organização. Dados reais permanecem fora do Git.

[Licença MIT](LICENSE).
