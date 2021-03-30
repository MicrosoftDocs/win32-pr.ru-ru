---
description: '\_Класс WMI взаимосвязей Win32 принтерконтроллер связывает принтер и локальное устройство, к которому подключен принтер. Обратите внимание, что этот класс возвращает только экземпляры для локальных принтеров.'
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Класс Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895946"
---
# <a name="win32_printercontroller-class"></a><span data-ttu-id="823ea-104">\_Класс Win32 принтерконтроллер</span><span class="sxs-lookup"><span data-stu-id="823ea-104">Win32\_PrinterController class</span></span>

<span data-ttu-id="823ea-105">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ принтерконтроллер** связывает принтер и локальное устройство, к которому подключен принтер.</span><span class="sxs-lookup"><span data-stu-id="823ea-105">The **Win32\_PrinterController** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and the local device to which the printer is connected.</span></span> <span data-ttu-id="823ea-106">Обратите внимание, что этот класс возвращает только экземпляры для локальных принтеров.</span><span class="sxs-lookup"><span data-stu-id="823ea-106">Note that this class only returns instances for local printers.</span></span>

<span data-ttu-id="823ea-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="823ea-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="823ea-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="823ea-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="823ea-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="823ea-109">Syntax</span></span>

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a><span data-ttu-id="823ea-110">Члены</span><span class="sxs-lookup"><span data-stu-id="823ea-110">Members</span></span>

<span data-ttu-id="823ea-111">Класс **Win32 \_ принтерконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="823ea-111">The **Win32\_PrinterController** class has these types of members:</span></span>

-   [<span data-ttu-id="823ea-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="823ea-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="823ea-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="823ea-113">Properties</span></span>

<span data-ttu-id="823ea-114">Класс **Win32 \_ принтерконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="823ea-114">The **Win32\_PrinterController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="823ea-115">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="823ea-115">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="823ea-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ea-118">Состояние доступа контроллера к устройству.</span><span class="sxs-lookup"><span data-stu-id="823ea-118">State of the controller access to the device.</span></span> <span data-ttu-id="823ea-119">Эти сведения необходимы в том случае, если логическое устройство может быть командо или доступно через несколько контроллеров.</span><span class="sxs-lookup"><span data-stu-id="823ea-119">This information is necessary when a logical device can be commanded by, or accessed through, multiple controllers.</span></span>

<span data-ttu-id="823ea-120">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-120">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="823ea-121"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="823ea-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="823ea-122">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="823ea-122">Unknown</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="823ea-123"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="823ea-123"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="823ea-124">Активна</span><span class="sxs-lookup"><span data-stu-id="823ea-124">Active</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="823ea-125"><span id="2"></span>**открыт**</span><span class="sxs-lookup"><span data-stu-id="823ea-125"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="823ea-126">Неактивно</span><span class="sxs-lookup"><span data-stu-id="823ea-126">Inactive</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="823ea-127">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="823ea-127">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-128">Тип данных: **CIM \_ Controller**</span><span class="sxs-lookup"><span data-stu-id="823ea-128">Data type: **CIM\_Controller**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823ea-130">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="823ea-130">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="823ea-131">Ссылка на экземпляр [**\_ контроллера CIM**](cim-controller.md) , представляющий локальное устройство, связанное с этим принтером.</span><span class="sxs-lookup"><span data-stu-id="823ea-131">Reference to the [**CIM\_Controller**](cim-controller.md) instance representing the local device associated with this printer.</span></span>

<span data-ttu-id="823ea-132">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-132">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="823ea-133">**Него**</span><span class="sxs-lookup"><span data-stu-id="823ea-133">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-134">Тип данных: **\_ принтер Win32**</span><span class="sxs-lookup"><span data-stu-id="823ea-134">Data type: **Win32\_Printer**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="823ea-136">Квалификаторы: [ **ключ**](../wmisdk/standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="823ea-136">Qualifiers: [**Key**](../wmisdk/standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="823ea-137">Ссылка на экземпляр [**\_ принтера Win32**](win32-printer.md) , представляющий принтер, связанный с локальным устройством.</span><span class="sxs-lookup"><span data-stu-id="823ea-137">Reference to the [**Win32\_Printer**](win32-printer.md) instance representing the printer associated with the local device.</span></span>

<span data-ttu-id="823ea-138">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-138">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="823ea-139">**неготиатеддатавидс**</span><span class="sxs-lookup"><span data-stu-id="823ea-139">**NegotiatedDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-140">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="823ea-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ea-142">Ширина данных, используемая между устройствами (если возможны несколько значений ширины данных для шины или соединения).</span><span class="sxs-lookup"><span data-stu-id="823ea-142">Data width in use between devices (when several bus or connection data widths are possible).</span></span> <span data-ttu-id="823ea-143">Ширина данных указывается в битах.</span><span class="sxs-lookup"><span data-stu-id="823ea-143">Data width is specified in bits.</span></span> <span data-ttu-id="823ea-144">Если ширина данных не согласована или если эта информация недоступна или важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="823ea-144">If data width is not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="823ea-145">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-145">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

</dd> <dt>

<span data-ttu-id="823ea-146">**неготиатедспид**</span><span class="sxs-lookup"><span data-stu-id="823ea-146">**NegotiatedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-147">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="823ea-147">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ea-149">Скорость использования между устройствами (если возможно несколько шин или скорость соединения).</span><span class="sxs-lookup"><span data-stu-id="823ea-149">Speed in use between devices (when several bus or connection speeds are possible).</span></span> <span data-ttu-id="823ea-150">Скорость указывается в битах в секунду.</span><span class="sxs-lookup"><span data-stu-id="823ea-150">Speed is specified in bits per second.</span></span> <span data-ttu-id="823ea-151">Если скорость подключения или шины не согласована или если эта информация недоступна или не важна для управления устройствами, свойство должно иметь значение 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="823ea-151">If connection or bus speeds are not negotiated, or if this information is not available or important to device management, the property should be set to 0 (zero).</span></span>

<span data-ttu-id="823ea-152">Это свойство наследуется от [**CIM \_ девицеконнектион**](cim-deviceconnection.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-152">This property is inherited from [**CIM\_DeviceConnection**](cim-deviceconnection.md).</span></span>

<span data-ttu-id="823ea-153">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="823ea-154">**нумберофхардресетс**</span><span class="sxs-lookup"><span data-stu-id="823ea-154">**NumberOfHardResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="823ea-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ea-157">Число жестких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="823ea-157">Number of hard resets issued by the controller.</span></span>

<span data-ttu-id="823ea-158">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-158">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> <dt>

<span data-ttu-id="823ea-159">**нумберофсофтресетс**</span><span class="sxs-lookup"><span data-stu-id="823ea-159">**NumberOfSoftResets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="823ea-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="823ea-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="823ea-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="823ea-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="823ea-162">Количество мягких сбросов, выданных контроллером.</span><span class="sxs-lookup"><span data-stu-id="823ea-162">Number of soft resets issued by the controller.</span></span>

<span data-ttu-id="823ea-163">Это свойство наследуется от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-163">This property is inherited from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="823ea-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="823ea-164">Remarks</span></span>

<span data-ttu-id="823ea-165">Класс **Win32 \_ принтерконтроллер** является производным от [**CIM \_ контролледби**](cim-controlledby.md).</span><span class="sxs-lookup"><span data-stu-id="823ea-165">The **Win32\_PrinterController** class is derived from [**CIM\_ControlledBy**](cim-controlledby.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="823ea-166">Требования</span><span class="sxs-lookup"><span data-stu-id="823ea-166">Requirements</span></span>



| <span data-ttu-id="823ea-167">Требование</span><span class="sxs-lookup"><span data-stu-id="823ea-167">Requirement</span></span> | <span data-ttu-id="823ea-168">Значение</span><span class="sxs-lookup"><span data-stu-id="823ea-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="823ea-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="823ea-169">Minimum supported client</span></span><br/> | <span data-ttu-id="823ea-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="823ea-170">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="823ea-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="823ea-171">Minimum supported server</span></span><br/> | <span data-ttu-id="823ea-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="823ea-172">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="823ea-173">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="823ea-173">Namespace</span></span><br/>                | <span data-ttu-id="823ea-174">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="823ea-174">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="823ea-175">MOF</span><span class="sxs-lookup"><span data-stu-id="823ea-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="823ea-176"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="823ea-176"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="823ea-177">DLL</span><span class="sxs-lookup"><span data-stu-id="823ea-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="823ea-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="823ea-178"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="823ea-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="823ea-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="823ea-180">**\_КОНТРОЛЛЕДБИ CIM**</span><span class="sxs-lookup"><span data-stu-id="823ea-180">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dt>

[<span data-ttu-id="823ea-181">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="823ea-181">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
