---
description: Установка скорости воспроизведения в сеансе мультимедиа
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Установка скорости воспроизведения в сеансе мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696932d0da0147ba87e49cbc22d7ad53a525bc52c9bc2b3518c0f3e956a650aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465994"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Установка скорости воспроизведения в сеансе мультимедиа

Для реализации таких функций воспроизведения, как быстрая переадресация и перемотка назад, приложениям может потребоваться изменить скорость воспроизведения потока мультимедиа. Media Foundation предоставляет службу контроля скорости, которую приложения должны использовать для динамического задания скорости воспроизведения.

Перед установкой скорости воспроизведения приложение должно проверить, поддерживается ли скорость источником мультимедиа. Сведения о запросах поддерживаемых тарифов см. [в разделе Определение поддерживаемых тарифов](how-to-determine-supported-rates.md).

Сведения о тарифах на воспроизведение см. в разделе [сведения об управлении скоростью](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>Установка скорости воспроизведения

1.  Вызовите [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , чтобы получить объект управления скоростью из сеанса мультимедиа.

    Приложения, вызывающие [**мфжетсервице**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) , должны обеспечить следующее:

    -   Параметр *объект punkObject* содержит инициализированный указатель интерфейса [**имфмедиасессион**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .
    -   Объект управления скоростью, полученный в параметре *ппвобжект* , освобождается, чтобы избежать утечек памяти.

2.  Вызовите метод [**имфратеконтрол:: сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) , чтобы задать скорость воспроизведения. После асинхронного завершения **сетрате** приложение получает событие [месессионратечанжед](mesessionratechanged.md) .

## <a name="example"></a>Пример

В следующем коде показано, как задать скорость воспроизведения, вызвав метод [**сетрате**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) .


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



Приложение должно быть остановлено или приостановлено, прежде чем оно сможет выполнить переход с отрицательной или нулевой ставки на положительный коэффициент. Сведения об этих состояниях см. [в разделе Управление состояниями представления](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сеанс мультимедиа](media-session.md)
</dt> <dt>

[Управление скоростью](rate-control.md)
</dt> <dt>

[поиск, Быстрая прокрутка и обратная игра](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



