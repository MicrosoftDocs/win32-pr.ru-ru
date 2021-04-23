---
title: Структура float3 (Виндовснумерикс. h)
description: Вектор с тремя компонентами.
ms.assetid: CAA10ADA-C5A8-4B75-A0A9-5C5B3FDD9A07
keywords:
- Структура float3
topic_type:
- apiref
api_name:
- float3 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ae524205c900c63438a50094dcd551a4903632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721052"
---
# <a name="float3-structure"></a><span data-ttu-id="6e918-104">Структура float3</span><span class="sxs-lookup"><span data-stu-id="6e918-104">float3 structure</span></span>

<span data-ttu-id="6e918-105">Вектор с тремя компонентами.</span><span class="sxs-lookup"><span data-stu-id="6e918-105">A vector with three components.</span></span>

<span data-ttu-id="6e918-106">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="6e918-106">This type is available only in C++.</span></span> <span data-ttu-id="6e918-107">Его эквивалент .NET — [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="6e918-107">Its .NET equivalent is [System.Numerics.Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="6e918-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="6e918-108">Constructors</span></span>

| <span data-ttu-id="6e918-109">Имя</span><span class="sxs-lookup"><span data-stu-id="6e918-109">Name</span></span> | <span data-ttu-id="6e918-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6e918-110">Description</span></span> |
|-|-|
| `float3()` | <span data-ttu-id="6e918-111">Создает неинициализированную float3.</span><span class="sxs-lookup"><span data-stu-id="6e918-111">Creates an uninitialized float3.</span></span> |
| `float3(float x, float y, float z)` | <span data-ttu-id="6e918-112">Создает объект float3 с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="6e918-112">Creates a float3 with the specified values.</span></span> |
| `float3(float2 value, float z)` | <span data-ttu-id="6e918-113">Создает float3 с координатами x и y, скопированными из float2 и указанным значением z.</span><span class="sxs-lookup"><span data-stu-id="6e918-113">Creates a float3 with x and y copied from a float2 plus the specified z value.</span></span> |
| `explicit float3(float value)` | <span data-ttu-id="6e918-114">Создает float3 со всеми компонентами, для которых задано указанное значение.</span><span class="sxs-lookup"><span data-stu-id="6e918-114">Creates a float3 with all components set to the specified value.</span></span> |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | <span data-ttu-id="6e918-115">Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector3** в float3.</span><span class="sxs-lookup"><span data-stu-id="6e918-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector3** to a float3.</span></span> |

## <a name="functions"></a><span data-ttu-id="6e918-116">Функции</span><span class="sxs-lookup"><span data-stu-id="6e918-116">Functions</span></span>

| <span data-ttu-id="6e918-117">Имя</span><span class="sxs-lookup"><span data-stu-id="6e918-117">Name</span></span> | <span data-ttu-id="6e918-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6e918-118">Description</span></span> |
|-|-|
| `float length(float3 const& value)` | <span data-ttu-id="6e918-119">Вычисляет длину вектора (евклидово distance).</span><span class="sxs-lookup"><span data-stu-id="6e918-119">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float3 const& value)` | <span data-ttu-id="6e918-120">Вычисляет длину (или евклидово расстояние) вектора в квадрате.</span><span class="sxs-lookup"><span data-stu-id="6e918-120">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-121">Вычисляет евклидово расстояние между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="6e918-121">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-122">Вычисляет евклидово расстояние между двумя векторами в квадрате.</span><span class="sxs-lookup"><span data-stu-id="6e918-122">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="6e918-123">Вычисляет скалярное произведение двух векторов.</span><span class="sxs-lookup"><span data-stu-id="6e918-123">Calculates the dot product of two vectors.</span></span> |
| `float3 normalize(float3 const& value)` | <span data-ttu-id="6e918-124">Создает единичный вектор из указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-124">Creates a unit vector from the specified vector.</span></span> |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | <span data-ttu-id="6e918-125">Вычисляет векторное произведение двух векторов.</span><span class="sxs-lookup"><span data-stu-id="6e918-125">Calculates the cross product of two vectors.</span></span> |
| `float3 reflect(float3 const& vector, float3 const& normal)` | <span data-ttu-id="6e918-126">Определяет вектор отражения заданного вектора и нормали.</span><span class="sxs-lookup"><span data-stu-id="6e918-126">Determines the reflect vector of the given vector and normal.</span></span> |
| `float3 min(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-127">Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="6e918-127">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float3 max(float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-128">Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="6e918-128">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | <span data-ttu-id="6e918-129">Разрешает значение в пределах указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="6e918-129">Restricts a value to be within a specified range.</span></span> |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | <span data-ttu-id="6e918-130">Выполняет линейную интерполяцию между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="6e918-130">Performs a linear interpolation between two vectors.</span></span> |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="6e918-131">Преобразует вектор (x, y, z, 1) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="6e918-131">Transforms the vector (x, y, z, 1) by the specified matrix.</span></span> |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | <span data-ttu-id="6e918-132">Преобразует Стандартный вектор (x, y, z, 0) в указанную матрицу.</span><span class="sxs-lookup"><span data-stu-id="6e918-132">Transforms the normal vector (x, y, z, 0) by the specified matrix.</span></span> |
| `float3 transform(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="6e918-133">Преобразует float3 в заданный кватернион.</span><span class="sxs-lookup"><span data-stu-id="6e918-133">Transforms a float3 by the given quaternion.</span></span> |

## <a name="methods"></a><span data-ttu-id="6e918-134">Методы</span><span class="sxs-lookup"><span data-stu-id="6e918-134">Methods</span></span>

| <span data-ttu-id="6e918-135">Имя</span><span class="sxs-lookup"><span data-stu-id="6e918-135">Name</span></span> | <span data-ttu-id="6e918-136">Описание</span><span class="sxs-lookup"><span data-stu-id="6e918-136">Description</span></span> |
|-|-|
| `static float3 zero()` | <span data-ttu-id="6e918-137">Возвращает float3 со всеми его компонентами, для которых задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="6e918-137">Returns a float3 with all of its components set to zero.</span></span> |
| `static float3 one()` | <span data-ttu-id="6e918-138">Возвращает float3 со всеми его компонентами, для которых задано значение One.</span><span class="sxs-lookup"><span data-stu-id="6e918-138">Returns a float3 with all of its components set to one.</span></span> |
| `static float3 unit_x()` | <span data-ttu-id="6e918-139">Возвращает float3 (1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="6e918-139">Returns the float3 (1, 0, 0).</span></span> |
| `static float3 unit_y()` | <span data-ttu-id="6e918-140">Возвращает float3 (0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="6e918-140">Returns the float3 (0, 1, 0).</span></span> |
| `static float3 unit_z()` | <span data-ttu-id="6e918-141">Возвращает float3 (0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="6e918-141">Returns the float3 (0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="6e918-142">Операторы</span><span class="sxs-lookup"><span data-stu-id="6e918-142">Operators</span></span>

| <span data-ttu-id="6e918-143">Имя</span><span class="sxs-lookup"><span data-stu-id="6e918-143">Name</span></span> | <span data-ttu-id="6e918-144">Описание</span><span class="sxs-lookup"><span data-stu-id="6e918-144">Description</span></span> |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-145">Складывает два вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-145">Adds two vectors.</span></span> |
| `float3 operator- (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-146">Вычитает вектор из вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-146">Subtracts a vector from a vector.</span></span> |
| `float3 operator* (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-147">Умножает компоненты двух векторов друг от друга.</span><span class="sxs-lookup"><span data-stu-id="6e918-147">Multiplies the components of two vectors by each other.</span></span> |
| `float3 operator* (float3 const& value1, float value2)` | <span data-ttu-id="6e918-148">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="6e918-148">Multiplies a vector by a scalar.</span></span> |
| `float3 operator* (float value1, float3 const& value2)` | <span data-ttu-id="6e918-149">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="6e918-149">Multiplies a vector by a scalar.</span></span> |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-150">Делит компоненты вектора на компоненты другого вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-150">Divides the components of a vector by the components of another vector.</span></span> |
| `float3 operator/ (float3 const& value1, float value2)` | <span data-ttu-id="6e918-151">Делит вектор на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="6e918-151">Divides a vector by a scalar value.</span></span> |
| `float3 operator- (float3 const& value)` | <span data-ttu-id="6e918-152">Возвращает вектор, указывающий в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="6e918-152">Returns a vector pointing in the opposite direction.</span></span> |
| `float3& operator+= (float3& value1, float3 const& value2)` | <span data-ttu-id="6e918-153">На месте добавляет два вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-153">In-place adds two vectors.</span></span> |
| `float3& operator-= (float3& value1, float3 const& value2)` | <span data-ttu-id="6e918-154">На месте выполняется вычитание вектора из вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-154">In-place subtracts a vector from a vector.</span></span> |
| `float3& operator*= (float3& value1, float3 const& value2)` | <span data-ttu-id="6e918-155">На месте компоненты двух векторов умножаются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="6e918-155">In-place multiplies the components of two vectors by each other.</span></span> |
| `float3& operator*= (float3& value1, float value2)` | <span data-ttu-id="6e918-156">На месте — вектор умножается скаляром.</span><span class="sxs-lookup"><span data-stu-id="6e918-156">In-place multiplies a vector by a scalar.</span></span> |
| `float3& operator/= (float3& value1, float3 const& value2)` | <span data-ttu-id="6e918-157">На месте компоненты вектора делятся компонентами другого вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-157">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float3& operator/= (float3& value1, float value2)` | <span data-ttu-id="6e918-158">На месте вектор помещается в скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="6e918-158">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-159">Определяет, равны ли два экземпляра float3.</span><span class="sxs-lookup"><span data-stu-id="6e918-159">Determines whether two instances of float3 are equal.</span></span> |
| `bool operator!= (float3 const& value1, float3 const& value2)` | <span data-ttu-id="6e918-160">Определяет, являются ли два экземпляра float3 неравными.</span><span class="sxs-lookup"><span data-stu-id="6e918-160">Determines whether two instances of float3 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | <span data-ttu-id="6e918-161">Преобразует float3 в объект **Microsoft. Graphics. Холст. Numerics. Vector3**.</span><span class="sxs-lookup"><span data-stu-id="6e918-161">Converts a float3 to a **Microsoft.Graphics.Canvas.Numerics.Vector3**.</span></span> |

## <a name="fields"></a><span data-ttu-id="6e918-162">Поля</span><span class="sxs-lookup"><span data-stu-id="6e918-162">Fields</span></span>

| <span data-ttu-id="6e918-163">name</span><span class="sxs-lookup"><span data-stu-id="6e918-163">Name</span></span> | <span data-ttu-id="6e918-164">Описание</span><span class="sxs-lookup"><span data-stu-id="6e918-164">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="6e918-165">Компонент X вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-165">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="6e918-166">Компонент Y вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-166">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="6e918-167">Компонент по оси Z вектора.</span><span class="sxs-lookup"><span data-stu-id="6e918-167">Z component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6e918-168">Требования</span><span class="sxs-lookup"><span data-stu-id="6e918-168">Requirements</span></span>

| <span data-ttu-id="6e918-169">Требование</span><span class="sxs-lookup"><span data-stu-id="6e918-169">Requirement</span></span> | <span data-ttu-id="6e918-170">Значение</span><span class="sxs-lookup"><span data-stu-id="6e918-170">Value</span></span> |
|-|-|
| <span data-ttu-id="6e918-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e918-171">Namespace</span></span> | <span data-ttu-id="6e918-172">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="6e918-172">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="6e918-173">Header</span><span class="sxs-lookup"><span data-stu-id="6e918-173">Header</span></span> | <dl> <span data-ttu-id="6e918-174"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e918-174"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="6e918-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e918-175">See also</span></span>

[<span data-ttu-id="6e918-176">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="6e918-176">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
