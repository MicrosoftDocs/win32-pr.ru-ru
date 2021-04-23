---
description: События сеанса звука
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: События сеанса звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90ec5de18c883f817c2f650ccfc48ad0149ac84e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990577"
---
# <a name="audio-session-events"></a><span data-ttu-id="cdbb7-103">События сеанса звука</span><span class="sxs-lookup"><span data-stu-id="cdbb7-103">Audio Session Events</span></span>

<span data-ttu-id="cdbb7-104">Приложение, которое управляет звуковыми потоками в общем режиме, может регистрироваться для получения уведомлений при возникновении событий сеанса.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-104">An application that manages shared-mode audio streams can register to receive notifications when session events occur.</span></span> <span data-ttu-id="cdbb7-105">Как упоминалось ранее, каждый поток принадлежит к [сеансу аудио](audio-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="cdbb7-105">As explained previously, each stream belongs to an [audio session](audio-sessions.md).</span></span> <span data-ttu-id="cdbb7-106">Событие сеанса инициируется изменением состояния сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-106">A session event is initiated by a change in the status of an audio session.</span></span>

<span data-ttu-id="cdbb7-107">Клиентское приложение может зарегистрироваться для получения уведомлений о следующих типах событий сеанса:</span><span class="sxs-lookup"><span data-stu-id="cdbb7-107">A client application can register to receive notifications of the following types of session events:</span></span>

-   <span data-ttu-id="cdbb7-108">Основной уровень громкости или состояние отключения сеанса субмикс изменилось.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-108">The master volume level or muting state of the session submix has changed.</span></span>
-   <span data-ttu-id="cdbb7-109">Изменился уровень громкости одного или нескольких каналов субмикс сеанса.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-109">The volume level of one or more channels of the session submix has changed.</span></span>
-   <span data-ttu-id="cdbb7-110">Сеанс отключен.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-110">The session has been disconnected.</span></span>
-   <span data-ttu-id="cdbb7-111">Состояние действия сеанса изменилось на активное, неактивное или с истекшим сроком действия.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-111">The activity state of the session has changed to active, inactive, or expired.</span></span>
-   <span data-ttu-id="cdbb7-112">Сеансу был назначен новый параметр группирования.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-112">The session has been assigned a new grouping parameter.</span></span>
-   <span data-ttu-id="cdbb7-113">Изменено свойство пользовательского интерфейса сеанса (значок или отображаемое имя).</span><span class="sxs-lookup"><span data-stu-id="cdbb7-113">A user-interface property of the session (icon or display name) has changed.</span></span>

<span data-ttu-id="cdbb7-114">Клиент получает уведомления об этих событиях через методы в своей реализации интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="cdbb7-114">The client receives notifications of these events through the methods in its implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cdbb7-115">В отличие от других интерфейсов в ВАСАПИ, которые реализуются системным модулем ВАСАПИ, клиент реализует **иаудиосессионевентс**.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-115">Unlike the other interfaces in WASAPI, which are implemented by the WASAPI system module, the client implements **IAudioSessionEvents**.</span></span> <span data-ttu-id="cdbb7-116">Методы этого интерфейса получают обратные вызовы из системного модуля ВАСАПИ при возникновении событий сеанса.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-116">The methods in this interface receive callbacks from the WASAPI system module when session events occur.</span></span>

<span data-ttu-id="cdbb7-117">Чтобы начать получать уведомления, клиент вызывает метод [**иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) для регистрации своего интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="cdbb7-117">To begin receiving notifications, the client calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register its [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cdbb7-118">Если клиенту больше не требуются уведомления, он вызывает метод [**иаудиосессионконтрол:: унрегистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) для удаления регистрации.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-118">When the client no longer requires notifications, it calls the [**IAudioSessionControl::UnregisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) method to delete the registration.</span></span>

<span data-ttu-id="cdbb7-119">В следующем примере кода показана возможная реализация интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :</span><span class="sxs-lookup"><span data-stu-id="cdbb7-119">The following code example shows a possible implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface:</span></span>


```C++
//-----------------------------------------------------------
// Client implementation of IAudioSessionEvents interface.
// WASAPI calls these methods to notify the application when
// a parameter or property of the audio session changes.
//-----------------------------------------------------------
class CAudioSessionEvents : public IAudioSessionEvents
{
    LONG _cRef;

public:
    CAudioSessionEvents() :
        _cRef(1)
    {
    }

    ~CAudioSessionEvents()
    {
    }

    // IUnknown methods -- AddRef, Release, and QueryInterface

    ULONG STDMETHODCALLTYPE AddRef()
    {
        return InterlockedIncrement(&_cRef);
    }

    ULONG STDMETHODCALLTYPE Release()
    {
        ULONG ulRef = InterlockedDecrement(&_cRef);
        if (0 == ulRef)
        {
            delete this;
        }
        return ulRef;
    }

    HRESULT STDMETHODCALLTYPE QueryInterface(
                                REFIID  riid,
                                VOID  **ppvInterface)
    {
        if (IID_IUnknown == riid)
        {
            AddRef();
            *ppvInterface = (IUnknown*)this;
        }
        else if (__uuidof(IAudioSessionEvents) == riid)
        {
            AddRef();
            *ppvInterface = (IAudioSessionEvents*)this;
        }
        else
        {
            *ppvInterface = NULL;
            return E_NOINTERFACE;
        }
        return S_OK;
    }

    // Notification methods for audio session events

    HRESULT STDMETHODCALLTYPE OnDisplayNameChanged(
                                LPCWSTR NewDisplayName,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnIconPathChanged(
                                LPCWSTR NewIconPath,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSimpleVolumeChanged(
                                float NewVolume,
                                BOOL NewMute,
                                LPCGUID EventContext)
    {
        if (NewMute)
        {
            printf("MUTE\n");
        }
        else
        {
            printf("Volume = %d percent\n",
                   (UINT32)(100*NewVolume + 0.5));
        }

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnChannelVolumeChanged(
                                DWORD ChannelCount,
                                float NewChannelVolumeArray[],
                                DWORD ChangedChannel,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnGroupingParamChanged(
                                LPCGUID NewGroupingParam,
                                LPCGUID EventContext)
    {
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnStateChanged(
                                AudioSessionState NewState)
    {
        char *pszState = "?????";

        switch (NewState)
        {
        case AudioSessionStateActive:
            pszState = "active";
            break;
        case AudioSessionStateInactive:
            pszState = "inactive";
            break;
        }
        printf("New session state = %s\n", pszState);

        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE OnSessionDisconnected(
              AudioSessionDisconnectReason DisconnectReason)
    {
        char *pszReason = "?????";

        switch (DisconnectReason)
        {
        case DisconnectReasonDeviceRemoval:
            pszReason = "device removed";
            break;
        case DisconnectReasonServerShutdown:
            pszReason = "server shut down";
            break;
        case DisconnectReasonFormatChanged:
            pszReason = "format changed";
            break;
        case DisconnectReasonSessionLogoff:
            pszReason = "user logged off";
            break;
        case DisconnectReasonSessionDisconnected:
            pszReason = "session disconnected";
            break;
        case DisconnectReasonExclusiveModeOverride:
            pszReason = "exclusive-mode override";
            break;
        }
        printf("Audio session disconnected (reason: %s)\n",
               pszReason);

        return S_OK;
    }
};
```



<span data-ttu-id="cdbb7-120">Класс Каудиосессионевентс в предыдущем примере кода является реализацией интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) .</span><span class="sxs-lookup"><span data-stu-id="cdbb7-120">The CAudioSessionEvents class in the preceding code example is an implementation of the [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface.</span></span> <span data-ttu-id="cdbb7-121">Эта конкретная реализация может быть частью консольного приложения, которое выводит сведения о событиях сеанса в окно командной строки.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-121">This particular implementation might be part of a console application that prints information about session events to a Command Prompt window.</span></span> <span data-ttu-id="cdbb7-122">Поскольку **иаудиосессионевентс** наследует от [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), определение класса содержит реализации методов **IUnknown** , [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span><span class="sxs-lookup"><span data-stu-id="cdbb7-122">Because **IAudioSessionEvents** inherits from [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), the class definition contains implementations of the **IUnknown** methods [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release), and [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span> <span data-ttu-id="cdbb7-123">Остальные открытые методы в определении класса относятся к интерфейсу **иаудиосессионевентс** .</span><span class="sxs-lookup"><span data-stu-id="cdbb7-123">The remaining public methods in the class definition are specific to the **IAudioSessionEvents** interface.</span></span>

<span data-ttu-id="cdbb7-124">Некоторые клиенты могут не заинтересовать наблюдение за всеми типами событий сеанса.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-124">Some clients might not be interested in monitoring all types of session events.</span></span> <span data-ttu-id="cdbb7-125">В предыдущем примере кода несколько методов уведомления в классе Каудиосессионевентс ничего не делают.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-125">In the preceding code example, several notification methods in the CAudioSessionEvents class do nothing.</span></span> <span data-ttu-id="cdbb7-126">Например, метод [**ончаннелволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) не выполняет никаких действий, кроме возврата кода состояния S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-126">For example, the [**OnChannelVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) method does nothing except to return status code S\_OK.</span></span> <span data-ttu-id="cdbb7-127">Это приложение не отслеживает тома каналов, так как не изменяет тома канала (путем вызова методов в интерфейсе [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) и не использует сеанс совместно с другими приложениями, которые могут изменять тома каналов.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-127">This application does not monitor channel volumes because it does not change the channel volumes (by calling the methods in the [**IChannelAudioVolume**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) interface), and it does not share the session with other applications that might change the channel volumes.</span></span>

<span data-ttu-id="cdbb7-128">Единственными тремя методами в классе Каудиосессионевентс, которые уведомляют пользователя о событиях сеанса, являются [**онсимплеволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**онстатечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)и [**онсессиондисконнектед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span><span class="sxs-lookup"><span data-stu-id="cdbb7-128">The only three methods in the CAudioSessionEvents class that notify the user of session events are [**OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**OnStateChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged), and [**OnSessionDisconnected**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected).</span></span> <span data-ttu-id="cdbb7-129">Например, если пользователь запускает программу системного управления громкостью, Сндвол и использует элемент управления громкостью в Сндвол для изменения уровня громкости приложения, `OnSimpleVolumeChanged` немедленно выводит новый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="cdbb7-129">For example, if the user runs the system volume-control program, Sndvol, and uses the volume control in Sndvol to change the application's volume level, `OnSimpleVolumeChanged` immediately prints the new volume level.</span></span>

<span data-ttu-id="cdbb7-130">Пример кода, который регистрирует и отменяет регистрацию интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) клиента, см. в разделе [события аудио для устаревших аудио приложений](audio-events-for-legacy-audio-applications.md).</span><span class="sxs-lookup"><span data-stu-id="cdbb7-130">For a code example that registers and unregisters a client's [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, see [Audio Events for Legacy Audio Applications](audio-events-for-legacy-audio-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdbb7-131">См. также</span><span class="sxs-lookup"><span data-stu-id="cdbb7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdbb7-132">Сеансы аудио</span><span class="sxs-lookup"><span data-stu-id="cdbb7-132">Audio Sessions</span></span>](audio-sessions.md)
</dt> </dl>

 

 
