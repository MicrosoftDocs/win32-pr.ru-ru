---
description: Представляет отношение CIM \_ контролледби, указывающее, к каким устройствам осуществляется доступ через контроллер SCSI и характеристики доступа.
ms.assetid: a036dbf9-f9ce-4c85-9184-fefcbe4583ba
ms.tgt_platform: multiple
title: Класс CIM_SCSIInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIInterface
- CIM_SCSIInterface.NegotiatedDataWidth
- CIM_SCSIInterface.NegotiatedSpeed
- CIM_SCSIInterface.AccessState
- CIM_SCSIInterface.NumberOfHardResets
- CIM_SCSIInterface.NumberOfSoftResets
- CIM_SCSIInterface.Dependent
- CIM_SCSIInterface.Antecedent
- CIM_SCSIInterface.SCSIRetries
- CIM_SCSIInterface.SCSITimeouts
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1211b142681f15aa8b4d5e61c1d2165a59f5a62c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807595"
---
# <a name="cim_scsiinterface-class"></a><span data-ttu-id="a104d-103">\_Класс CIM сксиинтерфаце</span><span class="sxs-lookup"><span data-stu-id="a104d-103">CIM\_SCSIInterface class</span></span>

<span data-ttu-id="a104d-104">Класс **CIM \_ сксиинтерфаце** представляет отношение [**CIM \_ контролледби**](cim-controlledby.md) , указывающее, к каким устройствам осуществляется доступ через контроллер SCSI и характеристики доступа.</span><span class="sxs-lookup"><span data-stu-id="a104d-104">The **CIM\_SCSIInterface** class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a104d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a104d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a104d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a104d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a104d-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a104d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a104d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a104d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a104d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a104d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{7CE7448E-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SCSIInterface : CIM_ControlledBy
{
  uint32                 NegotiatedDataWidth;
  uint64                 NegotiatedSpeed;
  uint16                 AccessState;
  uint32                 NumberOfHardResets;
  uint32                 NumberOfSoftResets;
  CIM_LogicalDevice  REF Dependent;
  CIM_SCSIController REF Antecedent;
  uint32                 SCSIRetries;
  uint32                 SCSITimeouts;
};
```

## <a name="members"></a><span data-ttu-id="a104d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="a104d-110">Members</span></span>

<span data-ttu-id="a104d-111">Класс **CIM \_ сксиинтерфаце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a104d-111">The **CIM\_SCSIInterface** class has these types of members:</span></span>

-   [<span data-ttu-id="a104d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="a104d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a104d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a104d-113">Properties</span></span>

<span data-ttu-id="a104d-114">Класс **CIM \_ сксиинтерфаце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a104d-114">The **CIM\_SCSIInterface** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a104d-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="a104d-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a104d-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a104d-118">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="a104d-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="a104d-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="a104d-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="a104d-120">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a104d-121">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="a104d-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="a104d-122">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="a104d-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="a104d-123">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="a104d-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a104d-124">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="a104d-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-125">Тип данных: **CIM \_ сксиконтроллер**</span><span class="sxs-lookup"><span data-stu-id="a104d-125">Data type: **CIM\_SCSIController**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a104d-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a104d-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a104d-128">[**\_ Сксиконтроллер CIM**](cim-scsicontroller.md) , описывающий контроллер SCSI.</span><span class="sxs-lookup"><span data-stu-id="a104d-128">A [**CIM\_SCSIController**](cim-scsicontroller.md) that describes the SCSI controller.</span></span>

</dd> <dt>

<span data-ttu-id="a104d-129">**Него**</span><span class="sxs-lookup"><span data-stu-id="a104d-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-130">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="a104d-130">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a104d-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="a104d-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a104d-133">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="a104d-133">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="a104d-134">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="a104d-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a104d-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a104d-137">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="a104d-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="a104d-138">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="a104d-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="a104d-139">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="a104d-139">Data width is specified in bits.</span></span> <span data-ttu-id="a104d-140">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="a104d-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a104d-141">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="a104d-142">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="a104d-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a104d-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a104d-145">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="a104d-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="a104d-146">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="a104d-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="a104d-147">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="a104d-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="a104d-148">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="a104d-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="a104d-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a104d-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="a104d-150">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="a104d-151">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="a104d-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a104d-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a104d-154">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="a104d-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="a104d-155">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="a104d-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="a104d-156">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="a104d-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="a104d-157">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="a104d-158">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="a104d-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a104d-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a104d-161">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="a104d-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="a104d-162">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="a104d-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="a104d-163">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="a104d-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="a104d-164">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="a104d-165">**сксиретриес**</span><span class="sxs-lookup"><span data-stu-id="a104d-165">**SCSIRetries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-166">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a104d-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a104d-168">Количество повторных попыток SCSI, произошедших с момента последнего жесткого или мягкого сброса, связанных с управляемым устройством.</span><span class="sxs-lookup"><span data-stu-id="a104d-168">Number of SCSI retries that have occurred since the last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="a104d-169">Время последнего сброса указывается в свойстве **тимеофдевицересет** , унаследованном от ассоциации [**\_ контролледби CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="a104d-169">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> <dt>

<span data-ttu-id="a104d-170">**скситимеаутс**</span><span class="sxs-lookup"><span data-stu-id="a104d-170">**SCSITimeouts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a104d-171">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a104d-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a104d-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a104d-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a104d-173">Число тайм-аутов SCSI, произошедших с момента последнего жесткого или мягкого сброса, связанных с управляемым устройством.</span><span class="sxs-lookup"><span data-stu-id="a104d-173">Number of SCSI time-outs that occurred since last hard or soft reset related to the controlled device.</span></span> <span data-ttu-id="a104d-174">Время последнего сброса указывается в свойстве **тимеофдевицересет** , унаследованном от ассоциации [**\_ контролледби CIM**](cim-controlledby.md) .</span><span class="sxs-lookup"><span data-stu-id="a104d-174">The time of the last reset is indicated in the **TimeOfDeviceReset** property, inherited from the [**CIM\_ControlledBy**](cim-controlledby.md) association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a104d-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a104d-175">Remarks</span></span>

<span data-ttu-id="a104d-176">Класс **CIM \_ сксиинтерфаце** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="a104d-176">The **CIM\_SCSIInterface** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="a104d-177">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a104d-177">WMI does not implement this class.</span></span>

<span data-ttu-id="a104d-178">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a104d-178">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a104d-179">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a104d-179">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a104d-180">Требования</span><span class="sxs-lookup"><span data-stu-id="a104d-180">Requirements</span></span>



| <span data-ttu-id="a104d-181">Требование</span><span class="sxs-lookup"><span data-stu-id="a104d-181">Requirement</span></span> | <span data-ttu-id="a104d-182">Значение</span><span class="sxs-lookup"><span data-stu-id="a104d-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a104d-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a104d-183">Minimum supported client</span></span><br/> | <span data-ttu-id="a104d-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a104d-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a104d-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a104d-185">Minimum supported server</span></span><br/> | <span data-ttu-id="a104d-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a104d-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a104d-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a104d-187">Namespace</span></span><br/>                | <span data-ttu-id="a104d-188">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a104d-188">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a104d-189">MOF</span><span class="sxs-lookup"><span data-stu-id="a104d-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a104d-190"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a104d-190"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a104d-191">DLL</span><span class="sxs-lookup"><span data-stu-id="a104d-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a104d-192"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a104d-192"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a104d-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a104d-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a104d-194">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="a104d-194">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

