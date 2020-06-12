# Deposit-CienciaVitae-DSpace
Ficheiros necessários para ativar o depósito a partir do CienciaVitae para uma instalação do DSpace. É baseado nas configurações do  RCAAP/SARIs

# Transformador CienciaVitae - DSpace (SWORDv2)
O transformador utilizado, é baseado no existente para o DSpace (mods-submission.xsl). Tem algumas adições no contexto RCAAP e adição de novos elementos. É baseado nos dados enviados pelo CienciaVitae e nos metadados mapeados no DSpace (DSpace + RCAAP).

# Versões DSpace!
Este transformador foi criado/modificado para a **versão 5.X** do DSpace, mas é possível que em versões anteriores ou posteriores do DSpace possa também ser utilizado. Desde que tenham o swordv2 instalado/ativo, deverá funcionar como na versão 5.X.

# Como aplicar o códgio

Há duas possibilidades de adicionar o código fornecido ao Repositório:

## 1 - Adicionar ao Código Fonte e Compilar  

* Copiar o ficheiro para a pasta do código do DSpace [SRC-DSPACE]
* Alterar o dspace.cfg
```
#Configure XSLT-driven submission crosswalk for MODS               
crosswalk.submission.MODS.stylesheet= crosswalks/mods-rcaap_cienciavitae-submission.xsl
```
* compilar/deploy
* restart do serviço


## Alterando na pasta de deploy do DSpace
* 2 - opiar o ficheiro para a pasta onde está a instalação do DSpace

* Alterar o dspace.cfg
```
#Configure XSLT-driven submission crosswalk for MODS               
crosswalk.submission.MODS.stylesheet= crosswalks/mods-rcaap_cienciavitae-submission.xsl
``` 

* restart do serviço


Nota: O nome mods-rcaap_cienciavitae-submission.xsl pode ser alterado para um outro nome desde que os nomes sejam iaguis em todos os locais onde exista, nomeadamente no dspace.cfg.


# Depósito a partir do CV

A informação de como proceder para ativar o depósito pode ser encontrada aqui:

> [Documentação](https://docs.google.com/document/d/1yYfE8HBU7z1hOTwnaagXWlWVWksgcYksz3HSh2wrNRM) 

## Ativação do Depósito
* Criar utilizador genérico
* Criar coleção genérica
* Comunicar com o CienciViate para ativar o serviço (Ver documentação)

# Input Forms
Alguns mapeamentos do transformador podem necessitar de algumas alterações no input-forms.xml, nomeadamente os IDs e/ou o mapeamento do esquema degois (usado no contexto RCAAP).
Ver Documentação sobre os mapeamentos.

# Alteração do transformador
Caso algum mapeamento dê erro, ver se existem no esquema de metadados do Repositório. Neste caso, ou adicionar ao repositótio ou remover do ficheiro de transformação. 
Por exemplo, no RCAAP existe o esquema degois. 

Para mais informações/ajuda contacar:
[RCAAP](mailto:helpdesk@rcaap.pt)