---
description: WMI автоматически сопоставляет SNMP-ловушки с событиями WMI. Система помещает данные, содержащиеся в ловушке, в соответствующие свойства экземпляра события WMI для доступа хост-компьютера WMI.
ms.assetid: 549f58a9-9d3b-41b9-a374-ab83877f63a7
ms.tgt_platform: multiple
title: Получение ловушек SNMP как событий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da24be8ea9a4882af0b961b1d0f6f0c3d442c70c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544703"
---
# <a name="receiving-snmp-traps-as-wmi-events"></a><span data-ttu-id="d0b70-104">Получение ловушек SNMP как событий WMI</span><span class="sxs-lookup"><span data-stu-id="d0b70-104">Receiving SNMP Traps as WMI Events</span></span>

<span data-ttu-id="d0b70-105">WMI автоматически сопоставляет SNMP-ловушки с событиями WMI.</span><span class="sxs-lookup"><span data-stu-id="d0b70-105">WMI automatically maps SNMP traps to WMI events.</span></span> <span data-ttu-id="d0b70-106">Система помещает данные, содержащиеся в ловушке, в соответствующие свойства экземпляра события WMI для доступа хост-компьютера WMI.</span><span class="sxs-lookup"><span data-stu-id="d0b70-106">The system places the data contained in the trap in the corresponding properties of a WMI event instance for access by the WMI host machine.</span></span>

> [!Note]  
> <span data-ttu-id="d0b70-107">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d0b70-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="d0b70-108">Получение SNMP-ловушки практически идентично получению событий от любого другого поставщика WMI.</span><span class="sxs-lookup"><span data-stu-id="d0b70-108">Receiving an SNMP trap is nearly identical to receiving events from any other WMI provider.</span></span> <span data-ttu-id="d0b70-109">Однако фильтр событий SNMP имеет несколько уникальных классов, которые следует учитывать перед регистрацией для событий.</span><span class="sxs-lookup"><span data-stu-id="d0b70-109">However, the SNMP event filter has several unique classes to be aware of before registering for events.</span></span> <span data-ttu-id="d0b70-110">Кроме того, поставщик событий требует \\ исключительного использования пространства имен Смир.</span><span class="sxs-lookup"><span data-stu-id="d0b70-110">Also, the event provider requires the use of the \\smir namespace exclusively.</span></span>

<span data-ttu-id="d0b70-111">Наиболее распространенными классами для регистрации являются [снмпнотификатион](snmpnotification.md) и [снмпекстендеднотификатион](snmpextendednotification.md).</span><span class="sxs-lookup"><span data-stu-id="d0b70-111">The most common classes to register with are [SnmpNotification](snmpnotification.md) and [SnmpExtendedNotification](snmpextendednotification.md).</span></span> <span data-ttu-id="d0b70-112">Потребители, намеренные использовать уведомления о событиях для обновления значений в отслеживаемых SNMP-устройствах, должны регистрироваться для событий Снмпекстендеднотификатион.</span><span class="sxs-lookup"><span data-stu-id="d0b70-112">Consumers intent on using event notifications to update values in monitored SNMP devices must register for SnmpExtendedNotification events.</span></span> <span data-ttu-id="d0b70-113">Сведения из событий Снмпнотификатион нельзя использовать повторно.</span><span class="sxs-lookup"><span data-stu-id="d0b70-113">The information from SnmpNotification events is not reusable.</span></span>

<span data-ttu-id="d0b70-114">В следующей таблице приведены сведения о настройке компьютера для получения ловушек SNMP в виде событий WMI.</span><span class="sxs-lookup"><span data-stu-id="d0b70-114">The following table lists information about setting up your computer to receive SNMP traps as WMI events.</span></span>



| <span data-ttu-id="d0b70-115">Задача</span><span class="sxs-lookup"><span data-stu-id="d0b70-115">Task</span></span>                                                                               | <span data-ttu-id="d0b70-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d0b70-116">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0b70-117">Выбор поставщиков событий SNMP</span><span class="sxs-lookup"><span data-stu-id="d0b70-117">Choosing Between SNMP Event Providers</span></span>](choosing-between-snmp-event-providers.md) | <span data-ttu-id="d0b70-118">WMI включает два поставщика событий SNMP.</span><span class="sxs-lookup"><span data-stu-id="d0b70-118">WMI includes two SNMP event providers.</span></span>                                             |
| [<span data-ttu-id="d0b70-119">Получение событий SNMP</span><span class="sxs-lookup"><span data-stu-id="d0b70-119">Receiving SNMP Events</span></span>](receiving-snmp-events.md)                                 | <span data-ttu-id="d0b70-120">Поставщики событий SNMP поддерживают три типа уведомлений о ловушках и SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="d0b70-120">SNMP event providers support three types of SNMPv1 traps and SNMPv2 notifications.</span></span> |



 

<span data-ttu-id="d0b70-121">В следующем примере настраивается компьютер для отслеживания события **снмплинкупнотификатион** из управляемого центра.</span><span class="sxs-lookup"><span data-stu-id="d0b70-121">The following example sets up a computer to monitor for the **SnmpLinkUpNotification** event from a managed hub.</span></span>


```VB
Set objLocator = CreateObject("wbemscripting.swbemlocator")
Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")

set objwbemEventsource = _ 
    objServices.ExecNotificationQuery _
   ("SELECT * FROM SnmpLinkUpNotification")

set objWbemObject = objwbemEventsource.NextEvent()

wscript.echo "Received " & objWbemObject.path_.class

for each prop in objWbemObject.properties_
    wscript.echo prop.name & " -- " & prop.value
next
```



 

 



