---
description: Класс CIM \_ директориконтаинсфиле представляет связь между каталогом и файлами, содержащимися в этом каталоге.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Класс CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896170"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="39d54-103">\_Класс CIM директориконтаинсфиле</span><span class="sxs-lookup"><span data-stu-id="39d54-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="39d54-104">Класс **CIM \_ директориконтаинсфиле** представляет связь между каталогом и файлами, содержащимися в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="39d54-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39d54-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="39d54-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39d54-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39d54-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39d54-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="39d54-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39d54-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="39d54-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d54-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39d54-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="39d54-110">Члены</span><span class="sxs-lookup"><span data-stu-id="39d54-110">Members</span></span>

<span data-ttu-id="39d54-111">Класс **CIM \_ директориконтаинсфиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39d54-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="39d54-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="39d54-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39d54-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="39d54-113">Properties</span></span>

<span data-ttu-id="39d54-114">Класс **CIM \_ директориконтаинсфиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39d54-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39d54-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="39d54-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d54-116">Тип данных: **\_ Каталог CIM**</span><span class="sxs-lookup"><span data-stu-id="39d54-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="39d54-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39d54-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d54-118">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="39d54-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="39d54-119">[**\_ Каталог CIM**](cim-directory.md) , описывающий каталог.</span><span class="sxs-lookup"><span data-stu-id="39d54-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="39d54-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="39d54-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39d54-121">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="39d54-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="39d54-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39d54-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39d54-123">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="39d54-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="39d54-124">[**\_ Файл CIM**](cim-datafile.md) , описывающий LogicalFile, содержащийся в каталоге.</span><span class="sxs-lookup"><span data-stu-id="39d54-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39d54-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39d54-125">Remarks</span></span>

<span data-ttu-id="39d54-126">WMI реализует класс **CIM \_ директориконтаинсфиле** , который является динамическим классом.</span><span class="sxs-lookup"><span data-stu-id="39d54-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="39d54-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="39d54-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39d54-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="39d54-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d54-129">Требования</span><span class="sxs-lookup"><span data-stu-id="39d54-129">Requirements</span></span>



| <span data-ttu-id="39d54-130">Требование</span><span class="sxs-lookup"><span data-stu-id="39d54-130">Requirement</span></span> | <span data-ttu-id="39d54-131">Значение</span><span class="sxs-lookup"><span data-stu-id="39d54-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39d54-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39d54-132">Minimum supported client</span></span><br/> | <span data-ttu-id="39d54-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39d54-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39d54-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39d54-134">Minimum supported server</span></span><br/> | <span data-ttu-id="39d54-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39d54-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39d54-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39d54-136">Namespace</span></span><br/>                | <span data-ttu-id="39d54-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39d54-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39d54-138">MOF</span><span class="sxs-lookup"><span data-stu-id="39d54-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39d54-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39d54-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39d54-140">DLL</span><span class="sxs-lookup"><span data-stu-id="39d54-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39d54-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39d54-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d54-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39d54-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d54-143">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="39d54-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

