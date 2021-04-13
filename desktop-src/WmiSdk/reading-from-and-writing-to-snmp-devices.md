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
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="56575-103">Чтение и запись на SNMP-устройства</span><span class="sxs-lookup"><span data-stu-id="56575-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="56575-104">Доступ к SNMP-устройствам можно получить с помощью чтения или записи в соответствующий экземпляр класса в Смир WMI (репозиторий сведений о модуле SNMP).</span><span class="sxs-lookup"><span data-stu-id="56575-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="56575-105">При работе с несколькими устройствами одного типа для повышения эффективности Загрузите MIB для одного типа SNMP-устройства в Смир.</span><span class="sxs-lookup"><span data-stu-id="56575-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="56575-106">Дополнительные сведения об установке поставщика см. в разделе [Настройка среды SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="56575-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="56575-107">Выберите один из следующих параметров для чтения или записи из каждого типа SNMP-устройства, обновив сведения о контексте экземпляра, прежде чем взаимодействовать с каждым из них.</span><span class="sxs-lookup"><span data-stu-id="56575-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="56575-108">Используйте DNS-имя вместо IP-адреса при ссылке на конкретное устройство.</span><span class="sxs-lookup"><span data-stu-id="56575-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="56575-109">В следующем примере показано, как использовать DNS-имя для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="56575-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="56575-110">Создайте отдельное пространство имен и свяжите адрес устройства с объектом пространства имен с помощью квалификатора экземпляра Ажентаддресс, чтобы пространство имен было постоянно привязано к устройству.</span><span class="sxs-lookup"><span data-stu-id="56575-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="56575-111">В этом случае не нужно указывать сведения об объекте контекста.</span><span class="sxs-lookup"><span data-stu-id="56575-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="56575-112">Чтение с SNMP-устройства.</span><span class="sxs-lookup"><span data-stu-id="56575-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="56575-113">В следующем примере выполняется операция Get для класса устройства.</span><span class="sxs-lookup"><span data-stu-id="56575-113">The following example performs a Get operation on a device class.</span></span>

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

    

-   <span data-ttu-id="56575-114">Запись на SNMP-устройство.</span><span class="sxs-lookup"><span data-stu-id="56575-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="56575-115">В следующем примере выполняется операция Set для класса устройства.</span><span class="sxs-lookup"><span data-stu-id="56575-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="56575-116">Коррелированные классы — это те, которые поддерживаются данным устройством SNMP при перечислении.</span><span class="sxs-lookup"><span data-stu-id="56575-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="56575-117">Корреляция влияет на набор классов, возвращаемых из Смир.</span><span class="sxs-lookup"><span data-stu-id="56575-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="56575-118">Некоррелированное перечисление возвращает все классы, находящиеся в Смир, независимо от того, поддерживает ли устройство их.</span><span class="sxs-lookup"><span data-stu-id="56575-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="56575-119">Дополнительные сведения об использовании методов корреляции WMI см. в разделе [корреляция классов SNMP WMI](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="56575-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



