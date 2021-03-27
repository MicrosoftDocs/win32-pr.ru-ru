---
description: Некоторые приложения преобразуют (или сдвигаются) объекты, отображаемые в клиентской области.
ms.assetid: e319a5c6-a045-42b1-a83e-3a978172b52c
title: Перевод
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699ec4c75ebb79e440fbc9b01231fe83feb942dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987797"
---
# <a name="translation"></a><span data-ttu-id="c3e3f-103">Перевод</span><span class="sxs-lookup"><span data-stu-id="c3e3f-103">Translation</span></span>

<span data-ttu-id="c3e3f-104">Некоторые приложения преобразуют (или сдвигаются) объекты, отображаемые в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-104">Some applications translate (or shift) objects drawn in the client area.</span></span> <span data-ttu-id="c3e3f-105">путем вызова функции [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , чтобы установить соответствующее преобразование пространства на страницу.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-105">by calling the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate world-space to page-space transformation.</span></span> <span data-ttu-id="c3e3f-106">Функция Сетворлдтрансформ получает указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) , содержащую соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-106">The SetWorldTransform function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="c3e3f-107">Члены eDx и еди XFORM определяют компоненты перевода по горизонтали и вертикали соответственно.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-107">The eDx and eDy members of XFORM specify the horizontal and vertical translation components, respectively.</span></span>

<span data-ttu-id="c3e3f-108">При *преобразовании* каждая точка в объекте смещается вертикально, горизонтально или по горизонтали на заданный объем.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-108">When *translation* occurs, each point in an object is shifted vertically, horizontally, or both, by a specified amount.</span></span> <span data-ttu-id="c3e3f-109">На следующем рисунке показан прямоугольник с 20 по 20 единиц, который был переведен вправо на 10 единиц при копировании из универсального пространства в пространство координат страницы.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-109">The following illustration shows a 20- by 20-unit rectangle that was translated to the right by 10 units when copied from world-coordinate space to page-coordinate space.</span></span>

![Иллюстрация, показывающая прямоугольник в одном месте в мировом пространстве и в другом месте в пространстве страницы](images/cstrn-09.png)

<span data-ttu-id="c3e3f-111">На предыдущем рисунке Координата x каждой точки в прямоугольнике равна 10 единицам, превышающим исходную координату x.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-111">In the preceding illustration, the x-coordinate of each point in the rectangle is 10 units greater than the original x-coordinate.</span></span>

<span data-ttu-id="c3e3f-112">Горизонтальное преобразование может быть представлено следующим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-112">Horizontal translation can be represented by the following algorithm.</span></span>

``` syntax
x' = x + Dx 
```

<span data-ttu-id="c3e3f-113">Где x — это новая Координата x, x — исходная координата x, а DX — горизонтальное расстояние перемещено.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-113">Where x' is the new x-coordinate, x is the original x-coordinate, and Dx is the horizontal distance moved.</span></span>

<span data-ttu-id="c3e3f-114">Вертикальный перевод может быть представлен следующим алгоритмом.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-114">Vertical translation can be represented by the following algorithm.</span></span>

``` syntax
y' = y + Dy 
```

<span data-ttu-id="c3e3f-115">Где y — это новая координата y, y — исходная координата y, а DY — перемещаемое расстояние по вертикали.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-115">Where y' is the new y-coordinate, y is the original y-coordinate, and Dy is the vertical distance moved.</span></span>

<span data-ttu-id="c3e3f-116">Горизонтальные и вертикальные преобразования перевода можно объединить в одну операцию с помощью матрицы размером 3 на 3.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-116">The horizontal and vertical translation transformations can be combined into a single operation by using a 3-by-3 matrix.</span></span>

``` syntax
                      |1   0   0| 
|x' y' 1| = |x y 1| * |0   1   0| 
                      |Dx  Dy  1| 
```

<span data-ttu-id="c3e3f-117">(Правила умножения матриц, что количество строк в одной матрице должно равняться числу столбцов в другом.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-117">(The rules of matrix multiplication state that the number of rows in one matrix must equal the number of columns in the other.</span></span> <span data-ttu-id="c3e3f-118">Целое число 1 в матрице \| x y 1 \| — это заполнитель, который был добавлен в соответствии с этим требованием.)</span><span class="sxs-lookup"><span data-stu-id="c3e3f-118">The integer 1 in the matrix \|x y 1\| is a placeholder that was added to meet this requirement.)</span></span>

<span data-ttu-id="c3e3f-119">Матрица с 3 по 3, которая продемонстрировала преобразование преобразований, содержит следующие значения.</span><span class="sxs-lookup"><span data-stu-id="c3e3f-119">The 3-by-3 matrix that produced the illustrated translation transformation contains the following values.</span></span>

``` syntax
|1  0  0| 
|0  1  0| 
|10 0  1| 
```

 

 



