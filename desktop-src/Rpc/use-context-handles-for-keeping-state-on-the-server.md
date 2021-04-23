---
title: Использование дескрипторов контекста для сохранения состояния на сервере
description: Использование дескрипторов контекста для сохранения состояния на сервере
ms.assetid: ee511745-04cf-445d-a02b-41734aabc193
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90bf14632ed1821a1a097a64951f6ca9aef751d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253332"
---
# <a name="use-context-handles-for-keeping-state-on-the-server"></a><span data-ttu-id="92ce1-103">Использование дескрипторов контекста для сохранения состояния на сервере</span><span class="sxs-lookup"><span data-stu-id="92ce1-103">Use Context Handles for Keeping State on the Server</span></span>

<span data-ttu-id="92ce1-104">**Рекомендации:** Когда состояние хранится на сервере между вызовами, используйте дескрипторы контекста.</span><span class="sxs-lookup"><span data-stu-id="92ce1-104">**Best practice:** Whenever state is kept on the server between calls, use context handles.</span></span>

<span data-ttu-id="92ce1-105">Дескрипторы контекста часто вас затруднительным для новых программистов RPC, а затраты на дескрипторы контекста обучения могут не полагаться на усилия.</span><span class="sxs-lookup"><span data-stu-id="92ce1-105">Context handles are often intimidating for new RPC programmers, and the overhead of learning context handles may not initially appear worth the effort.</span></span> <span data-ttu-id="92ce1-106">Это важно, поскольку дескрипторы контекста имеют встроенные решения для многих распространенных ловушек, обнаруженных в сетевом программировании, которые в противном случае придется реализовать с нуля.</span><span class="sxs-lookup"><span data-stu-id="92ce1-106">It is worth it because context handles have built-in solutions for many common pitfalls encountered in network programming that otherwise would have to be implemented from scratch.</span></span> <span data-ttu-id="92ce1-107">Понимание дескрипторов контекста оплачивает дивиденды позже.</span><span class="sxs-lookup"><span data-stu-id="92ce1-107">Understanding context handles pays dividends later.</span></span>

 

 




