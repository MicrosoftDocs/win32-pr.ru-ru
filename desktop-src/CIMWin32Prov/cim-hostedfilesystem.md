---
description: Ассоциация CIM \_ хостедфилесистем представляет собой связь между компьютерной системой и файловой системой, размещенной в компьютерной системе.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: Класс CIM_HostedFileSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141725"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="41727-103">\_Класс CIM хостедфилесистем</span><span class="sxs-lookup"><span data-stu-id="41727-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="41727-104">Ассоциация **CIM \_ хостедфилесистем** представляет собой связь между компьютерной системой и файловой системой, размещенной в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="41727-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41727-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="41727-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="41727-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="41727-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="41727-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="41727-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="41727-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="41727-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="41727-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41727-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="41727-110">Члены</span><span class="sxs-lookup"><span data-stu-id="41727-110">Members</span></span>

<span data-ttu-id="41727-111">Класс **CIM \_ хостедфилесистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="41727-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="41727-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="41727-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41727-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="41727-113">Properties</span></span>

<span data-ttu-id="41727-114">Класс **CIM \_ хостедфилесистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="41727-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41727-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="41727-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41727-116">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="41727-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="41727-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41727-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41727-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="41727-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="41727-119">Система [**CIM \_**](cim-computersystem.md) , описывающая компьютерную систему.</span><span class="sxs-lookup"><span data-stu-id="41727-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="41727-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="41727-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41727-121">Тип данных: **\_ Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="41727-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="41727-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="41727-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41727-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="41727-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="41727-124">Система [**CIM \_**](cim-filesystem.md) , которая описывает файловую систему, принадлежащую компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="41727-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41727-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41727-125">Remarks</span></span>

<span data-ttu-id="41727-126">Класс **CIM \_ хостедфилесистем** является производным от [**CIM \_ системкомпонент**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="41727-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="41727-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="41727-127">WMI does not implement this class.</span></span>

<span data-ttu-id="41727-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="41727-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="41727-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="41727-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="41727-130">Требования</span><span class="sxs-lookup"><span data-stu-id="41727-130">Requirements</span></span>



| <span data-ttu-id="41727-131">Требование</span><span class="sxs-lookup"><span data-stu-id="41727-131">Requirement</span></span> | <span data-ttu-id="41727-132">Значение</span><span class="sxs-lookup"><span data-stu-id="41727-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41727-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41727-133">Minimum supported client</span></span><br/> | <span data-ttu-id="41727-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41727-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="41727-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41727-135">Minimum supported server</span></span><br/> | <span data-ttu-id="41727-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41727-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="41727-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="41727-137">Namespace</span></span><br/>                | <span data-ttu-id="41727-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="41727-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="41727-139">MOF</span><span class="sxs-lookup"><span data-stu-id="41727-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41727-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41727-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="41727-141">DLL</span><span class="sxs-lookup"><span data-stu-id="41727-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41727-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41727-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41727-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41727-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41727-144">**\_СИСТЕМКОМПОНЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="41727-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

