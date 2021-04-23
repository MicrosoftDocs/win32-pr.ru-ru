---
description: Эллипс — это замкнутая кривая, определяемая двумя фиксированными точками (F1 и F2) таким, что сумма расстояний (D1 + D2) от любой точки кривой до двух фиксированных точек является константой.
ms.assetid: c4aab4cf-9575-4817-b51f-aed4e3c27d2f
title: О многоточии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77c6b2774da9886e25d3e1dcca7c701b034e7b45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554717"
---
# <a name="about-ellipses"></a><span data-ttu-id="604ae-103">О многоточии</span><span class="sxs-lookup"><span data-stu-id="604ae-103">About Ellipses</span></span>

<span data-ttu-id="604ae-104">Эллипс — это замкнутая кривая, определяемая двумя фиксированными точками (F1 и F2) таким, что сумма расстояний (D1 + D2) от любой точки кривой до двух фиксированных точек является константой.</span><span class="sxs-lookup"><span data-stu-id="604ae-104">An ellipse is a closed curve defined by two fixed points (f1 and f2 ) such that the sum of the distances (d1 +d2 ) from any point on the curve to the two fixed points is constant.</span></span> <span data-ttu-id="604ae-105">На следующем рисунке показан эллипс, нарисованный с помощью функции [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) .</span><span class="sxs-lookup"><span data-stu-id="604ae-105">The following illustration shows an ellipse drawn by using the [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse) function.</span></span>

![Иллюстрация, содержащая эллипс, две фиксированные точки, два расстояния и ограничивающий прямоугольник](images/csfsh-01.png)

<span data-ttu-id="604ae-107">При вызове метода [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse)приложение предоставляет координаты верхнего левого и нижнего правого угла ограничивающего прямоугольника эллипса.</span><span class="sxs-lookup"><span data-stu-id="604ae-107">When calling [**Ellipse**](/windows/desktop/api/Wingdi/nf-wingdi-ellipse), an application supplies the coordinates of the upper-left and lower-right corners of the ellipse's bounding rectangle.</span></span> <span data-ttu-id="604ae-108">*Ограничивающий прямоугольник* — это самый маленький прямоугольник, полностью окружающий эллипс.</span><span class="sxs-lookup"><span data-stu-id="604ae-108">A *bounding rectangle* is the smallest rectangle completely surrounding the ellipse.</span></span> <span data-ttu-id="604ae-109">Когда система рисует эллипс, она исключает правую и нижнюю стороны, если не заданы универсальные преобразования.</span><span class="sxs-lookup"><span data-stu-id="604ae-109">When the system draws the ellipse, it excludes the right and lower sides if no world transformations are set.</span></span> <span data-ttu-id="604ae-110">Таким образом, для любого прямоугольника, который измеряет x единиц в ширину по оси y, связанный эллипс измеряет единицы x1 в ширину по единицам измерения "высокий".</span><span class="sxs-lookup"><span data-stu-id="604ae-110">Therefore, for any rectangle measuring x units wide by y units high, the associated ellipse measures x1 units wide by y1 units high.</span></span> <span data-ttu-id="604ae-111">Если приложение устанавливает универсальное преобразование, вызывая функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) или [**модифиворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , система включает правую и нижнюю стороны.</span><span class="sxs-lookup"><span data-stu-id="604ae-111">If the application sets a world transformation by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower sides.</span></span>

 

 



