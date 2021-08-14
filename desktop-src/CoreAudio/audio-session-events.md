---
description: События сеанса звука
ms.assetid: 6943b405-0807-412b-a149-fc3a8ece1b48
title: События сеанса звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf0c3441a7f6f6835070a530c4ebb8985354b2701f312f2f085c5e449f12cbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407228"
---
# <a name="audio-session-events"></a>События сеанса звука

Приложение, которое управляет звуковыми потоками в общем режиме, может регистрироваться для получения уведомлений при возникновении событий сеанса. Как упоминалось ранее, каждый поток принадлежит к [сеансу аудио](audio-sessions.md). Событие сеанса инициируется изменением состояния сеанса аудио.

Клиентское приложение может зарегистрироваться для получения уведомлений о следующих типах событий сеанса:

-   Основной уровень громкости или состояние отключения сеанса субмикс изменилось.
-   Изменился уровень громкости одного или нескольких каналов субмикс сеанса.
-   Сеанс отключен.
-   Состояние действия сеанса изменилось на активное, неактивное или с истекшим сроком действия.
-   Сеансу был назначен новый параметр группирования.
-   Изменено свойство пользовательского интерфейса сеанса (значок или отображаемое имя).

Клиент получает уведомления об этих событиях через методы в своей реализации интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . В отличие от других интерфейсов в ВАСАПИ, которые реализуются системным модулем ВАСАПИ, клиент реализует **иаудиосессионевентс**. Методы этого интерфейса получают обратные вызовы из системного модуля ВАСАПИ при возникновении событий сеанса.

Чтобы начать получать уведомления, клиент вызывает метод [**иаудиосессионконтрол:: регистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-registeraudiosessionnotification) для регистрации своего интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Если клиенту больше не требуются уведомления, он вызывает метод [**иаудиосессионконтрол:: унрегистераудиосессионнотификатион**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-unregisteraudiosessionnotification) для удаления регистрации.

В следующем примере кода показана возможная реализация интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) :


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



Класс Каудиосессионевентс в предыдущем примере кода является реализацией интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) . Эта конкретная реализация может быть частью консольного приложения, которое выводит сведения о событиях сеанса в окно командной строки. Поскольку **иаудиосессионевентс** наследует от [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), определение класса содержит реализации методов **IUnknown** , [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)и [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Остальные открытые методы в определении класса относятся к интерфейсу **иаудиосессионевентс** .

Некоторые клиенты могут не заинтересовать наблюдение за всеми типами событий сеанса. В предыдущем примере кода несколько методов уведомления в классе Каудиосессионевентс ничего не делают. Например, метод [**ончаннелволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged) не выполняет никаких действий, кроме возврата кода состояния S \_ OK. Это приложение не отслеживает тома каналов, так как не изменяет тома канала (путем вызова методов в интерфейсе [**ичаннелаудиоволуме**](/windows/desktop/api/Audioclient/nn-audioclient-ichannelaudiovolume) ) и не использует сеанс совместно с другими приложениями, которые могут изменять тома каналов.

Единственными тремя методами в классе Каудиосессионевентс, которые уведомляют пользователя о событиях сеанса, являются [**онсимплеволумечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged), [**онстатечанжед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onstatechanged)и [**онсессиондисконнектед**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected). Например, если пользователь запускает программу системного управления громкостью, Сндвол и использует элемент управления громкостью в Сндвол для изменения уровня громкости приложения, `OnSimpleVolumeChanged` немедленно выводит новый уровень громкости.

Пример кода, который регистрирует и отменяет регистрацию интерфейса [**иаудиосессионевентс**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessionevents) клиента, см. в разделе [события аудио для устаревших аудио приложений](audio-events-for-legacy-audio-applications.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сеансы аудио](audio-sessions.md)
</dt> </dl>

 

 
