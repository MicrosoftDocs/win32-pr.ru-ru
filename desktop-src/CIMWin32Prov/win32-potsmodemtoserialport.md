---
description: '\_Класс WMI взаимосвязей Win32 потсмодемтосериалпорт связывает модем с последовательным портом, используемым модемом.'
ms.assetid: 4dbde5ae-f785-4d2d-80d9-508effd72cf2
ms.tgt_platform: multiple
title: Класс Win32_POTSModemToSerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_POTSModemToSerialPort
- Win32_POTSModemToSerialPort.NegotiatedDataWidth
- Win32_POTSModemToSerialPort.NegotiatedSpeed
- Win32_POTSModemToSerialPort.AccessState
- Win32_POTSModemToSerialPort.NumberOfHardResets
- Win32_POTSModemToSerialPort.NumberOfSoftResets
- Win32_POTSModemToSerialPort.Dependent
- Win32_POTSModemToSerialPort.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a1e6128ffde7afce0132dd4415e4eca1f06b5cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655876"
---
# <a name="win32_potsmodemtoserialport-class"></a><span data-ttu-id="f1999-103">\_Класс Win32 потсмодемтосериалпорт</span><span class="sxs-lookup"><span data-stu-id="f1999-103">Win32\_POTSModemToSerialPort class</span></span>

<span data-ttu-id="f1999-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ потсмодемтосериалпорт** связывает модем с последовательным портом, используемым модемом.</span><span class="sxs-lookup"><span data-stu-id="f1999-104">The **Win32\_POTSModemToSerialPort** association [WMI class](../wmisdk/retrieving-a-class.md) relates a modem to the serial port the modem uses.</span></span>

<span data-ttu-id="f1999-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f1999-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f1999-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f1999-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1999-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1999-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4B6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_POTSModemToSerialPort : CIM_ControlledBy
{
  uint32               NegotiatedDataWidth;
  uint64               NegotiatedSpeed;
  uint16               AccessState;
  uint32               NumberOfHardResets;
  uint32               NumberOfSoftResets;
  Win32_POTSModem  REF Dependent;
  Win32_SerialPort REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="f1999-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f1999-108">Members</span></span>

<span data-ttu-id="f1999-109">Класс **Win32 \_ потсмодемтосериалпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f1999-109">The **Win32\_POTSModemToSerialPort** class has these types of members:</span></span>

-   [<span data-ttu-id="f1999-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1999-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1999-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f1999-111">Properties</span></span>

<span data-ttu-id="f1999-112">Класс **Win32 \_ потсмодемтосериалпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f1999-112">The **Win32\_POTSModemToSerialPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1999-113">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="f1999-113">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-114">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1999-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1999-116">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="f1999-116">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="f1999-117">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="f1999-117">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="f1999-118">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-118">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f1999-119">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="f1999-119">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="f1999-120">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="f1999-120">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="f1999-121">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="f1999-121">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f1999-122">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f1999-122">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-123">Тип данных: **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="f1999-123">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1999-125">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="f1999-125">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="f1999-126">[**Win32 \_ SerialPort**](win32-serialport.md) , представляющий последовательный порт, используемый модемом.</span><span class="sxs-lookup"><span data-stu-id="f1999-126">A [**Win32\_SerialPort**](win32-serialport.md) that represents the serial port used by the modem.</span></span>

</dd> <dt>

<span data-ttu-id="f1999-127">**Него**</span><span class="sxs-lookup"><span data-stu-id="f1999-127">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-128">Тип данных: **Win32 \_ потсмодем**</span><span class="sxs-lookup"><span data-stu-id="f1999-128">Data type: **Win32\_POTSModem**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1999-130">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ потсмодем")</span><span class="sxs-lookup"><span data-stu-id="f1999-130">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_POTSModem")</span></span>
</dt> </dl>

<span data-ttu-id="f1999-131">[**\_ Потсмодем Win32**](win32-potsmodem.md) , представляющий POTS-модем, использующий последовательный порт.</span><span class="sxs-lookup"><span data-stu-id="f1999-131">A [**Win32\_POTSModem**](win32-potsmodem.md) that represents the POTS modem using the serial port.</span></span>

</dd> <dt>

<span data-ttu-id="f1999-132">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="f1999-132">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1999-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1999-135">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("биты")</span><span class="sxs-lookup"><span data-stu-id="f1999-135">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="f1999-136">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="f1999-136">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="f1999-137">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="f1999-137">Data width is specified in bits.</span></span> <span data-ttu-id="f1999-138">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f1999-138">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="f1999-139">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-139">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1999-140">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="f1999-140">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-141">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1999-141">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1999-143">Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="f1999-143">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="f1999-144">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="f1999-144">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="f1999-145">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="f1999-145">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="f1999-146">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="f1999-146">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="f1999-147">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-147">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="f1999-148">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-148">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1999-149">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="f1999-149">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-150">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1999-150">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1999-152">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="f1999-152">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="f1999-153">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="f1999-153">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="f1999-154">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="f1999-154">All internal device state information and data are lost.</span></span>

<span data-ttu-id="f1999-155">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-155">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1999-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="f1999-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1999-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1999-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1999-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f1999-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1999-159">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="f1999-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="f1999-160">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="f1999-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="f1999-161">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="f1999-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="f1999-162">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-162">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1999-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f1999-163">Remarks</span></span>

<span data-ttu-id="f1999-164">Класс **Win32 \_ потсмодемтосериалпорт** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="f1999-164">The **Win32\_POTSModemToSerialPort** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1999-165">Требования</span><span class="sxs-lookup"><span data-stu-id="f1999-165">Requirements</span></span>



| <span data-ttu-id="f1999-166">Требование</span><span class="sxs-lookup"><span data-stu-id="f1999-166">Requirement</span></span> | <span data-ttu-id="f1999-167">Значение</span><span class="sxs-lookup"><span data-stu-id="f1999-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1999-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1999-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f1999-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1999-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1999-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1999-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f1999-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1999-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1999-172">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f1999-172">Namespace</span></span><br/>                | <span data-ttu-id="f1999-173">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f1999-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f1999-174">MOF</span><span class="sxs-lookup"><span data-stu-id="f1999-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1999-175"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1999-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1999-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f1999-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1999-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1999-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1999-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1999-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1999-179">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="f1999-179">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="f1999-180">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="f1999-180">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
