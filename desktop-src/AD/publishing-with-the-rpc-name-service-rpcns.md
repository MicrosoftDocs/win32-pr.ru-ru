---
title: Публикация с помощью службы имен RPC
description: Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс).
ms.assetid: 0c8e1207-daeb-4dc8-b83a-a54cd59a46a7
ms.tgt_platform: multiple
keywords:
- Публикация с помощью службы имен RPC Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b672eec6308d709fe2f4cbc64ad22ecf0d6edd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069756"
---
# <a name="publishing-with-the-rpc-name-service"></a><span data-ttu-id="c51af-104">Публикация с помощью службы имен RPC</span><span class="sxs-lookup"><span data-stu-id="c51af-104">Publishing with the RPC Name Service</span></span>

<span data-ttu-id="c51af-105">Службы RPC могут публиковать свои идентификаторы в пространстве имен с помощью API-интерфейсов службы имен RPC (Рпкнс).</span><span class="sxs-lookup"><span data-stu-id="c51af-105">RPC services can publish their identifiers in a namespace using the RPC name service (RpcNs) APIs.</span></span> <span data-ttu-id="c51af-106">API-интерфейсы Рпкнс в Windows 2000 публикуют записи RPC в домен Active Directory Services.</span><span class="sxs-lookup"><span data-stu-id="c51af-106">The RpcNs APIs in Windows 2000 publish the RPC entries in Active Directory Domain Services.</span></span> <span data-ttu-id="c51af-107">Службы создают привязки RPC и публикуют их в пространстве имен как именованные записи RPC-сервера с атрибутами, включая уникальный идентификатор интерфейса, идентификатор GUID, распознаваемый клиентами.</span><span class="sxs-lookup"><span data-stu-id="c51af-107">Services create RPC bindings and publish them in the namespace as named RPC Server entries with attributes including the unique interface ID, a GUID that is recognized by clients.</span></span> <span data-ttu-id="c51af-108">Затем клиент может выполнить поиск серверов RPC, предлагающих нужный интерфейс, импортировать привязку и подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="c51af-108">A client can then search for RPC Servers offering the desired interface, import the binding, and connect to the server.</span></span>

<span data-ttu-id="c51af-109">Дополнительные сведения о публикации службы RPC см. в разделе [Привязка на стороне сервера](/windows/desktop/Rpc/server-side-binding).</span><span class="sxs-lookup"><span data-stu-id="c51af-109">For more information about publishing an RPC service, see [Server-side Binding](/windows/desktop/Rpc/server-side-binding).</span></span>

 

 