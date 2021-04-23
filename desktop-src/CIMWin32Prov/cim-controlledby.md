---
description: Отношение CIM \_ контролледби указывает, какие устройства отправляются логическим устройством контроллера или к которым осуществляется доступ через.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: Класс CIM_ControlledBy (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895801"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a><span data-ttu-id="3c057-103">Класс CIM_ControlledBy (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3c057-103">CIM_ControlledBy class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3c057-104">Отношение **CIM \_ контролледби** указывает, какие устройства отправляются логическим устройством контроллера или к которым осуществляется доступ через.</span><span class="sxs-lookup"><span data-stu-id="3c057-104">The **CIM\_ControlledBy** relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c057-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="3c057-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3c057-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3c057-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3c057-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c057-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3c057-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3c057-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c057-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c057-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="3c057-110">Члены</span><span class="sxs-lookup"><span data-stu-id="3c057-110">Members</span></span>

<span data-ttu-id="3c057-111">Класс **CIM \_ контролледби** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3c057-111">The **CIM\_ControlledBy** class has these types of members:</span></span>

-   [<span data-ttu-id="3c057-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c057-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c057-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3c057-113">Properties</span></span>

<span data-ttu-id="3c057-114">Класс **CIM \_ контролледби** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3c057-114">The **CIM\_ControlledBy** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c057-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="3c057-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3c057-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c057-118">Указывает, является ли контроллер активной командой или доступом к устройству.</span><span class="sxs-lookup"><span data-stu-id="3c057-118">Indicates whether the controller is actively commanding or accessing the device.</span></span> <span data-ttu-id="3c057-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="3c057-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="3c057-120">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="3c057-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="3c057-121">**Активно** (1)</span><span class="sxs-lookup"><span data-stu-id="3c057-121">**Active** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="3c057-122">**Неактивно** (2)</span><span class="sxs-lookup"><span data-stu-id="3c057-122">**Inactive** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3c057-123">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="3c057-123">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-124">Тип данных: **CIM \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="3c057-124">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c057-126">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3c057-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3c057-127">[**CIM- \_ контроллер**](cim-controller.md) , представляющий контроллер.</span><span class="sxs-lookup"><span data-stu-id="3c057-127">A [**CIM\_Controller**](cim-controller.md) that represents the controller.</span></span>

</dd> <dt>

<span data-ttu-id="3c057-128">**Него**</span><span class="sxs-lookup"><span data-stu-id="3c057-128">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-129">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="3c057-129">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c057-131">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="3c057-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3c057-132">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , представляющее управляемое устройство.</span><span class="sxs-lookup"><span data-stu-id="3c057-132">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the controlled device.</span></span>

</dd> <dt>

<span data-ttu-id="3c057-133">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="3c057-133">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c057-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c057-136">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("биты")</span><span class="sxs-lookup"><span data-stu-id="3c057-136">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="3c057-137">Если возможно несколько значений ширины данных для шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="3c057-137">When several bus or connection-data widths are possible, this property defines the one in use between the devices.</span></span> <span data-ttu-id="3c057-138">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="3c057-138">Data width is specified in bits.</span></span> <span data-ttu-id="3c057-139">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="3c057-139">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="3c057-140">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="3c057-140">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c057-141">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="3c057-141">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-142">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3c057-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c057-144">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("бит в секунду")</span><span class="sxs-lookup"><span data-stu-id="3c057-144">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="3c057-145">Если возможны несколько скоростей шины или соединения, это свойство определяет, какое из них используется между устройствами.</span><span class="sxs-lookup"><span data-stu-id="3c057-145">When several bus or connection speeds are possible, this property defines the one being used between the devices.</span></span> <span data-ttu-id="3c057-146">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="3c057-146">Speed is specified in bits-per-second.</span></span> <span data-ttu-id="3c057-147">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="3c057-147">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="3c057-148">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="3c057-148">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="3c057-149">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="3c057-149">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c057-150">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="3c057-150">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-151">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c057-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c057-153">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="3c057-153">Number of hard resets issued by the controller.</span></span> <span data-ttu-id="3c057-154">При жесткой сбросе устройство возвращается в состояние инициализации или загрузки.</span><span class="sxs-lookup"><span data-stu-id="3c057-154">A hard reset returns the device to its initialization or boot-up state.</span></span> <span data-ttu-id="3c057-155">Все внутренние сведения о состоянии устройства и данные теряются.</span><span class="sxs-lookup"><span data-stu-id="3c057-155">All internal device state information and data are lost.</span></span>

</dd> <dt>

<span data-ttu-id="3c057-156">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="3c057-156">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c057-157">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c057-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c057-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3c057-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c057-159">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="3c057-159">Number of soft resets issued by the controller.</span></span> <span data-ttu-id="3c057-160">При мягком сбросе текущее состояние и данные устройства не полностью очищаются.</span><span class="sxs-lookup"><span data-stu-id="3c057-160">A soft reset does not completely clear current device state and data.</span></span> <span data-ttu-id="3c057-161">Точная семантика зависит от устройства и от протоколов и механизмов, используемых для связи с ним.</span><span class="sxs-lookup"><span data-stu-id="3c057-161">Exact semantics are dependent on the device and on the protocols and mechanisms used to communicate to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c057-162">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c057-162">Remarks</span></span>

<span data-ttu-id="3c057-163">Класс **CIM \_ контролледби** является производным от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="3c057-163">The **CIM\_ControlledBy** class is derived from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="3c057-164">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="3c057-164">WMI does not implement this class.</span></span> <span data-ttu-id="3c057-165">Дополнительные сведения о классах, производных от **CIM \_ контролледби**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3c057-165">For more information about classes derived from **CIM\_ControlledBy**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3c057-166">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="3c057-166">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3c057-167">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3c057-167">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c057-168">Требования</span><span class="sxs-lookup"><span data-stu-id="3c057-168">Requirements</span></span>



| <span data-ttu-id="3c057-169">Требование</span><span class="sxs-lookup"><span data-stu-id="3c057-169">Requirement</span></span> | <span data-ttu-id="3c057-170">Значение</span><span class="sxs-lookup"><span data-stu-id="3c057-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c057-171">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c057-171">Minimum supported client</span></span><br/> | <span data-ttu-id="3c057-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c057-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c057-173">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c057-173">Minimum supported server</span></span><br/> | <span data-ttu-id="3c057-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c057-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c057-175">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3c057-175">Namespace</span></span><br/>                | <span data-ttu-id="3c057-176">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3c057-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3c057-177">MOF</span><span class="sxs-lookup"><span data-stu-id="3c057-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c057-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c057-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c057-179">DLL</span><span class="sxs-lookup"><span data-stu-id="3c057-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c057-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c057-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c057-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c057-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c057-182">**\_ДЕВИЦЕКОННЕКТИОН CIM**</span><span class="sxs-lookup"><span data-stu-id="3c057-182">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> </dl>

 

