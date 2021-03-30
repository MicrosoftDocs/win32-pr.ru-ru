---
description: Класс CIM \_ софтварефеатуресапимплементатион представляет связь между точкой доступа к службе (SAP) и ее реализацией в программном обеспечении.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895409"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a><span data-ttu-id="15204-103">\_Класс CIM софтварефеатуресапимплементатион</span><span class="sxs-lookup"><span data-stu-id="15204-103">CIM\_SoftwareFeatureSAPImplementation class</span></span>

<span data-ttu-id="15204-104">Класс **CIM \_ софтварефеатуресапимплементатион** представляет связь между точкой доступа к службе (SAP) и ее реализацией в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="15204-104">The **CIM\_SoftwareFeatureSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented in software.</span></span> <span data-ttu-id="15204-105">SAP может предоставляться несколькими программными компонентами для взаимодействия друг с другом.</span><span class="sxs-lookup"><span data-stu-id="15204-105">A SAP can be provided by more than one software feature to operate in conjunction with one another.</span></span> <span data-ttu-id="15204-106">Кроме того, программная функция может предоставлять более одного SAP.</span><span class="sxs-lookup"><span data-stu-id="15204-106">Additionally, a software feature can provide more than one SAP.</span></span> <span data-ttu-id="15204-107">Если многие функции программного обеспечения связаны с одним SAP, предполагается, что элементы работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="15204-107">When many software features are associated with a single SAP, it is assumed that the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="15204-108">При наличии различных реализаций SAP каждая реализация будет создавать отдельные экземпляры объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="15204-108">If different implementations of a SAP exist, each implementation would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="15204-109">После этого отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="15204-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15204-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="15204-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15204-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15204-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="15204-112">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="15204-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="15204-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="15204-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15204-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15204-114">Syntax</span></span>

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="15204-115">Члены</span><span class="sxs-lookup"><span data-stu-id="15204-115">Members</span></span>

<span data-ttu-id="15204-116">Класс **CIM \_ софтварефеатуресапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="15204-116">The **CIM\_SoftwareFeatureSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="15204-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="15204-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15204-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="15204-118">Properties</span></span>

<span data-ttu-id="15204-119">Класс **CIM \_ софтварефеатуресапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15204-119">The **CIM\_SoftwareFeatureSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15204-120">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="15204-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15204-121">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="15204-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="15204-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15204-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15204-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="15204-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="15204-124">[**\_ Софтварефеатуре CIM**](cim-softwarefeature.md) , описывающий функцию предшествующего программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="15204-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="15204-125">**Него**</span><span class="sxs-lookup"><span data-stu-id="15204-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15204-126">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="15204-126">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="15204-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="15204-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15204-128">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="15204-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="15204-129">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий зависимую точку доступа службы.</span><span class="sxs-lookup"><span data-stu-id="15204-129">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the dependent service access point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15204-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15204-130">Remarks</span></span>

<span data-ttu-id="15204-131">Класс **CIM \_ софтварефеатуресапимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="15204-131">The **CIM\_SoftwareFeatureSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="15204-132">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="15204-132">WMI does not implement this class.</span></span>

<span data-ttu-id="15204-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="15204-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15204-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="15204-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15204-135">Требования</span><span class="sxs-lookup"><span data-stu-id="15204-135">Requirements</span></span>



| <span data-ttu-id="15204-136">Требование</span><span class="sxs-lookup"><span data-stu-id="15204-136">Requirement</span></span> | <span data-ttu-id="15204-137">Значение</span><span class="sxs-lookup"><span data-stu-id="15204-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15204-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15204-138">Minimum supported client</span></span><br/> | <span data-ttu-id="15204-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15204-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15204-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15204-140">Minimum supported server</span></span><br/> | <span data-ttu-id="15204-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15204-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15204-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="15204-142">Namespace</span></span><br/>                | <span data-ttu-id="15204-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="15204-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15204-144">MOF</span><span class="sxs-lookup"><span data-stu-id="15204-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15204-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15204-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15204-146">DLL</span><span class="sxs-lookup"><span data-stu-id="15204-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15204-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15204-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15204-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="15204-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15204-149">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="15204-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

