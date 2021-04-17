---
description: Демонстрирует использование сетевых функций, размещенных в беспроводной сети.
ms.assetid: 3da903c2-bdfa-4c1f-92e7-962551f0e08e
title: Пример беспроводной размещенной сети
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefc91dad883242876d7b0ddf1ec66fb92b18a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673321"
---
# <a name="wireless-hosted-network-sample"></a><span data-ttu-id="66c6f-103">Пример беспроводной размещенной сети</span><span class="sxs-lookup"><span data-stu-id="66c6f-103">Wireless Hosted Network Sample</span></span>

<span data-ttu-id="66c6f-104">В состав пакета средств разработки программного обеспечения (SDK) для Microsoft Windows входит пример беспроводной размещенной сети, демонстрирующий использование функций, размещенных в беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="66c6f-104">A wireless Hosted Network sample that demonstrates the use of wireless Hosted Network functions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="66c6f-105">Последняя версия Windows SDK доступна в [центре загрузки](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span><span class="sxs-lookup"><span data-stu-id="66c6f-105">The latest version of the Windows SDK is available from the [Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).</span></span>

<span data-ttu-id="66c6f-106">По умолчанию исходный код с примером беспроводной размещенной сети устанавливается в следующем каталоге:</span><span class="sxs-lookup"><span data-stu-id="66c6f-106">By default, the wireless Hosted Network sample source code is installed in the following directory:</span></span>

<span data-ttu-id="66c6f-107">**C: \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ нетдс \\ WLAN**</span><span class="sxs-lookup"><span data-stu-id="66c6f-107">**C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\NetDs\\Wlan**</span></span>

<span data-ttu-id="66c6f-108">Пример беспроводной размещенной сети находится в следующей папке:</span><span class="sxs-lookup"><span data-stu-id="66c6f-108">The wireless Hosted Network sample is located under the following folder:</span></span>

<span data-ttu-id="66c6f-109">**вирелесшостеднетворк**</span><span class="sxs-lookup"><span data-stu-id="66c6f-109">**WirelessHostedNetwork**</span></span>

<span data-ttu-id="66c6f-110">Образец беспроводной размещенной сети можно скомпилировать на Windows SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="66c6f-110">The Wireless Hosted Network sample can be compiled on the Windows SDK for Windows 7.</span></span> <span data-ttu-id="66c6f-111">Пример беспроводной размещенной сети можно запустить в Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="66c6f-111">The Wireless Hosted Network sample can be run on Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed.</span></span>

<span data-ttu-id="66c6f-112">В Windows 7 и Windows Server 2008 R2 с установленной службой беспроводной локальной сети операционная система устанавливает виртуальное устройство, если на компьютере имеется беспроводной адаптер с поддержкой размещенного сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="66c6f-112">On Windows 7 and on Windows Server 2008 R2 with the Wireless LAN Service installed, the operating system installs a virtual device if a Hosted Network capable wireless adapter is present on the machine.</span></span> <span data-ttu-id="66c6f-113">Это виртуальное устройство обычно отображается в папке "Сетевые подключения" как "Беспроводное сетевое подключение 2" с именем устройства "адаптер мини-порта Microsoft Virtual WiFi", если компьютер имеет один беспроводной сетевой адаптер.</span><span class="sxs-lookup"><span data-stu-id="66c6f-113">This virtual device normally shows up in the "Network Connections Folder" as "Wireless Network Connection 2" with a Device Name of "Microsoft Virtual WiFi Miniport adapter" if the computer has a single wireless network adapter.</span></span> <span data-ttu-id="66c6f-114">Это виртуальное устройство используется исключительно для выполнения подключений к точке доступа к программному обеспечению (Софтап).</span><span class="sxs-lookup"><span data-stu-id="66c6f-114">This virtual device is used exclusively for performing software access point (SoftAP) connections.</span></span> <span data-ttu-id="66c6f-115">Время существования этого виртуального устройства привязывается к физическому адаптеру беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="66c6f-115">The lifetime of this virtual device is tied to the physical wireless adapter.</span></span> <span data-ttu-id="66c6f-116">Если физический адаптер беспроводной сети отключен, это виртуальное устройство также будет удалено.</span><span class="sxs-lookup"><span data-stu-id="66c6f-116">If the physical wireless adapter is disabled, this virtual device will be removed as well.</span></span>

<span data-ttu-id="66c6f-117">Сетевые функции, размещенные в беспроводной сети, используются для запуска и отключения беспроводной размещенной сети, настройки или изменения параметров или запроса сведений.</span><span class="sxs-lookup"><span data-stu-id="66c6f-117">The wireless Hosted Network functions are used to start and stop the wireless Hosted Network, configure or change settings, or query for information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66c6f-118">См. также</span><span class="sxs-lookup"><span data-stu-id="66c6f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66c6f-119">Сведения о беспроводной размещенной сети</span><span class="sxs-lookup"><span data-stu-id="66c6f-119">About the Wireless Hosted Network</span></span>](about-the-wireless-hosted-network.md)
</dt> <dt>

[<span data-ttu-id="66c6f-120">Использование размещенной сети и общего доступа к подключению к Интернету</span><span class="sxs-lookup"><span data-stu-id="66c6f-120">Using Hosted Network and Internet Connection Sharing</span></span>](using-hosted-network-and-internet-connection-sharing.md)
</dt> <dt>

[<span data-ttu-id="66c6f-121">**вланхостеднетворкфорцестарт**</span><span class="sxs-lookup"><span data-stu-id="66c6f-121">**WlanHostedNetworkForceStart**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
</dt> <dt>

[<span data-ttu-id="66c6f-122">**вланхостеднетворкинитсеттингс**</span><span class="sxs-lookup"><span data-stu-id="66c6f-122">**WlanHostedNetworkInitSettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
</dt> <dt>

[<span data-ttu-id="66c6f-123">**вланхостеднетворккуерипроперти**</span><span class="sxs-lookup"><span data-stu-id="66c6f-123">**WlanHostedNetworkQueryProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
</dt> <dt>

[<span data-ttu-id="66c6f-124">**вланхостеднетворккуерисекондарикэй**</span><span class="sxs-lookup"><span data-stu-id="66c6f-124">**WlanHostedNetworkQuerySecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
</dt> <dt>

[<span data-ttu-id="66c6f-125">**вланхостеднетворккуеристатус**</span><span class="sxs-lookup"><span data-stu-id="66c6f-125">**WlanHostedNetworkQueryStatus**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
</dt> <dt>

[<span data-ttu-id="66c6f-126">**вланхостеднетворкрефрешсекуритисеттингс**</span><span class="sxs-lookup"><span data-stu-id="66c6f-126">**WlanHostedNetworkRefreshSecuritySettings**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
</dt> <dt>

[<span data-ttu-id="66c6f-127">**вланхостеднетворксетпроперти**</span><span class="sxs-lookup"><span data-stu-id="66c6f-127">**WlanHostedNetworkSetProperty**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
</dt> <dt>

[<span data-ttu-id="66c6f-128">**вланхостеднетворксетсекондарикэй**</span><span class="sxs-lookup"><span data-stu-id="66c6f-128">**WlanHostedNetworkSetSecondaryKey**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
</dt> <dt>

[<span data-ttu-id="66c6f-129">**вланхостеднетворкстартусинг**</span><span class="sxs-lookup"><span data-stu-id="66c6f-129">**WlanHostedNetworkStartUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
</dt> <dt>

[<span data-ttu-id="66c6f-130">**вланхостеднетворкстопусинг**</span><span class="sxs-lookup"><span data-stu-id="66c6f-130">**WlanHostedNetworkStopUsing**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
</dt> <dt>

[<span data-ttu-id="66c6f-131">**вланрегистервиртуалстатионнотификатион**</span><span class="sxs-lookup"><span data-stu-id="66c6f-131">**WlanRegisterVirtualStationNotification**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)
</dt> </dl>

 

 



