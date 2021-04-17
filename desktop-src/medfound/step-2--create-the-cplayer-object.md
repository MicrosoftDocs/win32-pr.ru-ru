---
description: В этом разделе приведен шаг 2 руководства по воспроизведению мультимедийных файлов с помощью Media Foundation.
ms.assetid: b489312f-ab8c-4ec6-8070-f5848034087e
title: Шаг 2. Создание объекта Кплайер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021ffa383506c0ab1be8d6c1ca327f67ed8f52f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711389"
---
# <a name="step-2-create-the-cplayer-object"></a>Шаг 2. Создание объекта Кплайер

В этом разделе приведен шаг 2 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md). Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).

Чтобы создать экземпляр `CPlayer` класса, приложение вызывает статический `CPlayer::CreateInstance` метод. Этот метод принимает следующие параметры:

-   *хвидео* указывает окно для вывода видео.
-   *Хевент* указывает окно для получения событий. Допускается передача одного и того же дескриптора для обоих дескрипторов окна.
-   *ппплайер* получает указатель на новый `CPlayer` экземпляр.

В следующем примере кода показан метод `CreateInstance`:


```C++
//  Static class method to create the CPlayer object.

HRESULT CPlayer::CreateInstance(
    HWND hVideo,                  // Video window.
    HWND hEvent,                  // Window to receive notifications.
    CPlayer **ppPlayer)           // Receives a pointer to the CPlayer object.
{
    if (ppPlayer == NULL)
    {
        return E_POINTER;
    }

    CPlayer *pPlayer = new (std::nothrow) CPlayer(hVideo, hEvent);
    if (pPlayer == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pPlayer->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppPlayer = pPlayer;
    }
    else
    {
        pPlayer->Release();
    }
    return hr;
}

HRESULT CPlayer::Initialize()
{
    // Start up Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        m_hCloseEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
        if (m_hCloseEvent == NULL)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }
    return hr;
}
```



В следующем коде показан `CPlayer` конструктор:


```C++
CPlayer::CPlayer(HWND hVideo, HWND hEvent) : 
    m_pSession(NULL),
    m_pSource(NULL),
    m_pVideoDisplay(NULL),
    m_hwndVideo(hVideo),
    m_hwndEvent(hEvent),
    m_state(Closed),
    m_hCloseEvent(NULL),
    m_nRefCount(1)
{
}
```



Конструктор выполняет следующие действия:

1.  Вызывает [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации платформы Media Foundation.
2.  Создает событие автоматического сброса. Это событие используется при закрытии сеанса мультимедиа. см. [Шаг 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md).

Деструктор завершает сеанс мультимедиа, как описано в [шаге 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md).


```C++
CPlayer::~CPlayer()
{
    assert(m_pSession == NULL);  
    // If FALSE, the app did not call Shutdown().

    // When CPlayer calls IMediaEventGenerator::BeginGetEvent on the
    // media session, it causes the media session to hold a reference 
    // count on the CPlayer. 
    
    // This creates a circular reference count between CPlayer and the 
    // media session. Calling Shutdown breaks the circular reference 
    // count.

    // If CreateInstance fails, the application will not call 
    // Shutdown. To handle that case, call Shutdown in the destructor. 

    Shutdown();
}
```



Обратите внимание, что конструктор и деструктор являются защищенными методами класса. Приложение создает объект, используя статический `CreateInstance` метод. Он уничтожает объект, вызывая **IUnknown:: Release**, а не явно с помощью инструкции **Delete**.

Далее: [Шаг 3. Открытие файла мультимедиа](step-3--open-a-media-file.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Воспроизведение звука/видео](audio-video-playback.md)
</dt> <dt>

[Воспроизведение мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



