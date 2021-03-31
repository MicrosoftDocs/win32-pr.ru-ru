---
description: '\_Ассоциация ФРОМДИРЕКТОРЯКТИОН CIM определяет исходный каталог для действия с файлом.'
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: Класс CIM_FromDirectoryAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f485fa32561e746afa16a899a1392b4fddc18f1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896021"
---
# <a name="cim_fromdirectoryaction-class"></a><span data-ttu-id="87f77-103">\_Класс CIM фромдиректоряктион</span><span class="sxs-lookup"><span data-stu-id="87f77-103">CIM\_FromDirectoryAction class</span></span>

<span data-ttu-id="87f77-104">Ассоциация **\_ фромдиректоряктион CIM** определяет исходный каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="87f77-104">The **CIM\_FromDirectoryAction** association identifies the source directory for the file action.</span></span> <span data-ttu-id="87f77-105">При использовании этой ассоциации предполагается, что исходный каталог был создан предыдущим действием.</span><span class="sxs-lookup"><span data-stu-id="87f77-105">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="87f77-106">Эта ассоциация не может существовать с Ассоциацией [**CIM \_ фромдиректориспеЦификатион**](cim-fromdirectoryspecification.md) ; действие файла может содержать только один исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="87f77-106">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87f77-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="87f77-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="87f77-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="87f77-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="87f77-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="87f77-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="87f77-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="87f77-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87f77-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87f77-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="87f77-112">Члены</span><span class="sxs-lookup"><span data-stu-id="87f77-112">Members</span></span>

<span data-ttu-id="87f77-113">Класс **CIM \_ фромдиректоряктион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87f77-113">The **CIM\_FromDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="87f77-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="87f77-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87f77-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="87f77-115">Properties</span></span>

<span data-ttu-id="87f77-116">Класс **CIM \_ фромдиректоряктион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87f77-116">The **CIM\_FromDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87f77-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="87f77-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f77-118">Тип данных: **CIM \_ филеактион**</span><span class="sxs-lookup"><span data-stu-id="87f77-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="87f77-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87f77-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87f77-120">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="87f77-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="87f77-121">Ссылка на имя файла.</span><span class="sxs-lookup"><span data-stu-id="87f77-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="87f77-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="87f77-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87f77-123">Тип данных: **CIM \_ директоряктион**</span><span class="sxs-lookup"><span data-stu-id="87f77-123">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="87f77-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87f77-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87f77-125">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="87f77-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="87f77-126">Ссылка на исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="87f77-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87f77-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87f77-127">Remarks</span></span>

<span data-ttu-id="87f77-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="87f77-128">WMI does not implement this class.</span></span>

<span data-ttu-id="87f77-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="87f77-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="87f77-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="87f77-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="87f77-131">Требования</span><span class="sxs-lookup"><span data-stu-id="87f77-131">Requirements</span></span>



| <span data-ttu-id="87f77-132">Требование</span><span class="sxs-lookup"><span data-stu-id="87f77-132">Requirement</span></span> | <span data-ttu-id="87f77-133">Значение</span><span class="sxs-lookup"><span data-stu-id="87f77-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87f77-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87f77-134">Minimum supported client</span></span><br/> | <span data-ttu-id="87f77-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87f77-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87f77-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87f77-136">Minimum supported server</span></span><br/> | <span data-ttu-id="87f77-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87f77-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87f77-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87f77-138">Namespace</span></span><br/>                | <span data-ttu-id="87f77-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87f77-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87f77-140">MOF</span><span class="sxs-lookup"><span data-stu-id="87f77-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87f77-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87f77-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87f77-142">DLL</span><span class="sxs-lookup"><span data-stu-id="87f77-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87f77-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87f77-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

