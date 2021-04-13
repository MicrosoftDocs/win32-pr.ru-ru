---
description: В этом разделе описывается, как управлять громкостью звука при использовании Мфплай для воспроизведения звука и видео.
ms.assetid: 4cf3dd0f-4c8a-4720-9eb3-d23352f3a85e
title: Управление сеансом аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5231ca02603279675fabaaac4b96a1cd001906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342655"
---
# <a name="managing-the-audio-session"></a><span data-ttu-id="8854a-103">Управление сеансом аудио</span><span class="sxs-lookup"><span data-stu-id="8854a-103">Managing the Audio Session</span></span>

<span data-ttu-id="8854a-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8854a-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8854a-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="8854a-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="8854a-106">\]</span><span class="sxs-lookup"><span data-stu-id="8854a-106">\]</span></span>

<span data-ttu-id="8854a-107">В этом разделе описывается, как управлять громкостью звука при использовании Мфплай для воспроизведения звука и видео.</span><span class="sxs-lookup"><span data-stu-id="8854a-107">This topic describes how to control audio volume when using MFPlay for audio/video playback.</span></span>

<span data-ttu-id="8854a-108">Мфплай предоставляет следующие методы управления звуковым томом во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="8854a-108">MFPlay provides the following methods to control the audio volume during playback.</span></span>



| <span data-ttu-id="8854a-109">Метод</span><span class="sxs-lookup"><span data-stu-id="8854a-109">Method</span></span>                                                            | <span data-ttu-id="8854a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8854a-110">Description</span></span>                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="8854a-111">**Имфпмедиаплайер:: Сетбаланце**</span><span class="sxs-lookup"><span data-stu-id="8854a-111">**IMFPMediaPlayer::SetBalance**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | <span data-ttu-id="8854a-112">Устанавливает баланс между левым и правым каналами.</span><span class="sxs-lookup"><span data-stu-id="8854a-112">Sets the balance between the left and right channels.</span></span> |
| [<span data-ttu-id="8854a-113">**Имфпмедиаплайер:: Сетмуте**</span><span class="sxs-lookup"><span data-stu-id="8854a-113">**IMFPMediaPlayer::SetMute**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | <span data-ttu-id="8854a-114">Выключает или выключает звук.</span><span class="sxs-lookup"><span data-stu-id="8854a-114">Mutes or unmutes the audio.</span></span>                           |
| [<span data-ttu-id="8854a-115">**Имфпмедиаплайер:: Сетволуме**</span><span class="sxs-lookup"><span data-stu-id="8854a-115">**IMFPMediaPlayer::SetVolume**</span></span>](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | <span data-ttu-id="8854a-116">Задает уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="8854a-116">Sets the volume level.</span></span>                                |



 

<span data-ttu-id="8854a-117">Чтобы понять поведение этих методов, необходимо знать некоторую терминологию из API сеанса Windows Audio (ВАСАПИ), которая реализует низкоуровневые функции аудио, используемые Мфплай.</span><span class="sxs-lookup"><span data-stu-id="8854a-117">To understand the behavior of these methods, you must know some terminology from the Windows Audio Session API (WASAPI), which implements the low-level audio functionality used by MFPlay.</span></span>

<span data-ttu-id="8854a-118">В ВАСАПИ каждый аудиопоток принадлежит только одному *сеансу аудио*, который представляет собой группу связанных звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="8854a-118">In WASAPI, every audio stream belongs to exactly one *audio session*, which is a group of related audio streams.</span></span> <span data-ttu-id="8854a-119">Как правило, приложение поддерживает один сеанс звука, хотя приложения могут создавать более одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="8854a-119">Typically, an application maintains a single audio session, although applications can create more than one session.</span></span> <span data-ttu-id="8854a-120">Программа системного управления громкостью (Сндвол) отображает регулятор громкости для каждого сеанса звука.</span><span class="sxs-lookup"><span data-stu-id="8854a-120">The system volume-control program (Sndvol) displays a volume control for each audio session.</span></span> <span data-ttu-id="8854a-121">С помощью Сндвол пользователь может настроить громкость звукового сеанса за пределами приложения.</span><span class="sxs-lookup"><span data-stu-id="8854a-121">Through Sndvol, a user can adjust the volume of an audio session from outside of the application.</span></span> <span data-ttu-id="8854a-122">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8854a-122">The following image illustrates this process.</span></span>

![Схема, показывающая звуковые потоки, передающие Управление громкостью на динамики; приложение и сндвол точка управления томами](images/audio-session.gif)

<span data-ttu-id="8854a-124">В Мфплай элемент мультимедиа может иметь один или несколько активных звуковых потоков (обычно только один).</span><span class="sxs-lookup"><span data-stu-id="8854a-124">In MFPlay, a media item can have one or more active audio streams (typically only one).</span></span> <span data-ttu-id="8854a-125">На внутреннем уровне Мфплай использует [потоковый рендеринг звука](streaming-audio-renderer.md) (САР) для отображения звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="8854a-125">Internally, MFPlay uses the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR) to render the audio streams.</span></span> <span data-ttu-id="8854a-126">Если вы не настроите его, то САР присоединяется к сеансу аудио по умолчанию для приложения.</span><span class="sxs-lookup"><span data-stu-id="8854a-126">Unless you configure it otherwise, the SAR joins the application's default audio session.</span></span>

<span data-ttu-id="8854a-127">Методы аудио Мфплай управляют только потоками, принадлежащими текущему элементу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="8854a-127">The MFPlay audio methods control only the streams that belong to the current media item.</span></span> <span data-ttu-id="8854a-128">Они не влияют на том для других потоков, принадлежащих к одному сеансу звука.</span><span class="sxs-lookup"><span data-stu-id="8854a-128">They do not affect the volume for any other streams that belong to the same audio session.</span></span> <span data-ttu-id="8854a-129">С точки зрения ВАСАПИ методы Мфплай управляют уровнями громкости *каждого канала* , а не главным уровнем громкости.</span><span class="sxs-lookup"><span data-stu-id="8854a-129">In terms of WASAPI, the MFPlay methods control the *per-channel* volume levels, not the master volume level.</span></span> <span data-ttu-id="8854a-130">Этот процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="8854a-130">The following image illustrates this process.</span></span>

![схема аналогична предыдущей, но второй поток начинается с элемента мультимедиа, а приложение указывает на второй поток и управление томом.](images/audio-session02.gif)

<span data-ttu-id="8854a-132">Важно понимать некоторые последствия этой функции Мфплай.</span><span class="sxs-lookup"><span data-stu-id="8854a-132">It is important to understand some implications of this feature of MFPlay.</span></span> <span data-ttu-id="8854a-133">Во первых, приложение может настраивать громкость воспроизведения, не затрагивая другие звуковые потоки.</span><span class="sxs-lookup"><span data-stu-id="8854a-133">First, an application can adjust the playback volume without affecting other audio streams.</span></span> <span data-ttu-id="8854a-134">Эту функцию можно использовать, если Мфплай для реализации перекрестного затухания звука, создавая два экземпляра объекта Мфплай и настраивая том отдельно.</span><span class="sxs-lookup"><span data-stu-id="8854a-134">You could use this feature if MFPlay to implement audio cross-fading, by creating two instances of the MFPlay object and adjusting the volume separately.</span></span>

<span data-ttu-id="8854a-135">Если вы используете методы Мфплай для изменения тома или отключения состояния, изменения не отображаются в Сндвол.</span><span class="sxs-lookup"><span data-stu-id="8854a-135">If you use MFPlay methods to change the volume or mute state, the changes do not appear in Sndvol.</span></span> <span data-ttu-id="8854a-136">Например, можно вызвать [**сетмуте**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) , чтобы отключить звук, но сндвол не будет отображать сеанс как отключенный.</span><span class="sxs-lookup"><span data-stu-id="8854a-136">For example, you can call [**SetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) to mute the audio, but Sndvol will not show the session as muted.</span></span> <span data-ttu-id="8854a-137">И наоборот, если Сндвол используется для корректировки объема сеанса, изменения не отражаются в значениях, возвращаемых [**имфпмедиаплайер::**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) или [**имфпмедиаплайер::-приглушением**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span><span class="sxs-lookup"><span data-stu-id="8854a-137">Conversely, if SndVol is used to adjust the session volume, the changes are not reflected in the values returned by [**IMFPMediaPlayer::GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) or [**IMFPMediaPlayer::GetMute**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).</span></span>

<span data-ttu-id="8854a-138">Для каждого экземпляра объекта Player Мфплай эффективный уровень громкости равен *фплайерволуме* × *Фсессионволуме*, где *фплайерволуме* — это значение, возвращаемое методом GetObject [**, а**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) *фсессионволуме* — главный том для сеанса.</span><span class="sxs-lookup"><span data-stu-id="8854a-138">For each instance of the MFPlay player object, the effective volume level equals *fPlayerVolume* × *fSessionVolume*, where *fPlayerVolume* is the value returned by [**GetVolume**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume), and *fSessionVolume* is the master volume for the session.</span></span>

<span data-ttu-id="8854a-139">Для простых сценариев воспроизведения может быть предпочтительнее использовать ВАСАПИ для управления звуковым томом для всего сеанса, а не использовать методы Мфплай.</span><span class="sxs-lookup"><span data-stu-id="8854a-139">For simple playback scenarios, it might be preferable to use the WASAPI to control the audio volume for the entire session, rather than use the MFPlay methods.</span></span>

## <a name="example-code"></a><span data-ttu-id="8854a-140">Пример кода</span><span class="sxs-lookup"><span data-stu-id="8854a-140">Example Code</span></span>

<span data-ttu-id="8854a-141">Ниже приведен класс C++, который обрабатывает основные задачи в ВАСАПИ:</span><span class="sxs-lookup"><span data-stu-id="8854a-141">What follows is a C++ class that handles the basic tasks in WASAPI:</span></span>

-   <span data-ttu-id="8854a-142">Управление томом и выключение его состояния для сеанса.</span><span class="sxs-lookup"><span data-stu-id="8854a-142">Controlling the volume and mute state for the session.</span></span>
-   <span data-ttu-id="8854a-143">Получение уведомлений при каждом изменении тома или выключении его состояния.</span><span class="sxs-lookup"><span data-stu-id="8854a-143">Getting notifications whenever the volume or mute state change.</span></span>

### <a name="class-declaration"></a><span data-ttu-id="8854a-144">Объявление класса</span><span class="sxs-lookup"><span data-stu-id="8854a-144">Class Declaration</span></span>

<span data-ttu-id="8854a-145">`CAudioSessionVolume`Объявление класса реализует интерфейс [**иаудиосессионевентс**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , который является интерфейсом обратного вызова для событий сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="8854a-145">The `CAudioSessionVolume` class declaration implements the [**IAudioSessionEvents**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) interface, which is the callback interface for audio session events.</span></span>


```C++
class CAudioSessionVolume : public IAudioSessionEvents
{
public:
    // Static method to create an instance of the object.
    static HRESULT CreateInstance(
        UINT uNotificationMessage,
        HWND hwndNotification,
        CAudioSessionVolume **ppAudioSessionVolume
    );

    // IUnknown methods.
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IAudioSessionEvents methods.

    STDMETHODIMP OnSimpleVolumeChanged(
        float NewVolume,
        BOOL NewMute,
        LPCGUID EventContext
        );

    // The remaining audio session events do not require any action.
    STDMETHODIMP OnDisplayNameChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnIconPathChanged(LPCWSTR,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnChannelVolumeChanged(DWORD,float[],DWORD,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnGroupingParamChanged(LPCGUID,LPCGUID)
    {
        return S_OK;
    }

    STDMETHODIMP OnStateChanged(AudioSessionState)
    {
        return S_OK;
    }

    STDMETHODIMP OnSessionDisconnected(AudioSessionDisconnectReason)
    {
        return S_OK;
    }

    // Other methods
    HRESULT EnableNotifications(BOOL bEnable);
    HRESULT GetVolume(float *pflVolume);
    HRESULT SetVolume(float flVolume);
    HRESULT GetMute(BOOL *pbMute);
    HRESULT SetMute(BOOL bMute);
    HRESULT SetDisplayName(const WCHAR *wszName);

protected:
    CAudioSessionVolume(UINT uNotificationMessage, HWND hwndNotification);
    ~CAudioSessionVolume();

    HRESULT Initialize();

protected:
    LONG m_cRef;                        // Reference count.
    UINT m_uNotificationMessage;        // Window message to send when an audio event occurs.
    HWND m_hwndNotification;            // Window to receives messages.
    BOOL m_bNotificationsEnabled;       // Are audio notifications enabled?

    IAudioSessionControl    *m_pAudioSession;
    ISimpleAudioVolume      *m_pSimpleAudioVolume;
};
```



<span data-ttu-id="8854a-146">Когда `CAudioSessionVolume` объект получает событие сеанса аудио, он отправляет приложению сообщение частного окна.</span><span class="sxs-lookup"><span data-stu-id="8854a-146">When the `CAudioSessionVolume` object receives an audio session event, it posts a private window message to the application.</span></span> <span data-ttu-id="8854a-147">Обработчик окна и сообщение окна передаются в качестве параметров в статический `CAudioSessionVolume::CreateInstance` метод.</span><span class="sxs-lookup"><span data-stu-id="8854a-147">The window handle and the window message are given as parameters to the static `CAudioSessionVolume::CreateInstance` method.</span></span>

### <a name="getting-the-wasapi-interface-pointers"></a><span data-ttu-id="8854a-148">Получение указателей интерфейса ВАСАПИ</span><span class="sxs-lookup"><span data-stu-id="8854a-148">Getting the WASAPI Interface Pointers</span></span>

<span data-ttu-id="8854a-149">`CAudioSessionVolume` использует два основных интерфейса ВАСАПИ:</span><span class="sxs-lookup"><span data-stu-id="8854a-149">`CAudioSessionVolume` uses two main WASAPI interfaces:</span></span>

-   <span data-ttu-id="8854a-150">[**Иаудиосессионконтрол**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) управляет сеансом аудио.</span><span class="sxs-lookup"><span data-stu-id="8854a-150">[**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) manages the audio session.</span></span>
-   <span data-ttu-id="8854a-151">[**Исимплеаудиоволуме**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) управляет уровнем громкости и отключением состояния сеанса.</span><span class="sxs-lookup"><span data-stu-id="8854a-151">[**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) controls the volume level and mute state of the session.</span></span>

<span data-ttu-id="8854a-152">Чтобы получить эти интерфейсы, необходимо перечислить конечную точку аудио, используемую в САР.</span><span class="sxs-lookup"><span data-stu-id="8854a-152">To get these interfaces, you must enumerate the audio endpoint that is used by the SAR.</span></span> <span data-ttu-id="8854a-153">*Конечная точка аудио* — это устройство, которое фиксирует или потребляет звуковые данные.</span><span class="sxs-lookup"><span data-stu-id="8854a-153">An *audio endpoint* is a hardware device that captures or consumes audio data.</span></span> <span data-ttu-id="8854a-154">Для воспроизведения звука конечная точка — это просто докладчик или другие звуковые выходные данные.</span><span class="sxs-lookup"><span data-stu-id="8854a-154">For audio playback, an endpoint is simply a speaker or other audio output.</span></span> <span data-ttu-id="8854a-155">По умолчанию в САР используется конечная точка по умолчанию для роли устройства **еконсоле** .</span><span class="sxs-lookup"><span data-stu-id="8854a-155">By default, the SAR uses the default endpoint for the **eConsole** device role.</span></span> <span data-ttu-id="8854a-156">*Роль устройства* — это назначенная роль для конечной точки.</span><span class="sxs-lookup"><span data-stu-id="8854a-156">A *device role* is an assigned role for an endpoint.</span></span> <span data-ttu-id="8854a-157">Роли устройств задаются перечислением [**ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , которое описано в статье [Основные API-интерфейсы для аудио](../coreaudio/core-audio-apis-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="8854a-157">Device roles are specified by the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration, which is documented in [Core Audio APIs](../coreaudio/core-audio-apis-in-windows-vista.md).</span></span>

<span data-ttu-id="8854a-158">В следующем коде показано, как перечислить конечную точку и получить интерфейсы ВАСАПИ.</span><span class="sxs-lookup"><span data-stu-id="8854a-158">The following code shows how to enumerate the endpoint and get the WASAPI interfaces.</span></span>


```C++
HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}
```



### <a name="controlling-the-volume"></a><span data-ttu-id="8854a-159">Управление томом</span><span class="sxs-lookup"><span data-stu-id="8854a-159">Controlling the Volume</span></span>

<span data-ttu-id="8854a-160">`CAudioSessionVolume`Методы, управляющие звуковым томом, вызывают эквивалентные методы [**исимплеаудиоволуме**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) .</span><span class="sxs-lookup"><span data-stu-id="8854a-160">The `CAudioSessionVolume` methods that control the audio volume call the equivalent [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) methods.</span></span> <span data-ttu-id="8854a-161">Например, `CAudioSessionVolume::SetVolume` вызывает [**исимплеаудиоволуме:: сетмастерволуме**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="8854a-161">For example, `CAudioSessionVolume::SetVolume` calls [**ISimpleAudioVolume::SetMasterVolume**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), as shown in the following code.</span></span>


```C++
HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}
```



## <a name="complete-caudiosessionvolume-code"></a><span data-ttu-id="8854a-162">Завершение кода Каудиосессионволуме</span><span class="sxs-lookup"><span data-stu-id="8854a-162">Complete CAudioSessionVolume Code</span></span>

<span data-ttu-id="8854a-163">Ниже приведен полный список методов `CAudioSessionVolume` класса.</span><span class="sxs-lookup"><span data-stu-id="8854a-163">Here is the complete listing for the methods of the `CAudioSessionVolume` class.</span></span>


```C++
static const GUID AudioSessionVolumeCtx =
{ 0x2715279f, 0x4139, 0x4ba0, { 0x9c, 0xb1, 0xb3, 0x51, 0xf1, 0xb5, 0x8a, 0x4a } };


CAudioSessionVolume::CAudioSessionVolume(
    UINT uNotificationMessage,
    HWND hwndNotification
    )
    : m_cRef(1),
      m_uNotificationMessage(uNotificationMessage),
      m_hwndNotification(hwndNotification),
      m_bNotificationsEnabled(FALSE),
      m_pAudioSession(NULL),
      m_pSimpleAudioVolume(NULL)
{
}

CAudioSessionVolume::~CAudioSessionVolume()
{
    EnableNotifications(FALSE);

    SafeRelease(&m_pAudioSession);
    SafeRelease(&m_pSimpleAudioVolume);
};


//  Creates an instance of the CAudioSessionVolume object.

/* static */
HRESULT CAudioSessionVolume::CreateInstance(
    UINT uNotificationMessage,
    HWND hwndNotification,
    CAudioSessionVolume **ppAudioSessionVolume
    )
{

    CAudioSessionVolume *pAudioSessionVolume = new (std::nothrow)
        CAudioSessionVolume(uNotificationMessage, hwndNotification);

    if (pAudioSessionVolume == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pAudioSessionVolume->Initialize();
    if (SUCCEEDED(hr))
    {
        *ppAudioSessionVolume = pAudioSessionVolume;
    }
    else
    {
        pAudioSessionVolume->Release();
    }

    return hr;
}


//  Initializes the CAudioSessionVolume object.

HRESULT CAudioSessionVolume::Initialize()
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator *pDeviceEnumerator = NULL;
    IMMDevice *pDevice = NULL;
    IAudioSessionManager *pAudioSessionManager = NULL;

    // Get the enumerator for the audio endpoint devices.
    hr = CoCreateInstance(
        __uuidof(MMDeviceEnumerator),
        NULL,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&pDeviceEnumerator)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the default audio endpoint that the SAR will use.
    hr = pDeviceEnumerator->GetDefaultAudioEndpoint(
        eRender,
        eConsole,   // The SAR uses 'eConsole' by default.
        &pDevice
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the session manager for this device.
    hr = pDevice->Activate(
        __uuidof(IAudioSessionManager),
        CLSCTX_INPROC_SERVER,
        NULL,
        (void**) &pAudioSessionManager
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Get the audio session.
    hr = pAudioSessionManager->GetAudioSessionControl(
        &GUID_NULL,     // Get the default audio session.
        FALSE,          // The session is not cross-process.
        &m_pAudioSession
        );


    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioSessionManager->GetSimpleAudioVolume(
        &GUID_NULL, 0, &m_pSimpleAudioVolume
        );

done:
    SafeRelease(&pDeviceEnumerator);
    SafeRelease(&pDevice);
    SafeRelease(&pAudioSessionManager);
    return hr;
}

STDMETHODIMP CAudioSessionVolume::QueryInterface(REFIID riid, void **ppv)
{
    static const QITAB qit[] =
    {
        QITABENT(CAudioSessionVolume, IAudioSessionEvents),
        { 0 },
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CAudioSessionVolume::Release()
{
    LONG cRef = InterlockedDecrement( &m_cRef );
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}


// Enables or disables notifications from the audio session. For example, the
// application is notified if the user mutes the audio through the system
// volume-control program (Sndvol).

HRESULT CAudioSessionVolume::EnableNotifications(BOOL bEnable)
{
    HRESULT hr = S_OK;

    if (m_hwndNotification == NULL || m_pAudioSession == NULL)
    {
        return E_FAIL;
    }

    if (m_bNotificationsEnabled == bEnable)
    {
        // No change.
        return S_OK;
    }

    if (bEnable)
    {
        hr = m_pAudioSession->RegisterAudioSessionNotification(this);
    }
    else
    {
        hr = m_pAudioSession->UnregisterAudioSessionNotification(this);
    }

    if (SUCCEEDED(hr))
    {
        m_bNotificationsEnabled = bEnable;
    }

    return hr;
}


// Gets the session volume level.

HRESULT CAudioSessionVolume::GetVolume(float *pflVolume)
{
    if ( m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMasterVolume(pflVolume);
    }
}

//  Sets the session volume level.
//
//  flVolume: Ranges from 0 (silent) to 1 (full volume)

HRESULT CAudioSessionVolume::SetVolume(float flVolume)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMasterVolume(
            flVolume,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}


//  Gets the muting state of the session.

HRESULT CAudioSessionVolume::GetMute(BOOL *pbMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->GetMute(pbMute);
    }
}

//  Mutes or unmutes the session audio.

HRESULT CAudioSessionVolume::SetMute(BOOL bMute)
{
    if (m_pSimpleAudioVolume == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pSimpleAudioVolume->SetMute(
            bMute,
            &AudioSessionVolumeCtx  // Event context.
            );
    }
}

//  Sets the display name for the session audio.

HRESULT CAudioSessionVolume::SetDisplayName(const WCHAR *wszName)
{
    if (m_pAudioSession == NULL)
    {
        return E_FAIL;
    }
    else
    {
        return m_pAudioSession->SetDisplayName(wszName, NULL);
    }
}


//  Called when the session volume level or muting state changes.
//  (Implements IAudioSessionEvents::OnSimpleVolumeChanged.)

HRESULT CAudioSessionVolume::OnSimpleVolumeChanged(
    float NewVolume,
    BOOL NewMute,
    LPCGUID EventContext
    )
{
    // Check if we should post a message to the application.

    if ( m_bNotificationsEnabled &&
        (*EventContext != AudioSessionVolumeCtx) &&
        (m_hwndNotification != NULL)
        )
    {
        // Notifications are enabled, AND
        // We did not trigger the event ourselves, AND
        // We have a valid window handle.

        // Post the message.
        ::PostMessage(
            m_hwndNotification,
            m_uNotificationMessage,
            *((WPARAM*)(&NewVolume)),  // Coerce the float.
            (LPARAM)NewMute
            );
    }
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="8854a-164">Требования</span><span class="sxs-lookup"><span data-stu-id="8854a-164">Requirements</span></span>

<span data-ttu-id="8854a-165">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8854a-165">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8854a-166">См. также</span><span class="sxs-lookup"><span data-stu-id="8854a-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8854a-167">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="8854a-167">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
