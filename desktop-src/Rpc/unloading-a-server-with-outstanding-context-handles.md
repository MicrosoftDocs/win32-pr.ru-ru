---
title: Выгрузка сервера с необработанными дескрипторами контекста
description: Обычно выгрузка библиотеки DLL, которая обслуживает вызовы RPC с помощью дескрипторов контекста, без предварительной остановки хост-процесса была проблематичной.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258936"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="78393-103">Выгрузка сервера с необработанными дескрипторами контекста</span><span class="sxs-lookup"><span data-stu-id="78393-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="78393-104">Обычно выгрузка библиотеки DLL, которая обслуживает вызовы RPC с помощью дескрипторов контекста, без предварительной остановки хост-процесса была проблематичной.</span><span class="sxs-lookup"><span data-stu-id="78393-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="78393-105">Это вызвано тем, что подсистема запуска больше не действительна при выгрузке библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="78393-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="78393-106">Если клиент с ранее открытым контекстом завершается с ошибкой, а во время выполнения RPC попытается закрыть маркер контекста, то попытка вызова процедуры, вызывающей запуск, нарушается, и сервер завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="78393-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="78393-107">Начиная с Windows XP был добавлен новый API с именем [**рпксерверунрегистерифекс**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) .</span><span class="sxs-lookup"><span data-stu-id="78393-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="78393-108">**Рпксерверунрегистерифекс** закрывает дескрипторы контекста, открытые незарегистрированным интерфейсом. Функция [**рпксерверунрегистериф**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) не имеет значение.</span><span class="sxs-lookup"><span data-stu-id="78393-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="78393-109">Использование **рпксерверунрегистерифекс** не является обязательным, когда весь процесс завершается, но это необходимо, если одна или несколько библиотек DLL, в которых размещаются подпрограммы выполнения, выгружаются, когда существуют необработанные дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="78393-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




