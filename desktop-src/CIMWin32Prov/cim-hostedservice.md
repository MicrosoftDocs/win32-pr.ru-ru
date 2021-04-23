---
description: Класс CIM \_ HostedService представляет ассоциацию между службой и системой, в которой находятся функциональные возможности.
ms.assetid: 23bb385d-dd22-4126-aea9-d2f22527223e
ms.tgt_platform: multiple
title: Класс CIM_HostedService (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedService
- CIM_HostedService.Dependent
- CIM_HostedService.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c63b28fed7977c9fce78fe1030afbe66d5b2d75e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655909"
---
# <a name="cim_hostedservice-class-cimwin32-wmi-providers"></a><span data-ttu-id="dbe11-103">Класс CIM_HostedService (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="dbe11-103">CIM_HostedService class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="dbe11-104">Класс **CIM \_ HostedService** представляет ассоциацию между службой и системой, в которой находятся функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="dbe11-104">The **CIM\_HostedService** class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="dbe11-105">В системе может быть размещено множество служб, которые откладываются на систему размещения.</span><span class="sxs-lookup"><span data-stu-id="dbe11-105">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="dbe11-106">Модель не представляет службы, размещенные в нескольких системах.</span><span class="sxs-lookup"><span data-stu-id="dbe11-106">The model does not represent services hosted across multiple systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dbe11-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="dbe11-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dbe11-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dbe11-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dbe11-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe11-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dbe11-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dbe11-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe11-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbe11-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{83B2A7AA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedService : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_System  REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="dbe11-112">Члены</span><span class="sxs-lookup"><span data-stu-id="dbe11-112">Members</span></span>

<span data-ttu-id="dbe11-113">Класс **CIM \_ HostedService** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dbe11-113">The **CIM\_HostedService** class has these types of members:</span></span>

-   [<span data-ttu-id="dbe11-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbe11-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dbe11-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="dbe11-115">Properties</span></span>

<span data-ttu-id="dbe11-116">Класс **CIM \_ HostedService** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="dbe11-116">The **CIM\_HostedService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dbe11-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="dbe11-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe11-118">Тип данных: **\_ система CIM**</span><span class="sxs-lookup"><span data-stu-id="dbe11-118">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="dbe11-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbe11-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbe11-120">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="dbe11-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="dbe11-121">[**\_ Система CIM**](cim-system.md) , которая описывает систему размещения.</span><span class="sxs-lookup"><span data-stu-id="dbe11-121">A [**CIM\_System**](cim-system.md) that describes the hosting system.</span></span>

</dd> <dt>

<span data-ttu-id="dbe11-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="dbe11-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dbe11-123">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="dbe11-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="dbe11-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dbe11-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dbe11-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="dbe11-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="dbe11-126">[**\_ Служба CIM**](cim-service.md) , которая описывает службу, размещенную в системе.</span><span class="sxs-lookup"><span data-stu-id="dbe11-126">A [**CIM\_Service**](cim-service.md) that describes the service hosted on the system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dbe11-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbe11-127">Remarks</span></span>

<span data-ttu-id="dbe11-128">**Модель CIM \_ HostedService** является производной [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="dbe11-128">**CIM\_HostedService** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="dbe11-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="dbe11-129">WMI does not implement this class.</span></span>

<span data-ttu-id="dbe11-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="dbe11-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dbe11-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="dbe11-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe11-132">Требования</span><span class="sxs-lookup"><span data-stu-id="dbe11-132">Requirements</span></span>



| <span data-ttu-id="dbe11-133">Требование</span><span class="sxs-lookup"><span data-stu-id="dbe11-133">Requirement</span></span> | <span data-ttu-id="dbe11-134">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe11-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe11-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbe11-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe11-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dbe11-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dbe11-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbe11-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe11-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dbe11-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dbe11-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbe11-139">Namespace</span></span><br/>                | <span data-ttu-id="dbe11-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="dbe11-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dbe11-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dbe11-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbe11-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dbe11-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbe11-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe11-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe11-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbe11-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe11-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbe11-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe11-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="dbe11-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

