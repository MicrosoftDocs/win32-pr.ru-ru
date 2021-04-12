---
description: '\_Ассоциация РЕЛАТЕДСТАТИСТИКС CIM представляет иерархии и зависимости связанных \_ классов CIM статистикалинформатион.'
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: Класс CIM_RelatedStatistics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 01fb70535a4ae8f84d637cf92a06eee4fe318a49
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538489"
---
# <a name="cim_relatedstatistics-class"></a><span data-ttu-id="39b3b-103">\_Класс CIM релатедстатистикс</span><span class="sxs-lookup"><span data-stu-id="39b3b-103">CIM\_RelatedStatistics class</span></span>

<span data-ttu-id="39b3b-104">Ассоциация **\_ релатедстатистикс CIM** представляет иерархии и зависимости связанных классов [**CIM \_ статистикалинформатион**](cim-statisticalinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="39b3b-104">The **CIM\_RelatedStatistics** association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39b3b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="39b3b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39b3b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39b3b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39b3b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="39b3b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39b3b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="39b3b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39b3b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39b3b-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="39b3b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="39b3b-110">Members</span></span>

<span data-ttu-id="39b3b-111">Класс **CIM \_ релатедстатистикс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39b3b-111">The **CIM\_RelatedStatistics** class has these types of members:</span></span>

-   [<span data-ttu-id="39b3b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="39b3b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39b3b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="39b3b-113">Properties</span></span>

<span data-ttu-id="39b3b-114">Класс **CIM \_ релатедстатистикс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39b3b-114">The **CIM\_RelatedStatistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39b3b-115">**релатедстатс**</span><span class="sxs-lookup"><span data-stu-id="39b3b-115">**RelatedStats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39b3b-116">Тип данных: **CIM \_ статистикалинформатион**</span><span class="sxs-lookup"><span data-stu-id="39b3b-116">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="39b3b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39b3b-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39b3b-118">Ссылка на связанную статистику или метрики.</span><span class="sxs-lookup"><span data-stu-id="39b3b-118">Reference to the related statistics or metrics.</span></span>

</dd> <dt>

<span data-ttu-id="39b3b-119">**Статистика**</span><span class="sxs-lookup"><span data-stu-id="39b3b-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39b3b-120">Тип данных: **CIM \_ статистикалинформатион**</span><span class="sxs-lookup"><span data-stu-id="39b3b-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="39b3b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39b3b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39b3b-122">Ссылка на сведения о статистике или объект.</span><span class="sxs-lookup"><span data-stu-id="39b3b-122">Reference to the statistic information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39b3b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39b3b-123">Remarks</span></span>

<span data-ttu-id="39b3b-124">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="39b3b-124">WMI does not implement this class.</span></span>

<span data-ttu-id="39b3b-125">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="39b3b-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39b3b-126">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="39b3b-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39b3b-127">Требования</span><span class="sxs-lookup"><span data-stu-id="39b3b-127">Requirements</span></span>



| <span data-ttu-id="39b3b-128">Требование</span><span class="sxs-lookup"><span data-stu-id="39b3b-128">Requirement</span></span> | <span data-ttu-id="39b3b-129">Значение</span><span class="sxs-lookup"><span data-stu-id="39b3b-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39b3b-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39b3b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39b3b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39b3b-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39b3b-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39b3b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39b3b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39b3b-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39b3b-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39b3b-134">Namespace</span></span><br/>                | <span data-ttu-id="39b3b-135">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="39b3b-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39b3b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="39b3b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39b3b-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39b3b-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39b3b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="39b3b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39b3b-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39b3b-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




