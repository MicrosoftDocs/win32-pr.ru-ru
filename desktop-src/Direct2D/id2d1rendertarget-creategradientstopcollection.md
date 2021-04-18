---
title: Методы Креатеградиентстопколлектион ID2D1RenderTarget (D2d1 \_ 1. h)
description: Создает объект ID2D1GradientStopCollection из указанного массива элементов D2D1 \_ градиента \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Методы Креатеградиентстопколлектион Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4a298414d1a84b03d81c80e308113d8731369040
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685280"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>Методы ID2D1RenderTarget:: Креатеградиентстопколлектион

Создает объект [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из указанного массива элементов [**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .

### <a name="overload-list"></a>Список перегрузок



| Метод                                                                                                                                                                                                                                                               | Описание                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Креатеградиентстопколлектион (D2D1 \_ градиента \_ \* , D2D1 \_ гамма, \_ режим расширенного развертывания D2D1 \_ , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-d2d1-gamma-d2d1-extend-mode-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx) | Создает [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) из указанных ограничителей градиента, гаммы интерполяции цвета и режима расширения. <br/>                                                              |
| [**Креатеградиентстопколлектион (D2D1 \_ градиента \_ \* , ID2D1GradientStopCollection \* \* )**](id2d1rendertarget-creategradientstopcollection-ptr-d2d1-gradient-stop-ptr-ptr-https://msdn.microsoft.com/library/Dd316783(v=VS.85).aspx)                                                            | Создает объект [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) на основе заданных ограничителей градиента, который использует гамму гаммы [**D2D1 \_ \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) для интерполяции цвета и режим расширения среза.<br/> |



## <a name="examples"></a>Примеры

В следующем примере создается массив ограничителей градиента, а затем он используется для создания [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



В следующем примере кода используется [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) для создания [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (включение D2d1. h)</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**D2D1 \_ градиента \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Создание кисти линейного градиента](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Создание кисти радиального градиента](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Обзор кистей](direct2d-brushes-overview.md)
</dt> </dl>
