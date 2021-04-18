---
description: В инфраструктуре WMI служба WMI (winmgmt) — это компонент операционной системы, который выступает в качестве медиатора между приложениями управления и поставщиками данных WMI. Репозиторий WMI — это область хранилища для статических данных, связанных с WMI.
ms.assetid: 6ef157be-fb75-4453-bc20-4568a3dc18c0
ms.tgt_platform: multiple
title: Инфраструктура WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4370af9ec062ffa845d54eafda054357a76dc07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702057"
---
# <a name="wmi-infrastructure"></a><span data-ttu-id="f0c1c-104">Инфраструктура WMI</span><span class="sxs-lookup"><span data-stu-id="f0c1c-104">WMI Infrastructure</span></span>

<span data-ttu-id="f0c1c-105">В инфраструктуре WMI служба WMI (winmgmt) — это компонент операционной системы, который выступает в качестве медиатора между приложениями управления и [*поставщиками*](gloss-p.md)данных WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-105">In the WMI infrastructure, the WMI service (Winmgmt) is the operating system component that acts as the mediator between management applications and WMI data [*providers*](gloss-p.md).</span></span> <span data-ttu-id="f0c1c-106">[*Репозиторий WMI*](gloss-w.md) — это область хранилища для статических данных, связанных с WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-106">The [*WMI repository*](gloss-w.md) is a storage area for WMI-related static data.</span></span>

<span data-ttu-id="f0c1c-107">Служба WMI реализуется как процесс службы в рамках процесса общего узла службы (SVCHOST).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-107">The WMI service is implemented as a service process within a shared service host process (SVCHOST).</span></span> <span data-ttu-id="f0c1c-108">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-108">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="f0c1c-109">Служба WMI запускается, когда первое приложение или сценарий управления вызывает подключение к пространству имен WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-109">The WMI service starts when the first management application or script makes a call to connect to a WMI namespace.</span></span> <span data-ttu-id="f0c1c-110">В зависимости от настройки Служба WMI может завершить работу или перейти в профиль нехватки памяти, если он не вызывается приложением управления.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-110">Depending on the setup, the WMI service may shut down or go into a low memory profile when not being called by a management application.</span></span>

<span data-ttu-id="f0c1c-111">Служба WMI взаимодействует с приложениями управления через интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-111">The WMI service interacts with management applications through the COM interface.</span></span> <span data-ttu-id="f0c1c-112">Когда приложение выполняет запрос через интерфейс, WMI определяет, относится ли запрос к статическим или динамическим данным.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-112">When an application makes a request through the interface, WMI determines whether the request is for static or dynamic data.</span></span> <span data-ttu-id="f0c1c-113">Если запрос включает статические данные, например имя управляемого объекта, Инструментарий WMI получает данные из репозитория.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-113">If the request involves static data, such as the name of a managed object, WMI retrieves the data from the repository.</span></span> <span data-ttu-id="f0c1c-114">Если запрос включает динамические данные, например объем памяти, который в настоящее время используется управляемым объектом, WMI передает запрос поставщику.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-114">If the request involves dynamic data, such as the amount of memory a managed object is currently using, WMI passes the request on to a provider.</span></span>

<span data-ttu-id="f0c1c-115">Поставщики регистрируют свое расположение в службе WMI, что позволяет инструментарию WMI маршрутизировать запросы данных.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-115">Providers register their location with the WMI service, which allows WMI to route data requests.</span></span> <span data-ttu-id="f0c1c-116">Поставщик также регистрирует поддержку определенных операций, таких как получение данных, изменение, удаление, перечисление или обработка запросов.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-116">A provider also registers support for particular operations, such as data retrieval, modification, deletion, enumeration, or query processing.</span></span> <span data-ttu-id="f0c1c-117">Служба WMI использует сведения о регистрации поставщика для сопоставления запросов приложений с соответствующим поставщиком.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-117">The WMI service uses the provider registration information to match application requests with the appropriate provider.</span></span> <span data-ttu-id="f0c1c-118">Инструментарий WMI также использует сведения о регистрации для загрузки и выгрузки поставщиков при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-118">WMI also uses the registration information to load and unload providers, as necessary.</span></span> <span data-ttu-id="f0c1c-119">Когда поставщик заканчивает обработку запроса, поставщик возвращает результат обратно в службу WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-119">When a provider finishes processing a request, the provider returns the result back to the WMI service.</span></span> <span data-ttu-id="f0c1c-120">Затем WMI перенаправляет результат в приложение через интерфейс COM.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-120">WMI then forwards the result on to the application through the COM interface.</span></span> <span data-ttu-id="f0c1c-121">Дополнительные сведения см. [в разделе Предоставление данных инструментарию WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="f0c1c-122">Инструментарий WMI использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) для записи действий службы WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c1c-122">WMI uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) to record WMI service activity.</span></span>

<span data-ttu-id="f0c1c-123">Поскольку инфраструктура обрабатывает весь трафик между поставщиками и приложениями управления, инфраструктура предоставляет следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="f0c1c-123">Because the infrastructure handles all traffic between the providers and the management applications, the infrastructure provides the following features:</span></span>

-   <span data-ttu-id="f0c1c-124">Поддержка уведомлений о событиях</span><span class="sxs-lookup"><span data-stu-id="f0c1c-124">Event Notification Support</span></span>

    <span data-ttu-id="f0c1c-125">Дополнительные сведения см. в разделе [наблюдение за событиями](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-125">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="f0c1c-126">Поддержка языка запросов</span><span class="sxs-lookup"><span data-stu-id="f0c1c-126">Query Language Support</span></span>

    <span data-ttu-id="f0c1c-127">Дополнительные сведения см. [в разделе запросы с помощью WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-127">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

-   <span data-ttu-id="f0c1c-128">Поддержка безопасности</span><span class="sxs-lookup"><span data-stu-id="f0c1c-128">Security Support</span></span>

    <span data-ttu-id="f0c1c-129">Дополнительные сведения см. в разделе [обслуживание безопасности WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-129">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

-   <span data-ttu-id="f0c1c-130">Создание сценариев для доступа к данным счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="f0c1c-130">Scripting Access to Performance Counter Data</span></span>

    <span data-ttu-id="f0c1c-131">Дополнительные сведения см. в разделе [наблюдение за данными производительности](monitoring-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="f0c1c-131">For more information, see [Monitoring Performance Data](monitoring-performance-data.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0c1c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="f0c1c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c1c-133">Архитектура WMI</span><span class="sxs-lookup"><span data-stu-id="f0c1c-133">WMI Architecture</span></span>](wmi-architecture.md)
</dt> </dl>

 

 
