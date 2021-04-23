---
description: '\_Класс статистики CIM представляет ассоциацию, которая связывает управляемые системные элементы с применяемыми к ним статистическими группами.'
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: Класс CIM_Statistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990394"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="0a4e8-103">\_Класс статистики CIM</span><span class="sxs-lookup"><span data-stu-id="0a4e8-103">CIM\_Statistics class</span></span>

<span data-ttu-id="0a4e8-104">Класс **\_ статистики CIM** представляет ассоциацию, которая связывает управляемые системные элементы с применяемыми к ним статистическими группами.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a4e8-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0a4e8-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0a4e8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0a4e8-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0a4e8-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4e8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a4e8-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="0a4e8-110">Члены</span><span class="sxs-lookup"><span data-stu-id="0a4e8-110">Members</span></span>

<span data-ttu-id="0a4e8-111">Класс **\_ статистики CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0a4e8-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="0a4e8-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a4e8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a4e8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="0a4e8-113">Properties</span></span>

<span data-ttu-id="0a4e8-114">Класс **\_ статистики CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a4e8-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0a4e8-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4e8-116">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="0a4e8-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="0a4e8-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a4e8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a4e8-118">Ссылка на класс [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) , для которого определены статистические данные или метрики.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="0a4e8-119">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="0a4e8-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4e8-120">Тип данных: **CIM \_ статистикалинформатион**</span><span class="sxs-lookup"><span data-stu-id="0a4e8-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="0a4e8-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0a4e8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a4e8-122">Ссылка на статистическую информацию или объект.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a4e8-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a4e8-123">Remarks</span></span>

<span data-ttu-id="0a4e8-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-124">WMI does not implement this class.</span></span>

<span data-ttu-id="0a4e8-125">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0a4e8-126">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="0a4e8-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4e8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="0a4e8-127">Requirements</span></span>



| <span data-ttu-id="0a4e8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="0a4e8-128">Requirement</span></span> | <span data-ttu-id="0a4e8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="0a4e8-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4e8-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0a4e8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4e8-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a4e8-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0a4e8-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0a4e8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4e8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a4e8-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0a4e8-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0a4e8-134">Namespace</span></span><br/>                | <span data-ttu-id="0a4e8-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0a4e8-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0a4e8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="0a4e8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a4e8-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a4e8-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a4e8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="0a4e8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4e8-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a4e8-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




