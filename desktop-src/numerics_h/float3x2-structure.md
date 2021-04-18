---
title: Структура float3x2 (Виндовснумерикс. h)
description: Матрица 3x2, используемая для двумерных преобразований.
ms.assetid: 5C2A4C30-3EC4-4DE9-A42A-6A19F96F8D69
keywords:
- Структура float3x2
topic_type:
- apiref
api_name:
- float3x2 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9351fae9636ca2512825c7df5383eddf1558583e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721051"
---
# <a name="float3x2-structure"></a><span data-ttu-id="7c968-104">Структура float3x2</span><span class="sxs-lookup"><span data-stu-id="7c968-104">float3x2 structure</span></span>

<span data-ttu-id="7c968-105">Матрица 3x2, используемая для двумерных преобразований.</span><span class="sxs-lookup"><span data-stu-id="7c968-105">A 3x2 matrix, used for 2D transforms.</span></span>

<span data-ttu-id="7c968-106">Этот тип матрицы использует макет вектора строк.</span><span class="sxs-lookup"><span data-stu-id="7c968-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="7c968-107">X и y вектора перевода этой матрицы соответствуют полям M31, M32.</span><span class="sxs-lookup"><span data-stu-id="7c968-107">The x and y of this matrix's translation vector correspond to the fields m31, m32.</span></span>

<span data-ttu-id="7c968-108">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="7c968-108">This type is available only in C++.</span></span> <span data-ttu-id="7c968-109">Его эквивалент .NET — [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="7c968-109">Its .NET equivalent is [System.Numerics.Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="7c968-110">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="7c968-110">Constructors</span></span>

| <span data-ttu-id="7c968-111">Имя</span><span class="sxs-lookup"><span data-stu-id="7c968-111">Name</span></span> | <span data-ttu-id="7c968-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7c968-112">Description</span></span> |
|-|-|
| `float3x2()` | <span data-ttu-id="7c968-113">Создает неинициализированную float3x2.</span><span class="sxs-lookup"><span data-stu-id="7c968-113">Creates an uninitialized float3x2.</span></span> |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | <span data-ttu-id="7c968-114">Создает объект float3x2 с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="7c968-114">Creates a float3x2 with the specified values.</span></span> |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | <span data-ttu-id="7c968-115">Преобразует объект **Microsoft. Graphics. Холст. Numerics. Matrix3x2** в float3x2.</span><span class="sxs-lookup"><span data-stu-id="7c968-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2** to a float3x2.</span></span> |

## <a name="functions"></a><span data-ttu-id="7c968-116">Функции</span><span class="sxs-lookup"><span data-stu-id="7c968-116">Functions</span></span>

| <span data-ttu-id="7c968-117">Имя</span><span class="sxs-lookup"><span data-stu-id="7c968-117">Name</span></span> | <span data-ttu-id="7c968-118">Описание</span><span class="sxs-lookup"><span data-stu-id="7c968-118">Description</span></span> |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | <span data-ttu-id="7c968-119">Создает матрицу трансляции.</span><span class="sxs-lookup"><span data-stu-id="7c968-119">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | <span data-ttu-id="7c968-120">Создает матрицу трансляции.</span><span class="sxs-lookup"><span data-stu-id="7c968-120">Creates a translation matrix.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | <span data-ttu-id="7c968-121">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="7c968-121">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | <span data-ttu-id="7c968-122">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="7c968-122">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales)` | <span data-ttu-id="7c968-123">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="7c968-123">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | <span data-ttu-id="7c968-124">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="7c968-124">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_scale(float scale)` | <span data-ttu-id="7c968-125">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="7c968-125">Creates a scaling matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | <span data-ttu-id="7c968-126">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="7c968-126">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | <span data-ttu-id="7c968-127">Создает матрицу отклонения, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="7c968-127">Creates a skew matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | <span data-ttu-id="7c968-128">Создает матрицу отклонения, центрированную по заданной точке.</span><span class="sxs-lookup"><span data-stu-id="7c968-128">Creates a skew matrix, centered on the specified point.</span></span> |
| `float3x2 make_float3x2_rotation(float radians)` | <span data-ttu-id="7c968-129">Создает матрицу вращения, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="7c968-129">Creates a rotation matrix, centered on the origin.</span></span> |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | <span data-ttu-id="7c968-130">Создает матрицу вращения, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="7c968-130">Creates a rotation matrix, centered on the specified point.</span></span> |
| `bool is_identity(float3x2 const& value)` | <span data-ttu-id="7c968-131">Проверяет, является ли это матрицей удостоверений.</span><span class="sxs-lookup"><span data-stu-id="7c968-131">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float3x2 const& value)` | <span data-ttu-id="7c968-132">Вычисляет определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-132">Calculates the determinant of the matrix.</span></span> |
| `float2 translation(float3x2 const& value)` | <span data-ttu-id="7c968-133">Возвращает вектор смещения матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-133">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | <span data-ttu-id="7c968-134">Вычисляет обратную матрицу.</span><span class="sxs-lookup"><span data-stu-id="7c968-134">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="7c968-135">Возвращает значение true, если матрица может быть инвертирована; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="7c968-135">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | <span data-ttu-id="7c968-136">Линейная интерполяция между соответствующими значениями двух матриц.</span><span class="sxs-lookup"><span data-stu-id="7c968-136">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="7c968-137">Методы</span><span class="sxs-lookup"><span data-stu-id="7c968-137">Methods</span></span>

| <span data-ttu-id="7c968-138">Имя</span><span class="sxs-lookup"><span data-stu-id="7c968-138">Name</span></span> | <span data-ttu-id="7c968-139">Описание</span><span class="sxs-lookup"><span data-stu-id="7c968-139">Description</span></span> |
|-|-|
| `static float3x2 identity()` | <span data-ttu-id="7c968-140">Возвращает экземпляр матрицы идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="7c968-140">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="7c968-141">Операторы</span><span class="sxs-lookup"><span data-stu-id="7c968-141">Operators</span></span>

| <span data-ttu-id="7c968-142">Имя</span><span class="sxs-lookup"><span data-stu-id="7c968-142">Name</span></span> | <span data-ttu-id="7c968-143">Описание</span><span class="sxs-lookup"><span data-stu-id="7c968-143">Description</span></span> |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-144">Добавляет каждый компонент матрицы в другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="7c968-144">Adds each component of a matrix to another matrix.</span></span> |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-145">Вычитает каждый компонент матрицы из другой матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-145">Subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-146">Умножает матрицу на другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="7c968-146">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7c968-147">Это влияет на объединение двух преобразований.</span><span class="sxs-lookup"><span data-stu-id="7c968-147">This has the effect of concatenating two transforms.</span></span> |
| `float3x2 operator* (float3x2 const& value1, float value2)` | <span data-ttu-id="7c968-148">Умножает каждый компонент матрицы на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="7c968-148">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float3x2 operator- (float3x2 const& value)` | <span data-ttu-id="7c968-149">Инвертирует каждый компонент матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-149">Negates each component of a matrix.</span></span> |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-150">На месте добавляет каждый компонент матрицы в другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="7c968-150">In-place adds each component of a matrix to another matrix.</span></span> |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-151">На месте вычитается каждый компонент матрицы из другой матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-151">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-152">На месте матрица умножается на другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="7c968-152">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="7c968-153">Это влияет на объединение двух преобразований.</span><span class="sxs-lookup"><span data-stu-id="7c968-153">This has the effect of concatenating two transforms.</span></span> |
| `float3x2& operator*= (float3x2& value1, float value2)` | <span data-ttu-id="7c968-154">На месте каждый компонент матрицы умножается на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="7c968-154">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-155">Определяет, равны ли два экземпляра float3x2.</span><span class="sxs-lookup"><span data-stu-id="7c968-155">Determines whether two instances of float3x2 are equal.</span></span> |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | <span data-ttu-id="7c968-156">Определяет, являются ли два экземпляра float3x2 неравными.</span><span class="sxs-lookup"><span data-stu-id="7c968-156">Determines whether two instances of float3x2 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | <span data-ttu-id="7c968-157">Преобразует float3x2 в объект **Microsoft. Graphics. Холст. Numerics. Matrix3x2**.</span><span class="sxs-lookup"><span data-stu-id="7c968-157">Converts a float3x2 to a **Microsoft.Graphics.Canvas.Numerics.Matrix3x2**.</span></span> |

## <a name="fields"></a><span data-ttu-id="7c968-158">Поля</span><span class="sxs-lookup"><span data-stu-id="7c968-158">Fields</span></span>

| <span data-ttu-id="7c968-159">name</span><span class="sxs-lookup"><span data-stu-id="7c968-159">Name</span></span> | <span data-ttu-id="7c968-160">Описание</span><span class="sxs-lookup"><span data-stu-id="7c968-160">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="7c968-161">Значение в строке 1 столбца 1 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-161">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="7c968-162">Значение в строке 1 столбца 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-162">Value at row 1 column 2 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="7c968-163">Значение в столбце 1 строки 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-163">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="7c968-164">Значение для столбца 2 в строке 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-164">Value at row 2 column 2 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="7c968-165">Значение в столбце 1 строки 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-165">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="7c968-166">Значение в столбце 2 строки 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="7c968-166">Value at row 3 column 2 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="7c968-167">Требования</span><span class="sxs-lookup"><span data-stu-id="7c968-167">Requirements</span></span>

| <span data-ttu-id="7c968-168">Требование</span><span class="sxs-lookup"><span data-stu-id="7c968-168">Requirement</span></span> | <span data-ttu-id="7c968-169">Значение</span><span class="sxs-lookup"><span data-stu-id="7c968-169">Value</span></span> |
|-|-|
| <span data-ttu-id="7c968-170">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7c968-170">Namespace</span></span> | <span data-ttu-id="7c968-171">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="7c968-171">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="7c968-172">Header</span><span class="sxs-lookup"><span data-stu-id="7c968-172">Header</span></span> | <dl> <span data-ttu-id="7c968-173"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c968-173"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="7c968-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c968-174">See also</span></span>

[<span data-ttu-id="7c968-175">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="7c968-175">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
