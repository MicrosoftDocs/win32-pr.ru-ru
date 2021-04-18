---
description: '\_Ассоциация ДИРЕКТОРИСПЕЦИФИКАТИОНФИЛЕ CIM представляет каталог, содержащий файл, указанный в ссылке на \_ класс CIM директориспеЦификатион.'
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: Класс CIM_DirectorySpecificationFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142052"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="6f694-103">\_Класс CIM директориспеЦификатионфиле</span><span class="sxs-lookup"><span data-stu-id="6f694-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="6f694-104">Ассоциация **\_ директориспеЦификатионфиле CIM** представляет каталог, содержащий файл, указанный в ссылке на класс [**CIM \_ директориспеЦификатион**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="6f694-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6f694-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6f694-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6f694-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6f694-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6f694-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6f694-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6f694-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6f694-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f694-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6f694-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="6f694-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6f694-110">Members</span></span>

<span data-ttu-id="6f694-111">Класс **CIM \_ директориспеЦификатионфиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6f694-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="6f694-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f694-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6f694-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f694-113">Properties</span></span>

<span data-ttu-id="6f694-114">Класс **CIM \_ директориспеЦификатионфиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6f694-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6f694-115">**директориспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="6f694-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f694-116">Тип данных: **CIM \_ директориспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="6f694-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="6f694-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f694-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f694-118">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="6f694-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="6f694-119">Ссылка на спецификацию каталога.</span><span class="sxs-lookup"><span data-stu-id="6f694-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="6f694-120">**филеспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="6f694-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f694-121">Тип данных: **CIM \_ филеспеЦификатион**</span><span class="sxs-lookup"><span data-stu-id="6f694-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="6f694-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6f694-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6f694-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="6f694-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="6f694-124">Ссылка на спецификацию файла.</span><span class="sxs-lookup"><span data-stu-id="6f694-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f694-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f694-125">Remarks</span></span>

<span data-ttu-id="6f694-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6f694-126">WMI does not implement this class.</span></span>

<span data-ttu-id="6f694-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6f694-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6f694-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6f694-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f694-129">Требования</span><span class="sxs-lookup"><span data-stu-id="6f694-129">Requirements</span></span>



| <span data-ttu-id="6f694-130">Требование</span><span class="sxs-lookup"><span data-stu-id="6f694-130">Requirement</span></span> | <span data-ttu-id="6f694-131">Значение</span><span class="sxs-lookup"><span data-stu-id="6f694-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f694-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f694-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6f694-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f694-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f694-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f694-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6f694-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f694-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f694-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f694-136">Namespace</span></span><br/>                | <span data-ttu-id="6f694-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6f694-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6f694-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6f694-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f694-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6f694-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f694-140">DLL</span><span class="sxs-lookup"><span data-stu-id="6f694-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f694-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f694-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

