---
description: '\_Класс WMI взаимосвязей Win32 1394ControllerDevice связывает с контроллером высокоскоростной последовательной шины (IEEE 1394 Firewire) и \_ подключенным к нему экземпляром CIM.'
ms.assetid: 327fbced-4637-4402-a06f-6ac352da920c
ms.tgt_platform: multiple
title: Класс Win32_1394ControllerDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_1394ControllerDevice
- Win32_1394ControllerDevice.NegotiatedDataWidth
- Win32_1394ControllerDevice.NegotiatedSpeed
- Win32_1394ControllerDevice.AccessState
- Win32_1394ControllerDevice.NumberOfHardResets
- Win32_1394ControllerDevice.NumberOfSoftResets
- Win32_1394ControllerDevice.Antecedent
- Win32_1394ControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: af3a54db81a388184da148cd411895ebb910de7d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896362"
---
# <a name="win32_1394controllerdevice-class"></a><span data-ttu-id="2da45-103">\_Класс Win32 1394ControllerDevice</span><span class="sxs-lookup"><span data-stu-id="2da45-103">Win32\_1394ControllerDevice class</span></span>

<span data-ttu-id="2da45-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ 1394ControllerDevice** связывает с контроллером высокоскоростной последовательной шины (IEEE 1394 Firewire) и подключенным к нему экземпляром [**\_ CIM**](cim-logicaldevice.md) .</span><span class="sxs-lookup"><span data-stu-id="2da45-104">The **Win32\_1394ControllerDevice** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the high-speed serial bus (IEEE 1394 Firewire) Controller and the [**CIM\_LogicalDevice**](cim-logicaldevice.md) instance connected to it.</span></span> <span data-ttu-id="2da45-105">Эта последовательная шина обеспечивает улучшенное подключение для широкого спектра устройств, включая аудио-и видеокомпоненты, периферийные устройства хранения, другие компьютеры и портативные устройства.</span><span class="sxs-lookup"><span data-stu-id="2da45-105">This serial bus provides enhanced connectivity for a wide range of devices, including consumer audio or video components, storage peripherals, other computers, and portable devices.</span></span> <span data-ttu-id="2da45-106">Стандарт IEEE 1394 реализован в индустрии бытовой электроники и предоставляет совместимый с самонастраивающийся интерфейс расширения.</span><span class="sxs-lookup"><span data-stu-id="2da45-106">IEEE 1394 has been adopted by the consumer electronics industry and provides a Plug and Play-compatible expansion interface.</span></span>

<span data-ttu-id="2da45-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2da45-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2da45-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2da45-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da45-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2da45-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8835CFC9-BAEF-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class Win32_1394ControllerDevice : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  Win32_1394Controller REF Antecedent;
  CIM_LogicalDevice    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="2da45-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2da45-110">Members</span></span>

<span data-ttu-id="2da45-111">Класс **Win32 \_ 1394ControllerDevice** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2da45-111">The **Win32\_1394ControllerDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="2da45-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2da45-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2da45-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2da45-113">Properties</span></span>

<span data-ttu-id="2da45-114">Класс **Win32 \_ 1394ControllerDevice** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2da45-114">The **Win32\_1394ControllerDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2da45-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="2da45-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2da45-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2da45-118">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="2da45-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="2da45-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="2da45-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="2da45-120">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2da45-121">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="2da45-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="2da45-122">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="2da45-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="2da45-123">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="2da45-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2da45-124">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2da45-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-125">Тип данных: **Win32 \_ 1394Controller**</span><span class="sxs-lookup"><span data-stu-id="2da45-125">Data type: **Win32\_1394Controller**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2da45-127">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ 1394Controller")</span><span class="sxs-lookup"><span data-stu-id="2da45-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_1394Controller")</span></span>
</dt> </dl>

<span data-ttu-id="2da45-128">Ссылка на Win32 \_ 1394Controller Antecedent представляет контроллер 1394, связанный с этим устройством.</span><span class="sxs-lookup"><span data-stu-id="2da45-128">The Win32\_1394Controller antecedent reference represents the 1394 controller associated with this device.</span></span>

</dd> <dt>

<span data-ttu-id="2da45-129">**Него**</span><span class="sxs-lookup"><span data-stu-id="2da45-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-130">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="2da45-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2da45-132">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="2da45-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="2da45-133">\_Зависимая ссылка на модель CIM представляет собой CIM, \_ подключенный к контроллеру 1394.</span><span class="sxs-lookup"><span data-stu-id="2da45-133">The CIM\_LogicalDevice dependent reference represents the CIM\_LogicalDevice connected to the 1394 controller.</span></span>

</dd> <dt>

<span data-ttu-id="2da45-134">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="2da45-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2da45-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2da45-137">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="2da45-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="2da45-138">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="2da45-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="2da45-139">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="2da45-139">Data width is specified in bits.</span></span> <span data-ttu-id="2da45-140">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="2da45-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="2da45-141">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="2da45-142">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="2da45-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2da45-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2da45-145">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="2da45-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="2da45-146">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="2da45-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="2da45-147">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="2da45-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="2da45-148">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="2da45-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="2da45-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2da45-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2da45-150">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="2da45-151">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="2da45-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2da45-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2da45-154">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="2da45-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="2da45-155">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="2da45-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="2da45-156">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="2da45-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="2da45-157">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="2da45-158">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="2da45-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2da45-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2da45-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2da45-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2da45-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2da45-161">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="2da45-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="2da45-162">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="2da45-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="2da45-163">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="2da45-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="2da45-164">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2da45-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2da45-165">Remarks</span></span>

<span data-ttu-id="2da45-166">Класс **Win32 \_ 1394ControllerDevice** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="2da45-166">The **Win32\_1394ControllerDevice** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2da45-167">Примеры</span><span class="sxs-lookup"><span data-stu-id="2da45-167">Examples</span></span>

<span data-ttu-id="2da45-168">Следующий пример кода PowerShell извлекает сведения об устройстве контроллера 1394.</span><span class="sxs-lookup"><span data-stu-id="2da45-168">The following PowerShell code sample retrieves 1394 controller device information.</span></span>


```PowerShell
# Helper function to return AccessState

function get-WmiAccessState {
param ([uint16] $char)

# parse and return values

If ($char -le 2 -and $char -ge 0) {

switch ($char) {
0 {"00-Reserved"}
1 {"01-Reserved"}
2 {"02-Unknown"}
}
}

Else {
"$char - unknown value"
}
}

# Get 1394 Controller Device information from WMI
$1394Cont = Get-WMIObject Win32_1394ControllerDevice

# Display Details
"Win32_1394ControllerDevice WMI Information"
"=========================================="

foreach ($device in $1394Cont) {

"Device Characteristics - Device {0}" -f ++$i

"Access State : {0}" -f (Get-WmiAccessState($ch))
"Antecedent : {0}" -f $device.Antecedent
"Negotiated Data Width : {0}" -f $device.NegotiatedDataWidth
"Negotiated Speed : {0}" -f $device.NegotiatedSpeed
"Number of Hard Resets : {0}" -f $device.NumberofHardResets
"Number of Soft Resets : {0}" -f $device.NumberofSoftResets
} 
```



<span data-ttu-id="2da45-169">Предыдущий пример кода возвращает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="2da45-169">The previous code sample returns the following information:</span></span>

``` syntax
# Win32_1394ControllerDevice WMI Information

Device Characteristics -Device 1
Access State : 00-Reserved
Antecedent : \\UK0N055\root\CIMV2:Win32_1394Controller.DeviceID="PCI\\VEN_1217&DEV_00F7&SUBSYS_01CC1028
&REV_02\\4&2FE911E8&0&0CF0"
Negotiated Data Width :
Negotiated Speed :
Number of Hard Resets :
Number of Soft Resets :
```

## <a name="requirements"></a><span data-ttu-id="2da45-170">Требования</span><span class="sxs-lookup"><span data-stu-id="2da45-170">Requirements</span></span>



| <span data-ttu-id="2da45-171">Требование</span><span class="sxs-lookup"><span data-stu-id="2da45-171">Requirement</span></span> | <span data-ttu-id="2da45-172">Значение</span><span class="sxs-lookup"><span data-stu-id="2da45-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2da45-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2da45-173">Minimum supported client</span></span><br/> | <span data-ttu-id="2da45-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2da45-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2da45-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2da45-175">Minimum supported server</span></span><br/> | <span data-ttu-id="2da45-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2da45-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2da45-177">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2da45-177">Namespace</span></span><br/>                | <span data-ttu-id="2da45-178">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2da45-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2da45-179">MOF</span><span class="sxs-lookup"><span data-stu-id="2da45-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2da45-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2da45-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2da45-181">DLL</span><span class="sxs-lookup"><span data-stu-id="2da45-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2da45-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2da45-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da45-183">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2da45-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da45-184">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="2da45-184">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="2da45-185">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2da45-185">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

