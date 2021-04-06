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
# <a name="name-service-entry-cleanup"></a><span data-ttu-id="af0db-103">Очистка записи службы имен</span><span class="sxs-lookup"><span data-stu-id="af0db-103">Name Service Entry Cleanup</span></span>

<span data-ttu-id="af0db-104">Запись службы имен должна содержать сведения, которые не меняются часто.</span><span class="sxs-lookup"><span data-stu-id="af0db-104">A name service entry should contain information that does not change frequently.</span></span> <span data-ttu-id="af0db-105">По этой причине не включайте динамические конечные точки в экспортированные дескрипторы привязки, так как они изменятся при каждом вызове сервера и будут перегружать запись службы имен.</span><span class="sxs-lookup"><span data-stu-id="af0db-105">For this reason, do not include dynamic endpoints in your exported binding handles because they will change at each invocation of the server and will clutter up your name service entry.</span></span> <span data-ttu-id="af0db-106">Чтобы удалить эти дескрипторы привязки, используйте [**рпкбиндингресет**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span><span class="sxs-lookup"><span data-stu-id="af0db-106">To remove these binding handles, use [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset).</span></span>

<span data-ttu-id="af0db-107">Например, разумная последовательность операций сервера будет выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="af0db-107">For example, a reasonable sequence of server operations would be:</span></span>

<span data-ttu-id="af0db-108">Для более чем одного транспорта:</span><span class="sxs-lookup"><span data-stu-id="af0db-108">For more than one transport:</span></span>

``` syntax
RpcServerUseProtseq();
RpcServerUseProtseq();
```

<span data-ttu-id="af0db-109">Размещение привязок в модуле сопоставления конечных точек:</span><span class="sxs-lookup"><span data-stu-id="af0db-109">To place bindings in the endpoint mapper:</span></span>

``` syntax
RpcServerInqBindings(&Vector);
RpcEpRegister(Interface, Vector);
```

<span data-ttu-id="af0db-110">Чтобы удалить конечные точки из привязок:</span><span class="sxs-lookup"><span data-stu-id="af0db-110">To remove endpoints from bindings:</span></span>

``` syntax
for (i=0; i < Vector- > Count; + + i)
{
    RpcBindingReset(Vector->BindingH[i];
}
```

<span data-ttu-id="af0db-111">Чтобы добавить привязки в службу имен, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="af0db-111">To add bindings to the name service:</span></span>

``` syntax
RpcNsBindingExport(RPC_C_NS_SYNTAX_DEFAULT, EntryName, Interface
                   Vector);
RpcServerListen();
```

 

 




