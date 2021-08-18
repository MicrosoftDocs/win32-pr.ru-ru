---
title: Методы Креатетрансформеджеометри ID2D1Factory (D2d1. h)
description: Преобразует указанную геометрию и сохраняет результат в виде объекта ID2D1TransformedGeometry.
ms.assetid: 71f26200-0f35-49d7-951d-2962768d16bc
keywords:
- Методы Креатетрансформеджеометри Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 8216b5b63951e3f393dc1c8a204a4a4e38ee652d79eb795ba4f4e97041aff3f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832854"
---
# <a name="id2d1factorycreatetransformedgeometry-methods"></a>Методы ID2D1Factory:: Креатетрансформеджеометри

Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) .

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                  | Описание                                                                                                                                    |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатетрансформеджеометри (ID2D1Geometry \* , \_ Матрица D2D \_ 3X2 \_ F \* , ID2D1TransformedGeometry \* \* )**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) | Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |
| [**Креатетрансформеджеометри (ID2D1Geometry \* , \_ Матрица D2D \_ 3X2 \_ F&, ID2D1TransformedGeometry \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry))  | Преобразует указанную геометрию и сохраняет результат в виде объекта [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85)) . <br/> |



## <a name="remarks"></a>Remarks

Как и другие ресурсы, преобразованная геометрия наследует пространство ресурсов и политику потоков фабрики, создавшей ее. Этот объект является неизменяемым.

При обводке преобразованной геометрии с помощью метода [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) на толщину штриха не влияет преобразование, применяемое к геометрии. Ширина штриха зависит только от универсального преобразования.

## <a name="examples"></a>Примеры

В следующем примере создается [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry)), а затем рисуется без его преобразования. Он создает выходные данные, показанные на следующем рисунке.

![Иллюстрация прямоугольника](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```



В следующем примере используется целевой объект отрисовки для масштабирования геометрии по коэффициенту 3, после чего рисуется. На следующем рисунке показан результат рисования прямоугольника без преобразования и преобразования. Обратите внимание, что после преобразования штрих становится толще, несмотря на то, что толщина штриха равна 1.

![Рисунок меньшего прямоугольника внутри более крупного прямоугольника с толстой обводкой](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



В следующем примере используется метод **креатетрансформеджеометри** для масштабирования геометрии по коэффициенту 3, после чего рисуется. Он создает выходные данные, показанные на следующем рисунке. Обратите внимание, что, хотя размер прямоугольника больше, его штрих не увеличился.

![Иллюстрация прямоугольника меньшего размера внутри более крупного прямоугольника с одинаковой обводкой](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );


// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```





## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
