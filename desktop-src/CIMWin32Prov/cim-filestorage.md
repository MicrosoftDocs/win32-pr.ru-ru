---
description: '\_Ассоциация ФИЛЕСТОРАЖЕ CIM связывает файловую систему и логические файлы, адресованные через файловую систему.'
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: Класс CIM_FileStorage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655913"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="e0091-103">\_Класс CIM филестораже</span><span class="sxs-lookup"><span data-stu-id="e0091-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="e0091-104">Ассоциация **\_ филестораже CIM** связывает файловую систему и логические файлы, адресованные через файловую систему.</span><span class="sxs-lookup"><span data-stu-id="e0091-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0091-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e0091-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0091-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e0091-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0091-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e0091-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e0091-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e0091-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0091-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0091-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e0091-110">Члены</span><span class="sxs-lookup"><span data-stu-id="e0091-110">Members</span></span>

<span data-ttu-id="e0091-111">Класс **CIM \_ филестораже** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e0091-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="e0091-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0091-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0091-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0091-113">Properties</span></span>

<span data-ttu-id="e0091-114">Класс **CIM \_ филестораже** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e0091-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0091-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="e0091-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0091-116">Тип данных: **\_ Файловая система CIM**</span><span class="sxs-lookup"><span data-stu-id="e0091-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e0091-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0091-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0091-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e0091-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e0091-119">Файловая система [**CIM \_**](cim-filesystem.md) с описанием файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e0091-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="e0091-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e0091-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0091-121">Тип данных: **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="e0091-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="e0091-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0091-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0091-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0091-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0091-124">[**\_ LogicalFile CIM**](cim-logicalfile.md) , описывающий логический файл, хранящийся в контексте файловой системы.</span><span class="sxs-lookup"><span data-stu-id="e0091-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0091-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e0091-125">Remarks</span></span>

<span data-ttu-id="e0091-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e0091-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e0091-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e0091-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e0091-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e0091-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0091-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e0091-129">Requirements</span></span>



| <span data-ttu-id="e0091-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e0091-130">Requirement</span></span> | <span data-ttu-id="e0091-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e0091-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0091-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0091-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e0091-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0091-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0091-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0091-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e0091-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0091-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0091-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0091-136">Namespace</span></span><br/>                | <span data-ttu-id="e0091-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e0091-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0091-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e0091-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0091-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0091-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0091-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e0091-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0091-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0091-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0091-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e0091-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0091-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="e0091-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

