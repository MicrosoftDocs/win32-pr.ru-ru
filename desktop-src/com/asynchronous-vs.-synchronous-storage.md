---
title: Асинхронное и синхронное хранилище
description: Асинхронное и синхронное хранилище
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533545"
---
# <a name="asynchronous-and-synchronous-storage"></a>Асинхронное и синхронное хранилище

Асинхронные моникеры также могут возвращать [асинхронный объект хранилища](/windows/desktop/Stg/asynchronous-storage) в уведомлении [**метода интерфейса IBindStatusCallback:: ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Этот объект хранилища может разрешить доступ к некоторым из постоянных данных объекта, пока привязка еще выполняется. Клиент может выбрать один из двух режимов хранения: Блокировка и неблокировка.

В режиме блокировки, который совместим с текущими реализациями объектов хранилища, если данные недоступны, вызов блокируется до поступления данных. В неблокирующем режиме, вместо того чтобы блокировать вызов, объект хранилища возвращает новую ошибку E Pending, \_ когда данные недоступны. Клиент, осведомленный о асинхронной привязке и хранилище, задерживает эту ошибку и ожидает дальнейших уведомлений ([**ондатааваилабле**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))), чтобы повторить операцию. Клиент может выбрать между синхронным (блокирующее) и асинхронным (неблочным) хранилищем, выбрав, следует ли установить \_ флаг биндф асинкстораже в значении *грфбиндф* , возвращаемом в [**метода интерфейса IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Асинхронные моникеры](asynchronous-monikers.md)
</dt> </dl>

 

 