---
description: Чистый виртуальный метод, переопределяемый производными классами.
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: Кбасеконтролвидео. ЖетстатиЦимаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69496754c8a1f80be341c475f422229aba6108dbc0e73cd1db9506a301690ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660834"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>Кбасеконтролвидео. ЖетстатиЦимаже, метод

Чистый виртуальный метод, переопределяемый производными классами.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пбуфферсизе* 
</dt> <dd>

Указатель на размер выходного буфера.

</dd> <dt>

*пдибимаже* 
</dt> <dd>

Указатель на выходной буфер.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** .

## <a name="remarks"></a>Remarks

С помощью интерфейса [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) приложение может запрашивать, что ему предоставляется копия текущего изображения в буфере памяти (некоторые модули подготовки отчетов могут возвращать в него значение E \_ нотимпл, если они не поддерживаются). Производный класс определяет способ получения изображения. Когда приложение вызывает **кбасеконтролвидео:: жетстатиЦимаже**, оно вызывает чистый виртуальный метод, который производный класс должен переопределить для его реализации. Это также вызывается функцией-членом [**кбасеконтролвидео:: жеткуррентимаже**](cbasecontrolvideo-getcurrentimage.md) .

Класс предоставляет вспомогательную функцию-член [**кбасеконтролвидео:: копимаже**](cbasecontrolvideo-copyimage.md), которой можно предоставить образец, содержащий изображение, а функция-член скопирует соответствующий раздел (на основе текущего исходного прямоугольника) в выходной буфер, предоставленный приложением.

В следующем примере демонстрируется реализация этой функции-члена в производном классе. В этом примере m \_ прендерер содержит объект класса, производного от [**кбасевидеорендерер**](cbasevideorenderer.md).


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасеконтролвидео**](cbasecontrolvideo.md)
</dt> </dl>

 

 




