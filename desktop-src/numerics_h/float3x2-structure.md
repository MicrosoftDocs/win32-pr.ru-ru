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
ms.openlocfilehash: 24d403446fa3544bdb001c065e9874f812a829680e19a5e6b526ed12276fd6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971763"
---
# <a name="float3x2-structure"></a>Структура float3x2

Матрица 3x2, используемая для двумерных преобразований.

Этот тип матрицы использует макет вектора строк. X и y вектора перевода этой матрицы соответствуют полям M31, M32.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. Matrix3x2](/dotnet/api/system.numerics.matrix3x2?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `float3x2()` | Создает неинициализированную float3x2. |
| `float3x2(float m11, float m12, float m21, float m22, float m31, float m32)` | Создает объект float3x2 с указанными значениями. |
| `float3x2(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2 const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. Matrix3x2** в float3x2. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `float3x2 make_float3x2_translation(float2 const& position)` | Создает матрицу трансляции. |
| `float3x2 make_float3x2_translation(float xPosition, float yPosition)` | Создает матрицу трансляции. |
| `float3x2 make_float3x2_scale(float xScale, float yScale)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float3x2 make_float3x2_scale(float xScale, float yScale, float2 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float3x2 make_float3x2_scale(float2 const& scales)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float3x2 make_float3x2_scale(float2 const& scales, float2 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float3x2 make_float3x2_scale(float scale)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float3x2 make_float3x2_scale(float scale, float2 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY)` | Создает матрицу отклонения, центрированную по источнику. |
| `float3x2 make_float3x2_skew(float radiansX, float radiansY, float2 const& centerPoint)` | Создает матрицу отклонения, центрированную по заданной точке. |
| `float3x2 make_float3x2_rotation(float radians)` | Создает матрицу вращения, центрированную по источнику. |
| `float3x2 make_float3x2_rotation(float radians, float2 const& centerPoint)` | Создает матрицу вращения, центрированную по указанной точке. |
| `bool is_identity(float3x2 const& value)` | Проверяет, является ли это матрицей удостоверений. |
| `float determinant(float3x2 const& value)` | Вычисляет определитель матрицы. |
| `float2 translation(float3x2 const& value)` | Возвращает вектор смещения матрицы. |
| `bool invert(float3x2 const& matrix, _Out_ float3x2* result)` | Вычисляет обратную матрицу. Возвращает значение true, если матрица может быть инвертирована; в противном случае — значение false. |
| `float3x2 lerp(float3x2 const& matrix1, float3x2 const& matrix2, float amount)` | Линейная интерполяция между соответствующими значениями двух матриц. |

## <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
| `static float3x2 identity()` | Возвращает экземпляр матрицы идентификаторов. |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `float3x2 operator+ (float3x2 const& value1, float3x2 const& value2)` | Добавляет каждый компонент матрицы в другую матрицу. |
| `float3x2 operator- (float3x2 const& value1, float3x2 const& value2)` | Вычитает каждый компонент матрицы из другой матрицы. |
| `float3x2 operator* (float3x2 const& value1, float3x2 const& value2)` | Умножает матрицу на другую матрицу. Это влияет на объединение двух преобразований. |
| `float3x2 operator* (float3x2 const& value1, float value2)` | Умножает каждый компонент матрицы на скалярное значение. |
| `float3x2 operator- (float3x2 const& value)` | Инвертирует каждый компонент матрицы. |
| `float3x2& operator+= (float3x2& value1, float3x2 const& value2)` | На месте добавляет каждый компонент матрицы в другую матрицу. |
| `float3x2& operator-= (float3x2& value1, float3x2 const& value2)` | На месте вычитается каждый компонент матрицы из другой матрицы. |
| `float3x2& operator*= (float3x2& value1, float3x2 const& value2)` | На месте матрица умножается на другую матрицу. Это влияет на объединение двух преобразований. |
| `float3x2& operator*= (float3x2& value1, float value2)` | На месте каждый компонент матрицы умножается на скалярное значение. |
| `bool operator== (float3x2 const& value1, float3x2 const& value2)` | Определяет, равны ли два экземпляра float3x2. |
| `bool operator!= (float3x2 const& value1, float3x2 const& value2)` | Определяет, являются ли два экземпляра float3x2 неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix3x2() const` | Преобразует float3x2 в объект **Microsoft. Graphics. Холст. Numerics. Matrix3x2**. |

## <a name="fields"></a>Поля

| Имя | Описание |
|-|-|
| `float m11` | Значение в строке 1 столбца 1 матрицы. |
| `float m12` | Значение в строке 1 столбца 2 матрицы. |
| `float m21` | Значение в столбце 1 строки 2 матрицы. |
| `float m22` | Значение для столбца 2 в строке 2 матрицы. |
| `float m31` | Значение в столбце 1 строки 3 матрицы. |
| `float m32` | Значение в столбце 2 строки 3 матрицы. |

## <a name="requirements"></a>Requirements (Требования)

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numerics |
| Заголовок | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
