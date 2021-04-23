---
title: Перенос вызовов плоскости набора элементов
description: В OpenGL вы выделяете плоскости трафаретов, запрашивая соответствующий формат пикселей с помощью OpenGL Ауксинитдисплаймоде или Чусепикселформат.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Перенос GL в ГК, плоскости трафаретов
- Перенос из ДИАФРАГМы в ГК, плоскости трафаретов
- перенос в OpenGL из IRI GL, трафаретов набора элементов
- Перенос по стандарту OpenGL из IRI GL, плоскости трафаретов
- плоскости трафаретов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331000"
---
# <a name="porting-stencil-plane-calls"></a><span data-ttu-id="7d988-108">Перенос вызовов плоскости набора элементов</span><span class="sxs-lookup"><span data-stu-id="7d988-108">Porting Stencil Plane Calls</span></span>

<span data-ttu-id="7d988-109">В OpenGL вы выделяете плоскости трафаретов, запрашивая соответствующий формат пикселей с помощью OpenGL **ауксинитдисплаймоде** или [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span><span class="sxs-lookup"><span data-stu-id="7d988-109">In OpenGL, you allocate stencil planes by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).</span></span> <span data-ttu-id="7d988-110">функции.</span><span class="sxs-lookup"><span data-stu-id="7d988-110">functions.</span></span> <span data-ttu-id="7d988-111">В следующей таблице перечислены функции IRI GL, которые влияют на плоскости трафаретов и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="7d988-111">The following table lists IRIS GL functions that affect the stencil planes and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="7d988-112">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="7d988-112">IRIS GL function</span></span>             | <span data-ttu-id="7d988-113">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="7d988-113">OpenGL function</span></span>                                         | <span data-ttu-id="7d988-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7d988-114">Meaning</span></span>                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="7d988-115">**стенсизе**</span><span class="sxs-lookup"><span data-stu-id="7d988-115">**stensize**</span></span>                 | <span data-ttu-id="7d988-116">**чусепикселформат**</span><span class="sxs-lookup"><span data-stu-id="7d988-116">**ChoosePixelFormat**</span></span>                                   |                                                        |
| <span data-ttu-id="7d988-117">**набор элементов**( **true**,...)</span><span class="sxs-lookup"><span data-stu-id="7d988-117">**stencil**( **TRUE**, ... )</span></span> | <span data-ttu-id="7d988-118">[**гленабле**](glenable.md) ( \_ тест шаблона GL \_ )</span><span class="sxs-lookup"><span data-stu-id="7d988-118">[**glEnable**](glenable.md) ( GL\_STENCIL\_TEST )</span></span>      | <span data-ttu-id="7d988-119">Включает тесты наборов элементов.</span><span class="sxs-lookup"><span data-stu-id="7d988-119">Enables stencil tests.</span></span>                                 |
| <span data-ttu-id="7d988-120">**набор элементов**</span><span class="sxs-lookup"><span data-stu-id="7d988-120">**stencil**</span></span>                  | [<span data-ttu-id="7d988-121">**глстенЦилоп**</span><span class="sxs-lookup"><span data-stu-id="7d988-121">**glStencilOp**</span></span>](glstencilop.md)                      | <span data-ttu-id="7d988-122">Задает действия теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="7d988-122">Sets stencil test actions.</span></span>                             |
| <span data-ttu-id="7d988-123">**набор элементов**(... Func,...)</span><span class="sxs-lookup"><span data-stu-id="7d988-123">**stencil**(... func, ... )</span></span>  | [<span data-ttu-id="7d988-124">**глстенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="7d988-124">**glStencilFunc**</span></span>](glstencilfunc.md)                  | <span data-ttu-id="7d988-125">Задает значение функции и ссылки для тестирования набора элементов.</span><span class="sxs-lookup"><span data-stu-id="7d988-125">Sets function and reference value for stencil testing.</span></span> |
| <span data-ttu-id="7d988-126">**свритемаск**</span><span class="sxs-lookup"><span data-stu-id="7d988-126">**swritemask**</span></span>               | [<span data-ttu-id="7d988-127">**глстенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="7d988-127">**glStencilMask**</span></span>](glstencilmask.md)                  | <span data-ttu-id="7d988-128">Указывает, какие биты набора элементов могут быть записаны.</span><span class="sxs-lookup"><span data-stu-id="7d988-128">Specifies which stencil bits can be written.</span></span>           |
|                              | [<span data-ttu-id="7d988-129">**глклеарстенЦил**</span><span class="sxs-lookup"><span data-stu-id="7d988-129">**glClearStencil**</span></span>](glclearstencil.md)                | <span data-ttu-id="7d988-130">Задает значение Clear для буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="7d988-130">Specifies the clear value for the stencil buffer.</span></span>      |
| <span data-ttu-id="7d988-131">**склеар**</span><span class="sxs-lookup"><span data-stu-id="7d988-131">**sclear**</span></span>                   | <span data-ttu-id="7d988-132">[**глклеар**](glclear.md) ( \_ \_ бит буфера шаблона GL \_ )</span><span class="sxs-lookup"><span data-stu-id="7d988-132">[**glClear**](glclear.md) ( GL\_STENCIL\_BUFFER\_BIT )</span></span> |                                                        |



 

<span data-ttu-id="7d988-133">Функции сравнения наборов элементов и операции успешного и неуспешного набора элементов почти эквивалентны в OpenGL и IRI GL.</span><span class="sxs-lookup"><span data-stu-id="7d988-133">Stencil-comparison functions and stencil pass/fail operations are nearly equivalent in OpenGL and IRIS GL.</span></span> <span data-ttu-id="7d988-134">Флаги функции трафарета IRI GL начинаются с «SF». Флаги OpenGL с GL.</span><span class="sxs-lookup"><span data-stu-id="7d988-134">The IRIS GL stencil-function flags are prefaced with SF; the OpenGL flags with GL.</span></span> <span data-ttu-id="7d988-135">Флаги операции "пройденные/неудачные" в IRI GL начинаются с ST; Флаги OpenGL с GL.</span><span class="sxs-lookup"><span data-stu-id="7d988-135">IRIS GL pass/fail operation flags are prefaced with ST; the OpenGL flags with GL.</span></span>

 

 




