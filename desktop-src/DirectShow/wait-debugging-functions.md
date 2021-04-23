---
description: Функции ожидания отладки
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Функции ожидания отладки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683068"
---
# <a name="wait-debugging-functions"></a><span data-ttu-id="c8de0-103">Функции ожидания отладки</span><span class="sxs-lookup"><span data-stu-id="c8de0-103">Wait Debugging Functions</span></span>

<span data-ttu-id="c8de0-104">Microsoft DirectShow предоставляет несколько функций для отладки бесконечного ожидания.</span><span class="sxs-lookup"><span data-stu-id="c8de0-104">Microsoft DirectShow provides several functions for debugging infinite waits.</span></span>

<span data-ttu-id="c8de0-105">В розничных сборках функции [**дбгваитформултиплеобжектс**](dbgwaitformultipleobjects.md) и [**дбгваитфорсинглеобжект**](dbgwaitforsingleobject.md) работают подобно своим аналогам API Windows, **WaitForMultipleObjects** и **WaitForSingleObject** с неограниченными интервалами времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="c8de0-105">In retail builds, the [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) and [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) functions work like their Windows API counterparts, **WaitForMultipleObjects** and **WaitForSingleObject**, with infinite time-out intervals.</span></span>

<span data-ttu-id="c8de0-106">В отладочных сборках эти функции используют глобальное значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="c8de0-106">In debug builds, these functions use a global time-out value.</span></span> <span data-ttu-id="c8de0-107">Если время ожидания истекает, функция активирует утверждение.</span><span class="sxs-lookup"><span data-stu-id="c8de0-107">If the time-out expires, the function triggers an assert.</span></span> <span data-ttu-id="c8de0-108">В следующем разделе реестра указывается значение времени ожидания в миллисекундах:</span><span class="sxs-lookup"><span data-stu-id="c8de0-108">The following registry key specifies the time-out value, in milliseconds:</span></span>

<span data-ttu-id="c8de0-109">**\_ \_ \\ <DebugRoot> \\ <Module Name> \\ время ожидания на локальном компьютере hKey**</span><span class="sxs-lookup"><span data-stu-id="c8de0-109">**HKEY\_LOCAL\_MACHINE\\<DebugRoot>\\<Module Name>\\TIMEOUT**</span></span>

<span data-ttu-id="c8de0-110">где *<DebugRoot>* — путь реестра, описанный в разделе [функции выходных данных отладки](debug-output-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c8de0-110">where *<DebugRoot>* is the registry path described in the topic [Debug Output Functions](debug-output-functions.md).</span></span>

<span data-ttu-id="c8de0-111">Если ключ не существует, значение времени ожидания по умолчанию равно бесконечности.</span><span class="sxs-lookup"><span data-stu-id="c8de0-111">If the key does not exist, the time-out value defaults to INFINITE.</span></span> <span data-ttu-id="c8de0-112">Для переопределения записи реестра можно использовать функцию [**дбгсетваиттимеаут**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="c8de0-112">You can use the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function to override the registry entry.</span></span>



| <span data-ttu-id="c8de0-113">Функция</span><span class="sxs-lookup"><span data-stu-id="c8de0-113">Function</span></span>                                                       | <span data-ttu-id="c8de0-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c8de0-114">Description</span></span>                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="c8de0-115">**дбгсетваиттимеаут**</span><span class="sxs-lookup"><span data-stu-id="c8de0-115">**DbgSetWaitTimeout**</span></span>](dbgsetwaittimeout.md)                 | <span data-ttu-id="c8de0-116">Задает значение времени ожидания отладки.</span><span class="sxs-lookup"><span data-stu-id="c8de0-116">Sets the debugging time-out value.</span></span>                              |
| [<span data-ttu-id="c8de0-117">**дбгваитформултиплеобжектс**</span><span class="sxs-lookup"><span data-stu-id="c8de0-117">**DbgWaitForMultipleObjects**</span></span>](dbgwaitformultipleobjects.md) | <span data-ttu-id="c8de0-118">Ожидает сигнала для всех (или всех) указанных объектов.</span><span class="sxs-lookup"><span data-stu-id="c8de0-118">Waits for any (or all) of the specified objects to be signaled.</span></span> |
| [<span data-ttu-id="c8de0-119">**дбгваитфорсинглеобжект**</span><span class="sxs-lookup"><span data-stu-id="c8de0-119">**DbgWaitForSingleObject**</span></span>](dbgwaitforsingleobject.md)       | <span data-ttu-id="c8de0-120">Ожидает, пока объект станет сигнальным.</span><span class="sxs-lookup"><span data-stu-id="c8de0-120">Waits for an object to become signaled.</span></span>                         |



 

 

 



