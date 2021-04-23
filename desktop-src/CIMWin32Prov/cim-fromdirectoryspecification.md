---
description: '\_Ассоциация ФРОМДИРЕКТОРИСПЕЦИФИКАТИОН CIM определяет исходный каталог для действия с файлом.'
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: Класс CIM_FromDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7690514b46d89bdf1aa926438456c49598034700
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655911"
---
# <a name="cim_fromdirectoryspecification-class"></a><span data-ttu-id="46995-103">\_Класс CIM фромдиректориспеЦификатион</span><span class="sxs-lookup"><span data-stu-id="46995-103">CIM\_FromDirectorySpecification class</span></span>

<span data-ttu-id="46995-104">Ассоциация **\_ фромдиректориспеЦификатион CIM** определяет исходный каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="46995-104">The **CIM\_FromDirectorySpecification** association identifies the source directory for the file action.</span></span> <span data-ttu-id="46995-105">При использовании этой ассоциации предполагается, что исходный каталог уже существует.</span><span class="sxs-lookup"><span data-stu-id="46995-105">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="46995-106">Эта ассоциация не может существовать с Ассоциацией [**CIM \_ фромдиректоряктион**](cim-fromdirectoryaction.md) ; действие файла может содержать только один исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="46995-106">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46995-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="46995-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="46995-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="46995-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="46995-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="46995-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="46995-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="46995-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="46995-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46995-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="46995-112">Члены</span><span class="sxs-lookup"><span data-stu-id="46995-112">Members</span></span>

<span data-ttu-id="46995-113">Класс **CIM \_ фромдиректориспеЦификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="46995-113">The **CIM\_FromDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="46995-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="46995-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46995-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="46995-115">Properties</span></span>

<span data-ttu-id="46995-116">Класс **CIM \_ фромдиректориспеЦификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="46995-116">The **CIM\_FromDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46995-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="46995-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46995-118">Тип данных: **CIM \_ филеактион**</span><span class="sxs-lookup"><span data-stu-id="46995-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="46995-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46995-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46995-120">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="46995-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="46995-121">Ссылка на имя файла.</span><span class="sxs-lookup"><span data-stu-id="46995-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="46995-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="46995-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46995-123">Тип данных: **CIM \_ директориспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="46995-123">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="46995-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46995-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46995-125">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="46995-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="46995-126">Ссылка на исходный каталог.</span><span class="sxs-lookup"><span data-stu-id="46995-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46995-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46995-127">Remarks</span></span>

<span data-ttu-id="46995-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="46995-128">WMI does not implement this class.</span></span>

<span data-ttu-id="46995-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="46995-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="46995-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="46995-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="46995-131">Требования</span><span class="sxs-lookup"><span data-stu-id="46995-131">Requirements</span></span>



| <span data-ttu-id="46995-132">Требование</span><span class="sxs-lookup"><span data-stu-id="46995-132">Requirement</span></span> | <span data-ttu-id="46995-133">Значение</span><span class="sxs-lookup"><span data-stu-id="46995-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46995-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46995-134">Minimum supported client</span></span><br/> | <span data-ttu-id="46995-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46995-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46995-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46995-136">Minimum supported server</span></span><br/> | <span data-ttu-id="46995-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46995-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46995-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46995-138">Namespace</span></span><br/>                | <span data-ttu-id="46995-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="46995-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="46995-140">MOF</span><span class="sxs-lookup"><span data-stu-id="46995-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46995-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46995-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="46995-142">DLL</span><span class="sxs-lookup"><span data-stu-id="46995-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46995-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46995-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

