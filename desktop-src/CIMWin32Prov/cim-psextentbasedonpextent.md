---
description: Класс CIM \_ псекстентбаседонпекстент связывает экстенты защищенного пространства, основанные на физическом экстенте.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: Класс CIM_PSExtentBasedOnPExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141434"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="58f39-103">\_Класс CIM псекстентбаседонпекстент</span><span class="sxs-lookup"><span data-stu-id="58f39-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="58f39-104">Класс **CIM \_ псекстентбаседонпекстент** связывает экстенты защищенного пространства, основанные на физическом экстенте.</span><span class="sxs-lookup"><span data-stu-id="58f39-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58f39-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="58f39-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="58f39-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="58f39-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="58f39-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="58f39-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="58f39-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="58f39-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f39-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58f39-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="58f39-110">Члены</span><span class="sxs-lookup"><span data-stu-id="58f39-110">Members</span></span>

<span data-ttu-id="58f39-111">Класс **CIM \_ псекстентбаседонпекстент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58f39-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="58f39-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="58f39-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="58f39-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="58f39-113">Properties</span></span>

<span data-ttu-id="58f39-114">Класс **CIM \_ псекстентбаседонпекстент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58f39-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58f39-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="58f39-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f39-116">Тип данных: **CIM \_ фисикалекстент**</span><span class="sxs-lookup"><span data-stu-id="58f39-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="58f39-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58f39-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f39-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="58f39-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="58f39-119">[**\_ Фисикалекстент CIM**](cim-physicalextent.md) , описывающий физическую область.</span><span class="sxs-lookup"><span data-stu-id="58f39-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="58f39-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="58f39-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f39-121">Тип данных: **CIM \_ протектедспацеекстент**</span><span class="sxs-lookup"><span data-stu-id="58f39-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="58f39-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58f39-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58f39-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="58f39-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="58f39-124">[**\_ Протектедспацеекстент CIM**](cim-protectedspaceextent.md) , описывающий область защищенного пространства, созданную на основе физического экстента.</span><span class="sxs-lookup"><span data-stu-id="58f39-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="58f39-125">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="58f39-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f39-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58f39-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58f39-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58f39-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f39-128">Указывает конец высокоуровневого экстента в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="58f39-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="58f39-129">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="58f39-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="58f39-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="58f39-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="58f39-131">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="58f39-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="58f39-132">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="58f39-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58f39-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="58f39-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="58f39-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58f39-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58f39-135">Указывает начало экстента высокого уровня в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="58f39-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="58f39-136">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="58f39-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="58f39-137">Это свойство наследуется от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="58f39-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="58f39-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58f39-138">Remarks</span></span>

<span data-ttu-id="58f39-139">Класс **CIM \_ псекстентбаседонпекстент** является производным от [**CIM \_ BasedOn**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="58f39-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="58f39-140">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="58f39-140">WMI does not implement this class.</span></span>

<span data-ttu-id="58f39-141">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="58f39-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="58f39-142">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="58f39-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f39-143">Требования</span><span class="sxs-lookup"><span data-stu-id="58f39-143">Requirements</span></span>



| <span data-ttu-id="58f39-144">Требование</span><span class="sxs-lookup"><span data-stu-id="58f39-144">Requirement</span></span> | <span data-ttu-id="58f39-145">Значение</span><span class="sxs-lookup"><span data-stu-id="58f39-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58f39-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58f39-146">Minimum supported client</span></span><br/> | <span data-ttu-id="58f39-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58f39-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58f39-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58f39-148">Minimum supported server</span></span><br/> | <span data-ttu-id="58f39-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58f39-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58f39-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58f39-150">Namespace</span></span><br/>                | <span data-ttu-id="58f39-151">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="58f39-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="58f39-152">MOF</span><span class="sxs-lookup"><span data-stu-id="58f39-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f39-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58f39-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="58f39-154">DLL</span><span class="sxs-lookup"><span data-stu-id="58f39-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f39-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f39-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f39-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58f39-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f39-157">**\_BASEDON CIM**</span><span class="sxs-lookup"><span data-stu-id="58f39-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

