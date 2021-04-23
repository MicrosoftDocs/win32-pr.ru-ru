---
description: '\_Класс WMI взаимосвязей Win32 усбконтроллердевице связывает с контроллером универсальной последовательной шины (USB) и \_ подключенным к нему экземпляром CIM.'
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Класс Win32_USBControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9bf72c92a4ae23ac7750cdd52914e86f5dbcdd01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655747"
---
# <a name="win32_usbcontrollerdevice-class"></a><span data-ttu-id="17183-103">\_Класс Win32 усбконтроллердевице</span><span class="sxs-lookup"><span data-stu-id="17183-103">Win32\_USBControllerDevice class</span></span>

<span data-ttu-id="17183-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ усбконтроллердевице** связывает с контроллером универсальной последовательной шины (USB) и подключенным к нему экземпляром [**\_ CIM**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="17183-104">The **Win32\_USBControllerDevice** association [WMI class](../wmisdk/retrieving-a-class.md) relates a universal serial bus (USB) controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span>

<span data-ttu-id="17183-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="17183-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="17183-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="17183-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17183-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17183-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="17183-108">Члены</span><span class="sxs-lookup"><span data-stu-id="17183-108">Members</span></span>

<span data-ttu-id="17183-109">Класс **Win32 \_ усбконтроллердевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="17183-109">The **Win32\_USBControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="17183-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="17183-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17183-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="17183-111">Properties</span></span>

<span data-ttu-id="17183-112">Класс **Win32 \_ усбконтроллердевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="17183-112">The **Win32\_USBControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17183-113">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="17183-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="17183-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="17183-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17183-116">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="17183-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="17183-117">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="17183-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="17183-118">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="17183-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="17183-119">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="17183-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="17183-120">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="17183-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="17183-121">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="17183-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="17183-122">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="17183-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-123">Тип данных: **CIM \_ усбконтроллер**</span><span class="sxs-lookup"><span data-stu-id="17183-123">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="17183-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17183-125">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ усбконтроллер")</span><span class="sxs-lookup"><span data-stu-id="17183-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_USBController")</span></span>
</dt> </dl>

<span data-ttu-id="17183-126">[**\_ Усбконтроллер CIM**](cim-usbcontroller.md) , представляющий контроллер универсальной последовательной шины (USB), связанный с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="17183-126">A [**CIM\_USBController**](cim-usbcontroller.md) representing the Universal Serial Bus (USB) controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="17183-127">**Него**</span><span class="sxs-lookup"><span data-stu-id="17183-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-128">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="17183-128">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="17183-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17183-130">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="17183-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="17183-131">[**CIM- \_ логическое**](cim-logicaldevice.md) значение, описывающее логическое устройство, подключенное к контроллеру универсальной последовательной шины (USB).</span><span class="sxs-lookup"><span data-stu-id="17183-131">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) describing the logical device connected to the Universal Serial Bus (USB) controller.</span></span>

</dd> <dt>

<span data-ttu-id="17183-132">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="17183-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17183-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17183-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17183-135">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("биты")</span><span class="sxs-lookup"><span data-stu-id="17183-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="17183-136">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="17183-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="17183-137">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="17183-137">Data width is specified in bits.</span></span> <span data-ttu-id="17183-138">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="17183-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="17183-139">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="17183-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="17183-140">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="17183-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="17183-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="17183-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17183-143">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="17183-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="17183-144">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="17183-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="17183-145">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="17183-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="17183-146">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="17183-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="17183-147">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="17183-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="17183-148">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="17183-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="17183-149">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="17183-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17183-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17183-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17183-152">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="17183-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="17183-153">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="17183-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="17183-154">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="17183-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="17183-155">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="17183-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="17183-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="17183-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17183-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="17183-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="17183-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="17183-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="17183-159">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="17183-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="17183-160">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="17183-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="17183-161">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="17183-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="17183-162">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="17183-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17183-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17183-163">Remarks</span></span>

<span data-ttu-id="17183-164">Класс **Win32 \_ усбконтроллердевице** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="17183-164">The **Win32\_USBControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="17183-165">Обсуждение об использовании см. в блоге [USB-устройства с помощью инструментария WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) .</span><span class="sxs-lookup"><span data-stu-id="17183-165">For a discussion on using, see the [Displaying USB Devices using WMI](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) blog article.</span></span> <span data-ttu-id="17183-166">Обсуждение использования классов ассоциаций см. в статье [Get-USB-using WMI Association classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) .</span><span class="sxs-lookup"><span data-stu-id="17183-166">For a discussion of using association classes, see the [Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) article.</span></span>

## <a name="examples"></a><span data-ttu-id="17183-167">Примеры</span><span class="sxs-lookup"><span data-stu-id="17183-167">Examples</span></span>

<span data-ttu-id="17183-168">В следующем примере PowerShell извлекается зависимое логическое устройство и отображаются соответствующие сведения.</span><span class="sxs-lookup"><span data-stu-id="17183-168">The following PowerShell example retrieves the dependent logical device and displays the relevant information.</span></span>


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
```



## <a name="requirements"></a><span data-ttu-id="17183-169">Требования</span><span class="sxs-lookup"><span data-stu-id="17183-169">Requirements</span></span>



| <span data-ttu-id="17183-170">Требование</span><span class="sxs-lookup"><span data-stu-id="17183-170">Requirement</span></span> | <span data-ttu-id="17183-171">Значение</span><span class="sxs-lookup"><span data-stu-id="17183-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17183-172">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17183-172">Minimum supported client</span></span><br/> | <span data-ttu-id="17183-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17183-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17183-174">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17183-174">Minimum supported server</span></span><br/> | <span data-ttu-id="17183-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17183-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17183-176">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="17183-176">Namespace</span></span><br/>                | <span data-ttu-id="17183-177">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17183-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17183-178">MOF</span><span class="sxs-lookup"><span data-stu-id="17183-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17183-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17183-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17183-180">DLL</span><span class="sxs-lookup"><span data-stu-id="17183-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17183-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17183-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17183-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17183-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17183-183">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="17183-183">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="17183-184">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="17183-184">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
