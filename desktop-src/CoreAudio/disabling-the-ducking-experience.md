---
description: Пользователь может отключить интерфейс Дуккинг по умолчанию, предоставляемый системой, с помощью параметров, доступных на вкладке "связь" панели управления Windows мультимедиа, Mmsys.cpl.
ms.assetid: 5604b927-99f8-450f-a48c-b38d782584de
title: Отключение интерфейса Дуккинг по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed33fa7d9473cb5c68a018b98bff8a826612387e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142778"
---
# <a name="disabling-the-default-ducking-experience"></a>Отключение интерфейса Дуккинг по умолчанию

Пользователь может отключить [интерфейс Дуккинг по умолчанию](stream-attenuation.md) , предоставляемый системой, с помощью параметров, доступных на вкладке " **связь** " панели управления Windows мультимедиа, Mmsys.cpl.

Когда применяется дуккинг, эффект затухания и исчезновения используется в течение 1 секунды. Игровое приложение может не помешать потоку обмена данными с звуком игры. Некоторые мультимедийные приложения могут обнаружить, что при постепенном воспроизведении музыки жарринг. Эти типы приложений могут не участвовать в работе дуккинг.

Программно, прямой ВАСАПИ клиент может отказаться от использования диспетчера сеансов для сеанса звука, предоставляющего управление томами для потоков, не связанных с обменом данными. Обратите внимание, что даже если клиент перейдет из дуккинг, он по-прежнему получает уведомления дуккинг от системы.

Чтобы отказаться от дуккинг, клиент должен получить ссылку на интерфейс [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) диспетчера сеансов. Чтобы отказаться от работы с дуккинг, выполните следующие действия.

1.  Создайте экземпляр перечислителя устройства и используйте его для получения ссылки на конечную точку устройства, используемое приложением мультимедиа для отображения потока без связи.
2.  Активируйте диспетчер сеансов из конечной точки устройства и получите ссылку на интерфейс [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) диспетчера сеансов.
3.  С помощью указателя [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) получите ссылку на интерфейс [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) диспетчера сеансов.
4.  Запрос [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) из интерфейса [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .
5.  Вызовите метод [**IAudioSessionControl2:: сетдуккингпреференце**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) и передайте **значение true** или **false** , чтобы указать предпочтение дуккинг. Указанные параметры можно динамически изменить во время сеанса. Обратите внимание, что изменение согласия не вступит в силу, пока поток не будет остановлен и запущен снова.

В следующем коде показано, как приложение может указать свои предпочтения дуккинг. Вызывающая функция должна передавать **значение true** или **false** в параметре дуккингоптаутчеккед. В зависимости от переданного значения дуккинг включается или отключается с помощью [**IAudioSessionControl2:: сетдуккингпреференце**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).


```C++
////////////////////////////////////////////////////////////////////
//Description: Specifies the ducking options for the application.
//Parameters: 
//    If DuckingOptOutChecked is TRUE system ducking is disabled; 
//    FALSE, system ducking is enabled.
////////////////////////////////////////////////////////////////////

HRESULT DuckingOptOut(bool DuckingOptOutChecked)
{
    HRESULT hr = S_OK;

    IMMDeviceEnumerator* pDeviceEnumerator NULL;
    IMMDevice* pEndpoint = NULL;
    IAudioSessionManager2* pSessionManager2 = NULL;
    IAudioSessionControl* pSessionControl = NULL;
    IAudioSessionControl2* pSessionControl2 = NULL;


    //  Start with the default endpoint.

    hr = CoCreateInstance(__uuidof(MMDeviceEnumerator), 
                          NULL, 
                          CLSCTX_INPROC_SERVER, 
                          IID_PPV_ARGS(&pDeviceEnumerator));
    
    if (SUCCEEDED(hr))
    {
        hr = pDeviceEnumerator>GetDefaultAudioEndpoint(eRender, eConsole, &pEndpoint);

        pDeviceEnumerator>Release();
        pDeviceEnumerator = NULL;
    }

    // Activate session manager.
    if (SUCCEEDED(hr))
    {
        hr = pEndpoint->Activate(__uuidof(IAudioSessionManager2), 
                                 CLSCTX_INPROC_SERVER,
                                 NULL, 
                                 reinterpret_cast<void **>(&pSessionManager2));
        pEndpoint->Release();
        pEndpoint = NULL;
    }
    if (SUCCEEDED(hr))
    {
        hr = pSessionManager2->GetAudioSessionControl(NULL, 0, &pSessionControl);
        
        pSessionManager2->Release();
        pSessionManager2 = NULL;
    }

    if (SUCCEEDED(hr))
    {
        hr = pSessionControl->QueryInterface(
                  __uuidof(IAudioSessionControl2),
                  (void**)&pSessionControl2);
                
        pSessionControl->Release();
        pSessionControl = NULL;
    }

    //  Sync the ducking state with the specified preference.

    if (SUCCEEDED(hr))
    {
        if (DuckingOptOutChecked)
        {
            hr = pSessionControl2->SetDuckingPreference(TRUE);
        }
        else
        {
            hr = pSessionControl2->SetDuckingPreference(FALSE);
        }
        pSessionControl2->Release();
        pSessionControl2 = NULL;
    }
    return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование коммуникационного устройства](using-the-communication-device.md)
</dt> <dt>

[Интерфейс Дуккинг по умолчанию](stream-attenuation.md)
</dt> <dt>

[Предоставление пользовательского поведения Дуккинг](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Рекомендации по реализации для уведомлений Дуккинг](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Получение событий Дуккинг](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



