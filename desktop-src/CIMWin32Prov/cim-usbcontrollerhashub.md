---
description: Класс CIM \_ усбконтроллерхашуб определяет концентраторы, расположенные на контроллере USB.
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: Класс CIM_USBControllerHasHub
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140870"
---
# <a name="cim_usbcontrollerhashub-class"></a><span data-ttu-id="e241a-103">\_Класс CIM усбконтроллерхашуб</span><span class="sxs-lookup"><span data-stu-id="e241a-103">CIM\_USBControllerHasHub class</span></span>

<span data-ttu-id="e241a-104">Класс **CIM \_ усбконтроллерхашуб** определяет концентраторы, расположенные на контроллере USB.</span><span class="sxs-lookup"><span data-stu-id="e241a-104">The **CIM\_USBControllerHasHub** class defines the hubs that are downstream of the USB controller.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e241a-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e241a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e241a-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e241a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e241a-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e241a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e241a-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e241a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e241a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e241a-109">Syntax</span></span>

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="e241a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e241a-110">Members</span></span>

<span data-ttu-id="e241a-111">Класс **CIM \_ усбконтроллерхашуб** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e241a-111">The **CIM\_USBControllerHasHub** class has these types of members:</span></span>

-   [<span data-ttu-id="e241a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e241a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e241a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e241a-113">Properties</span></span>

<span data-ttu-id="e241a-114">Класс **CIM \_ усбконтроллерхашуб** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e241a-114">The **CIM\_USBControllerHasHub** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e241a-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="e241a-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e241a-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e241a-118">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="e241a-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="e241a-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="e241a-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="e241a-120">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e241a-121">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="e241a-121">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="e241a-122">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="e241a-122">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="e241a-123">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="e241a-123">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e241a-124">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="e241a-124">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-125">Тип данных: **CIM \_ усбконтроллер**</span><span class="sxs-lookup"><span data-stu-id="e241a-125">Data type: **CIM\_USBController**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e241a-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e241a-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e241a-128">[**\_ Усбконтроллер CIM**](cim-usbcontroller.md) , описывающий усбконтроллер.</span><span class="sxs-lookup"><span data-stu-id="e241a-128">A [**CIM\_USBController**](cim-usbcontroller.md) describing the USBController.</span></span>

</dd> <dt>

<span data-ttu-id="e241a-129">**Него**</span><span class="sxs-lookup"><span data-stu-id="e241a-129">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-130">Тип данных: **CIM \_ усбхуб**</span><span class="sxs-lookup"><span data-stu-id="e241a-130">Data type: **CIM\_USBHub**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e241a-132">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="e241a-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="e241a-133">[**\_ Усбхуб CIM**](cim-usbhub.md) , описывающий усбхуб, связанный с контроллером.</span><span class="sxs-lookup"><span data-stu-id="e241a-133">A [**CIM\_USBHub**](cim-usbhub.md) describing the USBHub that is associated with the Controller.</span></span>

</dd> <dt>

<span data-ttu-id="e241a-134">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="e241a-134">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-135">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e241a-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e241a-137">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="e241a-137">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="e241a-138">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="e241a-138">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="e241a-139">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="e241a-139">Data width is specified in bits.</span></span> <span data-ttu-id="e241a-140">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e241a-140">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e241a-141">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-141">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e241a-142">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="e241a-142">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e241a-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e241a-145">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="e241a-145">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="e241a-146">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="e241a-146">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="e241a-147">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="e241a-147">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="e241a-148">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e241a-148">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="e241a-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="e241a-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="e241a-150">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-150">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="e241a-151">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="e241a-151">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-152">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e241a-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e241a-154">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="e241a-154">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="e241a-155">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="e241a-155">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="e241a-156">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="e241a-156">All internal device state information and data are lost.</span></span>

<span data-ttu-id="e241a-157">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-157">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="e241a-158">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="e241a-158">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e241a-159">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e241a-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e241a-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e241a-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e241a-161">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="e241a-161">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="e241a-162">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="e241a-162">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="e241a-163">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="e241a-163">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

<span data-ttu-id="e241a-164">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-164">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e241a-165">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e241a-165">Remarks</span></span>

<span data-ttu-id="e241a-166">Класс **CIM \_ усбконтроллерхашуб** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-166">The **CIM\_USBControllerHasHub** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<span data-ttu-id="e241a-167">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e241a-167">WMI does not implement this class.</span></span> <span data-ttu-id="e241a-168">Классы WMI, производные от **CIM \_ усбконтроллерхашуб**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e241a-168">For WMI classes derived from **CIM\_USBControllerHasHub**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e241a-169">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e241a-169">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e241a-170">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e241a-170">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e241a-171">Требования</span><span class="sxs-lookup"><span data-stu-id="e241a-171">Requirements</span></span>



| <span data-ttu-id="e241a-172">Требование</span><span class="sxs-lookup"><span data-stu-id="e241a-172">Requirement</span></span> | <span data-ttu-id="e241a-173">Значение</span><span class="sxs-lookup"><span data-stu-id="e241a-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e241a-174">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e241a-174">Minimum supported client</span></span><br/> | <span data-ttu-id="e241a-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e241a-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e241a-176">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e241a-176">Minimum supported server</span></span><br/> | <span data-ttu-id="e241a-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e241a-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e241a-178">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e241a-178">Namespace</span></span><br/>                | <span data-ttu-id="e241a-179">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e241a-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e241a-180">MOF</span><span class="sxs-lookup"><span data-stu-id="e241a-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e241a-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e241a-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e241a-182">DLL</span><span class="sxs-lookup"><span data-stu-id="e241a-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e241a-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e241a-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e241a-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e241a-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e241a-185">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="e241a-185">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> </dl>

 

