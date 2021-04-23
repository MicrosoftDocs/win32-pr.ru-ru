---
description: Интерфейс Дуккинг по умолчанию, предоставляемый системой, утками все потоки, не связанные с обменом данными, доступные в системе при открытии коммуникационного потока.
ms.assetid: 1b92574e-7cde-49c0-a68e-223492412361
title: Рекомендации по реализации для уведомлений Дуккинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de07ea23b7cdc8d726ab68a5a6554bf1713a921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141857"
---
# <a name="implementation-considerations-for-ducking-notifications"></a><span data-ttu-id="efeb4-103">Рекомендации по реализации для уведомлений Дуккинг</span><span class="sxs-lookup"><span data-stu-id="efeb4-103">Implementation Considerations for Ducking Notifications</span></span>

<span data-ttu-id="efeb4-104">[Интерфейс Дуккинг по умолчанию](stream-attenuation.md) , предоставляемый системой, утками все потоки, не связанные с обменом данными, доступные в системе при открытии коммуникационного потока.</span><span class="sxs-lookup"><span data-stu-id="efeb4-104">The [Default Ducking Experience](stream-attenuation.md) provided by the system ducks all non-communication streams available in the system when a communication stream opens.</span></span> <span data-ttu-id="efeb4-105">Приложение мультимедиа может переопределить обработку по умолчанию, если известно, когда начинается и заканчивается сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="efeb4-105">A media application can override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="efeb4-106">Рассмотрим сценарий, реализуемый приложением мультимедиа в примере [дуккингмедиаплайер](duckingmediaplayer.md) .</span><span class="sxs-lookup"><span data-stu-id="efeb4-106">Consider the scenario implemented by the media application in the [DuckingMediaPlayer](duckingmediaplayer.md) sample.</span></span> <span data-ttu-id="efeb4-107">Приложение приостанавливает поток звука, который воспроизводится при получении уведомления утка и возобновляет воспроизведение при получении уведомления ундукк.</span><span class="sxs-lookup"><span data-stu-id="efeb4-107">The application pauses the audio stream that it is playing when it receives a duck notification and continues playback when it receives an unduck notification.</span></span> <span data-ttu-id="efeb4-108">События приостановки и продолжения отражаются в пользовательском интерфейсе приложения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="efeb4-108">The pause and continue events are reflected in the media application's user interface.</span></span> <span data-ttu-id="efeb4-109">Это поддерживается двумя сообщениями окон, определяемыми приложением, \_ \_ сеансами приложений WM \_ дуккед и \_ \_ ундуккед сеанса приложения WM \_ .</span><span class="sxs-lookup"><span data-stu-id="efeb4-109">This is supported through two application-defined window messages, WM\_APP\_SESSION\_DUCKED and WM\_APP\_SESSION\_UNDUCKED.</span></span> <span data-ttu-id="efeb4-110">Уведомления дуккинг получаются асинхронно в фоновом режиме, и приложение мультимедиа не должно блокировать поток уведомлений для обработки оконных сообщений.</span><span class="sxs-lookup"><span data-stu-id="efeb4-110">The ducking notifications are received asynchronously in the background and the media application must not block the notification thread to process the window messages.</span></span> <span data-ttu-id="efeb4-111">Оконные сообщения должны обрабатываться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="efeb4-111">The window messages must be processed on the user interface thread.</span></span>

<span data-ttu-id="efeb4-112">Поведение дуккинг работает через механизм уведомления.</span><span class="sxs-lookup"><span data-stu-id="efeb4-112">The ducking behavior works through a notification mechanism.</span></span> <span data-ttu-id="efeb4-113">Чтобы обеспечить настраиваемый интерфейс, приложение мультимедиа должно реализовать интерфейс [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) и зарегистрировать реализацию в звуковой системе.</span><span class="sxs-lookup"><span data-stu-id="efeb4-113">To provide a customized experience, the media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="efeb4-114">После успешной регистрации приложение мультимедиа получает уведомления о событиях в форме обратных вызовов через методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="efeb4-114">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="efeb4-115">Диспетчер сеансов, обрабатывающий сеанс связи, вызывает [**иаудиоволумедуккнотификатион:: онволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) , когда поток связи открывается, а затем вызывает [**Иаудиоволумедуккнотификатион:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) при закрытии потока на коммуникационном устройстве.</span><span class="sxs-lookup"><span data-stu-id="efeb4-115">The session manager handling the communication session calls [**IAudioVolumeDuckNotification::OnVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) when the communication stream opens and then calls [**IAudioVolumeDuckNotification::OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) when the stream is closed on the communication device.</span></span>

<span data-ttu-id="efeb4-116">В следующем коде показан пример реализации интерфейса [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="efeb4-116">The following code shows a sample implementation of the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface.</span></span> <span data-ttu-id="efeb4-117">Определение Кмедиаплайер::D Уккингоптаут см. в разделе Получение событий Дуккинг с коммуникационного устройства.</span><span class="sxs-lookup"><span data-stu-id="efeb4-117">For the definition of CMediaPlayer::DuckingOptOut, see Getting Ducking Events from a Communication Device.</span></span>


```C++
class CMediaPlayer : public IAudioVolumeDuckNotification
{
    LONG _refCount;

    HWND _AppWindow;

    ~CMediaPlayer();

    STDMETHOD(OnVolumeDuckNotification) (LPCWSTR sessionID, 
                  UINT32 countCommunicationSessions);
    STDMETHOD(OnVolumeUnduckNotification) (LPCWSTR sessionID);

public:
    CDuckingImpl(HWND hWnd);
    HRESULT DuckingOptOut(bool GetDuckEvents);

    // IUnknown
    IFACEMETHODIMP QueryInterface(__in REFIID riid, __deref_out void **ppv);
    IFACEMETHODIMP_(ULONG) AddRef();
    IFACEMETHODIMP_(ULONG) Release();
};

CMediaPlayer::CMediaPlayer(HWND AppWindow) :
        _AppWindow(AppWindow),
        _refCount(1)
{
}
CMediaPlayer::~CMediaPlayer()
{
}

// When we receive a duck notification, 
// post a "Session Ducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeDuckNotification(LPCWSTR SessionID, 
                                                    UINT32 CountCommunicationsSessions)
{
    PostMessage(_AppWindow, WM_APP_SESSION_DUCKED, 0, 0);
    return 0;
}


// When we receive an unduck notification, 
// post a "Session Unducked" message to the application window.

STDMETHODIMP CMediaPlayer::OnVolumeUnduckNotification(LPCWSTR SessionID)
{
    PostMessage(_AppWindow, WM_APP_SESSION_UNDUCKED, 0, 0);
    return 0;
}

IFACEMETHODIMP CMediaPlayer::QueryInterface(REFIID iid, void **pvObject)
{
    if (pvObject == NULL)
    {
        return E_POINTER;
    }
    *pvObject = NULL;
    if (iid == IID_IUnknown)
    {
        *pvObject = static_cast<IUnknown *>(static_cast<IAudioVolumeDuckNotification *>
                                                                              (this));
        AddRef();
    }
    else if (iid == __uuidof(IAudioVolumeDuckNotification))
    {
        *pvObject = static_cast<IAudioVolumeDuckNotification *>(this);
        AddRef();
    }
    else
    {
        return E_NOINTERFACE;
    }
    return S_OK;
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::AddRef()
{
    return InterlockedIncrement(&_refCount);
}

IFACEMETHODIMP_(ULONG) CMediaPlayer::Release()
{
    LONG refs = InterlockedDecrement(&_refCount);

    if (refs == 0)
    {
        delete this; 
    }

    return refs;   
}
```



## <a name="related-topics"></a><span data-ttu-id="efeb4-118">См. также</span><span class="sxs-lookup"><span data-stu-id="efeb4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efeb4-119">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="efeb4-119">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="efeb4-120">Интерфейс Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="efeb4-120">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="efeb4-121">Отключение интерфейса Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="efeb4-121">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="efeb4-122">Предоставление пользовательского поведения Дуккинг</span><span class="sxs-lookup"><span data-stu-id="efeb4-122">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="efeb4-123">Получение событий Дуккинг</span><span class="sxs-lookup"><span data-stu-id="efeb4-123">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



