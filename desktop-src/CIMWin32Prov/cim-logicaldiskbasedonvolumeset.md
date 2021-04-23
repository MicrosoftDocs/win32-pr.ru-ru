---
description: '\_Ассоциация ЛОГИКАЛДИСКБАСЕДОНВОЛУМЕСЕТ CIM связывает логические диски с томом, на котором они находятся. Логические диски могут быть основаны на одном томе (например, предоставленном диспетчером программных томов) или в разделе диска.'
ms.assetid: 15a588c9-a6b0-4393-927f-8e8818315542
ms.tgt_platform: multiple
title: Класс CIM_LogicalDiskBasedOnVolumeSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnVolumeSet
- CIM_LogicalDiskBasedOnVolumeSet.EndingAddress
- CIM_LogicalDiskBasedOnVolumeSet.StartingAddress
- CIM_LogicalDiskBasedOnVolumeSet.Dependent
- CIM_LogicalDiskBasedOnVolumeSet.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2af4c141fe0b64979c6fb6e5b7b0e6068d018d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141087"
---
# <a name="cim_logicaldiskbasedonvolumeset-class"></a><span data-ttu-id="0c62a-104">\_Класс CIM логикалдискбаседонволумесет</span><span class="sxs-lookup"><span data-stu-id="0c62a-104">CIM\_LogicalDiskBasedOnVolumeSet class</span></span>

<span data-ttu-id="0c62a-105">Ассоциация **\_ логикалдискбаседонволумесет CIM** связывает логические диски с томом, на котором они находятся.</span><span class="sxs-lookup"><span data-stu-id="0c62a-105">The **CIM\_LogicalDiskBasedOnVolumeSet** association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="0c62a-106">Логические диски могут быть основаны на одном томе (например, предоставленном диспетчером программных томов) или в разделе диска.</span><span class="sxs-lookup"><span data-stu-id="0c62a-106">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0c62a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0c62a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0c62a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0c62a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0c62a-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0c62a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0c62a-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0c62a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c62a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c62a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3A608798-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_LogicalDiskBasedOnVolumeSet : CIM_BasedOn
{
  uint64              EndingAddress;
  uint64              StartingAddress;
  CIM_LogicalDisk REF Dependent;
  CIM_VolumeSet   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="0c62a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="0c62a-112">Members</span></span>

<span data-ttu-id="0c62a-113">Класс **CIM \_ логикалдискбаседонволумесет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0c62a-113">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these types of members:</span></span>

-   [<span data-ttu-id="0c62a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c62a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c62a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0c62a-115">Properties</span></span>

<span data-ttu-id="0c62a-116">Класс **CIM \_ логикалдискбаседонволумесет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0c62a-116">The **CIM\_LogicalDiskBasedOnVolumeSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c62a-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0c62a-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c62a-118">Тип данных: **" \_ том CIM** "</span><span class="sxs-lookup"><span data-stu-id="0c62a-118">Data type: **CIM\_VolumeSet**</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c62a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-120">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="0c62a-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0c62a-121">Набор [**\_ томов CIM**](cim-volumeset.md) с описанием набора томов.</span><span class="sxs-lookup"><span data-stu-id="0c62a-121">A [**CIM\_VolumeSet**](cim-volumeset.md) that describes the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="0c62a-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="0c62a-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c62a-123">Тип данных: **CIM \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="0c62a-123">Data type: **CIM\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c62a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="0c62a-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0c62a-126">Логический [**\_ логический диск CIM**](cim-logicaldisk.md) , описывающий логические диски, созданные на основе набора томов.</span><span class="sxs-lookup"><span data-stu-id="0c62a-126">A [**CIM\_LogicalDisk**](cim-logicaldisk.md) that describes the logical disk which is built on the volume set.</span></span>

</dd> <dt>

<span data-ttu-id="0c62a-127">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="0c62a-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c62a-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c62a-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c62a-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c62a-130">Указывает конец высокоуровневого экстента в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="0c62a-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="0c62a-131">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="0c62a-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="0c62a-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c62a-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0c62a-133">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="0c62a-133">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="0c62a-134">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="0c62a-134">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c62a-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0c62a-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0c62a-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0c62a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c62a-137">Указывает начало экстента высокого уровня в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="0c62a-137">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="0c62a-138">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="0c62a-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="0c62a-139">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="0c62a-139">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c62a-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c62a-140">Remarks</span></span>

<span data-ttu-id="0c62a-141">Класс **CIM \_ логикалдискбаседонволумесет** является производным от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="0c62a-141">The **CIM\_LogicalDiskBasedOnVolumeSet** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="0c62a-142">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0c62a-142">WMI does not implement this class.</span></span>

<span data-ttu-id="0c62a-143">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0c62a-143">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0c62a-144">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0c62a-144">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c62a-145">Требования</span><span class="sxs-lookup"><span data-stu-id="0c62a-145">Requirements</span></span>



| <span data-ttu-id="0c62a-146">Требование</span><span class="sxs-lookup"><span data-stu-id="0c62a-146">Requirement</span></span> | <span data-ttu-id="0c62a-147">Значение</span><span class="sxs-lookup"><span data-stu-id="0c62a-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c62a-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c62a-148">Minimum supported client</span></span><br/> | <span data-ttu-id="0c62a-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0c62a-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0c62a-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c62a-150">Minimum supported server</span></span><br/> | <span data-ttu-id="0c62a-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0c62a-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0c62a-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0c62a-152">Namespace</span></span><br/>                | <span data-ttu-id="0c62a-153">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0c62a-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0c62a-154">MOF</span><span class="sxs-lookup"><span data-stu-id="0c62a-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c62a-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c62a-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c62a-156">DLL</span><span class="sxs-lookup"><span data-stu-id="0c62a-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c62a-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c62a-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c62a-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c62a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c62a-159">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="0c62a-159">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

