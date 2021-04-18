---
title: Принудительное применение уровня приложения (ALE)
description: ALE — это набор слоев режима ядра платформы фильтрации Windows (WFP), которые используются для фильтрации с отслеживанием состояния.
ms.assetid: ffebd312-9220-476c-a4ba-28e2e8ac8879
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f4cab1b2583d221c59d83c513c451077c806129
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412914"
---
# <a name="application-layer-enforcement-ale"></a><span data-ttu-id="05465-103">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="05465-103">Application Layer Enforcement (ALE)</span></span>

<span data-ttu-id="05465-104">ALE — это набор слоев режима ядра платформы фильтрации Windows (WFP), которые используются для фильтрации с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="05465-104">ALE is a set of Windows Filtering Platform (WFP) kernel-mode layers that are used for stateful filtering.</span></span>

<span data-ttu-id="05465-105">Фильтрация с отслеживанием состояния отслеживает состояние сетевых подключений и разрешает только пакеты, соответствующие известному состоянию соединения.</span><span class="sxs-lookup"><span data-stu-id="05465-105">Stateful filtering keeps track of the state of network connections and allows only packets that match a known connection state.</span></span> <span data-ttu-id="05465-106">Например, фильтрация с отслеживанием состояния для TCP-подключения, инициированного через брандмауэр, может разрешить только входящие пакеты, которые соответствуют предыдущим исходящим пакетам, отправленным с помощью защищенной стороны.</span><span class="sxs-lookup"><span data-stu-id="05465-106">For example, stateful filtering for a TCP connection initiated from behind a firewall can allow only incoming packets that match previous outgoing packets sent by the party protected.</span></span>

<span data-ttu-id="05465-107">Фильтры в слоях ALE разрешают входящее и исходящее подключение, назначение портов, операции сокета, такие как [**Listen ()**](/windows/desktop/api/winsock2/nf-winsock2-listen), создание необработанных сокетов и получение неизбирательного режима.</span><span class="sxs-lookup"><span data-stu-id="05465-107">Filters in the ALE layers authorize inbound and outbound connection creation, port assignments, socket operations such as [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen), raw socket creation, and promiscuous mode receiving.</span></span>

<span data-ttu-id="05465-108">Трафик на уровнях ALE классифицируется как для каждого подключения, так и для каждой операции сокета.</span><span class="sxs-lookup"><span data-stu-id="05465-108">Traffic at the ALE layers is classified either per-connection or per-socket operation.</span></span> <span data-ttu-id="05465-109">В слоях, не относящихся к ALE, фильтры могут классифицировать трафик только на основе каждого пакета.</span><span class="sxs-lookup"><span data-stu-id="05465-109">At non-ALE layers, filters can only classify traffic on a per-packet basis.</span></span>

<span data-ttu-id="05465-110">Уровни ALE — это единственные уровни WFP, в которых можно фильтровать сетевой трафик на основе удостоверения приложения, используя нормализованное имя файла и основанное на удостоверении пользователя, используя дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="05465-110">ALE layers are the only WFP layers where network traffic can be filtered based on the application identity—using a normalized file name—and based on the user identity—using a security descriptor.</span></span> <span data-ttu-id="05465-111">(См. ФЛТ \_ \_Сведения об имени файла \_ в документации по Windows Driver Kit (WDK) для получения дополнительных сведений об нормализованных именах файлов.)</span><span class="sxs-lookup"><span data-stu-id="05465-111">(See FLT\_FILE\_NAME\_INFORMATION in the Windows Driver Kit (WDK) documentation, for more information on normalized file names.)</span></span>

<span data-ttu-id="05465-112">Кроме того, если для защиты подключения используется протокол IPsec, фильтрация на уровнях ALE также может выполняться на удостоверении удаленного компьютера и на удаленном удостоверении пользователя.</span><span class="sxs-lookup"><span data-stu-id="05465-112">In addition, when IPsec is used to secure the connection, filtering at ALE layers can also be performed on the remote machine identity and on the remote user identity.</span></span> <span data-ttu-id="05465-113">Идентификаторы удаленного компьютера и пользователя получаются из учетных данных, используемых при создании сеанса IPsec.</span><span class="sxs-lookup"><span data-stu-id="05465-113">The remote machine and user identities are obtained from the credentials used in the creation of an IPsec session.</span></span>

<span data-ttu-id="05465-114">По этой причине политики, которые определяют, кто (например, "Администратор") и (или) какое приложение (например, "Internet Explorer") могут выполнять сетевые операции, упомянутые выше, создаются на уровнях ALE.</span><span class="sxs-lookup"><span data-stu-id="05465-114">For this reason, policies that enforce who (for example, "administrator") and/or which application (for example, "Internet Explorer") are allowed to perform the network operations mentioned above are authored at the ALE layers.</span></span>

<span data-ttu-id="05465-115">ALE обеспечивает применение политик, таких как «разрешить Windows Messenger полный доступ к сети при блокировании всех других приложений».</span><span class="sxs-lookup"><span data-stu-id="05465-115">ALE provides enforcement for policies such as "allow Windows Messenger all access to the network while blocking all other applications."</span></span> <span data-ttu-id="05465-116">В этом примере, когда приложение «Messenger» подключается по сети, ALE проверяет событие, определяет, что оно было инициировано программой Messenger, и запрашивает обработчик фильтра WFP, чтобы определить, разрешено ли продолжение работы сокета.</span><span class="sxs-lookup"><span data-stu-id="05465-116">In such an example, when the application "Messenger" connects across the network, ALE traps the event, determines that it was initiated by Messenger and queries the WFP filter engine to determine whether the socket should be allowed to proceed.</span></span>

> [!Note]  
> <span data-ttu-id="05465-117">Из-за природы истинных сокетов с двумя IP-адресами классификации на уровне ALE IPv4 могут не произойти.</span><span class="sxs-lookup"><span data-stu-id="05465-117">Due to the nature of true dual-IP sockets, classifications at the IPv4 ALE layer may not occur.</span></span> <span data-ttu-id="05465-118">Это обусловлено проектированием, поскольку для всех целей и задач сокет является сокетом IPv6.</span><span class="sxs-lookup"><span data-stu-id="05465-118">This is by design, because for all intents and purposes, the socket is an IPv6 socket.</span></span> <span data-ttu-id="05465-119">Чтобы просмотреть трафик v4 для такого сокета, создайте фильтры на уровне V6, используя сопоставленный IPv6 адрес.</span><span class="sxs-lookup"><span data-stu-id="05465-119">To see the V4 traffic for such a socket, create filters at the V6 layer using the IPv6-mapped address.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="05465-120">См. также</span><span class="sxs-lookup"><span data-stu-id="05465-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05465-121">Уровни ALE</span><span class="sxs-lookup"><span data-stu-id="05465-121">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="05465-122">Фильтрация с отслеживанием состояния ALE</span><span class="sxs-lookup"><span data-stu-id="05465-122">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="05465-123">Многоадресный или широковещательный трафик ALE</span><span class="sxs-lookup"><span data-stu-id="05465-123">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="05465-124">Повторная авторизация ALE</span><span class="sxs-lookup"><span data-stu-id="05465-124">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="05465-125">Настройка потока ALE</span><span class="sxs-lookup"><span data-stu-id="05465-125">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> </dl>

 

 