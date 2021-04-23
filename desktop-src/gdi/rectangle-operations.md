---
description: Функция SetRect создает прямоугольник, функция Копирект создает копию данного прямоугольника, а функция Сетректемпти — пустой прямоугольник.
ms.assetid: 982d6283-673b-41a1-abc7-10ef87ff3c6f
title: Операции с прямоугольниками
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3117fda697000e92258c99cf90af470e8815e237
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344642"
---
# <a name="rectangle-operations"></a><span data-ttu-id="da430-103">Операции с прямоугольниками</span><span class="sxs-lookup"><span data-stu-id="da430-103">Rectangle Operations</span></span>

<span data-ttu-id="da430-104">Функция [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) создает прямоугольник, функция [**копирект**](/windows/desktop/api/Winuser/nf-winuser-copyrect) создает копию данного прямоугольника, а функция [**сетректемпти**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) — пустой прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="da430-104">The [**SetRect**](/windows/desktop/api/Winuser/nf-winuser-setrect) function creates a rectangle, the [**CopyRect**](/windows/desktop/api/Winuser/nf-winuser-copyrect) function makes a copy of a given rectangle, and the [**SetRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-setrectempty) function creates an empty rectangle.</span></span> <span data-ttu-id="da430-105">Пустой прямоугольник — это любой прямоугольник с нулевой шириной, нулевой высотой или обоими.</span><span class="sxs-lookup"><span data-stu-id="da430-105">An empty rectangle is any rectangle that has zero width, zero height, or both.</span></span> <span data-ttu-id="da430-106">Функция [**исректемпти**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) определяет, является ли данный прямоугольник пустым.</span><span class="sxs-lookup"><span data-stu-id="da430-106">The [**IsRectEmpty**](/windows/desktop/api/Winuser/nf-winuser-isrectempty) function determines whether a given rectangle is empty.</span></span> <span data-ttu-id="da430-107">Функция [**екуалрект**](/windows/desktop/api/Winuser/nf-winuser-equalrect) определяет идентичность двух прямоугольников (независимо от того, имеют ли они одинаковые координаты).</span><span class="sxs-lookup"><span data-stu-id="da430-107">The [**EqualRect**](/windows/desktop/api/Winuser/nf-winuser-equalrect) function determines whether two rectangles are identical that is, whether they have the same coordinates.</span></span>

<span data-ttu-id="da430-108">Функция [**инфлатерект**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) увеличивает или уменьшает ширину или высоту прямоугольника или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="da430-108">The [**InflateRect**](/windows/desktop/api/Winuser/nf-winuser-inflaterect) function increases or decreases the width or height of a rectangle, or both.</span></span> <span data-ttu-id="da430-109">Он может добавлять или удалять ширину обеих сторон прямоугольника. Он может добавлять или удалять высоту как в верхней, так и в нижней части прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="da430-109">It can add or remove width from both ends of the rectangle; it can add or remove height from both the top and bottom of the rectangle.</span></span>

<span data-ttu-id="da430-110">Функция [**оффсетрект**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) Перемещает прямоугольник на заданный объем.</span><span class="sxs-lookup"><span data-stu-id="da430-110">The [**OffsetRect**](/windows/desktop/api/Winuser/nf-winuser-offsetrect) function moves a rectangle by a given amount.</span></span> <span data-ttu-id="da430-111">Он перемещает прямоугольник, добавляя заданные значения x-Amount, y или x и y в угловые координаты.</span><span class="sxs-lookup"><span data-stu-id="da430-111">It moves the rectangle by adding the given x-amount, y-amount, or x- and y-amounts to the corner coordinates.</span></span>

<span data-ttu-id="da430-112">Функция [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) определяет, находится ли заданная точка в пределах данного прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="da430-112">The [**PtInRect**](/windows/desktop/api/Winuser/nf-winuser-ptinrect) function determines whether a given point lies within a given rectangle.</span></span> <span data-ttu-id="da430-113">Точка находится в прямоугольнике, если она находится на левой или верхней стороне или полностью находится внутри прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="da430-113">The point is in the rectangle if it lies on the left or top side or is completely within the rectangle.</span></span> <span data-ttu-id="da430-114">Точка отсутствует в прямоугольнике, если она находится на правой или нижней стороне.</span><span class="sxs-lookup"><span data-stu-id="da430-114">The point is not in the rectangle if it lies on the right or bottom side.</span></span>

<span data-ttu-id="da430-115">Функция [**интерсектрект**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) создает новый прямоугольник, который является пересечением двух существующих прямоугольников, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="da430-115">The [**IntersectRect**](/windows/desktop/api/Winuser/nf-winuser-intersectrect) function creates a new rectangle that is the intersection of two existing rectangles, as shown in the following figure.</span></span>

![<span data-ttu-id="da430-116">Иллюстрация, демонстрирующая два перекрывающихся прямоугольника с темным затенением для обозначения пересечения</span><span class="sxs-lookup"><span data-stu-id="da430-116">illustration showing two overlapping rectangles, with darker shading to indicate the intersection</span></span> ](images/csrec-01.png)

<span data-ttu-id="da430-117">Функция [**унионрект**](/windows/desktop/api/Winuser/nf-winuser-unionrect) создает новый прямоугольник, который является объединением двух существующих прямоугольников, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="da430-117">The [**UnionRect**](/windows/desktop/api/Winuser/nf-winuser-unionrect) function creates a new rectangle that is the union of two existing rectangles, as shown in the following figure.</span></span>

![Иллюстрация двух перекрывающихся прямоугольников с темным затенением, указывающим области внутри объединения, но не в пределах одного прямоугольника](images/csrec-02.png)

<span data-ttu-id="da430-119">Сведения о функциях, рисующих эллипсы и многоугольники, см. в разделе [закрашенные фигуры](filled-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="da430-119">For information about functions that draw ellipses and polygons, see [Filled Shapes](filled-shapes.md).</span></span>

 

 



