---
description: Некоторые приложения предоставляют функции, которые заменяют объекты, отображаемые в клиентской области.
ms.assetid: e5b82013-f6b9-460d-9f53-1b50dee2064f
title: Сдвиг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c641ee0275828a7552251b0f8901c1ea41280b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265526"
---
# <a name="shear"></a><span data-ttu-id="ab3dc-103">Сдвиг</span><span class="sxs-lookup"><span data-stu-id="ab3dc-103">Shear</span></span>

<span data-ttu-id="ab3dc-104">Некоторые приложения предоставляют функции, которые заменяют объекты, отображаемые в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-104">Some applications provide features that shear objects drawn in the client area.</span></span> <span data-ttu-id="ab3dc-105">Приложения, использующие возможности сдвига, используют функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) для установки соответствующих значений в мировом пространстве для преобразования страничного пространства.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-105">Applications that use shear capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="ab3dc-106">Эта функция получает указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) , содержащую соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="ab3dc-107">Члены eM12 и eM21 XFORM указывают горизонтальные и вертикальные константы пропортионалити соответственно.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-107">The eM12 and eM21 members of XFORM specify the horizontal and vertical proportionality constants, respectively.</span></span>

<span data-ttu-id="ab3dc-108">Существует два компонента *преобразования «сдвиг*».</span><span class="sxs-lookup"><span data-stu-id="ab3dc-108">There are two components of the *shear transformation*.</span></span> <span data-ttu-id="ab3dc-109">Первый изменяет вертикальные линии в объекте; Вторая изменяет горизонтальные линии.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-109">The first alters the vertical lines in an object; the second alters the horizontal lines.</span></span> <span data-ttu-id="ab3dc-110">На следующем рисунке показан прямоугольник с 20 по 20, который обрезается по горизонтали при копировании из мира в пространство страницы.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-110">The following illustration shows a 20-by-20-unit rectangle sheared horizontally when copied from world space to page space.</span></span>

![Иллюстрация, показывающая прямоугольник в мировом пространстве и трапезиод в пространстве страницы](images/cstrn-13.png)

<span data-ttu-id="ab3dc-112">Горизонтальное наклонное значение может быть представлено следующим алгоритмом:</span><span class="sxs-lookup"><span data-stu-id="ab3dc-112">A horizontal shear can be represented by the following algorithm:</span></span>

``` syntax
x' = x + (Sx * y) 
```

<span data-ttu-id="ab3dc-113">где x — исходная координата x, SX — константа пропортионалити, а x — результат преобразования «сдвиг».</span><span class="sxs-lookup"><span data-stu-id="ab3dc-113">where x is the original x-coordinate, Sx is the proportionality constant, and x' is the result of the shear transformation.</span></span>

<span data-ttu-id="ab3dc-114">Вертикальный сдвиг может быть представлен следующим алгоритмом:</span><span class="sxs-lookup"><span data-stu-id="ab3dc-114">A vertical shear can be represented by the following algorithm:</span></span>

``` syntax
y' = y + (Sy * x) 
```

<span data-ttu-id="ab3dc-115">где y — исходная координата y, SY — константа пропортионалити, а y — результат преобразования «сдвиг».</span><span class="sxs-lookup"><span data-stu-id="ab3dc-115">where y is the original y-coordinate, Sy is the proportionality constant, and y' is the result of the shear transformation.</span></span>

<span data-ttu-id="ab3dc-116">Преобразования «горизонтальное и вертикальное наклонное» можно объединить в одну операцию, используя матрицу размером 2 на 2.</span><span class="sxs-lookup"><span data-stu-id="ab3dc-116">The horizontal-shear and vertical-shear transformations can be combined into a single operation using a 2-by-2 matrix.</span></span>

``` syntax
|x' y'| == |x y| * |  1   Sx| 
                   | Sy    1| 
```

<span data-ttu-id="ab3dc-117">Матрица размером 2 на 2, которая вызвала сдвиг, содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ab3dc-117">The 2-by-2 matrix that produced the shear contains the following values:</span></span>

``` syntax
|1    1| 
|0    1| 
```

 

 



