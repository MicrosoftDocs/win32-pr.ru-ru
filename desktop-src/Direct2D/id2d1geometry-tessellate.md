---
title: Методы тесселяции ID2D1Geometry
description: Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском.
ms.assetid: 4e0af188-d14b-43c0-be11-16577f054b90
keywords:
- Методы тесселяции Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: b40602fb38ec2a0834ba202252114f7c0c34a4948e4473703ff4daf8bf2ee97a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917894"
---
# <a name="id2d1geometrytessellate-methods"></a>Методы ID2D1Geometry:: тесселяции

Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                    | Описание                                                                                                                                                                          |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Тесселяция (D2D1 \_ Matrix \_ 3X2 \_ F \* , ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__id2d1tessellationsink))             | Создает набор треугольников по часовой стрелке, которые охватывают геометрию после ее преобразования с помощью указанной матрицы и обравниваются с использованием отклонения по умолчанию. <br/>   |
| [**Тесселяция (D2D1 \_ Matrix \_ 3X2 \_ F&, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_id2d1tessellationsink))              | Создает набор треугольников по часовой стрелке, которые охватывают геометрию после ее преобразования с помощью указанной матрицы и обравниваются с использованием отклонения по умолчанию. <br/>   |
| [**Тесселяция (D2D1 \_ Matrix \_ 3X2 \_ F \* , float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f_float_id2d1tessellationsink)) | Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском. <br/> |
| [**Тесселяция (D2D1 \_ Matrix \_ 3X2 \_ F&, float, ID2D1TessellationSink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-tessellate(constd2d1_matrix_3x2_f__float_id2d1tessellationsink))  | Создает набор повернутых по часовой стрелке треугольников, покрывающих геометрию после ее преобразования с использованием заданной матрицы и выпрямления с заданным допуском.<br/>  |



## <a name="examples"></a>Примеры

В следующем примере кода показано использование тесселяции для создания набора треугольников по часовой стрелке, охватывающих геометрию.


```C++
 ID2D1GeometrySink *pGeometrySink = NULL;
 hr = pPathGeometry->Open(&pGeometrySink);
 if (SUCCEEDED(hr))
 {
     hr = pGeometry->Widen(
             strokeWidth,
             pIStrokeStyle,
             pWorldTransform,
             pGeometrySink
             );

     if (SUCCEEDED(hr))
     {
         hr = pGeometrySink->Close();
         if (SUCCEEDED(hr))
         {
             ID2D1Mesh *pMesh = NULL;
             hr = m_pRT->CreateMesh(&pMesh);
             if (SUCCEEDED(hr))
             {
                 ID2D1TessellationSink *pSink = NULL;
                 hr = pMesh->Open(&pSink);
                 if (SUCCEEDED(hr))
                 {
                     hr = pPathGeometry->Tessellate(
                             NULL, // world transform (already handled in Widen)
                             pSink
                             );
                     if (SUCCEEDED(hr))
                     {
                         hr = pSink->Close();
                         if (SUCCEEDED(hr))
                         {
                             SafeReplace(&m_pStrokeMesh, pMesh);
                         }
                     }
                     pSink->Release();
                 }
                 pMesh->Release();
             }
         }
     }
     pGeometrySink->Release();
 }
 pPathGeometry->Release();
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

 

