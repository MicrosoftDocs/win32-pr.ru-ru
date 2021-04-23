---
description: Определяет средства, с помощью которых клиент может обнаружить методы, предоставляемые службой миграции, и допустимый диапазон данных параметров миграции виртуальной системы.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Класс Msvm_VirtualSystemMigrationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540282"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="c3c68-103">\_Класс мсвм виртуалсистеммигратионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="c3c68-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="c3c68-104">Определяет средства, с помощью которых клиент может обнаружить методы, предоставляемые службой миграции, и допустимый диапазон данных параметров миграции виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="c3c68-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="c3c68-105">Объект **\_ виртуалсистеммигратионкапабилитиес мсвм** связан с объектами [**мсвм \_ виртуалсистеммигратионсеттингдата**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c3c68-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="c3c68-106">Эти ассоциации определяют допустимый диапазон доступных служб миграции.</span><span class="sxs-lookup"><span data-stu-id="c3c68-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="c3c68-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c3c68-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c68-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3c68-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="c3c68-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c3c68-109">Members</span></span>

<span data-ttu-id="c3c68-110">Класс **мсвм \_ виртуалсистеммигратионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c3c68-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c3c68-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3c68-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3c68-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3c68-112">Properties</span></span>

<span data-ttu-id="c3c68-113">Класс **мсвм \_ виртуалсистеммигратионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c3c68-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3c68-114">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="c3c68-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-115">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c3c68-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-117">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("асинчронаусмесодссуппортед")</span><span class="sxs-lookup"><span data-stu-id="c3c68-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-118">Определяет методы, реализация которых может быть асинхронной; Это значит, что операция не будет выполнена немедленно и вернет задание.</span><span class="sxs-lookup"><span data-stu-id="c3c68-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="c3c68-119">Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="c3c68-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="c3c68-120">**Мигратевиртуалсистемтохостсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c68-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="c3c68-121">**Мигратевиртуалсистемтосистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c68-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="c3c68-122">**Чекквиртуалсистемисмигратаблесуппортед** (32768)</span><span class="sxs-lookup"><span data-stu-id="c3c68-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c3c68-123">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="c3c68-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3c68-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-126">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c3c68-126">A short description of the object.</span></span> <span data-ttu-id="c3c68-127">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности миграции".</span><span class="sxs-lookup"><span data-stu-id="c3c68-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="c3c68-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c3c68-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3c68-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-131">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="c3c68-131">A description of the object.</span></span> <span data-ttu-id="c3c68-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности миграции виртуальной системы".</span><span class="sxs-lookup"><span data-stu-id="c3c68-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="c3c68-133">**дестинатионхостформатссуппортед**</span><span class="sxs-lookup"><span data-stu-id="c3c68-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-134">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c3c68-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-136">Массив форматов имен, поддерживаемых для параметра *дестинатионхост* методов [**мигратевиртуалсистемтохост**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) и [**чекквиртуалсистемисмигратабле**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="c3c68-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="c3c68-137">Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="c3c68-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="c3c68-138">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c68-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="c3c68-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c68-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="c3c68-140"><dt>**Домаиннамеформатсуппортед**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c3c68-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="c3c68-141">Поддержка формата доменных имен в соответствии с RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="c3c68-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="c3c68-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c3c68-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="c3c68-143">Поддержка десятичного формата IPv4 в соответствии с RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="c3c68-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="c3c68-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c3c68-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="c3c68-145">Поддержка формата текста IPv6 в соответствии с RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="c3c68-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="c3c68-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="c3c68-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3c68-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-149">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="c3c68-149">A display name for the object.</span></span> <span data-ttu-id="c3c68-150">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c68-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c68-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c3c68-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3c68-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-154">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="c3c68-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-155">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="c3c68-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="c3c68-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="c3c68-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="c3c68-157">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="c3c68-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3c68-158">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="c3c68-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3c68-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c3c68-160">Определяет методы, реализация которых может быть синхронной; то есть операция будет завершена немедленно и не будет возвращать задание.</span><span class="sxs-lookup"><span data-stu-id="c3c68-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="c3c68-161">Это свойство наследуется от **CIM \_ виртуалсистеммигратионкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="c3c68-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="c3c68-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**Мигратевиртуалсистемтохостсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="c3c68-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**Мигратевиртуалсистемтосистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="c3c68-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**Чекквиртуалсистемисмигратаблетохостсуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="c3c68-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**Чекквиртуалсистемисмигратаблетосистемсуппортед** (5)</span><span class="sxs-lookup"><span data-stu-id="c3c68-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c3c68-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="c3c68-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="c3c68-167">)</span><span class="sxs-lookup"><span data-stu-id="c3c68-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3c68-168">Требования</span><span class="sxs-lookup"><span data-stu-id="c3c68-168">Requirements</span></span>



| <span data-ttu-id="c3c68-169">Требование</span><span class="sxs-lookup"><span data-stu-id="c3c68-169">Requirement</span></span> | <span data-ttu-id="c3c68-170">Значение</span><span class="sxs-lookup"><span data-stu-id="c3c68-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c68-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3c68-171">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c68-172">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c3c68-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c3c68-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3c68-173">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c68-174">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c3c68-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c3c68-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3c68-175">Namespace</span></span><br/>                | <span data-ttu-id="c3c68-176">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c3c68-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c3c68-177">MOF</span><span class="sxs-lookup"><span data-stu-id="c3c68-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3c68-178"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3c68-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3c68-179">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c68-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3c68-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3c68-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

