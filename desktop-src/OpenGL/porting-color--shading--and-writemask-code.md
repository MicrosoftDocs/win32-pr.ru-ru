---
title: Перенос цвета, заливки и кода Вритемаск
description: Перенос цвета, заливки и кода Вритемаск
ms.assetid: ffcf33b2-c3b8-4e89-9c2f-085b98cbb496
keywords:
- Перенос GL по IRI, цвет
- Перенос из IRI GL, цвет
- перенос в OpenGL из IRI GL, цвет
- Перенос по стандарту OpenGL из IRI GL, цвет
- Перенос GL по IRI, заливка
- Перенос из ДИАФРАГМы в ГК, заливка
- перенос в OpenGL из IRI GL, заливка
- Перенос по стандарту OpenGL из IRI GL, заливка
- Перенос GL в ГК, вритемаск
- Перенос из IRI GL, вритемаск
- перенос в OpenGL из IRI GL, вритемаск
- Перенос по стандарту OpenGL из IRI GL, вритемаск
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f8bc35986bc0f9d7076411fecbd9c1fa5d7bfbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774003"
---
# <a name="porting-color-shading-and-writemask-code"></a><span data-ttu-id="1e89a-115">Перенос цвета, заливки и кода Вритемаск</span><span class="sxs-lookup"><span data-stu-id="1e89a-115">Porting Color, Shading, and Writemask Code</span></span>

<span data-ttu-id="1e89a-116">При переносе цвета, заливки и вритемаск кода в OpenGL учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="1e89a-116">When porting color, shading, and writemask code to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="1e89a-117">Хотя индексы цветовой схемы можно задать с помощью функции OpenGL [глиндекс](glindex-functions.md) , OpenGL не имеет функции для загрузки индексов цветовой схемы.</span><span class="sxs-lookup"><span data-stu-id="1e89a-117">Though you can set color-map indexes with the OpenGL [glIndex](glindex-functions.md) function, OpenGL does not have a function for loading color-map indexes.</span></span>
-   <span data-ttu-id="1e89a-118">Значения цвета нормализуются к типу данных.</span><span class="sxs-lookup"><span data-stu-id="1e89a-118">Color values are normalized to their data type.</span></span> <span data-ttu-id="1e89a-119">(Дополнительные сведения о цветовых значениях см. в разделе [глколор](glcolor-functions.md)).</span><span class="sxs-lookup"><span data-stu-id="1e89a-119">(For information about color values, see [glColor](glcolor-functions.md)).</span></span>
-   <span data-ttu-id="1e89a-120">Простого эквивалента для **кпакк** не существует.</span><span class="sxs-lookup"><span data-stu-id="1e89a-120">There is no simple equivalent for **cpack**.</span></span>
-   <span data-ttu-id="1e89a-121">Может потребоваться перевести код, включающий функции **c** или **Color** , в [**глклеарколор**](glclearcolor.md) или [**глклеариндекс**](glclearindex.md) вместо **глколор** или **глиндекс**.</span><span class="sxs-lookup"><span data-stu-id="1e89a-121">You may have to translate code that includes the **c** or **color** functions to [**glClearColor**](glclearcolor.md) or [**glClearIndex**](glclearindex.md) instead of **glColor** or **glIndex**.</span></span>
-   <span data-ttu-id="1e89a-122">Вритемаск RGBA применяется к каждому компоненту, но не для каждого бита.</span><span class="sxs-lookup"><span data-stu-id="1e89a-122">The RGBA writemask applies to each component but not for each bit.</span></span>
-   <span data-ttu-id="1e89a-123">IRI GL предоставляет определенные константы цвета: черный, синий, красный, зеленый, пурпурный, голубой, желтый и белый.</span><span class="sxs-lookup"><span data-stu-id="1e89a-123">IRIS GL provides defined color constants: BLACK, BLUE, RED, GREEN, MAGENTA, CYAN, YELLOW, and WHITE.</span></span> <span data-ttu-id="1e89a-124">OpenGL не предоставляет эти константы.</span><span class="sxs-lookup"><span data-stu-id="1e89a-124">OpenGL does not provide these constants.</span></span>

<span data-ttu-id="1e89a-125">Этот раздел содержит сведения о следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="1e89a-125">This topic includes information on the following.</span></span>

-   [<span data-ttu-id="1e89a-126">Перенос цветовых вызовов</span><span class="sxs-lookup"><span data-stu-id="1e89a-126">Porting Color Calls</span></span>](porting-color-calls.md)
-   [<span data-ttu-id="1e89a-127">Перенос моделей заливки</span><span class="sxs-lookup"><span data-stu-id="1e89a-127">Porting Shading Models</span></span>](porting-shading-models.md)

 

 




