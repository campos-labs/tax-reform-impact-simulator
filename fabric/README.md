# Microsoft Fabric

As definições nativas serão geradas pela integração Git oficial, conforme o [DESIGN](../DESIGN.md). Criar os itens conforme forem implementados, preservando os arquivos e identificadores gerados pelo Fabric.

## Fluxo Git

Conectar o workspace de desenvolvimento a uma branch de trabalho deste repositório e à pasta `fabric/`. Revisar o sentido da sincronização inicial e os diffs antes de sincronizar. As mudanças seguem por PR para a `main`.

- **Notebook:** importa a wheel da release; conferir os vínculos de Environment e Lakehouse no destino.
- **Environment:** fixa runtime e dependências. A sincronização atualiza a preparação; publicar antes de usar a nova configuração.
- **Lakehouse:** versionar metadados. Arquivos, tabelas e dados do OneLake exigem preparação e recuperação próprias.
- **Data Pipeline:** conferir parâmetros, conexões e referências aos itens de destino.
- **Semantic Model e Report:** conferir os vínculos entre relatório, modelo e SQL Analytics Endpoint. A integração desses tipos está em preview.

A fundação Python cobre o build e a instalação local da wheel. A entrega da plataforma inclui configurar o workspace, o Notebook e o Environment, publicar a wheel no Fabric, validar a importação no Notebook e verificar a sincronização pela integração Git.

Referências: [conexão Git](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started), [tipos suportados](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/intro-to-git-integration), [Environment](https://learn.microsoft.com/en-us/fabric/data-engineering/environment-git-and-deployment-pipeline) e [Lakehouse](https://learn.microsoft.com/en-us/fabric/data-engineering/lakehouse-git-deployment-pipelines).
