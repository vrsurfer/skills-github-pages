---
title: ERP vs WMS vs SAP
---

# ERP, WMS e SAP: onde é que cada um entra

Confusão comum em operações e supply chain: tratar "SAP" como sinónimo de ERP, ou achar que ERP e WMS fazem o mesmo. Não fazem. Esta página explica a diferença e onde cada peça encaixa numa cadeia de abastecimento real.

## O que é um ERP

ERP significa Enterprise Resource Planning, planeamento de recursos empresariais. É um sistema único que junta numa só base de dados os processos centrais de uma empresa: finanças, compras, vendas, recursos humanos, produção, inventário a alto nível. A ideia central é acabar com ilhas de informação: o departamento financeiro e o de compras veem os mesmos números, em tempo real, sem exportar Excel de um lado para o outro.

Fornecedores conhecidos: SAP (S/4HANA), Oracle NetSuite, Microsoft Dynamics 365, Odoo (open source, mais usado em PME).

## O que é um WMS

WMS significa Warehouse Management System, sistema de gestão de armazém. Ao contrário do ERP, não tenta gerir a empresa toda, foca-se só na operação física do armazém: onde está cada palete, que rota de picking é mais eficiente, como optimizar o slotting (a localização dos produtos nas prateleiras), que ordem de embalamento e expedição faz sentido.

Um ERP sabe que "existem 500 unidades do produto X em stock". Um WMS sabe "essas 500 unidades estão no corredor 4, prateleira C, e o picker mais próximo é o João". É esse nível de detalhe operacional que separa os dois sistemas.

Fornecedores conhecidos: Manhattan Associates, Blue Yonder (antiga JDA), Körber, e o próprio SAP tem o seu módulo de WMS (ver secção seguinte).

## Onde entra o SAP

Aqui está a confusão mais comum. SAP não é "um ERP", SAP é uma empresa alemã, fundada em 1972, que vende vários produtos, sendo o principal deles um ERP.

Os produtos SAP mais relevantes para supply chain e aduaneiro:

- **SAP S/4HANA**: o ERP actual da SAP, sucessor do antigo SAP ECC. É o "cérebro" que junta finanças, compras, produção e vendas.
- **SAP EWM (Extended Warehouse Management)**: o módulo WMS da SAP, para gestão avançada de armazém. Não tenho a certeza sobre o estado actual do módulo mais antigo, o SAP WM clássico, sei que a SAP tem vindo a empurrar clientes para o EWM nas versões mais recentes, mas o calendário exacto de descontinuação convém confirmar no Learning Hub.
- **SAP GTS (Global Trade Services)**: o módulo de compliance de comércio internacional, gestão de sanções, classificação pautal automatizada, documentação aduaneira. Este é o que mais se cruza com a tua área, e é o que está previsto no teu plano de formação para 2027 se a decisão for GO.

## Tabela resumo

| | Âmbito | Pergunta a que responde | Exemplos |
|---|---|---|---|
| ERP | Empresa inteira | Quanto stock existe, quanto custou, quem comprou | SAP S/4HANA, Oracle NetSuite, Dynamics 365 |
| WMS | Armazém físico | Onde está, como se apanha, como se expede | Manhattan, Blue Yonder, SAP EWM |
| SAP GTS | Compliance aduaneiro | Esta remessa pode sair, que código HS aplicar | Módulo SAP dedicado a trade compliance |

## Como isto se liga na prática

Uma encomenda de exportação passa tipicamente por três camadas de sistema, cada uma com o seu papel:

1. O **ERP** regista a venda, reserva o stock e gera a ordem de expedição
2. O **WMS** organiza o picking, packing e a saída física do armazém
3. Um sistema de **compliance aduaneiro** (como o SAP GTS, ou os sistemas nacionais como o IMPCAU/EXPCAU que já usas) valida se a remessa cumpre a legislação e gera a declaração

Nenhum destes sistemas substitui o outro. Uma empresa pode ter SAP como ERP e Manhattan como WMS ao mesmo tempo, é uma combinação comum na indústria.

## Fontes para aprofundar

SAP Learning Hub (acesso já activo): journey [Configuring the Essential Functions of SAP GTS](https://learning.sap.com/learning-journeys/configuring-the-essential-functions-of-sap-global-trade-services). É a fonte primária para qualquer detalhe de versão ou módulo que precises de confirmar.
