---
description: Класс CIM \_ девицесервицеимплементатион представляет ассоциацию между службой и ее реализацией.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: Класс CIM_DeviceServiceImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990664"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="36d6f-103">\_Класс CIM девицесервицеимплементатион</span><span class="sxs-lookup"><span data-stu-id="36d6f-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="36d6f-104">Класс **CIM \_ девицесервицеимплементатион** представляет ассоциацию между службой и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="36d6f-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="36d6f-105">Если несколько устройств связаны с одной службой, эти элементы работают совместно, чтобы предоставить службу.</span><span class="sxs-lookup"><span data-stu-id="36d6f-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="36d6f-106">При наличии различных реализаций службы каждая реализация приводит к отдельным экземплярам объекта службы.</span><span class="sxs-lookup"><span data-stu-id="36d6f-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="36d6f-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="36d6f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="36d6f-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="36d6f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="36d6f-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="36d6f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="36d6f-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="36d6f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d6f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36d6f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="36d6f-112">Члены</span><span class="sxs-lookup"><span data-stu-id="36d6f-112">Members</span></span>

<span data-ttu-id="36d6f-113">Класс **CIM \_ девицесервицеимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="36d6f-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="36d6f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="36d6f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36d6f-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="36d6f-115">Properties</span></span>

<span data-ttu-id="36d6f-116">Класс **CIM \_ девицесервицеимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="36d6f-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="36d6f-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="36d6f-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d6f-118">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="36d6f-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="36d6f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36d6f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d6f-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="36d6f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="36d6f-121">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="36d6f-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="36d6f-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="36d6f-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="36d6f-123">Тип данных: **\_ Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="36d6f-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="36d6f-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="36d6f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="36d6f-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="36d6f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="36d6f-126">[**\_ Служба CIM**](cim-service.md) , которая описывает службу, реализованную с помощью логического устройства.</span><span class="sxs-lookup"><span data-stu-id="36d6f-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36d6f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36d6f-127">Remarks</span></span>

<span data-ttu-id="36d6f-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="36d6f-128">WMI does not implement this class.</span></span>

<span data-ttu-id="36d6f-129">Класс **CIM \_ девицесервицеимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="36d6f-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="36d6f-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="36d6f-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="36d6f-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="36d6f-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d6f-132">Требования</span><span class="sxs-lookup"><span data-stu-id="36d6f-132">Requirements</span></span>



| <span data-ttu-id="36d6f-133">Требование</span><span class="sxs-lookup"><span data-stu-id="36d6f-133">Requirement</span></span> | <span data-ttu-id="36d6f-134">Значение</span><span class="sxs-lookup"><span data-stu-id="36d6f-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36d6f-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36d6f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="36d6f-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36d6f-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="36d6f-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36d6f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="36d6f-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36d6f-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="36d6f-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36d6f-139">Namespace</span></span><br/>                | <span data-ttu-id="36d6f-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="36d6f-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="36d6f-141">MOF</span><span class="sxs-lookup"><span data-stu-id="36d6f-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36d6f-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36d6f-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="36d6f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="36d6f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d6f-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d6f-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36d6f-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36d6f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d6f-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="36d6f-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

