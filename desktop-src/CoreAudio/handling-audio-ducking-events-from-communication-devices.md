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
# <a name="implementation-considerations-for-ducking-notifications"></a>Рекомендации по реализации для уведомлений Дуккинг

[Интерфейс Дуккинг по умолчанию](stream-attenuation.md) , предоставляемый системой, утками все потоки, не связанные с обменом данными, доступные в системе при открытии коммуникационного потока. Приложение мультимедиа может переопределить обработку по умолчанию, если известно, когда начинается и заканчивается сеанс связи.

Рассмотрим сценарий, реализуемый приложением мультимедиа в примере [дуккингмедиаплайер](duckingmediaplayer.md) . Приложение приостанавливает поток звука, который воспроизводится при получении уведомления утка и возобновляет воспроизведение при получении уведомления ундукк. События приостановки и продолжения отражаются в пользовательском интерфейсе приложения мультимедиа. Это поддерживается двумя сообщениями окон, определяемыми приложением, \_ \_ сеансами приложений WM \_ дуккед и \_ \_ ундуккед сеанса приложения WM \_ . Уведомления дуккинг получаются асинхронно в фоновом режиме, и приложение мультимедиа не должно блокировать поток уведомлений для обработки оконных сообщений. Оконные сообщения должны обрабатываться в потоке пользовательского интерфейса.

Поведение дуккинг работает через механизм уведомления. Чтобы обеспечить настраиваемый интерфейс, приложение мультимедиа должно реализовать интерфейс [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) и зарегистрировать реализацию в звуковой системе. После успешной регистрации приложение мультимедиа получает уведомления о событиях в форме обратных вызовов через методы интерфейса. Диспетчер сеансов, обрабатывающий сеанс связи, вызывает [**иаудиоволумедуккнотификатион:: онволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeducknotification) , когда поток связи открывается, а затем вызывает [**Иаудиоволумедуккнотификатион:: OnVolumeUnduckNotification**](/windows/desktop/api/AudioPolicy/nf-audiopolicy-iaudiovolumeducknotification-onvolumeunducknotification) при закрытии потока на коммуникационном устройстве.

В следующем коде показан пример реализации интерфейса [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . Определение Кмедиаплайер::D Уккингоптаут см. в разделе Получение событий Дуккинг с коммуникационного устройства.


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование коммуникационного устройства](using-the-communication-device.md)
</dt> <dt>

[Интерфейс Дуккинг по умолчанию](stream-attenuation.md)
</dt> <dt>

[Отключение интерфейса Дуккинг по умолчанию](disabling-the-ducking-experience.md)
</dt> <dt>

[Предоставление пользовательского поведения Дуккинг](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Получение событий Дуккинг](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



