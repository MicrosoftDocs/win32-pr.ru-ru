---
description: '\_Класс экспорта CIM представляет связь между локальной файловой системой и ее каталогами, что означает, что указанные каталоги доступны для подключения.'
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Класс CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990597"
---
# <a name="cim_export-class"></a><span data-ttu-id="a4d64-103">\_Класс экспорта CIM</span><span class="sxs-lookup"><span data-stu-id="a4d64-103">CIM\_Export class</span></span>

<span data-ttu-id="a4d64-104">Класс **\_ экспорта CIM** представляет связь между локальной файловой системой и ее каталогами, что означает, что указанные каталоги доступны для подключения.</span><span class="sxs-lookup"><span data-stu-id="a4d64-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="a4d64-105">При экспорте всей файловой системы каталог должен ссылаться на самый верхний каталог файловой системы.</span><span class="sxs-lookup"><span data-stu-id="a4d64-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a4d64-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a4d64-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a4d64-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a4d64-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a4d64-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a4d64-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a4d64-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a4d64-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4d64-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4d64-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="a4d64-111">Члены</span><span class="sxs-lookup"><span data-stu-id="a4d64-111">Members</span></span>

<span data-ttu-id="a4d64-112">Класс **\_ экспорта CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a4d64-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="a4d64-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4d64-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a4d64-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a4d64-114">Properties</span></span>

<span data-ttu-id="a4d64-115">Класс **\_ экспорта CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="a4d64-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a4d64-116">**Каталог**</span><span class="sxs-lookup"><span data-stu-id="a4d64-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d64-117">Тип данных: **\_ Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="a4d64-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a4d64-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4d64-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d64-119">Ссылка на каталог, экспортированный для подключения NFS.</span><span class="sxs-lookup"><span data-stu-id="a4d64-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="a4d64-120">**експортеддиректоринаме**</span><span class="sxs-lookup"><span data-stu-id="a4d64-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d64-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a4d64-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a4d64-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4d64-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a4d64-123">Имя, под которым экспортируется каталог.</span><span class="sxs-lookup"><span data-stu-id="a4d64-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="a4d64-124">**локалфс**</span><span class="sxs-lookup"><span data-stu-id="a4d64-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a4d64-125">Тип данных: **CIM \_ локалфилесистем**</span><span class="sxs-lookup"><span data-stu-id="a4d64-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a4d64-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a4d64-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a4d64-127">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a4d64-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a4d64-128">Ссылка на локальную файловую систему.</span><span class="sxs-lookup"><span data-stu-id="a4d64-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a4d64-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a4d64-129">Remarks</span></span>

<span data-ttu-id="a4d64-130">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a4d64-130">WMI does not implement this class.</span></span>

<span data-ttu-id="a4d64-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a4d64-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a4d64-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a4d64-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4d64-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a4d64-133">Requirements</span></span>



| <span data-ttu-id="a4d64-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a4d64-134">Requirement</span></span> | <span data-ttu-id="a4d64-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a4d64-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d64-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4d64-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a4d64-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4d64-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a4d64-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4d64-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a4d64-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4d64-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a4d64-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4d64-140">Namespace</span></span><br/>                | <span data-ttu-id="a4d64-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a4d64-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a4d64-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a4d64-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4d64-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4d64-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4d64-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a4d64-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4d64-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4d64-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

