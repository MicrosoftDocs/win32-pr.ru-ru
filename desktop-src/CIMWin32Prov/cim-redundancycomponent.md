---
description: Класс CIM \_ редунданцикомпонент связывает группу избыточности, состоящую из управляемых системных элементов, и указывает, что вместе элементы обеспечивают избыточность.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Класс CIM_RedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895414"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="e321f-103">\_Класс CIM редунданцикомпонент</span><span class="sxs-lookup"><span data-stu-id="e321f-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="e321f-104">Класс **CIM \_ редунданцикомпонент** связывает группу избыточности, состоящую из управляемых системных элементов, и указывает, что вместе элементы обеспечивают избыточность.</span><span class="sxs-lookup"><span data-stu-id="e321f-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="e321f-105">Все элементы, Объединенные в группу избыточности, должны быть экземплярами одного и того же класса объектов.</span><span class="sxs-lookup"><span data-stu-id="e321f-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e321f-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e321f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e321f-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e321f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e321f-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e321f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e321f-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e321f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e321f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e321f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e321f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e321f-111">Members</span></span>

<span data-ttu-id="e321f-112">Класс **CIM \_ редунданцикомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e321f-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e321f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e321f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e321f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e321f-114">Properties</span></span>

<span data-ttu-id="e321f-115">Класс **CIM \_ редунданцикомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e321f-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e321f-116">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="e321f-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e321f-117">Тип данных: **CIM \_ редунданциграуп**</span><span class="sxs-lookup"><span data-stu-id="e321f-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="e321f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e321f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e321f-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e321f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e321f-120">Ассоциация **\_ редунданцикомпонент CIM** указывает, что "Этот набор вентиляторов" или "эти физические экстенты" участвуют в одной группе избыточности.</span><span class="sxs-lookup"><span data-stu-id="e321f-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="e321f-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e321f-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e321f-122">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="e321f-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e321f-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e321f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e321f-124">[**\_ Манажедсистемелемент CIM**](cim-managedsystemelement.md) , описывающий дочерний элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="e321f-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="e321f-125">Это свойство наследуется [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="e321f-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e321f-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e321f-126">Remarks</span></span>

<span data-ttu-id="e321f-127">**Модель CIM \_ Редунданцикомпонент** является производным [**от \_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="e321f-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="e321f-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e321f-128">WMI does not implement this class.</span></span>

<span data-ttu-id="e321f-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e321f-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e321f-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e321f-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e321f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e321f-131">Requirements</span></span>



| <span data-ttu-id="e321f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e321f-132">Requirement</span></span> | <span data-ttu-id="e321f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e321f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e321f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e321f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e321f-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e321f-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e321f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e321f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e321f-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e321f-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e321f-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e321f-138">Namespace</span></span><br/>                | <span data-ttu-id="e321f-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e321f-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e321f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e321f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e321f-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e321f-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e321f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e321f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e321f-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e321f-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e321f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e321f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e321f-145">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="e321f-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

