---
title: Очистка бездействующего подключения
description: По умолчанию соединения в пуле потоков не закрываются, пока не завершится вся ассоциация.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887859"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="f8485-103">Очистка бездействующего подключения</span><span class="sxs-lookup"><span data-stu-id="f8485-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="f8485-104">По умолчанию соединения в пуле потоков не закрываются, пока не завершится вся ассоциация.</span><span class="sxs-lookup"><span data-stu-id="f8485-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="f8485-105">Эта политика позволяет клиентам с большим количеством потоков или идентификаторов безопасности выполнять вызовы RPC на сервере эффективным образом.</span><span class="sxs-lookup"><span data-stu-id="f8485-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="f8485-106">Недостаток заключается в том, что для поддержания этих подключений может быть зафиксировано недостаточное количество ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8485-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="f8485-107">Для управления процессом RPC предоставляет функцию [**рпкмгмтенаблеидлеклеануп**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) .</span><span class="sxs-lookup"><span data-stu-id="f8485-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="f8485-108">Эта функция включает очистку бездействующего подключения; Клиент периодически проверяет пул подключений и закрывает соединения, которые не использовались недавно.</span><span class="sxs-lookup"><span data-stu-id="f8485-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="f8485-109">Если ассоциация поддерживает дескрипторы контекста, то очистка неактивных соединений закрывает все неактивные подключения, но гарантирует, что по крайней мере одно соединение остается открытым, даже если соединение бездействует (в противном случае сервер получает дескриптор контекста).</span><span class="sxs-lookup"><span data-stu-id="f8485-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="f8485-110">Если ассоциация не поддерживает дескрипторы контекста, то очистка неактивных соединений закрывает все неактивные соединения, даже если в пуле нет соединений.</span><span class="sxs-lookup"><span data-stu-id="f8485-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="f8485-111">В Windows XP время выполнения RPC отслеживает количество открытых соединений в ассоциации и автоматически включает очистку бездействующего подключения, если число подключений в любой связи превышает определенное пороговое значение.</span><span class="sxs-lookup"><span data-stu-id="f8485-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




