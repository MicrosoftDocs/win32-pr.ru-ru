---
description: Приложение мультимедиа, которое хочет предоставить собственный дуккинг интерфейс, должно прослушивать уведомления о событиях при открытии или закрытии потока связи в системе.
ms.assetid: 709ad912-6b03-4ad3-bc47-ad8b6bd6de45
title: Получение событий Дуккинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5869aa02a64ef3b7d035743b9bee3c91d295448c4d89d659862c5efc81d89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828265"
---
# <a name="getting-ducking-events"></a>Получение событий Дуккинг

Приложение мультимедиа, которое хочет предоставить собственный дуккинг интерфейс, должно прослушивать уведомления о событиях при открытии или закрытии потока связи в системе. пользовательскую реализацию можно предоставить с помощью медиафаундатион, DirectShow или DirectSound, которые используют основные api аудио. Прямой ВАСАПИ клиент может также переопределить обработку по умолчанию, если он знает, когда начинается и заканчивается сеанс связи.

Чтобы обеспечить пользовательскую реализацию, приложение мультимедиа должно получать уведомления от системы, когда приложение для обмена данными запускается или завершает поток связи. Приложение мультимедиа должно реализовать интерфейс [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) и зарегистрировать реализацию в звуковой системе. После успешной регистрации приложение мультимедиа получает уведомления о событиях в форме обратных вызовов через методы интерфейса. Дополнительные сведения см. в статье [рекомендации по реализации для уведомлений дуккинг](handling-audio-ducking-events-from-communication-devices.md).

Чтобы отправлять уведомления дуккинг, в звуковой системе должно быть указано, какой сеанс звука прослушивает события дуккинг. Каждый сеанс звука однозначно идентифицируется с помощью GUID — идентификатора экземпляра сеанса. Диспетчер сеансов позволяет приложению получать сведения о сеансе, такие как название сеанса аудио, состояние отрисовки и идентификатор экземпляра сеанса. Идентификатор можно получить с помощью интерфейса управления политиками [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2).

Ниже приведено краткое описание процесса получения идентификатора экземпляра сеанса приложения мультимедиа.

1.  Создайте экземпляр перечислителя устройства и используйте его для получения ссылки на конечную точку устройства, используемое приложением мультимедиа для отображения потока без связи.
2.  Активируйте диспетчер сеансов из конечной точки устройства и получите ссылку на интерфейс [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) диспетчера сеансов.
3.  С помощью указателя [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) получите ссылку на интерфейс [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) диспетчера сеансов.
4.  Запрос [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) из интерфейса [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Вызовите метод [**IAudioSessionControl2:: жетсессионинстанцеидентифиер**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-getsessioninstanceidentifier) и получите строку, содержащую идентификатор сеанса для текущего сеанса аудио.

Чтобы получать уведомления дуккинг о потоках связи, приложение мультимедиа вызывает [**IAudioSessionManager2:: регистердуккнотификатион**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-registerducknotification). Приложение мультимедиа предоставляет свой идентификатор экземпляра сеанса звуковой системе и указатель на реализацию [**иаудиоволумедуккнотификатион**](/windows/desktop/api/AudioPolicy/nn-audiopolicy-iaudiovolumeducknotification) . Теперь приложение может получить уведомление о событии при открытии потока на коммуникационном устройстве. Чтобы отключить получение уведомлений, приложение мультимедиа должно вызвать [**IAudioSessionManager2:: унрегистердуккнотификатион**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessionmanager2-unregisterducknotification).

В следующем коде показано, как приложение может зарегистрироваться для получения уведомлений дуккинг. Класс Кмедиаплайер определяется в [вопросах реализации уведомлений дуккинг](handling-audio-ducking-events-from-communication-devices.md). В примере [дуккингмедиаплайер](duckingmediaplayer.md) реализована эта функция.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование коммуникационного устройства](using-the-communication-device.md)
</dt> <dt>

[Интерфейс Дуккинг по умолчанию](stream-attenuation.md)
</dt> <dt>

[Отключение интерфейса Дуккинг по умолчанию](disabling-the-ducking-experience.md)
</dt> <dt>

[Предоставление пользовательского поведения Дуккинг](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Рекомендации по реализации для уведомлений Дуккинг](handling-audio-ducking-events-from-communication-devices.md)
</dt> </dl>

 

 



