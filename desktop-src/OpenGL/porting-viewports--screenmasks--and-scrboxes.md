---
title: Перенос окна просмотра, Скринмаскс и Скрбоксес
description: Следующие функции окна просмотра IRI GL не имеют эквивалента OpenGL
ms.assetid: 223e9b5b-1ddd-45a6-8489-b262d0207a5a
keywords:
- Перенос GL в ГК, функции окна просмотра
- Перенос из IRI GL, функции окна просмотра
- перенос в OpenGL из IRI GL, функции окна просмотра
- Перенос по стандарту OpenGL из IRI GL, функции окна просмотра
- функции окна просмотра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b3429a0d154f4ef62a12d767c6497099ac09751
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661527"
---
# <a name="porting-viewports-screenmasks-and-scrboxes"></a><span data-ttu-id="a81b6-108">Перенос окна просмотра, Скринмаскс и Скрбоксес</span><span class="sxs-lookup"><span data-stu-id="a81b6-108">Porting Viewports, Screenmasks, and Scrboxes</span></span>

<span data-ttu-id="a81b6-109">Следующие функции окна просмотра IRI GL не имеют эквивалента OpenGL:</span><span class="sxs-lookup"><span data-stu-id="a81b6-109">The following IRIS GL viewport functions have no OpenGL equivalent:</span></span>

-   <span data-ttu-id="a81b6-110">**решапевиевпорт**</span><span class="sxs-lookup"><span data-stu-id="a81b6-110">**reshapeviewport**</span></span>
-   <span data-ttu-id="a81b6-111">**скрбокс**</span><span class="sxs-lookup"><span data-stu-id="a81b6-111">**scrbox**</span></span>
-   <span data-ttu-id="a81b6-112">**жетскрбокс**</span><span class="sxs-lookup"><span data-stu-id="a81b6-112">**getscrbox**</span></span>

<span data-ttu-id="a81b6-113">С помощью функции **просмотра** IRI GL вы указываете координаты x (в пикселях) слева и справа от прямоугольника просмотра и координаты y для верхней и нижней части.</span><span class="sxs-lookup"><span data-stu-id="a81b6-113">With the IRIS GL **viewport** function, you specify the x coordinates (in pixels) for the left and right of a viewport rectangle and the y coordinates for the top and bottom.</span></span> <span data-ttu-id="a81b6-114">Однако с помощью функции OpenGL [**глвиевпорт**](glviewport.md) вы указываете координаты x и y (в пикселях) левого нижнего угла прямоугольника окна просмотра, а также его ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="a81b6-114">With the OpenGL [**glViewport**](glviewport.md) function, however, you specify the x and y coordinates (in pixels) of the lower-left corner of the viewport rectangle along with its width and height.</span></span>

<span data-ttu-id="a81b6-115">В следующей таблице перечислены функции окна просмотра IRI GL и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a81b6-115">The following table lists IRIS GL viewport functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a81b6-116">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="a81b6-116">IRIS GL function</span></span>                          | <span data-ttu-id="a81b6-117">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="a81b6-117">OpenGL function</span></span>                                                                                         | <span data-ttu-id="a81b6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="a81b6-118">Meaning</span></span>                      |
|-------------------------------------------|---------------------------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="a81b6-119">**окно просмотра** (слева, справа, снизу, сверху)</span><span class="sxs-lookup"><span data-stu-id="a81b6-119">**viewport** ( left, right, bottom, top )</span></span> | <span data-ttu-id="a81b6-120">[**глвиевпорт**](glviewport.md) (x, y, ширина, высота)</span><span class="sxs-lookup"><span data-stu-id="a81b6-120">[**glViewport**](glviewport.md) ( x, y, width, height )</span></span>                                                | <span data-ttu-id="a81b6-121">Задает окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="a81b6-121">Sets the viewport.</span></span>           |
| <span data-ttu-id="a81b6-122">**попвиевпортпушвиевпорт**</span><span class="sxs-lookup"><span data-stu-id="a81b6-122">**popviewportpushviewport**</span></span><br/>    | <span data-ttu-id="a81b6-123">[**глпопаттриб**](glpopattrib.md)[**глпушаттриб**](glpushattrib.md) ( \_ бит окна просмотра GL \_ )</span><span class="sxs-lookup"><span data-stu-id="a81b6-123">[**glPopAttrib**](glpopattrib.md)[**glPushAttrib**](glpushattrib.md) ( GL\_VIEWPORT\_BIT )</span></span><br/> | <span data-ttu-id="a81b6-124">Отправляет и выводит стек.</span><span class="sxs-lookup"><span data-stu-id="a81b6-124">Pushes and pops the stack.</span></span>   |
| <span data-ttu-id="a81b6-125">**окно просмотра**</span><span class="sxs-lookup"><span data-stu-id="a81b6-125">**getviewport**</span></span>                           | <span data-ttu-id="a81b6-126">[**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( \_ окно просмотра GL)</span><span class="sxs-lookup"><span data-stu-id="a81b6-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ( GL\_VIEWPORT )</span></span>               | <span data-ttu-id="a81b6-127">Возвращает размеры окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="a81b6-127">Returns viewport dimensions.</span></span> |



 

<span data-ttu-id="a81b6-128">??</span><span class="sxs-lookup"><span data-stu-id="a81b6-128">??</span></span>

 

 





