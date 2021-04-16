---
title: Функции, вызываемые системой
description: Функции, вызываемые системой
ms.assetid: 006ac524-d456-44e9-957b-42a85dc92519
keywords:
- мультимедиа аудио, функции ACM
- функции Audio, ACM
- Диспетчер аудиосжатия (ACM), функции
- ACM (диспетчер аудиосжатия), функции
- Функции ACM
- функции обратного вызова
- Диспетчер аудиосжатия (ACM), функции обратного вызова
- ACM (диспетчер аудиосжатия), функции обратного вызова
- процедуры-обработчики
- процедуры драйвера
- Диспетчер аудиосжатия (ACM), процедуры-обработчики
- ACM (диспетчер аудиосжатия), процедуры-обработчики
- Диспетчер аудиосжатия (ACM), процедуры драйверов
- ACM (диспетчер аудиосжатия), процедуры драйвера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1324ea168892d54f21754658607476c35075910
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105650340"
---
# <a name="functions-called-by-the-system"></a><span data-ttu-id="47bba-117">Функции, вызываемые системой</span><span class="sxs-lookup"><span data-stu-id="47bba-117">Functions Called by the System</span></span>

<span data-ttu-id="47bba-118">Система вызывает три различных вида определяемых приложением функций.</span><span class="sxs-lookup"><span data-stu-id="47bba-118">The system calls three different kinds of application-defined functions.</span></span> <span data-ttu-id="47bba-119">Функции обратного вызова — это функции в приложении, которые система вызывает в ответ на запрос, выполняемый приложением.</span><span class="sxs-lookup"><span data-stu-id="47bba-119">Callback functions are functions in your application that the system calls in response to a request made by an application.</span></span> <span data-ttu-id="47bba-120">Процедуры-ловушки помогают приложению управлять настройкой диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="47bba-120">Hook procedures help an application handle the customization of dialog boxes.</span></span> <span data-ttu-id="47bba-121">Процедура драйвера — это реализация собственного кодека, преобразователя или фильтра в приложении.</span><span class="sxs-lookup"><span data-stu-id="47bba-121">A driver procedure is an application's implementation of its own codec, converter, or filter.</span></span>

<span data-ttu-id="47bba-122">Функции обратного вызова имеют следующие имена:</span><span class="sxs-lookup"><span data-stu-id="47bba-122">The callback functions have the following names:</span></span>

-   [<span data-ttu-id="47bba-123">**акмдриверенумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="47bba-123">**acmDriverEnumCallback**</span></span>](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [<span data-ttu-id="47bba-124">**акмфилтеренумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="47bba-124">**acmFilterEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [<span data-ttu-id="47bba-125">**акмфилтертаженумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="47bba-125">**acmFilterTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)
-   [<span data-ttu-id="47bba-126">**акмформатенумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="47bba-126">**acmFormatEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [<span data-ttu-id="47bba-127">**акмформаттаженумкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="47bba-127">**acmFormatTagEnumCallback**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)
-   <span data-ttu-id="47bba-128">[**акмстреамконверткаллбакк**](/previous-versions//dd742925(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="47bba-128">[**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))</span></span>

<span data-ttu-id="47bba-129">Большинство функций перечисления в ACM используют функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="47bba-129">Most of the enumeration functions in the ACM use callback functions.</span></span> <span data-ttu-id="47bba-130">Например, при вызове функции перечисления ACM перечисляет элементы путем повторного вызова приложения с помощью функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="47bba-130">For example, when you call an enumeration function, the ACM enumerates the items by repeatedly calling the application through the callback function.</span></span>

<span data-ttu-id="47bba-131">Некоторые функции не могут быть вызваны из этих функций обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="47bba-131">Some functions cannot be called from within these callback functions.</span></span> <span data-ttu-id="47bba-132">Функции, которые нельзя вызывать, управляют внутренними структурами ACM, которые используются функциями перечисления.</span><span class="sxs-lookup"><span data-stu-id="47bba-132">Functions that cannot be called manipulate internal ACM structures that are used by the enumeration functions.</span></span> <span data-ttu-id="47bba-133">Следующие функции не должны вызываться из функции обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="47bba-133">The following functions should not be called from within a callback function:</span></span>

-   [<span data-ttu-id="47bba-134">**акмдриверадд**</span><span class="sxs-lookup"><span data-stu-id="47bba-134">**acmDriverAdd**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [<span data-ttu-id="47bba-135">**акмдриверприорити**</span><span class="sxs-lookup"><span data-stu-id="47bba-135">**acmDriverPriority**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [<span data-ttu-id="47bba-136">**акмдриверремове**</span><span class="sxs-lookup"><span data-stu-id="47bba-136">**acmDriverRemove**</span></span>](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

<span data-ttu-id="47bba-137">Система вызывает следующие функции, которые помогают приложению управлять настройкой диалоговых окон:</span><span class="sxs-lookup"><span data-stu-id="47bba-137">The system calls the following functions to help an application handle the customization of dialog boxes:</span></span>

-   [<span data-ttu-id="47bba-138">**акмфилтерчусехукпрок**</span><span class="sxs-lookup"><span data-stu-id="47bba-138">**acmFilterChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [<span data-ttu-id="47bba-139">**акмформатчусехукпрок**</span><span class="sxs-lookup"><span data-stu-id="47bba-139">**acmFormatChooseHookProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)

<span data-ttu-id="47bba-140">Следующая функция указывается как прототип, позволяющий приложению использовать настраиваемый кодек, преобразователь или фильтр.</span><span class="sxs-lookup"><span data-stu-id="47bba-140">The following function is specified as a prototype that allows an application to use a customized codec, converter, or filter.</span></span> <span data-ttu-id="47bba-141">Функция, которая соответствует этому прототипу, может передаваться в качестве аргумента функции [**акмдриверадд**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) .</span><span class="sxs-lookup"><span data-stu-id="47bba-141">A function conforming to this prototype may be passed as an argument to the [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) function.</span></span>

-   [<span data-ttu-id="47bba-142">**акмдриверпрок**</span><span class="sxs-lookup"><span data-stu-id="47bba-142">**acmDriverProc**</span></span>](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)

 

 