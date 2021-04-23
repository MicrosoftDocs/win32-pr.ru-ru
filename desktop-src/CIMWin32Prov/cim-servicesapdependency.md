---
description: Класс CIM \_ сервицесапдепенденци представляет ассоциацию между службой и точкой доступа к службе (SAP), которая указывает на то, что служба SAP используется службой для обеспечения ее функциональности.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: Класс CIM_ServiceSAPDependency (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141427"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="b5b2d-103">Класс CIM_ServiceSAPDependency (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b5b2d-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b5b2d-104">Класс **CIM \_ сервицесапдепенденци** представляет ассоциацию между службой и точкой доступа к службе (SAP), которая указывает на то, что служба SAP используется службой для обеспечения ее функциональности.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="b5b2d-105">Например, службы загрузки могут вызывать службы дисков BIOS (прерывания) для функционирования.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5b2d-106">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5b2d-107">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5b2d-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5b2d-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5b2d-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5b2d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5b2d-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b5b2d-111">Члены</span><span class="sxs-lookup"><span data-stu-id="b5b2d-111">Members</span></span>

<span data-ttu-id="b5b2d-112">Класс **CIM \_ сервицесапдепенденци** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b5b2d-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="b5b2d-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5b2d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5b2d-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b5b2d-114">Properties</span></span>

<span data-ttu-id="b5b2d-115">Класс **CIM \_ сервицесапдепенденци** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5b2d-116">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="b5b2d-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5b2d-117">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="b5b2d-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="b5b2d-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5b2d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5b2d-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="b5b2d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b5b2d-120">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий необходимую точку доступа к службе.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="b5b2d-121">**Него**</span><span class="sxs-lookup"><span data-stu-id="b5b2d-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5b2d-122">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="b5b2d-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="b5b2d-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b5b2d-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5b2d-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="b5b2d-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b5b2d-125">[**\_ Служба CIM**](cim-service.md) , которая описывает службу, которая зависит от базового SAP.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5b2d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5b2d-126">Remarks</span></span>

<span data-ttu-id="b5b2d-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b5b2d-128">Класс **CIM \_ сервицесапдепенденци** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b5b2d-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="b5b2d-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5b2d-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b5b2d-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5b2d-131">Требования</span><span class="sxs-lookup"><span data-stu-id="b5b2d-131">Requirements</span></span>



| <span data-ttu-id="b5b2d-132">Требование</span><span class="sxs-lookup"><span data-stu-id="b5b2d-132">Requirement</span></span> | <span data-ttu-id="b5b2d-133">Значение</span><span class="sxs-lookup"><span data-stu-id="b5b2d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5b2d-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5b2d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b5b2d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5b2d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5b2d-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5b2d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b5b2d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5b2d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5b2d-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b5b2d-138">Namespace</span></span><br/>                | <span data-ttu-id="b5b2d-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b5b2d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5b2d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b5b2d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5b2d-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5b2d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5b2d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5b2d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5b2d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5b2d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5b2d-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5b2d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5b2d-145">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="b5b2d-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

