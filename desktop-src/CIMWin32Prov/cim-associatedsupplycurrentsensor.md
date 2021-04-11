---
description: Класс CIM \_ ассоЦиатедсуппликуррентсенсор связывает источник питания с датчиком тока (ампераже), который отслеживает частоту входных данных.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: Класс CIM_AssociatedSupplyCurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262710"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a><span data-ttu-id="4835d-103">\_Класс CIM ассоЦиатедсуппликуррентсенсор</span><span class="sxs-lookup"><span data-stu-id="4835d-103">CIM\_AssociatedSupplyCurrentSensor class</span></span>

<span data-ttu-id="4835d-104">Класс **CIM \_ ассоЦиатедсуппликуррентсенсор** связывает источник питания с датчиком тока (ампераже), который отслеживает частоту входных данных.</span><span class="sxs-lookup"><span data-stu-id="4835d-104">The **CIM\_AssociatedSupplyCurrentSensor** class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4835d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="4835d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4835d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4835d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4835d-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4835d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4835d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4835d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4835d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4835d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="4835d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4835d-110">Members</span></span>

<span data-ttu-id="4835d-111">Класс **CIM \_ ассоЦиатедсуппликуррентсенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4835d-111">The **CIM\_AssociatedSupplyCurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="4835d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4835d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4835d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4835d-113">Properties</span></span>

<span data-ttu-id="4835d-114">Класс **CIM \_ ассоЦиатедсуппликуррентсенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4835d-114">The **CIM\_AssociatedSupplyCurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4835d-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4835d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4835d-116">Тип данных: **CIM \_ куррентсенсор**</span><span class="sxs-lookup"><span data-stu-id="4835d-116">Data type: **CIM\_CurrentSensor**</span></span>
</dt> <dt>

<span data-ttu-id="4835d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4835d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4835d-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4835d-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4835d-119">[**\_ Куррентсенсор CIM**](cim-currentsensor.md) , описывающий текущий датчик.</span><span class="sxs-lookup"><span data-stu-id="4835d-119">A [**CIM\_CurrentSensor**](cim-currentsensor.md) that describes the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="4835d-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="4835d-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4835d-121">Тип данных: **Источник \_ питания CIM**</span><span class="sxs-lookup"><span data-stu-id="4835d-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="4835d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4835d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4835d-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4835d-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4835d-124">Источник питания CIM, описывающий питание, связанное с текущим датчиком. [**\_**](cim-powersupply.md)</span><span class="sxs-lookup"><span data-stu-id="4835d-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="4835d-125">**мониторингранже**</span><span class="sxs-lookup"><span data-stu-id="4835d-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4835d-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4835d-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4835d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4835d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4835d-128">Указывает диапазон входных частот источника питания, измеряемый соответствующим датчиком.</span><span class="sxs-lookup"><span data-stu-id="4835d-128">Indicates the power supply input frequency range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4835d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4835d-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4835d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4835d-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="4835d-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Диапазон 1** (2)</span><span class="sxs-lookup"><span data-stu-id="4835d-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="4835d-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Диапазон 2** (3)</span><span class="sxs-lookup"><span data-stu-id="4835d-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="4835d-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Диапазоны 1 и 2** (4)</span><span class="sxs-lookup"><span data-stu-id="4835d-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4835d-134">Диапазон 1 и 2</span><span class="sxs-lookup"><span data-stu-id="4835d-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4835d-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4835d-135">Remarks</span></span>

<span data-ttu-id="4835d-136">Класс **CIM \_ ассоЦиатедсуппликуррентсенсор** является производным от [**CIM \_ ассоЦиатедсенсор**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="4835d-136">The **CIM\_AssociatedSupplyCurrentSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="4835d-137">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="4835d-137">WMI does not implement this class.</span></span>

<span data-ttu-id="4835d-138">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="4835d-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4835d-139">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="4835d-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4835d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="4835d-140">Requirements</span></span>



| <span data-ttu-id="4835d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="4835d-141">Requirement</span></span> | <span data-ttu-id="4835d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="4835d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4835d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4835d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4835d-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4835d-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4835d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4835d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4835d-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4835d-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4835d-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4835d-147">Namespace</span></span><br/>                | <span data-ttu-id="4835d-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4835d-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4835d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4835d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4835d-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4835d-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4835d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="4835d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4835d-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4835d-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4835d-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4835d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4835d-154">**\_АССОЦИАТЕДСЕНСОР CIM**</span><span class="sxs-lookup"><span data-stu-id="4835d-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

