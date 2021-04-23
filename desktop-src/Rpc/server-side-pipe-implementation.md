---
title: Реализация Server-Sideного канала
description: Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6927350e10061850c5fac0ab0db7c18570dd2bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068232"
---
# <a name="server-side-pipe-implementation"></a><span data-ttu-id="fbcca-103">Реализация Server-Sideного канала</span><span class="sxs-lookup"><span data-stu-id="fbcca-103">Server-Side Pipe Implementation</span></span>

<span data-ttu-id="fbcca-104">Серверным программам для распределенных приложений, использующих каналы, не требуется реализовывать какие-либо функции push, Pull или Alloc.</span><span class="sxs-lookup"><span data-stu-id="fbcca-104">Server programs for distributed applications that use pipes need not implement any push, pull, or alloc functions.</span></span> <span data-ttu-id="fbcca-105">Они должны содержать процедуры, которые клиенты могут вызывать удаленно для инициации передачи данных.</span><span class="sxs-lookup"><span data-stu-id="fbcca-105">They do need to contain procedures that clients can invoke remotely to initiate data transfers.</span></span> <span data-ttu-id="fbcca-106">В следующих разделах в этом разделе объясняется, как можно реализовать удаленные процедуры на сервере.</span><span class="sxs-lookup"><span data-stu-id="fbcca-106">In the following topics, this section explains how the server's remote procedures can be implemented.</span></span>

-   [<span data-ttu-id="fbcca-107">Реализация входных каналов на сервере</span><span class="sxs-lookup"><span data-stu-id="fbcca-107">Implementing Input Pipes on the Server</span></span>](implementing-input-pipes-on-the-server.md)
-   [<span data-ttu-id="fbcca-108">Реализация выходных каналов на сервере</span><span class="sxs-lookup"><span data-stu-id="fbcca-108">Implementing Output Pipes on the Server</span></span>](implementing-output-pipes-on-the-server.md)

 

 




