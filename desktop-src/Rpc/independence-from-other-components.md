---
title: Независимость от других компонентов
description: Расширенные данные об ошибках полезны, даже если сервер или приложение, с помощью которых передается цепочка, не распознает Расширенные данные об ошибках или не использует ее. Рекомендуемые подходы для таких ситуаций приведены в конце этого раздела.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Независимость от других компонентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986765"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="786ea-105">Независимость от других компонентов</span><span class="sxs-lookup"><span data-stu-id="786ea-105">Independence From Other Components</span></span>

<span data-ttu-id="786ea-106">Расширенные данные об ошибках полезны, даже если сервер или приложение, с помощью которых передается цепочка, не распознает Расширенные данные об ошибках или не использует ее.</span><span class="sxs-lookup"><span data-stu-id="786ea-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="786ea-107">Рекомендуемые подходы для таких ситуаций приведены в конце этого раздела.</span><span class="sxs-lookup"><span data-stu-id="786ea-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="786ea-108">Расширенные данные об ошибках наиболее полезны, если приложения или серверы, использующие RPC, используют расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="786ea-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="786ea-109">При исследовании \_ кода ошибки RPC S, если \_ \* используемые серверы или приложения не делают доступными Расширенные данные об ошибках, рассмотрите следующие подходы.</span><span class="sxs-lookup"><span data-stu-id="786ea-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="786ea-110">Пройдите пробный анализ.</span><span class="sxs-lookup"><span data-stu-id="786ea-110">Take a sniff.</span></span>

    <span data-ttu-id="786ea-111">Воспроизводите сценарий, выполняя пробное использование.</span><span class="sxs-lookup"><span data-stu-id="786ea-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="786ea-112">При прослушивании сети будут содержаться Расширенные данные об ошибках.</span><span class="sxs-lookup"><span data-stu-id="786ea-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="786ea-113">Изучите его из отладчика.</span><span class="sxs-lookup"><span data-stu-id="786ea-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="786ea-114">Если анализ проблемы не работает, так как вызов является локальным или происходит локально, Подключите отладчик к процессу, который возвращает ошибку, и разместите точку останова сразу после вызова RPC, вызвав ошибку.</span><span class="sxs-lookup"><span data-stu-id="786ea-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="786ea-115">RPC часто указывает на ошибки, вызывая исключения, поэтому, если вы ищете ошибку 1825 (ошибка пакетом RPC \_ S \_ sec \_ pkg \_ ), включите исключение 1825 и при прерывании отладчика на этом исключении Проверьте расширенные сведения об ошибке для потока.</span><span class="sxs-lookup"><span data-stu-id="786ea-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




