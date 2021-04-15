---
description: Представляет возможности \_ объекта ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM.
ms.assetid: 484b0378-b354-49c4-b98b-a960a7b07b92
title: Класс CIM_VirtualSystemManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementCapabilities
- CIM_VirtualSystemManagementCapabilities.VirtualSystemTypesSupported
- CIM_VirtualSystemManagementCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemManagementCapabilities.IndicationsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2772068ed011a2a61cdd4f5c1396e057838b7720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662803"
---
# <a name="cim_virtualsystemmanagementcapabilities-class"></a><span data-ttu-id="3e42e-103">\_Класс CIM виртуалсистемманажементкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="3e42e-103">CIM\_VirtualSystemManagementCapabilities class</span></span>

<span data-ttu-id="3e42e-104">Представляет возможности объекта [**\_ виртуалсистемманажементсервице CIM**](cim-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3e42e-104">Represents the capabilities of a [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e42e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e42e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string VirtualSystemTypesSupported[];
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 IndicationsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="3e42e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="3e42e-106">Members</span></span>

<span data-ttu-id="3e42e-107">Класс **CIM \_ виртуалсистемманажементкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3e42e-107">The **CIM\_VirtualSystemManagementCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="3e42e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e42e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e42e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e42e-109">Properties</span></span>

<span data-ttu-id="3e42e-110">Класс **CIM \_ виртуалсистемманажементкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3e42e-110">The **CIM\_VirtualSystemManagementCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e42e-111">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e42e-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e42e-112">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e42e-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e42e-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e42e-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e42e-114">Массив, содержащий имена методов класса [**CIM \_ виртуалсистемманажементсервице**](cim-virtualsystemmanagementservice.md) , которые поддерживаются для асинхронных операций.</span><span class="sxs-lookup"><span data-stu-id="3e42e-114">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-115">**Дефинесистемсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="3e42e-115">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-116">**Дестройсистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="3e42e-116">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="3e42e-117">**Дестройсистемконфигуратионсуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="3e42e-117">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="3e42e-118">**Модифиресаурцесеттингссуппортед** (5)</span><span class="sxs-lookup"><span data-stu-id="3e42e-118">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="3e42e-119">**Модифисистемсеттингссуппортед** (6)</span><span class="sxs-lookup"><span data-stu-id="3e42e-119">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="3e42e-120">**Ремовересаурцессуппортед** (7)</span><span class="sxs-lookup"><span data-stu-id="3e42e-120">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="3e42e-121">**Селектсистемконфигуратионсуппортед** (8)</span><span class="sxs-lookup"><span data-stu-id="3e42e-121">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-122">**Снапшотсистемсуппортед** (9)</span><span class="sxs-lookup"><span data-stu-id="3e42e-122">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="3e42e-123">**Аддресаурцессуппортед** (10)</span><span class="sxs-lookup"><span data-stu-id="3e42e-123">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e42e-124">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e42e-124">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e42e-125">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e42e-125">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e42e-126">**индикатионссуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e42e-126">**IndicationsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e42e-127">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e42e-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e42e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e42e-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e42e-129">Массив, содержащий Поддерживаемые типы реализации.</span><span class="sxs-lookup"><span data-stu-id="3e42e-129">An array that contains the supported indications types of the implementation.</span></span>

<dt>

<span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3e42e-130">**Виртуалресаурцестатечанжеиндикатионссуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="3e42e-130">**VirtualResourceStateChangeIndicationsSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3e42e-131">**Конкретежобстатечанжеиндикатионссуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="3e42e-131">**ConcreteJobStateChangeIndicationsSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span>

<span data-ttu-id="3e42e-132">**Виртуалсистемстатечанжеиндикатионссуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="3e42e-132">**VirtualSystemStateChangeIndicationsSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e42e-133">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e42e-133">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e42e-134">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e42e-134">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e42e-135">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e42e-135">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e42e-136">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="3e42e-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3e42e-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e42e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e42e-138">Массив, содержащий имена методов класса [**CIM \_ виртуалсистемманажементсервице**](cim-virtualsystemmanagementservice.md) , которые поддерживаются для синхронных операций.</span><span class="sxs-lookup"><span data-stu-id="3e42e-138">An array that contains method names for the [**CIM\_VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md) class methods that are supported for synchronous operations.</span></span>

<dt>

<span id="DefineSystemSupported"></span><span id="definesystemsupported"></span><span id="DEFINESYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-139">**Дефинесистемсуппортед** (2)</span><span class="sxs-lookup"><span data-stu-id="3e42e-139">**DefineSystemSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemSupported"></span><span id="destroysystemsupported"></span><span id="DESTROYSYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-140">**Дестройсистемсуппортед** (3)</span><span class="sxs-lookup"><span data-stu-id="3e42e-140">**DestroySystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DestroySystemConfigurationSupported"></span><span id="destroysystemconfigurationsupported"></span><span id="DESTROYSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="3e42e-141">**Дестройсистемконфигуратионсуппортед** (4)</span><span class="sxs-lookup"><span data-stu-id="3e42e-141">**DestroySystemConfigurationSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettingsSupported"></span><span id="modifyresourcesettingssupported"></span><span id="MODIFYRESOURCESETTINGSSUPPORTED"></span>

<span data-ttu-id="3e42e-142">**Модифиресаурцесеттингссуппортед** (5)</span><span class="sxs-lookup"><span data-stu-id="3e42e-142">**ModifyResourceSettingsSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ModifySystemSettingsSupported"></span><span id="modifysystemsettingssupported"></span><span id="MODIFYSYSTEMSETTINGSSUPPORTED"></span>

<span data-ttu-id="3e42e-143">**Модифисистемсеттингссуппортед** (6)</span><span class="sxs-lookup"><span data-stu-id="3e42e-143">**ModifySystemSettingsSupported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="RemoveResourcesSupported"></span><span id="removeresourcessupported"></span><span id="REMOVERESOURCESSUPPORTED"></span>

<span data-ttu-id="3e42e-144">**Ремовересаурцессуппортед** (7)</span><span class="sxs-lookup"><span data-stu-id="3e42e-144">**RemoveResourcesSupported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SelectSystemConfigurationSupported"></span><span id="selectsystemconfigurationsupported"></span><span id="SELECTSYSTEMCONFIGURATIONSUPPORTED"></span>

<span data-ttu-id="3e42e-145">**Селектсистемконфигуратионсуппортед** (8)</span><span class="sxs-lookup"><span data-stu-id="3e42e-145">**SelectSystemConfigurationSupported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SnapshotSystemSupported"></span><span id="snapshotsystemsupported"></span><span id="SNAPSHOTSYSTEMSUPPORTED"></span>

<span data-ttu-id="3e42e-146">**Снапшотсистемсуппортед** (9)</span><span class="sxs-lookup"><span data-stu-id="3e42e-146">**SnapshotSystemSupported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="AddResourcesSupported"></span><span id="addresourcessupported"></span><span id="ADDRESOURCESSUPPORTED"></span>

<span data-ttu-id="3e42e-147">**Аддресаурцессуппортед** (10)</span><span class="sxs-lookup"><span data-stu-id="3e42e-147">**AddResourcesSupported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="3e42e-148">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="3e42e-148">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="3e42e-149">**Зарезервировано поставщиком** (32767.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3e42e-149">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3e42e-150">**виртуалсистемтипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="3e42e-150">**VirtualSystemTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e42e-151">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="3e42e-151">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3e42e-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e42e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e42e-153">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md).**Виртуалсистемтипе**")</span><span class="sxs-lookup"><span data-stu-id="3e42e-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md).**VirtualSystemType**")</span></span>
</dt> </dl>

<span data-ttu-id="3e42e-154">Тип виртуальных систем, поддерживаемых реализацией.</span><span class="sxs-lookup"><span data-stu-id="3e42e-154">The type of virtual systems supported by the implementation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e42e-155">Требования</span><span class="sxs-lookup"><span data-stu-id="3e42e-155">Requirements</span></span>



| <span data-ttu-id="3e42e-156">Требование</span><span class="sxs-lookup"><span data-stu-id="3e42e-156">Requirement</span></span> | <span data-ttu-id="3e42e-157">Значение</span><span class="sxs-lookup"><span data-stu-id="3e42e-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e42e-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e42e-158">Minimum supported client</span></span><br/> | <span data-ttu-id="3e42e-159">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3e42e-159">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="3e42e-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e42e-160">Minimum supported server</span></span><br/> | <span data-ttu-id="3e42e-161">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e42e-161">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="3e42e-162">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3e42e-162">Namespace</span></span><br/>                | <span data-ttu-id="3e42e-163">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3e42e-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="3e42e-164">MOF</span><span class="sxs-lookup"><span data-stu-id="3e42e-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e42e-165"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e42e-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e42e-166">DLL</span><span class="sxs-lookup"><span data-stu-id="3e42e-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e42e-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3e42e-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3e42e-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e42e-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e42e-169">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТКАПАБИЛИТИЕС CIM**</span><span class="sxs-lookup"><span data-stu-id="3e42e-169">**CIM\_EnabledLogicalElementCapabilities**</span></span>](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

