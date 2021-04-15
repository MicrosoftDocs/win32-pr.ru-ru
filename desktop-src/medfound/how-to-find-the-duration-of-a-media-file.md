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
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="0ffdf-103">Как определить длительность файла мультимедиа</span><span class="sxs-lookup"><span data-stu-id="0ffdf-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="0ffdf-104">Чтобы узнать длительность файла мультимедиа, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="0ffdf-105">Используйте [сопоставитель источников](source-resolver.md) для создания источника мультимедиа, который может проанализировать файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="0ffdf-106">Вызовите [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) в источнике мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="0ffdf-107">Этот метод возвращает дескриптор представления, описывающий содержимое файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="0ffdf-108">Запросите дескриптор представления для атрибута " [ \_ \_ Продолжительность MF PD](mf-pd-duration-attribute.md) ", вызвав метод [**имфаттрибутес:: ' UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) '.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="0ffdf-109">Значение атрибута, если оно имеется, является длительностью файла в 100-наносекундных единицах.</span><span class="sxs-lookup"><span data-stu-id="0ffdf-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0ffdf-110">См. также</span><span class="sxs-lookup"><span data-stu-id="0ffdf-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ffdf-111">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="0ffdf-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



