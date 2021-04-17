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
# <a name="float4-structure"></a>Структура float4

Вектор с четырьмя компонентами.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. Vector4](/dotnet/api/system.numerics.vector4?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `float4()` | Создает неинициализированную float4. |
| `float4(float x, float y, float z, float w)` | Создает объект float4 с указанными значениями. |
| `float4(float2 value, float z, float w)` | Создает float4 с координатами x и y, скопированными из float2 и заданными значениями z и w. |
| `float4(float3 value, float w)` | Создает объект float4 с координатами x, y и z, скопированными из float3 и указанным значением w. |
| `explicit float4(float value)` | Создает float4 со всеми com. ентс, для которых задано указанное значение. |
| `float4(Microsoft::?Graphics::?Canvas::?Numerics::?Vector4 const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector4** в float4. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `float length(float4 const& value)` | Вычисляет длину вектора (евклидово distance). |
| `float length_squared(float4 const& value)` | Вычисляет длину (или евклидово расстояние) вектора в квадрате. |
| `float distance(float4 const& value1, float4 const& value2)` | Вычисляет евклидово расстояние между двумя векторами. |
| `float distance_squared(float4 const& value1, float4 const& value2)` | Вычисляет евклидово расстояние между двумя векторами в квадрате. |
| `float dot(float4 const& vector1, float4 const& vector2)` | Вычисляет скалярное произведение двух векторов. |
| `float4 normalize(float4 const& vector)` | Создает единичный вектор из указанного вектора. |
| `float4 min(float4 const& value1, float4 const& value2)` | Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов. |
| `float4 max(float4 const& value1, float4 const& value2)` | Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов. |
| `float4 clamp(float4 const& value1, float4 const& min, float4 const& max)` | Разрешает значение в пределах указанного диапазона. |
| `float4 lerp(float4 const& value1, float4 const& value2, float amount)` | Выполняет линейную интерполяцию между двумя векторами. |
| `float4 transform(float4 const& vector, float4x4 const& matrix)` | Преобразует объект float4 в заданную матрицу. |
| `float4 transform4(float3 const& position, float4x4 const& matrix)` | Преобразует объект float3 в заданную матрицу, возвращая float4. |
| `float4 transform4(float2 const& position, float4x4 const& matrix)` | Преобразует объект float2 в заданную матрицу, возвращая float4. |
| `float4 transform(float4 const& value, quaternion const& rotation)` | Преобразует float4 в заданный кватернион. |
| `float4 transform4(float3 const& value, quaternion const& rotation)` | Преобразует float3 в заданном кватернион, возвращая float4. |
| `float4 transform4(float2 const& value, quaternion const& rotation)` | Преобразует float2 в заданном кватернион, возвращая float4. |

## <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
| `static float4 zero()` | Возвращает float4 со всеми его компонентами, для которых задано значение 0. |
| `static float4 one()` | Возвращает float4 со всеми его компонентами, для которых задано значение One. |
| `static float4 unit_x()` | Возвращает float4 (1, 0, 0, 0). |
| `static float4 unit_y()` | Возвращает float4 (0, 1, 0, 0). |
| `static float4 unit_z()` | Возвращает float4 (0, 0, 1, 0). |
| `static float4 unit_w()` | Возвращает float4 (0, 0, 0, 1). |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `float4 operator+ (float4 const& value1, float4 const& value2)` | Складывает два вектора. |
| `float4 operator- (float4 const& value1, float4 const& value2)` | Вычитает вектор из вектора. |
| `float4 operator* (float4 const& value1, float4 const& value2)` | Умножает компоненты двух векторов друг от друга. |
| `float4 operator* (float4 const& value1, float value2)` | Умножает вектор на скалярный. |
| `float4 operator* (float value1, float4 const& value2)` | Умножает вектор на скалярный. |
| `float4 operator/ (float4 const& value1, float4 const& value2)` | Делит компоненты вектора на компоненты другого вектора. |
| `float4 operator/ (float4 const& value1, float value2)` | Делит вектор на скалярное значение. |
| `float4 operator- (float4 const& value)` | Возвращает вектор, указывающий в обратном направлении. |
| `float4& operator+= (float4& value1, float4 const& value2)` | На месте добавляет два вектора. |
| `float4& operator-= (float4& value1, float4 const& value2)` | На месте выполняется вычитание вектора из вектора. |
| `float4& operator*= (float4& value1, float4 const& value2)` | На месте компоненты двух векторов умножаются друг на друга. |
| `float4& operator*= (float4& value1, float value2)` | На месте — вектор умножается скаляром. |
| `float4& operator/= (float4& value1, float4 const& value2)` | На месте компоненты вектора делятся компонентами другого вектора. |
| `float4& operator/= (float4& value1, float value2)` | На месте вектор помещается в скалярное значение. |
| `bool operator== (float4 const& value1, float4 const& value2)` | Определяет, равны ли два экземпляра float4. |
| `bool operator!= (float4 const& value1, float4 const& value2)` | Определяет, являются ли два экземпляра float4 неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector4() const` | Преобразует float4 в объект **Microsoft. Graphics. Холст. Numerics. Vector4**. |

## <a name="fields"></a>Поля

| name | Описание |
|-|-|
| `float x` | Компонент X вектора. |
| `float y` | Компонент Y вектора. |
| `float z` | Компонент по оси Z вектора. |
| `float w` | Компонент вектора «W». |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numeric |
| Header | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
