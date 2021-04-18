---
description: '\_Класс WMI ассоциации подкаталогов Win32 связывает каталог (папку) и один из его подкаталогов (вложенных папок).'
ms.assetid: f0565b7b-d593-468b-96b1-3922428c61e1
ms.tgt_platform: multiple
title: Класс Win32_SubDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubDirectory
- Win32_SubDirectory.GroupComponent
- Win32_SubDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 046de6ad1e09874351b37d58f7277126e39e990a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142250"
---
# <a name="win32_subdirectory-class"></a><span data-ttu-id="a88f9-103">\_Класс подкаталога Win32</span><span class="sxs-lookup"><span data-stu-id="a88f9-103">Win32\_SubDirectory class</span></span>

<span data-ttu-id="a88f9-104">[Класс WMI](../wmisdk/retrieving-a-class.md) ассоциации **\_ подкаталогов Win32** связывает каталог (папку) и один из его подкаталогов (вложенных папок).</span><span class="sxs-lookup"><span data-stu-id="a88f9-104">The **Win32\_SubDirectory** association [WMI class](../wmisdk/retrieving-a-class.md) relates a directory (folder) and one of its subdirectories (subfolders).</span></span>

<span data-ttu-id="a88f9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a88f9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a88f9-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="a88f9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88f9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a88f9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE469-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_SubDirectory : CIM_Component
{
  Win32_Directory REF GroupComponent;
  Win32_Directory REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="a88f9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a88f9-108">Members</span></span>

<span data-ttu-id="a88f9-109">Класс **\_ подкаталога Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a88f9-109">The **Win32\_SubDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="a88f9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a88f9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a88f9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a88f9-111">Properties</span></span>

<span data-ttu-id="a88f9-112">Класс **\_ подкаталога Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a88f9-112">The **Win32\_SubDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a88f9-113">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="a88f9-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a88f9-114">Тип данных: **\_ Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="a88f9-114">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a88f9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a88f9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a88f9-116">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI- \| \_ Каталог Win32")</span><span class="sxs-lookup"><span data-stu-id="a88f9-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="a88f9-117">Ссылка на экземпляр, представляющий свойства родительского каталога (папки) в этой ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a88f9-117">Reference to the instance representing the properties of the parent directory (folder) in this association.</span></span>

</dd> <dt>

<span data-ttu-id="a88f9-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="a88f9-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a88f9-119">Тип данных: **\_ Каталог Win32**</span><span class="sxs-lookup"><span data-stu-id="a88f9-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="a88f9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a88f9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a88f9-121">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI- \| \_ Каталог Win32")</span><span class="sxs-lookup"><span data-stu-id="a88f9-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="a88f9-122">Ссылка на экземпляр, представляющий подкаталог (вложенную папку) ассоциации.</span><span class="sxs-lookup"><span data-stu-id="a88f9-122">Reference to the instance representing the subdirectory (subfolder) part of the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a88f9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a88f9-123">Remarks</span></span>

<span data-ttu-id="a88f9-124">Класс **\_ подкаталога Win32** является производным от [**\_ компонента CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="a88f9-124">The **Win32\_SubDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="a88f9-125">Чтобы получить коллекцию вложенных папок для папки, создайте запрос связи, который задает для *ресултроле* значение *PartComponent*.</span><span class="sxs-lookup"><span data-stu-id="a88f9-125">To return a collection of subfolders for a folder, create an association query that sets the *ResultRole* to *PartComponent*.</span></span> <span data-ttu-id="a88f9-126">Это означает, что все элементы в возвращенной коллекции должны играть роль PartComponent или вложенной папки объекта Folder.</span><span class="sxs-lookup"><span data-stu-id="a88f9-126">This indicates that all the items in the returned collection must play the role of a PartComponent, or subfolder, of the folder object.</span></span> <span data-ttu-id="a88f9-127">Чтобы получить родительскую папку для папки, задайте для *ресултроле* значение *GroupComponent*.</span><span class="sxs-lookup"><span data-stu-id="a88f9-127">To return the parent folder for a folder, set the *ResultRole* to *GroupComponent*.</span></span>

<span data-ttu-id="a88f9-128">Класс **\_ подкаталога Win32** работает только на уровне файловой системы непосредственно над указанной папкой или непосредственно под ней.</span><span class="sxs-lookup"><span data-stu-id="a88f9-128">The **Win32\_SubDirectory** class works only on the file system level immediately above or immediately below the specified folder.</span></span>

## <a name="examples"></a><span data-ttu-id="a88f9-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="a88f9-129">Examples</span></span>

<span data-ttu-id="a88f9-130">Следующий пример сценария VBScript возвращает список всех вложенных папок в папке C: \\ Scripts.</span><span class="sxs-lookup"><span data-stu-id="a88f9-130">The following VBScript sample returns a list of all subfolders within the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSubfolders = objWMIService.ExecQuery _
 ("ASSOCIATORS OF {Win32_Directory.Name='c:\scripts'} " _
 & "WHERE AssocClass = Win32_Subdirectory " _
 & "ResultRole = PartComponent")
For Each objFolder in colSubfolders
 Wscript.Echo objFolder.Name
Next
```



## <a name="requirements"></a><span data-ttu-id="a88f9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="a88f9-131">Requirements</span></span>



| <span data-ttu-id="a88f9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="a88f9-132">Requirement</span></span> | <span data-ttu-id="a88f9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="a88f9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a88f9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a88f9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a88f9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a88f9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a88f9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a88f9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a88f9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a88f9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a88f9-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a88f9-138">Namespace</span></span><br/>                | <span data-ttu-id="a88f9-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a88f9-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a88f9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a88f9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a88f9-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a88f9-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a88f9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a88f9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a88f9-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a88f9-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a88f9-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a88f9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88f9-145">**\_Компонент CIM**</span><span class="sxs-lookup"><span data-stu-id="a88f9-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

[<span data-ttu-id="a88f9-146">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="a88f9-146">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
