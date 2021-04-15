---
description: Как определить длительность файла мультимедиа.
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Как определить длительность файла мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104547362"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> </dl>

 

 



