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
ms.openlocfilehash: 521c63f99c35e68f18d9a6c0a81118f647ff131effb0f6528e2ef3882c43e234
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939520"
---
# <a name="float3-structure"></a>Структура float3

Вектор с тремя компонентами.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. Vector3](/dotnet/api/system.numerics.vector3?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `float3()` | Создает неинициализированную float3. |
| `float3(float x, float y, float z)` | Создает объект float3 с указанными значениями. |
| `float3(float2 value, float z)` | Создает float3 с координатами x и y, скопированными из float2 и указанным значением z. |
| `explicit float3(float value)` | Создает float3 со всеми компонентами, для которых задано указанное значение. |
| `float3(Microsoft::Graphics::Canvas::Numerics::Vector3 const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector3** в float3. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `float length(float3 const& value)` | Вычисляет длину вектора (евклидово distance). |
| `float length_squared(float3 const& value)` | Вычисляет длину (или евклидово расстояние) вектора в квадрате. |
| `float distance(float3 const& value1, float3 const& value2)` | Вычисляет евклидово расстояние между двумя векторами. |
| `float distance_squared(float3 const& value1, float3 const& value2)` | Вычисляет евклидово расстояние между двумя векторами в квадрате. |
| `float dot(float3 const& vector1, float3 const& vector2)` | Вычисляет скалярное произведение двух векторов. |
| `float3 normalize(float3 const& value)` | Создает единичный вектор из указанного вектора. |
| `float3 cross(float3 const& vector1, float3 const& vector2)` | Вычисляет векторное произведение двух векторов. |
| `float3 reflect(float3 const& vector, float3 const& normal)` | Определяет вектор отражения заданного вектора и нормали. |
| `float3 min(float3 const& value1, float3 const& value2)` | Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов. |
| `float3 max(float3 const& value1, float3 const& value2)` | Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов. |
| `float3 clamp(float3 const& value1, float3 const& min, float3 const& max)` | Разрешает значение в пределах указанного диапазона. |
| `float3 lerp(float3 const& value1, float3 const& value2, float amount)` | Выполняет линейную интерполяцию между двумя векторами. |
| `float3 transform(float3 const& position, float4x4 const& matrix)` | Преобразует вектор (x, y, z, 1) в указанную матрицу. |
| `float3 transform_normal(float3 const& normal, float4x4 const& matrix)` | Преобразует Стандартный вектор (x, y, z, 0) в указанную матрицу. |
| `float3 transform(float3 const& value, quaternion const& rotation)` | Преобразует float3 в заданный кватернион. |

## <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
| `static float3 zero()` | Возвращает float3 со всеми его компонентами, для которых задано значение 0. |
| `static float3 one()` | Возвращает float3 со всеми его компонентами, для которых задано значение One. |
| `static float3 unit_x()` | Возвращает float3 (1, 0, 0). |
| `static float3 unit_y()` | Возвращает float3 (0, 1, 0). |
| `static float3 unit_z()` | Возвращает float3 (0, 0, 1). |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `float3 operator+ (float3 const& value1, float3 const& value2)` | Складывает два вектора. |
| `float3 operator- (float3 const& value1, float3 const& value2)` | Вычитает вектор из вектора. |
| `float3 operator* (float3 const& value1, float3 const& value2)` | Умножает компоненты двух векторов друг от друга. |
| `float3 operator* (float3 const& value1, float value2)` | Умножает вектор на скалярный. |
| `float3 operator* (float value1, float3 const& value2)` | Умножает вектор на скалярный. |
| `float3 operator/ (float3 const& value1, float3 const& value2)` | Делит компоненты вектора на компоненты другого вектора. |
| `float3 operator/ (float3 const& value1, float value2)` | Делит вектор на скалярное значение. |
| `float3 operator- (float3 const& value)` | Возвращает вектор, указывающий в обратном направлении. |
| `float3& operator+= (float3& value1, float3 const& value2)` | На месте добавляет два вектора. |
| `float3& operator-= (float3& value1, float3 const& value2)` | На месте выполняется вычитание вектора из вектора. |
| `float3& operator*= (float3& value1, float3 const& value2)` | На месте компоненты двух векторов умножаются друг на друга. |
| `float3& operator*= (float3& value1, float value2)` | На месте — вектор умножается скаляром. |
| `float3& operator/= (float3& value1, float3 const& value2)` | На месте компоненты вектора делятся компонентами другого вектора. |
| `float3& operator/= (float3& value1, float value2)` | На месте вектор помещается в скалярное значение. |
| `bool operator== (float3 const& value1, float3 const& value2)` | Определяет, равны ли два экземпляра float3. |
| `bool operator!= (float3 const& value1, float3 const& value2)` | Определяет, являются ли два экземпляра float3 неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector3() const` | Преобразует float3 в объект **Microsoft. Graphics. Холст. Numerics. Vector3**. |

## <a name="fields"></a>Поля

| Имя | Описание |
|-|-|
| `float x` | Компонент X вектора. |
| `float y` | Компонент Y вектора. |
| `float z` | Компонент по оси Z вектора. |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numerics |
| Заголовок | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
