---
description: Класс CIM \_ линкхасконнектор связывает Кабели и ссылки, используемые в качестве физических соединителей, которые соединяют физические элементы. Эта ассоциация явно определяет связь соединителей для CIM \_ фисикаллинк.
ms.assetid: c8244b93-749a-424a-ab40-ce5ce79c8b02
ms.tgt_platform: multiple
title: Класс CIM_LinkHasConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LinkHasConnector
- CIM_LinkHasConnector.PartComponent
- CIM_LinkHasConnector.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: daeb9d07fefc4c52c7b630dcc69099c1cae429a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896006"
---
# <a name="cim_linkhasconnector-class"></a><span data-ttu-id="41c31-104">\_Класс CIM линкхасконнектор</span><span class="sxs-lookup"><span data-stu-id="41c31-104">CIM\_LinkHasConnector class</span></span>

<span data-ttu-id="41c31-105">Класс **CIM \_ линкхасконнектор** связывает Кабели и ссылки, используемые в качестве физических соединителей, которые соединяют физические элементы.</span><span class="sxs-lookup"><span data-stu-id="41c31-105">The **CIM\_LinkHasConnector** class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="41c31-106">Эта ассоциация явно определяет связь соединителей для [**CIM \_ фисикаллинк**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="41c31-106">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41c31-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="41c31-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41c31-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41c31-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41c31-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="41c31-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="41c31-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="41c31-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41c31-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41c31-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8B-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_LinkHasConnector : CIM_Component
{
  CIM_PhysicalConnector REF PartComponent;
  CIM_PhysicalLink      REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="41c31-112">Члены</span><span class="sxs-lookup"><span data-stu-id="41c31-112">Members</span></span>

<span data-ttu-id="41c31-113">Класс **CIM \_ линкхасконнектор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41c31-113">The **CIM\_LinkHasConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="41c31-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="41c31-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41c31-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="41c31-115">Properties</span></span>

<span data-ttu-id="41c31-116">Класс **CIM \_ линкхасконнектор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41c31-116">The **CIM\_LinkHasConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41c31-117">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="41c31-117">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c31-118">Тип данных: **CIM \_ фисикаллинк**</span><span class="sxs-lookup"><span data-stu-id="41c31-118">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="41c31-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c31-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c31-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="41c31-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="41c31-121">[**\_ Фисикаллинк CIM**](cim-physicallink.md) , описывающий физическую связь с соединителем.</span><span class="sxs-lookup"><span data-stu-id="41c31-121">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link that has a connector.</span></span>

</dd> <dt>

<span data-ttu-id="41c31-122">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="41c31-122">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c31-123">Тип данных: **CIM \_ фисикалконнектор**</span><span class="sxs-lookup"><span data-stu-id="41c31-123">Data type: **CIM\_PhysicalConnector**</span></span>
</dt> <dt>

<span data-ttu-id="41c31-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41c31-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41c31-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="41c31-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="41c31-126">[**\_ Фисикалконнектор CIM**](cim-physicalconnector.md) , описывающий физический соединитель.</span><span class="sxs-lookup"><span data-stu-id="41c31-126">A [**CIM\_PhysicalConnector**](cim-physicalconnector.md) that describes the physical connector.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41c31-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41c31-127">Remarks</span></span>

<span data-ttu-id="41c31-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="41c31-128">WMI does not implement this class.</span></span>

<span data-ttu-id="41c31-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="41c31-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41c31-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="41c31-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41c31-131">Требования</span><span class="sxs-lookup"><span data-stu-id="41c31-131">Requirements</span></span>



| <span data-ttu-id="41c31-132">Требование</span><span class="sxs-lookup"><span data-stu-id="41c31-132">Requirement</span></span> | <span data-ttu-id="41c31-133">Значение</span><span class="sxs-lookup"><span data-stu-id="41c31-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41c31-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41c31-134">Minimum supported client</span></span><br/> | <span data-ttu-id="41c31-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41c31-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41c31-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41c31-136">Minimum supported server</span></span><br/> | <span data-ttu-id="41c31-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41c31-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41c31-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41c31-138">Namespace</span></span><br/>                | <span data-ttu-id="41c31-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41c31-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41c31-140">MOF</span><span class="sxs-lookup"><span data-stu-id="41c31-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41c31-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41c31-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41c31-142">DLL</span><span class="sxs-lookup"><span data-stu-id="41c31-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41c31-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41c31-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c31-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41c31-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c31-145">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="41c31-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

