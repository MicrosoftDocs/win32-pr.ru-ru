---
title: Группы атрибутов
description: Группы атрибутов
ms.assetid: 9fd7dc6e-6749-4e32-b795-21b63b64c291
keywords:
- OpenGL, группы атрибутов
- Справочник по OpenGL, группы атрибутов
- Справочник по OpenGL, группам атрибутов
- группы атрибутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d93582c8996438ad99d7bf896cf83bdf6fbf72d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672057"
---
# <a name="attribute-groups"></a><span data-ttu-id="96826-107">Группы атрибутов</span><span class="sxs-lookup"><span data-stu-id="96826-107">Attribute Groups</span></span>



| <span data-ttu-id="96826-108">Бит маски</span><span class="sxs-lookup"><span data-stu-id="96826-108">Mask bit</span></span>                  | <span data-ttu-id="96826-109">Группа атрибутов</span><span class="sxs-lookup"><span data-stu-id="96826-109">Attribute group</span></span> |
|---------------------------|-----------------|
| <span data-ttu-id="96826-110">\_бит накопленного \_ буфера GL \_</span><span class="sxs-lookup"><span data-stu-id="96826-110">GL\_ACCUM\_BUFFER\_BIT</span></span>    | <span data-ttu-id="96826-111">накопленный буфер</span><span class="sxs-lookup"><span data-stu-id="96826-111">accum-buffer</span></span>    |
| <span data-ttu-id="96826-112">\_все \_ атрибуты и \_ биты GL</span><span class="sxs-lookup"><span data-stu-id="96826-112">GL\_ALL\_ATTRIB\_BITS</span></span>     |                 |
| <span data-ttu-id="96826-113">\_ \_ бит буфера цвета \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-113">GL\_COLOR\_BUFFER\_BIT</span></span>    | <span data-ttu-id="96826-114">цветовой буфер</span><span class="sxs-lookup"><span data-stu-id="96826-114">color-buffer</span></span>    |
| <span data-ttu-id="96826-115">\_текущий \_ бит GL</span><span class="sxs-lookup"><span data-stu-id="96826-115">GL\_CURRENT\_BIT</span></span>          | <span data-ttu-id="96826-116">текущий</span><span class="sxs-lookup"><span data-stu-id="96826-116">current</span></span>         |
| <span data-ttu-id="96826-117">\_ \_ бит буфера глубины \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-117">GL\_DEPTH\_BUFFER\_BIT</span></span>    | <span data-ttu-id="96826-118">буфер глубины</span><span class="sxs-lookup"><span data-stu-id="96826-118">depth-buffer</span></span>    |
| <span data-ttu-id="96826-119">\_бит включения \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-119">GL\_ENABLE\_BIT</span></span>           | <span data-ttu-id="96826-120">enable</span><span class="sxs-lookup"><span data-stu-id="96826-120">enable</span></span>          |
| <span data-ttu-id="96826-121">\_бит оценки \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-121">GL\_EVAL\_BIT</span></span>             | <span data-ttu-id="96826-122">eval</span><span class="sxs-lookup"><span data-stu-id="96826-122">eval</span></span>            |
| <span data-ttu-id="96826-123">бит в главной системе \_ тумана \_</span><span class="sxs-lookup"><span data-stu-id="96826-123">GL\_FOG\_BIT</span></span>              | <span data-ttu-id="96826-124">туман</span><span class="sxs-lookup"><span data-stu-id="96826-124">fog</span></span>             |
| <span data-ttu-id="96826-125">бит указания GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="96826-125">GL\_HINT\_BIT</span></span>             | <span data-ttu-id="96826-126">подсказка</span><span class="sxs-lookup"><span data-stu-id="96826-126">hint</span></span>            |
| <span data-ttu-id="96826-127">\_бит освещения \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-127">GL\_LIGHTING\_BIT</span></span>         | <span data-ttu-id="96826-128">освещение;</span><span class="sxs-lookup"><span data-stu-id="96826-128">lighting</span></span>        |
| <span data-ttu-id="96826-129">\_бит строки \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-129">GL\_LINE\_BIT</span></span>             | <span data-ttu-id="96826-130">line</span><span class="sxs-lookup"><span data-stu-id="96826-130">line</span></span>            |
| <span data-ttu-id="96826-131">\_бит списка \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-131">GL\_LIST\_BIT</span></span>             | <span data-ttu-id="96826-132">list</span><span class="sxs-lookup"><span data-stu-id="96826-132">list</span></span>            |
| <span data-ttu-id="96826-133">\_ \_ бит режима "пиксель" в GL \_</span><span class="sxs-lookup"><span data-stu-id="96826-133">GL\_PIXEL\_MODE\_BIT</span></span>      | <span data-ttu-id="96826-134">пиксел</span><span class="sxs-lookup"><span data-stu-id="96826-134">pixel</span></span>           |
| <span data-ttu-id="96826-135">\_бит точки \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-135">GL\_POINT\_BIT</span></span>            | <span data-ttu-id="96826-136">point</span><span class="sxs-lookup"><span data-stu-id="96826-136">point</span></span>           |
| <span data-ttu-id="96826-137">бит GL для \_ многоугольника \_</span><span class="sxs-lookup"><span data-stu-id="96826-137">GL\_POLYGON\_BIT</span></span>          | <span data-ttu-id="96826-138">polygon</span><span class="sxs-lookup"><span data-stu-id="96826-138">polygon</span></span>         |
| <span data-ttu-id="96826-139">\_ \_ стипплеый БИТОВЫЙ многоугольник GL \_</span><span class="sxs-lookup"><span data-stu-id="96826-139">GL\_POLYGON\_STIPPLE\_BIT</span></span> | <span data-ttu-id="96826-140">многоугольник — стиппле</span><span class="sxs-lookup"><span data-stu-id="96826-140">polygon-stipple</span></span> |
| <span data-ttu-id="96826-141">\_бит вырезание GL \_</span><span class="sxs-lookup"><span data-stu-id="96826-141">GL\_SCISSOR\_BIT</span></span>          | <span data-ttu-id="96826-142">распашн</span><span class="sxs-lookup"><span data-stu-id="96826-142">scissor</span></span>         |
| <span data-ttu-id="96826-143">\_ \_ бит буфера шаблона \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-143">GL\_STENCIL\_BUFFER\_BIT</span></span>  | <span data-ttu-id="96826-144">набор элементов-буфер</span><span class="sxs-lookup"><span data-stu-id="96826-144">stencil-buffer</span></span>  |
| <span data-ttu-id="96826-145">\_бит текстуры \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-145">GL\_TEXTURE\_BIT</span></span>          | <span data-ttu-id="96826-146">текстура</span><span class="sxs-lookup"><span data-stu-id="96826-146">texture</span></span>         |
| <span data-ttu-id="96826-147">\_бит преобразования \_ GL</span><span class="sxs-lookup"><span data-stu-id="96826-147">GL\_TRANSFORM\_BIT</span></span>        | <span data-ttu-id="96826-148">преобразование</span><span class="sxs-lookup"><span data-stu-id="96826-148">transform</span></span>       |
| <span data-ttu-id="96826-149">\_бит окна просмотра GL \_</span><span class="sxs-lookup"><span data-stu-id="96826-149">GL\_VIEWPORT\_BIT</span></span>         | <span data-ttu-id="96826-150">окно просмотра</span><span class="sxs-lookup"><span data-stu-id="96826-150">viewport</span></span>        |



 

 

 




