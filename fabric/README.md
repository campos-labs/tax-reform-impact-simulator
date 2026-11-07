# Microsoft Fabric

As definições nativas serão geradas pela integração Git oficial, conforme o [DESIGN](../DESIGN.md). Criar os itens conforme forem implementados, preservando os arquivos e identificadores gerados pelo Fabric.

## Fluxo Git

Conectar o workspace de desenvolvimento a uma branch de trabalho deste repositório e à pasta `fabric/`. Revisar o sentido da sincronização inicial e os diffs antes de sincronizar. As mudanças seguem por PR para a `main`.

- **Notebook:** importa a wheel da release; conferir os vínculos de Environment e Lakehouse no destino.
- **Environment:** fixa runtime e dependências. A sincronização atualiza a preparação; publicar antes de usar a nova configuração.
- **Lakehouse:** versionar metadados. Arquivos, tabelas e dados do OneLake exigem preparação e recuperação próprias.
- **Data Pipeline:** conferir parâmetros, conexões e referências aos itens de destino.
- **Semantic Model e Report:** conferir os vínculos entre relatório, modelo e SQL Analytics Endpoint. A integração desses tipos está em preview.

A fundação técnica validará build e instalação da wheel, importação no Notebook, publicação do Environment e sincronização de ida e volta. Os itens reais e esses testes serão entregues nas Issues de execução.

Referências: [conexão Git](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started), [tipos suportados](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration), [Environment](https://learn.microsoft.com/en-us/fabric/data-engineering/environment-git-and-deployment-pipeline) e [Lakehouse](https://learn.microsoft.com/en-us/fabric/data-engineering/lakehouse-git-deployment-pipelines).
