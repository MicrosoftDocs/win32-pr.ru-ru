---
description: '\_Класс WMI взаимосвязей Win32 идеконтроллердевице связывает контроллер интегрированной системы управления устройствами (IDE) и логическое устройство, подключенное к, например, к диску.'
ms.assetid: 1b0a551c-d836-4147-91ed-a0a7d97f4a5b
ms.tgt_platform: multiple
title: Класс Win32_IDEControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IDEControllerDevice
- Win32_IDEControllerDevice.NegotiatedDataWidth
- Win32_IDEControllerDevice.NegotiatedSpeed
- Win32_IDEControllerDevice.AccessState
- Win32_IDEControllerDevice.NumberOfHardResets
- Win32_IDEControllerDevice.NumberOfSoftResets
- Win32_IDEControllerDevice.Antecedent
- Win32_IDEControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc690aadd442d656132b2d9e4539cc27961c3ef9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423466"
---
# <a name="win32_idecontrollerdevice-class"></a><span data-ttu-id="74021-103">\_Класс Win32 идеконтроллердевице</span><span class="sxs-lookup"><span data-stu-id="74021-103">Win32\_IDEControllerDevice class</span></span>

<span data-ttu-id="74021-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ идеконтроллердевице** связывает контроллер интегрированной системы управления устройствами (IDE) и логическое устройство, подключенное к, например, к диску.</span><span class="sxs-lookup"><span data-stu-id="74021-104">The **Win32\_IDEControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates an Integrated Drive Electronics (IDE) controller and the logical device connected to, for example, a disk drive.</span></span>

<span data-ttu-id="74021-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="74021-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="74021-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="74021-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="74021-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74021-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{5BC42B62-C7A1-11d2-911D-0060081A46FD}"), AMENDMENT]
class Win32_IDEControllerDevice : CIM_ControlledBy
{
  uint32                  NegotiatedDataWidth;
  uint64                  NegotiatedSpeed;
  uint16                  AccessState;
  uint32                  NumberOfHardResets;
  uint32                  NumberOfSoftResets;
  Win32_IDEController REF Antecedent;
  CIM_LogicalDevice   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="74021-108">Члены</span><span class="sxs-lookup"><span data-stu-id="74021-108">Members</span></span>

<span data-ttu-id="74021-109">Класс **Win32 \_ идеконтроллердевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74021-109">The **Win32\_IDEControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="74021-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="74021-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74021-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="74021-111">Properties</span></span>

<span data-ttu-id="74021-112">Класс **Win32 \_ идеконтроллердевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74021-112">The **Win32\_IDEControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74021-113">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="74021-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74021-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74021-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74021-116">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="74021-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="74021-117">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="74021-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="74021-118">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="74021-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="74021-119">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="74021-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="74021-120">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="74021-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="74021-121">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="74021-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74021-122">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="74021-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-123">Тип данных: **Win32 \_ идеконтроллер**</span><span class="sxs-lookup"><span data-stu-id="74021-123">Data type: **Win32\_IDEController**</span></span>
</dt> <dt>

<span data-ttu-id="74021-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74021-125">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| Win32 \_ идеконтроллер")</span><span class="sxs-lookup"><span data-stu-id="74021-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|Win32\_IDEController")</span></span>
</dt> </dl>

<span data-ttu-id="74021-126">[**\_ Идеконтроллер Win32**](win32-idecontroller.md) , представляющий контроллер IDE, связанный с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="74021-126">A [**Win32\_IDEController**](win32-idecontroller.md) that represents the IDE controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="74021-127">**Него**</span><span class="sxs-lookup"><span data-stu-id="74021-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-128">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="74021-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="74021-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74021-130">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="74021-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="74021-131">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , представляющая логическое устройство, подключенное к контроллеру IDE.</span><span class="sxs-lookup"><span data-stu-id="74021-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the logical device connected to the IDE controller.</span></span>

</dd> <dt>

<span data-ttu-id="74021-132">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="74021-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74021-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74021-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74021-135">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="74021-135">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="74021-136">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="74021-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="74021-137">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="74021-137">Data width is specified in bits.</span></span> <span data-ttu-id="74021-138">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="74021-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="74021-139">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="74021-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="74021-140">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="74021-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="74021-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="74021-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74021-143">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="74021-143">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="74021-144">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="74021-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="74021-145">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="74021-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="74021-146">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="74021-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="74021-147">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="74021-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="74021-148">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="74021-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="74021-149">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="74021-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74021-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74021-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74021-152">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="74021-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="74021-153">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="74021-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="74021-154">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="74021-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="74021-155">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="74021-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="74021-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="74021-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74021-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74021-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74021-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74021-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74021-159">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="74021-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="74021-160">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="74021-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="74021-161">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="74021-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="74021-162">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="74021-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74021-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74021-163">Remarks</span></span>

<span data-ttu-id="74021-164">Класс **Win32 \_ идеконтроллердевице** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="74021-164">The **Win32\_IDEControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74021-165">Требования</span><span class="sxs-lookup"><span data-stu-id="74021-165">Requirements</span></span>



| <span data-ttu-id="74021-166">Требование</span><span class="sxs-lookup"><span data-stu-id="74021-166">Requirement</span></span> | <span data-ttu-id="74021-167">Значение</span><span class="sxs-lookup"><span data-stu-id="74021-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74021-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74021-168">Minimum supported client</span></span><br/> | <span data-ttu-id="74021-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74021-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74021-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74021-170">Minimum supported server</span></span><br/> | <span data-ttu-id="74021-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74021-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74021-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74021-172">Namespace</span></span><br/>                | <span data-ttu-id="74021-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="74021-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="74021-174">MOF</span><span class="sxs-lookup"><span data-stu-id="74021-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74021-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74021-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="74021-176">DLL</span><span class="sxs-lookup"><span data-stu-id="74021-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74021-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74021-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74021-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74021-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74021-179">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="74021-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="74021-180">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="74021-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

