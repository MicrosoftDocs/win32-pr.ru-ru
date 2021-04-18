---
description: События аудио для устаревших звуковых приложений
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: События аудио для устаревших звуковых приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fe99195910b1c1c68c0f3a1b39dd2706dde0be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142790"
---
# <a name="audio-events-for-legacy-audio-applications"></a><span data-ttu-id="6c655-103">События аудио для устаревших звуковых приложений</span><span class="sxs-lookup"><span data-stu-id="6c655-103">Audio Events for Legacy Audio Applications</span></span>

<span data-ttu-id="6c655-104">Устаревшие API аудио, такие как DirectSound, DirectShow и функции **вавеауткскскс** , позволяют приложениям получать и задавать уровни громкости звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="6c655-104">Legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions enable applications to get and set the volume levels of audio streams.</span></span> <span data-ttu-id="6c655-105">Приложения могут использовать возможности управления томами в этих API для показа ползунков громкости в окнах приложений.</span><span class="sxs-lookup"><span data-stu-id="6c655-105">Applications can use the volume-control capabilities in these APIs to display volume sliders in their application windows.</span></span>

<span data-ttu-id="6c655-106">В Windows Vista программа системного управления громкостью, Сндвол, позволяет пользователям управлять уровнями громкости звука для отдельных приложений.</span><span class="sxs-lookup"><span data-stu-id="6c655-106">In Windows Vista, the system volume-control program, Sndvol, allows users to control the audio volume levels for individual applications.</span></span> <span data-ttu-id="6c655-107">Ползунки громкости, отображаемые приложениями, должны быть связаны с соответствующими ползунками громкости в Сндвол.</span><span class="sxs-lookup"><span data-stu-id="6c655-107">The volume sliders that are displayed by applications should be linked to the corresponding volume sliders in Sndvol.</span></span> <span data-ttu-id="6c655-108">Если пользователь настраивает том приложения с помощью ползунка громкости в окне приложения, соответствующий ползунок в Сндвол немедленно перемещается, чтобы показать новый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="6c655-108">If a user adjusts the application volume through a volume slider in an application window, then the corresponding volume slider in Sndvol immediately moves to indicate the new volume level.</span></span> <span data-ttu-id="6c655-109">И наоборот, если пользователь настраивает том приложения через Сндвол, ползунки громкости в окне приложения должны перемещаться, чтобы показать новый уровень громкости.</span><span class="sxs-lookup"><span data-stu-id="6c655-109">Conversely, if the user adjusts the application volume through Sndvol, then the volume sliders in the application window should move to indicate the new volume level.</span></span>

<span data-ttu-id="6c655-110">В Windows Vista Сндвол немедленно отражает изменения томов, с помощью которых приложение выполняет вызовы метода **идиректсаундбуффер:: сетволуме** или функции **вавеаутсетволуме** .</span><span class="sxs-lookup"><span data-stu-id="6c655-110">In Windows Vista, Sndvol immediately reflects volume changes that an application makes through calls to the **IDirectSoundBuffer::SetVolume** method or **waveOutSetVolume** function.</span></span> <span data-ttu-id="6c655-111">Однако устаревший аудио API, например DirectSound или функции **вавеауткскскс** , не предоставляет средств уведомления о приложении, когда пользователь изменяет том приложения через сндвол.</span><span class="sxs-lookup"><span data-stu-id="6c655-111">However, a legacy audio API such as DirectSound or the **waveOutXxx** functions provides no means to notify an application when the user changes the application volume through Sndvol.</span></span> <span data-ttu-id="6c655-112">Если приложение отображает ползунок громкости, но не получает уведомлений об изменениях тома, то ползунок не будет отражать изменения, внесенные пользователем в Сндвол.</span><span class="sxs-lookup"><span data-stu-id="6c655-112">If an application displays a volume slider but does not receive notifications of volume changes, then the slider will fail to reflect changes made by the user in Sndvol.</span></span> <span data-ttu-id="6c655-113">Чтобы реализовать соответствующее поведение, конструктор приложений должен каким-либо образом компенсировать отсутствие уведомлений от устаревших API аудио.</span><span class="sxs-lookup"><span data-stu-id="6c655-113">To implement the appropriate behavior, the application designer must somehow compensate for the lack of notifications by the legacy audio API.</span></span>

<span data-ttu-id="6c655-114">Одно из решений может быть для того, чтобы приложение установило таймер для периодического напоминания об изменении уровня громкости, чтобы проверить, изменился ли он.</span><span class="sxs-lookup"><span data-stu-id="6c655-114">One solution might be for the application to set a timer to periodically remind it to check the volume level to see if it has changed.</span></span>

<span data-ttu-id="6c655-115">Более элегантное решение заключается в том, чтобы приложение использовало возможности уведомления о событиях основных API-интерфейсов аудио.</span><span class="sxs-lookup"><span data-stu-id="6c655-115">A more elegant solution is for the application to use the event notification capabilities of the core audio APIs.</span></span> <span data-ttu-id="6c655-116">В частности, приложение может зарегистрировать интерфейс [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) для получения обратных вызовов при изменении громкости или других типах звуковых событий.</span><span class="sxs-lookup"><span data-stu-id="6c655-116">In particular, the application can register an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface to receive callbacks when volume changes or other types of audio events occur.</span></span> <span data-ttu-id="6c655-117">При изменении тома подпрограммы обратного вызова изменения тома могут немедленно обновить ползунок тома приложения, чтобы отразить изменение.</span><span class="sxs-lookup"><span data-stu-id="6c655-117">When the volume changes, the volume-change callback routine can immediately update the application's volume slider to reflect the change.</span></span>

<span data-ttu-id="6c655-118">В следующем примере кода показано, как приложение может зарегистрироваться для получения уведомлений об изменениях тома и других звуковых событиях.</span><span class="sxs-lookup"><span data-stu-id="6c655-118">The following code example shows how an application can register to receive notifications of volume changes and other audio events:</span></span>


```C++
//-----------------------------------------------------------
// Register the application to receive notifications when the
// volume level changes on the default process-specific audio
// session (with session GUID value GUID_NULL) on the audio
// endpoint device with the specified data-flow direction
// (eRender or eCapture) and device role.
//-----------------------------------------------------------
#define EXIT_ON_ERROR(hr)  \
              if (FAILED(hr)) { goto Exit; }
#define SAFE_RELEASE(punk)  \
              if ((punk) != NULL)  \
                { (punk)->Release(); (punk) = NULL; }

class AudioVolumeEvents
{
    HRESULT _hrStatus;
    IAudioSessionManager *_pManager;
    IAudioSessionControl *_pControl;
    IAudioSessionEvents *_pAudioEvents;
public:
    AudioVolumeEvents(EDataFlow, ERole, IAudioSessionEvents*);
    ~AudioVolumeEvents();
    HRESULT GetStatus() { return _hrStatus; };
};

// Constructor
AudioVolumeEvents::AudioVolumeEvents(EDataFlow flow, ERole role,
                                     IAudioSessionEvents *pAudioEvents)
{
    IMMDeviceEnumerator *pEnumerator = NULL;
    IMMDevice *pDevice = NULL;

    _hrStatus = S_OK;
    _pManager = NULL;
    _pControl = NULL;
    _pAudioEvents = pAudioEvents;

    if (_pAudioEvents == NULL)
    {
        _hrStatus = E_POINTER;
        return;
    }

    _pAudioEvents->AddRef();

    // Get the enumerator for the audio endpoint devices
    // on this system.
    _hrStatus = CoCreateInstance(__uuidof(MMDeviceEnumerator),
                                 NULL, CLSCTX_INPROC_SERVER,
                                 __uuidof(IMMDeviceEnumerator),
                                 (void**)&pEnumerator);
    EXIT_ON_ERROR(_hrStatus)

    // Get the audio endpoint device with the specified data-flow
    // direction (eRender or eCapture) and device role.
    _hrStatus = pEnumerator->GetDefaultAudioEndpoint(flow, role,
                                                     &pDevice);
    EXIT_ON_ERROR(_hrStatus)

    // Get the session manager for the endpoint device.
    _hrStatus = pDevice->Activate(__uuidof(IAudioSessionManager),
                                  CLSCTX_INPROC_SERVER, NULL,
                                  (void**)&_pManager);
    EXIT_ON_ERROR(_hrStatus)

    // Get the control interface for the process-specific audio
    // session with session GUID = GUID_NULL. This is the session
    // that an audio stream for a DirectSound, DirectShow, waveOut,
    // or PlaySound application stream belongs to by default.
    _hrStatus = _pManager->GetAudioSessionControl(NULL, 0, &_pControl);
    EXIT_ON_ERROR(_hrStatus)

    _hrStatus = _pControl->RegisterAudioSessionNotification(_pAudioEvents);
    EXIT_ON_ERROR(_hrStatus)

Exit:
    SAFE_RELEASE(pEnumerator)
    SAFE_RELEASE(pDevice)
}

// Destructor
AudioVolumeEvents::~AudioVolumeEvents()
{
    if (_pControl != NULL)
    {
        _pControl->UnregisterAudioSessionNotification(_pAudioEvents);
    }
    SAFE_RELEASE(_pManager)
    SAFE_RELEASE(_pControl)
    SAFE_RELEASE(_pAudioEvents)
};
```



<span data-ttu-id="6c655-119">В предыдущем примере кода реализуется класс с именем Аудиоволумивентс.</span><span class="sxs-lookup"><span data-stu-id="6c655-119">The preceding code example implements a class named AudioVolumeEvents.</span></span> <span data-ttu-id="6c655-120">Во время инициализации программы звуковое приложение включает уведомления о событиях аудио, создавая объект Аудиоволумивентс.</span><span class="sxs-lookup"><span data-stu-id="6c655-120">During program initialization, the audio application enables audio-event notifications by creating an AudioVolumeEvents object.</span></span> <span data-ttu-id="6c655-121">Конструктор для этого класса принимает три входных параметра:</span><span class="sxs-lookup"><span data-stu-id="6c655-121">The constructor for this class takes three input parameters:</span></span>

-   <span data-ttu-id="6c655-122">*Flow*— направление потока данных [устройства конечной точки аудио](audio-endpoint-devices.md) (значение перечисления [**едатафлов**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).</span><span class="sxs-lookup"><span data-stu-id="6c655-122">*flow*—the data-flow direction of the [audio endpoint device](audio-endpoint-devices.md) (an [**EDataFlow**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) enumeration value).</span></span>
-   <span data-ttu-id="6c655-123">*роль*— текущая [роль устройства](device-roles.md) конечной точки (значение перечисления [**ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).</span><span class="sxs-lookup"><span data-stu-id="6c655-123">*role*—the current [device role](device-roles.md) of the endpoint device (an [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration value).</span></span>
-   <span data-ttu-id="6c655-124">*паудиоевентс*— указатель на объект (экземпляр интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ), который содержит набор подпрограмм обратного вызова, реализованных приложением.</span><span class="sxs-lookup"><span data-stu-id="6c655-124">*pAudioEvents*—pointer to an object (an [**IAudioSessionEvents**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) interface instance) that contains a set of callback routines that are implemented by the application.</span></span>

<span data-ttu-id="6c655-125">Конструктор предоставляет значения потока и роли в качестве входных параметров для метода [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) .</span><span class="sxs-lookup"><span data-stu-id="6c655-125">The constructor supplies the flow and role values as input parameters to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method.</span></span> <span data-ttu-id="6c655-126">Метод создает объект [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , инкапсулирующий устройство конечных точек звука с указанным направлением потока данных и ролью устройства.</span><span class="sxs-lookup"><span data-stu-id="6c655-126">The method creates an [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) object that encapsulates the audio endpoint device with the specified data-flow direction and device role.</span></span>

<span data-ttu-id="6c655-127">Приложение реализует объект, на который указывает *паудиоевентс*.</span><span class="sxs-lookup"><span data-stu-id="6c655-127">The application implements the object pointed to by *pAudioEvents*.</span></span> <span data-ttu-id="6c655-128">(Реализация не показана в предыдущем примере кода.</span><span class="sxs-lookup"><span data-stu-id="6c655-128">(The implementation is not shown in the preceding code example.</span></span> <span data-ttu-id="6c655-129">Пример кода, в котором реализуется интерфейс **иаудиосессионевентс** , см. в разделе [события сеанса звука](audio-session-events.md).) Каждый метод в этом интерфейсе получает уведомления о звуковом событии определенного типа.</span><span class="sxs-lookup"><span data-stu-id="6c655-129">For a code example that implements an **IAudioSessionEvents** interface, see [Audio Session Events](audio-session-events.md).) Each method in this interface receives notifications of a particular type of audio event.</span></span> <span data-ttu-id="6c655-130">Если приложение не заинтересовано в определенном типе событий, метод для этого типа события не должен выполнять никаких действий, но возвращать значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="6c655-130">If the application is not interested in a particular event type, then the method for that event type should do nothing but return S\_OK.</span></span>

<span data-ttu-id="6c655-131">Метод [**иаудиосессионевентс:: онсимплеволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) получает уведомления об изменениях тома.</span><span class="sxs-lookup"><span data-stu-id="6c655-131">The [**IAudioSessionEvents::OnSimpleVolumeChanged**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) method receives notifications of volume changes.</span></span> <span data-ttu-id="6c655-132">Как правило, этот метод обновляет ползунок громкости приложения.</span><span class="sxs-lookup"><span data-stu-id="6c655-132">Typically, this method updates the application's volume slider.</span></span>

<span data-ttu-id="6c655-133">В приведенном выше примере кода конструктор для класса Аудиоволумивентс регистрируется для уведомлений в [звуковом сеансе](audio-sessions.md) конкретного процесса, который определяется идентификатором GUID сеанса \_ null.</span><span class="sxs-lookup"><span data-stu-id="6c655-133">In the preceding code example, the constructor for the AudioVolumeEvents class registers for notifications on the process-specific [audio session](audio-sessions.md) that is identified by session GUID value GUID\_NULL.</span></span> <span data-ttu-id="6c655-134">По умолчанию устаревшие API аудио, такие как DirectSound, DirectShow и функции **вавеауткскскс** , назначают свои потоки этому сеансу.</span><span class="sxs-lookup"><span data-stu-id="6c655-134">By default, legacy audio APIs such as DirectSound, DirectShow, and the **waveOutXxx** functions assign their streams to this session.</span></span> <span data-ttu-id="6c655-135">Однако приложение DirectSound или DirectShow может, как вариант, переопределять поведение по умолчанию и назначать его потоки межпроцессному сеансу или сеансу, который определяется значением GUID, отличным от GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="6c655-135">However, a DirectSound or DirectShow application can, as an option, override the default behavior and assign its streams to a cross-process session or to a session that is identified by a GUID value other than GUID\_NULL.</span></span> <span data-ttu-id="6c655-136">(В настоящее время механизм для приложения **вавеауткскскс** не предназначен для переопределения поведения по умолчанию аналогичным образом.) Пример кода приложения DirectShow с таким поведением см. в разделе [роли устройств для приложений DirectShow](device-roles-for-directshow-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6c655-136">(No mechanism is currently provided for a **waveOutXxx** application to override the default behavior in a similar manner.) For a code example of a DirectShow application with this behavior, see [Device Roles for DirectShow Applications](device-roles-for-directshow-applications.md).</span></span> <span data-ttu-id="6c655-137">Для размещения такого приложения можно изменить конструктор в предыдущем примере кода, чтобы принять два дополнительных входных параметра — GUID сеанса и флаг, указывающий, является ли отслеживаемый сеанс межпроцессным или конкретным процессом.</span><span class="sxs-lookup"><span data-stu-id="6c655-137">To accommodate such an application, you can modify the constructor in the preceding code example to accept two additional input parameters—a session GUID and a flag to indicate whether the session that is to be monitored is a cross-process or process-specific session.</span></span> <span data-ttu-id="6c655-138">Передайте эти параметры в вызов метода [**иаудиосессионманажер:: жетаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) в конструкторе.</span><span class="sxs-lookup"><span data-stu-id="6c655-138">Pass these parameters to the call to the [**IAudioSessionManager::GetAudioSessionControl**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) method in the constructor.</span></span>

<span data-ttu-id="6c655-139">После того как конструктор вызывает метод [**иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) для регистрации уведомлений, приложение продолжит получать уведомления только при условии, что существует либо интерфейс [**Иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) , либо [**иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) .</span><span class="sxs-lookup"><span data-stu-id="6c655-139">After the constructor calls the [**IAudioSessionControl::RegisterAudioSessionNotification**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) method to register for notifications, the application continues to receive notifications for only as long as either the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) or [**IAudioSessionManager**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) interface exists.</span></span> <span data-ttu-id="6c655-140">Объект Аудиоволумивентс в предыдущем примере кода содержит ссылки на эти интерфейсы, пока не будет вызван его деструктор.</span><span class="sxs-lookup"><span data-stu-id="6c655-140">The AudioVolumeEvents object in the preceding code example holds references to these interfaces until its destructor is called.</span></span> <span data-ttu-id="6c655-141">Такое поведение гарантирует, что приложение продолжит получать уведомления в течение времени существования объекта Аудиоволумивентс.</span><span class="sxs-lookup"><span data-stu-id="6c655-141">This behavior ensures that the application will continue to receive notifications for the lifetime of the AudioVolumeEvents object.</span></span>

<span data-ttu-id="6c655-142">Вместо неявного выбора звукового устройства на основе его роли устройства Устройство DirectSound или устаревшее приложение Windows мультимедиа может позволить пользователю явно выбрать устройство из списка доступных устройств, идентифицируемых их понятными именами.</span><span class="sxs-lookup"><span data-stu-id="6c655-142">Instead of implicitly selecting an audio device based on its device role, a DirectSound or legacy Windows multimedia application might allow the user to explicitly select a device from a list of available devices that are identified by their friendly names.</span></span> <span data-ttu-id="6c655-143">Для поддержки такого поведения необходимо изменить предыдущий пример кода, чтобы создать уведомления о звуковых событиях для выбранного устройства.</span><span class="sxs-lookup"><span data-stu-id="6c655-143">To support this behavior, the preceding code example must be modified to generate audio-event notifications for the selected device.</span></span> <span data-ttu-id="6c655-144">Требуются два изменения.</span><span class="sxs-lookup"><span data-stu-id="6c655-144">Two modifications are required.</span></span> <span data-ttu-id="6c655-145">Сначала измените определение конструктора, чтобы принять [строку идентификатора конечной точки](endpoint-id-strings.md) в качестве входного параметра (вместо параметров Flow и Role в примере кода).</span><span class="sxs-lookup"><span data-stu-id="6c655-145">First, change the constructor definition to accept an [endpoint ID string](endpoint-id-strings.md) as an input parameter (in place of the flow and role parameters in the code example).</span></span> <span data-ttu-id="6c655-146">Эта строка определяет устройство аудио конечной точки, соответствующее выбранному устройству аудио или устаревшей версии DirectSound.</span><span class="sxs-lookup"><span data-stu-id="6c655-146">This string identifies the audio endpoint device that corresponds to the selected DirectSound or legacy waveform device.</span></span> <span data-ttu-id="6c655-147">Во-вторых, замените вызов метода [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) вызовом метода [**иммдевицеенумератор::-Device**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) .</span><span class="sxs-lookup"><span data-stu-id="6c655-147">Second, replace the call to the [**IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) method with a call to the [**IMMDeviceEnumerator::GetDevice**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) method.</span></span> <span data-ttu-id="6c655-148">Вызов **метода** GetString принимает строку идентификатора конечной точки в качестве входного параметра и создает экземпляр устройства конечной точки, определяемый строкой.</span><span class="sxs-lookup"><span data-stu-id="6c655-148">The **GetDevice** call takes the endpoint ID string as an input parameter and creates an instance of the endpoint device that is identified by the string.</span></span>

<span data-ttu-id="6c655-149">Ниже приведена методика получения строки идентификатора конечной точки для устройства DirectSound или устаревшей версии аудио.</span><span class="sxs-lookup"><span data-stu-id="6c655-149">The technique for obtaining the endpoint ID string for a DirectSound device or legacy waveform device is as follows.</span></span>

<span data-ttu-id="6c655-150">Во первых, во время перечисления устройств DirectSound предоставляет строку идентификатора конечной точки для каждого перечислимого устройства.</span><span class="sxs-lookup"><span data-stu-id="6c655-150">First, during device enumeration, DirectSound supplies the endpoint ID string for each enumerated device.</span></span> <span data-ttu-id="6c655-151">Чтобы начать перечисление устройств, приложение передает указатель функции обратного вызова в качестве входного параметра в функцию **директсаундкреате** или **директсаундкаптурекреате** .</span><span class="sxs-lookup"><span data-stu-id="6c655-151">To begin device enumeration, the application passes a callback function pointer as an input parameter to the **DirectSoundCreate** or **DirectSoundCaptureCreate** function.</span></span> <span data-ttu-id="6c655-152">Определение функции обратного вызова:</span><span class="sxs-lookup"><span data-stu-id="6c655-152">The definition of the callback function is:</span></span>


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



<span data-ttu-id="6c655-153">В Windows Vista параметр *лпкстрмодуле* указывает на строку идентификатора конечной точки.</span><span class="sxs-lookup"><span data-stu-id="6c655-153">In Windows Vista, the *lpcstrModule* parameter points to the endpoint ID string.</span></span> <span data-ttu-id="6c655-154">(В более ранних версиях Windows, включая Windows Server 2003, Windows XP и Windows 2000, параметр *лпкстрмодуле* указывает на имя модуля драйвера для устройства.) Параметр *лпкстрдескриптион* указывает на строку, содержащую понятное имя устройства.</span><span class="sxs-lookup"><span data-stu-id="6c655-154">(In earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000, the *lpcstrModule* parameter points to the name of the driver module for the device.) The *lpcstrDescription* parameter points to a string that contains the friendly name of the device.</span></span> <span data-ttu-id="6c655-155">Дополнительные сведения о перечислении устройств DirectSound см. в документации по Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="6c655-155">For more information about DirectSound device enumeration, see the Windows SDK documentation.</span></span>

<span data-ttu-id="6c655-156">Во-вторых, чтобы получить строку идентификатора конечной точки для устаревшего устройства волны, используйте функцию **вавеаутмессаже** или **вавеинмессаже** для отправки \_ сообщения DRV куерифунктионинстанцеид в драйвер устройства волны.</span><span class="sxs-lookup"><span data-stu-id="6c655-156">Second, to obtain the endpoint ID string for a legacy waveform device, use the **waveOutMessage** or **waveInMessage** function to send a DRV\_QUERYFUNCTIONINSTANCEID message to the waveform device driver.</span></span> <span data-ttu-id="6c655-157">Пример кода, демонстрирующий использование этого сообщения, см. в разделе [роли устройств для устаревших приложений Windows мультимедиа](device-roles-for-legacy-windows-multimedia-applications.md).</span><span class="sxs-lookup"><span data-stu-id="6c655-157">For a code example that shows the use of this message, see [Device Roles for Legacy Windows Multimedia Applications](device-roles-for-legacy-windows-multimedia-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c655-158">См. также</span><span class="sxs-lookup"><span data-stu-id="6c655-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c655-159">Взаимодействие с устаревшими API аудио</span><span class="sxs-lookup"><span data-stu-id="6c655-159">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



