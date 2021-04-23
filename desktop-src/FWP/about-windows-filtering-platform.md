---
title: О платформе фильтрации Windows
description: Платформа фильтрации Windows (WFP) — это платформа обработки сетевого трафика, предназначенная для замены интерфейсов фильтрации сетевого трафика Windows XP и Windows Server 2003.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "105661730"
---
# <a name="about-windows-filtering-platform"></a><span data-ttu-id="74373-103">О платформе фильтрации Windows</span><span class="sxs-lookup"><span data-stu-id="74373-103">About Windows Filtering Platform</span></span>

<span data-ttu-id="74373-104">Платформа фильтрации Windows (WFP) — это платформа обработки сетевого трафика, предназначенная для замены интерфейсов фильтрации сетевого трафика Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="74373-104">Windows Filtering Platform (WFP) is a network traffic processing platform designed to replace the Windows XP and Windows Server 2003 network traffic filtering interfaces.</span></span> <span data-ttu-id="74373-105">WFP состоит из набора обработчиков в сетевом стеке и механизма фильтрации, который координирует взаимодействие сетевого стека.</span><span class="sxs-lookup"><span data-stu-id="74373-105">WFP consists of a set of hooks into the network stack and a filtering engine that coordinates network stack interactions.</span></span>

## <a name="the-wfp-components"></a><span data-ttu-id="74373-106">Компоненты платформы WFP</span><span class="sxs-lookup"><span data-stu-id="74373-106">The WFP components</span></span>

### <a name="filter-engine"></a><span data-ttu-id="74373-107">Обработчик фильтров</span><span class="sxs-lookup"><span data-stu-id="74373-107">Filter Engine</span></span>

<span data-ttu-id="74373-108">Основная инфраструктура многоуровневого фильтрации, размещенная как в режиме ядра, так и в пользовательском режиме, которая заменяет несколько модулей фильтрации в сетевой подсистеме Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="74373-108">The core multi-layer filtering infrastructure, hosted in both kernel-mode and user-mode, that replaces the multiple filtering modules in the Windows XP and Windows Server 2003 networking subsystem.</span></span>

-   <span data-ttu-id="74373-109">Фильтрует сетевой трафик на любом уровне системы в любом поле данных, которое может предоставить оболочка совместимости.</span><span class="sxs-lookup"><span data-stu-id="74373-109">Filters network traffic at any layer in the system over any data fields that a shim can provide.</span></span>
-   <span data-ttu-id="74373-110">Реализует фильтры "выноску" путем вызова выносок во время классификации.</span><span class="sxs-lookup"><span data-stu-id="74373-110">Implements the "Callout" filters by invoking callouts during classification.</span></span>
-   <span data-ttu-id="74373-111">Возвращает действия "разрешить" или "блокировать" в оболочке совместимости, которая ее вызвала для принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="74373-111">Returns "Permit" or "Block" actions to the shim that invoked it for enforcement.</span></span>
-   <span data-ttu-id="74373-112">Предоставляет арбитраж между разными источниками политики.</span><span class="sxs-lookup"><span data-stu-id="74373-112">Provides arbitration between different policy sources.</span></span> <span data-ttu-id="74373-113">Например, определяет приоритет, если приложение настроено для защиты любого сетевого трафика, связанного с ним, но локальный брандмауэр настроен для предотвращения трафика, защищенного приложением.</span><span class="sxs-lookup"><span data-stu-id="74373-113">For example, determines priority when an application is configured to secure any network traffic related to it, but the local firewall is configured to prevent application secured traffic.</span></span><br/>

### <a name="base-filtering-engine-bfe"></a><span data-ttu-id="74373-114">Модуль базовой фильтрации (BFE)</span><span class="sxs-lookup"><span data-stu-id="74373-114">Base Filtering Engine (BFE)</span></span>

<span data-ttu-id="74373-115">Служба, управляющая работой платформы фильтрации Windows.</span><span class="sxs-lookup"><span data-stu-id="74373-115">A service that controls the operation of the Windows Filtering Platform.</span></span> <span data-ttu-id="74373-116">Она выполняет следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="74373-116">It performs the following tasks.</span></span>

-   <span data-ttu-id="74373-117">Принимает фильтры и другие параметры конфигурации для платформы.</span><span class="sxs-lookup"><span data-stu-id="74373-117">Accepts filters and other configuration settings for the platform.</span></span>
-   <span data-ttu-id="74373-118">Сообщает о текущем состоянии системы, включая статистику.</span><span class="sxs-lookup"><span data-stu-id="74373-118">Reports the current state of the system, including statistics.</span></span>
-   <span data-ttu-id="74373-119">Применяет модель безопасности для приема конфигурации на платформе.</span><span class="sxs-lookup"><span data-stu-id="74373-119">Enforces the security model for accepting configuration in the platform.</span></span> <span data-ttu-id="74373-120">Например, локальный администратор может добавлять фильтры, но другие пользователи могут только просматривать их.</span><span class="sxs-lookup"><span data-stu-id="74373-120">For example, a local administrator can add filters but other users can only view them.</span></span><br/>
-   <span data-ttu-id="74373-121">Позволяет подключить параметры конфигурации к другим модулям в системе.</span><span class="sxs-lookup"><span data-stu-id="74373-121">Plumbs configuration settings to other modules in the system.</span></span> <span data-ttu-id="74373-122">Например, политики согласования IPsec переходят к модулям ключей IKE/AuthIP, фильтры попадают в обработчик фильтров.</span><span class="sxs-lookup"><span data-stu-id="74373-122">For example, IPsec negotiation polices go to IKE/AuthIP keying modules, filters go to the filter engine.</span></span><br/>

### <a name="shims"></a><span data-ttu-id="74373-123">Оболочек совместимости</span><span class="sxs-lookup"><span data-stu-id="74373-123">Shims</span></span>

<span data-ttu-id="74373-124">Компоненты режима ядра, расположенные между сетевым стеком и обработчиком фильтров.</span><span class="sxs-lookup"><span data-stu-id="74373-124">Kernel-mode components that reside between the Network Stack and the filter engine.</span></span> <span data-ttu-id="74373-125">Оболочки делают принятие решений по фильтрации, классифицируются по механизму фильтрации.</span><span class="sxs-lookup"><span data-stu-id="74373-125">Shims make the filtering decision by classifying against the filter engine.</span></span> <span data-ttu-id="74373-126">Ниже приведен список доступных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="74373-126">Following is a list of available shims.</span></span>

-   <span data-ttu-id="74373-127">Оболочка совместимости прикладного уровня (ALE).</span><span class="sxs-lookup"><span data-stu-id="74373-127">Application Layer Enforcement (ALE) shim.</span></span>
-   <span data-ttu-id="74373-128">Оболочка модуля транспортного уровня.</span><span class="sxs-lookup"><span data-stu-id="74373-128">Transport Layer Module shim.</span></span>
-   <span data-ttu-id="74373-129">Оболочка модуля сетевого уровня.</span><span class="sxs-lookup"><span data-stu-id="74373-129">Network Layer Module shim.</span></span>
-   <span data-ttu-id="74373-130">Оболочка ошибок протокола ICMP.</span><span class="sxs-lookup"><span data-stu-id="74373-130">Internet Control Message Protocol (ICMP) Error shim.</span></span>
-   <span data-ttu-id="74373-131">Удалить оболочку совместимости.</span><span class="sxs-lookup"><span data-stu-id="74373-131">Discard shim.</span></span>
-   <span data-ttu-id="74373-132">Оболочка потока.</span><span class="sxs-lookup"><span data-stu-id="74373-132">Stream shim.</span></span>

### <a name="callouts"></a><span data-ttu-id="74373-133">Выноски</span><span class="sxs-lookup"><span data-stu-id="74373-133">Callouts</span></span>

<span data-ttu-id="74373-134">Набор функций, предоставляемых драйвером и используемый для специальной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="74373-134">Set of functions exposed by a driver and used for specialized filtering.</span></span> <span data-ttu-id="74373-135">Помимо основных действий "разрешить" и "блокировать", выноски могут изменять и защищать входящий и исходящий сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="74373-135">Besides the basic actions of "Permit" and "Block", callouts can modify and secure inbound and outbound network traffic.</span></span> <span data-ttu-id="74373-136">Дополнительные сведения о выносках см. в разделе [драйверы выноски платформы фильтрации Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) в документации по Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="74373-136">See the [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) topic in the Windows Driver Kit (WDK) documentation for more information on callouts.</span></span> <span data-ttu-id="74373-137">WFP предоставляет встроенные выноски, которые выполняют следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="74373-137">WFP provides built-in callouts that accomplish the following tasks.</span></span><br/>

-   <span data-ttu-id="74373-138">Выполните обработку IPsec.</span><span class="sxs-lookup"><span data-stu-id="74373-138">Perform IPsec processing.</span></span>
-   <span data-ttu-id="74373-139">Настройте поведение фильтрации с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="74373-139">Adjust stateful filtering behavior.</span></span>
-   <span data-ttu-id="74373-140">Выполняет фильтрацию в скрытом режиме (без уведомления о пакетах, которые не были запрошены).</span><span class="sxs-lookup"><span data-stu-id="74373-140">Perform stealth mode filtering (silent drop of packets that were not requested).</span></span>
-   <span data-ttu-id="74373-141">Управление разгрузкой TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="74373-141">Control TCP chimney offload.</span></span>
-   <span data-ttu-id="74373-142">Взаимодействие со службой Teredo.</span><span class="sxs-lookup"><span data-stu-id="74373-142">Interact with the Teredo service.</span></span>

<br/> <span data-ttu-id="74373-143">Механизм фильтрации позволяет внешним вызовам регистрироваться на каждом из уровней ядра.</span><span class="sxs-lookup"><span data-stu-id="74373-143">The filter engine allows third-party callouts to register at each of its kernel-mode layers.</span></span><br/>

### <a name="application-programming-interface"></a><span data-ttu-id="74373-144">Прикладной программный интерфейс</span><span class="sxs-lookup"><span data-stu-id="74373-144">Application Programming Interface</span></span>

<span data-ttu-id="74373-145">Набор типов данных и функций, доступных разработчикам для создания приложений фильтрации сети и управления ими.</span><span class="sxs-lookup"><span data-stu-id="74373-145">A set of data types and functions available to the developers to build and manage network filtering applications.</span></span> <span data-ttu-id="74373-146">Эти типы данных и функции группируются в несколько [наборов API](api-sets.md).</span><span class="sxs-lookup"><span data-stu-id="74373-146">These data types and functions are grouped into multiple [API sets](api-sets.md).</span></span>

## <a name="wfp-features"></a><span data-ttu-id="74373-147">Функции WFP</span><span class="sxs-lookup"><span data-stu-id="74373-147">WFP Features</span></span>

-   <span data-ttu-id="74373-148">Предоставляет инфраструктуру фильтрации пакетов, в которой независимые поставщики программного обеспечения могут подключаться к специализированным модулям фильтрации.</span><span class="sxs-lookup"><span data-stu-id="74373-148">Provides a packet filtering infrastructure where independent software vendors (ISVs) can plug-in specialized filtering modules.</span></span>
-   <span data-ttu-id="74373-149">Работает с IPv4 и IPv6.</span><span class="sxs-lookup"><span data-stu-id="74373-149">Works with both IPv4 and IPv6.</span></span>
-   <span data-ttu-id="74373-150">Обеспечивает фильтрацию, изменение и повторную вставку данных.</span><span class="sxs-lookup"><span data-stu-id="74373-150">Allows for data filtering, modification, and re-injection.</span></span>
-   <span data-ttu-id="74373-151">Выполняет как пакетную, так и потоковую обработку.</span><span class="sxs-lookup"><span data-stu-id="74373-151">Performs both packet and stream processing.</span></span>
-   <span data-ttu-id="74373-152">Позволяет включить фильтрацию пакетов для каждого приложения, для каждого пользователя и для каждого подключения в дополнение к сетевому интерфейсу или по каждому порту.</span><span class="sxs-lookup"><span data-stu-id="74373-152">Allows packet filtering to be enabled per application, per user, and per connection in addition to per network interface or per port.</span></span>
-   <span data-ttu-id="74373-153">Обеспечивает безопасность во время загрузки до запуска модуля базовой фильтрации (BFE).</span><span class="sxs-lookup"><span data-stu-id="74373-153">Provides boot-time security until Base Filtering Engine (BFE) can start.</span></span>
-   <span data-ttu-id="74373-154">Включает фильтрацию подключений с отслеживанием состояния.</span><span class="sxs-lookup"><span data-stu-id="74373-154">Enables stateful connection filtering.</span></span>
-   <span data-ttu-id="74373-155">Обрабатывает как предварительные, так и POST-шифрованные данные IPsec.</span><span class="sxs-lookup"><span data-stu-id="74373-155">Handles both pre and post IPsec-encrypted data.</span></span>
-   <span data-ttu-id="74373-156">Позволяет интегрировать политики фильтрации IPsec и брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="74373-156">Allows integration of IPsec and firewall filtering policies.</span></span>
-   <span data-ttu-id="74373-157">Предоставляет инфраструктуру управления политиками, позволяющую определить, когда должны быть активированы определенные фильтры.</span><span class="sxs-lookup"><span data-stu-id="74373-157">Provides a policy management infrastructure to determine when specific filters should be activated.</span></span> <span data-ttu-id="74373-158">Сюда входят обрабатывают конфликтные требования из нескольких фильтров, предоставляемых разными поставщиками.</span><span class="sxs-lookup"><span data-stu-id="74373-158">This includes mediating conflicting requirements from multiple filters provided by different vendors.</span></span>
-   <span data-ttu-id="74373-159">Обрабатывает большую часть пересборки и отслеживания состояния пакетов.</span><span class="sxs-lookup"><span data-stu-id="74373-159">Handles most packet reassembly and state tracking.</span></span>
-   <span data-ttu-id="74373-160">Включает универсальную систему уведомлений пользователей, которая информирует подписчиков об изменениях в системе фильтрации.</span><span class="sxs-lookup"><span data-stu-id="74373-160">Includes a generic user notification system that informs subscribers of changes to the filtering system.</span></span>
-   <span data-ttu-id="74373-161">Реализует функции перечисления, которые сообщают о состоянии системы.</span><span class="sxs-lookup"><span data-stu-id="74373-161">Implements enumeration functions that report on the state of the system.</span></span>
-   <span data-ttu-id="74373-162">Использует события NET для записи ошибок IPsec и перепадения пакетов.</span><span class="sxs-lookup"><span data-stu-id="74373-162">Uses net events to record IPsec errors and packet drops.</span></span>
-   <span data-ttu-id="74373-163">Поддерживает класс поддержки среды диагностики сети [(NDF)](/windows/desktop/NDF/extensible-helper-classes).</span><span class="sxs-lookup"><span data-stu-id="74373-163">Supports a Network Diagnostics Framework [(NDF) helper class](/windows/desktop/NDF/extensible-helper-classes).</span></span>
-   <span data-ttu-id="74373-164">Поддерживает [безопасные расширения сокетов](/windows/desktop/WinSock/winsock-secure-socket-extensions) для API Winsock, которые позволяют сетевым приложениям защищать трафик путем настройки WFP.</span><span class="sxs-lookup"><span data-stu-id="74373-164">Supports the [Secure Socket extensions](/windows/desktop/WinSock/winsock-secure-socket-extensions) to the Winsock API, which allow network applications to secure their traffic by configuring WFP.</span></span>
-   <span data-ttu-id="74373-165">На уровнях применения уровня приложения (ALE) минимальное влияние на производительность сети за счет обработки только первого пакета в соединении.</span><span class="sxs-lookup"><span data-stu-id="74373-165">At Application Layer Enforcement (ALE) layers, minimally impacts network performance by processing only the first packet in a connection.</span></span>
-   <span data-ttu-id="74373-166">Интегрирует аппаратную разгрузку, где модули выноски в режиме ядра могут использовать оборудование для выполнения определенной проверки пакетов.</span><span class="sxs-lookup"><span data-stu-id="74373-166">Integrates hardware offload where kernel-mode callout modules can use hardware to perform specific packet inspection.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74373-167">См. также</span><span class="sxs-lookup"><span data-stu-id="74373-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74373-168">Архитектура WFP</span><span class="sxs-lookup"><span data-stu-id="74373-168">WFP Architecture</span></span>](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[<span data-ttu-id="74373-169">Операция WFP</span><span class="sxs-lookup"><span data-stu-id="74373-169">WFP Operation</span></span>](basic-operation.md)
</dt> <dt>

[<span data-ttu-id="74373-170">Принудительное применение уровня приложения (ALE)</span><span class="sxs-lookup"><span data-stu-id="74373-170">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="74373-171">Конфигурация IPsec</span><span class="sxs-lookup"><span data-stu-id="74373-171">IPsec Configuration</span></span>](ipsec-configuration.md)
</dt> <dt>

[<span data-ttu-id="74373-172">Конфигурация WFP</span><span class="sxs-lookup"><span data-stu-id="74373-172">WFP Configuration</span></span>](wfp-configuration.md)
</dt> <dt>

[<span data-ttu-id="74373-173">Мониторинг WFP</span><span class="sxs-lookup"><span data-stu-id="74373-173">WFP Monitoring</span></span>](wfp-monitoring.md)
</dt> <dt>

[<span data-ttu-id="74373-174">API WFP</span><span class="sxs-lookup"><span data-stu-id="74373-174">WFP API</span></span>](api-sets.md)
</dt> </dl>

 

