---
description: Представляет возможности \_ объекта ВИРТУАЛСИСТЕММИГРАТИОНСЕРВИЦЕ CIM.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: Класс CIM_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545218"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="30177-103">\_Класс CIM виртуалсистеммигратионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="30177-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="30177-104">Представляет возможности объекта [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="30177-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="30177-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30177-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="30177-106">Члены</span><span class="sxs-lookup"><span data-stu-id="30177-106">Members</span></span>

<span data-ttu-id="30177-107">Класс **CIM \_ виртуалсистеммигратионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="30177-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="30177-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="30177-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30177-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="30177-109">Properties</span></span>

<span data-ttu-id="30177-110">Класс **CIM \_ виртуалсистеммигратионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="30177-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30177-111">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="30177-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30177-112">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="30177-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="30177-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30177-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30177-114">Массив, указывающий методы [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) , которые поддерживаются для асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="30177-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="30177-115">**Мигратевиртуалсистемтохостсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="30177-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="30177-116">**Мигратевиртуалсистемтосистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="30177-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="30177-117">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="30177-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="30177-118">**дестинатионхостформатссуппортед**</span><span class="sxs-lookup"><span data-stu-id="30177-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30177-119">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="30177-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="30177-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30177-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30177-121">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ виртуалсистеммигратионсервице**](cim-virtualsystemmigrationservice.md).**Мигратевиртуалсистемтохост (Дестинатионхост)**","**CIM \_ виртуалсистеммигратионсервице**.**Чекквиртуалсистемисмигратаблетохост (Дестинатионхост)**")</span><span class="sxs-lookup"><span data-stu-id="30177-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="30177-122">Массив, содержащий Поддерживаемые форматы для параметра *дестинатионхост* методов [**мигратевиртуалсистемтохост**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) и [**чекквиртуалсистемисмигратаблетохост**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) для объекта [**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="30177-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="30177-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**Домаиннамеформатсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="30177-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="30177-124">Поддержка текстового формата доменного имени в соответствии с RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="30177-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="30177-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="30177-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="30177-126">Поддержка десятичного формата IPv4 в соответствии с RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="30177-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="30177-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="30177-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="30177-128">Поддержка формата текста IPv6 в соответствии с RFC 4291</span><span class="sxs-lookup"><span data-stu-id="30177-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="30177-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="30177-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="30177-130">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="30177-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30177-131">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="30177-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="30177-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="30177-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="30177-133">Массив, указывающий методы [**\_ виртуалсистеммигратионсервице CIM**](cim-virtualsystemmigrationservice.md) , которые поддерживаются для синхронных операций.</span><span class="sxs-lookup"><span data-stu-id="30177-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="30177-134">Перечисление идентификаторов методов, реализация которых может быть синхронной; то есть операция может завершиться немедленно, поэтому метод может не возвращать задание.</span><span class="sxs-lookup"><span data-stu-id="30177-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="30177-135">**Мигратевиртуалсистемтохостсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="30177-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="30177-136">**Мигратевиртуалсистемтосистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="30177-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="30177-137">**Чекквиртуалсистемисмигратаблетохостсуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="30177-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="30177-138">**Чекквиртуалсистемисмигратаблетосистемсуппортед** (5)</span><span class="sxs-lookup"><span data-stu-id="30177-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="30177-139">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="30177-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="30177-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="30177-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="30177-141">Требования</span><span class="sxs-lookup"><span data-stu-id="30177-141">Requirements</span></span>



| <span data-ttu-id="30177-142">Требование</span><span class="sxs-lookup"><span data-stu-id="30177-142">Requirement</span></span> | <span data-ttu-id="30177-143">Значение</span><span class="sxs-lookup"><span data-stu-id="30177-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30177-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30177-144">Minimum supported client</span></span><br/> | <span data-ttu-id="30177-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="30177-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="30177-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30177-146">Minimum supported server</span></span><br/> | <span data-ttu-id="30177-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="30177-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="30177-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="30177-148">Namespace</span></span><br/>                | <span data-ttu-id="30177-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="30177-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="30177-150">MOF</span><span class="sxs-lookup"><span data-stu-id="30177-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30177-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30177-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="30177-152">DLL</span><span class="sxs-lookup"><span data-stu-id="30177-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30177-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="30177-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="30177-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30177-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30177-155">**\_Возможности CIM**</span><span class="sxs-lookup"><span data-stu-id="30177-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

