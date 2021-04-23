---
title: Структура плоскости (Виндовснумерикс. h)
description: Эта структура представляет плоскость с использованием нормали трехмерного вектора и значения расстояния.
ms.assetid: 3C5A5EA0-8A51-4F9B-A84A-0C8E726CE3FD
keywords:
- Структура плоскости
topic_type:
- apiref
api_name:
- plane structure
api_location:
- windowsnumerics.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d870e2769121b4aec542235081011406e439d579
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721043"
---
# <a name="plane-structure"></a><span data-ttu-id="6e416-104">Структура плоскости</span><span class="sxs-lookup"><span data-stu-id="6e416-104">plane structure</span></span>

<span data-ttu-id="6e416-105">Эта структура представляет плоскость с использованием нормали трехмерного вектора и значения расстояния.</span><span class="sxs-lookup"><span data-stu-id="6e416-105">This structure represents a plane using a 3D vector normal and a distance value.</span></span>

<span data-ttu-id="6e416-106">Этот тип доступен только в C++.</span><span class="sxs-lookup"><span data-stu-id="6e416-106">This type is available only in C++.</span></span> <span data-ttu-id="6e416-107">Его эквивалент .NET — [System. Numerics. плоскость](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span><span class="sxs-lookup"><span data-stu-id="6e416-107">Its .NET equivalent is [System.Numerics.Plane](/dotnet/api/system.numerics.plane?view=netframework-4.8).</span></span>

## <a name="constructors"></a><span data-ttu-id="6e416-108">Конструкторы</span><span class="sxs-lookup"><span data-stu-id="6e416-108">Constructors</span></span>

| <span data-ttu-id="6e416-109">Имя</span><span class="sxs-lookup"><span data-stu-id="6e416-109">Name</span></span> | <span data-ttu-id="6e416-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6e416-110">Description</span></span> |
|-|-|
| `plane()` | <span data-ttu-id="6e416-111">Создает неинициализированную плоскость.</span><span class="sxs-lookup"><span data-stu-id="6e416-111">Creates an uninitialized plane.</span></span> |
| `plane(float x, float y, float z, float d)` | <span data-ttu-id="6e416-112">Создает плоскость с указанными значениями.</span><span class="sxs-lookup"><span data-stu-id="6e416-112">Creates a plane with the specified values.</span></span> |
| `plane(float3 normal, float d)` | <span data-ttu-id="6e416-113">Создает плоскость на основе float3 и расстояния.</span><span class="sxs-lookup"><span data-stu-id="6e416-113">Creates a plane from a float3 and a distance.</span></span> |
| `explicit plane(float4 value)` | <span data-ttu-id="6e416-114">Создает плоскость из float4.</span><span class="sxs-lookup"><span data-stu-id="6e416-114">Creates a plane from a float4.</span></span> |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | <span data-ttu-id="6e416-115">Преобразует объект **Microsoft. Graphics. Холст. Numerics. плоскость** в плоскость.</span><span class="sxs-lookup"><span data-stu-id="6e416-115">Converts a **Microsoft.Graphics.Canvas.Numerics.Plane** to a plane.</span></span> |

## <a name="functions"></a><span data-ttu-id="6e416-116">Функции</span><span class="sxs-lookup"><span data-stu-id="6e416-116">Functions</span></span>

| <span data-ttu-id="6e416-117">Имя</span><span class="sxs-lookup"><span data-stu-id="6e416-117">Name</span></span> | <span data-ttu-id="6e416-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6e416-118">Description</span></span> |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | <span data-ttu-id="6e416-119">Создает плоскость из набора из трех позиций вершин, которые должны быть разными, а не в прямой линии.</span><span class="sxs-lookup"><span data-stu-id="6e416-119">Creates a plane from a set of three vertex positions, which must all be different and not in a straight line.</span></span> |
| `plane normalize(plane const& value)` | <span data-ttu-id="6e416-120">Изменяет коэффициенты обычного вектора плоскости, чтобы сделать ее длиной единицы.</span><span class="sxs-lookup"><span data-stu-id="6e416-120">Changes the coefficients of the normal vector of a plane to make it of unit length.</span></span> |
| `plane transform(plane const& plane, float4x4 const& matrix)` | <span data-ttu-id="6e416-121">Преобразует нормализованную плоскость на матрицу.</span><span class="sxs-lookup"><span data-stu-id="6e416-121">Transforms a normalized plane by a matrix.</span></span> |
| `plane transform(plane const& plane, quaternion const& rotation)` | <span data-ttu-id="6e416-122">Преобразует нормализованную плоскость на поворот кватернион.</span><span class="sxs-lookup"><span data-stu-id="6e416-122">Transforms a normalized plane by a quaternion rotation.</span></span> |
| `float dot(plane const& plane, float4 const& value)` | <span data-ttu-id="6e416-123">Вычисляет скалярное произведение плоскости с помощью вектора.</span><span class="sxs-lookup"><span data-stu-id="6e416-123">Calculates the dot product of a plane with a vector.</span></span> |
| `float dot_coordinate(plane const& plane, float3 const& value)` | <span data-ttu-id="6e416-124">Вычисляет точку произведения плоскости с координатой float3.</span><span class="sxs-lookup"><span data-stu-id="6e416-124">Calculates the dot product of a plane with a float3 coordinate.</span></span> <span data-ttu-id="6e416-125">В отличие от \_ обычной точки, это вычисление включает значение плоскости d.</span><span class="sxs-lookup"><span data-stu-id="6e416-125">Unlike dot\_normal, this computation includes the plane d value.</span></span> |
| `float dot_normal(plane const& plane, float3 const& value)` | <span data-ttu-id="6e416-126">Вычисляет скалярное произведение плоскости с float3 нормальным.</span><span class="sxs-lookup"><span data-stu-id="6e416-126">Calculates the dot product of a plane with a float3 normal.</span></span> <span data-ttu-id="6e416-127">В отличие от \_ координаты точки, это вычисление игнорирует значение плоскости d.</span><span class="sxs-lookup"><span data-stu-id="6e416-127">Unlike dot\_coordinate, this computation ignores the plane d value.</span></span> |

## <a name="operators"></a><span data-ttu-id="6e416-128">Операторы</span><span class="sxs-lookup"><span data-stu-id="6e416-128">Operators</span></span>

| <span data-ttu-id="6e416-129">Имя</span><span class="sxs-lookup"><span data-stu-id="6e416-129">Name</span></span> | <span data-ttu-id="6e416-130">Описание</span><span class="sxs-lookup"><span data-stu-id="6e416-130">Description</span></span> |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | <span data-ttu-id="6e416-131">Определяет, равны ли два экземпляра плоскости.</span><span class="sxs-lookup"><span data-stu-id="6e416-131">Determines whether two instances of plane are equal.</span></span> |
| `bool operator!= (plane const& value1, plane const& value2)` | <span data-ttu-id="6e416-132">Определяет, являются ли два экземпляра плоскости неравными.</span><span class="sxs-lookup"><span data-stu-id="6e416-132">Determines whether two instances of plane are not equal.</span></span> |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | <span data-ttu-id="6e416-133">Преобразует плоскость в **Microsoft. Graphics. Canvas. Numerics. плоскость**.</span><span class="sxs-lookup"><span data-stu-id="6e416-133">Converts a plane to a **Microsoft.Graphics.Canvas.Numerics.Plane**.</span></span> |

## <a name="fields"></a><span data-ttu-id="6e416-134">Поля</span><span class="sxs-lookup"><span data-stu-id="6e416-134">Fields</span></span>

| <span data-ttu-id="6e416-135">name</span><span class="sxs-lookup"><span data-stu-id="6e416-135">Name</span></span> | <span data-ttu-id="6e416-136">Описание</span><span class="sxs-lookup"><span data-stu-id="6e416-136">Description</span></span> |
|-|-|
| `float3 normal` | <span data-ttu-id="6e416-137">Нормальный вектор плоскости.</span><span class="sxs-lookup"><span data-stu-id="6e416-137">Normal vector of the plane.</span></span> |
| `float d` | <span data-ttu-id="6e416-138">Расстояние от плоскости до ее нормали от начала координат.</span><span class="sxs-lookup"><span data-stu-id="6e416-138">Distance of the plane along its normal from the origin.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6e416-139">Требования</span><span class="sxs-lookup"><span data-stu-id="6e416-139">Requirements</span></span>

| <span data-ttu-id="6e416-140">Требование</span><span class="sxs-lookup"><span data-stu-id="6e416-140">Requirement</span></span> | <span data-ttu-id="6e416-141">Значение</span><span class="sxs-lookup"><span data-stu-id="6e416-141">Value</span></span> |
|-|-|
| <span data-ttu-id="6e416-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6e416-142">Namespace</span></span> | <span data-ttu-id="6e416-143">Windows:: Foundation:: numeric</span><span class="sxs-lookup"><span data-stu-id="6e416-143">Windows::Foundation::Numerics</span></span> |
| <span data-ttu-id="6e416-144">Header</span><span class="sxs-lookup"><span data-stu-id="6e416-144">Header</span></span> | <dl> <span data-ttu-id="6e416-145"><dt>Виндовснумерикс. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e416-145"><dt>Windowsnumerics.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="6e416-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e416-146">See also</span></span>

[<span data-ttu-id="6e416-147">API-интерфейсы виндовснумерикс. h</span><span class="sxs-lookup"><span data-stu-id="6e416-147">windowsnumerics.h APIs</span></span>](windowsnumerics-h-apis-portal.md)
