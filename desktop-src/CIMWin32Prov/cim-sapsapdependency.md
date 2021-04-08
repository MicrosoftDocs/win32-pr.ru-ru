---
description: Класс CIM \_ сапсапдепенденци — это ассоциация между двумя точками доступа к службе (SAPS), которая указывает, что второй SAP необходим для подключения первой SAP к своей службе.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: Класс CIM_SAPSAPDependency (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990457"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="bced8-103">Класс CIM_SAPSAPDependency (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="bced8-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="bced8-104">Класс **CIM \_ сапсапдепенденци** — это ассоциация между двумя точками доступа к службе (SAPS), которая указывает, что второй SAP необходим для подключения первой SAP к своей службе.</span><span class="sxs-lookup"><span data-stu-id="bced8-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="bced8-105">Например, для печати на сетевом принтере точки доступа к локальным принтерам должны использовать базовые SAPs, связанные с сетью, или конечные точки протокола, чтобы отправить запрос на печать.</span><span class="sxs-lookup"><span data-stu-id="bced8-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bced8-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="bced8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bced8-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bced8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bced8-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="bced8-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bced8-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="bced8-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bced8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bced8-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bced8-111">Члены</span><span class="sxs-lookup"><span data-stu-id="bced8-111">Members</span></span>

<span data-ttu-id="bced8-112">Класс **CIM \_ сапсапдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bced8-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="bced8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="bced8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bced8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="bced8-114">Properties</span></span>

<span data-ttu-id="bced8-115">Класс **CIM \_ сапсапдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="bced8-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bced8-116">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="bced8-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bced8-117">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="bced8-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="bced8-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bced8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bced8-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="bced8-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bced8-120">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий необходимую точку доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="bced8-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="bced8-121">**Него**</span><span class="sxs-lookup"><span data-stu-id="bced8-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bced8-122">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="bced8-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="bced8-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="bced8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bced8-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="bced8-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bced8-125">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий точку доступа службы, которая зависит от базового SAP.</span><span class="sxs-lookup"><span data-stu-id="bced8-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bced8-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bced8-126">Remarks</span></span>

<span data-ttu-id="bced8-127">Класс **CIM \_ сапсапдепенденци** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="bced8-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="bced8-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="bced8-128">WMI does not implement this class.</span></span>

<span data-ttu-id="bced8-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="bced8-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bced8-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="bced8-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bced8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="bced8-131">Requirements</span></span>



| <span data-ttu-id="bced8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="bced8-132">Requirement</span></span> | <span data-ttu-id="bced8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="bced8-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bced8-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bced8-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bced8-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bced8-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bced8-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bced8-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bced8-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bced8-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bced8-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bced8-138">Namespace</span></span><br/>                | <span data-ttu-id="bced8-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="bced8-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bced8-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bced8-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bced8-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bced8-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bced8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bced8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bced8-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bced8-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bced8-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bced8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bced8-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="bced8-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

