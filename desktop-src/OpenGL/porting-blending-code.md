---
title: Перенос кода смешения
description: В IRI GL при рисовании как на передний, так и в задний буферах смешивание выполняется путем считывания одного из буферов, смешивания с этим цветом и последующей записи результата в оба буфера. Однако в OpenGL каждый буфер считывается в свою очередь, смешивается, а затем записывается.
ms.assetid: 18334c6b-586d-44a3-aa95-d10589ba99f4
keywords:
- Перенос GL по модулю IRI, смешивание
- Перенос из ДИАФРАГМы в ГК, смешивание
- перенос в OpenGL из IRI GL, смешивание
- Перенос по стандарту OpenGL из IRI GL, смешивание
- смешение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7956c675848f454b660126a7a17869295a827438
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661625"
---
# <a name="porting-blending-code"></a><span data-ttu-id="db81e-109">Перенос кода смешения</span><span class="sxs-lookup"><span data-stu-id="db81e-109">Porting Blending Code</span></span>

<span data-ttu-id="db81e-110">В IRI GL при рисовании как на передний, так и в задний буферах смешивание выполняется путем считывания одного из буферов, смешивания с этим цветом и последующей записи результата в оба буфера.</span><span class="sxs-lookup"><span data-stu-id="db81e-110">In IRIS GL, when drawing to both front and back buffers, blending is done by reading one of the buffers, blending with that color, and then writing the result to both buffers.</span></span> <span data-ttu-id="db81e-111">Однако в OpenGL каждый буфер считывается в свою очередь, смешивается, а затем записывается.</span><span class="sxs-lookup"><span data-stu-id="db81e-111">In OpenGL, however, each buffer is read in turn, blended, and then written.</span></span>

<span data-ttu-id="db81e-112">В следующей таблице перечислены функции смешения наложения IRI и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="db81e-112">The following table lists IRIS GL blending functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="db81e-113">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="db81e-113">IRIS GL function</span></span>  | <span data-ttu-id="db81e-114">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="db81e-114">OpenGL function</span></span>                            | <span data-ttu-id="db81e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="db81e-115">Meaning</span></span>                     |
|-------------------|--------------------------------------------|-----------------------------|
|                   | <span data-ttu-id="db81e-116">[**гленабле**](glenable.md) (ГК \_ Blend)</span><span class="sxs-lookup"><span data-stu-id="db81e-116">[**glEnable**](glenable.md) ( GL\_BLEND )</span></span> | <span data-ttu-id="db81e-117">Включает смешение.</span><span class="sxs-lookup"><span data-stu-id="db81e-117">Turns on blending.</span></span>          |
| <span data-ttu-id="db81e-118">**блендфунктион**</span><span class="sxs-lookup"><span data-stu-id="db81e-118">**blendfunction**</span></span> | [<span data-ttu-id="db81e-119">**глблендфунк**</span><span class="sxs-lookup"><span data-stu-id="db81e-119">**glBlendFunc**</span></span>](glblendfunc.md)         | <span data-ttu-id="db81e-120">Задает функцию Blend.</span><span class="sxs-lookup"><span data-stu-id="db81e-120">Specifies a blend function.</span></span> |



 

<span data-ttu-id="db81e-121">Функция OpenGL **глблендфунк** и функция IRI GL **блендфунктион** практически идентичны.</span><span class="sxs-lookup"><span data-stu-id="db81e-121">The OpenGL **glBlendFunc** function and the IRIS GL **blendfunction** function are almost identical.</span></span> <span data-ttu-id="db81e-122">В следующей таблице перечислены Коэффициенты смешения и их эквиваленты OpenGL для ДИАФРАГМы.</span><span class="sxs-lookup"><span data-stu-id="db81e-122">The following table lists IRIS GL blend factors and their OpenGL equivalents.</span></span>



| <span data-ttu-id="db81e-123">IRI GL</span><span class="sxs-lookup"><span data-stu-id="db81e-123">IRIS GL</span></span>          | <span data-ttu-id="db81e-124">OpenGL</span><span class="sxs-lookup"><span data-stu-id="db81e-124">OpenGL</span></span>                     | <span data-ttu-id="db81e-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="db81e-125">Notes</span></span>             |
|------------------|----------------------------|-------------------|
| <span data-ttu-id="db81e-126">BF \_ 0</span><span class="sxs-lookup"><span data-stu-id="db81e-126">BF\_ZERO</span></span>         | <span data-ttu-id="db81e-127">ноль в ГК \_</span><span class="sxs-lookup"><span data-stu-id="db81e-127">GL\_ZERO</span></span>                   |                   |
| <span data-ttu-id="db81e-128">BF \_ один</span><span class="sxs-lookup"><span data-stu-id="db81e-128">BF\_ONE</span></span>          | <span data-ttu-id="db81e-129">\_один GL</span><span class="sxs-lookup"><span data-stu-id="db81e-129">GL\_ONE</span></span>                    |                   |
| <span data-ttu-id="db81e-130">BF \_ SA</span><span class="sxs-lookup"><span data-stu-id="db81e-130">BF\_SA</span></span>           | <span data-ttu-id="db81e-131">\_альфа- \_ канал ГК src</span><span class="sxs-lookup"><span data-stu-id="db81e-131">GL\_SRC\_ALPHA</span></span>             |                   |
| <span data-ttu-id="db81e-132">BF \_ MSA</span><span class="sxs-lookup"><span data-stu-id="db81e-132">BF\_MSA</span></span>          | <span data-ttu-id="db81e-133">1-я, ГК, \_ один \_ минус \_ \_ альфа</span><span class="sxs-lookup"><span data-stu-id="db81e-133">GL\_ONE\_MINUS\_SRC\_ALPHA</span></span> |                   |
| <span data-ttu-id="db81e-134">BF \_ Da</span><span class="sxs-lookup"><span data-stu-id="db81e-134">BF\_DA</span></span>           | <span data-ttu-id="db81e-135">\_альфа- \_ канал летнего времени</span><span class="sxs-lookup"><span data-stu-id="db81e-135">GL\_DST\_ALPHA</span></span>             |                   |
| <span data-ttu-id="db81e-136">BF \_ MDA</span><span class="sxs-lookup"><span data-stu-id="db81e-136">BF\_MDA</span></span>          | <span data-ttu-id="db81e-137">ГК \_ 1 \_ минус \_ альфа-летнее \_</span><span class="sxs-lookup"><span data-stu-id="db81e-137">GL\_ONE\_MINUS\_DST\_ALPHA</span></span> |                   |
| <span data-ttu-id="db81e-138">BF \_ SC</span><span class="sxs-lookup"><span data-stu-id="db81e-138">BF\_SC</span></span>           | <span data-ttu-id="db81e-139">\_Цвет src в GL \_</span><span class="sxs-lookup"><span data-stu-id="db81e-139">GL\_SRC\_COLOR</span></span>             |                   |
| <span data-ttu-id="db81e-140">BF \_ MSC</span><span class="sxs-lookup"><span data-stu-id="db81e-140">BF\_MSC</span></span>          | <span data-ttu-id="db81e-141">\_Цвет источника \_ "один за минус" \_ \_</span><span class="sxs-lookup"><span data-stu-id="db81e-141">GL\_ONE\_MINUS\_SRC\_COLOR</span></span> | <span data-ttu-id="db81e-142">Только назначение.</span><span class="sxs-lookup"><span data-stu-id="db81e-142">Destination only.</span></span> |
| <span data-ttu-id="db81e-143">BF \_ DC</span><span class="sxs-lookup"><span data-stu-id="db81e-143">BF\_DC</span></span>           | <span data-ttu-id="db81e-144">\_Цвет летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="db81e-144">GL\_DST\_COLOR</span></span>             | <span data-ttu-id="db81e-145">Только источник.</span><span class="sxs-lookup"><span data-stu-id="db81e-145">Source only.</span></span>      |
| <span data-ttu-id="db81e-146">BF \_ MDC</span><span class="sxs-lookup"><span data-stu-id="db81e-146">BF\_MDC</span></span>          | <span data-ttu-id="db81e-147">\_один и тот же \_ \_ Цвет периода летнего времени \_</span><span class="sxs-lookup"><span data-stu-id="db81e-147">GL\_ONE\_MINUS\_DST\_COLOR</span></span> | <span data-ttu-id="db81e-148">Только источник.</span><span class="sxs-lookup"><span data-stu-id="db81e-148">Source only.</span></span>      |
| <span data-ttu-id="db81e-149">BF \_ min \_ SA \_ MDA</span><span class="sxs-lookup"><span data-stu-id="db81e-149">BF\_MIN\_SA\_MDA</span></span> | <span data-ttu-id="db81e-150">\_альфа- \_ канал ИСХОДНОГО \_ сегмента GL</span><span class="sxs-lookup"><span data-stu-id="db81e-150">GL\_SRC\_ALPHA\_SATURATE</span></span>   |                   |



 

<span data-ttu-id="db81e-151">??</span><span class="sxs-lookup"><span data-stu-id="db81e-151">??</span></span>

 

 




