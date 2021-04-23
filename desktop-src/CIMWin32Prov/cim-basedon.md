---
description: Класс CIM \_ BasedOn представляет ассоциацию, которая описывает, как можно собирать экстенты хранилища из экстентов более низкого уровня.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: Класс CIM_BasedOn (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262709"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="7f6f9-103">Класс CIM_BasedOn (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7f6f9-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7f6f9-104">Класс **CIM \_ BasedOn** представляет ассоциацию, которая описывает, как можно собирать экстенты хранилища из экстентов более низкого уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="7f6f9-105">Например, физические экстенты включают экстенты защищенного пространства.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="7f6f9-106">Таким же набор томов собирается из одного или нескольких физических или защищенных экстентов.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="7f6f9-107">Память кэша может быть определена независимо и реализована в физическом элементе или на основе энергозависимых или временных экстентов хранения.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f6f9-108">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7f6f9-109">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7f6f9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7f6f9-110">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f6f9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f6f9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="7f6f9-112">Члены</span><span class="sxs-lookup"><span data-stu-id="7f6f9-112">Members</span></span>

<span data-ttu-id="7f6f9-113">Класс **CIM \_ BasedOn** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7f6f9-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="7f6f9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f6f9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7f6f9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="7f6f9-115">Properties</span></span>

<span data-ttu-id="7f6f9-116">Класс **CIM \_ BasedOn** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7f6f9-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6f9-118">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f6f9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7f6f9-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7f6f9-121">[**\_ Сторажеекстент CIM**](cim-storageextent.md) , описывающий экстент хранения нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="7f6f9-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6f9-123">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f6f9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="7f6f9-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7f6f9-126">[**\_ Сторажеекстент CIM**](cim-storageextent.md) , описывающий экстент хранения более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="7f6f9-127">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6f9-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f6f9-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6f9-130">Указывает конец высокоуровневого экстента в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="7f6f9-131">Это свойство полезно при сопоставлении несмежных экстентов с группировкой более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="7f6f9-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7f6f9-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7f6f9-133">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7f6f9-134">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7f6f9-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7f6f9-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7f6f9-136">Указывает начало экстента высокого уровня в хранилище нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="7f6f9-137">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7f6f9-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f6f9-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7f6f9-138">Remarks</span></span>

<span data-ttu-id="7f6f9-139">Класс **CIM \_ BasedOn** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7f6f9-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7f6f9-140">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-140">WMI does not implement this class.</span></span>

<span data-ttu-id="7f6f9-141">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7f6f9-142">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7f6f9-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f6f9-143">Требования</span><span class="sxs-lookup"><span data-stu-id="7f6f9-143">Requirements</span></span>



| <span data-ttu-id="7f6f9-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7f6f9-144">Requirement</span></span> | <span data-ttu-id="7f6f9-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7f6f9-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f6f9-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f6f9-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7f6f9-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7f6f9-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7f6f9-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f6f9-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7f6f9-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7f6f9-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7f6f9-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7f6f9-150">Namespace</span></span><br/>                | <span data-ttu-id="7f6f9-151">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7f6f9-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7f6f9-152">MOF</span><span class="sxs-lookup"><span data-stu-id="7f6f9-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f6f9-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7f6f9-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f6f9-154">DLL</span><span class="sxs-lookup"><span data-stu-id="7f6f9-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f6f9-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f6f9-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f6f9-156">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f6f9-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f6f9-157">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="7f6f9-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

