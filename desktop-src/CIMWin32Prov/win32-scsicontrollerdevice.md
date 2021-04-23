---
description: '\_Класс WMI взаимосвязей Win32 сксиконтроллердевице связывает контроллер с системным интерфейсом (SCSI) и логическим устройством (дисковый накопитель), подключенным к нему.'
ms.assetid: 0334829c-3625-4acf-8ef3-da934c51e9bf
ms.tgt_platform: multiple
title: Класс Win32_SCSIControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SCSIControllerDevice
- Win32_SCSIControllerDevice.NegotiatedDataWidth
- Win32_SCSIControllerDevice.NegotiatedSpeed
- Win32_SCSIControllerDevice.AccessState
- Win32_SCSIControllerDevice.NumberOfHardResets
- Win32_SCSIControllerDevice.NumberOfSoftResets
- Win32_SCSIControllerDevice.Antecedent
- Win32_SCSIControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7a3189f9d9b75321df7c69214e68779864953f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539347"
---
# <a name="win32_scsicontrollerdevice-class"></a><span data-ttu-id="1c1d9-103">\_Класс Win32 сксиконтроллердевице</span><span class="sxs-lookup"><span data-stu-id="1c1d9-103">Win32\_SCSIControllerDevice class</span></span>

<span data-ttu-id="1c1d9-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сксиконтроллердевице** связывает контроллер с системным интерфейсом (SCSI) и логическим устройством (дисковый накопитель), подключенным к нему.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-104">The **Win32\_SCSIControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a small computer system interface (SCSI) controller and the logical device (disk drive) connected to it.</span></span>

<span data-ttu-id="1c1d9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1c1d9-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1d9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c1d9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{CC0F48D2-C847-11d2-911E-0060081A46FD}"), AMENDMENT]
class Win32_SCSIControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_SCSIController REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="1c1d9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="1c1d9-108">Members</span></span>

<span data-ttu-id="1c1d9-109">Класс **Win32 \_ сксиконтроллердевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c1d9-109">The **Win32\_SCSIControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="1c1d9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c1d9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c1d9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c1d9-111">Properties</span></span>

<span data-ttu-id="1c1d9-112">Класс **Win32 \_ сксиконтроллердевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-112">The **Win32\_SCSIControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c1d9-113">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-116">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="1c1d9-117">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="1c1d9-118">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1c1d9-119">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="1c1d9-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="1c1d9-120">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="1c1d9-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="1c1d9-121">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="1c1d9-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1c1d9-122">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-123">Тип данных: **Win32 \_ сксиконтроллер**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-123">Data type: **Win32\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-125">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| Win32 \_ сксиконтроллер")</span><span class="sxs-lookup"><span data-stu-id="1c1d9-125">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|Win32\_SCSIController")</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-126">Ссылка на [**Win32 \_ сксиконтроллер**](win32-scsicontroller.md) ANTECEDENT представляет контроллер SCSI, связанный с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-126">The [**Win32\_SCSIController**](win32-scsicontroller.md) antecedent reference represents the SCSI controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="1c1d9-127">**Него**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-128">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="1c1d9-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-130">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="1c1d9-130">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-131">Ссылка Dependent логического устройства [**CIM \_**](cim-logicaldevice.md) представляет логическое устройство, подключенное к контроллеру SCSI.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-131">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) dependent reference represents the logical device connected to the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="1c1d9-132">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-135">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("биты")</span><span class="sxs-lookup"><span data-stu-id="1c1d9-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-136">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="1c1d9-137">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-137">Data width is specified in bits.</span></span> <span data-ttu-id="1c1d9-138">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1c1d9-139">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1d9-140">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-143">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="1c1d9-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-144">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="1c1d9-145">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="1c1d9-146">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="1c1d9-147">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="1c1d9-148">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1d9-149">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-152">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="1c1d9-153">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="1c1d9-154">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="1c1d9-155">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="1c1d9-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c1d9-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c1d9-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c1d9-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c1d9-159">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="1c1d9-160">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="1c1d9-161">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="1c1d9-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="1c1d9-162">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c1d9-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c1d9-163">Remarks</span></span>

<span data-ttu-id="1c1d9-164">Класс **Win32 \_ сксиконтроллердевице** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="1c1d9-164">The **Win32\_SCSIControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1d9-165">Требования</span><span class="sxs-lookup"><span data-stu-id="1c1d9-165">Requirements</span></span>



| <span data-ttu-id="1c1d9-166">Требование</span><span class="sxs-lookup"><span data-stu-id="1c1d9-166">Requirement</span></span> | <span data-ttu-id="1c1d9-167">Значение</span><span class="sxs-lookup"><span data-stu-id="1c1d9-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1d9-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c1d9-168">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1d9-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c1d9-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c1d9-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c1d9-170">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1d9-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c1d9-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c1d9-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c1d9-172">Namespace</span></span><br/>                | <span data-ttu-id="1c1d9-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c1d9-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c1d9-174">MOF</span><span class="sxs-lookup"><span data-stu-id="1c1d9-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c1d9-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c1d9-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c1d9-176">DLL</span><span class="sxs-lookup"><span data-stu-id="1c1d9-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c1d9-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1d9-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1d9-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c1d9-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1d9-179">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="1c1d9-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="1c1d9-180">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="1c1d9-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
