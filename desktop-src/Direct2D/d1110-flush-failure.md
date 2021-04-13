---
title: Сбой очистки D1110
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: Сбой вызова записи на диск для целевого объекта прорисовки
keywords:
- Сбой D1110 Flush Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413676"
---
# <a name="d1110-flush-failure"></a>D1110: сбой записи на диск

Неудачный вызов операции записи на диск в целевом \[ *ресурсе* прорисовки \] . Теги \[ *TAG1*, *tag2* \] .

## <a name="placeholders"></a>Заполнители

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ресурсов*
</dt> <dd>

Адрес целевого объекта прорисовки.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*TAG1*
</dt> <dd>

Первое значение тега. Дополнительные сведения см. в разделе [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Второе значение тега. Дополнительные сведения см. в разделе [**сеттагс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) .

</dd> </dl> 

|             |         |
|-------------|---------|
| Уровень ошибки | Предупреждение |



 

## <a name="examples"></a>Примеры

**Пример 1.** В следующем коде показано, что вызов Draw находится в недопустимом состоянии. Чтобы избежать предупреждающего сообщения, используйте [**сетантиалиасмоде**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) , чтобы задать \_ режим сглаживания \_ D2D1 \_ перед вызовом [**филлопаЦитимаск**](id2d1rendertarget-fillopacitymask.md) .


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





В этом примере создается следующее сообщение отладки:

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**Пример 2:** В следующем коде показано, что [**Сброс**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) вызывается после вызова [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



В этом примере создается следующее сообщение отладки:

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>Возможные причины

Вызов функции [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) может завершиться ошибкой по одной из двух причин. Может произойти сбой, поскольку метод вызывался за пределами вызова [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) или может завершиться ошибкой из-за ошибки, вызванной одной из операций целевого объекта прорисовки, которые были обработаны с момента последнего вызова метода **flush** или **EndDraw** . Чтобы устранить эту проблему, приложение должно определить причину ошибки и выполнить соответствующее действие.

## <a name="fixes"></a>Исправления

Вызов [**очистки**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) может завершиться неудачей по нескольким причинам. Приложение должно определить причину ошибки и предпринять соответствующие действия.

 

 