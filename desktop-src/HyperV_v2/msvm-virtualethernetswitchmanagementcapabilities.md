---
description: Описание возможностей связанного Мсвм \_ виртуалесернетсвитчманажементсервице.
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Класс Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650913"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a><span data-ttu-id="5770c-103">\_Класс мсвм виртуалесернетсвитчманажементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="5770c-103">Msvm\_VirtualEthernetSwitchManagementCapabilities class</span></span>

<span data-ttu-id="5770c-104">Описание возможностей связанного [**мсвм \_ виртуалесернетсвитчманажементсервице**](msvm-virtualethernetswitchmanagementservice.md).</span><span class="sxs-lookup"><span data-stu-id="5770c-104">Describes the capabilities of the associated [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md).</span></span>

<span data-ttu-id="5770c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5770c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5770c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5770c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a><span data-ttu-id="5770c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5770c-107">Members</span></span>

<span data-ttu-id="5770c-108">Класс **мсвм \_ виртуалесернетсвитчманажементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5770c-108">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="5770c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5770c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5770c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5770c-110">Properties</span></span>

<span data-ttu-id="5770c-111">Класс **мсвм \_ виртуалесернетсвитчманажементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5770c-111">The **Msvm\_VirtualEthernetSwitchManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5770c-112">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-112">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-113">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5770c-113">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5770c-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ виртуалсистемманажементкапабилитиес. асинчронаусмесодссуппортед")</span><span class="sxs-lookup"><span data-stu-id="5770c-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="5770c-116">Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ виртуалесернетсвитчманажементсервице**](msvm-virtualethernetswitchmanagementservice.md) , который поддерживается асинхронно реализацией.</span><span class="sxs-lookup"><span data-stu-id="5770c-116">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported asynchronously by the implementation.</span></span> <span data-ttu-id="5770c-117">Это свойство наследуется от **CIM \_ виртуалсистемманажементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-117">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

<span data-ttu-id="5770c-118">**Дефинесистем** (2)</span><span class="sxs-lookup"><span data-stu-id="5770c-118">**DefineSystem** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

<span data-ttu-id="5770c-119">**Дестройсистем** (3)</span><span class="sxs-lookup"><span data-stu-id="5770c-119">**DestroySystem** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

<span data-ttu-id="5770c-120">**Дестройсистемконфигуратион** (4)</span><span class="sxs-lookup"><span data-stu-id="5770c-120">**DestroySystemConfiguration** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

<span data-ttu-id="5770c-121">**Модифиресаурцесеттингс** (5)</span><span class="sxs-lookup"><span data-stu-id="5770c-121">**ModifyResourceSettings** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

<span data-ttu-id="5770c-122">**Модифисистемсеттингс** (6)</span><span class="sxs-lookup"><span data-stu-id="5770c-122">**ModifySystemSettings** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

<span data-ttu-id="5770c-123">**Ремовересаурцес** (7)</span><span class="sxs-lookup"><span data-stu-id="5770c-123">**RemoveResources** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

<span data-ttu-id="5770c-124">**Селектсистемконфигуратион** (8)</span><span class="sxs-lookup"><span data-stu-id="5770c-124">**SelectSystemConfiguration** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

<span data-ttu-id="5770c-125">**Снапшотсистем** (9)</span><span class="sxs-lookup"><span data-stu-id="5770c-125">**SnapshotSystem** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

<span data-ttu-id="5770c-126">**Аддресаурцес** (10)</span><span class="sxs-lookup"><span data-stu-id="5770c-126">**AddResources** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-127">**Аддфеатуресеттингссуппортед** (32779)</span><span class="sxs-lookup"><span data-stu-id="5770c-127">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-128">**Модифифеатуресеттингссуппортед** (32780)</span><span class="sxs-lookup"><span data-stu-id="5770c-128">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-129">**Ремовефеатуресеттингссуппортед** (32781)</span><span class="sxs-lookup"><span data-stu-id="5770c-129">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-130">**Аддфеатуресеттингссуппортед** (32779)</span><span class="sxs-lookup"><span data-stu-id="5770c-130">**AddFeatureSettingsSupported** (32779)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-131">**Модифифеатуресеттингссуппортед** (32780)</span><span class="sxs-lookup"><span data-stu-id="5770c-131">**ModifyFeatureSettingsSupported** (32780)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

<span data-ttu-id="5770c-132">**Ремовефеатуресеттингссуппортед** (32781)</span><span class="sxs-lookup"><span data-stu-id="5770c-132">**RemoveFeatureSettingsSupported** (32781)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5770c-133">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5770c-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5770c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-136">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5770c-136">A short description of the object.</span></span> <span data-ttu-id="5770c-137">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы управления коммутаторами виртуального Ethernet Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5770c-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5770c-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5770c-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5770c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-141">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5770c-141">A description of the object.</span></span> <span data-ttu-id="5770c-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "определяет возможности службы управления виртуальным коммутатором Ethernet".</span><span class="sxs-lookup"><span data-stu-id="5770c-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5770c-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5770c-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5770c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-146">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="5770c-146">A display name for the object.</span></span> <span data-ttu-id="5770c-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы управления коммутаторами виртуального Ethernet Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="5770c-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Virtual Ethernet Switch Management Service Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="5770c-148">**елементнамидитсуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-148">**ElementNameEditSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-149">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5770c-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-151">Указывает, можно ли изменить свойство **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="5770c-151">Indicates whether the **ElementName** property can be modified.</span></span> <span data-ttu-id="5770c-152">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-152">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-153">**елементнамемаск**</span><span class="sxs-lookup"><span data-stu-id="5770c-153">**ElementNameMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5770c-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-156">Задает ограничения для **ElementName**, выраженные в виде регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="5770c-156">Specifies the restrictions on **ElementName**, expressed as a regular expression.</span></span> <span data-ttu-id="5770c-157">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-157">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-158">**индикатионссуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-158">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-159">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5770c-159">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-161">Массив идентификаторов индикации, каждый из которых определяет указание, поддерживаемое реализацией.</span><span class="sxs-lookup"><span data-stu-id="5770c-161">An array of indication identifiers, each identifying an indication that is supported by the implementation.</span></span> <span data-ttu-id="5770c-162">Это свойство наследуется от **CIM \_ виртуалсистемманажементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-162">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>



| <span data-ttu-id="5770c-163">Значение</span><span class="sxs-lookup"><span data-stu-id="5770c-163">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="5770c-164">Значение</span><span class="sxs-lookup"><span data-stu-id="5770c-164">Meaning</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="5770c-165"><dt>**Виртуалресаурцестатечанжеиндикатионссуппортед**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-165"><dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="5770c-166">Указывает, поддерживает ли реализация уведомления об изменениях состояния экземпляров [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) , представляющих ресурсы виртуальных систем.</span><span class="sxs-lookup"><span data-stu-id="5770c-166">Indicates whether the implementation supports notification on state changes of [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) instances that represent resources of virtual systems.</span></span><br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="5770c-167"><dt>**Конкретежобстатечанжеиндикатионссуппортед**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-167"><dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt></span></span> </dl>                 | <span data-ttu-id="5770c-168">Указывает, поддерживает ли реализация уведомления об изменениях состояния экземпляров [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5770c-168">Indicates whether the implementation supports notification on state changes of [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)) instances.</span></span><br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <span data-ttu-id="5770c-169"><dt>**Виртуалсистемстатечанжеиндикатионссуппортед**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-169"><dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt></span></span> </dl>         | <span data-ttu-id="5770c-170">Указывает, поддерживает ли реализация уведомления об изменениях состояния экземпляров [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющих виртуальные системы.</span><span class="sxs-lookup"><span data-stu-id="5770c-170">Indicates whether the implementation supports notification on state changes of [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instances that represent virtual systems.</span></span><br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="5770c-171"><dt>**Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-171"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="5770c-172"><dt> **Зарезервировано поставщиком**</dt> <dt>32767.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-172"><dt>**Vendor Reserved** </dt> <dt>32767..65535 </dt></span></span> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="5770c-173">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5770c-173">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5770c-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5770c-176">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5770c-176">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5770c-177">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="5770c-177">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5770c-178">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5770c-178">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5770c-179">**иовсуппорт**</span><span class="sxs-lookup"><span data-stu-id="5770c-179">**IOVSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-180">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="5770c-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-182">Логическое значение, указывающее, поддерживается ли в платформе виртуализация ввода-вывода (IOV).</span><span class="sxs-lookup"><span data-stu-id="5770c-182">A boolean value that indicates whether I/O virtualization (IOV) is supported by the platform.</span></span> <span data-ttu-id="5770c-183">Если значение равно **true**, платформа IOV поддерживается платформой, а **иовсуппортреасонс** будет пустым.</span><span class="sxs-lookup"><span data-stu-id="5770c-183">If the value is **True**, then IOV is supported by the platform and **IOVSupportReasons** will be empty.</span></span> <span data-ttu-id="5770c-184">В противном случае свойство **иовсуппортреасонс** будет иметь причины, по которым невозможно поддерживать IOV.</span><span class="sxs-lookup"><span data-stu-id="5770c-184">Otherwise the **IOVSupportReasons** property will have the reasons why IOV cannot be supported.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-185">**иовсуппортреасонс**</span><span class="sxs-lookup"><span data-stu-id="5770c-185">**IOVSupportReasons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-186">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5770c-186">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-188">Массив строк, указывающий возможные причины, по которым не поддерживается IOV.</span><span class="sxs-lookup"><span data-stu-id="5770c-188">An array of strings that indicates the possible reasons why IOV is not supported.</span></span> <span data-ttu-id="5770c-189">Если значение **иовсуппорт** равно **true**, этот массив будет пустым.</span><span class="sxs-lookup"><span data-stu-id="5770c-189">If the value of **IOVSupport** is **True**, this array will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-190">**макселементнамелен**</span><span class="sxs-lookup"><span data-stu-id="5770c-190">**MaxElementNameLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-191">Тип данных: **unit16**</span><span class="sxs-lookup"><span data-stu-id="5770c-191">Data type: **unit16**</span></span>
</dt> <dt>

<span data-ttu-id="5770c-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5770c-193">Квалификаторы: **MaxValue** (256)</span><span class="sxs-lookup"><span data-stu-id="5770c-193">Qualifiers: **MaxValue** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5770c-194">Задает максимальную поддерживаемую длину свойства **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="5770c-194">Specifies the maximum supported length of the **ElementName** property.</span></span> <span data-ttu-id="5770c-195">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-195">This property is inherited from **CIM\_EnabledLogicalElementCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-196">**рекуестедстатессуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-196">**RequestedStatesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-197">Тип данных: массив **unit16**</span><span class="sxs-lookup"><span data-stu-id="5770c-197">Data type: **unit16** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-199">Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента.</span><span class="sxs-lookup"><span data-stu-id="5770c-199">Indicates the possible states that can be requested when using the **RequestStateChange** method on the enabled logical element.</span></span> <span data-ttu-id="5770c-200">Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес** и всегда имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5770c-200">This property is inherited from **CIM\_EnabledLogicalElementCapabilities** and is always **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="5770c-201">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-201">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-202">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5770c-202">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-204">Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ виртуалесернетсвитчманажементсервице**](msvm-virtualethernetswitchmanagementservice.md) , который поддерживается в синхронном режиме реализацией.</span><span class="sxs-lookup"><span data-stu-id="5770c-204">An array of method identifiers, each identifying a method of the [**Msvm\_VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) class that is supported synchronously by the implementation.</span></span> <span data-ttu-id="5770c-205">Это свойство наследуется от **CIM \_ виртуалсистемманажементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-205">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="5770c-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**Дефинесистем** (2)</span><span class="sxs-lookup"><span data-stu-id="5770c-206"><span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**Дестройсистем** (3)</span><span class="sxs-lookup"><span data-stu-id="5770c-207"><span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**Дестройсистемконфигуратион** (4)</span><span class="sxs-lookup"><span data-stu-id="5770c-208"><span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**Модифиресаурцесеттингс** (5)</span><span class="sxs-lookup"><span data-stu-id="5770c-209"><span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**Модифисистемсеттингс** (6)</span><span class="sxs-lookup"><span data-stu-id="5770c-210"><span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**Ремовересаурцес** (7)</span><span class="sxs-lookup"><span data-stu-id="5770c-211"><span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**Селектсистемконфигуратион** (8)</span><span class="sxs-lookup"><span data-stu-id="5770c-212"><span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**Снапшотсистем** (9)</span><span class="sxs-lookup"><span data-stu-id="5770c-213"><span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**Аддресаурцес** (10)</span><span class="sxs-lookup"><span data-stu-id="5770c-214"><span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**AddResources** (10)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**Аддфеатуресеттингс** (32779)</span><span class="sxs-lookup"><span data-stu-id="5770c-215"><span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**Модифифеатуресеттингс** (32780)</span><span class="sxs-lookup"><span data-stu-id="5770c-216"><span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)</span></span>
</dt> <dt>

<span data-ttu-id="5770c-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**Ремовефеатуресеттингс** (32781)</span><span class="sxs-lookup"><span data-stu-id="5770c-217"><span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5770c-218">**виртуалсистемтипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="5770c-218">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5770c-219">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5770c-219">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5770c-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5770c-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5770c-221">Массив строк, каждый из которых обозначает тип виртуальной системы, поддерживаемой реализацией.</span><span class="sxs-lookup"><span data-stu-id="5770c-221">An array of strings, each designating a type of virtual system that the implementation supports.</span></span> <span data-ttu-id="5770c-222">Значение каждого элемента массива, отличного от **null** , должно соответствовать формату, определенному для свойства **Виртуалсистемтипе** класса [**\_ виртуалсистемсеттингдата мсвм**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="5770c-222">The value of each non-**Null** array element must conform to the format defined for the **VirtualSystemType** property of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span> <span data-ttu-id="5770c-223">Это свойство наследуется от **CIM \_ виртуалсистемманажементкапабилитиес**.</span><span class="sxs-lookup"><span data-stu-id="5770c-223">This property is inherited from **CIM\_VirtualSystemManagementCapabilities**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5770c-224">Требования</span><span class="sxs-lookup"><span data-stu-id="5770c-224">Requirements</span></span>



| <span data-ttu-id="5770c-225">Требование</span><span class="sxs-lookup"><span data-stu-id="5770c-225">Requirement</span></span> | <span data-ttu-id="5770c-226">Значение</span><span class="sxs-lookup"><span data-stu-id="5770c-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5770c-227">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5770c-227">Minimum supported client</span></span><br/> | <span data-ttu-id="5770c-228">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5770c-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5770c-229">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5770c-229">Minimum supported server</span></span><br/> | <span data-ttu-id="5770c-230">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5770c-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5770c-231">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5770c-231">Namespace</span></span><br/>                | <span data-ttu-id="5770c-232">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5770c-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5770c-233">MOF</span><span class="sxs-lookup"><span data-stu-id="5770c-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5770c-234"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5770c-235">DLL</span><span class="sxs-lookup"><span data-stu-id="5770c-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5770c-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5770c-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

