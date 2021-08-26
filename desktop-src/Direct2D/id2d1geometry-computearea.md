---
title: ID2D1Geometry Компутеареа методы
description: Выполняет вычисление области геометрии.
ms.assetid: 655f11bc-7435-4d23-b4b1-3d7c2110aa48
keywords:
- Методы Компутеареа Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 344cb55314c3cafc2e84479944342633c74bd5a35754c9f7a4f6d53a30da58fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044174"
---
# <a name="id2d1geometrycomputearea-methods"></a>Методы ID2D1Geometry:: Компутеареа

Выполняет вычисление области геометрии.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                      | Описание                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F&, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float))              | Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием отклонения по умолчанию.<br/>    |
| [**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F \* , float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float))             | Выполняет вычисление области геометрии после ее преобразования в указанную матрицу и плоской с использованием отклонения по умолчанию.<br/> |
| [**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F&, float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f__float_float))  | Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.<br/>  |
| [**Компутеареа (D2D1 \_ Matrix \_ 3X2 \_ F \* , float, float \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-computearea(constd2d1_matrix_3x2_f_float)) | Выполняет вычисление области геометрии после преобразования указанной матрицы и плоской с использованием указанного допуска.<br/>  |



## <a name="examples"></a>Примеры

В следующем примере кода используется **компутеареа** для вычислить площадь указанного круга (**m \_ pCircleGeometry1**).


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

