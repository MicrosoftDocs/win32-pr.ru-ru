---
description: Связывает устройство хранения с контроллером хранилища, которому принадлежит устройство.
ms.assetid: 3DE05EDC-C54A-4C3C-9057-4418246037D5
title: Класс Msvm_ControlledBy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ControlledBy
- Msvm_ControlledBy.NegotiatedSpeed
- Msvm_ControlledBy.NegotiatedDataWidth
- Msvm_ControlledBy.Antecedent
- Msvm_ControlledBy.Dependent
- Msvm_ControlledBy.AccessState
- Msvm_ControlledBy.TimeOfDeviceReset
- Msvm_ControlledBy.NumberOfHardResets
- Msvm_ControlledBy.NumberOfSoftResets
- Msvm_ControlledBy.DeviceNumber
- Msvm_ControlledBy.AccessMode
- Msvm_ControlledBy.AccessPriority
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7986ffb842f7a1a104a0a8d846c1b6ee47a21523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684269"
---
# <a name="msvm_controlledby-class"></a><span data-ttu-id="57d3a-103">\_Класс мсвм контролледби</span><span class="sxs-lookup"><span data-stu-id="57d3a-103">Msvm\_ControlledBy class</span></span>

<span data-ttu-id="57d3a-104">Связывает устройство хранения с контроллером хранилища, которому принадлежит устройство.</span><span class="sxs-lookup"><span data-stu-id="57d3a-104">Associates a storage device with the storage controller that owns the device.</span></span> <span data-ttu-id="57d3a-105">Эта ассоциация используется как с IDE, так и с контроллерами флоппи-дисковода.</span><span class="sxs-lookup"><span data-stu-id="57d3a-105">This association is used with both IDE and floppy controllers.</span></span>

<span data-ttu-id="57d3a-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="57d3a-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d3a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57d3a-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ControlledBy : CIM_ControlledBy
{
  uint64                NegotiatedSpeed = 0;
  uint32                NegotiatedDataWidth = 0;
  CIM_Controller    REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint16                AccessState = 1;
  datetime              TimeOfDeviceReset;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  string                DeviceNumber;
  uint16                AccessMode = 2;
  uint16                AccessPriority = 0;
};
```

## <a name="members"></a><span data-ttu-id="57d3a-108">Члены</span><span class="sxs-lookup"><span data-stu-id="57d3a-108">Members</span></span>

<span data-ttu-id="57d3a-109">Класс **мсвм \_ контролледби** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="57d3a-109">The **Msvm\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="57d3a-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="57d3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57d3a-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="57d3a-111">Properties</span></span>

<span data-ttu-id="57d3a-112">Класс **мсвм \_ контролледби** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="57d3a-112">The **Msvm\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57d3a-113">**AccessMode**</span><span class="sxs-lookup"><span data-stu-id="57d3a-113">**AccessMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57d3a-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-116">Доступность устройства через предшествующий контроллер.</span><span class="sxs-lookup"><span data-stu-id="57d3a-116">The accessibility of the device through the antecedent controller.</span></span> <span data-ttu-id="57d3a-117">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 2 (чтение и запись).</span><span class="sxs-lookup"><span data-stu-id="57d3a-117">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 2 (read/write).</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-118">**акцессприорити**</span><span class="sxs-lookup"><span data-stu-id="57d3a-118">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57d3a-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-121">Приоритет, предоставляемый для доступа к устройству через этот контроллер.</span><span class="sxs-lookup"><span data-stu-id="57d3a-121">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="57d3a-122">Путь с наивысшим приоритетом будет иметь наименьшее значение.</span><span class="sxs-lookup"><span data-stu-id="57d3a-122">The highest priority path will have the lowest value.</span></span> <span data-ttu-id="57d3a-123">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="57d3a-123">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-124">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="57d3a-124">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-125">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="57d3a-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-127">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="57d3a-127">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="57d3a-128">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby)и всегда имеет значение 1 (активно).</span><span class="sxs-lookup"><span data-stu-id="57d3a-128">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), and it is always set to 1 (Active).</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-129">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="57d3a-129">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-130">Тип данных: **[ **CIM \_ Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span><span class="sxs-lookup"><span data-stu-id="57d3a-130">Data type: **[**CIM\_Controller**](/windows/desktop/CIMWin32Prov/cim-controller)**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-132">Ссылка на контроллер.</span><span class="sxs-lookup"><span data-stu-id="57d3a-132">A reference to the controller.</span></span> <span data-ttu-id="57d3a-133">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="57d3a-133">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-134">**Него**</span><span class="sxs-lookup"><span data-stu-id="57d3a-134">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-135">Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="57d3a-135">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-137">Ссылка на управляемое устройство.</span><span class="sxs-lookup"><span data-stu-id="57d3a-137">A reference to the controlled device.</span></span> <span data-ttu-id="57d3a-138">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="57d3a-138">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-139">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="57d3a-139">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="57d3a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-142">Адрес связанного устройства в контексте предшествующего контроллера.</span><span class="sxs-lookup"><span data-stu-id="57d3a-142">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="57d3a-143">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span><span class="sxs-lookup"><span data-stu-id="57d3a-143">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby).</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-144">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="57d3a-144">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-145">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57d3a-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-147">Это свойство наследуется от [**CIM \_ девицеконнектион**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="57d3a-147">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-148">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="57d3a-148">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-149">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="57d3a-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-151">Это свойство наследуется от [**CIM \_ девицеконнектион**](/windows/desktop/CIMWin32Prov/cim-deviceconnection)и всегда имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="57d3a-151">This property is inherited from [**CIM\_DeviceConnection**](/windows/desktop/CIMWin32Prov/cim-deviceconnection), and it is always set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-152">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="57d3a-152">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-153">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57d3a-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-155">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.</span><span class="sxs-lookup"><span data-stu-id="57d3a-155">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="57d3a-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="57d3a-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-159">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.</span><span class="sxs-lookup"><span data-stu-id="57d3a-159">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="57d3a-160">**тимеофдевицересет**</span><span class="sxs-lookup"><span data-stu-id="57d3a-160">**TimeOfDeviceReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57d3a-161">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="57d3a-161">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="57d3a-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="57d3a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="57d3a-163">Это свойство наследуется от [**CIM \_ контролледби**](/windows/desktop/CIMWin32Prov/cim-controlledby), но не используется.</span><span class="sxs-lookup"><span data-stu-id="57d3a-163">This property is inherited from [**CIM\_ControlledBy**](/windows/desktop/CIMWin32Prov/cim-controlledby), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57d3a-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57d3a-164">Remarks</span></span>

<span data-ttu-id="57d3a-165">Доступ к классу **\_ контролледби мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="57d3a-165">Access to the **Msvm\_ControlledBy** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="57d3a-166">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="57d3a-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="57d3a-167">Требования</span><span class="sxs-lookup"><span data-stu-id="57d3a-167">Requirements</span></span>



| <span data-ttu-id="57d3a-168">Требование</span><span class="sxs-lookup"><span data-stu-id="57d3a-168">Requirement</span></span> | <span data-ttu-id="57d3a-169">Значение</span><span class="sxs-lookup"><span data-stu-id="57d3a-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d3a-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57d3a-170">Minimum supported client</span></span><br/> | <span data-ttu-id="57d3a-171">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="57d3a-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="57d3a-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57d3a-172">Minimum supported server</span></span><br/> | <span data-ttu-id="57d3a-173">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="57d3a-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57d3a-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="57d3a-174">Namespace</span></span><br/>                | <span data-ttu-id="57d3a-175">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="57d3a-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="57d3a-176">MOF</span><span class="sxs-lookup"><span data-stu-id="57d3a-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57d3a-177"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57d3a-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="57d3a-178">DLL</span><span class="sxs-lookup"><span data-stu-id="57d3a-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57d3a-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="57d3a-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="57d3a-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57d3a-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d3a-181">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="57d3a-181">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="57d3a-182">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="57d3a-182">**CIM\_ControlledBy**</span></span>](/windows/desktop/CIMWin32Prov/cim-controlledby)
</dt> <dt>

[<span data-ttu-id="57d3a-183">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="57d3a-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

