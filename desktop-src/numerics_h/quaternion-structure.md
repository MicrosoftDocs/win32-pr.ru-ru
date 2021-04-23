---
title: Структура кватерниона (Виндовснумерикс. h)
description: 4-мерный вектор, используемый для представления вращения.
ms.assetid: A6B25885-8ECB-4039-9DC6-41D5F3A02489
keywords:
- Структура кватерниона
topic_type:
- apiref
api_name:
- quaternion structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b56ae169232f83e6753505f9d5d07fffac09e67e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721042"
---
# <a name="quaternion-structure"></a><span data-ttu-id="aae71-104">Структура кватерниона</span><span class="sxs-lookup"><span data-stu-id="aae71-104">quaternion Structure</span></span>

<span data-ttu-id="aae71-105">4-мерный вектор, используемый для представления вращения.</span><span class="sxs-lookup"><span data-stu-id="aae71-105">A four dimensional vector, used to represent a rotation.</span></span>

<span data-ttu-id="aae71-106">Кватернион может эффективно поворачивать объект вокруг вектора (x, y, z) на угол тета, где w = cos (тета/2).</span><span class="sxs-lookup"><span data-stu-id="aae71-106">A quaternion can efficiently rotate an object about the (x, y, z) vector by the angle theta, where w = cos(theta/2).</span></span> <span data-ttu-id="aae71-107">Кватернионы обычно используются для плавной интерполяции между двумя углами и для предотвращения проблемы с блокировкой гимбал, которая может возникнуть с Эйлера углами.</span><span class="sxs-lookup"><span data-stu-id="aae71-107">Quaternions are typically used for smooth interpolation between two angles, and for avoiding the gimbal lock problem that can occur with Euler angles.</span></span>

<span data-ttu-id="aae71-108">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="aae71-108">This type is available only in C++.</span></span> <span data-ttu-id="aae71-109">Его эквивалент .NET — [System. Numerics. кватернион](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="aae71-109">Its .NET equivalent is [System.Numerics.Quaternion](/dotnet/api/system.numerics.quaternion?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="aae71-110">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="aae71-110">Constructors</span></span>

| <span data-ttu-id="aae71-111">Имя</span><span class="sxs-lookup"><span data-stu-id="aae71-111">Name</span></span> | <span data-ttu-id="aae71-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aae71-112">Description</span></span> |
|-|-|
| `quaternion()` | <span data-ttu-id="aae71-113">Создает неинициализированный кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-113">Creates an uninitialized quaternion.</span></span> |
| `quaternion(float x, float y, float z, float w)` | <span data-ttu-id="aae71-114">Создает кватернион с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="aae71-114">Creates a quaternion with the specified values.</span></span> |
| `quaternion(float3 vectorPart, float scalarPart)` | <span data-ttu-id="aae71-115">Создает кватернион из float3 и скалярного.</span><span class="sxs-lookup"><span data-stu-id="aae71-115">Creates a quaternion from a float3 and scalar.</span></span> |
| `quaternion(Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion const& value)` | <span data-ttu-id="aae71-116">Преобразует объект **Microsoft. Graphics. Холст. Numerics. кватернион** в кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-116">Converts a **Microsoft.Graphics.Canvas.Numerics.Quaternion** to a quaternion.</span></span> |

## <a name="functions"></a><span data-ttu-id="aae71-117">Функции</span><span class="sxs-lookup"><span data-stu-id="aae71-117">Functions</span></span>

| <span data-ttu-id="aae71-118">Имя</span><span class="sxs-lookup"><span data-stu-id="aae71-118">Name</span></span> | <span data-ttu-id="aae71-119">Описание</span><span class="sxs-lookup"><span data-stu-id="aae71-119">Description</span></span> |
|-|-|
| `quaternion make_quaternion_from_axis_angle(float3 const& axis, float angle)` | <span data-ttu-id="aae71-120">Создает кватернион на основе вектора и угла поворота вокруг вектора.</span><span class="sxs-lookup"><span data-stu-id="aae71-120">Creates a quaternion from a vector and an angle to rotate about the vector.</span></span> |
| `quaternion make_quaternion_from_yaw_pitch_roll(float yaw, float pitch, float roll)` | <span data-ttu-id="aae71-121">Создает кватернион на основе указанных значения нутации, высоты и углов.</span><span class="sxs-lookup"><span data-stu-id="aae71-121">Creates a quaternion from specified yaw, pitch, and roll angles.</span></span> |
| `quaternion make_quaternion_from_rotation_matrix(float4x4 const& matrix)` | <span data-ttu-id="aae71-122">Создает кватернион из матрицы вращения.</span><span class="sxs-lookup"><span data-stu-id="aae71-122">Creates a quaternion from a rotation matrix.</span></span> |
| `bool is_identity(quaternion const& value)` | <span data-ttu-id="aae71-123">Проверяет, является ли этот кватернион единичным (без поворота).</span><span class="sxs-lookup"><span data-stu-id="aae71-123">Checks whether this is an identity (no rotation) quaternion.</span></span> |
| `float length(quaternion const& value)` | <span data-ttu-id="aae71-124">Вычисляет длину кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-124">Calculates the length of a quaternion.</span></span> |
| `float length_squared(quaternion const& value)` | <span data-ttu-id="aae71-125">Вычисляет длину объекта Quaternion в квадрате.</span><span class="sxs-lookup"><span data-stu-id="aae71-125">Calculates the length squared of a quaternion.</span></span> |
| `float dot(quaternion const& quaternion1, quaternion const& quaternion2)` | <span data-ttu-id="aae71-126">Вычисляет скалярное произведение двух кватернионов.</span><span class="sxs-lookup"><span data-stu-id="aae71-126">Calculates the dot product of two quaternions.</span></span> |
| `quaternion normalize(quaternion const& value)` | <span data-ttu-id="aae71-127">Делит каждый компонент кватерниона на длину кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-127">Divides each component of a quaternion by the length of the quaternion.</span></span> |
| `quaternion conjugate(quaternion const& value)` | <span data-ttu-id="aae71-128">Вычисляет сопряженный кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-128">Calculates the conjugate of a quaternion.</span></span> |
| `quaternion inverse(quaternion const& value)` | <span data-ttu-id="aae71-129">Вычисляет обратную часть кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-129">Calculates the inverse of a quaternion.</span></span> |
| `quaternion slerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="aae71-130">Выполняет интерполяцию между двумя кватернионами, используя сферическую линейную интерполяцию.</span><span class="sxs-lookup"><span data-stu-id="aae71-130">Interpolates between two quaternions, using spherical linear interpolation.</span></span> |
| `quaternion lerp(quaternion const& quaternion1, quaternion const& quaternion2, float amount)` | <span data-ttu-id="aae71-131">Линейная интерполяция между двумя кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-131">Linearly interpolates between two quaternions.</span></span> |
| `quaternion concatenate(quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-132">Сцепляет два кватерниона; Результат представляет первый поворот, за которым следует второй поворот.</span><span class="sxs-lookup"><span data-stu-id="aae71-132">Concatenates two quaternions; the result represents the first rotation followed by the second rotation.</span></span> |

## <a name="methods"></a><span data-ttu-id="aae71-133">Методы</span><span class="sxs-lookup"><span data-stu-id="aae71-133">Methods</span></span>

| <span data-ttu-id="aae71-134">Имя</span><span class="sxs-lookup"><span data-stu-id="aae71-134">Name</span></span> | <span data-ttu-id="aae71-135">Описание</span><span class="sxs-lookup"><span data-stu-id="aae71-135">Description</span></span> |
|-|-|
| `static quaternion identity()` | <span data-ttu-id="aae71-136">Возвращает экземпляр идентификатора кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-136">Returns an instance of the identity quaternion.</span></span> |

## <a name="operators"></a><span data-ttu-id="aae71-137">Операторы</span><span class="sxs-lookup"><span data-stu-id="aae71-137">Operators</span></span>

| <span data-ttu-id="aae71-138">Имя</span><span class="sxs-lookup"><span data-stu-id="aae71-138">Name</span></span> | <span data-ttu-id="aae71-139">Описание</span><span class="sxs-lookup"><span data-stu-id="aae71-139">Description</span></span> |
|-|-|
| `quaternion operator+ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-140">Складывает два кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-140">Adds two quaternions.</span></span> |
| `quaternion operator- (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-141">Вычитает кватернион из другого кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-141">Subtracts a quaternion from another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-142">Умножает кватернион на другой кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-142">Multiplies a quaternion by another quaternion.</span></span> |
| `quaternion operator* (quaternion const& value1, float value2)` | <span data-ttu-id="aae71-143">Умножает кватернион на скалярное значение.</span><span class="sxs-lookup"><span data-stu-id="aae71-143">Multiplies a quaternion by a scalar value.</span></span> |
| `quaternion operator/ (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-144">Делит кватернион на другой кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-144">Divides a quaternion by another quaternion.</span></span> |
| `quaternion operator- (quaternion const& value)` | <span data-ttu-id="aae71-145">Переворачивает знак каждого компонента кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-145">Flips the sign of each component of the quaternion.</span></span> |
| `quaternion& operator+= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="aae71-146">На месте добавляется два кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-146">In-place adds two quaternions.</span></span> |
| `quaternion& operator-= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="aae71-147">На месте вычитается кватернион из другого кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-147">In-place subtracts a quaternion from another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="aae71-148">На месте умножает кватернион на другой кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-148">In-place multiplies a quaternion by another quaternion.</span></span> |
| `quaternion& operator*= (quaternion& value1, float value2)` | <span data-ttu-id="aae71-149">На месте нултиплиес кватернион скалярным значением.</span><span class="sxs-lookup"><span data-stu-id="aae71-149">In-place nultiplies a quaternion by a scalar value.</span></span> |
| `quaternion& operator/= (quaternion& value1, quaternion const& value2)` | <span data-ttu-id="aae71-150">На месте делит кватернион на другой кватернион.</span><span class="sxs-lookup"><span data-stu-id="aae71-150">In-place divides a quaternion by another quaternion.</span></span> |
| `bool operator== (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-151">Определяет, равны ли два экземпляра кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-151">Determines whether two instances of quaternion are equal.</span></span> |
| `bool operator!= (quaternion const& value1, quaternion const& value2)` | <span data-ttu-id="aae71-152">Определяет, являются ли два экземпляра кватерниона неравными.</span><span class="sxs-lookup"><span data-stu-id="aae71-152">Determines whether two instances of quaternion are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Quaternion() const` | <span data-ttu-id="aae71-153">Преобразует кватернион в объект **Microsoft. Graphics. Холст. Numerics. кватернион**.</span><span class="sxs-lookup"><span data-stu-id="aae71-153">Converts a quaternion to a **Microsoft.Graphics.Canvas.Numerics.Quaternion**.</span></span> |

## <a name="fields"></a><span data-ttu-id="aae71-154">Поля</span><span class="sxs-lookup"><span data-stu-id="aae71-154">Fields</span></span>

| <span data-ttu-id="aae71-155">name</span><span class="sxs-lookup"><span data-stu-id="aae71-155">Name</span></span> | <span data-ttu-id="aae71-156">Описание</span><span class="sxs-lookup"><span data-stu-id="aae71-156">Description</span></span> |
|-|-|
| `float x` | <span data-ttu-id="aae71-157">Значение X компонента вектора кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-157">X value of the vector component of the quaternion.</span></span> |
| `float y` | <span data-ttu-id="aae71-158">Значение Y компонента вектора кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-158">Y value of the vector component of the quaternion.</span></span> |
| `float z` | <span data-ttu-id="aae71-159">Значение Z компонента вектора кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-159">Z value of the vector component of the quaternion.</span></span> |
| `float w` | <span data-ttu-id="aae71-160">Компонент вращения кватерниона.</span><span class="sxs-lookup"><span data-stu-id="aae71-160">Rotation component of the quaternion.</span></span> |

## <a name="requirements"></a><span data-ttu-id="aae71-161">Требования</span><span class="sxs-lookup"><span data-stu-id="aae71-161">Requirements</span></span>

| <span data-ttu-id="aae71-162">Требование</span><span class="sxs-lookup"><span data-stu-id="aae71-162">Requirement</span></span> | <span data-ttu-id="aae71-163">Значение</span><span class="sxs-lookup"><span data-stu-id="aae71-163">Value</span></span> |
|-|-|
| <span data-ttu-id="aae71-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aae71-164">Namespace</span></span> | <span data-ttu-id="aae71-165">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="aae71-165">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="aae71-166">Header</span><span class="sxs-lookup"><span data-stu-id="aae71-166">Header</span></span> | <dl> <span data-ttu-id="aae71-167"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae71-167"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="aae71-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae71-168">See also</span></span>

[<span data-ttu-id="aae71-169">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="aae71-169">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
