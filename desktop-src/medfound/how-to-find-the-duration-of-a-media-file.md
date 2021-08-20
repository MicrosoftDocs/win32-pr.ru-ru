---
description: Как определить длительность файла мультимедиа.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Как определить длительность файла мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1885d356be54875079341eabc7433c9753792daf01c4848a00ee4ed4fbb343ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878848"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Как определить длительность файла мультимедиа

Чтобы узнать длительность файла мультимедиа, выполните следующие действия.

1.  Используйте [сопоставитель источников](source-resolver.md) для создания источника мультимедиа, который может проанализировать файл мультимедиа.
2.  Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа. Этот метод возвращает дескриптор представления, описывающий содержимое файла мультимедиа.
3.  Запросите дескриптор представления для атрибута " [ \_ \_ Продолжительность MF PD](mf-pd-duration-attribute.md) ", вызвав метод [**имфаттрибутес:: ' UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) '. Значение атрибута, если оно имеется, является длительностью файла в 100-наносекундных единицах.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> </dl>

 

 



