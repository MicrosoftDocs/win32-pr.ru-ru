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
# <a name="managing-the-audio-session"></a>Управление сеансом аудио

\[Мфплай доступен для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. \]

В этом разделе описывается, как управлять громкостью звука при использовании Мфплай для воспроизведения звука и видео.

Мфплай предоставляет следующие методы управления звуковым томом во время воспроизведения.



| Метод                                                            | Описание                                           |
|-------------------------------------------------------------------|-------------------------------------------------------|
| [**Имфпмедиаплайер:: Сетбаланце**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance) | Устанавливает баланс между левым и правым каналами. |
| [**Имфпмедиаплайер:: Сетмуте**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute)       | Выключает или выключает звук.                           |
| [**Имфпмедиаплайер:: Сетволуме**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume)   | Задает уровень громкости.                                |



 

Чтобы понять поведение этих методов, необходимо знать некоторую терминологию из API сеанса Windows Audio (ВАСАПИ), которая реализует низкоуровневые функции аудио, используемые Мфплай.

В ВАСАПИ каждый аудиопоток принадлежит только одному *сеансу аудио*, который представляет собой группу связанных звуковых потоков. Как правило, приложение поддерживает один сеанс звука, хотя приложения могут создавать более одного сеанса. Программа системного управления громкостью (Сндвол) отображает регулятор громкости для каждого сеанса звука. С помощью Сндвол пользователь может настроить громкость звукового сеанса за пределами приложения. Этот процесс показан на следующем рисунке.

![Схема, показывающая звуковые потоки, передающие Управление громкостью на динамики; приложение и сндвол точка управления томами](images/audio-session.gif)

В Мфплай элемент мультимедиа может иметь один или несколько активных звуковых потоков (обычно только один). На внутреннем уровне Мфплай использует [потоковый рендеринг звука](streaming-audio-renderer.md) (САР) для отображения звуковых потоков. Если вы не настроите его, то САР присоединяется к сеансу аудио по умолчанию для приложения.

Методы аудио Мфплай управляют только потоками, принадлежащими текущему элементу мультимедиа. Они не влияют на том для других потоков, принадлежащих к одному сеансу звука. С точки зрения ВАСАПИ методы Мфплай управляют уровнями громкости *каждого канала* , а не главным уровнем громкости. Этот процесс показан на следующем рисунке.

![схема аналогична предыдущей, но второй поток начинается с элемента мультимедиа, а приложение указывает на второй поток и управление томом.](images/audio-session02.gif)

Важно понимать некоторые последствия этой функции Мфплай. Во первых, приложение может настраивать громкость воспроизведения, не затрагивая другие звуковые потоки. Эту функцию можно использовать, если Мфплай для реализации перекрестного затухания звука, создавая два экземпляра объекта Мфплай и настраивая том отдельно.

Если вы используете методы Мфплай для изменения тома или отключения состояния, изменения не отображаются в Сндвол. Например, можно вызвать [**сетмуте**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute) , чтобы отключить звук, но сндвол не будет отображать сеанс как отключенный. И наоборот, если Сндвол используется для корректировки объема сеанса, изменения не отражаются в значениях, возвращаемых [**имфпмедиаплайер::**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) или [**имфпмедиаплайер::-приглушением**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute).

Для каждого экземпляра объекта Player Мфплай эффективный уровень громкости равен *фплайерволуме* × *Фсессионволуме*, где *фплайерволуме* — это значение, возвращаемое методом GetObject [**, а**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume) *фсессионволуме* — главный том для сеанса.

Для простых сценариев воспроизведения может быть предпочтительнее использовать ВАСАПИ для управления звуковым томом для всего сеанса, а не использовать методы Мфплай.

## <a name="example-code"></a>Пример кода

Ниже приведен класс C++, который обрабатывает основные задачи в ВАСАПИ:

-   Управление томом и выключение его состояния для сеанса.
-   Получение уведомлений при каждом изменении тома или выключении его состояния.

### <a name="class-declaration"></a>Объявление класса

`CAudioSessionVolume`Объявление класса реализует интерфейс [**иаудиосессионевентс**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionevents) , который является интерфейсом обратного вызова для событий сеанса аудио.


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



Когда `CAudioSessionVolume` объект получает событие сеанса аудио, он отправляет приложению сообщение частного окна. Обработчик окна и сообщение окна передаются в качестве параметров в статический `CAudioSessionVolume::CreateInstance` метод.

### <a name="getting-the-wasapi-interface-pointers"></a>Получение указателей интерфейса ВАСАПИ

`CAudioSessionVolume` использует два основных интерфейса ВАСАПИ:

-   [**Иаудиосессионконтрол**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol) управляет сеансом аудио.
-   [**Исимплеаудиоволуме**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) управляет уровнем громкости и отключением состояния сеанса.

Чтобы получить эти интерфейсы, необходимо перечислить конечную точку аудио, используемую в САР. *Конечная точка аудио* — это устройство, которое фиксирует или потребляет звуковые данные. Для воспроизведения звука конечная точка — это просто докладчик или другие звуковые выходные данные. По умолчанию в САР используется конечная точка по умолчанию для роли устройства **еконсоле** . *Роль устройства* — это назначенная роль для конечной точки. Роли устройств задаются перечислением [**ероле**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) , которое описано в статье [Основные API-интерфейсы для аудио](../coreaudio/core-audio-apis-in-windows-vista.md).

В следующем коде показано, как перечислить конечную точку и получить интерфейсы ВАСАПИ.


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



### <a name="controlling-the-volume"></a>Управление томом

`CAudioSessionVolume`Методы, управляющие звуковым томом, вызывают эквивалентные методы [**исимплеаудиоволуме**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume) . Например, `CAudioSessionVolume::SetVolume` вызывает [**исимплеаудиоволуме:: сетмастерволуме**](/windows/win32/api/audioclient/nf-audioclient-isimpleaudiovolume-setmastervolume), как показано в следующем коде.


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



## <a name="complete-caudiosessionvolume-code"></a>Завершение кода Каудиосессионволуме

Ниже приведен полный список методов `CAudioSessionVolume` класса.


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



## <a name="requirements"></a>Требования

Для Мфплай требуется Windows 7.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Мфплай для воспроизведения звука и видео](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
