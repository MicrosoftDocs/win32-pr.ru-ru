---
description: '\_Агрегат СТОРАЖЕДЕФЕКТ CIM собирает ошибки хранилища для экстента хранения.'
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Класс CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990747"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="d236d-103">\_Класс CIM сторажедефект</span><span class="sxs-lookup"><span data-stu-id="d236d-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="d236d-104">Агрегат **\_ сторажедефект CIM** собирает ошибки хранилища для экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="d236d-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d236d-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d236d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d236d-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d236d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d236d-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d236d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="d236d-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d236d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d236d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d236d-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="d236d-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d236d-110">Members</span></span>

<span data-ttu-id="d236d-111">Класс **CIM \_ сторажедефект** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d236d-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="d236d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d236d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d236d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d236d-113">Properties</span></span>

<span data-ttu-id="d236d-114">Класс **CIM \_ сторажедефект** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d236d-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d236d-115">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="d236d-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d236d-116">Тип данных: **CIM \_ сторажееррор**</span><span class="sxs-lookup"><span data-stu-id="d236d-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="d236d-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d236d-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d236d-118">Квалификаторы: [ **слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d236d-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d236d-119">Ссылка на объект Error, который определяет начальный и конечный адреса, сопоставленные с областью хранения.</span><span class="sxs-lookup"><span data-stu-id="d236d-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="d236d-120">**Экстент**</span><span class="sxs-lookup"><span data-stu-id="d236d-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d236d-121">Тип данных: **CIM \_ сторажеекстент**</span><span class="sxs-lookup"><span data-stu-id="d236d-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="d236d-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d236d-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d236d-123">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d236d-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d236d-124">Ссылка на область хранения, в которой произошли ошибки.</span><span class="sxs-lookup"><span data-stu-id="d236d-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d236d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d236d-125">Remarks</span></span>

<span data-ttu-id="d236d-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d236d-126">WMI does not implement this class.</span></span>

<span data-ttu-id="d236d-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d236d-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d236d-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d236d-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d236d-129">Требования</span><span class="sxs-lookup"><span data-stu-id="d236d-129">Requirements</span></span>



| <span data-ttu-id="d236d-130">Требование</span><span class="sxs-lookup"><span data-stu-id="d236d-130">Requirement</span></span> | <span data-ttu-id="d236d-131">Значение</span><span class="sxs-lookup"><span data-stu-id="d236d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d236d-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d236d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d236d-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d236d-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d236d-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d236d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d236d-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d236d-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d236d-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d236d-136">Namespace</span></span><br/>                | <span data-ttu-id="d236d-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d236d-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d236d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d236d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d236d-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d236d-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d236d-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d236d-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d236d-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d236d-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

