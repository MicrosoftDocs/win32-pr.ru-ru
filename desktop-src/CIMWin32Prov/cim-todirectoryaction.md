---
description: '\_Ассоциация ТОДИРЕКТОРЯКТИОН CIM определяет целевой каталог для действия с файлом.'
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: Класс CIM_ToDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807937"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="3fdb9-103">\_Класс CIM тодиректоряктион</span><span class="sxs-lookup"><span data-stu-id="3fdb9-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="3fdb9-104">Ассоциация **\_ тодиректоряктион CIM** определяет целевой каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="3fdb9-105">При использовании этой ассоциации предполагается, что целевой каталог был создан предыдущим действием.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="3fdb9-106">Эта ассоциация не может существовать с [**Ассоциацией \_ тодиректориспеЦификатион CIM**](cim-todirectoryspecification.md) , так как действие файла может содержать только один целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3fdb9-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3fdb9-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3fdb9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3fdb9-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3fdb9-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fdb9-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3fdb9-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="3fdb9-112">Члены</span><span class="sxs-lookup"><span data-stu-id="3fdb9-112">Members</span></span>

<span data-ttu-id="3fdb9-113">Класс **CIM \_ тодиректоряктион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3fdb9-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="3fdb9-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fdb9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3fdb9-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="3fdb9-115">Properties</span></span>

<span data-ttu-id="3fdb9-116">Класс **CIM \_ тодиректоряктион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3fdb9-117">**дестинатиондиректори**</span><span class="sxs-lookup"><span data-stu-id="3fdb9-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fdb9-118">Тип данных: **CIM \_ директоряктион**</span><span class="sxs-lookup"><span data-stu-id="3fdb9-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="3fdb9-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fdb9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fdb9-120">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="3fdb9-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3fdb9-121">Ссылка на каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="3fdb9-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3fdb9-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3fdb9-123">Тип данных: **CIM \_ копифилеактион**</span><span class="sxs-lookup"><span data-stu-id="3fdb9-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="3fdb9-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3fdb9-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3fdb9-125">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="3fdb9-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3fdb9-126">Ссылка на имя файла.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fdb9-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3fdb9-127">Remarks</span></span>

<span data-ttu-id="3fdb9-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-128">WMI does not implement this class.</span></span>

<span data-ttu-id="3fdb9-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3fdb9-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="3fdb9-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fdb9-131">Требования</span><span class="sxs-lookup"><span data-stu-id="3fdb9-131">Requirements</span></span>



| <span data-ttu-id="3fdb9-132">Требование</span><span class="sxs-lookup"><span data-stu-id="3fdb9-132">Requirement</span></span> | <span data-ttu-id="3fdb9-133">Значение</span><span class="sxs-lookup"><span data-stu-id="3fdb9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fdb9-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3fdb9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3fdb9-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fdb9-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fdb9-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3fdb9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3fdb9-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fdb9-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fdb9-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3fdb9-138">Namespace</span></span><br/>                | <span data-ttu-id="3fdb9-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3fdb9-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3fdb9-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3fdb9-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3fdb9-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3fdb9-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3fdb9-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3fdb9-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fdb9-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fdb9-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

