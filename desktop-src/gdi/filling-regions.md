---
description: Приложение заполняет внутреннюю часть области путем вызова функции Филлргн и предоставления дескриптора, идентифицирующего определенную кисть.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Заполнение регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080496"
---
# <a name="filling-regions"></a><span data-ttu-id="f5275-103">Заполнение регионов</span><span class="sxs-lookup"><span data-stu-id="f5275-103">Filling Regions</span></span>

<span data-ttu-id="f5275-104">Приложение заполняет внутреннюю часть области путем вызова функции [**филлргн**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) и предоставления дескриптора, идентифицирующего определенную кисть.</span><span class="sxs-lookup"><span data-stu-id="f5275-104">An application fills the interior of a region by calling the [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) function and supplying a handle that identifies a specific brush.</span></span> <span data-ttu-id="f5275-105">Когда приложение вызывает Филлргн, система заполняет область кистью, используя текущий режим заполнения для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="f5275-105">When an application calls FillRgn , the system fills the region with the brush by using the current fill mode for the specified device context.</span></span> <span data-ttu-id="f5275-106">Существует два режима заливки: чередование и обмотка.</span><span class="sxs-lookup"><span data-stu-id="f5275-106">There are two fill modes: alternate and winding.</span></span> <span data-ttu-id="f5275-107">Приложение может задать режим заполнения для контекста устройства, вызвав функцию [**сетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="f5275-107">The application can set the fill mode for a device context by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="f5275-108">Приложение может получить текущий режим заполнения для контекста устройства, вызвав функцию [**жетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="f5275-108">The application can retrieve the current fill mode for a device context by calling the [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) function.</span></span>

<span data-ttu-id="f5275-109">На следующем рисунке показаны два одинаковых региона: один заполнен с использованием альтернативного режима и другой заполненный режим поворота.</span><span class="sxs-lookup"><span data-stu-id="f5275-109">The following illustration shows two identical regions: one filled using alternate mode and the other filled using winding mode.</span></span>

![Иллюстрация, показывающая 2 5 на звездах: одна заполнена только точками, другая заполненная полностью](images/csrgn-03.png)

## <a name="alternate-mode"></a><span data-ttu-id="f5275-111">Альтернативный режим</span><span class="sxs-lookup"><span data-stu-id="f5275-111">Alternate Mode</span></span>

<span data-ttu-id="f5275-112">Чтобы определить, какие пиксели выделяются системой при указании альтернативного режима, выполните следующий тест:</span><span class="sxs-lookup"><span data-stu-id="f5275-112">To determine which pixels the system highlights when alternate mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="f5275-113">Выберите пиксель внутри внутренней области.</span><span class="sxs-lookup"><span data-stu-id="f5275-113">Select a pixel within the region's interior.</span></span>
2.  <span data-ttu-id="f5275-114">Нарисуйте воображаемый луч в положительном направлении x от этого пикселя до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="f5275-114">Draw an imaginary ray, in the positive x-direction, from that pixel toward infinity.</span></span>
3.  <span data-ttu-id="f5275-115">Каждый раз, когда луч пересекает линию границы, увеличивает значение Count.</span><span class="sxs-lookup"><span data-stu-id="f5275-115">Each time the ray intersects a boundary line, increment a count value.</span></span>

<span data-ttu-id="f5275-116">Система выделяет пиксель, если значение Count является нечетным числом.</span><span class="sxs-lookup"><span data-stu-id="f5275-116">The system highlights the pixel if the count value is an odd number.</span></span>

## <a name="winding-mode"></a><span data-ttu-id="f5275-117">Режим поворота</span><span class="sxs-lookup"><span data-stu-id="f5275-117">Winding Mode</span></span>

<span data-ttu-id="f5275-118">Чтобы определить, какие пиксели выделяются системой при указании режима поворота, выполните следующий тест:</span><span class="sxs-lookup"><span data-stu-id="f5275-118">To determine which pixels the system highlights when winding mode is specified, perform the following test:</span></span>

1.  <span data-ttu-id="f5275-119">Определите направление, в котором рисуется каждая линия границы.</span><span class="sxs-lookup"><span data-stu-id="f5275-119">Determine the direction in which each boundary line is drawn.</span></span>
2.  <span data-ttu-id="f5275-120">Выберите пиксель внутри внутренней области.</span><span class="sxs-lookup"><span data-stu-id="f5275-120">Select a pixel within the region's interior.</span></span>
3.  <span data-ttu-id="f5275-121">Рисование мнимого луча в положительном направлении по оси x от точки до бесконечности.</span><span class="sxs-lookup"><span data-stu-id="f5275-121">Draw an imaginary ray, in the positive x-direction, from the pixel toward infinity.</span></span>
4.  <span data-ttu-id="f5275-122">Каждый раз, когда луч пересекает линию границы с положительным компонентом y, увеличивает значение счетчика.</span><span class="sxs-lookup"><span data-stu-id="f5275-122">Each time the ray intersects a boundary line with a positive y-component, increment a count value.</span></span> <span data-ttu-id="f5275-123">Каждый раз, когда луч пересекает линию границы с отрицательным компонентом y, уменьшает значение Count.</span><span class="sxs-lookup"><span data-stu-id="f5275-123">Each time the ray intersects a boundary line with a negative y-component, decrement the count value.</span></span>

<span data-ttu-id="f5275-124">Система выделяет пиксель, если значение счетчика не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="f5275-124">The system highlights the pixel if the count value is nonzero.</span></span>

 

 



