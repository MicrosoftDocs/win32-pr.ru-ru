---
description: Пакет SDK для сетевой монитор содержит функции и примеры кода, необходимые для создания экспертов. Однако можно также использовать существующие инструменты, в том числе редактор диалоговых окон.
ms.assetid: 6a3834b7-753f-42cc-986f-3d7e8bf79fd9
title: Программирование эксперта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df633d971558f9b14374680b09a22771e10ea0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156307"
---
# <a name="programming-an-expert"></a><span data-ttu-id="1ca5c-104">Программирование эксперта</span><span class="sxs-lookup"><span data-stu-id="1ca5c-104">Programming an Expert</span></span>

<span data-ttu-id="1ca5c-105">Пакет SDK для сетевой монитор содержит функции и примеры кода, необходимые для создания экспертов.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-105">The Network Monitor SDK includes the functions and sample code you need to build experts.</span></span> <span data-ttu-id="1ca5c-106">Однако можно также использовать существующие инструменты, в том числе редактор диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-106">However, you can also use existing tools, including a dialog editor.</span></span>

## <a name="minimum-requirements-to-run-an-expert"></a><span data-ttu-id="1ca5c-107">Минимальные требования для запуска эксперта</span><span class="sxs-lookup"><span data-stu-id="1ca5c-107">Minimum Requirements to Run an Expert</span></span>

<span data-ttu-id="1ca5c-108">В следующей таблице перечислены точки входа библиотеки DLL и функции экспертов, которые необходимо использовать для создания эксперта.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-108">The following table lists the DLL entry points and expert functions you must use to build an expert.</span></span>



| <span data-ttu-id="1ca5c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="1ca5c-109">Name</span></span>                                                 | <span data-ttu-id="1ca5c-110">Тип</span><span class="sxs-lookup"><span data-stu-id="1ca5c-110">Type</span></span>               | <span data-ttu-id="1ca5c-111">Обязательно?</span><span class="sxs-lookup"><span data-stu-id="1ca5c-111">Required?</span></span>                                       |
|------------------------------------------------------|--------------------|-------------------------------------------------|
| [<span data-ttu-id="1ca5c-112">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-112">**DllMain**</span></span>](dllmain-expert.md)                    | <span data-ttu-id="1ca5c-113">Функция записи DLL</span><span class="sxs-lookup"><span data-stu-id="1ca5c-113">DLL entry function</span></span> | <span data-ttu-id="1ca5c-114">Да</span><span class="sxs-lookup"><span data-stu-id="1ca5c-114">Yes</span></span>                                             |
| [<span data-ttu-id="1ca5c-115">**Регистрация экспертов**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-115">**Register Expert**</span></span>](register-expert.md)           | <span data-ttu-id="1ca5c-116">Функция записи DLL</span><span class="sxs-lookup"><span data-stu-id="1ca5c-116">DLL entry function</span></span> | <span data-ttu-id="1ca5c-117">Да</span><span class="sxs-lookup"><span data-stu-id="1ca5c-117">Yes</span></span>                                             |
| [<span data-ttu-id="1ca5c-118">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-118">**Run**</span></span>](run.md)                                   | <span data-ttu-id="1ca5c-119">Функция записи DLL</span><span class="sxs-lookup"><span data-stu-id="1ca5c-119">DLL entry function</span></span> | <span data-ttu-id="1ca5c-120">Да</span><span class="sxs-lookup"><span data-stu-id="1ca5c-120">Yes</span></span>                                             |
| [<span data-ttu-id="1ca5c-121">**Configure**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-121">**Configure**</span></span>](configure.md)                       | <span data-ttu-id="1ca5c-122">Функция записи DLL</span><span class="sxs-lookup"><span data-stu-id="1ca5c-122">DLL entry function</span></span> | <span data-ttu-id="1ca5c-123">Только в том случае, если эксперт предоставляет пользователю конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-123">Only if the expert provides user configuration.</span></span> |
| [<span data-ttu-id="1ca5c-124">**експертиндикатестатус**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-124">**ExpertIndicateStatus**</span></span>](expertindicatestatus.md) | <span data-ttu-id="1ca5c-125">Экспертная функция</span><span class="sxs-lookup"><span data-stu-id="1ca5c-125">Expert function</span></span>    | <span data-ttu-id="1ca5c-126">Да</span><span class="sxs-lookup"><span data-stu-id="1ca5c-126">Yes</span></span>                                             |
| [<span data-ttu-id="1ca5c-127">**експертсубмитевент**</span><span class="sxs-lookup"><span data-stu-id="1ca5c-127">**ExpertSubmitEvent**</span></span>](expertsubmitevent.md)       | <span data-ttu-id="1ca5c-128">Экспертная функция</span><span class="sxs-lookup"><span data-stu-id="1ca5c-128">Expert function</span></span>    | <span data-ttu-id="1ca5c-129">Да</span><span class="sxs-lookup"><span data-stu-id="1ca5c-129">Yes</span></span>                                             |



 

<span data-ttu-id="1ca5c-130">Просмотрите разделы справки эксперта и анализатора в сетевой монитор SDK, чтобы обновить исходный код, а затем используйте пример кода и процедуры, приведенные в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="1ca5c-130">Review the expert and parser reference topics in the Network Monitor SDK to update your source code and then use the sample code and procedures provided in these topics:</span></span>

-   [<span data-ttu-id="1ca5c-131">Создание эксперта</span><span class="sxs-lookup"><span data-stu-id="1ca5c-131">Building an Expert</span></span>](building-an-expert.md)
-   [<span data-ttu-id="1ca5c-132">Установка эксперта</span><span class="sxs-lookup"><span data-stu-id="1ca5c-132">Installing an Expert</span></span>](installing-an-expert-to-network-monitor-2-1.md)
-   [<span data-ttu-id="1ca5c-133">Отладка эксперта</span><span class="sxs-lookup"><span data-stu-id="1ca5c-133">Debugging an Expert</span></span>](debugging-an-expert.md)

<span data-ttu-id="1ca5c-134">Для экспертных библиотек DLL требуется язык C, а не C++, соглашение о вызовах, поскольку функции вызываются через указатели функций с помощью оверлея.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-134">Expert DLLs require the C, not the C++, calling convention because functions are called through function pointers by using an overlay.</span></span> <span data-ttu-id="1ca5c-135">С помощью набора специализированных экспертных функций эксперт имеет доступ к кадрам в записи.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-135">Through a set of specialized expert functions, the expert has access to the frames in the capture.</span></span> <span data-ttu-id="1ca5c-136">Эксперт может использовать большую часть API сетевой монитор для управления возвращаемыми данными.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-136">The expert can use most of the Network Monitor API to manipulate the returned data.</span></span> <span data-ttu-id="1ca5c-137">Когда эксперт находит сведения для отправки пользователю, он упаковывает данные в структуру данных событий и отправляет их в сетевой монитор, который затем отображает информацию в окне вывода экспертов.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-137">When an expert finds information to send to the user, it packages the information in an event data structure and submits it to Network Monitor, which then displays the information in an expert output window.</span></span> <span data-ttu-id="1ca5c-138">Эксперт должен периодически обновлять сетевой монитор с информацией о состоянии завершения, которая предоставляется функцией [**експертиндикатестатус**](expertindicatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca5c-138">The expert must periodically update Network Monitor with percentage-completion status information, which is provided by the [**ExpertIndicateStatus**](expertindicatestatus.md) function.</span></span>

<span data-ttu-id="1ca5c-139">Экспортированные функции экспертов вызываются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1ca5c-139">The expert's exported functions are called as follows:</span></span>

-   <span data-ttu-id="1ca5c-140">Когда сетевой монитор создает список экспертов, которые должны предоставляться пользователю, сетевой монитор вызывает функцию [**регистрации экспертов**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca5c-140">When Network Monitor is creating the list of experts to present to the user, Network Monitor calls the [**Register Expert**](register-expert.md) function.</span></span>
-   <span data-ttu-id="1ca5c-141">Если после вызова функции **регистрации** эксперта настраивается, сетевой монитор вызывает функцию [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca5c-141">After the call to **Register**, if the expert is configurable, Network Monitor calls the [**Configure**](configure.md) function.</span></span>
-   <span data-ttu-id="1ca5c-142">Когда сетевой монитор пользователь щелкает " **запустить эксперт**", сетевой монитор вызывает функцию [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="1ca5c-142">When the Network Monitor user clicks **Run Expert**, Network Monitor calls the [**Run**](run.md) function.</span></span>

<span data-ttu-id="1ca5c-143">Когда специалисты анализируют запрошенные кадры и находят проблему, они используют [**експертсубмитевент**](expertsubmitevent.md) для отправки события, содержащего сведения о проблеме.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-143">When experts analyze the requested frames and find a problem, they use [**ExpertSubmitEvent**](expertsubmitevent.md) to submit an event that contains information about the problem.</span></span> <span data-ttu-id="1ca5c-144">Сетевой монитор распространяет событие в стандартный (общий) Просмотр событий или (если он регистрируется специалистом) в частном Просмотр событий.</span><span class="sxs-lookup"><span data-stu-id="1ca5c-144">Network Monitor distributes the event to either the standard (shared) Event Viewer or (if the expert registers for it) to a private Event Viewer.</span></span>

 

 



