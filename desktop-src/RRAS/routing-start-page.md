---
title: Маршрутизация
description: Интерфейсы API маршрутизации позволяют создавать приложения для администрирования возможностей маршрутизации операционной системы.
ms.assetid: 66e1bbb4-73c8-40fc-9575-ffe76d4b697b
keywords:
- Маршрутизация RAS
- RAS-сервер маршрутизации, начальная страница
- RAS RRAS
- RAS RRAS см. в разделе Маршрутизация.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e3b2a92a6c54f47693d657315ec0a48e660061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891020"
---
# <a name="routing"></a><span data-ttu-id="9ff98-107">Маршрутизация</span><span class="sxs-lookup"><span data-stu-id="9ff98-107">Routing</span></span>

## <a name="purpose"></a><span data-ttu-id="9ff98-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="9ff98-108">Purpose</span></span>

<span data-ttu-id="9ff98-109">Интерфейсы API маршрутизации позволяют создавать приложения для администрирования возможностей маршрутизации операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9ff98-109">The Routing APIs make it possible to create applications to administer the routing capabilities of the operating system.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="9ff98-110">Где применимо</span><span class="sxs-lookup"><span data-stu-id="9ff98-110">Where applicable</span></span>

<span data-ttu-id="9ff98-111">Маршрутизация позволяет компьютеру работать в качестве сетевого маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="9ff98-111">Routing makes it possible for a computer to function as a network router.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9ff98-112">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="9ff98-112">Developer audience</span></span>

<span data-ttu-id="9ff98-113">API-интерфейсы маршрутизации предназначены для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="9ff98-113">The Routing APIs are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="9ff98-114">Программисты также должны быть знакомы с основными понятиями сети.</span><span class="sxs-lookup"><span data-stu-id="9ff98-114">Programmers should also be familiar with networking concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9ff98-115">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="9ff98-115">Run-time requirements</span></span>

<span data-ttu-id="9ff98-116">Маршрутизация — это серверная технология.</span><span class="sxs-lookup"><span data-stu-id="9ff98-116">Routing is a server-based technology.</span></span> <span data-ttu-id="9ff98-117">Все функции маршрутизации встроены в Windows 2000 Server и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9ff98-117">All the functionality of Routing is incorporated into Windows 2000 Server and the Windows Server 2003.</span></span> <span data-ttu-id="9ff98-118">Приложения маршрутизации не могут работать на компьютерах под управлением Windows NT Workstation 4,0 или в клиентских операционных системах, таких как Windows 95.</span><span class="sxs-lookup"><span data-stu-id="9ff98-118">Routing applications cannot run on Windows NT Workstation 4.0 or on client operating systems, such as Windows 95.</span></span> <span data-ttu-id="9ff98-119">Дополнительные сведения о том, какие операционные системы поддерживают определенную функцию, см. в разделах о требованиях в документации.</span><span class="sxs-lookup"><span data-stu-id="9ff98-119">For more specific information about which operating systems support a particular function, refer to the Requirements sections in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9ff98-120">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="9ff98-120">In this section</span></span>



| <span data-ttu-id="9ff98-121">Раздел</span><span class="sxs-lookup"><span data-stu-id="9ff98-121">Topic</span></span>                                                                                               | <span data-ttu-id="9ff98-122">Описание</span><span class="sxs-lookup"><span data-stu-id="9ff98-122">Description</span></span>                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ff98-123">Управление маршрутизаторами</span><span class="sxs-lookup"><span data-stu-id="9ff98-123">Router Management</span></span>](about-router-management.md)<br/>                                         | <span data-ttu-id="9ff98-124">API администрирования маршрутизатора позволяет разработчикам создавать приложения для управления службой маршрутизатора на компьютере под управлением Windows 2000 Server и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="9ff98-124">The router administration API allows developers to create applications to manage the router service on a computer running Windows 2000 Server and later operating systems.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="9ff98-125">База данных диспетчеров и управления маршрутизаторами</span><span class="sxs-lookup"><span data-stu-id="9ff98-125">Router Managers and Management Information Base</span></span>](/windows/desktop/RRAS/about-router-management-with-mib)<br/> | <span data-ttu-id="9ff98-126">API-интерфейсы базы MIB для управления маршрутизаторами позволяют запрашивать и задавать значения переменных MIB, экспортируемых одним из диспетчеров маршрутизаторов или любыми протоколами маршрутизации, которые служба диспетчера маршрутизаторов.</span><span class="sxs-lookup"><span data-stu-id="9ff98-126">The Management Information Base (MIB) APIs for router management makes it possible to query and set the values of MIB variables exported by one of the router managers or any of the routing protocols that the router managers service.</span></span> <span data-ttu-id="9ff98-127">С помощью этого API маршрутизатор поддерживает протокол SNMP.</span><span class="sxs-lookup"><span data-stu-id="9ff98-127">By using this API, the router supports the Simple Network Management Protocol (SNMP).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9ff98-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9ff98-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ff98-129">Функции IP Helper</span><span class="sxs-lookup"><span data-stu-id="9ff98-129">IP Helper Functions</span></span>](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[<span data-ttu-id="9ff98-130">Удаленный доступ</span><span class="sxs-lookup"><span data-stu-id="9ff98-130">Remote Access</span></span>](remote-access-start-page.md)
</dt> <dt>

[<span data-ttu-id="9ff98-131">Протоколы маршрутизации</span><span class="sxs-lookup"><span data-stu-id="9ff98-131">Routing Protocols</span></span>](routing-protocols-start-page.md)
</dt> </dl>

 

