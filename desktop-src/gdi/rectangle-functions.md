---
description: С прямоугольниками используются следующие функции.
ms.assetid: b03da8c9-ee6d-4045-8d90-8beceb09ead5
title: Функции Rectangle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a5c72812363185217e5cf30ae88447f82edc42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263655"
---
# <a name="rectangle-functions"></a><span data-ttu-id="24873-103">Функции Rectangle</span><span class="sxs-lookup"><span data-stu-id="24873-103">Rectangle Functions</span></span>

<span data-ttu-id="24873-104">С прямоугольниками используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="24873-104">The following functions are used with rectangles.</span></span>



| <span data-ttu-id="24873-105">Функция</span><span class="sxs-lookup"><span data-stu-id="24873-105">Function</span></span>                               | <span data-ttu-id="24873-106">Описание</span><span class="sxs-lookup"><span data-stu-id="24873-106">Description</span></span>                                                                                                                                   |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="24873-107">**копирект**</span><span class="sxs-lookup"><span data-stu-id="24873-107">**CopyRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-copyrect)           | <span data-ttu-id="24873-108">Копирует координаты одного прямоугольника в другой.</span><span class="sxs-lookup"><span data-stu-id="24873-108">Copies the coordinates of one rectangle to another.</span></span>                                                                                           |
| [<span data-ttu-id="24873-109">**екуалрект**</span><span class="sxs-lookup"><span data-stu-id="24873-109">**EqualRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-equalrect)         | <span data-ttu-id="24873-110">Определяет, равны ли два указанных прямоугольника, сравнивая координаты их верхнего левого угла.</span><span class="sxs-lookup"><span data-stu-id="24873-110">Determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.</span></span>           |
| [<span data-ttu-id="24873-111">**инфлатерект**</span><span class="sxs-lookup"><span data-stu-id="24873-111">**InflateRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-inflaterect)     | <span data-ttu-id="24873-112">Увеличивает или уменьшает ширину и высоту указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="24873-112">Increases or decreases the width and height of the specified rectangle.</span></span>                                                                       |
| [<span data-ttu-id="24873-113">**интерсектрект**</span><span class="sxs-lookup"><span data-stu-id="24873-113">**IntersectRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-intersectrect) | <span data-ttu-id="24873-114">Вычисляет пересечение двух исходных прямоугольников и помещает координаты прямоугольника пересечения в прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="24873-114">Calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.</span></span> |
| [<span data-ttu-id="24873-115">**исректемпти**</span><span class="sxs-lookup"><span data-stu-id="24873-115">**IsRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isrectempty)     | <span data-ttu-id="24873-116">Определяет, является ли указанный прямоугольник пустым.</span><span class="sxs-lookup"><span data-stu-id="24873-116">Determines whether the specified rectangle is empty.</span></span>                                                                                          |
| [<span data-ttu-id="24873-117">**оффсетрект**</span><span class="sxs-lookup"><span data-stu-id="24873-117">**OffsetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-offsetrect)       | <span data-ttu-id="24873-118">Перемещает указанный прямоугольник на заданные смещения.</span><span class="sxs-lookup"><span data-stu-id="24873-118">Moves the specified rectangle by the specified offsets.</span></span>                                                                                       |
| [<span data-ttu-id="24873-119">**PtInRect**</span><span class="sxs-lookup"><span data-stu-id="24873-119">**PtInRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ptinrect)           | <span data-ttu-id="24873-120">Определяет, находится ли указанная точка в пределах указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="24873-120">Determines whether the specified point lies within the specified rectangle.</span></span>                                                                   |
| [<span data-ttu-id="24873-121">**SetRect**</span><span class="sxs-lookup"><span data-stu-id="24873-121">**SetRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrect)             | <span data-ttu-id="24873-122">Задает координаты указанного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="24873-122">Sets the coordinates of the specified rectangle.</span></span>                                                                                              |
| [<span data-ttu-id="24873-123">**сетректемпти**</span><span class="sxs-lookup"><span data-stu-id="24873-123">**SetRectEmpty**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setrectempty)   | <span data-ttu-id="24873-124">Создает пустой прямоугольник, в котором все координаты имеют нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="24873-124">Creates an empty rectangle in which all coordinates are set to zero.</span></span>                                                                          |
| [<span data-ttu-id="24873-125">**субтрактрект**</span><span class="sxs-lookup"><span data-stu-id="24873-125">**SubtractRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-subtractrect)   | <span data-ttu-id="24873-126">Определяет координаты прямоугольника, сформированного путем вычитания одного прямоугольника из другого.</span><span class="sxs-lookup"><span data-stu-id="24873-126">Determines the coordinates of a rectangle formed by subtracting one rectangle from another.</span></span>                                                   |
| [<span data-ttu-id="24873-127">**унионрект**</span><span class="sxs-lookup"><span data-stu-id="24873-127">**UnionRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-unionrect)         | <span data-ttu-id="24873-128">Создает объединение двух прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="24873-128">Creates the union of two rectangles.</span></span>                                                                                                          |



 

 

 



