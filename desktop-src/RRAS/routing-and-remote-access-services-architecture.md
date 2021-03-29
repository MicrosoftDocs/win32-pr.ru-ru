---
title: Архитектура служб маршрутизации и удаленного доступа
description: На следующем рисунке представлено общее представление архитектуры маршрутизатора Windows 2000.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- Маршрутизация и удаленный доступ служба RRAS, архитектура службы маршрутизации и удаленного доступа RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486920"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="60851-104">Архитектура служб маршрутизации и удаленного доступа</span><span class="sxs-lookup"><span data-stu-id="60851-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="60851-105">На следующем рисунке представлено общее представление архитектуры маршрутизатора Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="60851-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="60851-106">Компоненты, относящиеся к семейству протоколов IP, отображаются светло-серым цветом.</span><span class="sxs-lookup"><span data-stu-id="60851-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="60851-107">Компоненты, относящиеся к семейству протоколов IPX, показаны темно-серым цветом.</span><span class="sxs-lookup"><span data-stu-id="60851-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="60851-108">Компоненты, общие для всех семейств протоколов, не затенены.</span><span class="sxs-lookup"><span data-stu-id="60851-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="60851-109">Служба маршрутизации и удаленного доступа предоставляет API-интерфейсы для администрирования и настройки службы.</span><span class="sxs-lookup"><span data-stu-id="60851-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="60851-110">Эти интерфейсы API включают агенты SNMP для IP-адресов и IPX.</span><span class="sxs-lookup"><span data-stu-id="60851-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="60851-111">Служба RRAS включает протоколы маршрутизации для IP и IPX.</span><span class="sxs-lookup"><span data-stu-id="60851-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="60851-112">Для IP-адреса служба RRAS предоставляет протокол RIP и открытые протоколы маршрутизации OSPF.</span><span class="sxs-lookup"><span data-stu-id="60851-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="60851-113">Для IPX служба RRAS предоставляет протокол IPX RIP и SAP.</span><span class="sxs-lookup"><span data-stu-id="60851-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="60851-114">RRAS использует один диспетчер таблиц маршрутизации (RTM) для IP-адресов и IPX.</span><span class="sxs-lookup"><span data-stu-id="60851-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="60851-115">Однако каждое семейство протоколов имеет собственный диспетчер маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="60851-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="60851-116">RRAS также имеет отдельный компонент для управления группами многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="60851-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="60851-117">Интерфейс диспетчера динамических интерфейсов (DIM) со службами PPP и TAPI используется для управления интерфейсами PPP, используемыми некоторыми маршрутами.</span><span class="sxs-lookup"><span data-stu-id="60851-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![общее архитектурное представление маршрутизатора Windows 2000](images/rtarch.png)

 

 




