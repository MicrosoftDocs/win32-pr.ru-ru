---
description: Как выполнить очистку
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Как выполнить очистку
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab86ae39567132352592883b7441e4f325cb1b021b74e5b7a67f4a2755c3c947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063361"
---
# <a name="how-to-perform-scrubbing"></a>Как выполнить очистку

Очистка выполняется для мгновенного поиска конкретных точек в файле путем взаимодействия с визуальным представлением времени, например с помощью полосы прокрутки. В Media Foundation очистка означает поиск в файле и получение одного обновленного кадра.

Дополнительные сведения об очистке см. в разделе [сведения об управлении скоростью](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Выполнение очистки

1.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить интерфейс [**Имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из [сеанса мультимедиа](media-session.md).
    > [!Note]  
    > Не получает интерфейс [**имфратеконтрол**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) из источника мультимедиа. Всегда получите интерфейс из сеанса мультимедиа.

     

2.  Вызовите [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) , чтобы установить скорость воспроизведения равным нулю. Дополнительные сведения о вызове этого метода см. в разделе [Установка скорости воспроизведения в сеансе мультимедиа](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Создайте положение поиска в **пропвариант** , указав время презентации для поиска в типе **мфтиме** .
4.  Вызовите [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) с позицией поиска, чтобы начать воспроизведение.
5.  После завершения операции очистки сеанс мультимедиа отправляет событие [месессионскрубсамплекомплете](mesessionscrubsamplecomplete.md) . Дождитесь этого события перед повторным вызовом [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) для другой операции очистки.

## <a name="example"></a>Пример

В следующем примере кода показано, как выполнить очистку.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Успешная операция очистки создает событие [месессионскрубсамплекомплете](mesessionscrubsamplecomplete.md) после того, как все приемники потока обновляются новым кадром, а операция очистки завершается успешно. При очистке видеофайла отображается кадр, который был выполнен, но не создает звуковые выходные данные.

Приложение может выполнять пошаговое выполнение кадра, устанавливая скорость воспроизведения равным нулю, а затем передавая **пропвариант** , для которого задано значение **VT \_ Empty** , в вызове [**имфмедиасессион:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Управление скоростью](rate-control.md)
</dt> </dl>

 

 



