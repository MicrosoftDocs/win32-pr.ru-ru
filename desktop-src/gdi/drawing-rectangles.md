---
description: Прямоугольник — это четыре многоугольника, в противоположные — параллельные и равные длине.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Рисование прямоугольников
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898418"
---
# <a name="drawing-rectangles"></a><span data-ttu-id="4a606-103">Рисование прямоугольников</span><span class="sxs-lookup"><span data-stu-id="4a606-103">Drawing Rectangles</span></span>

<span data-ttu-id="4a606-104">Прямоугольник — это четыре многоугольника, в противоположные — параллельные и равные длине.</span><span class="sxs-lookup"><span data-stu-id="4a606-104">A rectangle is a four-sided polygon whose opposing sides are parallel and equal in length.</span></span> <span data-ttu-id="4a606-105">Хотя приложение может нарисовать прямоугольник путем вызова функции [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) , указав координаты каждого угла, функция [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) предоставляет более простой метод.</span><span class="sxs-lookup"><span data-stu-id="4a606-105">Although an application can draw a rectangle by calling the [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) function, supplying the coordinates of each corner, the [**Rectangle**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) function provides a simpler method.</span></span> <span data-ttu-id="4a606-106">Для этой функции требуются только координаты левого верхнего угла и правого нижнего угла.</span><span class="sxs-lookup"><span data-stu-id="4a606-106">This function requires only the coordinates for the upper-left and the lower-right corners.</span></span> <span data-ttu-id="4a606-107">Когда приложение вызывает функцию [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) , система рисует прямоугольник, исключая правую и нижнюю стороны, если для данного контекста устройства не задано универсальное преобразование.</span><span class="sxs-lookup"><span data-stu-id="4a606-107">When an application calls the [**Rectangle**](/windows/win32/api/wingdi/nf-wingdi-rectangle) function, the system draws the rectangle, excluding the right and lower sides if no world transformation is set for the given device context.</span></span>

<span data-ttu-id="4a606-108">Если универсальное преобразование было установлено с помощью функции [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) или [**модифиворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) , система включает правый и нижний края.</span><span class="sxs-lookup"><span data-stu-id="4a606-108">If a world transformation has been set by using the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) or [**ModifyWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) function, the system includes the right and lower edges.</span></span>

<span data-ttu-id="4a606-109">В дополнение к рисованию традиционного прямоугольника можно нарисовать прямоугольники со скругленными углами.</span><span class="sxs-lookup"><span data-stu-id="4a606-109">In addition to drawing a traditional rectangle, you can draw rectangles with rounded corners.</span></span> <span data-ttu-id="4a606-110">Функция [**раундрект**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) требует, чтобы приложение предоставило координаты левого нижнего и верхнего правого угла, а также ширину и высоту эллипса, используемого для округления каждого угла.</span><span class="sxs-lookup"><span data-stu-id="4a606-110">The [**RoundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) function requires that the application supply the coordinates of the lower-left and upper-right corners, as well as the width and height of the ellipse used to round each corner.</span></span>

<span data-ttu-id="4a606-111">Приложения могут использовать следующие функции для управления прямоугольниками.</span><span class="sxs-lookup"><span data-stu-id="4a606-111">Applications can use the following functions to manipulate rectangles.</span></span>



| <span data-ttu-id="4a606-112">Функция</span><span class="sxs-lookup"><span data-stu-id="4a606-112">Function</span></span>                         | <span data-ttu-id="4a606-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4a606-113">Description</span></span>                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="4a606-114">**филлрект**</span><span class="sxs-lookup"><span data-stu-id="4a606-114">**FillRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | <span data-ttu-id="4a606-115">Перерисовывает внутреннюю часть прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4a606-115">Repaints the interior of a rectangle.</span></span>                              |
| [<span data-ttu-id="4a606-116">**фрамерект**</span><span class="sxs-lookup"><span data-stu-id="4a606-116">**FrameRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-framerect)   | <span data-ttu-id="4a606-117">Перерисовывает стороны прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4a606-117">Redraws the sides of a rectangle.</span></span>                                  |
| [<span data-ttu-id="4a606-118">**инвертрект**</span><span class="sxs-lookup"><span data-stu-id="4a606-118">**InvertRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-invertrect) | <span data-ttu-id="4a606-119">Инвертирует цвета, отображаемые в внутренней части прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="4a606-119">Inverts the colors that appear within the interior of a rectangle.</span></span> |



 

 

 
