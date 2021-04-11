---
description: Связывает источник питания с датчиком напряжения, отслеживающим свое входное напряжение.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: Класс CIM_AssociatedSupplyVoltageSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142085"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="04ff2-103">\_Класс CIM ассоЦиатедсуппливолтажесенсор</span><span class="sxs-lookup"><span data-stu-id="04ff2-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="04ff2-104">Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** связывает источник питания с датчиком напряжения, отслеживающим свое входное напряжение.</span><span class="sxs-lookup"><span data-stu-id="04ff2-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04ff2-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="04ff2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="04ff2-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="04ff2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="04ff2-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="04ff2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="04ff2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="04ff2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="04ff2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04ff2-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="04ff2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="04ff2-110">Members</span></span>

<span data-ttu-id="04ff2-111">Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="04ff2-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="04ff2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="04ff2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="04ff2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="04ff2-113">Properties</span></span>

<span data-ttu-id="04ff2-114">Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="04ff2-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04ff2-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="04ff2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ff2-116">Тип данных: **CIM \_ датчик напряжения**</span><span class="sxs-lookup"><span data-stu-id="04ff2-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="04ff2-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="04ff2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ff2-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="04ff2-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="04ff2-119">[**\_ Датчик напряжения CIM**](cim-voltagesensor.md) , описывающий датчик напряжения.</span><span class="sxs-lookup"><span data-stu-id="04ff2-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="04ff2-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="04ff2-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ff2-121">Тип данных: **Источник \_ питания CIM**</span><span class="sxs-lookup"><span data-stu-id="04ff2-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="04ff2-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="04ff2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="04ff2-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="04ff2-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="04ff2-124">Источник питания CIM, описывающий питание, связанное с датчиком напряжения. [**\_**](cim-powersupply.md)</span><span class="sxs-lookup"><span data-stu-id="04ff2-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="04ff2-125">**мониторингранже**</span><span class="sxs-lookup"><span data-stu-id="04ff2-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04ff2-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="04ff2-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="04ff2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="04ff2-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04ff2-128">Указывает диапазон входного напряжения источника питания, измеряемый соответствующим датчиком.</span><span class="sxs-lookup"><span data-stu-id="04ff2-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="04ff2-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="04ff2-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="04ff2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="04ff2-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="04ff2-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Диапазон 1** (2)</span><span class="sxs-lookup"><span data-stu-id="04ff2-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="04ff2-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Диапазон 2** (3)</span><span class="sxs-lookup"><span data-stu-id="04ff2-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="04ff2-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Диапазоны 1 и 2** (4)</span><span class="sxs-lookup"><span data-stu-id="04ff2-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="04ff2-134">Диапазон 1 и 2</span><span class="sxs-lookup"><span data-stu-id="04ff2-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="04ff2-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="04ff2-135">Remarks</span></span>

<span data-ttu-id="04ff2-136">Класс **CIM \_ ассоЦиатедсуппливолтажесенсор** является производным от [**CIM \_ ассоЦиатедсенсор**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="04ff2-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="04ff2-137">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="04ff2-137">WMI does not implement this class.</span></span>

<span data-ttu-id="04ff2-138">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="04ff2-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="04ff2-139">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="04ff2-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="04ff2-140">Требования</span><span class="sxs-lookup"><span data-stu-id="04ff2-140">Requirements</span></span>



| <span data-ttu-id="04ff2-141">Требование</span><span class="sxs-lookup"><span data-stu-id="04ff2-141">Requirement</span></span> | <span data-ttu-id="04ff2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="04ff2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="04ff2-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04ff2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="04ff2-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04ff2-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="04ff2-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04ff2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="04ff2-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04ff2-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="04ff2-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="04ff2-147">Namespace</span></span><br/>                | <span data-ttu-id="04ff2-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="04ff2-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="04ff2-149">MOF</span><span class="sxs-lookup"><span data-stu-id="04ff2-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04ff2-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04ff2-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="04ff2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="04ff2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04ff2-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04ff2-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04ff2-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04ff2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04ff2-154">**\_АССОЦИАТЕДСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="04ff2-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

