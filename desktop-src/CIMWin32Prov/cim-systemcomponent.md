---
description: Класс ассоциации модель CIM (CIM), устанавливающий связи между системой и управляемыми системными элементами, из которых она состоит.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: Класс CIM_SystemComponent (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141929"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="19796-103">Класс CIM_SystemComponent (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="19796-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="19796-104">Класс **CIM \_ системкомпонент** — это класс ассоциации модель CIM (CIM), который устанавливает связи между системой и управляемыми системными элементами, из которых она состоит.</span><span class="sxs-lookup"><span data-stu-id="19796-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19796-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="19796-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="19796-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="19796-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="19796-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="19796-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="19796-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="19796-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19796-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19796-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="19796-110">Члены</span><span class="sxs-lookup"><span data-stu-id="19796-110">Members</span></span>

<span data-ttu-id="19796-111">Класс **CIM \_ системкомпонент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="19796-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="19796-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="19796-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19796-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="19796-113">Properties</span></span>

<span data-ttu-id="19796-114">Класс **CIM \_ системкомпонент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="19796-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19796-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="19796-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19796-116">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="19796-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="19796-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19796-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19796-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="19796-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="19796-119">[**\_ Система CIM**](cim-system.md) , которая описывает родительскую систему в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="19796-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="19796-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="19796-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19796-121">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="19796-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="19796-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="19796-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19796-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="19796-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="19796-124">[**\_ Манажедсистемелемент CIM**](cim-managedsystemelement.md) , описывающий дочерний элемент, являющийся компонентом системы.</span><span class="sxs-lookup"><span data-stu-id="19796-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19796-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="19796-125">Remarks</span></span>

<span data-ttu-id="19796-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="19796-126">WMI does not implement this class.</span></span> <span data-ttu-id="19796-127">Классы WMI, производные от **CIM \_ системкомпонент**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="19796-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="19796-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="19796-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19796-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="19796-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19796-130">Требования</span><span class="sxs-lookup"><span data-stu-id="19796-130">Requirements</span></span>



| <span data-ttu-id="19796-131">Требование</span><span class="sxs-lookup"><span data-stu-id="19796-131">Requirement</span></span> | <span data-ttu-id="19796-132">Значение</span><span class="sxs-lookup"><span data-stu-id="19796-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19796-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="19796-133">Minimum supported client</span></span><br/> | <span data-ttu-id="19796-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19796-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19796-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="19796-135">Minimum supported server</span></span><br/> | <span data-ttu-id="19796-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19796-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19796-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="19796-137">Namespace</span></span><br/>                | <span data-ttu-id="19796-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="19796-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19796-139">MOF</span><span class="sxs-lookup"><span data-stu-id="19796-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19796-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19796-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19796-141">DLL</span><span class="sxs-lookup"><span data-stu-id="19796-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19796-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19796-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19796-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19796-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19796-144">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="19796-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

