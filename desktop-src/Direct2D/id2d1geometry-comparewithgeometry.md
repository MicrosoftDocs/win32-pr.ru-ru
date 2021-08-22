---
title: ID2D1Geometry Компаревисжеометри методы
description: Описывает пересечение между этой геометрией и заданной геометрией.
ms.assetid: 75ddd674-b50b-4d34-b291-9e7e65828304
keywords:
- Методы Компаревисжеометри Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09978c38c3e4be7ad8a86ccfccb43387ed4ac48232e39e1ed19001d806362c88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119304804"
---
# <a name="id2d1geometrycomparewithgeometry-methods"></a>Методы ID2D1Geometry:: Компаревисжеометри

Описывает пересечение между этой геометрией и заданной геометрией.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                            | Описание                                                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Компаревисжеометри (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3X2 \_ F&, D2D1 \_ геометрическая \_ связь \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__d2d1_geometry_relation))              | Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с использованием отклонения спрямления по умолчанию.<br/>      |
| [**Компаревисжеометри (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3X2 \_ F \* , D2D1 \_ геометрическая \_ связь \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_d2d1_geometry_relation))             | Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с использованием отклонения спрямления по умолчанию.<br/>      |
| [**Компаревисжеометри (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3X2 \_ F&, float, D2D1 \_ геометрическая \_ связь \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f__float_d2d1_geometry_relation))  | Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с заданной допускной обпрозрачкой.<br/>    |
| [**Компаревисжеометри (ID2D1Geometry \* , D2D1 \_ Matrix \_ 3X2 \_ F \* , float, D2D1 \_ геометрическая \_ связь \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-comparewithgeometry(id2d1geometry_constd2d1_matrix_3x2_f_float_d2d1_geometry_relation)) | Описывает пересечение между этой геометрией и заданной геометрией. Сравнение выполняется с использованием указанного допуска обработки прозрачности.<br/> |



## <a name="remarks"></a>Remarks

При интерпретации возвращаемого значения *отношения* важно помнить, что [**\_ отношение геометрического элемента D2D1 \_ \_ состоит \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) из типа перечисления **D2D1 \_ Geometry \_** , что означает, что эта геометрия содержится внутри *инпутжеометри*, а не в том, что эта геометрия содержит *инпутжеометри*.

Дополнительные сведения о том, как интерпретировать другие возможные возвращаемые значения, см. в разделе [**D2D1 \_ Geometry \_ RELATION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)
</dt> </dl>

 

