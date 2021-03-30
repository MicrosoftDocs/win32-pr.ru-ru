---
description: В этой статье описывается, как обновить реализацию ВАСАПИ, чтобы воспользоваться преимуществами автоматической маршрутизации потоков.
ms.assetid: 718CBEB9-A7A0-4898-81B7-CBD76AFA3A06
title: Автоматическая маршрутизация потоков
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a9848c5fd764ee49e485fc112c35c347a0f84d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990774"
---
# <a name="automatic-stream-routing"></a><span data-ttu-id="5ea14-103">Автоматическая маршрутизация потоков</span><span class="sxs-lookup"><span data-stu-id="5ea14-103">Automatic Stream Routing</span></span>

<span data-ttu-id="5ea14-104">В этой статье описывается, как обновить реализацию ВАСАПИ, чтобы воспользоваться преимуществами автоматической маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5ea14-104">This article describes how to update a WASAPI implementation to take advantage of automatic stream routing.</span></span>

<span data-ttu-id="5ea14-105">Начиная с Windows 7, всякий раз, когда звуковое устройство по умолчанию изменится, поток воспроизведения звука в приложении плавно передается с предыдущего звукового устройства по умолчанию на новое звуковое устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ea14-105">Starting with Windows 7, whenever the default audio device changes, an app's audio playback stream is seamlessly transferred from the previous default audio device to the new default audio device .</span></span> <span data-ttu-id="5ea14-106">Этот перенос происходит автоматически без дополнительного кода приложения.</span><span class="sxs-lookup"><span data-stu-id="5ea14-106">This transfer occurs automatically without any additional application code.</span></span> <span data-ttu-id="5ea14-107">Однако до Windows 10 версии 1607 приложения, в которых использовался API нижнего уровня Windows Audio (ВАСАПИ), не могли участвовать в этой функции автоматической маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5ea14-107">However, prior to Windows 10, version 1607, apps that used the low-level Windows Audio Session API (WASAPI) could not participate in this automated stream routing functionality.</span></span> <span data-ttu-id="5ea14-108">Приложения, использующие ВАСАПИ, требовались для реализации собственной формы потоковой маршрутизации путем добавления дополнительного кода для обнаружения прибытия и удаления звуковых устройств и переключения потока на соответствующие устройства.</span><span class="sxs-lookup"><span data-stu-id="5ea14-108">Apps using WASAPI were required to implement their own form of stream routing by adding additional code to detect the arrival and removal of audio devices and switch the stream to those devices as appropriate.</span></span> <span data-ttu-id="5ea14-109">Приложения, использующие ВАСАПИ, которые не реализуют собственный механизм маршрутизации потоков при получении или удалении устройства, подвержены риску, что обеспечивает менее оптимальное взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ea14-109">Applications using WASAPI that did not implement their own stream routing mechanism on device arrival or removal risked providing a less than ideal user experience.</span></span>

<span data-ttu-id="5ea14-110">Начиная с Windows 10 версии 1607, приложения, использующие ВАСАПИ, могут воспользоваться преимуществами автоматической маршрутизации потоков.</span><span class="sxs-lookup"><span data-stu-id="5ea14-110">Starting with the Windows 10, version 1607, apps that use WASAPI can take advantage of automatic stream routing.</span></span> <span data-ttu-id="5ea14-111">Если приложение использует ВАСАПИ, настоятельно рекомендуется обновить приложение, чтобы воспользоваться преимуществами этой новой возможности, выполнив следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5ea14-111">If your application uses WASAPI it is highly recommended that you update your application to take advantage of this new capability using the following steps:</span></span>

1.  <span data-ttu-id="5ea14-112">Windows 10, версия 1607, определяет два новых идентификатора GUID, которые можно использовать для активации интерфейса отрисовки аудио или записи с автоматической маршрутизацией, [девинтерфаце \_ воспроизведения \_ звука](/windows/desktop/CoreAudio/devinterface-xxx-guids) и [девинтерфаце \_ \_ записи звука](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span><span class="sxs-lookup"><span data-stu-id="5ea14-112">Windows 10, version 1607, defines two new GUIDs that can be used to activate an audio render or capture interface with automatic stream routing, [DEVINTERFACE\_AUDIO\_RENDER](/windows/desktop/CoreAudio/devinterface-xxx-guids) and [DEVINTERFACE\_AUDIO\_CAPTURE](/windows/desktop/CoreAudio/devinterface-xxx-guids).</span></span> <span data-ttu-id="5ea14-113">Получите строковое представление этих идентификаторов GUID, вызвав [**Ошибка stringfromiid**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span><span class="sxs-lookup"><span data-stu-id="5ea14-113">Get a string representation of these GUIDs by calling [**StringFromIID**](/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid).</span></span> <span data-ttu-id="5ea14-114">В следующем примере показан этот вызов для GUID отрисовки аудио.</span><span class="sxs-lookup"><span data-stu-id="5ea14-114">The following example shows this call for the audio render GUID.</span></span>

    ```C++
    PWSTR audioRenderGuidString;
    StringFromIID(DEVINTERFACE_AUDIO_RENDER, &audioRenderGuidString);
    ```

    

2.  <span data-ttu-id="5ea14-115">Активируйте конечную точку аудио, передав строку идентификатора в функцию ВАСАПИ [**активатеаудиоинтерфацеасинк**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) .</span><span class="sxs-lookup"><span data-stu-id="5ea14-115">Activate the audio endpoint by passing the identifier string to the WASAPI [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) function.</span></span> <span data-ttu-id="5ea14-116">В следующем примере передается идентификатор прорисовки аудио, полученный на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="5ea14-116">The following example passes in the audio render identifier obtained in step 1:</span></span>

    ```C++
    //Activate the default audio interface
    ActivateAudioInterfaceAsync(audioRenderGuidString
                                __uuidof(IAudioClient),
                                NULL,
                                completionHandler.Get(),
                                operation.GetAddressOf()));
    ```

    

3.  <span data-ttu-id="5ea14-117">Освободите память, выделенную для хранения идентификатора конечной точки:</span><span class="sxs-lookup"><span data-stu-id="5ea14-117">Free the memory allocated for holding the endpoint identifier:</span></span>

    ```C++
    CoTaskMemFree(audioRenderGuidString);  //free the string memory
    ```

    

<span data-ttu-id="5ea14-118">После изменения приложения для активации звукового интерфейса описанным выше способом он будет участвовать в функции автоматической маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="5ea14-118">After you have modified your app to activate the audio interface in the manner described above, it will participate in the automatic stream routing feature.</span></span>

<span data-ttu-id="5ea14-119">Чтобы продемонстрировать автоматическую маршрутизацию потоков, используйте ноутбук или планшет, оснащенные внутренними динамиками для воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="5ea14-119">To demonstrate automatic stream routing, use a laptop or tablet equipped with internal speakers to play back audio.</span></span> <span data-ttu-id="5ea14-120">Вы должны слышать звук, воспроизводимый внутренними динамиками устройства.</span><span class="sxs-lookup"><span data-stu-id="5ea14-120">You should hear the audio playing through the device's internal speakers.</span></span> <span data-ttu-id="5ea14-121">Во время воспроизведения звука подключите пару наушников.</span><span class="sxs-lookup"><span data-stu-id="5ea14-121">While audio is playing, connect a pair of headphones.</span></span> <span data-ttu-id="5ea14-122">Теперь вы должны слышать звук, проигрывается по наушникам.</span><span class="sxs-lookup"><span data-stu-id="5ea14-122">You should now hear audio playing through the headphones.</span></span> <span data-ttu-id="5ea14-123">Затем, Отсоедините наушники и аудио, должны автоматически маршрутизироваться к внутренним динамикам.</span><span class="sxs-lookup"><span data-stu-id="5ea14-123">Then, unplug the headphones and audio should automatically route back to the internal speakers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ea14-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5ea14-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ea14-125">Потоковая маршрутизация</span><span class="sxs-lookup"><span data-stu-id="5ea14-125">Stream Routing</span></span>](stream-routing.md)
</dt> <dt>

[<span data-ttu-id="5ea14-126">**Медиадевице. Жетдефаултаудиорендерид**</span><span class="sxs-lookup"><span data-stu-id="5ea14-126">**MediaDevice.GetDefaultAudioRenderId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiorenderid)
</dt> <dt>

[<span data-ttu-id="5ea14-127">**Медиадевице. Жетдефаултаудиокаптуреид**</span><span class="sxs-lookup"><span data-stu-id="5ea14-127">**MediaDevice.GetDefaultAudioCaptureId**</span></span>](/uwp/api/windows.media.devices.mediadevice.getdefaultaudiocaptureid)
</dt> <dt>

[<span data-ttu-id="5ea14-128">**активатеаудиоинтерфацеасинк**</span><span class="sxs-lookup"><span data-stu-id="5ea14-128">**ActivateAudioInterfaceAsync**</span></span>](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync)
</dt> </dl>

 

 
