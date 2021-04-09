---
title: Структуры API службы удаленных рабочих столов
description: Содержит структуры, используемые с API службы удаленных рабочих столов.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104133923"
---
# <a name="remote-desktop-services-api-structures"></a><span data-ttu-id="0f3b7-103">Структуры API службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="0f3b7-103">Remote Desktop Services API Structures</span></span>

<span data-ttu-id="0f3b7-104">С службы удаленных рабочих столов API используются следующие структуры.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-104">The following structures are used with the Remote Desktop Services API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0f3b7-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="0f3b7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="0f3b7-106">**DEF по КАНАЛу \_**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-106">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

<span data-ttu-id="0f3b7-107">Содержит имя и параметры виртуального канала службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-107">Contains the name and options of a Remote Desktop Services virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-108">**\_точки входа \_ каналов**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-108">**CHANNEL\_ENTRY\_POINTS**</span></span>](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

<span data-ttu-id="0f3b7-109">Содержит указатели на функции, вызываемые клиентской библиотекой DLL для доступа к виртуальным каналам.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-109">Contains pointers to the functions called by a client-side DLL to access virtual channels.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-110">**\_заголовок канала PDU \_**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-110">**CHANNEL\_PDU\_HEADER**</span></span>](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

<span data-ttu-id="0f3b7-111">Содержит сведения о блоке данных, получаемом серверным концом виртуального канала.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-111">Contains information about a data block being received by the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-112">**лскэйпакк**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-112">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dd>

<span data-ttu-id="0f3b7-113">Содержит сведения о конкретном пакете лицензионных ключей службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-113">Contains information about a specific Remote Desktop Services licensing key pack.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-114">**лслиценсе**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-114">**LSLicense**</span></span>](lslicense.md)
</dt> <dd>

<span data-ttu-id="0f3b7-115">Содержит сведения о конкретной лицензии службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-115">Contains information about a specific Remote Desktop Services license.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-116">**втсклиент**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-116">**WTSCLIENT**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

<span data-ttu-id="0f3b7-117">Содержит сведения о клиенте подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-117">Contains information about a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-118">**втсконфигинфо**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-118">**WTSCONFIGINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

<span data-ttu-id="0f3b7-119">Содержит сведения о службы удаленных рабочих столов сеансе.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-119">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-120">**втсинфо**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-120">**WTSINFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

<span data-ttu-id="0f3b7-121">Содержит сведения о службы удаленных рабочих столов сеансе.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-121">Contains information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-122">**втсинфоекс**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-122">**WTSINFOEX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

<span data-ttu-id="0f3b7-123">Содержит [**втсинфоекс на \_ уровне**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) объединения, который содержит расширенные сведения о сеансе службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-123">Contains a [**WTSINFOEX\_LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) union that contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-124">**ВТСИНФОЕКС \_ level1**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-124">**WTSINFOEX\_LEVEL1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

<span data-ttu-id="0f3b7-125">Содержит расширенные сведения о службы удаленных рабочих столов сеансе.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-125">Contains extended information about a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-126">**втслистенерконфиг**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-126">**WTSLISTENERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

<span data-ttu-id="0f3b7-127">Содержит сведения о прослушивателе службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-127">Contains information about a Remote Desktop Services listener.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-128">**ВТССБКС \_ IP- \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-128">**WTSSBX\_IP\_ADDRESS**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

<span data-ttu-id="0f3b7-129">Содержит сведения о IP-адресе сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-129">Contains information about the IP address of a network resource.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-130">**\_ \_ сведения о подключении к втссбкс машине \_**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-130">**WTSSBX\_MACHINE\_CONNECT\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

<span data-ttu-id="0f3b7-131">Содержит сведения о компьютере, принимающем удаленные подключения.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-131">Contains information about a computer that is accepting remote connections.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-132">**\_ \_ сведения о компьютере втссбкс**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-132">**WTSSBX\_MACHINE\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

<span data-ttu-id="0f3b7-133">Содержит сведения о компьютере и его текущем состоянии.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-133">Contains information about a computer and its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-134">**\_сведения о сеансе втссбкс \_**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-134">**WTSSBX\_SESSION\_INFO**</span></span>](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

<span data-ttu-id="0f3b7-135">Содержит сведения о сеансах, доступных для подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-135">Contains information about sessions that are available to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-136">**\_уведомление втссессион**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-136">**WTSSESSION\_NOTIFICATION**</span></span>](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

<span data-ttu-id="0f3b7-137">Предоставляет сведения о уведомлении об изменении сеанса.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-137">Provides information about the session change notification.</span></span> <span data-ttu-id="0f3b7-138">Служба получает эту структуру в своей функции [*хандлерекс*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) в ответ на событие изменения сеанса.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-138">A service receives this structure in its [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) function in response to a session change event.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-139">**втсусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-139">**WTSUSERCONFIG**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

<span data-ttu-id="0f3b7-140">Содержит сведения о конфигурации пользователя на контроллере домена или на сервере узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-140">Contains configuration information for a user on a domain controller or Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-141">**\_адрес клиента \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-141">**WTS\_CLIENT\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

<span data-ttu-id="0f3b7-142">Содержит сетевой адрес клиента службы удаленных рабочих столов сеанса.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-142">Contains the client network address of a Remote Desktop Services session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-143">**\_Отображение клиента \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-143">**WTS\_CLIENT\_DISPLAY**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

<span data-ttu-id="0f3b7-144">Содержит сведения о дисплее клиента подключение к удаленному рабочему столу (RDC).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-144">Contains information about the display of a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-145">**\_ \_ сведения о процессе ВТС**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-145">**WTS\_PROCESS\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

<span data-ttu-id="0f3b7-146">Содержит сведения о процессе, выполняющемся на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-146">Contains information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-147">**\_сведения о процессе ВТС, \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-147">**WTS\_PROCESS\_INFO\_EX**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

<span data-ttu-id="0f3b7-148">Содержит расширенные сведения о процессе, работающем на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-148">Contains extended information about a process running on a RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="0f3b7-149">[**\_ \_ сведения о продукте ВТС**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0f3b7-149">[**WTS\_PRODUCT\_INFO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)</span></span>
</dt> <dd>

<span data-ttu-id="0f3b7-150">Сведения о лицензии продукта, необходимой для подключения к серверу терминалов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-150">The details of the product license that is required to connect to a terminal server.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-151">**\_ \_ сведения о сервере ВТС**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-151">**WTS\_SERVER\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

<span data-ttu-id="0f3b7-152">Содержит сведения о конкретном сервере службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-152">Contains information about a specific Remote Desktop Services server.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-153">**\_адрес сеанса \_ ВТС**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-153">**WTS\_SESSION\_ADDRESS**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

<span data-ttu-id="0f3b7-154">Содержит виртуальный IP-адрес, назначенный сеансу.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-154">Contains the virtual IP address assigned to a session.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-155">**\_сведения о сеансе ВТС \_**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-155">**WTS\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

<span data-ttu-id="0f3b7-156">Содержит сведения о клиентском сеансе на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0f3b7-156">Contains information about a client session on a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="0f3b7-157">**\_Сведения о сеансе ВТС \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="0f3b7-157">**WTS\_SESSION\_INFO\_1**</span></span>](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

<span data-ttu-id="0f3b7-158">Содержит расширенные сведения о клиентском сеансе на сервере узла сеансов удаленных рабочих столов или на сервере узла виртуализации удаленных рабочих столов (Узел виртуализации удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="0f3b7-158">Contains extended information about a client session on a RD Session Host server or Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

</dd> </dl>

 

 