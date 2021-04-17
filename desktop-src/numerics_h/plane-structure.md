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
# <a name="plane-structure"></a>Структура плоскости

Эта структура представляет плоскость с использованием нормали трехмерного вектора и значения расстояния.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. плоскость](/dotnet/api/system.numerics.plane?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `plane()` | Создает неинициализированную плоскость. |
| `plane(float x, float y, float z, float d)` | Создает плоскость с указанными значениями. |
| `plane(float3 normal, float d)` | Создает плоскость на основе float3 и расстояния. |
| `explicit plane(float4 value)` | Создает плоскость из float4. |
| `plane(Microsoft::?Graphics::?Canvas::?Numerics::?Plane const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. плоскость** в плоскость. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `plane make_plane_from_vertices(float3 const& point1, float3 const& point2, float3 const& point3)` | Создает плоскость из набора из трех позиций вершин, которые должны быть разными, а не в прямой линии. |
| `plane normalize(plane const& value)` | Изменяет коэффициенты обычного вектора плоскости, чтобы сделать ее длиной единицы. |
| `plane transform(plane const& plane, float4x4 const& matrix)` | Преобразует нормализованную плоскость на матрицу. |
| `plane transform(plane const& plane, quaternion const& rotation)` | Преобразует нормализованную плоскость на поворот кватернион. |
| `float dot(plane const& plane, float4 const& value)` | Вычисляет скалярное произведение плоскости с помощью вектора. |
| `float dot_coordinate(plane const& plane, float3 const& value)` | Вычисляет точку произведения плоскости с координатой float3. В отличие от \_ обычной точки, это вычисление включает значение плоскости d. |
| `float dot_normal(plane const& plane, float3 const& value)` | Вычисляет скалярное произведение плоскости с float3 нормальным. В отличие от \_ координаты точки, это вычисление игнорирует значение плоскости d. |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `bool operator== (plane const& value1, plane const& value2)` | Определяет, равны ли два экземпляра плоскости. |
| `bool operator!= (plane const& value1, plane const& value2)` | Определяет, являются ли два экземпляра плоскости неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Plane() const` | Преобразует плоскость в **Microsoft. Graphics. Canvas. Numerics. плоскость**. |

## <a name="fields"></a>Поля

| name | Описание |
|-|-|
| `float3 normal` | Нормальный вектор плоскости. |
| `float d` | Расстояние от плоскости до ее нормали от начала координат. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numeric |
| Header | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
