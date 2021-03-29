---
title: Методы структуры ID2D1Geometry
description: Выполняет вычисление контура геометрии и записывает результат в ID2D1SimplifiedGeometrySink.
ms.assetid: ec92db79-a1aa-4661-9e75-45a1763af370
keywords:
- Методы структуры Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 40d4ff1122d4a00e11ea35914f001b6dc9e06e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657646"
---
# <a name="id2d1geometryoutline-methods"></a>Методы ID2D1Geometry:: структуризации

Выполняет вычисление контура геометрии и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                          | Описание                                                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Структура (D2D1 \_ Matrix \_ 3X2 \_ F&, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink))              | Выполняет вычисление контура геометрии и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). <br/> |
| [**Структура (D2D1 \_ Matrix \_ 3X2 \_ F \* , ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_id2d1simplifiedgeometrysink))             | Выполняет вычисление контура геометрии и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Структура (D2D1 \_ Matrix \_ 3X2 \_ F&, float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__float_id2d1simplifiedgeometrysink))  | Выполняет вычисление контура геометрии и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |
| [**Структура (D2D1 \_ Matrix \_ 3X2 \_ F \* , float, ID2D1SimplifiedGeometrySink \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f_float_id2d1simplifiedgeometrysink)) | Выполняет вычисление контура геометрии и записывает результат в [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink).<br/>  |



## <a name="remarks"></a>Комментарии

Метод [**структуры**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) позволяет вызывающему объекту создать геометрию с эквивалентной заливкой для входной геометрии со следующими дополнительными свойствами:

-   Выходная геометрия не содержит пересечения с поворотом. Это значит, что сегменты могут касаться, но они никогда не пересекаются.
-   Самые наружные фигуры в выходной геометрии ориентированы против часовой стрелки.
-   Выходная геометрия — это инвариантный режим заливки; то есть заливка геометрии не зависит от выбора режима заполнения. Дополнительные сведения о режиме заполнения см. в разделе [**\_ \_ режим заполнения D2D1**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode).

Кроме того, метод [**структуры**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometry-outline(constd2d1_matrix_3x2_f__id2d1simplifiedgeometrysink)) может быть полезен при удалении избыточных частей таких геометрических объектов для упрощения сложных геометрических объектов. Его также можно использовать в сочетании с [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) , чтобы создавать объединения между несколькими геометриями одновременно.

## <a name="examples"></a>Примеры

В следующем коде показано, как использовать **структуру** для создания эквивалентной геометрии без самостоятельных пересечения. Он использует допуск по умолчанию для обработки и, следовательно, не должен использоваться с очень маленькими геометриями.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
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

 

