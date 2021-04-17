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
# <a name="step-2-create-the-cplayer-object"></a><span data-ttu-id="7966f-103">Шаг 2. Создание объекта Кплайер</span><span class="sxs-lookup"><span data-stu-id="7966f-103">Step 2: Create the CPlayer Object</span></span>

<span data-ttu-id="7966f-104">В этом разделе приведен шаг 2 руководства по [воспроизведению мультимедийных файлов с помощью Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="7966f-104">This topic is step 2 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="7966f-105">Полный код показан в разделе [Пример воспроизведения сеанса мультимедиа](media-session-playback-example.md).</span><span class="sxs-lookup"><span data-stu-id="7966f-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="7966f-106">Чтобы создать экземпляр `CPlayer` класса, приложение вызывает статический `CPlayer::CreateInstance` метод.</span><span class="sxs-lookup"><span data-stu-id="7966f-106">To create an instance of the `CPlayer` class, the application calls the static `CPlayer::CreateInstance` method.</span></span> <span data-ttu-id="7966f-107">Этот метод принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="7966f-107">This method takes the following parameters:</span></span>

-   <span data-ttu-id="7966f-108">*хвидео* указывает окно для вывода видео.</span><span class="sxs-lookup"><span data-stu-id="7966f-108">*hVideo* specifies the window to display video.</span></span>
-   <span data-ttu-id="7966f-109">*Хевент* указывает окно для получения событий.</span><span class="sxs-lookup"><span data-stu-id="7966f-109">*hEvent* specifies a window to receive events.</span></span> <span data-ttu-id="7966f-110">Допускается передача одного и того же дескриптора для обоих дескрипторов окна.</span><span class="sxs-lookup"><span data-stu-id="7966f-110">It is valid to pass the same handle for both window handles.</span></span>
-   <span data-ttu-id="7966f-111">*ппплайер* получает указатель на новый `CPlayer` экземпляр.</span><span class="sxs-lookup"><span data-stu-id="7966f-111">*ppPlayer* receives a pointer to a new `CPlayer` instance.</span></span>

<span data-ttu-id="7966f-112">В следующем примере кода показан метод `CreateInstance`:</span><span class="sxs-lookup"><span data-stu-id="7966f-112">The following code shows the `CreateInstance` method:</span></span>


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



<span data-ttu-id="7966f-113">В следующем коде показан `CPlayer` конструктор:</span><span class="sxs-lookup"><span data-stu-id="7966f-113">The following code shows the `CPlayer` constructor:</span></span>


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



<span data-ttu-id="7966f-114">Конструктор выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7966f-114">The constructor does the following:</span></span>

1.  <span data-ttu-id="7966f-115">Вызывает [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) для инициализации платформы Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="7966f-115">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
2.  <span data-ttu-id="7966f-116">Создает событие автоматического сброса.</span><span class="sxs-lookup"><span data-stu-id="7966f-116">Creates an auto-reset event.</span></span> <span data-ttu-id="7966f-117">Это событие используется при закрытии сеанса мультимедиа. см. [Шаг 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="7966f-117">This event is used when closing the Media Session; see [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>

<span data-ttu-id="7966f-118">Деструктор завершает сеанс мультимедиа, как описано в [шаге 7. Завершение сеанса мультимедиа](step-7--shut-down-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="7966f-118">The destructor shuts down the Media Session, as described in [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md).</span></span>


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



<span data-ttu-id="7966f-119">Обратите внимание, что конструктор и деструктор являются защищенными методами класса.</span><span class="sxs-lookup"><span data-stu-id="7966f-119">Note that the constructor and destructor are both protected class methods.</span></span> <span data-ttu-id="7966f-120">Приложение создает объект, используя статический `CreateInstance` метод.</span><span class="sxs-lookup"><span data-stu-id="7966f-120">The application creates the object using the static `CreateInstance` method.</span></span> <span data-ttu-id="7966f-121">Он уничтожает объект, вызывая **IUnknown:: Release**, а не явно с помощью инструкции **Delete**.</span><span class="sxs-lookup"><span data-stu-id="7966f-121">It destroys the object by calling **IUnknown::Release**, rather than explicitly using **delete**.</span></span>

<span data-ttu-id="7966f-122">Далее: [Шаг 3. Открытие файла мультимедиа](step-3--open-a-media-file.md)</span><span class="sxs-lookup"><span data-stu-id="7966f-122">Next: [Step 3: Open a Media File](step-3--open-a-media-file.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="7966f-123">См. также</span><span class="sxs-lookup"><span data-stu-id="7966f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7966f-124">Воспроизведение звука/видео</span><span class="sxs-lookup"><span data-stu-id="7966f-124">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="7966f-125">Воспроизведение мультимедийных файлов с помощью Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7966f-125">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



