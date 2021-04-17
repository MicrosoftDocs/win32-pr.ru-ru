---
title: ID2D1Factory Креатестрокестиле методы
description: Создает ID2D1StrokeStyle, описывающий начало, штрих-шаблон и другие функции штриха.
ms.assetid: cc7bd68b-a6eb-4d05-b331-032ce80f375c
keywords:
- Методы Креатестрокестиле Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 09a578cafe6795bbf742d9dac114365d6e850586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679998"
---
# <a name="id2d1factorycreatestrokestyle-methods"></a>Методы ID2D1Factory:: Креатестрокестиле

Создает [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , описывающий начало, штрих-шаблон и другие функции штриха.

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                  | Описание                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатестрокестиле ( \_ \_ свойства стиля STROKE D2D1 \_&, float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties__constfloat_uint32_id2d1strokestyle))  | Создает [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , описывающий начало, штрих-шаблон и другие функции штриха.<br/> |
| [**Креатестрокестиле ( \_ \_ свойства стиля Stroke \_ D2D1 \* , float \* , uint, ID2D1StrokeStyle \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createstrokestyle(constd2d1_stroke_style_properties_constfloat_uint32_id2d1strokestyle)) | Создает [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) , описывающий начало, штрих-шаблон и другие функции штриха.<br/> |



## <a name="examples"></a>Примеры

В следующем примере создается штрих, использующий пользовательский шаблон штриха.


```C++
// Dash array for dashStyle D2D1_DASH_STYLE_CUSTOM
float dashes[] = {1.0f, 2.0f, 2.0f, 3.0f, 2.0f, 2.0f};

// Stroke Style with Dash Style -- Custom
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateStrokeStyle(
        D2D1::StrokeStyleProperties(
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_FLAT,
            D2D1_CAP_STYLE_ROUND,
            D2D1_LINE_JOIN_MITER,
            10.0f,
            D2D1_DASH_STYLE_CUSTOM,
            0.0f),
        dashes,
        ARRAYSIZE(dashes),
        &m_pStrokeStyleCustomOffsetZero
        );
}
```



В следующем примере используется стиль обводки при рисовании линии.


```C++
m_pRenderTarget->DrawLine(
    D2D1::Point2F(0, 310),
    D2D1::Point2F(200, 310),
    m_pCornflowerBlueBrush,
    10.0f,
    m_pStrokeStyleCustomOffsetZero
    );
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>

 

