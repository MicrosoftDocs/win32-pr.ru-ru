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
# <a name="float4x4-structure"></a>Структура float4x4

Матрица 4x4, используемая для трехмерных преобразований.

Этот тип матрицы использует макет вектора строк. X, y и z этого вектора перевода матрицы соответствуют полям M41, M42, M43.

Этот тип доступен только в C++. Его эквивалент .NET — [System. Numerics. Matrix4x4](/dotnet/api/system.numerics.matrix4x4?view=netframework-4.8).

## <a name="constructors"></a>Конструкторы

| Имя | Описание |
|-|-|
| `float4x4()` | Создает неинициализированную float4x4. |
| `float4x4(float m11, float m12, float m13, float m14, float m21, float m22, float m23, float m24, float m31, float m32, float m33, float m34, float m41, float m42, float m43, float m44)` | Создает объект float4x4 с указанными значениями. |
| `explicit float4x4(float3x2 value)` | Создает float4x4 из float3x2. |
| `float4x4(Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4 const& value)` | Преобразует объект **Microsoft. Graphics. Холст. Numerics. Matrix4x4** в float4x4. |

## <a name="functions"></a>Функции

| Имя | Описание |
|-|-|
| `float4x4 make_float4x4_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& cameraUpVector, float3 const& cameraForwardVector)` | Создает сферическую рекламу, которая поворачивается вокруг указанного расположения объекта, используя правую систему координат. |
| `float4x4 make_float4x4_?constrained_billboard(float3 const& objectPosition, float3 const& cameraPosition, float3 const& rotateAxis, float3 const& cameraForwardVector, float3 const& objectForwardVector)` | Создает цилиндрическое объявление, которое поворачивается вокруг заданной оси с помощью правой руки системы координат. |
| `float4x4 make_float4x4_translation(float3 const& position)` | Создает матрицу трансляции. |
| `float4x4 make_float4x4_translation(float xPosition, float yPosition, float zPosition)` | Создает матрицу трансляции. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float4x4 make_float4x4_scale(float xScale, float yScale, float zScale, float3 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float4x4 make_float4x4_scale(float3 const& scales)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float4x4 make_float4x4_scale(float3 const& scales, float3 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float4x4 make_float4x4_scale(float scale)` | Создает матрицу масштабирования, центрированную по источнику. |
| `float4x4 make_float4x4_scale(float scale, float3 const& centerPoint)` | Создает матрицу масштабирования, центрированную по указанной точке. |
| `float4x4 make_float4x4_rotation_x(float radians)` | Создает матрицу вращения по оси x, центрированную по источнику. |
| `float4x4 make_float4x4_rotation_x(float radians, float3 const& centerPoint)` | Создает матрицу вращения по оси x, центрированную по указанной точке. |
| `float4x4 make_float4x4_rotation_y(float radians)` | Создает матрицу вращения по оси y, центрированную по источнику. |
| `float4x4 make_float4x4_rotation_y(float radians, float3 const& centerPoint)` | Создает матрицу вращения по оси y, центрированную по указанной точке. |
| `float4x4 make_float4x4_rotation_z(float radians)` | Создает матрицу поворота оси z, центрированную по источнику. |
| `float4x4 make_float4x4_rotation_z(float radians, float3 const& centerPoint)` | Создает матрицу поворота оси z, центрированную по указанной точке. |
| `float4x4 make_float4x4_from_axis_angle(float3 const& axis, float angle)` | Создает матрицу, которая вращается вокруг произвольного вектора. |
| `float4x4 make_float4x4_?perspective_field_of_view(float fieldOfView, float aspectRatio, float nearPlaneDistance, float farPlaneDistance)` | Создает матрицу перспективной проекции на основе поля представления с помощью правой правильной системы координат. |
| `float4x4 make_float4x4_perspective(float width, float height, float nearPlaneDistance, float farPlaneDistance)` | Создает матрицу перспективной проекции с использованием правой рукой системы координат. |
| `float4x4 make_float4x4_?perspective_off_center(float left, float right, float bottom, float top, float nearPlaneDistance, float farPlaneDistance)` | Создает настраиваемую матрицу перспективной проекции с использованием правой рукой системы координат. |
| `float4x4 make_float4x4_orthographic(float width, float height, float zNearPlane, float zFarPlane)` | Создает матрицу ортогональной проекции с использованием правой рукой системы координат. |
| `float4x4 make_float4x4_?orthographic_off_center(float left, float right, float bottom, float top, float zNearPlane, float zFarPlane)` | Создает настраиваемую матрицу ортогональной проекции с использованием правой рукой системы координат. |
| `float4x4 make_float4x4_look_at(float3 const& cameraPosition, float3 const& cameraTarget, float3 const& cameraUpVector)` | Создает матрицу представления с помощью правой правильной системы координат. |
| `float4x4 make_float4x4_world(float3 const& position, float3 const& forward, float3 const& up)` | Создает матрицу мира с помощью правой правильной системы координат. Это можно использовать для размещения объектов в трехмерном пространстве. |
| `float4x4 make_float4x4_?from_quaternion(quaternion const& quaternion)` | Создает матрицу вращения из кватерниона. |
| `float4x4 make_float4x4_?from_yaw_pitch_roll(float yaw, float pitch, float roll)` | Создает матрицу вращения на основе указанного значения нутации, высоты и рулона. |
| `float4x4 make_float4x4_shadow(float3 const& lightDirection, plane const& plane)` | Создает матрицу, которая создает проекцию геометрической фигуры на указанной плоскости подобно отбрасыванию тени от указанного источника света. |
| `float4x4 make_float4x4_reflection(plane const& value)` | Создает матрицу, отражающую систему координат для указанной плоскости. |
| `bool is_identity(float4x4 const& value)` | Проверяет, является ли это матрицей удостоверений. |
| `float determinant(float4x4 const& value)` | Вычисляет определитель матрицы. |
| `float3 translation(float4x4 const& value)` | Возвращает вектор смещения матрицы. |
| `bool invert(float4x4 const& matrix, _Out_ float4x4* result)` | Вычисляет обратную матрицу. Возвращает значение true, если матрица может быть инвертирована; в противном случае — значение false. |
| `bool decompose(float4x4 const& matrix, _Out_ float3* scale, _Out_ quaternion* rotation, _Out_ float3* translation)` | Извлекает скалярные компоненты, переводы и вращение из матрицы трехмерной шкалы, вращения и перевода (SRT). Возвращает значение true, если матрицу можно разложить; в противном случае — значение false. |
| `float4x4 transform(float4x4 const& value, quaternion const& rotation)` | Преобразует матрицу, применяя поворот кватернион. |
| `float4x4 transpose(float4x4 const& matrix)` | Переставит компоненты матрицы вдоль диагонали. |
| `float4x4 lerp(float4x4 const& matrix1, float4x4 const& matrix2, float amount)` | Линейная интерполяция между соответствующими значениями двух матриц. |

## <a name="methods"></a>Методы

| Имя | Описание |
|-|-|
| `static float4x4 identity()` | Возвращает экземпляр матрицы идентификаторов. |

## <a name="operators"></a>Операторы

| Имя | Описание |
|-|-|
| `float4x4 operator+ (float4x4 const& value1, float4x4 const& value2)` | Добавляет каждый компонент матрицы в другую матрицу. |
| `float4x4 operator- (float4x4 const& value1, float4x4 const& value2)` | Вычитает каждый компонент матрицы из другой матрицы. |
| `float4x4 operator* (float4x4 const& value1, float4x4 const& value2)` | Умножает матрицу на другую матрицу. Это влияет на объединение двух преобразований. |
| `float4x4 operator* (float4x4 const& value1, float value2)` | Умножает каждый компонент матрицы на скалярное значение. |
| `float4x4 operator- (float4x4 const& value)` | Инвертирует каждый компонент матрицы. |
| `float4x4& operator+= (float4x4& value1, float4x4 const& value2)` | На месте добавляет каждый компонент матрицы в другую матрицу. |
| `float4x4& operator-= (float4x4& value1, float4x4 const& value2)` | На месте вычитается каждый компонент матрицы из другой матрицы. |
| `float4x4& operator*= (float4x4& value1, float4x4 const& value2)` | На месте матрица умножается на другую матрицу. Это влияет на объединение двух преобразований. |
| `float4x4& operator*= (float4x4& value1, float value2)` | На месте каждый компонент матрицы умножается на скалярное значение. |
| `bool operator== (float4x4 const& value1, float4x4 const& value2)` | Определяет, равны ли два экземпляра float4x4. |
| `bool operator!= (float4x4 const& value1, float4x4 const& value2)` | Определяет, являются ли два экземпляра float4x4 неравными. |
| `operator Microsoft::?Graphics::?Canvas::?Numerics::?Matrix4x4() const` | Преобразует float4x4 в объект **Microsoft. Graphics. Холст. Numerics. Matrix4x4**. |

## <a name="fields"></a>Поля

| name | Описание |
|-|-|
| `float m11` | Значение в строке 1 столбца 1 матрицы. |
| `float m12` | Значение в строке 1 столбца 2 матрицы. |
| `float m13` | Значение в строке 1 столбца 3 матрицы. |
| `float m14` | Значение в строке 1 столбца 4 матрицы. |
| `float m21` | Значение в столбце 1 строки 2 матрицы. |
| `float m22` | Значение для столбца 2 в строке 2 матрицы. |
| `float m23` | Значение для столбца 3 в строке 2 матрицы. |
| `float m24` | Значение для столбца 4 в строке 2 матрицы. |
| `float m31` | Значение в столбце 1 строки 3 матрицы. |
| `float m32` | Значение в столбце 2 строки 3 матрицы. |
| `float m33` | Значение для столбца 3 в строке 3 матрицы. |
| `float m34` | В строке 3, столбец 4 матрицы. |
| `float m41` | В строке 4, столбец 1 матрицы. |
| `float m42` | Значение в строке 4 столбца 2 матрицы. |
| `float m43` | В строке 4, столбец 3 матрицы. |
| `float m44` | В строке 4 столбца 4 матрицы. |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Пространство имен | Windows:: Foundation:: numeric |
| Header | <dl> <dt>Виндовснумерикс. h</dt> </dl> |

## <a name="see-also"></a>См. также раздел

[API-интерфейсы виндовснумерикс. h](windowsnumerics-h-apis-portal.md)
