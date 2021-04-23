---
title: Структура float4 (Виндовснумерикс. h)
description: Вектор с четырьмя компонентами.
ms.assetid: AC07C6D0-E7FD-4582-B40D-4838F49FB8B4
keywords:
- Структура float4
topic_type:
- apiref
api_name:
- float4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4a2a4721e3ab7e5520545b42367d2432ba967f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721045"
---
# <a name="float4-structure"></a><span data-ttu-id="b9e09-104">Структура float4</span><span class="sxs-lookup"><span data-stu-id="b9e09-104">float4 structure</span></span>

<span data-ttu-id="b9e09-105">Вектор с четырьмя компонентами.</span><span class="sxs-lookup"><span data-stu-id="b9e09-105">A vector with four components.</span></span>

<span data-ttu-id="b9e09-106">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="b9e09-106">This type is available only in C++.</span></span> <span data-ttu-id="b9e09-107">Его эквивалент .NET — [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="b9e09-107">Its .NET equivalent is [System.Numerics.Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="b9e09-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="b9e09-108">Constructors</span></span>

| <span data-ttu-id="b9e09-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b9e09-109">Name</span></span> | <span data-ttu-id="b9e09-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b9e09-110">Description</span></span> |
|-|-|
| `float4()` | <span data-ttu-id="b9e09-111">Создает неинициализированную float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-111">Creates an uninitialized float4.</span></span> |
| `float4(float x, float y, float z, float w)` | <span data-ttu-id="b9e09-112">Создает объект float4 с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="b9e09-112">Creates a float4 with the specified values.</span></span> |
| `float4(float2 value, float z, float w)` | <span data-ttu-id="b9e09-113">Создает float4 с координатами x и y, скопированными из float2 и заданными значениями z и w.</span><span class="sxs-lookup"><span data-stu-id="b9e09-113">Creates a float4 with x and y copied from a float2 plus the specified z and w values.</span></span> |
| `float4(float3 value, float w)` | <span data-ttu-id="b9e09-114">Создает объект float4 с координатами x, y и z, скопированными из float3 и указанным значением w.</span><span class="sxs-lookup"><span data-stu-id="b9e09-114">Creates a float4 with x, y and z copied from a float3 plus the specified w value.</span></span> |
| `explicit float4(float value)` | <span data-ttu-id="b9e09-115">Создает float4 со всеми com. ентс, для которых задано указанное значение.</span><span class="sxs-lookup"><span data-stu-id="b9e09-115">Creates a float4 with all com.ents set to the specified value.</span></span> |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | <span data-ttu-id="b9e09-116">Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector4** в float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Vector4** to a float4.</span></span> |

## <a name="functions"></a><span data-ttu-id="b9e09-117">Функции</span><span class="sxs-lookup"><span data-stu-id="b9e09-117">Functions</span></span>

| <span data-ttu-id="b9e09-118">Имя</span><span class="sxs-lookup"><span data-stu-id="b9e09-118">Name</span></span> | <span data-ttu-id="b9e09-119">Описание</span><span class="sxs-lookup"><span data-stu-id="b9e09-119">Description</span></span> |
|-|-|
| `float length(float4 const& value)` | <span data-ttu-id="b9e09-120">Вычисляет длину вектора (евклидово distance).</span><span class="sxs-lookup"><span data-stu-id="b9e09-120">Calculates the length, or Euclidean distance, of the vector.</span></span> |
| `float length_squared(float4 const& value)` | <span data-ttu-id="b9e09-121">Вычисляет длину (или евклидово расстояние) вектора в квадрате.</span><span class="sxs-lookup"><span data-stu-id="b9e09-121">Calculates the length, or Euclidean distance, of the vector squared.</span></span> |
| `float distance(float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-122">Вычисляет евклидово расстояние между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="b9e09-122">Calculates the Euclidean distance between two vectors.</span></span> |
| `float distance_squared(float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-123">Вычисляет евклидово расстояние между двумя векторами в квадрате.</span><span class="sxs-lookup"><span data-stu-id="b9e09-123">Calculates the Euclidean distance between two vectors squared.</span></span> |
| `float dot(float4 const& vector1, float4 const& vector2)` | <span data-ttu-id="b9e09-124">Вычисляет скалярное произведение двух векторов.</span><span class="sxs-lookup"><span data-stu-id="b9e09-124">Calculates the dot product of two vectors.</span></span> |
| `float4 normalize(float4 const& vector)` | <span data-ttu-id="b9e09-125">Создает единичный вектор из указанного вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-125">Creates a unit vector from the specified vector.</span></span> |
| `float4 min(float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-126">Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="b9e09-126">Returns a vector that contains the lowest value from each matching pair of components.</span></span> |
| `float4 max(float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-127">Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов.</span><span class="sxs-lookup"><span data-stu-id="b9e09-127">Returns a vector that contains the highest value from each matching pair of components.</span></span> |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | <span data-ttu-id="b9e09-128">Разрешает значение в пределах указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="b9e09-128">Restricts a value to be within a specified range.</span></span> |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | <span data-ttu-id="b9e09-129">Выполняет линейную интерполяцию между двумя векторами.</span><span class="sxs-lookup"><span data-stu-id="b9e09-129">Performs a linear interpolation between two vectors.</span></span> |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | <span data-ttu-id="b9e09-130">Преобразует объект float4 в заданную матрицу.</span><span class="sxs-lookup"><span data-stu-id="b9e09-130">Transforms a float4 by the given matrix.</span></span> |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | <span data-ttu-id="b9e09-131">Преобразует объект float3 в заданную матрицу, возвращая float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-131">Transforms a float3 by the given matrix, returning a float4.</span></span> |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | <span data-ttu-id="b9e09-132">Преобразует объект float2 в заданную матрицу, возвращая float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-132">Transforms a float2 by the given matrix, returning a float4.</span></span> |
| `float4 transform(float4 const& value, quaternion const& rotation)` | <span data-ttu-id="b9e09-133">Преобразует float4 в заданный кватернион.</span><span class="sxs-lookup"><span data-stu-id="b9e09-133">Transforms a float4 by the given quaternion.</span></span> |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | <span data-ttu-id="b9e09-134">Преобразует float3 в заданном кватернион, возвращая float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-134">Transforms a float3 by the given quaternion, returning a float4.</span></span> |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | <span data-ttu-id="b9e09-135">Преобразует float2 в заданном кватернион, возвращая float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-135">Transforms a float2 by the given quaternion, returning a float4.</span></span> |

## <a name="methods"></a><span data-ttu-id="b9e09-136">Методы</span><span class="sxs-lookup"><span data-stu-id="b9e09-136">Methods</span></span>

| <span data-ttu-id="b9e09-137">Имя</span><span class="sxs-lookup"><span data-stu-id="b9e09-137">Name</span></span> | <span data-ttu-id="b9e09-138">Описание</span><span class="sxs-lookup"><span data-stu-id="b9e09-138">Description</span></span> |
|-|-|
| `static float4 zero()` | <span data-ttu-id="b9e09-139">Возвращает float4 со всеми его компонентами, для которых задано значение 0.</span><span class="sxs-lookup"><span data-stu-id="b9e09-139">Returns a float4 with all of its components set to zero.</span></span> |
| `static float4 one()` | <span data-ttu-id="b9e09-140">Возвращает float4 со всеми его компонентами, для которых задано значение One.</span><span class="sxs-lookup"><span data-stu-id="b9e09-140">Returns a float4 with all of its components set to one.</span></span> |
| `static float4 unit_x()` | <span data-ttu-id="b9e09-141">Возвращает float4 (1, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="b9e09-141">Returns the float4 (1, 0, 0, 0).</span></span> |
| `static float4 unit_y()` | <span data-ttu-id="b9e09-142">Возвращает float4 (0, 1, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="b9e09-142">Returns the float4 (0, 1, 0, 0).</span></span> |
| `static float4 unit_z()` | <span data-ttu-id="b9e09-143">Возвращает float4 (0, 0, 1, 0).</span><span class="sxs-lookup"><span data-stu-id="b9e09-143">Returns the float4 (0, 0, 1, 0).</span></span> |
| `static float4 unit_w()` | <span data-ttu-id="b9e09-144">Возвращает float4 (0, 0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="b9e09-144">Returns the float4 (0, 0, 0, 1).</span></span> |

## <a name="operators"></a><span data-ttu-id="b9e09-145">Операторы</span><span class="sxs-lookup"><span data-stu-id="b9e09-145">Operators</span></span>

| <span data-ttu-id="b9e09-146">Имя</span><span class="sxs-lookup"><span data-stu-id="b9e09-146">Name</span></span> | <span data-ttu-id="b9e09-147">Описание</span><span class="sxs-lookup"><span data-stu-id="b9e09-147">Description</span></span> |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-148">Складывает два вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-148">Adds two vectors.</span></span> |
| `float4 operator- (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-149">Вычитает вектор из вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-149">Subtracts a vector from a vector.</span></span> |
| `float4 operator* (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-150">Умножает компоненты двух векторов друг от друга.</span><span class="sxs-lookup"><span data-stu-id="b9e09-150">Multiplies the components of two vectors by each other.</span></span> |
| `float4 operator* (float4 const& value1, float value2)` | <span data-ttu-id="b9e09-151">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="b9e09-151">Multiplies a vector by a scalar.</span></span> |
| `float4 operator* (float value1, float4 const& value2)` | <span data-ttu-id="b9e09-152">Умножает вектор на скалярный.</span><span class="sxs-lookup"><span data-stu-id="b9e09-152">Multiplies a vector by a scalar.</span></span> |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-153">Делит компоненты вектора на компоненты другого вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-153">Divides the components of a vector by the components of another vector.</span></span> |
| `float4 operator/ (float4 const& value1, float value2)` | <span data-ttu-id="b9e09-154">Делит вектор на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="b9e09-154">Divides a vector by a scalar value.</span></span> |
| `float4 operator- (float4 const& value)` | <span data-ttu-id="b9e09-155">Возвращает вектор, указывающий в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="b9e09-155">Returns a vector pointing in the opposite direction.</span></span> |
| `float4& operator+= (float4& value1, float4 const& value2)` | <span data-ttu-id="b9e09-156">На месте добавляет два вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-156">In-place adds two vectors.</span></span> |
| `float4& operator-= (float4& value1, float4 const& value2)` | <span data-ttu-id="b9e09-157">На месте выполняется вычитание вектора из вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-157">In-place subtracts a vector from a vector.</span></span> |
| `float4& operator*= (float4& value1, float4 const& value2)` | <span data-ttu-id="b9e09-158">На месте компоненты двух векторов умножаются друг на друга.</span><span class="sxs-lookup"><span data-stu-id="b9e09-158">In-place multiplies the components of two vectors by each other.</span></span> |
| `float4& operator*= (float4& value1, float value2)` | <span data-ttu-id="b9e09-159">На месте — вектор умножается скаляром.</span><span class="sxs-lookup"><span data-stu-id="b9e09-159">In-place multiplies a vector by a scalar.</span></span> |
| `float4& operator/= (float4& value1, float4 const& value2)` | <span data-ttu-id="b9e09-160">На месте компоненты вектора делятся компонентами другого вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-160">In-place divides the components of a vector by the components of another vector.</span></span> |
| `float4& operator/= (float4& value1, float value2)` | <span data-ttu-id="b9e09-161">На месте вектор помещается в скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="b9e09-161">In-place divides a vector by a scalar value.</span></span> |
| `bool operator== (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-162">Определяет, равны ли два экземпляра float4.</span><span class="sxs-lookup"><span data-stu-id="b9e09-162">Determines whether two instances of float4 are equal.</span></span> |
| `bool operator!= (float4 const& value1, float4 const& value2)` | <span data-ttu-id="b9e09-163">Определяет, являются ли два экземпляра float4 неравными.</span><span class="sxs-lookup"><span data-stu-id="b9e09-163">Determines whether two instances of float4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | <span data-ttu-id="b9e09-164">Преобразует float4 в объект **Microsoft. Graphics. Холст. Numerics. Vector4**.</span><span class="sxs-lookup"><span data-stu-id="b9e09-164">Converts a float4 to a **Microsoft.Graphics.Canvas.Numerics.Vector4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="b9e09-165">Поля</span><span class="sxs-lookup"><span data-stu-id="b9e09-165">Fields</span></span>

| <span data-ttu-id="b9e09-166">name</span><span class="sxs-lookup"><span data-stu-id="b9e09-166">Name</span></span> | <span data-ttu-id="b9e09-167">Описание</span><span class="sxs-lookup"><span data-stu-id="b9e09-167">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="b9e09-168">Компонент X вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-168">X component of the vector.</span></span> |
| `float y` | <span data-ttu-id="b9e09-169">Компонент Y вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-169">Y component of the vector.</span></span> |
| `float z` | <span data-ttu-id="b9e09-170">Компонент по оси Z вектора.</span><span class="sxs-lookup"><span data-stu-id="b9e09-170">Z component of the vector.</span></span> |
| `float w` | <span data-ttu-id="b9e09-171">Компонент вектора «W».</span><span class="sxs-lookup"><span data-stu-id="b9e09-171">W component of the vector.</span></span> |

## <a name="requirements"></a><span data-ttu-id="b9e09-172">Требования</span><span class="sxs-lookup"><span data-stu-id="b9e09-172">Requirements</span></span>

| <span data-ttu-id="b9e09-173">Требование</span><span class="sxs-lookup"><span data-stu-id="b9e09-173">Requirement</span></span> | <span data-ttu-id="b9e09-174">Значение</span><span class="sxs-lookup"><span data-stu-id="b9e09-174">Value</span></span> |
|-|-|
| <span data-ttu-id="b9e09-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b9e09-175">Namespace</span></span> | <span data-ttu-id="b9e09-176">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="b9e09-176">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="b9e09-177">Header</span><span class="sxs-lookup"><span data-stu-id="b9e09-177">Header</span></span> | <dl> <span data-ttu-id="b9e09-178"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e09-178"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="b9e09-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b9e09-179">See also</span></span>

[<span data-ttu-id="b9e09-180">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="b9e09-180">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
