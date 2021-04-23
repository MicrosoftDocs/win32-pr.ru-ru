---
title: Распределение и освобождение узлов по узлам
description: Выделение и освобождение структур данных по узлам с помощью заглушек — это метод управления памятью по умолчанию для всех параметров на клиенте и на сервере.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487981"
---
# <a name="node-by-node-allocation-and-deallocation"></a><span data-ttu-id="2f62f-103">Распределение и освобождение узлов по узлам</span><span class="sxs-lookup"><span data-stu-id="2f62f-103">Node-by-Node Allocation and Deallocation</span></span>

<span data-ttu-id="2f62f-104">Выделение и освобождение структур данных по узлам с помощью заглушек — это метод управления памятью по умолчанию для всех параметров на клиенте и на сервере.</span><span class="sxs-lookup"><span data-stu-id="2f62f-104">Node-by-node allocation and deallocation of data structures by the stubs is the default method of memory management for all parameters on both the client and the server.</span></span> <span data-ttu-id="2f62f-105">На стороне клиента заглушка выделяет каждый узел с помощью отдельного вызова для [ \_ \_ вынесения пользователем MIDL](/windows/desktop/Midl/midl-user-allocate-1).</span><span class="sxs-lookup"><span data-stu-id="2f62f-105">On the client side, the stub allocates each node with a separate call to [midl\_user\_allocate](/windows/desktop/Midl/midl-user-allocate-1).</span></span> <span data-ttu-id="2f62f-106">На стороне сервера вместо вызова метода **\_ пользовательского \_ выделения MIDL** используется частная память везде, где это возможно.</span><span class="sxs-lookup"><span data-stu-id="2f62f-106">On the server side, rather than calling **midl\_user\_allocate**, private memory is used whenever possible.</span></span> <span data-ttu-id="2f62f-107">Если вызывается **\_ пользовательское \_ выделение MIDL** , заглушки сервера будут вызывать **MIDL- \_ пользователь \_** , чтобы освободить данные.</span><span class="sxs-lookup"><span data-stu-id="2f62f-107">If **midl\_user\_allocate** is called, the server stubs will call **midl\_user\_free** to free the data.</span></span> <span data-ttu-id="2f62f-108">В большинстве случаев использование выделения и освобождения узлов, а не использования **\[ выделения (всех \_ узлов) \]** , приведет к повышению производительности заглушек на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="2f62f-108">In most cases, using node-by-node allocation and deallocation instead of using **\[allocate (all\_nodes)\]** will result in increased performance of the server side stubs.</span></span>

 

 