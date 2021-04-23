---
title: Очистка на стороне сервера
description: Очистка на стороне сервера и удаленный вызов процедур (RPC).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068233"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="9a143-103">Очистка на стороне сервера</span><span class="sxs-lookup"><span data-stu-id="9a143-103">Server-side Cleanup</span></span>

<span data-ttu-id="9a143-104">Представьте себе следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="9a143-104">Imagine the following scenario:</span></span>

<span data-ttu-id="9a143-105">Клиент открывает обработчик контекста, а затем либо останавливает, либо теряет подключение к серверу.</span><span class="sxs-lookup"><span data-stu-id="9a143-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="9a143-106">Как сервер обнаруживает, что клиент завершился сбоем, и должен быть запущен обработчик контекста?</span><span class="sxs-lookup"><span data-stu-id="9a143-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="9a143-107">Существует два подсценария: один заключается в том, что работа клиента завершается упорядоченным способом.</span><span class="sxs-lookup"><span data-stu-id="9a143-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="9a143-108">В таком случае он уведомляет сервер о завершении работы, а сервер может выполнить очистку, включая выполнение контекста.</span><span class="sxs-lookup"><span data-stu-id="9a143-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="9a143-109">Если клиент не завершает работу последовательно или не может уведомить сервер, сервер использует проверку активности, чтобы определить, доступен ли клиент по-прежнему.</span><span class="sxs-lookup"><span data-stu-id="9a143-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="9a143-110">На стороне сервера функция [**рпкмгмтсеткомтимеаут**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) не действует.</span><span class="sxs-lookup"><span data-stu-id="9a143-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="9a143-111">Вместо этого сервер использует параметр "Глобальный том на компьютер — проверка активности", значение по умолчанию примерно два часа.</span><span class="sxs-lookup"><span data-stu-id="9a143-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="9a143-112">Если клиент не отвечает на активность сохранения сервера, соединение закрывается.</span><span class="sxs-lookup"><span data-stu-id="9a143-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="9a143-113">Когда все соединения с данным клиентским процессом закрываются, сервер очищает и запускает незавершенные дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="9a143-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




