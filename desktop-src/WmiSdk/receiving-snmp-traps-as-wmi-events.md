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
# <a name="receiving-snmp-traps-as-wmi-events"></a>Получение ловушек SNMP как событий WMI

WMI автоматически сопоставляет SNMP-ловушки с событиями WMI. Система помещает данные, содержащиеся в ловушке, в соответствующие свойства экземпляра события WMI для доступа хост-компьютера WMI.

> [!Note]  
> Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Получение SNMP-ловушки практически идентично получению событий от любого другого поставщика WMI. Однако фильтр событий SNMP имеет несколько уникальных классов, которые следует учитывать перед регистрацией для событий. Кроме того, поставщик событий требует \\ исключительного использования пространства имен Смир.

Наиболее распространенными классами для регистрации являются [снмпнотификатион](snmpnotification.md) и [снмпекстендеднотификатион](snmpextendednotification.md). Потребители, намеренные использовать уведомления о событиях для обновления значений в отслеживаемых SNMP-устройствах, должны регистрироваться для событий Снмпекстендеднотификатион. Сведения из событий Снмпнотификатион нельзя использовать повторно.

В следующей таблице приведены сведения о настройке компьютера для получения ловушек SNMP в виде событий WMI.



| Задача                                                                               | Описание                                                                        |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [Выбор поставщиков событий SNMP](choosing-between-snmp-event-providers.md) | WMI включает два поставщика событий SNMP.                                             |
| [Получение событий SNMP](receiving-snmp-events.md)                                 | Поставщики событий SNMP поддерживают три типа уведомлений о ловушках и SNMPv2. |



 

В следующем примере настраивается компьютер для отслеживания события **снмплинкупнотификатион** из управляемого центра.


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



 

 



