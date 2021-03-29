---
description: Класс CIM \_ клустерсервицеакцессбисап представляет связь между службой кластеризации и ее точками доступа.
ms.assetid: b1e03ef1-909c-4836-a75f-c8d88a4d0087
ms.tgt_platform: multiple
title: Класс CIM_ClusterServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ClusterServiceAccessBySAP
- CIM_ClusterServiceAccessBySAP.Dependent
- CIM_ClusterServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b6e6f0df20f182be392de3fbb0cb13068cbeffc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990641"
---
# <a name="cim_clusterserviceaccessbysap-class"></a><span data-ttu-id="eb770-103">\_Класс CIM клустерсервицеакцессбисап</span><span class="sxs-lookup"><span data-stu-id="eb770-103">CIM\_ClusterServiceAccessBySAP class</span></span>

<span data-ttu-id="eb770-104">Класс **CIM \_ клустерсервицеакцессбисап** представляет связь между службой кластеризации и ее точками доступа.</span><span class="sxs-lookup"><span data-stu-id="eb770-104">The **CIM\_ClusterServiceAccessBySAP** class represents the relationship between a clustering service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb770-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="eb770-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb770-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb770-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb770-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb770-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="eb770-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="eb770-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb770-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb770-109">Syntax</span></span>

``` syntax
[UUID("{88F073D8-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ClusterServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_ClusteringSAP     REF Dependent;
  CIM_ClusteringService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="eb770-110">Члены</span><span class="sxs-lookup"><span data-stu-id="eb770-110">Members</span></span>

<span data-ttu-id="eb770-111">Класс **CIM \_ клустерсервицеакцессбисап** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eb770-111">The **CIM\_ClusterServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="eb770-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb770-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb770-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb770-113">Properties</span></span>

<span data-ttu-id="eb770-114">Класс **CIM \_ клустерсервицеакцессбисап** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eb770-114">The **CIM\_ClusterServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb770-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="eb770-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb770-116">Тип данных: **CIM \_ клустерингсервице**</span><span class="sxs-lookup"><span data-stu-id="eb770-116">Data type: **CIM\_ClusteringService**</span></span>
</dt> <dt>

<span data-ttu-id="eb770-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb770-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb770-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="eb770-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eb770-119">[**\_ Клустерингсервице CIM**](cim-clusteringservice.md) , описывающий службу кластеризации.</span><span class="sxs-lookup"><span data-stu-id="eb770-119">A [**CIM\_ClusteringService**](cim-clusteringservice.md) that describes the clustering service.</span></span>

</dd> <dt>

<span data-ttu-id="eb770-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="eb770-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb770-121">Тип данных: **CIM \_ клустерингсап**</span><span class="sxs-lookup"><span data-stu-id="eb770-121">Data type: **CIM\_ClusteringSAP**</span></span>
</dt> <dt>

<span data-ttu-id="eb770-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb770-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb770-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="eb770-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eb770-124">[**\_ Клустерингсап CIM**](cim-clusteringsap.md) , описывающий точку доступа для службы кластеризации.</span><span class="sxs-lookup"><span data-stu-id="eb770-124">A [**CIM\_ClusteringSAP**](cim-clusteringsap.md) that describes an access point for the clustering service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb770-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb770-125">Remarks</span></span>

<span data-ttu-id="eb770-126">Класс **CIM \_ клустерсервицеакцессбисап** является производным от [**CIM \_ сервицеакцессбисап**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="eb770-126">The **CIM\_ClusterServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="eb770-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="eb770-127">WMI does not implement this class.</span></span>

<span data-ttu-id="eb770-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb770-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb770-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb770-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb770-130">Требования</span><span class="sxs-lookup"><span data-stu-id="eb770-130">Requirements</span></span>



| <span data-ttu-id="eb770-131">Требование</span><span class="sxs-lookup"><span data-stu-id="eb770-131">Requirement</span></span> | <span data-ttu-id="eb770-132">Значение</span><span class="sxs-lookup"><span data-stu-id="eb770-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb770-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb770-133">Minimum supported client</span></span><br/> | <span data-ttu-id="eb770-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb770-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb770-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb770-135">Minimum supported server</span></span><br/> | <span data-ttu-id="eb770-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb770-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb770-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eb770-137">Namespace</span></span><br/>                | <span data-ttu-id="eb770-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb770-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb770-139">MOF</span><span class="sxs-lookup"><span data-stu-id="eb770-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb770-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb770-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb770-141">DLL</span><span class="sxs-lookup"><span data-stu-id="eb770-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb770-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb770-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb770-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb770-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb770-144">**\_СЕРВИЦЕАКЦЕССБИСАП CIM**</span><span class="sxs-lookup"><span data-stu-id="eb770-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

