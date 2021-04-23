---
description: Круг — это область, ограниченная пересечением кривой эллипса и двумя радиальными. На следующем рисунке показана круговая диаграмма, изображенная с помощью функции круговой диаграммы.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: О кругах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080510"
---
# <a name="about-pies"></a><span data-ttu-id="ae7c0-104">О кругах</span><span class="sxs-lookup"><span data-stu-id="ae7c0-104">About Pies</span></span>

<span data-ttu-id="ae7c0-105">*Круг* — это область, ограниченная пересечением кривой эллипса и двумя радиальными.</span><span class="sxs-lookup"><span data-stu-id="ae7c0-105">A *pie* is a region bounded by the intersection of an ellipse curve and two radials.</span></span> <span data-ttu-id="ae7c0-106">На следующем рисунке показана круговая диаграмма, изображенная с помощью функции [**круговой диаграммы**](/windows/desktop/api/Wingdi/nf-wingdi-pie) .</span><span class="sxs-lookup"><span data-stu-id="ae7c0-106">The following illustration shows a pie drawn by using the [**Pie**](/windows/desktop/api/Wingdi/nf-wingdi-pie) function.</span></span>

![Иллюстрация с эллипсом с затененной круговой диаграммой](images/csfsh-03.png)

<span data-ttu-id="ae7c0-108">При вызове [**круговой диаграммы**](/windows/win32/api/wingdi/nf-wingdi-pie)приложение предоставляет координаты верхнего левого и нижнего правого угла ограничивающего прямоугольника эллипса, а также координаты двух точек, определяющих два радиальных элемента.</span><span class="sxs-lookup"><span data-stu-id="ae7c0-108">When calling [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span>

<span data-ttu-id="ae7c0-109">Когда система рисует изогнутую часть круговой диаграммы, она использует текущее направление дуги для данного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="ae7c0-109">When the system draws the curved part of the pie, it uses the current arc direction for the given device context.</span></span> <span data-ttu-id="ae7c0-110">Направление дуги по умолчанию — против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="ae7c0-110">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="ae7c0-111">Приложение может сбросить направление дуги, вызвав функцию [**сетаркдиректион**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="ae7c0-111">An application can reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
