---
description: Класс CIM \_ логикалдискбаседонпартитион связывает логический диск с разделом диска, на котором он находится.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: Класс CIM_LogicalDiskBasedOnPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538504"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a><span data-ttu-id="55a9d-103">\_Класс CIM логикалдискбаседонпартитион</span><span class="sxs-lookup"><span data-stu-id="55a9d-103">CIM\_LogicalDiskBasedOnPartition class</span></span>

<span data-ttu-id="55a9d-104">Класс **CIM \_ логикалдискбаседонпартитион** связывает логический диск с разделом диска, на котором он находится.</span><span class="sxs-lookup"><span data-stu-id="55a9d-104">The **CIM\_LogicalDiskBasedOnPartition** class associates a logical disk with the disk partition on which it resides.</span></span>

<span data-ttu-id="55a9d-105">Например, диск C может находиться в разделе на локальном физическом носителе, что указывает на то, что логический диск не может охватывать более одной секции.</span><span class="sxs-lookup"><span data-stu-id="55a9d-105">For example, a computer's drive C can be located on a partition on local physical media, which dictates that a logical disk cannot span more than one partition.</span></span> <span data-ttu-id="55a9d-106">Если логический диск может охватывать более одной секции, логический диск основан на конфигурации RAID (например, зеркальном или чередующемся наборе).</span><span class="sxs-lookup"><span data-stu-id="55a9d-106">When a logical disk can span more than one partition, however, the logical disk is based on RAID configuration (for example, a mirror or stripe set).</span></span> <span data-ttu-id="55a9d-107">В этом случае логический диск основан на томе хранилища.</span><span class="sxs-lookup"><span data-stu-id="55a9d-107">In which case, the logical disk is based on storage volume.</span></span> <span data-ttu-id="55a9d-108">Чтобы предотвратить неправильное использование ассоциации **\_ логикалдискбаседонпартитион CIM** , квалификатор **Max (1)** помещается в ссылку **Antecedent** на раздел диска.</span><span class="sxs-lookup"><span data-stu-id="55a9d-108">To prevent using the **CIM\_LogicalDiskBasedOnPartition** association incorrectly, the **Max(1)** qualifier was put on the **Antecedent** reference to the disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="55a9d-109">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="55a9d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="55a9d-110">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="55a9d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="55a9d-111">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="55a9d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="55a9d-112">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="55a9d-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a9d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55a9d-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="55a9d-114">Члены</span><span class="sxs-lookup"><span data-stu-id="55a9d-114">Members</span></span>

<span data-ttu-id="55a9d-115">Класс **CIM \_ логикалдискбаседонпартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55a9d-115">The **CIM\_LogicalDiskBasedOnPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="55a9d-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="55a9d-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55a9d-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="55a9d-117">Properties</span></span>

<span data-ttu-id="55a9d-118">Класс **CIM \_ логикалдискбаседонпартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="55a9d-118">The **CIM\_LogicalDiskBasedOnPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55a9d-119">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="55a9d-119">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9d-120">Тип данных: **CIM \_ дискпартитион**</span><span class="sxs-lookup"><span data-stu-id="55a9d-120">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55a9d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="55a9d-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="55a9d-123">[**\_ Дискпартитион CIM**](cim-diskpartition.md) , описывающий раздел диска.</span><span class="sxs-lookup"><span data-stu-id="55a9d-123">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition.</span></span>

</dd> <dt>

<span data-ttu-id="55a9d-124">**Него**</span><span class="sxs-lookup"><span data-stu-id="55a9d-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9d-125">Тип данных: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="55a9d-125">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55a9d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-127">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="55a9d-127">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="55a9d-128">Логический [**\_ логический диск CIM**](cim-logicaldisk.md) , описывающий логические диски, созданные на основе секции.</span><span class="sxs-lookup"><span data-stu-id="55a9d-128">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the partition.</span></span>

</dd> <dt>

<span data-ttu-id="55a9d-129">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="55a9d-129">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9d-130">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55a9d-130">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55a9d-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55a9d-132">Указывает конец высокоуровневого экстента в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="55a9d-132">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="55a9d-133">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="55a9d-133">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="55a9d-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55a9d-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="55a9d-135">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="55a9d-135">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="55a9d-136">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="55a9d-136">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a9d-137">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55a9d-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55a9d-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="55a9d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55a9d-139">Указывает начало экстента высокого уровня в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="55a9d-139">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="55a9d-140">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="55a9d-140">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="55a9d-141">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="55a9d-141">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55a9d-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55a9d-142">Remarks</span></span>

<span data-ttu-id="55a9d-143">Класс **CIM \_ логикалдискбаседонпартитион** является производным от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="55a9d-143">The **CIM\_LogicalDiskBasedOnPartition** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="55a9d-144">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="55a9d-144">WMI does not implement this class.</span></span> <span data-ttu-id="55a9d-145">Классы, производные от **CIM \_ логикалдискбаседонпартитион**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="55a9d-145">For classes derived from **CIM\_LogicalDiskBasedOnPartition**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="55a9d-146">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="55a9d-146">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="55a9d-147">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="55a9d-147">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="55a9d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="55a9d-148">Requirements</span></span>



| <span data-ttu-id="55a9d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="55a9d-149">Requirement</span></span> | <span data-ttu-id="55a9d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="55a9d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55a9d-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55a9d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="55a9d-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55a9d-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55a9d-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55a9d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="55a9d-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55a9d-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55a9d-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55a9d-155">Namespace</span></span><br/>                | <span data-ttu-id="55a9d-156">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55a9d-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55a9d-157">MOF</span><span class="sxs-lookup"><span data-stu-id="55a9d-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55a9d-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55a9d-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55a9d-159">DLL</span><span class="sxs-lookup"><span data-stu-id="55a9d-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a9d-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a9d-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a9d-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55a9d-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a9d-162">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="55a9d-162">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

