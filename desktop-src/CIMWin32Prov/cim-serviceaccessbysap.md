---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM сервицеакцессбисап представляет точки доступа для службы. Например, доступ к принтеру можно получить из NetWare, Macintosh или точек доступа к службам Windows (SAPs), которые могут размещаться в разных системах.'
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: Класс CIM_ServiceAccessBySAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990529"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="df997-104">\_Класс CIM сервицеакцессбисап</span><span class="sxs-lookup"><span data-stu-id="df997-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="df997-105">Класс сопоставления **CIM \_ сервицеакцессбисап** представляет точки доступа для службы.</span><span class="sxs-lookup"><span data-stu-id="df997-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="df997-106">Например, доступ к принтеру можно получить из NetWare, Macintosh или точек доступа к службам Windows (SAPs), которые могут размещаться в разных системах.</span><span class="sxs-lookup"><span data-stu-id="df997-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df997-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="df997-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="df997-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="df997-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="df997-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="df997-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="df997-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="df997-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="df997-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df997-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="df997-112">Члены</span><span class="sxs-lookup"><span data-stu-id="df997-112">Members</span></span>

<span data-ttu-id="df997-113">Класс **CIM \_ сервицеакцессбисап** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="df997-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="df997-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="df997-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df997-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="df997-115">Properties</span></span>

<span data-ttu-id="df997-116">Класс **CIM \_ сервицеакцессбисап** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="df997-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df997-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="df997-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df997-118">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="df997-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="df997-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df997-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df997-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="df997-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="df997-121">[**\_ Служба CIM**](cim-service.md) , которая описывает службу.</span><span class="sxs-lookup"><span data-stu-id="df997-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="df997-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="df997-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df997-123">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="df997-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="df997-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="df997-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="df997-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="df997-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="df997-126">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий точку доступа для службы.</span><span class="sxs-lookup"><span data-stu-id="df997-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="df997-127">Точки доступа зависят от этой связи, так как у них нет функции без соответствующей службы.</span><span class="sxs-lookup"><span data-stu-id="df997-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df997-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df997-128">Remarks</span></span>

<span data-ttu-id="df997-129">Класс **CIM \_ сервицеакцессбисап** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="df997-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="df997-130">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="df997-130">WMI does not implement this class.</span></span> <span data-ttu-id="df997-131">Сведения о классах WMI, которые являются производными от **CIM \_ сервицеакцессбисап**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="df997-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="df997-132">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="df997-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="df997-133">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="df997-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="df997-134">Требования</span><span class="sxs-lookup"><span data-stu-id="df997-134">Requirements</span></span>



| <span data-ttu-id="df997-135">Требование</span><span class="sxs-lookup"><span data-stu-id="df997-135">Requirement</span></span> | <span data-ttu-id="df997-136">Значение</span><span class="sxs-lookup"><span data-stu-id="df997-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="df997-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df997-137">Minimum supported client</span></span><br/> | <span data-ttu-id="df997-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df997-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="df997-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df997-139">Minimum supported server</span></span><br/> | <span data-ttu-id="df997-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df997-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="df997-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="df997-141">Namespace</span></span><br/>                | <span data-ttu-id="df997-142">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="df997-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="df997-143">MOF</span><span class="sxs-lookup"><span data-stu-id="df997-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df997-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df997-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="df997-145">DLL</span><span class="sxs-lookup"><span data-stu-id="df997-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df997-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df997-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df997-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df997-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df997-148">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="df997-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

