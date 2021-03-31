---
description: Представляет связь между логическим устройством и контроллером протокола, подключенным к устройству.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: Класс CIM_ProtocolControllerForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911352"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="102bb-103">\_Класс CIM протоколконтроллерфордевице</span><span class="sxs-lookup"><span data-stu-id="102bb-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="102bb-104">Представляет связь между логическим устройством и контроллером протокола, подключенным к устройству.</span><span class="sxs-lookup"><span data-stu-id="102bb-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="102bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="102bb-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="102bb-106">Члены</span><span class="sxs-lookup"><span data-stu-id="102bb-106">Members</span></span>

<span data-ttu-id="102bb-107">Класс **CIM \_ протоколконтроллерфордевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="102bb-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="102bb-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="102bb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="102bb-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="102bb-109">Properties</span></span>

<span data-ttu-id="102bb-110">Класс **CIM \_ протоколконтроллерфордевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="102bb-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="102bb-111">**акцессприорити**</span><span class="sxs-lookup"><span data-stu-id="102bb-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102bb-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="102bb-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="102bb-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="102bb-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="102bb-114">Приоритет доступа, предоставленный устройству через контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="102bb-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="102bb-115">Самый высокий приоритет имеет наименьшее значение.</span><span class="sxs-lookup"><span data-stu-id="102bb-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="102bb-116">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="102bb-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102bb-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="102bb-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="102bb-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="102bb-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="102bb-119">Доступность логического устройства через контроллер протокола</span><span class="sxs-lookup"><span data-stu-id="102bb-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="102bb-120">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="102bb-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="102bb-121">**Активно** (2)</span><span class="sxs-lookup"><span data-stu-id="102bb-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="102bb-122">**Неактивно** (3)</span><span class="sxs-lookup"><span data-stu-id="102bb-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="102bb-123">**Репликация выполняется** (4)</span><span class="sxs-lookup"><span data-stu-id="102bb-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="102bb-124">**Несогласованность сопоставления** (5)</span><span class="sxs-lookup"><span data-stu-id="102bb-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="102bb-125">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="102bb-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102bb-126">Тип данных: **CIM \_ протоколконтроллер**</span><span class="sxs-lookup"><span data-stu-id="102bb-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="102bb-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="102bb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="102bb-128">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="102bb-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="102bb-129">Контроллер протокола в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="102bb-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="102bb-130">**Него**</span><span class="sxs-lookup"><span data-stu-id="102bb-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102bb-131">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="102bb-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="102bb-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="102bb-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="102bb-133">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="102bb-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="102bb-134">Логическое устройство в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="102bb-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="102bb-135">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="102bb-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="102bb-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="102bb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="102bb-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="102bb-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="102bb-138">Адрес связанного устройства в контексте управления протоколом.</span><span class="sxs-lookup"><span data-stu-id="102bb-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="102bb-139">Требования</span><span class="sxs-lookup"><span data-stu-id="102bb-139">Requirements</span></span>



| <span data-ttu-id="102bb-140">Требование</span><span class="sxs-lookup"><span data-stu-id="102bb-140">Requirement</span></span> | <span data-ttu-id="102bb-141">Значение</span><span class="sxs-lookup"><span data-stu-id="102bb-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102bb-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="102bb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="102bb-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="102bb-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="102bb-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="102bb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="102bb-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="102bb-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="102bb-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="102bb-146">Namespace</span></span><br/>                | <span data-ttu-id="102bb-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="102bb-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="102bb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="102bb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="102bb-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="102bb-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="102bb-150">DLL</span><span class="sxs-lookup"><span data-stu-id="102bb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="102bb-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="102bb-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="102bb-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="102bb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102bb-153">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="102bb-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

