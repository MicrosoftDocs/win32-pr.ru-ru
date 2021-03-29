---
description: Класс CIM \_ хостедакцесспоинт представляет связь между точкой доступа к службе (SAP) и системой, в которой она предоставляется. Каждая система может содержать много SAPs.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: Класс CIM_HostedAccessPoint (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d451cec7ad42fa519b70c576fbd02a32d0289e8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141737"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="32e58-104">Класс CIM_HostedAccessPoint (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="32e58-104">CIM_HostedAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="32e58-105">Класс **CIM \_ хостедакцесспоинт** представляет связь между точкой доступа к службе (SAP) и системой, в которой она предоставляется.</span><span class="sxs-lookup"><span data-stu-id="32e58-105">The **CIM\_HostedAccessPoint** class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="32e58-106">Каждая система может содержать много SAPs.</span><span class="sxs-lookup"><span data-stu-id="32e58-106">Each system may host many SAPs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="32e58-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="32e58-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="32e58-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="32e58-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="32e58-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="32e58-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="32e58-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="32e58-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="32e58-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="32e58-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="32e58-112">Члены</span><span class="sxs-lookup"><span data-stu-id="32e58-112">Members</span></span>

<span data-ttu-id="32e58-113">Класс **CIM \_ хостедакцесспоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="32e58-113">The **CIM\_HostedAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="32e58-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="32e58-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32e58-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="32e58-115">Properties</span></span>

<span data-ttu-id="32e58-116">Класс **CIM \_ хостедакцесспоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="32e58-116">The **CIM\_HostedAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="32e58-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="32e58-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e58-118">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="32e58-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="32e58-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32e58-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e58-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="32e58-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="32e58-121">[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.</span><span class="sxs-lookup"><span data-stu-id="32e58-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="32e58-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="32e58-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32e58-123">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="32e58-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="32e58-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="32e58-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32e58-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="32e58-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="32e58-126">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий SAP (ы), размещенные в этой системе.</span><span class="sxs-lookup"><span data-stu-id="32e58-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes The SAP(s) that are hosted on this system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32e58-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32e58-127">Remarks</span></span>

<span data-ttu-id="32e58-128">**Модель CIM \_ Хостедакцесспоинт** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="32e58-128">**CIM\_HostedAccessPoint** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="32e58-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="32e58-129">WMI does not implement this class.</span></span>

<span data-ttu-id="32e58-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="32e58-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="32e58-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="32e58-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="32e58-132">Требования</span><span class="sxs-lookup"><span data-stu-id="32e58-132">Requirements</span></span>



| <span data-ttu-id="32e58-133">Требование</span><span class="sxs-lookup"><span data-stu-id="32e58-133">Requirement</span></span> | <span data-ttu-id="32e58-134">Значение</span><span class="sxs-lookup"><span data-stu-id="32e58-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e58-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32e58-135">Minimum supported client</span></span><br/> | <span data-ttu-id="32e58-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32e58-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32e58-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32e58-137">Minimum supported server</span></span><br/> | <span data-ttu-id="32e58-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32e58-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32e58-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="32e58-139">Namespace</span></span><br/>                | <span data-ttu-id="32e58-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="32e58-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32e58-141">MOF</span><span class="sxs-lookup"><span data-stu-id="32e58-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32e58-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32e58-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32e58-143">DLL</span><span class="sxs-lookup"><span data-stu-id="32e58-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32e58-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32e58-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e58-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32e58-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e58-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="32e58-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

