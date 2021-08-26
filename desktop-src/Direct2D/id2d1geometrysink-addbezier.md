---
title: Методы Аддбезиер ID2D1GeometrySink (D2d1. h)
description: Создает кривую Безье третьего порядка между текущей точкой и заданной конечной точкой и добавляет ее в приемник геометрии.
ms.assetid: d1e228eb-dac6-485d-b3c9-69b2bd45e531
keywords:
- Методы Аддбезиер Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 5dff3f4a59b592b4820bf6e91f9415da98a0960cf333afc48115f894111d423b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917824"
---
# <a name="id2d1geometrysinkaddbezier-methods"></a>Методы ID2D1GeometrySink:: Аддбезиер

Создает кривую Безье третьего порядка между текущей точкой и заданной конечной точкой и добавляет ее в приемник геометрии.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                            | Описание                                                                                    |
|:--------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Аддбезиер ( \_ сегмент Безье D2D1 \_&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment_))  | Создает кривую Безье третьего порядка между текущей и заданной конечной точками.<br/> |
| [**Аддбезиер ( \_ сегмент Безье \_ D2D1 \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addbezier(constd2d1_bezier_segment)) | Создает кривую Безье третьего порядка между текущей точкой и указанной конечной точкой.<br/>  |



## <a name="examples"></a>Примеры

В следующем примере создается [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry), извлекается приемник и используется для определения формы песочных часов. Полный пример см. в разделе [Рисование и заполнение сложной фигуры](how-to-draw-and-fill-a-complex-shape.md).


```C++
ID2D1GeometrySink *pSink = NULL;



// Create a path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);

    if (SUCCEEDED(hr))
    {
        // Write to the path geometry using the geometry sink.
        hr = m_pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            pSink->BeginFigure(
                D2D1::Point2F(0, 0),
                D2D1_FIGURE_BEGIN_FILLED
                );

            pSink->AddLine(D2D1::Point2F(200, 0));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(150, 50),
                    D2D1::Point2F(150, 150),
                    D2D1::Point2F(200, 200))
                );

            pSink->AddLine(D2D1::Point2F(0, 200));

            pSink->AddBezier(
                D2D1::BezierSegment(
                    D2D1::Point2F(50, 150),
                    D2D1::Point2F(50, 50),
                    D2D1::Point2F(0, 0))
                );

            pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

            hr = pSink->Close();
        }
        SafeRelease(&pSink);
    }
}
```





## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink)
</dt> </dl>

�

�
