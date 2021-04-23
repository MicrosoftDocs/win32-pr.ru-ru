---
description: Многоугольник — это заполненная фигура с прямыми сторонами.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: О многоугольниках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080509"
---
# <a name="about-polygons"></a><span data-ttu-id="2eded-103">О многоугольниках</span><span class="sxs-lookup"><span data-stu-id="2eded-103">About Polygons</span></span>

<span data-ttu-id="2eded-104">*Многоугольник* — это заполненная фигура с прямыми сторонами.</span><span class="sxs-lookup"><span data-stu-id="2eded-104">A *polygon* is a filled shape with straight sides.</span></span> <span data-ttu-id="2eded-105">Стороны многоугольника рисуются с помощью текущего пера.</span><span class="sxs-lookup"><span data-stu-id="2eded-105">The sides of a polygon are drawn by using the current pen.</span></span> <span data-ttu-id="2eded-106">Когда система заполняет многоугольник, она использует текущую кисть и режим заливки текущего многоугольника.</span><span class="sxs-lookup"><span data-stu-id="2eded-106">When the system fills a polygon, it uses the current brush and the current polygon fill mode.</span></span> <span data-ttu-id="2eded-107">Два режима заливки, альтернативный (по умолчанию) и обмотка, определяют, будут ли регионы внутри составного многоугольника заполнены или оставлены нерисованными.</span><span class="sxs-lookup"><span data-stu-id="2eded-107">The two fill modes, alternate (the default) and winding, determine whether regions within a complex polygon are filled or left unpainted.</span></span> <span data-ttu-id="2eded-108">Приложение может выбрать любой из этих режимов, вызвав функцию [**сетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) .</span><span class="sxs-lookup"><span data-stu-id="2eded-108">An application can select either mode by calling the [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) function.</span></span> <span data-ttu-id="2eded-109">Дополнительные сведения о режимах заливки многоугольников см. в разделе [регионы](regions.md).</span><span class="sxs-lookup"><span data-stu-id="2eded-109">For more information about polygon fill modes, see [Regions](regions.md).</span></span>

<span data-ttu-id="2eded-110">На следующем рисунке показан многоугольник, рисуемый с помощью [**многоугольника**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span><span class="sxs-lookup"><span data-stu-id="2eded-110">The following illustration shows a polygon drawn by using [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon).</span></span>

![Иллюстрация многоугольника в форме 5-направленной звезды](images/csfsh-04.png)

<span data-ttu-id="2eded-112">В дополнение к рисованию одного многоугольника с помощью [**многоугольника**](/windows/win32/api/wingdi/nf-wingdi-polygon)приложение может нарисовать несколько многоугольников с помощью функции [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) .</span><span class="sxs-lookup"><span data-stu-id="2eded-112">In addition to drawing a single polygon by using [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon), an application can draw multiple polygons by using the [**PolyPolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) function.</span></span>

 

 
