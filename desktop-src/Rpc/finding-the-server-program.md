---
title: Поиск программы сервера
description: После того как время выполнения RPC на стороне клиента подключается к системе узла сервера, запрошенной в маркере привязки, Библиотека времени выполнения RPC клиента находит серверный процесс.
ms.assetid: 0c863018-746a-4793-abe7-1838d988e0f4
keywords:
- Удаленный вызов процедур RPC, задачи, Поиск программы сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b822dbca1a927e13f01d7c91aa7c78267db4d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672085"
---
# <a name="finding-the-server-program"></a><span data-ttu-id="eb558-104">Поиск программы сервера</span><span class="sxs-lookup"><span data-stu-id="eb558-104">Finding the Server Program</span></span>

<span data-ttu-id="eb558-105">После того как время выполнения RPC на стороне клиента подключается к системе узла сервера, запрошенной в маркере привязки, Библиотека времени выполнения RPC клиента находит серверный процесс.</span><span class="sxs-lookup"><span data-stu-id="eb558-105">After the client side RPC run time connects to a server host system requested in the binding handle, the client RPC run-time library finds the server process.</span></span> <span data-ttu-id="eb558-106">Для этого он запрашивает карту конечных точек в системе узла сервера.</span><span class="sxs-lookup"><span data-stu-id="eb558-106">To do this, it queries the endpoint map on the server host system.</span></span> <span data-ttu-id="eb558-107">На карте конечных точек содержатся сведения о том, на какой конечной точке ожидает сервер.</span><span class="sxs-lookup"><span data-stu-id="eb558-107">The endpoint map contains information about which endpoint the server is listening to.</span></span>

 

 




