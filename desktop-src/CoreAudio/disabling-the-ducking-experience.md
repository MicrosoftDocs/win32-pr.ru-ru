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
# <a name="disabling-the-default-ducking-experience"></a><span data-ttu-id="2f2a6-103">Отключение интерфейса Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2f2a6-103">Disabling the Default Ducking Experience</span></span>

<span data-ttu-id="2f2a6-104">Пользователь может отключить [интерфейс Дуккинг по умолчанию](stream-attenuation.md) , предоставляемый системой, с помощью параметров, доступных на вкладке " **связь** " панели управления Windows мультимедиа, Mmsys.cpl.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-104">A user can disable the [Default Ducking Experience](stream-attenuation.md) provided by the system by using the options that are available on the **Communications** tab of the Windows multimedia control panel, Mmsys.cpl.</span></span>

<span data-ttu-id="2f2a6-105">Когда применяется дуккинг, эффект затухания и исчезновения используется в течение 1 секунды.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-105">When ducking is applied, a fade-out and fade-in effect is used for a period of 1 second.</span></span> <span data-ttu-id="2f2a6-106">Игровое приложение может не помешать потоку обмена данными с звуком игры.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-106">A game application might not want the communication stream to interfere with the game audio.</span></span> <span data-ttu-id="2f2a6-107">Некоторые мультимедийные приложения могут обнаружить, что при постепенном воспроизведении музыки жарринг.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-107">Some media applications might find that the playback experience is jarring when music fades back in.</span></span> <span data-ttu-id="2f2a6-108">Эти типы приложений могут не участвовать в работе дуккинг.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-108">These types of applications can choose not to participate in the ducking experience.</span></span>

<span data-ttu-id="2f2a6-109">Программно, прямой ВАСАПИ клиент может отказаться от использования диспетчера сеансов для сеанса звука, предоставляющего управление томами для потоков, не связанных с обменом данными.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-109">Programmatically, a direct WASAPI client can opt out by using the session manager for the audio session that provides volume control for the non-communication streams.</span></span> <span data-ttu-id="2f2a6-110">Обратите внимание, что даже если клиент перейдет из дуккинг, он по-прежнему получает уведомления дуккинг от системы.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-110">Note that even if an client opts out of ducking, it still receives ducking notifications from the system.</span></span>

<span data-ttu-id="2f2a6-111">Чтобы отказаться от дуккинг, клиент должен получить ссылку на интерфейс [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) диспетчера сеансов.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-111">To opt out of ducking, the client must get a reference to the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) interface of the session manager.</span></span> <span data-ttu-id="2f2a6-112">Чтобы отказаться от работы с дуккинг, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-112">To opt out of the ducking experience, use the following steps:</span></span>

1.  <span data-ttu-id="2f2a6-113">Создайте экземпляр перечислителя устройства и используйте его для получения ссылки на конечную точку устройства, используемое приложением мультимедиа для отображения потока без связи.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-113">Instantiate the device enumerator and use it to get a reference to the endpoint of the device that the media application is using to render the non-communication stream.</span></span>
2.  <span data-ttu-id="2f2a6-114">Активируйте диспетчер сеансов из конечной точки устройства и получите ссылку на интерфейс [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) диспетчера сеансов.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-114">Activate the session manager from the device endpoint and get a reference to the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) interface of the session manager.</span></span>
3.  <span data-ttu-id="2f2a6-115">С помощью указателя [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) получите ссылку на интерфейс [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) диспетчера сеансов.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-115">By using the [**IAudioSessionManager2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager2) pointer, get a reference to the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface of the session manager.</span></span>
4.  <span data-ttu-id="2f2a6-116">Запрос [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) из интерфейса [**иаудиосессионконтрол**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) .</span><span class="sxs-lookup"><span data-stu-id="2f2a6-116">Query for the [**IAudioSessionControl2**](/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol2) from the [**IAudioSessionControl**](/windows/desktop/api/Audiopolicy/nn-audiopolicy-iaudiosessioncontrol) interface.</span></span>
5.  <span data-ttu-id="2f2a6-117">Вызовите метод [**IAudioSessionControl2:: сетдуккингпреференце**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) и передайте **значение true** или **false** , чтобы указать предпочтение дуккинг.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-117">Call [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference) and pass **TRUE** or **FALSE** to specify the ducking preference.</span></span> <span data-ttu-id="2f2a6-118">Указанные параметры можно динамически изменить во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-118">The specified preference can be changed dynamically during the session.</span></span> <span data-ttu-id="2f2a6-119">Обратите внимание, что изменение согласия не вступит в силу, пока поток не будет остановлен и запущен снова.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-119">Note that the opt-out change does not take effect until the stream is stopped and started again.</span></span>

<span data-ttu-id="2f2a6-120">В следующем коде показано, как приложение может указать свои предпочтения дуккинг.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-120">The following code shows how an application can specify its ducking preference.</span></span> <span data-ttu-id="2f2a6-121">Вызывающая функция должна передавать **значение true** или **false** в параметре дуккингоптаутчеккед.</span><span class="sxs-lookup"><span data-stu-id="2f2a6-121">The caller of the function must pass **TRUE** or **FALSE** in the DuckingOptOutChecked parameter.</span></span> <span data-ttu-id="2f2a6-122">В зависимости от переданного значения дуккинг включается или отключается с помощью [**IAudioSessionControl2:: сетдуккингпреференце**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span><span class="sxs-lookup"><span data-stu-id="2f2a6-122">Depending on the value passed, ducking is enabled or disabled through the [**IAudioSessionControl2::SetDuckingPreference**](/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol2-setduckingpreference).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="2f2a6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="2f2a6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2a6-124">Использование коммуникационного устройства</span><span class="sxs-lookup"><span data-stu-id="2f2a6-124">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="2f2a6-125">Интерфейс Дуккинг по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2f2a6-125">Default Ducking Experience</span></span>](stream-attenuation.md)
</dt> <dt>

[<span data-ttu-id="2f2a6-126">Предоставление пользовательского поведения Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2f2a6-126">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="2f2a6-127">Рекомендации по реализации для уведомлений Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2f2a6-127">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="2f2a6-128">Получение событий Дуккинг</span><span class="sxs-lookup"><span data-stu-id="2f2a6-128">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



