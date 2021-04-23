---
description: Собственный API Wi-Fi содержит набор функций, которые поддерживают использование Wi-Fi Direct для классических приложений.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: О функции Direct Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674300"
---
# <a name="about-the-wi-fi-direct-feature"></a><span data-ttu-id="d27e9-103">О функции Direct Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d27e9-103">About the Wi-Fi Direct feature</span></span>

<span data-ttu-id="d27e9-104">Собственный API Wi-Fi содержит набор функций, которые поддерживают использование Wi-Fi Direct для классических приложений.</span><span class="sxs-lookup"><span data-stu-id="d27e9-104">The Native Wifi API contains a set of functions that support the use of Wi-Fi Direct for desktop apps.</span></span> <span data-ttu-id="d27e9-105">Начиная с Windows 8 и Windows Server 2012, Wi-Fi прямые функции были добавлены в собственный интерфейс API WiFi.</span><span class="sxs-lookup"><span data-stu-id="d27e9-105">Starting on Windows 8 and Windows Server 2012, Wi-Fi Direct functions were added to the Native Wifi API.</span></span>

<span data-ttu-id="d27e9-106">Функция Wi-Fi Direct основана на разработке Wi-Fi технической спецификации v 1.1 в Wi-Fi Alliance (см. статью [опубликованные спецификации Wi-Fi Alliance](https://www.wi-fi.org/)).</span><span class="sxs-lookup"><span data-stu-id="d27e9-106">The Wi-Fi Direct feature is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see [Wi-Fi Alliance Published Specifications](https://www.wi-fi.org/)).</span></span> <span data-ttu-id="d27e9-107">Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводной доступ) для настройки подключения или использования существующего механизма Wi-Fi ad hoc (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="d27e9-107">The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi ad hoc (IBSS) mechanism.</span></span>

> [!Note]  
> <span data-ttu-id="d27e9-108">Нерегламентированный режим может быть недоступен в будущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d27e9-108">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="d27e9-109">Начиная с Windows 8.1 и Windows Server 2012 R2 используйте вместо них Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="d27e9-109">Starting with Windows 8.1 and Windows Server 2012 R2, use Wi-Fi Direct instead.</span></span>

 

<span data-ttu-id="d27e9-110">Для классического приложения функция Wi-Fi Direct требует, чтобы устройства Wi-FI Direct были ранее парными для пользователя с помощью пользовательского интерфейса связывания Windows.</span><span class="sxs-lookup"><span data-stu-id="d27e9-110">For a desktop app, the Wi-Fi Direct feature requires that Wi-FI Direct devices be previously paired by the user with the Windows Pairing experience user interface.</span></span> <span data-ttu-id="d27e9-111">После завершения связывания сохраняется профиль, который позволяет использовать Wi-Fi прямые функции для запуска Wi-Fi прямого сеанса для установления соединения между Wi-Fiными устройствами.</span><span class="sxs-lookup"><span data-stu-id="d27e9-111">Once this pairing is completed, a profile is stored that allows the Wi-Fi Direct functions to be used to start a Wi-Fi Direct session to establish a connection between the Wi-Fi Direct devices.</span></span>

<span data-ttu-id="d27e9-112">Следующие функции поддерживают функцию прямого Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="d27e9-112">The following functions support the Wi-Fi Direct feature.</span></span>

-   <span data-ttu-id="d27e9-113">[**Вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) — указывает, что приложению требуется отменить отложенную функцию [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) , которая не была завершена.</span><span class="sxs-lookup"><span data-stu-id="d27e9-113">[**WFDCancelOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) - Indicates that the app wants to cancel a pending [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function that has not completed.</span></span>
-   <span data-ttu-id="d27e9-114">[**Вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) — закрывает обработчик для Wi-Fi Direct Service.</span><span class="sxs-lookup"><span data-stu-id="d27e9-114">[**WFDCloseHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) - Closes a handle to the Wi-Fi Direct service.</span></span>
-   <span data-ttu-id="d27e9-115">[**Вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) — закрывает сеанс после предыдущего успешного вызова функции [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .</span><span class="sxs-lookup"><span data-stu-id="d27e9-115">[**WFDCloseSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) - Closes a session after a previously successful call to the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function.</span></span>
-   <span data-ttu-id="d27e9-116">[**Вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) — открывает обработчик для Wi-Fi Direct Service и согласовывает версию интерфейса API прямого подключения Wi-Fi для использования.</span><span class="sxs-lookup"><span data-stu-id="d27e9-116">[**WFDOpenHandle**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) - Opens a handle to the Wi-Fi Direct service and negotiates a version of the Wi-FI Direct API to use.</span></span>
-   <span data-ttu-id="d27e9-117">[**Вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) — извлекает и применяет сохраненный профиль для устройства Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="d27e9-117">[**WFDOpenLegacySession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) - Retrieves and applies a stored profile for a Wi-Fi Direct legacy device.</span></span>
-   <span data-ttu-id="d27e9-118">[**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) — запускает подключение по требованию к конкретному Wi-Fi прямое устройство, которое ранее было парно с помощью связывания Windows.</span><span class="sxs-lookup"><span data-stu-id="d27e9-118">[**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) - Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.</span></span>
-   <span data-ttu-id="d27e9-119">[**Вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) — обновляет видимость устройства для Wi-Fi адресом прямого устройства для заданного установленного Wi-Fi прямого узла устройства.</span><span class="sxs-lookup"><span data-stu-id="d27e9-119">[**WFDUpdateDeviceVisibility**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) - Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.</span></span>
-   <span data-ttu-id="d27e9-120">[**WFD \_ \_ \_ \_ Обратный вызов для завершения открытия сеанса**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) — определяет функцию обратного вызова, вызываемую функцией [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) по завершении операции **вфдстартопенсессион**</span><span class="sxs-lookup"><span data-stu-id="d27e9-120">[**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) - Defines the callback function that is called by the [**WFDStartOpenSession**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) function when the **WFDStartOpenSession** operation completes</span></span>

<span data-ttu-id="d27e9-121">Дополнительные сведения об использовании Wi-Fi Direct в классическом приложении см. в разделе [Использование функций Wi-Fi Direct](using-the-wi-fi-direct-api.md).</span><span class="sxs-lookup"><span data-stu-id="d27e9-121">For more information on using Wi-Fi Direct in a desktop app, see [Using the Wi-Fi Direct functions](using-the-wi-fi-direct-api.md).</span></span>

<span data-ttu-id="d27e9-122">Дополнительные сведения о Wi-Fi Direct для использования в приложениях для Магазина Windows см. в разделе [**пирфиндер**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) и связанные классы в пространстве имен [**Windows. Networking. близость**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .</span><span class="sxs-lookup"><span data-stu-id="d27e9-122">For more information on Wi-Fi Direct for use in Windows Store apps, see [**PeerFinder**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) and related classes in the [**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d27e9-123">См. также</span><span class="sxs-lookup"><span data-stu-id="d27e9-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d27e9-124">**Другие источники**</span><span class="sxs-lookup"><span data-stu-id="d27e9-124">**Other resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d27e9-125">О встроенных WiFi</span><span class="sxs-lookup"><span data-stu-id="d27e9-125">About Native Wifi</span></span>](about-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="d27e9-126">Сведения о встроенном API Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d27e9-126">About the Native Wifi API</span></span>](about-the-native-wifi-api.md)
</dt> <dt>

[<span data-ttu-id="d27e9-127">Сведения о беспроводном нерегламентированном API</span><span class="sxs-lookup"><span data-stu-id="d27e9-127">About the Wireless Ad Hoc API</span></span>](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[<span data-ttu-id="d27e9-128">Использование прямых функций Wi-Fi</span><span class="sxs-lookup"><span data-stu-id="d27e9-128">Using the Wi-Fi Direct functions</span></span>](using-the-wi-fi-direct-api.md)
</dt> <dt>

<span data-ttu-id="d27e9-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d27e9-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d27e9-130">**пирфиндер**</span><span class="sxs-lookup"><span data-stu-id="d27e9-130">**PeerFinder**</span></span>](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[<span data-ttu-id="d27e9-131">**\_ \_ \_ обратный вызов для завершения открытого сеанса \_ WFD**</span><span class="sxs-lookup"><span data-stu-id="d27e9-131">**WFD\_OPEN\_SESSION\_COMPLETE\_CALLBACK**</span></span>](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[<span data-ttu-id="d27e9-132">**вфдканцелопенсессион**</span><span class="sxs-lookup"><span data-stu-id="d27e9-132">**WFDCancelOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[<span data-ttu-id="d27e9-133">**вфдклосехандле**</span><span class="sxs-lookup"><span data-stu-id="d27e9-133">**WFDCloseHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[<span data-ttu-id="d27e9-134">**вфдклосесессион**</span><span class="sxs-lookup"><span data-stu-id="d27e9-134">**WFDCloseSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[<span data-ttu-id="d27e9-135">**вфдопенхандле**</span><span class="sxs-lookup"><span data-stu-id="d27e9-135">**WFDOpenHandle**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[<span data-ttu-id="d27e9-136">**вфдопенлегацисессион**</span><span class="sxs-lookup"><span data-stu-id="d27e9-136">**WFDOpenLegacySession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[<span data-ttu-id="d27e9-137">**вфдстартопенсессион**</span><span class="sxs-lookup"><span data-stu-id="d27e9-137">**WFDStartOpenSession**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[<span data-ttu-id="d27e9-138">**вфдупдатедевицевисибилити**</span><span class="sxs-lookup"><span data-stu-id="d27e9-138">**WFDUpdateDeviceVisibility**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[<span data-ttu-id="d27e9-139">**Windows.Networking.Proximity**</span><span class="sxs-lookup"><span data-stu-id="d27e9-139">**Windows.Networking.Proximity**</span></span>](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
