---
description: В этом разделе описывается этап 3 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: cc0d2b60-64d7-49f3-844f-97487cab8466
title: Шаг 3. Открытие файла мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b50f036b84806f96e4349f77a3f06e02e08764
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081710"
---
# <a name="step-3-open-a-media-file"></a>Шаг 3. Открытие файла мультимедиа

В этом разделе описывается этап 3 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

`CPlayer::OpenURL`Метод открывает файл мультимедиа из URL-адреса.


```C++
//  Open a URL for playback.
HRESULT CPlayer::OpenURL(const WCHAR *sURL)
{
    // 1. Create a new media session.
    // 2. Create the media source.
    // 3. Create the topology.
    // 4. Queue the topology [asynchronous]
    // 5. Start playback [asynchronous - does not happen in this method.]

    IMFTopology *pTopology = NULL;
    IMFPresentationDescriptor* pSourcePD = NULL;

    // Create the media session.
    HRESULT hr = CreateSession();
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the media source.
    hr = CreateMediaSource(sURL, &m_pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the presentation descriptor for the media source.
    hr = m_pSource->CreatePresentationDescriptor(&pSourcePD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pSourcePD, m_hwndVideo, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

    // If SetTopology succeeds, the media session will queue an 
    // MESessionTopologySet event.

done:
    if (FAILED(hr))
    {
        m_state = Closed;
    }

    SafeRelease(&pSourcePD);
    SafeRelease(&pTopology);
    return hr;
}
```



Этот метод выполняет следующие действия:

1.  Вызывает **кплайер:: CreateSession** для создания нового экземпляра сеанса мультимедиа. См. [Шаг 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md).
2.  Создает источник мультимедиа по URL-адресу. Полный код для этого шага приведен в разделе [Использование сопоставителя источников](using-the-source-resolver.md).
3.  Вызывает [**имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) , чтобы получить дескриптор представления источника мультимедиа. Дескриптор представления описывает каждый поток в исходном файле.
4.  Создает топологию воспроизведения. Код для этого шага показан в разделе [Создание топологий воспроизведения](creating-playback-topologies.md).
5.  Вызывает [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) , чтобы задать топологию в сеансе мультимедиа.

Метод [**сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) завершается асинхронно. По завершении вызывается метод [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) объекта кплайер; см. [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md).

Далее: [Шаг 4. Создание сеанса мультимедиа](step-4--create-the-media-session.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



