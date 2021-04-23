---
description: Класс CIM \_ реализесдискпартитион представляет раздел диска на физическом носителе, который моделирует создание разделов на необработанном диске SCSI или IDE.
ms.assetid: cc317f7d-06cd-4126-8123-6a3eb32f792e
ms.tgt_platform: multiple
title: Класс CIM_RealizesDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesDiskPartition
- CIM_RealizesDiskPartition.Dependent
- CIM_RealizesDiskPartition.Antecedent
- CIM_RealizesDiskPartition.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d138aafd179f5fefa40896fe4b9e6a0426b34422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141431"
---
# <a name="cim_realizesdiskpartition-class"></a><span data-ttu-id="89b35-103">\_Класс CIM реализесдискпартитион</span><span class="sxs-lookup"><span data-stu-id="89b35-103">CIM\_RealizesDiskPartition class</span></span>

<span data-ttu-id="89b35-104">Класс **CIM \_ реализесдискпартитион** представляет раздел диска на физическом носителе, который моделирует создание разделов на необработанном диске SCSI или IDE.</span><span class="sxs-lookup"><span data-stu-id="89b35-104">The **CIM\_RealizesDiskPartition** class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89b35-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="89b35-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89b35-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89b35-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89b35-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="89b35-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="89b35-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="89b35-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b35-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="89b35-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B80-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesDiskPartition : CIM_Realizes
{
  CIM_DiskPartition REF Dependent;
  CIM_PhysicalMedia REF Antecedent;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="89b35-110">Члены</span><span class="sxs-lookup"><span data-stu-id="89b35-110">Members</span></span>

<span data-ttu-id="89b35-111">Класс **CIM \_ реализесдискпартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="89b35-111">The **CIM\_RealizesDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="89b35-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="89b35-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89b35-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="89b35-113">Properties</span></span>

<span data-ttu-id="89b35-114">Класс **CIM \_ реализесдискпартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="89b35-114">The **CIM\_RealizesDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89b35-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="89b35-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b35-116">Тип данных: **CIM \_ фисикалмедиа**</span><span class="sxs-lookup"><span data-stu-id="89b35-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="89b35-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89b35-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b35-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="89b35-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="89b35-119">[**\_ Фисикалмедиа CIM**](cim-physicalmedia.md) , описывающий физический носитель, на котором реализован экстент.</span><span class="sxs-lookup"><span data-stu-id="89b35-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="89b35-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="89b35-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b35-121">Тип данных: **CIM \_ дискпартитион**</span><span class="sxs-lookup"><span data-stu-id="89b35-121">Data type: **CIM\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="89b35-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89b35-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89b35-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="89b35-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="89b35-124">[**\_ Дискпартитион CIM**](cim-diskpartition.md) , описывающий раздел диска, расположенный на носителе.</span><span class="sxs-lookup"><span data-stu-id="89b35-124">A [**CIM\_DiskPartition**](cim-diskpartition.md) that describes the disk partition that is located on the media.</span></span>

</dd> <dt>

<span data-ttu-id="89b35-125">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="89b35-125">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89b35-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="89b35-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="89b35-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="89b35-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89b35-128">Начальный адрес на физическом носителе, с которого начинается раздел диска.</span><span class="sxs-lookup"><span data-stu-id="89b35-128">Starting address on the physical media where the disk partition begins.</span></span> <span data-ttu-id="89b35-129">Конечный адрес секции определяется с **помощью свойств** **нумберофблоккс** и размерности объекта [**CIM \_ дискпартитион**](cim-diskpartition.md) .</span><span class="sxs-lookup"><span data-stu-id="89b35-129">The partition's ending address is determined using the **NumberOfBlocks** and **BlockSize** properties of the [**CIM\_DiskPartition**](cim-diskpartition.md) object.</span></span>

<span data-ttu-id="89b35-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="89b35-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89b35-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89b35-131">Remarks</span></span>

<span data-ttu-id="89b35-132">Класс **CIM \_ реализесдискпартитион** является производным от [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="89b35-132">The **CIM\_RealizesDiskPartition** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="89b35-133">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="89b35-133">WMI does not implement this class.</span></span>

<span data-ttu-id="89b35-134">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="89b35-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89b35-135">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="89b35-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b35-136">Требования</span><span class="sxs-lookup"><span data-stu-id="89b35-136">Requirements</span></span>



| <span data-ttu-id="89b35-137">Требование</span><span class="sxs-lookup"><span data-stu-id="89b35-137">Requirement</span></span> | <span data-ttu-id="89b35-138">Значение</span><span class="sxs-lookup"><span data-stu-id="89b35-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89b35-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89b35-139">Minimum supported client</span></span><br/> | <span data-ttu-id="89b35-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89b35-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89b35-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89b35-141">Minimum supported server</span></span><br/> | <span data-ttu-id="89b35-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89b35-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89b35-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="89b35-143">Namespace</span></span><br/>                | <span data-ttu-id="89b35-144">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="89b35-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89b35-145">MOF</span><span class="sxs-lookup"><span data-stu-id="89b35-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89b35-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89b35-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89b35-147">DLL</span><span class="sxs-lookup"><span data-stu-id="89b35-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89b35-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89b35-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b35-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89b35-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b35-150">**\_Реализации CIM**</span><span class="sxs-lookup"><span data-stu-id="89b35-150">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

