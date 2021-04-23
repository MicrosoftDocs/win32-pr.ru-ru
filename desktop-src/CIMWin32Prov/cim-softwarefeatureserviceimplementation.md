---
description: Класс CIM \_ софтварефеатуресервицеимплементатион представляет ассоциацию между службой и ее реализацией в программном обеспечении.
ms.assetid: fa80cc91-8dd7-4726-a24a-5c4dfa3e786b
ms.tgt_platform: multiple
title: Класс CIM_SoftwareFeatureServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureServiceImplementation
- CIM_SoftwareFeatureServiceImplementation.Dependent
- CIM_SoftwareFeatureServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dc521de933a4567c0760495880baf9251a774938
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104140995"
---
# <a name="cim_softwarefeatureserviceimplementation-class"></a><span data-ttu-id="eb87e-103">\_Класс CIM софтварефеатуресервицеимплементатион</span><span class="sxs-lookup"><span data-stu-id="eb87e-103">CIM\_SoftwareFeatureServiceImplementation class</span></span>

<span data-ttu-id="eb87e-104">Класс **CIM \_ софтварефеатуресервицеимплементатион** представляет ассоциацию между службой и ее реализацией в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="eb87e-104">The **CIM\_SoftwareFeatureServiceImplementation** class represents an association between a service and how it is implemented in software.</span></span> <span data-ttu-id="eb87e-105">Служба может предоставляться более чем одним программным обеспечением, работающими совместно друг с другом.</span><span class="sxs-lookup"><span data-stu-id="eb87e-105">A service can be provided by more than one software feature, operating in conjunction with one another.</span></span> <span data-ttu-id="eb87e-106">Кроме того, компонент программного обеспечения может предоставлять более одной службы.</span><span class="sxs-lookup"><span data-stu-id="eb87e-106">Additionally, a software feature can provide more than one service.</span></span> <span data-ttu-id="eb87e-107">Если несколько функций программного обеспечения связаны с одной службой, предполагается, что элементы работают совместно, чтобы предоставить службу.</span><span class="sxs-lookup"><span data-stu-id="eb87e-107">When multiple software features are associated with a single service, it is assumed that the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="eb87e-108">При наличии различных реализаций службы каждая реализация будет создавать отдельные экземпляры объекта службы.</span><span class="sxs-lookup"><span data-stu-id="eb87e-108">If different implementations of a service exist, each implementation would result in individual instantiations of the service object.</span></span> <span data-ttu-id="eb87e-109">После этого отдельные экземпляры будут иметь связи с уникальными реализациями.</span><span class="sxs-lookup"><span data-stu-id="eb87e-109">Individual instantiations would then have associations to the unique implementations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eb87e-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="eb87e-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="eb87e-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="eb87e-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="eb87e-112">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="eb87e-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="eb87e-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="eb87e-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb87e-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eb87e-114">Syntax</span></span>

``` syntax
[UUID("{8AC984F4-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureServiceImplementation : CIM_Dependency
{
  CIM_Service         REF Dependent;
  CIM_SoftwareFeature REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="eb87e-115">Члены</span><span class="sxs-lookup"><span data-stu-id="eb87e-115">Members</span></span>

<span data-ttu-id="eb87e-116">Класс **CIM \_ софтварефеатуресервицеимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eb87e-116">The **CIM\_SoftwareFeatureServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="eb87e-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb87e-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eb87e-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="eb87e-118">Properties</span></span>

<span data-ttu-id="eb87e-119">Класс **CIM \_ софтварефеатуресервицеимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eb87e-119">The **CIM\_SoftwareFeatureServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eb87e-120">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="eb87e-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb87e-121">Тип данных: **CIM \_ софтварефеатуре**</span><span class="sxs-lookup"><span data-stu-id="eb87e-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="eb87e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb87e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb87e-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="eb87e-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="eb87e-124">[**\_ Софтварефеатуре CIM**](cim-softwarefeature.md) , описывающий функцию предшествующего программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="eb87e-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) that describes the antecedent software feature.</span></span>

</dd> <dt>

<span data-ttu-id="eb87e-125">**Него**</span><span class="sxs-lookup"><span data-stu-id="eb87e-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eb87e-126">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="eb87e-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="eb87e-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eb87e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="eb87e-128">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="eb87e-128">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="eb87e-129">[**\_ Служба CIM**](cim-service.md) , которая описывает зависимую службу.</span><span class="sxs-lookup"><span data-stu-id="eb87e-129">A [**CIM\_Service**](cim-service.md) that describes the dependent service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eb87e-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb87e-130">Remarks</span></span>

<span data-ttu-id="eb87e-131">Класс **CIM \_ софтварефеатуресервицеимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="eb87e-131">The **CIM\_SoftwareFeatureServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="eb87e-132">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="eb87e-132">WMI does not implement this class.</span></span>

<span data-ttu-id="eb87e-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="eb87e-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="eb87e-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb87e-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb87e-135">Требования</span><span class="sxs-lookup"><span data-stu-id="eb87e-135">Requirements</span></span>



| <span data-ttu-id="eb87e-136">Требование</span><span class="sxs-lookup"><span data-stu-id="eb87e-136">Requirement</span></span> | <span data-ttu-id="eb87e-137">Значение</span><span class="sxs-lookup"><span data-stu-id="eb87e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb87e-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eb87e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="eb87e-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb87e-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb87e-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eb87e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="eb87e-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb87e-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb87e-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eb87e-142">Namespace</span></span><br/>                | <span data-ttu-id="eb87e-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="eb87e-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb87e-144">MOF</span><span class="sxs-lookup"><span data-stu-id="eb87e-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb87e-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb87e-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb87e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="eb87e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb87e-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb87e-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb87e-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb87e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb87e-149">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="eb87e-149">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

