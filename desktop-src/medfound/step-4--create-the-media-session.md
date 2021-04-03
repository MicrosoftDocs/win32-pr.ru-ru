---
description: В этом разделе приведен шаг 4 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: Шаг 4. Создание сеанса мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103999984"
---
# <a name="step-4-create-the-media-session"></a>Шаг 4. Создание сеанса мультимедиа

В этом разделе приведен шаг 4 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

`CPlayer::CreateSession`Создает новый экземпляр сеанса мультимедиа.


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



Этот метод выполняет следующие действия:

1.  Вызывает метод `CPlayer::CloseSession` , чтобы закрыть все предыдущие экземпляры сеанса мультимедиа.
2.  Вызывает [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) для создания нового экземпляра сеанса мультимедиа.
3.  Вызывает метод [**имфмедиаевентженератор:: бегинжетевент**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) для запроса следующего события из сеанса мультимедиа. Первый параметр для **бегинжетевент** — это указатель на сам объект **кплайер** , который имплентс интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .

Обработка событий описана на шаге 5.

Далее: [Шаг 5. Работа с событиями сеанса мультимедиа](step-5--handle-media-session-events.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



