---
description: События аудио для устаревших звуковых приложений
ms.assetid: 91a93b79-2563-4b25-af5d-ca5f7d35d77b
title: События аудио для устаревших звуковых приложений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e030561123ba8501a66a2837bcc323a6505226a80c385f3dcaa532b2e6cd8c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018492"
---
# <a name="audio-events-for-legacy-audio-applications"></a>События аудио для устаревших звуковых приложений

устаревшие api аудио, такие как DirectSound, DirectShow и функции **вавеауткскскс** , позволяют приложениям получать и задавать уровни громкости звуковых потоков. Приложения могут использовать возможности управления томами в этих API для показа ползунков громкости в окнах приложений.

в Windows Vista программа системного управления громкостью, сндвол, позволяет пользователям управлять уровнями громкости звука для отдельных приложений. Ползунки громкости, отображаемые приложениями, должны быть связаны с соответствующими ползунками громкости в Сндвол. Если пользователь настраивает том приложения с помощью ползунка громкости в окне приложения, соответствующий ползунок в Сндвол немедленно перемещается, чтобы показать новый уровень громкости. И наоборот, если пользователь настраивает том приложения через Сндвол, ползунки громкости в окне приложения должны перемещаться, чтобы показать новый уровень громкости.

в Windows Vista сндвол немедленно отражает изменения томов, с помощью которых приложение выполняет вызовы метода **идиректсаундбуффер:: сетволуме** или функции **вавеаутсетволуме** . Однако устаревший аудио API, например DirectSound или функции **вавеауткскскс** , не предоставляет средств уведомления о приложении, когда пользователь изменяет том приложения через сндвол. Если приложение отображает ползунок громкости, но не получает уведомлений об изменениях тома, то ползунок не будет отражать изменения, внесенные пользователем в Сндвол. Чтобы реализовать соответствующее поведение, конструктор приложений должен каким-либо образом компенсировать отсутствие уведомлений от устаревших API аудио.

Одно из решений может быть для того, чтобы приложение установило таймер для периодического напоминания об изменении уровня громкости, чтобы проверить, изменился ли он.

Более элегантное решение заключается в том, чтобы приложение использовало возможности уведомления о событиях основных API-интерфейсов аудио. В частности, приложение может зарегистрировать интерфейс [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) для получения обратных вызовов при изменении громкости или других типах звуковых событий. При изменении тома подпрограммы обратного вызова изменения тома могут немедленно обновить ползунок тома приложения, чтобы отразить изменение.

В следующем примере кода показано, как приложение может зарегистрироваться для получения уведомлений об изменениях тома и других звуковых событиях.


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



В предыдущем примере кода реализуется класс с именем Аудиоволумивентс. Во время инициализации программы звуковое приложение включает уведомления о событиях аудио, создавая объект Аудиоволумивентс. Конструктор для этого класса принимает три входных параметра:

-   *Flow*— направление потока данных [устройства конечной точки аудио](audio-endpoint-devices.md) (значение перечисления [**едатафлов**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow) ).
-   *роль*— текущая [роль устройства](device-roles.md) конечной точки (значение перечисления [**ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) ).
-   *паудиоевентс*— указатель на объект (экземпляр интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) ), который содержит набор подпрограмм обратного вызова, реализованных приложением.

Конструктор предоставляет значения потока и роли в качестве входных параметров для метода [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) . Метод создает объект [**иммдевице**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) , инкапсулирующий устройство конечных точек звука с указанным направлением потока данных и ролью устройства.

Приложение реализует объект, на который указывает *паудиоевентс*. (Реализация не показана в предыдущем примере кода. Пример кода, в котором реализуется интерфейс **иаудиосессионевентс** , см. в разделе [события сеанса звука](audio-session-events.md).) Каждый метод в этом интерфейсе получает уведомления о звуковом событии определенного типа. Если приложение не заинтересовано в определенном типе событий, метод для этого типа события не должен выполнять никаких действий, но возвращать значение S \_ ОК.

Метод [**иаудиосессионевентс:: онсимплеволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) получает уведомления об изменениях тома. Как правило, этот метод обновляет ползунок громкости приложения.

В приведенном выше примере кода конструктор для класса Аудиоволумивентс регистрируется для уведомлений в [звуковом сеансе](audio-sessions.md) конкретного процесса, который определяется идентификатором GUID сеанса \_ null. по умолчанию устаревшие api аудио, такие как DirectSound, DirectShow и функции **вавеауткскскс** , назначают свои потоки этому сеансу. однако приложение DirectSound или DirectShow может, как вариант, переопределять поведение по умолчанию и назначать его потоки межпроцессному сеансу или сеансу, который определяется значением guid, отличным от guid \_ NULL. (В настоящее время механизм для приложения **вавеауткскскс** не предназначен для переопределения поведения по умолчанию аналогичным образом.) пример кода приложения DirectShow с таким поведением см. в разделе [роли устройств для DirectShow приложений](device-roles-for-directshow-applications.md). Для размещения такого приложения можно изменить конструктор в предыдущем примере кода, чтобы принять два дополнительных входных параметра — GUID сеанса и флаг, указывающий, является ли отслеживаемый сеанс межпроцессным или конкретным процессом. Передайте эти параметры в вызов метода [**иаудиосессионманажер:: жетаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionmanager-getaudiosessioncontrol) в конструкторе.

После того как конструктор вызывает метод [**иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) для регистрации уведомлений, приложение продолжит получать уведомления только при условии, что существует либо интерфейс [**Иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) , либо [**иаудиосессионманажер**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionmanager) . Объект Аудиоволумивентс в предыдущем примере кода содержит ссылки на эти интерфейсы, пока не будет вызван его деструктор. Такое поведение гарантирует, что приложение продолжит получать уведомления в течение времени существования объекта Аудиоволумивентс.

вместо неявного выбора звукового устройства на основе его роли устройства приложение DirectSound или устаревшее Windows мультимедиа может позволить пользователю явно выбрать устройство из списка доступных устройств, идентифицируемых их понятными именами. Для поддержки такого поведения необходимо изменить предыдущий пример кода, чтобы создать уведомления о звуковых событиях для выбранного устройства. Требуются два изменения. Сначала измените определение конструктора, чтобы принять [строку идентификатора конечной точки](endpoint-id-strings.md) в качестве входного параметра (вместо параметров Flow и Role в примере кода). Эта строка определяет устройство аудио конечной точки, соответствующее выбранному устройству аудио или устаревшей версии DirectSound. Во-вторых, замените вызов метода [**иммдевицеенумератор:: жетдефаултаудиоендпоинт**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) вызовом метода [**иммдевицеенумератор::-Device**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdevice) . Вызов **метода** GetString принимает строку идентификатора конечной точки в качестве входного параметра и создает экземпляр устройства конечной точки, определяемый строкой.

Ниже приведена методика получения строки идентификатора конечной точки для устройства DirectSound или устаревшей версии аудио.

Во первых, во время перечисления устройств DirectSound предоставляет строку идентификатора конечной точки для каждого перечислимого устройства. Чтобы начать перечисление устройств, приложение передает указатель функции обратного вызова в качестве входного параметра в функцию **директсаундкреате** или **директсаундкаптурекреате** . Определение функции обратного вызова:


```C++
BOOL DSEnumCallback(
  LPGUID  lpGuid,
  LPCSTR  lpcstrDescription,
  LPCSTR  lpcstrModule,
  LPVOID  lpContext
);
```



в Windows Vista параметр *лпкстрмодуле* указывает на строку идентификатора конечной точки. (в более ранних версиях Windows, включая Windows Server 2003, Windows XP и Windows 2000, параметр *лпкстрмодуле* указывает на имя модуля драйвера для устройства.) Параметр *лпкстрдескриптион* указывает на строку, содержащую понятное имя устройства. дополнительные сведения о перечислении устройств DirectSound см. в документации по Windows SDK.

Во-вторых, чтобы получить строку идентификатора конечной точки для устаревшего устройства волны, используйте функцию **вавеаутмессаже** или **вавеинмессаже** для отправки \_ сообщения DRV куерифунктионинстанцеид в драйвер устройства волны. пример кода, демонстрирующий использование этого сообщения, см. в разделе [роли устройств для устаревших Windows мультимедийных приложений](device-roles-for-legacy-windows-multimedia-applications.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Взаимодействие с устаревшими API аудио](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



