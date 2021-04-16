---
title: Функции обработчика привязки
description: В следующей таблице содержится список исполняемых процедур среды выполнения RPC, которые работают с дескрипторами привязки и указывают тип разрешенного дескриптора привязки.
ms.assetid: 16effe59-ebe2-48c3-b97a-90656b6d3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e00b3cbb2d5fc5637b9414d6f009cfb2e4ade4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672015"
---
# <a name="binding-handle-functions"></a>Функции обработчика привязки

В следующей таблице содержится список исполняемых процедур среды выполнения RPC, которые работают с дескрипторами привязки и указывают тип разрешенного дескриптора привязки.



| Подпрограмма                                                            | Входной аргумент   | Выходной аргумент |
|--------------------------------------------------------------------|------------------|-----------------|
| [**рпкбиндингкопи**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy)                           | Сервер           | Сервер          |
| [**рпкбиндингфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree)                           | Сервер           | Нет            |
| [**рпкбиндингфромстрингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) | Нет             | Сервер          |
| [**рпкбиндингинкаусклиент**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)         | Клиент           | Нет            |
| [**рпкбиндингинкаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)             | Сервер           | Нет            |
| [**рпкбиндингинкобжект**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqobject)                 | Сервер или клиент | Нет            |
| [**рпкбиндингресет**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset)                         | Сервер           | Нет            |
| [**рпкбиндингсетаусинфо**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)             | Сервер           | Нет            |
| [**рпкбиндингсетобжект**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetobject)                 | Сервер           | Нет            |
| [**рпкбиндингтострингбиндинг**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)     | Сервер или клиент | Нет            |
| [**рпкбиндингвекторфри**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingvectorfree)               | Сервер           | Нет            |
| [**рпкнсбиндинжекспорт**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingexporta)                   | Сервер           | Нет            |
| [**рпкнсбиндингимпортнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)           | Нет             | Сервер          |
| [**рпкнсбиндинглукупнекст**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)           | Нет             | Сервер          |
| [**рпкнсбиндингселект**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingselect)                   | Сервер           | Сервер          |
| [**рпксерверинкбиндингс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverinqbindings)               | Нет             | Сервер          |



 

 

 




