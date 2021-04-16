---
title: ID2D1Geometry Компутепоинтатленгс методы
description: Вычисляет точку и вектор касательных на заданном расстоянии вдоль геометрии \ 160;.
ms.assetid: b76aa3db-2967-4baa-a449-f664b080fb74
keywords:
- Методы Компутепоинтатленгс Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 5b49be0b5a17dd828c9bd86ca41b4a3ff115f47a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680022"
---
# <a name="id2d1geometrycomputepointatlength-methods"></a>Методы ID2D1Geometry:: Компутепоинтатленгс

Вычисляет точку и вектор касательных на заданном расстоянии вдоль геометрии.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                        | Описание                                                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Компутепоинтатленгс (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F&, D2D1 \_ точка \_ 2F \* , D2D1 \_ Point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f__d2d1_point_2f_d2d1_point_2f))              | Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием отклонения по умолчанию.<br/>   |
| [**Компутепоинтатленгс (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F \* , D2D1 \_ точка \_ 2F \* , D2D1 \_ Point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_d2d1_point_2f_d2d1_point_2f))             | Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием отклонения по умолчанию.<br/>   |
| [**Компутепоинтатленгс (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F&, float, D2D1 \_ точка \_ 2F \* , D2D1 \_ Point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-combinewithgeometry(id2d1geometry_d2d1_combine_mode_constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink))  | Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием указанного допуска.<br/> |
| [**Компутепоинтатленгс (FLOAT, D2D1 \_ Matrix \_ 3X2 \_ F \* , float, D2D1 \_ точка \_ 2F \* , D2D1 \_ Point \_ 2F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computepointatlength(float_constd2d1_matrix_3x2_f_float_d2d1_point_2f_d2d1_point_2f)) | Вычисляет точку и вектор касательно на заданном расстоянии относительно геометрии после преобразования в указанной матрице и плоской с использованием указанного допуска.<br/> |



## <a name="examples"></a>Примеры

В следующем примере кода показано, как использовать **компутепоинтатленгс** для вычисления точки и вектора касательно на заданном расстоянии вдоль геометрии.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;
```




```C++
// Ask the geometry to give us the point that corresponds with the
// length at the current time.
hr = m_pPathGeometry->ComputePointAtLength(
    length, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

