---
description: Список функций плоскости, предоставляемых Директксмас.
ms.assetid: 6505e72e-4af5-5db3-4fc0-f83fa77692b1
title: Функции плоскости библиотеки Директксмас
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b3f450b4dbaa5ed1b4348ad8b090210c14e2022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701853"
---
# <a name="directxmath-library-plane-functions"></a><span data-ttu-id="6b414-103">Функции плоскости библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="6b414-103">DirectXMath Library plane functions</span></span>

<span data-ttu-id="6b414-104">Список функций плоскости, предоставляемых Директксмас.</span><span class="sxs-lookup"><span data-stu-id="6b414-104">Lists the plane functions provided by DirectXMath.</span></span>

<span data-ttu-id="6b414-105">Эти функции используют КСМВЕКТОР 4-Vector для представления коэффициентов уравнения плоскости, AX + by + CZ + D = 0, где X-компонент — это, компонент Y — B, компонент Z — C, а W-компонент — D.</span><span class="sxs-lookup"><span data-stu-id="6b414-105">These functions use an XMVECTOR 4-vector to represent the coefficients of the plane equation, Ax+By+Cz+D = 0, where the X-component is A, the Y-component is B, the Z-component is C, and the W-component is D.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b414-106">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="6b414-106">In this section</span></span>



| <span data-ttu-id="6b414-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="6b414-107">Topic</span></span>                                                               | <span data-ttu-id="6b414-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6b414-108">Description</span></span>                                                                                                      |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b414-109">**ксмпланедот**</span><span class="sxs-lookup"><span data-stu-id="6b414-109">**XMPlaneDot**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)<br/>                         | <span data-ttu-id="6b414-110">Вычисляет точку произведения между входной плоскостью и вектором 4D.</span><span class="sxs-lookup"><span data-stu-id="6b414-110">Calculates the dot product between an input plane and a 4D vector.</span></span><br/>                                    |
| [<span data-ttu-id="6b414-111">**ксмпланедоткурд**</span><span class="sxs-lookup"><span data-stu-id="6b414-111">**XMPlaneDotCoord**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)<br/>               | <span data-ttu-id="6b414-112">Вычисляет точку произведения между входной плоскостью и трехмерным вектором.</span><span class="sxs-lookup"><span data-stu-id="6b414-112">Calculates the dot product between an input plane and a 3D vector.</span></span><br/>                                    |
| [<span data-ttu-id="6b414-113">**ксмпланедотнормал**</span><span class="sxs-lookup"><span data-stu-id="6b414-113">**XMPlaneDotNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)<br/>             | <span data-ttu-id="6b414-114">Вычисляет точку произведения между нормальным вектором плоскости и трехмерным вектором.</span><span class="sxs-lookup"><span data-stu-id="6b414-114">Calculates the dot product between the normal vector of a plane and a 3D vector.</span></span><br/>                      |
| [<span data-ttu-id="6b414-115">**ксмпланикуал**</span><span class="sxs-lookup"><span data-stu-id="6b414-115">**XMPlaneEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneequal)<br/>                     | <span data-ttu-id="6b414-116">Определяет, равны ли две плоскости.</span><span class="sxs-lookup"><span data-stu-id="6b414-116">Determines if two planes are equal.</span></span><br/>                                                                   |
| [<span data-ttu-id="6b414-117">**ксмпланефромпоинтнормал**</span><span class="sxs-lookup"><span data-stu-id="6b414-117">**XMPlaneFromPointNormal**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)<br/> | <span data-ttu-id="6b414-118">Выполняет вычисление уравнения плоскости, созданной на основе точки в плоскости и обычного вектора.</span><span class="sxs-lookup"><span data-stu-id="6b414-118">Computes the equation of a plane constructed from a point in the plane and a normal vector.</span></span><br/>           |
| [<span data-ttu-id="6b414-119">**ксмпланефромпоинтс**</span><span class="sxs-lookup"><span data-stu-id="6b414-119">**XMPlaneFromPoints**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)<br/>           | <span data-ttu-id="6b414-120">Вычисление уравнения плоскости, построенной на основе трех точек в плоскости.</span><span class="sxs-lookup"><span data-stu-id="6b414-120">Computes the equation of a plane constructed from three points in the plane.</span></span><br/>                          |
| [<span data-ttu-id="6b414-121">**ксмпланеинтерсектлине**</span><span class="sxs-lookup"><span data-stu-id="6b414-121">**XMPlaneIntersectLine**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)<br/>     | <span data-ttu-id="6b414-122">Находит пересечение между плоскостью и линией.</span><span class="sxs-lookup"><span data-stu-id="6b414-122">Finds the intersection between a plane and a line.</span></span><br/>                                                    |
| [<span data-ttu-id="6b414-123">**ксмпланеинтерсектплане**</span><span class="sxs-lookup"><span data-stu-id="6b414-123">**XMPlaneIntersectPlane**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectplane)<br/>   | <span data-ttu-id="6b414-124">Находит пересечение двух плоскостей.</span><span class="sxs-lookup"><span data-stu-id="6b414-124">Finds the intersection of two planes.</span></span><br/>                                                                 |
| [<span data-ttu-id="6b414-125">**ксмпланеисинфините**</span><span class="sxs-lookup"><span data-stu-id="6b414-125">**XMPlaneIsInfinite**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisinfinite)<br/>           | <span data-ttu-id="6b414-126">Проверяет, является ли любая из коэффициентов плоскости положительной или отрицательной бесконечностью.</span><span class="sxs-lookup"><span data-stu-id="6b414-126">Tests whether any of the coefficients of a plane is positive or negative infinity.</span></span><br/>                    |
| [<span data-ttu-id="6b414-127">**ксмпланеиснан**</span><span class="sxs-lookup"><span data-stu-id="6b414-127">**XMPlaneIsNaN**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplaneisnan)<br/>                     | <span data-ttu-id="6b414-128">Проверяет, является ли ни одно из коэффициентов плоскости значением NaN.</span><span class="sxs-lookup"><span data-stu-id="6b414-128">Tests whether any of the coefficients of a plane is a NaN.</span></span><br/>                                            |
| [<span data-ttu-id="6b414-129">**ксмпланенеарекуал**</span><span class="sxs-lookup"><span data-stu-id="6b414-129">**XMPlaneNearEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenearequal)<br/>             | <span data-ttu-id="6b414-130">Определяет, являются ли две плоскости почти равными.</span><span class="sxs-lookup"><span data-stu-id="6b414-130">Determines whether two planes are nearly equal.</span></span><br/>                                                       |
| [<span data-ttu-id="6b414-131">**ксмпланенормализе**</span><span class="sxs-lookup"><span data-stu-id="6b414-131">**XMPlaneNormalize**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize)<br/>             | <span data-ttu-id="6b414-132">Нормализует коэффициенты плоскости таким образом, чтобы коэффициенты координат x, y и z были вектором обычной единицы.</span><span class="sxs-lookup"><span data-stu-id="6b414-132">Normalizes the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/> |
| [<span data-ttu-id="6b414-133">**ксмпланенормализист**</span><span class="sxs-lookup"><span data-stu-id="6b414-133">**XMPlaneNormalizeEst**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)<br/>       | <span data-ttu-id="6b414-134">Оценивает коэффициенты плоскости таким образом, что коэффициенты x, y и z образуют вектор нормали единицы.</span><span class="sxs-lookup"><span data-stu-id="6b414-134">Estimates the coefficients of a plane so that coefficients of x, y, and z form a unit normal vector.</span></span><br/>  |
| [<span data-ttu-id="6b414-135">**ксмпланенотекуал**</span><span class="sxs-lookup"><span data-stu-id="6b414-135">**XMPlaneNotEqual**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanenotequal)<br/>               | <span data-ttu-id="6b414-136">Определяет, являются ли две плоскости неравными.</span><span class="sxs-lookup"><span data-stu-id="6b414-136">Determines if two planes are unequal.</span></span><br/>                                                                 |
| [<span data-ttu-id="6b414-137">**ксмпланетрансформ**</span><span class="sxs-lookup"><span data-stu-id="6b414-137">**XMPlaneTransform**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)<br/>             | <span data-ttu-id="6b414-138">Преобразует плоскость в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="6b414-138">Transforms a plane by a given matrix.</span></span><br/>                                                                 |
| [<span data-ttu-id="6b414-139">**ксмпланетрансформстреам**</span><span class="sxs-lookup"><span data-stu-id="6b414-139">**XMPlaneTransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)<br/> | <span data-ttu-id="6b414-140">Преобразует поток плоскостей по заданной матрице.</span><span class="sxs-lookup"><span data-stu-id="6b414-140">Transforms a stream of planes by a given matrix.</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="6b414-141">См. также</span><span class="sxs-lookup"><span data-stu-id="6b414-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b414-142">Функции библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="6b414-142">DirectXMath Library Functions</span></span>](ovw-xnamath-reference-functions.md)
</dt> </dl>

 

 
