---
description: Представляет связь между контроллером и логическим устройством, которое управляется контроллером.
ms.assetid: 5a938fa4-3b91-42ad-beee-12ed0ce6df9a
title: Класс CIM_ControlledBy (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.TimeOfDeviceReset
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
- CIM_ControlledBy.DeviceNumber
- CIM_ControlledBy.AccessMode
- CIM_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7b035a93c47f9c33d981614ba6fc46b35f916e7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897894"
---
# <a name="cim_controlledby-class-hyper-v-management"></a><span data-ttu-id="4cea0-103">Класс CIM_ControlledBy (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4cea0-103">CIM_ControlledBy class (Hyper-V management)</span></span>

<span data-ttu-id="4cea0-104">Представляет связь между контроллером и логическим устройством, которое управляется контроллером.</span><span class="sxs-lookup"><span data-stu-id="4cea0-104">Represents a relationship between a controller and a logical device that is managed by the controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cea0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4cea0-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode;
  uint16                AccessPriority;
};
```

## <a name="members"></a><span data-ttu-id="4cea0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4cea0-106">Members</span></span>

<span data-ttu-id="4cea0-107">Класс **CIM \_ контролледби** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4cea0-107">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="4cea0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cea0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4cea0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cea0-109">Properties</span></span>

<span data-ttu-id="4cea0-110">Класс **CIM \_ контролледби** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4cea0-110">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4cea0-111">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="4cea0-111">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cea0-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-114">Это свойство описывает доступность устройства через контроллер.</span><span class="sxs-lookup"><span data-stu-id="4cea0-114">This property that describes the accessibility of the device through the controller.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="4cea0-115">**ReadWrite** (2)</span><span class="sxs-lookup"><span data-stu-id="4cea0-115">**ReadWrite** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="4cea0-116">**ReadOnly** (3)</span><span class="sxs-lookup"><span data-stu-id="4cea0-116">**ReadOnly** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="NoAccess"></span><span id="noaccess"></span><span id="NOACCESS"></span>

<span data-ttu-id="4cea0-117">**Недоступно** (4)</span><span class="sxs-lookup"><span data-stu-id="4cea0-117">**NoAccess** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4cea0-118">**акцессприорити**</span><span class="sxs-lookup"><span data-stu-id="4cea0-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cea0-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-121">Приоритет доступа устройства через контроллер.</span><span class="sxs-lookup"><span data-stu-id="4cea0-121">The priority for access of the device through the controller.</span></span> <span data-ttu-id="4cea0-122">Более низкое значение указывает более высокий приоритет.</span><span class="sxs-lookup"><span data-stu-id="4cea0-122">A lower value indicates a higher priority.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-123">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="4cea0-123">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-124">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4cea0-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-126">Указывает, активно ли устройство управляет устройством.</span><span class="sxs-lookup"><span data-stu-id="4cea0-126">Indicates whether the controller is actively managing the device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4cea0-127">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4cea0-127">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="4cea0-128">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="4cea0-128">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="4cea0-129">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="4cea0-129">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4cea0-130">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4cea0-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-131">Тип данных: **CIM \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="4cea0-131">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-133">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4cea0-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-134">Контроллер.</span><span class="sxs-lookup"><span data-stu-id="4cea0-134">The controller.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-135">**Него**</span><span class="sxs-lookup"><span data-stu-id="4cea0-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-136">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="4cea0-136">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-138">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4cea0-138">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-139">Логические устройства.</span><span class="sxs-lookup"><span data-stu-id="4cea0-139">The logical devices.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-140">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="4cea0-140">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4cea0-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-143">Адрес связанного устройства в контексте контроллера.</span><span class="sxs-lookup"><span data-stu-id="4cea0-143">The address of the associated device in the context of the controller.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-144">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="4cea0-144">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cea0-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-147">Квалификаторы: **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="4cea0-147">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-148">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="4cea0-148">The number of hard resets issued by the controller.</span></span> <span data-ttu-id="4cea0-149">Жесткий сброс возвращает устройство в состояние инициализации или загрузки, после чего теряются все внутренние сведения о состоянии устройства и данные.</span><span class="sxs-lookup"><span data-stu-id="4cea0-149">A hard reset returns a device to its initialization or boot-up state, after which all internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-150">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="4cea0-150">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4cea0-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-153">Квалификаторы: **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="4cea0-153">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-154">Число мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="4cea0-154">The number of soft resets issued by the controller.</span></span> <span data-ttu-id="4cea0-155">При мягком сбросе состояние устройства или данные не удаляются.</span><span class="sxs-lookup"><span data-stu-id="4cea0-155">A soft reset does not clear the device state or data.</span></span>

</dd> <dt>

<span data-ttu-id="4cea0-156">**тимеофдевицересет**</span><span class="sxs-lookup"><span data-stu-id="4cea0-156">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4cea0-157">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4cea0-157">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4cea0-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4cea0-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4cea0-159">Время последнего сброса подчиненного устройства контроллером.</span><span class="sxs-lookup"><span data-stu-id="4cea0-159">The time when the downstream device was last reset by the controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4cea0-160">Требования</span><span class="sxs-lookup"><span data-stu-id="4cea0-160">Requirements</span></span>



| <span data-ttu-id="4cea0-161">Требование</span><span class="sxs-lookup"><span data-stu-id="4cea0-161">Requirement</span></span> | <span data-ttu-id="4cea0-162">Значение</span><span class="sxs-lookup"><span data-stu-id="4cea0-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cea0-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cea0-163">Minimum supported client</span></span><br/> | <span data-ttu-id="4cea0-164">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4cea0-164">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4cea0-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cea0-165">Minimum supported server</span></span><br/> | <span data-ttu-id="4cea0-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4cea0-166">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4cea0-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4cea0-167">Namespace</span></span><br/>                | <span data-ttu-id="4cea0-168">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4cea0-168">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4cea0-169">MOF</span><span class="sxs-lookup"><span data-stu-id="4cea0-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4cea0-170"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4cea0-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4cea0-171">DLL</span><span class="sxs-lookup"><span data-stu-id="4cea0-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cea0-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4cea0-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4cea0-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cea0-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cea0-174">**\_ДЕВИЦЕКОННЕКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="4cea0-174">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

