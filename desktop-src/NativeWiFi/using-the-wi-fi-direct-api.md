---
description: Показывает, как использовать Wi-Fi прямые функции в классических приложениях.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Использование прямых функций Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663040"
---
# <a name="using-the-wi-fi-direct-functions"></a><span data-ttu-id="df979-103">Использование прямых функций Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="df979-103">Using the Wi-Fi Direct functions</span></span>

<span data-ttu-id="df979-104">В этом разделе показано, как использовать Wi-Fi прямые функции в классических приложениях.</span><span class="sxs-lookup"><span data-stu-id="df979-104">This topics shows how to use Wi-Fi Direct functions in desktop apps.</span></span> <span data-ttu-id="df979-105">Начиная с Windows 8 и Windows Server 2012, Wi-Fi прямые функции были добавлены в собственный интерфейс API WiFi.</span><span class="sxs-lookup"><span data-stu-id="df979-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="df979-106">Функция Wi-Fi Direct основана на разработке Wi-Fi технической спецификации v 1.1 в Wi-Fi Alliance (см. статью [опубликованные спецификации Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="df979-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="df979-107">Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводной доступ) для настройки подключения или использования существующего механизма Wi-Fi ad hoc (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="df979-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="df979-108">Нерегламентированный режим может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="df979-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="df979-109">Начиная с Windows 8.1 и Windows Server 2012 R2 используйте вместо них Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="df979-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="df979-110">Следующие функции поддерживают функцию прямого Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="df979-110">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="df979-111">[**Вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) — указывает, что приложению требуется отменить отложенную функцию [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) , которая не была завершена.</span><span class="sxs-lookup"><span data-stu-id="df979-111">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="df979-112">[**Вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) — закрывает обработчик для Wi-Fi Direct Service.</span><span class="sxs-lookup"><span data-stu-id="df979-112">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="df979-113">[**Вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) — закрывает сеанс после предыдущего успешного вызова функции [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="df979-113">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="df979-114">[**Вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) — открывает обработчик для Wi-Fi Direct Service и согласовывает версию интерфейса API прямого подключения Wi-Fi для использования.</span><span class="sxs-lookup"><span data-stu-id="df979-114">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="df979-115">[**Вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) — извлекает и применяет сохраненный профиль для устройства Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="df979-115">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="df979-116">[**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) — запускает подключение по требованию к конкретному Wi-Fi прямое устройство, которое ранее было парно с помощью связывания Windows.</span><span class="sxs-lookup"><span data-stu-id="df979-116">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="df979-117">[**Вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) — обновляет видимость устройства для Wi-Fi адресом прямого устройства для заданного установленного Wi-Fi прямого узла устройства.</span><span class="sxs-lookup"><span data-stu-id="df979-117">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="df979-118">[**WFD \_ \_ \_ \_ Обратный вызов для завершения открытия сеанса**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) — определяет функцию обратного вызова, вызываемую функцией [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) по завершении операции **вфдстартопенсессион**</span><span class="sxs-lookup"><span data-stu-id="df979-118">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="df979-119">Для классического приложения функция Wi-Fi Direct требует, чтобы устройства Wi-FI Direct были ранее парными для пользователя с помощью пользовательского интерфейса связывания Windows.</span><span class="sxs-lookup"><span data-stu-id="df979-119">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="df979-120">После завершения связывания сохраняется профиль, который позволяет использовать Wi-Fi прямые функции для запуска Wi-Fi прямого сеанса для установления соединения между Wi-Fiными устройствами.</span><span class="sxs-lookup"><span data-stu-id="df979-120">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="df979-121">Чтобы использовать Wi-Fi Direct, приложение должно сначала получить обработчик прямой службы Wi-Fi, вызвав функцию [**вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) .</span><span class="sxs-lookup"><span data-stu-id="df979-121">In order to use Wi-Fi Direct, an app must first obtain a handle to the Wi-Fi Direct service by calling the [**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) function.</span></span> <span data-ttu-id="df979-122">Wi-Fi Direct (WFD), возвращаемый функцией **вфдопенхандле** , используется для последующего Wi-Fi прямых вызовов функций, выполненных в Wi-Fi Direct Service.</span><span class="sxs-lookup"><span data-stu-id="df979-122">The Wi-Fi Direct (WFD) handle returned by the **WFDOpenHandle** function is used for subsequent Wi-Fi Direct function calls made to the Wi-Fi Direct service.</span></span>

<span data-ttu-id="df979-123">Функция [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) запускает асинхронную операцию для запуска подключения по требованию к конкретному Wi-Fi непосредственному устройству.</span><span class="sxs-lookup"><span data-stu-id="df979-123">The [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function starts an asynchronous operation to start an on-demand connection to a specific Wi-Fi Direct device.</span></span> <span data-ttu-id="df979-124">Целевое устройство Wi-Fi должно быть ранее сопряжено с помощью функции связывания Windows.</span><span class="sxs-lookup"><span data-stu-id="df979-124">The target Wi-Fi device must previously have been paired through the Windows Pairing experience.</span></span> <span data-ttu-id="df979-125">По завершении асинхронной операции вызывается функция обратного вызова, указанная в параметре *пфнкаллбакк* .</span><span class="sxs-lookup"><span data-stu-id="df979-125">When the asynchronous operation completes, the callback function specified in the *pfnCallback* parameter is called.</span></span>

<span data-ttu-id="df979-126">После того как приложение будет выполнено с помощью Wi-Fi Direct Service, приложение должно вызвать функцию [**вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) , чтобы сообщить Wi-Fi прямой службе о том, что приложение выполняется с помощью службы.</span><span class="sxs-lookup"><span data-stu-id="df979-126">Once an application is done using the Wi-Fi Direct service, the application should call the [**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) function to signal to the Wi-Fi Direct service that the application is done using the service.</span></span> <span data-ttu-id="df979-127">Это позволяет службе Wi-Fi Direct Service выпустить ресурсы, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="df979-127">This allows the Wi-Fi Direct service to release resources used by the application.</span></span>

<span data-ttu-id="df979-128">Дополнительные сведения о Wi-Fi Direct для использования в приложениях для Магазина Windows см. в разделе [**пирфиндер**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) и связанные классы в пространстве имен [**Windows. Networking. близость**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="df979-128">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df979-129">См. также</span><span class="sxs-lookup"><span data-stu-id="df979-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="df979-130">**Другие источники**</span><span class="sxs-lookup"><span data-stu-id="df979-130">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="df979-131">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="df979-131">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="df979-132">Сведения о встроенном API Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="df979-132">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="df979-133">О функции Direct Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="df979-133">About the Wi-Fi Direct feature</span></span>](about-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="df979-134">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="df979-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="df979-135">**пирфиндер**</span><span class="sxs-lookup"><span data-stu-id="df979-135">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="df979-136">**\_ \_ \_ обратный вызов для завершения открытого сеанса \_ WFD**</span><span class="sxs-lookup"><span data-stu-id="df979-136">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="df979-137">**вфдканцелопенсессион**</span><span class="sxs-lookup"><span data-stu-id="df979-137">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="df979-138">**вфдклосехандле**</span><span class="sxs-lookup"><span data-stu-id="df979-138">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="df979-139">**вфдклосесессион**</span><span class="sxs-lookup"><span data-stu-id="df979-139">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="df979-140">**вфдопенхандле**</span><span class="sxs-lookup"><span data-stu-id="df979-140">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="df979-141">**вфдопенлегацисессион**</span><span class="sxs-lookup"><span data-stu-id="df979-141">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="df979-142">**вфдстартопенсессион**</span><span class="sxs-lookup"><span data-stu-id="df979-142">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="df979-143">**вфдупдатедевицевисибилити**</span><span class="sxs-lookup"><span data-stu-id="df979-143">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="df979-144">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="df979-144">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
