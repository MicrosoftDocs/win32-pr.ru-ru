---
title: Перенос функций комплектации
description: Все функции комплектации IRI GL имеют эквиваленты OpenGL, за исключением клеархиткоде. В следующей таблице перечислены функции комплектации IRI GL и их эквивалентные функции OpenGL.
ms.assetid: f8fbd0c2-14bf-47bc-be7f-eeef346dbac1
keywords:
- Перенос по ГК IRI, комплектация
- Перенос из IRI GL, комплектация
- Перенос на OpenGL из IRI GL, комплектация
- Перенос по стандарту OpenGL из IRI GL, комплектация
- сортировк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db4c0ea6011860f7d5010dd0bb7d5d23b671d99a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661599"
---
# <a name="porting-picking-functions"></a><span data-ttu-id="1e44d-109">Перенос функций комплектации</span><span class="sxs-lookup"><span data-stu-id="1e44d-109">Porting Picking Functions</span></span>

<span data-ttu-id="1e44d-110">Все функции комплектации IRI GL имеют эквиваленты OpenGL, за исключением **клеархиткоде**.</span><span class="sxs-lookup"><span data-stu-id="1e44d-110">All IRIS GL picking functions have OpenGL equivalents, with the exception of **clearhitcode**.</span></span> <span data-ttu-id="1e44d-111">В следующей таблице перечислены функции комплектации IRI GL и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1e44d-111">The following table lists the IRIS GL picking functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="1e44d-112">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="1e44d-112">IRIS GL function</span></span>                | <span data-ttu-id="1e44d-113">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="1e44d-113">OpenGL function</span></span>                                                                           | <span data-ttu-id="1e44d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1e44d-114">Meaning</span></span>                                |
|---------------------------------|-------------------------------------------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="1e44d-115">**клеархиткоде**</span><span class="sxs-lookup"><span data-stu-id="1e44d-115">**clearhitcode**</span></span>                | <span data-ttu-id="1e44d-116">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1e44d-116">Not supported.</span></span>                                                                            | <span data-ttu-id="1e44d-117">Очищает глобальную переменную и хиткоде.</span><span class="sxs-lookup"><span data-stu-id="1e44d-117">Clears global variable and hitcode.</span></span>    |
| <span data-ttu-id="1e44d-118">**пиккселект**</span><span class="sxs-lookup"><span data-stu-id="1e44d-118">**pickselect**</span></span><br/>       | <span data-ttu-id="1e44d-119">[**глрендермоде**](glrendermode.md) ( \_ Выбор GL)</span><span class="sxs-lookup"><span data-stu-id="1e44d-119">[**glRenderMode**](glrendermode.md) ( GL\_SELECT )</span></span>                                       | <span data-ttu-id="1e44d-120">Переключается в режим выбора или подбора.</span><span class="sxs-lookup"><span data-stu-id="1e44d-120">Switches to selection or picking mode.</span></span> |
| <span data-ttu-id="1e44d-121">**ендпиккендселект**</span><span class="sxs-lookup"><span data-stu-id="1e44d-121">**endpickendselect**</span></span><br/> | <span data-ttu-id="1e44d-122">[**глрендермоде**](glrendermode.md) ( \_ рендеринг GL)</span><span class="sxs-lookup"><span data-stu-id="1e44d-122">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )</span></span>                                       | <span data-ttu-id="1e44d-123">Переключается в режим рендеринга.</span><span class="sxs-lookup"><span data-stu-id="1e44d-123">Switches to rendering mode.</span></span>            |
| <span data-ttu-id="1e44d-124">**пикксизе**</span><span class="sxs-lookup"><span data-stu-id="1e44d-124">**picksize**</span></span>                    | <span data-ttu-id="1e44d-125">[**глупиккматрикс**](glupickmatrix.md)[**глселектбуффер**](glselectbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="1e44d-125">[**gluPickMatrix**](glupickmatrix.md)[**glSelectBuffer**](glselectbuffer.md)</span></span><br/> | <span data-ttu-id="1e44d-126">Задает возвращаемый массив.</span><span class="sxs-lookup"><span data-stu-id="1e44d-126">Sets the return array.</span></span>                 |
| <span data-ttu-id="1e44d-127">**инитнамес**</span><span class="sxs-lookup"><span data-stu-id="1e44d-127">**initnames**</span></span>                   | [<span data-ttu-id="1e44d-128">**глинитнамес**</span><span class="sxs-lookup"><span data-stu-id="1e44d-128">**glInitNames**</span></span>](glinitnames.md)                                                        |                                        |
| <span data-ttu-id="1e44d-129">**пушнамепопнаме**</span><span class="sxs-lookup"><span data-stu-id="1e44d-129">**pushnamepopname**</span></span><br/>  | <span data-ttu-id="1e44d-130">[**глпушнаме**](glpushname.md)[**глпопнаме**](glpopname.md)</span><span class="sxs-lookup"><span data-stu-id="1e44d-130">[**glPushName**](glpushname.md)[**glPopName**](glpopname.md)</span></span><br/>                 |                                        |
| <span data-ttu-id="1e44d-131">**лоаднаме**</span><span class="sxs-lookup"><span data-stu-id="1e44d-131">**loadname**</span></span>                    | [<span data-ttu-id="1e44d-132">**гллоаднаме**</span><span class="sxs-lookup"><span data-stu-id="1e44d-132">**glLoadName**</span></span>](glloadname.md)                                                          |                                        |



 

<span data-ttu-id="1e44d-133">Дополнительные сведения о комплектации см. в разделе [**глупиккматрикс**](glupickmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="1e44d-133">For more information on picking, see [**gluPickMatrix**](glupickmatrix.md).</span></span>

 

 





