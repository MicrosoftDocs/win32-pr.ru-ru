---
description: Демонстрирует использование основных функций управления беспроводной сетью.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Пример собственного API WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ac72000363fcb91f013c3f55d4686335c0a59e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683345"
---
# <a name="native-wifi-api-sample"></a><span data-ttu-id="1f2a2-103">Пример собственного API WiFi</span><span class="sxs-lookup"><span data-stu-id="1f2a2-103">Native Wifi API Sample</span></span>

<span data-ttu-id="1f2a2-104">Встроенный пример API WiFi, демонстрирующий использование основных функций управления беспроводной сетью, входит в состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-104">A Native Wifi API sample that demonstrates the use of basic wireless network management functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1f2a2-105">Последняя версия Windows SDK доступна в [центре загрузки](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-105">The latest version of the Windows SDK is available from the [Download Center](https://developer.microsoft.com/windows/downloads).</span></span>

<span data-ttu-id="1f2a2-106">По умолчанию исходный код образца Wi-Fi устанавливается в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="1f2a2-106">By default, the Native Wifi sample source code is installed in the following directory:</span></span>

<span data-ttu-id="1f2a2-107">**C: \\ Program Files \\ Microsoft пакеты SDK для \\ Windows \\ <version number> \\ примеры \\ нетдс \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="1f2a2-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="1f2a2-108">Собственный пример API WiFi находится в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="1f2a2-108">The Native Wifi API sample is located under the following folder:</span></span>

<span data-ttu-id="1f2a2-109">**AutoConfig**</span><span class="sxs-lookup"><span data-stu-id="1f2a2-109">**autoconfig**</span></span>

<span data-ttu-id="1f2a2-110">Встроенный пример Wi-Fi можно скомпилировать и запустить в Windows Vista и более поздних версиях, Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-110">The Native Wifi sample can be compiled and run on Windows Vista and later, Windows XP with Service Pack 3 (SP3), and Wireless LAN API for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="1f2a2-111">Некоторые функции образца не поддерживаются в Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-111">Some features of the sample are not supported on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span> <span data-ttu-id="1f2a2-112">Список функций, поддерживаемых Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2), см. [в разделе Встроенная поддержка API WiFi в Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)</span><span class="sxs-lookup"><span data-stu-id="1f2a2-112">For a list of functions supported by Windows XP with SP3 and Wireless LAN API for Windows XP with SP2, see [Native Wifi API Support on Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md).</span></span>

<span data-ttu-id="1f2a2-113">В примере машинного кода WiFi показано, как выполнять следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-113">The Native Wifi sample demonstrates how to perform the following tasks:</span></span>

-   <span data-ttu-id="1f2a2-114">Перечисление беспроводных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-114">Enumerate wireless interfaces.</span></span> <span data-ttu-id="1f2a2-115">См. [**вланенуминтерфацес**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-115">See [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).</span></span>
-   <span data-ttu-id="1f2a2-116">Получите возможности интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-116">Get the capabilities of an interface.</span></span> <span data-ttu-id="1f2a2-117">См. [**вланжетинтерфацекапабилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-117">See [**WlanGetInterfaceCapability**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).</span></span>

    <span data-ttu-id="1f2a2-118">\* \* Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2): \* \* Эта функция не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-118">\*\*Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:  \*\* This feature is not supported.</span></span>

-   <span data-ttu-id="1f2a2-119">Запрос интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-119">Query an interface.</span></span> <span data-ttu-id="1f2a2-120">См. [**вланкуеринтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-120">See [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).</span></span>
-   <span data-ttu-id="1f2a2-121">Задайте параметры для сетевого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-121">Set parameters for a network interface.</span></span> <span data-ttu-id="1f2a2-122">См. [**влансетинтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-122">See [**WlanSetInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface).</span></span> <span data-ttu-id="1f2a2-123">Эта функция может использоваться для включения и отключения беспроводного радио (и, следовательно, включения или отключения беспроводных сетевых подключений).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-123">This function can be used to turn the wireless radio on and off (and therefore enable or disable wireless network connectivity).</span></span>
-   <span data-ttu-id="1f2a2-124">Проверьте наличие доступных беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-124">Scan for available wireless networks.</span></span> <span data-ttu-id="1f2a2-125">См. [**вланскан**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-125">See [**WlanScan**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).</span></span>
-   <span data-ttu-id="1f2a2-126">Получение списка доступных или видимых беспроводных сетей.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-126">Get the list of available or visible wireless networks.</span></span> <span data-ttu-id="1f2a2-127">См. [**вланжетаваилабленетворклист**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-127">See [**WlanGetAvailableNetworkList**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).</span></span>
-   <span data-ttu-id="1f2a2-128">Получение, сохранение или удаление профиля.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-128">Get, save, or delete a profile.</span></span> <span data-ttu-id="1f2a2-129">См. раздел [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)и [**вланделетепрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-129">See [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), and [**WlanDeleteProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).</span></span>
-   <span data-ttu-id="1f2a2-130">Подключение к беспроводной сети или отключение от нее.</span><span class="sxs-lookup"><span data-stu-id="1f2a2-130">Connect to or disconnect from a wireless network.</span></span> <span data-ttu-id="1f2a2-131">См. раздел [**вланконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**вландисконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span><span class="sxs-lookup"><span data-stu-id="1f2a2-131">See [**WlanConnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**WlanDisconnect**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f2a2-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1f2a2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f2a2-133">Использование собственного WiFi</span><span class="sxs-lookup"><span data-stu-id="1f2a2-133">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="1f2a2-134">Форум Windows Vista Wireless SDK</span><span class="sxs-lookup"><span data-stu-id="1f2a2-134">Windows Vista Wireless SDK Forum</span></span>](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

<span data-ttu-id="1f2a2-135">[Устранение неполадок беспроводных подключений Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="1f2a2-135">[Troubleshooting Windows Vista 802.11 Wireless Connections](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))</span></span>
</dt> </dl>

 

 
