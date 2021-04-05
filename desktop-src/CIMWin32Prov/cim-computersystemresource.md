---
description: Класс CIM \_ компутерсистемресаурце представляет связь между компьютерной системой и ее доступными системными ресурсами.
ms.assetid: 365a3cc2-89f9-4fbd-aa70-a89608fc3c1f
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemResource
- CIM_ComputerSystemResource.PartComponent
- CIM_ComputerSystemResource.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 170e92b6c31ce038f1bccc4003248b8ae86d5f79
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072479"
---
# <a name="cim_computersystemresource-class"></a><span data-ttu-id="ab103-103">\_Класс CIM компутерсистемресаурце</span><span class="sxs-lookup"><span data-stu-id="ab103-103">CIM\_ComputerSystemResource class</span></span>

<span data-ttu-id="ab103-104">Класс **CIM \_ компутерсистемресаурце** представляет связь между компьютерной системой и ее доступными системными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="ab103-104">The **CIM\_ComputerSystemResource** class represents an association between a computer system and its available system resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab103-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ab103-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ab103-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ab103-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ab103-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ab103-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ab103-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ab103-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab103-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab103-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340A-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemResource : CIM_SystemComponent
{
  CIM_SystemResource REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="ab103-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ab103-110">Members</span></span>

<span data-ttu-id="ab103-111">Класс **CIM \_ компутерсистемресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ab103-111">The **CIM\_ComputerSystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="ab103-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab103-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab103-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ab103-113">Properties</span></span>

<span data-ttu-id="ab103-114">Класс **CIM \_ компутерсистемресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ab103-114">The **CIM\_ComputerSystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ab103-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="ab103-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab103-116">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="ab103-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="ab103-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab103-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab103-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="ab103-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ab103-119">Система [**CIM \_**](cim-computersystem.md) , описывающая компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="ab103-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="ab103-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="ab103-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ab103-121">Тип данных: **CIM \_ системресаурце**</span><span class="sxs-lookup"><span data-stu-id="ab103-121">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="ab103-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ab103-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ab103-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="ab103-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="ab103-124">[**\_ Системресаурце CIM**](cim-systemresource.md) , описывающий системный ресурс компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="ab103-124">A [**CIM\_SystemResource**](cim-systemresource.md) that describes a system resource of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ab103-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab103-125">Remarks</span></span>

<span data-ttu-id="ab103-126">Класс **CIM \_ компутерсистемресаурце** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="ab103-126">The **CIM\_ComputerSystemResource** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="ab103-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ab103-127">WMI does not implement this class.</span></span> <span data-ttu-id="ab103-128">Дополнительные сведения о классах, производных от **CIM \_ компутерсистемресаурце**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ab103-128">For more information about classes derived from **CIM\_ComputerSystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ab103-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ab103-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ab103-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ab103-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab103-131">Требования</span><span class="sxs-lookup"><span data-stu-id="ab103-131">Requirements</span></span>



| <span data-ttu-id="ab103-132">Требование</span><span class="sxs-lookup"><span data-stu-id="ab103-132">Requirement</span></span> | <span data-ttu-id="ab103-133">Значение</span><span class="sxs-lookup"><span data-stu-id="ab103-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab103-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab103-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ab103-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab103-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ab103-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab103-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ab103-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab103-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ab103-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ab103-138">Namespace</span></span><br/>                | <span data-ttu-id="ab103-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ab103-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ab103-140">MOF</span><span class="sxs-lookup"><span data-stu-id="ab103-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ab103-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ab103-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ab103-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ab103-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab103-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab103-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab103-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab103-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab103-145">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ab103-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

