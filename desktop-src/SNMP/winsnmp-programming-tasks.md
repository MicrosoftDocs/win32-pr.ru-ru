---
title: Задачи WinSNMP программирования
description: В следующей таблице перечислены основные процедуры программирования, которые необходимо выполнить для создания кода для приложения WinSNMP, а также разделы, содержащие сведения об этих задачах.
ms.assetid: 70c24042-bf44-4484-8e5e-d117e2ba28d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75fa8d2ad223fbd8f71eff78c7cd232ddc492a9
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "103890215"
---
# <a name="winsnmp-programming-tasks"></a><span data-ttu-id="bb421-103">Задачи WinSNMP программирования</span><span class="sxs-lookup"><span data-stu-id="bb421-103">WinSNMP Programming Tasks</span></span>

<span data-ttu-id="bb421-104">В следующей таблице перечислены основные процедуры программирования, которые необходимо выполнить для создания кода для приложения WinSNMP, а также разделы, содержащие сведения об этих задачах.</span><span class="sxs-lookup"><span data-stu-id="bb421-104">The following table summarizes the basic programming procedures that you must perform to code a WinSNMP application, and the topics that provide information about these tasks.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb421-105">Задача программирования</span><span class="sxs-lookup"><span data-stu-id="bb421-105">Programming task</span></span></th>
<th><span data-ttu-id="bb421-106">Функции и разделы, связанные с задачами</span><span class="sxs-lookup"><span data-stu-id="bb421-106">Task-related function and topics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bb421-107">Откройте приложение WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-107">Open the WinSNMP application.</span></span></td>
<td><span data-ttu-id="bb421-108">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>снмпстартуп</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-108">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup"><strong>SnmpStartup</strong></a>.</span></span> <span data-ttu-id="bb421-109">См. раздел <a href="opening-and-closing-a-winsnmp-application.md">Открытие и закрытие приложения WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-109">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb421-110">Откройте один или несколько сеансов WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-110">Open one or more WinSNMP sessions.</span></span></td>
<td><span data-ttu-id="bb421-111">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>снмпкреатесессион</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-111">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession"><strong>SnmpCreateSession</strong></a>.</span></span> <span data-ttu-id="bb421-112">См. раздел <a href="opening-and-closing-a-winsnmp-session.md">Открытие и закрытие сеанса WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-112">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb421-113">Зарегистрируйтесь для получения ловушек или уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bb421-113">Register to receive traps or notifications.</span></span></td>
<td><span data-ttu-id="bb421-114">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>снмпрегистер</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-114">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister"><strong>SnmpRegister</strong></a>.</span></span> <span data-ttu-id="bb421-115">См. раздел <a href="managing-traps-and-notifications.md">Управление ловушками и уведомлениями</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-115">See <a href="managing-traps-and-notifications.md">Managing Traps and Notifications</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb421-116">Создайте один или несколько списков привязок переменных для Организации в PDU.</span><span class="sxs-lookup"><span data-stu-id="bb421-116">Create one or more variable binding lists for incorporation in a PDU.</span></span></td>
<td><span data-ttu-id="bb421-117">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>снмпкреатевбл</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>снмпдупликатевбл</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>снмпсетвб</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-117">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatevbl"><strong>SnmpCreateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatevbl"><strong>SnmpDuplicateVbl</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetvb"><strong>SnmpSetVb</strong></a>.</span></span> <span data-ttu-id="bb421-118">См. раздел <a href="working-with-variable-binding-lists.md">Работа с списками привязок переменных</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-118">See <a href="working-with-variable-binding-lists.md">Working with Variable Binding Lists</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bb421-119">Приложению может потребоваться вызвать другие <a href="winsnmp-functions.md">функции привязки переменных</a> для создания списка привязок переменных.</span><span class="sxs-lookup"><span data-stu-id="bb421-119">The application may need to call other <a href="winsnmp-functions.md">variable binding functions</a> to create the variable binding list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb421-120">Создайте одно или несколько устройств PDU для передачи и обработки.</span><span class="sxs-lookup"><span data-stu-id="bb421-120">Create one or more PDUs for transmission and processing.</span></span></td>
<td><span data-ttu-id="bb421-121">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>снмпкреатепду</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>снмпсетпдудата</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>снмпдупликатепду</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-121">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu"><strong>SnmpCreatePDU</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata"><strong>SnmpSetPduData</strong></a>, <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpduplicatepdu"><strong>SnmpDuplicatePDU</strong></a>.</span></span> <span data-ttu-id="bb421-122">См. раздел <a href="working-with-protocol-data-units.md">Работа с единицами данных протокола</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-122">See <a href="working-with-protocol-data-units.md">Working with Protocol Data Units</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="bb421-123">Приложению может потребоваться вызвать другие <a href="winsnmp-functions.md">функции PDU</a> и <a href="winsnmp-functions.md">функции WinSNMP Utility</a> для создания PDU.</span><span class="sxs-lookup"><span data-stu-id="bb421-123">The application may need to call other <a href="winsnmp-functions.md">PDU functions</a> and WinSNMP <a href="winsnmp-functions.md">utility functions</a> to create the PDU.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb421-124">Отправьте один или несколько запросов на операции SNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-124">Submit one or more SNMP operation requests.</span></span></td>
<td><span data-ttu-id="bb421-125">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>снмпсендмсг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-125">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg"><strong>SnmpSendMsg</strong></a>.</span></span> <span data-ttu-id="bb421-126">См. раздел <a href="sending-snmp-messages.md">Отправка SNMP-сообщений</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-126">See <a href="sending-snmp-messages.md">Sending SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb421-127">Получите ответ на запрос операции SNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-127">Retrieve the response to the SNMP operation request.</span></span></td>
<td><span data-ttu-id="bb421-128">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>снмпреквмсг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-128">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg"><strong>SnmpRecvMsg</strong></a>.</span></span> <span data-ttu-id="bb421-129">См. раздел <a href="receiving-snmp-messages.md">Получение SNMP-сообщений</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-129">See <a href="receiving-snmp-messages.md">Receiving SNMP Messages</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb421-130">Обработка ответа на запрос.</span><span class="sxs-lookup"><span data-stu-id="bb421-130">Process the request response.</span></span></td>
<td><span data-ttu-id="bb421-131">Используйте логику конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="bb421-131">Use application-specific logic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bb421-132">Закройте каждый сеанс WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-132">Close each WinSNMP session.</span></span></td>
<td><span data-ttu-id="bb421-133">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>снмпклосе</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-133">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose"><strong>SnmpClose</strong></a>.</span></span> <span data-ttu-id="bb421-134">См. раздел <a href="opening-and-closing-a-winsnmp-session.md">Открытие и закрытие сеанса WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-134">See <a href="opening-and-closing-a-winsnmp-session.md">Opening and Closing a WinSNMP Session</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bb421-135">Закройте приложение WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-135">Close the WinSNMP application.</span></span></td>
<td><span data-ttu-id="bb421-136">Используйте <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>снмпклеануп</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-136">Use <a href="/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup"><strong>SnmpCleanup</strong></a>.</span></span> <span data-ttu-id="bb421-137">См. раздел <a href="opening-and-closing-a-winsnmp-application.md">Открытие и закрытие приложения WinSNMP</a>.</span><span class="sxs-lookup"><span data-stu-id="bb421-137">See <a href="opening-and-closing-a-winsnmp-application.md">Opening and Closing a WinSNMP Application</a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bb421-138">Следующие разделы содержат дополнительные сведения о других общих концепциях программирования, характерных для среды WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-138">The following topics contain additional information about other general programming concepts specific to the WinSNMP environment.</span></span>



|                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb421-139">Общие задачи программирования</span><span class="sxs-lookup"><span data-stu-id="bb421-139">General programming tasks</span></span>](general-winsnmp-programming-tasks.md) | <span data-ttu-id="bb421-140">[Управление идентификаторами объектов](managing-object-identifiers.md)[освобождение дескрипторов WinSNMP](freeing-winsnmp-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="bb421-140">[Managing Object Identifiers](managing-object-identifiers.md)[Freeing WinSNMP Descriptors](freeing-winsnmp-descriptors.md)</span></span><br/> [<span data-ttu-id="bb421-141">Настройка режима преобразования объектов и контекста</span><span class="sxs-lookup"><span data-stu-id="bb421-141">Setting the Entity and Context Translation Mode</span></span>](setting-the-entity-and-context-translation-mode.md)<br/> [<span data-ttu-id="bb421-142">Управление политикой повторной передачи</span><span class="sxs-lookup"><span data-stu-id="bb421-142">Managing the Retransmission Policy</span></span>](managing-the-retransmission-policy.md)<br/> [<span data-ttu-id="bb421-143">Создание WinSNMP Applications с несколькими потоками</span><span class="sxs-lookup"><span data-stu-id="bb421-143">Writing WinSNMP Applications with Multiple Threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)<br/> [<span data-ttu-id="bb421-144">Регистрация приложения агента SNMP</span><span class="sxs-lookup"><span data-stu-id="bb421-144">Registering an SNMP Agent Application</span></span>](registering-an-snmp-agent-application.md)<br/> |



 

<span data-ttu-id="bb421-145">Кроме того, приложению WinSNMP может потребоваться включить вызовы следующих функций WinSNMP: [**снмпфривбл**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**снмпфриентити**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**снмпфридескриптор**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**снмпфриконтекст**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext)и [**снмпфрипду**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span><span class="sxs-lookup"><span data-stu-id="bb421-145">In addition, the WinSNMP application may need to incorporate calls to the following WinSNMP functions: [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity), [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext), and [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu).</span></span> <span data-ttu-id="bb421-146">Это позволяет реализации Microsoft WinSNMP освобождать объекты WinSNMP Memory.</span><span class="sxs-lookup"><span data-stu-id="bb421-146">This enables the Microsoft WinSNMP implementation to free WinSNMP memory objects.</span></span> <span data-ttu-id="bb421-147">Как правило, приложение WinSNMP должно освобождать все ресурсы, выделенные в результате вызова функции WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="bb421-147">As a general rule, the WinSNMP application should free all resources allocated as the result of a call to a WinSNMP function.</span></span> <span data-ttu-id="bb421-148">Дополнительные сведения о освобождении ресурсов см. в разделе [выделение объектов WinSNMP Memory](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bb421-148">For additional information about deallocating resources, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 





