---
description: Класс CIM \_ аггрегатередунданцикомпонент описывает совокупную физическую область в группе избыточности хранилища.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: Класс CIM_AggregateRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807685"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="5747b-103">\_Класс CIM аггрегатередунданцикомпонент</span><span class="sxs-lookup"><span data-stu-id="5747b-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="5747b-104">Класс **CIM \_ аггрегатередунданцикомпонент** описывает совокупную физическую область в группе избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="5747b-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5747b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="5747b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5747b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5747b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5747b-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="5747b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5747b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="5747b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5747b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5747b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5747b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="5747b-110">Members</span></span>

<span data-ttu-id="5747b-111">Класс **CIM \_ аггрегатередунданцикомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5747b-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="5747b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="5747b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5747b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="5747b-113">Properties</span></span>

<span data-ttu-id="5747b-114">Класс **CIM \_ аггрегатередунданцикомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5747b-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5747b-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="5747b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5747b-116">Тип данных: **CIM \_ сторажередунданциграуп**</span><span class="sxs-lookup"><span data-stu-id="5747b-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="5747b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5747b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5747b-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5747b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5747b-119">[**\_ Сторажередунданциграуп CIM**](cim-storageredundancygroup.md) , которая содержит группу избыточности хранилища.</span><span class="sxs-lookup"><span data-stu-id="5747b-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="5747b-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5747b-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5747b-121">Тип данных: **CIM \_ аггрегатепекстент**</span><span class="sxs-lookup"><span data-stu-id="5747b-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="5747b-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5747b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5747b-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5747b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5747b-124">[**\_ Аггрегатепекстент CIM**](cim-aggregatepextent.md) , который содержит объединенные физические экстенты, участвующие в группе избыточности.</span><span class="sxs-lookup"><span data-stu-id="5747b-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5747b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5747b-125">Remarks</span></span>

<span data-ttu-id="5747b-126">Класс **CIM \_ аггрегатередунданцикомпонент** является производным от [**CIM \_ редунданцикомпонент**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="5747b-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="5747b-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="5747b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5747b-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="5747b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5747b-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="5747b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5747b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="5747b-130">Requirements</span></span>



| <span data-ttu-id="5747b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="5747b-131">Requirement</span></span> | <span data-ttu-id="5747b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="5747b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5747b-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5747b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5747b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5747b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5747b-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5747b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5747b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5747b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5747b-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5747b-137">Namespace</span></span><br/>                | <span data-ttu-id="5747b-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5747b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5747b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5747b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5747b-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5747b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5747b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5747b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5747b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5747b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5747b-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5747b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5747b-144">**\_РЕДУНДАНЦИКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="5747b-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

