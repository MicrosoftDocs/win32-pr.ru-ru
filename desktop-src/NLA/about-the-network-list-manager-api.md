---
title: Сведения об API диспетчера списка сетей
description: Сведения об API диспетчера списка сетей
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779124"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="c5d8b-103">Сведения об API диспетчера списка сетей</span><span class="sxs-lookup"><span data-stu-id="c5d8b-103">About the Network List Manager API</span></span>

<span data-ttu-id="c5d8b-104">Сетевая среда Microsoft Windows позволяет многосетевым компьютерам одновременно подключаться к нескольким сетям.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="c5d8b-105">Можно использовать несколько беспроводных сетей вместе с локальной сетью и коммутируемыми подключениями.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="c5d8b-106">Диспетчер списка сетей определяет доступные сети и возвращает приложению данные атрибутов сети.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="c5d8b-107">API диспетчера списка сетей взаимодействует со службой диспетчера списка сетей для определения и извлечения свойств каждой сети, к которой подключается компьютер.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="c5d8b-108">Каждая сеть уникально идентифицируется с помощью подписи сети на основе уникально идентифицируемых свойств этой сети.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="c5d8b-109">Когда приложение регистрируется для уведомлений диспетчера списка сетей, оно получает уведомления о доступности новых сетевых подключений или изменениях существующих сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="c5d8b-110">Приложения могут настраивать свою логику в зависимости от того, к какой сети они подключены. к какому сетевому подключению они подключены; или свойства сети.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="c5d8b-111">С помощью этих информационных приложений можно настроить действия в соответствии с текущими условиями сети.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="c5d8b-112">В Windows Vista появились новые интерфейсы, которые можно использовать для получения подробных сведений об этих характеристиках сети и многом другое.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="c5d8b-113">С помощью интерфейса [**инетворклистманажер**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) можно легко перечислить все сети ([**инетворк**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)), когда компьютер уже встречался или только подключенные сети, либо только отключенные сети.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="c5d8b-114">Интерфейс **инетворклистманажер** также упрощает перечисление сетевых интерфейсов на компьютере.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="c5d8b-115">Интерфейс [**инетворк**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) используется для определения свойств сетевого подключения: имя, описание, идентификатор, управляемый, аутентифицированный, подключенный или отключенный, а также другие.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="c5d8b-116">Возможно, что одна сеть подключена к нескольким интерфейсам, поэтому через интерфейс **инетворк** можно также перечислить используемые экземпляры интерфейса **инетворк** .</span><span class="sxs-lookup"><span data-stu-id="c5d8b-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="c5d8b-117">Интерфейс [**инетворк**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) сообщает о соответствующих свойствах интерфейса: ID, GUID, тип (управляемый, аутентифицированный) и состояние (подключено, отключено, локально, v4 Интернета, IPv6, локальная версия, V6 Интернет).</span><span class="sxs-lookup"><span data-stu-id="c5d8b-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="c5d8b-118">V4 local означает локальный доступ с помощью протокола IP версии 4 (IPv4).</span><span class="sxs-lookup"><span data-stu-id="c5d8b-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="c5d8b-119">V4 Интернет означает IPv4 с доступом к Интернету.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="c5d8b-120">V6 Local и V6 Internet означают IPv6.</span><span class="sxs-lookup"><span data-stu-id="c5d8b-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="c5d8b-121">Корневым элементом дерева объектов для сетевого расположения является интерфейс [**инетворклистманажер**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) .</span><span class="sxs-lookup"><span data-stu-id="c5d8b-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="c5d8b-122">Этот интерфейс реализован в компонентном классе **CLSID \_ нетворклистманажер** .</span><span class="sxs-lookup"><span data-stu-id="c5d8b-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="c5d8b-123">Чтобы использовать этот интерфейс, необходимо создать COM-объект **\_ нетворклистманажер CLSID** , как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="c5d8b-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




