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
# <a name="float2-structure"></a>Структура float2

Вектор с двумя компонентами.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. Vector2](/dotnet/api/system.numerics.vector2?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `float2()` | Создает неинициализированную float2. |
| `float2(float x, float y)` | Создает объект float2 с указанными значениями. |
| `explicit float2(float value)` | Создает float2 со всеми компонентами, для которых задано указанное значение. |
| `float2(Microsoft::Graphics::Canvas::Numerics::Vector2 const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. Vector2** в float2. |
| `float2(Windows::Foundation::Point const& value)` | Преобразует [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point) в float2. |
| `float2(Windows::Foundation::Size const& value)` | Преобразует [**Windows. Foundation. size**](/uwp/api/Windows.Foundation.Size) в float2. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `float length(float2 const& value)` | Вычисляет длину вектора (евклидово distance). |
| `float length_squared(float2 const& value)` | Вычисляет длину (или евклидово расстояние) вектора в квадрате. |
| `float distance(float2 const& value1, float2 const& value2)` | Вычисляет евклидово расстояние между двумя векторами. |
| `float distance_squared(float2 const& value1, float2 const& value2)` | Вычисляет евклидово расстояние между двумя векторами в квадрате. |
| `float dot(float2 const& value1, float2 const& value2)` | Вычисляет скалярное произведение двух векторов. |
| `float2 normalize(float2 const& value)` | Создает единичный вектор из указанного вектора. |
| `float2 reflect(float2 const& vector, float2 const& normal)` | Определяет вектор отражения заданного вектора и нормали. |
| `float2 min(float2 const& value1, float2 const& value2)` | Возвращает вектор, который содержит наименьшее значение из каждой соответствующей пары компонентов. |
| `float2 max(float2 const& value1, float2 const& value2)` | Возвращает вектор, который содержит наибольшее значение из каждой соответствующей пары компонентов. |
| `float2 clamp(float2 const& value1, float2 const& min, float2 const& max)` | Разрешает значение в пределах указанного диапазона. |
| `float2 lerp(float2 const& value1, float2 const& value2, float amount)` | Выполняет линейную интерполяцию между двумя векторами. |
| `float2 transform(float2 const& position, float3x2 const& matrix)` | Преобразует вектор (x, y, 0, 1) в указанную матрицу. |
| `float2 transform(float2 const& position, float4x4 const& matrix)` | Преобразует вектор (x, y, 0, 1) в указанную матрицу. |
| `float2 transform_normal(float2 const& normal, float3x2 const& matrix)` | Преобразует Стандартный вектор (x, y, 0, 0) в указанную матрицу. |
| `float2 transform_normal(float2 const& normal, float4x4 const& matrix)` | Преобразует Стандартный вектор (x, y, 0, 0) в указанную матрицу. |
| `float2 transform(float2 const& value, quaternion const& rotation)` | Преобразует float2 в заданный кватернион. |

## <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
| `static float2 zero()` | Возвращает float2 со всеми его компонентами, для которых задано значение 0. |
| `static float2 one()` | Возвращает float2 со всеми его компонентами, для которых задано значение One. |
| `static float2 unit_x()` | Возвращает float2 (1, 0). |
| `static float2 unit_y()` | Возвращает float2 (0, 1). |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `operator Windows::Foundation::Point() const` | Преобразует float2 в [**Windows. Foundation. Point**](/uwp/api/Windows.Foundation.Point). |
| `operator Windows::Foundation::Size() const` | Преобразует float2 в [**Windows. Foundation. size**](/uwp/api/Windows.Foundation.Size). |
| `float2 operator+ (float2 const& value1, float2 const& value2)` | Складывает два вектора. |
| `float2 operator- (float2 const& value1, float2 const& value2)` | Вычитает вектор из вектора. |
| `float2 operator* (float2 const& value1, float2 const& value2)` | Умножает компоненты двух векторов друг от друга. |
| `float2 operator* (float2 const& value1, float value2)` | Умножает вектор на скалярный. |
| `float2 operator* (float value1, float2 const& value2)` | Умножает вектор на скалярный. |
| `float2 operator/ (float2 const& value1, float2 const& value2)` | Делит компоненты вектора на компоненты другого вектора. |
| `float2 operator/ (float2 const& value1, float value2)` | Делит вектор на скалярное значение. |
| `float2 operator- (float2 const& value)` | Возвращает вектор, указывающий в обратном направлении. |
| `float2& operator+= (float2& value1, float2 const& value2)` | На месте добавляет два вектора. |
| `float2& operator-= (float2& value1, float2 const& value2)` | На месте выполняется вычитание вектора из вектора. |
| `float2& operator*= (float2& value1, float2 const& value2)` | На месте компоненты двух векторов умножаются друг на друга. |
| `float2& operator*= (float2& value1, float value2)` | На месте — вектор умножается скаляром. |
| `float2& operator/= (float2& value1, float2 const& value2)` | На месте компоненты вектора делятся компонентами другого вектора. |
| `float2& operator/= (float2& value1, float value2)` | На месте вектор помещается в скалярное значение. |
| `bool operator== (float2 const& value1, float2 const& value2)` | Определяет, равны ли два экземпляра float2. |
| `bool operator!= (float2 const& value1, float2 const& value2)` | Определяет, являются ли два экземпляра float2 неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Vector2() const` | Преобразует float2 в объект **Microsoft. Graphics. Холст. Numerics. Vector2**. |

## <a name="fields"></a>Поля

| name | Описание |
|-|-|
| `float x` | Компонент X вектора. |
| `float y` | Компонент Y вектора. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numeric |
| Header | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
