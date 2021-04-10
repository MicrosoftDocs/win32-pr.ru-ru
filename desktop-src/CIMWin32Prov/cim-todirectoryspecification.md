---
description: '\_Ассоциация ТОДИРЕКТОРИСПЕЦИФИКАТИОН CIM определяет целевой каталог для действия с файлом.'
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Класс CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142931"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="2744a-103">\_Класс CIM тодиректориспеЦификатион</span><span class="sxs-lookup"><span data-stu-id="2744a-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="2744a-104">Ассоциация **\_ тодиректориспеЦификатион CIM** определяет целевой каталог для действия с файлом.</span><span class="sxs-lookup"><span data-stu-id="2744a-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="2744a-105">При использовании этой ассоциации предполагается, что целевой каталог уже существует.</span><span class="sxs-lookup"><span data-stu-id="2744a-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="2744a-106">Эта ассоциация не может существовать с [**Ассоциацией \_ тодиректоряктион CIM**](cim-todirectoryaction.md) , так как действие файла может содержать только один целевой каталог.</span><span class="sxs-lookup"><span data-stu-id="2744a-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2744a-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2744a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2744a-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2744a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2744a-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2744a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2744a-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2744a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2744a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2744a-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="2744a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="2744a-112">Members</span></span>

<span data-ttu-id="2744a-113">Класс **CIM \_ тодиректориспеЦификатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2744a-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="2744a-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="2744a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2744a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="2744a-115">Properties</span></span>

<span data-ttu-id="2744a-116">Класс **CIM \_ тодиректориспеЦификатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2744a-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2744a-117">**дестинатиондиректори**</span><span class="sxs-lookup"><span data-stu-id="2744a-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2744a-118">Тип данных: **CIM \_ директориспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="2744a-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="2744a-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2744a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2744a-120">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="2744a-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="2744a-121">Ссылка на каталог назначения.</span><span class="sxs-lookup"><span data-stu-id="2744a-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="2744a-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="2744a-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2744a-123">Тип данных: **CIM \_ копифилеактион**</span><span class="sxs-lookup"><span data-stu-id="2744a-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="2744a-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2744a-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2744a-125">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="2744a-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="2744a-126">Ссылка на имя файла.</span><span class="sxs-lookup"><span data-stu-id="2744a-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2744a-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2744a-127">Remarks</span></span>

<span data-ttu-id="2744a-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2744a-128">WMI does not implement this class.</span></span>

<span data-ttu-id="2744a-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2744a-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2744a-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2744a-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2744a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="2744a-131">Requirements</span></span>



| <span data-ttu-id="2744a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="2744a-132">Requirement</span></span> | <span data-ttu-id="2744a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="2744a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2744a-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2744a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2744a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2744a-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2744a-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2744a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2744a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2744a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2744a-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2744a-138">Namespace</span></span><br/>                | <span data-ttu-id="2744a-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2744a-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2744a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="2744a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2744a-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2744a-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2744a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="2744a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2744a-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2744a-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

