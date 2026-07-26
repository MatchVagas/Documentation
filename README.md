# MatchVagas — Documentação

Repositório oficial da documentação do Sistema MatchVagas, plataforma de vagas de trabalho e estágio.

## Baseline documental

| Artefato | Versão candidata | Situação |
|---|---:|---|
| Especificação de Requisitos (ERS) | v5.1 | Canônico |
| Backlog do Produto | v4.0 | Deve refletir integralmente o ERS |
| Arquitetura de Software | v3.1 | Deve separar implementação atual de roadmap |
| UML, DER e dados de exemplo | v5.1 | Devem declarar a versão do ERS de referência |
| Matriz de rastreabilidade | v1.0 | Obrigatória antes da aprovação |

A branch `dev` é a baseline de trabalho atual. Alterações normativas devem ser propostas em branch própria, revisadas por pull request e aprovadas como um conjunto coerente.

## Navegação

- [Especificação de Requisitos](Documento%20de%20Requisitos/Documento%20de%20Requisitos%20MatchVagas.adoc)
- [Arquitetura de Software](Documento%20de%20Arquitetura/Documento%20de%20Arquitetura%20de%20Software%20-%20MatchVagas.adoc)
- [Backlog revisado](Planejamento/Backlog%20Revisao.adoc)
- [Matriz de rastreabilidade](Planejamento/Matriz%20de%20Rastreabilidade.adoc)
- [Registro da revisão v5.1](REVISAO_V5_1.adoc)
- [Diagramas](Diagramas/)

O arquivo `Documento de Requisitos/Outra Visão.adoc` é legado e não deve ser usado como especificação normativa. Ideias ainda válidas devem migrar para o backlog antes de sua futura remoção ou arquivamento.

## Regras de manutenção

1. Cada requisito deve possuir ator, precondição, entradas, resultado, pós-condição, exceções e critério verificável.
2. Backlog, casos de uso, endpoints, entidades e testes devem apontar para o mesmo identificador de requisito.
3. Funcionalidades planejadas devem ser marcadas como `FUTURO`; não podem aparecer como implementadas na arquitetura.
4. Exclusões de dados exigem regra explícita de retenção, auditoria e integridade referencial.
5. Nenhum documento é aprovado isoladamente quando sua mudança afeta outros artefatos.

## Renderização local

Com Asciidoctor instalado:

```bash
mkdir -p build
asciidoctor -D build "Documento de Requisitos/Documento de Requisitos MatchVagas.adoc"
asciidoctor -D build "Documento de Arquitetura/Documento de Arquitetura de Software - MatchVagas.adoc"
asciidoctor -D build "Planejamento/Backlog Revisao.adoc"
asciidoctor -D build "Planejamento/Matriz de Rastreabilidade.adoc"
```

## Portões para aprovação da v5.1

- [ ] Requisitos P0 revisados e testáveis.
- [ ] Matriz RF–US–UC–endpoint–entidade–teste completa.
- [ ] Backlog e arquitetura alinhados ao ERS v5.1.
- [ ] UML, DER, DDL e seed SQL reconciliados.
- [ ] Filtro etário validado juridicamente ou removido.
- [ ] Tratamento de dados e direitos do titular validados.
- [ ] Diagramas distinguem componentes atuais de componentes futuros.
