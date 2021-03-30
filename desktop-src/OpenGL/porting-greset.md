---
title: Перенос гресет
description: OpenGL заменяет функцию IRI GL, гресет с помощью функций, Глпушаттриб и Глпопаттриб.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Перенос GL в ГК, переменные состояния
- Перенос из ДИАФРАГМы в ГК, переменные состояния
- перенос в OpenGL из IRI GL, переменные состояния
- Перенос по стандарту OpenGL из IRI GL, переменные состояния
- переменные состояния
- Перенос GL в ГК, функция гресет
- Перенос из IRI GL, функция гресет
- перенос в OpenGL из IRI GL, функция гресет
- Перенос по стандарту OpenGL из IRI GL, функция гресет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411131"
---
# <a name="porting-greset"></a><span data-ttu-id="01bc9-112">Перенос гресет</span><span class="sxs-lookup"><span data-stu-id="01bc9-112">Porting greset</span></span>

<span data-ttu-id="01bc9-113">OpenGL заменяет функцию IRI GL, **гресет** с помощью функций, [**глпушаттриб**](glpushattrib.md) и [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="01bc9-113">OpenGL replaces the IRIS GL function, **greset**, with the functions, [**glPushAttrib**](glpushattrib.md) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="01bc9-114">Эти функции используются для сохранения и восстановления групп переменных состояния.</span><span class="sxs-lookup"><span data-stu-id="01bc9-114">Use these functions to save and restore groups of state variables.</span></span> <span data-ttu-id="01bc9-115">Например,</span><span class="sxs-lookup"><span data-stu-id="01bc9-115">For example,</span></span>

``` syntax
void glPushAttrib( GLbitfield mask );
```

<span data-ttu-id="01bc9-116">Этот пример принимает побитовую или для символьных констант, указывая, какие группы переменных состояния следует отправить в стек атрибутов.</span><span class="sxs-lookup"><span data-stu-id="01bc9-116">This example takes a bitwise OR of symbolic constants, indicating which groups of state variables to push onto an attribute stack.</span></span> <span data-ttu-id="01bc9-117">Каждая константа ссылается на группу переменных состояния.</span><span class="sxs-lookup"><span data-stu-id="01bc9-117">Each constant refers to a group of state variables.</span></span> <span data-ttu-id="01bc9-118">В следующей таблице показаны группы атрибутов с эквивалентными именами символьных констант.</span><span class="sxs-lookup"><span data-stu-id="01bc9-118">The following table shows the attribute groups with their equivalent symbolic constant names.</span></span> <span data-ttu-id="01bc9-119">Полный список переменных состояния OpenGL, связанных с каждой константой, см. в разделе [**глпушаттриб**](glpushattrib.md).</span><span class="sxs-lookup"><span data-stu-id="01bc9-119">For a complete list of the OpenGL state variables associated with each constant, see [**glPushAttrib**](glpushattrib.md).</span></span>



| <span data-ttu-id="01bc9-120">attribute</span><span class="sxs-lookup"><span data-stu-id="01bc9-120">Attribute</span></span>                       | <span data-ttu-id="01bc9-121">Константа</span><span class="sxs-lookup"><span data-stu-id="01bc9-121">Constant</span></span>                  |
|---------------------------------|---------------------------|
| <span data-ttu-id="01bc9-122">очистить значение буфера накопления</span><span class="sxs-lookup"><span data-stu-id="01bc9-122">accumulation buffer clear value</span></span> | <span data-ttu-id="01bc9-123">\_бит накопленного \_ буфера GL \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-123">GL\_ACCUM\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="01bc9-124">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="01bc9-124">color buffer</span></span>                    | <span data-ttu-id="01bc9-125">\_ \_ бит буфера цвета \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-125">GL\_COLOR\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="01bc9-126">текущий</span><span class="sxs-lookup"><span data-stu-id="01bc9-126">current</span></span>                         | <span data-ttu-id="01bc9-127">\_текущий \_ бит GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-127">GL\_CURRENT\_BIT</span></span>          |
| <span data-ttu-id="01bc9-128">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="01bc9-128">depth buffer</span></span>                    | <span data-ttu-id="01bc9-129">\_ \_ бит буфера глубины \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-129">GL\_DEPTH\_BUFFER\_BIT</span></span>    |
| <span data-ttu-id="01bc9-130">enable</span><span class="sxs-lookup"><span data-stu-id="01bc9-130">enable</span></span>                          | <span data-ttu-id="01bc9-131">\_бит включения \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-131">GL\_ENABLE\_BIT</span></span>           |
| <span data-ttu-id="01bc9-132">оценивающих</span><span class="sxs-lookup"><span data-stu-id="01bc9-132">evaluators</span></span>                      | <span data-ttu-id="01bc9-133">\_бит EGL Val \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-133">EGL\_VAL\_BIT</span></span>             |
| <span data-ttu-id="01bc9-134">туман</span><span class="sxs-lookup"><span data-stu-id="01bc9-134">fog</span></span>                             | <span data-ttu-id="01bc9-135">бит в главной системе \_ тумана \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-135">GL\_FOG\_BIT</span></span>              |
| <span data-ttu-id="01bc9-136">\_ \_ Базовый параметр списка GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-136">GL\_LIST\_BASE setting</span></span>          | <span data-ttu-id="01bc9-137">\_бит списка \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-137">GL\_LIST\_BIT</span></span>             |
| <span data-ttu-id="01bc9-138">Указание переменных</span><span class="sxs-lookup"><span data-stu-id="01bc9-138">hint variables</span></span>                  | <span data-ttu-id="01bc9-139">бит указания GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-139">GL\_HINT\_BIT</span></span>             |
| <span data-ttu-id="01bc9-140">переменные освещения</span><span class="sxs-lookup"><span data-stu-id="01bc9-140">lighting variables</span></span>              | <span data-ttu-id="01bc9-141">\_бит освещения \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-141">GL\_LIGHTING\_BIT</span></span>         |
| <span data-ttu-id="01bc9-142">режим рисования линий</span><span class="sxs-lookup"><span data-stu-id="01bc9-142">line drawing mode</span></span>               | <span data-ttu-id="01bc9-143">\_бит строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-143">GL\_LINE\_BIT</span></span>             |
| <span data-ttu-id="01bc9-144">переменные режима пикселей</span><span class="sxs-lookup"><span data-stu-id="01bc9-144">pixel mode variables</span></span>            | <span data-ttu-id="01bc9-145">\_ \_ бит режима "пиксель" в GL \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-145">GL\_PIXEL\_MODE\_BIT</span></span>      |
| <span data-ttu-id="01bc9-146">переменные Point</span><span class="sxs-lookup"><span data-stu-id="01bc9-146">point variables</span></span>                 | <span data-ttu-id="01bc9-147">\_бит точки \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-147">GL\_POINT\_BIT</span></span>            |
| <span data-ttu-id="01bc9-148">polygon</span><span class="sxs-lookup"><span data-stu-id="01bc9-148">polygon</span></span>                         | <span data-ttu-id="01bc9-149">бит GL для \_ многоугольника \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-149">GL\_POLYGON\_BIT</span></span>          |
| <span data-ttu-id="01bc9-150">многоугольник стиппле</span><span class="sxs-lookup"><span data-stu-id="01bc9-150">polygon stipple</span></span>                 | <span data-ttu-id="01bc9-151">\_ \_ стипплеый БИТОВЫЙ многоугольник GL \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-151">GL\_POLYGON\_STIPPLE\_BIT</span></span> |
| <span data-ttu-id="01bc9-152">распашн</span><span class="sxs-lookup"><span data-stu-id="01bc9-152">scissor</span></span>                         | <span data-ttu-id="01bc9-153">\_бит вырезание GL \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-153">GL\_SCISSOR\_BIT</span></span>          |
| <span data-ttu-id="01bc9-154">буфер набора элементов</span><span class="sxs-lookup"><span data-stu-id="01bc9-154">stencil buffer</span></span>                  | <span data-ttu-id="01bc9-155">\_ \_ бит буфера шаблона \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-155">GL\_STENCIL\_BUFFER\_BIT</span></span>  |
| <span data-ttu-id="01bc9-156">текстура</span><span class="sxs-lookup"><span data-stu-id="01bc9-156">texture</span></span>                         | <span data-ttu-id="01bc9-157">\_бит текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-157">GL\_TEXTURE\_BIT</span></span>          |
| <span data-ttu-id="01bc9-158">преобразование</span><span class="sxs-lookup"><span data-stu-id="01bc9-158">transform</span></span>                       | <span data-ttu-id="01bc9-159">\_бит преобразования \_ GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-159">GL\_TRANSFORM\_BIT</span></span>        |
| <span data-ttu-id="01bc9-160">окно просмотра</span><span class="sxs-lookup"><span data-stu-id="01bc9-160">viewport</span></span>                        | <span data-ttu-id="01bc9-161">\_бит окна просмотра GL \_</span><span class="sxs-lookup"><span data-stu-id="01bc9-161">GL\_VIEWPORT\_BIT</span></span>         |
|                                 | <span data-ttu-id="01bc9-162">\_все \_ атрибуты и \_ биты GL</span><span class="sxs-lookup"><span data-stu-id="01bc9-162">GL\_ALL\_ATTRIB\_BITS</span></span>     |



 

<span data-ttu-id="01bc9-163">Чтобы восстановить значения переменных состояния, сохраненные с последним [**глпушаттриб**](glpushattrib.md), просто вызовите [**глпопаттриб**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="01bc9-163">To restore the values of the state variables to those saved with the last [**glPushAttrib**](glpushattrib.md), simply call [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="01bc9-164">Переменные, которые вы не сохраняли, останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="01bc9-164">The variables you didn't save will remain unchanged.</span></span> <span data-ttu-id="01bc9-165">Конечная глубина стека атрибутов не меньше 16.</span><span class="sxs-lookup"><span data-stu-id="01bc9-165">The attribute stack has a finite depth of at least 16.</span></span>

 

 




