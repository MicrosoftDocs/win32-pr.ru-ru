---
description: Класс CIM \_ пекстентредунданцикомпонент представляет физические экстенты, участвующие в группе избыточности хранилища.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Класс CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495954"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="cc85c-103">\_Класс CIM пекстентредунданцикомпонент</span><span class="sxs-lookup"><span data-stu-id="cc85c-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="cc85c-104">Класс **CIM \_ пекстентредунданцикомпонент** представляет физические экстенты, участвующие в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc85c-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc85c-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="cc85c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc85c-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc85c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc85c-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="cc85c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cc85c-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="cc85c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc85c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc85c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="cc85c-110">Члены</span><span class="sxs-lookup"><span data-stu-id="cc85c-110">Members</span></span>

<span data-ttu-id="cc85c-111">Класс **CIM \_ пекстентредунданцикомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cc85c-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="cc85c-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="cc85c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc85c-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="cc85c-113">Properties</span></span>

<span data-ttu-id="cc85c-114">Класс **CIM \_ пекстентредунданцикомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cc85c-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc85c-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="cc85c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc85c-116">Тип данных: **CIM \_ сторажередунданциграуп**</span><span class="sxs-lookup"><span data-stu-id="cc85c-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="cc85c-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cc85c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc85c-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="cc85c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cc85c-119">[**\_ Сторажередунданциграуп CIM**](cim-storageredundancygroup.md) , описывающий группу избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="cc85c-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="cc85c-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cc85c-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc85c-121">Тип данных: **CIM \_ фисикалекстент**</span><span class="sxs-lookup"><span data-stu-id="cc85c-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="cc85c-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="cc85c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc85c-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="cc85c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cc85c-124">[**\_ Фисикалекстент CIM**](cim-physicalextent.md) , описывающий физическое пространство, участвующее в группе избыточности.</span><span class="sxs-lookup"><span data-stu-id="cc85c-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc85c-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cc85c-125">Remarks</span></span>

<span data-ttu-id="cc85c-126">Класс **CIM \_ пекстентредунданцикомпонент** является производным от [**CIM \_ редунданцикомпонент**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cc85c-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="cc85c-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="cc85c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="cc85c-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc85c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc85c-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="cc85c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc85c-130">Требования</span><span class="sxs-lookup"><span data-stu-id="cc85c-130">Requirements</span></span>



| <span data-ttu-id="cc85c-131">Требование</span><span class="sxs-lookup"><span data-stu-id="cc85c-131">Requirement</span></span> | <span data-ttu-id="cc85c-132">Значение</span><span class="sxs-lookup"><span data-stu-id="cc85c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc85c-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cc85c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cc85c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc85c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc85c-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cc85c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cc85c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc85c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc85c-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cc85c-137">Namespace</span></span><br/>                | <span data-ttu-id="cc85c-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cc85c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc85c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="cc85c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc85c-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc85c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc85c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="cc85c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc85c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc85c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc85c-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cc85c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc85c-144">**\_РЕДУНДАНЦИКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="cc85c-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

