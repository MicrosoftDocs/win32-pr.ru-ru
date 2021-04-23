---
description: Некоторые приложения предоставляют функции, отражающие (или зеркальные) объекты, созданные в клиентской области.
ms.assetid: 2205dc3c-ca4b-4a0a-be3e-0332ce8467a0
title: Отражение
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8e327af098a4e232e2a6734b37a17a1ac85f19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984837"
---
# <a name="reflection"></a><span data-ttu-id="0ae01-103">Отражение</span><span class="sxs-lookup"><span data-stu-id="0ae01-103">Reflection</span></span>

<span data-ttu-id="0ae01-104">Некоторые приложения предоставляют функции, отражающие (или зеркальные) объекты, созданные в клиентской области.</span><span class="sxs-lookup"><span data-stu-id="0ae01-104">Some applications provide features that reflect (or mirror) objects drawn in the client area.</span></span> <span data-ttu-id="0ae01-105">Приложения, которые содержат возможности отражения, используют функцию [**сетворлдтрансформ**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , чтобы установить соответствующие значения в пространстве для преобразования «пространство на странице».</span><span class="sxs-lookup"><span data-stu-id="0ae01-105">Applications that contain reflection capabilities use the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function to set the appropriate values in the world-space to page-space transformation.</span></span> <span data-ttu-id="0ae01-106">Эта функция получает указатель на структуру [**XForm**](/windows/win32/api/wingdi/ns-wingdi-xform) , содержащую соответствующие значения.</span><span class="sxs-lookup"><span data-stu-id="0ae01-106">This function receives a pointer to an [**XFORM**](/windows/win32/api/wingdi/ns-wingdi-xform) structure containing the appropriate values.</span></span> <span data-ttu-id="0ae01-107">Члены eM11 и eM22 XFORM определяют компоненты отражения по горизонтали и вертикали соответственно.</span><span class="sxs-lookup"><span data-stu-id="0ae01-107">The eM11 and eM22 members of XFORM specify the horizontal and vertical reflection components, respectively.</span></span>

<span data-ttu-id="0ae01-108">*Преобразование «отражение* » создает зеркальное изображение объекта относительно оси x или y.</span><span class="sxs-lookup"><span data-stu-id="0ae01-108">The *reflection transformation* creates a mirror image of an object with respect to either the x- or y-axis.</span></span> <span data-ttu-id="0ae01-109">Вкратце, отражение — это просто отрицательное масштабирование.</span><span class="sxs-lookup"><span data-stu-id="0ae01-109">In short, reflection is just negative scaling.</span></span> <span data-ttu-id="0ae01-110">Чтобы создать горизонтальное отражение, координаты x умножаются на 1.</span><span class="sxs-lookup"><span data-stu-id="0ae01-110">To produce a horizontal reflection, x-coordinates are multiplied by 1.</span></span> <span data-ttu-id="0ae01-111">Для создания вертикального отражения координаты y умножаются на 1.</span><span class="sxs-lookup"><span data-stu-id="0ae01-111">To produce a vertical reflection, y-coordinates are multiplied by 1.</span></span>

<span data-ttu-id="0ae01-112">Отражение по горизонтали может быть представлено следующим алгоритмом:</span><span class="sxs-lookup"><span data-stu-id="0ae01-112">Horizontal reflection can be represented by the following algorithm:</span></span>

``` syntax
x' = -x 
```

<span data-ttu-id="0ae01-113">где x — это координата x, а x — результат отражения.</span><span class="sxs-lookup"><span data-stu-id="0ae01-113">where x is the x-coordinate and x' is the result of the reflection.</span></span>

<span data-ttu-id="0ae01-114">Матрица размером 2 на 2, которая выдала горизонтальное отражение, содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ae01-114">The 2-by-2 matrix that produced horizontal reflection contains the following values:</span></span>

``` syntax
|-1    0| 
|0     1| 
```

<span data-ttu-id="0ae01-115">Вертикальное отражение может быть представлено следующим алгоритмом:</span><span class="sxs-lookup"><span data-stu-id="0ae01-115">Vertical reflection can be represented by the following algorithm:</span></span>

``` syntax
y' = -y 
```

<span data-ttu-id="0ae01-116">где y — это y-координата, а y — результат отражения.</span><span class="sxs-lookup"><span data-stu-id="0ae01-116">where y is the y-coordinate and y' is the result of the reflection.</span></span>

<span data-ttu-id="0ae01-117">Матрица размером 2 на 2, которая выдала вертикальное отражение, содержит следующие значения:</span><span class="sxs-lookup"><span data-stu-id="0ae01-117">The 2-by-2 matrix that produced vertical reflection contains the following values:</span></span>

``` syntax
|1    0| 
|0   -1| 
```

<span data-ttu-id="0ae01-118">Операции горизонтального отражения и вертикального отражения можно объединить в одну операцию, используя следующую матрицу размером 2 на 2:</span><span class="sxs-lookup"><span data-stu-id="0ae01-118">The horizontal-reflection and vertical-reflection operations can be combined into a single operation by using the following 2-by-2 matrix:</span></span>

``` syntax
|-1    0| 
|0    -1| 
```

 

 



