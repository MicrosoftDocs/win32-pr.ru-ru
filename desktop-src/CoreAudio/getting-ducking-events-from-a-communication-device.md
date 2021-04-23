---
description: Приложение мультимедиа, которое хочет предоставить собственный дуккинг интерфейс, должно прослушивать уведомления о событиях при открытии или закрытии потока связи в системе.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Получение событий Дуккинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e45557c25570a89452a39683a0b6732b9632129
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538945"
---
# <a name="getting-ducking-events"></a><span data-ttu-id="2052c-103">Получение событий Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2052c-103">Getting Ducking Events</span></span>

<span data-ttu-id="2052c-104">Приложение мультимедиа, которое хочет предоставить собственный дуккинг интерфейс, должно прослушивать уведомления о событиях при открытии или закрытии потока связи в системе.</span><span class="sxs-lookup"><span data-stu-id="2052c-104">A media application that wants to provide a customised ducking experience must listen for the event notifications when a communication stream is opened or closed in the system.</span></span> <span data-ttu-id="2052c-105">Пользовательская реализация может предоставляться с помощью Медиафаундатион, DirectShow или DirectSound, использующих основные API аудио.</span><span class="sxs-lookup"><span data-stu-id="2052c-105">The custom implementation can be provided by using MediaFoundation, DirectShow, or DirectSound, which use the Core Audio APIs.</span></span> <span data-ttu-id="2052c-106">Прямой ВАСАПИ клиент может также переопределить обработку по умолчанию, если он знает, когда начинается и заканчивается сеанс связи.</span><span class="sxs-lookup"><span data-stu-id="2052c-106">A direct WASAPI client can also override the default handling if it knows when the communication session starts and ends.</span></span>

<span data-ttu-id="2052c-107">Чтобы обеспечить пользовательскую реализацию, приложение мультимедиа должно получать уведомления от системы, когда приложение для обмена данными запускается или завершает поток связи.</span><span class="sxs-lookup"><span data-stu-id="2052c-107">To provide a custom implementation, a media application needs to get notifications from the system when a communication application starts or ends a communication stream.</span></span> <span data-ttu-id="2052c-108">Приложение мультимедиа должно реализовать интерфейс [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) и зарегистрировать реализацию в звуковой системе.</span><span class="sxs-lookup"><span data-stu-id="2052c-108">The media application must implement the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) interface and register the implementation with the audio system.</span></span> <span data-ttu-id="2052c-109">После успешной регистрации приложение мультимедиа получает уведомления о событиях в форме обратных вызовов через методы интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2052c-109">Upon successful registration, the media application receives event notifications in the form of callbacks through the methods in the interface.</span></span> <span data-ttu-id="2052c-110">Дополнительные сведения см. в статье [рекомендации по реализации для уведомлений дуккинг](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2052c-110">For more information, see [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span>

<span data-ttu-id="2052c-111">Чтобы отправлять уведомления дуккинг, в звуковой системе должно быть указано, какой сеанс звука прослушивает события дуккинг.</span><span class="sxs-lookup"><span data-stu-id="2052c-111">To send ducking notifications, the audio system must know which audio session is listening for the ducking events.</span></span> <span data-ttu-id="2052c-112">Каждый сеанс звука однозначно идентифицируется с помощью GUID — идентификатора экземпляра сеанса.</span><span class="sxs-lookup"><span data-stu-id="2052c-112">Each audio session is uniquely identified with a GUID—session instance identifier.</span></span> <span data-ttu-id="2052c-113">Диспетчер сеансов позволяет приложению получать сведения о сеансе, такие как название сеанса аудио, состояние отрисовки и идентификатор экземпляра сеанса.</span><span class="sxs-lookup"><span data-stu-id="2052c-113">The session manager allows an application to get information about the session such as title of audio session, the rendering state, and the session instance identifier.</span></span> <span data-ttu-id="2052c-114">Идентификатор можно получить с помощью интерфейса управления политиками [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span><span class="sxs-lookup"><span data-stu-id="2052c-114">The identifier can be retrieved by using the policy control interface, [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).</span></span>

<span data-ttu-id="2052c-115">Ниже приведено краткое описание процесса получения идентификатора экземпляра сеанса приложения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2052c-115">The following steps summarize the process of getting the session instance identifier of the media application:</span></span>

1.  <span data-ttu-id="2052c-116">Создайте экземпляр перечислителя устройства и используйте его для получения ссылки на конечную точку устройства, используемое приложением мультимедиа для отображения потока без связи.</span><span class="sxs-lookup"><span data-stu-id="2052c-116">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="2052c-117">Активируйте диспетчер сеансов из конечной точки устройства и получите ссылку на интерфейс [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) диспетчера сеансов.</span><span class="sxs-lookup"><span data-stu-id="2052c-117">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="2052c-118">С помощью указателя [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) получите ссылку на интерфейс [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) диспетчера сеансов.</span><span class="sxs-lookup"><span data-stu-id="2052c-118">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="2052c-119">Запрос [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) из интерфейса [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="2052c-119">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="2052c-120">Вызовите метод [**IAudioSessionControl2:: жетсессионинстанцеидентифиер**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) и получите строку, содержащую идентификатор сеанса для текущего сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="2052c-120">Call [**IAudioSessionControl2::GetSessionInstanceIdentifier**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) and retrieve a string that contains the session identifier for the current audio session.</span></span>

<span data-ttu-id="2052c-121">Чтобы получать уведомления дуккинг о потоках связи, приложение мультимедиа вызывает [**IAudioSessionManager2:: регистердуккнотификатион**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span><span class="sxs-lookup"><span data-stu-id="2052c-121">To get ducking notifications about communication streams, the media application calls [**IAudioSessionManager2::RegisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification).</span></span> <span data-ttu-id="2052c-122">Приложение мультимедиа предоставляет свой идентификатор экземпляра сеанса звуковой системе и указатель на реализацию [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) .</span><span class="sxs-lookup"><span data-stu-id="2052c-122">The media application supplies its session instance identifier to the audio system and a pointer to the [**IAudioVolumeDuckNotification**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) implementation.</span></span> <span data-ttu-id="2052c-123">Теперь приложение может получить уведомление о событии при открытии потока на коммуникационном устройстве.</span><span class="sxs-lookup"><span data-stu-id="2052c-123">The application can now receive event notification when a stream opened on the communication device.</span></span> <span data-ttu-id="2052c-124">Чтобы отключить получение уведомлений, приложение мультимедиа должно вызвать [**IAudioSessionManager2:: унрегистердуккнотификатион**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span><span class="sxs-lookup"><span data-stu-id="2052c-124">To stop getting notification, the media application must call [**IAudioSessionManager2::UnregisterDuckNotification**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).</span></span>

<span data-ttu-id="2052c-125">В следующем коде показано, как приложение может зарегистрироваться для получения уведомлений дуккинг.</span><span class="sxs-lookup"><span data-stu-id="2052c-125">The following code shows how an application can register to get ducking notifications.</span></span> <span data-ttu-id="2052c-126">Класс Кмедиаплайер определяется в [вопросах реализации уведомлений дуккинг](handling-audio-ducking-events-from-communication-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2052c-126">The CMediaPlayer class is defined in [Implementation Considerations for Ducking Notifications](handling-audio-ducking-events-from-communication-devices.md).</span></span> <span data-ttu-id="2052c-127">В примере [дуккингмедиаплайер](duckingmediaplayer.md) реализована эта функция.</span><span class="sxs-lookup"><span data-stu-id="2052c-127">The [DuckingMediaPlayer](duckingmediaplayer.md) sample implements this functionality.</span></span>


```C++
////////////////////////////////////////////////////////////////////
//Description: Registers for duck notifications depending on the 
//             the ducking options specified by the caller.
//Parameters: 
//    If DuckingOptOutChecked is TRUE, the client is registered for
//    to receive ducking notifications; 
//    FALSE, the client's registration is deleted.
////////////////////////////////////////////////////////////////////

HRESULT CMediaPlayer::DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;

    LPWSTR sessionId = NULL;

    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(
              eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate the session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>
                                 (&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(
                                  NULL, 0, &pSessionControl);
        
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                               IID_PPV_ARGS(&pSessionControl2));
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    // Get the session instance identifier.
    
    if (SUCCEEDED(hr))
    {
        hr = pSessionControl2->GetSessionInstanceIdentifier(
                                 sessionId);
                
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }

    //  Register for ducking events depending on 
    //  the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionManager2->RegisterDuckNotification(
                                    sessionId, this);
        }
        else
        {
            hr = pSessionManager2->UnregisterDuckNotification
                                      (FALSE);
        }
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="2052c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2052c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2052c-129">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="2052c-129">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="2052c-130">Интерфейс Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2052c-130">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="2052c-131">Отключение интерфейса Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2052c-131">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2052c-132">Предоставление пользовательского поведения Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2052c-132">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2052c-133">Рекомендации по реализации для уведомлений Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2052c-133">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



