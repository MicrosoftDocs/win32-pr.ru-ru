---
description: '\_Ассоциация РЕАЛИЗЕСПЕКСТЕНТ CIM представляет связь, в которой физические экстенты реализуются на физическом носителе. Кроме того, указывается начальный адрес физического экстента на физическом носителе.'
ms.assetid: 9abe1a7d-8463-4d48-8cec-52bf934ad08b
ms.tgt_platform: multiple
title: Класс CIM_RealizesPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesPExtent
- CIM_RealizesPExtent.Dependent
- CIM_RealizesPExtent.Antecedent
- CIM_RealizesPExtent.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 906861c7bc7a7e09d40d3457d069cdb9dd3a6b11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655831"
---
# <a name="cim_realizespextent-class"></a><span data-ttu-id="fcd80-104">\_Класс CIM реализеспекстент</span><span class="sxs-lookup"><span data-stu-id="fcd80-104">CIM\_RealizesPExtent class</span></span>

<span data-ttu-id="fcd80-105">Ассоциация **\_ реализеспекстент CIM** представляет связь, в которой физические экстенты реализуются на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="fcd80-105">The **CIM\_RealizesPExtent** association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="fcd80-106">Кроме того, указывается начальный адрес физического экстента на физическом носителе.</span><span class="sxs-lookup"><span data-stu-id="fcd80-106">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fcd80-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fcd80-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fcd80-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fcd80-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fcd80-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fcd80-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fcd80-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fcd80-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcd80-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcd80-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B7F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesPExtent : CIM_Realizes
{
  CIM_PhysicalExtent REF Dependent;
  CIM_PhysicalMedia  REF Antecedent;
  uint64                 StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="fcd80-112">Члены</span><span class="sxs-lookup"><span data-stu-id="fcd80-112">Members</span></span>

<span data-ttu-id="fcd80-113">Класс **CIM \_ реализеспекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fcd80-113">The **CIM\_RealizesPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="fcd80-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcd80-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcd80-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcd80-115">Properties</span></span>

<span data-ttu-id="fcd80-116">Класс **CIM \_ реализеспекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fcd80-116">The **CIM\_RealizesPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcd80-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="fcd80-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd80-118">Тип данных: **CIM \_ фисикалмедиа**</span><span class="sxs-lookup"><span data-stu-id="fcd80-118">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="fcd80-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcd80-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd80-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="fcd80-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fcd80-121">[**\_ Фисикалмедиа CIM**](cim-physicalmedia.md) , описывающий физический носитель, на котором реализован экстент.</span><span class="sxs-lookup"><span data-stu-id="fcd80-121">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="fcd80-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="fcd80-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd80-123">Тип данных: **CIM \_ фисикалекстент**</span><span class="sxs-lookup"><span data-stu-id="fcd80-123">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="fcd80-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcd80-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcd80-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="fcd80-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="fcd80-126">[**\_ Фисикалекстент CIM**](cim-physicalextent.md) , описывающий физическую область, расположенную на носителе.</span><span class="sxs-lookup"><span data-stu-id="fcd80-126">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="fcd80-127">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="fcd80-127">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcd80-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcd80-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcd80-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcd80-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcd80-130">Начальный адрес физического носителя, на котором начинается физическая область.</span><span class="sxs-lookup"><span data-stu-id="fcd80-130">Starting address on the physical media where the physical extent begins.</span></span> <span data-ttu-id="fcd80-131">Конечный адрес физического экстента определяется с **помощью свойств** **нумберофблоккс** и размерности объекта [**CIM \_ фисикалекстент**](cim-physicalextent.md) .</span><span class="sxs-lookup"><span data-stu-id="fcd80-131">The ending address of the physical extent is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_PhysicalExtent**](cim-physicalextent.md) object.</span></span>

<span data-ttu-id="fcd80-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="fcd80-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcd80-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcd80-133">Remarks</span></span>

<span data-ttu-id="fcd80-134">Класс **CIM \_ реализеспекстент** является производным от [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="fcd80-134">The **CIM\_RealizesPExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="fcd80-135">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="fcd80-135">WMI does not implement this class.</span></span>

<span data-ttu-id="fcd80-136">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fcd80-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fcd80-137">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fcd80-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcd80-138">Требования</span><span class="sxs-lookup"><span data-stu-id="fcd80-138">Requirements</span></span>



| <span data-ttu-id="fcd80-139">Требование</span><span class="sxs-lookup"><span data-stu-id="fcd80-139">Requirement</span></span> | <span data-ttu-id="fcd80-140">Значение</span><span class="sxs-lookup"><span data-stu-id="fcd80-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcd80-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcd80-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fcd80-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcd80-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fcd80-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcd80-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fcd80-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcd80-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fcd80-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fcd80-145">Namespace</span></span><br/>                | <span data-ttu-id="fcd80-146">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fcd80-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fcd80-147">MOF</span><span class="sxs-lookup"><span data-stu-id="fcd80-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcd80-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcd80-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcd80-149">DLL</span><span class="sxs-lookup"><span data-stu-id="fcd80-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcd80-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcd80-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcd80-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcd80-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcd80-152">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="fcd80-152">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

