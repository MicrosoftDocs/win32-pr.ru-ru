---
description: Аккорд — это область, ограниченная пересечением эллипса и сегмента линии под названием секанс. На следующем рисунке показана аккорд, рисуемая с помощью функции аккорд.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: О аккордах
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543631"
---
# <a name="about-chords"></a><span data-ttu-id="b4e3d-104">О аккордах</span><span class="sxs-lookup"><span data-stu-id="b4e3d-104">About Chords</span></span>

<span data-ttu-id="b4e3d-105">*Аккорд* — это область, ограниченная пересечением эллипса и сегмента линии под названием *секанс*.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-105">A *chord* is a region bounded by the intersection of an ellipse and a line segment called a *secant*.</span></span> <span data-ttu-id="b4e3d-106">На следующем рисунке показана аккорд, рисуемая с помощью функции [**аккорд**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .</span><span class="sxs-lookup"><span data-stu-id="b4e3d-106">The following illustration shows a chord drawn by using the [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) function.</span></span>

![Иллюстрация елипсеа, показывающая два радиальных круга, секанс и Аккорд](images/csfsh-02.png)

<span data-ttu-id="b4e3d-108">При вызове функции [**аккорд**](/windows/win32/api/wingdi/nf-wingdi-chord)приложение предоставляет координаты верхнего левого и нижнего правого угла ограничивающего прямоугольника эллипса, а также координаты двух точек, определяющих два радиальных элемента.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-108">When calling [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle, as well as the coordinates of two points defining two radials.</span></span> <span data-ttu-id="b4e3d-109">Радиальный — это линия, нарисованная из центра ограничивающего прямоугольника эллипса в точку на эллипсе.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-109">A radial is a line drawn from the center of an ellipse's bounding rectangle to a point on the ellipse.</span></span>

<span data-ttu-id="b4e3d-110">Когда система рисует изогнутую часть аккорда, она делает это с помощью текущего направления дуги для указанного контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-110">When the system draws the curved part of the chord, it does so by using the current arc direction for the specified device context.</span></span> <span data-ttu-id="b4e3d-111">Направление дуги по умолчанию — против часовой стрелки.</span><span class="sxs-lookup"><span data-stu-id="b4e3d-111">The default arc direction is counterclockwise.</span></span> <span data-ttu-id="b4e3d-112">Приложение можно сбросить в направлении дуги, вызвав функцию [**сетаркдиректион**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .</span><span class="sxs-lookup"><span data-stu-id="b4e3d-112">You can have your application reset the arc direction by calling the [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) function.</span></span>

 

 
