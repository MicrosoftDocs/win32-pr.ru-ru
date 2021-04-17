---
title: Структура float4x4 (Виндовснумерикс. h)
description: Матрица 4x4, используемая для трехмерных преобразований.
ms.assetid: C0D2198A-B547-4153-AD02-9A47835FD272
keywords:
- Структура float4x4
topic_type:
- apiref
api_name:
- float4x4 structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71c91de5eef404db33eff118568540be912d551d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721044"
---
# <a name="float4x4-structure"></a><span data-ttu-id="2ecab-104">Структура float4x4</span><span class="sxs-lookup"><span data-stu-id="2ecab-104">float4x4 structure</span></span>

<span data-ttu-id="2ecab-105">Матрица 4x4, используемая для трехмерных преобразований.</span><span class="sxs-lookup"><span data-stu-id="2ecab-105">A 4x4 matrix, used for 3D transforms.</span></span>

<span data-ttu-id="2ecab-106">Этот тип матрицы использует макет вектора строк.</span><span class="sxs-lookup"><span data-stu-id="2ecab-106">This matrix type uses a row vector layout.</span></span> <span data-ttu-id="2ecab-107">X, y и z этого вектора перевода матрицы соответствуют полям M41, M42, M43.</span><span class="sxs-lookup"><span data-stu-id="2ecab-107">The x, y, and z of this matrix's translation vector correspond to the fields m41, m42, m43.</span></span>

<span data-ttu-id="2ecab-108">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="2ecab-108">This type is available only in C++.</span></span> <span data-ttu-id="2ecab-109">Его эквивалент .NET — [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="2ecab-109">Its .NET equivalent is [System.Numerics.Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="2ecab-110">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="2ecab-110">Constructors</span></span>

| <span data-ttu-id="2ecab-111">Имя</span><span class="sxs-lookup"><span data-stu-id="2ecab-111">Name</span></span> | <span data-ttu-id="2ecab-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecab-112">Description</span></span> |
|-|-|
| `float4x4()` | <span data-ttu-id="2ecab-113">Создает неинициализированную float4x4.</span><span class="sxs-lookup"><span data-stu-id="2ecab-113">Creates an uninitialized float4x4.</span></span> |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | <span data-ttu-id="2ecab-114">Создает объект float4x4 с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="2ecab-114">Creates a float4x4 with the specified values.</span></span> |
| `explicit float4x4(float3x2 value)` | <span data-ttu-id="2ecab-115">Создает float4x4 из float3x2.</span><span class="sxs-lookup"><span data-stu-id="2ecab-115">Creates a float4x4 from a float3x2.</span></span> |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | <span data-ttu-id="2ecab-116">Преобразует объект **Microsoft. Graphics. Холст. Numerics. Matrix4x4** в float4x4.</span><span class="sxs-lookup"><span data-stu-id="2ecab-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4** to a float4x4.</span></span> |

## <a name="functions"></a><span data-ttu-id="2ecab-117">Функции</span><span class="sxs-lookup"><span data-stu-id="2ecab-117">Functions</span></span>

| <span data-ttu-id="2ecab-118">Имя</span><span class="sxs-lookup"><span data-stu-id="2ecab-118">Name</span></span> | <span data-ttu-id="2ecab-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecab-119">Description</span></span> |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | <span data-ttu-id="2ecab-120">Создает сферическую рекламу, которая поворачивается вокруг указанного расположения объекта, используя правую систему координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-120">Creates a spherical billboard that rotates around a specified object position, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | <span data-ttu-id="2ecab-121">Создает цилиндрическое объявление, которое поворачивается вокруг заданной оси с помощью правой руки системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-121">Creates a cylindrical billboard that rotates around a specified axis, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_translation(float3 const& position)` | <span data-ttu-id="2ecab-122">Создает матрицу трансляции.</span><span class="sxs-lookup"><span data-stu-id="2ecab-122">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | <span data-ttu-id="2ecab-123">Создает матрицу трансляции.</span><span class="sxs-lookup"><span data-stu-id="2ecab-123">Creates a translation matrix.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | <span data-ttu-id="2ecab-124">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-124">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | <span data-ttu-id="2ecab-125">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-125">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales)` | <span data-ttu-id="2ecab-126">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-126">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | <span data-ttu-id="2ecab-127">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-127">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_scale(float scale)` | <span data-ttu-id="2ecab-128">Создает матрицу масштабирования, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-128">Creates a scaling matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | <span data-ttu-id="2ecab-129">Создает матрицу масштабирования, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-129">Creates a scaling matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians)` | <span data-ttu-id="2ecab-130">Создает матрицу вращения по оси x, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-130">Creates an x-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | <span data-ttu-id="2ecab-131">Создает матрицу вращения по оси x, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-131">Creates an x-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians)` | <span data-ttu-id="2ecab-132">Создает матрицу вращения по оси y, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-132">Creates a y-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | <span data-ttu-id="2ecab-133">Создает матрицу вращения по оси y, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-133">Creates a y-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians)` | <span data-ttu-id="2ecab-134">Создает матрицу поворота оси z, центрированную по источнику.</span><span class="sxs-lookup"><span data-stu-id="2ecab-134">Creates a z-axis rotation matrix, centered on the origin.</span></span> |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | <span data-ttu-id="2ecab-135">Создает матрицу поворота оси z, центрированную по указанной точке.</span><span class="sxs-lookup"><span data-stu-id="2ecab-135">Creates a z-axis rotation matrix, centered on the specified point.</span></span> |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="2ecab-136">Создает матрицу, которая вращается вокруг произвольного вектора.</span><span class="sxs-lookup"><span data-stu-id="2ecab-136">Creates a matrix that rotates around an arbitrary vector.</span></span> |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="2ecab-137">Создает матрицу перспективной проекции на основе поля представления с помощью правой правильной системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-137">Creates a perspective projection matrix based on a field of view, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="2ecab-138">Создает матрицу перспективной проекции с использованием правой рукой системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-138">Creates a perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | <span data-ttu-id="2ecab-139">Создает настраиваемую матрицу перспективной проекции с использованием правой рукой системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-139">Creates a customized perspective projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | <span data-ttu-id="2ecab-140">Создает матрицу ортогональной проекции с использованием правой рукой системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-140">Creates an orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | <span data-ttu-id="2ecab-141">Создает настраиваемую матрицу ортогональной проекции с использованием правой рукой системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-141">Creates a customized orthographic projection matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | <span data-ttu-id="2ecab-142">Создает матрицу представления с помощью правой правильной системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-142">Creates a view matrix, using a right handed coordinate system.</span></span> |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | <span data-ttu-id="2ecab-143">Создает матрицу мира с помощью правой правильной системы координат.</span><span class="sxs-lookup"><span data-stu-id="2ecab-143">Creates a world matrix, using a right handed coordinate system.</span></span> <span data-ttu-id="2ecab-144">Это можно использовать для размещения объектов в трехмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="2ecab-144">This can be used to position objects in 3D space.</span></span> |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | <span data-ttu-id="2ecab-145">Создает матрицу вращения из кватерниона.</span><span class="sxs-lookup"><span data-stu-id="2ecab-145">Creates a rotation matrix from a quaternion.</span></span> |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="2ecab-146">Создает матрицу вращения на основе указанного значения нутации, высоты и рулона.</span><span class="sxs-lookup"><span data-stu-id="2ecab-146">Creates a rotation matrix from a specified yaw, pitch, and roll.</span></span> |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | <span data-ttu-id="2ecab-147">Создает матрицу, которая создает проекцию геометрической фигуры на указанной плоскости подобно отбрасыванию тени от указанного источника света.</span><span class="sxs-lookup"><span data-stu-id="2ecab-147">Creates a matrix that flattens geometry into a specified plane as if casting a shadow from a specified light source.</span></span> |
| `float4x4 make_float4x4_reflection(plane const& value)` | <span data-ttu-id="2ecab-148">Создает матрицу, отражающую систему координат для указанной плоскости.</span><span class="sxs-lookup"><span data-stu-id="2ecab-148">Creates a matrix that reflects the coordinate system about a specified plane.</span></span> |
| `bool is_identity(float4x4 const& value)` | <span data-ttu-id="2ecab-149">Проверяет, является ли это матрицей удостоверений.</span><span class="sxs-lookup"><span data-stu-id="2ecab-149">Checks whether this is an identity matrix.</span></span> |
| `float determinant(float4x4 const& value)` | <span data-ttu-id="2ecab-150">Вычисляет определитель матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-150">Calculates the determinant of the matrix.</span></span> |
| `float3 translation(float4x4 const& value)` | <span data-ttu-id="2ecab-151">Возвращает вектор смещения матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-151">Gets the translation vector of the matrix.</span></span> |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | <span data-ttu-id="2ecab-152">Вычисляет обратную матрицу.</span><span class="sxs-lookup"><span data-stu-id="2ecab-152">Calculates the inverse of a matrix.</span></span> <span data-ttu-id="2ecab-153">Возвращает значение true, если матрица может быть инвертирована; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2ecab-153">Returns true if the matrix can be inverted; false otherwise.</span></span> |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | <span data-ttu-id="2ecab-154">Извлекает скалярные компоненты, переводы и вращение из матрицы трехмерной шкалы, вращения и перевода (SRT).</span><span class="sxs-lookup"><span data-stu-id="2ecab-154">Extracts the scalar, translation, and rotation components from a 3D scale/rotate/translate (SRT) matrix.</span></span> <span data-ttu-id="2ecab-155">Возвращает значение true, если матрицу можно разложить; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="2ecab-155">Returns true if the matrix can be decomposed; false otherwise.</span></span> |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | <span data-ttu-id="2ecab-156">Преобразует матрицу, применяя поворот кватернион.</span><span class="sxs-lookup"><span data-stu-id="2ecab-156">Transforms a matrix by applying a quaternion rotation.</span></span> |
| `float4x4 transpose(float4x4 const& matrix)` | <span data-ttu-id="2ecab-157">Переставит компоненты матрицы вдоль диагонали.</span><span class="sxs-lookup"><span data-stu-id="2ecab-157">Transposes the components of a matrix along its diagonal.</span></span> |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | <span data-ttu-id="2ecab-158">Линейная интерполяция между соответствующими значениями двух матриц.</span><span class="sxs-lookup"><span data-stu-id="2ecab-158">Linearly interpolates between the corresponding values of two matrices.</span></span> |

## <a name="methods"></a><span data-ttu-id="2ecab-159">Методы</span><span class="sxs-lookup"><span data-stu-id="2ecab-159">Methods</span></span>

| <span data-ttu-id="2ecab-160">Имя</span><span class="sxs-lookup"><span data-stu-id="2ecab-160">Name</span></span> | <span data-ttu-id="2ecab-161">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecab-161">Description</span></span> |
|-|-|
| `static float4x4 identity()` | <span data-ttu-id="2ecab-162">Возвращает экземпляр матрицы идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="2ecab-162">Returns an instance of the identity matrix.</span></span> |

## <a name="operators"></a><span data-ttu-id="2ecab-163">Операторы</span><span class="sxs-lookup"><span data-stu-id="2ecab-163">Operators</span></span>

| <span data-ttu-id="2ecab-164">Имя</span><span class="sxs-lookup"><span data-stu-id="2ecab-164">Name</span></span> | <span data-ttu-id="2ecab-165">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecab-165">Description</span></span> |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-166">Добавляет каждый компонент матрицы в другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2ecab-166">Adds each component of a matrix to another matrix.</span></span> |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-167">Вычитает каждый компонент матрицы из другой матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-167">Subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-168">Умножает матрицу на другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2ecab-168">Multiplies a matrix by another matrix.</span></span> <span data-ttu-id="2ecab-169">Это влияет на объединение двух преобразований.</span><span class="sxs-lookup"><span data-stu-id="2ecab-169">This has the effect of concatenating two transforms.</span></span> |
| `float4x4 operator* (float4x4 const& value1, float value2)` | <span data-ttu-id="2ecab-170">Умножает каждый компонент матрицы на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="2ecab-170">Multiplies each component of a matrix by a scalar value.</span></span> |
| `float4x4 operator- (float4x4 const& value)` | <span data-ttu-id="2ecab-171">Инвертирует каждый компонент матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-171">Negates each component of a matrix.</span></span> |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-172">На месте добавляет каждый компонент матрицы в другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2ecab-172">In-place adds each component of a matrix to another matrix.</span></span> |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-173">На месте вычитается каждый компонент матрицы из другой матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-173">In-place subtracts each component of a matrix from another matrix.</span></span> |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-174">На месте матрица умножается на другую матрицу.</span><span class="sxs-lookup"><span data-stu-id="2ecab-174">In-place multiplies a matrix by another matrix.</span></span> <span data-ttu-id="2ecab-175">Это влияет на объединение двух преобразований.</span><span class="sxs-lookup"><span data-stu-id="2ecab-175">This has the effect of concatenating two transforms.</span></span> |
| `float4x4& operator*= (float4x4& value1, float value2)` | <span data-ttu-id="2ecab-176">На месте каждый компонент матрицы умножается на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="2ecab-176">In-place multiplies each component of a matrix by a scalar value.</span></span> |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-177">Определяет, равны ли два экземпляра float4x4.</span><span class="sxs-lookup"><span data-stu-id="2ecab-177">Determines whether two instances of float4x4 are equal.</span></span> |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | <span data-ttu-id="2ecab-178">Определяет, являются ли два экземпляра float4x4 неравными.</span><span class="sxs-lookup"><span data-stu-id="2ecab-178">Determines whether two instances of float4x4 are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | <span data-ttu-id="2ecab-179">Преобразует float4x4 в объект **Microsoft. Graphics. Холст. Numerics. Matrix4x4**.</span><span class="sxs-lookup"><span data-stu-id="2ecab-179">Converts a float4x4 to a **Microsoft.Graphics.Canvas.Numerics.Matrix4x4**.</span></span> |

## <a name="fields"></a><span data-ttu-id="2ecab-180">Поля</span><span class="sxs-lookup"><span data-stu-id="2ecab-180">Fields</span></span>

| <span data-ttu-id="2ecab-181">name</span><span class="sxs-lookup"><span data-stu-id="2ecab-181">Name</span></span> | <span data-ttu-id="2ecab-182">Описание</span><span class="sxs-lookup"><span data-stu-id="2ecab-182">Description</span></span> |
|-|-|
| `float m11` | <span data-ttu-id="2ecab-183">Значение в строке 1 столбца 1 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-183">Value at row 1 column 1 of the matrix.</span></span> |
| `float m12` | <span data-ttu-id="2ecab-184">Значение в строке 1 столбца 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-184">Value at row 1 column 2 of the matrix.</span></span> |
| `float m13` | <span data-ttu-id="2ecab-185">Значение в строке 1 столбца 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-185">Value at row 1 column 3 of the matrix.</span></span> |
| `float m14` | <span data-ttu-id="2ecab-186">Значение в строке 1 столбца 4 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-186">Value at row 1 column 4 of the matrix.</span></span> |
| `float m21` | <span data-ttu-id="2ecab-187">Значение в столбце 1 строки 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-187">Value at row 2 column 1 of the matrix.</span></span> |
| `float m22` | <span data-ttu-id="2ecab-188">Значение для столбца 2 в строке 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-188">Value at row 2 column 2 of the matrix.</span></span> |
| `float m23` | <span data-ttu-id="2ecab-189">Значение для столбца 3 в строке 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-189">Value at row 2 column 3 of the matrix.</span></span> |
| `float m24` | <span data-ttu-id="2ecab-190">Значение для столбца 4 в строке 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-190">Value at row 2 column 4 of the matrix.</span></span> |
| `float m31` | <span data-ttu-id="2ecab-191">Значение в столбце 1 строки 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-191">Value at row 3 column 1 of the matrix.</span></span> |
| `float m32` | <span data-ttu-id="2ecab-192">Значение в столбце 2 строки 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-192">Value at row 3 column 2 of the matrix.</span></span> |
| `float m33` | <span data-ttu-id="2ecab-193">Значение для столбца 3 в строке 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-193">Value at row 3 column 3 of the matrix.</span></span> |
| `float m34` | <span data-ttu-id="2ecab-194">В строке 3, столбец 4 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-194">Value at row 3 column 4 of the matrix.</span></span> |
| `float m41` | <span data-ttu-id="2ecab-195">В строке 4, столбец 1 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-195">Value at row 4 column 1 of the matrix.</span></span> |
| `float m42` | <span data-ttu-id="2ecab-196">Значение в строке 4 столбца 2 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-196">Value at row 4 column 2 of the matrix.</span></span> |
| `float m43` | <span data-ttu-id="2ecab-197">В строке 4, столбец 3 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-197">Value at row 4 column 3 of the matrix.</span></span> |
| `float m44` | <span data-ttu-id="2ecab-198">В строке 4 столбца 4 матрицы.</span><span class="sxs-lookup"><span data-stu-id="2ecab-198">Value at row 4 column 4 of the matrix.</span></span> |

## <a name="requirements"></a><span data-ttu-id="2ecab-199">Требования</span><span class="sxs-lookup"><span data-stu-id="2ecab-199">Requirements</span></span>

| <span data-ttu-id="2ecab-200">Требование</span><span class="sxs-lookup"><span data-stu-id="2ecab-200">Requirement</span></span> | <span data-ttu-id="2ecab-201">Значение</span><span class="sxs-lookup"><span data-stu-id="2ecab-201">Value</span></span> |
|-|-|
| <span data-ttu-id="2ecab-202">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2ecab-202">Namespace</span></span> | <span data-ttu-id="2ecab-203">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="2ecab-203">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="2ecab-204">Header</span><span class="sxs-lookup"><span data-stu-id="2ecab-204">Header</span></span> | <dl> <span data-ttu-id="2ecab-205"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ecab-205"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="2ecab-206">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ecab-206">See also</span></span>

[<span data-ttu-id="2ecab-207">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="2ecab-207">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
