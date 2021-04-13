---
description: Доступ к SNMP-устройствам можно получить с помощью чтения или записи в соответствующий экземпляр класса в Смир WMI (репозиторий сведений о модуле SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Чтение и запись на SNMP-устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544831"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Чтение и запись на SNMP-устройства

Доступ к SNMP-устройствам можно получить с помощью чтения или записи в соответствующий экземпляр класса в Смир WMI (репозиторий сведений о модуле SNMP). При работе с несколькими устройствами одного типа для повышения эффективности Загрузите MIB для одного типа SNMP-устройства в Смир.

> [!Note]  
> Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Выберите один из следующих параметров для чтения или записи из каждого типа SNMP-устройства, обновив сведения о контексте экземпляра, прежде чем взаимодействовать с каждым из них.

-   Используйте DNS-имя вместо IP-адреса при ссылке на конкретное устройство.

    В следующем примере показано, как использовать DNS-имя для конкретного устройства.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Создайте отдельное пространство имен и свяжите адрес устройства с объектом пространства имен с помощью квалификатора экземпляра Ажентаддресс, чтобы пространство имен было постоянно привязано к устройству. В этом случае не нужно указывать сведения об объекте контекста.
-   Чтение с SNMP-устройства.

    В следующем примере выполняется операция Get для класса устройства.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   Запись на SNMP-устройство.

    В следующем примере выполняется операция Set для класса устройства.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Коррелированные классы — это те, которые поддерживаются данным устройством SNMP при перечислении. Корреляция влияет на набор классов, возвращаемых из Смир. Некоррелированное перечисление возвращает все классы, находящиеся в Смир, независимо от того, поддерживает ли устройство их. Дополнительные сведения об использовании методов корреляции WMI см. в разделе [корреляция классов SNMP WMI](wmi-snmp-class-correlation.md).

 

 



