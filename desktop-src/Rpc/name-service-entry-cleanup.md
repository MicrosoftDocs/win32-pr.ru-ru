---
title: Очистка записи службы имен
description: Запись службы имен должна содержать сведения, которые не меняются часто.
ms.assetid: b581bc10-e537-4714-b89a-d998fec23360
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0ed6a21074a49a472d7505dcfea37cf182026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068307"
---
# <a name="name-service-entry-cleanup"></a>Очистка записи службы имен

Запись службы имен должна содержать сведения, которые не меняются часто. По этой причине не включайте динамические конечные точки в экспортированные дескрипторы привязки, так как они изменятся при каждом вызове сервера и будут перегружать запись службы имен. Чтобы удалить эти дескрипторы привязки, используйте [**рпкбиндингресет**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).

Например, разумная последовательность операций сервера будет выглядеть так:

Для более чем одного транспорта:

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

Размещение привязок в модуле сопоставления конечных точек:

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

Чтобы удалить конечные точки из привязок:

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

Чтобы добавить привязки в службу имен, сделайте следующее:

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




