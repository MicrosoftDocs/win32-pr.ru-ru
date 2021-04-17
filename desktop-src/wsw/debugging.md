---
title: Отладка (веб-службы Windows)
description: Набор функций доступен только в ОТЛАДОЧной сборке и предназначен для тестирования и отладки.
ms.assetid: 23c01420-3f51-4c3f-9ee1-2614de3a278f
keywords:
- Отладка веб-служб для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cad0abe916e068408cfda48184aa86e40029203
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710423"
---
# <a name="debugging-windows-web-services"></a><span data-ttu-id="ea53b-106">Отладка (веб-службы Windows)</span><span class="sxs-lookup"><span data-stu-id="ea53b-106">Debugging (Windows Web Services)</span></span>

<span data-ttu-id="ea53b-107">Набор функций доступен только в ОТЛАДОЧной сборке и предназначен для тестирования и отладки.</span><span class="sxs-lookup"><span data-stu-id="ea53b-107">A set of functions is only available in the DEBUG build, and are intended for testing and debugging.</span></span>


<span data-ttu-id="ea53b-108">Существует несколько функций и переменных среды, доступных только в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="ea53b-108">There are a number of functions and environment variables available in the DEBUG mode only.</span></span> <span data-ttu-id="ea53b-109">Их можно использовать для тестирования и отладки.</span><span class="sxs-lookup"><span data-stu-id="ea53b-109">They can be used to help with testing and debugging.</span></span>

-   <span data-ttu-id="ea53b-110">Установка Встимеаут = 0 приведет к бесконечности времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="ea53b-110">Setting WsTimeout=0 will cause all timeouts to be INFINITE.</span></span> <span data-ttu-id="ea53b-111">Это полезно при пошаговом выполнении отладчика во время операций с учетом времени.</span><span class="sxs-lookup"><span data-stu-id="ea53b-111">This is useful when stepping through the debugger during time sensitive operations.</span></span>
-   <span data-ttu-id="ea53b-112">Параметр Всфаилкаунт имеет тот же результат, что и вызов Вссетаутофаил.</span><span class="sxs-lookup"><span data-stu-id="ea53b-112">Setting WsFailCount has the same effect as calling WsSetAutoFail.</span></span>
-   <span data-ttu-id="ea53b-113">Всфлагс позволяет задавать различные флаги, изменяющие поведение во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="ea53b-113">WsFlags allows you to set various flags that modify the runtime behavior.</span></span> <span data-ttu-id="ea53b-114">Синтаксис — Всфлагс = a, b, c.</span><span class="sxs-lookup"><span data-stu-id="ea53b-114">The syntax is WsFlags=a,b,c.</span></span> <span data-ttu-id="ea53b-115">Поддерживаются флаги Модифитиместамп, Модифинклусивепрефиксес, Модифитиместампдижест, Модифитохеадердижест и ModifySignatureValue.</span><span class="sxs-lookup"><span data-stu-id="ea53b-115">The supported flags are ModifyTimestamp, ModifyInclusivePrefixes, ModifyTimestampDigest, ModifyToHeaderDigest and ModifySignatureValue.</span></span>

<span data-ttu-id="ea53b-116">При отладке используются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="ea53b-116">The following functions are used with debugging:</span></span>

-   [<span data-ttu-id="ea53b-117">**всдумпмемори**</span><span class="sxs-lookup"><span data-stu-id="ea53b-117">**WsDumpMemory**</span></span>](wsdumpmemory.md)
-   [<span data-ttu-id="ea53b-118">**вссетаутофаил**</span><span class="sxs-lookup"><span data-stu-id="ea53b-118">**WsSetAutoFail**</span></span>](wssetautofail.md)

 

 




