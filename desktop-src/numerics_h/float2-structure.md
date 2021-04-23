---
title: Структура float2 (Виндовснумерикс. h)
description: Вектор с двумя компонентами.
ms.assetid: 1A23C1E3-F34F-4249-80EA-92A13CD4B34F
keywords:
- Структура float2
topic_type:
- apiref
api_name:
- float2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72398bdc087e0f7a0845703a2cefea40b5465b21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721053"
---
# <a name="float2-structure"></a><span data-ttu-id="371cf-104">Структура float2</span><span class="sxs-lookup"><span data-stu-id="371cf-104">float2 structure</span></span>

<span data-ttu-id="371cf-105">Вектор с двумя компонентами.</span><span class="sxs-lookup"><span data-stu-id="371cf-105">A vector with two components.</span></span>

<span data-ttu-id="371cf-106">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="371cf-106">This type is available only in C++.</span></span> <span data-ttu-id="371cf-107">Его эквивалент .NET — [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="371cf-107">Its .NET equivalent is [System.Numerics.Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="371cf-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="371cf-108">Constructors</span></span>

| <span data-ttu-id="371cf-109">Имя</span><span class="sxs-lookup"><span data-stu-id="371cf-109">Name</span></span> | <span data-ttu-id="371cf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="371cf-110">Description</span></span> |
|-|-|
| `float2()` | <span data-ttu-id="371cf-111">Создает неинициализированную float2.</span><span class="sxs-lookup"><span data-stu-id="371cf-111">Creates an uninitialized float2.</span></span> |
| `float2(float x, float y)` | <span data-ttu-id="371cf-112">Создает объект float2 с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="371cf-112">Creates a float2 with the specified values.</span></span> |
| `explicit float2(float value)` | <span data-ttu-id="371cf-113">Создает float2 со всеми компонентами, для которых задано указанное значение.</span><span class="sxs-lookup"><span data-stu-id="371cf-113">Creates a float2 with all components set to the specified value.</span></span> |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | <span data-ttu-id="371cf-114">Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector2** в float2.</span><span class="sxs-lookup"><span data-stu-id="371cf-114">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector2** to a float2.</span></span> |
| `float2(Windows::Foundation::Point const& value)` | <span data-ttu-id="371cf-115">Преобразует [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) в float2.</span><span class="sxs-lookup"><span data-stu-id="371cf-115">Converts a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point) to a float2.</span></span> |
| `float2(Windows::Foundation::Size const& value)` | <span data-ttu-id="371cf-116">Преобразует [**Windows. Foundation. size**](/uwp/api/Windows.Foundation.Size) в float2.</span><span class="sxs-lookup"><span data-stu-id="371cf-116">Converts a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size) to a float2.</span></span> |

## <a name="functions"></a><span data-ttu-id="371cf-117">Функции</span><span class="sxs-lookup"><span data-stu-id="371cf-117">Functions</span></span>

| <span data-ttu-id="371cf-118">Имя</span><span class="sxs-lookup"><span data-stu-id="371cf-118">Name</span></span> | <span data-ttu-id="371cf-119">Описание</span><span class="sxs-lookup"><span data-stu-id="371cf-119">Description</span></span> |
|-|-|
| `float length(float2 const& value)` | <span data-ttu-id="371cf-120">Вычисляет длину вектора (евклидово distance).</span><span class="sxs-lookup"><span data-stu-id="371cf-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float2 const& value)` | <span data-ttu-id="371cf-121">Вычисляет длину (или евклидово расстояние) вектора в квадрате.</span><span class="sxs-lookup"><span data-stu-id="371cf-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-122">Вычисляет евклидово расстояние между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="371cf-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-123">Вычисляет евклидово расстояние между двумя векторами в квадрате.</span><span class="sxs-lookup"><span data-stu-id="371cf-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-124">Вычисляет скалярное произведение двух векторов.</span><span class="sxs-lookup"><span data-stu-id="371cf-124">Calculates the dot product of two vectors.</span></span> |
| `float2 normalize(float2 const& value)` | <span data-ttu-id="371cf-125">Создает единичный вектор из указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-125">Creates a unit vector from the specified vector.</span></span> |
| `float2 reflect(float2 const& vector, float2 const& normal)` | <span data-ttu-id="371cf-126">Определяет вектор отражения заданного вектора и нормали.</span><span class="sxs-lookup"><span data-stu-id="371cf-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float2 min(float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-127">Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="371cf-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float2 max(float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-128">Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="371cf-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | <span data-ttu-id="371cf-129">Разрешает значение в пределах указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="371cf-129">Restricts a value to be within a specified range.</span></span> |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | <span data-ttu-id="371cf-130">Выполняет линейную интерполяцию между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="371cf-130">Performs a linear interpolation between two vectors.</span></span> |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | <span data-ttu-id="371cf-131">Преобразует вектор (x, y, 0, 1) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="371cf-131">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="371cf-132">Преобразует вектор (x, y, 0, 1) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="371cf-132">Transforms the vector (x, y, 0, 1) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | <span data-ttu-id="371cf-133">Преобразует Стандартный вектор (x, y, 0, 0) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="371cf-133">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | <span data-ttu-id="371cf-134">Преобразует Стандартный вектор (x, y, 0, 0) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="371cf-134">Transforms the normal vector (x, y, 0, 0) by the specified matrix.</span></span> |
| `float2 transform(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="371cf-135">Преобразует float2 в заданный кватернион.</span><span class="sxs-lookup"><span data-stu-id="371cf-135">Transforms a float2 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="371cf-136">Методы</span><span class="sxs-lookup"><span data-stu-id="371cf-136">Methods</span></span>

| <span data-ttu-id="371cf-137">Имя</span><span class="sxs-lookup"><span data-stu-id="371cf-137">Name</span></span> | <span data-ttu-id="371cf-138">Описание</span><span class="sxs-lookup"><span data-stu-id="371cf-138">Description</span></span> |
|-|-|
| `static float2 zero()` | <span data-ttu-id="371cf-139">Возвращает float2 со всеми его компонентами, для которых задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="371cf-139">Returns a float2 with all of its components set to zero.</span></span> |
| `static float2 one()` | <span data-ttu-id="371cf-140">Возвращает float2 со всеми его компонентами, для которых задано значение One.</span><span class="sxs-lookup"><span data-stu-id="371cf-140">Returns a float2 with all of its components set to one.</span></span> |
| `static float2 unit_x()` | <span data-ttu-id="371cf-141">Возвращает float2 (1, 0).</span><span class="sxs-lookup"><span data-stu-id="371cf-141">Returns the float2 (1, 0).</span></span> |
| `static float2 unit_y()` | <span data-ttu-id="371cf-142">Возвращает float2 (0, 1).</span><span class="sxs-lookup"><span data-stu-id="371cf-142">Returns the float2 (0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="371cf-143">Операторы</span><span class="sxs-lookup"><span data-stu-id="371cf-143">Operators</span></span>

| <span data-ttu-id="371cf-144">Имя</span><span class="sxs-lookup"><span data-stu-id="371cf-144">Name</span></span> | <span data-ttu-id="371cf-145">Описание</span><span class="sxs-lookup"><span data-stu-id="371cf-145">Description</span></span> |
|-|-|
| `operator Windows::Foundation::Point() const` | <span data-ttu-id="371cf-146">Преобразует float2 в [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point).</span><span class="sxs-lookup"><span data-stu-id="371cf-146">Converts a float2 to a [**Windows.Foundation.Point**](/uwp/api/Windows.Foundation.Point).</span></span> |
| `operator Windows::Foundation::Size() const` | <span data-ttu-id="371cf-147">Преобразует float2 в [**Windows. Foundation. size**](/uwp/api/Windows.Foundation.Size).</span><span class="sxs-lookup"><span data-stu-id="371cf-147">Converts a float2 to a [**Windows.Foundation.Size**](/uwp/api/Windows.Foundation.Size).</span></span> |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-148">Складывает два вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-148">Adds two vectors.</span></span> |
| `float2 operator- (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-149">Вычитает вектор из вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-149">Subtracts a vector from a vector.</span></span> |
| `float2 operator* (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-150">Умножает компоненты двух векторов друг от друга.</span><span class="sxs-lookup"><span data-stu-id="371cf-150">Multiplies the components of two vectors by each other.</span></span> |
| `float2 operator* (float2 const& value1, float value2)` | <span data-ttu-id="371cf-151">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="371cf-151">Multiplies a vector by a scalar.</span></span> |
| `float2 operator* (float value1, float2 const& value2)` | <span data-ttu-id="371cf-152">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="371cf-152">Multiplies a vector by a scalar.</span></span> |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-153">Делит компоненты вектора на компоненты другого вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float2 operator/ (float2 const& value1, float value2)` | <span data-ttu-id="371cf-154">Делит вектор на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="371cf-154">Divides a vector by a scalar value.</span></span> |
| `float2 operator- (float2 const& value)` | <span data-ttu-id="371cf-155">Возвращает вектор, указывающий в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="371cf-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float2& operator+= (float2& value1, float2 const& value2)` | <span data-ttu-id="371cf-156">На месте добавляет два вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-156">In-place adds two vectors.</span></span> |
| `float2& operator-= (float2& value1, float2 const& value2)` | <span data-ttu-id="371cf-157">На месте выполняется вычитание вектора из вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-157">In-place subtracts a vector from a vector.</span></span> |
| `float2& operator*= (float2& value1, float2 const& value2)` | <span data-ttu-id="371cf-158">На месте компоненты двух векторов умножаются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="371cf-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float2& operator*= (float2& value1, float value2)` | <span data-ttu-id="371cf-159">На месте — вектор умножается скаляром.</span><span class="sxs-lookup"><span data-stu-id="371cf-159">In-place multiplies a vector by a scalar.</span></span> |
| `float2& operator/= (float2& value1, float2 const& value2)` | <span data-ttu-id="371cf-160">На месте компоненты вектора делятся компонентами другого вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float2& operator/= (float2& value1, float value2)` | <span data-ttu-id="371cf-161">На месте вектор помещается в скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="371cf-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-162">Определяет, равны ли два экземпляра float2.</span><span class="sxs-lookup"><span data-stu-id="371cf-162">Determines whether two instances of float2 are equal.</span></span> |
| `bool operator!= (float2 const& value1, float2 const& value2)` | <span data-ttu-id="371cf-163">Определяет, являются ли два экземпляра float2 неравными.</span><span class="sxs-lookup"><span data-stu-id="371cf-163">Determines whether two instances of float2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | <span data-ttu-id="371cf-164">Преобразует float2 в объект **Microsoft. Graphics. Холст. Numerics. Vector2**.</span><span class="sxs-lookup"><span data-stu-id="371cf-164">Converts a float2 to a **Microsoft.Graphics.Canvas.Numerics.Vector2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="371cf-165">Поля</span><span class="sxs-lookup"><span data-stu-id="371cf-165">Fields</span></span>

| <span data-ttu-id="371cf-166">name</span><span class="sxs-lookup"><span data-stu-id="371cf-166">Name</span></span> | <span data-ttu-id="371cf-167">Описание</span><span class="sxs-lookup"><span data-stu-id="371cf-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="371cf-168">Компонент X вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="371cf-169">Компонент Y вектора.</span><span class="sxs-lookup"><span data-stu-id="371cf-169">Y component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="371cf-170">Требования</span><span class="sxs-lookup"><span data-stu-id="371cf-170">Requirements</span></span>

| <span data-ttu-id="371cf-171">Требование</span><span class="sxs-lookup"><span data-stu-id="371cf-171">Requirement</span></span> | <span data-ttu-id="371cf-172">Значение</span><span class="sxs-lookup"><span data-stu-id="371cf-172">Value</span></span> |
|-|-|
| <span data-ttu-id="371cf-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="371cf-173">Namespace</span></span> | <span data-ttu-id="371cf-174">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="371cf-174">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="371cf-175">Header</span><span class="sxs-lookup"><span data-stu-id="371cf-175">Header</span></span> | <dl> <span data-ttu-id="371cf-176"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="371cf-176"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="371cf-177">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="371cf-177">See also</span></span>

[<span data-ttu-id="371cf-178">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="371cf-178">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
