---
title: Вызов метода WMI
description: Основной целью инструментария WMI является предоставление доступа к классам и экземплярам, представляющим объекты в сети.
ms.assetid: 8d559eee-3dbf-4132-b1c0-a6925b8feb56
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 892561785280e78ecf29da1030883994990fc822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546098"
---
# <a name="how-to-call-a-wmi-method"></a>Вызов метода WMI

Основной целью инструментария WMI является предоставление доступа к классам и экземплярам, представляющим объекты в сети. Эти классы и экземпляры поддерживаются поставщиками. Например, все экземпляры, представляющие стандартные аппаратные устройства на предприятии, такие как [**Win32 \_ фисикалмемори**](/windows/desktop/CIMWin32Prov/win32-physicalmemory) или [**\_ принтер Win32**](/windows/desktop/CIMWin32Prov/win32-printer), поддерживаются поставщиком Win32. Аналогичным образом, доступ к журналу событий можно получить с помощью регистратора событий и реестра с помощью поставщика реестра.

Методы, реализуемые WMI в интерфейсах, таких как [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) или объекты скриптов, такие как [**SwbemServices**](swbemservices.md), в основном используются для универсального получения данных, предоставляемых любым поставщиком, и управления ими. Например, используйте [**SwbemServices. инстанцесоф**](swbemservices-instancesof.md) для получения всех экземпляров [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process) в подмножестве компьютеров предприятия. Затем можно вызвать метод поставщика Win32 [**жетовнерсид**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) для каждого объекта **\_ процесса Win32** .

В следующем примере метод [**жетовнерсид**](/windows/desktop/CIMWin32Prov/getownersid-method-in-class-win32-process) вызывается как метод автоматизации для объекта Process. Метод WMI, например метод [**\_ path**](swbemobject-path-.md) , определенный для [**SWbemObject**](swbemobject.md) , также может вызываться для объекта **Process** .


```VB
Set ProcessCollection = _
    GetObject("WinMgmts:").InstancesOf("Win32_Process")

For Each Process In ProcessCollection
    SID = Process.GetOwnerSid
Next
```



Фактический процесс использования методов WMI идентичен использованию любых других интерфейсов COM или интерфейса автоматизации Windows. Дополнительные сведения см. в разделе [com](../cossdk/component-services-portal.md) и [Создание приложения или скрипта WMI](creating-a-wmi-application-or-script.md). Дополнительные сведения о интерфейсах, поддерживаемых WMI, см. в разделе [API COM для WMI](com-api-for-wmi.md) и [API сценариев для WMI](scripting-api-for-wmi.md).

Дополнительные сведения см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Вызов метода](calling-a-method.md)
</dt> </dl>

 

 
